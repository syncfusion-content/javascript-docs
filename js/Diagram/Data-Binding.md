---
layout: post
title: Data-Binding
description: data binding
platform: js
control: Diagram
documentation: ug
---

# Data Binding

**Diagram** can be populated with the node and connector based on information from an external data source using data binding. **Diagram** supports binding data sources containing hierarchical data and supports both local data and remote data, for retrieving data from a specified data source. Diagram exposes its specific data-related properties allowing you to specify the data source fields from where the node information has to be retrieved from.

You can populate **Diagram** elements using data binding support such as **JSON** and **OData** services.

#### DataSource Settings

The **DataSourceSettings** property of **Diagram** includes the required data source fields and it can be set with appropriate values as follows.

<table>
<tr>
<td>
<b>Name</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
dataSource</td><td>
datasource receives <b>Essential DataManager</b> object and <b>JSON</b> object.</td></tr>
<tr>
<td>
query</td><td>
It receives query to retrieve data from the table (query is same as SQL).<br/>
Example: ej.Query().from("Categories").select("CategoryID, CategoryName").take(3);</td></tr>
<tr>
<td>
tableName</td><td>
It receives table name to execute query on the corresponding table.</td></tr>
<tr>
<td>
id</td><td>
Specifies the unique id of data source items</td></tr>
<tr>
<td>
parent</td><td>
Specifies the parent id of the data source items.</td></tr>
</table>

_Field properties_

## Local Data

To bind the **Local Data** to the Diagram control, map the user-defined **JSON** data names with its appropriate data source field. You can bind data to the **Diagram** by mapping fields such as **dataSource, id** and **parent.** The following code example illustrates how to bind local data to the **Diagram.**

{% highlight js %}

//To Initialize data
var data = [
    {"Name": "Director"},
    {"Name": "Manager", "ReportingPerson":"Director"},
    {"Name": "TeamLead", "ReportingPerson":"Director" },
    {"Name": "Software Developer", "ReportingPerson":"TeamLead"},
    {"Name": "Testing engineer", "ReportingPerson":"TeamLead"},
    {"Name": "Software Developer", "ReportingPerson":"Manager"},
    {"Name": "Testing engineer", "ReportingPerson":"Manager"}
];

//To customize nodes before rendering
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Name;
} 

//To Initialize diagram
$("#diagram").ejDiagram ({   
    //use automatic layout to arranging elements on the page        
    layout: { type: "hierarchicaltree"},          
    defaultSettings: {
        //set the default properties of the node.
        node: { 
            width: 100, height: 40, fillColor:"darkcyan",          
            labels: [{name: "label1", bold: true }] 
        },
        //set the default properties of the connector.         
        connector: { 
            segments: [{ "type": "orthogonal" }], 
            targetDecorator: {shape: "none"} 
        }
    },
    //initialize the node template.
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        id: "Name", parent: "ReportingPerson",
        dataSource: data //specifies the dataSource
    } 
});               

{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Data-Binding_images/Data-Binding_img1.png" Caption="Local Data binding"%}

## Remote Data

You can bind the **Diagram** to Remote Data using **dataManager** and the query in fields is used to retrieve the data. **dataManager** supports the following types of data-binding: JSON, Web Services, oData. It uses two different classes: ej.DataManager for processing and ej.Query for serving data. ej.DataManager communicates with data source and ej.Query generates data queries that are read by the dataManager. The following link explains in detail on how to create dataManager. [http://help.syncfusion.com/ug/js/default.htm#!Documents/createyourdatamanage.htm](http://help.syncfusion.com/ug/js/default.htm)

The following code illustrates how to bind remote data to the **Diagram**.

{% highlight js %}

//Initialize Diagram Model
$("#diagram").ejDiagram({
    //To customize node before rendering
    nodeTemplate: nodeTemplate,
    
    //Initialize automatic layout
    layout: { type: "hierarchicaltree" },
    defaultSettings: {
        //set the default properties of the nodes
        node: {
            width: 100, height: 40, fillColor: "darkcyan",
            labels: [{ name: "label1", bold: true, fontColor: "white" }],
            borderColor: "none" },
        
        //set the default properties of the connectors
         connector: { segments: [{ type: "orthogonal" }] }
    },
    
    //Configure data source
    dataSourceSettings: {
        dataSource: ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/" }),
        query: ej.Query().from("Employees").select("EmployeeID, ReportsTo, FirstName"), 
        tableName: "Employees",
        id: "EmployeeID", parent: "ReportsTo"
    }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Data-Binding_images/Data-Binding_img2.png" Caption="Remote data binding"%}

### Root

During automatic layout, node without parent is treated as root of the layout. You can specify this root by using the data source settings. The following code example illustrates how to specify the root object for the Diagram.

{% highlight js %}

//configure data source for diagram
dataSourceSettings: {
    id: "Name",   parent: "ReportingPerson",
    
    //Object with id "Manager", is considered as root of tree layout.
    root: "Manager",   
    
    //specifies the dataSource
    dataSource: data
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Data-Binding_images/Data-Binding_img3.png" Caption="DataSource with Root"%}

## HTML Binding

The Diagram provides support to form diagram from the **HTML table**. It is flexible to convert **HTML** table to diagram using **Data Manager**. The following code example illustrates how to convert **HTML** table to diagram.

{% highlight html %}

<!-- HTML Table -->
<table id="Table1">
     <thead>
         <tr>
             <th>Id</th>
             <th>Designation</th>
             <th>Color</th>
             <th>ReportingPerson</th>
         </tr>
     </thead>
     <tbody>
         <tr>
             <td>parent</td>                
             <td>Managing Director</td>
             <td>#822b86</td>
             <td>null</td>
         </tr>
         <tr>
             <td>1</td>
             <td>Project manager</td>
             <td>#3c418d</td>
             <td>parent</td>
         </tr>
         <tr>
             <td>2</td>
             <td>Project manager</td>
             <td>#108d8d</td>
             <td>parent</td>
         </tr>
          <tr>
             <td>3</td>
             <td>Product Lead</td>
             <td>#3c418d</td>
             <td>1</td>
         </tr>
         <tr>
             <td>4</td>
             <td>Product Lead</td>
             <td>#3c418d</td>
             <td>1</td>
         </tr>
         <tr>
             <td>5</td>
             <td>Product Lead</td>
             <td>#108d8d</td>
             <td>2</td>
         </tr>
         <tr>
             <td>6</td>
             <td>Product Lead</td>
             <td>#108d8d</td>
             <td>2</td>
         </tr>
         <tr>
             <td>7</td>
             <td>S/W engineer</td>
             <td>#3c418d</td>
             <td>4</td>
         </tr>
         <tr>
             <td>8</td>
             <td>S/W engineer</td>
             <td>#3c418d</td>
             <td>4</td>
         </tr>
     </tbody>
</table>
{% endhighlight %}

{% highlight js %}

//configure data source for diagram	
dataSourceSettings: {
    id: "Id", parent: "ReportingPerson",
    //specifies the table name 
    dataSource: ej.DataManager($("#Table1"))
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Concepts-and-Features/Data-Binding_images/Data-Binding_img4.png" Caption="HTML Data Binding"%}
