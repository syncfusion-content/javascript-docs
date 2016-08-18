---
layout: post
title: API reference for ejSparkline
description: What are the options, methods and events available in Essential JavaScript Sparkline.
documentation: API
platform: js
keywords: ejSparkline, API, Essential JS Sparkline, Sparkline
metaname: 
metacontent: 
---

# ejSparkline
<ts root="datavisualization" />

Essential sparkline can be easily configured to the DOM element, such as div. You can create a Sparkline with highly customizable look and feel.


#### Syntax

{% highlight js %}

$(element).ejSparkline();

{% endhighlight %}


#### Example


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Create Sparkline
$('#container').ejSparkline();      
</script>

{% endhighlight %}




#### Requires

* module:jQuery.js

* module:ej.core.js

* module:ej.data.js

* module:ej.sparkline.js

* module:ej.globalize.js


## Members

### background `string`
{:#members:background}

Background color of the plot area.

#### Default Value

* transparent

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

    background : "white" 
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/picztz23)




### fill `string`
{:#members:fill}

Fill color for the sparkline series.

#### Default Value

* "#33ccff"

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    fill : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### stroke `string`
{:#members:stroke}

Border color of the series.

#### Default Value

*  null

#### Example

{% highlight js %}
  
$("#container").ejSparkline({
    stroke: "green"                   
});

{% endhighlight %}



### border `object`
{:#members:border}

Options for customizing the color, opacity and width of the sparkline border.



### border.color `string`
{:#members:border-color}

Border color of the sparkline.


#### Default Value

* transparent

#### Example

{% highlight js %}
                             
$("#container").ejSparkline({

   border: { color: "green" }                      

});

{% endhighlight %}




### border.width `number`
{:#members:border-width}

Width of the Sparkline border.

#### Default Value

* 1

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   border: { width: 2 }                      

});

{% endhighlight %}




### width `number`
{:#members:width}

Border width of the series.

#### Default Value

* 1

#### Example

{% highlight js %}

$("#container").ejSparkline({
    width : 2                   
});

{% endhighlight %}




### opacity `number`
{:#members:opacity}

Opacity of the series.

#### Default Value

* 1

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
    opacity : 2                  
});

{% endhighlight %}




### highPointColor `string`
{:#members:highpointcolor}

Color for series high point.

#### Default Value

* null

#### Example

{% highlight js %}
  
$("#container").ejSparkline({
    highPointColor : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### lowPointColor `string`
{:#members:lowpointcolor}

Color for series low point.

#### Default Value

* null

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    lowPointColor : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### startPointColor `string`
{:#members:startpointcolor}

Color for series start point.

#### Default Value

* null

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    startPointColor : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### endPointColor `string`
{:#members:endpointcolor}

Color for series end point.

#### Default Value

* null

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    endPointColor : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### negativePointColor `string`
{:#members:negativepointcolor}

Color for series negative point.

#### Default Value

* null

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    negativePointColor : "green"                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)


### rangeBandSettings `object`
{:#members:rangebandsettings}

Options for customizing the color, opacity of the sparkline start and end range.




### rangeBandSettings.startRange `number`
{:#members:rangebandsettings-startrange}

Start value of the range band.

#### Default Value

* null

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
     rangeBandSettings:{
        startRange : 2
    }                  
});

{% endhighlight %}




### rangeBandSettings.endRange `number`
{:#members:rangebandsettings-endrange}

End value of the range band.

#### Default Value

* null

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
    rangeBandSettings:{
        endRange : 2
    }                  
});

{% endhighlight %}




### rangeBandSettings.opacity `number`
{:#members:rangebandsettings-opacity}

Range band opacity of the series.

#### Default Value

* 1

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
     rangeBandSettings:{
        opacity : 2
    }                  
});

{% endhighlight %}




### rangeBandSettings.color `string`
{:#members:rangebandsettings-color}

Range band color of the series.

#### Default Value

* transparent

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
    rangeBandSettings:{
        color : 'purple'
    }                  
});

{% endhighlight %}




### palette `string`
{:#members:palette}

Name of a field in data source, where the fill color for all the data points is generated.

#### Default Value

* ""

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    palette : "ColorFieldName"                  
});
{% endhighlight %}


### isResponsive `boolean`
{:#members:isresponsive}

Controls whether sparkline has to be responsive or not.

#### Default Value

* true


#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   isResponsive : true             

});

{% endhighlight %}


### enableCanvasRendering `boolean`
{:#members:enablecanvasrendering}

Controls whether Sparkline has to be rendered as Canvas or SVG.Canvas rendering supports all functionalities in SVG rendering.

#### Default Value

* false

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

    enableCanvasRendering : true             

});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2nvdn2ml)




### dataSource `object`
{:#members:datasource}

Specifies the dataSource for the series. It can be an array of JSON objects or an instance of ej.DataManager.

#### Default Value

* null

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    
    dataSource: data
                       
});

{% endhighlight %}

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/soesgx0m)




### xName `string`
{:#members:xname}

Name of the property in the datasource that contains x value for the series.

#### Default Value

 * null

#### Example

{% highlight js %}

$("#container").ejSparkline({
    
    xName: "XValue"
                       
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5ffbprmm)




### yName `string`
{:#members:yname}

Name of the property in the datasource that contains y value for the series.

#### Default Value

 * null

#### Example

{% highlight js %}

$("#container").ejSparkline({
    
    yName: "YValue"
                       
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5ffbprmm)




### padding `number`
{:#members:padding}

Gap or padding for sparkline.

#### Default Value

* 8

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

    padding : 5                     

});

{% endhighlight %}




### type `enum`
{:#members:type}

<ts name = "ej.datavisualization.Sparkline.Type"/>

Specifies the type of the series to render in sparkline.

<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Area</td>
<td class="type">string</td> 
<td class="description">Specifies the series type as area.</td>
</tr>
<tr>
<td class="name">
Line</td>
<td class="type">string</td>
<td class="description">Specifies the series type as line.</td>
</tr> 
<tr>
<td class="name">
Column</td>
<td class="type">string</td> 
<td class="description">Specifies the series type as column.</td>
</tr>
<tr>
<td class="name">
Pie</td>
<td class="type">string</td> 
<td class="description">Specifies the series type as pie.</td>
</tr>
<tr>
<td class="name">
WinLoss</td>
<td class="type">string</td> 
<td class="description">Specifies the series type as WinLoss.</td>
</tr>
</tbody>
</table>

#### Default Value

* "line". See <a href="global.html#members:type">Type</a>

#### Example

{% highlight js %}
 
 
$("#container").ejSparkline({
    type : "area"                  
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/iyglee55)




### theme `enum`
{:#members:theme}

<ts name = "ej.datavisualization.Sparkline.Theme"/>

Specifies the theme for Sparkline.

<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Azure</td>
<td class="type">string</td> 
<td class="description">The Sparkline will be displayed in azure theme</td>
</tr>
<tr>
<td class="name">
FlatLight</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in light flat theme</td>
</tr> 
<tr>
<td class="name">
FlatDark</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in dark flat theme</td>
</tr> 
<tr>
<td class="name">
Azuredark</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in dark azure theme</td>
</tr> 
<tr>
<td class="name">
Lime</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in lime theme</td>
</tr> 
<tr>
<td class="name">
LimeDark</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in dark lime theme</td>
</tr> 
<tr>
<td class="name">
Saffron</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in saffron theme</td>
</tr> 
<tr>
<td class="name">
SaffronDark</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in dark saffron theme</td>
</tr> 
<tr>
<td class="name">
GradientLight</td>  
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in light gradient theme</td>
</tr> 
<tr>
<td class="name">
GradientDark</td>
<td class="type">string</td>
<td class="description">The Sparkline will be displayed in dark gradient theme</td>
</tr> 
</tbody>
</table>

#### Default Value

* "Flatlight". See <a href="global.html#members:theme">Theme</a>

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   theme : "flatdark"            

});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jael2rfm)




### tooltip `object`
{:#members:tooltip}

Options to customize the tooltip.




### tooltip.visible `boolean`
{:#members:tooltip-visible}

Show/hides the tooltip visibility.

#### Default Value

* false

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   tooltip :{visible :true}              

});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/31w3q03j)



### tooltip.fill `string`
{:#members:tooltip-fill}

Fill color for the sparkline tooltip.

#### Default Value

* "white"

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    tooltip:{
        fill : "green"
    }                  
});

{% endhighlight %}

Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)




### tooltip.template `string`
{:#members:tooltip-template}

Custom template to the tooltip.

#### Default Value

* ""

#### Example

{% highlight js %}

$("#container").ejSparkline({
    tooltip :{template : "item"}                  
});

{% endhighlight %}
 
Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/l5pmkkgr)
 

 
### tooltip.border `object`
{:#members:tooltip-border}

Options for customizing the border of the tooltip.

### tooltip.border.color `string`
{:#members:tooltip-border-color}

Border color of the tooltip. 

#### Default Value

* "transparent"

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    tooltip:{
        border:{color : "green"}
    }                  
});

{% endhighlight %}




### tooltip.border.width `number`
{:#members:tooltip-border-width}

Border width of the tooltip. 

#### Default Value

* 1

#### Example

{% highlight js %}

$("#container").ejSparkline({
    tooltip :{border :{width : 2}}                  
});

{% endhighlight %}


### tooltip.font `object`
{:#members:tooltip-font}

Options for customizing the font of the tooltip.

### tooltip.font.color `string`
{:#members:tooltip-font-color}




Font color of the text in the tooltip.


#### Default Value



* "#111111"




#### Example


{% highlight js %}
 
 
$("#container").ejSparkline({
tooltip :{font :{color : "green"}}                 
});
{% endhighlight %}

### tooltip.font.fontFamily `string`
{:#members:tooltip-font-fontfamily}




Font Family for the tooltip.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 

$("#container").ejSparkline({
tooltip :{ font : { fontFamily : "Algerian"}}                 
});
 {% endhighlight %}
 
 
### tooltip.font.fontStyle `enum`
{:#members:tooltip-font-fontstyle}


<ts name = "ej.datavisualization.Sparkline.FontStyle"/>


Specifies the font Style for the tooltip.


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td> 
<td class="description">Specifies the fontStyle as normal.</td>
</tr>
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="description">Specifies the fontStyle as italic.</td>
</tr> 
</tbody>
</table>


#### Default Value



* "Normal"



#### Example


{% highlight js %}
 

$("#container").ejSparkline({
tooltip : {font :{fontStyle : "italic"}}                 
});
{% endhighlight %}


### tooltip.font.fontWeight `enum`
{:#members:tooltip-font-fontweight}


<ts name = "ej.datavisualization.Sparkline.FontWeight"/>


Specifies the font weight for the tooltip.


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Regular</td>
<td class="type">string</td> 
<td class="description">Specifies the font weight as regular.</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="description">Specifies the font weight as bold.</td>
</tr> 
<tr>
<td class="name">
Lighter</td>
<td class="type">string</td>
<td class="description">Specifies the font weight as lighter.</td>
</tr> 
</tbody>
</table>


#### Default Value



* "Regular"




#### Example


{% highlight js %}
 

$("#container").ejSparkline({
tooltip :{font :{fontWeight : "lighter"}}                 
});
{% endhighlight %}




### tooltip.font.opacity `number`
{:#members:tooltip-font-opacity}




Opacity for text in the tooltip.


#### Default Value



* 1




#### Example


{% highlight js %}
 

$("#container").ejSparkline({
tooltip :{font :{opacity : 0.5}}                 
});
{% endhighlight %}




### tooltip.font.size `string`
{:#members:tooltip-font-size}




Font size for text in the tooltip.

#### Default Value



 * "8px"




#### Example


{% highlight js %}
 
 
$("#container").ejSparkline({
tooltip :{font :{size : "14px"}}                 
});
{% endhighlight %}

### markerSettings `object`
{:#members:markersettings}

Options for displaying and customizing marker for a data point.




### markerSettings.opacity `number`
{:#members:markersettings-opacity}

Controls the opacity of the marker.

#### Default Value

* 1

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
    markerSettings:{
        opacity : 2
    }                  
});

{% endhighlight %}




### markerSettings.visible `boolean`
{:#members:markersettings-visible}

Controls the visibility of the marker shape. 

#### Default Value

* false

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    markerSettings :{ visible : true}                  
});

{% endhighlight %}




### markerSettings.width `number`
{:#members:markersettings-width}

width of the marker shape. 

#### Default Value

* 2

#### Example

{% highlight js %}

$("#container").ejSparkline({
    markerSettings :{width : 2}                  
});

{% endhighlight %}




### markerSettings.fill `string`
{:#members:markersettings-fill}

Color of the marker shape. 

#### Default Value

* "white"

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    markerSettings : { fill : "green" }                  
});

{% endhighlight %}




### markerSettings.border `object`
{:#members:markersettings-border}

Options for customizing the border of the marker shape.

### markerSettings.border.color `string`
{:#members:markersettings-border-color}

Border color of the marker shape. 

#### Default Value

* "transparent"

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    markerSettings:{
        border:{color : "green"}
    }                  
});

{% endhighlight %}



### markerSettings.border.opacity `number`
{:#members:markersettings-border-opacity}

Controls the opacity of the marker border.

#### Default Value

* 1

#### Example

{% highlight js %} 
 
$("#container").ejSparkline({
    markerSettings:{
        border:{opacity : 2}
    }                  
});

{% endhighlight %}




### markerSettings.border.width `number`
{:#members:markersettings-border-width}

Border width of the marker shape. 

#### Default Value

* null

#### Example

{% highlight js %}

$("#container").ejSparkline({
    markerSettings :{border :{width : 2}}                  
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3vkjgyc0)




### size `object`
{:#members:size}

Options to customize the Sparkline size.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wpvk5t3p)




### size.height `string`
{:#members:size-height}

Height of the Sparkline. Height can be specified in either pixel or percentage.

#### Default Value

* ''

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   size :{height : '80%'}          

});

{% endhighlight %}




### size.width `string`
{:#members:size-width}

Width of the Sparkline. Width can be specified in either pixel or percentage.

#### Default Value

* ''

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   size :{width : '80%'}          

});

{% endhighlight %}




### axisLineSettings `object`
{:#members:axislineSettings}

Options for customizing the color,dashArray and width of the axisLine.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wxxv2rq1)



### axisLineSettings.visible `boolean`
{:#members:axislineSettings-visible}

Controls the visibility of the axis. 

#### Default Value

* false

#### Example

{% highlight js %}
 
$("#container").ejSparkline({
    axisLineSettings : {visible:true}                  
});

{% endhighlight %}




### axisLineSettings.color `string`
{:#members:axislineSettings-color}

Color of the axis line.

#### Default Value

* '#111111'

#### Example

{% highlight js %}
                             
$("#container").ejSparkline({

   axisLineSettings: { color: "green" }                      

});

{% endhighlight %}




### axisLineSettings.width `number`
{:#members:axisLineSettings-width}

Width of the axis line.

#### Default Value

* 1

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   axisLineSettings: { width: 2 }                      

});

{% endhighlight %}




### axisLineSettings.dashArray `number`
{:#members:axisLineSettings-dashArray}

Dash array of the axis line.

#### Default Value

* 1

#### Example

{% highlight js %}
 
$("#container").ejSparkline({

   axisLineSettings: { dashArray: 2 }                      

});

{% endhighlight %}


## Methods


### redraw()
{:#methods:redraw}

Redraws the entire sparkline. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.

#### Example

{% highlight js %}
// Redraw Sparkline
var sparklineObj = $("#container").data("ejSparkline");
sparklineObj.redraw();
{% endhighlight %}


{% highlight js %}
 
$("#container").ejSparkline("redraw");      
{% endhighlight %}





## Events



### load
{:#events:load}

Fires before loading the sparkline.

#### Example

{% highlight js %}
 
//load event for sparkline

$("#container").ejSparkline({

    load: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>




### loaded
{:#events:loaded}

Fires after loaded the sparkline.

#### Example

{% highlight js %}
 
//loaded event for sparkline

$("#container").ejSparkline({

    loaded: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>




### tooltipInitialize
{:#events:tooltipinitialization}

Fires before rendering trackball tooltip. You can use this event to customize the text displayed in trackball tooltip.

#### Example

{% highlight js %}
 
//ToolTip event for sparkline

$("#container").ejSparkline({

    tooltipInitialize: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationX{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">X Location of the trackball tooltip in pixels</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationY{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Y Location of the trackball tooltip in pixels</td>
</tr>
<tr>
<td class="name">{% highlight js %}
pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point for which trackball tooltip is displayed</td>
</tr>
<tr>
<td class="name">{% highlight js %}
currentText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text to be displayed in trackball tooltip. Use this option to add custom text in trackball tooltip</td>
</tr>
</tbody>
</table>



### seriesRendering
{:#events:seriesrendering}




Fires before rendering a series. This event is fired for each series in Sparkline.

#### Example


{% highlight js %}
 
//seriesRendering event for sparkline

$("#container").ejSparkline({

    seriesRendering: function (args) {
              //Do something
    }
    
});

{% endhighlight %}


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
minX{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Minimum x value of the data point</td>
</tr>
<tr>
<td class="name">{% highlight js %}
minY{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Minimum y value of the data point</td>
</tr>
<tr>
<td class="name">{% highlight js %}
maxX{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Maximum x value of the data point</td>
</tr>
<tr>
<td class="name">{% highlight js %}
maxY{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Maximum y value of the data point</td>
</tr>
</tbody>
</table>




### pointRegionMouseMove
{:#events:pointregionmousemove}

Fires when mouse is moved over a point. 

#### Example

{% highlight js %}
 
//pointRegionMouseMove event for sparkline

$("#container").ejSparkline({

    pointRegionMouseMove: function (args) {
                  //Do something
    }
   
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point in series</td>
</tr>
<tr>
<td class="name">{% highlight js %}
seriesType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Type of the series</td>
</tr>
</tbody>
</table>




### pointRegionMouseClick
{:#events:pointregionmouseclick}

Fires on clicking a point in sparkline. You can use this event to handle clicks made on points.

#### Example

{% highlight js %}
 
//pointRegionClick event for sparkline

$("#container").ejSparkline({

    pointRegionMouseClick: function (args) {
             //Do something
    }
    
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
locationY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point in series</td>
</tr>
<tr>
<td class="name">{% highlight js %}
seriesType{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Type of the series</td>
</tr>
</tbody>
</table>




### sparklineMouseMove
{:#events:sparklinemousemove}

Fires on moving mouse over the sparkline.

#### Example

{% highlight js %}
 
//sparklineMouseMove event for sparkline

$("#container").ejSparkline({

    sparklineMouseMove: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>




### sparklineMouseLeave
{:#events:sparklinemouseleave}

Fires on moving mouse outside the sparkline.

#### Example

{% highlight js %}
 
//sparklineMouseLeave event for sparkline

$("#container").ejSparkline({

    sparklineMouseLeave: function (args) {
              //Do something
    }
   
});

{% endhighlight %}

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight js %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the sparkline model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>