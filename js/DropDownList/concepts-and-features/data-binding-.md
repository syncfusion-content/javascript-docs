---
layout: post
title: data-binding-
description: data-binding 
platform: js
control: DropDownList
documentation: ug
---

# Data-binding 

**Data fields and configuration** 

The following sub-properties provides you a way to bind either the local or remote data to the **Dropdown** control.

_Table_ _1__:_ _Properties_ _of JavaScript_ _and MVC_

<table>
<tr>
<td>
<b>Properties</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dataSource</td><td>
The data source contains the list of data for generating the <b>DropDownList</b> items.</td></tr>
<tr>
<td>
query</td><td>
It specifies the query to retrieve the data from the online server.</td></tr>
<tr>
<td>
fields</td><td>
It specifies the mapping fields for the data items of the <b>DropDownList</b> textbox.</td></tr>
<tr>
<td>
id</td><td>
It specifies the ID of the tag.</td></tr>
<tr>
<td>
text</td><td>
It specifies the text content of the tag.</td></tr>
<tr>
<td>
value</td><td>
It specifies the value of the tag.</td></tr>
<tr>
<td>
category</td><td>
It is used to categorize the items and is used when the grouping is enabled.</td></tr>
<tr>
<td>
imageUrl</td><td>
It defines the <b>imageURL</b> for the image location.</td></tr>
<tr>
<td>
imageAttributes</td><td>
It defines the image attributes such as height, width, styles, etc.</td></tr>
<tr>
<td>
spriteCssClass</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
htmlAttributes</td><td>
It defines the HTML attributes such as class and styles for an item.</td></tr>
<tr>
<td>
selected</td><td>
This field defines the tag value to be selected initially. Corresponding field mapped has boolean values to select the list items on control creation. The data with value <b>true</b> in this field is selected automatically when the control is initialized.</td></tr>
<tr>
<td>
tableName</td><td>
It defines the table name for the tag value or displays text while rendering remote data.</td></tr>
</table>


_Table_ _2__:_ _Properties of ASP.NET_

<table>
<tr>
<td>
<i><b>Properties</b></i></td><td>
<i><b>Description</b></i></td><td>
<i><b>Default value</b></i></td><td>
<i><b>Data type</b></i></td></tr>
<tr>
<td>
<i>DataSource</i></td><td>
<i>The data source contains the list of data for generating the </i><i><b>DropDownList</b></i><i> items.</i></td><td>
<i>Null</i></td><td>
<i>object</i></td></tr>
<tr>
<td>
<i>Query</i></td><td>
<i>It specifies the query to retrieve the data from the online server.</i></td><td>
<i>Null</i></td><td>
<i>object</i></td></tr>
<tr>
<td>
<i>ID</i></td><td>
<i>It specifies the ID of the tag.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>Text</i></td><td>
<i>It specifies the text content of the tag.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>Value</i></td><td>
<i>It specifies the value of the tag.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>Category</i></td><td>
<i>Used to categorize the items. It is used when the grouping is enabled.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataIdField</i></td><td>
<i>It specifies the ID of the data.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataSourceID</i></td><td>
<i>Specifies the ID of the </i><i><b>DataSource</b></i><i>.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataMember</i></td><td>
<i>Specifies the member in a data source to bind to the </i><i><b>data list</b></i><i> control.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataTextField</i></td><td>
<i>It specifies the name of the column value that binds the </i><i><b>DropDownList</b></i><i> text.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataValueField</i></td><td>
<i>It specifies the ID of the value.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataImageUrlField</i></td><td>
<i>It defines the </i><i><b>imageURL</b></i><i> for the image location.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataImageAttributesField</i></td><td>
<i>It defines the image attributes such as height, width, styles, etc.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataSpriteCssField</i></td><td>
<i>It defines the sprite CSS for the image tag.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataHtmlAttributesField</i></td><td>
<i>It defines the html attributes such as ID, class, styles for the item.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataSelectedField</i></td><td>
<i>This field defines the tag value to be selected initially. Corresponding field that is mapped has boolean values to select the list items on control creation. The data with value </i><i><b>true</b></i><i> in this field is selected automatically when the control is initialized.</i></td><td>
<i>Null</i></td><td>
<i>String</i></td></tr>
<tr>
<td>
<i>DataTableNameField</i></td><td>
<i>It defines the table name for tag value or displays text while rendering remote data.</i><i> </i></td><td>
<i>Null</i></td><td>
<i>object</i></td></tr>
</table>
_**Local data**_

**Dropdown** provides data binding support for **DropdownList**. Thus you can bind the data from **JSON** Data. To achieve this, you need to map the corresponding file with their column names

And also you need to provide support to add and customize the images and list item by using appropriate data fields. 

The following steps explains you the details of data binding with **DropdownList**. 

1. In an **HTML** page, add a **&lt;input&gt;** element to configure **Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]</b>   &lt;div class="control"&gt;        <div class="ctrllabel">Select a bike</div>        &lt;input type="text" id="dropdownlist" /&gt;   &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>    &lt;script type="text/javascript"&gt;               $(function () {            // declaration            BikeList = [                 { id: "bk1", text: "Aache RTR" }, { id: "bk2", text: "CBR 150-R" }, { id: "bk3", text: "CBZ Xtreme" },                 { id: "bk4", text: "Discover" }, { id: "bk5", text: "Dazzler" }, { id: "bk6", text: "Flame" },                 { id: "bk7", text: "Fazzer" }, { id: "bk8", text: "FZ-S" }, { id: "bk9", text: "Pulsar" },                 { id: "bk10", text: "Shine" }, { id: "bk11", text: "R15" }, { id: "bk12", text: "Unicorn" }            ];            $('#dropdownlist').ejDropDownList({                dataSource: BikeList,            fields: { id: "id", text: "text", value: "text" }        });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>// Add a DropDownList element using the helper class in CSHTML&lt;div class="control"&gt;        <div class="ctrllabel">Select a bike</div>        @Html.EJ().DropDownList("dropdownlist").Datasource((IEnumerable<Data>)ViewData["BikeList"] ).DropDownListFields(f => f.Text("Text")).DropDownListFields(f => f.Value("Id")).Width("150px")                                    &lt;/div&gt;</td></tr>
<tr>
<td>
[CS]// Initialize Datasource in the controller        public ActionResult DropdownlistFeatures()        {                    List<Data> ListOrder = new List<Data>();            ListOrder.Add(new Data() { Id = "bk1", Text = "Aache RTR" });            ListOrder.Add(new Data() { Id = "bk2", Text = "CBR 150-R" });            ListOrder.Add(new Data() { Id = "bk3", Text = "CBZ Xtreme" });            ListOrder.Add(new Data() { Id = "bk4", Text = "Discover" });            ListOrder.Add(new Data() { Id = "bk5", Text = "Dazzler" });            ListOrder.Add(new Data() { Id = "bk6", Text = "Flame" });            ListOrder.Add(new Data() { Id = "bk7", Text = "Fazzer" });            ListOrder.Add(new Data() { Id = "bk8", Text = "FZ-S" });            ListOrder.Add(new Data() { Id = "bk9", Text = "Pulsar" });            ListOrder.Add(new Data() { Id = "bk10", Text = "Shine" });            ListOrder.Add(new Data() { Id = "bk11", Text = "R15" });            ListOrder.Add(new Data() { Id = "bk12", Text = "Unicorn" });            ViewData["BikeList"] = ListOrder;            return View();       }       public class Data       {            public string Id { get; set; }            public string Text { get; set; }       }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// Add Dropdown list widget in ASPX page&lt;ej:DropDownList ID="dropdownlist" Width="200px"  runat="server" DataIdField="Id" DataTextField="Text"&gt;     &lt;/ej:DropDownList&gt;</td></tr>
<tr>
<td>
[C#]// Create list to bind data in Dropdown list  protected void Page_Load(object sender, EventArgs e)        {            List<vehicle> vehiclelist = new List<vehicle>();            vehiclelist.Add(new vehicle() { Id = "1", Text = "Railways" });            vehiclelist.Add(new vehicle() { Id = "2", Text = "Roadways" });            vehiclelist.Add(new vehicle() { Id = "3", Text = "Airways" });            vehiclelist.Add(new vehicle() { Id = "4", Text = "Waterways" });            vehiclelist.Add(new vehicle() { Id = "5", Text = "Electric Trains" });            dropdownlist.DataSource = vehiclelist;        }        public class vehicle        {            public string Text { get; set; }            public string Id { get; set; }                 }</td></tr>
</table>


Output of the above steps



![C:\Users\ApoorvahR\Desktop\1.png](data-binding-_images\data-binding-_img1.png)

_Figure_ _30__10__: Dropdown with Data binding -local_ 

**SQLDataSource**

SqlDataSource is designed to work with SQL Server databases. It uses internally, the **SQL Server .NET** data provider. SQL Server .NET data provider classes are defined in the **System.Data.SqlClient** namespace. 

    The following steps explains you the details about the data binding from **SQLDataSource**. 

* In the **ASPX** page, add Dropdown list widget



**[ASPX]**



  &lt;ej:DropDownList ID="dropdownlist" runat="server" DataTextField="text" DataValueField="id" DataSourceID="SqlDataSource1"&gt;&lt;/ej:DropDownList&gt;

           <asp:SqlDataSource ID="SqlDataSource1" runat="server" SelectCommand="SELECT [id], [text] FROM [Vehicle]"

        ConnectionString='&lt;%$ ConnectionStrings:DatabindingConnectionString %&gt;'>&lt;/asp:SqlDataSource&gt;





* Create a data table in .mdf format with the following structure and add it in APP_Data folder 



{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img2.png" Caption="Figure 31: Structure of Vehicle table"%}

* Add connectionstring in Web.config file.

![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img3.png)_**Note: Please change the username with your system name in below connection string**_



[WEB.CONFIG]



  &lt;configuration&gt;

  &lt;connectionStrings&gt;

    <add name="DatabindingConnectionString" connectionString="Data Source=SYNCLAPN4732;Initial Catalog=Databinding;Integrated Security=True"

      providerName="System.Data.SqlClient" />

  &lt;/connectionStrings&gt;

&lt;/configuration&gt;





Output of the above steps



{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img4.png" Caption="Figure 32: Dropdown with Data binding -SQL"%}

**LINQDataSource**

LinqDataSource is designed to work with DataContext. It uses internally, the data model (dbml) file. Data model contains list of tables from specific database. 

The following steps explains you the details about the data binding from **LinqDataSource**. 

* In the **ASPX** page, add Dropdown list widget



**[ASPX]**



&lt;ej:DropDownList ID="dropdownlist" Width="200px" DataTextField="text" DataValueField="id" DataSourceID="LinqDataSource1" runat="server"&gt;&lt;/ej:DropDownList&gt;



&lt;asp:LinqDataSource ID="LinqDataSource1" runat="server" ContextTypeName="dropdownlist.Database.common_datamodelDataContext" TableName="Vehicles" EntityTypeName=""&gt;&lt;/asp:LinqDataSource&gt;





* Create a table in .mdf format using the following table structure, create a dbml file in APP_DATA folder and drag and drop table into it. 



{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img5.png" Caption="Figure 33: Structure of Vehicle table"%}

* Add connection String in Web.config file.



![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img6.png)_**Note: Please change the username with your system name in below connection string.**_



**[WEB.CONFIG]**



  &lt;configuration&gt;

  &lt;connectionStrings&gt;

    <add name="DatabindingConnectionString" connectionString="Data Source=SYNCLAPN4732;Initial Catalog=Databinding;Integrated Security=True"

      providerName="System.Data.SqlClient" />

  &lt;/connectionStrings&gt;

&lt;/configuration&gt;





Output of the above steps



{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img7.png" Caption="Figure 34: Dropdown with Data binding –Linq to SQL"%}

**ObjectDataSource**

The ObjectDataSource control allows you to bind a specific data layer, in a similar manner to that the other controls bind to the database. The ObjectDataSource control can bind to any method that returns a DataSet or an IEnumerable object (for example, a DataReader or a collection of Classes). The major advantage of binding via ObjectDataSource is, only the records that are required in the current view are retrieved from the database, greatly optimizing the performance and runtime memory usage. 

The following steps explains you the details about the data binding from **ObjectDataSource**.

* In the **ASPX** page, add Dropdown list widget 



**[ASPX]**



  &lt;ej:DropDownList ID="dropdownlist" Width="200px" DataTextField="Text" DataValueField="ID" DataSourceID="ObjectDataSource1" runat="server"&gt;&lt;/ej:DropDownList&gt;

           <asp:ObjectDataSource ID="ObjectDataSource1" runat="server" TypeName="TabData"

        SelectMethod="GetTabItems">&lt;/asp:ObjectDataSource&gt;





* Create new CS file in App_Data folder and name as ‘Data.cs’ and add the following codes in the page. 



[C#]

  [Serializable]

public class TabData

{



    public TabData(int _id,string _text)

    {

        this.ID = _id;

        this.Text = _text;

    }

    public TabData()

    {



    }



    [Browsable(true)]

    public int ID

    {

        get;

        set;

    }



    [Browsable(true)]

    public string Text

    {

        get;

        set;

    }





    public List<TabData> GetTabItems()

    {

        List<TabData> data = new List<TabData>();

        data.Add(new TabData(1, "Railways"));

        data.Add(new TabData(2, "Roadways"));

        data.Add(new TabData(3, "Airways"));

        data.Add(new TabData(4, "Waterways"));

        data.Add(new TabData(5, "Electric Trains"));

        data.Add(new TabData(6, "Diesel Trains"));

        data.Add(new TabData(7, "Heavy Motor Vehicles"));

        data.Add(new TabData(8, "Light Motor Vehicles"));

        data.Add(new TabData(9, "Aeroplanes"));

        data.Add(new TabData(10,"Helicopters"));

        data.Add(new TabData(11,"Ships"));

        data.Add(new TabData(12,"Submarines"));



        return data;

    }

}





Output of the above steps

{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img8.png" Caption="Figure 35: Dropdown with Data binding -Object"%}

**XMLDataSource**

XmlDataSource is used to work with XML documents. The following steps explains you the details about the data binding from **XmlDataSource**.

* In the **ASPX** page, add Dropdown list widget



**[ASPX]**



 &lt;ej:DropDownList ID="dropdownlist" runat="server" Width="200px" DataValueField="Id" DataTextField="Text" DataSourceID="XmlDataSource1" DataMember="Items"&gt;&lt;/ej:DropDownList&gt;

          &lt;asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~/App_Data/XMLData.xml"&gt;&lt;/asp:XmlDataSource&gt;                                           



* Create new xml file in App_Data folder as ‘XMLData.xml’ and add the following codes in the page. 



#XMLData.xml

&lt;Items&gt;

 &lt;Item Id="1" Text=" Railways"&gt;

  &lt;/Item&gt;

  &lt;Item Id="2" Text="Roadways"&gt;

  &lt;/Item&gt;

  &lt;Item Id="3" Text="Airways"&gt;

  &lt;/Item&gt;

  &lt;Item Id="4" Text="Waterways"&gt;

  &lt;/Item&gt;

 &lt;Item Id="5" Text="Electric Trains"&gt;

 &lt;/Item&gt;

&lt;/Items&gt;



Output of the above steps



{% include image.html url="\js\DropDownList\concepts-and-features\data-binding-_images\data-binding-_img9.png" Caption="Figure 36: Dropdown with Data binding -Xml"%}

**Remote data** 

You can bind the data’s for the **DropdownList** from remote, that can fetch the data from any other server that is located as remote web service. By using **query** options, you can pass the query string to filter the data that helps to avoid the extensive properties look up. 

The following steps explains you the details of data binding from remote. 

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
<b>[HTML]</b><div class="ctrllabel">Select a customer</div>    &lt;input type="text" id="dropdownlist" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;              $(function () {            // DataManager creation            var dataManger = ej.DataManager({                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"            });            // Query creation            var query = ej.Query()                   .from("Customers").take(6);             $('#dropdownlist'$('#dropdownlist’).ejDropDownList({                dataSource: dataManger,                fields: { text: "CustomerID" },                query: query,            });        });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

// Add a DropDownList element using the helper class in CSHTML



<div class="ctrllabel">Select a customer</div>

   @Html.EJ().DropDownList("dropdownlist").Datasource(ds=>ds.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).**Query**("ej.Query().from('Customers').take(6)").DropDownListFields(f => f.Text("CustomerID")).Width("150px")                      



**[ASPX]**

// Add Dropdown list widget in ASPX page

<div class="ctrllabel">Select a Customer</div>

     &lt;ej:DropDownList ID="dropdownlist" runat="server" DataTextField="CustomerID" &gt;

        &lt;/ej:DropDownList&gt;

[C#]

// Initialize the control in CS page

  protected void Page_Load(object sender, EventArgs e)

        {

            this.dropdownlist.DataSource = "http://mvc.syncfusion.com/Services/Northwnd.svc/";

            this.dropdownlist.Query = "ej.Query().from('Customers').take(6)";        

        }



Output of the above steps



![C:\Users\ApoorvahR\Desktop\2.png](data-binding-_images\data-binding-_img10.png)

_Figure_ _37__11__: Dropdown with Data binding -Remote_ 

**Angular Binding** 

**DropdownList** widget contains two types of angular **JS** support namely, 

* One way binding

* Two way binding 

One way binding refers to the process of applying scope values to all the available properties of the **Dropdown list** widget, but the changes made in **DropdownList****Dropdown list** widget does not reflect or trigger in turn to the scope collection. This kind of binding applies to all the properties of the **DropdownList****Dropdown list** widget.

Two-way binding supports both the processes – it applies the scope values to the **Dropdown list** properties as well as the changes made in the **DropdownList****Dropdown list** widget is also reflected back and triggered within the angular scope change function.

To know more detail about the Angular binding, you can refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

The following example depicts the way to bind data to the **DropdownList****Dropdown list** widget through angular support



> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img11.png) _**Note: You need to include “ej.widget.angular.min.js” file library to achieve this behaviour and you need to pass the control properties as data attribute in input tag itself as like data role behaviour.**_



* In the **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;!doctype html&gt;&lt;html xmlns="http://www.w3.org/1999/xhtml" ng-app="DropCtrl"&gt;&lt;head&gt;    <title>Essential Studio for JavaScript :  Angular</title>    &lt;!-- style sheet for default theme(flat azure) --&gt;    &lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;    &lt;!--scripts--&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"&gt;&lt;/script&gt;&lt;/head&gt;&lt;body ng-controller="DropDownCtrl"&gt;    &lt;div class="content-container-fluid"&gt;        &lt;div class="row"&gt;            &lt;div class="cols-sample-area"&gt;                &lt;div class="frame" style="width: 50%; height: 27px"&gt;                    <span>Select a section</span>                    &lt;div&gt;                        &lt;div id="control" style="float: left; width: 45%"&gt;                            &lt;input id="dropdownlist" ej-dropdownlist e-datasource="dataList" e-value="value" /&gt;                            &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                        &lt;/div&gt;                    &lt;/div&gt;                    &lt;div id="binding" style="float: right; margin: auto; width: 45%"&gt;                        &lt;input type="text" id="dropValue" class="input ejinputtext" ng-model="value" /&gt;                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;body ng-controller="DropDownCtrl"&gt;    &lt;div class="content-container-fluid"&gt;        &lt;div class="row"&gt;            &lt;div class="cols-sample-area"&gt;                &lt;div class="frame" style="width: 50%; height: 27px"&gt;                    <span>Select a section</span>                    &lt;div&gt;                        &lt;div id="control" style="float: left; width: 45%"&gt;                            &lt;input id="dropdownlist" ej-dropdownlist e-datasource="dataList" e-value="value" /&gt;                            &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                        &lt;/div&gt;                    &lt;/div&gt;                    &lt;div id="binding" style="float: right; margin: auto; width: 45%"&gt;                        &lt;input type="text" id="dropValue" class="input ejinputtext" ng-model="value" /&gt;                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;    &lt;/body&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;// Initialize the control and bind the data in <b>JavaScript</b>       var list = [                   { id: "cr1", text: "Dodge Avenger" },                   { id: "cr2", text: "Chrysler 200" },                   { id: "cr3", text: "Ford Focus" },                   { id: "cr4", text: "Ford Taurus", },                   { id: "cr5", text: "Dazzler", },                   { id: "cr6", text: "Chevy Spark", },                   { id: "cr7", text: "Chevy Volt", },                   { id: "cr8", text: "Honda Fit", },                   { id: "cr9", text: "Honda Crosstour", },                   { id: "cr10", text: "Acura RL", },                   { id: "cr11", text: "Hyundai Elantra", },                   { id: "cr12", text: "Mazda3", }       ];       angular.module('DropCtrl', ['ejangular'])          .controller('DropDownCtrl', function ($scope) {              $scope.dataList = list;              $scope.value = "Ford Focus";          });    &lt;/script&gt;&lt;style type="text/css"&gt;        .control {            margin-top: 10px;        }        .input {            height: 27px;            text-indent: 10px;            width: 81%;        }    &lt;/style&gt;&lt;/body&gt;&lt;/html&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>&lt;div ng-app="DropCtrl"&gt; &lt;div ng-controller="DropDownCtrl"&gt;        &lt;div class="content-container-fluid"&gt;            &lt;div class="row"&gt;                &lt;div class="cols-sample-area"&gt;                    &lt;div class="frame" style="width: 50%; height: 27px"&gt;                        <span>Select a section</span>                        &lt;div&gt;                            &lt;div id="control" style="float: left; width: 45%"&gt;                                &lt;input id="dropdownlist" ej-dropdownlist e-datasource="dataList" e-value="value" /&gt;                                &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                            &lt;/div&gt;                        &lt;/div&gt;                        &lt;div idl="binding" style="float: right; margin: auto; width: 45%"&gt;                            &lt;input type="text" id="dropValue" class="input ejinputtext" ng-model="value" /&gt;                        &lt;/div&gt;                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JavaScript]&lt;script type="text/javascript"&gt;       var list = [                   { id: "cr1", text: "Dodge Avenger" },                   { id: "cr2", text: "Chrysler 200" },                   { id: "cr3", text: "Ford Focus" },                   { id: "cr4", text: "Ford Taurus", },                   { id: "cr5", text: "Dazzler", },                   { id: "cr6", text: "Chevy Spark", },                   { id: "cr7", text: "Chevy Volt", },                   { id: "cr8", text: "Honda Fit", },                   { id: "cr9", text: "Honda Crosstour", },                   { id: "cr10", text: "Acura RL", },                   { id: "cr11", text: "Hyundai Elantra", },                   { id: "cr12", text: "Mazda3", }       ];       angular.module('DropCtrl', ['ejangular'])          .controller('DropDownCtrl', function ($scope) {              $scope.dataList = list;              $scope.value = "Ford Focus";          });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// Add Dropdown list widget in ASPX page&lt;body ng-controller="DropDownCtrl"&gt;    &lt;div class="content-container-fluid"&gt;        &lt;div class="row"&gt;            &lt;div class="cols-sample-area"&gt;                &lt;div class="frame" style="width: 50%; height: 27px"&gt;                    <span>Select a section</span>                    &lt;div&gt;                        &lt;div id="control" style="float: left; width: 45%"&gt;                            &lt;input id="dropdownlist" ej-dropdownlist e-datasource="dataList" e-value="value" /&gt;                            &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                        &lt;/div&gt;                    &lt;/div&gt;                    &lt;div id="binding" style="float: right; margin: auto; width: 45%"&gt;                        &lt;input type="text" id="dropValue" class="input ejinputtext" ng-model="value" /&gt;                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;    &lt;/body&gt;</td></tr>
<tr>
<td>
[JavaScript]&lt;script type="text/javascript"&gt;       var list = [                   { Id: "cr1", Text: "Dodge Avenger" },                   { Id: "cr2", Text: "Chrysler 200" },                   { Id: "cr3", Text: "Ford Focus" },                   { Id: "cr4", Text: "Ford Taurus", },                   { Id: "cr5", Text: "Dazzler", },                   { Id: "cr6", Text: "Chevy Spark", },                   { Id: "cr7", Text: "Chevy Volt", },                   { Id: "cr8", Text: "Honda Fit", },                   { Id: "cr9", Text: "Honda Crosstour", },                   { Id: "cr10", Text: "Acura RL", },                   { Id: "cr11", Text: "Hyundai Elantra", },                   { Id: "cr12", Text: "Mazda3", }       ];       angular.module('DropCtrl', ['ejangular'])          .controller('DropDownCtrl', function ($scope) {              $scope.dataList = list;              $scope.value = "Ford Focus";          });    &lt;/script&gt;</td></tr>
</table>


Output of the above steps

![](data-binding-_images\data-binding-_img12.png)

_Figure_ _12__38__: Dropdown with Data binding -Angular_ 

**Knockout Binding**

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One-way binding

* Two-way binding

One way binding refers to the process of applying observable values to all the available properties of the **DropdownList****Dropdown List** widget, but the changes made in the widget does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the dropdown list widget.

Two-way binding supports both the processes – it applies the observable values to the **Dropdown List** widget properties as well as the changes made in the dropdown list widget is also reflected back and triggered within the observable collections. 

For more information about the knockout binding, refer the following online documentation in the following link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

The following example depicts the way to bind data to the **DropdownList****Dropdown List** widget through the knockout support that enables and populates data to a **DropdownList****Dropdown List** widget based on the value set to the other dropdown widget.


> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img13.png)_**Note: You need to include the “ej.widget.knockout.min.js” file library to achieve this behaviour and you need to pass the control properties as data attribute in input tag itself as like data role behaviour.**_

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget



<table>
<tr>
<td>
&lt;!DOCTYPE html&gt;&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;&lt;head&gt;    &lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"&gt;&lt;/script&gt;&lt;/head&gt;&lt;body&gt;    &lt;div class="control" style="float: left"&gt;        <div class="ctrllabel">Select a section</div>        &lt;input id="dropdownlist" data-bind="ejDropDownList: { dataSource: dataList, value: value }"&gt;    &lt;/div&gt;    &lt;div class="control" style="float: left; margin-left: 20px; height: 30px"&gt;        <div class="ctrllabel">Knockout textbox binding</div>        &lt;input type="text" id="Text4" class="input ejinputtext" data-bind="value: value" /&gt;    &lt;/div&gt;    &lt;script type="text/javascript"&gt;        // Initialize the control and bind the data in JavaScript        $(function () {            var carList = [                { id: "cr1", text: "Accordion" },                { id: "cr2", text: "Autocomplete" },                { id: "cr3", text: "Button" },                { id: "cr4", text: "Tab", },                { id: "cr5", text: "Menu", },                { id: "cr6", text: "Rating", },                { id: "cr7", text: "Slider", },                { id: "cr8", text: "Splitter", },                { id: "cr9", text: "Tagcloud", },                { id: "cr10", text: "Scroller", },                { id: "cr11", text: "TreeView", },                { id: "cr12", text: "WaitingPopup", }            ];            window.viewModel = {                dataList: ko.observable(carList),                value: ko.observable("Button"),            }            ko.applyBindings(viewModel);        });    &lt;/script&gt;    &lt;style type="text/css"&gt;        .ejinputtext {            background-color: #fff;            border: 1px solid #bbbcbb;            color: #5c5c5c;            height: 30px;            outline: medium none;        }    &lt;/style&gt;&lt;/body&gt;&lt;/html&gt;<b>[HTML]  </b> &lt;div class="control" style="float: left"&gt;        <div class="ctrllabel">Select a section</div>        &lt;input id="dropdownlist" data-bind="ejDropDownList: { dataSource: dataList, value: value }"&gt;    &lt;/div&gt;    &lt;div class="control" style="float: left; margin-left: 20px; height: 30px"&gt;        <div class="ctrllabel">Knockout textbox binding</div>        &lt;input type="text" id="Text4" class="input ejinputtext" data-bind="value: value" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            var carList = [                { id: "cr1", text: "Accordion" },                { id: "cr2", text: "Autocomplete" },                { id: "cr3", text: "Button" },                { id: "cr4", text: "Tab", },                { id: "cr5", text: "Menu", },                { id: "cr6", text: "Rating", },                { id: "cr7", text: "Slider", },                { id: "cr8", text: "Splitter", },                { id: "cr9", text: "Tagcloud", },                { id: "cr10", text: "Scroller", },                { id: "cr11", text: "TreeView", },                { id: "cr12", text: "WaitingPopup", }            ];            window.viewModel = {                dataList: ko.observable(carList),                value: ko.observable("Button"),            }            ko.applyBindings(viewModel);        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]  </b> &lt;div class="control" style="float: left"&gt;    <div class="ctrllabel">Select a section</div>    &lt;input id="dropdownlist" data-bind="ejDropDownList: { dataSource: dataList, value: value }"&gt;&lt;/div&gt;&lt;div class="control" style="float: left; margin-left: 20px; height: 30px"&gt;    <div class="ctrllabel">Knockout textbox binding</div>    &lt;input type="text" id="Text4" class="input ejinputtext" data-bind="value: value" /&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[JavaScript]&lt;script type="text/javascript"&gt;        $(function () {            var carList = [                { id: "cr1", text: "Accordion" },                { id: "cr2", text: "Autocomplete" },                { id: "cr3", text: "Button" },                { id: "cr4", text: "Tab", },                { id: "cr5", text: "Menu", },                { id: "cr6", text: "Rating", },                { id: "cr7", text: "Slider", },                { id: "cr8", text: "Splitter", },                { id: "cr9", text: "Tagcloud", },                { id: "cr10", text: "Scroller", },                { id: "cr11", text: "TreeView", },                { id: "cr12", text: "WaitingPopup", }            ];            window.viewModel = {                dataList: ko.observable(carList),                value: ko.observable("Button"),            }            ko.applyBindings(viewModel);        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]  </b>// Add Dropdown list widget in ASPX page &lt;div class="control" style="float: left"&gt;        <div class="ctrllabel">Select a section</div>        &lt;input id="dropdownlist" data-bind="ejDropDownList: { dataSource: dataList, value: value }"&gt;    &lt;/div&gt;    &lt;div class="control" style="float: left; margin-left: 20px; height: 30px"&gt;        <div class="ctrllabel">Knockout textbox binding</div>        &lt;input type="text" id="Text4" class="input ejinputtext" data-bind="value: value" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
[JavaScript]&lt;script type="text/javascript"&gt;        $(function () {            var CarList = [                { Id: "cr1", Text: "Accordion" },                { Id: "cr2", Text: "Autocomplete" },                { Id: "cr3", Text: "Button" },                { Id: "cr4", Text: "Tab", },                { Id: "cr5", Text: "Menu", },                { Id: "cr6", Text: "Rating", },                { Id: "cr7", Text: "Slider", },                { Id: "cr8", Text: "Splitter", },                { Id: "cr9", Text: "Tagcloud", },                { Id: "cr10", Text: "Scroller", },                { Id: "cr11", Text: "TreeView", },                { Id: "cr12", Text: "WaitingPopup", }            ];            window.viewModel = {                dataList: ko.observable(CarList),                value: ko.observable("Button"),            }            ko.applyBindings(viewModel);        });    &lt;/script&gt;</td></tr>
</table>


* Configure the styles 



**[CSS]** 



 &lt;style type="text/css"&gt;

        .ejinputtext {

            background-color: #fff;

            border: 1px solid #bbbcbb;

            color: #5c5c5c;

            height: 30px;

            outline: medium none;

        }

    &lt;/style&gt;



Output of the above steps



![](data-binding-_images\data-binding-_img14.png)

_Figure_ _39__13__: Dropdown with Data binding –Knockout_  

