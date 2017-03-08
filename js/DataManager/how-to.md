---
layout: post
title: How-to
description: How-to
platform: js
control: DataManager
documentation: ug
keywords: WebService, ESRI Rest Web Services, WCF-RESTful Service
---

# How To

## How I can call and bind to a WebService.asmx

Create a sample using ASP.NET Web Services

{% highlight html %}

    public class WebService1 : System.Web.Services.WebService
    {
        static string cons = ConfigurationManager.ConnectionStrings["SQLConnectionString"].ConnectionString;
        static SqlConnection con = new SqlConnection(cons);

        [WebMethod]
        public DataTable Get()
        {
            SqlCommand getData = new SqlCommand();
            getData.CommandText = "usp_DEV_ChangeLog_Select"; // Stored procedure for retrieve data from suppliers table
            getData.CommandType = CommandType.StoredProcedure;
            getData.Connection = con;
            if (con.State != ConnectionState.Open)
                con.Open();
            DataTable sqldata = new DataTable();
            SqlDataAdapter sqladapter = new SqlDataAdapter(getData);
            sqldata.TableName = "Suppliers";
            sqladapter.Fill(sqldata);
            return sqldata;
        }
    }

{% endhighlight %}

In the above code snippet, we have created webservices by using the ASP.NET web service and bound dataSource to Grid, in code behind GetDataSource method.

{% highlight html %}

    [WebMethod]
    [ScriptMethod(ResponseFormat = ResponseFormat.Json)] // Return the JSON formatted result
    public static object GetDataSource()
    {
        CRUD_Service.WebService1 service = new CRUD_Service.WebService1();
        var sqldata = service.Get();   // Get data from webservices
        DataResult result = new DataResult();
        List<EditableCustomer> data = (from ord in sqldata.AsEnumerable() // Perform skip take for on demand load paging
                                        select new EditableCustomer
                                        {
                                            SupplierID = ord.ItemArray[0].ToString(),
                                            CompanyName = ord.ItemArray[1].ToString(),
                                            City = ord.ItemArray[5].ToString(),
                                            PostalCode = ord.ItemArray[7].ToString(),
                                            Country = ord.ItemArray[8].ToString()
                                        }).ToList();

        con.Close();
        return data;
    }

{% endhighlight %}

{% highlight javascript %}

    var dataManager = ej.DataManager({

                url: "Default.aspx/GetDataSource",
                offline: true, 
                adaptor: "UrlAdaptor"

            });

{% endhighlight %}

## How do I control communication errors with the web service?

We can handle the error or any exception using fail event of ejDataManager during the post back. The fail method gets invoked when there is any error while making the request or an exception. 
Please refer to the below code example.

{% highlight html %}

    <script type="text/javascript">

        var dataManager = ej.DataManager({
            url: "/WebService.asmx/Get",
            adaptor: new ej.UrlAdaptor(), //"UrlAdaptor",
            crossDomain: false,
            offline: false
        });
        var data = [];
        var query = ej.Query();
        query.addParams("userName", "EB_HMACIAS");
        var promise = dataManager.executeQuery(query);
        promise.done(function (e) {
            data = e.result.result;
            window.employeeView = {
                dataSource: ko.observableArray(data),
                selectedRow: ko.observable(1),
                currentPage: ko.observable(2),
                actionBegin: ko.observable(function (args) {
                    if (args.requestType == "grouping")
                        $("#selectedRow").ejNumericTextbox("option", { value: -1 });
                })
            };
            ko.applyBindings(employeeView);
        });

        promise.fail(function (e) {
            alert(e.error.statusText);
        });
    </script>

{% endhighlight %}

## How-to use DataManager consume WCF-RESTful with and without parameter?

We have created a simple Grid sample which is loaded with the data from the WCF RESTful service using DataManager.

In the above sample, we have created two Grids and a WCF RESTful service with two method “GetDataWithParam” and “GetDataWithOutParam”.  Those methods are implemented from the interface IOrder.

{% highlight html %}

    //The method GetDataWithOutParam will be invoked when the URI is as defined in the UriTemplate as follow.

    [OperationContract]

    [WebGet(UriTemplate = "Orders",ResponseFormat = WebMessageFormat.Json)] //Call the method without parameter

    string GetDataWithOutParam();

 
    //The method GetDataWithParam will be invoked when a request is made without parameter.

    [OperationContract]

    [WebInvoke(Method = "POST", UriTemplate = "Orders", RequestFormat = WebMessageFormat.Json,

    ResponseFormat = WebMessageFormat.Json, BodyStyle = WebMessageBodyStyle.WrappedRequest)] //Call the method with parameter

    string GetDataWithParam(int take,int skip);

{% endhighlight %}

To request the web service without parameter using DataManager, please refer the following code snippet. In the below code snippet, request will be made to the web service using executeQuery method.

{% highlight html %}

    var data1 = ej.DataManager({ url: "/Order.svc/Orders" });

                var query = new ej.Query();
                var dm = data1.executeQuery(query); //Request the webservice
                dm.done(function (e) {

                    $("#Grid").ejGrid({
                        dataSource: e.result
                    });

                });

{% endhighlight %}

To request the WCF service with parameter, please refer the following code snippet. we have used the ej.Query() to add parameters and configured the DataManager using the UrlAdaptor and hence POST request will be send to the WCF RESTful Service with parameter skip and take.

{% highlight html %}

    var data2 = ej.DataManager({ url: "/Order.svc/Orders" });

            data2.adaptor = new ej.UrlAdaptor();

            var query1 = new ej.Query().skip(5).take(30); //Adding parameter to be send to the webservice

            var dm1 = data2.executeQuery(query1) //Request the webservice

            dm1.done(function (e) {

                $("#Grid1").ejGrid({
                    dataSource: e.result
                });

            });

{% endhighlight %}

Now the request will have made to the webservice with parameter value skip as 5 and take as 30.

For getting started with WCF OData service please refer [link](http://msdn.microsoft.com/en-us/data/odata.aspx).

## Can I use ESRI Rest Web Services in url of DataManager?

Yes, you can use ESRI Rest web services in url of DataManager. We have used a demo service from the site in our DataManager and prepared a sample with custom DataAdaptor in Datamanager. 
Refer to the following link for the sample: 

Playground sample : [Demo](http://jsplayground.syncfusion.com/jr2cgadj)


