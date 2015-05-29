---
layout: post
title: data-binding
description: data binding
platform: js
control: Menu
documentation: ug
---

# Data binding

Data binding enables you to synchronize the elements with different sources of data. You can bind data using two ways, Local data and remote data. 

**Field Members**

Field is a property that includes the object type. Fields are used to bind the data source and it includes following field members to make binding easier.

_Table_ _1__: List of Field members_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dataSource</td><td>
datasource receives  Essential DataManager object and JSON object. </td></tr>
<tr>
<td>
Query</td><td>
It receives query to retrieve data from the table (query is same as SQL). Example:  ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);</td></tr>
<tr>
<td>
tableName</td><td>
It receives table name to execute query on the corresponding table</td></tr>
<tr>
<td>
Id</td><td>
Specifies the id to menu items list</td></tr>
<tr>
<td>
parentId</td><td>
Specifies the parent id of the table.</td></tr>
<tr>
<td>
Text</td><td>
Specifies the text of menu items list</td></tr>
<tr>
<td>
spriteCssClass</td><td>
Specifies the sprite CSS class to “li” item list</td></tr>
<tr>
<td>
linkAttribute</td><td>
Specifies the link attribute to “a” tag in item list</td></tr>
<tr>
<td>
imageAttribute</td><td>
Specifies the image attribute to “img” tag inside items list </td></tr>
<tr>
<td>
htmlAttribute</td><td>
Specifies the html attributes to “li” item list</td></tr>
<tr>
<td>
imageUrl</td><td>
Specifies the image URL to “img” tag inside item list. </td></tr>
</table>
**Local data**

To define the local data to the **Menu** control, map the user-defined **JSON** data names with its appropriate dataSource column names.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]       </b>&lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="menujson"&gt;&lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]</b><b>// In JavaScript, you can initialize the Menu control.</b><br>&lt;script type="text/javascript"&gt;    var data = [        { id: 1, text: "Group A", parentId: null },        { id: 2, text: "Group B", parentId: null },        { id: 3, text: "Group C", parentId: null },        { id: 4, text: "Group D", parentId: null },        { id: 5, text: "Group E", parentId: null },        //first level child        { id: 11, parentId: 1, text: "Algeria" },        { id: 12, parentId: 1, text: "Armenia" },        { id: 13, parentId: 1, text: "Bangladesh" },        { id: 14, parentId: 1, text: "Cuba" },        { id: 15, parentId: 2, text: "Denmark" },        { id: 16, parentId: 2, text: "Egypt" },        { id: 17, parentId: 3, text: "Finland" },        { id: 18, parentId: 3, text: "India" },        { id: 19, parentId: 3, text: "Malaysia" },        { id: 20, parentId: 4, text: "New Zealand" },        { id: 21, parentId: 4, text: "Norway" },        { id: 22, parentId: 4, text: "Poland" },        { id: 23, parentId: 5, text: "Romania" },        { id: 24, parentId: 5, text: "Singapore" },        { id: 25, parentId: 5, text: "Thailand" },        { id: 26, parentId: 5, text: "Ukraine" },        //second level child        { id: 111, parentId: 11, text: "First Place" },        { id: 112, parentId: 12, text: "Second Place" },        { id: 113, parentId: 13, text: "Third place" },        { id: 114, parentId: 14, text: "Fourth Place" },        { id: 115, parentId: 15, text: "First Place" },        { id: 116, parentId: 16, text: "Second Place" },        { id: 117, parentId: 17, text: "Third Place" },        { id: 118, parentId: 18, text: "First Place" },        { id: 119, parentId: 19, text: "Second Place" },        { id: 120, parentId: 20, text: "First Place" },        { id: 121, parentId: 21, text: "Second Place" },        { id: 122, parentId: 22, text: "Third place" },        { id: 123, parentId: 23, text: "Fourth Place" },        { id: 120, parentId: 24, text: "First Place" },        { id: 121, parentId: 25, text: "Second Place" },        { id: 122, parentId: 26, text: "Third place" }    ];    jQuery(function ($) {        $("#menujson").ejMenu({            fields: { dataSource: data, id: "id", parentId: "parentId", text: "text " }        });    });&lt;/script&gt;  </td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]       </b><b>// Add the following code in your CSHTML page.</b>@Html.EJ().Menu("menujson").MenuFields(f => f.Datasource((IEnumerable<Check.Controllers.CheckController.MenuJson>)ViewBag.datasource).Id("pid").Text("mtext").ParentId("parent"))</td></tr>
<tr>
<td>
<b>[CS]</b>using System;using System.Collections.Generic;using System.Linq;using System.Web;using System.Web.Mvc;namespace Check.Controllers{    public class CheckController : Controller    {        public class MenuJson        {            public string mtext { get; set; }            public int pid { get; set; }            public string parent { get; set; }        }        List<MenuJson> menu = new List<MenuJson>();        public ActionResult DataBindingJson()        {            menu.Add(new MenuJson { pid = 1, mtext = "Group A", parent = null });            menu.Add(new MenuJson { pid = 2, mtext = "Group B", parent = null });            menu.Add(new MenuJson { pid = 3, mtext = "Group C", parent = null });            menu.Add(new MenuJson { pid = 4, mtext = "Group D", parent = null });            menu.Add(new MenuJson { pid = 5, mtext = "Group E", parent = null });            menu.Add(new MenuJson { pid = 11, parent = "1", mtext = "Algeria" });            menu.Add(new MenuJson { pid = 12, parent = "1", mtext = "Armenia" });            menu.Add(new MenuJson { pid = 13, parent = "1", mtext = "Bangladesh" });            menu.Add(new MenuJson { pid = 14, parent = "1", mtext = "Cuba" });            menu.Add(new MenuJson { pid = 15, parent = "2", mtext = "Denmark" });            menu.Add(new MenuJson { pid = 16, parent = "2", mtext = "Egypt" });            menu.Add(new MenuJson { pid = 17, parent = "3", mtext = "Finland" });            menu.Add(new MenuJson { pid = 18, parent = "3", mtext = "India" });            menu.Add(new MenuJson { pid = 19, parent = "3", mtext = "Malaysia" });            menu.Add(new MenuJson { pid = 20, parent = "4", mtext = "New Zealand" });            menu.Add(new MenuJson { pid = 21, parent = "4", mtext = "Norway" });            menu.Add(new MenuJson { pid = 22, parent = "4", mtext = "Romania" });            menu.Add(new MenuJson { pid = 23, parent = "5", mtext = "Singapore" });            menu.Add(new MenuJson { pid = 24, parent = "5", mtext = "Thailand" });            menu.Add(new MenuJson { pid = 25, parent = "5", mtext = "Ukraine" });            menu.Add(new MenuJson { pid = 26, parent = "11", mtext = "First Place" });            menu.Add(new MenuJson { pid = 27, parent = "12", mtext = "Second Place" });            menu.Add(new MenuJson { pid = 28, parent = "13", mtext = "Third place" });            menu.Add(new MenuJson { pid = 29, parent = "14", mtext = "Fourth Place" });            menu.Add(new MenuJson { pid = 30, parent = "15", mtext = "First Place" });            menu.Add(new MenuJson { pid = 31, parent = "16", mtext = "Second Place" });            menu.Add(new MenuJson { pid = 32, parent = "17", mtext = "Third Place" });            menu.Add(new MenuJson { pid = 33, parent = "18", mtext = "First Place" });            menu.Add(new MenuJson { pid = 34, parent = "19", mtext = "Second Place" });            menu.Add(new MenuJson { pid = 35, parent = "20", mtext = "First Place" });            menu.Add(new MenuJson { pid = 36, parent = "21", mtext = "Second Place" });            menu.Add(new MenuJson { pid = 37, parent = "22", mtext = "Third place" });            menu.Add(new MenuJson { pid = 38, parent = "23", mtext = "Fourth Place" });            menu.Add(new MenuJson { pid = 39, parent = "24", mtext = "First Place" });            menu.Add(new MenuJson { pid = 40, parent = "25", mtext = "Second Place" });            ViewBag.datasource = menu;            return View();        }    }}</td></tr>
</table>


The following screenshot displays the output of the above code.

![](data-binding_images\data-binding_img1.png)

_Figure_ _18__8__: Local data of Menu_

**Remote data**

The **Menu** control also provides support for Remote data binding. Here the remote data is placed in Web service and you can render the menu items from the web service using Service **URL**. The data is in **JSON** format. 

DataManager is used to manage relational data in **JavaScript**. DataManager uses two different classes, **ej.DataManager** for processing, and **ej.Query** for serving data. **ej.DataManager** communicates with data source and **ej.Query** generates data queries that are to be read by DataManager. To know more about DataManager and Query refer the following link location.

[http://help.syncfusion.com/ug/js/default.htm#!Documents/createyourdatamanage.htm](http://help.syncfusion.com/ug/js/default.htm)

In the following example, [http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)is used as the **URL**. This acts as web service that is located in the **Syncfusion** server. The webservice with the name Northwnd.svc is used here.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="content-container-fluid"&gt;    &lt;div class="row"&gt;        &lt;div class="cols-sample-area"&gt;            &lt;ul id="shipDetails"&gt;&lt;/ul&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Javascript]   </b><b>// Initialize the Menu control in JavaScript.</b>&lt;script type="text/javascript"&gt;    $(function () {        // DataManager creation        var dataManger = ej.DataManager({            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"        });        var query = null, query1 = null;        var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);        $("#shipDetails").ejMenu({            fields: {                dataSource: dataManger, query: query, id: "CategoryID", text: "CategoryName",                child: { dataSource: dataManger, tableName: "Products", id: "ProductID", parentId: "CategoryID", text: "ProductName" }            }        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code in your CSHTML page.**

@Html.EJ().Menu("shipDetails").MenuFields(f => f.Datasource(d => d.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).Query("ej.Query().from('Categories').select('CategoryID,CategoryName').take(3)").Id("CategoryID").Text("CategoryName").Child(c => c.Datasource(cd => cd.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).TableName("Products").Id("ProductID").ParentId("CategoryID").Text("ProductName")))



<table>
<tr>
<td>
<b>[ASPX]</b>// Add the code in ASPX page &lt;ul id="shipDetails"&gt;&lt;/ul&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the code in script section &lt;script type="text/javascript"&gt;        $(function () {            // DataManager creation            var dataManger = ej.DataManager({                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"            });            var query = null, query1 = null;            var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);            $("#shipDetails").ejMenu({                fields: {                    dataSource: dataManger, query: query, id: "CategoryID", text: "CategoryName",                    child: { dataSource: dataManger, tableName: "Products", id: "ProductID", parentId: "CategoryID", text: "ProductName" }                }            });        });    &lt;/script&gt;</td></tr>
</table>


The following screenshot displays the output of the above code. 

![](data-binding_images\data-binding_img2.png)

_Figure_ _19__9__:  Remote data of Menu_

**SQL Data binding**

SqlDataSource is designed to work with SQL Server databases. It uses the SQL **Server .NET** data provider internally. SQL Server .NET data provider classes are defined in the **System.Data.SqlClient** namespace. To bind the SqlDataSource to Menu, DataSourceID should be the id of **SqlDataSource**. You can select the table from **SelectCommand.** 

* Add the following code in your **ASPX** page to **SQL** Databinding.



[ASPX]



<ej:Menu ID="TreeSQL" DataTextField="Text" DataSourceID="SqlDataSource1" DataIdField="ID"

        DataParentIdField="ParentID" runat="server">

&lt;/ej:Menu&gt;

&lt;div&gt;

        &lt;asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="&lt;%$ ConnectionStrings:TreeDBConnectionString %&gt;"

            SelectCommand="SELECT * FROM [TreeBind]">&lt;/asp:SqlDataSource&gt;

&lt;/div&gt;



The following screen shot displays the output for the above code.                                                                                                       

{% include image.html url="\js\Menu\concepts-and-features\data-binding_images\data-binding_img3.png" Caption="Figure 20: SQL Databinding"%}

**Object Data binding**

The objectdatasource control lets you bind a specific data layer in the same manner by that you bind to the database using other controls. The objectdatasource control can bind to any method that returns a DataSet or an IEnumerable object (for example, a DataReader or a collection of Classes). The major advantage of binding via objectdatasource is, only records that are required in the current view are retrieved from the database, greatly optimizing the performance and runtime memory usage.

* Add the following code in your ASPX page



[ASPX]



&lt;ej:Menu ID="Menu1" DataSourceID="ObjectDataSource2" DataIdField="ID" DataParentIdField="ParentID" DataTextField="Text" runat="server"&gt;

    &lt;/ej:Menu&gt;

    <asp:ObjectDataSource ID="ObjectDataSource2" runat="server" TypeName="MenuLocalDataSource"

        SelectMethod="GetMenuDataItems">&lt;/asp:ObjectDataSource&gt;





Define Object DataSource elements using the ID,parentID and Text fields in code behind and map the list data to DataSource property.



[CodeBehind-C#]



public class MenuSource

    {

    }

    [Serializable]

    public class MenuLocalDataSource

    {

        //private int? ParentID;

        public MenuLocalDataSource()

        { }

        public MenuLocalDataSource(int _id, int? _parentid, string _text, string _hasChild, string _expanded)

        {



            this.ID = _id;

            this.ParentID = _parentid;

            this.Text = _text;

            this.HasChild = _hasChild;

            this.Expanded = _expanded;

        }

        [Browsable(true)]

        public int ID

        {

            get;

            set;

        }



        [Browsable(true)]

        public int? ParentID

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

        [Browsable(true)]

        public string HasChild

        {

            get;

            set;

        }

        [Browsable(true)]

        public string Expanded

        {

            get;

            set;

        }

        public List<MenuLocalDataSource> GetMenuDataItems()

        {

            List<MenuLocalDataSource> data = new List<MenuLocalDataSource>();



            data.Add(new MenuLocalDataSource(1, null, "Discover Music", "true", "true"));

            data.Add(new MenuLocalDataSource(2, 1, "Hot Singles", "", ""));

            data.Add(new MenuLocalDataSource(3, 1, "Rising Artists", "", ""));

            data.Add(new MenuLocalDataSource(4, 1, "Live Music", "", ""));

            data.Add(new MenuLocalDataSource(6, 1, "Best of 2013 So Far", "", ""));

            data.Add(new MenuLocalDataSource(7, null, "Sales and Events", "true", "true"));

            data.Add(new MenuLocalDataSource(8, 7, "100 Albums - $5 Each", "", ""));

            data.Add(new MenuLocalDataSource(9, 7, "Hip-Hop and R&B Sale", "", ""));

            data.Add(new MenuLocalDataSource(10, 7, "CD Deals", "", ""));

            data.Add(new MenuLocalDataSource(11, null, "Categories", "true", ""));

            data.Add(new MenuLocalDataSource(12, 11, "Songs", "", ""));

            data.Add(new MenuLocalDataSource(13, 11, "Bestselling Albums", "", ""));

            data.Add(new MenuLocalDataSource(14, 11, "New Releases", "", ""));

            data.Add(new MenuLocalDataSource(15, 11, "Bestselling Songs", "", ""));

            data.Add(new MenuLocalDataSource(16, null, "MP3 Albums", "true", ""));

            data.Add(new MenuLocalDataSource(17, 16, "Rock", "", ""));

            data.Add(new MenuLocalDataSource(18, 16, "Gospel", "", ""));

            data.Add(new MenuLocalDataSource(19, 16, "Latin Music", "", ""));

            data.Add(new MenuLocalDataSource(20, 16, "Jazz", "", ""));

            data.Add(new MenuLocalDataSource(21, null, "More in Music", "true", ""));

            data.Add(new MenuLocalDataSource(22, 21, "Music Trade-In", "", ""));

            data.Add(new MenuLocalDataSource(23, 21, "Redeem a Gift Card", "", ""));

            data.Add(new MenuLocalDataSource(24, 21, "Band T-Shirts", "", ""));

            data.Add(new MenuLocalDataSource(25, 21, "Mobile MVC", "", ""));



            return data;

        }

    }



The following screen shot displays the output for the above code.                                                                                                    

{% include image.html url="\js\Menu\concepts-and-features\data-binding_images\data-binding_img4.png" Caption="Figure 21: Object Databinding"%}

**XML Data binding**

**Xmldatasource** is used to work with XML documents. To bind the **XmlDataSource** to Menu, D**ataSourceID** of the menu should be the id of **XmlDataSource**.

* In the Design page, assign the values for DataTextField, DataParentIdField.In **DataSourceID** field assign the ID of the existing XML datasource



[ASPX]



&lt;ej:Menu ID="TreeXmlDSr" runat="server" DataSourceID="XmlDataSource1" DataTextField="Item" DataParentIdField="RootItem"&gt;&lt;/ej:Menu&gt;

    &lt;div&gt;

        &lt;asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~\App_Data\XMLData.xml"&gt;&lt;/asp:XmlDataSource&gt;

    &lt;/div&gt;



Load the menu items in the xml data as follows.



[XMLData.xml]



&lt;?xml version="1.0" encoding="utf-8" ?&gt;

&lt;Items&gt;

  &lt;RootItem Text="Home" Expanded="True" Url="#"&gt;

    &lt;Item Text="Foundation" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Launch" Url="#"&gt;&lt;/Item&gt;

    &lt;RootItem Text="About" Url="#"&gt;

      &lt;Item Text="Company" Url="#"&gt;&lt;/Item&gt;

      &lt;Item Text="Location" Url="#"&gt;&lt;/Item&gt;

    &lt;/RootItem&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Services" Expanded="True" Url="#"&gt;

    &lt;Item Text="Consulting" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Outsourcing" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="About" Url="#"&gt;&lt;/RootItem&gt;

  &lt;RootItem Text="Contact us" Url="#"&gt;

    &lt;Item Text="Contact Number" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Email" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Career" Url="#"&gt;

    &lt;RootItem Text="Position" Url="#"&gt;

      &lt;Item Text="Developer" Url="#"&gt;&lt;/Item&gt;

      &lt;Item Text="Manager" Url="#"&gt;&lt;/Item&gt;

    &lt;/RootItem&gt;

    &lt;Item Text="Apply online" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

&lt;/Items&gt;



The following screen shot displays the output for the XML Databinding.                                                                                                       

{% include image.html url="\js\Menu\concepts-and-features\data-binding_images\data-binding_img5.png" Caption="Figure 22: XML Databinding"%}

**Linq-to-SQL Data binding**

The linq datasource is used to bind Menu data via Linq to Sql. The property **ContextTypeName** indicates the location of the data source. Mention exact table name of your data base in **TableName** property. Provide the id of LinqDataSource to **DataSourceID** of Menu. Define a Linq-to-SQL data source in the web page and configure the data source as per requirement using the database.

* In the Design page, assign values for DataTextField, DataIdField, DataParentIdField. In **DataSourceID** field assign the ID of the existing Linq-to-SQL data source. 


[ASPX]



<ej:Menu ID="TreeSQL" DataTextField="Text" DataSourceID="linq" DataIdField="ID"

        DataParentIdField="ParentID" runat="server">

    &lt;/ej:Menu&gt;

    &lt;asp:LinqDataSource ID="linq" runat="server" ContextTypeName="WebSampleBrowser.Menu.MenuLinqSQLDataContext" EntityTypeName="" TableName="TreeBinds"&gt;&lt;/asp:LinqDataSource&gt;




The following screen shot displays the output for the above code.                                                                                                       

{% include image.html url="\js\Menu\concepts-and-features\data-binding_images\data-binding_img6.png" Caption="Figure 23: Linq-to-Sql Data"%}

