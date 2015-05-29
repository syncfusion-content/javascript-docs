---
layout: post
title: data-binding-
description: data binding 
platform: js
control: TreeView
documentation: ug
---

# Data Binding 

The **TreeView** is populated with the node information taken from a data source. The **TreeView** supports binding data sources containing hierarchical data and supports both local data and remote data, for retrieving data from a specified data source. You can also display the hierarchical data in **TreeView**. **TreeView** exposes its specific data-related properties allowing you to specify which data source field the node information has to be retrieved from.

You can populate **TreeView** items using data binding support such as **JSON** and **OData** services. 

## Fields

The **Ffields** property in **TreeView** includes the data source fields and it can be set with appropriate values as follows.

_Table_ _1__:_ _JS_ _Field_ _properties_

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
It receives table name to execute query on the corresponding table.</td></tr>
<tr>
<td>
Id</td><td>
Specifies the id to <b>TreeView</b> node items list.</td></tr>
<tr>
<td>
parentId</td><td>
Specifies the parent id of the table.</td></tr>
<tr>
<td>
Text</td><td>
Specifies the text of <b>TreeView</b> node items list.</td></tr>
<tr>
<td>
spriteCssClass</td><td>
Specifies the sprite CSS class to “li” item list.</td></tr>
<tr>
<td>
linkAttribute</td><td>
Specifies the link attribute to “a” tag in item list.</td></tr>
<tr>
<td>
imageAttribute</td><td>
Specifies the image attribute to “img” tag inside items list.</td></tr>
<tr>
<td>
htmlAttribute</td><td>
Specifies the html attributes to “li” item list.</td></tr>
<tr>
<td>
imageUrl</td><td>
Specifies the image URL to “img” tag inside item list. </td></tr>
<tr>
<td>
expanded</td><td>
When it’s <b>true</b>, corresponding node expands.</td></tr>
<tr>
<td>
Child</td><td>
When a parent has child nodes to pass the same mapper for child.</td></tr>
<tr>
<td>
hasChild</td><td>
A parent node has child, set this value as <b>true</b>.</td></tr>
<tr>
<td>
selected</td><td>
A <b>TreeView</b> control has only one node selected at time.</td></tr>
<tr>
<td>
isChecked</td><td>
When it’s true the Checkbox node is checked.</td></tr>
<tr>
<td>
Value</td><td>
Specifies the value of the <b>TreeView</b> node items.</td></tr>
</table>


_Table_ _2__: MVC field properties_

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Type</b></td><td>
<b>Default</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dataSource</td><td>
Object</td><td>
Null</td><td>
datasource receives  Essential DataManager object and JSON object. </td></tr>
<tr>
<td>
query</td><td>
Object</td><td>
Null</td><td>
It receives query to retrieve data from the table (query is same as SQL). Example:  ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);</td></tr>
<tr>
<td>
tableName</td><td>
String</td><td>
Null</td><td>
It receives table name to execute query on the corresponding table.</td></tr>
<tr>
<td>
id</td><td>
String</td><td>
Null</td><td>
Specifies the id to TreeView node items list.</td></tr>
<tr>
<td>
parentId</td><td>
String</td><td>
Null</td><td>
Specifies the parent id of the table.</td></tr>
<tr>
<td>
text</td><td>
String</td><td>
Null</td><td>
Specifies the text of TreeView node items list.</td></tr>
<tr>
<td>
spriteCssClass</td><td>
String</td><td>
Null</td><td>
Specifies the sprite CSS class to “li” item list.</td></tr>
<tr>
<td>
linkAttribute</td><td>
String</td><td>
Null</td><td>
Specifies the link attribute to “a” tag in item list.</td></tr>
<tr>
<td>
imageAttribute</td><td>
String</td><td>
Null</td><td>
Specifies the image attribute to “img” tag inside items list.</td></tr>
<tr>
<td>
htmlAttribute</td><td>
String</td><td>
Null</td><td>
Specifies the html attributes to “li” item list.</td></tr>
<tr>
<td>
imageUrl</td><td>
String</td><td>
Null</td><td>
Specifies the image URL to “img” tag inside item list. </td></tr>
<tr>
<td>
expanded</td><td>
String</td><td>
Null</td><td>
If it’s true the expanded property, corresponding node will expand.</td></tr>
<tr>
<td>
child</td><td>
String</td><td>
Null</td><td>
If a parent have child node to pass the same mapper for child.</td></tr>
<tr>
<td>
hasChild</td><td>
String</td><td>
Null</td><td>
A parent node have child, we must this value as true.</td></tr>
<tr>
<td>
selected</td><td>
String</td><td>
Null</td><td>
A TreeView control has only one node selected at time.</td></tr>
<tr>
<td>
isChecked</td><td>
String</td><td>
Null</td><td>
If it’s true the isChecked property,Checkbox node will be checked.</td></tr>
<tr>
<td>
value</td><td>
String</td><td>
Null</td><td>
Specifies the value of the TreeView node items.</td></tr>
</table>
## Local Data

To bind the **Local Data** to the **TreeView** control, map the user-defined **json** data names with its appropriate data source field. You can bind data to **TreeView** by mapping fields such as **dataSource,id, parentId, text, hasChild** and **expanded**. 

The following steps explain how you can bind local data to **TreeView**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>      &lt;div id="treeView"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Define local data source elements with fields.</b>               var localData = [                   { id: 1, name: "Favorites", hasChild: true },                   { id: 2, pid: 1, name: "Desktop" },                   { id: 3, pid: 1, name: "Downloads" },                   { id: 4, pid: 1, name: "Recent places" },                   { id: 5, name: "libraries", hasChild: true },                   { id: 6, pid: 5, name: "Documents", hasChild: true },                   { id: 7, pid: 6, name: "My Documents" },                   { id: 8, pid: 6, name: "Public Documents" },                   { id: 9, pid: 5, name: "Pictures", hasChild: true },                   { id: 10, pid: 9, name: "My Pictures" },                   { id: 11, pid: 9, name: "Public Pictures" },                   { id: 12, pid: 5, name: "Music", hasChild: true },                   { id: 13, pid: 9, name: "My Music" },                   { id: 14, pid: 9, name: "Public Music" },                   { id: 15, pid: 5, name: "Subversion" },                   { id: 16, name: "Computer", hasChild: true },                   { id: 17, pid: 16, name: "Folder(C)" },                   { id: 18, pid: 16, name: "Folder(D)" },                   { id: 19, pid: 16, name: "Folder(F)" },                  ];</td></tr>
<tr>
<td>
<b>[JavaScript]</b>      $("#treeView"). ejTreeView ({            // mapping JSON Data Source with the fields property of TreeView                fields: { dataSource: localData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }                          });        });</td></tr>
</table>


<table>
<tr>
<td>
<b>[Model]</b><b>// Add the following data list to be bind in the controller page and define the corresponding data.</b><b>// Define local data source elements with  fields            </b>public class treeviewData    {       //TreeView data source should have Id, ParentId and Text as mandatory        public int Id { get; set; }       // ParentId takes the value of the parent nodes Id        public int Pid { get; set; }       //Text to be displayed in the TreeView node        public string Name { get; set; }       //Set to true if node has children        public bool HasChild { get; set; }          }<b>[Controller]</b>//Refer the Model in the controllerusing &lt;Applicationname&gt;.Models;public ActionResult Index()    {           List<treeviewData> localData = new List<treeviewData>();            localData.Add(new treeviewData{ id= 1, name= "Favorites", hasChild= true });            localData.Add(new treeviewData{ id= 2, pid= 1, name= "Desktop" });            localData.Add(new treeviewData{ id= 3, pid= 1, name= "Downloads" });            localData.Add(new treeviewData{ id = 4, pid = 1, name = "Recent places" });            localData.Add(new treeviewData{ id= 5, name= "libraries", hasChild= true });            localData.Add(new treeviewData{ id= 6, pid= 5, name= "Documents", hasChild= true });            localData.Add(new treeviewData{ id= 7, pid= 6, name= "My Documents" });            localData.Add(new treeviewData{ id= 8, pid= 6, name= "Public Documents" });            localData.Add(new treeviewData{ id= 9, pid= 5, name= "Pictures", hasChild= true });            localData.Add(new treeviewData{ id= 10, pid= 9, name= "My Pictures" });            localData.Add(new treeviewData{ id= 11, pid= 9, name= "Public Pictures" });            localData.Add(new treeviewData{ id= 12, pid= 5, name= "Music", hasChild= true });            localData.Add(new treeviewData{ id= 13, pid= 9, name= "My Music" });            localData.Add(new treeviewData{ id= 14, pid= 9, name= "Public Music" });            localData.Add(new treeviewData{ id= 15, pid= 5, name= "Subversion" });            localData.Add(new treeviewData{ id= 16, name= "Computer", hasChild= true });            localData.Add(new treeviewData{ id= 17, pid= 16, name= "Folder(C)" });            localData.Add(new treeviewData{ id= 18, pid= 16, name= "Folder(D)" });            localData.Add(new treeviewData{ id= 19, pid= 16, name= "Folder(F)" });                                                                                      ViewBag.datasource = localData;            return View();    }</td></tr>
<tr>
<td>
<b>[View]</b><b>// Map Local datasource to corresponding fields in TreeView control.</b>      @Html.EJ().TreeView("tree").TreeViewFields(s => s.Datasource((IEnumerable<treeviewData>)ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild"))</td></tr>
</table>


<table>
<tr>
<td>
<b>[CodeBehind- C#]</b><b>\\ Define local DataSource elements using the ID,parentID ,Text and HasChild fields in code behind and map the list data to DataSource property.</b>public partial class _Default : Page    {        protected void Page_Load(object sender, EventArgs e)        {          this.treeview.DataSource = new TreeLocalDataSource().GetTreeDataItems().ToList();        }    }    public class TreeLocalDataSource    {        public TreeLocalDataSource()        { }        public TreeLocalDataSource(int _id, int _parentid, string _text, string _hasChild)        {            this.ID = _id;            this.ParentID = _parentid;            this.Text = _text;            this.HasChild = _hasChild;        }        [Browsable(true)]        public int ID        {            get;            set;        }        [Browsable(true)]        public int ParentID        {            get;            set;        }        [Browsable(true)]        public string Text        {            get;            set;        }        [Browsable(true)]        public string HasChild        {            get;            set;        }        public List<TreeLocalDataSource> GetTreeDataItems()        {            List<TreeLocalDataSource> data = new List<TreeLocalDataSource>();            data.Add(new TreeLocalDataSource(1, 0, "Favorites", "true"));            data.Add(new TreeLocalDataSource(2, 1, "Desktop", ""));            data.Add(new TreeLocalDataSource(3, 1, "Downloads", ""));            data.Add(new TreeLocalDataSource(4, 1, "Recent places", ""));            data.Add(new TreeLocalDataSource(5, 0, "libraries", "true"));            data.Add(new TreeLocalDataSource(6, 5, "Documents", "true"));            data.Add(new TreeLocalDataSource(7, 6, "My Documents", ""));            data.Add(new TreeLocalDataSource(8, 6, "Public Documents", ""));            data.Add(new TreeLocalDataSource(9, 5, "Pictures", "true"));            data.Add(new TreeLocalDataSource(10, 9, "My Pictures", ""));            data.Add(new TreeLocalDataSource(11, 9, "Public Pictures", ""));            data.Add(new TreeLocalDataSource(12, 5, "Music", "true"));            data.Add(new TreeLocalDataSource(13, 9, "My Music", ""));            data.Add(new TreeLocalDataSource(14, 9, "Public Music", ""));            data.Add(new TreeLocalDataSource(15, 5, "Subversion", ""));            data.Add(new TreeLocalDataSource(16, 0, "Computer", "true"));            data.Add(new TreeLocalDataSource(17, 16, "Folder(C)", ""));            data.Add(new TreeLocalDataSource(18, 16, "Folder(D)", ""));            data.Add(new TreeLocalDataSource(19, 16, "Folder(F)", ""));            return data;        }<b>    }</b></td></tr>
<tr>
<td>
<b>[ASPX]</b><b>\\ In the Design page, assign the values for DataTextField, DataIdField, DataParentIdField, DataHasChildField.</b>  <ej:TreeView ID="treeview" runat="server" DataTextField="Text" DataIdField="ID"        DataParentIdField="ParentID" DataHasChildField="HasChild"><b>  &lt;/ej:TreeView&gt;</b></td></tr>
</table>


The output for **TreeView** control with **Local Data** binding is as follows.



![](data-binding-_images\data-binding-_img1.png)

_Figure_ _17__43__: TreeView with_ _local data-bin__ding_

## Remote Data

You can bind **TreeView** to **Remote Data** using **dataManager** and the query in fields is used to retrieve the data. **dataManager** supports the following types of data-binding: JSON, Web Services, oData. It uses two different classes; **ej.DataManager** for processing, and **ej.Query** for serving data. **ej.DataManager** communicates with data source and **ej.Query** generates data queries that are read by the **dataManager**. In the following link, how to create **dataManager** is explained in full detail.

[http://help.syncfusion.com/ug/js/default.htm#!Documents/createyourdatamanage.htm](http://help.syncfusion.com/ug/js/default.htm)

The following steps explain how you can bind remote data to **TreeView** control.

1. In the **HTML** page, add a **&lt;div&gt;** element to configure **TreeView.**

****

{% highlight html %}

**[HTML]**

      <div id="treeView"></div>



{% endhighlight %}



2. Define **dataManager** and assign remote data source to it. Here **dataManager** gets the remote web service and filters the data using **Query**. The **select** property of **ejQuery** is used to retrieve the specified columns from the data source.

****

{% highlight js %}

**[JavaScript]**

      // DataMangaer creation
        var dataManager = ej.DataManager ej. ({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        // query creation

        var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);




{% endhighlight %}

****

3. Assign **dataSource** and **query** property values to bind the remote data. Map the corresponding fields in **TreeView** control as follows.



{% highlight js %}

**[JavaScript]**
        $("#treeView").ejTreeView(
       {
           width: 300,
           height:300,
           fields: {
               dataSource: dataManager, query: query, id: "CategoryID", text: "CategoryName",
               child: { dataSource: dataManager, tableName: "Products", id: "ProductID", parentId: "CategoryID", text: "ProductName" }
           }
       }
   );


{% endhighlight %}



**[View]**



      @Html.EJ().TreeView("treeView").TreeViewFields(s => s.Datasource(s1 => s1.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).Query(" ej.Query().from('Categories').select('CategoryID,CategoryName').take(3)").Id("CategoryID").Text("CategoryName").Child(s2 => s2.Datasource(s3 => s3.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).TableName("Products").Id("ProductID").ParentId("CategoryID").Text("ProductName"))) 



**[ASPX]**



        $("#treeView").ejTreeView(

       {

           width: 300,

           height:300,

           fields: {

               dataSource: dataManager, query: query, id: "CategoryID", text: "CategoryName",

               child: { dataSource: dataManager, tableName: "Products", id: "ProductID", parentId: "CategoryID", text: "ProductName" }

           }

       }

   **);**



The output for **TreeView** control with **Remote Data** binding is as follows.



{% include image.html url="\js\TreeView\concepts-and-features\data-binding-_images\data-binding-_img2.png" Caption="Figure 4418: TreeView with remote data binding"%}

**SQL Data**

**TreeView** provides extensive data binding support to populate TreeView nodes, so that the values can be mapped to the TreeView fields from an existing SQL data source, using **DataSourceID** property. 

The following steps explain SQL data binding to TreeView.

1. Define an SQL data source in the web page and configure the data source as per your requirement. For the following code example an SQL data table is created.

The following image shows the sample database used.



<table>
<tr>
<td>
<img src="data-binding-_images\data-binding-_img3.png" alt="" width="245pt" height="109pt"</td><td>
<img src="data-binding-_images\data-binding-_img4.png" alt="" width="376pt" height="302pt"</td></tr>
</table>
_Figure_ _45__:_ _Database table structure_

1. In the **Design** page, assign the values for **DataTextField**, **DataIdField**, **DataParentIdField**, **DataHasChildField**. In **DataSourceID** field assign the ID of the existing SQL data source. 



**[ASPX]**



<ej:TreeView ID="TreeSQLDS" runat="server" DataSourceID="SqlDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded">

    &lt;/ej:TreeView&gt;

    &lt;div&gt;

        &lt;%--DataBase configured for TreeView control--%&gt;

        &lt;asp:SqlDataSource ID="SqlDataSource1" runat="server" ConnectionString="&lt;%$ ConnectionStrings:TreeDBConnectionString %&gt;"

            SelectCommand="SELECT * FROM [TreeBind]">&lt;/asp:SqlDataSource&gt;





The following image is the output for **TreeView** control with **SQL data binding**.



{% include image.html url="\js\TreeView\concepts-and-features\data-binding-_images\data-binding-_img5.png" Caption="Figure 46: TreeView with remote databinding"%}

**Object DataSource**

**TreeView** provides **ObjectDataSource** data binding support to populate **TreeView** nodes, so that the values can be mapped to the **TreeView** fields from an existing **ObjectDataSource**, using **DataSourceID** property. 

The following steps explain the **ObjectDataSource** data binding to TreeView.

1. Define an **ObjectDataSource** in the web page and configure the data source elements. Add the class file to App_Data folder in your web application.



**[C#]**

namespace ASPWebTreeView

{

    public class TreeObjectDataSource

    {



        public TreeObjectDataSource()

        { }

        public TreeObjectDataSource(int _id, int _parentid, string _text, string _hasChild, string _expanded)

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

        public int ParentID

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

        public List<TreeObjectDataSource> GetTreeDataItems()

        {

            List<TreeObjectDataSource> data = new List<TreeObjectDataSource>();



            data.Add(new TreeObjectDataSource(1, 0, "Favorites", "true", "true"));

            data.Add(new TreeObjectDataSource(2, 1, "Desktop", "", ""));

            data.Add(new TreeObjectDataSource(3, 1, "Downloads", "", ""));

            data.Add(new TreeObjectDataSource(4, 1, "Recent places", "", ""));

            data.Add(new TreeObjectDataSource(5, 0, "libraries", "true", ""));

            data.Add(new TreeObjectDataSource(6, 5, "Documents", "true", ""));

            data.Add(new TreeObjectDataSource(7, 6, "My Documents", "", ""));

            data.Add(new TreeObjectDataSource(8, 6, "Public Documents", "", ""));

            data.Add(new TreeObjectDataSource(9, 5, "Pictures", "true", ""));

            data.Add(new TreeObjectDataSource(10, 9, "My Pictures", "", ""));

            data.Add(new TreeObjectDataSource(11, 9, "Public Pictures", "", ""));

            data.Add(new TreeObjectDataSource(12, 5, "Music", "true", ""));

            data.Add(new TreeObjectDataSource(13, 9, "My Music", "", ""));

            data.Add(new TreeObjectDataSource(14, 9, "Public Music", "", ""));

            data.Add(new TreeObjectDataSource(15, 5, "Subversion", "", ""));

            data.Add(new TreeObjectDataSource(16, 0, "Computer", "true", ""));

            data.Add(new TreeObjectDataSource(17, 16, "Folder(C)", "", ""));

            data.Add(new TreeObjectDataSource(18, 16, "Folder(D)", "", ""));

            data.Add(new TreeObjectDataSource(19, 16, "Folder(F)", "", ""));

            return data;

        }

    } 

}



2. In the **Design** page, assign the values for **DataTextField**, **DataIdField**, **DataParentIdField**, **DataHasChildField**.In **DataSourceID** field assign the ID of the existing ObjectDataSource.



**[ASPX]**



    <ej:TreeView ID="Treeview" runat="server" DataSourceID="ObjectDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded">

    &lt;/ej:TreeView&gt;

    &lt;div&gt;

         &lt;%--DataBase configured for TreeView control--%&gt;



        &lt;asp:ObjectDataSource ID="ObjectDataSource1" runat="server" TypeName=" ASPWebTreeView.TreeObjectDataSource" SelectMethod="GetTreeDataItems"&gt;

&lt;/asp:ObjectDataSource&gt;



3. The following image is the output for **TreeView** control with **ObjectDataSource****data binding**.



{% include image.html url="\js\TreeView\concepts-and-features\data-binding-_images\data-binding-_img6.png" Caption="Figure 47: TreeView with remote databinding"%}

**Linq-to-SQL Data**

**TreeView** provides extensive data binding support to populate TreeView nodes, so that the values can be mapped to the **TreeView** fields from an existing **Linq-to-SQL** data source, using **DataSourceID** property. 

The following steps explain the SQL data binding to TreeView textbox.

1. Define a Linq-to-SQL data source in the web page and configure the data source asyou’re your requirement using the database. In the following sample code, an SQL table is used to create a DBML class.



<table>
<tr>
<td>
<img src="data-binding-_images\data-binding-_img7.png" alt="" width="245pt" height="109pt"</td><td>
<img src="data-binding-_images\data-binding-_img8.png" alt="" width="376pt" height="302pt"</td></tr>
</table>
_Figure_ _48__:_ _DataBase table structure used in Linq-to-SQL cla__ss_



2. In the **Design** page, assign values for **DataTextField**, **DataIdField**, **DataParentIdField**, **DataHasChildField**. In **DataSourceID** field assign the ID of the existing Linq-to-SQL data source.



**[ASPX]**



<ej:TreeView ID="TreeLinqToSql" runat="server" DataSourceID="LinqDataSource1" DataTextField="Text" DataIdField="ID"

        DataParentIdField="ParentID" DataHasChildField="HasChild" DataExpandedField="Expanded">

    &lt;/ej:TreeView&gt;

    &lt;div&gt;

        &lt;asp:LinqDataSource ID="LinqDataSource1" runat="server" ContextTypeName="ASPweb.TreeView.Tree_Linq_To_SqlDataContext" EntityTypeName="" TableName="TreeLinqs"&gt;

        &lt;/asp:LinqDataSource&gt;



3. The following image is the output for TreeView control with **Linq-to-SQL****data binding**.



{% include image.html url="\js\TreeView\concepts-and-features\data-binding-_images\data-binding-_img9.png" Caption="Figure 49: TreeView with remote databinding"%}

**XML Data**

TreeView provides XML data binding support to populate TreeeView nodes, so that the values can be mapped to the **TreeView** fields from an existing XML data, using **DataSourceID** property. 

The following steps explain the **XML** data binding to **TreeView**.

1. In the **Design** page, assign the values for **DataTextField**, **DataParentIdField**. In **DataSourceID** field assign the ID of the existing XML datasource.



**[ASPX]**



    <ej:TreeView ID="TreeXmlDS" runat="server" DataSourceID="XmlDataSource1"

        DataTextField="Item" DataParentIdField="RootItem">

    &lt;/ej:TreeView&gt;



    &lt;div&gt;

        &lt;asp:XmlDataSource ID="XmlDataSource1" runat="server" DataFile="~\App_Data\XMLData.xml"&gt;&lt;/asp:XmlDataSource&gt;

    &lt;/div&gt;





2. Load the nodes of **TreeView** in the xml data as follows.



**[XMLData.xml]**



&lt;?xml version="1.0" encoding="utf-8" ?&gt;

&lt;Items&gt;

  &lt;RootItem Text="Favorites" Url="#"&gt;

    &lt;Item Text="Desktop" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Downloads" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Recent places" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Libraries" Url="#"&gt;

    &lt;RootItem Text="Documents" Url="#"&gt;

      &lt;Item Text="My Documents" Url="#"&gt;&lt;/Item&gt;

      &lt;Item Text="Public Documents" Url="#"&gt;&lt;/Item&gt;

    &lt;/RootItem&gt;

    &lt;RootItem Text="Pictures" Url="#"&gt;

      &lt;Item Text="My Pictures" Url="#"&gt;&lt;/Item&gt;

      &lt;Item Text="Public Pictures" Url="#"&gt;&lt;/Item&gt;

    &lt;/RootItem&gt;

    &lt;RootItem Text="Music" Url="#"&gt;

      &lt;Item Text="My Music" Url="#"&gt;&lt;/Item&gt;

      &lt;Item Text="Public Music" Url="#"&gt;&lt;/Item&gt;

    &lt;/RootItem&gt;

  &lt;/RootItem&gt;



  &lt;RootItem Text="Computer" Expanded="True" Url="#"&gt;

    &lt;Item Text="Folder(C)" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Folder(D)" Url="#"&gt;&lt;/Item&gt;

    &lt;Item Text="Folder(F)" Url="#"&gt;&lt;/Item&gt;

  &lt;/RootItem&gt;

&lt;/Items&gt;



3. The following image is the output for TreeView control with **XML data binding**.         

{% include image.html url="\js\TreeView\concepts-and-features\data-binding-_images\data-binding-_img10.png" Caption="Figure 50: TreeView with remote databinding"%}

