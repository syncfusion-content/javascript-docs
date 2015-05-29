---
layout: post
title: load-on-demand
description: load on demand
platform: js
control: TreeView
documentation: ug
---

# Load on Demand

**Load****on Demand** option is useful when the full content of the **TreeView** is too large to be loaded completely, up front. The mechanism lets the nodes load their child nodes as you expand the parent by clicking the **expand****icon**. While clicking on the parent node it first loads their particular child nodes and then loads the first level of nodes.

This feature is used reduce the loading time of the large number nodes in **TreeView**. For example, when you are using the **TreeView** with 10,000 nodes or greater, it takes a long time to load their child nodes. In this case, **Load on Demand** is used to load the particular part of child nodes when you click their parent node. Hence it reduces the loading time of **TreeView.**

To enable **load on demand**, set the appropriate value for the **loadOnDemand** property.

The following steps explain how to enable the **loadOnDemand** property for **TreeView**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **TreeView.**

****

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="treeView"&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// Define local data source elements with fields.</b>              var localData = [                   { id: 1, name: "Favorites", hasChild: true },                   { id: 2, pid: 1, name: "Desktop" },                   { id: 3, pid: 1, name: "Downloads" },                   { id: 4, pid: 1, name: "Recent places" },                   { id: 5, name: "libraries", hasChild: true },                   { id: 6, pid: 5, name: "Documents", hasChild: true },                   { id: 7, pid: 6, name: "My Documents" },                   { id: 8, pid: 6, name: "Public Documents" },                   { id: 9, pid: 5, name: "Pictures", hasChild: true },                   { id: 10, pid: 9, name: "My Pictures" },                   { id: 11, pid: 9, name: "Public Pictures" },                   { id: 12, pid: 5, name: "Music", hasChild: true },                   { id: 13, pid: 9, name: "My Music" },                   { id: 14, pid: 9, name: "Public Music" },                   { id: 15, pid: 5, name: "Subversion" },                   { id: 16, name: "Computer", hasChild: true },                   { id: 17, pid: 16, name: "Folder(C)" },                   { id: 18, pid: 16, name: "Folder(D)" },                   { id: 19, pid: 16, name: "Folder(F)" },        ];</td></tr>
<tr>
<td>
            <b>[JavaScript]</b><b>// Map local data source to corresponding fields and enable loadOnDemand for TreeView control as follows.</b>            $("#treeView").ejTreeView({                <b>loadOnDemand</b>: true,                fields: { dataSource: localData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }            });</td></tr>
</table>


<table>
<tr>
<td>
<b>[Model]</b><b>// Define local data source elements with  fields            </b>public class treeviewData    {       //TreeView data source should have Id, ParentId and Text as mandatory        public int Id { get; set; }       // ParentId takes the value of the parent nodes Id        public int Pid { get; set; }       //Text to be displayed in the TreeView node        public string Name { get; set; }       //Set to true if node has children        public bool HasChild { get; set; }          }<b>[Controller]</b>//Refer the Model in the controllerusing &lt;Applicationname&gt;.Models;public ActionResult Index()    {            List<treeviewData> localData = new List<treeviewData>();            localData.Add(new treeviewData{ id= 1, name= "Favorites", hasChild= true });            localData.Add(new treeviewData{ id= 2, pid= 1, name= "Desktop" });            localData.Add(new treeviewData{ id= 3, pid= 1, name= "Downloads" });            localData.Add(new treeviewData{ id = 4, pid = 1, name = "Recent places" });            localData.Add(new treeviewData{ id= 5, name= "libraries", hasChild= true });            localData.Add(new treeviewData{ id= 6, pid= 5, name= "Documents", hasChild= true });            localData.Add(new treeviewData{ id= 7, pid= 6, name= "My Documents" });            localData.Add(new treeviewData{ id= 8, pid= 6, name= "Public Documents" });            localData.Add(new treeviewData{ id= 9, pid= 5, name= "Pictures", hasChild= true });            localData.Add(new treeviewData{ id= 10, pid= 9, name= "My Pictures" });            localData.Add(new treeviewData{ id= 11, pid= 9, name= "Public Pictures" });            localData.Add(new treeviewData{ id= 12, pid= 5, name= "Music", hasChild= true });            localData.Add(new treeviewData{ id= 13, pid= 9, name= "My Music" });            localData.Add(new treeviewData{ id= 14, pid= 9, name= "Public Music" });            localData.Add(new treeviewData{ id= 15, pid= 5, name= "Subversion" });            localData.Add(new treeviewData{ id= 16, name= "Computer", hasChild= true });            localData.Add(new treeviewData{ id= 17, pid= 16, name= "Folder(C)" });            localData.Add(new treeviewData{ id= 18, pid= 16, name= "Folder(D)" });            localData.Add(new treeviewData{ id= 19, pid= 16, name= "Folder(F)" });                                                                                      ViewBag.datasource = localData;            return View();   }</td></tr>
<tr>
<td>
<b>[View]</b><b>// Map Local datasource to corresponding fields and enable LoadOnDemand for TreeView control</b>@Html.EJ().TreeView("tree").TreeViewFields(s => s.Datasource((IEnumerable<treeviewData>)ViewBag.datasource).Id("id").ParentId("pid").Text("name").HasChild("hasChild")).<b>LoadOnDemand(true)</b> </td></tr>
</table>


<table>
<tr>
<td>
<b>[CodeBehind- C#]</b><b>\\ Define local DataSource elements using the ID,parentID ,Text and HasChild fields in code behind and map the list data to DataSource property.</b>public partial class LoadOnDemand : System.Web.UI.Page    {        protected void Page_Load(object sender, EventArgs e)        {            this.treeview.DataSource = new TreeOnDemandDataSource().GetTreeItems().ToList();        }    }    public class TreeOnDemandDataSource    {        public TreeOnDemandDataSource(int _id, int _parentid, string _text, string _hasChild)        {            this.ID = _id;            this.ParentID = _parentid;            this.Text = _text;            this.HasChild = _hasChild;        }        public TreeOnDemandDataSource()        { }        [Browsable(true)]        public int ID        {            get;            set;        }        [Browsable(true)]        public int ParentID        {            get;            set;        }        [Browsable(true)]        public string Text        {            get;            set;        }        [Browsable(true)]        public string HasChild        {            get;            set;        }        public List<TreeOnDemandDataSource> GetTreeItems()        {            List<TreeOnDemandDataSource> data = new List<TreeOnDemandDataSource>();            data.Add(new TreeOnDemandDataSource(1, 0, "Favorites", "true"));            data.Add(new TreeOnDemandDataSource(2, 1, "Desktop", ""));            data.Add(new TreeOnDemandDataSource(3, 1, "Downloads", ""));            data.Add(new TreeOnDemandDataSource(4, 1, "Recent places", ""));            data.Add(new TreeOnDemandDataSource(5, 0, "libraries", "true"));            data.Add(new TreeOnDemandDataSource(6, 5, "Documents", "true"));            data.Add(new TreeOnDemandDataSource(7, 6, "My Documents", ""));            data.Add(new TreeOnDemandDataSource(8, 6, "Public Documents", ""));            data.Add(new TreeOnDemandDataSource(9, 5, "Pictures", "true"));            data.Add(new TreeOnDemandDataSource(10, 9, "My Pictures", ""));            data.Add(new TreeOnDemandDataSource(11, 9, "Public Pictures", ""));            data.Add(new TreeOnDemandDataSource(12, 5, "Music", "true"));            data.Add(new TreeOnDemandDataSource(13, 9, "My Music", ""));            data.Add(new TreeOnDemandDataSource(14, 9, "Public Music", ""));            data.Add(new TreeOnDemandDataSource(15, 5, "Subversion", ""));            data.Add(new TreeOnDemandDataSource(16, 0, "Computer", "true"));            data.Add(new TreeOnDemandDataSource(17, 16, "Folder(C)", ""));            data.Add(new TreeOnDemandDataSource(18, 16, "Folder(D)", ""));            data.Add(new TreeOnDemandDataSource(19, 16, "Folder(F)", ""));            return data;        }<b>    }</b></td></tr>
<tr>
<td>
<b>[ASPX]</b><b>\\ In the Design page, assign the values for DataTextField, DataIdField, DataParentIdField, DataHasChildField.</b>  <ej:TreeView ID="treeview" runat="server" DataTextField="Text" DataIdField="ID"        DataParentIdField="ParentID" DataHasChildField="HasChild"><b>    &lt;/ej:TreeView&gt;</b></td></tr>
</table>


The output for **TreeView** when **loadOnDemand** is set to “**True**” is as follows.



{% include image.html url="\js\TreeView\concepts-and-features\load-on-demand_images\load-on-demand_img1.png" Caption="Figure 519: TreeView with loadOnDemand"%}{% include image.html url="\js\TreeView\concepts-and-features\load-on-demand_images\load-on-demand_img2.png" Caption="Figure 519: TreeView with loadOnDemand"%}

