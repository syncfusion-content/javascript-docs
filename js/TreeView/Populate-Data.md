---
layout: post
title: Populate-Data
description: populate data 
platform: js
control: TreeView
documentation: ug
api: /api/js/ejtreeview
---


# Populate Data

TreeView can be populated with local or remote data source by using a property [dataSource](https://help.syncfusion.com/api/js/ejtreeview#members:fields-datasource), which is the member of [fields](https://help.syncfusion.com/api/js/ejtreeview#members:fields) property.

In TreeView, you should use “**fields**” property to go with data source. It specifies the mapping fields for the data source to receive the data, query to process the data and field mappers to map the data members.

## Fields

The following table contains the list of members with description for **fields** property.

<table>
<tr>
<th>
Properties</th><th>
Description</th></tr>
<tr>
<td>
{{'[dataSource](https://help.syncfusion.com/api/js/ejtreeview#members:fields-datasource)'| markdownify }}<br/><br/></td><td>
The data source contains the list of data for generating the TreeView list.<br/><br/></td></tr>
<tr>
<td>
{{'[query](https://help.syncfusion.com/api/js/ejtreeview#members:fields-query)'| markdownify }}<br/><br/></td><td>
It specifies the query to retrieve the data from the online server.<br/><br/></td></tr>
<tr>
<td>
{{'[tableName](https://help.syncfusion.com/api/js/ejtreeview#members:fields-tablename)'| markdownify }}<br/><br/></td><td>
It specifies the name of the table from which data to be processed from given data source.<br/><br/></td></tr>
<tr>
<td>
{{'[id](https://help.syncfusion.com/api/js/ejtreeview#members:fields-id)'| markdownify }}<br/><br/></td><td>
It specifies the ID of the node.<br/><br/></td></tr>
<tr>
<td>
{{'[parentId](https://help.syncfusion.com/api/js/ejtreeview#members:fields-parentid)'| markdownify }}<br/><br/></td><td>
It specifies the parent id of the node<br/><br/></td></tr>
<tr>
<td>
{{'[text](https://help.syncfusion.com/api/js/ejtreeview#members:fields-text)'| markdownify }}<br/><br/></td><td>
It specifies the text content of the node.<br/><br/></td></tr>
<tr>
<td>
{{'[hasChild](https://help.syncfusion.com/api/js/ejtreeview#members:fields-haschild)'| markdownify }}<br/><br/></td><td>
It specifies the node has child (which is the nested or inner level of nodes). Also it’s used in load on demand of tree data.<br/><br/></td></tr>
<tr>
<td>
{{'[expanded](https://help.syncfusion.com/api/js/ejtreeview#members:fields-expanded)'| markdownify }}<br/><br/></td><td>
It specifies the tree node to be in expanded state<br/><br/></td></tr>
<tr>
<td>
{{'[selected](https://help.syncfusion.com/api/js/ejtreeview#members:fields-selected)'| markdownify }}<br/><br/></td><td>
It specifies the select node at initialize. N> only one node get selected by default. If you enable multiple selection in TreeView then you can able to select one or more nodes at initialize.<br/><br/></td></tr>
<tr>
<td>
{{'[isChecked](https://help.syncfusion.com/api/js/ejtreeview#members:fields-ischecked)'| markdownify }} <br/><br/></td><td>
It specifies the node to be in checked state, if tree node represented with checkboxes. <br/><br/></td></tr>
<tr>
<td>
{{'[imageUrl](https://help.syncfusion.com/api/js/ejtreeview#members:fields-imageurl)'| markdownify }}<br/><br/></td><td>
It defines the image location.<br/><br/></td></tr>
<tr>
<td>
{{'[imageAttribute](https://help.syncfusion.com/api/js/ejtreeview#members:fields-imageattribute)'| markdownify }}<br/><br/></td><td>
It defines the image attributes such as height, width, styles, etc.<br/><br/></td></tr>
<tr>
<td>
{{'[spriteCssClass](https://help.syncfusion.com/api/js/ejtreeview#members:fields-spritecssclass)'| markdownify }}<br/><br/></td><td>
It defines the sprite CSS for the image tag.<br/><br/></td></tr>
<tr>
<td>
{{'[htmlAttribute](https://help.syncfusion.com/api/js/ejtreeview#members:fields-htmlattribute)'| markdownify }}<br/><br/></td><td>
It defines the HTML attributes such as class and styles for a node ("li" tag).<br/><br/></td></tr>
<tr>
<td>
{{'[linkAttribute](https://help.syncfusion.com/api/js/ejtreeview#members:fields-linkattribute)'| markdownify }}<br/><br/></td><td>
It defines the HTML attributes such as class and styles for a link tag, which is child of node.<br/><br/></td></tr>
</table>
Mapping all fields members with corresponding key from the array of JSON data.

{% highlight js %}

        var localData = [

       { id: 1, text: "Item 1", expanded: true, nodeProperty: { class: "textBlue", value: "Item 1" } },

       { id: 2, text: "Item 2", linkProperty: { class: "textUnderline", href: "http://www.syncfusion.com", target: "_blank" } },

       { id: 3, text: "Item 3", selected: true, spriteImage: "mailicon sprite-calendar" },

       { id: 4, text: "Item 4", checked: true, imageProperty: { width: 20, height: 20 }, imageUrl: "http://cdn.syncfusion.com/13.3.0.7/js/web/flat-azure/images/ajax-loader.gif" },

       { id: 5, parent: 1, text: "Item 1.1" },

       { id: 6, parent: 1, text: "Item 1.2" },

       { id: 7, parent: 1, text: "Item 1.3" },

       { id: 8, parent: 3, text: "Item 3.1" },

       { id: 9, parent: 3, text: "Item 3.2" },

       { id: 10, parent: 5, text: "Item 1.1.1" }

        ];

        $(function () {

            $("#treeView").ejTreeView(

            {

                showCheckbox: true,

                fields: {

                    id: "id",

                    text: "text",

                    parentId: "parent",

                    dataSource: localData,

                    isChecked: "checked",

                    selected: "selected",

                    spriteCssClass: "spriteImage",

                    imageUrl: "imageUrl",

                    htmlAttribute: "nodeProperty",

                    linkAttribute: "linkProperty",

                    imageAttribute: "imageProperty"

                }

            });

        });

{% endhighlight %}

N>  If you want to display nodes in Root level, exclude **parentId** attribute or specify **“0”** in corresponding value.

To find the complete details about fields, refer the sample [here](http://jsplayground.syncfusion.com/iyhtz2bm#).

## Local Data

TreeView can be rendered from a self-referential data by providing the two required fields [id](https://help.syncfusion.com/api/js/ejtreeview#members:fields-id) and [parentId](https://help.syncfusion.com/api/js/ejtreeview#members:fields-parentid). 

{% highlight js %}

        var localData = [

        { id: 1, text: "Item 1" },

        { id: 2, text: "Item 2" },

        { id: 3, text: "Item 3" },

        { id: 4, text: "Item 4" },

        { id: 5, parent: 1, text: "Item 1.1" }                

        ];

{% endhighlight %}

Above flat array of JSON data can be directly assigned to [dataSource](https://help.syncfusion.com/api/js/ejtreeview#members:fields-datasource) property and mapping data fields with respect to the mapper field in order to create TreeView.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var localData = [

        { id: 1, text: "Item 1" },

        { id: 2, text: "Item 2" },

        { id: 3, text: "Item 3" },

        { id: 4, text: "Item 4" },

        { id: 5, parent: 1, text: "Item 1.1" },

        { id: 6, parent: 1, text: "Item 1.2" },

        { id: 7, parent: 1, text: "Item 1.3" },

        { id: 8, parent: 3, text: "Item 3.1" },

        { id: 9, parent: 3, text: "Item 3.2" },

        { id: 10, parent: 5, text: "Item 1.1.1" }

        ];

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });

{% endhighlight %}

### Nested Object Support

The nested object support is provided for the TreeView component. Please find the following JSON.

{% highlight js %}

        var localData = [
          { id: 1, name: { nodeName: "Discover Music"}, hasChild: true, expanded: true },
          { id: 2, pid: 1, name: {nodeName:"Hot Singles" }},
          { id: 3, pid: 1, name: {nodeName:"Rising Artists" }},
          { id: 4, pid: 1, name:{nodeName: "Live Music" }}];

        $(function () {

            // initialize and bind the TreeView with local data with nested object

            $("#treeView").ejTreeView({
               fields: { id: "id", parentId: "pid", text: "name.nodeName", hasChild: "hasChild", dataSource: localData, expanded: "expanded" }}
            );
        });

{% endhighlight %}

The above flat array of JSON data can be directly assigned to the [dataSource](https://help.syncfusion.com/api/js/ejtreeview#members:fields-datasource) property and mapping nested data fields with respect to the mapper field to create the TreeView. The sample is in the following location.

[Sample](http://jsplayground.syncfusion.com/j4040dpu)

## Remote Data

When using remote data binding, the adaptor of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager#) plays vital role in processing queries to make them suitable to sends along with data request and also process the response data from the server.

### OData

**OData** is a standardized protocol for creating and consuming data. You can bind [oData service](http://www.odata.org/#) data to TreeView in two ways using DataManager.

* Passing OData service link to DataManager

You can provide the OData service URL directly to the [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager#) class and then we can assign it to TreeView dataSource.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var parentData = ej.DataManager("//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Categories"),

        childData = ej.DataManager("//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Products");

        $(function () {

            // initialize and bind the TreeView with Remote data

            $("#treeView").ejTreeView({

                fields: {

                    dataSource: parentData,

                    id: "CategoryID", text: "CategoryName",

                    child: {

                        dataSource: childData,

                        id: "ProductID", parentId: "CategoryID", text: "ProductName"

                    }

                }

            });

        });

{% endhighlight %}

* Passing OData service link to “**url**” property of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager#)

By using “**url**” property of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager#) we can bind OData Service to Dropdown. Here we may also specify the **adaptor** as [ej.ODataAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#odata-adaptor) and it is optional to specify.

We can provide adaptor value either as string value (“ODataAdaptor”) or by creating a new instance (new [ej.ODataAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#odata-adaptor))

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var dataManager = ej.DataManager({

            url: "//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Categories",

            adaptor: new ej.ODataAdaptor()

        });

        $(function () {

            // initialize and bind the TreeView with Remote data

            $("#treeView").ejTreeView({

                fields: {

                    dataSource: dataManager,

                    query: ej.Query().select("CategoryID , CategoryName").take(3),

                    id: "CategoryID", text: "CategoryName",

                    child: {

                        dataSource: ej.DataManager({

                            url: "//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Products"

                        }),

                        id: "ProductID", parentId: "CategoryID", text: "ProductName"

                    }

                }

            });

        });

{% endhighlight %}

N>  We can use above code until OData service version 3. For OData Service version 4 End Point, we have created a separate adaptor [ej.ODataV4Adaptor](https://help.syncfusion.com/js/datamanager/data-binding#odata-v4) for data binding.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var dataManager = ej.DataManager({

            url: "//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Categories",

            adaptor: new ej.ODataV4Adaptor()

        });

        $(function () {

            // initialize and bind the TreeView with Remote data

            $("#treeView").ejTreeView({

                fields: {

                    dataSource: dataManager,

                    query: ej.Query().select("CategoryID , CategoryName").take(3),

                    id: "CategoryID", text: "CategoryName",

                    child: {

                        dataSource: ej.DataManager({

                            url: "//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/Products"

                        }),

                        id: "ProductID", parentId: "CategoryID", text: "ProductName"

                    }

                }

            });

        });

{% endhighlight %}

### WebApi

Using [ej.WebApiAdaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#webapi-adaptor), you can bind WebApi service data to TreeView as shown in below code example

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            var dataManager = ej.DataManager({

                url: "http://js.syncfusion.com/demos/ejServices/api/TreeViewData/GetAllData",

                crossDomain: true,

                adaptor: new ej.WebApiAdaptor()

            });

            $("#treeView").ejTreeView({

                fields: {

                    dataSource: dataManager,

                    id: "id", text: "name", parentId: "pid",

                }

            });

        });

{% endhighlight %}

### Other Restful Web Services

The Custom Adaptor concept of [ej.DataManager](https://help.syncfusion.com/api/js/ejdatamanager#) allow you to customize or generate your own adaptor which is used to process query and result data. 

[https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor](https://help.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor)

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            window.treeData = [

            { id: 1, text: "Item 1" },

            { id: 2, text: "Item 2" },

            { id: 3, text: "Item 3" },

            { id: 4, text: "Item 4" }

            ];

            //custom adaptor

            var customAdaptor = new ej.Adaptor().extend({

                insert: function (dataObj, data) {

                    return dataObj.dataSource.json.push(data);

                },

                processQuery: ej.JsonAdaptor.prototype.processQuery // reused process query from JSON adaptor

            });

            var dataManager = new ej.DataManager(window.treeData);

            // assigning custom adaptor to datamanager

            dataManager.adaptor = new customAdaptor();

            // insert from custom adaptor usage

            dataManager.insert({ id: 5, text: "Item 1.1", parent: 1 });

            $('#treeView').ejTreeView({

                fields: { dataSource: dataManager, id: "id", parentId: "parent", text: "text" }

            });

        });

{% endhighlight %}

## Load on Demand

Load on demand is a technique (Lazy load) that is used to reduce the bandwidth size of consuming huge data. You can load data on demand in TreeView by using [loadOnDemand](https://help.syncfusion.com/api/js/ejtreeview#members:loadOnDemand) property when you’re going to use huge data.

For local data source, TreeView loads the first level nodes initially. While expand a parent node then TreeView loads it’s their child nodes from the data source based on the parentId member. It reduces the time to render TreeView with huge data.

Refer below code example to load data on demand from local data source.

{% highlight html %}

<!--create the TreeView wrapper-->

<div id="treeview"></div>

{% endhighlight %}

{% highlight js %}

var localData = [
    { id: 1, name: "Local Disk(C:)", hasChild: true },
    { id: 2, name: "Local Disk(D:)", hasChild: true },
    { id: 3, name: "Local Disk(E:)", hasChild: true },
    { id: 4, parentId: 1, name: "Folder 1", hasChild: true },
    { id: 5, parentId: 1, name: "Folder 2" },
    { id: 6, parentId: 1, name: "Folder 3" },
    { id: 7, parentId: 2, name: "Folder 4" },
    { id: 8, parentId: 2, name: "Folder 5", hasChild: true },
    { id: 9, parentId: 2, name: "Folder 6" },
    { id: 10, parentId: 3, name: "Folder 7" },
    { id: 11, parentId: 3, name: "Folder 8" },
    { id: 12, parentId: 3, name: "Folder 9", hasChild: true },
    { id: 13, parentId: 4, name: "File 1" },
    { id: 14, parentId: 4, name: "File 2" },
    { id: 15, parentId: 4, name: "File 3" },
    { id: 16, parentId: 8, name: "File 4" },
    { id: 17, parentId: 8, name: "File 5" },
    { id: 18, parentId: 8, name: "File 6" },
    { id: 19, parentId: 12, name: "File 7" },
    { id: 20, parentId: 12, name: "File 8" },
    { id: 21, parentId: 12, name: "File 9" }
];
$(function () {
    $("#treeview").ejTreeView({
        loadOnDemand: true,
        fields: { dataSource: localData, id: "id", parentId: "parentId", text: "name", hasChild: "hasChild" },
    });
});

{% endhighlight %}

The following screenshot displays the load on demand for local data source in TreeView control.

![](/js/TreeView/Populate-Data_images/Populate-Data_img1.png)

While expanding the parent node
{:.caption}

![](/js/TreeView/Populate-Data_images/Populate-Data_img2.png)

After expanding the parent node
{:.caption}

For more details about load on demand for local data source, refer the sample [here](http://jsplayground.syncfusion.com/5mnzloq0).


For remote data source, TreeView loads the first level nodes initially. While expand the node from TreeView, the data manager passes the query to the controller. Based on this query, you can filter the data from table and return to TreeView.

Refer below code example to load data on demand from remote data source.

{% highlight html %}

<!--create the TreeView wrapper-->

<div id="treeview"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
    // DataManager creation
    var dataManger = ej.DataManager({
        url: "//js.syncfusion.com/demos/ejServices/Wcf/Northwind.svc/"
    });
    // Query creation
    var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);
    $("#treeview").ejTreeView({
        loadOnDemand: true,
        fields: {
            dataSource: dataManger, query: query, id: "CategoryID", text: "CategoryName", hasChild: "CategoryName",
            child: { dataSource: dataManger, tableName: "Products", parentId: "CategoryID", text: "ProductName" }
        }
    });
});

{% endhighlight %}

For more details about load on demand for remote data source, refer the sample [here](http://jsplayground.syncfusion.com/fgln2q3v).


For URL Adaptor, TreeView loads the first level nodes initially. While expand the node from TreeView, the data manager passes the Data Manager instance to the controller. The Data Manager instance contains the parent Id and filter options. Based on the Data Manager instance, you can filter the data from data source and return to TreeView.

Refer below code example to load data on demand with URL adaptor.

{% highlight html %}

<!--create the TreeView wrapper-->

<div id="treeview"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
    window.dataManger = ej.DataManager({
        url:"/home/Data",
        adaptor: new ej.UrlAdaptor(),
        crossDomain: true,
    });
    window.fields = {
        dataSource: dataManger, text: "name", parentId: "parentId", hasChild: "hasChild"
    }
    $("#treeview").ejTreeView({
        loadOnDemand: true,
        fields: fields,
    });
});

{% endhighlight %}

{% highlight c# %}

public class HomeController : Controller
{

    public ActionResult Index()
    {
        return View();
    }

    public JsonResult Data(DataManager dataManagerObj)
    {
        List<loadOnDemand> treeData = GetTreeData();
        IEnumerable<loadOnDemand> results;
        if (dataManagerObj.Where == null)
        {
            //return the first level nodes
            results = treeData.Where(item => item.parentId == null);
        }
        else
        {
            //return the nodes which has parentId as you request
            results = treeData.Where(s => s.parentId == Convert.ToInt32(dataManagerObj.Where[0].value));
        }
        return Json(results, JsonRequestBehavior.AllowGet);
    }

    List<loadOnDemand> data = new List<loadOnDemand>();

    public List<loadOnDemand> GetTreeData()
    {
        data.Add(new loadOnDemand { id = 1, name = "Local Disk(C:)", hasChild = true });
        data.Add(new loadOnDemand { id = 2, name = "Local Disk(D:)", hasChild = true });
        data.Add(new loadOnDemand { id = 3, name = "Local Disk(E:)", hasChild = true });
        data.Add(new loadOnDemand { id = 4, parentId = 1, name = "Folder 1", hasChild = true });
        data.Add(new loadOnDemand { id = 5, parentId = 1, name = "Folder 2" });
        data.Add(new loadOnDemand { id = 6, parentId = 1, name = "Folder 3" });
        data.Add(new loadOnDemand { id = 7, parentId = 2, name = "Folder 4" });
        data.Add(new loadOnDemand { id = 8, parentId = 2, name = "Folder 5", hasChild = true });
        data.Add(new loadOnDemand { id = 9, parentId = 2, name = "Folder 6" });
        data.Add(new loadOnDemand { id = 10, parentId = 3, name = "Folder 7" });
        data.Add(new loadOnDemand { id = 11, parentId = 3, name = "Folder 8" });
        data.Add(new loadOnDemand { id = 12, parentId = 3, name = "Folder 9", hasChild = true });
        data.Add(new loadOnDemand { id = 13, parentId = 4, name = "File 1" });
        data.Add(new loadOnDemand { id = 14, parentId = 4, name = "File 2" });
        data.Add(new loadOnDemand { id = 15, parentId = 4, name = "File 3" });
        data.Add(new loadOnDemand { id = 16, parentId = 8, name = "File 4" });
        data.Add(new loadOnDemand { id = 17, parentId = 8, name = "File 5" });
        data.Add(new loadOnDemand { id = 18, parentId = 8, name = "File 6" });
        data.Add(new loadOnDemand { id = 19, parentId = 12, name = "File 7" });
        data.Add(new loadOnDemand { id = 20, parentId = 12, name = "File 8" });
        data.Add(new loadOnDemand { id = 21, parentId = 12, name = "File 9" });
        return data;
    }
}

public class loadOnDemand
{
    public int id { get; set; }
    public int? parentId { get; set; }
    public string name { get; set; }
    public bool? hasChild { get; set; }
    public bool? expanded { get; set; }
    public bool? ischecked { get; set; }
    public bool? selected { get; set; }
    public string spriteCss { get; set; }
}

{% endhighlight %}

The following screenshot displays the load on demand for URL Adaptor in TreeView control.

![](/js/TreeView/Populate-Data_images/Populate-Data_img1.png)

While expanding the parent node
{:.caption}

![](/js/TreeView/Populate-Data_images/Populate-Data_img2.png)

After expanding the parent node
{:.caption}

