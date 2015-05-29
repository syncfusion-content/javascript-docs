---
layout: post
title: data-binding
description: data binding
platform: js
control: Toolbar
documentation: ug
---

# Data binding

**Toolbar** provides you a flexible approach for binding data from various data sources. There are various properties in **Toolbar** for Data Binding.

## Data fields and configuration 

The following sub-properties provides a way to bind either the local/remote data to the **Toolbar** control.

_Table_ _1__: Property Table of JavaScript Toolbar control_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Syntax</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dDataSource</td><td>
dataSource: window.countriesField</td><td>
It specifies the data source of the Toolbar. The data source contains the list of data for generating the Toolbar items. By default, its value is null and its data type is object. </td></tr>
<tr>
<td>
fField</td><td>
fields: {text: "name", value: "key" }</td><td>
It specifies the mapping fields for the data items of the Toolbar. By default, its value is null and its data type is object.</td></tr>
<tr>
<td>
qQuery</td><td>
query: ej.Query().from("Suppliers").select("ContactName");       	 </td><td>
It specifies the query to retrieve the data from online server. By default, its value is null and its data type is object. </td></tr>
<tr>
<td>
idId</td><td>
id</td><td>
It specifies the id of the tag and its default value is null and data type is string. </td></tr>
<tr>
<td>
textText</td><td>
text</td><td>
It specifies the text content of the tag and its default value is null and data type is string. </td></tr>
<tr>
<td>
imageUrlImage URL</td><td>
imageUrl</td><td>
This property defines the imageURL for the image location. While setting images, the folder name in which the images are stored should be set to imageUrl property. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
imageAttributesImage Attributes</td><td>
imageAttributes</td><td>
This property defines style for the image. While setting an image, styles can be applied such as height, width by using this property. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
spriteCssClassSprite CSS Class</td><td>
spriteCssClass</td><td>
This property sets the Sprite CSS for the image tag in Toolbar. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
htmlAttributesHTML Attributes</td><td>
htmlAttributes</td><td>
This property sets the <b>HTML</b> attribute for the Toolbar item. The value set to this property should be <b>object</b> type. It can be any <b>HTML</b> attribute such as id, class, style.</td></tr>
<tr>
<td>
tooltipText  Tooltip text</td><td>
tooltipText  </td><td>
This property sets the text value for Toolbar item while mouse over in Toolbar. The value set to this property should be <b>string</b> type.</td></tr>
</table>
_Table_ _2__: Property Table of MVC Toolbar control_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Value type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
DataSource</td><td>
object</td><td>
It specifies the data source of the Toolbar. The data source contains the list of data for generating the Toolbar items.</td></tr>
<tr>
<td>
ToolbarFields</td><td>
object</td><td>
It specifies the mapping fields for the data items of the Toolbar.</td></tr>
<tr>
<td>
Id</td><td>
string</td><td>
It specifies the id of the tag.</td></tr>
<tr>
<td>
Text</td><td>
string</td><td>
It specifies the text content of the tag.</td></tr>
<tr>
<td>
ImageUrl</td><td>
string</td><td>
This property defines the imageURL for the image location. While setting images, the folder name in which the images are stored should be set to imageUrl property.</td></tr>
<tr>
<td>
ImageAttributes</td><td>
string</td><td>
This property defines style for the image. While setting an image, styles can be applied such as height, width by using this property.</td></tr>
<tr>
<td>
SpriteCssClass</td><td>
string</td><td>
This property sets the Sprite CSS for the image tag in Toolbar.</td></tr>
<tr>
<td>
HtmlAttributes</td><td>
object</td><td>
This property sets the <b>HTML</b> attribute for the Toolbar item. It can be any <b>HTML</b> attribute such as id, class, style.</td></tr>
<tr>
<td>
TooltipText</td><td>
string</td><td>
This property sets the text value for Toolbar item while mouse over in Toolbar.</td></tr>
<tr>
<td>
Query</td><td>
object</td><td>
It specifies the query to retrieve the data from online server.</td></tr>
<tr>
<td>
Group</td><td>
string</td><td>
It groups the given Toolbar items.</td></tr>
</table>
_Table_ _3__: Property Table of ASP.NET Toolbar control_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Value Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
DataSource </td><td>
object</td><td>
It specifies the data source of the Toolbar. The data source contains the list of data for generating the Toolbar items.</td></tr>
<tr>
<td>
DataSourceID</td><td>
object</td><td>
It specifies the source from which the data is bound in Toolbar items.</td></tr>
<tr>
<td>
Query</td><td>
object</td><td>
It specifies the query to retrieve the data from online server.</td></tr>
<tr>
<td>
DataIdField</td><td>
string</td><td>
It specifies the id of the tag</td></tr>
<tr>
<td>
DataTextField </td><td>
string</td><td>
It specifies the text content of the tag</td></tr>
<tr>
<td>
DataImageUrlField</td><td>
string</td><td>
This property defines the imageURL for the image location. While setting images, the folder name in which the images are stored should be set to <b>ImageUrl</b> property.</td></tr>
<tr>
<td>
DataImageAttributeField</td><td>
string</td><td>
This property defines style for the image. While setting an image, styles can be applied such as Height, Width by using this property.</td></tr>
<tr>
<td>
DataSpriteCssClassField</td><td>
string</td><td>
This property sets the Sprite CSS for the image tag in Toolbar.</td></tr>
<tr>
<td>
DataHtmlAttributeField</td><td>
object</td><td>
This property sets the <b>HTML</b> attribute for the Toolbar item.</td></tr>
<tr>
<td>
DataTooltipTextField</td><td>
string</td><td>
This property sets the text value for Toolbar item while mouse over in Toolbar.</td></tr>
<tr>
<td>
DataGroupField</td><td>
string</td><td>
This property is used to group the Toolbar items.</td></tr>
<tr>
<td>
DataMember</td><td>
string</td><td>
This property is used to assign the tag name in which the Toolbar items can be defined in xml.</td></tr>
</table>
## Local data

**Toolbar** provides you an extensive data binding support to generate **Toolbar** items, that the values can be mapped to the **ToolBar** fields, namely **key** and **text**.

And also you can add image, image styles, sprite css class, query and html attributes options with data binding fields. The following code explains the details about the data binding with **Toolbar**. 

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="cols-sample-area"&gt;    &lt;div id="toolbarcontent"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>    &lt;script type="text/javascript"&gt;    $(function () {        // declaration        BrowserItems = [{            iconid: "1",            spriteCss: "ToolbarItems LeftAlign_tool",            tooltipText: "left",        }, {            iconid: "2",            spriteCss: "ToolbarItems CenterAlign_tool",            tooltipText: "centre",        }, {            iconid: "3",            spriteCss: "ToolbarItems RightAlign_tool",            tooltipText: "right",        }, {            iconid: "4",            spriteCss: "ToolbarItems Justify_tool",            text: "Justify",            imageAttributes: [{ height: "50px" }, { width: "30px" }],            tooltipText: "justify",        }, {            iconid: "5",            spriteCss: "ToolbarItems Bold_tool",            imageAttributes: [{ height: "50px" }, { width: "30px" }],            tooltipText: "bold",            htmlAttributes: [{ class: "html" }],        }, {            iconid: "6",            spriteCss: "ToolbarItems Italic_tool",            tooltipText: "italic",        }, {            iconid: "7",            spriteCss: "ToolbarItems StrikeThrough_tool",            tooltipText: "strike",        }, {            iconid: "8",            spriteCss: "ToolbarItems Underline_tool",            tooltipText: "underline",        }        ];        $("#toolbarcontent").ejToolbar({            width: "300px",            dataSource: BrowserItems,            fields: { id: "iconid", spriteCssClass: "spriteCss", imageUrl: "url", imageAttributes: "imageAttributes", tooltipText: "tooltipText", text: "text", htmlAttributes: "htmlAttributes", },            orientation: ej.Orientation.Horizontal,        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).Orientation(Orientation.Horizontal)&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b>            public class ToolbarLocalBinding        {            public string IconId { get; set; }            public string SpriteCss { get; set; }            public string Tooltip { get; set; }        }        public ActionResult Index()        {            List<ToolbarLocalBinding> toolslist = new List<ToolbarLocalBinding>();            toolslist.Add(new ToolbarLocalBinding { IconId = "1", SpriteCss = "LeftAlign_tool", Tooltip = "left" });            toolslist.Add(new ToolbarLocalBinding { IconId = "2", SpriteCss = "CenterAlign_tool", Tooltip = "centre" });            toolslist.Add(new ToolbarLocalBinding { IconId = "3", SpriteCss = "RightAlign_tool", Tooltip = "right" });            toolslist.Add(new ToolbarLocalBinding { IconId = "4", SpriteCss = "Justify_tool", Tooltip = "justify" });            toolslist.Add(new ToolbarLocalBinding { IconId = "5", SpriteCss = "Bold_tool", Tooltip = "bold" });            toolslist.Add(new ToolbarLocalBinding { IconId = "6", SpriteCss = "Italic_tool", Tooltip = "italic" });            toolslist.Add(new ToolbarLocalBinding { IconId = "7", SpriteCss = "StrikeThrough_tool", Tooltip = "strike" });            toolslist.Add(new ToolbarLocalBinding { IconId = "8", SpriteCss = "Underline_tool", Tooltip = "underline" });            ViewBag.datasource = toolslist;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>&lt;div class="cols-sample-area"&gt;    &lt;ej:Toolbar  ID="toolbarcontent"  runat="server" Width="300px" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[C#]</b>    public class ToolData        {            public string Id            {                get;                set;            }            public string Css            {                get;                set;            }            public string Tooltip            {                get;                set;            }        }        protected void Page_Load(object sender, EventArgs e)        {            List<ToolData> data = new List<ToolData>();            data.Add(new ToolData {Id ="1", Css = "ToolbarItems LeftAlign_tool", Tooltip = "left"});            data.Add(new ToolData {Id ="2", Css="ToolbarItems CenterAlign_tool", Tooltip="centre"});            data.Add(new ToolData {Id="3", Css="ToolbarItems RightAlign_tool", Tooltip="right"});            data.Add(new ToolData {Id="4", Css="ToolbarItems Justify_tool",Tooltip="justify"});            data.Add(new ToolData {Id="5", Css="ToolbarItems Bold_tool", Tooltip="bold"});            data.Add(new ToolData {Id="6", Css="ToolbarItems Italic_tool", Tooltip="italic"});            data.Add(new ToolData {Id="7", Css="ToolbarItems StrikeThrough_tool", Tooltip="strike"});            data.Add(new ToolData {Id="8", Css = "ToolbarItems Underline_tool", Tooltip = "underline"});            this.toolbarcontent.DataSource = data;        }</td></tr>
</table>


{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }

    .html {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}



![](data-binding_images\data-binding_img1.png)

_Figure_ _16__6__: ToolBar control bounded to Local Data_

## Remote data

You can bind the data for the **Toolbar** items from remote. That is, you can access the data from any other server that is located as remote web service. It uses DataManager to retrieve data and you can create DataManager with its **URL**. To create DataManager, define ej.DataManager() to a variable. Then provide online link to **url** property. Assign this variable to **Toolbar** dataSource. 

To bind Remote data to **Toolbar**, use the following code example.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="toolbarcontent"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // DataManager creation        var dataManger = ej.DataManager({            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"        });        // Query creation        var query = ej.Query()             .from("Orders").take(6);        $("#toolbarcontent").ejToolbar({            dataSource: dataManger,            fields: { text: "CustomerID" },            query: query,            orientation: "horizontal",            width: "340px"        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@Html.EJ().Toolbar("toolbarcontent").Datasource(ds => ds.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).Query("ej.Query().from('Orders').take(6)").ToolbarFields(f => f.Text("CustomerID")).Orientation(Orientation.Horizontal).Width("340")



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="340px" Orientation="Horizontal" DataTextField="CustomerID" Query="ej.Query().from('Orders').take(6)"&gt;&lt;/ej:Toolbar &gt;</td></tr>
<tr>
<td>
<b>[C#]</b>protected void Page_Load(object sender, EventArgs e)        {            this.toolbarcontent.DataSource = "http://mvc.syncfusion.com/Services/Northwnd.svc/";        }</td></tr>
</table>


![](data-binding_images\data-binding_img2.png)

_Figure_ _17__7__: ToolBar control bounded to Remote Data_

**Sql Data**

**SqlDataSource** is designed to work with **SQL** Server databases. It uses the SQL **Server .NET** data provider internally. **SQL** server .NET data provider classes are defined in the **System.Data.SqlClient** namespace. You can bind the **SqlDataSource** to **ToolBar** with****DataSourceID as the id of **sqldatasource**. You can select the table from **selectcommand.** Create a table with the following fields in Sql and refer that in connectionstring to run the following sample.****Refer the following table for fields and its corresponding data types.


{% include image.html url="\js\Toolbar\concepts-and-features\data-binding_images\data-binding_img3.png" Caption="Figure 18: ToolBar control with Sql table"%}

Refer the following code sample to bind **SQL** data in **Toolbar**.


**[ASPX]**

&lt;%--Refer Local data sections for styles--%&gt;

&lt;div class="cols-sample-area"&gt;

    <ej:Toolbar  ID="toolbarcontent" runat="server" Orientation="Horizontal" DataIdField="Id" DataSpriteCssClassField="IconCss" DataTooltipTextField="ToolTip"

        DataSourceID="SqlDataSource1" Width="600px">

            &lt;/ej:Toolbar &gt;



    &lt;asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="Data Source=(LocalDB)\v11.0;AttachDbFilename=|DataDirectory|\TreeEntity.mdf;Integrated Security=True" ProviderName="System.Data.SqlClient" SelectCommand="SELECT * FROM [ToolBarItems]"&gt;&lt;/asp:SqlDataSource&gt;

&lt;/div&gt;



{% include image.html url="\js\Toolbar\concepts-and-features\data-binding_images\data-binding_img4.png" Caption="Figure 19: ToolBar control bounded to SQL Data"%}

**Object Data**

The objectdatasource control lets you bind a specific data layer in the same manner as you bind the database using other controls. The objectdatasource control can bind to any method that returns a DataSet or an IEnumerable object (for example, a DataReader or a collection of Classes). The major advantage of binding via objectdatasource is, only records that are required in the current view are retrieved from the database, greatly optimizing the performance and runtime memory usage. To bind the objectdatasource to **ToolBar**, use the following code sample.

<table>
<tr>
<td>
<b>[ASPX]</b>&lt;%--Refer Local data sections for styles--%&gt;<ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px"    DataSourceID="ObjectDataSource1"    DataTooltipTextField="Tooltip" DataIdField="Id" DataSpriteCssClassField="Css">            &lt;/ej:Toolbar &gt;&lt;asp:ObjectDataSource ID="ObjectDataSource1" runat="server" SelectMethod="GetToolItems" TypeName="ToolData"&gt;&lt;/asp:ObjectDataSource&gt;</td></tr>
<tr>
<td>
<b>[C#]</b>[Serializable]public class ToolData{    public ToolData(string _id, string _css, string _tip)    {        this.Id = _id;        this.Tooltip = _tip;        this.Css = _css;    }    public ToolData()    {    }    [Browsable(true)]    public string Id    {        get;        set;    }    [Browsable(true)]    public string Css    {        get;        set;    }    [Browsable(true)]    public string Tooltip    {        get;        set;    }    public List<ToolData> GetToolItems()    {        List<ToolData> data = new List<ToolData>();         data.Add(new ToolData { Id = "1", Css = "ToolbarItems LeftAlign_tool", Tooltip = "left" });            data.Add(new ToolData { Id = "2", Css = "ToolbarItems CenterAlign_tool", Tooltip = "centre" });            data.Add(new ToolData { Id = "3", Css = "ToolbarItems RightAlign_tool", Tooltip = "right" });            data.Add(new ToolData { Id = "4", Css = "ToolbarItems Justify_tool", Tooltip = "justify" });            data.Add(new ToolData { Id = "5", Css = "ToolbarItems Bold_tool", Tooltip = "bold" });            data.Add(new ToolData { Id = "6", Css = "ToolbarItems Italic_tool", Tooltip = "italic" });            data.Add(new ToolData { Id = "7", Css = "ToolbarItems StrikeThrough_tool", Tooltip = "strike" });            data.Add(new ToolData { Id = "8", Css = "ToolbarItems Underline_tool", Tooltip = "underline" });        return data;    }}</td></tr>
</table>


{% include image.html url="\js\Toolbar\concepts-and-features\data-binding_images\data-binding_img5.png" Caption="Figure 20: ToolBar control bounded to Object Data"%}

**Xml Data**

**XmlDataSource** is used to work with **XML** documents. You can bind the **XmlDataSource** to **ToolBar**, with **DataSourceID** of the toolbar should be the id of **XmlDataSource**. Refer the following code sample.



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;%--Refer Local data sections for styles--%&gt;&lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" DataIdField="Id" DataSpriteCssClassField="Sprite" DataTooltipTextField="Tooltip" DataMember="RootItem" DataSourceID="XmlDataSource1"&gt;&lt;/ej:Toolbar &gt;&lt;asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~/App_Data/XMLTool.xml"&gt;&lt;/asp:XmlDataSource &gt;</td></tr>
<tr>
<td>
[XML]&lt;?xml version="1.0" encoding="utf-8" ?&gt;&lt;Items&gt;  &lt;RootItem Sprite="ToolbarItems LeftAlign_tool" Id="one"&gt;    <Tooltip>Left</Tooltip>  &lt;/RootItem&gt;  &lt;RootItem Sprite="ToolbarItems CenterAlign_tool" Id="two" &gt;    <Tooltip>Center</Tooltip>  &lt;/RootItem&gt;  &lt;RootItem Sprite="ToolbarItems RightAlign_tool" Id="three" &gt;    <Tooltip>Right</Tooltip>  &lt;/RootItem&gt;  &lt;RootItem Sprite="ToolbarItems Justify_tool" Id="four" &gt;    <Tooltip>Justify</Tooltip>  &lt;/RootItem&gt;  &lt;RootItem Sprite="ToolbarItems Bold_tool" Id="five"&gt;    <Tooltip>Bold</Tooltip>  &lt;/RootItem&gt; &lt;RootItem Sprite="ToolbarItems Italic_tool" Id="six"&gt;    <Tooltip>Italic</Tooltip>  &lt;/RootItem&gt; &lt;RootItem Sprite="ToolbarItems StrikeThrough_tool" Id="seven"&gt;    <Tooltip>Strike</Tooltip>  &lt;/RootItem&gt; &lt;RootItem Sprite="ToolbarItems Underline_tool" Id="eight"&gt;    <Tooltip>Underline</Tooltip>  &lt;/RootItem&gt;&lt;/Items&gt;</td></tr>
</table>


{% include image.html url="\js\Toolbar\concepts-and-features\data-binding_images\data-binding_img6.png" Caption="Figure 21: ToolBar control bounded to Xml Data"%}

**Linq to Sql Data**

The linqdatasource is used to bind **Toolbar** data via Linq to Sql. The property **contexttypename** indicates the location of the data source. Mention exact table name of your data base in **tablename** property. Provide the id of linqdatasource to **DataSourceID** of **Toolbar**. To bind data by using Linq to Sql to **Toolbar**, you can create a table with the provided fields in Linq to Sql and refer that in **tablename** and mention **contexttypename** as the location of the data base. Refer the following code.



**[ASPX]**

&lt;%--Refer Local data sections for styles--%&gt;

&lt;div class="cols-sample-area"&gt;

    <ej:Toolbar  ID="toolbarcontent" runat="server" Orientation="Horizontal" DataIdField="Id" DataSpriteCssClassField="IconCss" DataTooltipTextField="ToolTip"

        DataSourceID="LinqDataSource1" Width="600px">

            &lt;/ej:Toolbar &gt;

    &lt;asp:LinqDataSource ID="LinqDataSource1" runat="server" ContextTypeName=" DataClasses1DataContext" EntityTypeName="" TableName="ToolBarItems"&gt;&lt;/asp:LinqDataSource&gt;



&lt;/div&gt;

## 

## 

## Figure 22: ToolBar control bounded to Linq to sql

## Knockout binding

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One-way binding

* Two-way binding

One-way binding refers to the process of applying observable values to all the available properties of the **Toolbar**, where the changes made in **Toolbar** widget is not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **Toolbar**.

Two-way binding supports both the processes – it applies the observable values to the **Toolbar** properties as well as the changes made in the Toolbar widget is reflected back and triggered within the observable collections. 

For more information about the knockout binding, refer the following link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)



> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding_images\data-binding_img7.png)_**Note: Add the following script files along with the specified code to access knockout binding. It contains JS library for knockout binding.**_

* Knockout.min.js

* ej.widget.ko.min.js

The link for the script file is as follows:

[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js)


The following code example depicts you the way to bind data to the **Toolbar** through the knockout support. 


<table>
<tr>
<td>
<b>[HTML]</b>&lt;!DOCTYPE html&gt;&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;&lt;head&gt;    &lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"&gt;&lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt; &lt;/script&gt;    &lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"&gt;&lt;/script&gt;&lt;/head&gt;&lt;body&gt;    &lt;div class="cols-sample-area"&gt;        &lt;div id="toolbarcontent" data-bind="ejToolbar:{ dataSource:dataList, fields:{ id:'iconid', spriteCssClass:'spriteCss', text:'text'}, width:width }"&gt;&lt;/div&gt;    &lt;/div&gt;&lt;/body&gt;&lt;/html&gt;&lt;div class="cols-sample-area"&gt;    &lt;div id="toolbarcontent" data-bind="ejToolbar:{ dataSource:dataList, fields:{ id:'iconid', spriteCssClass:'spriteCss', text:'text'}, width:width }"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        var tool = [{            iconid: "1",            spriteCss: "ToolbarItems LeftAlign_tool",        }, {            iconid: "2",            spriteCss: "ToolbarItems CenterAlign_tool",        }, {            iconid: "3",            spriteCss: "ToolbarItems RightAlign_tool",        }, {            iconid: "4",            spriteCss: "ToolbarItems Justify_tool",        }, {            iconid: "5",            spriteCss: "ToolbarItems Bold_tool",        }, {            iconid: "6",            spriteCss: "ToolbarItems Italic_tool",        }, {            iconid: "7",            spriteCss: "ToolbarItems StrikeThrough_tool",        }, {            iconid: "8",            spriteCss: "ToolbarItems Underline_tool",        }        ];        window.viewModel = {            dataList: ko.observableArray(tool),            width: ko.observable("300px"),        };        ko.applyBindings(viewModel);    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

&lt;div class="cols-sample-area"&gt;

&lt;div id="toolbarcontent" data-bind="ejToolbar:{ dataSource:dataList, fields:{ id:'IconId', spriteCssClass:'SpriteCss'}, width:width }"&gt;&lt;/div&gt;

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;%--Refer Local data sections for styles--%&gt;&lt;div class="cols-sample-area"&gt;    &lt;div id="toolbarcontent" data-bind="ejToolbar:{ dataSource:dataList, fields:{ id:'IconId', spriteCssClass:'SpriteCss'}, Width:Width }"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        var tool = [{            IconId: "1",            SpriteCss: "ToolbarItems LeftAlign_tool",        }, {            IconId: "2",            SpriteCss: "ToolbarItems CenterAlign_tool",        }, {            IconId: "3",            SpriteCss: "ToolbarItems RightAlign_tool",        }, {            IconId: "4",            SpriteCss: "ToolbarItems Justify_tool",        }, {            IconId: "5",            SpriteCss: "ToolbarItems Bold_tool",        }, {            IconId: "6",            SpriteCss: "ToolbarItems Italic_tool",        }, {            IconId: "7",            SpriteCss: "ToolbarItems StrikeThrough_tool",        }, {            IconId: "8",            SpriteCss: "ToolbarItems Underline_tool",        }        ];        window.viewModel = {            dataList: ko.observableArray(tool),            Width: ko.observable("300px"),        };        ko.applyBindings(viewModel);    });&lt;/script&gt;</td></tr>
</table>


{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}



![](data-binding_images\data-binding_img8.png)

_Figure_ _23__8__: Toolbar with Knockout support_

## Angular binding

**Toolbar** is availed with two types of **angular JS** support namely, 

* One way binding

* Two way binding 

One-way binding refers to the process of applying scope values to all the available properties of the Toolbar, where the changes made in **Toolbar** widget is not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **Toolbar**.

Two-way binding supports both the processes – it applies the scope values to the **Toolbar** properties as well as the changes made in the **Toolbar** widget is also reflected back and triggered within the angular scope change function.

To know more detail about the Angular binding, refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)


> ![C:\Users\ApoorvahR\Desktop\Note.png](data-binding_images\data-binding_img9.png)_**Note: Add the following script files as given in the below example to access knockout binding. It contains JS library for angular binding.**_

* Angular.min.js

* ej.widget.angular.min.js

The following code example depicts you the way to bind data to the **Toolbar** widget through angular support,

{% highlight html %}

**[HTML]**
<!DOCTYPE html>
<html lang="en" ng-app="toolApp">
<head>
    <title>Essential Studio for JavaScript :Angular JS Support for Toolbar</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js)"> </script>
</head>
<body ng-controller="ToolCtrl">

    <div class="cols-sample-area">
        <div id="toolbarcontent" ej-toolbar e-datasource="dataList" e-width="230px"
            e-fields-id="iconid" e-fields-spritecssclass="spriteCss">
        </div>
    </div>

</body>
</html>


{% endhighlight %}



{% highlight js %}

**[JS]**
<script>
    var list = [{
        iconid: "1",
        spriteCss: "ToolbarItems LeftAlign_tool",

    }, {
        iconid: "2",
        spriteCss: "ToolbarItems CenterAlign_tool",
    }, {
        iconid: "3",
        spriteCss: "ToolbarItems RightAlign_tool",
    }, {
        iconid: "4",
        spriteCss: "ToolbarItems Justify_tool",

    }, {
        iconid: "5",
        spriteCss: "ToolbarItems Bold_tool",
    }, {
        iconid: "6",
        spriteCss: "ToolbarItems Italic_tool",
    }, {
        iconid: "7",
        spriteCss: "ToolbarItems StrikeThrough_tool",
    }, {
        iconid: "8",
        spriteCss: "ToolbarItems Underline_tool",
    }
    ];

    angular.module('toolApp', ['ejangular']).controller('ToolCtrl', function ($scope) {
        $scope.dataList = list;
    });
</script>


{% endhighlight %}



**[CSHTML]**

&lt;!DOCTYPE html&gt;

&lt;html lang="en" ng-app="toolApp"&gt;

&lt;head&gt;

    <title>Essential Studio for JavaScript :Angular JS Support for Toolbar</title>

    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" /&gt;

    &lt;link href=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" /&gt;

    &lt;!--scripts--&gt;

    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt; &lt;/script&gt;

    &lt;script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"&gt; &lt;/script&gt; 



    &lt;script src="http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/web/ej.unobtrusive-latest.min.js "&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/web/ej.widget.ko-latest.min.js"&gt;&lt;/script&gt;

&lt;/head&gt;

&lt;body ng-controller="ToolCtrl"&gt;



            &lt;div class="cols-sample-area"&gt;					

                        <div id="toolbarcontent" ej-toolbar e-datasource="dataList" e-width="230px"

                            e-fields-id="IconId" e-fields-spriteCssClass="SpriteCss">&lt;/div&gt;

                    &lt;/div&gt;



&lt;/body&gt;

&lt;/html&gt;



**[ASPX]**

&lt;%--Refer Local data sections for styles--%&gt;

&lt;!DOCTYPE html&gt;

&lt;html lang="en" ng-app="toolApp"&gt;

&lt;head&gt;

    <title>Essential Studio for JavaScript :Angular JS Support for Toolbar</title>

    &lt;meta name="viewport" content="Width=device-Width, initial-scale=1.0" charset="utf-8" /&gt;

    &lt;link href=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" /&gt;

    &lt;!--scripts--&gt;

    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"&gt; &lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/web/ej.unobtrusive-latest.min.js "&gt;&lt;/script&gt;

&lt;script src="http://cdn.syncfusion.com/js/web/ej.widget.angular-latest.min.js"&gt; &lt;/script&gt;

&lt;/head&gt;

&lt;body ng-controller="ToolCtrl"&gt;



    &lt;div class="cols-sample-area"&gt;

        <div id="toolbarcontent" ej-toolbar e-datasource="dataList" e-Width="230px"

            e-fields-id="IconId" e-fields-spritecssclass="SpriteCss">

        &lt;/div&gt;

    &lt;/div&gt;



&lt;/body&gt;

&lt;/html&gt;





**[JS]**

&lt;script&gt;

    var list = [{

        IconId: "1",

        SpriteCss: "ToolbarItems LeftAlign_tool",



    }, {

        IconId: "2",

        SpriteCss: "ToolbarItems CenterAlign_tool",

    }, {

        IconId: "3",

        SpriteCss: "ToolbarItems RightAlign_tool",

    }, {

        IconId: "4",

        SpriteCss: "ToolbarItems Justify_tool",



    }, {

        IconId: "5",

        SpriteCss: "ToolbarItems Bold_tool",

    }, {

        IconId: "6",

        SpriteCss: "ToolbarItems Italic_tool",

    }, {

        IconId: "7",

        SpriteCss: "ToolbarItems StrikeThrough_tool",

    }, {

        IconId: "8",

        SpriteCss: "ToolbarItems Underline_tool",

    }

    ];



    angular.module('toolApp', ['ejangular']).controller('ToolCtrl', function ($scope) {

        $scope.dataList = list;

    });

&lt;/script&gt;



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    /*controls*/
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}



![](data-binding_images\data-binding_img10.png)

_Figure_ _24__9__: Toolbar with Angular support_

