---
layout: post
title: data-binding-
description: data-binding 
platform: js
control: ListBox
documentation: ug
---

# Data-binding 

The **ListBox** is populated with the node information taken from a data source. The **ListBox** supports binding data sources containing hierarchical data. and supports Object data, Remote data, XML Data, SQL Data and LinqToSql Data, for retrieving data from a specified data source.

**Data fields and configuration** 

The following sub-properties provides you a way to bind either the local or remote data to the **ListBox** control.

_Table_ _1__: Property Table_ _for JavaScript ListBox_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dataSource</td><td>
The data source contains the list of data for generating the ListBox items</td></tr>
<tr>
<td>
query</td><td>
It specifies the query to retrieve the data from online server</td></tr>
<tr>
<td>
fields</td><td>
It specifies the mapping fields for the data items of the ListBox</td></tr>
<tr>
<td>
id</td><td>
It specifies the id of the tag</td></tr>
<tr>
<td>
text</td><td>
It specifies the text content of the tag</td></tr>
<tr>
<td>
value</td><td>
It specifies the value of the tag</td></tr>
<tr>
<td>
imageUrl</td><td>
It’s defines the imageURL for the image location</td></tr>
<tr>
<td>
imageAttributes</td><td>
It’s defines the image attributes such as height, width, styles and so on</td></tr>
<tr>
<td>
spriteCssClass</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
htmlAttributes</td><td>
It defines the html attributes such as id, class, styles for the item</td></tr>
<tr>
<td>
selected</td><td>
It defines the tag value to be selected initially</td></tr>
<tr>
<td>
toolTipText  </td><td>
It specifies the Tooltip text  of the tag</td></tr>
<tr>
<td>
category</td><td>
It specifies the category of the tag</td></tr>
<tr>
<td>
tableName</td><td>
It defines the table name for tag value or display text while render with remote data</td></tr>
</table>
_Table_ _2__: Property Table for_ _ASP.NET MVC_ _ListBox_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Datasource</td><td>
The data source contains the list of data for generating the ListBox items</td></tr>
<tr>
<td>
Query</td><td>
It specifies the query to retrieve the data from online server</td></tr>
<tr>
<td>
ListBoxFields</td><td>
It specifies the mapping fields for the data items of the ListBox</td></tr>
<tr>
<td>
ID</td><td>
It specifies the id of the tag</td></tr>
<tr>
<td>
Text</td><td>
It specifies the text content of the tag</td></tr>
<tr>
<td>
Value</td><td>
It specifies the value of the tag</td></tr>
<tr>
<td>
ImageUrl</td><td>
It’s defines the imageURL for the image location</td></tr>
<tr>
<td>
ImageAttributes</td><td>
It’s defines the image attributes such as height, width, styles and so on</td></tr>
<tr>
<td>
SpriteCssClass</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
HtmlAttributes</td><td>
It defines the html attributes such as id, class, styles for the item</td></tr>
<tr>
<td>
Selected</td><td>
It defines the tag value to be selected initially</td></tr>
<tr>
<td>
ToolTipText</td><td>
It specifies the Tooltip text  of the tag</td></tr>
<tr>
<td>
Category</td><td>
It specifies the category of the tag</td></tr>
<tr>
<td>
TableName</td><td>
It defines the table name for tag value or display text while render with remote data</td></tr>
</table>
_Table_ _3__: Property Table for_ _ASP.NET_ _ListBox_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
DataSource</td><td>
The data source contains the list of data for generating the ListBox items</td></tr>
<tr>
<td>
Query</td><td>
It specifies the query to retrieve the data from online server</td></tr>
<tr>
<td>
DataIdField</td><td>
It specifies the id of the tag</td></tr>
<tr>
<td>
DataTextField </td><td>
It specifies the text content of the tag</td></tr>
<tr>
<td>
DataValueField</td><td>
It specifies the value of the tag</td></tr>
<tr>
<td>
DataImageUrlField</td><td>
It’s defines the imageURL for the image location</td></tr>
<tr>
<td>
DataImageAttributesField</td><td>
It’s defines the image attributes such as height, width, styles and so on</td></tr>
<tr>
<td>
DataSpriteCSSField</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
DataHtmlAttributesField </td><td>
It defines the html attributes such as id, class, styles for the item</td></tr>
<tr>
<td>
DataSelectedField  </td><td>
It defines the tag value to be selected initially</td></tr>
<tr>
<td>
ToolTipText</td><td>
It specifies the Tooltip text  of the tag</td></tr>
<tr>
<td>
DataTableNameField</td><td>
It defines the table name for tag value or display text while render with remote data</td></tr>
</table>
**Local data**

**ListBox** provides data binding support. Thus, you can bind the data from **JSON** Data source. To achieve this, map the corresponding fields with their column names.

And also, provide support to add and customize the list item by using appropriate data fields. 

The following steps explains you the details of data binding with **ListBox**. 

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", <b>dataSource: skillset,</b><b>            fields: { text: "skill" }</b>        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").<b>Datasource((IEnumerable<skillset>)ViewBag.datasource).ListBoxFields(df=>df.Text("text"))</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page<b>	</b>        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>




Output of the above steps



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img1.png" Caption="Figure 7: ListBox with local Data binding"%}

**Object Data**

**ListBox** provides **ObjectDataSource** data binding support to populate **ListBox**. Therefore, the values can be mapped to the **ListBox** fields from an existing **ObjectDataSource**, using **DataSourceID** property.

The following steps explain the **ObjectDataSource** data binding to **ListBox**.

* Define an **ObjectDataSource** in the web page and configure the data source elements. 




 **[CS]**

        protected void Page_Load(object sender, EventArgs e)

        {

**listboxsample.DataSource = GetData();**

        }

        private List<Languages> GetData()

        {

            List<Languages> data = new List<Languages>();

            data.Add(new Languages() { Name = "ASP.NET" });

            data.Add(new Languages() { Name = "ActionScript" });

            data.Add(new Languages() { Name = "Basic" });

            data.Add(new Languages() { Name = "C++" });

            data.Add(new Languages() { Name = "C#" });

            data.Add(new Languages() { Name = "dBase" });

            data.Add(new Languages() { Name = "Delphi" });

            data.Add(new Languages() { Name = "ESPOL" });

            data.Add(new Languages() { Name = "F#" });

            data.Add(new Languages() { Name = "FoxPro" });

            data.Add(new Languages() { Name = "Java" });

            data.Add(new Languages() { Name = "J#" });

            data.Add(new Languages() { Name = "Lisp" });

            data.Add(new Languages() { Name = "Logo" });

            data.Add(new Languages() { Name = "PHP" });

            return data;

        }





        public class Languages

        {

            public string Name;

        }



In the **Design** page, assign the values for **DataTextField,****DataValueField**. In **DataSourceID** field assign the ID of the existing **ObjectDataSource**.



**[ASPX]**

&lt;div id="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select a skill</div>

    &lt;ej:listbox id="listboxsample" runat="server" DataTextField="Name" DataValueField="Name"  width="240"&gt;&lt;/ej:listbox&gt;

&lt;/div&gt;





The following image is the output for **ListBox** control with **ObjectDataSource** data binding.



![](data-binding-_images\data-binding-_img2.png)

Figure 8: ListBox with local Data binding

**Remote data** 

You can bind the data for the **ListBox** from remote that can fetch the data from remote web service. You can pass the query string to filter the data that helps to avoid the extensive properties look up by using **query** options. 

The following steps explains you the details of data binding from remote. 

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // DataManager creation        var dataManger = ej.DataManager({            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"        });        // Query creation        var query = ej.Query()               .from("Customers").take(6);        $('#listboxSample').ejListBox({            <b>dataSource: dataManger,</b><b>            fields: { text: "CustomerID" },</b><b>            query: query,</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[View]**

// Add the following code in View page to configure ListBox widget

&lt;div class="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select a customer

    &lt;/div&gt;

    @Html.EJ().ListBox("listboxsample").**Datasource(ds => ds.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).Query("ej.Query().from('Customers').take(10)").ListBoxFields(f => f.Text("CustomerID"))**

&lt;/div&gt;





<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a customer</div>    &lt;ej:listbox id="listboxsample" DataTextField="CustomerID"  runat="server" width="240"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            <b>listboxsample.DataSource = "http://mvc.syncfusion.com/Services/Northwnd.svc/";</b><b>            listboxsample.Query = "ej.Query().from('Customers').take(14)";</b>        }</td></tr>
</table>


Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img3.png" Caption="Figure 98: ListBox with remote Data binding"%}

**SQL Data**

**ListBox** provides extensive data binding support to populate **ListBox** nodes. Therefore the values can be mapped to the **ListBox** fields from an existing SQL data source, using **DataSourceID** property.

The following steps explain **SQL** data binding to **ListBox**.

* Define an SQL data source in the web page and configure the data source as per your requirement. Use the following code example to create an SQL data table.

The following screenshot illustrates the sample database used.

{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img4.png" Caption="Figure 10: Database table structure"%}

In the **Design** page, assign the values for **DataTextField**, **DataValueField**. In **DataSourceID** field assign the ID of the existing SQL data source.



**[ASPX]**

&lt;div class="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select a Transport

    &lt;/div&gt;

    <ej:listbox id="DrpDwnsql" runat="server" DataTextField="text" DataValueField="id"

**DataSourceId="SqlDataSource1"**>

            &lt;/ej:listbox&gt;

&lt;/div&gt;

**&lt;asp:SqlDataSource ID="SqlDataSource1" runat="server" SelectCommand="SELECT * FROM [Vehicle]"  ConnectionString='&lt;%$ ConnectionStrings:Linq_To_SQLConnectionString %&gt;' ProviderName='&lt;%$ ConnectionStrings:Linq_To_SQLConnectionString.ProviderName %&gt;'>**

**&lt;/asp:SqlDataSource&gt;**





The following image is the output for **ListBox** control with **SQL** data binding.



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img5.png" Caption="Figure 11: ListBox with SQL Data binding"%}

**LinqToSQL Data**

**ListBox** provides data binding support. Thus, you can bind the data from **LinqToSQL** Data source. To achieve this, map the corresponding fields with their column names.

And also, provide support to add and customize the list item by using appropriate data fields. 

The following steps explains you the details of data binding with **ListBox**. 

* Define a Linq-to-SQL data source in the web page and configure the data source as per your requirement using the database. In the following code example, an SQL table is used to create a DBML class.

The following illustrates the sample database used.



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img6.jpeg" Caption="Figure 12: Database table structure"%}

In the **Design** page, assign values for **DataTextField**, **DataValueField**. In **DataSourceID** field assign the ID of the existing Linq-to-SQL data source.


**[ASPX]**

&lt;div class="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select an Album</div>

    <ej:listbox id="DrpDwnsql" runat="server" DataTextField="Text" DataValueField="Id"

        **DataSourceId="LinqDataSource1"**>

            &lt;/ej:listbox&gt;

&lt;/div&gt;

**<asp:LinqDataSource ID="LinqDataSource1" runat="server" ContextTypeName="WebSampleBrowser.database.Linq_Common_DataDataContext"**

    **EntityTypeName="" TableName="Databindings">&lt;/asp:LinqDataSource&gt;**





Output of the above steps



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img7.png" Caption="Figure 13: ListBox with LinqToSQL Data binding"%}

**XML Data**

**ListBox** provides XML data binding support to populate **ListBox** content. Therefore, the values can be mapped to the ListBox fields from an existing XML data, using DataSourceID property.

The following steps explain the XML data binding to **ListBox**.

* In the Design page, assign the values for **DataTextField**, **DataValueField**. In DataSourceID field assign the ID of the existing XML datasource. 



**[ASPX]**

&lt;div class="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select a Product</div>

    &lt;ej:listbox id="DrpDwnxml" datamember="RootItem" DataTextField="Text" DataValueField="Text" runat="server" DataSourceId="XmlDataSource1" &gt; &lt;/ej:listbox&gt;

&lt;/div&gt;

**&lt;asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~/App_Data/ListBoxXml.xml"&gt;**

**&lt;/asp:XmlDataSource&gt;**





Load the **ListBox** - xml data as follows.



**[XML]**

&lt;?xml version="1.0" encoding="utf-8" ?&gt;

&lt;items&gt;

  &lt;RootItem Text="Essential Grid Web" Expanded="True" Url="#"&gt;

    &lt;Item Text="Binary Price : $595.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $995.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Essential Tools Web" Expanded="True" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Essential Chart Web" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Essential Diagram Web" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Essential Tools MVC" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Grid MVC" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Chart MVC" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Diagram MVC" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Tools JS" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Grid JS" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Chart JS" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

  &lt;RootItem Text="Essential Diagram JS" Url="#"&gt;

    &lt;Item Text="Binary Price : $495.00" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Source Price : $895.00" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



&lt;/items&gt;





The following image is the output for **ListBox** control with **XML** data binding. 



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img8.png" Caption="Figure 14: ListBox with XML Data binding"%}

**Angular binding** 

**ListBox** widget contains two types of angular **JS** support namely, 

* One way binding

* Two way binding 

One way binding refers to the process of applying scope values to all the available properties of the **ListBox** widget, but the changes made in **ListBox** widget does not reflect or trigger in turn to the scope collection. This kind of binding applies to all the properties of the **ListBox** widget.

Two-way binding supports both the processes – it applies the scope values to the **ListBox** properties as well as the changes made in the **ListBox** widget is also reflected back and triggered within the angular scope change function.

To know more detail about the Angular binding, you can refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

The following example depicts the way to bind data to the **ListBox** widget through angular support.

> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img9.png) _**Note: You can include the “ej.widget.angular.min.js” file library to achieve this behaviour and you can pass the control properties as data attribute in ul tag itself as like data role behaviour.**_



* In the **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.



<table>
<tr>
<td>
<b>[HTML]</b> &lt;!doctype html&gt;&lt;html xmlns="http://www.w3.org/1999/xhtml" ng-app="ListCtrl"&gt;&lt;head&gt;    <title>Essential Studio for JavaScript :  Angular</title>    &lt;!-- style sheet for default theme(flat azure) --&gt;    &lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;    &lt;!--scripts--&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"&gt;&lt;/script&gt;&lt;/head&gt;&lt;body ng-controller="ListBoxCtrl"&gt;    &lt;div id="control" style="height: 300px;"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    <div class="ctrllabel">Select a section</div>                    &lt;ul id="bookselect" ej-listbox e-datasource="dataList" e-value="value"&gt;&lt;/ul&gt;                &lt;/td&gt;                &lt;td id="binding"&gt;                    &lt;div&gt;                        &lt;input type="text" id="dropvalue" class="input ejinputtext" ng-model="value" /&gt;                        &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                    &lt;/div&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;    &lt;script type="text/javascript"&gt;<b>// </b>Initialize the control and bind the data in <b>JavaScript</b>        var list = [                    { empid: "cr1", text: "Dodge Avenger" },                    { empid: "cr2", text: "Chrysler 200" },                    { empid: "cr3", text: "Ford Focus" },                    { empid: "cr4", text: "Ford Taurus", },                    { empid: "cr5", text: "Dazzler", },                    { empid: "cr6", text: "Chevy Spark", },                    { empid: "cr7", text: "Chevy Volt", },                    { empid: "cr8", text: "Honda Fit", },                    { empid: "cr9", text: "Honda Crosstour", },                    { empid: "cr10", text: "Acura RL", },                    { empid: "cr11", text: "Hyundai Elantra", },                    { empid: "cr12", text: "Mazda3", }        ];        angular.module('ListCtrl', ['ejangular'])           .controller('ListBoxCtrl', function ($scope) {               $scope.dataList = list;               $scope.value = "Ford Focus";           });    &lt;/script&gt;    &lt;style&gt;        #binding {            width: 100px;            padding-bottom: 216px;            padding-left: 100px;        }    &lt;/style&gt;&lt;/body&gt;&lt;/html&gt;&lt;body&gt;    &lt;div ng-app="ListCtrl"&gt;        &lt;div ng-controller="ListBoxCtrl"&gt;            &lt;div id="control" style="height: 300px;"&gt;                &lt;table&gt;                    &lt;tr&gt;                        &lt;td&gt;                            <div class="ctrllabel">Select a section</div>                            &lt;ul id="bookselect" ej-listbox e-datasource="dataList" e-value="value"&gt;                            &lt;/ul&gt;                        &lt;/td&gt;                        &lt;td id="binding"&gt;                            &lt;div&gt;                                &lt;input type="text" id="dropvalue" class="input ejinputtext" ng-model="value" /&gt;                                &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                            &lt;/div&gt;                        &lt;/td&gt;                    &lt;/tr&gt;                &lt;/table&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/body&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    var list = [                { empid: "cr1", text: "Dodge Avenger" },                { empid: "cr2", text: "Chrysler 200" },                { empid: "cr3", text: "Ford Focus" },                { empid: "cr4", text: "Ford Taurus", },                { empid: "cr5", text: "Dazzler", },                { empid: "cr6", text: "Chevy Spark", },                { empid: "cr7", text: "Chevy Volt", },                { empid: "cr8", text: "Honda Fit", },                { empid: "cr9", text: "Honda Crosstour", },                { empid: "cr10", text: "Acura RL", },                { empid: "cr11", text: "Hyundai Elantra", },                { empid: "cr12", text: "Mazda3", }    ];    angular.module('ListCtrl', ['ejangular'])       .controller('ListBoxCtrl', function ($scope) {<b>           $scope.dataList = list;</b><b>           $scope.value = "Ford Focus";</b>       });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b> // Add the following code in View page to configure ListBox widget&lt;body&gt;    &lt;div ng-app="ListCtrl"&gt;        &lt;div ng-controller="ListBoxCtrl"&gt;            &lt;div id="control" style="height: 300px;"&gt;                &lt;table&gt;                    &lt;tr&gt;                        &lt;td&gt;                            &lt;div class="ctrllabel"&gt;                                Select a section                            &lt;/div&gt;                            &lt;ul id="bookselect" ej-listbox e-datasource="dataList" e-value="value"&gt;&lt;/ul&gt;                        &lt;/td&gt;                        &lt;td id="binding"&gt;                            &lt;div&gt;                                &lt;input type="text" id="dropvalue" class="input ejinputtext" ng-model="value" /&gt;                                &lt;h6&gt;                                    &lt;span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;"&gt;                                        Note:Two Way Angular Support                                    &lt;/span&gt;                                &lt;/h6&gt;                            &lt;/div&gt;                        &lt;/td&gt;                    &lt;/tr&gt;                &lt;/table&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/body&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control and bind the data in <b>JavaScript</b>.&lt;script type="text/javascript"&gt;    var list = [                { empid: "cr1", text: "Dodge Avenger" },                { empid: "cr2", text: "Chrysler 200" },                { empid: "cr3", text: "Ford Focus" },                { empid: "cr4", text: "Ford Taurus", },                { empid: "cr5", text: "Dazzler", },                { empid: "cr6", text: "Chevy Spark", },                { empid: "cr7", text: "Chevy Volt", },                { empid: "cr8", text: "Honda Fit", },                { empid: "cr9", text: "Honda Crosstour", },                { empid: "cr10", text: "Acura RL", },                { empid: "cr11", text: "Hyundai Elantra", },                { empid: "cr12", text: "Mazda3", }    ];    <b>angular.module('ListCtrl', ['ejangular'])</b><b>       .controller('ListBoxCtrl', function ($scope) {</b><b>           $scope.dataList = list;</b><b>           $scope.value = "Ford Focus";</b><b>       });</b>&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b> // In the ASPX page, add a &lt;ul&gt; element to configure ListBox control&lt;body&gt;    &lt;div ng-app="ListCtrl"&gt;        &lt;div ng-controller="ListBoxCtrl"&gt;            &lt;div id="control" style="height: 300px;"&gt;                &lt;table&gt;                    &lt;tr&gt;                        &lt;td&gt;                            <div class="ctrllabel">Select a section</div>                            &lt;ul id="bookselect" ej-listbox e-datasource="dataList" e-value="value"&gt;                            &lt;/ul&gt;                        &lt;/td&gt;                        &lt;td id="binding"&gt;                            &lt;div&gt;                                &lt;input type="text" id="dropvalue" class="input ejinputtext" ng-model="value" /&gt;                                &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span>&lt;/h6&gt;                            &lt;/div&gt;                        &lt;/td&gt;                    &lt;/tr&gt;                &lt;/table&gt;            &lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;&lt;/body&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    var list = [                { empid: "cr1", text: "Dodge Avenger" },                { empid: "cr2", text: "Chrysler 200" },                { empid: "cr3", text: "Ford Focus" },                { empid: "cr4", text: "Ford Taurus", },                { empid: "cr5", text: "Dazzler", },                { empid: "cr6", text: "Chevy Spark", },                { empid: "cr7", text: "Chevy Volt", },                { empid: "cr8", text: "Honda Fit", },                { empid: "cr9", text: "Honda Crosstour", },                { empid: "cr10", text: "Acura RL", },                { empid: "cr11", text: "Hyundai Elantra", },                { empid: "cr12", text: "Mazda3", }    ];    angular.module('ListCtrl', ['ejangular'])       .controller('ListBoxCtrl', function ($scope) {<b>           $scope.dataList = list;</b><b>           $scope.value = "Ford Focus";</b>       });&lt;/script&gt;</td></tr>
</table>


Add the following styles in your sample



**[HTML]**



&lt;style&gt;

    #binding {

        width: 100px;

        padding-bottom: 216px;

        padding-left: 100px;

    }

&lt;/style&gt;





Output of the above steps

{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img10.png" Caption="Figure 159: ListBox with angular two-way Data binding"%}

**Knockout binding**

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One-way binding

* Two-way binding

One way binding refers to the process of applying observable values to all the available properties of the **ListBox** widget, but the changes made in the widget does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the ListBox widget.

Two-way binding supports both the processes – it applies the observable values to the **ListBox** widget properties as well as the changes made in the ListBox widget is also reflected back and triggered within the observable collections. 

For more information about the knockout binding, refer the following online documentation in the following link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

The following example depicts the way to bind data to the **ListBox** widget through the knockout support that enables and populates data to a **ListBox** widget based on the value set to the other **ListBox** widget.


> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding-_images\data-binding-_img11.png)_**Note: You caninclude the “ej.widget.knockout.min.js” file library to achieve this behaviour and you can pass the control properties as data attribute in ul tag itself as like data role behaviour.**_

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.



<table>
<tr>
<td>
&lt;!DOCTYPE html&gt;&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;&lt;head&gt;    &lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"&gt;&lt;/script&gt;&lt;/head&gt;&lt;body&gt;    &lt;div id="control"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    <div class="ctrllabel">Select a section</div>                    &lt;ul id="controlselect" data-bind="ejListBox: { dataSource: dataList, value: value }"&gt;&lt;/ul&gt;                &lt;/td&gt;                &lt;td id="binding"&gt;                    &lt;div&gt;                        &lt;input type="text" id="dropvalue" class="input ejinputtext" data-bind="value: value" /&gt;                        &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Knockout Support</span>&lt;/h6&gt;                    &lt;/div&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;    &lt;script type="text/javascript"&gt;        $(function () {            var carList = [                { empid: "cr1", text: "Accordion" },                { empid: "cr2", text: "Autocomplete" },                { empid: "cr3", text: "Button" },                { empid: "cr4", text: "Tab", },                { empid: "cr5", text: "Menu", },                { empid: "cr6", text: "Rating", },                { empid: "cr7", text: "Slider", },                { empid: "cr8", text: "Splitter", },                { empid: "cr9", text: "Tagcloud", },                { empid: "cr10", text: "Scroller", },                { empid: "cr11", text: "TreeView", },                { empid: "cr12", text: "WaitingPopup", }            ];            window.viewModel = {                dataList: ko.observable(carList),                value: ko.observable("Button"),            }            ko.applyBindings(viewModel);        });    &lt;/script&gt;    &lt;style type="text/css"&gt;        .ejinputtext {            background-color: #fff;            border: 1px solid #bbbcbb;            color: #5c5c5c;            height: 30px;            outline: medium none;        }        #binding {            width: 100px;            padding-bottom: 216px;            padding-left: 100px;        }    &lt;/style&gt;&lt;/body&gt;&lt;/html&gt;<b>[HTML]  </b>&lt;div id="control"&gt;    &lt;table&gt;        &lt;tr&gt;            &lt;td&gt;                <div class="ctrllabel">Select a section</div>                &lt;ul id="controlselect" data-bind="ejListBox: { dataSource: dataList, value: value }"&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td id="binding"&gt;                &lt;div&gt;                    &lt;input type="text" id="dropvalue" class="input ejinputtext" data-bind="value: value" /&gt;                    &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Knockout Support</span>&lt;/h6&gt;                &lt;/div&gt;            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var carList = [            { empid: "cr1", text: "Accordion" },            { empid: "cr2", text: "Autocomplete" },            { empid: "cr3", text: "Button" },            { empid: "cr4", text: "Tab", },            { empid: "cr5", text: "Menu", },            { empid: "cr6", text: "Rating", },            { empid: "cr7", text: "Slider", },            { empid: "cr8", text: "Splitter", },            { empid: "cr9", text: "Tagcloud", },            { empid: "cr10", text: "Scroller", },            { empid: "cr11", text: "TreeView", },            { empid: "cr12", text: "WaitingPopup", }        ];        window.viewModel = {            <b>dataList: ko.observable(carList),</b>            value: ko.observable("Button"),        }       <b> ko.applyBindings(viewModel);</b>    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]  </b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;table&gt;        &lt;tr&gt;            &lt;td&gt;                &lt;div class="ctrllabel"&gt;                    Select a section                &lt;/div&gt;                &lt;ul id="controlselect" data-bind="ejListBox: { dataSource: dataList, value: value }"&gt;&lt;/ul&gt;            &lt;/td&gt;            &lt;td id="binding"&gt;                &lt;div&gt;                    &lt;input type="text" id="dropvalue" class="input ejinputtext" data-bind="value: value" /&gt;                    &lt;h6&gt;                        &lt;span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;"&gt;                            Note:Two Way Knockout Support                        &lt;/span&gt;                    &lt;/h6&gt;                &lt;/div&gt;            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control and bind the data in <b>JavaScript</b>.&lt;script type="text/javascript"&gt;    $(function () {        var carList = [            { empid: "cr1", text: "Accordion" },            { empid: "cr2", text: "Autocomplete" },            { empid: "cr3", text: "Button" },            { empid: "cr4", text: "Tab", },            { empid: "cr5", text: "Menu", },            { empid: "cr6", text: "Rating", },            { empid: "cr7", text: "Slider", },            { empid: "cr8", text: "Splitter", },            { empid: "cr9", text: "Tagcloud", },            { empid: "cr10", text: "Scroller", },            { empid: "cr11", text: "TreeView", },            { empid: "cr12", text: "WaitingPopup", }        ];        <b>window.viewModel = {</b><b>            dataList: ko.observable(carList),</b><b>            value: ko.observable("Button"),</b><b>        }</b><b>        ko.applyBindings(viewModel);</b>    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]  </b>// In the ASPX page, add a &lt;ul&gt; element to configure ListBox control&lt;div id="control"&gt;    &lt;table&gt;        &lt;tr&gt;            &lt;td&gt;                <div class="ctrllabel">Select a section</div>                &lt;ul id="controlselect" data-bind="ejListBox: { dataSource: dataList, value: value }"&gt;                &lt;/ul&gt;            &lt;/td&gt;            &lt;td id="binding"&gt;                &lt;div&gt;                    &lt;input type="text" id="dropvalue" class="input ejinputtext" data-bind="value: value" /&gt;                    &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Knockout Support</span>&lt;/h6&gt;                &lt;/div&gt;            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control and bind the data in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var carList = [            { empid: "cr1", text: "Accordion" },            { empid: "cr2", text: "Autocomplete" },            { empid: "cr3", text: "Button" },            { empid: "cr4", text: "Tab", },            { empid: "cr5", text: "Menu", },            { empid: "cr6", text: "Rating", },            { empid: "cr7", text: "Slider", },            { empid: "cr8", text: "Splitter", },            { empid: "cr9", text: "Tagcloud", },            { empid: "cr10", text: "Scroller", },            { empid: "cr11", text: "TreeView", },            { empid: "cr12", text: "WaitingPopup", }        ];        window.viewModel = {            <b>dataList: ko.observable(carList),</b>            value: ko.observable("Button"),        }       <b> ko.applyBindings(viewModel);</b>    });&lt;/script&gt;</td></tr>
</table>


Configure the styles.



**[CSS]** 



&lt;style type="text/css" class="cssStyles"&gt;

    #binding {

        width: 100px;

        padding-bottom: 216px;

        padding-left: 100px;

&lt;/style&gt;





Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\data-binding-_images\data-binding-_img12.png" Caption="Figure 1610: ListBox with KO Data binding"%}

