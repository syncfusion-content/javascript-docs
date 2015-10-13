---
layout: post
title: Automatic-Layout
description: automatic layout
platform: js
control: Diagram
documentation: ug
---

# Automatic Layout

Diagram provides support to auto-arrange the nodes on diagram area which is referred as **Layout**. It includes the following layout modes.

  * Hierarchical Layout
  * Organization Chart
  * Radial Tree

## Hierarchical Layout

The Hierarchical Tree Layout arranges nodes in a tree-like structure, where the nodes in the hierarchical layout may have multiple parents. There is no need to specify the layout root. 
To arrange the nodes in hierarchical structure, you need to specify the layout `type` as hierarchical tree.   Following example shows how to arrange nodes in hierarchical structure.


{% highlight js %}

//Initialize data source
var data = [{
    Name: "Steve-Ceo"
}, {
    Name: "Kevin-Manager",
    ReportingPerson: "Steve-Ceo"
}, {
    Name: "Peter-Manager",
    ReportingPerson: "Steve-Ceo"
}, {
    Name: "John- Manager",
    ReportingPerson: "Peter-Manager"
}, {
    Name: "Mary-CSE ",
    ReportingPerson: "Peter-Manager"
}, {
    Name: "Jim-CSE ",
    ReportingPerson: "Kevin-Manager"
}, {
    Name: "Martin-CSE",
    ReportingPerson: "Kevin-Manager"
}];

var type = ej.datavisualization.Diagram.LayoutTypes;

//Bind custom JSON with node
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Name;
}

$("#diagram").ejDiagram({
    //use layout to auto-arrange nodes on the diagram page          
    layout: {
        //set layout type
        type: type.HierarchicalTree
    },
    defaultSettings: {
        //set the default properties for nodes and connectors.
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
                "type": "orthogonal"
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
        //Define the unique field
        id: "Name",
        //define the relationship
        parent: "ReportingPerson",
        //specifies the dataSource
        dataSource: data
    }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img1.png" %}

N> You can ignore a particular Node from layout arrangement by setting its **excludeFromLayout** property as true.

## Radial Tree Layout

The Radial Tree layout arranges nodes on a virtual concentric circles around a root node. Sub-trees formed by the branching of child nodes are located radially around the child nodes. This arrangement results in an ever-expanding concentric arrangement with radial proximity to the root node, indicating the node level in the hierarchy. If no root node is set, the algorithm automatically considers one of the diagram nodes as the root node.

To arrange nodes in a radial tree structure, you need to set the `type` property of layout as radial tree. The following code illustrates how to arrange the nodes in a radial tree structure. 

{% highlight js %}

//Initialize data source
var data = [{
    Id: "parent",
    ImageUrl: "images/Clayton.png"
}, {
    Id: 1,
    ImageUrl: "images/image55.png",
    ReportingPerson: "parent"
}, {
    Id: 2,
    ImageUrl: "images/Robin.PNG",
    ReportingPerson: "parent"
}, {
    Id: 3,
    ImageUrl: "images/Robin.PNG",
    ReportingPerson: "parent"
}, {
    Id: 4,
    ImageUrl: "images/Paul.png",
    ReportingPerson: "parent"
}, {
    Id: 5,
    ImageUrl: "images/image53.png",
    ReportingPerson: "parent"
}, {
    Id: 6,
    ImageUrl: "images/Maria.png",
    ReportingPerson: "parent"
}, {
    Id: 7,
    ImageUrl: "images/Jenny.png",
    ReportingPerson: 3
}, {
    Id: 8,
    ImageUrl: "images/Thomas.PNG",
    ReportingPerson: "parent"
}, {
    Id: 9,
    ImageUrl: "images/Jenny.png",
    ReportingPerson: 2
}, {
    Id: 10,
    ImageUrl: "images/Thomas.png",
    ReportingPerson: 2
}, {
    Id: 11,
    ImageUrl: "images/Maria.PNG",
    ReportingPerson: 4
}, {
    Id: 12,
    ImageUrl: "images/Thomas.PNG",
    ReportingPerson: 1
}, {
    Id: 13,
    ImageUrl: "images/Clayton.png",
    ReportingPerson: 6
}, {
    Id: 14,
    ImageUrl: "images/Jenny.png",
    ReportingPerson: 3
}, {
    Id: 15,
    ImageUrl: "images/Thomas.png",
    ReportingPerson: 3
}, {
    Id: 16,
    ImageUrl: "images/John.png",
    ReportingPerson: 6
}, {
    Id: 17,
    ImageUrl: "images/Jenny.png",
    ReportingPerson: 4
}, {
    Id: 18,
    ImageUrl: "images/Robin.png",
    ReportingPerson: 4
}, {
    Id: 19,
    ImageUrl: "images/Clayton.png",
    ReportingPerson: 4
}, {
    Id: 20,
    ImageUrl: "images/image57.png",
    ReportingPerson: 12
}, {
    Id: 21,
    ImageUrl: "images/Robin.png",
    ReportingPerson: 5
}, {
    Id: 22,
    ImageUrl: "images/image51.png",
    ReportingPerson: 6
}, {
    Id: 23,
    ImageUrl: "images/image55.png",
    ReportingPerson: 19
}, {
    Id: 24,
    ImageUrl: "images/Thomas.png",
    ReportingPerson: 8
}, {
    Id: 25,
    ImageUrl: "images/image56.png",
    ReportingPerson: 8
}, {
    Id: 26,
    ImageUrl: "images/image55.png",
    ReportingPerson: 1
}, {
    Id: 27,
    ImageUrl: "images/image57.png",
    ReportingPerson: 13
}, {
    Id: 28,
    ImageUrl: "images/Robin.PNG",
    ReportingPerson: 12
}, {
    Id: 29,
    ImageUrl: "images/Thomas.PNG",
    ReportingPerson: 13
}, {
    Id: 30,
    ImageUrl: "images/image57.png",
    ReportingPerson: 19
}, ];

//Bind custom JSON with node
function nodeTemplate(diagram, node) {
    node.name = node.Id;
    node.source = node.ImageUrl;
}

$("#diagram").ejDiagram({
    width: "100%",
    height: "700px",
    //use layout to auto-arrange nodes on the diagram page          
    layout: {
        type: "radialtree",
        horizontalSpacing: 30,
        verticalSpacing: 30
    },
    //set the default properties of the nodes
    defaultSettings: {
        node: {
            width: 50,
            height: 50,
            borderColor: "transparent",
            type: "image"
        }
    },
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        id: "Id",
        parent: "ReportingPerson",
        dataSource: data
    },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img2.png" %}

## Organizational Chart

An **organizational chart** is a diagram that displays the structure of an organization and relationships. To create an organizational chart, `type` property of layout should be set as organizatoinal chart.
The following code example illustrates how to create an organizational chart.

{% highlight js %}

//Initialize data source
var data = [{
    Id: "parent",
    Role: "Project Management"
}, {
    Id: 1,
    Role: "R&D Team",
    Team: "parent"
}, {
    Id: 3,
    Role: "Philosophy",
    Team: "1"
}, {
    Id: 4,
    Role: " Organization",
    Team: "1"
}, {
    Id: 5,
    Role: "Technology",
    Team: "1"
}, {
    Id: 7,
    Role: " Funding",
    Team: "1"
}, {
    Id: 8,
    Role: "Resource Allocation",
    Team: "1"
}, {
    Id: 9,
    Role: "Targeting",
    Team: "1"
}, {
    Id: 11,
    Role: "Evaluation",
    Team: "1"
}, {
    Id: 156,
    Role: "HR Team",
    Team: "parent"
}, {
    Id: 13,
    Role: "Recruitment",
    Team: "156"
}, {
    Id: 113,
    Role: "Training",
    Team: "12"
}, {
    Id: 112,
    Role: "Employee Relation",
    Team: "156"
}, {
    Id: 14,
    Role: "Record Keeping",
    Team: "12"
}, {
    Id: 15,
    Role: "Compensations & Benefits",
    Team: "12"
}, {
    Id: 16,
    Role: "Compliances",
    Team: "12"
}, {
    Id: 17,
    Role: "Production & Sales Team",
    Team: "parent"
}, {
    Id: 119,
    Role: "Design",
    Team: "17"
}, {
    Id: 19,
    Role: "Operation",
    Team: "17"
}, {
    Id: 20,
    Role: "Support",
    Team: "17"
}, {
    Id: 21,
    Role: "Quality Assurance",
    Team: "17"
}, {
    Id: 23,
    Role: "Customer Interaction",
    Team: "17"
}, {
    Id: 24,
    Role: "Support and Maintenance",
    Team: "17"
}, {
    Id: 25,
    Role: "Task Coordination",
    Team: "17"
}];

//Bind JSON data with node
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Role;
}

//Initialize diagram
$("#diagram").ejDiagram({
    //Define default layout as organizational chart
    layout: {
        type: "organizationalchart"
    },
    defaultSettings: {
        //set the default properties of the node.
        node: {
            width: 100,
            height: 40,
            fillColor: "#546e20",
            labels: [{
                name: "label1",
                fontColor: "white"
            }]
        },
        //set the default properties of the connector.    
        connector: {
            segments: [{
                "type": "orthogonal"
            }],
            targetDecorator: {
                shape: "none"
            }
        }
    },
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        id: "Id",
        parent: "Team",
        dataSource: data
    },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img3.png" %}

Organizational chart layout starts parsing from root and iterate through all its child elements. ‘getLayoutInfo’ method provides necessary information of a node’s children and the way to arrange (direction, orientation, offsets, etc.) them. You can customize the arrangements by overriding this function, explained as follows.

### GetLayoutInfo

You can set Chart orientations, chart types and offset to be left between parent and child nodes by overriding the method diagram.model.layout.getLayoutInfo. The getLayoutInfo method is called to configure every subtree of the organizational chart. And it takes the following arguments.

  * diagram (Reference of diagram)
  * node (Parent node to that options are to be customized)
  * options (object to set the customizable properties)
  
The following code example illustrates how to define the method getLayoutInfo.

{% highlight js %}

var  chartOrientations = ej.datavisualization.Diagram.ChartOrientations;
var  chartTypes = ej.datavisualization.Diagram.ChartTypes;
 
//Defining getLayoutInfo
function getLayoutInfo(diagram, node, options) {
    options.orientation = chartOrientations.Vertical;
    //Configures the sub tree of the node vertically at right side.
    options.type = chartTypes.Right;
    options.offset = 10;
}
 
//Initialize diagram
$("#diagram").ejDiagram({
    //use automatic layout to arrange elements
    layout: {
        type: "organizationalchart",
        getLayoutInfo: getLayoutInfo
    }
});

{% endhighlight %}

Following table illustrates the properties that "options" argument takes.

<table>
<tr>
<th>
Property</th><th>
Description</th><th>
Default Value</th></tr>
<tr>
<td>
options.children</td><td>
Contains the list of child nodes.Children collection can be modified.</td><td>
Array of child nodes</td></tr>
<tr>
<td>
options.assistants</td><td>
By default, the collection is empty. When any of the child nodes have to be set as "Assistant", you can remove from children collection and have to insert into assistants collection. </td><td>
Empty array</td></tr>
<tr>
<td>
options.orientation</td><td>
Gets or sets the organizational chart orientation. </td><td>
ChartOrientation.Vertical </td></tr>
<tr>
<td>
options.type</td><td>
Gets or sets the chart organizational chart type </td><td>
For horizontal chart orientation:ChartType.Center For Vertical chart orientation:ChartType.Alternate</td></tr>
<tr>
<td>
options.offset</td><td>
Offset is the horizontal space to be left between parent and child nodes.</td><td>
20 pixels.Applicable only for vertical chart orientations.</td></tr>
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
By default, Connections are routed based on the chart type and orientations.This property gets or sets whether default routing is to be enabled or disabled.</td><td>
true</td></tr>
</table>


Following table illustrates the different chart orientations and chart types.

<table>
<tr>
<th>
Orientation </th><th>
Type </th><th>
Description</th><th>
Example</th></tr>
<tr>
<td>
Horizontal</td><td>
Left</td><td>
Arranges the child nodes horizontally at the left side of parent.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img4.png" alt="" width="225pt" height="85pt"/></td></tr>
<tr>
<td>
 </td><td>
Right</td><td>
Arranges the child nodes horizontally at the right side of parent.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img5.png" alt="" width="224pt" height="84pt"/></td></tr>
<tr>
<td>
 </td><td>
Center</td><td>
Arranges the children like standard tree layout orientation.</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img6.png" alt="" width="223pt" height="83pt"/></td></tr>
<tr>
<td>
Vertical</td><td>
Left</td><td>
Vertically arranges the children at the left side of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img7.png" alt="" width="111pt" height="139pt"/></td></tr>
<tr>
<td>
 </td><td>
Right</td><td>
Vertically arranges the children at the right side of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img8.png" alt="" width="111pt" height="138pt"/></td></tr>
<tr>
<td>
 </td><td>
Alternate</td><td>
Vertically arranges the children at both left and right sides of parent</td><td>
<img src="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img9.png" alt="" width="157pt" height="105pt"/></td></tr>
</table>

Following code example illustrates how to set the vertical right arrangement to the leaf level trees.

{% highlight js %}

//Initialize data source
var data = [{
    Id: "parent",
    Role: "Board"
}, {
    Id: "1",
    Role: "General Manager",
    Manager: "parent"
}, {
    Id: "2",
    Role: "Human Resource Manager",
    Manager: "1"
}, {
    Id: "3",
    Role: "Trainers",
    Manager: "2"
}, {
    Id: "4",
    Role: "Recruiting Team",
    Manager: "2"
}, {
    Id: "5",
    Role: "Finance Asst. Manager",
    Manager: "2"
}, {
    Id: "6",
    Role: "Design Manager",
    Manager: "1",
}, {
    Id: "7",
    Role: "Design Supervisor",
    Manager: "6"
}, {
    Id: "8",
    Role: "Development Supervisor",
    Manager: "6"
}, {
    Id: "9",
    Role: "Drafting Supervisor",
    Manager: "6"
}, {
    Id: "10",
    Role: "Marketing Manager",
    Manager: "1",
}, {
    Id: "11",
    Role: "Oversea sales Manager",
    Manager: "10"
}, {
    Id: "12",
    Role: "Petroleum Manager",
    Manager: "10"
}, {
    Id: "13",
    Role: "Service Dept. Manager",
    Manager: "10"
}, ];

var  chartOrientations = ej.datavisualization.Diagram.ChartOrientations;
var  chartTypes = ej.datavisualization.Diagram.ChartTypes;

//creating the node template
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Role;
}

function getLayoutInfo(diagram, node, options) {
    if (!options.hasSubTree) {
        options.type = chartTypes.Right;
        options.orientation = chartOrientations.Vertical;
    }
}

//Initialize diagram
$("#diagram").ejDiagram({
    //Define default layout as organizational chart
    layout: {
        type: "organizationalchart",
        getLayoutInfo: getLayoutInfo
    },
    defaultSettings: {
        node: {
            width: 100,
            height: 40,
            fillColor: "#3c418B",
            borderColor: "transparent",
            labels: [{
                fontColor: "white"
            }]
        },
        connector: {
            segments: [{
                "type": "orthogonal"
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
        id: "Id",
        parent: "Manager",
        dataSource: data
    },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img10.png" %}

### Assistant

**Assistants** are child item that have a different relationship with the parent node. They are laid out in a dedicated part of the tree. You can specify a node as an assistant of its parent by adding it to **assistants** property of the argument "options".

The following code example illustrates how to add assistants to layout.

{% highlight js %}

//Initialize data source
var data = [{
    Id: 1,
    Role: "General Manager"
}, {
    Id: 2,
    Role: "Assistant Manager",
    Team: 1
}, {
    Id: 3,
    Role: "Human Resource Manager",
    Team: 1
}, {
    Id: 4,
    Role: "Design Manager",
    Team: 1
}, {
    Id: 5,
    Role: "Operation Manager",
    Team: 1
}, {
    Id: 6,
    Role: "Marketing Manager",
    Team: 1
}, ];

//creating the node template
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Role;
}

//defining getLayoutInfo 
function getLayoutInfo(diagram, node, options) {
    if (node.labels[0].text == "General Manager") {
        options.assistants.push(options.children[0]);
        options.children.splice(0, 1);
    }
    options.orientation = "horizontal";
    options.type = "center"
}

//Initialize diagram
$("#diagram").ejDiagram({
    //Define default layout as organizational chart
    layout: {
        type: "organizationalchart",
        getLayoutInfo: getLayoutInfo
    },
    defaultSettings: {
        node: {
            width: 100,
            height: 40,
            fillColor: "#546e20",
            labels: [{
                name: "label1",
                fontColor: "white"
            }]
        },
        connector: {
            segments: [{
                "type": "orthogonal"
            }],
            targetDecorator: {
                shape: "none"
            }
        }
    },
    nodeTemplate: nodeTemplate,
    dataSourceSettings: {
        id: "Id",
        parent: "Team",
        dataSource: data
    },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img11.png" %}

## Customize Layout

Orientation, spacings and position of layout can be customized with a set of properties.

To explore layout properties, refer [Layout Properties](/js/api/ejDiagram "members:layout").

### Layout Orientation 

Diagram provides support to customize the orientation of layout. You can set the desired orinetation to the `orientation` property of layout. For more information about orientation, refer [Layout Orientations](/js/api/global "LayoutOrientations")

The following code illustrates how to arrange the nodes in a "BottomToTop" orientation.

{% highlight js %}

var type = ej.datavisualization.Diagram.LayoutTypes;
var orientation = ej.datavisualization.Diagram.LayoutOrientations;

$("#diagram").ejDiagram({
    layout: {
        //Sets the type of the layout
        type: type.HierarchicalTree,
        //Sets the orientation
        orientation: orientation.BottomToTop,
        //Sets the space to be horizontally left between nodes
        horizontalSpacing: 20,
        //Sets the space to be vertically left between nodes
        verticalSpacing: 20
    },
    defaultSettings: {
        //set the default properties of the node.
        //set the default properties of the connector.    
    },

    //initialize the node template.
    nodeTemplate: nodeTemplate,

    //configure data source for diagram
    dataSourceSettings: {
        //specifies the dataSource
    }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img12.png" %}

### Fixed Node

Layout provides support to arrange the nodes with reference to the position of a fixed node and the fixed node has to be set to the`fixedNode` propery of layout. 
This will be helpful, when you try to expand/collapse a node. It might be expected that the position of the double clicked node should not be changed. 

{% highlight js %}

//Initialize data source
var data = [{
    name: "parent",
    Role: "General Manager",
    offsetX: 250, offsetY: 50
}, {
    name: "1",
    Role: "Human Resource Manager",
    Manager: "parent"
}, {
    name: "2",
    Role: "Design Manager",
    Manager: "parent",
}, {
    name: "3",
    Role: "Marketing Manager",
    Manager: "parent",
}];

//creating the node template
function nodeTemplate(diagram, node) {
    node.labels[0].text = node.Role;
}

//defining getLayoutInfo 
function getLayoutInfo(diagram, node, options) {
    options.orientation = "horizontal";
    options.type = "center"
}

//Initialize diagram
$("#DiagramContent").ejDiagram({
    //Define default layout as organizational chart
    layout: {
        type: "organizationalchart", fixedNode: "parent",
        getLayoutInfo: getLayoutInfo
    },
    defaultSettings: {
        //set the default properties of the node.
        //set the default properties of the connector.    
    },
    nodeTemplate: nodeTemplate,
    //configure data source for diagram
    dataSourceSettings: {
        //specifies the dataSource
    }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Automatic-Layout_images/Automatic-Layout_img13.png" %}

### Expand and collapse

Diagram allows to expand/collapse the sub trees of a layout. `isExpanded` property of node allows you to expand/collapse its children. Following code example shows how to expand/collapse the children of a node. 
    
{% highlight js %}

//Initialize diagram
$("#diagram").ejDiagram({
    //Define default layout as organizational chart
    layout: {
        type: "organizationalchart", fixedNode: "node1"
    },
    //Define double click event
    doubleClick: onDoubleClick
});

function onDoubleClick(args) {
    var diagram = $("#diagram").ejDiagram("instance");
    var node = args.element;
    
    // Set the double clicked node as fixed node 
    $("#diagram").ejDiagram({ layout: { fixedNode: node.name } });
        
    //Expand/collapse the children of node
    diagram.updateNode(node.name, { isExpanded: !node.isExpanded });
}

{% endhighlight %}

In above example, while expanding/collapsing a node, it is set as fixed node in order to prevent it from repositioning. 

### Refresh layout

Diagram allows to refresh the layout at runtime. To refresh the layout, refer [Refresh layout](/js/api/ejDiagram "methods:layout").