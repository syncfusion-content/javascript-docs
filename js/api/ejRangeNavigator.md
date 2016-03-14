---
layout: post
title: ejRangeNavigator
documentation: API
platform: js
metaname: 
metacontent: 
---

The range navigator can be easily configured to the DOM element, such as div. You can create a range navigator with a highly customizable look and feel.










$(element).ejRangeNavigator(options, options)







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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for range navigator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for range navigator</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Create RangeNavigator
$('#container').ejRangeNavigator();       
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.globalize.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.chart.js


* module:ej.rangenavigator.js




## Members








### allowSnapping `boolean`
{:#members:allowsnapping}








Toggles the placement of slider exactly on the place it left or on the nearest interval.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   allowSnapping: true;
   });
</script> 

 {% endhighlight %}







### dataSource `object`
{:#members:datasource}








Specifies the data source for range navigator.





#### Example


{% highlight html %}
     $("#container").ejRangeNavigator({
   dataSource:"data1", 
    xName: "X", 
    yName: "Y"
   });{% endhighlight %}







### enableAutoResizing `boolean`
{:#members:enableautoresizing}








Sets a value whether to make the range navigator responsive on resize.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   enableAutoResizing: true;
   });
</script>  {% endhighlight %}







### enableDeferredUpdate `boolean`
{:#members:enabledeferredupdate}








Toggles the redrawing of chart on moving the sliders.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   enableDeferredUpdate:false,
   });
</script>  {% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Toggles the direction of rendering the range navigator control.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  enableRTL: true,
   });
</script>  {% endhighlight %}







### labelSettings `object`
{:#members:labelsettings}








Options for customizing the labels colors, font, style, size, horizontalAlignment and opacity.











### labelSettings.higherLevel `object`
{:#members:labelsettings-higherlevel}








Options for customizing the higher level labels in range navigator.











### labelSettings.higherLevel.border `object`
{:#members:labelsettings-higherlevel-border}








Options for customizing the border of grid lines in higher level.











### labelSettings.higherLevel.border.color `string`
{:#members:labelsettings-higherlevel-border-color}








Specifies the border color of grid lines.




#### Default Value






* "transparent"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  labelSettings:{higherLevel:{ border :{color:"#ff0000"}}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.border.width `string`
{:#members:labelsettings-higherlevel-border-width}








Specifies the border width of grid lines.




#### Default Value






* "0.5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ border :{width:1}}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.fill `string`
{:#members:labelsettings-higherlevel-fill}








Specifies the fill color of higher level labels.




#### Default Value






* "transparent"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ fill:"days"}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.gridLineStyle `object`
{:#members:labelsettings-higherlevel-gridlinestyle}








Options for customizing the grid line colors, width, dashArray, border.











### labelSettings.higherLevel.gridLineStyle.color `string`
{:#members:labelsettings-higherlevel-gridlinestyle-color}








Specifies the color of grid lines in higher level.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{color:"#ff0000"}}},
   });{% endhighlight %}







### labelSettings.higherLevel.gridLineStyle.dashArray `string`
{:#members:labelsettings-higherlevel-gridlinestyle-dasharray}








Specifies the dashArray of grid lines in higher level.




#### Default Value






* "20 5 0"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{dashArray:"20 10 5"}}},
   });
</script> {% endhighlight %}







### labelSettings.higherLevel.gridLineStyle.width `string`
{:#members:labelsettings-higherlevel-gridlinestyle-width}








Specifies the width of grid lines in higher level.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ gridLineStyle :{width:1}}},
   });
</script> {% endhighlight %}







### labelSettings.higherLevel.intervalType `enum`
{:#members:labelsettings-higherlevel-intervaltype}

<ts name="ej.RangeNavigator.IntervalType"/>






Specifies the intervalType for higher level labels. See <a href="global.html#IntervalType">IntervalType</a>


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
Years</td>
<td class="type">string</td> 
<td class="description last">The labels are displayed with year as intervals between them </td>
</tr>
<tr>
<td class="name">
Quarters</td>
<td class="type">string</td>
<td class="description last">The labels are displayed with quarter as intervals  between them</td>
</tr> 
<tr>
<td class="name">
Months</td>
<td class="type">string</td>
<td class="description last">The labels are displayed with months as intervals between them</td>
</tr> 
<tr>
<td class="name">
Weeks</td>
<td class="type">string</td>
<td class="description last">The labels are displayed with weeks as intervals between them</td>
</tr> 
<tr>
<td class="name">
Days</td>
<td class="type">string</td>
<td class="description last">The labels are displayed with days as intervals between them</td>
</tr> 
<tr>
<td class="name">
Hours</td>

<td class="type">string</td>
<td class="description last">The labels are displayed with hours as intervals between them</td>
</tr> 
</tbody>
</table>

#### Default Value






* "years"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ intervalType:"days"}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.labelPlacement `enum`
{:#members:labelsettings-higherlevel-labelplacement}

<ts name="ej.RangeNavigator.LabelPlacement"/>

Specifies the position of the labels to render either inside or outside of plot area


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
Inside</td>
<td class="type">string</td> 
<td class="description last">The Labels are displayed inside the Range Navigator </td>
</tr>
<tr>
<td class="name">
Outside</td>
<td class="type">string</td>
<td class="description last">The Labels are displayed outside the Range Navigator</td>
</tr> 
</tbody>
</table>



Specifies the position of the labels to render either inside or outside of plot area. See <a href="global.html#LabelPlacement">LabelPlacement</a>




#### Default Value






* "outside"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ labelPlacement:"inside"}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.position `enum`
{:#members:labelsettings-higherlevel-position}


<ts name="ej.RangeNavigator.Position"/>

Specifies the position of the labels in higher level


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
Top</td>
<td class="type">string</td>
<td class="description last">Labels are placed on top of the slider</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="type">string</td>
<td class="description last">Labels are placed at teh bottom of the slider</td>
</tr> 
</tbody>
</table>



Specifies the position of the labels in higher level.See <a href="global.html#Position">Position</a>




#### Default Value






* "top"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ position:"bottom"}},
   });
</script>{% endhighlight %}







### labelSettings.higherLevel.style `object`
{:#members:labelsettings-higherlevel-style}








Options for customizing the style of higher level labels.











### labelSettings.higherLevel.style.font `object`
{:#members:labelsettings-higherlevel-style-font}








Options for customizing the font properties.











### labelSettings.higherLevel.style.font.color `string`
{:#members:labelsettings-higherlevel-style-font-color}








Specifies the label font color. Labels render with the specified font color.




#### Default Value






* "black"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{color: "red"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.font.fontFamily `string`
{:#members:labelsettings-higherlevel-style-font-fontfamily}








Specifies the label font family. Labels render with the specified font family.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontFamily: "Algerian"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.font.fontStyle `string`
{:#members:labelsettings-higherlevel-style-font-fontstyle}








Specifies the label font style. Labels render with the specified font style.




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontStyle: "Italic"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.font.fontWeight `string`
{:#members:labelsettings-higherlevel-style-font-fontweight}








Specifies the label font weight. Labels render with the specified font weight.




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{fontWeight: "regular"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.font.opacity `number`
{:#members:labelsettings-higherlevel-style-font-opacity}








Specifies the label opacity. Labels render with the specified opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{opacity: "14px"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.font.size `string`
{:#members:labelsettings-higherlevel-style-font-size}








Specifies the label font size. Labels render with the specified font size.




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{font:{size: "14px"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.style.horizontalAlignment `string`
{:#members:labelsettings-higherlevel-style-horizontalalignment}








Specifies the horizontal text alignment of the text in label.




#### Default Value






* "middle"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ style:{horizontalAlignment: "left"}}},
   });
</script>  {% endhighlight %}







### labelSettings.higherLevel.visible `boolean`
{:#members:labelsettings-higherlevel-visible}








Toggles the visibility of higher level labels.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{higherLevel:{ visible:false}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel `object`
{:#members:labelsettings-lowerlevel}








Options for customizing the labels in lower level.











### labelSettings.lowerLevel.border `object`
{:#members:labelsettings-lowerlevel-border}








Options for customizing the border of grid lines in lower level.











### labelSettings.lowerLevel.border.color `string`
{:#members:labelsettings-lowerlevel-border-color}








Specifies the border color of grid lines.




#### Default Value






* "transparent"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ border :{color:"#ff0000"}}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel.border.width `string`
{:#members:labelsettings-lowerlevel-border-width}








Specifies the border width of grid lines.




#### Default Value






* "0.5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ border :{width:1}}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel.fill `string`
{:#members:labelsettings-lowerlevel-fill}








Specifies the fill color of labels in lower level.




#### Default Value






* "transparent"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  labelSettings:{lowerLevel:{ fill:"days"}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel.gridLineStyle `object`
{:#members:labelsettings-lowerlevel-gridlinestyle}








Options for customizing the grid lines in lower level.











### labelSettings.lowerLevel.gridLineStyle.color `string`
{:#members:labelsettings-lowerlevel-gridlinestyle-color}








Specifies the color of grid lines in lower level.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ gridLineStyle :{color:"#ff0000"}}},
   });
</script> {% endhighlight %}







### labelSettings.lowerLevel.gridLineStyle.dashArray `string`
{:#members:labelsettings-lowerlevel-gridlinestyle-dasharray}








Specifies the dashArray of gridLines in lowerLevel.




#### Default Value






* "20 5 0"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   lowerLevel:{ gridLineStyle :{dashArray:"20 10 5"}}},
   });
</script> {% endhighlight %}







### labelSettings.lowerLevel.gridLineStyle.width `string`
{:#members:labelsettings-lowerlevel-gridlinestyle-width}








Specifies the width of grid lines in lower level.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ gridLineStyle :{width:1}}},
   });
</script> {% endhighlight %}







### labelSettings.lowerLevel.intervalType `enum`
{:#members:labelsettings-lowerlevel-intervaltype}

<ts ref="ej.RangeNavigator.IntervalType"/>



Specifies the intervalType of the labels in lower level.See <a href="global.html#IntervalType">IntervalType</a>




#### Default Value






* "years"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ intervalType:"days"}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.labelPlacement `enum`
{:#members:labelsettings-lowerlevel-labelplacement}

<ts ref="ej.RangeNavigator.LabelPlacement"/>






Specifies the position of the labels to render either inside or outside of plot area. See <a href="global.html#LabelPlacement">LabelPlacement</a>




#### Default Value






* "outside"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ labelPlacement:"inside"}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel.position `enum`
{:#members:labelsettings-lowerlevel-position}


<ts ref="ej.RangeNavigator.Position"/>





Specifies the position of the labels in lower level.See <a href="global.html#Position">Position</a>




#### Default Value






* "bottom"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ position:"bottom"}},
   });
</script>{% endhighlight %}







### labelSettings.lowerLevel.style `object`
{:#members:labelsettings-lowerlevel-style}








Options for customizing the style of labels.











### labelSettings.lowerLevel.style.font `object`
{:#members:labelsettings-lowerlevel-style-font}








Options for customizing the font of labels.











### labelSettings.lowerLevel.style.font.color `string`
{:#members:labelsettings-lowerlevel-style-font-color}








Specifies the color of labels. Label text render in this specified color.




#### Default Value






* "black"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{color: "red"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.font.fontFamily `string`
{:#members:labelsettings-lowerlevel-style-font-fontfamily}








Specifies the font family of labels. Label text render in this specified font family.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontFamily: "Algerian"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.font.fontStyle `string`
{:#members:labelsettings-lowerlevel-style-font-fontstyle}








Specifies the font style of labels. Label text render in this specified font style.




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontStyle: "Italic"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.font.fontWeight `string`
{:#members:labelsettings-lowerlevel-style-font-fontweight}








Specifies the font weight of labels. Label text render in this specified font weight.




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{fontWeight: "regular"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.font.opacity `string`
{:#members:labelsettings-lowerlevel-style-font-opacity}








Specifies the opacity of labels. Label text render in this specified opacity.




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{opacity: "14px"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.font.size `string`
{:#members:labelsettings-lowerlevel-style-font-size}








Specifies the size of labels. Label text render in this specified size.




#### Default Value






* "12px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{font:{size: "14px"}}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.style.horizontalAlignment `string`
{:#members:labelsettings-lowerlevel-style-horizontalalignment}








Specifies the horizontal text alignment of the text in label.




#### Default Value






* "middle"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ style:{horizontalAlignment: "left"}}},
   });
</script>  {% endhighlight %}







### labelSettings.lowerLevel.visible `boolean`
{:#members:labelsettings-lowerlevel-visible}








Toggles the visibility of labels in lower level.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{lowerLevel:{ visible:false}},
   });
</script>{% endhighlight %}







### labelSettings.style `object`
{:#members:labelsettings-style}








Options for customizing the style of labels in range navigator.











### labelSettings.style.font `object`
{:#members:labelsettings-style-font}








Options for customizing the font of labels in range navigator.











### labelSettings.style.font.color `string`
{:#members:labelsettings-style-font-color}








Specifies the label color. This color is applied to the labels in range navigator.




#### Default Value






* "#FFFFFF"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{color:"#ff0000"}}},
   });
</script>{% endhighlight %}







### labelSettings.style.font.family `string`
{:#members:labelsettings-style-font-family}








Specifies the label font family. Labels render with the specified font family.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{family:"Arial"}}},
   });
</script>{% endhighlight %}







### labelSettings.style.font.opacity ` number`
{:#members:labelsettings-style-font-opacity}








Specifies the label font opacity. Labels render with the specified font opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{opacity:0.5}}}
   });
</script>{% endhighlight %}







### labelSettings.style.font.size `string`
{:#members:labelsettings-style-font-size}








Specifies the label font size. Labels render with the specified font size.




#### Default Value






* "1px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{size:"12px"}}},
   });
</script>{% endhighlight %}







### labelSettings.style.font.style `enum`
{:#members:labelsettings-style-font-style}

<ts name="ej.RangeNavigator.Style"/>

Specifies the label font style. Labels render with the specified font style..


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
<td class="description last">The labels are displayed in the default format</td>
</tr>
<tr>
<td class="name">
Bold</td>
<td class="type">string</td>
<td class="description last">The labels are displayed in Bold format</td>
</tr> 
<tr>
<td class="name">
Italic</td>
<td class="type">string</td>
<td class="description last">The labels are displayed in the itialized format</td>
</tr> 
</tbody>
</table>






Specifies the label font style. Labels render with the specified font style..See <a href="global.html#FontStyle">FontStyle</a>




#### Default Value






* "Normal"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{style:"Noraml"}}},
   });
</script>{% endhighlight %}







### labelSettings.style.font.weight `enum`
{:#members:labelsettings-style-font-weight}

<ts name="ej.RangeNavigator.Weight"/>

Specifies the lable font weight



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
<td class="description last">The Labels are displayed in the default manner</td>
</tr>
<tr>
<td class="name">Lighter</td>
<td class="type">string</td>
<td class="description last">The Labels are displayed lighter than the normal text</td>
</tr> 
</tbody>
</table>






Specifies the label font weight. Labels render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>




#### Default Value






* "regular"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   labelSettings:{style:{ font:{weight:"Regular"}}},
   });
</script>{% endhighlight %}







### labelSettings.style.horizontalAlignment `enum`
{:#members:labelsettings-style-horizontalalignment}

<ts name="ej.RangeNavigator.HorizontalAlignment"/>

Specifies the horizontalAlignment of the label in RangeNavigator


<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th> 
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Middle</td>
<td class="type">string</td> 
<td class="description last">The labels are aligned to the center </td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="description last">The labels are aligned to the left</td>
</tr> 
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="description last">The labels are aligned to the right</td>
</tr> 
</tbody>
</table>







Specifies the horizontalAlignment of the label in range navigator. See <a href="global.html#HorizontalAlignment">HorizontalAlignment</a>




#### Default Value






* "middle"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  labelSettings:{style:{ horizontalAlignment:"middle"}},
   });
</script>{% endhighlight %}







### locale `string`
{:#members:locale}








This property is to specify the localization of range navigator.




#### Default Value






* "en-US"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   locale: "en-US",
   });
</script>  {% endhighlight %}







### navigatorStyleSettings `object`
{:#members:navigatorstylesettings}








Options for customizing the range navigator.











### navigatorStyleSettings.background `string`
{:#members:navigatorstylesettings-background}








Specifies the background color of range navigator.




#### Default Value






* "#dddddd"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ background:"#ff0000"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.border `object`
{:#members:navigatorstylesettings-border}








Options for customizing the border color and width of range navigator.











### navigatorStyleSettings.border.color `string`
{:#members:navigatorstylesettings-border-color}








Specifies the border color of range navigator.




#### Default Value






* "transparent"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{color:"#ff0000"}},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.border.dashArray `string`
{:#members:navigatorstylesettings-border-dasharray}








Specifies the dash array of range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{dashArray:"2,3"}},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.border.width ` number`
{:#members:navigatorstylesettings-border-width}








Specifies the border width of range navigator.




#### Default Value






* 0.5








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ border:{width:1}},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.leftThumbTemplate `string`
{:#members:navigatorstylesettings-leftthumbtemplate}








Specifies the left side thumb template in range navigator we can give either div id or html string




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ leftThumbTemplate:"item"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.majorGridLineStyle `object`
{:#members:navigatorstylesettings-majorgridlinestyle}








Options for customizing the major grid lines.











### navigatorStyleSettings.majorGridLineStyle.color `string`
{:#members:navigatorstylesettings-majorgridlinestyle-color}








Specifies the color of major grid lines in range navigator.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{color:"#ff0000"}},
   });
</script> {% endhighlight %}







### navigatorStyleSettings.majorGridLineStyle.visible `boolean`
{:#members:navigatorstylesettings-majorgridlinestyle-visible}








Toggles the visibility of major grid lines.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{visible:false}},
   });
</script> {% endhighlight %}







### navigatorStyleSettings.minorGridLineStyle `object`
{:#members:navigatorstylesettings-minorgridlinestyle}








Options for customizing the minor grid lines.











### navigatorStyleSettings.minorGridLineStyle.color `string`
{:#members:navigatorstylesettings-minorgridlinestyle-color}








Specifies the color of minor grid lines in range navigator.




#### Default Value






* "#B5B5B5"








#### Example


{% highlight html %}
 
//Gets or sets color of majorGridLines in range navigator, after initialization:
        //Gets the color of majorGridLines in range navigator
        $("#container").ejRangeNavigator("option", "navigatorStyleSettings.majorGridLineStyle.color");
                      
        //Sets the color of majorGridLines in range navigator{% endhighlight %}







### navigatorStyleSettings.minorGridLineStyle.visible `boolean`
{:#members:navigatorstylesettings-minorgridlinestyle-visible}








Toggles the visibility of minor grid lines.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ majorGridLineStyle:{visible:false}},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.opacity ` number`
{:#members:navigatorstylesettings-opacity}








Specifies the opacity of RangeNavigator.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ opacity:0.5},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.rightThumbTemplate `string`
{:#members:navigatorstylesettings-rightthumbtemplate}








Specifies the right side thumb template in range navigator we can give either div id or html string




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ rightThumbTemplate:"item"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.selectedRegionColor `string`
{:#members:navigatorstylesettings-selectedregioncolor}








Specifies the color of the selected region in range navigator.




#### Default Value






* "#EFEFEF"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ selectedRegionColor:"#ff0000"}},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.selectedRegionOpacity `number`
{:#members:navigatorstylesettings-selectedregionopacity}








Specifies the opacity of Selected Region.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ selectedRegionOpacity:0.5},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.thumbColor `string`
{:#members:navigatorstylesettings-thumbcolor}








Specifies the color of the thumb in range navigator.




#### Default Value






* "#2382C3"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbColor:"#ff0000"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.thumbRadius `number`
{:#members:navigatorstylesettings-thumbradius}








Specifies the radius of the thumb in range navigator.




#### Default Value






* 10








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbRadius:15},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.thumbStroke `string`
{:#members:navigatorstylesettings-thumbstroke}








Specifies the stroke color of the thumb in range navigator.




#### Default Value






* "#303030"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ thumbStroke:"#ff0000"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.unselectedRegionColor `string`
{:#members:navigatorstylesettings-unselectedregioncolor}








Specifies the color of the unselected region in range navigator.




#### Default Value






* "#5EABDE"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ unselectedRegionColor:"#ff0000"},
   });
</script>  {% endhighlight %}







### navigatorStyleSettings.unselectedRegionOpacity `number`
{:#members:navigatorstylesettings-unselectedregionopacity}








Specifies the opacity of Unselected Region.




#### Default Value






* 0.3








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   navigatorStyleSettings:{ unselectedRegionOpacity:0.5},
   });
</script>  {% endhighlight %}







### padding `string`
{:#members:padding}








Padding specifies the gap between the container and the range navigator.




#### Default Value






* "0"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   padding: "15";
   });
</script>  {% endhighlight %}







### rangePadding `enum`
{:#members:rangepadding}

<ts name="ej.RangeNavigator.RangePadding"/>

If the range is not given explicitly, range will be calculated automatically.


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
Additional</td>
<td class="type">string</td> 
<td class="description last">The range is added with an extra interval when the RangePadding is set as Additional</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="type">string</td>
<td class="description last">The automatic range calculation differs based on the data when the RangePadding is set as Normal </td>
</tr> 
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="description last">The Range is calculated based on the minimum and maximum value in the data when the  RangePadding is set as None</td>
</tr> 
<tr>
<td class="name">
Round</td>
<td class="type">string</td>
<td class="description last">The Range is rounded to the nearest possible values when the RangePadding is set as  Round</td>
</tr> 
</tbody>
</table>




If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>




#### Default Value






* "none"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  rangePadding: "normal",
   });
</script>  {% endhighlight %}







### rangeSettings `object`
{:#members:rangesettings}








Options for customizing the starting and ending ranges.











### rangeSettings.end `string`
{:#members:rangesettings-end}








Specifies the ending range of range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   rangeSettings:{end:"01/05/1993"}
   });
</script>  {% endhighlight %}







### rangeSettings.start `string`
{:#members:rangesettings-start}








Specifies the starting range of range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   rangeSettings:{start:"01/05/1993"},
   });{% endhighlight %}







### selectedData `object`
{:#members:selecteddata}








selectedData is for getting the data when the "rangeChanged" event trigger from client side.











### selectedRangeSettings `object`
{:#members:selectedrangesettings}








Options for customizing the start and end range values.











### selectedRangeSettings.end `string`
{:#members:selectedrangesettings-end}








Specifies the ending range of range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   selectedRangeSettings:{end:"01/05/1993"},
   });
</script>  {% endhighlight %}







### selectedRangeSettings.start `string`
{:#members:selectedrangesettings-start}








Specifies the starting range of range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  selectedRangeSettings:{start:"01/05/1992"},
   });
</script>  {% endhighlight %}







### sizeSettings `object`
{:#members:sizesettings}








Contains property to customize the hight and width of range navigator.











### sizeSettings.height `string`
{:#members:sizesettings-height}








Specifies height of the range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
                             
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   sizeSettings: { height : "130" },
   });
</script>  {% endhighlight %}







### sizeSettings.width `string`
{:#members:sizesettings-width}








Specifies width of the range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   sizeSettings: { width : "900" },
   });
</script>  {% endhighlight %}







### theme `string`
{:#members:theme}








By specifying this property the user can change the theme of the range navigator.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   theme: "flatdark";
   });
</script>  {% endhighlight %}







### tooltipSettings `object`
{:#members:tooltipsettings}








Options for customizing the tooltip in range navigator.





#### Example


{% highlight html %}
     $("#container").ejRangeNavigator({
   tooltipSettings: { visible: true, labelFormat: "MMM/dd/yyyy", tooltipDisplayMode: "always", tooltipDisplayMode: "always" },
   });{% endhighlight %}







### tooltipSettings.backgroundColor `string`
{:#members:tooltipsettings-backgroundcolor}








Specifies the background color of tooltip.




#### Default Value






* "#303030"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{backgroundColor: "#303030"},
   });
</script>  {% endhighlight %}







### tooltipSettings.font `object`
{:#members:tooltipsettings-font}








Options for customizing the font in tooltip.











### tooltipSettings.font.color `string`
{:#members:tooltipsettings-font-color}








Specifies the color of text in tooltip. Tooltip text render in the specified color.




#### Default Value






* "#FFFFFF"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{color : "FFFFFF"}},
   });
</script>{% endhighlight %}







### tooltipSettings.font.family `string`
{:#members:tooltipsettings-font-family}








Specifies the font family of text in tooltip. Tooltip text render in the specified font family.




#### Default Value






* "Segoe UI"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
                tooltipSettings:{font:{family:"Arial"}}
                }); 
</script>{% endhighlight %}







### tooltipSettings.font.fontStyle `string`
{:#members:tooltipsettings-font-fontstyle}








Specifies the font style of text in tooltip. Tooltip text render in the specified font style.




#### Default Value






* ej.datavisualization.RangeNavigator.fontStyle.Normal








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{fontStyle:"Normal"}}
   });
</script>{% endhighlight %}







### tooltipSettings.font.opacity ` number`
{:#members:tooltipsettings-font-opacity}








Specifies the opacity of text in tooltip. Tooltip text render in the specified opacity.




#### Default Value






* 1








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
  tooltipSettings:{ font:{opacity:0.5}}
   });
</script>{% endhighlight %}







### tooltipSettings.font.size `string`
{:#members:tooltipsettings-font-size}








Specifies the size of text in tooltip. Tooltip text render in the specified size.




#### Default Value






* "10px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{font:{size:"12px"}},
   });
</script>{% endhighlight %}







### tooltipSettings.font.weight `string`
{:#members:tooltipsettings-font-weight}








Specifies the weight of text in tooltip. Tooltip text render in the specified weight.




#### Default Value






* ej.datavisualization.RangeNavigator.weight.Regular








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{ font:{weight:"regular"}},
   });
</script>{% endhighlight %}







### tooltipSettings.labelFormat `string`
{:#members:tooltipsettings-labelformat}








Specifies the format of text to be displayed in tooltip.




#### Default Value






* "MM/dd/yyyy"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings: { labelFormat: "MM/dd/yyyy"}
   });
</script>  {% endhighlight %}







### tooltipSettings.tooltipDisplayMode `string`
{:#members:tooltipsettings-tooltipdisplaymode}








Specifies the mode of displaying the tooltip. Neither to display the tooltip always nor on demand.




#### Default Value






* null








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{tooltipDisplayMode: "always"},
   });
</script>  {% endhighlight %}







### tooltipSettings.visible `boolean`
{:#members:tooltipsettings-visible}








Toggles the visibility of tooltip.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   tooltipSettings:{visible: true}
   });
</script>  {% endhighlight %}







### valueAxisSettings `object`
{:#members:valueaxissettings}








Options for configuring minor grid lines, major grid lines, axis line of axis.











### valueAxisSettings.axisLine `object`
{:#members:valueaxissettings-axisline}








Options for customizing the axis line.











### valueAxisSettings.axisLine.visible `string`
{:#members:valueaxissettings-axisline-visible}








Toggles the visibility of axis line.




#### Default Value






* "none"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{axisLine: {visible: true}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.font `object`
{:#members:valueaxissettings-font}








Options for customizing the font of the axis.











### valueAxisSettings.font.size `string`
{:#members:valueaxissettings-font-size}








Text in axis render with the specified size.




#### Default Value






* "0px"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{font: {size: '12px'}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.majorGridLines `object`
{:#members:valueaxissettings-majorgridlines}








Options for customizing the major grid lines.











### valueAxisSettings.majorGridLines.visible `boolean`
{:#members:valueaxissettings-majorgridlines-visible}








Toggles the visibility of major grid lines.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorGridLines: {visible: true}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.majorTickLines `object`
{:#members:valueaxissettings-majorticklines}








Options for customizing the major tick lines in axis.











### valueAxisSettings.majorTickLines.size `number`
{:#members:valueaxissettings-majorticklines-size}








Specifies the size of the majorTickLines in range navigator




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {size: 3}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.majorTickLines.visible `boolean`
{:#members:valueaxissettings-majorticklines-visible}








Toggles the visibility of major tick lines.




#### Default Value






* true








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {visible: false}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.majorTickLines.width `number`
{:#members:valueaxissettings-majorticklines-width}








Specifies width of the major tick lines.




#### Default Value






* 0








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{majorTickLines: {width: 3}}
   });
</script>  {% endhighlight %}







### valueAxisSettings.rangePadding `string`
{:#members:valueaxissettings-rangepadding}








If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding.




#### Default Value






* "none"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{rangePadding: "normal"},
   });
</script>  {% endhighlight %}







### valueAxisSettings.visible `boolean`
{:#members:valueaxissettings-visible}








Toggles the visibility of axis in range navigator.




#### Default Value






* false








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueAxisSettings:{visble: true}
   });
</script>  {% endhighlight %}







### valueType `enum`
{:#members:valuetype}

<ts name='ej.RangeNavigator.ValueType'/>
You can plot data of type date time or numeric. This property determines the type of data that this axis will handle.


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
Numeric</td>
<td class="type">string</td> 
<td class="description last">The numeric data is used in the RangeNavigator then the ValueType is set as Numeric</td>
</tr>
<tr>
<td class="name">
DateTime</td>
<td class="type">string</td>
<td class="description last">The default value type of Range Navigator is DateTime and it reprsents the DateTime Values</td>
</tr> 

</tbody>
</table>


#### Default Value






* "datetime"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   valueType: "numeric",
   });
</script>  {% endhighlight %}







### xName `object`
{:#members:xname}








Specifies the xName for dataSource. This is used to take the x values from dataSource





#### Example


{% highlight html %}
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   dataSource:"data1", 
   xName: "X"
   });
</script> {% endhighlight %}







### yName `object`
{:#members:yname}








Specifies the yName for dataSource. This is used to take the y values from dataSource





#### Example


{% highlight html %}
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   dataSource:"data1", 
   yName: "Y"
   });
</script> {% endhighlight %}







### zoomSettings.zoomFactor `string`
{:#members:zoomsettings-zoomfactor}








This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1.




#### Default Value






* "1"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
                         zoomFactor:"1"
   });
</script>  {% endhighlight %}







### zoomSettings.zoomPosition `string`
{:#members:zoomsettings-zoomposition}








This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.




#### Default Value






* "0"








#### Example


{% highlight html %}
 
<div id="RangeNavigator"></div> 
<script>
        $("#container").ejRangeNavigator({
   zoomPosition:"0",
   });
</script>  {% endhighlight %}





## Methods








### _destroy ()
{:#methods:_destroy}








destroy the range navigator widget





#### Example


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Destroy range navigator
var obj = $("#container").data("ejRangeNavigator");
obj.destroy(); // destroy the range navigator
</script>{% endhighlight %}


{% highlight html %}
 
<div id="container"></div> 
 
<script>
$("#container").ejRangeNavigator("destroy");    
</script>{% endhighlight %}





## Events








### load
{:#events:load}








Fires on load of range navigator.

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
<td class="name">{% highlight html %}
Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from range navigator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the range navigator model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//load event for chart
$("#container").ejRangeNavigator({
   load: function (args) {}
});{% endhighlight %}







### loaded
{:#events:loaded}








Fires after range navigator is loaded.

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
<td class="name">{% highlight html %}
Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from range navigator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the range navigator model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//loaded event for chart
$("#container").ejRangeNavigator({
   loaded: function (args) {}
});{% endhighlight %}







### rangeChanged
{:#events:rangechanged}








Fires on changing the range of range navigator.

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
<td class="name">{% highlight html %}
Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from range navigator</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the range navigator model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example


{% highlight html %}
 
//rangeChanged event for chart
$("#container").ejRangeNavigator({
   rangeChanged: function (args) {}
});{% endhighlight %}




