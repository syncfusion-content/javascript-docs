---
layout: post
title: Properties, Methods and Events of ejMap Widget
description: API reference for ejMap
documentation: API
platform: js
keywords: map, ejmap, map api, syncfusion
---

# ejMap

The map can be easily configured to the DOM element, such as div and can be created with a highly customized look and feel.

#### Syntax

{% highlight javascript %}

$(element).ejMap();

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="container"> 
 
<script>
// Create Map
$('#container').ejMap();        
</script> 
  
</div>

{% endhighlight %}


#### Requires

* module:jQuery

* module:ej.datavisualization.Map

* module:JsRender

* module:properties


## Members

### background `string`
{:#members:background}

Specifies the background color for map

#### Default Value

* "white"

#### Example

{% highlight html %}
 
//To set background API value during initialization 
  $("#container").ejMap({background:'white'});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the background API, after initialization:

  //Gets the background value
   
  var property = $("#container").data("ejMap").model.background;
  
  //Sets the background value 
  
  $("#container").data("ejMap").model.background="transparent";

{% endhighlight %}


### baseMapIndex `number`
{:#members:basemapindex}

Specifies the index of the map to determine the shape layer to be displayed

#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set baseMapIndex API value during initialization 
  $("#container").ejMap({baseMapIndex:0});

{% endhighlight %}


{% highlight html %}
 
//Get or set the baseMapIndex API, after initialization:

   //Gets the baseMapIndex value 
   
   var property = $("#container").data("ejMap").model.baseMapIndex;
   
   //Sets the baseMapIndex value 
   
   $("#container").data("ejMap").model.baseMapIndex= 0;
   
{% endhighlight %}


### centerPosition `object`
{:#members:centerposition}

Specify the center position where map should be displayed

#### Default Value

* [0,0]

#### Example

{% highlight html %}
  
// Set the centerPosition during initialization.                        
   $("#container").ejMap({centerPosition: [38.5000, -98]});

{% endhighlight %}


{% highlight html %}
 
//Get or set the centerPosition after initialization:

  //Gets the centerPosition from map.
  
  var property =$("#container").data("ejMap").model.centerPosition;
  
  //Sets the centerPosition to map.
  
  $("#container").data("ejMap").model.centerPosition = [38.5000, -98];

{% endhighlight %}


### enableAnimation `boolean`
{:#members:enableanimation}

Enables or Disables the map animation

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set enableAnimation API value during initialization 
   $("#container").ejMap({enableAnimation:true});  

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableAnimation API, after initialization:
   
   //Gets the enableAnimation value 
   
   var property = $("#container").data("ejMap").model.enableAnimation;
         
   //Sets the enableAnimation value
    
   $("#container").data("ejMap").model.enableAnimation=true }); 

{% endhighlight %}


### enableLayerChangeAnimation `boolean`
{:#members:enablelayerchangeanimation}

Enables or Disables the animation for layer change in map

#### Default Value

* false

#### Example


{% highlight html %}
 
//To set enableLayerChangeAnimation API value during initialization 
   $("#container").ejMap({enableLayerChangeAnimation:true});       

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableLayerChangeAnimation API, after initialization:

   //Gets the enableLayerChangeAnimation value 
   
   var property = $("#container").data("ejMap").model.enableLayerChangeAnimation;
              
   //Sets the enableLayerChangeAnimation value
    
   $("#container").data("ejMap").model.enableLayerChangeAnimation=false }); 

{% endhighlight %}


### enablePan `boolean`
{:#members:enablepan}

Enables or Disables the map panning

#### Default Value

* true

#### Example

{% highlight html %}
 
//To set enablePan API value during initialization 
   $("#container").ejMap({enablePan:true});        

{% endhighlight %}


{% highlight html %}
 
//Get or set the enablePan API, after initialization:
 
   //Gets the enablePan value 
   
   var property = $("#container").data("ejMap").model.enablePan;
               
   //Sets the enablePan value
    
   $("#container").data("ejMap").model.enablePan=true });

{% endhighlight %}


### enableResize `boolean`
{:#members:enableresize}

Determines whether map need to resize when container is resized

#### Default Value

* true

#### Example

{% highlight html %}
 
//To set enableResize API value during initialization 
   $("#container").ejMap({enableResize:true});     

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableResize API, after initialization:
   
   //Gets the enableResize value 
   
   var property = $("#container").data("ejMap").model.enableResize;
            
   //Sets the enableResize value 
   
   $("#container").data("ejMap").model.enableResize= true }); 
{% endhighlight %}


### enableZoom `boolean`
{:#members:enablezoom}

Enables or Disables the zooming of map

#### Default Value

* true

#### Example

{% highlight html %}
 
//To set enableZoom API value during initialization 
   $("#container").ejMap({zoomSettings:{enableZoom:true}});           

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableZoom API, after initialization:

   //Gets the enableZoom value 
   
   var property = $("#container").data("ejMap").model.zoomSettings.enableZoom;
         
   //Sets the enableZoom value
    
   $("#container").data("ejMap").model.zoomSettings.enableZoom=true }); 

{% endhighlight %}


### enableZoomOnSelection `boolean`
{:#members:enablezoomonselection}

Enables or Disables the zoom on selecting the map shape

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set enableZoomOnSelection API value during initialization 
   $("#container").ejMap({zoomSettings:{enableZoomOnSelection:true}});
             
{% endhighlight %}


{% highlight html %}
 
//Get or set the enableZoomOnSelection API, after initialization:

   //Gets the enableZoomOnSelection value
    
   var property = $("#container").data("ejMap").model.zoomSettings.enableZoomOnSelection;
              
   //Sets the enableZoomOnSelection value
    
   $("#container").data("ejMap").model.zoomSettings.enableZoomOnSelection=true }); 

{% endhighlight %}


### factor `number`
{:#members:factor}

Specifies the zoom factor for map zoom value.

#### Default Value

* 1

#### Example

{% highlight html %}
 
//To set zoomFactor API value during initialization 
  $("#container").ejMap({zoomSettings:{factor:1}});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the zoomFactor API, after initialization:
   
   //Gets the zoomFactor value 
   
   var property = $("#container").data("ejMap").model.zoomSettings.factor;
   
   //Sets the zoomFactor value
    
   $("#container").data("ejMap").model.zoomSettings.factor= 1;

{% endhighlight %}


### layers `array`
{:#members:layers}

Hold the shape layers to be displayed in map

#### Default Value

* []


#### Example

{% highlight html %}
  
// Set the layers during initialization.                        
   $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the layer after initialization:
  
  //Gets the layer from map.
  
  var layer =$("#container").data("ejMap").model.layers[layerIndex];
  
  //Sets the layer to map.
  
  $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa };

{% endhighlight %}


### level `number`
{:#members:level}

Specifies the zoom level value for which map to be zoomed

#### Default Value

* 1

#### Example

{% highlight html %}
 
//To set zoomLevel API value during initialization 
  $("#container").ejMap({zoomSettings:{level:1}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the zoomLevel API, after initialization:
   //Gets the zoomLevel value
    
   var property = $("#container").data("ejMap").model.zoomSettings.level;
   
   //Sets the zoomLevel value
    
   $("#container").data("ejMap").model.zoomSettings.level= 1;

{% endhighlight %}


### maxValue `number`
{:#members:maxvalue}

Specifies the maximum zoom level of the map

#### Default Value

* 100

#### Example

{% highlight html %}
 
//To set maxValue API value during initialization 
  $("#container").ejMap({zoomSettings:{maxValue:100}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the maxValue API, after initialization:
   
   //Gets the maxValue value
    
   var property = $("#container").data("ejMap").model.zoomSettings.maxValue;
   
   //Sets the maxValue value 
   
   $("#container").data("ejMap").model.zoomSettings.maxValue= 100;

{% endhighlight %}


### minValue `number`
{:#members:minvalue}

Specifies the minimum zoomSettings level of the map

#### Default Value

* 1

#### Example

{% highlight html %}
 
//To set minValue API value during initialization 
  $("#container").ejMap({zoomSettings:{minValue:1}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the minValue API, after initialization:
   
   //Gets the minValue value 
   
   var property = $("#container").data("ejMap").model.zoomSettings.minValue;
   
   //Sets the minValue value
    
   $("#container").data("ejMap").model.zoomSettings.minValue= 1;

{% endhighlight %}


### model.navigationControl.absolutePosition `object`
{:#members:model-navigationcontrol-}

Set the absolutePosition for navigation control


#### Default Value

* [0,0]

#### Example

{% highlight html %}
 
//To set absolutePosition API value during initialization 
   $("#container").ejMap(navigationControl:{absolutePosition:{x:5,y:20}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the absolutePosition, after initialization:
   
   //Gets the absolutePosition value
   
   var property = $("#container").data("ejMap").model.navigationControl.absolutePosition;
   
   //Sets the absolutePosition value
   
   $("#container").data("ejMap").model.navigationControl.absolutePosition={x:5,y:20}});

{% endhighlight %}


### model.navigationControl.content `string`
{:#members:model-navigationcontrol-}

Specifies the navigation control template for map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set navigation control template for map during initialization 
   $("#container").ejMap(navigationControl:{content:null});

{% endhighlight %}


{% highlight html %}

//Get or set the navigation control template for map, after initialization:

   //Gets the navigation control template
   
   var property = $("#container").data("ejMap").model.navigationControl.content;
   
   //Sets the navigation control template
   
   $("#container").data("ejMap").model.navigationControl.content=null });
{% endhighlight %}


### model.navigationControl.dockPosition `enum`
{:#members:model-navigationcontrol-dockposition}

<ts name = "ej.datavisualization.Map.Position"/>

Set the dockPosition value for navigation control

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
	    <tr>
			<td class="name">none</td>			
			<td class="description">specifies the none position</td>
		</tr>
		<tr>
			<td class="name">topleft</td>			
			<td class="description">specifies the topleft position</td>
		</tr>
        <tr>
			<td class="name">topcenter</td>			
			<td class="description">specifies the topcenter position</td>
		</tr>
        <tr>
			<td class="name">topright</td>			
			<td class="description">specifies the topright position</td>
		</tr>    
        <tr>
			<td class="name">centerleft</td>			
			<td class="description">specifies the centerleft position</td>
		</tr>
		<tr>
			<td class="name">center</td>			
			<td class="description">specifies the center position</td>
		</tr>
        <tr>
			<td class="name">centerright</td>			
			<td class="description">specifies the centerright position</td>
		</tr>
        <tr>
			<td class="name">bottomleft</td>			
			<td class="description">specifies the bottomleft position</td>
		</tr>
        <tr>
			<td class="name">bottomcenter</td>			
			<td class="description">specifies the bottomcenter position</td>
		</tr>
        <tr>
			<td class="name">bottomright</td>			
			<td class="description">specifies the bottomright position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* centerleft

#### Example

{% highlight html %}
 
//To set dockPosition value during initialization 
   $("#container").ejMap(navigationControl:{dockPosition:'centerleft'});
   
{% endhighlight %}


{% highlight html %}
 
//Get or set the dockPosition value, after initialization:
   
   //Gets the dockPosition value
   
   var property = $("#container").data("ejMap").model.navigationControl.dockPosition;
   
   //Sets the dockPosition value
   
   $("#container").data("ejMap").model.navigationControl.dockPosition='centerleft' });

{% endhighlight %}


### model.navigationControl.enableNavigation `boolean`
{:#members:model-navigationcontrol-}

Enables or Disables the Navigation for handling zooming map

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set enableNavigation API value during initialization 
   $("#container").ejMap(navigationControl:{enableNavigation:false});

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableNavigation, after initialization:
   
   //Gets the enableNavigation value
   
   var property = $("#container").data("ejMap").model.navigationControl.enableNavigation;
   
   //Sets the enableNavigation value
   
   $("#container").data("ejMap").model.navigationControl.enableNavigation=false });

{% endhighlight %}


### model.navigationControl.orientation `enum`
{:#members:model-navigationcontrol-orientation}

<ts name = "ej.datavisualization.Map.Orientation"/>

Set the orientation value for navigation control

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">horizontal</td>			
			<td class="description">specifies the horizontal position</td>
		</tr>
		<tr>
			<td class="name">vertical</td>			
			<td class="description">specifies the vertical position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* vertical

#### Example

{% highlight html %}
 
//To set orientation value during initialization 
   $("#container").ejMap(navigationControl:{orientation:'vertical'});
   
{% endhighlight %}


{% highlight html %}
 
//Get or set the orientation value, after initialization:
   
   //Gets the orientation value
   
   var property = $("#container").data("ejMap").model.navigationControl.orientation;
   
   //Sets the orientation value
   
   $("#container").data("ejMap").model.navigationControl.orientation='vertical' });

{% endhighlight %}


### navigationControl `object`
{:#members:navigationcontrol}

Enables or Disables the navigation control for map to perform zooming and panning on map shapes.


### shapeLayer `object`
{:#members:shapelayer}

Layer for holding the map shapes


### shapeLayer.bingMapType `enum`
{:#members:shapelayer-bingmaptype}

<ts name = "ej.datavisualization.Map.BingMapType"/>

to get the type of bing map.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">aerial</td>			
			<td class="description">specifies the aerial type</td>
		</tr>
		<tr>
			<td class="name">aerialwithlabel</td>			
			<td class="description">specifies the aerialwithlabel type</td>
		</tr>
        <tr>
			<td class="name">road</td>			
			<td class="description">specifies the road type</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "aerial"

#### Example

{% highlight html %}
  
// Set the type of bing map during initialization.                      
   $("#container").ejMap({layers: [{ bingMapType:'aerial' }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the type of bing map after initialization:

  //Gets the type of bing map.

  var property =$("#container").data("ejMap").model.layers[layerIndex].bingMapType;

  //Sets the type of bing map.

  $("#container").data("ejMap").model.layers[layerIndex].bingMapType  = 'aerial';
  
{% endhighlight %}


### shapeLayer.bubbleSettings `object`
{:#members:shapelayer-bubblesettings}

Specifies the bubble settings for map

#### Example

{% highlight html %}
 
// Set the bubbleSettings of layer during initialization.                       
   $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },bubbleSettings:{ valuePath: "valuePath", minValue: 20, maxValue: 30, color: "#379F64",}, shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the bubbleSettings after initialization:
  
  //Gets the bubbleSettings from map.
  
  var bubbleSettings =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings;
  
  //Sets the bubbleSettings to map.
  
  $("#container").data("ejMap").model.layers[layerIndex].bubbleSettings  = { valuePath: "valuePath", minValue: 20, maxValue: 30, color: "#379F64"};

{% endhighlight %}


### shapeLayer.bubbleSettings.bubbleOpacity `number`
{:#members:shapelayer-bubblesettings-bubbleopacity}

Specifies the bubble Opacity value of bubbles for shape layer in map

#### Default Value

* "0.9"

#### Example

{% highlight html %}
 
//To set bubbleOpacity API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {bubbleOpacity:'0.9'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the bubbleOpacity API, after initialization:

   //Gets the bubble Opacity value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.bubbleOpacity;
  
   //Sets the bubble Opacity value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.bubbleOpacity='0.9'; 

{% endhighlight %}


### shapeLayer.bubbleSettings.color `string`
{:#members:shapelayer-bubblesettings-color}

Specifies the mouse hover color of the shape layer in map

#### Default Value

* "gray"

#### Example

{% highlight html %}
 
//To set color API value during initialization 
   $("#container").ejMap({layers:{bubbleSettings: {color:'gray'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the color API, after initialization:
   
   //Gets the color value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.color;
  
   //Sets the color value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.color='gray'; 

{% endhighlight %}

### shapeLayer.bubbleSettings.colorMappings `object`
{:#members:shapelayer-bubblesettings-colormappings}

Specifies the colorMappings of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set colorMappings API value during initialization 
  $("#container").ejMap({layers:{ bubbleSettings: {colorMappings:{rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}}}});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the colorMappings API, after initialization:
   
   //Gets the colorMappings value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.colorMappings;
  
   //Sets the colorMappings value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.colorMappings={rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}; 

{% endhighlight %}


### shapeLayer.bubbleSettings.colorValuePath `string`
{:#members:shapelayer-bubblesettings-colorvaluepath}

Specifies the bubble color valuePath of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set colorValuePath  API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {colorValuePath :'sales'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the colorValuePath  API, after initialization:
   //Gets the colorValuePath  value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.colorValuePath ;
        
   //Sets the colorValuePath  value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.colorValuePath ='sales'; 

{% endhighlight %}

### shapeLayer.bubbleSettings.maxValue `number`
{:#members:shapelayer-bubblesettings-maxvalue}

Specifies the maximum size value of bubbles for shape layer in map

#### Default Value

* "20"

#### Example

{% highlight html %}
 
//To set maxValue API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {maxValue:'20'}}});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the maxValue API, after initialization:
   
   //Gets the maxValue value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.maxValue;
       
   //Sets the maxValue value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.maxValue='20'; 

{% endhighlight %}


### shapeLayer.bubbleSettings.minValue  `number`
{:#members:shapelayer-bubblesettings-minvalue}

Specifies the minimum size value of bubbles for shape layer in map

#### Default Value

* "10"

#### Example

{% highlight html %}
 
//To set minValue API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {minValue:'10'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the minValue API, after initialization:
   
   //Gets the minValue value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.minValue;
       
   //Sets the minValue value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.minValue='10'; 

{% endhighlight %}


### shapeLayer.bubbleSettings.showBubble `boolean`
{:#members:shapelayer-bubblesettings-showbubble}

Specifies the showBubble visibility status map

#### Default Value

* true

#### Example

{% highlight html %}
 
//To set showBubble API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {showBubble:true}}});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the showBubble API, after initialization:
   
   //Gets the showBubble value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.showBubble;
     
   //Sets the showBubble value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.showBubble=true; 

{% endhighlight %}


### shapeLayer.bubbleSettings.showTooltip `boolean`
{:#members:shapelayer-bubblesettings-showtooltip}

Specifies the tooltip visibility status of the shape layer in map

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set showTooltip API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {showTooltip:false}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the showTooltip API, after initialization:
   
   //Gets the showTooltip value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.showTooltip;
    
   //Sets the showTooltip value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.showTooltip=false; 

{% endhighlight %}


### shapeLayer.bubbleSettings.tooltipTemplate `string`
{:#members:shapelayer-bubblesettings-tooltiptemplate}

Specifies the bubble tooltip template of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set tooltipTemplate API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {tooltipTemplate:'template'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the tooltipTemplate API, after initialization:
   
   //Gets the tooltipTemplate value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.tooltipTemplate;
        
   //Sets the tooltipTemplate value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.tooltipTemplate='template'; 

{% endhighlight %}


### shapeLayer.bubbleSettings.valuePath `string`
{:#members:shapelayer-bubblesettings-valuepath}

Specifies the bubble valuePath of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set valuePath API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {valuePath:'name'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the valuePath API, after initialization:
   
   //Gets the valuePath value 
   
   var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.valuePath;
      
   //Sets the valuePath value 
   
   $("#container").data("ejMap").model.layers[0].bubbleSettings.valuePath='name'; 

{% endhighlight %}


### shapeLayer.dataSource `object`
{:#members:shapelayer-datasource}

Specifies the datasource for the shape layer

#### Example

{% highlight html %}

// Set the dataSource of layer during initialization.                        
   $("#container").ejMap({layers: [{ layerType: "geometry", dataSource: source,  shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the dataSource after initialization:
   
   //Gets the dataSource from map layer.
   
   var dataSource =$("#container").data("ejMap").model.layers[layerIndex].dataSource;
   
   //Sets the dataSource to map layer.
   
   $("#container").data("ejMap").model.layers[layerIndex].dataSource  = source;

{% endhighlight %}


### shapeLayer.enableAnimation `boolean`
{:#members:shapelayer-enableanimation}

Enables or disables the animation

#### Default Value

* false

#### Example
{:.example}


{% highlight html %}
  
// Set the enableAnimation during initialization.                       
   $("#container").ejMap({layers: [{ enableAnimation:false }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableAnimation after initialization:
   
   //Gets the enableAnimation from map.
   
   var property =$("#container").data("ejMap").model.layers[layerIndex].enableAnimation;
   
   //Sets the enableAnimation to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].enableAnimation  = false;

{% endhighlight %}


### shapeLayer.enableMouseHover `boolean`
{:#members:shapelayer-enablemousehover}

Enables or disables the shape mouse hover

#### Default Value

* false

#### Example

{% highlight html %}
  
// Set the enableMouseHover during initialization.                      
   $("#container").ejMap({layers: [{ enableMouseHover:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the enableMouseHover after initialization:
   
   //Gets the enableMouseHover from map.
   
   var property =$("#container").data("ejMap").model.layers[layerIndex].enableMouseHover;
   
   //Sets the enableMouseHover to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].enableMouseHover  = false;
   
{% endhighlight %}


### shapeLayer.enableSelection `boolean`
{:#members:shapelayer-enableselection}

Enables or disables the shape selection

#### Default Value

* true

#### Example

{% highlight html %}
  
// Set the enableSelection during initialization.                       
   $("#container").ejMap({layers: [{ enableSelection:true }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableSelection after initialization:
   
   //Gets the enableSelection from map.
   
   var property =$("#container").data("ejMap").model.layers[layerIndex].enableSelection;
   
   //Sets the enableSelection to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].enableSelection  = true;

{% endhighlight %}


### shapeLayer.key `string`
{:#members:shapelayer-key}

to get the key of bing map

#### Default Value

* null

#### Example

{% highlight html %}
 
//to get the key of bing map during initialization 
   $("#container").ejMap({layers: [{  layerType: 'bing', key: "" }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the key of bing map after initialization:
   
   //Gets the key of bing map value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].key;     
   
   //Sets the bing map key value 
   
   $("#container").data("ejMap").model.layers[layerIndex].key = "";

{% endhighlight %}


### shapeLayer.labelSettings `object`
{:#members:shapelayer-labelsettings}

Options for enabling and configuring labelSettings labelPath, smartLabelSize, labelLength etc.,


### shapeLayer.labelSettings.enableSmartLabel `Boolean`
{:#members:shapelayer-labelsettings-enablesmartlabel}

enable or disable the enableSmartLabel property

#### Default Value

* false

#### Example

{% highlight html %}

// Set the enableSmartLabel value of layer during initialization.                    
   $("#container").ejMap({layers:[{labelSettings: { enableSmartLabel: false}}]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableSmartLabel value after initialization:
   
   //Gets the enableSmartLabel value 
   
   var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.enableSmartLabel;
   
   //Sets the enableSmartLabel value
   
   $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { enableSmartLabel: false};                   

{% endhighlight %}


### shapeLayer.labelSettings.labelLength `number`
{:#members:shapelayer-labelsettings-labellength}

set the labelLength property

#### Default Value

* '2'

#### Example


{% highlight html %}

// Set the labelLength value of layer during initialization.                         
   $("#container").ejMap({layers:[{labelSettings: { labelLength: 2}}]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the labelLength value after initialization:
   
   //Gets the labelLength value 
   
   var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.labelLength;
   
   //Sets the labelLength value

   $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { labelLength: 2};                     

{% endhighlight %}


### shapeLayer.labelSettings.labelPath `string`
{:#members:shapelayer-labelsettings-labelpath}

set the labelPath property

#### Default Value

* null

#### Example
{:.example}


{% highlight html %}

// Set the labelPath value of layer during initialization.                   
   $("#container").ejMap({layers:[{labelSettings: { labelPath: ""}}]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the labelPath value after initialization:
   
   //Gets the labelPath value 
   
   var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.labelPath;
   
   //Sets the labelPath value
   
   $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { labelPath: ""};                      

{% endhighlight %}


### shapeLayer.labelSettings.showLabels `boolean`
{:#members:shapelayer-labelsettings-showlabels}

The property specifies wheather to show labels or not.

#### Default Value

* false

#### Example

{% highlight html %}
// Set the showLabel value of layer during initialization.                   
   $("#container").ejMap({layers:[{labelSettings: { showLabels: false}}]})
        
{% endhighlight %}


{% highlight html %}
 
//Get or set the showLabel value after initialization:
   
   //Gets the showLabel value 
   
   var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.showLabels;
   
   //Sets the showLabel value
   
   $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { showLabels: false};                  

{% endhighlight %}


### shapeLayer.labelSettings.smartLabelSize `enum`
{:#members:shapelayer-labelsettings-smartlabelsize}

<ts name = "ej.datavisualization.Map.LabelSize"/>

set the smartLabelSize property

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">fixed</td>			
			<td class="description">specifies the fixed size</td>
		</tr>
		<tr>
			<td class="name">default</td>			
			<td class="description">specifies the default size</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "fixed"

#### Example

{% highlight html %}
// Set the smartLabelSize value of layer during initialization.                      
   $("#container").ejMap({layers:[{labelSettings: { smartLabelSize: 'fixed'}}]})
 
 {% endhighlight %}


{% highlight html %}
 
//Get or set the smartLabelSize value after initialization:
   
   //Gets the smartLabelSize value 
   
   var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.smartLabelSize;
   
   //Sets the smartLabelSize value
   
   $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { smartLabelSize: 'fixed'};                    

{% endhighlight %}


### shapeLayer.layerType `enum`
{:#members:shapelayer-layertype}

<ts name = "ej.datavisualization.Map.LayerType"/>

Specifies the map type.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">geometry</td>			
			<td class="description">specifies the geometry type</td>
		</tr>
		<tr>
			<td class="name">osm</td>			
			<td class="description">specifies the osm type</td>
		</tr>
        <tr>
			<td class="name">bing</td>			
			<td class="description">specifies the bing type</td>
		</tr>
	</tbody>
</table>

#### Default Value

* 'geometry'

#### Example

{% highlight html %}
  
// Set the layerType during initialization.                     
   $("#container").ejMap({layers: [{ layerType:'geometry' }]})
{% endhighlight %}


{% highlight html %}
 
//Get or set the layerType after initialization:
   
   //Gets the layerType from map.
   
   var property =$("#container").data("ejMap").model.layers[layerIndex].layerType;
   
   //Sets the layerType to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].layerType  = 'geometry';

{% endhighlight %}


### shapeLayer.legendSettings `object`
{:#members:shapelayer-legendsettings}

Options for enabling and configuring legendSettings position, height, width, mode, type etc.,


### shapeLayer.legendSettings.dockOnMap `boolean`
{:#members:shapelayer-legendsettings-dockonmap}

Determines whether the legend should be placed outside or inside the map bounds

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set dockOnMap API value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {dockOnMap:false} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the dockOnMap API, after initialization:
   
   //Gets the dockOnMap value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.dockOnMap;        
   
   //Sets the dockOnMap value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {dockOnMap:false};

{% endhighlight %}


### shapeLayer.legendSettings.dockPosition `enum`
{:#members:shapelayer-legendsettings-dockposition}

<ts name = "ej.datavisualization.Map.DockPosition"/>

Determines the legend placement and it is valid only when dockOnMap is true

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">top</td>			
			<td class="description">specifies the top position</td>
		</tr>
		<tr>
			<td class="name">bottom</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">right</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">left</td>			
			<td class="description">specifies the left position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "top"

#### Example

{% highlight html %}
 
//To set dockPosition value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {dockPosition:"top"} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set dockPosition value after initialization:
  
  //Gets the dockPosition value
  
  var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.dockPosition;     
  
  //Sets the dockPosition value value 
  
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {dockPosition:"top"};

{% endhighlight %}


### shapeLayer.legendSettings.height `number`
{:#members:shapelayer-legendsettings-height}

height value for legend setting

#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set height value for legend during initialization 
   $("#container").ejMap({layers: [{legendSettings: {height:20} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the height value for legend, after initialization:
   
   //Gets the height value for legend value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.height;   
   
   //Sets the height value for legend value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {height:20};
   
{% endhighlight %}


### shapeLayer.legendSettings.icon `enum`
{:#members:shapelayer-legendsettings-icon}

<ts name = "ej.datavisualization.Map.LegendIcons"/>

to get icon value for legend setting

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">rectangle</td>			
			<td class="description">specifies the rectangle position</td>
		</tr>
		<tr>
			<td class="name">circle</td>			
			<td class="description">specifies the circle position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "rectangle"

#### Example


{% highlight html %}
 
//To set icon value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {icon:"rectangle"} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set icon value after initialization:
   
   //Gets the icon value value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.icon;     
   
   //Sets the icon value value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {icon:"rectangle"};

{% endhighlight %}


### shapeLayer.legendSettings.iconHeight `number`
{:#members:shapelayer-legendsettings-iconheight}

icon height value for legend setting

#### Default Value

* 20

#### Example

{% highlight html %}
 
//To set iconHeight value for legend during initialization 
   $("#container").ejMap({layers: [{legendSettings: {iconHeight:20} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the iconHeight value for legend, after initialization:
   
   //Gets the iconHeight value for legend value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.iconHeight;       
   
   //Sets the iconHeight value for legend value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {iconHeight:20};

{% endhighlight %}


### shapeLayer.legendSettings.iconWidth `number`
{:#members:shapelayer-legendsettings-iconwidth}

icon Width value for legend setting

#### Default Value:

* 20

#### Example


{% highlight html %}
 
//To set iconWidth value for legend during initialization 
   $("#container").ejMap({layers: [{legendSettings: {iconWidth:20} }]})           

{% endhighlight %}

{% highlight html %}
 
//Get or set the iconWidth value for legend, after initialization:
   
   //Gets the iconWidth value for legend value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.iconWidth;        
   
   //Sets the iconWidth value for legend value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {iconWidth:20};
   
{% endhighlight %}


### shapeLayer.legendSettings.labelOrientation `enum`
{:#members:shapelayer-legendsettings-labelorientation}

<ts name = "ej.datavisualization.Map.LabelOrientation"/>

set the orientation of legend labels

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">horizontal</td>			
			<td class="description">specifies the horizontal position</td>
		</tr>
		<tr>
			<td class="name">vertical</td>			
			<td class="description">specifies the vertical position</td>
		</tr>  
	</tbody>
</table>

#### Default Value

* vertical

#### Example

{% highlight html %}
 
//To set label orientaion API value for legend setting during initialization 
   $("#container").ejMap({layers: [{legendSettings: {labelOrientation: "vertical"} }]})                      

{% endhighlight %}


{% highlight html %}
 
//Get or set the label orientation API, after initialization:
   
   //Gets the label orientation value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.labelOrientation; 
   
   //Sets the label orientation value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {labelOrientation: "vertical"};

{% endhighlight %}


### shapeLayer.legendSettings.leftLabel `string`
{:#members:shapelayer-legendsettings-leftlabel}

to get leftLabel value for legend setting

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set leftLabel value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {leftLabel:""} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set leftLabel value after initialization:
   
   //Gets the leftLabel value value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.leftLabel;        
   
   //Sets the leftLabel value value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {leftLabel:""};

{% endhighlight %}


### shapeLayer.legendSettings.mode `enum`
{:#members:shapelayer-legendsettings-mode}

<ts name = "ej.datavisualization.Map.LegendMode"/>

to get mode of legend setting

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">default</td>			
			<td class="description">specifies the default mode</td>
		</tr>
		<tr>
			<td class="name">interactive</td>			
			<td class="description">specifies the interactive mode</td>
		</tr>
	</tbody>
</table>


#### Default Value

* "default"

#### Example

{% highlight html %}
 
//To set legend mode during initialization 
   $("#container").ejMap({layers: [{legendSettings: {mode:"default"} }]})
              
{% endhighlight %}


{% highlight html %}
 
//Get or set the legend mode after initialization:
   
   //Gets the legend mode value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.mode;     
   
   //Sets the legend mode value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {mode:"default"};

{% endhighlight %}


### shapeLayer.legendSettings.position `enum`
{:#members:shapelayer-legendsettings-position}

<ts ref = "ej.datavisualization.Map.Position"/>

set the position of legend settings

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
	    <tr>
			<td class="name">none</td>			
			<td class="description">specifies the none position</td>
		</tr>
		<tr>
			<td class="name">topleft</td>			
			<td class="description">specifies the topleft position</td>
		</tr>
        <tr>
			<td class="name">topcenter</td>			
			<td class="description">specifies the topcenter position</td>
		</tr>
        <tr>
			<td class="name">topright</td>			
			<td class="description">specifies the topright position</td>
		</tr>    
        <tr>
			<td class="name">centerleft</td>			
			<td class="description">specifies the centerleft position</td>
		</tr>
		<tr>
			<td class="name">center</td>			
			<td class="description">specifies the center position</td>
		</tr>
        <tr>
			<td class="name">centerright</td>			
			<td class="description">specifies the centerright position</td>
		</tr>
        <tr>
			<td class="name">bottomleft</td>			
			<td class="description">specifies the bottomleft position</td>
		</tr>
        <tr>
			<td class="name">bottomcenter</td>			
			<td class="description">specifies the bottomcenter position</td>
		</tr>
        <tr>
			<td class="name">bottomright</td>			
			<td class="description">specifies the bottomright position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* topleft

#### Example

{% highlight html %}
 
//To set legend position API value for legend setting during initialization 
   $("#container").ejMap({layers: [{legendSettings: {position: "topleft"} }]})                      

{% endhighlight %}


{% highlight html %}
 
//Get or set the legend position API, after initialization:
   
   //Gets the legend position value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.position; 
   
   //Sets the legend position value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {position: "topleft"};

{% endhighlight %}


### shapeLayer.legendSettings.positionX `number`
{:#members:shapelayer-legendsettings-positionx}

x position value for legend setting

#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set x position value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {positionX: 0} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the x position, after initialization:
   
   //Gets the x position value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.positionX;        
   
   //Sets the x position value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {positionX: 0};

{% endhighlight %}


### shapeLayer.legendSettings.positionY `number`
{:#members:shapelayer-legendsettings-positiony}

y position value for legend setting

#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set y position value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {positionY: 0} }]})           
{% endhighlight %}


{% highlight html %}
 
//Get or set the y position, after initialization:
   
   //Gets the y position value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.positionY;        
   
   //Sets the y position value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {positionY: 0};

{% endhighlight %}


### shapeLayer.legendSettings.rightLabel `string`
{:#members:shapelayer-legendsettings-rightlabel}

to get rightLabel value for legend setting

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set rightLabel value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {rightLabel:""} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set rightLabel value after initialization:
   
   //Gets the rightLabel value value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.rightLabel;       
   
   //Sets the rightLabel value value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {rightLabel:""};

{% endhighlight %}


### shapeLayer.legendSettings.showLabels `boolean`
{:#members:shapelayer-legendsettings-showlabels}

Enables or Disables the showLabels

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set showLabels API value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {showLabels:false} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the showLabels API, after initialization:
   
   //Gets the showLabels value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.showLabels;       
   
   //Sets the showLabels value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {showLabels:false};

{% endhighlight %}


### shapeLayer.legendSettings.showLegend `boolean`
{:#members:shapelayer-legendsettings-showlegend}

Enables or Disables the showLegend

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set showLegend API value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {showLegend:false} }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the showLegend API, after initialization:
   
   //Gets the showLegend value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.showLegend;       
   
   //Sets the showLegend value 

   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {showLegend:false};
  
{% endhighlight %}


### shapeLayer.legendSettings.title `string`
{:#members:shapelayer-legendsettings-title}

to get title of legend setting

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set legend title during initialization 
   $("#container").ejMap({layers: [{legendSettings: {title: ""} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the legend title after initialization:
   
   //Gets the legend title value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.title;    
   
   //Sets the legend title value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {title: ""};

{% endhighlight %}


### shapeLayer.legendSettings.type `enum`
{:#members:shapelayer-legendsettings-type}

<ts name = "ej.datavisualization.Map.LegendType"/>

to get type of legend setting

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">layers</td>			
			<td class="description">specifies the layers type</td>
		</tr>
		<tr>
			<td class="name">bubbles</td>			
			<td class="description">specifies the bubbles type</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "layers"

#### Example

{% highlight html %}
 
//To set legend type value during initialization 
   $("#container").ejMap({layers: [{legendSettings: {type:"layers"} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the legend type value after initialization:
   
   //Gets the legend type value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.type;     
   
   //Sets the legend type value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {type:"layers"};

{% endhighlight %}


### shapeLayer.legendSettings.width `number`
{:#members:shapelayer-legendsettings-width}

width value for legend setting

#### Default Value

* 0

#### Example

{% highlight html %}
 
//To set width value for legend during initialization 
   $("#container").ejMap({layers: [{legendSettings: {width:20} }]})           

{% endhighlight %}


{% highlight html %}
 
//Get or set the width value for legend, after initialization:
   
   //Gets the width value for legend value 
   
   var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.width;    
   
   //Sets the width value for legend value 
   
   $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {width:20};

{% endhighlight %}


### shapeLayer.mapItemsTemplate `string`
{:#members:shapelayer-mapitemstemplate}

Specifies the map items template for shapes.

#### Example

{% highlight html %}

// Set the mapItemsTemplate of layer during initialization.                  
   $("#container").ejMap({layers: [{ layerType: "geometry", mapItemsTemplate: "Template",  shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the mapItemsTemplate after initialization:
   
   //Gets the mapItemsTemplate from map.
   
   var mapItemsTemplate =$("#container").data("ejMap").model.layers[layerIndex].mapItemsTemplate;
   
   //Sets the mapItemsTemplate to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].mapItemsTemplate  = "Template";

{% endhighlight %}


### shapeLayer.markers `array`
{:#members:shapelayer-markers}

Specify markers for shape layer.

#### Default Value

* []

#### Example

{% highlight html %}
  
// Set the markers during initialization.                       
   $("#container").ejMap({layers: [{markers:[{label : "chennai",latitude : 13.08 ,longitude : 80.27}]}]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the markers after initialization:
   
   //Gets the markers from map.
   
   var marker =$("#container").data("ejMap").model.layers[layerIndex].markers[markerIndex];
   
   //Sets the marker to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].markers[markerIndex]  = {label : "chennai",latitude : 13.08 ,longitude : 80.27};

{% endhighlight %}


### shapeLayer.markerTemplate `string`
{:#members:shapelayer-markertemplate}

Specifies the map marker template for map layer.

#### Default Value

* null

#### Example

{% highlight html %}

// Set the markerTemplate of layer during initialization.                    
   $("#container").ejMap({layers: [{ layerType: "geometry", markerTemplate: "Template",  shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the markerTemplate after initialization:
   
   //Gets the markerTemplate from map.
   
   var markerTemplate =$("#container").data("ejMap").model.layers[layerIndex].markerTemplate;
   
   //Sets the markerTemplate to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].markerTemplate  = "Template";

{% endhighlight %}


### shapeLayer.selectedMapShapes `array`
{:#members:shapelayer-selectedmapshapes}

Specify selectedMapShapes for shape layer

#### Default Value

* []

#### Example

{% highlight html %}
 
//Gets the selectedMapShapes from map 
   var selectedShapes =$("#container").data("ejMap").model.layers[layerIndex].selectedMapShapes;         

{% endhighlight %}


### shapeLayer.selectionMode `enum`
{:#members:shapelayer-selectionmode}

<ts name = "ej.datavisualization.Map.SelectionMode"/>

Specifies the selection mode of the map. Accepted selection mode values are Default and Multiple.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">default</td>			
			<td class="description">specifies the default position</td>
		</tr>
		<tr>
			<td class="name">multiple</td>			
			<td class="description">specifies the multiple position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "default"

#### Example


{% highlight html %}
  
// Set the selection mode during initialization.                        
   $("#container").ejMap({layers: [{ selectionMode:'default' }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the selection mode after initialization:
   
   //Gets the selection mode from map.
   
   var property =$("#container").data("ejMap").model.layers[layerIndex].selectionMode;
   
   //Sets the selection mode to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].selectionMode  = 'default';

{% endhighlight %}


### shapeLayer.shapeData object `object`
{:#members:shapelayer-shapedata}

Specifies the shape data for the shape layer

#### Example

{% highlight html %}

// Set the shapeData of layer during initialization.                         
   $("#container").ejMap({layers: [{ layerType: "geometry", shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the data after initialization:
   
   //Gets the data from map layer.
   
   var data =$("#container").data("ejMap").model.layers[layerIndex].shapeData;
   
   //Sets the data to map layer.
   
   $("#container").data("ejMap").model.layers[layerIndex].shapeData  = mapShapeData;

{% endhighlight %}


### shapeLayer.shapeSettings `object`
{:#members:shapelayer-shapesettings}

Specifies the shape settings of map layer

#### Example

{% highlight html %}

// Set the shapeSettings of layer during initialization.                     
   $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the shapeSettings after initialization:
   
   //Gets the shapeSettings from map.
   
   var shapeSettings =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings;
   
   //Sets the shapeSettings to map.
   
   $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa };

{% endhighlight %}


### shapeLayer.shapeSettings.autoFill `boolean`
{:#members:shapelayer-shapesettings-autofill}

Enables or Disables the auto fill colors for shape layer in map. When this property value set to true, shapes will be filled with palette colors.

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set autoFill API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {autoFill:false}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the autoFill API, after initialization:
   
   //Gets the autoFill value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.autoFill;
         
   //Sets the autoFill value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.autoFill=false;
    
{% endhighlight %}


### shapeLayer.shapeSettings.colorMappings `object`
{:#members:shapelayer-shapesettings-colormappings}

Specifies the colorMappings of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set colorMappings API value during initialization 
  $("#container").ejMap({layers:{ shapeSettings: {colorMappings:{rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}}}});
{% endhighlight %}


{% highlight html %}
 
//Get or set the colorMappings API, after initialization:
   
   //Gets the colorMappings value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorMappings;
    
   //Sets the colorMappings value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.colorMappings={rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}; 
{% endhighlight %}


### shapeLayer.shapeSettings.colorPalette `string`
{:#members:shapelayer-shapesettings-colorpalette}

Specifies the shape color palette value of the shape layer in map. Accepted colorPalette values are palette1, palette2, palette3 and custompalette.

#### Default Value

* "palette1"

#### Example

{% highlight html %}
 
//To set colorPalette API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {colorPalette:'palette1'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the colorPalette API, after initialization:
   
   //Gets the colorPalette value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorPalette;
     
   //Sets the colorPalette value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.colorPalette='palette1'; 

{% endhighlight %}


### shapeLayer.shapeSettings.colorValuePath `string`
{:#members:shapelayer-shapesettings-colorvaluepath}

Specifies the shape color valuePath of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set colorValuePath  API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {colorValuePath :'sales'}}});

{% endhighlight %}

{% highlight html %}
 
//Get or set the colorValuePath  API, after initialization:
   
   //Gets the colorValuePath  value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorValuePath ;
  
   //Sets the colorValuePath  value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.colorValuePath ='sales'; 

{% endhighlight %}


### shapeLayer.shapeSettings.enableGradient `boolean`
{:#members:shapelayer-shapesettings-enablegradient}

Enables or Disables the gradient colors for map shapes.

#### Default Value

* false

#### Example

{% highlight html %}
 
//To set enableGradient API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {enableGradient:false}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the enableGradient API, after initialization:
   
   //Gets the enableGradient value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.enableGradient;
   
   //Sets the enableGradient value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.enableGradient=false; 

{% endhighlight %}


### shapeLayer.shapeSettings.fill `string`
{:#members:shapelayer-shapesettings-fill}

Specifies the shape fill color of the shape layer in map

#### Default Value

* "#E5E5E5"

#### Example

{% highlight html %}
 
//To set fill API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {fill:'#E5E5E5'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the fill API, after initialization:

   //Gets the fill value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.fill;
     
   //Sets the fill value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.fill='#E5E5E5'; 

{% endhighlight %}


### shapeLayer.shapeSettings.highlightBorderWidth `number`
{:#members:shapelayer-shapesettings-highlightborderwidth}

Specifies the mouse over width of the shape layer in map

#### Default Value

* 1

#### Example

{% highlight html %}
 
//To set highlightBorderWidth API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {highlightBorderWidth:1}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightBorderWidth API, after initialization:
   
   //Gets the highlightBorderWidth value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightBorderWidth;
     
   //Sets the highlightBorderWidth value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.highlightBorderWidth=1;
    
{% endhighlight %}


### shapeLayer.shapeSettings.highlightColor `string`
{:#members:shapelayer-shapesettings-highlightcolor}

Specifies the mouse hover color of the shape layer in map

#### Default Value

* "gray"

Example

{% highlight html %}
 
//To set highlightColor API value during initialization 
  $("#container").ejMap({layers:{shapeSettings: {highlightColor:'gray'}}});
  
{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightColor API, after initialization:
   
   //Gets the highlightColor value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightColor;
   
   //Sets the highlightColor value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.highlightColor='gray'; 

{% endhighlight %}


### shapeLayer.shapeSettings.highlightStroke `string`
{:#members:shapelayer-shapesettings-highlightstroke}

Specifies the mouse over stroke color of the shape layer in map

#### Default Value

* "#C1C1C1"

#### Example

{% highlight html %}
 
//To set highlightStroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {highlightStroke:'#C1C1C1'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightStroke API, after initialization:
   
   //Gets the highlightStroke value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightStroke;
  
   //Sets the highlightStroke value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.highlightStroke='#C1C1C1'; 

{% endhighlight %}


### shapeLayer.shapeSettings.selectionColor `string`
{:#members:shapelayer-shapesettings-selectioncolor}

Specifies the shape selection color of the shape layer in map

#### Default Value

* "gray"

#### Example

{% highlight html %}
 
//To set selectionColor API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionColor:'gray'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionColor API, after initialization:
   
   //Gets the selectionColor value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionColor;
   
   //Sets the selectionColor value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.selectionColor='gray'; 

{% endhighlight %}


### shapeLayer.shapeSettings.selectionStroke `string`
{:#members:shapelayer-shapesettings-selectionstroke}

Specifies the shape selection stroke color of the shape layer in map

#### Default Value

* "#C1C1C1"

#### Example

{% highlight html %}
 
//To set selectionStroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionStroke:'#C1C1C1'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionStroke API, after initialization:
   
   //Gets the selectionStroke value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionStroke;
  
   //Sets the selectionStroke value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.selectionStroke='#C1C1C1'; 

{% endhighlight %}


### shapeLayer.shapeSettings.selectionStrokeWidth `number`
{:#members:shapelayer-shapesettings-selectionstrokewidth}

Specifies the shape selection stroke width of the shape layer in map

#### Default Value

* 1

#### Example

{% highlight html %}
 
//To set selectionStrokeWidth API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionStrokeWidth:1}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionStrokeWidth API, after initialization:
   
   //Gets the selectionStrokeWidth value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionStrokeWidth;
     
   //Sets the selectionStrokeWidth value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.selectionStrokeWidth=1; 

{% endhighlight %}


### shapeLayer.shapeSettings.stroke `string`
{:#members:shapelayer-shapesettings-stroke}

Specifies the shape stroke color of the shape layer in map

#### Default Value

* "#C1C1C1"

#### Example

{% highlight html %}
 
//To set stroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {stroke:'#C1C1C1'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the stroke API, after initialization:
   
   //Gets the stroke value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.stroke;
   
   //Sets the stroke value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.stroke='#C1C1C1'; 

{% endhighlight %}


### shapeLayer.shapeSettings.strokeThickness `number`
{:#members:shapelayer-shapesettings-strokethickness}

Specifies the shape stroke thickness value of the shape layer in map

#### Default Value

* "0.2"

#### Example

{% highlight html %}
 
//To set strokeThickness API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {strokeThickness:'0.2'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the strokeThickness API, after initialization:
   
   //Gets the strokeThickness value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.strokeThickness;
  
   //Sets the strokeThickness value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.strokeThickness='0.2'; 

{% endhighlight %}


### shapeLayer.shapeSettings.valuePath `string`
{:#members:shapelayer-shapesettings-valuepath}

Specifies the shape valuePath of the shape layer in map

#### Default Value

* null

#### Example

{% highlight html %}
 
//To set valuePath API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {valuePath:'name'}}});

{% endhighlight %}


{% highlight html %}
 
//Get or set the valuePath API, after initialization:
   
   //Gets the valuePath value 
   
   var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.valuePath;
        
   //Sets the valuePath value 
   
   $("#container").data("ejMap").model.layers[0].shapeSettings.valuePath='name'; 

{% endhighlight %}


### shapeLayer.showMapItems `boolean`
{:#members:shapelayer-showmapitems}

Shows or hides the map items.

#### Default Value

* false

#### Example

{% highlight html %}
  
// Set the showMapItems during initialization.                  
   $("#container").ejMap({layers: [{ showMapItems:false }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the showMapItems after initialization:

  //Gets the showMapItems from map.

  var property =$("#container").data("ejMap").model.layers[layerIndex].showMapItems;

  //Sets the showMapItems to map.

  $("#container").data("ejMap").model.layers[layerIndex].showMapItems  = false;

{% endhighlight %}


### shapeLayer.showTooltip `boolean`
{:#members:shapelayer-showtooltip}

Shows or hides the tooltip for shapes

#### Default Value

* false

#### Example

{% highlight html %}
  
// Set the showTooltip during initialization.                   
   $("#container").ejMap({layers: [{ showTooltip:false }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the showTooltip after initialization:

  //Gets the showTooltip from map.

  var property =$("#container").data("ejMap").model.layers[layerIndex].showTooltip;

  //Sets the showTooltip to map.

  $("#container").data("ejMap").model.layers[layerIndex].showTooltip  = false;

{% endhighlight %}


### shapeLayer.subLayers `array`
{:#members:shapelayer-sublayers}

Specifies the sub shape layers

#### Default Value

* []

#### Example

{% highlight html %}
  
// Set the subLayers during initialization.                     

   $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },subLayers: [{shapeDataPath: "pathName", shapePropertyPath: "tableFieldName", mapItemsTemplate: 'Template', showMapItems: true, enableMouseHover: true, dataSource: mapDataSource, shapeSettings: { fill: "#9FD0D3", strokeThickness: "0.2", stroke: "white", highlightColor: "#63B7B7", },  shapeData: mapShapeData }, shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the layer after initialization:
   
   //Gets the layer from map.
   
   var layer =$("#container").data("ejMap").model.layers[layerIndex];
   
   //Sets the layer to map.
   
   $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },subLayers: [{shapeDataPath: "pathName", shapePropertyPath: "tableFieldName", mapItemsTemplate: 'Template', showMapItems: true, enableMouseHover: true, dataSource: mapDataSource, shapeSettings: { fill: "#9FD0D3", strokeThickness: "0.2", stroke: "white", highlightColor: "#63B7B7", },  shapeData: mapSubShapeData }, shapeData: mapShapeData };{% endhighlight %}


### shapeLayer.tooltipTemplate `string`
{:#members:shapelayer-tooltiptemplate}

Specifies the tooltip template for shapes.

#### Example

{% highlight html %}

// Set the tooltipTemplate of layer during initialization.                   
        $("#container").ejMap({layers: [{ layerType: "geometry", tooltipTemplate: "Template",  shapeData: mapShapeData }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the tooltipTemplate after initialization:
   
   //Gets the tooltipTemplate from map.
   
   var tooltipTemplate =$("#container").data("ejMap").model.layers[layerIndex].tooltipTemplate;
   
   //Sets the tooltipTemplate to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].tooltipTemplate  ="Template";

{% endhighlight %}


### shapeLayer.urlTemplate `string`
{:#members:shapelayer-urltemplate}

Specifies the URL template for the OSM type map.

#### Default Value

* 'http://a.tile.openstreetmap.org/level/tileX/tileY.png'

#### Example

{% highlight html %}
  
// Set the urlTemplate during initialization.                   
   $("#container").ejMap({layers: [{ urlTemplate:'http://a.tile.openstreetmap.org/level/tileX/tileY.png' }]})

{% endhighlight %}


{% highlight html %}
 
//Get or set the urlTemplate after initialization:
 
   //Gets the urlTemplate from map.
  
   var property =$("#container").data("ejMap").model.layers[layerIndex].urlTemplate;
   
   //Sets the urlTemplate to map.
   
   $("#container").data("ejMap").model.layers[layerIndex].urlTemplate  = 'http://a.tile.openstreetmap.org/level/tileX/tileY.png';

{% endhighlight %}


### zoomSettings `object`
{:#members:zoomsettings}

Enables or Disables the Zooming for map.



## Methods

### navigateTo(latitude, longitude, level)
{:#methods:navigateto}

Method for navigating to specific shape based on latitude, longitude and zoom level.

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
            <td class="name">{% highlight html %}latitude{% endhighlight %}</td>
            <td class="type"><span class="param-type">number</span></td>
            <td class="description last">Pass the latitude value for map</td>
        </tr>
        <tr>
            <td class="name">{% highlight html %}longitude{% endhighlight %}</td>
            <td class="type"><span class="param-type">number</span></td>
            <td class="description last">Pass the longitude value for map</td>
        </tr>
        <tr>
            <td class="name">{% highlight html %}level{% endhighlight %}</td>
            <td class="type"><span class="param-type">number</span></td>
            <td class="description last">Pass the zoom level for map</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//navigateTo method for map
   $("#container").ejMap("navigateTo", lat, lon, level);
   
{% endhighlight %}


### pan(direction)
{:#methods:pan}

Method to perform map panning

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
            <td class="name">{% highlight html %}direction{% endhighlight %}</td>
            <td class="type"><span class="param-type">string</span></td>
            <td class="description last">Pass the direction in which map should be panned</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//pan method for map
   $("#container").ejMap("pan", direction);

{% endhighlight %}


### refresh()
{:#methods:refresh}

Method to reload the map.

#### Example

{% highlight html %}
 
//refresh method for map
   $("#container").ejMap("refresh");

{% endhighlight %}


### refreshLayers()
{:#methods:refreshlayers}

Method to reload the shapeLayers with updated values

#### Example

{% highlight html %}
 
//refresh layers method for map
   $("#container").ejMap("refreshLayers");

{% endhighlight %}


### refreshNavigationControl(navigation)
{:#methods:refreshnavigationcontrol}

Method to reload the navigation control with updated values.

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
            <td class="name">{% highlight html %}navigation{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Pass the navigation control instance</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//Refresh navigation control method for map
   $("#container").ejMap("refreshNavigationControl",navigation);{% endhighlight %}


### zoom(level, isAnimate)
{:#methods:zoom}

Method to perform map zooming.

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
            <td class="name">{% highlight html %}level{% endhighlight %}</td>
            <td class="type"><span class="param-type">number</span></td>
            <td class="description last">Pass the zoom level for map to be zoomed</td>
        </tr>
        <tr>
            <td class="name">{% highlight html %}isAnimate{% endhighlight %}</td>
            <td class="type"><span class="param-type">boolean</span></td>
            <td class="description last">Pass the boolean value to enable or disable animation while zooming</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//zoom method for map
   $("#container").ejMap("zoom",level,isAnimate);

{% endhighlight %}



## Events

### markerSelected
{:#events:markerselected}

Triggered on selecting the map markers.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns marker object.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//markerSelected event for map
  
  $("#container").ejMap({
   markerSelected: function (event) {}
  });

{% endhighlight %}


### mouse leave
{:#events:mouseleave}

Triggers while leaving the hovered map shape

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns hovered map shape object.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//mouseleave  event for map
  $("#container").ejMap({
   mouseleave : function (event) {}
  });

{% endhighlight %}


### mouseover
{:#events:mouseover}

Triggers while hovering the map shape.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns hovered map shape object.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//mouseover  event for map
  $("#container").ejMap({
   mouseover : function (event) {}
  });

{% endhighlight %}


### onRenderComplete
{:#events:onrendercomplete}

Triggers once map render completed.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">Object</span></td>
            <td class="description last">Event parameters from map</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//onRenderComplete event for map
  $("#container").ejMap({
   onRenderComplete: function () {}
  });
  
{% endhighlight %}


### panned
{:#events:panned}

Triggers when map panning ends.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">Object</span></td>
            <td class="description last">Event parameters from map</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//panned event for map
  $("#container").ejMap({
   panned: function (event) {}
  });
{% endhighlight %}


### shapeSelected
{:#events:shapeselected}

Triggered on selecting the map shapes.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns selected shape object.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//shapeSelected event for map
  $("#container").ejMap({
   shapeSelected: function (event) {}
  });

{% endhighlight %}


### zoomedIn
{:#events:zoomedin}

Triggered when map is zoomed-in.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">Object</span></td>
            <td class="description last">Event parameters from map</td>
        </tr>
        <tr>
            <td class="name">{% highlight html %}zoomLevel{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns zoom level value for which the map is zoomed.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
//zoomedIn event for map
  $("#container").ejMap({
   zoomedIn: function (event) {}
  });

{% endhighlight %}


### zoomedOut
{:#events:zoomedout}

Triggers when map is zoomed out.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">Object</span></td>
            <td class="description last">Event parameters from map</td>
        </tr>
        <tr>
            <td class="name">{% highlight html %}zoomLevel{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns zoom level value for which the map is zoomed.</td>
        </tr>
    </tbody>
</table>

Example
{:.example}


{% highlight html %}
 
//zoomedOut event for map
  $("#container").ejMap({
   zoomedOut: function () {}
  });

{% endhighlight %}


<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>





