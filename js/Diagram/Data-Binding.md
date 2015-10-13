---
layout: post
title: Data-Binding
description: data binding
platform: js
control: Diagram
documentation: ug
---

# Data Binding

  * Diagram can be populated with the nodes and connectors based on the information provided from an external data source. 

  * Diagram exposes its specific data-related properties allowing you to specify the data source fields from where the node information has to be retrieved from.

To explore those properties, see [Data source settings](/js/api/ejDiagram "members:datasourcesettings")

  * Diagram supports three different kinds of Data binding.

    * Local Data

    * Remote Data

    * Html Table Data

## Local Data

Diagram can be populated based on the user defined JSON data (**Local Data**) by mapping the relevant data source fields.

To map the user defined JSON data with diagram, you have to configure the fields of `dataSourceSettings`. The following code example illustrates how to bind local data with the Diagram.

{% highlight js %}

//Initialize local data

var data = [{
        "Name": "Director"
    },

    {
        "Name": "Manager",
        "ReportingPerson": "Director"
    },

    {
        "Name": "TeamLead",
        "ReportingPerson": "Director"
    },

    {
        "Name": "Software Developer",
        "ReportingPerson": "TeamLead"
    },

    {
        "Name": "Testing engineer",
        "ReportingPerson": "TeamLead"
    },

    {
        "Name": "Software Developer",
        "ReportingPerson": "Manager"
    },

    {
        "Name": "Testing engineer",
        "ReportingPerson": "Manager"
    }
];

//To bind the JSON(local data) with node

function nodeTemplate(diagram, node) {
    // Set the Name field of JSON data as label.
    node.labels[0].text = node.Name;
}

$(function() {
    //Initialize Diagram
    $("#diagram").ejDiagram({
        //use automatic layout to arranging elements on the page        
        layout: {
            type: "hierarchicaltree"
        },
        //set the default properties for nodes and connectors.
        defaultSettings: {
            node: {
                width: 100,
                height: 40,
                fillColor: "darkcyan",
                labels: [{
                    name: "label1",
                    bold: true,
                    fontColor: "white"
                }]
            },
            connector: {
                segments: [{
                    type: "orthogonal"
                }],
                targetDecorator: {
                    shape: "none"
                }
            }
        },
        //initialize the node template.
        nodeTemplate: nodeTemplate,
        //configure data source for diagram
        dataSourceSettings: {
            // Define the unique field of each JSON data
            id: "Name",
            // Define the parent field which builds the relationship
            parent: "ReportingPerson",
            //set the local data source to the diagram.
            dataSource: data
        }
    });
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Data-Binding_images/Data-Binding_img1.png" %}

## Remote Data

You can bind the Diagram with Remote Data using dataManager.  

  * DataManager supports the following types of data-binding: JSON, Web Services, oData. 

  * It uses two different classes: ej.DataManager for processing and ej.Query for serving data. ej.DataManager communicates with data source and ej.Query generates data queries that are read by the dataManager. 

  * To learn more, refer [Data Manager](/js/DataManager/Getting-Started).

To bind remote data to diagram, you have to configure the fields of `dataSourceSettings`. The following code illustrates how to bind remote data to the Diagram.

{% highlight js %}

$(function() {
    //Initialize Diagram
    $("#diagram").ejDiagram({
        //To bind the custom JSON fields with node
        nodeTemplate: nodeTemplate,
        //Initialize automatic layout
        layout: {
            type: "hierarchicaltree"
        },
        //set the default properties for nodes and connectors
        defaultSettings: {
            node: {
                width: 100,
                height: 40,
                fillColor: "darkcyan",
                labels: [{
                    name: "label1",
                    bold: true,
                    fontColor: "white"
                }],
                borderColor: "none"
            },
            connector: {
                segments: [{
                    type: "orthogonal"
                }]
            }
        },
        //Configure data source
        dataSourceSettings: {
            //Initialize the data manager
            dataSource: ej.DataManager({
                // Specify the remote data service
                url: "[http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)"
            }),
            //Define the query to retrieve data
            query: ej.Query().from("Employees").select("EmployeeID, ReportsTo, FirstName"),
            // Define the table name
            tableName: "Employees",
            // Define the unique field
            id: "EmployeeID",
            // Define the field to relate objects
            parent: "ReportsTo"
        }
    });
});

//Bind custom JSON with node

function nodeTemplate(diagram, node) {
    node.labels[0].text = node.FirstName;
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Data-Binding_images/Data-Binding_img2.png" %}

## Html Table Data

The Diagram provides support to populate diagram from the **HTML table**. It is flexible to convert HTML table to diagram using **Data Manager**.

The following code illustrates how to convert HTML table to diagram.

{% highlight html %}
<!-- HTML Table -->
<table id="htmlbinding">
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

//Bind custom JSON with node

function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Designation;
    node.fillColor = node.Color;
}

$(function() {
    //Initialize Diagram
    $("#diagram").ejDiagram({
        width: "100%",
        height: "600px",
        layout: {
            type: "hierarchicaltree"
        },
        defaultSettings: {
            //set the default properties for nodes and connectors.
            node: {
                width: 120,
                height: 40,
                shape: "rectangle",
                borderColor: "transparent",
                labels: [{
                    name: "label1",
                    fontColor: "#ffffff"
                }]
            },
            connector: {
                segments: [{
                    "type": "orthogonal"
                }],
                targetDecorator: {
                    fillColor: "#4F4F4F",
                    borderColor: "#4F4F4F"
                }
            }
        },
        //initialize the node template.
        nodeTemplate: nodeTemplate,
        //configure data source for diagram
        dataSourceSettings: {
            id: "Id",
            parent: "ReportingPerson",
            //define data source with html table
            dataSource: ej.DataManager($("#htmlbinding")),
        }
    });
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Data-Binding_images/Data-Binding_img4.png" %}






