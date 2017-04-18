---
layout: post
title: Populate Diagram from external data sources
description: How to populate the Diagram from the local data, remote data, or html tables?
platform: js
control: Diagram
documentation: ug
api: /api/js/ejdiagram
---

# Data Binding

* Diagram can be populated with the nodes and connectors based on the information provided from an external data source.
* Diagram exposes its specific data-related properties allowing you to specify the data source fields from where the node information has to be retrieved from.

To explore those properties, see [Data source settings](/api/js/ejDiagram#members:datasourcesettings "Data source settings")

* Diagram supports three different kinds of Data binding.
	* Local Data
	* Remote Data
	* HTML Table Data

## Local Data

Diagram can be populated based on the user defined JSON data (**Local Data**) by mapping the relevant data source fields.

To map the user defined JSON data with Diagram, you have to configure the fields of `dataSourceSettings`. The following code example illustrates how to bind local data with the Diagram.

{% highlight javascript %}

//Initializes local data

var data = [{
	"Name": "Director"
},{
	"Name": "Manager",
	"ReportingPerson": "Director"
},{
	"Name": "TeamLead",
	"ReportingPerson": "Director"
},{
	"Name": "Software Developer",
	"ReportingPerson": "TeamLead"
},{
	"Name": "Testing engineer",
	"ReportingPerson": "TeamLead"
},{
	"Name": "Software Developer",
	"ReportingPerson": "Manager"
},{
	"Name": "Testing engineer",
	"ReportingPerson": "Manager"
}];

//Binds the JSON(local data) with node

function nodeTemplate(diagram, node) {
	// Sets the Name field of JSON data as label.
	node.labels[0].text = node.Name;
}

$(function() {
	//Initializes Diagram
	$("#diagram").ejDiagram({
		//Uses automatic layout to arrange elements on the page
		layout: {
			type: "hierarchicaltree"
		},
		//Sets the default properties for nodes and connectors.
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
		//Initializes the node template.
		nodeTemplate: nodeTemplate,
		//Configures data source for Diagram
		dataSourceSettings: {
			// Defines the unique field of each JSON data
			id: "Name",
			// Defines the parent field which builds the relationship
			parent: "ReportingPerson",
			//Sets the local data source to the diagram.
			dataSource: data
		}
	});
});

{% endhighlight %}

![](/js/Diagram/Data-Binding_images/Data-Binding_img1.png)

## Remote Data

You can bind the Diagram with Remote Data by using dataManager.

* DataManager supports the following types of data-binding: JSON, Web Services, oData.
* It uses two different classes: ej.DataManager for processing and ej.Query for serving data. ej.DataManager communicates with data source and ej.Query generates data queries that are read by the dataManager.
* To learn more, refer to [Data Manager](/js/DataManager/Getting-Started "Data Manager").

To bind remote data to the Diagram, you have to configure the fields of `dataSourceSettings`. The following code illustrates how to bind remote data to the Diagram.

{% highlight javascript %}

$(function() {
	//Initializes Diagram
	$("#diagram").ejDiagram({
		//Binds the custom JSON fields with node
		nodeTemplate: nodeTemplate,
		//Initializes automatic layout
		layout: {
			type: "hierarchicaltree"
		},
		//Sets the default properties for nodes and connectors
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
		//Configures data source
		dataSourceSettings: {
			//Initializes the data manager
			dataSource: ej.DataManager({
				// Specifies the remote data service
				url: "[http://mvc.syncfusion.com/Services/Northwnd.svc/](http://mvc.syncfusion.com/Services/Northwnd.svc/)"
			}),
			//Defines the query to retrieve data
			query: ej.Query().from("Employees").select("EmployeeID, ReportsTo, FirstName"),
			// Defines the table name
			tableName: "Employees",
			// Defines the unique field
			id: "EmployeeID",
			// Define the field to relate objects
			parent: "ReportsTo"
		}
	});
});

//Binds custom JSON with node

function nodeTemplate(diagram, node) {
	node.labels[0].text = node.FirstName;
}

{% endhighlight %}

![](/js/Diagram/Data-Binding_images/Data-Binding_img2.png)

## HTML Table Data

The Diagram provides support to populate the Diagram from the **HTML table**. It is flexible to convert HTML table to Diagram by using **Data Manager**.

The following code illustrates how to convert HTML table to the Diagram.

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
{% highlight javascript %}

//Binds custom JSON with node

function nodeTemplate(diagram, node) {
	node.labels[0].text = node.Designation;
	node.fillColor = node.Color;
}

$(function() {
	//Initializes Diagram
	$("#diagram").ejDiagram({
		width: "100%",
		height: "600px",
		layout: {
			type: "hierarchicaltree"
		},
		defaultSettings: {
			//Sets the default properties for nodes and connectors.
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
		//Initializes the node template.
		nodeTemplate: nodeTemplate,
		//Configures data source for Diagram
		dataSourceSettings: {
			id: "Id",
			parent: "ReportingPerson",
			//Defines data source with html table
			dataSource: ej.DataManager($("#htmlbinding")),
		}
	});
});

{% endhighlight %}

![](/js/Diagram/Data-Binding_images/Data-Binding_img4.png)






