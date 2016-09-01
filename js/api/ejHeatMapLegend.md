---
layout: post
title: Properties, Methods and Events of ejHeatMapLegend Widget
description: API reference for ejHeatMapLegend
documentation: API
platform: js
keywords: heat map, ejHeatMapLegend, heat map api, syncfusion
---

#ejHeatMapLegend

The diagram control provides 2D surface to visualize the data as shapes, lines, text and images. It can be configured to DOM element such as DIV.

#### Syntax
$(element).ejHeatMapLegend();

#### Example

{% highlight html %}
 
 

{% endhighlight %}

#### Requires

* module:jquery.js
* module:jquery.easing.min.js
* module:jsrender.min.js
* module:ej.core.js
* module:ej.draggable.js
* module:ej.scroller.js
* module:ej.touch.js
* module:ej.diagram.js
* module:ej.diagramcommon.js
* module:ej.diagraminteraction.js
* module:ej.diagramsvg.js
* module:ej.diagramtools.js
* module:ej.diagramlayout.js
* module:ej.matrix.js

## Members


### width `Number`
{:#members:width}

Specifies the width of the diagram

#### Default Value:

* null

#### Example

{% highlight html %}

{% endhighlight %}




### height `Number`
{:#members:height}

Specifies the width of the diagram

#### Default Value:

* null

#### Example

{% highlight html %}

{% endhighlight %}

 



### isResponsive `Boolean`
{:#members:isResponsive}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

{% endhighlight %}

 }
 
  
 





### showLabel `Boolean`
{:#members:showLabel}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

{% endhighlight %}

 }
 
 
 
 





### colorMappingCollection `Array`
{:#members:colorMappingCollection}

Array of JSON objects where each object represents a node

#### Default Value:

* []

#### Example

{% highlight html %}
 

{% endhighlight %}

### colorMappingCollection.color `String`
{:#members:colorMappingCollection-color}

Sets the border color of node

#### Default Value:

* "black"

#### Example

{% highlight html %}

 

{% endhighlight %}

### colorMappingCollection.value `Number`
{:#members:colorMappingCollection-value}

Sets the border color of node

#### Default Value:

* "black"

#### Example

{% highlight html %}
 

{% endhighlight %}

### colorMappingCollection.label `Object`
{:#members:colorMappingCollection-label}

A collection of objects where each object represents a label

#### Default Value:

* []

#### Example

{% highlight html %}

 

{% endhighlight %}

### colorMappingCollection.label.bold `Boolean`
{:#members:colorMappingCollection-label-bold}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

 

{% endhighlight %}

### colorMappingCollection.label.italic `Boolean`
{:#members:colorMappingCollection-label-italic}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

 
{% endhighlight %}

### colorMappingCollection.label.text `String`
{:#members:colorMappingCollection-label-text}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}
 
{% endhighlight %}

### colorMappingCollection.label.textDecoration `enum`
{:#members:colorMappingCollection-label-textDecoration}

<ts name = "ej.HeatMap.TextDecoration "/>

Enables/disables the bold style

<table class="props">
   <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
   <tbody>
        <tr>
            <td class="name">Underline</td>
            <td class="description last">Scales the graphic content non-uniformly to the width and height of the diagram area
            </td>
       </tr>
        <tr>
            <td class="name">Overline</td>
            <td class="description last">Used to align the image at the top left of diagram area </td>
       </tr>
        <tr>
            <td class="name">LineThrough</td>
            <td class="description last">Used to align the image at the left center of diagram area</td>
       </tr>
        <tr>
            <td class="name">None</td>
            <td class="description last">Used to align the image at the bottom left of diagram area</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* false

#### Example

{% highlight html %}
 

{% endhighlight %}

### colorMappingCollection.label.fontSize `Number`
{:#members:colorMappingCollection-label-fontSize}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}
 
{% endhighlight %}

### colorMappingCollection.label.fontFamily `String`
{:#members:colorMappingCollection-label-fontFamily}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

{% endhighlight %}

### colorMappingCollection.label.fontColor `String`
{:#members:colorMappingCollection-label-fontColor}

Enables/disables the bold style

#### Default Value:

* false

#### Example

{% highlight html %}

{% endhighlight %}




### orientation `enum`
{:#members:orientation}

<ts name = " ej.HeatMap.LegendOrientation"/>

Enables/disables the bold style

<table class="props">
   <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
   <tbody>
        <tr>
            <td class="name">Horizontal</td>
            <td class="description last">Scales the graphic content non-uniformly to the width and height of the diagram area
            </td>
       </tr>
        <tr>
            <td class="name">Vertical</td>
            <td class="description last">Used to align the image at the top left of diagram area </td>
       </tr> 
   </tbody>
</table>




### legendMode `enum`
{:#members:legendMode}

<ts name = " ej.HeatMap.LegendMode"/>

Enables/disables the bold style

<table class="props">
   <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
       </tr>
   </thead>
   <tbody>
        <tr>
            <td class="name">Gradient</td>
            <td class="description last">Scales the graphic content non-uniformly to the width and height of the diagram area
            </td>
       </tr>
        <tr>
            <td class="name">List</td>
            <td class="description last">Used to align the image at the top left of diagram area </td>
       </tr> 
   </tbody>
</table>