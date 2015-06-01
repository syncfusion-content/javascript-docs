---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Diagram
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Diagram** in your application with **JavaScript**.

## Control Structure

The following screen shot illustrates the structure of **Diagram control.**

{% include image.html url="/js/Diagram/Getting-Started_images/Getting-Started_img1.png" Caption="Diagram"%}

## Create your first Diagram in JavaScript

Getting started with your **Essential JavaScript Diagram** is easy. You can start by creating a simple **Organizational Chart**.

1. Create an HTML file and add the necessary script and CSS files in the Head tag as shown in the following code example.

{% highlight js %}

**[JS]**
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Getting Started With Diagram Control For Javascript
</title>

**<!-- jQuery Script -->**
**<script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>**
**<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>**

**<!--script to create Diagram-->**
**<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>**
</head>
<body>
</body>
</html>


{% endhighlight %}



2. Add the &lt;div&gt; element in the body tag to render the Diagram.

{% highlight html %}

**[HTML]**
 <html>
<head>
<!-- header -->
</head>
<body>
**<div id="DiagramContent"></div>**
</body>
</html>


{% endhighlight %}



3. Initialize the Diagram widget as follows.

{% highlight html %}

**[HTML]**

 <html>
<head>
<!-- header -->
</head>
<body>
<div id="DiagramContent"></div>
**<script type="text/javascript">**
**$("#DiagramContent").ejDiagram({**
**width: "100%",**
**height: "600px",**
**});**
**</script>**
</body>
</html>


{% endhighlight %}



4. This creates an empty diagram. In the following section, you can learn how to add “Employee Details” in the Diagram.

{% include image.html url="/js/Diagram/Getting-Started_images/Getting-Started_img2.png" Caption="Empty Diagram"%}

**Define Employee Information**

Define “Employee Information” as JSON data. The following code example shows a list of employees whose ‘Name’ value is used as a unique identifier and the ‘ReportingPerson’ value is used to identify the person to whom they report to in the organization.

{% highlight js %}

**[JS]**
<head>
<!-- header -->
</head>
<body>
<div id="DiagramContent"></div>
<script type="text/javascript">

**//Initialize data source...**
**var data = [**
**{ "name": "Elizabeth", "fillColor": "rgb(0, 139,139)" },**
**{ "name": "Christina", "fillColor": "rgb(30, 30,113)", "ReportingPerson": "Elizabeth" },**
**{ "name": "Yoshi", "fillColor": "rgb(0, 100, 0)", "ReportingPerson": "Christina" },**
**{ "name": "Philip", "fillColor": "rgb(0, 100,  0)", "ReportingPerson": "Christina" },**
**{ "name": "Yang", "fillColor": "rgb(30, 30,  113)", "ReportingPerson": "Elizabeth" },**
**{ "name": "Roland", "fillColor": "rgb(0, 100, 0)", "ReportingPerson": "Yang" },**
**{ "name": "Yvonne", "fillColor": "rgb(0, 100,0)", "ReportingPerson": "Yang" }**
	**];**  

$("#DiagramContent").ejDiagram({
width: "100%",
height: "600px",
});

    </script>
</body>


{% endhighlight %}

**Mapping Data Source**

Then, you can configure this “Employee Information” with Diagram, so that the node and connector are automatically generated using mapping properties. The following code examples show how **dataSourceSetting** is used to map ‘id’ and ‘parent’ with property name identifiers for employee information.

{% highlight js %}

**[JS]**
<head>
<!-- header -->
</head>
<body>
<div id="DiagramContent"></div>
<script type="text/javascript">

//Initialize data source...


$("#DiagramContent").ejDiagram({

**//Configure data source for diagram**
			**dataSourceSettings: {** 
				**id: "name",** 
**parent: "ReportingPerson",**
**//Specifies the dataSource**
				**dataSource: data**  
			**}** 
		});             
    </script>
</body>


{% endhighlight %}



Based on datasource and its settings, nodes and connector are automatically generated, and so you need to give appearance of nodes that represents the employee and use inbuilt layout manager to automatically place nodes in an organizational chart structure.

**Visualize Employee**

Following code examples indicate how to define the default appearance of node and connector using defaultSetting. The NodeTemplate is used to update each node based on employee data. 

{% highlight js %}

**[JS]**
<head>
<!-- header -->
</head>
<body>
<div id="DiagramContent"></div>
<script type="text/javascript">

**// To Customize node before rendering**
**function nodeTemplate(diagram, node) {**
**node.labels[0].text = node.name;**
**}**

//Initialize data source...

$("#DiagramContent").ejDiagram({

**defaultSettings: {**
**//Set the default properties of nodes.**
			**node: {** 
				**width: 70,** 
**height: 30,**
**shape: {**
**type: "rectangle",**
					**"cornerRadius": 5** 
**},**
**labels: [ {**
					**name: "label1",** 
					**fontSize: 11,** 
**bold: true,**
**fontFamily: "Segoe UI",**
					**fontColor:"white"** 
				**}]** 
**},**

**//Set the default properties of connectors.**
**connector: {**
				**segments: [{** 
**"type": "orthogonal"**
**}],**
**targetDecorator: {shape: "arrow"}}**
**},**

**//Initialize the node template.**
**nodeTemplate: nodeTemplate,**

//Configure data source for diagram
			dataSourceSettings: { 
				id: "name", 
parent: "ReportingPerson",
//Specifies the dataSource
				dataSource: data  
			} 
});
</script>
</body>


{% endhighlight %}

**Apply Organizational Chart Layout**

Next you need to arrange nodes in an organizational chart fashion, and to do this you can apply layout as shown in following code example. You can see that spacing, margin and orientation are defined, that can also be customized based on the needs. 

{% highlight js %}

**[JS]**
<head>
<!-- header -->
</head>
<body>
<div id="DiagramContent"></div>
<script type="text/javascript">

// To Customize node before rendering
function nodeTemplate(diagram, node) {
node.labels[0].text = node.name;
}

//Initialize data source...

$("#DiagramContent").ejDiagram({

		//Use automatic layout to arrange 
elements on the page
**layout: {**         
**type:ej.datavisualization.Diagram.LayoutTypes.**
               **OrganizationalChart,** 
               **marginX: 10,**
               **marginY: 50,** 
               **horizontalSpacing: 50,** 
               **verticalSpacing:50,**
               **orientation:ej.datavisualization.Diagram.**
               **LayoutOrientations.TopToBottom },**

defaultSettings: {

      		//Set the default properties of nodes.
			node: { 
				width: 70, 
height: 30,
shape: {
type: "rectangle",
					"cornerRadius": 5 
},
labels: [ {
					name: "label1", 
					fontSize: 11, 
bold: true,
fontFamily: "Segoe UI",
					fontColor:"white" 
				}] 
},

//Set the default properties of connectors.
connector: {
				segments: [{ 
"type": "orthogonal"
}],
targetDecorator: {shape: "arrow"}}
},

//Initialize the node template.
nodeTemplate: nodeTemplate,

//Configure data source for diagram
			dataSourceSettings: { 
				id: "name", 
parent: "ReportingPerson",
//Specifies the dataSource
				dataSource: data  
			} 
		});             
    </script>
</body>


{% endhighlight %}



{% highlight js %}

**[JS]**
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>
Getting Started With Diagram Control For Javascript
</title>

<!-- jQuery Script -->
<script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
<script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"></script>

<!--script to create Diagram-->
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
</head>

<body>
<div id="DiagramContent"></div>
<script type="text/javascript">

//Initialize data source
var data = [
{ "name": "Elizabeth", "fillColor": "rgb(0, 139,139)" },
{ "name": "Christina", "fillColor": "rgb(30, 30,113)", "ReportingPerson": "Elizabeth" },
{ "name": "Yoshi", "fillColor": "rgb(0, 100, 0)", "ReportingPerson": "Christina" },
{ "name": "Philip", "fillColor": "rgb(0, 100,  0)", "ReportingPerson": "Christina" },
{ "name": "Yang", "fillColor": "rgb(30, 30,  113)", "ReportingPerson": "Elizabeth" },
{ "name": "Roland", "fillColor": "rgb(0, 100, 0)", "ReportingPerson": "Yang" },
{ "name": "Yvonne", "fillColor": "rgb(0, 100,0)", "ReportingPerson": "Yang" }
	];  

// To Customize node before rendering
function nodeTemplate(diagram, node) {
node.labels[0].text = node.name;
}

$("#DiagramContent").ejDiagram({

//Use automatic layout to arrange elements on the page
		layout: {         
type:ej.datavisualization.Diagram.LayoutTypes.
			OrganizationalChart, 
marginX: 10,
			marginY: 50, 
			horizontalSpacing: 50, 
verticalSpacing:50,
orientation:ej.datavisualization.Diagram.
LayoutOrientations.TopToBottom },

defaultSettings: {

//Set the default properties of nodes.
			node: { 
				width: 70, 
height: 30,
shape: {
type: "rectangle",
					"cornerRadius": 5 
},
labels: [{
					name: "label1", 
					fontSize: 11, 
bold: true,
fontFamily: "Segoe UI",
					fontColor:"white" 
				}] 
},

//Set the default properties of connectors.
connector: {
				segments: [{ 
"type": "orthogonal"
}],
targetDecorator: {shape: "arrow"}}
},

//Initialize the node template.
nodeTemplate: nodeTemplate,

//Configure data source for diagram
			dataSourceSettings: { 
				id: "name", 
parent: "ReportingPerson",
//Specifies the dataSource
				dataSource: data  
			} 
		});             
    </script>
</body>
</html>


{% endhighlight %}



The Employee details are displayed in the Diagram as follows.

{% include image.html url="/js/Diagram/Getting-Started_images/Getting-Started_img3.png" Caption="Employee Details"%}

