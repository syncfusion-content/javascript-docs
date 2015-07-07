---
layout: post
title: ejChart
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Chart.

The chart can be easily configured to the DOM element, such as div. you can create a grid with a highly customizable look and feel.





$(element).ejChart<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Chart
$('#container').ejChart();      
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery.js

* module:ej.core.js

* module:ej.data.js

* module:ej.chart.js

* module:jQuery.globalize.js


## Members




### annotations<span class="type-signature type array">array</span>
{:#annotations}




Contains properties for customizing the annotations in chart.






### annotations.angle<span class="type-signature type number">number</span>
{:#annotations-angle}




Annotataion takes the specified value as angle for rotating it


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ angle : 45}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.content<span class="type-signature type string">string</span>
{:#annotations-content}




Specifies the content /element which is to be displayed as annotation


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ content :"Template"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.coordinateUnit<span class="type-signature type enum">enum</span>
{:#annotations-coordinateUnit}




Specifies the option based on which annotation is placed on the chart


Default Value:
{:.param}



* "none"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ coordinateUnit :"pixels"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.horizontalAlignment<span class="type-signature type enum">enum</span>
{:#annotations-horizontalAlignment}




To position the annotation horizontally


Default Value:
{:.param}



* "middle"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ horizontalAlignment :"left"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.margin<span class="type-signature type object">object</span>
{:#annotations-margin}




Contains property to customize the margin values of annotation






### annotations.margin.bottom<span class="type-signature type number">number</span>
{:#annotations-margin-bottom}




Specifies the bottom margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ margin :{ bottom:10}}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.margin.left<span class="type-signature type number">number</span>
{:#annotations-margin-left}




Specifies the left margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ margin :{ left:10}}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.margin.right<span class="type-signature type number">number</span>
{:#annotations-margin-right}




Specifies the right margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ margin :{ right:10}}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.margin.top<span class="type-signature type number">number</span>
{:#annotations-margin-top}




Specifies the top margin value for annotation


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ margin :{ top:10}}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.opacity<span class="type-signature type number">number</span>
{:#annotations-opacity}




Annotataion takes the specified value as opacity


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ opacity : 0.5}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.region<span class="type-signature type enum">enum</span>
{:#annotations-region}




To place the annotation with respect to chart / series


Default Value:
{:.param}



* "chart"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ region :"series"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.verticalAlignment<span class="type-signature type enum">enum</span>
{:#annotations-verticalAlignment}




To position the annotation vertically


Default Value:
{:.param}



* "middle"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ verticalAlignment :"top"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.visible<span class="type-signature type boolean">boolean</span>
{:#annotations-visible}




Specifies the visibility of annotation.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ visible :true}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.x<span class="type-signature type number">number</span>
{:#annotations-x}




Annotataion takes the specified x value


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ x : 100}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.xAxisName<span class="type-signature type string">string</span>
{:#annotations-xAxisName}




Binds annotation to the specified axis


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ xAxisName : "xAxis1"}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.y<span class="type-signature type number">number</span>
{:#annotations-y}




Annotataion takes the specified y value


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ y : 100}]                    
});
&lt;/script&gt;  </code>
</pre>



### annotations.yAxisName<span class="type-signature type string">string</span>
{:#annotations-yAxisName}




Binds annotation to the specified axis


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
annotations :[{ yAxisName : "yAxis1"}]                    
});
&lt;/script&gt;  </code>
</pre>



### backGroundImageUrl<span class="type-signature type string">string</span>
{:#backGroundImageUrl}




Specifies the background image path to display the image, plotting in the chart background.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
   backGroundImageUrl: "../images/chart/wheat.png"                      
});
&lt;/script&gt; </code>
</pre>



### border<span class="type-signature type object">object</span>
{:#border}




Options for customizing the color, opacity and width of the border of chart.






### border.color<span class="type-signature type string">string</span>
{:#border-color}




Specifies the border color of the chart.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>                             
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
   border: { color: "green" }                      
});
&lt;/script&gt;                </code>
</pre>



### border.opacity<span class="type-signature type number">number</span>
{:#border-opacity}




Specifies the border opacity of the chart


Default Value:
{:.param}



* 0.3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
   border: { opacity: 0.5 }                      
});
&lt;/script&gt; </code>
</pre>



### border.width<span class="type-signature type number">number</span>
{:#border-width}




Specifies the border width of the chart.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
   border: { width: 2 }                      
});
&lt;/script&gt; </code>
</pre>



### canResize<span class="type-signature type boolean">boolean</span>
{:#canResize}




Sets a value whether to make the chart responsive on resize.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
canResize : true             
});
&lt;/script&gt;</code>
</pre>



### chartArea<span class="type-signature type object">object</span>
{:#chartArea}




Specifies options for configuring the border and background for chart plotting area.






### chartArea.background<span class="type-signature type string">string</span>
{:#chartArea-background}




Specifies the background for chart plotting area.


Default Value:
{:.param}



* transparent




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
    chartArea: { background : "white" }                      
});
&lt;/script&gt; </code>
</pre>



### chartArea.border<span class="type-signature type object">object</span>
{:#chartArea-border}




Options for customizing the color, opacity and width of the border of chart plotting area.






### chartArea.border.color<span class="type-signature type string">string</span>
{:#chartArea-border-color}




Specifies the border color of chart plotting area.


Default Value:
{:.param}



* Gray




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
   chartArea: { border: { color :"green"} }                      
});
&lt;/script&gt; </code>
</pre>



### chartArea.border.opacity<span class="type-signature type number">number</span>
{:#chartArea-border-opacity}




Specifies the border opacity of chart plotting area.


Default Value:
{:.param}



* 0.3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
    chartArea: { border: { opacity : 0.5} }                      
});
&lt;/script&gt; </code>
</pre>



### chartArea.border.width<span class="type-signature type number">number</span>
{:#chartArea-border-width}




Specifies the border width of chart plotting area.


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
    chartArea: { border: { width : 0.2} }                      
});
&lt;/script&gt; </code>
</pre>



### columnDefinitions<span class="type-signature type array">array</span>
{:#columnDefinitions}




You can split chart into multiple plotting areas vertically. In order to split the chart vertically, you need to specify number of column objects in columDefintions array. Each object in the columnDefnitions represent a plotting area in chart.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
 columnDefinitions :[{unit : "percentage"}]                       
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions<span class="type-signature type object">object</span>
{:#commonSeriesOptions}




Options for configuring the properties commonly for all the series. You can also override the options for specific series by setting the options directly in each series object in series array.






### commonSeriesOptions.border<span class="type-signature type object">object</span>
{:#commonSeriesOptions-border}




Options for customizing the color, opacity and width of the border of series.






### commonSeriesOptions.border.color<span class="type-signature type string">string</span>
{:#commonSeriesOptions-border-color}




Specifies the border color of series.


Default Value:
{:.param}



* "transparent"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{border :{ color : "green" } }                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.border.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-border-width}




Specifies the border width of series.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{border :{ width : 2 } }                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.dashArray<span class="type-signature type string">string</span>
{:#commonSeriesOptions-dashArray}




Controls the pattern of dashes and gaps used to stroke the line series.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{dashArray : "2,3"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.dataSource<span class="type-signature type object">object</span>
{:#commonSeriesOptions-dataSource}




Specifies the dataSource for series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions : {dataSource: data.open }                   
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.doughnutCoefficient<span class="type-signature type number">number</span>
{:#commonSeriesOptions-doughnutCoefficient}




Sets the radius of the hole on the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.4




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ doughnutCoefficient : 0.5}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.doughnutSize<span class="type-signature type number">number</span>
{:#commonSeriesOptions-doughnutSize}




Sets the radius of the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ doughnutSize : 0.9}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.drawType<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-drawType}




Specifies the type of series that can be drawn in a Radar or Polar series. It supports line, column and area type. See <a href="global.html#DrawType">DrawType</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.DrawType.Line




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ drawType : "area"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-enableAnimation}




Specifies the series animation common to all series. By specifying this, we can enable/disable the animation of the series.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ enableAnimation : false}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.enableSmartLabels<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-enableSmartLabels}




Enabling this property can avoid pie series data label overlap each other.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ enableSmartLabels : false}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.endAngle<span class="type-signature type number">number</span>
{:#commonSeriesOptions-endAngle}




Specifies the ending angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ endAngle : 270}                  
});
&lt;/script&gt; ; </code>
</pre>



### commonSeriesOptions.explode<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-explode}




Explodes the pie slices on mouse move. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ explode : true}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.explodeAll<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-explodeAll}




Explodes all the pie slices. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ explodeAll : true}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.explodeIndex<span class="type-signature type number">number</span>
{:#commonSeriesOptions-explodeIndex}




Index of a slice to be exploded from the whole pie. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ explodeIndex : 2}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.explodeOffset<span class="type-signature type number">number</span>
{:#commonSeriesOptions-explodeOffset}




Represents the distance the slice has to be moved out when it is exploded.


Default Value:
{:.param}



* 0.4




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ explodeOffset : 20}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.fill<span class="type-signature type string">string</span>
{:#commonSeriesOptions-fill}




Specifies the fill color of series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{fill : "green"}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.font<span class="type-signature type object">object</span>
{:#commonSeriesOptions-font}




Specifies the font that is common to all series. These are the properties involved in customizing the font of the series in chart.






### commonSeriesOptions.font.color<span class="type-signature type string">string</span>
{:#commonSeriesOptions-font-color}




Specifies the color, that is common to all series. Text in the series, render with the specified font color.


Default Value:
{:.param}



* "#707070"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{font :{color : "green"}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.font.fontFamily<span class="type-signature type string">string</span>
{:#commonSeriesOptions-font-fontFamily}




Specifies the fontFamily, that is common to all series. Text in the series, render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ font : { fontFamily : "Algerian"}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.font.fontStyle<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-font-fontStyle}




Specifies the fontStyle, that is common to all series. Text in the series, render with the specified font style.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions : {font :{fontStyle : "italic"}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.font.fontWeight<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-font-fontWeight}




Specifies the fontWeight, that is common to all series. Text in the series, render with the specified font weight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{font :{fontWeight : "lighter"}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.font.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-font-opacity}




Specifies the opacity, that is common to all series. Text in the series, render with the specified font opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{font :{opacity : 0.5}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.font.size<span class="type-signature type string">string</span>
{:#commonSeriesOptions-font-size}




Specifies the font size, that is common to all series. Text in the series, render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{font :{size : "14px"}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.funnelHeight
{:#commonSeriesOptions-funnelHeight}




Sets the funnel height.


Default Value:
{:.param}



* "32.7%"(32.7% of actualheight)




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{funnelHeight : '40%' }]                   
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.funnelWidth
{:#commonSeriesOptions-funnelWidth}




Sets the funnel width.


Default Value:
{:.param}



* "11.6%"(11.6% of actualwidth)




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{funnelWidth : '40%' }]                   
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.gapRatio<span class="type-signature type number">number</span>
{:#commonSeriesOptions-gapRatio}




Specifies the gap between each slice of a pyramid series in pixels.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ gapRatio : 0.5}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.isClosed<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-isClosed}




Used in Polar and Radar series to specify whether the line/area series has to be rendered in a closed state by joining the start and end point of the series.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ isClosed : false}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.isStacking<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-isStacking}




Used in Polar and Radar series to specify whether column type has to be rendered the stacked value of chart.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ isStacking : "true"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.labelPosition<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-labelPosition}




Specifies the position of the axis labels to render labels either inside or outside of plot area. See <a href="global.html#LabelPosition">LabelPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelPosition.Inside




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ labelPosition : "outside"}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.lineCap<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-lineCap}




Specifies the style to draw the end point of a line like butt, round, square. See <a href="global.html#LineCap">LineCap</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineCap.Butt




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{lineCap : "butt"}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.lineJoin<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-lineJoin}




Specifies the shape to use at the intersection of two lines drawn. See <a href="global.html#LineJoin">LineJoin</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineJoin.Round




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{lineCap : "round"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker}




Contains the customizing properties to add marker symbols to the points plotted in the chart






### commonSeriesOptions.marker.border<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-border}




Options for customizing the color, opacity and width of the border of marker.






### commonSeriesOptions.marker.border.color<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-border-color}




Specifies the border color of marker.


Default Value:
{:.param}



* "white"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{color : "green"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.border.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-border-width}




Specifies the border width of marker.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{border :{width : 2}}}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-dataLabel}




Contains the customizing properties to add data labels of the points plotted in the chart.






### commonSeriesOptions.marker.dataLabel.angle<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-angle}




rotates dataLabel in the marker.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{angle : 90}}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.border<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-dataLabel-border}




Options for customizing the color, opacity and width of the border of datalabel.






### commonSeriesOptions.marker.dataLabel.border.color<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-dataLabel-border-color}




Specifies the border color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border : {color : "green"}}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.border.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-border-width}




Specifies the border width of datalabel.


Default Value:
{:.param}



* 0.1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{border :{ width :2 }}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.connectorLine<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-dataLabel-connectorLine}




Contains the options to customize the line connecting the point and the data label.






### commonSeriesOptions.marker.dataLabel.connectorLine.type<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-connectorLine-type}




Specifies whether to connect the point and data label using bezier curve or straight line. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ type : "spline" }}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.connectorLine.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-connectorLine-width}




Specifies the width of the connector line.


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{connectorLine :{ width : 2 }}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.fill<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-dataLabel-fill}




Specifies the fill color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{fill : "green"}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.font<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-dataLabel-font}




Specifies the font of the dataLabel. These are the properties involved in customizing the data label font.






### commonSeriesOptions.marker.dataLabel.font.fontFamily<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-dataLabel-font-fontFamily}




Specifies the fontFamily of dataLabel. Text in the data label render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.font.fontStyle<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-font-fontStyle}




Specifies the fontStyle of dataLabel. Text in the data label render with the specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.font.fontWeight<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-font-fontWeight}




Specifies the fontWeight of dataLabel. Text in the data label render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.font.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-font-opacity}




Specifies the opacity of the text in dataLabel. Text in the data label render with the specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font :{ opacity : 0.5 }}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.font.size<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-dataLabel-font-size}




Specifies the font size of dataLabel. Text in the data label render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{font : { size : "14px" }}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.horizontalTextAlignment<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-horizontalTextAlignment}




This property is used to change the alignment of the data label horizontally.


Default Value:
{:.param}



* ej.datavisualization.Chart.horizontalTextAlignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{horizontalTextAlignment : "far"}}}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.margin<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-dataLabel-margin}




Specifies the margin for the data label.






### commonSeriesOptions.marker.dataLabel.margin.bottom<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-margin-bottom}




Specifies the bottom margin value for dataLabel. By specifying this property, we can adjust the text in data label to bottom.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ bottom :10 }}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.margin.left<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-margin-left}




Specifies the left margin value for dataLabel. By specifying this property, we can adjust the text in data label to left.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ left : 10}}}}                 
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.dataLabel.margin.right<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-margin-right}




Specifies the right margin value for dataLabel. By specifying this property, we can adjust the text in data label to right.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ right :10 }}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.margin.top<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-margin-top}




Specifies the top margin value for dataLabel. By specifying this property, we can adjust the text in data label to top.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{margin :{ top :10 } }}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-dataLabel-opacity}




Specifies the opacity of dataLabel.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{opacity : 0.5}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.shape<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-shape}




Specifies the rendering shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{shape : "circle"}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.textPosition<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-textPosition}




This property is used to change the position of the text in data label. See <a href="global.html#TextPosition">TextPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.textPosition.Top




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{textPosition : "bottom"}}}                 
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.verticalTextAlignment<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-dataLabel-verticalTextAlignment}




This property is used to change the alignment of the data label vertically.


Default Value:
{:.param}



* ej.datavisualization.Chart.verticalTextAlignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{verticalTextAlignment : "far"}}}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.dataLabel.visible<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-marker-dataLabel-visible}




Toggles the visibility of dataLabel in the marker.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{dataLabel :{visible : true}}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.marker.fill<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-fill}




Specifies the fill color of the marker.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker : { fill : "green" } }                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.imageUrl<span class="type-signature type string">string</span>
{:#commonSeriesOptions-marker-imageUrl}




Specifies the image url location of the marker.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{ imageUrl: "../images/sample.png"}}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-opacity}




Specifies the opacity of the marker. Values ranges from 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{ opacity : 0.5 }}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.shape<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-marker-shape}




Specifies the shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.Circle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{ shape: "rectangle"}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.size<span class="type-signature type object">object</span>
{:#commonSeriesOptions-marker-size}




Specifies the size of the marker.






### commonSeriesOptions.marker.size.height<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-size-height}




Specifies the height of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{size :{height : 5}}}                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.size.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-marker-size-width}




Specifies the width of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{ size :{ width : 2 } } }                  
});
&lt;/script&gt;</code>
</pre>



### commonSeriesOptions.marker.visible<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-marker-visible}




Toggles the visibility of the marker.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{marker :{ visible : true}}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-opacity}




Specifies the opacity of series. The value ranges form 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{opacity : 0.5}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.pieCoefficient<span class="type-signature type number">number</span>
{:#commonSeriesOptions-pieCoefficient}




Sets the radius of the pie series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ pieCoefficient : 1}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.pyramidMode<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-pyramidMode}




Sets the rendering mode of the pyramid as linear or surface. See <a href="global.html#PyramidMode">PyramidMode</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.PyramidMode.Linear




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ pyramidMode : "linear"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.startAngle<span class="type-signature type number">number</span>
{:#commonSeriesOptions-startAngle}




Specifies the starting angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ startAngle : 150}                  
});
&lt;/script&gt; ; </code>
</pre>



### commonSeriesOptions.tooltip<span class="type-signature type object">object</span>
{:#commonSeriesOptions-tooltip}




Contains all the properties to customize tooltip






### commonSeriesOptions.tooltip.border<span class="type-signature type object">object</span>
{:#commonSeriesOptions-tooltip-border}




Options for customizing the color, opacity and width of the border of tooltip.






### commonSeriesOptions.tooltip.border.color<span class="type-signature type string">string</span>
{:#commonSeriesOptions-tooltip-border-color}




Specifies the border color of tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border:{ color : "green" }}}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.border.width<span class="type-signature type number">number</span>
{:#commonSeriesOptions-tooltip-border-width}




Specifies the border width of tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{border :{ width : 2}}}                  
});
&lt;/script&gt;   </code>
</pre>



### commonSeriesOptions.tooltip.duration<span class="type-signature type string">string</span>
{:#commonSeriesOptions-tooltip-duration}




Specifies the duration of the tooltip to stay awake.


Default Value:
{:.param}



* "500ms"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{duration : "300ms"}}                  
});
&lt;/script&gt;   </code>
</pre>



### commonSeriesOptions.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-tooltip-enableAnimation}




Enabling this property animates the tooltip on moving the cursor from one point to the other.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{enableAnimation : false}}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.fill<span class="type-signature type string">string</span>
{:#commonSeriesOptions-tooltip-fill}




Specifies the fill color of the tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{fill : "green"}}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.format<span class="type-signature type string">string</span>
{:#commonSeriesOptions-tooltip-format}




Formatting the values of point on a tooltip can be customized using this property.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ tooltip : { format : "#point.x# : #point.y#%" } }                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.opacity<span class="type-signature type number">number</span>
{:#commonSeriesOptions-tooltip-opacity}




Specifies the opacity of the tooltip. Values ranges from 0 to 1.


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{tooltip :{opacity : 0.5}}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.template<span class="type-signature type string">string</span>
{:#commonSeriesOptions-tooltip-template}




Specify the template for tooltip


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ tooltip: { template : "item" }}                  
});
&lt;/script&gt;  </code>
</pre>



### commonSeriesOptions.tooltip.visible<span class="type-signature type boolean">boolean</span>
{:#commonSeriesOptions-tooltip-visible}




tooltip visibility can be toggled using this property


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ tooltip :{visible : true} }                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.type<span class="type-signature type enum">enum</span>
{:#commonSeriesOptions-type}




Specifies the type of series to be rendered in chart. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ type : "spline"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.xAxisName<span class="type-signature type string">string</span>
{:#commonSeriesOptions-xAxisName}




Specifies the name of the xAxis.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ xAxisName : "xAxis"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.xName<span class="type-signature type string">string</span>
{:#commonSeriesOptions-xName}




Specifies the xName for dataSource in series. This is used to take the x values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions : {xName: "XValue" }                   
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.yAxisName<span class="type-signature type string">string</span>
{:#commonSeriesOptions-yAxisName}




Specifies the name of the yAxis.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{ yAxisName : "yAxis"}                  
});
&lt;/script&gt; </code>
</pre>



### commonSeriesOptions.yName<span class="type-signature type string">string</span>
{:#commonSeriesOptions-yName}




Specifies the yName for dataSource in series. This is used to take the y values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
commonSeriesOptions :{yName: "XValue" }               
});
&lt;/script&gt; </code>
</pre>



### crosshair<span class="type-signature type object">object</span>
{:#crosshair}




Contains the properties to customize crosshair or trackball.






### crosshair.marker<span class="type-signature type object">object</span>
{:#crosshair-marker}




Contains property to customize the marker in crosshair.






### crosshair.marker.border<span class="type-signature type object">object</span>
{:#crosshair-marker-border}




Options for customizing the width of the border of marker.






### crosshair.marker.border.width<span class="type-signature type number">number</span>
{:#crosshair-marker-border-width}




Specifies the border width of the marker in crosshair.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{marker :{border :{ width :2 }}}              
});
&lt;/script&gt;</code>
</pre>



### crosshair.marker.opacity<span class="type-signature type boolean">boolean</span>
{:#crosshair-marker-opacity}




Specifies the opacity of the marker in crosshair.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{marker :{opacity :2}}              
});
&lt;/script&gt; </code>
</pre>



### crosshair.marker.size<span class="type-signature type object">object</span>
{:#crosshair-marker-size}




Contains property to customize the size of marker.






### crosshair.marker.size.height<span class="type-signature type number">number</span>
{:#crosshair-marker-size-height}




Specifies the height of the marker in crosshair.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{marker :{size :{ height :15 }}}              
});
&lt;/script&gt; </code>
</pre>



### crosshair.marker.size.width<span class="type-signature type number">number</span>
{:#crosshair-marker-size-width}




Specifies the width of the marker in crosshair.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{marker :{size : {width :15}}}              
});
&lt;/script&gt;</code>
</pre>



### crosshair.marker.visible<span class="type-signature type boolean">boolean</span>
{:#crosshair-marker-visible}




Toggles the visibility of the marker in crosshair.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{marker :{visible :false}}              
});
&lt;/script&gt;</code>
</pre>



### crosshair.type<span class="type-signature type enum">enum</span>
{:#crosshair-type}




Specifies the type of the crosshair. It may be trackball or crosshair.


Default Value:
{:.param}



* ej.datavisualization.Chart.CrosshairType.Crosshair




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{type : "trackball"}              
});
&lt;/script&gt; </code>
</pre>



### crosshair.visible<span class="type-signature type boolean">boolean</span>
{:#crosshair-visible}




Toggles the visibility of the crosshair / trackball in the plot area


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
crosshair :{visible :true}              
});
&lt;/script&gt;</code>
</pre>



### depth<span class="type-signature type number">number</span>
{:#depth}




The depth property defines the depth of the 3D chart from front view of the series to wall.


Default Value:
{:.param}



* 100




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
depth : 100            
});
&lt;/script&gt;</code>
</pre>



### enable3D<span class="type-signature type boolean">boolean</span>
{:#enable3D}




To enable the 3D view of chart control. 3D view is supported only for column, bar, stacking column, stacking bar, pie and doughnut series types.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
enable3D : true             
});
&lt;/script&gt;</code>
</pre>



### enableCanvasRendering<span class="type-signature type boolean">boolean</span>
{:#enableCanvasRendering}




By enabling this property, the ejChart will render in Html5 canvas. This canvas rendering supports all other functionalities except 3D and animation.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
enableCanvasRendering : true             
});
&lt;/script&gt;</code>
</pre>



### enableRotation<span class="type-signature type boolean">boolean</span>
{:#enableRotation}




Enables the 3D chart to perform rotation.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
enableRotation : true             
});
&lt;/script&gt;</code>
</pre>



### indicators<span class="type-signature type array">array</span>
{:#indicators}




Contains properties for customizing the technical indicators.






### indicators.dPeriod<span class="type-signature type number">number</span>
{:#indicators-dPeriod}




Specifies the dperiod for the stochastic indicator.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ dPeriod : 4}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#indicators-enableAnimation}




Specifies the animation of the indicator. ejChart supports animation for the indicator. This can be enable/disable by this property


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ enableAnimation :  true}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.fill<span class="type-signature type string">string</span>
{:#indicators-fill}




Specifies the fill color of the indicator line


Default Value:
{:.param}



* "#00008B"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ fill : "#ff0000"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font<span class="type-signature type object">object</span>
{:#indicators-font}




Contains property to customize the font of the text in indicator.






### indicators.font.color<span class="type-signature type string">string</span>
{:#indicators-font-color}




Specifies the font color of the text in indicator


Default Value:
{:.param}



* "#707070"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ color: "#ff00ff" }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font.fontFamily<span class="type-signature type string">string</span>
{:#indicators-font-fontFamily}




Specifies the font family of the text in indicator


Default Value:
{:.param}



* "segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ fontFamily: "Algerian" }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font.fontStyle<span class="type-signature type string">string</span>
{:#indicators-font-fontStyle}




Specifies the font style of the text in indicator


Default Value:
{:.param}



* "Normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ fontStyle: "Italic" }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font.fontWeight<span class="type-signature type string">string</span>
{:#indicators-font-fontWeight}




Specifies the font weight of the text in indicator


Default Value:
{:.param}



* "Regular"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ fontWeight: "Regular" }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font.opacity<span class="type-signature type number">number</span>
{:#indicators-font-opacity}




Specifies the font opacity of the text in indicator


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ opacity: 1 }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.font.size<span class="type-signature type string">string</span>
{:#indicators-font-size}




Specifies the size of the text in indicator


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ font :{ size: "14px" }}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.histogram<span class="type-signature type object">object</span>
{:#indicators-histogram}




Contains property to customize the histogram in macd indicator.






### indicators.histogram.border<span class="type-signature type object">object</span>
{:#indicators-histogram-border}




Contains property to customize the boder of histogram in macd indicator.






### indicators.histogram.border.color<span class="type-signature type string">string</span>
{:#indicators-histogram-border-color}




Specifies the border color of histogram rendered in macd indicator.


Default Value:
{:.param}



* "#9999ff"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ histogram : {border: {color: "#ff0000"}}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.histogram.border.width<span class="type-signature type width">width</span>
{:#indicators-histogram-border-width}




Specifies the border width of histogram rendered in macd indicator.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ histogram : {border: {width: 2}}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.histogram.fill<span class="type-signature type string">string</span>
{:#indicators-histogram-fill}




Specifies the fill color of histogram rendered in macd indicator.


Default Value:
{:.param}



* "#ccccff"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ histogram : {fill: "#ff0000"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.histogram.opacity<span class="type-signature type number">number</span>
{:#indicators-histogram-opacity}




Specifies the opacity of histogram rendered in macd indicator.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ histogram : {opacity: 0.5}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.kPeriod<span class="type-signature type number">number</span>
{:#indicators-kPeriod}




Specifies the kperiod for the stochastic indicator.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ kPeriod : 4}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.longPeriod<span class="type-signature type number">number</span>
{:#indicators-longPeriod}




Specifies the long period for macd indicator


Default Value:
{:.param}



* 26




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ longPeriod :  14"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.lowerLine<span class="type-signature type object">object</span>
{:#indicators-lowerLine}




Contains property to customize the lower line in indicators.






### indicators.lowerLine.fill<span class="type-signature type string">string</span>
{:#indicators-lowerLine-fill}




Specifies the fill color of lower line.


Default Value:
{:.param}



* "#008000"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ lowerLine : {fill: "#ff0000"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.lowerLine.width<span class="type-signature type number">number</span>
{:#indicators-lowerLine-width}




Specifies the width of lower line.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ lowerLine : {width: 3}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.macdLine<span class="type-signature type object">object</span>
{:#indicators-macdLine}




Contains property to customize the macd line in indicators.






### indicators.macdLine.fill<span class="type-signature type string">string</span>
{:#indicators-macdLine-fill}




Specifies the fill color of macd line.


Default Value:
{:.param}



* "#ff9933"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ macdLine : {fill: "#ff0000"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.macdLine.width<span class="type-signature type number">number</span>
{:#indicators-macdLine-width}




Specifies the width of macd line.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ macdLine : {width: 3}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.macdType<span class="type-signature type string">string</span>
{:#indicators-macdType}




Specifies the type of macd indicator. It can be a line or histogram or both.


Default Value:
{:.param}



* "line"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ macdType :  "both"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.period<span class="type-signature type number">number</span>
{:#indicators-period}




Specifies the period of the indicator. Calculations are made based on this for indicator


Default Value:
{:.param}



* 14




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ period : 20}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.periodLine<span class="type-signature type object">object</span>
{:#indicators-periodLine}




Contains property to customize the period line in indicators.






### indicators.periodLine.fill<span class="type-signature type string">string</span>
{:#indicators-periodLine-fill}




Specifies the fill color of period line.


Default Value:
{:.param}



* "blue"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ periodLine : {fill: "#ff0000"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.periodLine.width<span class="type-signature type number">number</span>
{:#indicators-periodLine-width}




Specifies the width of period line.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ periodLine : {width: 3}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.seriesName<span class="type-signature type string">string</span>
{:#indicators-seriesName}




Specifies the series name of indicator.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ seriesName : "rsi"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.shortPeriod<span class="type-signature type number">number</span>
{:#indicators-shortPeriod}




Specifies the short period for macd indicator


Default Value:
{:.param}



* 13




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ shortPeriod :  14"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.standardDeviations<span class="type-signature type number">number</span>
{:#indicators-standardDeviations}




Specifies the standardDeviations for Bollingerband indicator.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ standardDeviations : 3}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip<span class="type-signature type object">object</span>
{:#indicators-tooltip}




Contains property to customize the tooltip of indicators.






### indicators.tooltip.border<span class="type-signature type object">object</span>
{:#indicators-tooltip-border}




Contains property to customize the border of the tooltip in indicators.






### indicators.tooltip.border.color<span class="type-signature type string">string</span>
{:#indicators-tooltip-border-color}




Specifies the border color of indicator tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{border : { color :"#0000ff"}} }]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.border.width<span class="type-signature type number">number</span>
{:#indicators-tooltip-border-width}




Specifies the border width of indicator tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{border : { width :2}} }]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.duration<span class="type-signature type string">string</span>
{:#indicators-tooltip-duration}




Specifies the animation duration of indicator tooltip.


Default Value:
{:.param}



* "500ms"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{duration : "300ms"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#indicators-tooltip-enableAnimation}




Specifies the animation of the indicator tooltip. ejChart supports animation for the tooltip. This can be enable/disable by this property


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{enableAnimation : false}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.format<span class="type-signature type string">string</span>
{:#indicators-tooltip-format}




Specifies the format of indicator tooltip.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{format : "#point.x#"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.format<span class="type-signature type string">string</span>
{:#indicators-tooltip-format}




Specifies the fill color of indicator tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{format : "#point.x#"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.opacity<span class="type-signature type number">number</span>
{:#indicators-tooltip-opacity}




Specifies the opacity of indicator tooltip.


Default Value:
{:.param}



* 0.95




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{opacity : 0.5}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.tooltip.visible<span class="type-signature type boolaean">boolaean</span>
{:#indicators-tooltip-visible}




Specifies the visibility of indicator tooltip.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ tooltip :{visible : true}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.trigger<span class="type-signature type number">number</span>
{:#indicators-trigger}




Specifies the trigger value for macd indicator


Default Value:
{:.param}



* 9




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ trigger :  14}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.trigger<span class="type-signature type string">string</span>
{:#indicators-trigger}




Specifies the visibility of indicator


Default Value:
{:.param}



* "visible"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ visibility :  "visible"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.type<span class="type-signature type string">string</span>
{:#indicators-type}




Specifies the type of the indicator to render.


Default Value:
{:.param}



* "sma"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ type : "momentum"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.upperLine<span class="type-signature type object">object</span>
{:#indicators-upperLine}




Contains property to customize the upper line in indicators.






### indicators.upperLine.fill<span class="type-signature type string">string</span>
{:#indicators-upperLine-fill}




Specifies the fill color of upper line.


Default Value:
{:.param}



* "#ff9933"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ upperLine : {fill: "#ff0000"}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.upperLine.width<span class="type-signature type number">number</span>
{:#indicators-upperLine-width}




Specifies the width of upper line.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ upperLine : {width: 3}}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.width<span class="type-signature type number">number</span>
{:#indicators-width}




Specifies the width of the indicator line


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ width :  3}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.xAxisName<span class="type-signature type string">string</span>
{:#indicators-xAxisName}




Specifies the xAxisName of the indicator


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ xAxisName :  "xAxis"}]                    
});
&lt;/script&gt;  </code>
</pre>



### indicators.yAxisName<span class="type-signature type string">string</span>
{:#indicators-yAxisName}




Specifies the yAxisName of the indicator


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
indicators :[{ yAxisName :  "yAxis"}]                    
});
&lt;/script&gt;  </code>
</pre>



### legend<span class="type-signature type object">object</span>
{:#legend}




Contains all the properties to customize legend.






### legend.alignment<span class="type-signature type enum">enum</span>
{:#legend-alignment}




This property is used to change the alignment of the legend horizontally.. See <a href="global.html#Alignment">Alignment</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Alignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{alignment : "far"}                    
});
&lt;/script&gt;   </code>
</pre>



### legend.border<span class="type-signature type object">object</span>
{:#legend-border}




Options for customizing the color and width of the border of legend.






### legend.border.color<span class="type-signature type string">string</span>
{:#legend-border-color}




Specifies the border color of legend.


Default Value:
{:.param}



* "transparent"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend : {border :{ color :"green"}}                     
});
&lt;/script&gt;   </code>
</pre>



### legend.border.width<span class="type-signature type number">number</span>
{:#legend-border-width}




Specifies the border width of legend.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ border :{width :2}}                     
});
&lt;/script&gt;  </code>
</pre>



### legend.columnCount<span class="type-signature type number">number</span>
{:#legend-columnCount}




This property specifies the number of columns for the legend items to arrange.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ columnCount : 2}                    
});
&lt;/script&gt; </code>
</pre>



### legend.fill<span class="type-signature type string">string</span>
{:#legend-fill}




Specifies the fill color of legend


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ fill : "green"}                    
});
&lt;/script&gt; </code>
</pre>



### legend.font<span class="type-signature type object">object</span>
{:#legend-font}




Specifies the legend font. These font properties are used to customize the legend item text.






### legend.font.fontFamily<span class="type-signature type string">string</span>
{:#legend-font-fontFamily}




Specifies the legend fontfamily color. Legend item text render with this specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ font :{fontFamily : "algerian"}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.font.fontStyle<span class="type-signature type enum">enum</span>
{:#legend-font-fontStyle}




Specifies the legend font style. Legend item text render with this specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ font :{fontStyle : "italic"}}                    
});
&lt;/script&gt; </code>
</pre>



### legend.font.fontWeight<span class="type-signature type enum">enum</span>
{:#legend-font-fontWeight}




Specifies the legend font weight. Legend item text render with this specified font weight.<a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ font :{fontWeight : "lighter"}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.font.size<span class="type-signature type string">string</span>
{:#legend-font-size}




Specifies the legend font size. Legend item text render with this specified size.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ font :{size : "14px"}}                    
});
&lt;/script&gt; </code>
</pre>



### legend.itemPadding<span class="type-signature type number">number</span>
{:#legend-itemPadding}




This is used to specify the gap/padding between the legend items.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{itemPadding : 5}                     
});
&lt;/script&gt;  </code>
</pre>



### legend.itemStyle<span class="type-signature type object">object</span>
{:#legend-itemStyle}




Contains property to customize the legend item style.






### legend.itemStyle.border<span class="type-signature type object">object</span>
{:#legend-itemStyle-border}




Options for customizing the color and width of the border of legend.






### legend.itemStyle.border.color<span class="type-signature type string">string</span>
{:#legend-itemStyle-border-color}




Specifies the border color of legend.


Default Value:
{:.param}



* "transparent"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ itemStyle :{border : { color : "green' }}}                    
});
&lt;/script&gt; </code>
</pre>



### legend.itemStyle.border.width<span class="type-signature type number">number</span>
{:#legend-itemStyle-border-width}




Specifies the border width of legend.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ itemStyle :{border :{ width : 2 }}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.itemStyle.height<span class="type-signature type number">number</span>
{:#legend-itemStyle-height}




Specifies the legend item height.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ itemStyle :{height : 20}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.itemStyle.width<span class="type-signature type number">number</span>
{:#legend-itemStyle-width}




Specifies the legend item width.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ itemStyle :{width : 15}}                    
});
&lt;/script&gt; </code>
</pre>



### legend.location<span class="type-signature type object">object</span>
{:#legend-location}




Contains property to customize the position of the legend






### legend.location.x<span class="type-signature type number">number</span>
{:#legend-location-x}




This property specifies the x position for rendering legend.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{location :{x :20}}                    
});
&lt;/script&gt;   </code>
</pre>



### legend.location.y<span class="type-signature type number">number</span>
{:#legend-location-y}




This property specifies the y position for rendering legend.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{location : {y : 100}}                  
});
&lt;/script&gt;  </code>
</pre>



### legend.opacity<span class="type-signature type number">number</span>
{:#legend-opacity}




Specifies the opacity of legend


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ opacity : 0.5}                    
});
&lt;/script&gt; </code>
</pre>



### legend.position<span class="type-signature type enum">enum</span>
{:#legend-position}




This property is used to change the alignment of the data label vertically. See <a href="global.html#Position">Position</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Position.Bottom




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ position : "top"}                    
});
&lt;/script&gt;   </code>
</pre>



### legend.rowCount<span class="type-signature type number">number</span>
{:#legend-rowCount}




This property specifies the number of rows for the legend items to arrange.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ rowCount :2}                    
});
&lt;/script&gt; </code>
</pre>



### legend.shape<span class="type-signature type enum">enum</span>
{:#legend-shape}




This property specifies the shape of the legend items. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ shape : "circle" }                      
});
&lt;/script&gt;  </code>
</pre>



### legend.size<span class="type-signature type object">object</span>
{:#legend-size}




Contains property to customize the size of legend.






### legend.size.height<span class="type-signature type number">number</span>
{:#legend-size-height}




Specifies the legend height.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ size :{height : 20%}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.size.width<span class="type-signature type number">number</span>
{:#legend-size-width}




Specifies the legend width.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{ size :{width : 20%}}                    
});
&lt;/script&gt;  </code>
</pre>



### legend.title<span class="type-signature type object">object</span>
{:#legend-title}




Specifies the title of the legend.






### legend.title.font<span class="type-signature type object">object</span>
{:#legend-title-font}




Specifies the font options to customize the legend title.






### legend.title.font.fontFamily<span class="type-signature type string">string</span>
{:#legend-title-font-fontFamily}




Specifies the font family of legend title text.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { font :{fontFamily: "Algerian" } } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#legend-title-font-fontStyle}




Specifies the font style of legend title text.


Default Value:
{:.param}



* "normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { font :{fontStyle: "normal" } } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#legend-title-font-fontWeight}




Specifies the font weight of legend title text.


Default Value:
{:.param}



* "normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { font :{fontWeight: "normal" } } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.title.font.size<span class="type-signature type string">string</span>
{:#legend-title-font-size}




Specifies the size of legend title text.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { font :{size: "14px" } } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.title.text<span class="type-signature type string">string</span>
{:#legend-title-text}




Specifies the text to be displayed as legend title.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { text : "Countries" } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.title.textAlignment<span class="type-signature type enum">enum</span>
{:#legend-title-textAlignment}




Specifies the text alignment of legend title.


Default Value:
{:.param}



* "center"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend: { title: { textAlignment : "near" } }                      
});
&lt;/script&gt; </code>
</pre>



### legend.visible<span class="type-signature type boolean">boolean</span>
{:#legend-visible}




Toggles the legend visibility.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
legend :{visible : false}                     
});
&lt;/script&gt;   </code>
</pre>



### locale<span class="type-signature type string">string</span>
{:#locale}




This property is to specify the localization of chart.


Default Value:
{:.param}



* "en-US"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
locale : "en-US"            
});
&lt;/script&gt;</code>
</pre>



### perspectiveAngle<span class="type-signature type number">number</span>
{:#perspectiveAngle}




Enables the 3D chart to perform rotation.


Default Value:
{:.param}



* 90




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
perspectiveAngle : 60             
});
&lt;/script&gt;</code>
</pre>



### primaryXAxis<span class="type-signature type object">object</span>
{:#primaryXAxis}




This is a horizontal axis which contains options to configure axis. This is the primary x axis for all the series in series array. If you need to override x axis for particular series, you can create an axis object by providing unique name using name property and add it to axes array. Then, assign the name to the series&rsquo;s xAxisName property to link both axis and series.






### primaryXAxis.alternateGridBand<span class="type-signature type object">object</span>
{:#primaryXAxis-alternateGridBand}




This is a horizontal axis alternate grid band which contains options to highlight alternate grid bands.






### primaryXAxis.alternateGridBand.even<span class="type-signature type object">object</span>
{:#primaryXAxis-alternateGridBand-even}




Specifies the Even Alternative Grid Band.






### primaryXAxis.alternateGridBand.even.fill<span class="type-signature type string">string</span>
{:#primaryXAxis-alternateGridBand-even-fill}




Specifies the fill color of Even grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { even :{ fill : "green" } } }                    
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.alternateGridBand.even.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-alternateGridBand-even-opacity}




Specifies the opacity of the Even grid band.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { even :{ opacity : 0.5 } } }                   
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.alternateGridBand.odd<span class="type-signature type object">object</span>
{:#primaryXAxis-alternateGridBand-odd}




Specifies the Odd Alternative Grid Band.






### primaryXAxis.alternateGridBand.odd.fill<span class="type-signature type string">string</span>
{:#primaryXAxis-alternateGridBand-odd-fill}




Specifies the fill color of Odd grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { odd :{ fill : "red" } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.alternateGridBand.odd.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-alternateGridBand-odd-opacity}




Specifies the opacity of the Odd grid band.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { alternateGridBand: { odd :{ opacity : 0.5 } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.axisLine<span class="type-signature type object">object</span>
{:#primaryXAxis-axisLine}




Specifies the options to configure axis line.






### primaryXAxis.axisLine.dashArray<span class="type-signature type string">string</span>
{:#primaryXAxis-axisLine-dashArray}




Controls the pattern of dashes and gaps used to stroke the axis line.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { axisLine : { dashArray : "2,3" } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.axisLine.offset<span class="type-signature type number">number</span>
{:#primaryXAxis-axisLine-offset}




Specifies the horizontal/vertical padding of axis line. Normally, it is used along with plotOffset to pad the plot area.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { axisLine : { offset : 5 } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.axisLine.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-axisLine-visible}




Specifies the visibility of axis line.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { axisLine : { visible : false } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.axisLine.width<span class="type-signature type number">number</span>
{:#primaryXAxis-axisLine-width}




Specifies the width of axisLine in primaryXAxis.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { axisLine : { width : 2 } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.columnIndex<span class="type-signature type number">number</span>
{:#primaryXAxis-columnIndex}




Index of the column object in columnDefinitions array to which this axis is associated with.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { columnIndex: 2 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.columnSpan<span class="type-signature type number">number</span>
{:#primaryXAxis-columnSpan}




An axis can be spanned along multiple columns or plotting areas. This property specifies the number of columns/plotting areas this axis should be spanned.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { columnSpan: 2 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.crosshairLabel<span class="type-signature type object">object</span>
{:#primaryXAxis-crosshairLabel}




Options to configure the visibility of the crosshair label.






### primaryXAxis.crosshairLabel.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-crosshairLabel-visible}




Specifies the visibility of crosshair label.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { crosshairLabel : { visible : true} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.desiredIntervals<span class="type-signature type number">number</span>
{:#primaryXAxis-desiredIntervals}




Specifies the desired number of intervals for the range. With this setting, you can request axis to calculate nice numbers such that they result in the number of intervals approximately equal to your desired interval.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { desiredIntervals: 5 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.edgeLabelPlacement<span class="type-signature type enum">enum</span>
{:#primaryXAxis-edgeLabelPlacement}




Determines how to position labels at the edge of the axis. See <a href="global.html#EdgeLabelPlacement">EdgeLabelPlacement</a> for the available options.


Default Value:
{:.param}



* ej.datavisualization.Chart.EdgeLabelPlacement.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { edgeLabelPlacement : "shift" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.enableTrim
{:#primaryXAxis-enableTrim}




Specifies the action to take when the axis labels are which is having more than the width 34.


Default Value:
{:.param}



* false type {boolean}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { enableTrim : true }                      
});
&lt;/script&gt;    </code>
</pre>



### primaryXAxis.font<span class="type-signature type object">object</span>
{:#primaryXAxis-font}




Specifies the font of primaryXAxis.






### primaryXAxis.font.fontFamily<span class="type-signature type string">string</span>
{:#primaryXAxis-font-fontFamily}




Specifies the fontfamily of primaryXAxis. The axis labels render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { font : { fontFamily : "Algerian"} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryXAxis.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryXAxis-font-fontStyle}




Specifies the fontStyle of primaryXAxis. The axis labels render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { font : { fontStyle : "Italic"} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.font.fontWeight<span class="type-signature type enum">enum</span>
{:#primaryXAxis-font-fontWeight}




Specifies the fontWeight of primaryXAxis. The axis labels render with this specified fontWeight.See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { font : { fontWeight : "lighter"} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.font.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-font-opacity}




Specifies the title opacity of primaryXAxis. The axis labels render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { font : { opacity : 0.5} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.font.size<span class="type-signature type string">string</span>
{:#primaryXAxis-font-size}




Specifies the title size of primaryXAxis. The axis labels render with this specified size.


Default Value:
{:.param}



* "13px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { font : { size : "12px"} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.intervalType<span class="type-signature type enum">enum</span>
{:#primaryXAxis-intervalType}




Specifies whether the type of the interval calculated is in days, months, hours, minutes etc., This is applicable only when valueType is &lsquo;datetime&rsquo;. See <a href="global.html#IntervalType">IntervalType</a>


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { intervalType: "days" }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.isInversed<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-isInversed}




Renders the axis in inversed position.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { isInversed : true}                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.labelFormat<span class="type-signature type string">string</span>
{:#primaryXAxis-labelFormat}




Provides the format for axis labels.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { labelFormat: "{value}%" }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.labelIntersectAction<span class="type-signature type enum">enum</span>
{:#primaryXAxis-labelIntersectAction}




Specifies the action to take when the axis labels are overlapping with each other. See <a href="global.html#LabelIntersectAction">LabelIntersectAction</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelIntersectAction.None




Example
{:.example}

<pre class="prettyprint">
<code>              
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { labelIntersectAction : "multipleRows" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.labelPosition<span class="type-signature type enum">enum</span>
{:#primaryXAxis-labelPosition}




Specifies the position of the axis labels.


Default Value:
{:.param}



* "outside"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { labelPosition : "inside" }                       
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.labelRotation<span class="type-signature type number">number</span>
{:#primaryXAxis-labelRotation}




Rotates the axis labels by the specified angle. Angle must be given in degrees.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { labelRotation: 90 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.logBase<span class="type-signature type number">number</span>
{:#primaryXAxis-logBase}




Specifies the logarithmic base value. This is applicable only when valueType is logarithmic.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { logBase: 5 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorGridLines<span class="type-signature type object">object</span>
{:#primaryXAxis-majorGridLines}




Options for configuring major grid lines color, width, dash arrays etc.,






### primaryXAxis.majorGridLines.dashArray<span class="type-signature type string">string</span>
{:#primaryXAxis-majorGridLines-dashArray}




Controls the pattern of dashes and gaps used to stroke the major grid lines.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
    primaryXAxis: { majorGridLines: { dashArray : "2,3"} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorGridLines.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-majorGridLines-opacity}




Specifies the opacity of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { majorGridLines: { opacity: 0.5 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-majorGridLines-visible}




Specifies the visibility of the major grid lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { majorGridLines: { visible: false } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorGridLines.width<span class="type-signature type number">number</span>
{:#primaryXAxis-majorGridLines-width}




Specifies the width of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
    primaryXAxis: { majorGridLines: { width : 0.5} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorTickLines<span class="type-signature type object">object</span>
{:#primaryXAxis-majorTickLines}




Options for configuring major tick lines color, width, dash arrays etc.,






### primaryXAxis.majorTickLines.size<span class="type-signature type number">number</span>
{:#primaryXAxis-majorTickLines-size}




Length of the major tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { majorTickLines: { size: 2 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.majorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-majorTickLines-visible}




Specifies the visibility of the major tick lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { majorTickLines: { visible: false } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.majorTickLines.width<span class="type-signature type number">number</span>
{:#primaryXAxis-majorTickLines-width}




Specifies the width of the major tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { majorTickLines: { width: 2 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.maximumLabels<span class="type-signature type number">number</span>
{:#primaryXAxis-maximumLabels}




Specifies the maximum number of labels to be displayed in 100 pixels.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { maximumLabels : 5 }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.maximumLabelWidth
{:#primaryXAxis-maximumLabelWidth}




Specifies the width of label till how much width we have to trim.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumLabelWidth type {int}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { maximumLabelWidth :34.5 }                      
});
&lt;/script&gt;    </code>
</pre>



### primaryXAxis.minorGridLines<span class="type-signature type object">object</span>
{:#primaryXAxis-minorGridLines}




Options for configuring minor grid lines color, width, dash arrays etc.,






### primaryXAxis.minorGridLines.dashArray<span class="type-signature type string">string</span>
{:#primaryXAxis-minorGridLines-dashArray}




Controls the pattern of dashes and gaps used to stroke the minor grid lines.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorGridLines: { dashArray: "2,3" } }                      
});
&lt;/script&gt;</code>
</pre>



### primaryXAxis.minorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-minorGridLines-visible}




Specifies the visibility of the minorGridLines. The user can modify the visibility of the minorGridLines in primaryXAxis.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorGridLines: { visible: true } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.minorGridLines.width<span class="type-signature type number">number</span>
{:#primaryXAxis-minorGridLines-width}




Specifies the width of the minorGridLines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorGridLines: { width: 2 } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.minorTickLines<span class="type-signature type object">object</span>
{:#primaryXAxis-minorTickLines}




Options for configuring minor tick lines color, width, dash arrays etc,.






### primaryXAxis.minorTickLines.size<span class="type-signature type number">number</span>
{:#primaryXAxis-minorTickLines-size}




Length of the minor tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorTickLines: { size: 2 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.minorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-minorTickLines-visible}




Specifies the visibility of the minor tick lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorTickLines: { visible: true } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.minorTickLines.width<span class="type-signature type number">number</span>
{:#primaryXAxis-minorTickLines-width}




Specifies the width of the minor tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorTickLines: { width: 2 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.minorTicksPerInterval<span class="type-signature type number">number</span>
{:#primaryXAxis-minorTicksPerInterval}




Specifies the number of minor ticks to render per major tick/interval.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { minorTicksPerInterval: 5 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.name<span class="type-signature type string">string</span>
{:#primaryXAxis-name}




Unique name of the axis.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { name: "xAxis" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.opposedPosition<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-opposedPosition}




Specifies a value that indicates whether to position the axis opposite to its default position.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { opposedPosition : true }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.plotOffset<span class="type-signature type number">number</span>
{:#primaryXAxis-plotOffset}




Horizontal/vertical padding for the plotting area based on the orientation of the axis.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { plotOffset: 0 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.rangePadding<span class="type-signature type enum">enum</span>
{:#primaryXAxis-rangePadding}




If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.rangePaddding.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { rangePadding : "normal" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.roundingPlaces<span class="type-signature type number">number</span>
{:#primaryXAxis-roundingPlaces}




Rounds the axis labels to the specified number of decimals.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { roundingPlaces: 3 }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.stripLine<span class="type-signature type array">array</span>
{:#primaryXAxis-stripLine}




Options to configure stripLine&rsquo;s color, text, border etc.,


Default Value:
{:.param}



* [ ]







### primaryXAxis.stripLine.borderColor<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-borderColor}




Border color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ borderColor: "green" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.color<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-color}




Background color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ color: "green" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.end<span class="type-signature type number">number</span>
{:#primaryXAxis-stripLine-end}




Specifies the end value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ end: 5 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font<span class="type-signature type object">object</span>
{:#primaryXAxis-stripLine-font}




Specifies the font of stripLine in primaryXAxis. These are font properties for stripLine text






### primaryXAxis.stripLine.font.color<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-font-color}




Specifies the color of stripLine in primaryXAxis. Stripline text render with this color


Default Value:
{:.param}



* "black"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { color: "green"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font.fontFamily<span class="type-signature type enum">enum</span>
{:#primaryXAxis-stripLine-font-fontFamily}




Specifies the fontFamily of stripLine in primaryXAxis. Stripline text render with this fontFamily


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryXAxis-stripLine-font-fontStyle}




Specifies the fontStyle of stripLine in primaryXAxis. Stripline text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* "Normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font.fontWeight<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-font-fontWeight}




Specifies the fontWeight of stripLine in primaryXAxis. Stripline text render with this fontWeight


Default Value:
{:.param}



* "regular"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-stripLine-font-opacity}




Specifies the opacity of stripLine in primaryXAxis. Stripline text render with this opacity


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { opacity: 0.5} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.font.size<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-font-size}




Specifies the size of stripLine in primaryXAxis. Stripline text render with this size


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ font : { size: "15px"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.start<span class="type-signature type number">number</span>
{:#primaryXAxis-stripLine-start}




Specifies the start value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ start: 2 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.startFromAxis<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-stripLine-startFromAxis}




Indicates whether to render the stripLine from the minimum/start value of the axis.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ startFromAxis : true }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.text<span class="type-signature type string">string</span>
{:#primaryXAxis-stripLine-text}




Text to be displayed inside the stripLine.


Default Value:
{:.param}



* "stripLine"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ text : "Empty Point" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.textAlignment<span class="type-signature type enum">enum</span>
{:#primaryXAxis-stripLine-textAlignment}




Alignment of the text displayed in stripLine. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ textAlignment : "middletop" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-stripLine-visible}




Specifies the visibility of the stripLine.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ visible : true }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.width<span class="type-signature type number">number</span>
{:#primaryXAxis-stripLine-width}




Stripline width to be calculated and displayed when enable startFromAxis or set start value of stripline.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ width : 0 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.stripLine.zIndex<span class="type-signature type enum">enum</span>
{:#primaryXAxis-stripLine-zIndex}




Specifies the z order position of the stripLine.


Default Value:
{:.param}



* "over"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { stripLine:[{ zIndex: "behind" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.tickLinesPosition<span class="type-signature type enum">enum</span>
{:#primaryXAxis-tickLinesPosition}




Specifies the position of the axis tick lines.


Default Value:
{:.param}



* "outside"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { tickLinesPosition : "inside" }                       
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.title<span class="type-signature type object">object</span>
{:#primaryXAxis-title}




Contains property to customize the title in chart.






### primaryXAxis.title.enableTrim<span class="type-signature type object">Object</span>
{:#primaryXAxis-title-enableTrim}




Options to trim and wrap the chart axis title .See enableTrim for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.enableTrim




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title:{enableTrim:true} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.title.font<span class="type-signature type object">object</span>
{:#primaryXAxis-title-font}




Specifies the font. These font properties are customization are applied for title text.






### primaryXAxis.title.font.fontFamily<span class="type-signature type string">string</span>
{:#primaryXAxis-title-font-fontFamily}




Specifies the title fontfamily of primaryXAxis. This fontFamily is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { font : { fontFamily : "Algerain"} } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryXAxis-title-font-fontStyle}




Specifies the title fontStyle of primaryXAxis. This fontStyle is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { font : { fontStyle : "Italic"} } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#primaryXAxis-title-font-fontWeight}




Specifies the title fontWeight of primaryXAxis. This fontWeight is applied to the title text of primaryXAxis. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { font : { fontWeight : "lighter"} } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.title.font.opacity<span class="type-signature type number">number</span>
{:#primaryXAxis-title-font-opacity}




Specifies the title opacity of primaryXAxis. This opacity value is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { font : { opacity : 0.8} } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.title.font.size<span class="type-signature type string">string</span>
{:#primaryXAxis-title-font-size}




Specifies the title size of primaryXAxis. This font size is applied to the title text of primaryXAxis.


Default Value:
{:.param}



* "16px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { font : { size : "14px"} } }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryXAxis.title.maximumTitleWidth<span class="type-signature type number">number</span>
{:#primaryXAxis-title-maximumTitleWidth}




use the value for trim and wrap the chart axis title based on the customer input .See maximumTitleWidth for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumTitleWidth.null




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title:{maximumTitleWidth: null} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.title.text<span class="type-signature type string">string</span>
{:#primaryXAxis-title-text}




The value of the title of chart can be specified using this property.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title: { text: "Year" } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryXAxis.valueType<span class="type-signature type enum">enum</span>
{:#primaryXAxis-valueType}




You can plot any type of data like date time, double, string etc., This property determines the type of data that this axis will handle. See <a href="global.html#ValueType">ValueType</a>


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { valueType: "double" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.visible<span class="type-signature type boolean">boolean</span>
{:#primaryXAxis-visible}




Specifies the visibility of the axis.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { visible: false }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.zoomFactor<span class="type-signature type number">number</span>
{:#primaryXAxis-zoomFactor}




This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { zoomFactor : 0.5 }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryXAxis.zoomPosition<span class="type-signature type number">number</span>
{:#primaryXAxis-zoomPosition}




This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { zoomPosition :0.5 }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis<span class="type-signature type object">object</span>
{:#primaryYAxis}




This is a vertical axis which contains options to configure axis. This is the primary y axis for all the series in series array. If you need to override y axis for particular series, you can create an axis object by providing unique name using name property and add it to axes array. Then, assign the name to the series&rsquo;s yAxisName property to link both axis and series.






### primaryYAxis.alternateGridBand<span class="type-signature type object">object</span>
{:#primaryYAxis-alternateGridBand}




This is a Vertical axis alternate grid band which contains options to highlight alternate grid bands.






### primaryYAxis.alternateGridBand.even<span class="type-signature type object">object</span>
{:#primaryYAxis-alternateGridBand-even}




Specifies the Even Alternative Grid Band.






### primaryYAxis.alternateGridBand.even.fill<span class="type-signature type string">string</span>
{:#primaryYAxis-alternateGridBand-even-fill}




Specifies the fill color of Even grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { even : {fill : "red" } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.alternateGridBand.even.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-alternateGridBand-even-opacity}




Specifies the opacity of the Even grid band.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { even : {opacity : 0.5 } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.alternateGridBand.odd<span class="type-signature type object">object</span>
{:#primaryYAxis-alternateGridBand-odd}




Specifies the Odd Alternative Grid Band.






### primaryYAxis.alternateGridBand.odd.fill<span class="type-signature type string">string</span>
{:#primaryYAxis-alternateGridBand-odd-fill}




Specifies the fill color of Odd grid bands


Default Value:
{:.param}



* transparent




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { odd : { fill :"red" }  } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.alternateGridBand.odd.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-alternateGridBand-odd-opacity}




Specifies the opacity of the Odd grid band.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { alternateGridBand: { odd : { opacity :0.5 }  } }                       
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.axisLine<span class="type-signature type object">object</span>
{:#primaryYAxis-axisLine}




Specifies the options to configure axis line.






### primaryYAxis.axisLine.dashArray<span class="type-signature type string">string</span>
{:#primaryYAxis-axisLine-dashArray}




Controls the pattern of dashes and gaps used to stroke the axis line.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { crosshairLabel: { axisLine :{ dashArray : "2,3" } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.axisLine.offset<span class="type-signature type number">number</span>
{:#primaryYAxis-axisLine-offset}




Specifies the horizontal/vertical padding of axis line. Normally, it is used along with plotOffset to pad the plot area.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { axisLine: { offset : 5 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.axisLine.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-axisLine-visible}




Specifies the visibility of axis line.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { axisLine: { visible : false } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.axisLine.width<span class="type-signature type number">number</span>
{:#primaryYAxis-axisLine-width}




Specifies the width of axisLine in primaryYAxis. The user can change the width of the axisLine.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { axisLine: { width : 2 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.crosshairLabel<span class="type-signature type object">object</span>
{:#primaryYAxis-crosshairLabel}




Options to configure the visibility of the crosshair label.






### primaryYAxis.crosshairLabel.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-crosshairLabel-visible}




Specifies the visibility of crosshairLabel. This is the property to change the visibility of the axis labels.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { crosshairLabel: { visible : true } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.desiredIntervals<span class="type-signature type number">number</span>
{:#primaryYAxis-desiredIntervals}




Specifies the desired number of intervals for the range. With this setting, you can request axis to calculate nice numbers such that they result in the number of intervals approximately equal to your desired interval.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { desiredIntervals: 5 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.edgeLabelPlacement<span class="type-signature type enum">enum</span>
{:#primaryYAxis-edgeLabelPlacement}




Determines how to position labels at the edge of the axis. See <a href="global.html#EdgeLabelPlacement">EdgeLabelPlacement</a> for the available options.


Default Value:
{:.param}



* ej.datavisualization.Chart.EdgeLabelPlacement.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { edgeLabelPlacement: "shift" }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.enableTrim
{:#primaryYAxis-enableTrim}




Specifies the action to take when the axis labels are which is having more than the width 34.


Default Value:
{:.param}



* false type {boolean}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { enableTrim : true }                      
});
&lt;/script&gt;    </code>
</pre>



### primaryYAxis.font<span class="type-signature type object">object</span>
{:#primaryYAxis-font}




Specifies the font of primaryYAxis. These font properties are applied for the axis labels.






### primaryYAxis.font.fontFamily<span class="type-signature type string">string</span>
{:#primaryYAxis-font-fontFamily}




Specifies the fontfamily of primaryYAxis. The axis labels render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { font: { fontFamily : "Algerian" } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryYAxis-font-fontStyle}




Specifies the fontStyle of primaryYAxis. The axis labels render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { font: { fontStyle : "italic" } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.font.fontWeight<span class="type-signature type enum">enum</span>
{:#primaryYAxis-font-fontWeight}




Specifies the fontWeight of primaryYAxis. The axis labels render with this specified fontWeight. <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { font: { fontWeight : "normal" } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.font.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-font-opacity}




Specifies the title opacity of primaryYAxis. The axis labels render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { font: { opacity : 0.5 } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.font.size<span class="type-signature type string">string</span>
{:#primaryYAxis-font-size}




Specifies the title size of primaryYAxis. The axis labels render with this specified size.


Default Value:
{:.param}



* "13px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { font: { size : "12px" } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.intervalType<span class="type-signature type enum">enum</span>
{:#primaryYAxis-intervalType}




Specifies whether the type of the interval calculated is in days, months, hours, minutes etc., This is applicable only when valueType is &lsquo;datetime&rsquo;. See <a href="global.html#IntervalType">IntervalType</a>


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { intervalType: "days" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.isInversed<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-isInversed}




Renders the axis in inversed position.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { isInversed : true}                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.labelFormat<span class="type-signature type string">string</span>
{:#primaryYAxis-labelFormat}




Provides the format for axis labels.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { labelFormat: "{value}F" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.labelIntersectAction<span class="type-signature type enum">enum</span>
{:#primaryYAxis-labelIntersectAction}




Specifies the action to take when the axis labels are overlapping with each other. See <a href="global.html#LabelIntersectAction">LabelIntersectAction</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LabelIntersectAction.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { labelIntersectAction: "multipleRows" }                      
});
&lt;/script&gt;    </code>
</pre>



### primaryYAxis.labelPosition<span class="type-signature type enum">enum</span>
{:#primaryYAxis-labelPosition}




Specifies the position of the axis labels.


Default Value:
{:.param}



* "outside"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { labelPosition : "inside" }                       
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.logBase<span class="type-signature type number">number</span>
{:#primaryYAxis-logBase}




Specifies the logarithmic base value. This is applicable only when valueType is logarithmic.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { logBase: 5 }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.majorGridLines<span class="type-signature type object">object</span>
{:#primaryYAxis-majorGridLines}




Options for configuring major grid lines color, width, dash arrays etc.,






### primaryYAxis.majorGridLines.dashArray<span class="type-signature type string">string</span>
{:#primaryYAxis-majorGridLines-dashArray}




Controls the pattern of dashes and gaps used to stroke the major grid lines.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorGridLines : {dashArray : "2,3"} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.majorGridLines.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-majorGridLines-opacity}




Specifies the opacity of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorGridLines : {opacity : 0.5} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.majorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-majorGridLines-visible}




Specifies the visibility of the major grid lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorGridLines : {visible : false} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.majorGridLines.width<span class="type-signature type number">number</span>
{:#primaryYAxis-majorGridLines-width}




Specifies the width of the major grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorGridLines : {width : 2} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.majorTickLines<span class="type-signature type object">object</span>
{:#primaryYAxis-majorTickLines}




Options for configuring major tick lines color, width, dash arrays etc.,






### primaryYAxis.majorTickLines.size<span class="type-signature type number">number</span>
{:#primaryYAxis-majorTickLines-size}




Length of the major tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorTickLines : {size : 2} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.majorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-majorTickLines-visible}




Specifies the visibility of the major tick lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorTickLines : {visible : false} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.majorTickLines.width<span class="type-signature type number">number</span>
{:#primaryYAxis-majorTickLines-width}




Specifies the width of the major tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { majorTickLines : {width : 2} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.maximumLabels<span class="type-signature type number">number</span>
{:#primaryYAxis-maximumLabels}




Specifies the maximum number of labels to be displayed in 100 pixels.


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { maximumLabels: 5 }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.maximumLabelWidth
{:#primaryYAxis-maximumLabelWidth}




Specifies the width of label till how much width we have to trim.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumLabelWidth type {int}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { maximumLabelWidth :34.5 }                      
});
&lt;/script&gt;    </code>
</pre>



### primaryYAxis.minorGridLines<span class="type-signature type object">object</span>
{:#primaryYAxis-minorGridLines}




Options for configuring minor grid lines color, width, dash arrays etc.,






### primaryYAxis.minorGridLines.dashArray<span class="type-signature type string">string</span>
{:#primaryYAxis-minorGridLines-dashArray}




Controls the pattern of dashes and gaps used to stroke the minor grid lines.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorGridLines : {dashArray : "2,3"} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.minorGridLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-minorGridLines-visible}




Specifies the visibility of the minorGridLines. The user can modify the visibility of the minorGridLines in primaryYAxis.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorGridLines : {visible : true} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.minorGridLines.width<span class="type-signature type number">number</span>
{:#primaryYAxis-minorGridLines-width}




Specifies the width of the minor grid lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorGridLines : {width : 2} }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.minorTickLines<span class="type-signature type object">object</span>
{:#primaryYAxis-minorTickLines}




Options for configuring minor tick lines color, width, dash arrays etc.,






### primaryYAxis.minorTickLines.size<span class="type-signature type number">number</span>
{:#primaryYAxis-minorTickLines-size}




Length of the minor tick lines.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorTickLines : {size : 2} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.minorTickLines.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-minorTickLines-visible}




Specifies the visibility of the minor tick lines.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorTickLines : {visible : true} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.minorTickLines.width<span class="type-signature type number">number</span>
{:#primaryYAxis-minorTickLines-width}




Specifies the width of the minor tick lines.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorTickLines : {width : 2} }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.minorTicksPerInterval<span class="type-signature type number">number</span>
{:#primaryYAxis-minorTicksPerInterval}




Specifies the number of minor ticks to render per major tick/interval.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { minorTicksPerInterval: 3 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.name<span class="type-signature type string">string</span>
{:#primaryYAxis-name}




Unique name of the axis.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { name: "yAxis" }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.opposedPosition<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-opposedPosition}




Specifies a value that indicates whether to position the axis opposite to its default position.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { opposedPosition : true }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.plotOffset<span class="type-signature type number">number</span>
{:#primaryYAxis-plotOffset}




Horizontal/vertical padding for the plotting area based on the orientation of the axis.


Default Value:
{:.param}



* 10




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { plotOffset: 5 }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.rangePadding<span class="type-signature type enum">enum</span>
{:#primaryYAxis-rangePadding}




If the range is not given explicitly, range will be calculated automatically. You can customize the automatic range calculation using rangePadding. See <a href="global.html#RangePadding">RangePadding</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.RangePadding.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { rangePadding : "none" }                      
});
&lt;/script&gt;   </code>
</pre>



### primaryYAxis.roundingPlaces<span class="type-signature type number">number</span>
{:#primaryYAxis-roundingPlaces}




Rounds the axis labels to the specified number of decimals.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { roundingPlaces: 2 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.rowIndex<span class="type-signature type number">number</span>
{:#primaryYAxis-rowIndex}




Index of the row object in rowDefinitions array to which this axis is associated with.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { rowIndex: 1 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.rowSpan<span class="type-signature type number">number</span>
{:#primaryYAxis-rowSpan}




An axis can be spanned along multiple rows or plotting areas. This property specifies the number of rows/plotting areas this axis should be spanned.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { rowSpan: 2 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine<span class="type-signature type array">array</span>
{:#primaryYAxis-stripLine}




Options to configure stripLine&rsquo;s color, text, border etc.,


Default Value:
{:.param}



* [ ]







### primaryYAxis.stripLine.borderColor<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-borderColor}




Border color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ borderColor: "green" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.color<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-color}




Background color of the stripLine.


Default Value:
{:.param}



* "gray"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ color: "green" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.end<span class="type-signature type number">number</span>
{:#primaryYAxis-stripLine-end}




Specifies the end value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ end: 5 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font<span class="type-signature type object">object</span>
{:#primaryYAxis-stripLine-font}




Specifies the font of stripLine in primaryYAxis. These are font properties for stripLine text






### primaryYAxis.stripLine.font.color<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-font-color}




Specifies the color of stripLine in primaryYAxis. Stripline text render with this color


Default Value:
{:.param}



* "black"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { color: "green"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font.fontFamily<span class="type-signature type enum">enum</span>
{:#primaryYAxis-stripLine-font-fontFamily}




Specifies the fontFamily of stripLine in primaryYAxis. Stripline text render with this fontFamily


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontFamily : "Algerian"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryYAxis-stripLine-font-fontStyle}




Specifies the fontStyle of stripLine in primaryYAxis. Stripline text render with this fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* "Normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontStyle: "Bold"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font.fontWeight<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-font-fontWeight}




Specifies the fontWeight of stripLine in primaryYAxis. Stripline text render with this fontWeight


Default Value:
{:.param}



* "regular"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { fontWeight: "lighter"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-stripLine-font-opacity}




Specifies the opacity of stripLine in primaryYAxis. Stripline text render with this opacity


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { opacity: 0.5} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.font.size<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-font-size}




Specifies the size of stripLine in primaryYAxis. Stripline text render with this size


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ font : { size: "15px"} }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.start<span class="type-signature type number">number</span>
{:#primaryYAxis-stripLine-start}




Specifies the start value of the stripLine.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ start: 2 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.startFromAxis<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-stripLine-startFromAxis}




Indicates whether to render the stripLine from the minimum/start value of the axis.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ startFromAxis : true }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.text<span class="type-signature type string">string</span>
{:#primaryYAxis-stripLine-text}




Text to be displayed inside the stripLine.


Default Value:
{:.param}



* "stripLine"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ text : "Empty Point" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.textAlignment<span class="type-signature type enum">enum</span>
{:#primaryYAxis-stripLine-textAlignment}




Alignment of the text displayed in stripLine. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* "middlecenter"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ textAlignment : "middletop" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-stripLine-visible}




Specifies the visibility of the stripLine.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ visible : true }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.width<span class="type-signature type number">number</span>
{:#primaryYAxis-stripLine-width}




Stripline width to be calculated and displayed when enable startFromAxis or set start value of stripline.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ width : 0 }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.stripLine.zIndex<span class="type-signature type enum">enum</span>
{:#primaryYAxis-stripLine-zIndex}




Specifies the z order position of the stripLine.


Default Value:
{:.param}



* "over"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { stripLine:[{ zIndex: "behind" }]}                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.tickLinesPosition<span class="type-signature type enum">enum</span>
{:#primaryYAxis-tickLinesPosition}




Specifies the position of the axis tick lines.


Default Value:
{:.param}



* "outside"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { tickLinesPosition : "inside" }                       
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.title<span class="type-signature type object">object</span>
{:#primaryYAxis-title}




Options to configure the title font and alignment of the axis title.






### primaryYAxis.title.enableTrim<span class="type-signature type object">Object</span>
{:#primaryYAxis-title-enableTrim}




Options to trim and wrap the chart axis title .See enableTrim for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.enableTrim




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryXAxis: { title:{enableTrim:true} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.title.font<span class="type-signature type object">object</span>
{:#primaryYAxis-title-font}




Specifies the font. These font properties are customization are applied for title text.






### primaryYAxis.title.font.fontFamily<span class="type-signature type string">string</span>
{:#primaryYAxis-title-font-fontFamily}




Specifies the title fontfamily of primaryYAxis. This fontFamily is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontFamily: "Algerian" } } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#primaryYAxis-title-font-fontStyle}




Specifies the title fontStyle of primaryYAxis. This fontStyle is applied to the title text of primaryYAxis. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontStyle : "Italic" } } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#primaryYAxis-title-font-fontWeight}




Specifies the title fontWeight of primaryYAxis. This fontWeight is applied to the title text of primaryYAxis. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ font :{ fontWeight: "normal" } } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.title.font.opacity<span class="type-signature type number">number</span>
{:#primaryYAxis-title-font-opacity}




Specifies the title opacity of primaryYAxis. This font size is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ font :{ opacity: 0.5 } } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.title.font.size<span class="type-signature type string">string</span>
{:#primaryYAxis-title-font-size}




Specifies the title size of primaryYAxis. This opacity value is applied to the title text of primaryYAxis.


Default Value:
{:.param}



* "16px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ font :{ size: "12px" } } }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.title.maximumTitleWidth<span class="type-signature type number">number</span>
{:#primaryYAxis-title-maximumTitleWidth}




use the value for trim and wrap the chart axis title based on the customer input .See maximumTitleWidth for the availbale options.


Default Value:
{:.param}



* ej.datavisualization.Chart.maximumTitleWidth.null




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title:{maximumTitleWidth: null} }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.title.text<span class="type-signature type string">string</span>
{:#primaryYAxis-title-text}




Text to be displayed as a title for axis.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { title :{ text: "yAxis" } }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.valueType<span class="type-signature type enum">enum</span>
{:#primaryYAxis-valueType}




You can plot any type of data like date time, double, string etc., This property determines the type of data that this axis will handle.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { valueType: "double" }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.visible<span class="type-signature type boolean">boolean</span>
{:#primaryYAxis-visible}




Specifies the visibility of the axis.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { visible : false }                      
});
&lt;/script&gt;  </code>
</pre>



### primaryYAxis.zoomFactor<span class="type-signature type number">number</span>
{:#primaryYAxis-zoomFactor}




This property determines the factor by which the axis is scaled. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { zoomFactor : 0.5 }                      
});
&lt;/script&gt; </code>
</pre>



### primaryYAxis.zoomPosition<span class="type-signature type number">number</span>
{:#primaryYAxis-zoomPosition}




This property determines the starting position of the zoomed axis. Value must be specified between 0 and 1.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
primaryYAxis: { zoomPosition : 0.5 }                      
});
&lt;/script&gt;  </code>
</pre>



### rotation<span class="type-signature type number">number</span>
{:#rotation}




The rotation property is used to spin the 3D chart.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
rotation : 45             
});
&lt;/script&gt;</code>
</pre>



### rowDefinitions<span class="type-signature type array">array</span>
{:#rowDefinitions}




You can split chart into multiple plotting areas horizontally. In order to split the chart horizontally, you need to specify number of row objects in rowDefintions array. Each object in the rowDefnitions represent a plotting area in chart.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
rowDefinitions :[{unit : "percentage"}]                      
});
&lt;/script&gt;  </code>
</pre>



### series<span class="type-signature type array">array</span>
{:#series}




Specifies the properties used for customizing the series.






### series.bearFillColor<span class="type-signature type string">string</span>
{:#series-bearFillColor}




Specifies the bearFillColor for series. This is used in hilo series types


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{bearFillColor: "blue" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.border<span class="type-signature type object">object</span>
{:#series-border}




Specifies the border of the series. These are the properties involved in customizing the series border.






### series.border.color<span class="type-signature type string">string</span>
{:#series-border-color}




Specifies the border color of series. Series in chart render with this specified color as border color


Default Value:
{:.param}



* "transparent"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{border :{ color : "green" } }]                  
});
&lt;/script&gt;</code>
</pre>



### series.border.width<span class="type-signature type number">number</span>
{:#series-border-width}




Specifies the border width of series.Series in chart render with this specified value as border width


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{border :{ width : 2 } }]                  
});
&lt;/script&gt;</code>
</pre>



### series.bullFillColor<span class="type-signature type string">string</span>
{:#series-bullFillColor}




Specifies the bullFillColor for series. This is used in hilo series types


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{bullFillColor: "green" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.dashArray<span class="type-signature type string">string</span>
{:#series-dashArray}




Controls the pattern of dashes and gaps used to stroke the line series.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{dashArray : "2,3"}]                  
});
&lt;/script&gt; </code>
</pre>



### series.dataSource<span class="type-signature type object">object</span>
{:#series-dataSource}




Specifies the dataSource for series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{dataSource: data.open }]                   
});
&lt;/script&gt; </code>
</pre>



### series.doughnutCoefficient<span class="type-signature type number">number</span>
{:#series-doughnutCoefficient}




Sets the radius of the hole on the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.4




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{doughnutCoefficient : 0.5 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.doughnutSize<span class="type-signature type number">number</span>
{:#series-doughnutSize}




Sets the radius of the doughnut series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{doughnutSize : 0.6 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.drawType<span class="type-signature type boolean">boolean</span>
{:#series-drawType}




Specifies the type of series that can be drawn in a Radar or Polar series. It supports line, column and area type. See <a href="global.html#DrawType">DrawType</a>


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{drawType : false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#series-enableAnimation}




Specifies the animation of the series. ejChart supports animation for the series. This can be enable/disable by this property


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{enableAnimation : false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.enableSmartLabels<span class="type-signature type number">number</span>
{:#series-enableSmartLabels}




Enabling this property can avoid pie series data label overlap each other.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{enableSmartLabels : false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.endAngle<span class="type-signature type number">number</span>
{:#series-endAngle}




Specifies the ending angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{endAngle: 270 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.explode<span class="type-signature type boolean">boolean</span>
{:#series-explode}




Explodes the pie slices on mouse move. (Also works for doughnut series)


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{explode: true }]                   
});
&lt;/script&gt; </code>
</pre>



### series.explodeAll<span class="type-signature type boolean">boolean</span>
{:#series-explodeAll}




Explodes all the pie slices. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{explodeAll: true }]                   
});
&lt;/script&gt; </code>
</pre>



### series.explodeIndex<span class="type-signature type number">number</span>
{:#series-explodeIndex}




Index of a slice to be exploded from the whole pie. (Also works for doughnut series)


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{explodeIndex : 2 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.explodeOffset<span class="type-signature type number">number</span>
{:#series-explodeOffset}




Represents the distance the slice has to be moved out when it is exploded.


Default Value:
{:.param}



* 25




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{explodeOffset : 20 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.fill<span class="type-signature type string">string</span>
{:#series-fill}




Specifies the fill color of series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{fill : "green"}]                 
});
&lt;/script&gt;</code>
</pre>



### series.font<span class="type-signature type object">object</span>
{:#series-font}




Specifies the font that is common to all series. These are the properties involved in customizing the font of the series in chart.






### series.font.color<span class="type-signature type string">string</span>
{:#series-font-color}




Specifies the color, that is common to all series. Text in the series, render with the specified font color.


Default Value:
{:.param}



* "#707070"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{font :{color : "green"}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.font.fontFamily<span class="type-signature type string">string</span>
{:#series-font-fontFamily}




Specifies the fontFamily, that is common to all series. Text in the series, render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{ font : { fontFamily : "Algerian"}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.font.fontStyle<span class="type-signature type enum">enum</span>
{:#series-font-fontStyle}




Specifies the fontStyle, that is common to all series. Text in the series, render with the specified font style.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{font :{fontStyle : "italic"}} ]                
});
&lt;/script&gt;</code>
</pre>



### series.font.fontWeight<span class="type-signature type enum">enum</span>
{:#series-font-fontWeight}




Specifies the fontWeight, that is common to all series. Text in the series, render with the specified font weight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{font :{fontWeight : "lighter"}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.font.opacity<span class="type-signature type number">number</span>
{:#series-font-opacity}




Specifies the opacity, that is common to all series. Text in the series, render with the specified font opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{font :{opacity : 0.5}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.font.size<span class="type-signature type string">string</span>
{:#series-font-size}




Specifies the font size, that is common to all series. Text in the series, render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{font :{size : "14px"}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.funnelHeight<span class="type-signature type string">string</span>
{:#series-funnelHeight}




Sets the funnel height.


Default Value:
{:.param}



* "32.7%"(32.7% of actualheight)




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{funnelHeight : '40%' }]                   
});
&lt;/script&gt; </code>
</pre>



### series.funnelWidth<span class="type-signature type string">string</span>
{:#series-funnelWidth}




Sets the funnel width.


Default Value:
{:.param}



* "11.6%"(11.6% of actualwidth)




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{funnelWidth : '40%' }]                   
});
&lt;/script&gt; </code>
</pre>



### series.gapRatio<span class="type-signature type number">number</span>
{:#series-gapRatio}




Specifies the gap between each slice of a pyramid series in pixels.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{gapRatio : 0.2 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.isClosed<span class="type-signature type boolean">boolean</span>
{:#series-isClosed}




Used in Polar and Radar series to specify whether the line/area series has to be rendered in a closed state by joining the start and end point of the series.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{isClosed : false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.isStacking<span class="type-signature type boolean">boolean</span>
{:#series-isStacking}




Used in Polar and Radar series to specify whether column type has to be rendered the stacked value of chart.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{isStacking : false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.labelPosition<span class="type-signature type enum">enum</span>
{:#series-labelPosition}




Specifies the position of the axis labels to render labels either inside or outside of plot area. See <a href="global.html#LabelPosition">LabelPosition</a>


Default Value:
{:.param}



* "inside"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{labelPosition : "outside" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.lineCap<span class="type-signature type enum">enum</span>
{:#series-lineCap}




Specifies the style to draw the end point of a line like butt, round, square. See <a href="global.html#LineCap">LineCap</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineCap.Butt




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{lineCap : "butt"}]                  
});
&lt;/script&gt;</code>
</pre>



### series.lineJoin<span class="type-signature type enum">enum</span>
{:#series-lineJoin}




Specifies the shape to use at the intersection of two lines drawn. See <a href="global.html#LineJoin">LineJoin</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.LineJoin.Round




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{lineJoin : "round"}]                  
});
&lt;/script&gt; </code>
</pre>



### series.marker<span class="type-signature type object">object</span>
{:#series-marker}




Contains the customizing properties to add marker symbols to the points plotted in the chart.






### series.marker.border<span class="type-signature type object">object</span>
{:#series-marker-border}




Options for customizing the color, opacity and width of the border of marker.






### series.marker.border.color<span class="type-signature type string">string</span>
{:#series-marker-border-color}




Specifies the border color of marker.


Default Value:
{:.param}



* "white"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{color : "green"}]                  
});
&lt;/script&gt; </code>
</pre>



### series.marker.border.width<span class="type-signature type number">number</span>
{:#series-marker-border-width}




Specifies the width of the marker


Default Value:
{:.param}



* 3




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{border :{width : 2}}}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel<span class="type-signature type object">object</span>
{:#series-marker-dataLabel}




Contains the customizing properties to add data labels of the points plotted in the chart.






### series.marker.dataLabel.angle<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-angle}




Specifies the rotation angle of dataLabel in the marker. The user can change the rotation angle of dataLabel by applying this property.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{angle : 90}}]                  
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.border<span class="type-signature type object">object</span>
{:#series-marker-dataLabel-border}




Options for customizing the color, opacity and width of the border of datalabel.






### series.marker.dataLabel.border.color<span class="type-signature type string">string</span>
{:#series-marker-dataLabel-border-color}




Specifies the border color of datalabel.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{border : {color : "green"}}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.border.width<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-border-width}




Specifies the border width of dataLabel.


Default Value:
{:.param}



* 0.1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{border :{ width :2 }}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.connectorLine<span class="type-signature type object">object</span>
{:#series-marker-dataLabel-connectorLine}




Contains the options to customize the line connecting the point and the data label.






### series.marker.dataLabel.connectorLine.type<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-connectorLine-type}




Specifies whether to connect the point and data label using bezier curve or straight line. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Type.Line




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ type : "spline" }}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.connectorLine.width<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-connectorLine-width}




Specifies the width of the connector line.


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{connectorLine :{ width : 2 }}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.fill<span class="type-signature type string">string</span>
{:#series-marker-dataLabel-fill}




Specifies the fill color of dataLabel.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{fill : "green"}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.font<span class="type-signature type object">object</span>
{:#series-marker-dataLabel-font}




Specifies the font of the dataLabel. These are the properties involved in customizing the data label font.






### series.marker.dataLabel.font.fontFamily<span class="type-signature type string">string</span>
{:#series-marker-dataLabel-font-fontFamily}




Specifies the fontFamily of dataLabel. Text in the data label render with the specified font family.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{ font :{fontFamily : "algerian"}}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.font.fontStyle<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-font-fontStyle}




Specifies the fontStyle of dataLabel. Text in the data label render with the specified font style. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ fontStyle : "italic" }}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.font.fontWeight<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-font-fontWeight}




Specifies the fontWeight of dataLabel. Text in the data label render with the specified font weight. See <a href="global.html#FontWeight">FontWeight</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { fontWeight : "lighter" }}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.font.opacity<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-font-opacity}




Specifies the opacity of the text in dataLabel. Text in the data label render with the specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{font :{ opacity : 0.5 }}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.font.size<span class="type-signature type string">string</span>
{:#series-marker-dataLabel-font-size}




Specifies the font size of dataLabel. Text in the data label render with the specified font size.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{font : { size : "14px" }}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.horizontalTextAlignment<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-horizontalTextAlignment}




This property is used to change the alignment of the data label horizontally.


Default Value:
{:.param}



* ej.datavisualization.Chart.horizontalTextAlignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{horizontalTextAlignment : "far"}}}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.margin<span class="type-signature type object">object</span>
{:#series-marker-dataLabel-margin}




Specifies the margin for the data label.






### series.marker.dataLabel.margin.bottom<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-margin-bottom}




Specifies the bottom margin value in dataLabel. By specifying this property, we can adjust the text in data label to bottom.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ bottom :10 }}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.margin.left<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-margin-left}




Specifies the left margin value in dataLabel. By specifying this property, we can adjust the text in data label to left.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ left : 10}}}}]                 
});
&lt;/script&gt; </code>
</pre>



### series.marker.dataLabel.margin.right<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-margin-right}




Specifies the right margin value in dataLabel. By specifying this property, we can adjust the text in data label to right.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ right :10 }}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.margin.top<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-margin-top}




Specifies the top margin value in dataLabel. By specifying this property, we can adjust the text in data label to top.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{margin :{ top :10 } }}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.opacity<span class="type-signature type number">number</span>
{:#series-marker-dataLabel-opacity}




Specifies the opacity of dataLabel.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{opacity : 0.5}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.shape<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-shape}




Specifies the rendering shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{shape : "circle"}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.textPosition<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-textPosition}




This property is used to change the position of the text in data label. See <a href="global.html#TextPosition">TextPosition</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.textPosition.Top




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{textPosition : "bottom"}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.verticalTextAlignment<span class="type-signature type enum">enum</span>
{:#series-marker-dataLabel-verticalTextAlignment}




This property is used to change the alignment of the data label vertically.


Default Value:
{:.param}



* ej.datavisualization.Chart.verticalTextAlignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{verticalTextAlignment : "far"}}}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.dataLabel.visible<span class="type-signature type boolean">boolean</span>
{:#series-marker-dataLabel-visible}




Specifies the visibility of dataLabel in the marker. The user can change the visibility of dataLabel by applying this property.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{dataLabel :{visible : true}}]                  
});
&lt;/script&gt; </code>
</pre>



### series.marker.fill<span class="type-signature type string">string</span>
{:#series-marker-fill}




Specifies the fill color of the marker.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker : { fill : "green" } }]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.imageUrl<span class="type-signature type string">string</span>
{:#series-marker-imageUrl}




Specifies the image url location of the marker.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{ imageUrl: "../images/sample.png"}}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.opacity<span class="type-signature type number">number</span>
{:#series-marker-opacity}




Specifies the opacity of the marker. Values ranges from 0 to 1.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{ opacity : 0.5 }}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.shape<span class="type-signature type enum">enum</span>
{:#series-marker-shape}




Specifies the shape of the marker. See <a href="global.html#Shape">Shape</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Shape.Circle




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{ shape: "rectangle"}]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.size<span class="type-signature type object">object</span>
{:#series-marker-size}




Specifies the size of the marker.






### series.marker.size.height<span class="type-signature type number">number</span>
{:#series-marker-size-height}




Specifies the height of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{size :{height : 5}}}]                 
});
&lt;/script&gt;</code>
</pre>



### series.marker.size.width<span class="type-signature type number">number</span>
{:#series-marker-size-width}




Specifies the width of the marker.


Default Value:
{:.param}



* 6




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{ size :{ width : 2 } } }]                  
});
&lt;/script&gt;</code>
</pre>



### series.marker.visible<span class="type-signature type boolean">boolean</span>
{:#series-marker-visible}




Toggles the visibility of the marker.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{marker :{ visible : true}}]                  
});
&lt;/script&gt; </code>
</pre>



### series.opacity<span class="type-signature type number">number</span>
{:#series-opacity}




Specifies the opacity of series. Series render with this specified opacity.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series :[{opacity : 0.5}]                  
});
&lt;/script&gt; </code>
</pre>



### series.pieCoefficient<span class="type-signature type number">number</span>
{:#series-pieCoefficient}




Sets the radius of the pie series with respect to plot area. Value ranges from 0 to 1.


Default Value:
{:.param}



* 0.8




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{pieCoefficient : 0.6 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.points<span class="type-signature type array">array</span>
{:#series-points}




Specifies the points of the series. This is to specify the point values for the series


Default Value:
{:.param}



* [ ]




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{points : [{x : 2000, y : 15}] }]                   
});
&lt;/script&gt; </code>
</pre>



### series.pyramidMode<span class="type-signature type enum">enum</span>
{:#series-pyramidMode}




Sets the rendering mode of the pyramid as linear or surface.


Default Value:
{:.param}



* "linear"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{pyramidMode : "linear" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.query<span class="type-signature type object">object</span>
{:#series-query}




Specifies the query for dataSource in series. This is used to take the query from dataSource


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
var query =  ej.Query().from("Orders").take(10);
$("#container").ejChart({
series : [{query: query }]                   
});
&lt;/script&gt; </code>
</pre>



### series.startAngle<span class="type-signature type number">number</span>
{:#series-startAngle}




Specifies the starting angle for rendering pie / doughnut series.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{startAngle: 140 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip<span class="type-signature type object">object</span>
{:#series-tooltip}




Contains all the properties to customize tooltip






### series.tooltip.border<span class="type-signature type object">object</span>
{:#series-tooltip-border}




Options for customizing the color, opacity and width of the border of tooltip.






### series.tooltip.border.color<span class="type-signature type string">string</span>
{:#series-tooltip-border-color}




Specifies the color of tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : {border : { color :"green"} }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.border.width<span class="type-signature type number">number</span>
{:#series-tooltip-border-width}




Specifies the width of tooltip.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : {border : { width :2} }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.duration<span class="type-signature type string">string</span>
{:#series-tooltip-duration}




Specifies the duration of the tooltip to stay awake.


Default Value:
{:.param}



* "500ms"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : { duration: "300ms" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#series-tooltip-enableAnimation}




Enabling this property animates the tooltip on moving the cursor from one point to the other.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : { enableAnimation: false }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.fill<span class="type-signature type string">string</span>
{:#series-tooltip-fill}




Specifies the fill color of the tooltip.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : {fill : "green"} }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.format<span class="type-signature type string">string</span>
{:#series-tooltip-format}




Formatting the values of point on a tooltip can be customized using this property.


Default Value:
{:.param}



* "#point.x# : #point.y#"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : {format : "#point.x# : #point.y#"} }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.opacity<span class="type-signature type number">number</span>
{:#series-tooltip-opacity}




Specifies the opacity of the tooltip. Values ranges from 0 to 1.


Default Value:
{:.param}



* 0.95




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : { opacity: 0.5 }]                   
});
&lt;/script&gt; </code>
</pre>



### series.tooltip.template<span class="type-signature type string">string</span>
{:#series-tooltip-template}




Specify the template for tooltip


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{ tooltip: { template : "item" }}]                  
});
&lt;/script&gt;  </code>
</pre>



### series.tooltip.visible<span class="type-signature type boolean">boolean</span>
{:#series-tooltip-visible}




tooltip visibility can be toggled using this property


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{tooltip : {visible : true} }]                   
});
&lt;/script&gt; </code>
</pre>



### series.type<span class="type-signature type enum">enum</span>
{:#series-type}




Specifies the type of series to be rendered in chart. see <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* "line"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{type : "column" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.visibility<span class="type-signature type string">string</span>
{:#series-visibility}




Specifies the visibility for series. This is used to change the visibility of series


Default Value:
{:.param}



* "visible"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{visibility: "hidden" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.xAxisName<span class="type-signature type string">string</span>
{:#series-xAxisName}




Specifies the XAxisName for series. This is used to specify the name of the xAxis


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{xAxisName: "xAxis" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.xName<span class="type-signature type string">string</span>
{:#series-xName}




Specifies the xName for dataSource in series. This is used to take the x values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{xName: "XValue" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.yAxisName<span class="type-signature type string">string</span>
{:#series-yAxisName}




Specifies the yAxisName for series. This is used to specify the name of the yAxis


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{yAxisName: "yAxis" }]                   
});
&lt;/script&gt; </code>
</pre>



### series.yName<span class="type-signature type string">string</span>
{:#series-yName}




Specifies the yName for dataSource in series. This is used to take the y values from dataSource


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
series : [{yName: "YValue" }]                   
});
&lt;/script&gt; </code>
</pre>



### sideBySideSeriesPlacement<span class="type-signature type boolean">boolean</span>
{:#sideBySideSeriesPlacement}




The sideBySideSeriesPlacement property defines the appearance of the different set of data on 3D chart


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
sideBySideSeriesPlacement : true             
});
&lt;/script&gt;</code>
</pre>



### theme<span class="type-signature type enum">enum</span>
{:#theme}




By specifying this property the user can change the theme of the chart. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.Theme.Flatlight




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
theme : "flatdark"            
});
&lt;/script&gt;</code>
</pre>



### tilt<span class="type-signature type number">number</span>
{:#tilt}




The tilt property defines the angle of the slope of 3D chart.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
tilt : 5             
});
&lt;/script&gt;</code>
</pre>



### title<span class="type-signature type object">object</span>
{:#title}




Specifies the chart title. This title property denotes the title of the chart.






### title.font<span class="type-signature type object">object</span>
{:#title-font}




Specifies the chart title. These are the font properties involved in chart title customization.






### title.font.fontFamily<span class="type-signature type string">string</span>
{:#title-font-fontFamily}




Specifies the title fontfamily of primaryXAxis. Chart title render with this specified fontFamily.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { font : { fontFamily : "Algerian" } }                     
});
&lt;/script&gt; </code>
</pre>



### title.font.fontStyle<span class="type-signature type enum">enum</span>
{:#title-font-fontStyle}




Specifies the title fontStyle of primaryXAxis. Chart title render with this specified fontStyle. See <a href="global.html#FontStyle">FontStyle</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.FontStyle.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { font : { fontStyle : "italic" } }                     
});
&lt;/script&gt; </code>
</pre>



### title.font.fontWeight<span class="type-signature type enum">enum</span>
{:#title-font-fontWeight}




Specifies the title fontWeight. Chart title render with this specified fontWeight.


Default Value:
{:.param}



* ej.datavisualization.Chart.FontWeight.Regular




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { font : { fontWeight : "lighter" } }                     
});
&lt;/script&gt; </code>
</pre>



### title.font.opacity<span class="type-signature type number">number</span>
{:#title-font-opacity}




Specifies the title opacity. Chart title render with this specified font opacity.


Default Value:
{:.param}



* 0.5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { font : { opacity : 0.8 } }                     
});
&lt;/script&gt; </code>
</pre>



### title.font.size<span class="type-signature type string">string</span>
{:#title-font-size}




Specifies the title size. Chart title render with this specified font size.


Default Value:
{:.param}



* "20px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { font : { size : "22px" } }                     
});
&lt;/script&gt; </code>
</pre>



### title.subTitle<span class="type-signature type object">object</span>
{:#title-subTitle}




Specifies the options to customize the chart subtitle.






### title.subTitle.font<span class="type-signature type object">object</span>
{:#title-subTitle-font}




Specifies the font options for customizing the subtitle.






### title.subTitle.font.fontFamily<span class="type-signature type string">string</span>
{:#title-subTitle-font-fontFamily}




Specifies the font family of subtitle.


Default Value:
{:.param}



* "Segoe UI"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: {subTitle : {font :{ fontFamily : "Algerian" } } }                      
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.font.fontStyle<span class="type-signature type enum">enum</span>
{:#title-subTitle-font-fontStyle}




Specifies the font style of subtitle.


Default Value:
{:.param}



* "Normal"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle : {font :{ fontStyle : "Normal" } } }                     
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.font.fontWeight<span class="type-signature type enum">enum</span>
{:#title-subTitle-font-fontWeight}




Specifies the font weight of subtitle.


Default Value:
{:.param}



* "regular"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle : {font :{ fontWeight : "regular" } } }                     
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.font.opacity<span class="type-signature type double">double</span>
{:#title-subTitle-font-opacity}




Specifies the font opacity of subtitle.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle : {font :{ opacity : 0.5 } } }                     
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.font.size<span class="type-signature type enum">enum</span>
{:#title-subTitle-font-size}




Specifies the font size of subtitle.


Default Value:
{:.param}



* "12px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle : {font :{ size : "14px" } } }                     
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.text<span class="type-signature type string">string</span>
{:#title-subTitle-text}




Specifies the text to be displayed as subtitle.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle: { text : "Performace chart" } }                      
});
&lt;/script&gt; </code>
</pre>



### title.subTitle.textAlignment<span class="type-signature type enum">enum</span>
{:#title-subTitle-textAlignment}




Specifies the text alignment for subtitle text.


Default Value:
{:.param}



* "far"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title: { subTitle: { textAlignment : "near" } }                      
});
&lt;/script&gt; </code>
</pre>



### title.text<span class="type-signature type string">string</span>
{:#title-text}




Specifies the text of the chart title. The text which is to be render as chart title is set here.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { text : "Power Production"}                     
});
&lt;/script&gt; </code>
</pre>



### title.textAlignment<span class="type-signature type enum">enum</span>
{:#title-textAlignment}




This property is used to change the alignment of the title horizontally. See <a href="global.html#TextAlignment">TextAlignment</a>


Default Value:
{:.param}



* ej.datavisualization.Chart.TextAlignment.Center




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
title : { textAlignment : "near"}                     
});
&lt;/script&gt; </code>
</pre>



### wallSize<span class="type-signature type number">number</span>
{:#wallSize}




In 3D, Cartesian axes lines are represented as wall. The property wallSize defines the width of the wall.


Default Value:
{:.param}



* 2




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
wallSize : 5             
});
&lt;/script&gt;</code>
</pre>



### zooming<span class="type-signature type object">object</span>
{:#zooming}




Contains property to customize zooming in chart.






### zooming.enable<span class="type-signature type boolean">boolean</span>
{:#zooming-enable}




Enabling this property will allow zooming for chart plot area.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
zooming :{enable :true}          
});
&lt;/script&gt;</code>
</pre>



### zooming.enableDeferredZoom<span class="type-signature type boolean">boolean</span>
{:#zooming-enableDeferredZoom}




Enabling this property will allow user to pan the zoomed chart on mouse up.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
zooming:{enableDeferredZoom : true}            
});
&lt;/script&gt; </code>
</pre>



### zooming.enableMouseWheel<span class="type-signature type boolean">boolean</span>
{:#zooming-enableMouseWheel}




Enabling this property will allow user to zoom plot are on rolling mouse wheel.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
zooming:{enableMouseWheel : true}            
});
&lt;/script&gt; </code>
</pre>



### zooming.type<span class="type-signature type string">string</span>
{:#zooming-type}




Specifies whether zooming has to be vertical or horizontal.


Default Value:
{:.param}



* 'x,y'




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
&lt;script&gt;
$("#container").ejChart({
zooming :{type : "y"}            
});
&lt;/script&gt; </code>
</pre>


## Methods




### exportChart<span class="signature">()</span>
{:#exportChart}




export the chart widget



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Export Chart
var canvas = $("#container").ejChart("exportChart"); 
var dt = canvas.toDataURL();
this.href = dt;
&lt;/script&gt;</code>
</pre>



### redraw<span class="signature">()</span>
{:#redraw}




redraw the chart widget



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Redraw Chart
var chartObj = $("#container").data("ejChart");
chartObj.redraw(); // redraw the chart
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="container"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$("#container").ejChart("redraw");      
&lt;/script&gt;</code>
</pre>


## Events




### animationComplete
{:#animationComplete}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//animationComplete event for chart
$("#container").ejChart({
   animationComplete: function (args) {}
});</code>
</pre>



### axesLabelRendering
{:#axesLabelRendering}




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
<td class="name"><code>argument.Axis</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.Label</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart for processing of labels</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//axesLabelRendering event for chart
$("#container").ejChart({
   axesLabelRendering: function (args) {}
});</code>
</pre>



### axesLabelsInitialize
{:#axesLabelsInitialize}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//axesLabelsInitialize event for chart
$("#container").ejChart({
   axesLabelsInitialize: function (args) {}
});</code>
</pre>



### axesRangeCalculate
{:#axesRangeCalculate}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//axesRangeCalculate event for chart
$("#container").ejChart({
   axesRangeCalculate: function (args) {}
});</code>
</pre>



### axesTitleRendering
{:#axesTitleRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//axesTitleRendering event for chart
$("#container").ejChart({
   axesTitleRendering: function (args) {}
});</code>
</pre>



### chartAreaBoundsCalculate
{:#chartAreaBoundsCalculate}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//chartAreaBoundsCalculate event for chart
$("#container").ejChart({
   chartAreaBoundsCalculate: function (args) {}
});</code>
</pre>



### create
{:#create}




Fires after chart is created.



Example
{:.example}

<pre class="prettyprint">
<code> 
//create event for chart
$("#container").ejChart("create");</code>
</pre>



### destroy
{:#destroy}




Fires when chart is destroyed completely.



Example
{:.example}

<pre class="prettyprint">
<code> 
//animationComplete event for chart
$("#container").ejChart("destroy");</code>
</pre>



### displayTextRendering
{:#displayTextRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//displayTextRendering event for chart
$("#container").ejChart({
   displayTextRendering: function (args) {}
});</code>
</pre>



### legendBoundsCalculate
{:#legendBoundsCalculate}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//legendBoundsCalculate event for chart
$("#container").ejChart({
   legendBoundsCalculate: function (args) {}
});</code>
</pre>



### legendItemClick
{:#legendItemClick}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//legendItemClick event for chart
$("#container").ejChart({
   legendItemClick: function (args) {}
});</code>
</pre>



### legendItemMouseMove
{:#legendItemMouseMove}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//legendItemMouseMove event for chart
$("#container").ejChart({
   legendItemMouseMove: function (args) {}
});</code>
</pre>



### legendItemRendering
{:#legendItemRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//legendItemRendering event for chart
$("#container").ejChart({
   legendItemRendering: function (args) {}
});</code>
</pre>



### load
{:#load}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//load event for chart
$("#container").ejChart({
   load: function (args) {}
});</code>
</pre>



### pointRegionClick
{:#pointRegionClick}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//pointRegionClick event for chart
$("#container").ejChart({
   pointRegionClick: function (args) {}
});</code>
</pre>



### pointRegionMouseMove
{:#pointRegionMouseMove}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//pointRegionMouseMove event for chart
$("#container").ejChart({
   pointRegionMouseMove: function (args) {}
});</code>
</pre>



### preRender
{:#preRender}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//preRender event for chart
$("#container").ejChart({
   preRender: function (args) {}
});</code>
</pre>



### seriesRendering
{:#seriesRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//seriesRendering event for chart
$("#container").ejChart({
   seriesRendering: function (args) {}
});</code>
</pre>



### symbolRendering
{:#symbolRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//symbolRendering event for chart
$("#container").ejChart({
   symbolRendering: function (args) {}
});</code>
</pre>



### titleRendering
{:#titleRendering}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//titleRendering event for chart
$("#container").ejChart({
   titleRendering: function (args) {}
});</code>
</pre>



### toolTipInitialize
{:#toolTipInitialize}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//toolTipInitialize event for chart
$("#container").ejChart({
   toolTipInitialize: function (args) {}
});</code>
</pre>



### trackAxisToolTip
{:#trackAxisToolTip}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//trackAxisToolTip event for chart
$("#container").ejChart({
   trackAxisToolTip: function (args) {}
});</code>
</pre>



### trackToolTip
{:#trackToolTip}




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
<td class="name"><code>argument.Data</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">parameters from chart</td>
</tr>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the chart model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
//trackToolTip event for chart
$("#container").ejChart({
   trackToolTip: function (args) {}
});</code>
</pre>


