---
layout: post
title: ejChart
documentation: API
platform: js
metaname: 
metacontent: 
---

The chart can be easily configured to the DOM element, such as div. you can create a grid with a highly customizable look and feel.





$(element).ejChart<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Create Chart
$('#container').ejChart();      
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery.js

* module:ej.core.js

* module:ej.data.js

* module:ej.chart.js

* module:jQuery.globalize.js


## Members




### annotations<span class="type-signature type array">array</span>
{:#members:annotations}




Contains properties for customizing the annotations in chart.






### annotations.angle<span class="type-signature type number">number</span>
{:#members:annotations-angle}




Annotataion takes the specified value as angle for rotating it


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ angle : 45}]                    
});
</script>  {% endhighlight %}




### annotations.content<span class="type-signature type string">string</span>
{:#members:annotations-content}




Specifies the content /element which is to be displayed as annotation


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ content :"Template"}]                    
});
</script>  {% endhighlight %}




### annotations.coordinateUnit<span class="type-signature type enum">enum</span>
{:#members:annotations-coordinateunit}




Specifies the option based on which annotation is placed on the chart


Default Value:
{:.param}



* "none"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ coordinateUnit :"pixels"}]                    
});
</script>  {% endhighlight %}




### annotations.horizontalAlignment<span class="type-signature type enum">enum</span>
{:#members:annotations-horizontalalignment}




To position the annotation horizontally


Default Value:
{:.param}



* "middle"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ horizontalAlignment :"left"}]                    
});
</script>  {% endhighlight %}




### annotations.margin<span class="type-signature type object">object</span>
{:#members:annotations-margin}




Contains property to customize the margin values of annotation






### annotations.margin.bottom<span class="type-signature type number">number</span>
{:#members:annotations-margin-bottom}




Specifies the bottom margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ margin :{ bottom:10}}]                    
});
</script>  {% endhighlight %}




### annotations.margin.left<span class="type-signature type number">number</span>
{:#members:annotations-margin-left}




Specifies the left margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ margin :{ left:10}}]                    
});
</script>  {% endhighlight %}




### annotations.margin.right<span class="type-signature type number">number</span>
{:#members:annotations-margin-right}




Specifies the right margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ margin :{ right:10}}]                    
});
</script>  {% endhighlight %}




### annotations.margin.top<span class="type-signature type number">number</span>
{:#members:annotations-margin-top}




Specifies the top margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ margin :{ top:10}}]                    
});
</script>  {% endhighlight %}




### annotations.opacity<span class="type-signature type number">number</span>
{:#members:annotations-opacity}




Annotataion takes the specified value as opacity


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ opacity : 0.5}]                    
});
</script>  {% endhighlight %}




### annotations.region<span class="type-signature type enum">enum</span>
{:#members:annotations-region}




To place the annotation with respect to chart / series


Default Value:
{:.param}



* "chart"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ region :"series"}]                    
});
</script>  {% endhighlight %}




### annotations.verticalAlignment<span class="type-signature type enum">enum</span>
{:#members:annotations-verticalalignment}




To position the annotation vertically


Default Value:
{:.param}



* "middle"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ verticalAlignment :"top"}]                    
});
</script>  {% endhighlight %}




### annotations.visible<span class="type-signature type boolean">boolean</span>
{:#members:annotations-visible}




Specifies the visibility of annotation.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ visible :true}]                    
});
</script>  {% endhighlight %}




### annotations.x<span class="type-signature type number">number</span>
{:#members:annotations-x}




Annotataion takes the specified x value


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ x : 100}]                    
});
</script>  {% endhighlight %}




### annotations.xAxisName<span class="type-signature type string">string</span>
{:#members:annotations-xaxisname}




Binds annotation to the specified axis


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ xAxisName : "xAxis1"}]                    
});
</script>  {% endhighlight %}




### annotations.y<span class="type-signature type number">number</span>
{:#members:annotations-y}




Annotataion takes the specified y value


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ y : 100}]                    
});
</script>  {% endhighlight %}




### annotations.yAxisName<span class="type-signature type string">string</span>
{:#members:annotations-yaxisname}




Binds annotation to the specified axis


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
annotations :[{ yAxisName : "yAxis1"}]                    
});
</script>  {% endhighlight %}




### backGroundImageUrl<span class="type-signature type string">string</span>
{:#members:backgroundimageurl}




Specifies the background image path to display the image, plotting in the chart background.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
   backGroundImageUrl: "../images/chart/wheat.png"                      
});
</script> {% endhighlight %}




### border<span class="type-signature type object">object</span>
{:#members:border}




Options for customizing the color, opacity and width of the border of chart.






### border.color<span class="type-signature type string">string</span>
{:#members:border-color}




Specifies the border color of the chart.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
                             
<div id="container"></div> 
<script>
$("#container").ejChart({
   border: { color: "green" }                      
});
</script>                {% endhighlight %}




### border.opacity<span class="type-signature type number">number</span>
{:#members:border-opacity}




Specifies the border opacity of the chart


Default Value:
{:.param}



* 0.3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
   border: { opacity: 0.5 }                      
});
</script> {% endhighlight %}




### border.width<span class="type-signature type number">number</span>
{:#members:border-width}




Specifies the border width of the chart.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
   border: { width: 2 }                      
});
</script> {% endhighlight %}




### canResize<span class="type-signature type boolean">boolean</span>
{:#members:canresize}




Sets a value whether to make the chart responsive on resize.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
canResize : true             
});
</script>{% endhighlight %}




### chartArea<span class="type-signature type object">object</span>
{:#members:chartarea}




Specifies options for configuring the border and background for chart plotting area.






### chartArea.background<span class="type-signature type string">string</span>
{:#members:chartarea-background}




Specifies the background for chart plotting area.


Default Value:
{:.param}



* transparent




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
    chartArea: { background : "white" }                      
});
</script> {% endhighlight %}




### chartArea.border<span class="type-signature type object">object</span>
{:#members:chartarea-border}




Options for customizing the color, opacity and width of the border of chart plotting area.






### chartArea.border.color<span class="type-signature type string">string</span>
{:#members:chartarea-border-color}




Specifies the border color of chart plotting area.


Default Value:
{:.param}



* Gray




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
   chartArea: { border: { color :"green"} }                      
});
</script> {% endhighlight %}




### chartArea.border.opacity<span class="type-signature type number">number</span>
{:#members:chartarea-border-opacity}




Specifies the border opacity of chart plotting area.


Default Value:
{:.param}



* 0.3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
    chartArea: { border: { opacity : 0.5} }                      
});
</script> {% endhighlight %}




### chartArea.border.width<span class="type-signature type number">number</span>
{:#members:chartarea-border-width}




Specifies the border width of chart plotting area.


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
    chartArea: { border: { width : 0.2} }                      
});
</script> {% endhighlight %}




### columnDefinitions<span class="type-signature type array">array</span>
{:#members:columndefinitions}




You can split chart into multiple plotting areas vertically. In order to split the chart vertically, you need to specify number of column objects in columDefintions array. Each object in the columnDefnitions represent a plotting area in chart.



Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
 columnDefinitions :[{unit : "percentage"}]                       
});
</script> {% endhighlight %}




### commonSeriesOptions<span class="type-signature type object">object</span>
{:#members:commonseriesoptions}




Options for configuring the properties commonly for all the series. You can also override the options for specific series by setting the options directly in each series object in series array.






### commonSeriesOptions.border<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-border}




Options for customizing the color, opacity and width of the border of series.






### commonSeriesOptions.border.color<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-border-color}




Specifies the border color of series.


Default Value:
{:.param}



* "transparent"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{border :{ color : "green" } }                  
});
</script>{% endhighlight %}




### commonSeriesOptions.border.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-border-width}




Specifies the border width of series.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{border :{ width : 2 } }                  
});
</script>{% endhighlight %}




### commonSeriesOptions.dashArray<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-dasharray}




Controls the pattern of dashes and gaps used to stroke the line series.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{dashArray : "2,3"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.dataSource<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-datasource}




Specifies the dataSource for series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions : {dataSource: data.open }                   
});
</script> {% endhighlight %}




### commonSeriesOptions.doughnutCoefficient<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-doughnutcoefficient}




Sets the radius of the hole on the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.4




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ doughnutCoefficient : 0.5}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.doughnutSize<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-doughnutsize}




Sets the radius of the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ doughnutSize : 0.9}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.drawType<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-drawtype}




Specifies the type of series that can be drawn in a Radar or Polar series. It supports line, column and area type. See <a href="global.html#DrawType">DrawType</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.DrawType.Line




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ drawType : "area"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-enableanimation}




Specifies the series animation common to all series. By specifying this, we can enable/disable the animation of the series.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ enableAnimation : false}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.enableSmartLabels<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-enablesmartlabels}




Enabling this property can avoid pie series data label overlap each other.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ enableSmartLabels : false}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.endAngle<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-endangle}




Specifies the ending angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ endAngle : 270}                  
});
</script> ; {% endhighlight %}




### commonSeriesOptions.explode<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-explode}




Explodes the pie slices on mouse move. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ explode : true}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.explodeAll<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-explodeall}




Explodes all the pie slices. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ explodeAll : true}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.explodeIndex<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-explodeindex}




Index of a slice to be exploded from the whole pie. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ explodeIndex : 2}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.explodeOffset<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-explodeoffset}




Represents the distance the slice has to be moved out when it is exploded.


Default Value:
{:.param}



* 0.4




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ explodeOffset : 20}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.fill<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-fill}




Specifies the fill color of series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{fill : "green"}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.font<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-font}




Specifies the font that is common to all series. These are the properties involved in customizing the font of the series in chart.






### commonSeriesOptions.font.color<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-font-color}




Specifies the color, that is common to all series. Text in the series, render with the specified font color.


Default Value:
{:.param}



* "#707070"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{font :{color : "green"}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.font.fontFamily<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-font-fontfamily}




Specifies the fontFamily, that is common to all series. Text in the series, render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ font : { fontFamily : "Algerian"}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-font-fontstyle}




Specifies the fontStyle, that is common to all series. Text in the series, render with the specified font style.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions : {font :{fontStyle : "italic"}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-font-fontweight}




Specifies the fontWeight, that is common to all series. Text in the series, render with the specified font weight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{font :{fontWeight : "lighter"}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.font.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-font-opacity}




Specifies the opacity, that is common to all series. Text in the series, render with the specified font opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{font :{opacity : 0.5}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.font.size<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-font-size}




Specifies the font size, that is common to all series. Text in the series, render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{font :{size : "14px"}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.funnelHeight
{:#members:commonseriesoptions-funnelheight}




Sets the funnel height.


Default Value:
{:.param}



* "32.7%"(32.7% of actualheight)




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{funnelHeight : '40%' }]                   
});
</script> {% endhighlight %}




### commonSeriesOptions.funnelWidth
{:#members:commonseriesoptions-funnelwidth}




Sets the funnel width.


Default Value:
{:.param}



* "11.6%"(11.6% of actualwidth)




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{funnelWidth : '40%' }]                   
});
</script> {% endhighlight %}




### commonSeriesOptions.gapRatio<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-gapratio}




Specifies the gap between each slice of a pyramid series in pixels.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ gapRatio : 0.5}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.isClosed<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-isclosed}




Used in Polar and Radar series to specify whether the line/area series has to be rendered in a closed state by joining the start and end point of the series.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ isClosed : false}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.isStacking<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-isstacking}




Used in Polar and Radar series to specify whether column type has to be rendered the stacked value of chart.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ isStacking : "true"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.labelPosition<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-labelposition}




Specifies the position of the axis labels to render labels either inside or outside of plot area. See <a href="global.html#LabelPosition">LabelPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelPosition.Inside




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ labelPosition : "outside"}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.lineCap<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-linecap}




Specifies the style to draw the end point of a line like butt, round, square. See <a href="global.html#LineCap">LineCap</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineCap.Butt




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{lineCap : "butt"}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.lineJoin<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-linejoin}




Specifies the shape to use at the intersection of two lines drawn. See <a href="global.html#LineJoin">LineJoin</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineJoin.Round




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{lineCap : "round"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.marker<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker}




Contains the customizing properties to add marker symbols to the points plotted in the chart






### commonSeriesOptions.marker.border<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-border}




Options for customizing the color, opacity and width of the border of marker.






### commonSeriesOptions.marker.border.color<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-border-color}




Specifies the border color of marker.


Default Value:
{:.param}



* "white"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{color : "green"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.border.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-border-width}




Specifies the border width of marker.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{border :{width : 2}}}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-datalabel}




Contains the customizing properties to add data labels of the points plotted in the chart.






### commonSeriesOptions.marker.dataLabel.angle<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-angle}




rotates dataLabel in the marker.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{angle : 90}}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.border<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-datalabel-border}




Options for customizing the color, opacity and width of the border of datalabel.






### commonSeriesOptions.marker.dataLabel.border.color<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-datalabel-border-color}




Specifies the border color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border : {color : "green"}}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.border.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-border-width}




Specifies the border width of datalabel.


Default Value:
{:.param}



* 0.1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border :{ width :2 }}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.connectorLine<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-datalabel-connectorline}




Contains the options to customize the line connecting the point and the data label.






### commonSeriesOptions.marker.dataLabel.connectorLine.type<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-connectorline-type}




Specifies whether to connect the point and data label using bezier curve or straight line. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ type : "spline" }}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.connectorLine.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-connectorline-width}




Specifies the width of the connector line.


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ width : 2 }}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.fill<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-datalabel-fill}




Specifies the fill color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{fill : "green"}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-datalabel-font}




Specifies the font of the dataLabel. These are the properties involved in customizing the data label font.






### commonSeriesOptions.marker.dataLabel.font.fontFamily<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-datalabel-font-fontfamily}




Specifies the fontFamily of dataLabel. Text in the data label render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-font-fontstyle}




Specifies the fontStyle of dataLabel. Text in the data label render with the specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-font-fontweight}




Specifies the fontWeight of dataLabel. Text in the data label render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-font-opacity}




Specifies the opacity of the text in dataLabel. Text in the data label render with the specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ opacity : 0.5 }}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.size<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-datalabel-font-size}




Specifies the font size of dataLabel. Text in the data label render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { size : "14px" }}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.horizontalTextAlignment<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-horizontaltextalignment}




This property is used to change the alignment of the data label horizontally.


Default Value:
{:.param}



* ej.datavisualization.Chart.horizontalTextAlignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{horizontalTextAlignment : "far"}}}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-datalabel-margin}




Specifies the margin for the data label.






### commonSeriesOptions.marker.dataLabel.margin.bottom<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-margin-bottom}




Specifies the bottom margin value for dataLabel. By specifying this property, we can adjust the text in data label to bottom.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ bottom :10 }}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.left<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-margin-left}




Specifies the left margin value for dataLabel. By specifying this property, we can adjust the text in data label to left.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ left : 10}}}}                 
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.right<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-margin-right}




Specifies the right margin value for dataLabel. By specifying this property, we can adjust the text in data label to right.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ right :10 }}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.top<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-margin-top}




Specifies the top margin value for dataLabel. By specifying this property, we can adjust the text in data label to top.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ top :10 } }}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-datalabel-opacity}




Specifies the opacity of dataLabel.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{opacity : 0.5}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.shape<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-shape}




Specifies the rendering shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{shape : "circle"}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.textPosition<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-textposition}




This property is used to change the position of the text in data label. See <a href="global.html#TextPosition">TextPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.textPosition.Top




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{textPosition : "bottom"}}}                 
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.verticalTextAlignment<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-datalabel-verticaltextalignment}




This property is used to change the alignment of the data label vertically.


Default Value:
{:.param}



* ej.datavisualization.Chart.verticalTextAlignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{verticalTextAlignment : "far"}}}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.visible<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-marker-datalabel-visible}




Toggles the visibility of dataLabel in the marker.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{visible : true}}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.marker.fill<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-fill}




Specifies the fill color of the marker.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker : { fill : "green" } }                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.imageUrl<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-marker-imageurl}




Specifies the image url location of the marker.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{ imageUrl: "../images/sample.png"}}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-opacity}




Specifies the opacity of the marker. Values ranges from 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{ opacity : 0.5 }}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.shape<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-marker-shape}




Specifies the shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.Circle




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{ shape: "rectangle"}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.size<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-marker-size}




Specifies the size of the marker.






### commonSeriesOptions.marker.size.height<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-size-height}




Specifies the height of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{size :{height : 5}}}                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.size.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-marker-size-width}




Specifies the width of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{ size :{ width : 2 } } }                  
});
</script>{% endhighlight %}




### commonSeriesOptions.marker.visible<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-marker-visible}




Toggles the visibility of the marker.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{marker :{ visible : true}}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-opacity}




Specifies the opacity of series. The value ranges form 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{opacity : 0.5}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.pieCoefficient<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-piecoefficient}




Sets the radius of the pie series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ pieCoefficient : 1}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.pyramidMode<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-pyramidmode}




Sets the rendering mode of the pyramid as linear or surface. See <a href="global.html#PyramidMode">PyramidMode</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.PyramidMode.Linear




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ pyramidMode : "linear"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.startAngle<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-startangle}




Specifies the starting angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ startAngle : 150}                  
});
</script> ; {% endhighlight %}




### commonSeriesOptions.tooltip<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-tooltip}




Contains all the properties to customize tooltip






### commonSeriesOptions.tooltip.border<span class="type-signature type object">object</span>
{:#members:commonseriesoptions-tooltip-border}




Options for customizing the color, opacity and width of the border of tooltip.






### commonSeriesOptions.tooltip.border.color<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-tooltip-border-color}




Specifies the border color of tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border:{ color : "green" }}}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.border.width<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-tooltip-border-width}




Specifies the border width of tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border :{ width : 2}}}                  
});
</script>   {% endhighlight %}




### commonSeriesOptions.tooltip.duration<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-tooltip-duration}




Specifies the duration of the tooltip to stay awake.


Default Value:
{:.param}



* "500ms"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{duration : "300ms"}}                  
});
</script>   {% endhighlight %}




### commonSeriesOptions.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-tooltip-enableanimation}




Enabling this property animates the tooltip on moving the cursor from one point to the other.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{enableAnimation : false}}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.fill<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-tooltip-fill}




Specifies the fill color of the tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{fill : "green"}}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.format<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-tooltip-format}




Formatting the values of point on a tooltip can be customized using this property.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ tooltip : { format : "#point.x# : #point.y#%" } }                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.opacity<span class="type-signature type number">number</span>
{:#members:commonseriesoptions-tooltip-opacity}




Specifies the opacity of the tooltip. Values ranges from 0 to 1.


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{tooltip :{opacity : 0.5}}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.template<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-tooltip-template}




Specify the template for tooltip


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ tooltip: { template : "item" }}                  
});
</script>  {% endhighlight %}




### commonSeriesOptions.tooltip.visible<span class="type-signature type boolean">boolean</span>
{:#members:commonseriesoptions-tooltip-visible}




tooltip visibility can be toggled using this property


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ tooltip :{visible : true} }                  
});
</script> {% endhighlight %}




### commonSeriesOptions.type<span class="type-signature type enum">enum</span>
{:#members:commonseriesoptions-type}




Specifies the type of series to be rendered in chart. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ type : "spline"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.xAxisName<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-xaxisname}




Specifies the name of the xAxis.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ xAxisName : "xAxis"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.xName<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-xname}




Specifies the xName for dataSource in series. This is used to take the x values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions : {xName: "XValue" }                   
});
</script> {% endhighlight %}




### commonSeriesOptions.yAxisName<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-yaxisname}




Specifies the name of the yAxis.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{ yAxisName : "yAxis"}                  
});
</script> {% endhighlight %}




### commonSeriesOptions.yName<span class="type-signature type string">string</span>
{:#members:commonseriesoptions-yname}




Specifies the yName for dataSource in series. This is used to take the y values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions :{yName: "XValue" }               
});
</script> {% endhighlight %}




### crosshair<span class="type-signature type object">object</span>
{:#members:crosshair}




Contains the properties to customize crosshair or trackball.






### crosshair.marker<span class="type-signature type object">object</span>
{:#members:crosshair-marker}




Contains property to customize the marker in crosshair.






### crosshair.marker.border<span class="type-signature type object">object</span>
{:#members:crosshair-marker-border}




Options for customizing the width of the border of marker.






### crosshair.marker.border.width<span class="type-signature type number">number</span>
{:#members:crosshair-marker-border-width}




Specifies the border width of the marker in crosshair.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{marker :{border :{ width :2 }}}              
});
</script>{% endhighlight %}




### crosshair.marker.opacity<span class="type-signature type boolean">boolean</span>
{:#members:crosshair-marker-opacity}




Specifies the opacity of the marker in crosshair.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{marker :{opacity :2}}              
});
</script> {% endhighlight %}




### crosshair.marker.size<span class="type-signature type object">object</span>
{:#members:crosshair-marker-size}




Contains property to customize the size of marker.






### crosshair.marker.size.height<span class="type-signature type number">number</span>
{:#members:crosshair-marker-size-height}




Specifies the height of the marker in crosshair.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{marker :{size :{ height :15 }}}              
});
</script> {% endhighlight %}




### crosshair.marker.size.width<span class="type-signature type number">number</span>
{:#members:crosshair-marker-size-width}




Specifies the width of the marker in crosshair.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{marker :{size : {width :15}}}              
});
</script>{% endhighlight %}




### crosshair.marker.visible<span class="type-signature type boolean">boolean</span>
{:#members:crosshair-marker-visible}




Toggles the visibility of the marker in crosshair.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{marker :{visible :false}}              
});
</script>{% endhighlight %}




### crosshair.type<span class="type-signature type enum">enum</span>
{:#members:crosshair-type}




Specifies the type of the crosshair. It may be trackball or crosshair.


Default Value:
{:.param}



* ej.datavisualization.Chart.CrosshairType.Crosshair




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{type : "trackball"}              
});
</script> {% endhighlight %}




### crosshair.visible<span class="type-signature type boolean">boolean</span>
{:#members:crosshair-visible}




Toggles the visibility of the crosshair / trackball in the plot area


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
crosshair :{visible :true}              
});
</script>{% endhighlight %}




### depth<span class="type-signature type number">number</span>
{:#members:depth}




The depth property defines the depth of the 3D chart from front view of the series to wall.


Default Value:
{:.param}



* 100




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
depth : 100            
});
</script>{% endhighlight %}




### enable3D<span class="type-signature type boolean">boolean</span>
{:#members:enable3d}




To enable the 3D view of chart control. 3D view is supported only for column, bar, stacking column, stacking bar, pie and doughnut series types.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
enable3D : true             
});
</script>{% endhighlight %}




### enableCanvasRendering<span class="type-signature type boolean">boolean</span>
{:#members:enablecanvasrendering}




By enabling this property, the ejChart will render in Html5 canvas. This canvas rendering supports all other functionalities except 3D and animation.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
enableCanvasRendering : true             
});
</script>{% endhighlight %}




### enableRotation<span class="type-signature type boolean">boolean</span>
{:#members:enablerotation}




Enables the 3D chart to perform rotation.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
enableRotation : true             
});
</script>{% endhighlight %}




### indicators<span class="type-signature type array">array</span>
{:#members:indicators}




Contains properties for customizing the technical indicators.






### indicators.dPeriod<span class="type-signature type number">number</span>
{:#members:indicators-dperiod}




Specifies the dperiod for the stochastic indicator.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ dPeriod : 4}]                    
});
</script>  {% endhighlight %}




### indicators.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:indicators-enableanimation}




Specifies the animation of the indicator. ejChart supports animation for the indicator. This can be enable/disable by this property


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ enableAnimation :  true}]                    
});
</script>  {% endhighlight %}




### indicators.fill<span class="type-signature type string">string</span>
{:#members:indicators-fill}




Specifies the fill color of the indicator line


Default Value:
{:.param}



* "#00008B"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ fill : "#ff0000"}]                    
});
</script>  {% endhighlight %}




### indicators.font<span class="type-signature type object">object</span>
{:#members:indicators-font}




Contains property to customize the font of the text in indicator.






### indicators.font.color<span class="type-signature type string">string</span>
{:#members:indicators-font-color}




Specifies the font color of the text in indicator


Default Value:
{:.param}



* "#707070"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ color: "#ff00ff" }}]                    
});
</script>  {% endhighlight %}




### indicators.font.fontFamily<span class="type-signature type string">string</span>
{:#members:indicators-font-fontfamily}




Specifies the font family of the text in indicator


Default Value:
{:.param}



* "segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ fontFamily: "Algerian" }}]                    
});
</script>  {% endhighlight %}




### indicators.font.fontStyle<span class="type-signature type string">string</span>
{:#members:indicators-font-fontstyle}




Specifies the font style of the text in indicator


Default Value:
{:.param}



* "Normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ fontStyle: "Italic" }}]                    
});
</script>  {% endhighlight %}




### indicators.font.fontWeight<span class="type-signature type string">string</span>
{:#members:indicators-font-fontweight}




Specifies the font weight of the text in indicator


Default Value:
{:.param}



* "Regular"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ fontWeight: "Regular" }}]                    
});
</script>  {% endhighlight %}




### indicators.font.opacity<span class="type-signature type number">number</span>
{:#members:indicators-font-opacity}




Specifies the font opacity of the text in indicator


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ opacity: 1 }}]                    
});
</script>  {% endhighlight %}




### indicators.font.size<span class="type-signature type string">string</span>
{:#members:indicators-font-size}




Specifies the size of the text in indicator


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ font :{ size: "14px" }}]                    
});
</script>  {% endhighlight %}




### indicators.histogram<span class="type-signature type object">object</span>
{:#members:indicators-histogram}




Contains property to customize the histogram in macd indicator.






### indicators.histogram.border<span class="type-signature type object">object</span>
{:#members:indicators-histogram-border}




Contains property to customize the boder of histogram in macd indicator.






### indicators.histogram.border.color<span class="type-signature type string">string</span>
{:#members:indicators-histogram-border-color}




Specifies the border color of histogram rendered in macd indicator.


Default Value:
{:.param}



* "#9999ff"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ histogram : {border: {color: "#ff0000"}}}]                    
});
</script>  {% endhighlight %}




### indicators.histogram.border.width<span class="type-signature type width">width</span>
{:#members:indicators-histogram-border-width}




Specifies the border width of histogram rendered in macd indicator.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ histogram : {border: {width: 2}}}]                    
});
</script>  {% endhighlight %}




### indicators.histogram.fill<span class="type-signature type string">string</span>
{:#members:indicators-histogram-fill}




Specifies the fill color of histogram rendered in macd indicator.


Default Value:
{:.param}



* "#ccccff"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ histogram : {fill: "#ff0000"}}]                    
});
</script>  {% endhighlight %}




### indicators.histogram.opacity<span class="type-signature type number">number</span>
{:#members:indicators-histogram-opacity}




Specifies the opacity of histogram rendered in macd indicator.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ histogram : {opacity: 0.5}}]                    
});
</script>  {% endhighlight %}




### indicators.kPeriod<span class="type-signature type number">number</span>
{:#members:indicators-kperiod}




Specifies the kperiod for the stochastic indicator.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ kPeriod : 4}]                    
});
</script>  {% endhighlight %}




### indicators.longPeriod<span class="type-signature type number">number</span>
{:#members:indicators-longperiod}




Specifies the long period for macd indicator


Default Value:
{:.param}



* 26




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ longPeriod :  14"}]                    
});
</script>  {% endhighlight %}




### indicators.lowerLine<span class="type-signature type object">object</span>
{:#members:indicators-lowerline}




Contains property to customize the lower line in indicators.






### indicators.lowerLine.fill<span class="type-signature type string">string</span>
{:#members:indicators-lowerline-fill}




Specifies the fill color of lower line.


Default Value:
{:.param}



* "#008000"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ lowerLine : {fill: "#ff0000"}}]                    
});
</script>  {% endhighlight %}




### indicators.lowerLine.width<span class="type-signature type number">number</span>
{:#members:indicators-lowerline-width}




Specifies the width of lower line.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ lowerLine : {width: 3}}]                    
});
</script>  {% endhighlight %}




### indicators.macdLine<span class="type-signature type object">object</span>
{:#members:indicators-macdline}




Contains property to customize the macd line in indicators.






### indicators.macdLine.fill<span class="type-signature type string">string</span>
{:#members:indicators-macdline-fill}




Specifies the fill color of macd line.


Default Value:
{:.param}



* "#ff9933"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ macdLine : {fill: "#ff0000"}}]                    
});
</script>  {% endhighlight %}




### indicators.macdLine.width<span class="type-signature type number">number</span>
{:#members:indicators-macdline-width}




Specifies the width of macd line.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ macdLine : {width: 3}}]                    
});
</script>  {% endhighlight %}




### indicators.macdType<span class="type-signature type string">string</span>
{:#members:indicators-macdtype}




Specifies the type of macd indicator. It can be a line or histogram or both.


Default Value:
{:.param}



* "line"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ macdType :  "both"}]                    
});
</script>  {% endhighlight %}




### indicators.period<span class="type-signature type number">number</span>
{:#members:indicators-period}




Specifies the period of the indicator. Calculations are made based on this for indicator


Default Value:
{:.param}



* 14




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ period : 20}]                    
});
</script>  {% endhighlight %}




### indicators.periodLine<span class="type-signature type object">object</span>
{:#members:indicators-periodline}




Contains property to customize the period line in indicators.






### indicators.periodLine.fill<span class="type-signature type string">string</span>
{:#members:indicators-periodline-fill}




Specifies the fill color of period line.


Default Value:
{:.param}



* "blue"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ periodLine : {fill: "#ff0000"}}]                    
});
</script>  {% endhighlight %}




### indicators.periodLine.width<span class="type-signature type number">number</span>
{:#members:indicators-periodline-width}




Specifies the width of period line.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ periodLine : {width: 3}}]                    
});
</script>  {% endhighlight %}




### indicators.seriesName<span class="type-signature type string">string</span>
{:#members:indicators-seriesname}




Specifies the series name of indicator.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ seriesName : "rsi"}]                    
});
</script>  {% endhighlight %}




### indicators.shortPeriod<span class="type-signature type number">number</span>
{:#members:indicators-shortperiod}




Specifies the short period for macd indicator


Default Value:
{:.param}



* 13




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ shortPeriod :  14"}]                    
});
</script>  {% endhighlight %}




### indicators.standardDeviations<span class="type-signature type number">number</span>
{:#members:indicators-standarddeviations}




Specifies the standardDeviations for Bollingerband indicator.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ standardDeviations : 3}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip<span class="type-signature type object">object</span>
{:#members:indicators-tooltip}




Contains property to customize the tooltip of indicators.






### indicators.tooltip.border<span class="type-signature type object">object</span>
{:#members:indicators-tooltip-border}




Contains property to customize the border of the tooltip in indicators.






### indicators.tooltip.border.color<span class="type-signature type string">string</span>
{:#members:indicators-tooltip-border-color}




Specifies the border color of indicator tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{border : { color :"#0000ff"}} }]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.border.width<span class="type-signature type number">number</span>
{:#members:indicators-tooltip-border-width}




Specifies the border width of indicator tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{border : { width :2}} }]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.duration<span class="type-signature type string">string</span>
{:#members:indicators-tooltip-duration}




Specifies the animation duration of indicator tooltip.


Default Value:
{:.param}



* "500ms"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{duration : "300ms"}}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:indicators-tooltip-enableanimation}




Specifies the animation of the indicator tooltip. ejChart supports animation for the tooltip. This can be enable/disable by this property


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{enableAnimation : false}}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.format<span class="type-signature type string">string</span>
{:#members:indicators-tooltip-format}




Specifies the format of indicator tooltip.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{format : "#point.x#"}}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.format<span class="type-signature type string">string</span>
{:#members:indicators-tooltip-format}




Specifies the fill color of indicator tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{format : "#point.x#"}}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.opacity<span class="type-signature type number">number</span>
{:#members:indicators-tooltip-opacity}




Specifies the opacity of indicator tooltip.


Default Value:
{:.param}



* 0.95




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{opacity : 0.5}}]                    
});
</script>  {% endhighlight %}




### indicators.tooltip.visible<span class="type-signature type boolaean">boolaean</span>
{:#members:indicators-tooltip-visible}




Specifies the visibility of indicator tooltip.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ tooltip :{visible : true}}]                    
});
</script>  {% endhighlight %}




### indicators.trigger<span class="type-signature type number">number</span>
{:#members:indicators-trigger}




Specifies the trigger value for macd indicator


Default Value:
{:.param}



* 9




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ trigger :  14}]                    
});
</script>  {% endhighlight %}




### indicators.trigger<span class="type-signature type string">string</span>
{:#members:indicators-trigger}




Specifies the visibility of indicator


Default Value:
{:.param}



* "visible"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ visibility :  "visible"}]                    
});
</script>  {% endhighlight %}




### indicators.type<span class="type-signature type string">string</span>
{:#members:indicators-type}




Specifies the type of the indicator to render.


Default Value:
{:.param}



* "sma"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ type : "momentum"}]                    
});
</script>  {% endhighlight %}




### indicators.upperLine<span class="type-signature type object">object</span>
{:#members:indicators-upperline}




Contains property to customize the upper line in indicators.






### indicators.upperLine.fill<span class="type-signature type string">string</span>
{:#members:indicators-upperline-fill}




Specifies the fill color of upper line.


Default Value:
{:.param}



* "#ff9933"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ upperLine : {fill: "#ff0000"}}]                    
});
</script>  {% endhighlight %}




### indicators.upperLine.width<span class="type-signature type number">number</span>
{:#members:indicators-upperline-width}




Specifies the width of upper line.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ upperLine : {width: 3}}]                    
});
</script>  {% endhighlight %}




### indicators.width<span class="type-signature type number">number</span>
{:#members:indicators-width}




Specifies the width of the indicator line


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ width :  3}]                    
});
</script>  {% endhighlight %}




### indicators.xAxisName<span class="type-signature type string">string</span>
{:#members:indicators-xaxisname}




Specifies the xAxisName of the indicator


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ xAxisName :  "xAxis"}]                    
});
</script>  {% endhighlight %}




### indicators.yAxisName<span class="type-signature type string">string</span>
{:#members:indicators-yaxisname}




Specifies the yAxisName of the indicator


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
indicators :[{ yAxisName :  "yAxis"}]                    
});
</script>  {% endhighlight %}




### legend<span class="type-signature type object">object</span>
{:#members:legend}




Contains all the properties to customize legend.






### legend.alignment<span class="type-signature type enum">enum</span>
{:#members:legend-alignment}




This property is used to change the alignment of the legend horizontally.. See <a href="global.html#Alignment">Alignment</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Alignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{alignment : "far"}                    
});
</script>   {% endhighlight %}




### legend.border<span class="type-signature type object">object</span>
{:#members:legend-border}




Options for customizing the color and width of the border of legend.






### legend.border.color<span class="type-signature type string">string</span>
{:#members:legend-border-color}




Specifies the border color of legend.


Default Value:
{:.param}



* "transparent"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend : {border :{ color :"green"}}                     
});
</script>   {% endhighlight %}




### legend.border.width<span class="type-signature type number">number</span>
{:#members:legend-border-width}




Specifies the border width of legend.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ border :{width :2}}                     
});
</script>  {% endhighlight %}




### legend.columnCount<span class="type-signature type number">number</span>
{:#members:legend-columncount}




This property specifies the number of columns for the legend items to arrange.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ columnCount : 2}                    
});
</script> {% endhighlight %}




### legend.fill<span class="type-signature type string">string</span>
{:#members:legend-fill}




Specifies the fill color of legend


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ fill : "green"}                    
});
</script> {% endhighlight %}




### legend.font<span class="type-signature type object">object</span>
{:#members:legend-font}




Specifies the legend font. These font properties are used to customize the legend item text.






### legend.font.fontFamily<span class="type-signature type string">string</span>
{:#members:legend-font-fontfamily}




Specifies the legend fontfamily color. Legend item text render with this specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ font :{fontFamily : "algerian"}}                    
});
</script>  {% endhighlight %}




### legend.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:legend-font-fontstyle}




Specifies the legend font style. Legend item text render with this specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ font :{fontStyle : "italic"}}                    
});
</script> {% endhighlight %}




### legend.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:legend-font-fontweight}




Specifies the legend font weight. Legend item text render with this specified font weight.<a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ font :{fontWeight : "lighter"}}                    
});
</script>  {% endhighlight %}




### legend.font.size<span class="type-signature type string">string</span>
{:#members:legend-font-size}




Specifies the legend font size. Legend item text render with this specified size.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ font :{size : "14px"}}                    
});
</script> {% endhighlight %}




### legend.itemPadding<span class="type-signature type number">number</span>
{:#members:legend-itempadding}




This is used to specify the gap/padding between the legend items.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{itemPadding : 5}                     
});
</script>  {% endhighlight %}




### legend.itemStyle<span class="type-signature type object">object</span>
{:#members:legend-itemstyle}




Contains property to customize the legend item style.






### legend.itemStyle.border<span class="type-signature type object">object</span>
{:#members:legend-itemstyle-border}




Options for customizing the color and width of the border of legend.






### legend.itemStyle.border.color<span class="type-signature type string">string</span>
{:#members:legend-itemstyle-border-color}




Specifies the border color of legend.


Default Value:
{:.param}



* "transparent"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ itemStyle :{border : { color : "green' }}}                    
});
</script> {% endhighlight %}




### legend.itemStyle.border.width<span class="type-signature type number">number</span>
{:#members:legend-itemstyle-border-width}




Specifies the border width of legend.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ itemStyle :{border :{ width : 2 }}}                    
});
</script>  {% endhighlight %}




### legend.itemStyle.height<span class="type-signature type number">number</span>
{:#members:legend-itemstyle-height}




Specifies the legend item height.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ itemStyle :{height : 20}}                    
});
</script>  {% endhighlight %}




### legend.itemStyle.width<span class="type-signature type number">number</span>
{:#members:legend-itemstyle-width}




Specifies the legend item width.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ itemStyle :{width : 15}}                    
});
</script> {% endhighlight %}




### legend.location<span class="type-signature type object">object</span>
{:#members:legend-location}




Contains property to customize the position of the legend






### legend.location.x<span class="type-signature type number">number</span>
{:#members:legend-location-x}




This property specifies the x position for rendering legend.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{location :{x :20}}                    
});
</script>   {% endhighlight %}




### legend.location.y<span class="type-signature type number">number</span>
{:#members:legend-location-y}




This property specifies the y position for rendering legend.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{location : {y : 100}}                  
});
</script>  {% endhighlight %}




### legend.opacity<span class="type-signature type number">number</span>
{:#members:legend-opacity}




Specifies the opacity of legend


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ opacity : 0.5}                    
});
</script> {% endhighlight %}




### legend.position<span class="type-signature type enum">enum</span>
{:#members:legend-position}




This property is used to change the alignment of the data label vertically. See <a href="global.html#Position">Position</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Position.Bottom




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ position : "top"}                    
});
</script>   {% endhighlight %}




### legend.rowCount<span class="type-signature type number">number</span>
{:#members:legend-rowcount}




This property specifies the number of rows for the legend items to arrange.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ rowCount :2}                    
});
</script> {% endhighlight %}




### legend.shape<span class="type-signature type enum">enum</span>
{:#members:legend-shape}




This property specifies the shape of the legend items. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ shape : "circle" }                      
});
</script>  {% endhighlight %}




### legend.size<span class="type-signature type object">object</span>
{:#members:legend-size}




Contains property to customize the size of legend.






### legend.size.height<span class="type-signature type number">number</span>
{:#members:legend-size-height}




Specifies the legend height.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ size :{height : 20%}}                    
});
</script>  {% endhighlight %}




### legend.size.width<span class="type-signature type number">number</span>
{:#members:legend-size-width}




Specifies the legend width.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{ size :{width : 20%}}                    
});
</script>  {% endhighlight %}




### legend.title<span class="type-signature type object">object</span>
{:#members:legend-title}




Specifies the title of the legend.






### legend.title.font<span class="type-signature type object">object</span>
{:#members:legend-title-font}




Specifies the font options to customize the legend title.






### legend.title.font.fontFamily<span class="type-signature type string">string</span>
{:#members:legend-title-font-fontfamily}




Specifies the font family of legend title text.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { font :{fontFamily: "Algerian" } } }                      
});
</script> {% endhighlight %}




### legend.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:legend-title-font-fontstyle}




Specifies the font style of legend title text.


Default Value:
{:.param}



* "normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { font :{fontStyle: "normal" } } }                      
});
</script> {% endhighlight %}




### legend.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:legend-title-font-fontweight}




Specifies the font weight of legend title text.


Default Value:
{:.param}



* "normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { font :{fontWeight: "normal" } } }                      
});
</script> {% endhighlight %}




### legend.title.font.size<span class="type-signature type string">string</span>
{:#members:legend-title-font-size}




Specifies the size of legend title text.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { font :{size: "14px" } } }                      
});
</script> {% endhighlight %}




### legend.title.text<span class="type-signature type string">string</span>
{:#members:legend-title-text}




Specifies the text to be displayed as legend title.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { text : "Countries" } }                      
});
</script> {% endhighlight %}




### legend.title.textAlignment<span class="type-signature type enum">enum</span>
{:#members:legend-title-textalignment}




Specifies the text alignment of legend title.


Default Value:
{:.param}



* "center"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend: { title: { textAlignment : "near" } }                      
});
</script> {% endhighlight %}




### legend.visible<span class="type-signature type boolean">boolean</span>
{:#members:legend-visible}




Toggles the legend visibility.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
legend :{visible : false}                     
});
</script>   {% endhighlight %}




### locale<span class="type-signature type string">string</span>
{:#members:locale}




This property is to specify the localization of chart.


Default Value:
{:.param}



* "en-US"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
locale : "en-US"            
});
</script>{% endhighlight %}




### perspectiveAngle<span class="type-signature type number">number</span>
{:#members:perspectiveangle}




Enables the 3D chart to perform rotation.


Default Value:
{:.param}



* 90




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
perspectiveAngle : 60             
});
</script>{% endhighlight %}




### primaryXAxis<span class="type-signature type object">object</span>
{:#members:primaryxaxis}




This is a horizontal axis which contains options to configure axis. This is the primary x axis for all the series in series array. If you need to override x axis for particular series, you can create an axis object by providing unique name using name property and add it to axes array. Then, assign the name to the series&rsquo;s xAxisName property to link both axis and series.






### primaryXAxis.alternateGridBand<span class="type-signature type object">object</span>
{:#members:primaryxaxis-alternategridband}




This is a horizontal axis alternate grid band which contains options to highlight alternate grid bands.






### primaryXAxis.alternateGridBand.even<span class="type-signature type object">object</span>
{:#members:primaryxaxis-alternategridband-even}




Specifies the Even Alternative Grid Band.






### primaryXAxis.alternateGridBand.even.fill<span class="type-signature type string">string</span>
{:#members:primaryxaxis-alternategridband-even-fill}




Specifies the fill color of Even grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { even :{ fill : "green" } } }                    
});
</script> {% endhighlight %}




### primaryXAxis.alternateGridBand.even.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-alternategridband-even-opacity}




Specifies the opacity of the Even grid band.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { even :{ opacity : 0.5 } } }                   
});
</script> {% endhighlight %}




### primaryXAxis.alternateGridBand.odd<span class="type-signature type object">object</span>
{:#members:primaryxaxis-alternategridband-odd}




Specifies the Odd Alternative Grid Band.






### primaryXAxis.alternateGridBand.odd.fill<span class="type-signature type string">string</span>
{:#members:primaryxaxis-alternategridband-odd-fill}




Specifies the fill color of Odd grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { odd :{ fill : "red" } } }                      
});
</script> {% endhighlight %}




### primaryXAxis.alternateGridBand.odd.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-alternategridband-odd-opacity}




Specifies the opacity of the Odd grid band.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { odd :{ opacity : 0.5 } } }                      
});
</script> {% endhighlight %}




### primaryXAxis.axisLine<span class="type-signature type object">object</span>
{:#members:primaryxaxis-axisline}




Specifies the options to configure axis line.






### primaryXAxis.axisLine.dashArray<span class="type-signature type string">string</span>
{:#members:primaryxaxis-axisline-dasharray}




Controls the pattern of dashes and gaps used to stroke the axis line.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { axisLine : { dashArray : "2,3" } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.axisLine.offset<span class="type-signature type number">number</span>
{:#members:primaryxaxis-axisline-offset}




Specifies the horizontal/vertical padding of axis line. Normally, it is used along with plotOffset to pad the plot area.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { axisLine : { offset : 5 } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.axisLine.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-axisline-visible}




Specifies the visibility of axis line.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { axisLine : { visible : false } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.axisLine.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-axisline-width}




Specifies the width of axisLine in primaryXAxis.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { axisLine : { width : 2 } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.columnIndex<span class="type-signature type number">number</span>
{:#members:primaryxaxis-columnindex}




Index of the column object in columnDefinitions array to which this axis is associated with.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { columnIndex: 2 }                      
});
</script> {% endhighlight %}




### primaryXAxis.columnSpan<span class="type-signature type number">number</span>
{:#members:primaryxaxis-columnspan}




An axis can be spanned along multiple columns or plotting areas. This property specifies the number of columns/plotting areas this axis should be spanned.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { columnSpan: 2 }                      
});
</script> {% endhighlight %}




### primaryXAxis.crosshairLabel<span class="type-signature type object">object</span>
{:#members:primaryxaxis-crosshairlabel}




Options to configure the visibility of the crosshair label.






### primaryXAxis.crosshairLabel.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-crosshairlabel-visible}




Specifies the visibility of crosshair label.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { crosshairLabel : { visible : true} }                      
});
</script>  {% endhighlight %}




### primaryXAxis.desiredIntervals<span class="type-signature type number">number</span>
{:#members:primaryxaxis-desiredintervals}




Specifies the desired number of intervals for the range. With this setting, you can request axis to calculate nice numbers such that they result in the number of intervals approximately equal to your desired interval.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { desiredIntervals: 5 }                      
});
</script> {% endhighlight %}




### primaryXAxis.edgeLabelPlacement<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-edgelabelplacement}




Determines how to position labels at the edge of the axis. See <a href="global.html#EdgeLabelPlacement">EdgeLabelPlacement</a> for the available options.


Default Value:
{:.param}



* ej.datavisualization.Chart.EdgeLabelPlacement.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { edgeLabelPlacement : "shift" }                      
});
</script>  {% endhighlight %}




### primaryXAxis.enableTrim
{:#members:primaryxaxis-enabletrim}




Specifies the action to take when the axis labels are which is having more than the width 34.


Default Value:
{:.param}



* false type {boolean}




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { enableTrim : true }                      
});
</script>    {% endhighlight %}




### primaryXAxis.font<span class="type-signature type object">object</span>
{:#members:primaryxaxis-font}




Specifies the font of primaryXAxis.






### primaryXAxis.font.fontFamily<span class="type-signature type string">string</span>
{:#members:primaryxaxis-font-fontfamily}




Specifies the fontfamily of primaryXAxis. The axis labels render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { font : { fontFamily : "Algerian"} }                      
});
</script>   {% endhighlight %}




### primaryXAxis.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-font-fontstyle}




Specifies the fontStyle of primaryXAxis. The axis labels render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { font : { fontStyle : "Italic"} }                      
});
</script>  {% endhighlight %}




### primaryXAxis.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-font-fontweight}




Specifies the fontWeight of primaryXAxis. The axis labels render with this specified fontWeight.See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { font : { fontWeight : "lighter"} }                      
});
</script>  {% endhighlight %}




### primaryXAxis.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-font-opacity}




Specifies the title opacity of primaryXAxis. The axis labels render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { font : { opacity : 0.5} }                      
});
</script>  {% endhighlight %}




### primaryXAxis.font.size<span class="type-signature type string">string</span>
{:#members:primaryxaxis-font-size}




Specifies the title size of primaryXAxis. The axis labels render with this specified size.


Default Value:
{:.param}



* "13px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { font : { size : "12px"} }                      
});
</script>  {% endhighlight %}




### primaryXAxis.intervalType<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-intervaltype}




Specifies whether the type of the interval calculated is in days, months, hours, minutes etc., This is applicable only when valueType is &lsquo;datetime&rsquo;. See <a href="global.html#IntervalType">IntervalType</a>


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { intervalType: "days" }                      
});
</script> {% endhighlight %}




### primaryXAxis.isInversed<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-isinversed}




Renders the axis in inversed position.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { isInversed : true}                      
});
</script>  {% endhighlight %}




### primaryXAxis.labelFormat<span class="type-signature type string">string</span>
{:#members:primaryxaxis-labelformat}




Provides the format for axis labels.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { labelFormat: "{value}%" }                      
});
</script> {% endhighlight %}




### primaryXAxis.labelIntersectAction<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-labelintersectaction}




Specifies the action to take when the axis labels are overlapping with each other. See <a href="global.html#LabelIntersectAction">LabelIntersectAction</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelIntersectAction.None




Example
{:.example}


{% highlight html %}
              
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { labelIntersectAction : "multipleRows" }                      
});
</script>  {% endhighlight %}




### primaryXAxis.labelPosition<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-labelposition}




Specifies the position of the axis labels.


Default Value:
{:.param}



* "outside"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { labelPosition : "inside" }                       
});
</script> {% endhighlight %}




### primaryXAxis.labelRotation<span class="type-signature type number">number</span>
{:#members:primaryxaxis-labelrotation}




Rotates the axis labels by the specified angle. Angle must be given in degrees.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { labelRotation: 90 }                      
});
</script> {% endhighlight %}




### primaryXAxis.logBase<span class="type-signature type number">number</span>
{:#members:primaryxaxis-logbase}




Specifies the logarithmic base value. This is applicable only when valueType is logarithmic.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { logBase: 5 }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorGridLines<span class="type-signature type object">object</span>
{:#members:primaryxaxis-majorgridlines}




Options for configuring major grid lines color, width, dash arrays etc.,






### primaryXAxis.majorGridLines.dashArray<span class="type-signature type string">string</span>
{:#members:primaryxaxis-majorgridlines-dasharray}




Controls the pattern of dashes and gaps used to stroke the major grid lines.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
    primaryXAxis: { majorGridLines: { dashArray : "2,3"} }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorGridLines.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-majorgridlines-opacity}




Specifies the opacity of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { majorGridLines: { opacity: 0.5 } }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-majorgridlines-visible}




Specifies the visibility of the major grid lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { majorGridLines: { visible: false } }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorGridLines.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-majorgridlines-width}




Specifies the width of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
    primaryXAxis: { majorGridLines: { width : 0.5} }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorTickLines<span class="type-signature type object">object</span>
{:#members:primaryxaxis-majorticklines}




Options for configuring major tick lines color, width, dash arrays etc.,






### primaryXAxis.majorTickLines.size<span class="type-signature type number">number</span>
{:#members:primaryxaxis-majorticklines-size}




Length of the major tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { majorTickLines: { size: 2 } }                      
});
</script> {% endhighlight %}




### primaryXAxis.majorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-majorticklines-visible}




Specifies the visibility of the major tick lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { majorTickLines: { visible: false } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.majorTickLines.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-majorticklines-width}




Specifies the width of the major tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { majorTickLines: { width: 2 } }                      
});
</script> {% endhighlight %}




### primaryXAxis.maximumLabels<span class="type-signature type number">number</span>
{:#members:primaryxaxis-maximumlabels}




Specifies the maximum number of labels to be displayed in 100 pixels.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { maximumLabels : 5 }                      
});
</script>  {% endhighlight %}




### primaryXAxis.maximumLabelWidth
{:#members:primaryxaxis-maximumlabelwidth}




Specifies the width of label till how much width we have to trim.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumLabelWidth type {int}




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { maximumLabelWidth :34.5 }                      
});
</script>    {% endhighlight %}




### primaryXAxis.minorGridLines<span class="type-signature type object">object</span>
{:#members:primaryxaxis-minorgridlines}




Options for configuring minor grid lines color, width, dash arrays etc.,






### primaryXAxis.minorGridLines.dashArray<span class="type-signature type string">string</span>
{:#members:primaryxaxis-minorgridlines-dasharray}




Controls the pattern of dashes and gaps used to stroke the minor grid lines.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorGridLines: { dashArray: "2,3" } }                      
});
</script>{% endhighlight %}




### primaryXAxis.minorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-minorgridlines-visible}




Specifies the visibility of the minorGridLines. The user can modify the visibility of the minorGridLines in primaryXAxis.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorGridLines: { visible: true } }                      
});
</script> {% endhighlight %}




### primaryXAxis.minorGridLines.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-minorgridlines-width}




Specifies the width of the minorGridLines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorGridLines: { width: 2 } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.minorTickLines<span class="type-signature type object">object</span>
{:#members:primaryxaxis-minorticklines}




Options for configuring minor tick lines color, width, dash arrays etc,.






### primaryXAxis.minorTickLines.size<span class="type-signature type number">number</span>
{:#members:primaryxaxis-minorticklines-size}




Length of the minor tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorTickLines: { size: 2 } }                      
});
</script> {% endhighlight %}




### primaryXAxis.minorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-minorticklines-visible}




Specifies the visibility of the minor tick lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorTickLines: { visible: true } }                      
});
</script> {% endhighlight %}




### primaryXAxis.minorTickLines.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-minorticklines-width}




Specifies the width of the minor tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorTickLines: { width: 2 } }                      
});
</script> {% endhighlight %}




### primaryXAxis.minorTicksPerInterval<span class="type-signature type number">number</span>
{:#members:primaryxaxis-minorticksperinterval}




Specifies the number of minor ticks to render per major tick/interval.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { minorTicksPerInterval: 5 }                      
});
</script> {% endhighlight %}




### primaryXAxis.name<span class="type-signature type string">string</span>
{:#members:primaryxaxis-name}




Unique name of the axis.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { name: "xAxis" }                      
});
</script>  {% endhighlight %}




### primaryXAxis.opposedPosition<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-opposedposition}




Specifies a value that indicates whether to position the axis opposite to its default position.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { opposedPosition : true }                      
});
</script>  {% endhighlight %}




### primaryXAxis.plotOffset<span class="type-signature type number">number</span>
{:#members:primaryxaxis-plotoffset}




Horizontal/vertical padding for the plotting area based on the orientation of the axis.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { plotOffset: 0 }                      
});
</script> {% endhighlight %}




### primaryXAxis.rangePadding<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-rangepadding}




If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.rangePaddding.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { rangePadding : "normal" }                      
});
</script>  {% endhighlight %}




### primaryXAxis.roundingPlaces<span class="type-signature type number">number</span>
{:#members:primaryxaxis-roundingplaces}




Rounds the axis labels to the specified number of decimals.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { roundingPlaces: 3 }                      
});
</script>  {% endhighlight %}




### primaryXAxis.stripLine<span class="type-signature type array">array</span>
{:#members:primaryxaxis-stripline}




Options to configure stripLine&rsquo;s color, text, border etc.,


Default Value:
{:.param}



* [ ]







### primaryXAxis.stripLine.borderColor<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-bordercolor}




Border color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ borderColor: "green" }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.color<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-color}




Background color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ color: "green" }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.end<span class="type-signature type number">number</span>
{:#members:primaryxaxis-stripline-end}




Specifies the end value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ end: 5 }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font<span class="type-signature type object">object</span>
{:#members:primaryxaxis-stripline-font}




Specifies the font of stripLine in primaryXAxis. These are font properties for stripLine text






### primaryXAxis.stripLine.font.color<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-font-color}




Specifies the color of stripLine in primaryXAxis. Stripline text render with this color


Default Value:
{:.param}



* "black"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { color: "green"} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font.fontFamily<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-stripline-font-fontfamily}




Specifies the fontFamily of stripLine in primaryXAxis. Stripline text render with this fontFamily


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-stripline-font-fontstyle}




Specifies the fontStyle of stripLine in primaryXAxis. Stripline text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* "Normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font.fontWeight<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-font-fontweight}




Specifies the fontWeight of stripLine in primaryXAxis. Stripline text render with this fontWeight


Default Value:
{:.param}



* "regular"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-stripline-font-opacity}




Specifies the opacity of stripLine in primaryXAxis. Stripline text render with this opacity


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { opacity: 0.5} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.font.size<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-font-size}




Specifies the size of stripLine in primaryXAxis. Stripline text render with this size


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { size: "15px"} }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.start<span class="type-signature type number">number</span>
{:#members:primaryxaxis-stripline-start}




Specifies the start value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ start: 2 }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.startFromAxis<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-stripline-startfromaxis}




Indicates whether to render the stripLine from the minimum/start value of the axis.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ startFromAxis : true }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.text<span class="type-signature type string">string</span>
{:#members:primaryxaxis-stripline-text}




Text to be displayed inside the stripLine.


Default Value:
{:.param}



* "stripLine"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ text : "Empty Point" }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.textAlignment<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-stripline-textalignment}




Alignment of the text displayed in stripLine. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ textAlignment : "middletop" }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-stripline-visible}




Specifies the visibility of the stripLine.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ visible : true }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.width<span class="type-signature type number">number</span>
{:#members:primaryxaxis-stripline-width}




Stripline width to be calculated and displayed when enable startFromAxis or set start value of stripline.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ width : 0 }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.stripLine.zIndex<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-stripline-zindex}




Specifies the z order position of the stripLine.


Default Value:
{:.param}



* "over"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { stripLine:[{ zIndex: "behind" }]}                      
});
</script> {% endhighlight %}




### primaryXAxis.tickLinesPosition<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-ticklinesposition}




Specifies the position of the axis tick lines.


Default Value:
{:.param}



* "outside"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { tickLinesPosition : "inside" }                       
});
</script> {% endhighlight %}




### primaryXAxis.title<span class="type-signature type object">object</span>
{:#members:primaryxaxis-title}




Contains property to customize the title in chart.






### primaryXAxis.title.enableTrim<span class="type-signature type object">Object</span>
{:#members:primaryxaxis-title-enabletrim}




Options to trim and wrap the chart axis title .See enableTrim for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.enableTrim




Example
{:.example}


{% highlight html %}
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title:{enableTrim:true} }                      
});
</script> {% endhighlight %}




### primaryXAxis.title.font<span class="type-signature type object">object</span>
{:#members:primaryxaxis-title-font}




Specifies the font. These font properties are customization are applied for title text.






### primaryXAxis.title.font.fontFamily<span class="type-signature type string">string</span>
{:#members:primaryxaxis-title-font-fontfamily}




Specifies the title fontfamily of primaryXAxis. This fontFamily is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { font : { fontFamily : "Algerain"} } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-title-font-fontstyle}




Specifies the title fontStyle of primaryXAxis. This fontStyle is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { font : { fontStyle : "Italic"} } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-title-font-fontweight}




Specifies the title fontWeight of primaryXAxis. This fontWeight is applied to the title text of primaryXAxis. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { font : { fontWeight : "lighter"} } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.title.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryxaxis-title-font-opacity}




Specifies the title opacity of primaryXAxis. This opacity value is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { font : { opacity : 0.8} } }                      
});
</script>  {% endhighlight %}




### primaryXAxis.title.font.size<span class="type-signature type string">string</span>
{:#members:primaryxaxis-title-font-size}




Specifies the title size of primaryXAxis. This font size is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* "16px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { font : { size : "14px"} } }                      
});
</script>   {% endhighlight %}




### primaryXAxis.title.maximumTitleWidth<span class="type-signature type number">number</span>
{:#members:primaryxaxis-title-maximumtitlewidth}




use the value for trim and wrap the chart axis title based on the customer input .See maximumTitleWidth for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumTitleWidth.null




Example
{:.example}


{% highlight html %}
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title:{maximumTitleWidth: null} }                      
});
</script> {% endhighlight %}




### primaryXAxis.title.text<span class="type-signature type string">string</span>
{:#members:primaryxaxis-title-text}




The value of the title of chart can be specified using this property.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title: { text: "Year" } }                      
});
</script> {% endhighlight %}




### primaryXAxis.valueType<span class="type-signature type enum">enum</span>
{:#members:primaryxaxis-valuetype}




You can plot any type of data like date time, double, string etc., This property determines the type of data that this axis will handle. See <a href="global.html#ValueType">ValueType</a>


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { valueType: "double" }                      
});
</script>  {% endhighlight %}




### primaryXAxis.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryxaxis-visible}




Specifies the visibility of the axis.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { visible: false }                      
});
</script>  {% endhighlight %}




### primaryXAxis.zoomFactor<span class="type-signature type number">number</span>
{:#members:primaryxaxis-zoomfactor}




This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { zoomFactor : 0.5 }                      
});
</script>  {% endhighlight %}




### primaryXAxis.zoomPosition<span class="type-signature type number">number</span>
{:#members:primaryxaxis-zoomposition}




This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { zoomPosition :0.5 }                      
});
</script>  {% endhighlight %}




### primaryYAxis<span class="type-signature type object">object</span>
{:#members:primaryyaxis}




This is a vertical axis which contains options to configure axis. This is the primary y axis for all the series in series array. If you need to override y axis for particular series, you can create an axis object by providing unique name using name property and add it to axes array. Then, assign the name to the series&rsquo;s yAxisName property to link both axis and series.






### primaryYAxis.alternateGridBand<span class="type-signature type object">object</span>
{:#members:primaryyaxis-alternategridband}




This is a Vertical axis alternate grid band which contains options to highlight alternate grid bands.






### primaryYAxis.alternateGridBand.even<span class="type-signature type object">object</span>
{:#members:primaryyaxis-alternategridband-even}




Specifies the Even Alternative Grid Band.






### primaryYAxis.alternateGridBand.even.fill<span class="type-signature type string">string</span>
{:#members:primaryyaxis-alternategridband-even-fill}




Specifies the fill color of Even grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { even : {fill : "red" } } }                      
});
</script> {% endhighlight %}




### primaryYAxis.alternateGridBand.even.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-alternategridband-even-opacity}




Specifies the opacity of the Even grid band.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { even : {opacity : 0.5 } } }                      
});
</script> {% endhighlight %}




### primaryYAxis.alternateGridBand.odd<span class="type-signature type object">object</span>
{:#members:primaryyaxis-alternategridband-odd}




Specifies the Odd Alternative Grid Band.






### primaryYAxis.alternateGridBand.odd.fill<span class="type-signature type string">string</span>
{:#members:primaryyaxis-alternategridband-odd-fill}




Specifies the fill color of Odd grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { odd : { fill :"red" }  } }                      
});
</script> {% endhighlight %}




### primaryYAxis.alternateGridBand.odd.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-alternategridband-odd-opacity}




Specifies the opacity of the Odd grid band.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { odd : { opacity :0.5 }  } }                       
});
</script> {% endhighlight %}




### primaryYAxis.axisLine<span class="type-signature type object">object</span>
{:#members:primaryyaxis-axisline}




Specifies the options to configure axis line.






### primaryYAxis.axisLine.dashArray<span class="type-signature type string">string</span>
{:#members:primaryyaxis-axisline-dasharray}




Controls the pattern of dashes and gaps used to stroke the axis line.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { crosshairLabel: { axisLine :{ dashArray : "2,3" } } }                      
});
</script> {% endhighlight %}




### primaryYAxis.axisLine.offset<span class="type-signature type number">number</span>
{:#members:primaryyaxis-axisline-offset}




Specifies the horizontal/vertical padding of axis line. Normally, it is used along with plotOffset to pad the plot area.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { axisLine: { offset : 5 } }                      
});
</script> {% endhighlight %}




### primaryYAxis.axisLine.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-axisline-visible}




Specifies the visibility of axis line.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { axisLine: { visible : false } }                      
});
</script> {% endhighlight %}




### primaryYAxis.axisLine.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-axisline-width}




Specifies the width of axisLine in primaryYAxis. The user can change the width of the axisLine.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { axisLine: { width : 2 } }                      
});
</script> {% endhighlight %}




### primaryYAxis.crosshairLabel<span class="type-signature type object">object</span>
{:#members:primaryyaxis-crosshairlabel}




Options to configure the visibility of the crosshair label.






### primaryYAxis.crosshairLabel.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-crosshairlabel-visible}




Specifies the visibility of crosshairLabel. This is the property to change the visibility of the axis labels.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { crosshairLabel: { visible : true } }                      
});
</script> {% endhighlight %}




### primaryYAxis.desiredIntervals<span class="type-signature type number">number</span>
{:#members:primaryyaxis-desiredintervals}




Specifies the desired number of intervals for the range. With this setting, you can request axis to calculate nice numbers such that they result in the number of intervals approximately equal to your desired interval.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { desiredIntervals: 5 }                      
});
</script> {% endhighlight %}




### primaryYAxis.edgeLabelPlacement<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-edgelabelplacement}




Determines how to position labels at the edge of the axis. See <a href="global.html#EdgeLabelPlacement">EdgeLabelPlacement</a> for the available options.


Default Value:
{:.param}



* ej.datavisualization.Chart.EdgeLabelPlacement.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { edgeLabelPlacement: "shift" }                      
});
</script> {% endhighlight %}




### primaryYAxis.enableTrim
{:#members:primaryyaxis-enabletrim}




Specifies the action to take when the axis labels are which is having more than the width 34.


Default Value:
{:.param}



* false type {boolean}




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { enableTrim : true }                      
});
</script>    {% endhighlight %}




### primaryYAxis.font<span class="type-signature type object">object</span>
{:#members:primaryyaxis-font}




Specifies the font of primaryYAxis. These font properties are applied for the axis labels.






### primaryYAxis.font.fontFamily<span class="type-signature type string">string</span>
{:#members:primaryyaxis-font-fontfamily}




Specifies the fontfamily of primaryYAxis. The axis labels render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { font: { fontFamily : "Algerian" } }                      
});
</script> {% endhighlight %}




### primaryYAxis.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-font-fontstyle}




Specifies the fontStyle of primaryYAxis. The axis labels render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { font: { fontStyle : "italic" } }                      
});
</script> {% endhighlight %}




### primaryYAxis.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-font-fontweight}




Specifies the fontWeight of primaryYAxis. The axis labels render with this specified fontWeight. <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { font: { fontWeight : "normal" } }                      
});
</script>  {% endhighlight %}




### primaryYAxis.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-font-opacity}




Specifies the title opacity of primaryYAxis. The axis labels render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { font: { opacity : 0.5 } }                      
});
</script> {% endhighlight %}




### primaryYAxis.font.size<span class="type-signature type string">string</span>
{:#members:primaryyaxis-font-size}




Specifies the title size of primaryYAxis. The axis labels render with this specified size.


Default Value:
{:.param}



* "13px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { font: { size : "12px" } }                      
});
</script> {% endhighlight %}




### primaryYAxis.intervalType<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-intervaltype}




Specifies whether the type of the interval calculated is in days, months, hours, minutes etc., This is applicable only when valueType is &lsquo;datetime&rsquo;. See <a href="global.html#IntervalType">IntervalType</a>


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { intervalType: "days" }                      
});
</script>  {% endhighlight %}




### primaryYAxis.isInversed<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-isinversed}




Renders the axis in inversed position.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { isInversed : true}                      
});
</script>  {% endhighlight %}




### primaryYAxis.labelFormat<span class="type-signature type string">string</span>
{:#members:primaryyaxis-labelformat}




Provides the format for axis labels.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { labelFormat: "{value}F" }                      
});
</script>  {% endhighlight %}




### primaryYAxis.labelIntersectAction<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-labelintersectaction}




Specifies the action to take when the axis labels are overlapping with each other. See <a href="global.html#LabelIntersectAction">LabelIntersectAction</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelIntersectAction.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { labelIntersectAction: "multipleRows" }                      
});
</script>    {% endhighlight %}




### primaryYAxis.labelPosition<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-labelposition}




Specifies the position of the axis labels.


Default Value:
{:.param}



* "outside"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { labelPosition : "inside" }                       
});
</script> {% endhighlight %}




### primaryYAxis.logBase<span class="type-signature type number">number</span>
{:#members:primaryyaxis-logbase}




Specifies the logarithmic base value. This is applicable only when valueType is logarithmic.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { logBase: 5 }                      
});
</script>   {% endhighlight %}




### primaryYAxis.majorGridLines<span class="type-signature type object">object</span>
{:#members:primaryyaxis-majorgridlines}




Options for configuring major grid lines color, width, dash arrays etc.,






### primaryYAxis.majorGridLines.dashArray<span class="type-signature type string">string</span>
{:#members:primaryyaxis-majorgridlines-dasharray}




Controls the pattern of dashes and gaps used to stroke the major grid lines.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorGridLines : {dashArray : "2,3"} }                      
});
</script>   {% endhighlight %}




### primaryYAxis.majorGridLines.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-majorgridlines-opacity}




Specifies the opacity of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorGridLines : {opacity : 0.5} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.majorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-majorgridlines-visible}




Specifies the visibility of the major grid lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorGridLines : {visible : false} }                      
});
</script>   {% endhighlight %}




### primaryYAxis.majorGridLines.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-majorgridlines-width}




Specifies the width of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorGridLines : {width : 2} }                      
});
</script>   {% endhighlight %}




### primaryYAxis.majorTickLines<span class="type-signature type object">object</span>
{:#members:primaryyaxis-majorticklines}




Options for configuring major tick lines color, width, dash arrays etc.,






### primaryYAxis.majorTickLines.size<span class="type-signature type number">number</span>
{:#members:primaryyaxis-majorticklines-size}




Length of the major tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorTickLines : {size : 2} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.majorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-majorticklines-visible}




Specifies the visibility of the major tick lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorTickLines : {visible : false} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.majorTickLines.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-majorticklines-width}




Specifies the width of the major tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { majorTickLines : {width : 2} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.maximumLabels<span class="type-signature type number">number</span>
{:#members:primaryyaxis-maximumlabels}




Specifies the maximum number of labels to be displayed in 100 pixels.


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { maximumLabels: 5 }                      
});
</script>   {% endhighlight %}




### primaryYAxis.maximumLabelWidth
{:#members:primaryyaxis-maximumlabelwidth}




Specifies the width of label till how much width we have to trim.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumLabelWidth type {int}




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { maximumLabelWidth :34.5 }                      
});
</script>    {% endhighlight %}




### primaryYAxis.minorGridLines<span class="type-signature type object">object</span>
{:#members:primaryyaxis-minorgridlines}




Options for configuring minor grid lines color, width, dash arrays etc.,






### primaryYAxis.minorGridLines.dashArray<span class="type-signature type string">string</span>
{:#members:primaryyaxis-minorgridlines-dasharray}




Controls the pattern of dashes and gaps used to stroke the minor grid lines.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorGridLines : {dashArray : "2,3"} }                      
});
</script>   {% endhighlight %}




### primaryYAxis.minorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-minorgridlines-visible}




Specifies the visibility of the minorGridLines. The user can modify the visibility of the minorGridLines in primaryYAxis.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorGridLines : {visible : true} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.minorGridLines.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-minorgridlines-width}




Specifies the width of the minor grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorGridLines : {width : 2} }                      
});
</script>   {% endhighlight %}




### primaryYAxis.minorTickLines<span class="type-signature type object">object</span>
{:#members:primaryyaxis-minorticklines}




Options for configuring minor tick lines color, width, dash arrays etc.,






### primaryYAxis.minorTickLines.size<span class="type-signature type number">number</span>
{:#members:primaryyaxis-minorticklines-size}




Length of the minor tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorTickLines : {size : 2} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.minorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-minorticklines-visible}




Specifies the visibility of the minor tick lines.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorTickLines : {visible : true} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.minorTickLines.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-minorticklines-width}




Specifies the width of the minor tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorTickLines : {width : 2} }                      
});
</script>  {% endhighlight %}




### primaryYAxis.minorTicksPerInterval<span class="type-signature type number">number</span>
{:#members:primaryyaxis-minorticksperinterval}




Specifies the number of minor ticks to render per major tick/interval.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { minorTicksPerInterval: 3 }                      
});
</script> {% endhighlight %}




### primaryYAxis.name<span class="type-signature type string">string</span>
{:#members:primaryyaxis-name}




Unique name of the axis.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { name: "yAxis" }                      
});
</script> {% endhighlight %}




### primaryYAxis.opposedPosition<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-opposedposition}




Specifies a value that indicates whether to position the axis opposite to its default position.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { opposedPosition : true }                      
});
</script> {% endhighlight %}




### primaryYAxis.plotOffset<span class="type-signature type number">number</span>
{:#members:primaryyaxis-plotoffset}




Horizontal/vertical padding for the plotting area based on the orientation of the axis.


Default Value:
{:.param}



* 10




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { plotOffset: 5 }                      
});
</script>   {% endhighlight %}




### primaryYAxis.rangePadding<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-rangepadding}




If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.RangePadding.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { rangePadding : "none" }                      
});
</script>   {% endhighlight %}




### primaryYAxis.roundingPlaces<span class="type-signature type number">number</span>
{:#members:primaryyaxis-roundingplaces}




Rounds the axis labels to the specified number of decimals.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { roundingPlaces: 2 }                      
});
</script> {% endhighlight %}




### primaryYAxis.rowIndex<span class="type-signature type number">number</span>
{:#members:primaryyaxis-rowindex}




Index of the row object in rowDefinitions array to which this axis is associated with.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { rowIndex: 1 }                      
});
</script> {% endhighlight %}




### primaryYAxis.rowSpan<span class="type-signature type number">number</span>
{:#members:primaryyaxis-rowspan}




An axis can be spanned along multiple rows or plotting areas. This property specifies the number of rows/plotting areas this axis should be spanned.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { rowSpan: 2 }                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine<span class="type-signature type array">array</span>
{:#members:primaryyaxis-stripline}




Options to configure stripLine&rsquo;s color, text, border etc.,


Default Value:
{:.param}



* [ ]







### primaryYAxis.stripLine.borderColor<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-bordercolor}




Border color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ borderColor: "green" }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.color<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-color}




Background color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ color: "green" }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.end<span class="type-signature type number">number</span>
{:#members:primaryyaxis-stripline-end}




Specifies the end value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ end: 5 }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font<span class="type-signature type object">object</span>
{:#members:primaryyaxis-stripline-font}




Specifies the font of stripLine in primaryYAxis. These are font properties for stripLine text






### primaryYAxis.stripLine.font.color<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-font-color}




Specifies the color of stripLine in primaryYAxis. Stripline text render with this color


Default Value:
{:.param}



* "black"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { color: "green"} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font.fontFamily<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-stripline-font-fontfamily}




Specifies the fontFamily of stripLine in primaryYAxis. Stripline text render with this fontFamily


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-stripline-font-fontstyle}




Specifies the fontStyle of stripLine in primaryYAxis. Stripline text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* "Normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font.fontWeight<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-font-fontweight}




Specifies the fontWeight of stripLine in primaryYAxis. Stripline text render with this fontWeight


Default Value:
{:.param}



* "regular"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-stripline-font-opacity}




Specifies the opacity of stripLine in primaryYAxis. Stripline text render with this opacity


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { opacity: 0.5} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.font.size<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-font-size}




Specifies the size of stripLine in primaryYAxis. Stripline text render with this size


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { size: "15px"} }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.start<span class="type-signature type number">number</span>
{:#members:primaryyaxis-stripline-start}




Specifies the start value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ start: 2 }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.startFromAxis<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-stripline-startfromaxis}




Indicates whether to render the stripLine from the minimum/start value of the axis.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ startFromAxis : true }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.text<span class="type-signature type string">string</span>
{:#members:primaryyaxis-stripline-text}




Text to be displayed inside the stripLine.


Default Value:
{:.param}



* "stripLine"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ text : "Empty Point" }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.textAlignment<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-stripline-textalignment}




Alignment of the text displayed in stripLine. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ textAlignment : "middletop" }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-stripline-visible}




Specifies the visibility of the stripLine.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ visible : true }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.width<span class="type-signature type number">number</span>
{:#members:primaryyaxis-stripline-width}




Stripline width to be calculated and displayed when enable startFromAxis or set start value of stripline.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ width : 0 }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.stripLine.zIndex<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-stripline-zindex}




Specifies the z order position of the stripLine.


Default Value:
{:.param}



* "over"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { stripLine:[{ zIndex: "behind" }]}                      
});
</script> {% endhighlight %}




### primaryYAxis.tickLinesPosition<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-ticklinesposition}




Specifies the position of the axis tick lines.


Default Value:
{:.param}



* "outside"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { tickLinesPosition : "inside" }                       
});
</script> {% endhighlight %}




### primaryYAxis.title<span class="type-signature type object">object</span>
{:#members:primaryyaxis-title}




Options to configure the title font and alignment of the axis title.






### primaryYAxis.title.enableTrim<span class="type-signature type object">Object</span>
{:#members:primaryyaxis-title-enabletrim}




Options to trim and wrap the chart axis title .See enableTrim for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.enableTrim




Example
{:.example}


{% highlight html %}
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryXAxis: { title:{enableTrim:true} }                      
});
</script> {% endhighlight %}




### primaryYAxis.title.font<span class="type-signature type object">object</span>
{:#members:primaryyaxis-title-font}




Specifies the font. These font properties are customization are applied for title text.






### primaryYAxis.title.font.fontFamily<span class="type-signature type string">string</span>
{:#members:primaryyaxis-title-font-fontfamily}




Specifies the title fontfamily of primaryYAxis. This fontFamily is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontFamily: "Algerian" } } }                      
});
</script> {% endhighlight %}




### primaryYAxis.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-title-font-fontstyle}




Specifies the title fontStyle of primaryYAxis. This fontStyle is applied to the title text of primaryYAxis. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontStyle : "Italic" } } }                      
});
</script>  {% endhighlight %}




### primaryYAxis.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-title-font-fontweight}




Specifies the title fontWeight of primaryYAxis. This fontWeight is applied to the title text of primaryYAxis. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontWeight: "normal" } } }                      
});
</script>  {% endhighlight %}




### primaryYAxis.title.font.opacity<span class="type-signature type number">number</span>
{:#members:primaryyaxis-title-font-opacity}




Specifies the title opacity of primaryYAxis. This font size is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ font :{ opacity: 0.5 } } }                      
});
</script>  {% endhighlight %}




### primaryYAxis.title.font.size<span class="type-signature type string">string</span>
{:#members:primaryyaxis-title-font-size}




Specifies the title size of primaryYAxis. This opacity value is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* "16px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ font :{ size: "12px" } } }                      
});
</script>  {% endhighlight %}




### primaryYAxis.title.maximumTitleWidth<span class="type-signature type number">number</span>
{:#members:primaryyaxis-title-maximumtitlewidth}




use the value for trim and wrap the chart axis title based on the customer input .See maximumTitleWidth for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumTitleWidth.null




Example
{:.example}


{% highlight html %}
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title:{maximumTitleWidth: null} }                      
});
</script> {% endhighlight %}




### primaryYAxis.title.text<span class="type-signature type string">string</span>
{:#members:primaryyaxis-title-text}




Text to be displayed as a title for axis.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { title :{ text: "yAxis" } }                      
});
</script> {% endhighlight %}




### primaryYAxis.valueType<span class="type-signature type enum">enum</span>
{:#members:primaryyaxis-valuetype}




You can plot any type of data like date time, double, string etc., This property determines the type of data that this axis will handle.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { valueType: "double" }                      
});
</script>  {% endhighlight %}




### primaryYAxis.visible<span class="type-signature type boolean">boolean</span>
{:#members:primaryyaxis-visible}




Specifies the visibility of the axis.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { visible : false }                      
});
</script>  {% endhighlight %}




### primaryYAxis.zoomFactor<span class="type-signature type number">number</span>
{:#members:primaryyaxis-zoomfactor}




This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { zoomFactor : 0.5 }                      
});
</script> {% endhighlight %}




### primaryYAxis.zoomPosition<span class="type-signature type number">number</span>
{:#members:primaryyaxis-zoomposition}




This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
primaryYAxis: { zoomPosition : 0.5 }                      
});
</script>  {% endhighlight %}




### rotation<span class="type-signature type number">number</span>
{:#members:rotation}




The rotation property is used to spin the 3D chart.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
rotation : 45             
});
</script>{% endhighlight %}




### rowDefinitions<span class="type-signature type array">array</span>
{:#members:rowdefinitions}




You can split chart into multiple plotting areas horizontally. In order to split the chart horizontally, you need to specify number of row objects in rowDefintions array. Each object in the rowDefnitions represent a plotting area in chart.



Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
rowDefinitions :[{unit : "percentage"}]                      
});
</script>  {% endhighlight %}




### series<span class="type-signature type array">array</span>
{:#members:series}




Specifies the properties used for customizing the series.






### series.bearFillColor<span class="type-signature type string">string</span>
{:#members:series-bearfillcolor}




Specifies the bearFillColor for series. This is used in hilo series types


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{bearFillColor: "blue" }]                   
});
</script> {% endhighlight %}




### series.border<span class="type-signature type object">object</span>
{:#members:series-border}




Specifies the border of the series. These are the properties involved in customizing the series border.






### series.border.color<span class="type-signature type string">string</span>
{:#members:series-border-color}




Specifies the border color of series. Series in chart render with this specified color as border color


Default Value:
{:.param}



* "transparent"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{border :{ color : "green" } }]                  
});
</script>{% endhighlight %}




### series.border.width<span class="type-signature type number">number</span>
{:#members:series-border-width}




Specifies the border width of series.Series in chart render with this specified value as border width


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{border :{ width : 2 } }]                  
});
</script>{% endhighlight %}




### series.bullFillColor<span class="type-signature type string">string</span>
{:#members:series-bullfillcolor}




Specifies the bullFillColor for series. This is used in hilo series types


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{bullFillColor: "green" }]                   
});
</script> {% endhighlight %}




### series.dashArray<span class="type-signature type string">string</span>
{:#members:series-dasharray}




Controls the pattern of dashes and gaps used to stroke the line series.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{dashArray : "2,3"}]                  
});
</script> {% endhighlight %}




### series.dataSource<span class="type-signature type object">object</span>
{:#members:series-datasource}




Specifies the dataSource for series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{dataSource: data.open }]                   
});
</script> {% endhighlight %}




### series.doughnutCoefficient<span class="type-signature type number">number</span>
{:#members:series-doughnutcoefficient}




Sets the radius of the hole on the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.4




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{doughnutCoefficient : 0.5 }]                   
});
</script> {% endhighlight %}




### series.doughnutSize<span class="type-signature type number">number</span>
{:#members:series-doughnutsize}




Sets the radius of the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{doughnutSize : 0.6 }]                   
});
</script> {% endhighlight %}




### series.drawType<span class="type-signature type boolean">boolean</span>
{:#members:series-drawtype}




Specifies the type of series that can be drawn in a Radar or Polar series. It supports line, column and area type. See <a href="global.html#DrawType">DrawType</a>


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{drawType : false }]                   
});
</script> {% endhighlight %}




### series.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:series-enableanimation}




Specifies the animation of the series. ejChart supports animation for the series. This can be enable/disable by this property


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{enableAnimation : false }]                   
});
</script> {% endhighlight %}




### series.enableSmartLabels<span class="type-signature type number">number</span>
{:#members:series-enablesmartlabels}




Enabling this property can avoid pie series data label overlap each other.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{enableSmartLabels : false }]                   
});
</script> {% endhighlight %}




### series.endAngle<span class="type-signature type number">number</span>
{:#members:series-endangle}




Specifies the ending angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{endAngle: 270 }]                   
});
</script> {% endhighlight %}




### series.explode<span class="type-signature type boolean">boolean</span>
{:#members:series-explode}




Explodes the pie slices on mouse move. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{explode: true }]                   
});
</script> {% endhighlight %}




### series.explodeAll<span class="type-signature type boolean">boolean</span>
{:#members:series-explodeall}




Explodes all the pie slices. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{explodeAll: true }]                   
});
</script> {% endhighlight %}




### series.explodeIndex<span class="type-signature type number">number</span>
{:#members:series-explodeindex}




Index of a slice to be exploded from the whole pie. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{explodeIndex : 2 }]                   
});
</script> {% endhighlight %}




### series.explodeOffset<span class="type-signature type number">number</span>
{:#members:series-explodeoffset}




Represents the distance the slice has to be moved out when it is exploded.


Default Value:
{:.param}



* 25




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{explodeOffset : 20 }]                   
});
</script> {% endhighlight %}




### series.fill<span class="type-signature type string">string</span>
{:#members:series-fill}




Specifies the fill color of series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{fill : "green"}]                 
});
</script>{% endhighlight %}




### series.font<span class="type-signature type object">object</span>
{:#members:series-font}




Specifies the font that is common to all series. These are the properties involved in customizing the font of the series in chart.






### series.font.color<span class="type-signature type string">string</span>
{:#members:series-font-color}




Specifies the color, that is common to all series. Text in the series, render with the specified font color.


Default Value:
{:.param}



* "#707070"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{font :{color : "green"}}]                 
});
</script>{% endhighlight %}




### series.font.fontFamily<span class="type-signature type string">string</span>
{:#members:series-font-fontfamily}




Specifies the fontFamily, that is common to all series. Text in the series, render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{ font : { fontFamily : "Algerian"}}]                 
});
</script> {% endhighlight %}




### series.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:series-font-fontstyle}




Specifies the fontStyle, that is common to all series. Text in the series, render with the specified font style.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{font :{fontStyle : "italic"}} ]                
});
</script>{% endhighlight %}




### series.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:series-font-fontweight}




Specifies the fontWeight, that is common to all series. Text in the series, render with the specified font weight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{font :{fontWeight : "lighter"}}]                 
});
</script>{% endhighlight %}




### series.font.opacity<span class="type-signature type number">number</span>
{:#members:series-font-opacity}




Specifies the opacity, that is common to all series. Text in the series, render with the specified font opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{font :{opacity : 0.5}}]                 
});
</script>{% endhighlight %}




### series.font.size<span class="type-signature type string">string</span>
{:#members:series-font-size}




Specifies the font size, that is common to all series. Text in the series, render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{font :{size : "14px"}}]                 
});
</script> {% endhighlight %}




### series.funnelHeight<span class="type-signature type string">string</span>
{:#members:series-funnelheight}




Sets the funnel height.


Default Value:
{:.param}



* "32.7%"(32.7% of actualheight)




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{funnelHeight : '40%' }]                   
});
</script> {% endhighlight %}




### series.funnelWidth<span class="type-signature type string">string</span>
{:#members:series-funnelwidth}




Sets the funnel width.


Default Value:
{:.param}



* "11.6%"(11.6% of actualwidth)




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{funnelWidth : '40%' }]                   
});
</script> {% endhighlight %}




### series.gapRatio<span class="type-signature type number">number</span>
{:#members:series-gapratio}




Specifies the gap between each slice of a pyramid series in pixels.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{gapRatio : 0.2 }]                   
});
</script> {% endhighlight %}




### series.isClosed<span class="type-signature type boolean">boolean</span>
{:#members:series-isclosed}




Used in Polar and Radar series to specify whether the line/area series has to be rendered in a closed state by joining the start and end point of the series.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{isClosed : false }]                   
});
</script> {% endhighlight %}




### series.isStacking<span class="type-signature type boolean">boolean</span>
{:#members:series-isstacking}




Used in Polar and Radar series to specify whether column type has to be rendered the stacked value of chart.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{isStacking : false }]                   
});
</script> {% endhighlight %}




### series.labelPosition<span class="type-signature type enum">enum</span>
{:#members:series-labelposition}




Specifies the position of the axis labels to render labels either inside or outside of plot area. See <a href="global.html#LabelPosition">LabelPosition</a>


Default Value:
{:.param}



* "inside"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{labelPosition : "outside" }]                   
});
</script> {% endhighlight %}




### series.lineCap<span class="type-signature type enum">enum</span>
{:#members:series-linecap}




Specifies the style to draw the end point of a line like butt, round, square. See <a href="global.html#LineCap">LineCap</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineCap.Butt




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{lineCap : "butt"}]                  
});
</script>{% endhighlight %}




### series.lineJoin<span class="type-signature type enum">enum</span>
{:#members:series-linejoin}




Specifies the shape to use at the intersection of two lines drawn. See <a href="global.html#LineJoin">LineJoin</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineJoin.Round




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{lineJoin : "round"}]                  
});
</script> {% endhighlight %}




### series.marker<span class="type-signature type object">object</span>
{:#members:series-marker}




Contains the customizing properties to add marker symbols to the points plotted in the chart.






### series.marker.border<span class="type-signature type object">object</span>
{:#members:series-marker-border}




Options for customizing the color, opacity and width of the border of marker.






### series.marker.border.color<span class="type-signature type string">string</span>
{:#members:series-marker-border-color}




Specifies the border color of marker.


Default Value:
{:.param}



* "white"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{color : "green"}]                  
});
</script> {% endhighlight %}




### series.marker.border.width<span class="type-signature type number">number</span>
{:#members:series-marker-border-width}




Specifies the width of the marker


Default Value:
{:.param}



* 3




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{border :{width : 2}}}]                  
});
</script>{% endhighlight %}




### series.marker.dataLabel<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel}




Contains the customizing properties to add data labels of the points plotted in the chart.






### series.marker.dataLabel.angle<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-angle}




Specifies the rotation angle of dataLabel in the marker. The user can change the rotation angle of dataLabel by applying this property.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{angle : 90}}]                  
});
</script> {% endhighlight %}




### series.marker.dataLabel.border<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel-border}




Options for customizing the color, opacity and width of the border of datalabel.






### series.marker.dataLabel.border.color<span class="type-signature type string">string</span>
{:#members:series-marker-datalabel-border-color}




Specifies the border color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{border : {color : "green"}}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.border.width<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-border-width}




Specifies the border width of dataLabel.


Default Value:
{:.param}



* 0.1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{border :{ width :2 }}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.connectorLine<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel-connectorline}




Contains the options to customize the line connecting the point and the data label.






### series.marker.dataLabel.connectorLine.type<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-connectorline-type}




Specifies whether to connect the point and data label using bezier curve or straight line. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ type : "spline" }}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.connectorLine.width<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-connectorline-width}




Specifies the width of the connector line.


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ width : 2 }}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.fill<span class="type-signature type string">string</span>
{:#members:series-marker-datalabel-fill}




Specifies the fill color of dataLabel.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{fill : "green"}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.font<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel-font}




Specifies the font of the dataLabel. These are the properties involved in customizing the data label font.






### series.marker.dataLabel.font.fontFamily<span class="type-signature type string">string</span>
{:#members:series-marker-datalabel-font-fontfamily}




Specifies the fontFamily of dataLabel. Text in the data label render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-font-fontstyle}




Specifies the fontStyle of dataLabel. Text in the data label render with the specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-font-fontweight}




Specifies the fontWeight of dataLabel. Text in the data label render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.font.opacity<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-font-opacity}




Specifies the opacity of the text in dataLabel. Text in the data label render with the specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ opacity : 0.5 }}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.font.size<span class="type-signature type string">string</span>
{:#members:series-marker-datalabel-font-size}




Specifies the font size of dataLabel. Text in the data label render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { size : "14px" }}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.horizontalTextAlignment<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-horizontaltextalignment}




This property is used to change the alignment of the data label horizontally.


Default Value:
{:.param}



* ej.datavisualization.Chart.horizontalTextAlignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{horizontalTextAlignment : "far"}}}]                  
});
</script>{% endhighlight %}




### series.marker.dataLabel.margin<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel-margin}




Specifies the margin for the data label.






### series.marker.dataLabel.margin.bottom<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-margin-bottom}




Specifies the bottom margin value in dataLabel. By specifying this property, we can adjust the text in data label to bottom.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ bottom :10 }}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.margin.left<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-margin-left}




Specifies the left margin value in dataLabel. By specifying this property, we can adjust the text in data label to left.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ left : 10}}}}]                 
});
</script> {% endhighlight %}




### series.marker.dataLabel.margin.right<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-margin-right}




Specifies the right margin value in dataLabel. By specifying this property, we can adjust the text in data label to right.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ right :10 }}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.margin.top<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-margin-top}




Specifies the top margin value in dataLabel. By specifying this property, we can adjust the text in data label to top.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ top :10 } }}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.opacity<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-opacity}




Specifies the opacity of dataLabel.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{opacity : 0.5}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.shape<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-shape}




Specifies the rendering shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{shape : "circle"}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.textPosition<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-textposition}




This property is used to change the position of the text in data label. See <a href="global.html#TextPosition">TextPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.textPosition.Top




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{textPosition : "bottom"}}}]                 
});
</script>{% endhighlight %}




### series.marker.dataLabel.verticalTextAlignment<span class="type-signature type enum">enum</span>
{:#members:series-marker-datalabel-verticaltextalignment}




This property is used to change the alignment of the data label vertically.


Default Value:
{:.param}



* ej.datavisualization.Chart.verticalTextAlignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{verticalTextAlignment : "far"}}}]                  
});
</script>{% endhighlight %}




### series.marker.dataLabel.visible<span class="type-signature type boolean">boolean</span>
{:#members:series-marker-datalabel-visible}




Specifies the visibility of dataLabel in the marker. The user can change the visibility of dataLabel by applying this property.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{dataLabel :{visible : true}}]                  
});
</script> {% endhighlight %}




### series.marker.fill<span class="type-signature type string">string</span>
{:#members:series-marker-fill}




Specifies the fill color of the marker.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker : { fill : "green" } }]                  
});
</script>{% endhighlight %}




### series.marker.imageUrl<span class="type-signature type string">string</span>
{:#members:series-marker-imageurl}




Specifies the image url location of the marker.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{ imageUrl: "../images/sample.png"}}]                  
});
</script>{% endhighlight %}




### series.marker.opacity<span class="type-signature type number">number</span>
{:#members:series-marker-opacity}




Specifies the opacity of the marker. Values ranges from 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{ opacity : 0.5 }}]                  
});
</script>{% endhighlight %}




### series.marker.shape<span class="type-signature type enum">enum</span>
{:#members:series-marker-shape}




Specifies the shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.Circle




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{ shape: "rectangle"}]                  
});
</script>{% endhighlight %}




### series.marker.size<span class="type-signature type object">object</span>
{:#members:series-marker-size}




Specifies the size of the marker.






### series.marker.size.height<span class="type-signature type number">number</span>
{:#members:series-marker-size-height}




Specifies the height of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{size :{height : 5}}}]                 
});
</script>{% endhighlight %}




### series.marker.size.width<span class="type-signature type number">number</span>
{:#members:series-marker-size-width}




Specifies the width of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{ size :{ width : 2 } } }]                  
});
</script>{% endhighlight %}




### series.marker.visible<span class="type-signature type boolean">boolean</span>
{:#members:series-marker-visible}




Toggles the visibility of the marker.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{marker :{ visible : true}}]                  
});
</script> {% endhighlight %}




### series.opacity<span class="type-signature type number">number</span>
{:#members:series-opacity}




Specifies the opacity of series. Series render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series :[{opacity : 0.5}]                  
});
</script> {% endhighlight %}




### series.pieCoefficient<span class="type-signature type number">number</span>
{:#members:series-piecoefficient}




Sets the radius of the pie series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{pieCoefficient : 0.6 }]                   
});
</script> {% endhighlight %}




### series.points<span class="type-signature type array">array</span>
{:#members:series-points}




Specifies the points of the series. This is to specify the point values for the series


Default Value:
{:.param}



* [ ]




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{points : [{x : 2000, y : 15}] }]                   
});
</script> {% endhighlight %}




### series.pyramidMode<span class="type-signature type enum">enum</span>
{:#members:series-pyramidmode}




Sets the rendering mode of the pyramid as linear or surface.


Default Value:
{:.param}



* "linear"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{pyramidMode : "linear" }]                   
});
</script> {% endhighlight %}




### series.query<span class="type-signature type object">object</span>
{:#members:series-query}




Specifies the query for dataSource in series. This is used to take the query from dataSource


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
var query =  ej.Query().from("Orders").take(10);
$("#container").ejChart({
series : [{query: query }]                   
});
</script> {% endhighlight %}




### series.startAngle<span class="type-signature type number">number</span>
{:#members:series-startangle}




Specifies the starting angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{startAngle: 140 }]                   
});
</script> {% endhighlight %}




### series.tooltip<span class="type-signature type object">object</span>
{:#members:series-tooltip}




Contains all the properties to customize tooltip






### series.tooltip.border<span class="type-signature type object">object</span>
{:#members:series-tooltip-border}




Options for customizing the color, opacity and width of the border of tooltip.






### series.tooltip.border.color<span class="type-signature type string">string</span>
{:#members:series-tooltip-border-color}




Specifies the color of tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : {border : { color :"green"} }]                   
});
</script> {% endhighlight %}




### series.tooltip.border.width<span class="type-signature type number">number</span>
{:#members:series-tooltip-border-width}




Specifies the width of tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : {border : { width :2} }]                   
});
</script> {% endhighlight %}




### series.tooltip.duration<span class="type-signature type string">string</span>
{:#members:series-tooltip-duration}




Specifies the duration of the tooltip to stay awake.


Default Value:
{:.param}



* "500ms"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : { duration: "300ms" }]                   
});
</script> {% endhighlight %}




### series.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:series-tooltip-enableanimation}




Enabling this property animates the tooltip on moving the cursor from one point to the other.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : { enableAnimation: false }]                   
});
</script> {% endhighlight %}




### series.tooltip.fill<span class="type-signature type string">string</span>
{:#members:series-tooltip-fill}




Specifies the fill color of the tooltip.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : {fill : "green"} }]                   
});
</script> {% endhighlight %}




### series.tooltip.format<span class="type-signature type string">string</span>
{:#members:series-tooltip-format}




Formatting the values of point on a tooltip can be customized using this property.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : {format : "#point.x# : #point.y#"} }]                   
});
</script> {% endhighlight %}




### series.tooltip.opacity<span class="type-signature type number">number</span>
{:#members:series-tooltip-opacity}




Specifies the opacity of the tooltip. Values ranges from 0 to 1.


Default Value:
{:.param}



* 0.95




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : { opacity: 0.5 }]                   
});
</script> {% endhighlight %}




### series.tooltip.template<span class="type-signature type string">string</span>
{:#members:series-tooltip-template}




Specify the template for tooltip


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{ tooltip: { template : "item" }}]                  
});
</script>  {% endhighlight %}




### series.tooltip.visible<span class="type-signature type boolean">boolean</span>
{:#members:series-tooltip-visible}




tooltip visibility can be toggled using this property


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{tooltip : {visible : true} }]                   
});
</script> {% endhighlight %}




### series.type<span class="type-signature type enum">enum</span>
{:#members:series-type}




Specifies the type of series to be rendered in chart. see <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* "line"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{type : "column" }]                   
});
</script> {% endhighlight %}




### series.visibility<span class="type-signature type string">string</span>
{:#members:series-visibility}




Specifies the visibility for series. This is used to change the visibility of series


Default Value:
{:.param}



* "visible"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{visibility: "hidden" }]                   
});
</script> {% endhighlight %}




### series.xAxisName<span class="type-signature type string">string</span>
{:#members:series-xaxisname}




Specifies the XAxisName for series. This is used to specify the name of the xAxis


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{xAxisName: "xAxis" }]                   
});
</script> {% endhighlight %}




### series.xName<span class="type-signature type string">string</span>
{:#members:series-xname}




Specifies the xName for dataSource in series. This is used to take the x values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{xName: "XValue" }]                   
});
</script> {% endhighlight %}




### series.yAxisName<span class="type-signature type string">string</span>
{:#members:series-yaxisname}




Specifies the yAxisName for series. This is used to specify the name of the yAxis


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{yAxisName: "yAxis" }]                   
});
</script> {% endhighlight %}




### series.yName<span class="type-signature type string">string</span>
{:#members:series-yname}




Specifies the yName for dataSource in series. This is used to take the y values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
series : [{yName: "YValue" }]                   
});
</script> {% endhighlight %}




### sideBySideSeriesPlacement<span class="type-signature type boolean">boolean</span>
{:#members:sidebysideseriesplacement}




The sideBySideSeriesPlacement property defines the appearance of the different set of data on 3D chart


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
sideBySideSeriesPlacement : true             
});
</script>{% endhighlight %}




### theme<span class="type-signature type enum">enum</span>
{:#members:theme}




By specifying this property the user can change the theme of the chart. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Theme.Flatlight




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
theme : "flatdark"            
});
</script>{% endhighlight %}




### tilt<span class="type-signature type number">number</span>
{:#members:tilt}




The tilt property defines the angle of the slope of 3D chart.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
tilt : 5             
});
</script>{% endhighlight %}




### title<span class="type-signature type object">object</span>
{:#members:title}




Specifies the chart title. This title property denotes the title of the chart.






### title.font<span class="type-signature type object">object</span>
{:#members:title-font}




Specifies the chart title. These are the font properties involved in chart title customization.






### title.font.fontFamily<span class="type-signature type string">string</span>
{:#members:title-font-fontfamily}




Specifies the title fontfamily of primaryXAxis. Chart title render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { font : { fontFamily : "Algerian" } }                     
});
</script> {% endhighlight %}




### title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:title-font-fontstyle}




Specifies the title fontStyle of primaryXAxis. Chart title render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { font : { fontStyle : "italic" } }                     
});
</script> {% endhighlight %}




### title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:title-font-fontweight}




Specifies the title fontWeight. Chart title render with this specified fontWeight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { font : { fontWeight : "lighter" } }                     
});
</script> {% endhighlight %}




### title.font.opacity<span class="type-signature type number">number</span>
{:#members:title-font-opacity}




Specifies the title opacity. Chart title render with this specified font opacity.


Default Value:
{:.param}



* 0.5




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { font : { opacity : 0.8 } }                     
});
</script> {% endhighlight %}




### title.font.size<span class="type-signature type string">string</span>
{:#members:title-font-size}




Specifies the title size. Chart title render with this specified font size.


Default Value:
{:.param}



* "20px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { font : { size : "22px" } }                     
});
</script> {% endhighlight %}




### title.subTitle<span class="type-signature type object">object</span>
{:#members:title-subtitle}




Specifies the options to customize the chart subtitle.






### title.subTitle.font<span class="type-signature type object">object</span>
{:#members:title-subtitle-font}




Specifies the font options for customizing the subtitle.






### title.subTitle.font.fontFamily<span class="type-signature type string">string</span>
{:#members:title-subtitle-font-fontfamily}




Specifies the font family of subtitle.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: {subTitle : {font :{ fontFamily : "Algerian" } } }                      
});
</script> {% endhighlight %}




### title.subTitle.font.fontStyle<span class="type-signature type enum">enum</span>
{:#members:title-subtitle-font-fontstyle}




Specifies the font style of subtitle.


Default Value:
{:.param}



* "Normal"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle : {font :{ fontStyle : "Normal" } } }                     
});
</script> {% endhighlight %}




### title.subTitle.font.fontWeight<span class="type-signature type enum">enum</span>
{:#members:title-subtitle-font-fontweight}




Specifies the font weight of subtitle.


Default Value:
{:.param}



* "regular"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle : {font :{ fontWeight : "regular" } } }                     
});
</script> {% endhighlight %}




### title.subTitle.font.opacity<span class="type-signature type double">double</span>
{:#members:title-subtitle-font-opacity}




Specifies the font opacity of subtitle.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle : {font :{ opacity : 0.5 } } }                     
});
</script> {% endhighlight %}




### title.subTitle.font.size<span class="type-signature type enum">enum</span>
{:#members:title-subtitle-font-size}




Specifies the font size of subtitle.


Default Value:
{:.param}



* "12px"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle : {font :{ size : "14px" } } }                     
});
</script> {% endhighlight %}




### title.subTitle.text<span class="type-signature type string">string</span>
{:#members:title-subtitle-text}




Specifies the text to be displayed as subtitle.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle: { text : "Performace chart" } }                      
});
</script> {% endhighlight %}




### title.subTitle.textAlignment<span class="type-signature type enum">enum</span>
{:#members:title-subtitle-textalignment}




Specifies the text alignment for subtitle text.


Default Value:
{:.param}



* "far"




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title: { subTitle: { textAlignment : "near" } }                      
});
</script> {% endhighlight %}




### title.text<span class="type-signature type string">string</span>
{:#members:title-text}




Specifies the text of the chart title. The text which is to be render as chart title is set here.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { text : "Power Production"}                     
});
</script> {% endhighlight %}




### title.textAlignment<span class="type-signature type enum">enum</span>
{:#members:title-textalignment}




This property is used to change the alignment of the title horizontally. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.TextAlignment.Center




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
title : { textAlignment : "near"}                     
});
</script> {% endhighlight %}




### wallSize<span class="type-signature type number">number</span>
{:#members:wallsize}




In 3D, Cartesian axes lines are represented as wall. The property wallSize defines the width of the wall.


Default Value:
{:.param}



* 2




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
wallSize : 5             
});
</script>{% endhighlight %}




### zooming<span class="type-signature type object">object</span>
{:#members:zooming}




Contains property to customize zooming in chart.






### zooming.enable<span class="type-signature type boolean">boolean</span>
{:#members:zooming-enable}




Enabling this property will allow zooming for chart plot area.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
zooming :{enable :true}          
});
</script>{% endhighlight %}




### zooming.enableDeferredZoom<span class="type-signature type boolean">boolean</span>
{:#members:zooming-enabledeferredzoom}




Enabling this property will allow user to pan the zoomed chart on mouse up.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
zooming:{enableDeferredZoom : true}            
});
</script> {% endhighlight %}




### zooming.enableMouseWheel<span class="type-signature type boolean">boolean</span>
{:#members:zooming-enablemousewheel}




Enabling this property will allow user to zoom plot are on rolling mouse wheel.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
zooming:{enableMouseWheel : true}            
});
</script> {% endhighlight %}




### zooming.type<span class="type-signature type string">string</span>
{:#members:zooming-type}




Specifies whether zooming has to be vertical or horizontal.


Default Value:
{:.param}



* 'x,y'




Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
zooming :{type : "y"}            
});
</script> {% endhighlight %}



## Methods




### exportChart<span class="signature">()</span>
{:#methods:exportchart}




export the chart widget



Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Export Chart
var canvas = $("#container").ejChart("exportChart"); 
var dt = canvas.toDataURL();
this.href = dt;
</script>{% endhighlight %}




### redraw<span class="signature">()</span>
{:#methods:redraw}




redraw the chart widget



Example
{:.example}


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Redraw Chart
var chartObj = $("#container").data("ejChart");
chartObj.redraw(); // redraw the chart
</script>{% endhighlight %}


{% highlight html %}
 
<div id="container"></div> 
 
<script>
$("#container").ejChart("redraw");      
</script>{% endhighlight %}



## Events




### animationComplete
{:#events:animationcomplete}




Fires on completion of animation.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//animationComplete event for chart
$("#container").ejChart({
   animationComplete: function (args) {}
});{% endhighlight %}




### axesLabelRendering
{:#events:axeslabelrendering}




Fires on rendering the axis labels.

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
argument.Axis{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.Label{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart for processing of labels</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//axesLabelRendering event for chart
$("#container").ejChart({
   axesLabelRendering: function (args) {}
});{% endhighlight %}




### axesLabelsInitialize
{:#events:axeslabelsinitialize}




Fires on initializing the axis labels.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//axesLabelsInitialize event for chart
$("#container").ejChart({
   axesLabelsInitialize: function (args) {}
});{% endhighlight %}




### axesRangeCalculate
{:#events:axesrangecalculate}




Fires on axes range calculation.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//axesRangeCalculate event for chart
$("#container").ejChart({
   axesRangeCalculate: function (args) {}
});{% endhighlight %}




### axesTitleRendering
{:#events:axestitlerendering}




Fires on rendering the axes title.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//axesTitleRendering event for chart
$("#container").ejChart({
   axesTitleRendering: function (args) {}
});{% endhighlight %}




### chartAreaBoundsCalculate
{:#events:chartareaboundscalculate}




Fires on chart area bounds calculation.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//chartAreaBoundsCalculate event for chart
$("#container").ejChart({
   chartAreaBoundsCalculate: function (args) {}
});{% endhighlight %}




### create
{:#events:create}




Fires after chart is created.



Example
{:.example}


{% highlight html %}
 
//create event for chart
$("#container").ejChart("create");{% endhighlight %}




### destroy
{:#events:destroy}




Fires when chart is destroyed completely.



Example
{:.example}


{% highlight html %}
 
//animationComplete event for chart
$("#container").ejChart("destroy");{% endhighlight %}




### displayTextRendering
{:#events:displaytextrendering}




Fires on rendering the display text.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//displayTextRendering event for chart
$("#container").ejChart({
   displayTextRendering: function (args) {}
});{% endhighlight %}




### legendBoundsCalculate
{:#events:legendboundscalculate}




Fires on calculating the legend bounds

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//legendBoundsCalculate event for chart
$("#container").ejChart({
   legendBoundsCalculate: function (args) {}
});{% endhighlight %}




### legendItemClick
{:#events:legenditemclick}




Fires on click of legend item

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//legendItemClick event for chart
$("#container").ejChart({
   legendItemClick: function (args) {}
});{% endhighlight %}




### legendItemMouseMove
{:#events:legenditemmousemove}




Fires on mouse move over legend item.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//legendItemMouseMove event for chart
$("#container").ejChart({
   legendItemMouseMove: function (args) {}
});{% endhighlight %}




### legendItemRendering
{:#events:legenditemrendering}




Fires on rendering of legend item.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//legendItemRendering event for chart
$("#container").ejChart({
   legendItemRendering: function (args) {}
});{% endhighlight %}




### load
{:#events:load}




Fires on load of chart.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//load event for chart
$("#container").ejChart({
   load: function (args) {}
});{% endhighlight %}




### pointRegionClick
{:#events:pointregionclick}




Fires on click of point region.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//pointRegionClick event for chart
$("#container").ejChart({
   pointRegionClick: function (args) {}
});{% endhighlight %}




### pointRegionMouseMove
{:#events:pointregionmousemove}




Fires on mousemove over the point region.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//pointRegionMouseMove event for chart
$("#container").ejChart({
   pointRegionMouseMove: function (args) {}
});{% endhighlight %}




### preRender
{:#events:prerender}




Fires on pre render.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//preRender event for chart
$("#container").ejChart({
   preRender: function (args) {}
});{% endhighlight %}




### seriesRendering
{:#events:seriesrendering}




Fires on rendering the series.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//seriesRendering event for chart
$("#container").ejChart({
   seriesRendering: function (args) {}
});{% endhighlight %}




### symbolRendering
{:#events:symbolrendering}




Fires on rendering the symbols.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//symbolRendering event for chart
$("#container").ejChart({
   symbolRendering: function (args) {}
});{% endhighlight %}




### titleRendering
{:#events:titlerendering}




Fires on rendering the title.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//titleRendering event for chart
$("#container").ejChart({
   titleRendering: function (args) {}
});{% endhighlight %}




### toolTipInitialize
{:#events:tooltipinitialize}




Fires on initialize the tooltip.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//toolTipInitialize event for chart
$("#container").ejChart({
   toolTipInitialize: function (args) {}
});{% endhighlight %}




### trackAxisToolTip
{:#events:trackaxistooltip}




Fires on track the axis tooltip.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//trackAxisToolTip event for chart
$("#container").ejChart({
   trackAxisToolTip: function (args) {}
});{% endhighlight %}




### trackToolTip
{:#events:tracktooltip}




Fires on tracking the tooltip.

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
argument.Data{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//trackToolTip event for chart
$("#container").ejChart({
   trackToolTip: function (args) {}
});{% endhighlight %}



