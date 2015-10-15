---
layout: post
title: Data-Binding
description: data binding 
platform: js
control: TreeView
documentation: ug
---

# Data Binding 

The **TreeView** is populated with the node information taken from a data source. The **TreeView** supports binding data sources containing hierarchical data and supports both local data and remote data, for retrieving data from a specified data source. You can also display the hierarchical data in **TreeView**. **TreeView** exposes its specific data-related properties allowing you to specify which data source field the node information has to be retrieved from.

You can populate **TreeView** items using data binding support such as **JSON** and **OData** services. 

## Fields

The **fields** property in **TreeView** includes the data source fields and it can be set with appropriate values as follows.

JS Field properties

<table>
<tr>
<th>
Name</th><th>
Description</th></tr>
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

## Local Data

To bind the **Local Data** to the **TreeView** control, map the user-defined **json** data names with its appropriate data source field. You can bind data to **TreeView** by mapping fields such as **dataSource,id, parentId, text, hasChild** and **expanded**. 

The following steps explain how you can bind local data to **TreeView**.

In the HTML page, add a &lt;div&gt; element to configure TreeView.

{% highlight html %}

<div id="treeView"></div>

{% endhighlight %}

{% highlight js %}

    var localData = [
                   { id: 1, name: "Favorites", hasChild: true },
                   { id: 2, pid: 1, name: "Desktop" },
                   { id: 3, pid: 1, name: "Downloads" },
                   { id: 4, pid: 1, name: "Recent places" },
                   { id: 5, name: "libraries", hasChild: true },
                   { id: 6, pid: 5, name: "Documents", hasChild: true },
                   { id: 7, pid: 6, name: "My Documents" },
                   { id: 8, pid: 6, name: "Public Documents" },
                   { id: 9, pid: 5, name: "Pictures", hasChild: true },
                   { id: 10, pid: 9, name: "My Pictures" },
                   { id: 11, pid: 9, name: "Public Pictures" },
                   { id: 12, pid: 5, name: "Music", hasChild: true },
                   { id: 13, pid: 9, name: "My Music" },
                   { id: 14, pid: 9, name: "Public Music" },
                   { id: 15, pid: 5, name: "Subversion" },
                   { id: 16, name: "Computer", hasChild: true },
                   { id: 17, pid: 16, name: "Folder(C)" },
                   { id: 18, pid: 16, name: "Folder(D)" },
                   { id: 19, pid: 16, name: "Folder(F)" },
                  ];
    $("#treeView").ejTreeView({
        // mapping JSON Data Source with the fields property of TreeView
        fields: {
            dataSource: localData,
            id: "id",
            parentId: "pid",
            text: "name",
            hasChild: "hasChild",
            expanded: "expanded"
        }
    });

{% endhighlight %}

The output for **TreeView** control with **Local Data** binding is as follows.

![]("/js/TreeView/Data-Binding_images/Data-Binding_img1.png")

## Remote Data

You can bind **TreeView** to **Remote Data** using **dataManager** and the query in fields is used to retrieve the data. **dataManager** supports the following types of data-binding: JSON, Web Services, oData. It uses two different classes; **ej.DataManager** for processing, and **ej.Query** for serving data. **ej.DataManager** communicates with data source and **ej.Query** generates data queries that are read by the **dataManager**. In the following link, how to create **dataManager** is explained in full detail.

<http://help.syncfusion.com/js/datamanager/getting-started#create-your-datamanager-in-javascript>

The following steps explain how you can bind remote data to **TreeView** control.

In the HTML page, add a &lt;div&gt; element to configure TreeView.

{% highlight html %}


<div id="treeView"></div>

{% endhighlight %}



Define dataManager and assign remote data source to it. Here dataManager gets the remote web service and filters the data using Query. The select property of ejQuery is used to retrieve the specified columns from the data source.

{% highlight js %}

      // DataMangaer creation
      var dataManager = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
      });
      // query creation
      var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);


{% endhighlight %}


Assign dataSource and query property values to bind the remote data. Map the corresponding fields in TreeView control as follows.

{% highlight js %}

    $("#treeView").ejTreeView({
        width: 300,
        height: 300,
        fields: {
            dataSource: dataManager,
            query: query,
            id: "CategoryID",
            text: "CategoryName",
            child: {
                dataSource: dataManager,
                tableName: "Products",
                id: "ProductID",
                parentId: "CategoryID",
                text: "ProductName"
            }
        }
    });


{% endhighlight %}

The output for **TreeView** control with **Remote Data** binding is as follows.

![]("/js/TreeView/Data-Binding_images/Data-Binding_img2.png")

