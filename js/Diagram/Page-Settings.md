---
layout: post
title: Page-Settings
description: page settings
platform: js
control: Diagram
documentation: ug
---

# Page Settings

**Page settings** enable you to customize the width and height of the Diagram page. The properties of Page setting are listed as follows.

<table>
<tr>
<th>
Properties</th><th>
Data Type</th><th>
Description</th></tr>
<tr>
<td>
pageWidth</td><td>
number</td><td>
Gets or sets the width of the page</td></tr>
<tr>
<td>
pageHeight</td><td>
number</td><td>
Gets or sets the height of the page</td></tr>
<tr>
<td>
multiplePage</td><td>
boolean</td><td>
Gets or sets whether  multiple page option is enabled or not</td></tr>
<tr>
<td>
pageBorderWidth</td><td>
number</td><td>
Gets or sets the border width of the page</td></tr>
<tr>
<td>
pageBackgroundColor</td><td>
string</td><td>
Gets or sets the background color of the page</td></tr>
<tr>
<td>
pageBorderColor</td><td>
string</td><td>
Gets or sets the border color of the page</td></tr>
<tr>
<td>
pageMargin</td><td>
number</td><td>
Gets or sets the  margin of the page</td></tr>
<tr>
<td>
showPageBreak</td><td>
boolean</td><td>
Gets or sets whether  page break option is enabled or not</td></tr>
<tr>
<td>
pageOrientation</td><td>
ej.datavisualization.Diagram.PageOrientations</td><td>
Gets or sets the orientation of the page</td></tr>
</table>

The following code illustrates how to customize Page Settings

{% highlight js %}

//set page setting properties
$("#Diagram").ejDiagram({
   pageSettings: {
      pageHeight: 300,
      pageWidth: 450,
      pageBorderWidth: 4,
      pageBackgroundColor: "lightblue",
      pageBorderColor: "black",
      pageMargin: 35,
      showPageBreaks: true,
      multiplePage: true,
      pageOrientation: ej.datavisualization.Diagram.Orientation.Portrait
   }
});

{% endhighlight %}

![]("/js/Diagram/Page-Settings_images/Page-Settings_img1.png") 

## MultiplePage and PageBreaks

When `multiplePage` is enabled, size of the page dynamically increases or decreases in multiples of page width and height and completely fits diagram within the page boundaries. `pageBreaks` is used as a visual guide to see how pages are split into multiple pages.

![]("/js/Diagram/Page-Settings_images/Page-Settings_img2.png") 

## AutoScroll

Autoscroll feature automatically scrolls the Diagram whenever the node or connector is beyond the boundary of the diagram so that, it is always visible during dragging, resizing and multiple selection operations. Autoscroll is automatically triggered when, any one of the following is dragged towards edges of the diagram.

* Node dragging
* Node's control points: resizer, rotator
* Connector's control points: end point, segment
* Rubber band selection
* Dropping item from palette

<table>
<tr>
<th>
Properties</th><th>
Data Type</th><th>
Description</th></tr>
<tr>
<td>
scrollLimit</td><td>
string</td><td>
Gets or sets the scroll limit of the page</td></tr>
<tr>
<td>
scrollableArea</td><td>
object</td><td>
Gets or sets the scrollable region of the page</td></tr>
<tr>
<td>
autoScrollBorder</td><td>
object</td><td>
Gets or sets the auto scroll starting point </td></tr>
</table>
_Properties table_

**Autoscroll border**

The autoscroll border is used to specify the distance, from where the autoscroll is to be enabled when moving the node or connector. The default value is set as 15 for all sides (left, right, top and bottom). The following code example illustrates how to set autoscroll border.

{% highlight js %}

pageSettings: 
    { 
        // Specifies autoscroll border
        autoScrollBorder: { left: 150, top: 15, right:15, bottom: 15}  
    }  

{% endhighlight %}

**Scroll limit**

The scroll limit allows you to scroll the diagram page along X and Y axis based on the options specified. 

* By default the value is set as `infinity` (can scroll in all directions, without any restrictions). 
* When `scrollLimit` is set as `diagram`, you are restricted to scroll the page beyond the diagram content. 
* By specifying the value as `limited` you can set the limit of the scrollable area through `scrollableArea` property. 

N>  Refer to the [scrollable area](/js/Diagram/Page-Settings#scrollable-area) for more details.

The following code example illustrates how to specify scroll limit. 

{% highlight js %}

//Scroll limit for diagram by default
pageSettings: { scrollLimit:"infinity" }

{% endhighlight %}

### Scrollable Area

You can restrict scrolling beyond a particular rectangular area and the rectangular area is specified using `scrollableArea` property. This is applicable only when the `scrollLimit` for the diagram is specified as `limited`. The following code example illustrates how to customize scrollable area of diagram.

{% highlight js %}

pageSettings: {
   //Scrolllimit for diagram as limited
   scrollLimit: "limited",

   //Set limit of the scrollable area
   scrollableArea: {
      x: 0,
      y: 0,
      width: 5000,
      height: 5000
   }
}

{% endhighlight %}

![]("/js/Diagram/Page-Settings_images/Page-Settings_img3.png") 
