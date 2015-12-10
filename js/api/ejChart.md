---
layout: post
title: API reference for ejChart
description: What are the options, methods and events available in Essential JavaScript Chart.
documentation: API
platform: js
keywords: ejChart, API, Essential JS Chart, Chart
metaname: 
metacontent: 
---

# ejChart

Essential chart can be easily configured to the DOM element, such as div. You can create a Chart with highly customizable look and feel.


#### Syntax

{% highlight js %}

$(element).ejChart();

{% endhighlight %}


#### Example


{% highlight html %}
 
<div id="container"></div> 
 
<script>
// Create Chart
$('#container').ejChart();      
</script>

{% endhighlight %}




#### Requires

* module:jQuery.js

* module:ej.core.js

* module:ej.data.js

* module:ej.chart.js

* module:jQuery.globalize.js


## Members




### annotations `array`
{:#members:annotations}




Options for adding and customizing annotations in Chart.






### annotations.angle `number`
{:#members:annotations-angle}




Angle to rotate the annotation in degrees.


#### Default Value

* '0'




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ angle : 45}]                    

});


{% endhighlight %}


Try it: [Annotation angle](http://jsplayground.syncfusion.com/rgl4uwkj)




### annotations.content `string`
{:#members:annotations-content}




Text content or id of a HTML element to be displayed as annotation.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ content :"Template"}]
                       
});


{% endhighlight %}


Try it: [Annotation Content](http://jsplayground.syncfusion.com/plihjtm3)




### annotations.coordinateUnit `enum`
{:#members:annotations-coordinateunit}




Specifies how annotations have to be placed in Chart.


#### Default Value

* "none". See <a href="global.html#members:coordinateunit">CoordinateUnit</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ coordinateUnit :"pixels"}]
                    
});

{% endhighlight %}




### annotations.horizontalAlignment `enum`
{:#members:annotations-horizontalalignment}




Specifies the horizontal alignment of the annotation.


#### Default Value

* "middle". See <a href="global.html#members:horizontalalignment">HorizontalAlignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ horizontalAlignment :"left"}]
                    
});

{% endhighlight %}


Try it: [Horizontal Alignment](http://jsplayground.syncfusion.com/n5zfhoir)




### annotations.margin `object`
{:#members:annotations-margin}




Options to customize the margin of annotation.


Try it: [Margin](http://jsplayground.syncfusion.com/n5zfhoir)






### annotations.margin.bottom `number`
{:#members:annotations-margin-bottom}




Annotation is placed at the specified value above its original position.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ margin :{ bottom:10}}]                    

});

{% endhighlight %}




### annotations.margin.left `number`
{:#members:annotations-margin-left}




Annotation is placed at the specified value from left side of its original position.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ margin :{ left:10}}]                    

});

{% endhighlight %}




### annotations.margin.right `number`
{:#members:annotations-margin-right}




Annotation is placed at the specified value from the right side of its original position.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ margin :{ right:10}}]                    

});

{% endhighlight %}




### annotations.margin.top `number`
{:#members:annotations-margin-top}




Annotation is placed at the specified value under its original position.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ margin :{ top:10}}]                    

});

{% endhighlight %}




### annotations.opacity `number`
{:#members:annotations-opacity}




Controls the opacity of the annotation.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ opacity : 0.5}]                    

});

{% endhighlight %}


Try it: [Annotation Opacity](http://jsplayground.syncfusion.com/rgl4uwkj)




### annotations.region `enum`
{:#members:annotations-region}




Specifies whether annotation has to be placed with respect to chart or series.


#### Default Value

* "chart". See <a href="global.html#members:region">Region</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ region :"series"}]                    

});

{% endhighlight %}


Try it: [Annotation Region](http://jsplayground.syncfusion.com/yfxghhut)




### annotations.verticalAlignment `enum`
{:#members:annotations-verticalalignment}




Specifies the vertical alignment of the annotation.


#### Default Value

* "middle". See <a href="global.html#members:verticalalignment">VerticalAlignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ verticalAlignment :"top"}]                    

});

{% endhighlight %}


Try it: [Vertical Alignment](http://jsplayground.syncfusion.com/frjpm2um)




### annotations.visible `boolean`
{:#members:annotations-visible}




Controls the visibility of the annotation.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ visible :true}]                    

});

{% endhighlight %}


Try it: [Annotation Visibility](http://jsplayground.syncfusion.com/plihjtm3)




### annotations.x `number`
{:#members:annotations-x}




Represents the horizontal offset when coordinateUnit is pixels. 
when coordinateUnit is points, it represents the x-coordinate of axis bounded with xAxisName property or primary X axis when xAxisName is not provided. 
This property is not applicable when coordinateUnit is none.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ x : 100}]                    

});

{% endhighlight %}


Try it: [Annotation Positioning](http://jsplayground.syncfusion.com/frjpm2um)




### annotations.xAxisName `string`
{:#members:annotations-xaxisname}




Name of the horizontal axis to be used for positioning the annotation. This property is applicable only when coordinateUnit is points.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ xAxisName : "xAxis1"}]                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/h23k4jcy)




### annotations.y `number`
{:#members:annotations-y}




Represents the vertical offset when coordinateUnit is pixels. 
When coordinateUnit is points, it represents the y-coordinate of axis bounded with yAxisName property or primary Y axis when yAxisName is not provided. 
This property is not applicable when coordinateUnit is none.


#### Default Value

* 0




#### Example


{% highlight js %}
 

$("#container").ejChart({
annotations :[{ y : 100}]                    
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/1nq2ss4v)




### annotations.yAxisName `string`
{:#members:annotations-yaxisname}




Name of the vertical axis to be used for positioning the annotation. 
This property is applicable only when coordinateUnit is points.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   annotations :[{ yAxisName : "yAxis1"}]                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2nqhtn0y)




### backGroundImageUrl `string`
{:#members:backgroundimageurl}




Url of the image to be used as chart background.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   backGroundImageUrl: "../images/chart/wheat.png"                      

});

{% endhighlight %}


Try it: [JS playground Sample](http://jsplayground.syncfusion.com/i1bys43l)




### border `object`
{:#members:border}




Options for customizing the color, opacity and width of the chart border.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wxxv2rq1)





### border.color `string`
{:#members:border-color}




Border color of the chart.


#### Default Value

* null




#### Example


{% highlight js %}
                             
$("#container").ejChart({

   border: { color: "green" }                      

});

{% endhighlight %}




### border.opacity `number`
{:#members:border-opacity}




Opacity of the chart border.


#### Default Value

* 0.3




#### Example


{% highlight js %}
 
$("#container").ejChart({

   border: { opacity: 0.5 }                      

});

{% endhighlight %}




### border.width `number`
{:#members:border-width}




Width of the Chart border.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   border: { width: 2 }                      

});

{% endhighlight %}




### canResize `boolean`
{:#members:canresize}




Controls whether Chart has to be responsive or not.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   canResize : true             

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/r12awtp3)




### chartArea `object`
{:#members:chartarea}




Options for configuring the border and background of the plot area.




### chartArea.background `string`
{:#members:chartarea-background}




Background color of the plot area.


#### Default Value



* transparent




#### Example


{% highlight js %}
 
$("#container").ejChart({

     chartArea: { background : "white" }
                          
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/picztz23)


### chartArea.border `object`
{:#members:chartarea-border}




Options for customizing the border of the plot area.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/kzy21bwx)




### chartArea.border.color `string`
{:#members:chartarea-border-color}




Border color of the plot area.


#### Default Value



* Gray




#### Example


{% highlight js %}
 
$("#container").ejChart({

    chartArea: { border: { color :"green"} }
                         
});

{% endhighlight %}


### chartArea.border.opacity `number`
{:#members:chartarea-border-opacity}




Opacity of the plot area border.


#### Default Value



* 0.3




#### Example


{% highlight js %}
 
$("#container").ejChart({

    chartArea: { border: { opacity : 0.5} }
                          
});

{% endhighlight %}


### chartArea.border.width `number`
{:#members:chartarea-border-width}




Border width of the plot area.


#### Default Value



* 0.5




#### Example


{% highlight js %}
 
$("#container").ejChart({

    chartArea: { border: { width : 0.2} }
                          
});

{% endhighlight %}




### columnDefinitions `array`
{:#members:columndefinitions}




Options to split Chart into multiple plotting areas vertically. Each object in the collection represents a plotting area in Chart.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zdfd1sai)




### columnDefinitions.unit `enum`
{:#members:columnDefinitions.unit}




Specifies the unit to measure the width of the column in plotting area.


#### Default Value

* 'pixel'. See <a href="global.html#members:unit">Unit</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

    columnDefinitions :[{unit : "percentage"}]                     

});

{% endhighlight %}




### columnDefinitions.columnWidth `number`
{:#members:columnDefinitions.columnWidth}




Width of the column in plotting area. Width is measured in either pixel or percentage based on the value of unit property.


#### Default Value

* 50




#### Example


{% highlight js %}
 
$("#container").ejChart({

   columnDefinitions :[{ columnWidth : 50 }]                     

});

{% endhighlight %}




### columnDefinitions.lineColor `string`
{:#members:columnDefinitions.lineColor}




Color of the line that indicates the starting point of the column in plotting area.


#### Default Value

* "transparent"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   columnDefinitions :[{ lineColor : "green" }]                     

});

{% endhighlight %}




### columnDefinitions.lineWidth `number`
{:#members:columnDefinitions.lineWidth}




Width of the line that indicates the starting point of the column in plot area.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   columnDefinitions :[{ lineWidth : 2 }]                     

});

{% endhighlight %}




### commonSeriesOptions `object`
{:#members:commonseriesoptions}




Options for configuring the properties of all the series. You can also override the options for specific series by using series collection.






### commonSeriesOptions.border `object`
{:#members:commonseriesoptions-border}




Options to customize the border of all the series.






### commonSeriesOptions.border.color `string`
{:#members:commonseriesoptions-border-color}




Border color of all series.


#### Default Value



* "transparent"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{border :{ color : "green" } }                  
});
{% endhighlight %}




### commonSeriesOptions.border.width `number`
{:#members:commonseriesoptions-border-width}




Border width of all series.


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{border :{ width : 2 } }                  
});
{% endhighlight %}




### commonSeriesOptions.dashArray `string`
{:#members:commonseriesoptions-dasharray}




Pattern of dashes and gaps used to stroke all the line type series.


#### Default Value



 * ""




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{dashArray : "2,3"}                  
});
 {% endhighlight %}




### commonSeriesOptions.dataSource `object`
{:#members:commonseriesoptions-datasource}




Set the dataSource for all series. It can be an array of JSON objects or an instance of ej.DataManager.


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions : {dataSource: data }                   
});

 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ubbu5ukf)




### commonSeriesOptions.doughnutCoefficient `number`
{:#members:commonseriesoptions-doughnutcoefficient}




Controls the size of the hole in doughnut series. Value ranges from 0 to 1


#### Default Value



* 0.4




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ doughnutCoefficient : 0.5}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/15exlbqk)



### commonSeriesOptions.doughnutSize `number`
{:#members:commonseriesoptions-doughnutsize}




Controls the size of the doughnut series. Value ranges from 0 to 1.


#### Default Value



* 0.8




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ doughnutSize : 0.9}                  
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ywbzcwhh)



### commonSeriesOptions.drawType `enum`
{:#members:commonseriesoptions-drawtype}




Specifies the type of series to be drawn in radar or polar series. 


#### Default Value



* "line". See <a href="global.html#members:drawtype">DrawType</a>

#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{ drawType : "area"}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/woedp3qa)



### commonSeriesOptions.enableAnimation `boolean`
{:#members:commonseriesoptions-enableanimation}




Enable/disable the animation for all the series.


#### Default Value



* true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ enableAnimation : false}                  
});
 {% endhighlight %}




### commonSeriesOptions.enableSmartLabels `boolean'
{:#members:commonseriesoptions-enablesmartlabels}




To avoid overlapping of data labels smartly. 


#### Default Value



* true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ enableSmartLabels : false}                  
});
  {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ojz1vbr4)



### commonSeriesOptions.endAngle `number`
{:#members:commonseriesoptions-endangle}




Start angle of pie/doughnut series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ endAngle : 270}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/52kkuy5d)


### commonSeriesOptions.explode `boolean`
{:#members:commonseriesoptions-explode}




Explodes the pie/doughnut slices on mouse move.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ explode : true}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/cletijkr)



### commonSeriesOptions.explodeAll `boolean`
{:#members:commonseriesoptions-explodeall}




Explodes all the slice of pie/doughnut on render.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ explodeAll : true}                  
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2btbqicb)



### commonSeriesOptions.explodeIndex `number`
{:#members:commonseriesoptions-explodeindex}




Index of the point to be exploded from pie/doughnut/pyramid/funnel.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ explodeIndex : 2}                  
});
 {% endhighlight %}
 
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/lypx2awm)




### commonSeriesOptions.explodeOffset `number`
{:#members:commonseriesoptions-explodeoffset}




Specifies the distance of the slice from the center, when it is exploded.


#### Default Value



* 0.4




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ explodeOffset : 20}                  
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/t2ysyshe)



### commonSeriesOptions.fill `string`
{:#members:commonseriesoptions-fill}




Fill color for all the series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{fill : "green"}                  
});
{% endhighlight %}



Try it: [JS Playground](http://jsplayground.syncfusion.com/wdgfh0f1)



### commonSeriesOptions.font `object`
{:#members:commonseriesoptions-font}




Options for customizing the font of all the series.






### commonSeriesOptions.font.color `string`
{:#members:commonseriesoptions-font-color}




Font color of the text in all series.


#### Default Value



* "#707070"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{font :{color : "green"}}                 
});
{% endhighlight %}




### commonSeriesOptions.font.fontFamily `string`
{:#members:commonseriesoptions-font-fontfamily}




Font Family for all the series.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{ font : { fontFamily : "Algerian"}}                 
});
 {% endhighlight %}




### commonSeriesOptions.font.fontStyle `enum`
{:#members:commonseriesoptions-font-fontstyle}




Specifies the font Style for all the series.


#### Default Value



* "normal"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions : {font :{fontStyle : "italic"}}                 
});
{% endhighlight %}




### commonSeriesOptions.font.fontWeight `enum`
{:#members:commonseriesoptions-font-fontweight}




Specifies the font weight for all the series.


#### Default Value



* "regular"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{font :{fontWeight : "lighter"}}                 
});
{% endhighlight %}




### commonSeriesOptions.font.opacity `number`
{:#members:commonseriesoptions-font-opacity}




Opacity for text in all the series.


#### Default Value



* 1




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{font :{opacity : 0.5}}                 
});
{% endhighlight %}




### commonSeriesOptions.font.size `string`
{:#members:commonseriesoptions-font-size}




Font size for text in all the series.

#### Default Value



 * "12px"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{font :{size : "14px"}}                 
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gmjlryrg)



### commonSeriesOptions.funnelHeight `string`
{:#members:commonseriesoptions-funnelheight}




Sets the height of the funnel in funnel series. Values can be either pixel or percentage.


#### Default Value



 * "32.7%"




#### Example


{% highlight js %}
 
<div id="container"></div> 
<script>
$("#container").ejChart({
commonSeriesOptions : {funnelHeight : '40%' }                 
});
</script> {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/cnku50hw)




### commonSeriesOptions.funnelWidth `string`
{:#members:commonseriesoptions-funnelwidth}




Sets the width of the funnel in funnel series. Values can be either pixel or percentage.

#### Default Value



 * "11.6%"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions : {funnelWidth : '40%' }                  
});
 {% endhighlight %}
 
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/aj4pwnrm)




### commonSeriesOptions.gapRatio `number`
{:#members:commonseriesoptions-gapratio}




Gap between the slices in pyramid and funnel series.


#### Default Value



 * 0




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ gapRatio : 0.5}                  
});
  {% endhighlight %}
  
  
Try it: [JS Playground](http://jsplayground.syncfusion.com/om3zazbd)




### commonSeriesOptions.isClosed `boolean`
{:#members:commonseriesoptions-isclosed}




Specifies whether to join start and end point of a line/area series used in polar/radar chart to form a closed path.


#### Default Value



 * true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ isClosed : false}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/d41kmmwt)




### commonSeriesOptions.isStacking `boolean`
{:#members:commonseriesoptions-isstacking}




Specifies whether to stack the column series in polar/radar charts.


#### Default Value



 * false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ isStacking : "true"}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/g40hdrpl)




### commonSeriesOptions.isTransposed `boolean`
{:#members:commonseriesoptions-isTransposed}




Renders the chart vertically. This is applicable only for cartesian type series.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {isTransposed : false }                   
});
{% endhighlight %}




### commonSeriesOptions.labelPosition `enum`
{:#members:commonseriesoptions-labelposition}




Position of the data label in pie/doughnut/pyramid/funnel series. OutsideExtended position is not applicable for pyramid/funnel.


#### Default Value



* "inside". See <a href="global.html#members:labelposition">LabelPosition</a>



#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{ labelPosition : "outside"}                  
});
 {% endhighlight %}
 

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/w5q1jt5k)



### commonSeriesOptions.lineCap `enum`
{:#members:commonseriesoptions-linecap}




Specifies the line cap of the series. 


#### Default Value



* "butt". See <a href="global.html#members:linecap">LineCap</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{lineCap : "butt"}                  
});
{% endhighlight %}




### commonSeriesOptions.lineJoin `enum`
{:#members:commonseriesoptions-linejoin}




Specifies the type of shape to be used where two lines meet.


#### Default Value



* "round". See <a href="global.html#members:linejoin">LineJoin</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{lineCap : "round"}                  
});
{% endhighlight %}




### commonSeriesOptions.marker `object`
{:#members:commonseriesoptions-marker}




Options for displaying and customizing marker for individual point in a series. Marker contains shapes and/or data labels.






### commonSeriesOptions.marker.border `object`
{:#members:commonseriesoptions-marker-border}




Options for customizing the border of the marker shape.






### commonSeriesOptions.marker.border.color `string`
{:#members:commonseriesoptions-marker-border-color}




Border color of the marker shape. 


#### Default Value



* "white"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{color : "green"}                  
});
 {% endhighlight %}




### commonSeriesOptions.marker.border.width `number`
{:#members:commonseriesoptions-marker-border-width}




Border width of the marker shape. 


#### Default Value



* 3




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{border :{width : 2}}}                  
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel `object`
{:#members:commonseriesoptions-marker-datalabel}




Options for displaying and customizing data labels.






### commonSeriesOptions.marker.dataLabel.angle `number`
{:#members:commonseriesoptions-marker-datalabel-angle}




Angle of the data label in degrees. Only the text gets rotated, whereas the background and border does not rotate. 


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{angle : 90}}}                  
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rbw3xizf)



### commonSeriesOptions.marker.dataLabel.border `object`
{:#members:commonseriesoptions-marker-datalabel-border}




Options for customizing the border of the data label.






### commonSeriesOptions.marker.dataLabel.border.color `string`
{:#members:commonseriesoptions-marker-datalabel-border-color}




Border color of the data label. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border : {color : "green"}}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.border.width `number`
{:#members:commonseriesoptions-marker-datalabel-border-width}




Border width of the data label. 


#### Default Value



* 0.1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border :{ width :2 }}}}                 
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/f4b4p32r)



### commonSeriesOptions.marker.dataLabel.connectorLine `object`
{:#members:commonseriesoptions-marker-datalabel-connectorline}




Options for displaying and customizing the line that connects point and data label.






### commonSeriesOptions.marker.dataLabel.connectorLine.type `enum`
{:#members:commonseriesoptions-marker-datalabel-connectorline-type}




Specifies when the connector has to be drawn as Bezier curve or straight line. This is applicable only for Pie and Doughnut chart types.


#### Default Value



* "line". See <a href="global.html#connectorlinetype">ConnectorLineType</a>


#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ type : "bezier" }}}}                 
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pmnp5qjl)



### commonSeriesOptions.marker.dataLabel.connectorLine.width `number`
{:#members:commonseriesoptions-marker-datalabel-connectorline-width}




Width of the connector.


#### Default Value



* 0.5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ width : 2 }}}}                 
});
 {% endhighlight %}
 

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pmnp5qjl)


### commonSeriesOptions.marker.dataLabel.fill `string`
{:#members:commonseriesoptions-marker-datalabel-fill}




Background color of the data label. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{fill : "green"}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font `object`
{:#members:commonseriesoptions-marker-datalabel-font}




Options for customizing the data label font.






### commonSeriesOptions.marker.dataLabel.font.fontFamily `string`
{:#members:commonseriesoptions-marker-datalabel-font-fontfamily}




Font family of the data label. 


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.fontStyle `enum`
{:#members:commonseriesoptions-marker-datalabel-font-fontstyle}




Font style of the data label.   


#### Default Value



* "normal". See <a href="global.html#fontstyle">FontStyle</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}                 
});
 {% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.fontWeight `enum`
{:#members:commonseriesoptions-marker-datalabel-font-fontweight}




Font weight of the data label.  


#### Default Value



* "regular". See <a href="global.html#members:fontweight">FontWeight</a>



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.opacity `number`
{:#members:commonseriesoptions-marker-datalabel-font-opacity}




Opacity of the text. 


#### Default Value



 * 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ opacity : 0.5 }}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.font.size `string`
{:#members:commonseriesoptions-marker-datalabel-font-size}




Font size of the data label. 


#### Default Value



* "12px"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { size : "14px" }}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.horizontalTextAlignment `enum`
{:#members:commonseriesoptions-marker-datalabel-horizontaltextalignment}




Horizontal alignment of the data label. 


#### Default Value



* "center"




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{horizontalTextAlignment : "far"}}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/c3i3lxpg)



### commonSeriesOptions.marker.dataLabel.margin `object`
{:#members:commonseriesoptions-marker-datalabel-margin}




Margin of the text to its background shape. The size of the background shape increases based on the margin applied to its text.






### commonSeriesOptions.marker.dataLabel.margin.bottom `number`
{:#members:commonseriesoptions-marker-datalabel-margin-bottom}




Bottom margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ bottom :10 }}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.left `number`
{:#members:commonseriesoptions-marker-datalabel-margin-left}



Left margin of the text. 


#### Default Value



 * 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ left : 10}}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.right `number`
{:#members:commonseriesoptions-marker-datalabel-margin-right}




Right margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ right :10 }}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.margin.top `number`
{:#members:commonseriesoptions-marker-datalabel-margin-top}




Top margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ top :10 } }}}                 
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dff0lfpg)



### commonSeriesOptions.marker.dataLabel.opacity `number`
{:#members:commonseriesoptions-marker-datalabel-opacity}




Opacity of the data label. 


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{opacity : 0.5}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.shape `enum`
{:#members:commonseriesoptions-marker-datalabel-shape}




Background shape of the data label. 


#### Default Value



* "none". See <a href="global.html#members:shape">Shape</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{shape : "circle"}}}                 
});
{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.text `string`
{:#members:commonseriesoptions-marker-datalabel-text}




Name of a field in data source, where datalabel text is displayed.  


#### Default Value



* ""


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonseriesoptions : { marker : { dataLabel : { text : "TextFieldName" }}}                 
});

{% endhighlight %}




### commonSeriesOptions.marker.dataLabel.textPosition `enum`
{:#members:commonseriesoptions-marker-datalabel-textposition}




Specifies the position of the data label. This property can be used only for the series such as column, bar, stacked column, stacked bar, 100% stacked column, 100% stacked bar, candle and OHLC.


#### Default Value



* "top". See <a href="global.html#members:textposition">TextPosition</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{textPosition : "bottom"}}}                 
});
{% endhighlight %}


Try it: [JS Playground  Sample](http://jsplayground.syncfusion.com/tzmb3o0y)



### commonSeriesOptions.marker.dataLabel.verticalTextAlignment `enum`
{:#members:commonseriesoptions-marker-datalabel-verticaltextalignment}




Vertical alignment of the data label. 


#### Default Value



* "center"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{verticalTextAlignment : "far"}}}                  
});
{% endhighlight %}


Try it: [JS Playground  Sample](http://jsplayground.syncfusion.com/zro5pbw2)



### commonSeriesOptions.marker.dataLabel.visible `boolean`
{:#members:commonseriesoptions-marker-datalabel-visible}




Controls the visibility of the data labels. 


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{visible : true}}                  
});
 {% endhighlight %}




### commonSeriesOptions.marker.fill `string`
{:#members:commonseriesoptions-marker-fill}




Color of the marker shape. 


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker : { fill : "green" } }                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wh0gldoo)



### commonSeriesOptions.marker.imageUrl `string`
{:#members:commonseriesoptions-marker-imageurl}




The URL for the Image to be displayed as marker. In order to display image as marker, set series.marker.shape as ‘image’.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{ imageUrl: "../images/sample.png"}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/251niupi)



### commonSeriesOptions.marker.opacity `number`
{:#members:commonseriesoptions-marker-opacity}




Opacity of the marker. 


#### Default Value



 * 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{ opacity : 0.5 }}                  
});
{% endhighlight %}




### commonSeriesOptions.marker.shape `enum`
{:#members:commonseriesoptions-marker-shape}




Specifies the shape of the marker. 


#### Default Value



* "circle". See <a href="global.html#members:shape">Shape</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{ shape: "rectangle"}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wh0gldoo)



### commonSeriesOptions.marker.size `object`
{:#members:commonseriesoptions-marker-size}




Options for customizing the size of the marker shape.






### commonSeriesOptions.marker.size.height `number`
{:#members:commonseriesoptions-marker-size-height}




Height of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{size :{height : 5}}}                  
});
{% endhighlight %}




### commonSeriesOptions.marker.size.width `number`
{:#members:commonseriesoptions-marker-size-width}




Width of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{marker :{ size :{ width : 2 } } }                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fbrqexxu)


### commonSeriesOptions.marker.visible `boolean`
{:#members:commonseriesoptions-marker-visible}




Controls the visibility of the marker shape. 


#### Default Value



* false




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{marker :{ visible : true}}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/f2qfyfbt)



### commonSeriesOptions.opacity `number`
{:#members:commonseriesoptions-opacity}




Opacity of the series.


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{opacity : 0.5}                  
});
 {% endhighlight %}




### commonSeriesOptions.palette `string`
{:#members:commonseriesoptions-palette}




Name of a field in data source, where the fill color for all the data points is generated.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : { palette : "ColorFieldName" }                  
});
{% endhighlight %}




### commonSeriesOptions.pieCoefficient `number`
{:#members:commonseriesoptions-piecoefficient}




Controls the size of pie series. Value ranges from 0 to 1.


#### Default Value



* 0.8




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ pieCoefficient : 1}                  
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yzleny3o)



### commonSeriesOptions.pyramidMode `enum`
{:#members:commonseriesoptions-pyramidmode}




Specifies the mode of the pyramid series. 


#### Default Value



* "linear". See <a href="global.html#members:pyramidmode">PyramidMode</a>

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ pyramidMode : "linear"}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/maeo3b3s)



### commonSeriesOptions.startAngle `number`
{:#members:commonseriesoptions-startangle}




Start angle from where the pie/doughnut series renders. By default it starts from 0.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ startAngle : 150}                  
});
 {% endhighlight %}
 

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gposb4vh)



### commonSeriesOptions.tooltip `object`
{:#members:commonseriesoptions-tooltip}




Options for customizing the tooltip of chart.





### commonSeriesOptions.tooltip.border `object`
{:#members:commonseriesoptions-tooltip-border}




Options for customizing the border of the tooltip.






### commonSeriesOptions.tooltip.border.color `string`
{:#members:commonseriesoptions-tooltip-border-color}




Border color of the tooltip.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border:{ color : "green" }}}                  
});
 {% endhighlight %}




### commonSeriesOptions.tooltip.border.width `number`
{:#members:commonseriesoptions-tooltip-border-width}




Border width of the tooltip.


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border :{ width : 2}}}                  
});
  {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dmvqb51g)


### commonSeriesOptions.tooltip.duration `string`
{:#members:commonseriesoptions-tooltip-duration}




Specifies the duration, the tooltip has to be displayed.


#### Default Value



* "500ms"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{duration : "300ms"}}                  
});
  {% endhighlight %}




### commonSeriesOptions.tooltip.enableAnimation `boolean`
{:#members:commonseriesoptions-tooltip-enableanimation}




Enables/disables the animation of the tooltip when moving from one point to other.


#### Default Value



* true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{enableAnimation : false}}                  
});
{% endhighlight %}




### commonSeriesOptions.tooltip.fill `string`
{:#members:commonseriesoptions-tooltip-fill}




Background color of the tooltip.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{fill : "green"}}                  
});
 {% endhighlight %}




### commonSeriesOptions.tooltip.format `string`
{:#members:commonseriesoptions-tooltip-format}




Format of the tooltip content.


#### Default Value



* "#point.x# : #point.y#"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ tooltip : { format : "#point.x# : #point.y#%" } }                  
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rzxmpi0c)



### commonSeriesOptions.tooltip.opacity `number`
{:#members:commonseriesoptions-tooltip-opacity}




Opacity of the tooltip.


#### Default Value



* 0.5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{tooltip :{opacity : 0.5}}                  
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jih5jejk)



### commonSeriesOptions.tooltip.template `string`
{:#members:commonseriesoptions-tooltip-template}




Custom template to format the tooltip content. Use “point.x” and “point.y” as a placeholder text to display the corresponding data point’s x and y value.


#### Default Value



* null




#### Example


{% highlight js %}
 <div id="item" style="display: none;"> 
    <div>
       <div>#point.x#</div>
        <div>#point.y#</div>
       </div>       
 </div>
 
$("#container").ejChart({
commonSeriesOptions :{ tooltip: { template : "item" }}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rmunfu1b)



### commonSeriesOptions.tooltip.visible `boolean`
{:#members:commonseriesoptions-tooltip-visible}




Controls the visibility of the tooltip.


#### Default Value



* false




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{ tooltip :{visible : true} }                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tpizvdt0)


### commonSeriesOptions.type `enum`
{:#members:commonseriesoptions-type}




Specifies the type of the series to render in chart. 


#### Default Value



* "column". See <a href="global.html#members:type">Type</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ type : "spline"}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/iyglee55)



### commonSeriesOptions.xAxisName `string`
{:#members:commonseriesoptions-xaxisname}




Specifies the name of the x-axis that has to be associated with this series. Add an axis instance with this name to axes collection.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{ xAxisName : "xAxis"}                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/p1t424pc)


### commonSeriesOptions.xName `string`
{:#members:commonseriesoptions-xname}




Name of the property in the datasource that contains x value for the series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {xName: "XValue" }                   
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ubbu5ukf)




### commonSeriesOptions.yAxisName `string`
{:#members:commonseriesoptions-yaxisname}




Specifies the name of the y-axis that has to be associated with this series. Add an axis instance with this name to axes collection.


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
commonSeriesOptions :{ yAxisName : "yAxis"}                  
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/kac2fcth)



### commonSeriesOptions.yName `string`
{:#members:commonseriesoptions-yname}




Name of the property in the datasource that contains y value for the series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{yName: "yValue" }               
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ubbu5ukf)
 
 

 
### commonSeriesOptions.high `string`
{:#members:commonseriesoptions-high}




Name of the property in the datasource that contains high value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {high: "high" }                  
});
{% endhighlight %}




### commonSeriesOptions.low `string`
{:#members:commonseriesoptions-low}




Name of the property in the datasource that contains low value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {low: "low" }                 
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fqxo0isj)



### commonSeriesOptions.open `string`
{:#members:commonseriesoptions-open}




Name of the property in the datasource that contains open value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {open: "oepn" }                   
});
{% endhighlight %}



### commonSeriesOptions.close `string`
{:#members:commonseriesoptions-close}


Name of the property in the datasource that contains close value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : {close: "close" }                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fqxo0isj)


### commonSeriesOptions.size `string`
{:#members:commonseriesoptions-size}




Name of the property in the datasource that contains the size value for the bubble series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions : [{size: "size" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/kf0d05wi)


### commonSeriesOptions.trendlines `array`
{:#members:commonseriesoptions-trendlines}




Option to add the trendlines to chart.




### commonSeriesOptions.trendlines.visibility `boolean`
{:#members:commonseriesoptions-trendlines-visibility}




Show/hides the trendline.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ visibility:'visible' }]}                 
});
{% endhighlight %}





### commonSeriesOptions.trendlines.type `string`
{:#members:commonseriesoptions-trendlines-type}




Specifies the type of the trendline for the series.


#### Default Value



* "linear". See <a href="global.html#members:trendlinestype">TrendlinesType</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ type:'linear' }]}                 
});
{% endhighlight %}



### commonSeriesOptions.trendlines.name `string`
{:#members:commonseriesoptions-trendlines-name}




Name for the trendlines that is to be displayed in the legend text.


#### Default Value



* "trendline"



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ name:'Trendline' }]}                  
});
{% endhighlight %}




### commonSeriesOptions.trendlines.fill `string`
{:#members:commonseriesoptions-trendlines-fill}




Fill color of the trendlines.


#### Default Value



* "#0000FF"



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ fill:'#0000FF' }]}                 
});
{% endhighlight %}




### commonSeriesOptions.trendlines.width `number`
{:#members:commonseriesoptions-trendlines-width}




Width of the trendlines.


#### Default Value



* 1



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ width:1 }]}                
});
{% endhighlight %}



### commonSeriesOptions.trendlines.opacity `number`
{:#members:commonseriesoptions-trendlines-opacity}




Opacity of the trendline.


#### Default Value



* 1



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ opacity:1 }]}                 
});
{% endhighlight %}




### commonSeriesOptions.trendlines.dashArray `string`
{:#members:commonseriesoptions-trendlines-dasharray}




Pattern of dashes and gaps used to stroke the trendline.


#### Default Value



* ""



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ dashArray:"" }]}                 
});
{% endhighlight %}



### commonSeriesOptions.trendlines.forwardForecast `string`
{:#members:commonseriesoptions-trendlines-forwardforecast}




Future trends of the current series.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ forwardForeCast:2 }]}                 
});
{% endhighlight %}



### commonSeriesOptions.trendlines.backwardForecast `string`
{:#members:commonseriesoptions-trendlines-backwardforecast}




Past trends of the current series.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ backwardForeCast:2 }]}                
});
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/d5o0dk1l)



### commonSeriesOptions.trendlines.polynomialOrder `string`
{:#members:commonseriesoptions-trendlines-polynomialorder}




Specifies the order of the polynomial trendlines.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{trendlines:[{ polynomialOrder:2 }]}             
});
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/opxwgddc)



### commonSeriesOptions.highlightSettings `object`
{:#members:commonseriesoptions-highlightsettings}




Options for customizing the appearance of the series or data point while highlighting.




### commonSeriesOptions.highlightSettings.enable `boolean`
{:#members:commonseriesoptions-highlightsettings-enable}




Enables/disables the ability to highlight the series or data point interactively.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{enable:true}}                  
});
{% endhighlight %}



### commonSeriesOptions.highlightSettings.mode `enum`
{:#members:commonseriesoptions-highlightsettings-mode}




Specifies whether the series or data point has to be highlighted.


#### Default Value



* "series". See <a href="global.html#members:mode">Mode</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{mode:"point"}}                  
});
{% endhighlight %}



### commonSeriesOptions.highlightSettings.color `string`
{:#members:commonseriesoptions-highlightsettings-color}




Color of the series/point on highlight.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{color:"red"}}                  
});
{% endhighlight %}



### commonSeriesOptions.highlightSettings.opacity `number`
{:#members:commonseriesoptions-highlightsettings-opacity}




Opacity of the series/point on highlight.


#### Default Value



* 0.6

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{opacity:1}}               
});
{% endhighlight %}



### commonSeriesOptions.highlightSettings.border `object`
{:#members:commonseriesoptions-highlightsettings-border}



Options for customizing the border of series on highlight.



### commonSeriesOptions.highlightSettings.border.color `string`
{:#members:commonseriesoptions-highlightsettings-border-color}



Border color of the series/point on highlight.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{border:{color:"black"}}}                 
});
{% endhighlight %}



### commonSeriesOptions.highlightSettings.border.width `string`
{:#members:commonseriesoptions-highlightsettings-border-width}



Border width of the series/point on highlight.


#### Default Value



* 2

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{border:{width:1}}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rppilz5a)


### commonSeriesOptions.highlightSettings.pattern `string`
{:#members:commonseriesoptions-highlightsettings-pattern}




Specifies the pattern for the series/point on highlight.

#### Default Value



* "none". See <a href="global.html#members:pattern">Pattern</a>

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{pattern:"chessboard"}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/e31yyof2)



### commonSeriesOptions.highlightSettings.customPattern `string`
{:#members:commonseriesoptions-highlightsettings-custompattern}




Custom pattern for the series on highlight.

#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{highlightSettings:{customPattern:""}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ecgabpa5)



### commonSeriesOptions.selectionSettings `object`
{:#members:commonseriesoptions-selectionsettings}




Options for customizing the appearance of the series/data point on selection.



### commonSeriesOptions.selectionSettings.enable `boolean`
{:#members:commonseriesoptions-selectionsettings-enable}




Enables/disables the ability to select a series/data point interactively.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{enable:true}}                  
});
{% endhighlight %}



### commonSeriesOptions.selectionSettings.mode `enum`
{:#members:commonseriesoptions-selectionsettings-mode}




Specifies whether the series or data point has to be selected.


#### Default Value



* "series". See <a href="global.html#members:mode">Mode</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{mode:"point"}}                  
});
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yghrxu21)



### commonSeriesOptions.selectionSettings.color `string`
{:#members:commonseriesoptions-selectionsettings-color}




Color of the series/point on selection.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{color:"red"}}                  
});
{% endhighlight %}



### commonSeriesOptions.selectionSettings.opacity `number`
{:#members:commonseriesoptions-selectionsettings-opacity}




Opacity of the series/point on selection.


#### Default Value



* 0.6

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions:{selectionSettings:{opacity:1}}                  
});
{% endhighlight %}


### commonSeriesOptions.selectionSettings.border `object`
{:#members:commonseriesoptions-selectionsettings-border}



Options for customizing the border of the series on selection.



### commonSeriesOptions.selectionSettings.border.color `string`
{:#members:commonseriesoptions-selectionsettings-border-color}



Border color of the series/point on selection.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{border:{color:"black"}}}                 
});
{% endhighlight %}



### commonSeriesOptions.selectionSettings.border.width `string`
{:#members:commonseriesoptions-selectionsettings-border-width}



Border width of the series/point on selection.


#### Default Value



* 2

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{border:{width:1}}}                  
});
{% endhighlight %}



### commonSeriesOptions.selectionSettings.pattern `string`
{:#members:commonseriesoptions-selectionsettings-pattern}




Specifies the pattern for the series/point on selection.

#### Default Value



* "none". See <a href="global.html#members:pattern">Pattern</a>

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{pattern:"chessboard"}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zbipilg5)


### commonSeriesOptions.selectionSettings.customPattern `string`
{:#members:commonseriesoptions-selectionsettings-custompattern}



Custom pattern for the series on selection.

#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
commonSeriesOptions :{selectionSettings:{customPattern:""}}                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ne1iit3s)




### crosshair `object`
{:#members:crosshair}




Options for displaying and customizing the crosshair.






### crosshair.marker `object`
{:#members:crosshair-marker}




Options for customizing the marker in crosshair.






### crosshair.marker.border `object`
{:#members:crosshair-marker-border}




Options for customizing the border.






### crosshair.marker.border.width `number`
{:#members:crosshair-marker-border-width}




Border width of the marker.


#### Default Value

* 3




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair : { marker : { border : { width :2 } } }              

});

{% endhighlight %}




### crosshair.marker.opacity `boolean`
{:#members:crosshair-marker-opacity}




Opacity of the marker.


#### Default Value

* true




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{marker :{opacity :2}}              

});

{% endhighlight %}




### crosshair.marker.size `object`
{:#members:crosshair-marker-size}




Options for customizing the size of the marker.






### crosshair.marker.size.height `number`
{:#members:crosshair-marker-size-height}




Height of the marker.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{marker :{size :{ height :15 }}}              

});

{% endhighlight %}




### crosshair.marker.size.width `number`
{:#members:crosshair-marker-size-width}




Width of the marker.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{marker :{size : {width :15}}}              

});

{% endhighlight %}




### crosshair.marker.visible `boolean`
{:#members:crosshair-marker-visible}




Show/hides the marker.


#### Default Value

* true




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{marker :{visible :false}}              

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hfja2bta)




### crosshair.type `enum`
{:#members:crosshair-type}




Specifies the type of the crosshair. It can be trackball or crosshair


#### Default Value

* "crosshair". See <a href="global.html#members:crosshairtype">CrosshairType</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{type : "trackball"}              

});

{% endhighlight %}




### crosshair.visible `boolean`
{:#members:crosshair-visible}




Show/hides the crosshair/trackball visibility.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   crosshair :{visible :true}              

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/31w3q03j)




### depth `number`
{:#members:depth}




Depth of the 3D Chart from front view of series to background wall. This property is applicable only for 3D view.


#### Default Value



* 100




#### Example

{% highlight js %}


$("#container").ejChart({

    depth : 100
                
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/mfcep44t)

### enable3D `boolean`
{:#members:enable3d}




Controls whether 3D view has to be enabled or not. 3D view is supported only for column, bar. Stacking column, stacking bar, pie and doughnut series types.


#### Default Value



* false




#### Example

{% highlight js %}


$("#container").ejChart({

        enable3D : true
                     
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dx0nj11k)




### enableCanvasRendering `boolean`
{:#members:enablecanvasrendering}




Controls whether Chart has to be rendered as Canvas or SVG. Canvas rendering supports all functionalities in SVG rendering except 3D Charts.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   enableCanvasRendering : true             

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2nvdn2ml)




### enableRotation `boolean`
{:#members:enablerotation}




Controls whether 3D view has to be rotated on dragging. This property is applicable only for 3D view.


#### Default Value



* false




#### Example


{% highlight js %}
 

$("#container").ejChart({

     enableRotation : true
                  
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hf5wopxp)


### indicators `array`
{:#members:indicators}




Options to customize the technical indicators.






### indicators.dPeriod `number`
{:#members:indicators-dperiod}




The dPeriod value for stochastic indicator.


#### Default Value



* 3




#### Example


{% highlight js %}
 
$("#container").ejChart({

      indicators :[{ dPeriod : 4}]
                    
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hnfnqsqd)


### indicators.enableAnimation `boolean`
{:#members:indicators-enableanimation}




Enables/disables the animation.


#### Default Value



* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

     indicators :[{ enableAnimation :  true}]
                    
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/p443wnjd)


### indicators.fill `string`
{:#members:indicators-fill}




Color of the technical indicator.


#### Default Value



* "#00008B"




#### Example


{% highlight js %}
 
$("#container").ejChart({

    indicators :[{ fill : "#ff0000"}]
                    
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/vrm2umdf)


### indicators.histogram `object`
{:#members:indicators-histogram}




Options to customize the histogram in MACD indicator.






### indicators.histogram.border `object`
{:#members:indicators-histogram-border}




Options to customize the histogram border in MACD indicator.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/stbnoy0x)



### indicators.histogram.border.color `string`
{:#members:indicators-histogram-border-color}




Color of the histogram border in MACD indicator.


#### Default Value


* "#9999ff"



#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ histogram : {border: {color: "#ff0000"}}}]
                        
});

{% endhighlight %}




### indicators.histogram.border.width `width`
{:#members:indicators-histogram-border-width}




Controls the width of histogram border line in MACD indicator.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({
 
    indicators :[{ histogram : {border: {width: 2}}}]
                        
});

{% endhighlight %}




### indicators.histogram.fill `string`
{:#members:indicators-histogram-fill}




Color of histogram columns in MACD indicator.


#### Default Value



* "#ccccff"




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ histogram : {fill: "#ff0000"}}]
                        
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2rvadgmd)


### indicators.histogram.opacity `number`
{:#members:indicators-histogram-opacity}




Opacity of histogram columns in MACD indicator.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ histogram : {opacity: 0.5}}]
                        
});

{% endhighlight %}




### indicators.kPeriod `number`
{:#members:indicators-kperiod}




Specifies the k period in stochastic indicator.


#### Default Value



* 3




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ kPeriod : 4}]
                        
});

{% endhighlight %}




### indicators.longPeriod `number`
{:#members:indicators-longperiod}




Specifies the long period in MACD indicator.


#### Default Value



* 26




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ longPeriod :  14"}]
                        
});

{% endhighlight %}




### indicators.lowerLine `object`
{:#members:indicators-lowerline}




Options to customize the lower line in indicators.






### indicators.lowerLine.fill `string`
{:#members:indicators-lowerline-fill}




Color of lower line.


#### Default Value



* "#008000"




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ lowerLine : {fill: "#ff0000"}}]
                         
});

{% endhighlight %}




### indicators.lowerLine.width `number`
{:#members:indicators-lowerline-width}




Width of the lower line.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ lowerLine : {width: 3}}]
                         
});

{% endhighlight %}




### indicators.macdLine `object`
{:#members:indicators-macdline}




Options to customize the MACD line.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/oarmpbow)




### indicators.macdLine.fill `string`
{:#members:indicators-macdline-fill}




Color of MACD line.


#### Default Value



* "#ff9933"




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ macdLine : {fill: "#ff0000"}}]
                        
});

{% endhighlight %}




### indicators.macdLine.width `number`
{:#members:indicators-macdline-width}




Width of the MACD line.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ macdLine : {width: 3}}]
                         
});

{% endhighlight %}




### indicators.macdType `string`
{:#members:indicators-macdtype}




Specifies the type of the MACD indicator. 


#### Default Value



* "line". See <a href="global.html#members:macdtype">MACDType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ macdType :  "both"}]
                        
});

{% endhighlight %}




### indicators.period `number`
{:#members:indicators-period}




Specifies period value in indicator.


#### Default Value



* 14




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ period : 20}]
                        
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yk3njhr1)


### indicators.periodLine `object`
{:#members:indicators-periodline}




Options to customize the period line in indicators.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/20dlmyxk)




### indicators.periodLine.fill `string`
{:#members:indicators-periodline-fill}




Color of period line in indicator.


#### Default Value



* "blue"




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ periodLine : {fill: "#ff0000"}}]
                        
});

{% endhighlight %}




### indicators.periodLine.width `number`
{:#members:indicators-periodline-width}




Width of the period line in indicators.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ periodLine : {width: 3}}]
                        
});

{% endhighlight %}




### indicators.seriesName `string`
{:#members:indicators-seriesname}




Name of the series for which indicator has to be drawn.


#### Default Value



* ""




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ seriesName : "rsi"}]
                        
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yk3njhr1)


### indicators.shortPeriod `number`
{:#members:indicators-shortperiod}




Specifies the short period in MACD indicator.


#### Default Value



* 13




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ shortPeriod :  14"}]
                         
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/2hpibxjj)


### indicators.standardDeviations `number`
{:#members:indicators-standarddeviations}




Specifies the standard deviation value for Bollinger band indicator.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({
    
     indicators :[{ standardDeviations : 3}]
                         
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/0b04ckwl)


### indicators.tooltip `object`
{:#members:indicators-tooltip}




Options to customize the tooltip.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ritlgl5w)




### indicators.tooltip.border `object`
{:#members:indicators-tooltip-border}




Option to customize the border of indicator tooltip.






### indicators.tooltip.border.color `string`
{:#members:indicators-tooltip-border-color}




Border color of indicator tooltip.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

       indicators :[{ tooltip :{border : { color :"#0000ff"}} }]
                             
});

{% endhighlight %}




### indicators.tooltip.border.width `number`
{:#members:indicators-tooltip-border-width}




Border width of indicator tooltip.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ tooltip :{border : { width :2}} }]
                         
});

{% endhighlight %}




### indicators.tooltip.duration `string`
{:#members:indicators-tooltip-duration}




Specifies the animation duration of indicator tooltip.


#### Default Value



* "500ms"




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ tooltip :{duration : "300ms"}}]
                        
});

{% endhighlight %}




### indicators.tooltip.enableAnimation `boolean`
{:#members:indicators-tooltip-enableanimation}




Enables/disables the tooltip animation.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({
 
        indicators :[{ tooltip :{enableAnimation : false}}]
                            
});

{% endhighlight %}




### indicators.tooltip.format `string`
{:#members:indicators-tooltip-format}




Format of indicator tooltip. Use “point.x” and “point.y” as a placeholder text to display the corresponding data point’s x and y value.


#### Default Value



* "#point.x# : #point.y#"




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ tooltip :{format : "#point.x#"}}]
                         
});

{% endhighlight %}




### indicators.tooltip.fill `string`
{:#members:indicators-tooltip-fill}




Background color of indicator tooltip.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ tooltip :{fill : "#FFF000"}}]
                        
});

{% endhighlight %}




### indicators.tooltip.opacity `number`
{:#members:indicators-tooltip-opacity}




Opacity of indicator tooltip.


#### Default Value



* 0.95




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ tooltip :{opacity : 0.5}}]
                        
});

{% endhighlight %}




### indicators.tooltip.visible `boolaean`
{:#members:indicators-tooltip-visible}




Controls the visibility of indicator tooltip.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ tooltip :{visible : true}}]
                        
});

{% endhighlight %}




### indicators.trigger `number`
{:#members:indicators-trigger}




Trigger value of MACD indicator.


#### Default Value



* 9




#### Example


{% highlight js %}

$("#container").ejChart({

    indicators :[{ trigger :  14}]
                        
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/nrh5tk4z)


### indicators.visibility `string`
{:#members:indicators-trigger}




Specifies the visibility of indicator.


#### Default Value



* "visible"




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ visibility :  "visible"}]
                         
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gshculgi)


### indicators.type `string`
{:#members:indicators-type}




Specifies the type of indicator that has to be rendered.


#### Default Value



* "sma". See <a href="global.html#members:indicatorstype">IndicatorsType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ type : "momentum"}]
                         
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/mr4ykv5i)


### indicators.upperLine `object`
{:#members:indicators-upperline}




Options to customize the upper line in indicators

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/duskfkix)




### indicators.upperLine.fill `string`
{:#members:indicators-upperline-fill}




Fill color of the upper line in indicators


#### Default Value



* "#ff9933"




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ upperLine : {fill: "#ff0000"}}]
                         
});

{% endhighlight %}




### indicators.upperLine.width `number`
{:#members:indicators-upperline-width}




Width of the upper line in indicators.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ upperLine : {width: 3}}]
                         
});

{% endhighlight %}




### indicators.width `number`
{:#members:indicators-width}




Width of the indicator line.


#### Default Value



* 2




#### Example


{% highlight js %}

$("#container").ejChart({

     indicators :[{ width :  3}]
                         
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/r23e0yrp)


### indicators.xAxisName `string`
{:#members:indicators-xaxisname}




Name of the horizontal axis used for indicator. Primary X axis is used when x axis name is not specified.


#### Default Value



* ""




#### Example


{% highlight js %}

$("#container").ejChart({
    
      indicators :[{ xAxisName :  "xAxis"}]
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/kksyu40s)


### indicators.yAxisName `string`
{:#members:indicators-yaxisname}




Name of the vertical axis used for indicator. Primary Y axis is used when y axis name is not specified


#### Default Value



* ""




#### Example


{% highlight js %}

$("#container").ejChart({
 
    indicators :[{ yAxisName :  "yAxis"}]
                        
});

{% endhighlight %}




### legend `object`
{:#members:legend}




Options to customize the legend items and legend title.






### legend.alignment `enum`
{:#members:legend-alignment}




Horizontal alignment of the legend.


#### Default Value

* "Center". See <a href="global.html#members:alignment">Alignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{alignment : "far"}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jpcc441l)




### legend.background `string`
{:#members:legend-background}




Background for the legend. Use this property to add a background image or background color for the legend.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ background : "green url('flower.png')"}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yesrbzgh)




### legend.border `object`
{:#members:legend-border}




Options for customizing the legend border.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zob1c5er)




### legend.border.color `string`
{:#members:legend-border-color}




Border color of the legend.


#### Default Value

* "transparent"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend : {border :{ color :"green"}}                     

});

{% endhighlight %}




### legend.border.width `number`
{:#members:legend-border-width}




Border width of the legend.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ border :{width :2}}                     

});

{% endhighlight %}




### legend.columnCount `number`
{:#members:legend-columncount}




Number of columns to arrange the legend items.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ columnCount : 2}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/g3p1ocgh)




### legend.enableScrollbar `boolean`
{:#members:legend-enableScrollbar}




Controls whether legend has to use scrollbar or not. When enabled, scroll bar appears depending upon size and position properties of legend.


#### Default Value

* true




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ enableScrollbar : false}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3budcknt)




### legend.fill `string`
{:#members:legend-fill}




Fill color for the legend items. By using this property, it displays all legend item shapes in same color. 
Legend items representing invisible series is displayed in gray color.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ fill : "green"}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3alytf20)




### legend.font `object`
{:#members:legend-font}




Options to customize the font used for legend item text.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jo5t2d4u)




### legend.font.fontFamily `string`
{:#members:legend-font-fontfamily}




Font family for legend item text.


#### Default Value

* "Segoe UI"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ font :{fontFamily : "algerian"}}                    

});

{% endhighlight %}




### legend.font.fontStyle `enum`
{:#members:legend-font-fontstyle}




Font style for legend item text.


#### Default Value

* "Normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ font :{fontStyle : "italic"}}                    

});

{% endhighlight %}




### legend.font.fontWeight `enum`
{:#members:legend-font-fontweight}




Font weight for legend item text.


#### Default Value

* "Regular". See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ font :{fontWeight : "lighter"}}                    

});

{% endhighlight %}




### legend.font.size `string`
{:#members:legend-font-size}




Font size for legend item text.


#### Default Value

* "12px"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ font :{size : "14px"}}                    

});

{% endhighlight %}




### legend.itemPadding `number`
{:#members:legend-itempadding}




Gap or padding between the legend items.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{itemPadding : 5}                     

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tozzsrit)




### legend.itemStyle `object`
{:#members:legend-itemstyle}




Options to customize the style of legend items.






### legend.itemStyle.border `object`
{:#members:legend-itemstyle-border}




Options for customizing the border of legend items.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hplwwoll)




### legend.itemStyle.border.color `string`
{:#members:legend-itemstyle-border-color}




Border color of the legend items.


#### Default Value

* "transparent"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ itemStyle :{border : { color : "green' }}}                    

});

{% endhighlight %}




### legend.itemStyle.border.width `number`
{:#members:legend-itemstyle-border-width}




Border width of the legend items.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ itemStyle :{border :{ width : 2 }}}                    

});

{% endhighlight %}




### legend.itemStyle.height `number`
{:#members:legend-itemstyle-height}




Height of the shape in legend items.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ itemStyle :{height : 20}}                    

});

{% endhighlight %}




### legend.itemStyle.width `number`
{:#members:legend-itemstyle-width}




Width of the shape in legend items.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ itemStyle :{width : 15}}                    

});

{% endhighlight %}




### legend.location `object`
{:#members:legend-location}




Options to customize the location of chart legend. Legend is placed in provided location only when value of **position** property is **custom**


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xurqtijv)




### legend.location.x `number`
{:#members:legend-location-x}




X value or horizontal offset to position the legend in chart.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{location :{x :20}}                    

});

{% endhighlight %}




### legend.location.y `number`
{:#members:legend-location-y}




Y value or vertical offset to position the legend.


#### Default Value

* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{location : {y : 100}}                  

});

{% endhighlight %}




### legend.opacity `number`
{:#members:legend-opacity}




Opacity of the legend.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ opacity : 0.5}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/nlewhk5r)




### legend.position `enum`
{:#members:legend-position}




Places the legend at specified position. Legend can be placed at **left**, **right**, **top** or **bottom** of the chart area. 
To manually specify the location of legend, set **custom** as value to this property.


#### Default Value

* "Bottom". See <a href="global.html#members:position">Position</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ position : "top"}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dwcvfzuv)




### legend.rowCount `number`
{:#members:legend-rowcount}




Number of rows to arrange the legend items.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ rowCount :2}                    

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tovkgqw5)




### legend.shape `enum`
{:#members:legend-shape}




Shape of the legend items. Default shape for pie and doughnut series is circle and all other series uses rectangle.


#### Default Value

* "None". See <a href="global.html#members:shape">Shape</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ shape : "circle" }                      

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/uq3eho3v)




### legend.size `object`
{:#members:legend-size}




Options to customize the size of the legend.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tovkgqw5)




### legend.size.height `string`
{:#members:legend-size-height}




Height of the legend. Height can be specified in either pixel or percentage.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ size :{height : "20%"}}                    

});

{% endhighlight %}




### legend.size.width `string`
{:#members:legend-size-width}




Width of the legend. Width can be specified in either pixel or percentage.


#### Default Value

* null




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend :{ size :{width : "20%"}}                    

});

{% endhighlight %}




### legend.title `object`
{:#members:legend-title}




Options to customize the legend title.






### legend.title.font `object`
{:#members:legend-title-font}




Options to customize the font used for legend title


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/bkgyatau)




### legend.title.font.fontFamily `string`
{:#members:legend-title-font-fontfamily}




Font family for the text in legend title.


#### Default Value

* "Segoe UI"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { font :{fontFamily: "Algerian" } } }                      

});

{% endhighlight %}




### legend.title.font.fontStyle `enum`
{:#members:legend-title-font-fontstyle}




Font style for legend title.


#### Default Value

* "normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { font :{fontStyle: "normal" } } }                      

});

{% endhighlight %}




### legend.title.font.fontWeight `enum`
{:#members:legend-title-font-fontweight}




Font weight for legend title.


#### Default Value

* "normal". See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { font :{fontWeight: "normal" } } }                      

});

{% endhighlight %}




### legend.title.font.size `string`
{:#members:legend-title-font-size}




Font size for legend title.


#### Default Value

* "12px"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { font :{size: "14px" } } }                      

});

{% endhighlight %}




### legend.title.text `string`
{:#members:legend-title-text}




Text to be displayed in legend title.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { text : "Countries" } }                      

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ux1xb3j4)




### legend.title.textAlignment `enum`
{:#members:legend-title-textalignment}




Alignment of the legend title.


#### Default Value

* "center". See <a href="global.html#members:alignment">Alignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend: { title: { textAlignment : "near" } }                      

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hnrnl1o1)




### legend.visible `boolean`
{:#members:legend-visible}




Controls the visibility of the legend.


#### Default Value

* true




#### Example


{% highlight js %}
 
$("#container").ejChart({

   legend : {visible : false}                     

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dwcvfzuv)




### locale `string`
{:#members:locale}




Name of the culture based on which chart should be localized. Number and date time values are localized with respect to the culture name. 
String type properties like title text are not localized automatically. Provide localized text as value to string type properties.


#### Default Value

* "en-US"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   locale : "en-US"            

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/g3q30pdl)




### Margin `object`
{:#members:margin}




Options to customize the left, right, top and bottom margins of chart area.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5rlvd0ri)




### margin.left `number`
{:#members:margin-left}




Spacing for the left margin of chart area. Setting positive value decreases the width of the chart area from left side.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   margin : { left: 15 }             

});

{% endhighlight %}




### margin.right `number`
{:#members:margin-right}




Spacing for the right margin of chart area. Setting positive value decreases the width of the chart area from right side.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   margin : { right: 10 }             

});

{% endhighlight %}




### margin.top `number`
{:#members:margin-top}




Spacing for the top margin of chart area. Setting positive value decreases the height of the chart area from the top.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   margin : { top: 10 }             

});

{% endhighlight %}




### margin.bottom `number`
{:#members:margin-bottom}




Spacing for the bottom margin of the chart area. Setting positive value decreases the height of the chart area from the bottom.


#### Default Value

* 10




#### Example


{% highlight js %}
 
$("#container").ejChart({

   margin : { bottom: 10 }             

});

{% endhighlight %}




### perspectiveAngle `number`
{:#members:perspectiveangle}




Perspective angle of the 3D view. Chart appears closer when perspective angle is decreased, and distant when perspective angle is increased. 
This property is applicable only when 3D view is enabled


#### Default Value



* 90




#### Example


{% highlight js %}

$("#container").ejChart({

     perspectiveAngle : 60
                  
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ofpxunlm)




### primaryXAxis `object`
{:#members:primaryxaxis}




This is a horizontal axis that contains options to configure axis and it is the primary x axis for all the series in series array. To override x axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s xAxisName property to link both axis and series.






### primaryXAxis.alternateGridBand `object`
{:#members:primaryxaxis-alternategridband}




Options for customizing horizontal axis alternate grid band.






### primaryXAxis.alternateGridBand.even `object`
{:#members:primaryxaxis-alternategridband-even}




Options for customizing even grid band.






### primaryXAxis.alternateGridBand.even.fill `string`
{:#members:primaryxaxis-alternategridband-even-fill}




Fill color for the even grid bands.


#### Default Value



* transparent




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { alternateGridBand: { even :{ fill : "green" } } }
                        
});

{% endhighlight %}




### primaryXAxis.alternateGridBand.even.opacity `number`
{:#members:primaryxaxis-alternategridband-even-opacity}




Opacity of the even grid band.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { alternateGridBand: { even :{ opacity : 0.5 } } }
                       
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/vanuvupl)


### primaryXAxis.alternateGridBand.odd `object`
{:#members:primaryxaxis-alternategridband-odd}




Options for customizing odd grid band.






### primaryXAxis.alternateGridBand.odd.fill `string`
{:#members:primaryxaxis-alternategridband-odd-fill}




Fill color of the odd grid bands


#### Default Value



* transparent




#### Example


{% highlight js %}
 
$("#container").ejChart({

    primaryXAxis: { alternateGridBand: { odd :{ fill : "red" } } }
                          
});

{% endhighlight %}




### primaryXAxis.alternateGridBand.odd.opacity `number`
{:#members:primaryxaxis-alternategridband-odd-opacity}




Opacity of odd grid band


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { alternateGridBand: { odd :{ opacity : 0.5 } } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/n23ku03f)


### primaryXAxis.axisLine `object`
{:#members:primaryxaxis-axisline}




Options for customizing the axis line.  






### primaryXAxis.axisLine.dashArray `string`
{:#members:primaryxaxis-axisline-dasharray}




Pattern of dashes and gaps to be applied to the axis line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { axisLine : { dashArray : "2,3" } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gx3dji4o)


### primaryXAxis.axisLine.offset `number`
{:#members:primaryxaxis-axisline-offset}




Padding for axis line. Normally, it is used along with plotOffset to pad the plot area.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { axisLine : { offset : 5 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fmchh3yz)


### primaryXAxis.axisLine.visible `boolean`
{:#members:primaryxaxis-axisline-visible}




Show/hides the axis line.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { axisLine : { visible : false } }
                          
});

{% endhighlight %}




### primaryXAxis.axisLine.width `number`
{:#members:primaryxaxis-axisline-width}




Width of axis line.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { axisLine : { width : 2 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/0chmy5rg)


### primaryXAxis.columnIndex `number`
{:#members:primaryxaxis-columnindex}




Specifies the index of the column where the axis is associated, when the chart area is divided into multiple plot areas by using columnDefinitions.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { columnIndex: 2 }
                           
});

{% endhighlight %}




### primaryXAxis.columnSpan `number`
{:#members:primaryxaxis-columnspan}




Specifies the number of columns or plot areas an axis has to span horizontally.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { columnSpan: 2 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zqgvpx1v)


### primaryXAxis.crosshairLabel `object`
{:#members:primaryxaxis-crosshairlabel}




Options to customize the crosshair label.






### primaryXAxis.crosshairLabel.visible `boolean`
{:#members:primaryxaxis-crosshairlabel-visible}




Show/hides the crosshair label associated with this axis.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { crosshairLabel : { visible : true} }
                          
});

{% endhighlight %}




### primaryXAxis.desiredIntervals `number`
{:#members:primaryxaxis-desiredintervals}




With this setting, you can request axis to calculate intervals approximately equal to your desired interval.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { desiredIntervals: 5 }
                           
});

{% endhighlight %}




### primaryXAxis.edgeLabelPlacement `enum`
{:#members:primaryxaxis-edgelabelplacement}




Specifies the position of labels at the edge of the axis. 


#### Default Value



* ej.datavisualization.Chart.EdgeLabelPlacement.None. See <a href="global.html#members:edgelabelplacement">EdgeLabelPlacement</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { edgeLabelPlacement : "shift" }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ff44lp52)


### primaryXAxis.enableTrim `boolean`
{:#members:primaryxaxis-enabletrim}




Specifies whether to trim the axis label when the width of the label exceeds the maximumLabelWidth.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { enableTrim : true }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/qt3th50v)


### primaryXAxis.font `object`
{:#members:primaryxaxis-font}




Options for customizing the font of the axis Labels.






### primaryXAxis.font.fontFamily `string`
{:#members:primaryxaxis-font-fontfamily}




Font family of labels.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { font : { fontFamily : "Algerian"} }
                           
});

{% endhighlight %}




### primaryXAxis.font.fontStyle `enum`
{:#members:primaryxaxis-font-fontstyle}




Font style of labels.


#### Default Value




* ej.datavisualization.Chart.FontStyle.Normal. See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { font : { fontStyle : "Italic"} }
                          
});

{% endhighlight %}




### primaryXAxis.font.fontWeight `enum`
{:#members:primaryxaxis-font-fontweight}




Font weight of the label.


#### Default Value



* ej.datavisualization.Chart.FontWeight.Regular. See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { font : { fontWeight : "lighter"} }
                           
});

{% endhighlight %}




### primaryXAxis.font.opacity `number`
{:#members:primaryxaxis-font-opacity}




Opacity of the axis labels.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { font : { opacity : 0.5} }
                          
});

{% endhighlight %}




### primaryXAxis.font.size `string`
{:#members:primaryxaxis-font-size}




Font size of the axis labels.


#### Default Value



* "13px"




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { font : { size : "12px"} }
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xm2ur0jj)


### primaryXAxis.intervalType `enum`
{:#members:primaryxaxis-intervaltype}




Specifies the type of interval in date time axis.


#### Default Value




* null. See <a href="global.html#members:intervaltype">IntervalType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { intervalType: "days" }
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/qccdazta)


### primaryXAxis.isInversed `boolean`
{:#members:primaryxaxis-isinversed}




Specifies whether to inverse the axis.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { isInversed : true}
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xp1frbzw)


### primaryXAxis.labelFormat `string`
{:#members:primaryxaxis-labelformat}




Custom formatting for axis label and supports all standard formatting type of numerical and date time values.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { labelFormat: "{value}%" }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/x22gftws)


### primaryXAxis.labelIntersectAction `enum`
{:#members:primaryxaxis-labelintersectaction}




Specifies the action to take when the axis labels are overlapping with each other. 


#### Default Value



* ej.datavisualization.Chart.LabelIntersectAction.None. See <a href="global.html#members:labelintersectaction">LabelIntersectAction</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { labelIntersectAction : "multipleRows" }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/sedhp2ek)


### primaryXAxis.labelPosition `enum`
{:#members:primaryxaxis-labelposition}




Specifies the position of the axis labels.


#### Default Value



* "outside". See <a href="global.html#members:labelposition">LabelPosition</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { labelPosition : "inside" }
                       
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/u0s1y0dg)


### primaryXAxis.labelRotation `number`
{:#members:primaryxaxis-labelrotation}




Angle in degrees to rotate the axis labels.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { labelRotation: 90 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gl5iwbsh)


### primaryXAxis.logBase `number`
{:#members:primaryxaxis-logbase}




Logarithmic base value. This is applicable only for logarithmic axis.


#### Default Value



* 10




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { logBase: 5 }
                          
});

  {% endhighlight %}




### primaryXAxis.majorGridLines `object`
{:#members:primaryxaxis-majorgridlines}




Options for customizing major gird lines.






### primaryXAxis.majorGridLines.dashArray `string`
{:#members:primaryxaxis-majorgridlines-dasharray}




Pattern of dashes and gaps used to stroke the major grid lines.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorGridLines: { dashArray : "2,3"} }
                          
});

{% endhighlight %}




### primaryXAxis.majorGridLines.opacity `number`
{:#members:primaryxaxis-majorgridlines-opacity}




Opacity of major grid lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorGridLines: { opacity: 0.5 } }
                          
});

{% endhighlight %}




### primaryXAxis.majorGridLines.visible `boolean`
{:#members:primaryxaxis-majorgridlines-visible}




Show/hides the major grid lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorGridLines: { visible: false } }
                          
});

{% endhighlight %}




### primaryXAxis.majorGridLines.width `number`
{:#members:primaryxaxis-majorgridlines-width}




Width of the major grid lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorGridLines: { width : 0.5} }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/1tjezqc0)


### primaryXAxis.majorTickLines `object`
{:#members:primaryxaxis-majorticklines}




Options for customizing the major tick lines.






### primaryXAxis.majorTickLines.size `number`
{:#members:primaryxaxis-majorticklines-size}




Length of the major tick lines.


#### Default Value



* 5




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorTickLines: { size: 2 } }
                          
});

{% endhighlight %}




### primaryXAxis.majorTickLines.visible `boolean`
{:#members:primaryxaxis-majorticklines-visible}




Show/hides the majorticklines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorTickLines: { visible: false } }
                          
});

{% endhighlight %}




### primaryXAxis.majorTickLines.width `number`
{:#members:primaryxaxis-majorticklines-width}




Width of the major tick lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { majorTickLines: { width: 2 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/30i5qgrm)


### primaryXAxis.maximumLabels `number`
{:#members:primaryxaxis-maximumlabels}




Maximum number of labels to be displayed in every 100 pixels.


#### Default Value



* 3




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { maximumLabels : 5 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/a4gcmpzx)


### primaryXAxis.maximumLabelWidth `number`
{:#members:primaryxaxis-maximumlabelwidth}




Maximum width of the axis label. When the label exceeds the width, the label gets trimmed when the enableTrim is set to true.


#### Default Value



* 34




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { maximumLabelWidth :34.5 }
                           
});

{% endhighlight %}




### primaryXAxis.minorGridLines `object`
{:#members:primaryxaxis-minorgridlines}




Options for customizing the minor grid lines.






### primaryXAxis.minorGridLines.dashArray `string`
{:#members:primaryxaxis-minorgridlines-dasharray}




Patterns of dashes and gaps used to stroke the minor grid lines.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { minorGridLines: { dashArray: "2,3" } }
                          
});

{% endhighlight %}




### primaryXAxis.minorGridLines.visible `boolean`
{:#members:primaryxaxis-minorgridlines-visible}




Show/hides the minor grid lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { minorGridLines: { visible: true } }
                          
});

{% endhighlight %}




### primaryXAxis.minorGridLines.width `number`
{:#members:primaryxaxis-minorgridlines-width}




Width of the minorGridLines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { minorGridLines: { width: 2 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xlobmfvj)


### primaryXAxis.minorTickLines `object`
{:#members:primaryxaxis-minorticklines}




Options for customizing the minor tick lines.






### primaryXAxis.minorTickLines.size `number`
{:#members:primaryxaxis-minorticklines-size}




Length of the minor tick lines.


#### Default Value



* 5




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { minorTickLines: { size: 2 } }
                          
});

{% endhighlight %}




### primaryXAxis.minorTickLines.visible `boolean`
{:#members:primaryxaxis-minorticklines-visible}




Show/hides the minor tick lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { minorTickLines: { visible: true } }
                          
});
Width of the minor tick line.
{% endhighlight %}




### primaryXAxis.minorTickLines.width `number`
{:#members:primaryxaxis-minorticklines-width}




Width of the minor tick line.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({
 
    primaryXAxis: { minorTickLines: { width: 2 } }
                          
});

{% endhighlight %}




### primaryXAxis.minorTicksPerInterval `number`
{:#members:primaryxaxis-minorticksperinterval}




Specifies the number of minor ticks per interval.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({
 
    primaryXAxis: { minorTicksPerInterval: 5 }
                          
});

{% endhighlight %}


### primaryXAxis.name `string`
{:#members:primaryxaxis-name}




Unique name of the axis. To associate an axis with the series, you have to set this name to the xAxisName/yAxisName property of the series.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { name: "xAxis" }
                          
});

{% endhighlight %}




### primaryXAxis.opposedPosition `boolean`
{:#members:primaryxaxis-opposedposition}




Specifies whether to render the axis at the opposite side of its default position.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { opposedPosition : true }
                          
});

{% endhighlight %}




### primaryXAxis.plotOffset `number`
{:#members:primaryxaxis-plotoffset}




Specifies the padding for the plot area.


#### Default Value



* 10




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { plotOffset: 0 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yo4ek2ci)


### primaryXAxis.range `object`
{:#members:primaryxaxis-range}




Options to customize the range of the axis.

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/Sync_jhhilggd)


### primaryXAxis.range.minimum `number`
{:#members:primaryxaxis-range-minimum}




Minimum value of the axis range.


#### Default Value

* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { range : { minimum: 10 } }
                          
});

{% endhighlight %}


### primaryXAxis.range.maximum `number`
{:#members:primaryxaxis-range-maximum}




Maximum value of the axis range.


#### Default Value

* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { range : { maximum: 100 } }
                          
});

{% endhighlight %}


### primaryXAxis.range.interval `number`
{:#members:primaryxaxis-range-interval}




Interval of the axis range.


#### Default Value

* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { range : { interval: 10 } }
                          
});

{% endhighlight %}


### primaryXAxis.rangePadding `enum`
{:#members:primaryxaxis-rangepadding}




Specifies the padding for the axis range.


#### Default Value



* ej.datavisualization.Chart.rangePaddding.None




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { rangePadding : "normal" }
                          
});

{% endhighlight %}




### primaryXAxis.roundingPlaces `number`
{:#members:primaryxaxis-roundingplaces}




Rounds the number to the given number of decimals.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { roundingPlaces: 3 }
                          
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hgqmxm50)




### primaryXAxis.stripLine `array`
{:#members:primaryxaxis-stripline}


Options for customizing the strip lines.


#### Default Value



* [ ]







### primaryXAxis.stripLine.borderColor `string`
{:#members:primaryxaxis-stripline-bordercolor}




Border color of the strip line.


#### Default Value



* "gray"




#### Example


{% highlight js %}

$("#container").ejChart({
 
    primaryXAxis: { stripLine:[{ borderColor: "green" }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.color `string`
{:#members:primaryxaxis-stripline-color}




Background color of the strip line.


#### Default Value



* "gray"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { stripLine:[{ color: "green" }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.end `number`
{:#members:primaryxaxis-stripline-end}




End value of the strip line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { stripLine:[{ end: 5 }]}
                           
});

{% endhighlight %}




### primaryXAxis.stripLine.font `object`
{:#members:primaryxaxis-stripline-font}




Options for customizing the font of the text.






### primaryXAxis.stripLine.font.color `string`
{:#members:primaryxaxis-stripline-font-color}




Font color of the strip line text.


#### Default Value



* "black"




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { stripLine:[{ font : { color: "green"} }]}
                           
});

{% endhighlight %}




### primaryXAxis.stripLine.font.fontFamily `enum`
{:#members:primaryxaxis-stripline-font-fontfamily}




Font family of the strip line text.


#### Default Value



* "middlecenter"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.font.fontStyle `enum`
{:#members:primaryxaxis-stripline-font-fontstyle}




Font style of the strip line text.


#### Default Value



* "Normal"




#### Example


{% highlight js %}

$("#container").ejChart({ 

    primaryXAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.font.fontWeight `string`
{:#members:primaryxaxis-stripline-font-fontweight}




Font weight of the strip line text.


#### Default Value



* "regular"




#### Example


{% highlight js %}

$("#container").ejChart({

      primaryXAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}
                            
});

{% endhighlight %}




### primaryXAxis.stripLine.font.opacity `number`
{:#members:primaryxaxis-stripline-font-opacity}




Opacity of the strip line text.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

primaryXAxis: { stripLine:[{ font : { opacity: 0.5} }]}
                      
});

{% endhighlight %}




### primaryXAxis.stripLine.font.size `string`
{:#members:primaryxaxis-stripline-font-size}




Font size of the strip line text.


#### Default Value



* "12px"




#### Example


{% highlight js %}

$("#container").ejChart({

        primaryXAxis: { stripLine:[{ font : { size: "15px"} }]}
                              
});

{% endhighlight %}




### primaryXAxis.stripLine.start `number`
{:#members:primaryxaxis-stripline-start}




Start value of the strip line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { stripLine:[{ start: 2 }]}
                           
});

{% endhighlight %}




### primaryXAxis.stripLine.startFromAxis `boolean`
{:#members:primaryxaxis-stripline-startfromaxis}




Indicates whether to render the strip line from the minimum/start value of the axis. This property does not work when start property is set.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { stripLine:[{ startFromAxis : true }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.text `string`
{:#members:primaryxaxis-stripline-text}




Specifies text to be displayed inside the strip line.


#### Default Value



* "stripLine"




#### Example


{% highlight js %}

$("#container").ejChart({
 
    primaryXAxis: { stripLine:[{ text : "Empty Point" }]}
                           
});

{% endhighlight %}




### primaryXAxis.stripLine.textAlignment `enum`
{:#members:primaryxaxis-stripline-textalignment}




Specifies the alignment of the text inside the strip line.


#### Default Value



* "middlecenter". See <a href="global.html#members:textalignment">TextAlignment</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { stripLine:[{ textAlignment : "middletop" }]}
                           
});

{% endhighlight %}




### primaryXAxis.stripLine.visible `boolean`
{:#members:primaryxaxis-stripline-visible}




Show/hides the strip line.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { stripLine:[{ visible : true }]}
                          
});

{% endhighlight %}




### primaryXAxis.stripLine.width `number`
{:#members:primaryxaxis-stripline-width}




Width of the strip line.


#### Default Value



* 0




#### Example


{% highlight js %}

$("#container").ejChart({

      primaryXAxis: { stripLine:[{ width : 0 }]}
                            
});

{% endhighlight %}




### primaryXAxis.stripLine.zIndex `enum`
{:#members:primaryxaxis-stripline-zindex}




Specifies the order where the strip line and the series have to be rendered. When zOrder is “behind”, strip line is rendered under the series and when it is “over”, it is rendered above the series.


#### Default Value



* "over". See <a href="global.html#members:zindex">ZIndex</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { stripLine:[{ zIndex: "behind" }]}
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/1at44wzi)


### primaryXAxis.tickLinesPosition `enum`
{:#members:primaryxaxis-ticklinesposition}




Specifies the position of the axis tick lines.


#### Default Value




* "outside". See <a href="global.html#members:ticklinesposition">TickLinesPosition</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { tickLinesPosition : "inside" }
                           
});

{% endhighlight %}




### primaryXAxis.title `object`
{:#members:primaryxaxis-title}




Options for customizing the axis title.






### primaryXAxis.title.enableTrim `boolean`
{:#members:primaryxaxis-title-enabletrim}




Specifies whether to trim the axis title when it exceeds the chart area or the maximum width of the title.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { title:{enableTrim:true} }
                      
});

{% endhighlight %}




### primaryXAxis.title.font `object`
{:#members:primaryxaxis-title-font}




Options for customizing the title font.






### primaryXAxis.title.font.fontFamily `string`
{:#members:primaryxaxis-title-font-fontfamily}




Font family of the title text.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { title: { font : { fontFamily : "Algerain"} } }
                      
});

{% endhighlight %}




### primaryXAxis.title.font.fontStyle `enum`
{:#members:primaryxaxis-title-font-fontstyle}




Font style of the title text.


#### Default Value



* ej.datavisualization.Chart.FontStyle.Normal




#### Example


{% highlight js %}


$("#container").ejChart({

     primaryXAxis: { title: { font : { fontStyle : "Italic"} } }
                      
});

{% endhighlight %}




### primaryXAxis.title.font.fontWeight `enum`
{:#members:primaryxaxis-title-font-fontweight}




Font weight of the title text.


#### Default Value



* ej.datavisualization.Chart.FontWeight.Regular. See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { title: { font : { fontWeight : "lighter"} } }
                      
});

{% endhighlight %}




### primaryXAxis.title.font.opacity `number`
{:#members:primaryxaxis-title-font-opacity}




Opacity of the axis title text.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { title: { font : { opacity : 0.8} } }
                           
});

{% endhighlight %}




### primaryXAxis.title.font.size `string`
{:#members:primaryxaxis-title-font-size}




Font size of the axis title.


#### Default Value



* "16px"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { title: { font : { size : "14px"} } }
                          
});

{% endhighlight %}




### primaryXAxis.title.maximumTitleWidth `number`
{:#members:primaryxaxis-title-maximumtitlewidth}




Maximum width of the title, when the title exceeds this width, the title gets trimmed, when enableTrim is true. 


#### Default Value



* 34




#### Example


{% highlight js %}

$("#container").ejChart({

      primaryYAxis: { title:{maximumTitleWidth: null} }
                            
});

{% endhighlight %}




### primaryXAxis.title.text `string`
{:#members:primaryxaxis-title-text}




Title for the axis.


#### Default Value



* ""




#### Example


{% highlight js %}

$("#container").ejChart({

primaryXAxis: { title: { text: "Year" } }
                      
});

{% endhighlight %}




### primaryXAxis.title.visible `boolean`
{:#members:primaryxaxis-title-visible}




Controls the visibility of axis title.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { title: { visible: false } }
                          
});

{% endhighlight %}




### primaryXAxis.valueType `enum`
{:#members:primaryxaxis-valuetype}




Specifies the type of data the axis is handling.


#### Default Value




* null. See <a href="global.html#members:valuetype">ValueType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryXAxis: { valueType: "double" }
                           
});

{% endhighlight %}




### primaryXAxis.visible `boolean`
{:#members:primaryxaxis-visible}




Show/hides the axis.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { visible: false }
                          
});

{% endhighlight %}




### primaryXAxis.zoomFactor `number`
{:#members:primaryxaxis-zoomfactor}




The axis is scaled by this factor. When zoomFactor is 0.5, the chart is scaled by 200% along this axis. Value ranges from 0 to 1.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { zoomFactor : 0.5 }
                          
});

{% endhighlight %}




### primaryXAxis.zoomPosition `number`
{:#members:primaryxaxis-zoomposition}




Position of the zoomed axis. Value ranges from 0 to 1.



#### Default Value



* 0




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryXAxis: { zoomPosition :0.5 }
                          
});

{% endhighlight %}




### primaryYAxis `object`
{:#members:primaryyaxis}




This is a vertical axis that contains options to configure axis. This is the primary y axis for all the series in series array. To override y axis for particular series, create an axis object by providing unique name by using name property and add it to axes array. Then, assign the name to the series&rsquo;s yAxisName property to link both axis and series.






### primaryYAxis.alternateGridBand `object`
{:#members:primaryyaxis-alternategridband}




Options for customizing vertical axis alternate grid band.






### primaryYAxis.alternateGridBand.even `object`
{:#members:primaryyaxis-alternategridband-even}




Options for customizing even grid band.






### primaryYAxis.alternateGridBand.even.fill `string`
{:#members:primaryyaxis-alternategridband-even-fill}




Fill color for the even grid bands.


#### Default Value



* transparent




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { alternateGridBand: { even : {fill : "red" } } }
                          
});

{% endhighlight %}




### primaryYAxis.alternateGridBand.even.opacity `number`
{:#members:primaryyaxis-alternategridband-even-opacity}




Opacity of the even grid band.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { alternateGridBand: { even : {opacity : 0.5 } } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/12z4yd2l)


### primaryYAxis.alternateGridBand.odd `object`
{:#members:primaryyaxis-alternategridband-odd}




Options for customizing odd grid band.






### primaryYAxis.alternateGridBand.odd.fill `string`
{:#members:primaryyaxis-alternategridband-odd-fill}




Fill color of the odd grid bands.


#### Default Value



* "transparent"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { alternateGridBand: { odd : { fill :"red" }  } }
                          
});

{% endhighlight %}




### primaryYAxis.alternateGridBand.odd.opacity `number`
{:#members:primaryyaxis-alternategridband-odd-opacity}




Opacity of odd grid band.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { alternateGridBand: { odd : { opacity :0.5 }  } }
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hyakwb3m)


### primaryYAxis.axisLine `object`
{:#members:primaryyaxis-axisline}




Options for customizing the axis line.






### primaryYAxis.axisLine.dashArray `string`
{:#members:primaryyaxis-axisline-dasharray}




Pattern of dashes and gaps to be applied to the axis line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: {  axisLine :{ dashArray : "2,3" } }
                          
});

{% endhighlight %}




### primaryYAxis.axisLine.offset `number`
{:#members:primaryyaxis-axisline-offset}




Padding for axis line. Normally, it is used along with plotOffset to pad the plot area.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { axisLine: { offset : 5 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3drq4c1j)


### primaryYAxis.axisLine.visible `boolean`
{:#members:primaryyaxis-axisline-visible}




Show/hides the axis line.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { axisLine: { visible : false } }
                          
});

{% endhighlight %}




### primaryYAxis.axisLine.width `number`
{:#members:primaryyaxis-axisline-width}




Width of axis line.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { axisLine: { width : 2 } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zz4cubdn)


### primaryYAxis.crosshairLabel `object`
{:#members:primaryyaxis-crosshairlabel}




Options to customize the crosshair label.






### primaryYAxis.crosshairLabel.visible `boolean`
{:#members:primaryyaxis-crosshairlabel-visible}




Show/hides the crosshair label associated with this axis.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { crosshairLabel: { visible : true } }
                          
});

{% endhighlight %}




### primaryYAxis.desiredIntervals `number`
{:#members:primaryyaxis-desiredintervals}




With this setting, you can request axis to calculate intervals approximately equal to your desired interval.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { desiredIntervals: 5 }
                          
});

{% endhighlight %}




### primaryYAxis.edgeLabelPlacement `enum`
{:#members:primaryyaxis-edgelabelplacement}




Specifies the position of labels at the edge of the axis. 


#### Default Value




* ej.datavisualization.Chart.EdgeLabelPlacement.None. See <a href="global.html#members:edgelabelplacement">EdgeLabelPlacement</a>




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryYAxis: { edgeLabelPlacement: "shift" }
                           
});

{% endhighlight %}




### primaryYAxis.enableTrim `boolean`
{:#members:primaryyaxis-enabletrim}




Specifies whether to trim the axis label when the width of the label exceeds the maximumLabelWidth. 


#### Default Value



* false 




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { enableTrim : true }
                          
});

{% endhighlight %}




### primaryYAxis.font `object`
{:#members:primaryyaxis-font}




Options for customizing the font of the axis Labels.






### primaryYAxis.font.fontFamily `string`
{:#members:primaryyaxis-font-fontfamily}




Font family of labels.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { font: { fontFamily : "Algerian" } }
                          
});

{% endhighlight %}




### primaryYAxis.font.fontStyle `enum`
{:#members:primaryyaxis-font-fontstyle}




Font style of labels.


#### Default Value




ej.datavisualization.Chart.FontStyle.Normal. See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { font: { fontStyle : "italic" } }
                          
});

{% endhighlight %}




### primaryYAxis.font.fontWeight `enum`
{:#members:primaryyaxis-font-fontweight}




Font weight of the label.


#### Default Value




* ej.datavisualization.Chart.FontWeight.Regular. See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { font: { fontWeight : "normal" } }
                          
});

{% endhighlight %}




### primaryYAxis.font.opacity `number`
{:#members:primaryyaxis-font-opacity}




Opacity of the axis labels.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { font: { opacity : 0.5 } }
                          
});

{% endhighlight %}




### primaryYAxis.font.size `string`
{:#members:primaryyaxis-font-size}




Font size of the axis labels.


#### Default Value



* "13px"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { font: { size : "12px" } }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/s1dshld4))


### primaryYAxis.intervalType `enum`
{:#members:primaryyaxis-intervaltype}




Specifies the type of interval in date time axis.


#### Default Value




* null. See <a href="global.html#members:intervaltype">IntervalType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { intervalType: "days" }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/n2dwkjtr)


### primaryYAxis.isInversed `boolean`
{:#members:primaryyaxis-isinversed}




Specifies whether to inverse the axis.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryYAxis: { isInversed : true}
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/mnnwkac1)


### primaryYAxis.labelFormat `string`
{:#members:primaryyaxis-labelformat}




Custom formatting for axis label and supports all standard formatting type of numerical and date time values.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { labelFormat: "{value}F" }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/n2dwkjtr)


### primaryYAxis.labelIntersectAction `enum`
{:#members:primaryyaxis-labelintersectaction}




Specifies the action to take when the axis labels are overlapping with each other. 


#### Default Value



* ej.datavisualization.Chart.LabelIntersectAction.None




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryYAxis: { labelIntersectAction: "multipleRows" }
                           
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pm2ksurr)


### primaryYAxis.labelPosition `enum`
{:#members:primaryyaxis-labelposition}




#### Default Value



* "outside". See <a href="global.html#members:labelposition">LabelPosition</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { labelPosition : "inside" }
                           
});

{% endhighlight %}




### primaryYAxis.logBase `number`
{:#members:primaryyaxis-logbase}




Logarithmic base value. This is applicable only for logarithmic axis.


#### Default Value




* 10




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { logBase: 5 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/nfviof2i)


### primaryYAxis.majorGridLines `object`
{:#members:primaryyaxis-majorgridlines}




Options for customizing major gird lines.






### primaryYAxis.majorGridLines.dashArray `string`
{:#members:primaryyaxis-majorgridlines-dasharray}




Pattern of dashes and gaps used to stroke the major grid lines.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorGridLines : {dashArray : "2,3"} }
                      
});

{% endhighlight %}




### primaryYAxis.majorGridLines.opacity `number`
{:#members:primaryyaxis-majorgridlines-opacity}




Opacity of major grid lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorGridLines : {opacity : 0.5} }
                          
});

{% endhighlight %}




### primaryYAxis.majorGridLines.visible `boolean`
{:#members:primaryyaxis-majorgridlines-visible}




Show/hides the major grid lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorGridLines : {visible : false} }
                          
});

{% endhighlight %}




### primaryYAxis.majorGridLines.width `number`
{:#members:primaryyaxis-majorgridlines-width}




Width of the major grid lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorGridLines : {width : 2} }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jaqmz0ox)


### primaryYAxis.majorTickLines `object`
{:#members:primaryyaxis-majorticklines}




Options for customizing the major tick lines.






### primaryYAxis.majorTickLines.size `number`
{:#members:primaryyaxis-majorticklines-size}




Length of the major tick lines.


#### Default Value



* 5




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorTickLines : {size : 2} }
                      
});

{% endhighlight %}




### primaryYAxis.majorTickLines.visible `boolean`
{:#members:primaryyaxis-majorticklines-visible}




Show/hides the majorticklines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorTickLines : {visible : false} }
                          
});

{% endhighlight %}




### primaryYAxis.majorTickLines.width `number`
{:#members:primaryyaxis-majorticklines-width}




Width of the major tick lines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { majorTickLines : {width : 2} }
                          
});
</script>  
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/dumkxazd)


### primaryYAxis.maximumLabels `number`
{:#members:primaryyaxis-maximumlabels}




Maximum number of labels to be displayed in every 100 pixels.


#### Default Value



* 3




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { maximumLabels: 5 }
                          
});

{% endhighlight %}




### primaryYAxis.maximumLabelWidth
{:#members:primaryyaxis-maximumlabelwidth}




Maximum width of the axis label. When the label exceeds the width, the label gets trimmed when the enableTrim is set to true.


#### Default Value



* ej.datavisualization.Chart.maximumLabelWidth type {int}




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { maximumLabelWidth :34.5 }
                          
});

{% endhighlight %}




### primaryYAxis.minorGridLines `object`
{:#members:primaryyaxis-minorgridlines}




Options for customizing the minor grid lines.






### primaryYAxis.minorGridLines.dashArray `string`
{:#members:primaryyaxis-minorgridlines-dasharray}




Patterns of dashes and gaps used to stroke the minor grid lines.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorGridLines : {dashArray : "2,3"} }
                          
});

{% endhighlight %}




### primaryYAxis.minorGridLines.visible `boolean`
{:#members:primaryyaxis-minorgridlines-visible}




Show/hides the minor grid lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorGridLines : {visible : true} }
                          
});

{% endhighlight %}




### primaryYAxis.minorGridLines.width `number`
{:#members:primaryyaxis-minorgridlines-width}




Width of the minorGridLines.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorGridLines : {width : 2} }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3ijc021x)


### primaryYAxis.minorTickLines `object`
{:#members:primaryyaxis-minorticklines}




Options for customizing the minor tick lines.






### primaryYAxis.minorTickLines.size `number`
{:#members:primaryyaxis-minorticklines-size}




Length of the minor tick lines.


#### Default Value



* 5




#### Example


{% highlight js %}


$("#container").ejChart({

    primaryYAxis: { minorTickLines : {size : 2} }
                          
});

{% endhighlight %}




### primaryYAxis.minorTickLines.visible `boolean`
{:#members:primaryyaxis-minorticklines-visible}




Show/hides the minor tick lines.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorTickLines : {visible : true} }    
                  
});
</script>  
{% endhighlight %}




### primaryYAxis.minorTickLines.width `number`
{:#members:primaryyaxis-minorticklines-width}




Width of the minor tick line


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorTickLines : {width : 2} }
                          
});

{% endhighlight %}




### primaryYAxis.minorTicksPerInterval `number`
{:#members:primaryyaxis-minorticksperinterval}




Specifies the number of minor ticks per interval.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { minorTicksPerInterval: 3 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tbbhdw21)


### primaryYAxis.name `string`
{:#members:primaryyaxis-name}




Unique name of the axis. To associate an axis with the series, you have to set this name to the xAxisName/yAxisName property of the series.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { name: "yAxis" }
                          
});

{% endhighlight %}




### primaryYAxis.opposedPosition `boolean`
{:#members:primaryyaxis-opposedposition}




Specifies whether to render the axis at the opposite side of its default position.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryYAxis: { opposedPosition : true }
                           
});

{% endhighlight %}



### primaryYAxis.plotOffset `number`
{:#members:primaryyaxis-plotoffset}




Specifies the padding for the plot area.


#### Default Value



* 10




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { plotOffset: 5 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ls2i5oiv)


### primaryYAxis.rangePadding `enum`
{:#members:primaryyaxis-rangepadding}




Specifies the padding for the axis range.


#### Default Value




* ej.datavisualization.Chart.RangePadding.None. See <a href="global.html#members:rangepadding">RangePadding</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { rangePadding : "none" }
                          
});

{% endhighlight %}




### primaryYAxis.roundingPlaces `number`
{:#members:primaryyaxis-roundingplaces}




Rounds the number to the given number of decimals.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { roundingPlaces: 2 }  
                    
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ad225rnj)


### primaryYAxis.rowIndex `number`
{:#members:primaryyaxis-rowindex}




Specifies the index of the row to which the axis is associated, when the chart area is divided into multiple plot areas by using rowDefinitions.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

     primaryYAxis: { rowIndex: 1 }                      
});
</script> 
{% endhighlight %}




### primaryYAxis.rowSpan `number`
{:#members:primaryyaxis-rowspan}




Specifies the number of row or plot areas an axis has to span vertically.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { rowSpan: 2 }
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fitf4tn3)


### primaryYAxis.stripLine `array`
{:#members:primaryyaxis-stripline}




Options for customizing the strip lines.


#### Default Value



* [ ]







### primaryYAxis.stripLine.borderColor `string`
{:#members:primaryyaxis-stripline-bordercolor}




Border color of the strip line.


#### Default Value



* "gray"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ borderColor: "green" }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.color `string`
{:#members:primaryyaxis-stripline-color}




Background color of the strip line.


#### Default Value



* "gray"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ color: "green" }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.end `number`
{:#members:primaryyaxis-stripline-end}




End value of the strip line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ end: 5 }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.font `object`
{:#members:primaryyaxis-stripline-font}




Options for customizing the font of the text.






### primaryYAxis.stripLine.font.color `string`
{:#members:primaryyaxis-stripline-font-color}




Font color of the strip line text.


#### Default Value



* "black"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ font : { color: "green"} }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.font.fontFamily `enum`
{:#members:primaryyaxis-stripline-font-fontfamily}




Font family of the strip line text.


#### Default Value



* "middlecenter"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.font.fontStyle `enum`
{:#members:primaryyaxis-stripline-font-fontstyle}




Font style of the strip line text.


#### Default Value



* "Normal"




#### Example


{% highlight js %}

$("#container").ejChart({

primaryYAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}
                      
});

{% endhighlight %}




### primaryYAxis.stripLine.font.fontWeight `string`
{:#members:primaryyaxis-stripline-font-fontweight}




Font weight of the strip line text.


#### Default Value



* "regular"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}
                      
});

{% endhighlight %}




### primaryYAxis.stripLine.font.opacity `number`
{:#members:primaryyaxis-stripline-font-opacity}




Opacity of the strip line text.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ font : { opacity: 0.5} }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.font.size `string`
{:#members:primaryyaxis-stripline-font-size}




Font size of the strip line text.


#### Default Value



* "12px"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ font : { size: "15px"} }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.start `number`
{:#members:primaryyaxis-stripline-start}




Start value of the strip line.


#### Default Value



* null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ start: 2 }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.startFromAxis `boolean`
{:#members:primaryyaxis-stripline-startfromaxis}




Indicates whether to render the strip line from the minimum/start value of the axis. This property won’t work when start property is set.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ startFromAxis : true }]} 
                     
});

{% endhighlight %}




### primaryYAxis.stripLine.text `string`
{:#members:primaryyaxis-stripline-text}




Specifies text to be displayed inside the strip line.


#### Default Value



* "stripLine"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ text : "Empty Point" }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.textAlignment `enum`
{:#members:primaryyaxis-stripline-textalignment}




Specifies the alignment of the text inside the strip line.


#### Default Value




* "middlecenter". See <a href="global.html#members:textalignment">TextAlignment</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ textAlignment : "middletop" }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.visible `boolean`
{:#members:primaryyaxis-stripline-visible}




Show/hides the strip line.


#### Default Value



* false




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ visible : true }]}
                          
});

{% endhighlight %}




### primaryYAxis.stripLine.width `number`
{:#members:primaryyaxis-stripline-width}




Width of the strip line.


#### Default Value



* 0




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ width : 0 }]}                      
});

{% endhighlight %}




### primaryYAxis.stripLine.zIndex `enum`
{:#members:primaryyaxis-stripline-zindex}




Specifies the order in which strip line and the series have to be rendered. When zOrder is “behind”, strip line is rendered below the series and when it is “over”, it is rendered above the series.


#### Default Value




* "over". See <a href="global.html#members:zindex">ZIndex</a>



#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { stripLine:[{ zIndex: "behind" }]}
                          
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pigg3hc0)


### primaryYAxis.tickLinesPosition `enum`
{:#members:primaryyaxis-ticklinesposition}




Specifies the position of the axis tick lines.


#### Default Value




* "outside". See <a href="global.html#members:ticklinesposition">TickLinesPosition</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { tickLinesPosition : "inside" }
                           
});

{% endhighlight %}




### primaryYAxis.title `object`
{:#members:primaryyaxis-title}




Options for customizing the axis title.






### primaryYAxis.title.enableTrim `boolean`
{:#members:primaryyaxis-title-enabletrim}




Specifies whether to trim the axis title when it exceeds the chart area or the maximum width of the title.


#### Default Value



* ej.datavisualization.Chart.enableTrim




#### Example


{% highlight js %}

$("#container").ejChart({

      primaryXAxis: { title:{enableTrim:true} }
                            
});

{% endhighlight %}




### primaryYAxis.title.font `object`
{:#members:primaryyaxis-title-font}




Options for customizing the title font.






### primaryYAxis.title.font.fontFamily `string`
{:#members:primaryyaxis-title-font-fontfamily}




Font family of the title text.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ font :{ fontFamily: "Algerian" } } }
                          
});

{% endhighlight %}




### primaryYAxis.title.font.fontStyle `enum`
{:#members:primaryyaxis-title-font-fontstyle}




Font style of the title text.


#### Default Value



* ej.datavisualization.Chart.FontStyle.Normal




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ font :{ fontStyle : "Italic" } } }
                          
});

{% endhighlight %}




### primaryYAxis.title.font.fontWeight `enum`
{:#members:primaryyaxis-title-font-fontweight}




Font weight of the title text.


#### Default Value



* ej.datavisualization.Chart.FontWeight.Regular. See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ font :{ fontWeight: "normal" } } }
                          
});

{% endhighlight %}




### primaryYAxis.title.font.opacity `number`
{:#members:primaryyaxis-title-font-opacity}




Opacity of the axis title text.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ font :{ opacity: 0.5 } } }
                          
});

{% endhighlight %}




### primaryYAxis.title.font.size `string`
{:#members:primaryyaxis-title-font-size}




Font size of the axis title.


#### Default Value



* "16px"




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ font :{ size: "12px" } } }
                          
});

{% endhighlight %}




### primaryYAxis.title.maximumTitleWidth `number`
{:#members:primaryyaxis-title-maximumtitlewidth}




Maximum width of the title, when the title exceeds this width, the title gets trimmed, when enableTrim is true. 


#### Default Value



* ej.datavisualization.Chart.maximumTitleWidth.null




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title:{maximumTitleWidth: null} }
                          
});

{% endhighlight %}




### primaryYAxis.title.text `string`
{:#members:primaryyaxis-title-text}




Title for the axis.


#### Default Value



* ""




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title :{ text: "yAxis" } }
                          
});

{% endhighlight %}




### primaryYAxis.title.visible `boolean`
{:#members:primaryyaxis-title-visible}




Controls the visibility of axis title.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { title: { visible: false } }
                          
});

{% endhighlight %}




### primaryYAxis.valueType `enum`
{:#members:primaryyaxis-valuetype}




Specifies the type of data the axis is handling.


#### Default Value




* null. See <a href="global.html#members:valuetype">ValueType</a>




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { valueType: "double" }
                          
});

{% endhighlight %}




### primaryYAxis.visible `boolean`
{:#members:primaryyaxis-visible}




Show/hides the axis.


#### Default Value



* true




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { visible : false }
                          
});

{% endhighlight %}




### primaryYAxis.zoomFactor `number`
{:#members:primaryyaxis-zoomfactor}




The axis is scaled by this factor. When zoomFactor is 0.5, the chart is scaled by 200% along this axis. Values ranges from 0 to 1.


#### Default Value



* 1




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { zoomFactor : 0.5 }
                          
});

{% endhighlight %}




### primaryYAxis.zoomPosition `number`
{:#members:primaryyaxis-zoomposition}




Position of the zoomed axis. Value ranges from 0 to 1


#### Default Value



* 0




#### Example


{% highlight js %}

$("#container").ejChart({

    primaryYAxis: { zoomPosition : 0.5 }
                          
});

{% endhighlight %}




### rotation<span class="type-signature type number">number</span>
{:#members:rotation}




Rotation angle of the 3D view. This property is applicable only when 3D view is enabled.


#### Default Value



* 0




#### Example


{% highlight js %}

$("#container").ejChart({

     rotation : 45
             
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pf23aw13)




### rowDefinitions `array`
{:#members:rowdefinitions}




Options to split Chart into multiple plotting areas horizontally. Each object in the collection represents a plotting area in Chart.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jydjcqbo)




### rowDefinitions.unit `enum`
{:#members:rowDefinitions.unit}




Specifies the unit to measure the height of the row in plotting area.


#### Default Value

* 'pixel'. See <a href="global.html#members:unit">Unit</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   rowDefinitions :[{ unit : "percentage" }]                     

});

{% endhighlight %}




### rowDefinitions.rowHeight `number`
{:#members:rowDefinitions.rowHeight}




Height of the row in plotting area. Height is measured in either pixel or percentage based on the value of unit property.


#### Default Value

* 50




#### Example


{% highlight js %}
 
$("#container").ejChart({

   rowDefinitions :[{ rowHeight : 50 }]                     

});

{% endhighlight %}




### rowDefinitions.lineColor `string`
{:#members:rowDefinitions.lineColor}




Color of the line that indicates the starting point of the row in plotting area.


#### Default Value

* "transparent"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   rowDefinitions :[{ lineColor : "green" }]                     

});

{% endhighlight %}




### rowDefinitions.lineWidth `number`
{:#members:rowDefinitions.lineWidth}




Width of the line that indicates the starting point of the row in plot area.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   rowDefinitions :[{ lineWidth : 2 }]                     

});

{% endhighlight %}




### series `array`
{:#members:series}




Specifies the properties used for customizing the series.






### series.bearFillColor `string`
{:#members:series-bearfillcolor}




Color of the point, where the close is up in financial chart.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{bearFillColor: "blue" }]                   
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/p404ugol)
 



### series.border `object`
{:#members:series-border}




Options for customizing the border of the series.






### series.border.color `string`
{:#members:series-border-color}




Border color of the series.


#### Default Value



*  "transparent"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{border :{ color : "green" } }]                  
});
{% endhighlight %}




### series.border.width `number`
{:#members:series-border-width}




Border width of the series.


#### Default Value



* 1




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{border :{ width : 2 } }]                  
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/vf2xong1)


### series.bullFillColor `string`
{:#members:series-bullfillcolor}




Color of the point, where the close is down in financial chart.


#### Default Value



 * null



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{bullFillColor: "green" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/v540kjyb)



### series.dashArray `string`
{:#members:series-dasharray}




Pattern of dashes and gaps used to stroke the line type series.


#### Default Value



* ""




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{dashArray : "2,3"}]                  
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/322c4ex3)



### series.dataSource `object`
{:#members:series-datasource}




Specifies the dataSource for the series. It can be an array of JSON objects or an instance of ej.DataManager.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{dataSource: data }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/soesgx0m)


### series.doughnutCoefficient `number`
{:#members:series-doughnutcoefficient}




Controls the size of the hole in doughnut series. Value ranges from 0 to 1.


#### Default Value



* 0.4




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{doughnutCoefficient : 0.5 }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/1xjrwrxl)


### series.doughnutSize `number`
{:#members:series-doughnutsize}




Controls the size of the doughnut series. Value ranges from 0 to 1.


#### Default Value



*  0.8




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{doughnutSize : 0.6 }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/eyi1qmre)

### series.drawType `boolean`
{:#members:series-drawtype}




Type of series to be drawn in radar or polar series. 


#### Default Value



* "line". See <a href="global.html#members:drawtype">DrawType</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({
series : [{drawType : "column" }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/pg04h4gh)


### series.enableAnimation `boolean`
{:#members:series-enableanimation}




Enable/disable the animation of series.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{enableAnimation : true }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/w4mkzixd)


### series.enableSmartLabels `number`
{:#members:series-enablesmartlabels}




To avoid overlapping of data labels smartly. 


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{enableSmartLabels : false }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/40docuib)


### series.endAngle `number`
{:#members:series-endangle}




End angle of pie/doughnut series. For a complete circle, it has to be 360, by default.


#### Default Value



 * null




#### Example


{% highlight js %}
 
$("#container").ejChart({
series : [{endAngle: 270 }]                   
});

{% endhighlight %}

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/fqpf3ort)



### series.explode `boolean`
{:#members:series-explode}




Explodes the pie/doughnut slices on mouse move.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{explode: true }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/prpei1ld)


### series.explodeAll `boolean`
{:#members:series-explodeall}




Explodes all the slice of pie/doughnut on render.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{explodeAll: true }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/n3if1tnn)


### series.explodeIndex `number`
{:#members:series-explodeindex}




Index of the point to be exploded from pie/doughnut/pyramid/funnel.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{explodeIndex : 2 }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/taccivfh)



### series.explodeOffset `number`
{:#members:series-explodeoffset}




Specifies the distance of the slice from the center, when it is exploded.


#### Default Value



 * 25




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{explodeOffset : 20 }]                   
});
 {% endhighlight %}
 

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/2j040lr0)



### series.fill `string`
{:#members:series-fill}




Fill color of the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{fill : "green"}]                 
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/sit3agft)


### series.font `object`
{:#members:series-font}




Options for customizing the series font.






### series.font.color `string`
{:#members:series-font-color}




Font color of the series text.


#### Default Value



* "#707070"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{font :{color : "green"}}]                 
});
{% endhighlight %}




### series.font.fontFamily `string`
{:#members:series-font-fontfamily}




Font Family of the series.


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ font : { fontFamily : "Algerian"}}]                 
});
 {% endhighlight %}




### series.font.fontStyle `enum`
{:#members:series-font-fontstyle}




Font Style of the series.


#### Default Value



* "Normal"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{font :{fontStyle : "italic"}} ]                
});
{% endhighlight %}




### series.font.fontWeight `enum`
{:#members:series-font-fontweight}




Font weight of the series.


#### Default Value



* "Regular"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{font :{fontWeight : "lighter"}}]                 
});
{% endhighlight %}




### series.font.opacity `number`
{:#members:series-font-opacity}




Opacity of series text.


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{font :{opacity : 0.5}}]                 
});
{% endhighlight %}




### series.font.size `string`
{:#members:series-font-size}




Size of the series text.


#### Default Value



* "12px"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{font :{size : "14px"}}]                 
});
 {% endhighlight %}

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/g0jeybnt)


### series.funnelHeight `string`
{:#members:series-funnelheight}




Specifies the height of the funnel in funnel series. Values can be in both pixel and percentage.


#### Default Value



* "32.7%"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{funnelHeight : '40%' }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/5gqzqndn)


### series.funnelWidth `string`
{:#members:series-funnelwidth}




Specifies the width of the funnel in funnel series. Values can be in both pixel and percentage.


#### Default Value



* "11.6%"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{funnelWidth : '40%' }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/u0f5hsbw)


### series.gapRatio `number`
{:#members:series-gapratio}




Gap between the slices of pyramid/funnel series.


#### Default Value



 * 0




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{gapRatio : 0.2 }]                   
});
 {% endhighlight %}

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/cjocyfce)


### series.isClosed `boolean`
{:#members:series-isclosed}




Specifies whether to join start and end point of a line/area series used in polar/radar chart to form a closed path.


#### Default Value



* true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{isClosed : false }]                   
});
 {% endhighlight %}

Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/ktrsbcrh)


### series.isStacking `boolean`
{:#members:series-isstacking}




Specifies whether to stack the column series in polar/radar charts.


#### Default Value



 * true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{isStacking : false }]                   
});
 {% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/mj2qdclr)




### series.isTransposed `boolean`
{:#members:series-isTransposed}




Renders the chart vertically. This is applicable only for cartesian type series.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{isTransposed : false }]                   
});
{% endhighlight %}


Try it : [JS Playground Sample](http://jsplayground.syncfusion.com/1ypcv5bf)




### series.labelPosition `enum`
{:#members:series-labelposition}




Position of the data label in pie/doughnut/pyramid/funnel series. OutsideExtended position is not applicable for pyramid/funnel.



#### Default Value



* "inside". See <a href="global.html#members:labelposition">LabelPosition</a>



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{labelPosition : "outside" }]                   
});
 {% endhighlight %}
 
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/q013nk40)



### series.lineCap `enum`
{:#members:series-linecap}




Specifies the line cap of the series. 


#### Default Value



* "Butt". See <a href="global.html#members:linecap">LineCap</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{lineCap : "butt"}]                  
});
{% endhighlight %}




### series.lineJoin `enum`
{:#members:series-linejoin}




Specifies the type of shape to be used where two lines meet.


#### Default Value



* "Round". See <a href="global.html#members:linejoin">LineJoin</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{lineJoin : "round"}]                  
});
{% endhighlight %}




### series.marker `object`
{:#members:series-marker}




Options for displaying and customizing marker for individual point in a series. Marker contains shapes and/or data labels.






### series.marker.border `object`
{:#members:series-marker-border}




Options for customizing the border of the marker shape.






### series.marker.border.color `string`
{:#members:series-marker-border-color}




Border color of the marker shape. 


#### Default Value



* "white"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker:{border:{color : "green"}}}]                  
});
{% endhighlight %}




### series.marker.border.width `number`
{:#members:series-marker-border-width}




Border width of the marker shape. 


#### Default Value



* 3




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{border :{width : 2}}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/po32cgmg)



### series.marker.dataLabel `object`
{:#members:series-marker-datalabel}




Options for displaying and customizing data labels.






### series.marker.dataLabel.angle `number`
{:#members:series-marker-datalabel-angle}




Angle of the data label in degrees. Only the text gets rotated, whereas the background and border does not rotate. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{angle : 90}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ulhda01g)


### series.marker.dataLabel.border `object`
{:#members:series-marker-datalabel-border}




Options for customizing the border of the data label.






### series.marker.dataLabel.border.color `string`
{:#members:series-marker-datalabel-border-color}




Border color of the data label. 

#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{border : {color : "green"}}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.border.width `number`
{:#members:series-marker-datalabel-border-width}




Border width of the data label. 


#### Default Value



* 0.1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{border :{ width :2 }}}}]                 
});
 {% endhighlight %}




### series.marker.dataLabel.connectorLine `object`
{:#members:series-marker-datalabel-connectorline}




Options for displaying and customizing the line that connects point and data label.






### series.marker.dataLabel.connectorLine.type `enum`
{:#members:series-marker-datalabel-connectorline-type}




Specifies when the connector has to be drawn as Bezier curve or straight line. This is applicable only for Pie and Doughnut chart types. 


#### Default Value



 * "line". See <a href="global.html#members:connectorlinetype">ConnectorLineType</a>



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ type : "bezier" }}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.connectorLine.width `number`
{:#members:series-marker-datalabel-connectorline-width}




Width of the connector. 


#### Default Value



 * 0.5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ width : 2 }}}}]                 
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fjr0nbgc)



### series.marker.dataLabel.fill `string`
{:#members:series-marker-datalabel-fill}




Background color of the data label. 


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{fill : "green"}}}]                 
});
 {% endhighlight %}




### series.marker.dataLabel.font `object`
{:#members:series-marker-datalabel-font}




Options for customizing the data label font.






### series.marker.dataLabel.font.fontFamily `string`
{:#members:series-marker-datalabel-font-fontfamily}




Font family of the data label. 


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}]                 
});
 {% endhighlight %}




### series.marker.dataLabel.font.fontStyle `enum`
{:#members:series-marker-datalabel-font-fontstyle}




Font style of the data label.  


#### Default Value



* "normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}]                 
});
 {% endhighlight %}




### series.marker.dataLabel.font.fontWeight `enum`
{:#members:series-marker-datalabel-font-fontweight}




Font weight of the data label. 


#### Default Value



* "regular". See <a href="global.html#members:fontweight">FontWeight</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.font.opacity `number`
{:#members:series-marker-datalabel-font-opacity}




Opacity of the text. 


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ opacity : 0.5 }}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.font.size `string`
{:#members:series-marker-datalabel-font-size}




Font size of the data label. 


#### Default Value



 * "12px"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { size : "14px" }}}}]                 
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fjr0nbgc)



### series.marker.dataLabel.horizontalTextAlignment `enum`
{:#members:series-marker-datalabel-horizontaltextalignment}




Horizontal alignment of the data label. 


#### Default Value



* "center"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{horizontalTextAlignment : "far"}}}]                  
});
{% endhighlight %}




### series.marker.dataLabel.margin<span class="type-signature type object">object</span>
{:#members:series-marker-datalabel-margin}




Margin of the text to its background shape. The size of the background shape increases based on the margin applied to its text.






### series.marker.dataLabel.margin.bottom<span class="type-signature type number">number</span>
{:#members:series-marker-datalabel-margin-bottom}




Bottom margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ bottom :10 }}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.margin.left `number`
{:#members:series-marker-datalabel-margin-left}




Left margin of the text. 


#### Default Value



 * 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ left : 10}}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.margin.right `number`
{:#members:series-marker-datalabel-margin-right}




Right margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ right :10 }}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.margin.top `number`
{:#members:series-marker-datalabel-margin-top}




Top margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ top :10 } }}}]                 
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3yoplr42)



### series.marker.dataLabel.opacity `number`
{:#members:series-marker-datalabel-opacity}




Opacity of the data label. 


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{opacity : 0.5}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.shape `enum`
{:#members:series-marker-datalabel-shape}




Background shape of the data label. 


#### Default Value



* No shape is rendered by default, so its value is ‘none’. See <a href="global.html#members:shape">Shape</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{shape : "circle"}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.text `string`
{:#members:series-marker-datalabel-text}




Name of a field in data source where datalabel text is displayed.  


#### Default Value



* ""


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{text : "TextFieldName"}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.textPosition `enum`
{:#members:series-marker-datalabel-textposition}




Specifies the position of the data label. This property can be used only for the series such as column, bar, stacked column, stacked bar, 100% stacked column, 100% stacked bar, candle and OHLC. 


#### Default Value



* "top". See <a href="global.html#members:textposition">TextPosition</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{dataLabel :{textPosition : "bottom"}}}]                 
});
{% endhighlight %}




### series.marker.dataLabel.verticalTextAlignment `enum`
{:#members:series-marker-datalabel-verticaltextalignment}




Vertical alignment of the data label. 


#### Default Value



* 'center'




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{dataLabel :{verticalTextAlignment : "far"}}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/emylj2pu)


### series.marker.dataLabel.visible `boolean`
{:#members:series-marker-datalabel-visible}




Controls the visibility of the data labels. 


#### Default Value



* false




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{dataLabel :{visible : true}}}]                  
});
 {% endhighlight %}


### series.marker.dataLabel.template `string`
{:#members:series-marker-datalabel-template}




Custom template to format the data label content. Use “point.x” and “point.y” as a placeholder text to display the corresponding data point’s x and y value.


#### Default Value



* ""




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{dataLabel :{template : "item"}}}]                  
});
 {% endhighlight %}
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/l5pmkkgr)
 
 
 
 
### series.marker.dataLabel.offset `number`
{:#members:series-marker-datalabel-offset}




Moves the label vertically by some offset.


#### Default Value



* 0




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{marker :{dataLabel :{offset : 10}}}]                  
});
 {% endhighlight %}



### series.marker.fill `string`
{:#members:series-marker-fill}




Color of the marker shape. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker : { fill : "green" } }]                  
});
{% endhighlight %}




### series.marker.imageUrl `string`
{:#members:series-marker-imageurl}




The URL for the Image that is to be displayed as marker. In order to display image as marker, set series.marker.shape as ‘image’.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{ imageUrl: "../images/sample.png"}}]                  
});
{% endhighlight %}




### series.marker.opacity `number`
{:#members:series-marker-opacity}




Opacity of the marker. 


#### Default Value



 * 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{ opacity : 0.5 }}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/1bavaoqq)



### series.marker.shape `enum`
{:#members:series-marker-shape}




Specifies the shape of the marker.  


#### Default Value



* "circle". See <a href="global.html#members:shape">Shape</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{ shape: "rectangle"}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/vd552nid)


### series.marker.size `object`
{:#members:series-marker-size}




Options for customizing the size of the marker shape.






### series.marker.size.height `number`
{:#members:series-marker-size-height}




Height of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{size :{height : 5}}}]                 
});
{% endhighlight %}




### series.marker.size.width `number`
{:#members:series-marker-size-width}




Width of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{ size :{ width : 2 } } }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/53gkiuse)


### series.marker.visible `boolean`
{:#members:series-marker-visible}




Controls the visibility of the marker shape. 


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{marker :{ visible : true}}]                  
});
 {% endhighlight %}




### series.opacity `number`
{:#members:series-opacity}




Opacity of the series.


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{opacity : 0.5}]                  
});
 {% endhighlight %}
 
 
 
 
### series.palette `string`
{:#members:series-palette}




Name of a field in data source where fill color for all the data points is generated.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{palette : "ColorFieldName"}]                  
});
{% endhighlight %}




### series.pieCoefficient `number`
{:#members:series-piecoefficient}




Controls the size of pie series. Value ranges from 0 to 1.




#### Default Value



 * 0.8




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{pieCoefficient : 0.6 }]                   
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hpl0ffff)



### series.points `array`
{:#members:series-points}




Option to add data points; each point should have x and y property. Also, optionally, you can customize the points color, border, marker by using fill, border and marker options.




### series.points.border `object`
{:#members:series-points-border}




Options for customizing the border of a point. This is applicable only for column type series and accumulation type series.






### series.points.border.color `string`
{:#members:series-points-border-color}




Border color of the point. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ border:{color : "green"} }] }]                  
});
{% endhighlight %}




### series.points.border.width `number`
{:#members:series-points-border-width}




Border width of the point. 


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points:[{ border :{width : 2} }] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/t5dhe5d0)




### series.points.close `number`
{:#members:series-points-close}




Close value of the point. Close value is applicable only for financial type series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ close : 50 }] }]                  
});
{% endhighlight %}


### series.points.size<span class="type-signature type number">number</span>
{:#members:series-points-size}




Size of a bubble in the bubble series. This is applicable only for the bubble series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ size : 5 }] }]                  
});
{% endhighlight %}




### series.points.fill `string`
{:#members:series-points-fill}




Background color of the point. This is applicable only for column type series and accumulation type series. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ fill : "green" }] }]                  
});
{% endhighlight %}




### series.points.high `number`
{:#members:series-points-high}




High value of the point. High value is applicable only for financial type series, range area series and range column series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ high : 120 }] }]                  
});
{% endhighlight %}




### series.points.low `number`
{:#members:series-points-x}




Low value of the point. Low value is applicable only for financial type series, range area series and range column series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ low : 70 }] }]                  
});
{% endhighlight %}




### series.points.marker `object`
{:#members:series-points-marker}




Options for displaying and customizing marker for a data point. Marker contains shapes and/or data labels.






### series.points.marker.border `object`
{:#members:series-points-marker-border}




Options for customizing the border of the marker shape.






### series.points.marker.border.color `string`
{:#members:series-points-marker-border-color}




Border color of the marker shape. 


#### Default Value



* "white"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker:{border:{color : "green"}} }] }]                  
});
{% endhighlight %}




### series.points.marker.border.width `number`
{:#members:series-points-marker-border-width}




Border width of the marker shape. 


#### Default Value



* 3




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points:[{ marker :{border :{width : 2}} }] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/3vkjgyc0)



### series.points.marker.dataLabel `object`
{:#members:series-points-marker-datalabel}




Options for displaying and customizing data label.






### series.points.marker.dataLabel.angle `number`
{:#members:series-points-marker-datalabel-angle}




Angle of the data label in degrees. Only the text gets rotated, whereas the background and border does not rotate. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{angle : 90} }] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/d3r5mcfc)


### series.points.marker.dataLabel.border `object`
{:#members:series-points-marker-datalabel-border}




Options for customizing the border of the data label.






### series.points.marker.dataLabel.border.color `string`
{:#members:series-points-marker-datalabel-border-color}




Border color of the data label. 

#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{border : {color : "green"}}} }] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.border.width `number`
{:#members:series-points-marker-datalabel-border-width}




Border width of the data label. 


#### Default Value



* 0.1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{border :{ width :2 }}} }] }]                 
});
 {% endhighlight %}




### series.points.marker.dataLabel.connectorLine `object`
{:#members:series-points-marker-datalabel-connectorline}




Options for displaying and customizing the line that connects point and data label.






### series.points.marker.dataLabel.connectorLine.type `enum`
{:#members:series-points-marker-datalabel-connectorline-type}




Specifies when the connector has to be drawn as Bezier curve or straight line. This is applicable only for Pie and Doughnut chart types. 


#### Default Value



 * "line". See <a href="global.html#members:connectorlinetype">ConnectorLineType</a>



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{connectorLine :{ type : "bezier" }}} }] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.connectorLine.width `number`
{:#members:series-points-marker-datalabel-connectorline-width}




Width of the connector. 


#### Default Value



 * 0.5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{connectorLine :{ width : 2 }}} }] }]                 
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/tm0wneyn)



### series.points.marker.dataLabel.fill `string`
{:#members:series-points-marker-datalabel-fill}




Background color of the data label. 


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{fill : "green"}}}]}]                 
});
 {% endhighlight %}




### series.points.marker.dataLabel.font `object`
{:#members:series-points-marker-datalabel-font}




Options for customizing the data label font.






### series.points.marker.dataLabel.font.fontFamily `string`
{:#members:series-points-marker-datalabel-font-fontfamily}




Font family of the data label. 


#### Default Value



* "Segoe UI"




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points:[{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}]}]                 
});
 {% endhighlight %}




### series.points.marker.dataLabel.font.fontStyle `enum`
{:#members:series-points-marker-datalabel-font-fontstyle}




Font style of the data label.  


#### Default Value



* "normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{points:[{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}]}]                 
});
 {% endhighlight %}




### series.points.marker.dataLabel.font.fontWeight `enum`
{:#members:series-points-marker-datalabel-font-fontweight}




Font weight of the data label. 


#### Default Value



* "regular". See <a href="global.html#members:fontweight">FontWeight</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{font : { fontWeight : "lighter" }}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.font.opacity `number`
{:#members:series-points-marker-datalabel-font-opacity}




Opacity of the text. 


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{font :{ opacity : 0.5 }}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.font.size `string`
{:#members:series-points-marker-datalabel-font-size}




Font size of the data label. 


#### Default Value



 * "12px"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{font : { size : "14px" }}}}] }]                 
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/v4rp3aio)



### series.points.marker.dataLabel.horizontalTextAlignment `enum`
{:#members:series-points-marker-datalabel-horizontaltextalignment}




Horizontal alignment of the data label. 


#### Default Value



* "center"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{horizontalTextAlignment : "far"}}}] }]                  
});
{% endhighlight %}




### series.points.marker.dataLabel.margin `object`
{:#members:series-points-marker-datalabel-margin}




Margin of the text to its background shape. The size of the background shape increases based on the margin applied to its text.






### series.points.marker.dataLabel.margin.bottom `number`
{:#members:series-points-marker-datalabel-margin-bottom}




Bottom margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{margin :{ bottom :10 }}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.margin.left `number`
{:#members:series-points-marker-datalabel-margin-left}




Left margin of the text. 


#### Default Value



 * 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points: [{ marker :{dataLabel :{margin :{ left : 10}}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.margin.right `number`
{:#members:series-points-marker-datalabel-margin-right}




Right margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{margin :{ right :10 }}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.margin.top `number`
{:#members:series-points-marker-datalabel-margin-top}




Top margin of the text. 


#### Default Value



* 5




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{margin :{ top :10 } }}}] }]                 
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rezz5cjo)



### series.points.marker.dataLabel.opacity `number`
{:#members:series-points-marker-datalabel-opacity}




Opacity of the data label. 


#### Default Value



* 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{opacity : 0.5}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.shape `enum`
{:#members:series-points-marker-datalabel-shape}




Background shape of the data label. 


#### Default Value



* No shape is rendered by default, so its value is ‘none’. See <a href="global.html#members:shape">Shape</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{shape : "circle"}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.textPosition `enum`
{:#members:series-points-marker-datalabel-textposition}




Specifies the position of the data label. This property can be used only for the series such as column, bar, stacked column, stacked bar, 100% stacked column, 100% stacked bar, candle and OHLC. 


#### Default Value



* "top". See <a href="global.html#members:textposition">TextPosition</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{textPosition : "bottom"}}}] }]                 
});
{% endhighlight %}




### series.points.marker.dataLabel.verticalTextAlignment `enum`
{:#members:series-points-marker-datalabel-verticaltextalignment}




Vertical alignment of the data label. 


#### Default Value



* 'center'




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points: [{ marker :{dataLabel :{verticalTextAlignment : "far"}}}] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/k5e5rltz)


### series.points.marker.dataLabel.visible `boolean`
{:#members:series-points-marker-datalabel-visible}




Controls the visibility of the data labels. 


#### Default Value



* false




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points: [{ marker :{dataLabel :{visible : true}}}] }]                  
});
 {% endhighlight %}


### series.points.marker.dataLabel.template `string`
{:#members:series-points-marker-datalabel-template}




Custom template to format the data label content. Use “point.x” and “point.y” as a placeholder text to display the corresponding data point’s x and y value.


#### Default Value



* ""




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{template : "item"}}}] }]                  
});
 {% endhighlight %}
 
 Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/lzjtnka5)

 
 
 
### series.points.marker.dataLabel.offset `number`
{:#members:series-points-marker-datalabel-offset}




Moves the label vertically by specified offset.


#### Default Value



* 0




#### Example


{% highlight js %}
 

$("#container").ejChart({
series :[{ points:[{ marker :{dataLabel :{offset : 10}}}] }]                  
});
 {% endhighlight %}



### series.points.marker.fill `string`
{:#members:series-points-marker-fill}




Color of the marker shape. 


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker : { fill : "green" } }] }]                  
});
{% endhighlight %}




### series.points.marker.imageUrl `string`
{:#members:series-points-marker-imageurl}




The URL for the Image that is to be displayed as marker. In order to display image as marker, set series.marker.shape as ‘image’.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{ imageUrl: "../images/sample.png"}}] }]                  
});
{% endhighlight %}




### series.points.marker.opacity `number`
{:#members:series-points-marker-opacity}




Opacity of the marker. 


#### Default Value



 * 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{ opacity : 0.5 }}] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fr1zj5v3)



### series.points.marker.shape `enum`
{:#members:series-points-marker-shape}




Specifies the shape of the marker.  


#### Default Value



* "circle". See <a href="global.html#members:shape">Shape</a>


#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{ shape: "rectangle"}] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5cgrkynp)


### series.points.marker.size `object`
{:#members:series-points-marker-size}




Options for customizing the size of the marker shape.






### series.points.marker.size.height `number`
{:#members:series-points-marker-size-height}




Height of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{size :{height : 5}}}] }]                 
});
>{% endhighlight %}




### series.points.marker.size.width `number`
{:#members:series-points-marker-size-width}




Width of the marker. 


#### Default Value



* 6




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{ size :{ width : 2 } } }] }]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hcnmls5c)


### series.points.marker.visible `boolean`
{:#members:series-points-marker-visible}




Controls the visibility of the marker shape. 


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ marker :{ visible : true}}] }]                  
});
{% endhighlight %}




### series.points.open `number`
{:#members:series-points-open}




Open value of the point. This is applicable only for financial type series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ open : 30 }] }]                  
});
{% endhighlight %}




### series.points.text `string` 
{:#members:series-points-text}




Datalabel text for the point.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ text : "20%" }] }]                  
});
{% endhighlight %}




### series.points.x `number`
{:#members:series-points-x}




X value of the point.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ x : 1 }] }]                  
});
{% endhighlight %}




### series.points.y `number`
{:#members:series-points-y}




Y value of the point.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{ points:[{ y : 20 }] }]                  
});
{% endhighlight %}




### series.pyramidMode `enum`
{:#members:series-pyramidmode}




Specifies the mode of the pyramid series.


#### Default Value



* "linear"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{pyramidMode : "linear" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xlnaeyog)



### series.query `object`
{:#members:series-query}




Specifies ej.Query to select data from dataSource. This property is applicable only when the dataSource is ej.DataManager.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
var query =  ej.Query().from("Orders").take(10);
$("#container").ejChart({
series : [{query: query }]                   
});
{% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5ffbprmm)



### series.startAngle `number`
{:#members:series-startangle}




Start angle from where the pie/doughnut series renders. It starts from 0, by default.


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
series : [{startAngle: 140 }]                   
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/cw1zlin3)


### series.tooltip `object`
{:#members:series-tooltip}




Options for customizing the tooltip of chart.






### series.tooltip.border `object`
{:#members:series-tooltip-border}




Options for customizing the border of the tooltip.






### series.tooltip.border.color `string`
{:#members:series-tooltip-border-color}




Border Color of the tooltip.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : {border : { color :"green"} }]                   
});
 {% endhighlight %}




### series.tooltip.border.width `number`
{:#members:series-tooltip-border-width}




Border Width of the tooltip.


#### Default Value



 * 1




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : {border : { width :2} }]                   
});
 {% endhighlight %}




### series.tooltip.duration `string`
{:#members:series-tooltip-duration}




Specifies the duration, the tooltip has to be displayed.


#### Default Value



* "500ms"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : { duration: "300ms" }]                   
});
 {% endhighlight %}




### series.tooltip.enableAnimation `boolean`
{:#members:series-tooltip-enableanimation}




Enables/disables the animation of the tooltip when moving from one point to another.


#### Default Value



* true




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : { enableAnimation: false }]                   
});
 {% endhighlight %}




### series.tooltip.fill `string`
{:#members:series-tooltip-fill}




Background color of the tooltip.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : {fill : "green"} }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xz1asbhm)



### series.tooltip.format `string`
{:#members:series-tooltip-format}




Format of the tooltip content.



#### Default Value



* "#point.x# : #point.y#"




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : {format : "#point.x# : #point.y#"} }]                   
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ykkxirn1)


### series.tooltip.opacity `number`
{:#members:series-tooltip-opacity}




Opacity of the tooltip.


#### Default Value



 * 0.95




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : { opacity: 0.5 }]                   
});
 {% endhighlight %}




### series.tooltip.template `string`
{:#members:series-tooltip-template}




Custom template to format the tooltip content. Use “point.x” and “point.y” as a placeholder text to display the corresponding data point’s x and y value.


#### Default Value



* null




#### Example


{% highlight js %}
 
 <div id="item" style="display: none;"> 
    <div>
       <div>#point.x#</div>
        <div>#point.y#</div>
       </div>       
 </div>


$("#container").ejChart({
series : [{ tooltip: { template : "item" }}]                  
});
 {% endhighlight %}



Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/j0twqmow)



### series.tooltip.visible `boolean`
{:#members:series-tooltip-visible}




Controls the visibility of the tooltip.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{tooltip : {visible : true} }]                   
});
 {% endhighlight %}




### series.type `enum`
{:#members:series-type}




Specifies the type of the series to render in chart.


#### Default Value



* "column". see <a href="global.html#members:type">Type</a>



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{type : "column" }]                   
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xab3pr0x)


### series.visibility `string`
{:#members:series-visibility}




Controls the visibility of the series.



#### Default Value



 * "visible"




#### Example


{% highlight js %}
 

$("#container").ejChart({
series : [{visibility: "hidden" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/mg5325qz)


### series.xAxisName `string`
{:#members:series-xaxisname}




Specifies the name of the x-axis that has to be associated with this series. Add an axis instance with this name to axes collection.


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
series : [{xAxisName: "xAxis" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hz4rz01v)


### series.xName `string`
{:#members:series-xname}




Name of the property in the datasource that contains x value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 

$("#container").ejChart({
series : [{xName: "XValue" }]                   
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/5ffbprmm)


### series.yAxisName `string`
{:#members:series-yaxisname}




Specifies the name of the y-axis that has to be associated with this series. Add an axis instance with this name to axes collection.


#### Default Value



* null




#### Example


{% highlight js %}
 

$("#container").ejChart({
series : [{yAxisName: "yAxis" }]                   
});
 {% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xn2uktf2)



### series.yName `string`
{:#members:series-yname}




Name of the property in the datasource that contains y value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{yName: "YValue" }]                   
});
{% endhighlight %}




### series.high `string`
{:#members:series-high}




Name of the property in the datasource that contains high value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{high: "high" }]                   
});
{% endhighlight %}




### series.low `string`
{:#members:series-low}




Name of the property in the datasource that contains low value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{low: "low" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pqshst44)



### series.open `string`
{:#members:series-open}




Name of the property in the datasource that contains open value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{open: "oepn" }]                   
});
{% endhighlight %}



### series.close `string`
{:#members:series-close}


Name of the property in the datasource that contains close value for the series.


#### Default Value



 * null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{close: "close" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/pqshst44)


### series.size `string`
{:#members:series-size}




Name of the property in the datasource that contains the size value for the bubble series.


#### Default Value



* null




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series : [{size: "size" }]                   
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/xsmhbrfn)


### series.trendlines `array`
{:#members:series-trendlines}




Option to add trendlines to chart.




### series.trendlines.visibility `boolean`
{:#members:series-trendlines-visibility}




Show/hides the trendline.


#### Default Value



* ""




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ visibility:'visible' }]}]                  
});
{% endhighlight %}





### series.trendlines.type `string`
{:#members:series-trendlines-type}




Specifies the type of trendline for the series.


#### Default Value



* "linear". See <a href="global.html#members:trendlinestype">TrendlinesType</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ type:'linear' }]}]                  
});
{% endhighlight %}



### series.trendlines.name `string`
{:#members:series-trendlines-name}




Name for the trendlines that is to be displayed in legend text.


#### Default Value



* "Trendline"



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ name:'Trendline' }]}]                  
});
{% endhighlight %}




### series.trendlines.fill `string`
{:#members:series-trendlines-fill}




Fill color of the trendlines.


#### Default Value



* "#0000FF"



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ fill:'#0000FF' }]}]                  
});
{% endhighlight %}




### series.trendlines.width `number`
{:#members:series-trendlines-width}




Width of the trendlines.


#### Default Value



* 1



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ width:1 }]}]                  
});
{% endhighlight %}



### series.trendlines.opacity `number`
{:#members:series-trendlines-opacity}




Opacity of the trendline.


#### Default Value



* 1



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ opacity:1 }]}]                  
});
{% endhighlight %}




### series.trendlines.dashArray `string`
{:#members:series-trendlines-dasharray}




Pattern of dashes and gaps used to stroke the trendline.


#### Default Value



* ""



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ dashArray:"" }]}]                  
});
{% endhighlight %}



### series.trendlines.forwardForecast `string`
{:#members:series-trendlines-forwardforecast}




Future trends of the current series.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ forwardForeCast:2 }]}]                  
});
{% endhighlight %}



### series.trendlines.backwardForecast `string`
{:#members:series-trendlines-backwardforecast}




Past trends of the current series.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ backwardForeCast:2 }]}]                  
});
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/d3gntcp0)



### series.trendlines.polynomialOrder `string`
{:#members:series-trendlines-polynomialorder}




Specifies the order of polynomial trendlines.


#### Default Value



* 0



#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{trendlines:[{ polynomialOrder:2 }]}]             
});
{% endhighlight %}

Try it: [JS Playground Sample](/http://jsplayground.syncfusion.com/gdpriupt)



### series.highlightsettings `object`
{:#members:series-highlightsettings}




Options for customizing the appearance of the series or data point while highlighting.




### series.highlightSettings.enable `boolean`
{:#members:series-highlightsettings-enable}




Enables/disables the ability to highlight series or data point interactively.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{enable:true}}]                  
});
{% endhighlight %}



### series.highlightSettings.mode `enum`
{:#members:series-highlightsettings-mode}




Specifies whether series or data point has to be highlighted.


#### Default Value



* "series". See <a href="global.html#members:mode">Mode</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{mode:"point"}}]                  
});
{% endhighlight %}



### series.highlightSettings.color `string`
{:#members:series-highlightsettings-color}




Color of the series/point on highlight.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{color:"red"}}]                  
});
{% endhighlight %}



### series.highlightSettings.opacity `number`
{:#members:series-highlightsettings-opacity}




Opacity of the series/point on highlight.


#### Default Value



* 0.6

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{opacity:1}}]                  
});
{% endhighlight %}



### series.highlightSettings.border `object`
{:#members:series-highlightsettings-border}



Options for customizing the border of series on highlight.



### series.highlightSettings.border.color `string`
{:#members:series-highlightsettings-border-color}



Border color of the series/point on highlight.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{border:{color:"black"}}}]                  
});
{% endhighlight %}



### series.highlightSettings.border.width `string`
{:#members:series-highlightsettings-border-width}



Border width of the series/point on highlight.


#### Default Value



* 2

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{border:{width:1}}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/ormhp3rz)


### series.highlightSettings.pattern `string`
{:#members:series-highlightsettings-pattern}




Specifies the pattern for the series/point on highlight.

#### Default Value



* "none". See <a href="global.html#members:pattern">Pattern</a>

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{pattern:"chessboard"}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/gcdopi4d)



### series.highlightSettings.customPattern `string`
{:#members:series-highlightsettings-custompattern}




Custom pattern for the series on highlight.

#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{highlightSettings:{customPattern:""}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/zmumutbx)



### series.selectionSettings `object`
{:#members:series-selectionsettings}




Options for customizing the appearance of the series/data point on selection.



### series.selectionSettings.enable `boolean`
{:#members:series-selectionsettings-enable}




Enables/disables the ability to select a series/data point interactively.


#### Default Value



* false




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{enable:true}}]                  
});
{% endhighlight %}



### series.selectionSettings.mode `enum`
{:#members:series-selectionsettings-mode}




Specifies whether series or data point has to be selected.


#### Default Value



* "series". See <a href="global.html#members:mode">Mode</a>




#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{mode:"point"}}]                  
});
{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/f0udmdts)



### series.selectionSettings.color `string`
{:#members:series-selectionsettings-color}




Color of the series/point on selection.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{color:"red"}}]                  
});
{% endhighlight %}



### series.selectionSettings.opacity `number`
{:#members:series-selectionsettings-opacity}




Opacity of the series/point on selection.


#### Default Value



* 0.6

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{opacity:1}}]                  
});
{% endhighlight %}


### series.selectionSettings.border `object`
{:#members:series-selectionsettings-border}



Options for customizing the border of series on selection.



### series.selectionSettings.border.color `string`
{:#members:series-selectionsettings-border-color}



Border color of the series/point on selection.


#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{border:{color:"black"}}}]                  
});
{% endhighlight %}



### series.selectionSettings.border.width `string`
{:#members:series-selectionsettings-border-width}



Border width of the series/point on selection.


#### Default Value



* 2

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{border:{width:1}}}]                  
});
{% endhighlight %}



### series.selectionSettings.pattern `string`
{:#members:series-selectionsettings-pattern}




Specifies the pattern for the series/point on selection.

#### Default Value



* "none". See <a href="global.html#members:pattern">Pattern</a>

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{pattern:"chessboard"}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/cuee3fgt)


### series.selectionSettings.customPattern `string`
{:#members:series-selectionsettings-custompattern}



Custom pattern for the series on selection.

#### Default Value



* ""

 

#### Example


{% highlight js %}
 
 
$("#container").ejChart({
series :[{selectionSettings:{customPattern:""}}]                  
});
{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wlovhaqi)




### sideBySideSeriesPlacement `boolean`
{:#members:sidebysideseriesplacement}




Controls whether data points has to be displayed side by side or along the depth of the axis. 


#### Default Value



* false




#### Example


{% highlight js %}
 
$("#container").ejChart({
    
        sideBySideSeriesPlacement : true
             
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/lhtjjczw)


### size `object
{:#members:size}




Options to customize the Chart size.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/wpvk5t3p)




### size.height `string`
{:#members:size-height}




Height of the Chart. Height can be specified in either pixel or percentage.


#### Default Value

* '450'




#### Example


{% highlight js %}
 
$("#container").ejChart({

   size :{height : '80%'}          

});

{% endhighlight %}




### size.width `string`
{:#members:size-width}




Width of the Chart. Width can be specified in either pixel or percentage.


#### Default Value

* '450'




#### Example


{% highlight js %}
 
$("#container").ejChart({

   size :{width : '80%'}          

});

{% endhighlight %}




### theme `enum`
{:#members:theme}




Specifies the theme for Chart.


#### Default Value

* "Flatlight". See <a href="global.html#members:theme">Theme</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   theme : "flatdark"            

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/jael2rfm)




### tilt `number`
{:#members:tilt}




Slope angle of 3D Chart. This property is applicable only when 3D view is enabled.


#### Default Value



* 0




#### Example


{% highlight js %}
 
$("#container").ejChart({

      tilt : 5
             
});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/p0cd1lvx)




### title `object`
{:#members:title}




Options for customizing the title and subtitle of Chart.




### title.font `object`
{:#members:title-font}




Options for customizing the font of Chart title.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/fhtgy2vx)




### title.font.fontFamily `string`
{:#members:title-font-fontfamily}




Font family for Chart title.


#### Default Value

* "Segoe UI"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { font : { fontFamily : "Algerian" } }                     

});

{% endhighlight %}




### title.font.fontStyle `enum`
{:#members:title-font-fontstyle}




Font style for Chart title.


#### Default Value

* "Normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { font : { fontStyle : "italic" } }                     

});

{% endhighlight %}




### title.font.fontWeight `enum`
{:#members:title-font-fontweight}




Font weight for Chart title.


#### Default Value

* "Regular". See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { font : { fontWeight : "lighter" } }                     

});

{% endhighlight %}




### title.font.opacity `number`
{:#members:title-font-opacity}




Opacity of the Chart title.


#### Default Value

* 0.5




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { font : { opacity : 0.8 } }                     

});

{% endhighlight %}




### title.font.size `string`
{:#members:title-font-size}




Font size for Chart title.


#### Default Value

* "20px"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { font : { size : "22px" } }                     

});

{% endhighlight %}




### title.subTitle `object`
{:#members:title-subtitle}




Options to customize the sub title of Chart.




### title.subTitle.font `object`
{:#members:title-subtitle-font}




Options for customizing the font of sub title.


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/vq3sp2j2)




### title.subTitle.font.fontFamily `string`
{:#members:title-subtitle-font-fontfamily}




Font family of sub title.


#### Default Value

* "Segoe UI"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: {subTitle : {font :{ fontFamily : "Algerian" } } }                      

});

{% endhighlight %}




### title.subTitle.font.fontStyle `enum`
{:#members:title-subtitle-font-fontstyle}




Font style for sub title.


#### Default Value

* "Normal". See <a href="global.html#members:fontstyle">FontStyle</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle : {font :{ fontStyle : "Normal" } } }                     

});

{% endhighlight %}




### title.subTitle.font.fontWeight `enum` 
{:#members:title-subtitle-font-fontweight}




Font weight for sub title.


#### Default Value

* "Regular". See <a href="global.html#members:fontweight">FontWeight</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle : {font :{ fontWeight : "regular" } } }                     

});

{% endhighlight %}




### title.subTitle.font.opacity `double`
{:#members:title-subtitle-font-opacity}




Opacity of the sub title.


#### Default Value

* 1




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle : {font :{ opacity : 0.5 } } }                     

});

{% endhighlight %}




### title.subTitle.font.size `enum`
{:#members:title-subtitle-font-size}




Font size for sub title.


#### Default Value

* "12px"




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle : {font :{ size : "14px" } } }                     

});

{% endhighlight %}




### title.subTitle.text `string`
{:#members:title-subtitle-text}




Text to be displayed in sub title.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle: { text : "Performace chart" } }                      

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/e3thfz5p)




### title.subTitle.textAlignment `enum`
{:#members:title-subtitle-textalignment}




Alignment of sub title text.


#### Default Value

* "far". See <a href="global.html#members:textalignment">TextAlignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title: { subTitle: { textAlignment : "near" } }                      

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/yh1hzrly)




### title.text `string`
{:#members:title-text}




Text to be displayed in Chart title.


#### Default Value

* ""




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { text : "Power Production"}                     

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/rk0x1e5u)




### title.textAlignment `enum`
{:#members:title-textalignment}




Alignment of the title text.


#### Default Value

* "Center". See <a href="global.html#members:textalignment">TextAlignment</a>




#### Example


{% highlight js %}
 
$("#container").ejChart({

   title : { textAlignment : "near"}                     

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/p1vsex5m)




### wallSize `number`
{:#members:wallsize}




Width of the wall used in 3D Chart. Wall is present only in Cartesian type 3D series and not in 3D pie or Doughnut series. This property is applicable only when 3D view is enabled.


#### Default Value



* 2




#### Example


{% highlight js %}
 
$("#container").ejChart({

      wallSize : 5
             
});

{% endhighlight %}

Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/q4nv04rw)




### zooming `object`
{:#members:zooming}




Options for enabling zooming feature of chart.






### zooming.enable `boolean`
{:#members:zooming-enable}




Enables or disables zooming.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   zooming :{enable :true}          

});

{% endhighlight %}




### zooming.enableDeferredZoom `boolean`
{:#members:zooming-enabledeferredzoom}




Enable or disables the differed zooming. When it is enabled, chart is updated only on mouse up action while zooming and panning.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   zooming:{enableDeferredZoom : true}            

});

{% endhighlight %}




### zooming.enableMouseWheel `boolean`
{:#members:zooming-enablemousewheel}




Enables/disables the ability to zoom the chart on moving the mouse wheel.


#### Default Value

* false




#### Example


{% highlight js %}
 
$("#container").ejChart({

   zooming:{enableMouseWheel : true}            

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/0gkvnyi3)




### zooming.type `string`
{:#members:zooming-type}




Specifies whether to allow zooming the chart vertically or horizontally or in both ways.


#### Default Value

* 'x,y'




#### Example


{% highlight js %}
 
$("#container").ejChart({

   zooming :{type : "y"}            

});

{% endhighlight %}


Try it: [JS Playground Sample](http://jsplayground.syncfusion.com/hqmmhpgk)




## Methods




### animate(options)
{:#methods:animate}




Animates the series and/or indicators in Chart. When parameter is not passed to this method, then all the series and indicators present in Chart are animated.

Following are the parameters that you can pass to this method.


<table class="params">
<thead>
<tr>
<th>Parameters</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">options</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Series and indicator objects passed in the array collection are animated.
<br/><br./>
Example

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
//animating series array
chartObj.animate(chartObj.model.series);
{% endhighlight %}
</td>
</tr>
<tr>
<td class="name">option</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Series or indicator object passed to this method are animated.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
//animating a specific indicator
chartObj.animate(chartObj.model.indicators[0]);
{% endhighlight %}
</td>
</tr>
</tbody>
</table>




### export(type, url, exportMultipleChart)
{:#methods:export}




Exports chart as an image or to an excel file. Chart can be exported as an image only when exportCanvasRendering option is set to true.

Following are the parameters that you can pass to this method,


<table class="params">
<thead>
<tr>
<th>Parameters</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Type of the export operation to be performed. Following are the two export types that are supported now,
<br/>
1. 'image'
2. 'excel'
<br/><br./>
Example

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export(‘image’);
{% endhighlight %}
</td>
</tr>
<tr>
<td class="name">url</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">
URL of the service, where the chart will be exported to excel.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export("excel", 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport')
{% endhighlight %}
</td>
</tr>
<tr>
<td class="name">
exportMultipleChart</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">
When this parameter is true, all the chart objects initialized to the same document are exported to a single excel file. This is an optional parameter. By default, it is false.
<br/><br/>
Example,

{% highlight js %}
var chartObj  = $("#container").data("ejChart");
chartObj.export("excel", 'http://js.syncfusion.com/ExportingServices/api/JSChartExport/ExcelExport', true)
{% endhighlight %}
</td>
</tr>
</tbody>
</table>




### redraw()
{:#methods:redraw}




Redraws the entire chart. You can call this method whenever you update, add or remove points from the data source or whenever you want to refresh the UI.



#### Example


{% highlight js %}
// Redraw Chart
var chartObj = $("#container").data("ejChart");
chartObj.redraw();
{% endhighlight %}


{% highlight js %}
 
$("#container").ejChart("redraw");      
{% endhighlight %}



## Events




### animationComplete
{:#events:animationcomplete}




Fires after the series animation is completed. This event will beis triggered for each series when animation is enabled.

Example:
{:.example}


{% highlight js %}

//animationComplete event for chart

$("#container").ejChart({

     animationComplete: function (argument) {
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
argument.data.series{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the series that completed has animation.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### axesLabelRendering
{:#events:axeslabelrendering}




Fires before rendering the labels. This event is fired for each label in axis. You can use this event to add custom text to axis labels.

#### Example


{% highlight js %}
 
//axesLabelRendering event for chart

$("#container").ejChart({

    axesLabelRendering: function (args) {
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
argument.Axis{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the corresponding axis.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.Label.Text{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">Formatted text of the respective label. You can also add custom text to the label.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.Label.Value{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">Actual value of the label.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>



### axesLabelsInitialize
{:#events:axeslabelsinitialize}




Fires during the initialization of axis labels.


#### Example


{% highlight js %}
 
//axesLabelsInitialize event for chart

$("#container").ejChart({

    axesLabelsInitialize: function (args) {
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
argument.data.axes{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Collection of axes in Chart</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### axesRangeCalculate
{:#events:axesrangecalculate}




Fires during axes range calculation. This event is fired for each axis present in Chart. You can use this event to customize axis range as required.

#### Example


{% highlight js %}
 
//axesRangeCalculate event for chart

$("#container").ejChart({

      axesRangeCalculate: function (args) {
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
argument.data.range.delta{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Difference between minimum and maximum value of axis range.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.range.interval{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Interval value of axis range. Grid lines, tick lines and axis labels are drawn based on this interval value.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.range.max{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Maximum value of axis range.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.range.min{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Minimum value of axis range.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### axesTitleRendering
{:#events:axestitlerendering}




Fires before rendering the axis title. This event is triggered for each axis with title. You can use this event to add custom text to axis title.


#### Example


{% highlight js %}
 
//axesTitleRendering event for chart

$("#container").ejChart({

     axesTitleRendering: function (args) {
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
argument.data.axes{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the axis whose title is being rendered</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.x{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of title location</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.y{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of title location</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.title{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Axis title text. You can add custom text to the title.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### chartAreaBoundsCalculate
{:#events:chartareaboundscalculate}




Fires during the calculation of chart area bounds. You can use this event to customize the bounds of chart area.


#### Example


{% highlight js %}
 
//chartAreaBoundsCalculate event for chart

$("#container").ejChart({

    chartAreaBoundsCalculate: function (args) {
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
argument.data.areaBounds.Height{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Height of the chart area.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.areaBounds.Width{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Width of the chart area.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.areaBounds.X{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of the chart area.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.areaBounds.Y{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of the chart area.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### create
{:#events:create}




Fires after chart is created.



#### Example


{% highlight js %}
 
//Create event for chart

$("#container").ejChart({

     create: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>




### destroy
{:#events:destroy}




Fires when chart is destroyed completely.



#### Example


{% highlight js %}
 
//Destroy event for chart

$("#container").ejChart({

     destroy: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>




### displayTextRendering
{:#events:displaytextrendering}




Fires before rendering the data labels. This event is triggered for each data label in the series. You can use this event to add custom text in data labels.


#### Example


{% highlight js %}
 
//displayTextRendering event for chart

$("#container").ejChart({

    displayTextRendering: function (args) {
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
argument.data.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text displayed in data label. You can add custom text to the data label</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.x{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of data label location</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.y{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of data label location</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.seriesIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the series in series Collection whose data label is being rendered </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point in series whose data label is being rendered </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>



### legendBoundsCalculate
{:#events:legendboundscalculate}




Fires during the calculation of legend bounds. You can use this event to customize the bounds of legend.

#### Example


{% highlight js %}
 
//legendBoundsCalculate event for chart

$("#container").ejChart({

     legendBoundsCalculate: function (args) {
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
argument.data.legendBounds.Height{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Height of the legend.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendBounds.Width{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Width of the legend.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data. legendBounds.Rows{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Number of rows to display the legend items</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### legendItemClick
{:#events:legenditemclick}




Fires on clicking the legend item. 


#### Example


{% highlight js %}
 
//legendItemClick event for chart

$("#container").ejChart({

     legendItemClick: function (args) {
              //Do something
     }
     
});{% endhighlight %}



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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.location.startX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.location.startY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.LegendItem{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the legend item object that is about to be rendered</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.style{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Options to customize the legend item styles such as border, color, size, etc…,</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.Bounds{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance that holds information about legend bounds and legend item bounds.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.symbolShape{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the legend item shape. Use this option to customize legend item shape before rendering</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.series{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the series object corresponding to the legend item</td>
</tr>
</tbody>
</table>


### legendItemMouseMove
{:#events:legenditemmousemove}




Fires when moving mouse over legend item. You can use this event for hit testing on legend items.

#### Example


{% highlight js %}
 
//legendItemMouseMove event for chart

$("#container").ejChart({

    legendItemMouseMove: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.location.startX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.location.startY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.LegendItem{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the legend item object that is about to be rendered</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.style{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Options to customize the legend item styles such as border, color, size, etc…,</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.Bounds{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Options to customize the legend item styles such as border, color, size, etc…,</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem.symbolShape{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the legend item shape. Use this option to customize legend item shape before rendering</td>
</tr>
<tr>
<td class="name">{% highlight js %}
Argument.data.legendItem.series{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the series object corresponding to the legend item</td>
</tr>
</tbody>
</table>



### legendItemRendering
{:#events:legenditemrendering}




Fires before rendering the legend item. This event is fired for each legend item in Chart. You can use this event to customize legend item shape or add custom text to legend item.


#### Example


{% highlight js %}
 
//legendItemRendering event for chart

$("#container").ejChart({

    legendItemRendering: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.startX{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.startY{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of legend item in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.legendItem{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the legend item object that is about to be rendered</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.style{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Options to customize the legend item styles such as border, color, size, etc.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the chart model object.</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.symbolShape{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the legend item shape. Use this option to customize legend item shape before rendering</td>
</tr>
</tbody>
</table>



### load
{:#events:load}




Fires before loading the chart.


#### Example


{% highlight js %}
 
//load event for chart

$("#container").ejChart({

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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### pointRegionClick
{:#events:pointregionclick}




Fires on clicking a point in chart. You can use this event to handle clicks made on points.

#### Example


{% highlight js %}
 
//pointRegionClick event for chart

$("#container").ejChart({

    pointRegionClick: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.x{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.y{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.region.Region.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point in series</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.region.Region.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the series in series collection to which the point belongs</td>
</tr>
</tbody>
</table>


### pointRegionMouseMove
{:#events:pointregionmousemove}




Fires when mouse is moved over a point. 

#### Example


{% highlight js %}
 
//pointRegionMouseMove event for chart

$("#container").ejChart({

    pointRegionMouseMove: function (args) {
                  //Do something
    }
   
});{% endhighlight %}


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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.x{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">X-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location.y{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Y-coordinate of point in pixel</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.region.Region.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point in series</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.region.seriesIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the series in series collection to which the point belongs</td>
</tr>
</tbody>
</table>


### preRender
{:#events:prerender}




Fires before rendering chart. 


#### Example


{% highlight js %}
 
//preRender event for chart

$("#container").ejChart({

    preRender: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
</tbody>
</table>


### seriesRegionClick
{:#events:seriesregionclick}




Fires after selecting a series. This event is triggered after selecting a series only if selection mode is series.

#### Example


{% highlight js %}
 
//seriesRendering event for chart

$("#container").ejChart({

    seriesRegionClick: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.series{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the selected series</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.seriesIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the selected series</td>
</tr>
</tbody>
</table>


### seriesRendering
{:#events:seriesrendering}




Fires before rendering a series. This event is fired for each series in Chart.

#### Example


{% highlight js %}
 
//seriesRendering event for chart

$("#container").ejChart({

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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.series{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance of the series which is about to get rendered</td>
</tr>
</tbody>
</table>


### symbolRendering
{:#events:symbolrendering}




Fires before rendering the marker symbols. This event is triggered for each marker in Chart.

#### Example


{% highlight js %}
 
//symbolRendering event for chart

$("#container").ejChart({
 
    symbolRendering: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Instance that holds the location of marker symbol</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.style{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Options to customize the marker style such as color, border and size</td>
</tr>
</tbody>
</table>


### titleRendering
{:#events:titlerendering}




Fires before rendering the Chart title. You can use this event to add custom text in Chart title.


#### Example


{% highlight js %}
 
//titleRendering event for chart

$("#container").ejChart({

    titleRendering: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Option to customize the title location in pixels</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.size{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Read-only option to find the size of the title</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.title{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Use this option to add custom text in title</td>
</tr>
</tbody>
</table>


### toolTipInitialize
{:#events:tooltipinitialize}




Fires before rendering the tooltip. This event is fired when tooltip is enabled and mouse is hovered on a Chart point. You can use this event to customize tooltip before rendering.

#### Example


{% highlight js %}
 
//toolTipInitialize event for chart
 
$("#container").ejChart({

    toolTipInitialize: function (args) {
              //Do something
    }
    
});{% endhighlight %}



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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.currentText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text to be displayed in tooltip. Set this option to customize the text displayed in tooltip</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point on which mouse is hovered</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.seriesIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the series in series collection whose point is hovered by mouse</td>
</tr>
</tbody>
</table>


### trackAxisToolTip
{:#events:trackaxistooltip}




Fires before rendering crosshair tooltip in axis. This event is fired for each axis with crosshair label enabled. You can use this event to customize crosshair label before rendering


#### Example


{% highlight js %}
 
//trackAxisToolTip event for chart

$("#container").ejChart({

    trackAxisToolTip: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Location of the crosshair label in pixels</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.axisIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the axis for which crosshair label is displayed</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.crossAxis{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Instance of the chart axis object for which cross hair label is displayed</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.currentTrackText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text to be displayed in crosshair label. Use this option to add custom text in crosshair label</td>
</tr>
</tbody>
</table>


### trackToolTip
{:#events:tracktooltip}




Fires before rendering trackball tooltip. This event is fired for each series in Chart because trackball tooltip is displayed for all the series. You can use this event to customize the text displayed in trackball tooltip.


#### Example


{% highlight js %}
 
//trackToolTip event for chart

$("#container").ejChart({

    trackToolTip: function (args) {
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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set this option to true to cancel the event    </td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the chart model object</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Name of the event</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.location{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Location of the trackball tooltip in pixels</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.pointIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the point for which trackball tooltip is displayed</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.seriesIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index of the series in series collection</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.currentText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Text to be displayed in trackball tooltip. Use this option to add custom text in trackball tooltip</td>
</tr>
<tr>
<td class="name">{% highlight js %}
argument.data.series{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Instance of the series object for which trackball tooltip is displayed.</td>
</tr>
</tbody>
</table>



