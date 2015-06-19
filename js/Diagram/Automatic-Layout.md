---
layout: post
title: Automatic-Layout
description: automatic layout
platform: js
control: Diagram
documentation: ug
---

# Automatic Layout

Diagram automatically provides support to layout nodes. It includes the following:

* Hierarchical Layout
* Organization Chart

## Hierarchical Layout

The **Hierarchical Tree Layout** arranges nodes in a tree-like structure, where the nodes in the hierarchical layout may have multiple parents. There is no need to specify the layout root. The following code illustrates how to arrange the nodes in a hierarchical structure.

{% highlight js %}

//Initialize data source
var data = [
    {"Name": "Steve-Ceo"},
    {"Name": "Kevin-Manager","ReportingPerson":"Steve-Ceo"},
    {"Name": "Peter-Manager","ReportingPerson":"Steve-Ceo"},
    {"Name": "John- Manager","ReportingPerson":"Peter-Manager"},
    {"Name": "Mary-CSE ","ReportingPerson":"Peter-Manager"},
    {"Name": "Jim-CSE ", "ReportingPerson":"Kevin-Manager"},
    {"Name": "Martin-CSE", "ReportingPerson":"Kevin-Manager"}
];

//Customize nodes before rendering
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Name;
} 

$("#diagram").ejDiagram ({ 
    //use automatic layout to arranging elements on the page          
    layout: { type: "hierarchicaltree"},      
    defaultSettings: {
        //set the default properties of the node.
        node: { width: 100, height: 40, fillColor: "darkcyan", 
                labels: [{ name: "label1", bold: true, fontColor: "white"}]
        },
        //set the default properties of the connector.    
        connector: { segments: [{ "type": "orthogonal"}], targetDecorator: {shape: "none"} } 
    },       
    //initialize the node template.
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        id: "Name", parent: "ReportingPerson",             
        //specifies the dataSource
        dataSource: data
    }
}); 

{% endhighlight %}

### Spacing

The following example illustrates the horizontal and vertical spacing of **Hierarchical Layout.**

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img1.png" Caption="Hierarchical Layout"%}

### Orientation

The **Orientation** property, **ej.datavisualization.Diagram.LayoutOrientations**, of layout is used to specify the tree orientation.

* **TopToBottom**- Places the root node at the top and the child nodes are arranged below the root node.

* **BottomToTop**- Places the root node at the bottom and the child nodes are arranged above the root node.

* **LeftToRight**- Places the root node at the left and the child nodes are arranged on the right side of the root node.

* **RightToLeft**- Places the root node at the right and the child nodes are arranged on the left side of the root node.

The following image displays “Bottom to Top” orientation of layout.

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img2.png" Caption="BottomToTop"%}

## Organizational Chart

An **organizational chart** is a diagram that displays the structure of an organization and the relationships. Diagram provides support to layout the nodes automatically. 

### How to create a basic organizational chart

The following code example illustrates how to create an organizational chart.

{% highlight js %}

//Data source
var data = [
    { "Id": "parent", "Role": "Project Management" },
    { "Id": 1, "Role": "R&D Team", "Team": "parent" },
    { "Id": 3, "Role": "Philosophy", "Team": "1" },
    { "Id": 4, "Role": " Organization", "Team": "1" },
    { "Id": 5, "Role": "Technology", "Team": "1" },
    { "Id": 7, "Role": " Funding", "Team": "1" },
    { "Id": 8, "Role": "Resource Allocation", "Team": "1" },
    { "Id": 9, "Role": "Targeting", "Team": "1" },
    { "Id": 11, "Role": "Evaluation", "Team": "1" },
    { "Id": 156, "Role": "HR Team", "Team": "parent" },
    { "Id": 13, "Role": "Recruitment", "Team": "156" },
    { "Id": 113, "Role": "Training", "Team": "12" },
    { "Id": 112, "Role": "Employee Relation", "Team": "156" },
    { "Id": 14, "Role": "Record Keeping", "Team": "12" },
    { "Id": 15, "Role": "Compensations & Benefits", "Team": "12" },
    { "Id": 16, "Role": "Compliances", "Team": "12" },
    { "Id": 17, "Role": "Production & Sales Team", "Team": "parent" },
    { "Id": 119, "Role": "Design", "Team": "17" },
    { "Id": 19, "Role": "Operation", "Team": "17" },
    { "Id": 20, "Role": "Support", "Team": "17" },
    { "Id": 21, "Role": "Quality Assurance", "Team": "17" },
    { "Id": 23, "Role": "Customer Interaction", "Team": "17" },
    { "Id": 24, "Role": "Support and Maintenance", "Team": "17" },
    { "Id": 25, "Role": "Task Coordination", "Team": "17" },
];

//creating the node template
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Role;
}

//Initialize diagram
$("#diagram").ejDiagram({
    //Define default layout as organizational chart
    layout: { type: "organizationalchart" },
    defaultSettings: {
        //set the default properties of the nodes.
        //set the default properties of the connectors. 
    },
    //initialize the node template.
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        id: "Id", 
        parent: "Team",
        dataSource: data
    }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img3.png" Caption="Organizational chart"%}

### Customizing the organizational chart

Organizational chart layout starts parsing from root and iterate through all its child elements. ‘getLayoutInfo’ method provides necessary information of a node’s children and the way to arrange (direction, orientation, offsets, etc.) them. You can customize the arrangements by overriding this function, explained as follows.

### GetLayoutInfo

You can set Chart orientations, chart types and offset to be left between parent and child nodes by overriding the method **diagram.model.layout.getLayoutInfo.**

### Arguments

The **getLayoutInfo** method is called to configure every subtree of the organizational chart. And it takes the following arguments.

1. diagram (Reference of diagram)
2. node (Parent node to that options are to be customized)
3. options (object to set the customizable properties)

The following code example illustrates how to define the method getLayoutInfo.

{% highlight js %}

//Defining getLayoutInfo
function getLayoutInfo(diagram, node, options) {
    options.orientation = "vertical"; 
    options.type = "right";
    options.offset = 10;
}

//Initialize diagram
$("#diagram").ejDiagram({
    //use automatic layout to arrange elements
    layout: { type: "organizationalchart", getLayoutInfo: getLayoutInfo }
});

{% endhighlight %}

Following table illustrates the properties that “options” argument takes.

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Description</b></td><td>
<b>Default Value</b></td></tr>
<tr>
<td>
options.children</td><td>
Contains the list of child nodes.Children collection can be modified.</td><td>
Array of child nodes</td></tr>
<tr>
<td>
options.assistants</td><td>
By default, the collection is empty. When any of the child nodes have to be set as “Assistant”, you can remove from children collection and have to insert into assistants collection. </td><td>
Empty array</td></tr>
<tr>
<td>
options.orientation</td><td>
Gets or sets the organizational chart orientation.</td><td>
ChartOrientation.Vertical </td></tr>
<tr>
<td>
options.type</td><td>
Gets or sets the chart organizational chart type </td><td>
For horizontal chart orientation: ChartType.Center<br/>
For Vertical chart orientation: ChartType.Alternate</td></tr>
<tr>
<td>
options.offset</td><td>
Offset is the horizontal space to be left between parent and child nodes.</td><td>
20 pixels. Applicable only for vertical chart orientations.</td></tr>
<tr>
<td>
options.hasSubTree</td><td>
Gets whether the node contains sub trees.</td><td>
Boolean</td></tr>
<tr>
<td>
options.level</td><td>
Gets the depth of the node from layout root</td><td>
Number</td></tr>
<tr>
<td>
options.enableRouting</td><td>
By default, Connections are routed based on the chart type and orientations. This property gets or sets whether default routing is to be enabled or disabled.</td><td>
true</td></tr>
</table>

_Properties of argument "option"_

### Orientations

Diagram provides the following orientation options.

1. Horizontal chart orientation
2. Vertical chart orientation

Following table illustrates the different chart orientations and chart types.

<table>
<tr>
<td>
<b>Orientation</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td><td>
<b>Example</b></td></tr>
<tr>
<td rowspan = "3">
Horizontal</td><td>
Left</td><td>
Arranges the child nodes horizontally at the left side of parent.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img4.png" alt="" width="224pt" height="79pt"/></td></tr>
<tr>
<td>
Right</td><td>
Arranges the child nodes horizontally at the right side of parent.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img5.png" alt="" width="214pt" height="85pt"/></td></tr>
<tr>
<td>
Center</td><td>
Arranges the children at the bottom/left/right/top center of parent based on layout orientation.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img6.png" alt="" width="220pt" height="85pt"/></td></tr>
<tr>
<td rowspan = "3">
Vertical</td><td>
Left</td><td>
Vertically arranges the children at the left side of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img7.png" alt="" width="109pt" height="125pt"/></td></tr>
<tr>
<td>
Right</td><td>
Vertically arranges the children at the right side of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img8.png" alt="" width="110pt" height="132pt"/></td></tr>
<tr>
<td>
Alternate</td><td>
Vertically arranges the children at both left and right sides of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img9.png" alt="" width="151pt" height="103pt"/></td></tr>
</table>

_Chart Orientations and Chart Types_

Following code example illustrates how to set the horizontal right arrangement to the leaf level trees.

{% highlight js %}

//Horizontal right layout arrangement
function getLayoutInfo(diagram, node, options) {
    if (!options.hasSubTree) {
        options.type = "left";
        options.orientation = "horizontal";
    }
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img10.png" Caption="Horizontal left arranged leaf level trees"%}

### Assistant Support

**Diagram** provides support to layout assistant nodes. You can add assistants at runtime by using the **getLayoutInfo** method. The **assistants** property of the “options” argument is an empty array by default. When any of the child nodes are to be set as Assistant, move those nodes to options.assistants from options.children. The following code example illustrates how to add assistants to layout.

{% highlight js %}

//Defining getLayoutInfo
function getLayoutInfo(diagram, node, options) {
    if (node.hasAssistant) {
        options.assistants.push(options.children[0]);
        options.children.splice(0, 1);
    }
    options.orientation = "vertical"; 
    options.type = "left"
    options.offset = -60;
}

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img11.png" Caption="Vertical left arrangement with assistant"%}
