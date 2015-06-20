---
layout: post
title: Group
description: group
platform: js
control: Diagram
documentation: ug
---

# Group

**Diagram** provides support to **Group** and **Ungroup** nodes. **Group** is a composite node that has a set of child nodes/connector and it is a container for its children. All the operations performed on a Group also affect the individual child in that particular Group. You can edit any node/connector in the group individually. On **Ungrouping**, the children in the group is a individual node/connector of the Diagram model. 

## Create Group

You can create **Group** like node and add it to the Diagram model using diagram model’s **nodes** property. You can set **isGroup** property as **true** to differentiate the group from node. You can set the array of children (nodes/connectors) names to **children** property. The group’s children nodes/connectors are added to the node array before adding the group to nodes array. 

The following code illustrates how a group node is created and added in the nodes array.

{% highlight js %}

//Creates a group node.
var nodes = [
   //Group node.
   {
      name: "group",
      type: "group",
      children: [{
         name: "node1",
         parent: "group"
      }, {
         name: "node2",
         parent: "group"
      }]
   }
];

{% endhighlight %}

{% include image.html url="/js/Diagram/Group_images/Group_img1.png" Caption="Group"%}

## Selecting a Group

You can select a group by clicking on any one of its children node. Consecutive clicks on a child object select the parent groups in the order of their creation. In a similar manner, consecutive clicks on a child object leads to the selection of inner groups and eventually the object itself and this cycle continues.

The following steps illustrate how to select an object that has two groups.

{% include image.html url="/js/Diagram/Group_images/Group_img2.png" Caption="Selecting a Group"%}

1. Click on Node1 to select the outer group.
2. Click again to select the inner group to which it belongs.
3. Click again to select the child node after all groups have been traversed.

{% include image.html url="/js/Diagram/Group_images/Group_img3.png" Caption="Selecting an inner Group"%}

{% include image.html url="/js/Diagram/Group_images/Group_img4.png" Caption="Selecting a Child of Group"%}

## Editing a Group

To edit a group, select the corresponding group. You can apply the following features on Group for editing. For example, resizing a group, automatically resizes its child objects to fit the selection area.

<table>
<tr>
<td>
<b>Editing Options</b></td><td>
<b>Before </b></td><td>
<b>After</b></td></tr>
<tr>
<td>
Resize</td><td>
<img src="/js/Diagram/Group_images/Group_img5.png" alt="" width="141pt" height="177pt"/></td><td>
<img src="/js/Diagram/Group_images/Group_img6.png" alt="" width="131pt" height="139pt"/></td></tr>
<tr>
<td>
Rotate</td><td>
<img src="/js/Diagram/Group_images/Group_img7.png" alt="" width="141pt" height="177pt"/></td><td>
<img src="/js/Diagram/Group_images/Group_img8.png" alt="" width="190pt" height="188pt"/></td></tr>
</table>

_Editing a Group_

## Layout Panel

The **Container** property of **Group** can be set to any of the available **‘layout panel’**. It is used to control the size and position of Group’s children. There are two types of layout panels.

* Canvas panel 
* Stack panel

The following properties are used to align the child element on the Group, this property is applicable for all panel.

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Data type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
marginLeft</td><td>
number</td><td>
Gets or sets the left margin value of the elements.</td></tr>
<tr>
<td>
marginRight</td><td>
number</td><td>
Gets or sets the right margin value of the elements.</td></tr>
<tr>
<td>
marginBottom</td><td>
number</td><td>
Gets or sets the bottom margin value of the elements.</td></tr>
<tr>
<td>
marginTop</td><td>
number</td><td>
Gets or sets the top margin value of the elements.</td></tr>
<tr>
<td>
horizontalAlignment</td><td>
string</td><td>
Gets or sets the horizontal alignment of the elements.</td></tr>
<tr>
<td>
verticalAlignment</td><td>
string</td><td>
Gets or sets the vertical alignment of the elements.</td></tr>
<tr>
<td>
paddingTop</td><td>
number</td><td>
Gets or sets the top padding value of the group.</td></tr>
<tr>
<td>
paddingBottom</td><td>
number</td><td>
Gets or sets the bottom padding value of the group.</td></tr>
<tr>
<td>
paddingLeft</td><td>
number</td><td>
Gets or sets the left padding value of the group.</td></tr>
<tr>
<td>
paddingRight</td><td>
number</td><td>
Gets or sets the right padding value of the group.</td></tr>
</table>

_Group properties_

### Canvas Panel

The Canvas panel supports absolute positioning and provides the least layout functionality to its contained diagram elements. Canvas allows you to position contained elements at an offset and also elements can be arranged with either horizontally or vertically.

{% highlight js %}

var nodes = [{
   name: "Canvas",
   offsetX: 400,
   offsetY: 400,
   children: [{
      type: "node",
      name: "snode1",
      fillColor: "darkCyan"
   }, {
      type: "node",
      name: "snode2",
      marginTop: 30,
      marginLeft: 30,
      fillColor: "white"
   }, {
      type: "node",
      name: "snode3",
      marginTop: 60,
      marginLeft: 60,
      fillColor: "darkCyan"
   }, {
      type: "node",
      name: "snode4",
      marginTop: 90,
      marginLeft: 90,
      fillColor: "white"
   }],
   //Canvas Panel.
   container: {
      type: "canvas"
   },
   fillColor: "#E7EBF4",
   borderColor: "black",
   paddingLeft: 30,
   paddingTop: 30,
   paddingRight: 30,
   paddingBottom: 30
}];

$("#diagram").ejDiagram({
   nodes: nodes,
   defaultSettings: {
      node: {
         height: 70,
         width: 70,
         parent: "Canvas",
      },
   },
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Group_images/Group_img9.png" Caption="Canvas Panel"%}

### Stack panel

Stack panel is used to arrange its childre in a single line or stack order, either vertically or horizontally. It controls spacing by setting margin properties of child and padding properties of group. By default, a Stack Panel’s orientation is vertical. The following code illustrates how to add stack panel.

{% highlight js %}

var nodes = [{
   type: "group",
   name: "Stack",
   offsetX: 200,
   offsetY: 400,
   children: [{
      type: "node",
      name: "cnode1",
      fillColor: "darkCyan",
      horizontalAlign: "left"
   }, {
      type: "node",
      name: "cnode2",
      fillColor: "darkCyan",
      horizontalAlign: "right"
   }, {
      type: "node",
      name: "cnode3",
      fillColor: "darkCyan",
      horizontalAlign: "stretch"
   }, ],
   // Stack panel.
   container: {
      type: "stack"
   },
   fillColor: "#E7EBF4",
   borderColor: "black",
   minHeight: 300,
   minWidth: 300
}];
$("#diagram").ejDiagram({
   nodes: nodes,
   defaultSettings: {
      node: {
         height: 100,
         width: 100,
         parent: "Stack",
      },
   }
});

{% endhighlight %}

{% include image.html url="/js/Diagram/Group_images/Group_img10.png" Caption="Stack Panel containing three nodes"%}
