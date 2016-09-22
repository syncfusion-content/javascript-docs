---
layout: post
title: Properties, Methods and Events of ejHeatMapLegend Widget
description: API reference for ejHeatMapLegend
documentation: API
platform: js
keywords: heatMapLegend, ejHeatMapLegend, heatMapLegend api, syncfusion
---

# ejHeatMapLegend
<ts root="datavisualization" />

Legend is a control used to summarize the range of colors in HeatMap. This gives visual guideline for mapping between value and color.

#### Syntax

     $("#heatmapLegend").ejHeatMapLegend();

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend();
    </script>
{% endhighlight %}

#### Requires

* module:ej.heatmap.base.js
* module:ej.heatmap.js
* module:ej.core.js
* module:ej.data.js   
* module:ej.globalize.js
* module:ej.touch.js  
* module:ej.scroller.js  

## Members


### width `Object`
{:#members:width}

Specifies the width of the heatmap legend.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            width: "400px"
        });
    </script>

{% endhighlight %}




### height `Object`
{:#members:height}

Specifies the height of the heatmap legend.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            height: "400px"
        });
    </script>

{% endhighlight %}
 

### isResponsive `Boolean`
{:#members:isResponsive}

Specifies can enable responsive mode or not for heatmap legend.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            isResponsive: true
        });
    </script>

{% endhighlight %}
 


### showLabel `Boolean`
{:#members:showLabel}

Specifies whether the cell label can be shown or not.

#### Default Value:

* false

#### Example

{% highlight html %}


    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            showLabel: false
        });
    </script>

{% endhighlight %}
 
  



### colorMappingCollection `Array`
{:#members:colorMappingCollection}

Specifies the color values of the column data.

#### Default Value:

* []

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { text: "0" } },
            { value: 100, color: "#0d47a1", label: { text: "100" } }
            ]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.color `String`
{:#members:colorMappingCollection-color}

Specifies the color of the heatmap legend data.

#### Default Value:

* "white"

#### Example

{% highlight html %}

     <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { text: "0" } },
            { value: 100, color: "#0d47a1", label: { text: "100" } }
            ]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.value `Number`
{:#members:colorMappingCollection-value}

Specifies the color values of the heatmap legend column data.

#### Default Value:

* 0

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { text: "0" } },
            { value: 100, color: "#0d47a1", label: { text: "100" } }
            ]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label `Object`
{:#members:colorMappingCollection-label}

Specifies the label properties of the heatmap legend color.

#### Default Value:

* null

#### Example

{% highlight html %}

     <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { text: "0" } },
            { value: 100, color: "#0d47a1", label: { text: "100" } }
            ]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.bold `Boolean`
{:#members:colorMappingCollection-label-bold}

Enables/disables the bold style of the heatmap legend label.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { bold: true } }]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.italic `Boolean`
{:#members:colorMappingCollection-label-italic}

Enables/disables the italic style of the heatmap legend label.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { italic: true } }]
        });
    </script>
 
{% endhighlight %}

### colorMappingCollection.label.text `String`
{:#members:colorMappingCollection-label-text}

specifies the text value of the heatmap legend label.

#### Default Value:

* ""

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { text: "10" } }]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.textDecoration `enum`
{:#members:colorMappingCollection-label-textDecoration}

<ts ref = "ej.datavisualization.HeatMap.TextDecoration "/>

Specifies the text style of the heatmap legend label.

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
            <td class="description last">Defines a line below the text
            </td>
       </tr>
        <tr>
            <td class="name">Overline</td>
            <td class="description last">Defines a line above the text</td>
       </tr>
        <tr>
            <td class="name">LineThrough</td>
            <td class="description last">Defines a line through the text</td>
       </tr>
        <tr>
            <td class="name">None</td>
            <td class="description last">Defines a normal text. This is default</td>
       </tr>
   </tbody>
</table>

#### Default Value:

* ej.HeatMap.TextDecoration.None

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { textDecoration: ej.HeatMap.TextDecoration.None } }]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.fontSize `Number`
{:#members:colorMappingCollection-label-fontSize}

Specifies the font size of the heatmap legend label.

#### Default Value:

* 10

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { fontSize: 16 } }]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.fontFamily `String`
{:#members:colorMappingCollection-label-fontFamily}

Specifies the font family of the heatmap legend label.

#### Default Value:

* "Arial"

#### Example

{% highlight html %}
  
  <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { fontFamily: "Arial" } }]
        });
    </script>

{% endhighlight %}

### colorMappingCollection.label.fontColor `String`
{:#members:colorMappingCollection-label-fontColor}

Specifies the font color of the heatmap legend label.

#### Default Value:

* "black"

#### Example

{% highlight html %}

    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            colorMappingCollection: [
            { value: 0, color: "#8ec8f8", label: { fontColor: "red" } }]
        });
    </script>

{% endhighlight %}




### orientation `enum`
{:#members:orientation}

<ts name = "ej.datavisualization.HeatMap.LegendOrientation"/>

Specifies the orientation of the heatmap legend 

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

#### Default Value:

*  ej.HeatMap.LegendOrientation.Horizontal

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            orientation: ej.HeatMap.LegendOrientation.Vertical
        });
    </script>


{% endhighlight %}



### legendMode `enum`
{:#members:legendMode}

<ts name = "ej.datavisualization.HeatMap.LegendMode"/>

Specifies the legend mode as gradient or list.

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

#### Default Value:

*  ej.HeatMap.LegendMode.Gradient

#### Example

{% highlight html %}
 
    <div id="heatmapLegend"></div>
    <script>
        $("#heatmapLegend").ejHeatMapLegend({
            legendMode: ej.HeatMap.LegendMode.List
        });
    </script>

{% endhighlight %}