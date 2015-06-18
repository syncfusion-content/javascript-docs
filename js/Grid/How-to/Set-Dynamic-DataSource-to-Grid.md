---
layout: post
title: Set-Dynamic-DataSource-to-Grid
description: set dynamic datasource to grid
platform: js
control: Grid
documentation: ug
---

### Set Dynamic DataSource to Grid

**Grid** control is capable of updating its dataSource as and when required. **Grid** method “dataSource” helps in achieving this and in this method parameter, you have to pass the new dataSource as json array.

For instance, consider a textbox above **Grid** and depending on its value, you can update a new datasource to Grid dynamically.

{% highlight html %}


Enter EmployeeID Field Value:
<input type="text" id="colValue" />
<input type="button" id="customButton" value="Change DataSource">

<div id="Grid"></div>

<script type="text/javascript">
    $(function () {

           // the datasource "window.gridData" is referred from jsondata.min.js
           $("#Grid").ejGrid({
               dataSource: window.gridData,
               allowPaging: true,
               allowSorting: true,
               columns: [
                       { field: "OrderID", headerText: "Order ID", width: 75 , textAlign: ej.TextAlign.Right },
                       { field: "CustomerID", headerText: "Customer ID", width: 80 },
                       { field: "EmployeeID", headerText: "Employee ID", width: 75, textAlign: ej.TextAlign.Right },
                       { field: "Freight", width: 75, format: "{0:C}", textAlign: ej.TextAlign.Right },
                       { field: "OrderDate", headerText: "Order Date", width: 80, format: "{0:MM/dd/yyyy}", textAlign: ej.TextAlign.Right },
                       { field: "ShipCity", headerText: "Ship City", width: 110 }
               ]
           });

          $("#customButton").ejButton({
            size: "Normal", click: function (args) {//updating dataSource in an external button click event
                var obj = $("#Grid").ejGrid("instance");
                var value = $("#colValue").val();
                //Add custom paramter to the server
                var query = new ej.Query().where("EmployeeID",ej.FilterOperators.equal, value);

                //Creating ejDataManager with UrlAdaptor

                var dm = ej.DataManager(window.gridData);

                var data = dm.executeLocal(query);
                    //Assign the result to the grid dataSource using "dataSource" method.
                    obj.dataSource(data)

            }
        })

       });

</script>


{% endhighlight %}



The following screenshot illustrates the output.

{% include image.html url="/js/Grid/How-to/Set-Dynamic-DataSource-to-Grid_images/Set-Dynamic-DataSource-to-Grid_img1.png" Caption="Dynamic DataSource in Grid"%}

