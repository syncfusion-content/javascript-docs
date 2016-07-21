---
layout: post
title: Populate-Data
description: populate data 
platform: js
control: TreeView
documentation: ug
---


# Populate Data

TreeView can be populated with local or remote data source by using a property [dataSource](http://help.syncfusion.com/js/api/ejtreeview#members:fields-datasource), which is the member of [fields](http://help.syncfusion.com/js/api/ejtreeview#members:fields) property.

In TreeView, you should use “**fields**” property to go with data source. It specifies the mapping fields for the data source to receive the data, query to process the data and field mappers to map the data members.

## Fields

Below table is list outs the field members with description.  

<table>
<tr>
<th>
Properties</th><th>
Description</th></tr>
<tr>
<td>
{{'[dataSource](http://help.syncfusion.com/js/api/ejtreeview#members:fields-datasource)'| markdownify }}<br/><br/></td><td>
The data source contains the list of data for generating the TreeView list.<br/><br/></td></tr>
<tr>
<td>
{{'[query](http://help.syncfusion.com/js/api/ejtreeview#members:fields-query)'| markdownify }}<br/><br/></td><td>
It specifies the query to retrieve the data from the online server.<br/><br/></td></tr>
<tr>
<td>
{{'[tableName](http://help.syncfusion.com/js/api/ejtreeview#members:fields-tablename)'| markdownify }}<br/><br/></td><td>
It specifies the name of the table from which data to be processed from given data source.<br/><br/></td></tr>
<tr>
<td>
{{'[id](http://help.syncfusion.com/js/api/ejtreeview#members:fields-id)'| markdownify }}<br/><br/></td><td>
It specifies the ID of the node.<br/><br/></td></tr>
<tr>
<td>
{{'[parentId](http://help.syncfusion.com/js/api/ejtreeview#members:fields-parentid)'| markdownify }}<br/><br/></td><td>
It specifies the parent id of the node<br/><br/></td></tr>
<tr>
<td>
{{'[text](http://help.syncfusion.com/js/api/ejtreeview#members:fields-text)'| markdownify }}<br/><br/></td><td>
It specifies the text content of the node.<br/><br/></td></tr>
<tr>
<td>
{{'[hasChild](http://help.syncfusion.com/js/api/ejtreeview#members:fields-haschild)'| markdownify }}<br/><br/></td><td>
It specifies the node has child (which is the nested or inner level of nodes). Also it’s used in load on demand of tree data.<br/><br/></td></tr>
<tr>
<td>
{{'[expanded](http://help.syncfusion.com/js/api/ejtreeview#members:fields-expanded)'| markdownify }}<br/><br/></td><td>
It specifies the tree node to be in expanded state<br/><br/></td></tr>
<tr>
<td>
{{'[selected](http://help.syncfusion.com/js/api/ejtreeview#members:fields-selected)'| markdownify }}<br/><br/></td><td>
It specifies the select node at initialize. N> only one node get selected <br/><br/></td></tr>
<tr>
<td>
{{'[isChecked](http://help.syncfusion.com/js/api/ejtreeview#members:fields-ischecked)'| markdownify }} <br/><br/></td><td>
It specifies the node to be in checked state, if tree node represented with checkboxes. <br/><br/></td></tr>
<tr>
<td>
{{'[imageUrl](http://help.syncfusion.com/js/api/ejtreeview#members:fields-imageurl)'| markdownify }}<br/><br/></td><td>
It defines the image location.<br/><br/></td></tr>
<tr>
<td>
{{'[imageAttribute](http://help.syncfusion.com/js/api/ejtreeview#members:fields-imageattribute)'| markdownify }}<br/><br/></td><td>
It defines the image attributes such as height, width, styles, etc.<br/><br/></td></tr>
<tr>
<td>
{{'[spriteCssClass](http://help.syncfusion.com/js/api/ejtreeview#members:fields-spritecssclass)'| markdownify }}<br/><br/></td><td>
It defines the sprite CSS for the image tag.<br/><br/></td></tr>
<tr>
<td>
{{'[htmlAttribute](http://help.syncfusion.com/js/api/ejtreeview#members:fields-htmlattribute)'| markdownify }}<br/><br/></td><td>
It defines the HTML attributes such as class and styles for a node ("li" tag).<br/><br/></td></tr>
<tr>
<td>
{{'[linkAttribute](http://help.syncfusion.com/js/api/ejtreeview#members:fields-linkattribute)'| markdownify }}<br/><br/></td><td>
It defines the HTML attributes such as class and styles for a link tag, which is child of node.<br/><br/></td></tr>
</table>
Mapping all fields with data source

{% highlight js %}

        var localData = [

       { id: 1, text: "Item 1", expanded: true, nodeProperty: { class: "textblue", value: "Item 1" } },

       { id: 2, text: "Item 2", linkProperty: { class: "textunderline", href: "http://www.syncfusion.com", target: "_blank" } },

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

TreeView can be rendered from a self-referential data by providing the two required fields [id](http://help.syncfusion.com/js/api/ejtreeview#members:fields-id) and [parentId](http://help.syncfusion.com/js/api/ejtreeview#members:fields-parentid). 

{% highlight js %}

        var localData = [

        { id: 1, text: "Item 1" },

        { id: 2, text: "Item 2" },

        { id: 3, text: "Item 3" },

        { id: 4, text: "Item 4" },

        { id: 5, parent: 1, text: "Item 1.1" }                

        ];

{% endhighlight %}

Above flat array of JSON data can be directly assigned to [dataSource](http://help.syncfusion.com/js/api/ejtreeview#members:fields-datasource) property and mapping data fields with respect to the mapper field in order to create TreeView.

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

## Remote Data

When using remote data binding, the adaptor of [ej.DataManager](http://helpjs.syncfusion.com/js/api/ejdatamanager#) plays vital role in processing queries to make them suitable to sends along with data request and also process the response data from the server.

### OData

**OData** is a standardized protocol for creating and consuming data. You can bind [oData service](http://www.odata.org/#) data to TreeView in two ways using DataManager.

* Passing OData service link to DataManager

You can provide the OData service URL directly to the [ej.DataManager](http://helpjs.syncfusion.com/js/api/ejdatamanager#) class and then we can assign it to TreeView dataSource.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var parentData = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Categories"),

        childData = ej.DataManager("http://mvc.syncfusion.com/Services/Northwnd.svc/Products");

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

* Passing OData service link to “**url**” property of [ej.DataManager](http://helpjs.syncfusion.com/js/api/ejdatamanager#)

By using “**url**” property of [ej.DataManager](http://helpjs.syncfusion.com/js/api/ejdatamanager#) we can bind OData Service to Dropdown. Here we may also specify the **adaptor** as [ej.ODataAdaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors#odata-adaptor) and it is optional to specify.

We can provide adaptor value either as string value (“ODataAdaptor”) or by creating a new instance (new [ej.ODataAdaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors#odata-adaptor))

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var dataManager = ej.DataManager({

            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Categories",

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

                            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Products"

                        }),

                        id: "ProductID", parentId: "CategoryID", text: "ProductName"

                    }

                }

            });

        });

{% endhighlight %}

N>  We can use above code until OData service version 3. For OData Service version 4 End Point, we have created a separate adaptor [ej.ODataV4Adaptor](http://helpjs.syncfusion.com/js/datamanager/data-binding#odata-v4) for data binding.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var dataManager = ej.DataManager({

            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Categories",

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

                            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Products"

                        }),

                        id: "ProductID", parentId: "CategoryID", text: "ProductName"

                    }

                }

            });

        });

{% endhighlight %}

### WebApi

Using [ej.WebApiAdaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors#webapi-adaptor), you can bind WebApi service data to TreeView as shown in below code example

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            var dataManager = ej.DataManager({

                url: "http://mvc.syncfusion.com/OdataServices/treeView/TreeViewData/GetAllData",

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

The Custom Adaptor concept of [ej.DataManager](http://helpjs.syncfusion.com/js/api/ejdatamanager#) allow you to customize or generate your own adaptor which is used to process query and result data. 

[http://helpjs.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor](http://helpjs.syncfusion.com/js/datamanager/data-adaptors#custom-adaptor)

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

                insert: function (dm, data) {

                    return dm.dataSource.json.push(data);

                },

                processQuery: ej.JsonAdaptor.prototype.processQuery // reused process query from json adaptor

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

Load on demand is a technique (Lazy load) that is used to reduce the bandwidth size of consuming huge data. You can load data on demand in TreeView by using [loadOnDemand](http://help.syncfusion.com/js/api/ejtreeview#members:loadondemand) property when you’re going to use huge data.

Refer below code example to load data on demand from local data source.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        var localData = [

        { id: 1, text: "Item 1", hasChild: true },

        { id: 2, text: "Item 2" },

        { id: 3, text: "Item 3", hasChild: true },

        { id: 4, text: "Item 4" },

        { id: 5, parent: 1, text: "Item 1.1", hasChild: true },

        { id: 6, parent: 1, text: "Item 1.2" },

        { id: 7, parent: 1, text: "Item 1.3" },

        { id: 8, parent: 3, text: "Item 3.1" },

        { id: 9, parent: 3, text: "Item 3.2" },

        { id: 10, parent: 5, text: "Item 1.1.1" }

        ];

        $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                loadOnDemand: true,

                fields: { dataSource: localData, id: "id", parentId: "parent", text: "text" }

            });

        });

{% endhighlight %}

Refer below code example to load data on demand from remote data source.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView">

    </div>

{% endhighlight %}

{% highlight js %}

        $(function () {

            var dataManager = ej.DataManager("http://mvc.syncfusion.com/OdataServices/treeView/TreeViewData/GetTreeData");

            $("#treeView").ejTreeView({

                loadOnDemand: true,

                fields: {

                    dataSource: dataManager,

                    id: "id", text: "name", parentId: "pid",

                }

            });

        });

{% endhighlight %}

