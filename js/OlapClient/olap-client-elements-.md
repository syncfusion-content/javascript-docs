---
layout: post
title: olap-client-elements-
description: olap client elements 
platform: js
control: OLAP Client
documentation: ug
---

## OLAP Client Elements 

### Cube Selector

Cube Selector allows you to browse and select a cube from the entire collection, populated by the data source.

#### Change the Cube

Cube can be changed by selecting a cube name from the list of names available within the Cube Selector drop-down list. When a cube is changed, the following elements refresh according to the new cube.

_Table: Components Table_

<table>
<tr>
<td>
<b>Component</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Report List</td><td>
Maintains a collection of reports.</td></tr>
<tr>
<td>
Axis Element Builder</td><td>
Collection of axes, namely: categorical, series and slicer.</td></tr>
<tr>
<td>
Elements Editor</td><td>
Dialog that holds a tree-view control displaying the members of the current dimension, and holds a collection of measures.</td></tr>
<tr>
<td>
Cube Dimension Browser</td><td>
A tree-view structure that comprises of dimensions, hierarchies, measures etc… belonging to the current cube into independent logical groups.</td></tr>
<tr>
<td>
Chart</td><td>
A chart is a graphical representation of data, in which the data is represented by symbols such as bars in bar chart, lines in line chart, or slices in a pie chart.</td></tr>
<tr>
<td>
Grid</td><td>
A grid is a tabular representation of data, arranged in the form of rows and columns, categorized accordingly.</td></tr>
</table>


{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img1.png" Caption="Figure: Cube Selector"%}

### Cube Dimension Browser

Cube Dimension Browser is a tree-view-like structure that organizes the dimensions, hierarchies, measures etc… from the selected cube into independent, logical groups.

_Table: List of nodes_

<table>
<tr>
<td>
<b>Type Of Nodes</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Cube</td><td>
Multidimensional set of data used for dynamic analysis.</td></tr>
<tr>
<td>
Measure Group</td><td>
Composition of a set of measures.</td></tr>
<tr>
<td>
Display Folder</td><td>
Folder that contains the dimension and measure.</td></tr>
<tr>
<td>
Measure</td><td>
Actual set of measures that compose the measure group.</td></tr>
<tr>
<td>
Dimension</td><td>
A name given to the parts of the cube that categorize the data, such as Date, Customer, etc. It contains hierarchy and level elements.</td></tr>
<tr>
<td>
Attribute Hierarchy</td><td>
Level of attributes down the hierarchy.</td></tr>
<tr>
<td>
User-defined hierarchy</td><td>
Members of a dimension in a hierarchical structure.</td></tr>
</table>
**Attribute Hierarchy**

Attribute hierarchy contains the following levels:

* A leaf level contains each distinct attribute member called leaf member with each member of the leaf level.

* Intermediate levels if the attribute hierarchy is a parent-child hierarchy.

* An optional (All) level (IsAggregatable=True) containing the aggregated value of the attribute hierarchy's leaf members, with the member of the (All) level also known as the (All) member.

**User-Defined Hierarchy**

User-defined hierarchy organizes the members of a dimension into hierarchical structure and provides navigation paths in a cube. For example, take a dimension table that supports three attributes such as Year, Quarter and Month. The Year, Quarter and Month attributes are used to construct a user-defined hierarchy, named Calendar, in the time dimension.

**Differentiating Attribute hierarchy and User-defined hierarchy**

Attribute hierarchy and User-defined hierarchy are normally differentiated by their tree node image.

_Table: Differentiating Attribute hierarchy and User-defined hierarchy_

<table>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img2.png" alt="" width="25pt" height="28pt"</td><td>
Attribute Hierarchy, contains only one level.</td></tr>
<tr>
<td>
<b> </b><img src="olap-client-elements-_images\olap-client-elements-_img3.png" alt="" width="22pt" height="24pt"</td><td>
User Defined Hierarchy and its levels are mentioned with a similar image. It contains one or more levels.</td></tr>
</table>
**Symbolic Representation of the Nodes inside Cube Dimension Browser**

_Table: Symbolic Representation of the Nodes inside Cube Dimension Browser_

<table>
<tr>
<th>
<b>Icon</b></th><th>
<b>Name</b></th></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img4.png" alt="" width="29pt" height="25pt"</td><td>
Display Folder</td></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img5.png" alt="" width="22pt" height="24pt"</td><td>
Measure</td></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img6.png" alt="" width="28pt" height="28pt"</td><td>
Dimension</td></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img7.png" alt="" width="29pt" height="28pt"</td><td>
User Defined Hierarchy</td></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img8.png" alt="" width="19pt" height="26pt"</td><td>
Attribute Hierarchy</td></tr>
<tr>
<td>
<img src="olap-client-elements-_images\olap-client-elements-_img9.png" alt="" width="22pt" height="24pt"</td><td>
Level Element</td></tr>
</table>


**Draggable and non-draggable nodes in the Cube Dimension Browser**

The dragabble nodes are:

* Measure

* Dimension

* Hierarchy

* Level Elements

The nodes that are not allowed to be dragged are:

* Cube

* Display Folder

### Axis Element Builder

Axis Element Builder allows you to build the element in an axis of the **OLAP Client**. It supports three axes namely: Categorical, Series and Slicer. Based on the elements constructed **OLAP Grid** and **OLAP Chart** will display the resultant data.

**Categorical (Column)**

The categorical axis defines one or more dimensions that are displayed along the chart's y-axis as labels and in the columns of the grid. If more than one dimension is on the categorical axis, the **Chart/Grid** will stack each dimension. The order in which the dimensions are stacked on the **Chart/Grid** is based on the order that they appear on the categorical axis.

**Series (Row)**

The series axis defines one or more dimensions that are displayed along the chart's x-axis as labels and in the rows of the grid. If more than one dimension is on the series axis, the **Chart/Grid** will stack each dimension. The order in which the dimensions are stacked on the **Chart/Grid** is based on the order that they appear on the series axis.

**Slicer**

The slicer axis is used as a filter to narrow the focus of the multidimensional data displayed in the **Chart/Grid**. The slicer axis lets you analyze any member of a dimension, in-depth. For the slicer to display the member's data, that member must not be present on both categorical axis and series axis.



.{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img10.png" Caption="Figure: Axis Element Builder"%}

#### Addition of Elements to an Axis Element Builder

##### Add Dimension, Hierarchy and Level to an Axis Element Builder 

The dimension, hierarchy and level elements can be dragged from the Cube Dimension Browser and dropped into the Axis Element Builder using the drag-and-drop operation. Also you can move the dimension, hierarchy and level elements from one axis to another by moving the appropriate Split Button.



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img11.png" Caption="Figure: Adding Dimension to Axis Element Builder"%}

##### Add Measure to an Axis Element Builder

The measure elements can be dragged from Cube Dimension Browser and dropped into Axis Element Builder using drag-and-drop operation. Also user can move the measure elements from one axis to another by moving the Split Button named Measures.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img12.png" Caption="Figure: Adding Measure to an Axis Element Builder"%}

#### Remove Elements from an Axis Element Builder

**Remove Dimension, Hierarchy and Level from an Axis Element Builder**

In order to remove dimension, hierarchy and level element from the Axis Element Builder, click the Remove symbol available next to the Split Button while hovering over it.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img13.png" Caption="Figure: Removing an element in Axis Element Builder"%}

##### Remove Measure from an Axis Element Builder

To remove the measure element from the Axis Element Builder, click the Remove symbol available next to the Measures Split Button while hovering over it.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img14.png" Caption="Figure: Removing Measure in Axis Element Builder "%}

#### Rearrange Elements in an Axis Element Builder

Rearranging can be done by dragging an element one below the other.

![](olap-client-elements-_images\olap-client-elements-_img15.png)



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img16.png" Caption="Figure: Rearranging elements"%}

### Split Button

Split Button highlights the elements in the Axis Element Builder. It holds dimensions/measures. When you drag and drop a node from Cube Dimensional Browser into Axis Element Builder**,** a Split Button is created, displaying the dimension name.

![](olap-client-elements-_images\olap-client-elements-_img17.png)

Figure: Split Button – Dimension

When you drag and drop a measure, the Axis Element Builder will create a Split Button only for the first measure. The next time a measure is added, it maintains the same single Split Button to hold the entire measure collection.


{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img18.png" Caption="Figure: Split Button – Measure"%}

##### Remove Split Button

Split Button can be removed with the help of the Remove option available while hovering over it.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img19.png" Caption="Figure: Removing Split Button"%}

### Elements Editor

**Measure Editor**

Measure Editor is a dialog that displays the collection of measures in the current report. 



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img20.png" Caption="Figure: Measure Editor"%}

**Remove a Measure** 

To remove a measure, click the Remove button next to the corresponding measure while hovering over it. To avoid removing the current selection, click Cancel.



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img21.png" Caption="Figure: Removing a Measure"%}

**Member Editor**

Member Editor is a tree-view control that displays the member elements of the current dimension.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img22.png" Caption="Figure: Member Editor"%}

**Represent State of Nodes of a dimension**

Nodes are represented in two states, namely:

* Checked

* Unchecked

**Select and Clear Nodes of a Dimension in the Member Editor**

The option Select is provided in such a way that on selecting the parent node, its corresponding child nodes are automatically selected. If a leaf node is selected, it does not affect others since it is the final node on a tree.

Unchecking the check box option is provided in such a way that on deselecting the parent node, its corresponding child nodes are automatically deselected. On deselecting all the child nodes, its corresponding parent node is automatically deselected.



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img23.png" Caption="Figure: Selecting and Unselecting Nodes"%}

**Check All and Uncheck All**

* **Check All** – Will select all nodes in the tree view.

* **Uncheck All** – Will uncheck all nodes in the tree view.

{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img24.png" Caption="Figure: Check all nodes"%}

### Toolbar



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img25.png" Caption="Figure: OLAP Client Toolbar"%}

_Table: Options Table_

<table>
<tr>
<th>
<b>Option</b></th><th>
<b>Description</b></th></tr>
<tr>
<td>
New Report</td><td>
Creates a new report, clearing the existing report in order to provide a new platform for new deployment based on the existing cube elements.</td></tr>
<tr>
<td>
Add Report</td><td>
Add a report to the existing list of reports.</td></tr>
<tr>
<td>
Remove Report</td><td>
Removes the current report from the report list. The button gets disabled if and only if the report list contains one report in it.</td></tr>
<tr>
<td>
Rename Report</td><td>
The rename option changes the name of the current report as per your input.</td></tr>
<tr>
<td>
Save Report</td><td>
The save option stores the current report/reports contained in the report list in a database.</td></tr>
<tr>
<td>
Load Report</td><td>
The load report option picks the saved report from the database.</td></tr>
<tr>
<td>
Exporting to Excel</td><td>
This option is used to export the Grid data to Excel format.</td></tr>
<tr>
<td>
Report List</td><td>
Select a report from the existing report collection.</td></tr>
<tr>
<td>
Filter/Sort column</td><td>
Filters/Sorts the data in the OlapReport with respect to Column.</td></tr>
<tr>
<td>
Filter/Sort Row</td><td>
Filters/Sorts the data in the OlapReport with respect to Row.</td></tr>
<tr>
<td>
Full Screen View</td><td>
This option is used to display Grid and Chart in a maximized view, according to the browsers height and width.</td></tr>
</table>
### Report List

Report List will hold all the reports of the current session of the **OLAP Client** control.



![](olap-client-elements-_images\olap-client-elements-_img26.png)



{% include image.html url="\js\OlapClient\olap-client-elements-_images\olap-client-elements-_img27.png" Caption="Figure: Report List"%}

When a change is made in the report, **OLAP** visualization controls and Axis Element Builder get re-populated with the data contained in the selected report.

### OLAP Grid

The **OLAP Grid** control for **JavaScript** is easily configurable, presentation-quality business control that reads **OLAP** data from a **Microsoft SQL Server Analysis Services** database, an **offline cube** or **XMLA**. The **OLAP** data is displayed with drill-up and drill-down capabilities and features exceptional performance.

For further information please refer the following link. [http://help.syncfusion.com/ug/js/default.htm#!Documents/overview25.htm](http://help.syncfusion.com/ug/js/default.htm)

### OLAP Chart

The **OLAP Chart** control for **JavaScript** is a lightweight control that reads **OLAP** information and visualizes it in graphical format with the ability to drill up and down. 

For further information please refer the following link.

[http://help.syncfusion.com/ug/js/default.htm#!Documents/overview22.htm](http://help.syncfusion.com/ug/js/default.htm)

