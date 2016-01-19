---
layout: post
title: ejMap
documentation: API
platform: js
metaname: 
metacontent: 
---





# Class: ejMap


The map can be easily configured to the DOM element, such as div and can be created with a highly customized look and feel.










$(element).ejMap<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div id="container"> 
 
<script>
// Create Map
$('#container').ejMap();        
</script> 
  
</div>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.datavisualization.Map


* module:jsrender


* module:properties




## Members








### background<span class="type-signature type string">string</span>
{:#members:background}








Specifies the background color for map




Default Value:
{:.param}






* "white"








Example
{:.example}


{% highlight html %}
 
//To set background API value during initialization 
  $("#container").ejMap({background:'white'});{% endhighlight %}


{% highlight html %}
 
//Get or set the background API, after initialization:
        //Gets the background value 
  var property = $("#container").data("ejMap").model.background;
        //Sets the background value 
        $("#container").data("ejMap").model.background="transparent";{% endhighlight %}







### baseMapIndex<span class="type-signature type number">number</span>
{:#members:basemapindex}








Specifies the base map-index of the map to determine the shapelayer to be displayed




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//To set baseMapIndex API value during initialization 
  $("#container").ejMap({baseMapIndex:0});{% endhighlight %}


{% highlight html %}
 
//Get or set the baseMapIndex API, after initialization:
        //Gets the baseMapIndex value 
        var property = $("#container").data("ejMap").model.baseMapIndex;
        //Sets the baseMapIndex value 
        $("#container").data("ejMap").model.baseMapIndex= 0;{% endhighlight %}







### centerPosition<span class="type-signature type object">object</span>
{:#members:centerposition}








Specify the center position where map should be displayed




Default Value:
{:.param}






* [0,0]








Example
{:.example}


{% highlight html %}
  
// Set the centerPosition during initialization.                        
         $("#container").ejMap({centerPosition: [38.5000, -98]});{% endhighlight %}


{% highlight html %}
 
//Get or set the centerPosition after initialization:
  //Gets the centerPosition from map.
  var property =$("#container").data("ejMap").model.centerPosition;
  //Sets the centerPosition to map.
  $("#container").data("ejMap").model.centerPosition = [38.5000, -98];{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Enables or Disables the map animation




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableAnimation API value during initialization 
        $("#container").ejMap({enableAnimation:true});  {% endhighlight %}


{% highlight html %}
 
//Get or set the enableAnimation API, after initialization:
        //Gets the enableAnimation value 
        var property = $("#container").data("ejMap").model.enableAnimation;
         
        //Sets the enableAnimation value 
        $("#container").data("ejMap").model.enableAnimation=true }); {% endhighlight %}







### enableLayerChangeAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enablelayerchangeanimation}








Enables or Disables the animation for layer change in map




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableLayerChangeAnimation API value during initialization 
        $("#container").ejMap({enableLayerChangeAnimation:true});       {% endhighlight %}


{% highlight html %}
 
//Get or set the enableLayerChangeAnimation API, after initialization:
        //Gets the enableLayerChangeAnimation value 
        var property = $("#container").data("ejMap").model.enableLayerChangeAnimation;
              
        //Sets the enableLayerChangeAnimation value 
        $("#container").data("ejMap").model.enableLayerChangeAnimation=false }); {% endhighlight %}







### enablePan<span class="type-signature type boolean">boolean</span>
{:#members:enablepan}








Enables or Disables the map panning




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set enablePan API value during initialization 
        $("#container").ejMap({enablePan:true});        {% endhighlight %}


{% highlight html %}
 
//Get or set the enablePan API, after initialization:
        //Gets the enablePan value 
        var property = $("#container").data("ejMap").model.enablePan;
               
        //Sets the enablePan value 
        $("#container").data("ejMap").model.enablePan=true }); {% endhighlight %}







### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}








Determines whether map need to resize when container is resized




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set enableResize API value during initialization 
        $("#container").ejMap({enableResize:true});     {% endhighlight %}


{% highlight html %}
 
//Get or set the enableResize API, after initialization:
        //Gets the enableResize value 
        var property = $("#container").data("ejMap").model.enableResize;
            
        //Sets the enableResize value 
        $("#container").data("ejMap").model.enableResize= true }); {% endhighlight %}







### enableZoom<span class="type-signature type boolean">boolean</span>
{:#members:enablezoom}








Enables or Disables the zooming of map




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set enableZoom API value during initialization 
        $("#container").ejMap({zoomSettings:{enableZoom:true}});            {% endhighlight %}


{% highlight html %}
 
//Get or set the enableZoom API, after initialization:
        //Gets the enableZoom value 
        var property = $("#container").data("ejMap").model.zoomSettings.enableZoom;
         
        //Sets the enableZoom value 
        $("#container").data("ejMap").model.zoomSettings.enableZoom=true }); {% endhighlight %}







### enableZoomOnSelection<span class="type-signature type boolean">boolean</span>
{:#members:enablezoomonselection}








Enables or Disables the zoom on selecting the map shape




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableZoomOnSelection API value during initialization 
        $("#container").ejMap({zoomSettings:{enableZoomOnSelection:true}});     {% endhighlight %}


{% highlight html %}
 
//Get or set the enableZoomOnSelection API, after initialization:
        //Gets the enableZoomOnSelection value 
        var property = $("#container").data("ejMap").model.zoomSettings.enableZoomOnSelection;
              
        //Sets the enableZoomOnSelection value 
        $("#container").data("ejMap").model.zoomSettings.enableZoomOnSelection=true }); {% endhighlight %}







### factor<span class="type-signature type number">number</span>
{:#members:factor}








Specifies the zoom factor for map zoom value.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set zoomFactor API value during initialization 
  $("#container").ejMap({zoomSettings:{factor:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the zoomFactor API, after initialization:
        //Gets the zoomFactor value 
        var property = $("#container").data("ejMap").model.zoomSettings.factor;
        //Sets the zoomFactor value 
        $("#container").data("ejMap").model.zoomSettings.factor= 1;{% endhighlight %}







### layers<span class="type-signature type shapelayer">shapeLayer</span>
{:#members:layers}








Hold the shapelayers to be displayed in map




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
  
// Set the layers during initialization.                        
        $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the layer after initialization:
  //Gets the layer from map.
  var layer =$("#container").data("ejMap").model.layers[layerIndex];
  //Sets the layer to map.
  $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa };{% endhighlight %}







### level<span class="type-signature type number">number</span>
{:#members:level}








Specifies the zoom level value for which map to be zoomed




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set zoomLevel API value during initialization 
  $("#container").ejMap({zoomSettings:{level:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the zoomLevel API, after initialization:
        //Gets the zoomLevel value 
        var property = $("#container").data("ejMap").model.zoomSettings.level;
        //Sets the zoomLevel value 
        $("#container").data("ejMap").model.zoomSettings.level= 1;{% endhighlight %}







### maxValue<span class="type-signature type number">number</span>
{:#members:maxvalue}








Specifies the maximum zoom level of the map




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
 
//To set maxValue API value during initialization 
  $("#container").ejMap({zoomSettings:{maxValue:100}});{% endhighlight %}


{% highlight html %}
 
//Get or set the maxValue API, after initialization:
        //Gets the maxValue value 
        var property = $("#container").data("ejMap").model.zoomSettings.maxValue;
        //Sets the maxValue value 
        $("#container").data("ejMap").model.zoomSettings.maxValue= 100;{% endhighlight %}







### minValue<span class="type-signature type number">number</span>
{:#members:minvalue}








Specifies the minimum zoomSettings level of the map




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set minValue API value during initialization 
  $("#container").ejMap({zoomSettings:{minValue:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the minValue API, after initialization:
        //Gets the minValue value 
        var property = $("#container").data("ejMap").model.zoomSettings.minValue;
        //Sets the minValue value 
        $("#container").data("ejMap").model.zoomSettings.minValue= 1;{% endhighlight %}







### model.navigationControl. absolutePosition<span class="type-signature type object">object</span>
{:#members:model-navigationcontrol-}








Set the absolutePosition for navigation control




Default Value:
{:.param}






* [0,0]








Example
{:.example}


{% highlight html %}
 
//To set absolutePosition API value during initialization 
$("#container").ejMap(navigationControl:{absolutePosition:{x:5,y:20}});{% endhighlight %}


{% highlight html %}
 
//Get or set the absolutePosition, after initialization:
        //Gets the absolutePosition value
        var property = $("#container").data("ejMap").model.navigationControl.absolutePosition;
        //Sets the absolutePosition value
        $("#container").data("ejMap").model.navigationControl.absolutePosition={x:5,y:20}});{% endhighlight %}







### model.navigationControl. content<span class="type-signature type string">string</span>
{:#members:model-navigationcontrol-}








Specifies the navigation control template for map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set navigation control template for map during initialization 
$("#container").ejMap(navigationControl:{content:null});{% endhighlight %}


{% highlight html %}
//Get or set the navigation control template for map, after initialization:
        //Gets the navigation control template
        var property = $("#container").data("ejMap").model.navigationControl.content;
        //Sets the navigation control template
        $("#container").data("ejMap").model.navigationControl.content=null });{% endhighlight %}







### model.navigationControl. dockPosition<span class="type-signature type enum">enum</span>
{:#members:model-navigationcontrol-}








Set the dockPosition value for navigation control




Default Value:
{:.param}






* centerleft








Example
{:.example}


{% highlight html %}
 
//To set dockPosition value during initialization 
$("#container").ejMap(navigationControl:{dockPosition:'centerleft'});{% endhighlight %}


{% highlight html %}
 
//Get or set the dockPosition value, after initialization:
        //Gets the dockPosition value
        var property = $("#container").data("ejMap").model.navigationControl.dockPosition;
        //Sets the dockPosition value
        $("#container").data("ejMap").model.navigationControl.dockPosition='centerleft' });{% endhighlight %}







### model.navigationControl. enableNavigation<span class="type-signature type boolean">boolean</span>
{:#members:model-navigationcontrol-}








Enables or Disables the Navigation for handling zooming map




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableNavigation API value during initialization 
$("#container").ejMap(navigationControl:{enableNavigation:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableNavigation, after initialization:
        //Gets the enableNavigation value
        var property = $("#container").data("ejMap").model.navigationControl.enableNavigation;
        //Sets the enableNavigation value
        $("#container").data("ejMap").model.navigationControl.enableNavigation=false });{% endhighlight %}







### model.navigationControl. orientation<span class="type-signature type enum">enum</span>
{:#members:model-navigationcontrol-}








Set the orientation value for navigation control




Default Value:
{:.param}






* vertical








Example
{:.example}


{% highlight html %}
 
//To set orientation value during initialization 
$("#container").ejMap(navigationControl:{orientation:'vertical'});{% endhighlight %}


{% highlight html %}
 
//Get or set the orientation value, after initialization:
        //Gets the orientation value
        var property = $("#container").data("ejMap").model.navigationControl.orientation;
        //Sets the orientation value
        $("#container").data("ejMap").model.navigationControl.orientation='vertical' });{% endhighlight %}







### navigationControl<span class="type-signature type object">object</span>
{:#members:navigationcontrol}








Enables or Disables the navigation control for map to perform zooming and panning on map shapes.











### shapeLayer
{:#members:shapelayer}








Layer for holding the map shapes











### shapeLayer.bingMapType<span class="type-signature type enum">enum</span>
{:#members:shapelayer-bingmaptype}








to get the type of bing map.




Default Value:
{:.param}






* "aerial"








Example
{:.example}


{% highlight html %}
  
// Set the type of bing map during initialization.                      
        $("#container").ejMap({layers: [{ bingMapType:'aerial' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the type of bing map after initialization:
  //Gets the type of bing map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].bingMapType;
  //Sets the type of bing map.
  $("#container").data("ejMap").model.layers[layerIndex].bingMapType  = 'aerial';{% endhighlight %}







### shapeLayer.bubbleSettings<span class="type-signature type object">object</span>
{:#members:shapelayer-bubblesettings}








Specifies the bubble settings for map





Example
{:.example}


{% highlight html %}
 
// Set the bubbleSettings of layer during initialization.                       
        $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },bubbleSettings:{ valuePath: "valuePath", minValue: 20, maxValue: 30, color: "#379F64",}, shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the bubbleSettings after initialization:
  //Gets the bubbleSettings from map.
  var bubbleSettings =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings;
  //Sets the bubbleSettings to map.
  $("#container").data("ejMap").model.layers[layerIndex].bubbleSettings  = { valuePath: "valuePath", minValue: 20, maxValue: 30, color: "#379F64"};{% endhighlight %}







### shapeLayer.bubbleSettings.bubbleOpacity<span class="type-signature type number">number</span>
{:#members:shapelayer-bubblesettings-bubbleopacity}








Specifies the bubble Opacity value of bubbles for shape layer in map




Default Value:
{:.param}






* "0.9"








Example
{:.example}


{% highlight html %}
 
//To set bubbleOpacity API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {bubbleOpacity:'0.9'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the bubbleOpacity API, after initialization:
        //Gets the bubble Opacity value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.bubbleOpacity;
  
        //Sets the bubble Opacity value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.bubbleOpacity='0.9'; {% endhighlight %}







### shapeLayer.bubbleSettings.color<span class="type-signature type string">string</span>
{:#members:shapelayer-bubblesettings-color}








Specifies the mouse hover color of the shape layer in map




Default Value:
{:.param}






* "gray"








Example
{:.example}


{% highlight html %}
 
//To set color API value during initialization 
  $("#container").ejMap({layers:{bubbleSettings: {color:'gray'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the color API, after initialization:
        //Gets the color value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.color;
  
        //Sets the color value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.color='gray'; {% endhighlight %}







### shapeLayer.bubbleSettings.colorMappings<span class="type-signature type object">object</span>
{:#members:shapelayer-bubblesettings-colormappings}








Specifies the colorMappings of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set colorMappings API value during initialization 
  $("#container").ejMap({layers:{ bubbleSettings: {colorMappings:{rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorMappings API, after initialization:
        //Gets the colorMappings value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.colorMappings;
  
        //Sets the colorMappings value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.colorMappings={rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}; {% endhighlight %}







### shapeLayer.bubbleSettings.colorValuePath<span class="type-signature type string">string</span>
{:#members:shapelayer-bubblesettings-colorvaluepath}








Specifies the bubble color valuePath of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set colorValuePath  API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {colorValuePath :'sales'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorValuePath  API, after initialization:
        //Gets the colorValuePath  value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.colorValuePath ;
        
        //Sets the colorValuePath  value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.colorValuePath ='sales'; {% endhighlight %}







### shapeLayer.bubbleSettings.maxValue<span class="type-signature type number">number</span>
{:#members:shapelayer-bubblesettings-maxvalue}








Specifies the maximum size value of bubbles for shape layer in map




Default Value:
{:.param}






* "20"








Example
{:.example}


{% highlight html %}
 
//To set maxValue API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {maxValue:'20'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the maxValue API, after initialization:
        //Gets the maxValue value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.maxValue;
       
        //Sets the maxValue value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.maxValue='20'; {% endhighlight %}







### shapeLayer.bubbleSettings.minValue<span class="type-signature type number">number</span>
{:#members:shapelayer-bubblesettings-minvalue}








Specifies the minimum size value of bubbles for shape layer in map




Default Value:
{:.param}






* "10"








Example
{:.example}


{% highlight html %}
 
//To set minValue API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {minValue:'10'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the minValue API, after initialization:
        //Gets the minValue value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.minValue;
       
        //Sets the minValue value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.minValue='10'; {% endhighlight %}







### shapeLayer.bubbleSettings.showBubble<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-bubblesettings-showbubble}








Specifies the showBubble visibility status map




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//To set showBubble API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {showBubble:true}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the showBubble API, after initialization:
        //Gets the showBubble value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.showBubble;
     
        //Sets the showBubble value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.showBubble=true; {% endhighlight %}







### shapeLayer.bubbleSettings.showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-bubblesettings-showtooltip}








Specifies the tooltip visibility status of the shape layer in map




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set showTooltip API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {showTooltip:false}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the showTooltip API, after initialization:
        //Gets the showTooltip value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.showTooltip;
    
        //Sets the showTooltip value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.showTooltip=false; {% endhighlight %}







### shapeLayer.bubbleSettings.tooltipTemplate<span class="type-signature type string">string</span>
{:#members:shapelayer-bubblesettings-tooltiptemplate}








Specifies the bubble tooltip template of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set tooltipTemplate API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {tooltipTemplate:'template'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the tooltipTemplate API, after initialization:
        //Gets the tooltipTemplate value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.tooltipTemplate;
        
        //Sets the tooltipTemplate value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.tooltipTemplate='template'; {% endhighlight %}







### shapeLayer.bubbleSettings.valuePath<span class="type-signature type string">string</span>
{:#members:shapelayer-bubblesettings-valuepath}








Specifies the bubble valuePath of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set valuePath API value during initialization 
  $("#container").ejMap({layers: {bubbleSettings: {valuePath:'name'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the valuePath API, after initialization:
        //Gets the valuePath value 
  var bubbleProperty =$("#container").data("ejMap").model.layers[layerIndex].bubbleSettings.valuePath;
      
        //Sets the valuePath value 
        $("#container").data("ejMap").model.layers[0].bubbleSettings.valuePath='name'; {% endhighlight %}







### shapeLayer.dataSource<span class="type-signature type object">object</span>
{:#members:shapelayer-datasource}








Specifies the datasource for the shape layer





Example
{:.example}


{% highlight html %}
// Set the dataSource of layer during initialization.                        
        $("#container").ejMap({layers: [{ layerType: "geometry", dataSource: source,  shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the dataSource after initialization:
  //Gets the dataSource from map layer.
  var dataSource =$("#container").data("ejMap").model.layers[layerIndex].dataSource;
  //Sets the dataSource to map layer.
  $("#container").data("ejMap").model.layers[layerIndex].dataSource  = source;{% endhighlight %}







### shapeLayer.enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-enableanimation}








Enables or disables the animation




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
  
// Set the enableAnimation during initialization.                       
        $("#container").ejMap({layers: [{ enableAnimation:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the enableAnimation after initialization:
  //Gets the enableAnimation from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].enableAnimation;
  //Sets the enableAnimation to map.
  $("#container").data("ejMap").model.layers[layerIndex].enableAnimation  = false;{% endhighlight %}







### shapeLayer.enableMouseHover<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-enablemousehover}








Enables or disables the shape mouse hover




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
  
// Set the enableMouseHover during initialization.                      
        $("#container").ejMap({layers: [{ enableMouseHover:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the enableMouseHover after initialization:
  //Gets the enableMouseHover from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].enableMouseHover;
  //Sets the enableMouseHover to map.
  $("#container").data("ejMap").model.layers[layerIndex].enableMouseHover  = false;{% endhighlight %}







### shapeLayer.enableSelection<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-enableselection}








Enables or disables the shape selection




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
  
// Set the enableSelection during initialization.                       
        $("#container").ejMap({layers: [{ enableSelection:true }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the enableSelection after initialization:
  //Gets the enableSelection from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].enableSelection;
  //Sets the enableSelection to map.
  $("#container").data("ejMap").model.layers[layerIndex].enableSelection  = true;{% endhighlight %}







### shapeLayer.key<span class="type-signature type string">string</span>
{:#members:shapelayer-key}








to get the key of bing map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//to get the key of bing map during initialization 
        $("#container").ejMap({layers: [{  layerType: 'bing', key: "" }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the key of bing map after initialization:
        //Gets the key of bing map value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].key;     
        //Sets the bing map key value 
  $("#container").data("ejMap").model.layers[layerIndex].key = "";{% endhighlight %}







### shapeLayer.labelSettings<span class="type-signature type object">object</span>
{:#members:shapelayer-labelsettings}








Options for enabling and configuring labelSettings labelPath, smartLabelSize, labelLength etc.,











### shapeLayer.labelSettings.enableSmartLabel<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-labelsettings-enablesmartlabel}








enable or disable the enableSmartLabel property




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
// Set the enableSmartLabel value of layer during initialization.                    
        $("#container").ejMap({layers:[{labelSettings: { enableSmartLabel: false}}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the enableSmartLabel value after initialization:
  //Gets the enableSmartLabel value 
  var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.enableSmartLabel;
  //Sets the enableSmartLabel value
  $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { enableSmartLabel: false};                    {% endhighlight %}







### shapeLayer.labelSettings.labelLength<span class="type-signature type number">number</span>
{:#members:shapelayer-labelsettings-labellength}








set the labelLength property




Default Value:
{:.param}






* '2'








Example
{:.example}


{% highlight html %}
// Set the labelLength value of layer during initialization.                         
        $("#container").ejMap({layers:[{labelSettings: { labelLength: 2}}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the labelLength value after initialization:
  //Gets the labelLength value 
  var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.labelLength;
  //Sets the labelLength value
  $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { labelLength: 2};                     {% endhighlight %}







### shapeLayer.labelSettings.labelPath<span class="type-signature type string">string</span>
{:#members:shapelayer-labelsettings-labelpath}








set the labelPath property




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
// Set the labelPath value of layer during initialization.                   
        $("#container").ejMap({layers:[{labelSettings: { labelPath: ""}}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the labelPath value after initialization:
  //Gets the labelPath value 
  var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.labelPath;
  //Sets the labelPath value
  $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { labelPath: ""};                      {% endhighlight %}







### shapeLayer.labelSettings.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-labelsettings-showlabels}








enable or disable the showlabel property




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
// Set the showLabel value of layer during initialization.                   
        $("#container").ejMap({layers:[{labelSettings: { showLabels: false}}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showLabel value after initialization:
  //Gets the showLabel value 
  var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.showLabels;
  //Sets the showLabel value
  $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { showLabels: false};                  {% endhighlight %}







### shapeLayer.labelSettings.smartLabelSize<span class="type-signature type enum">enum</span>
{:#members:shapelayer-labelsettings-smartlabelsize}








set the smartLabelSize property




Default Value:
{:.param}






* "fixed"








Example
{:.example}


{% highlight html %}
// Set the smartLabelSize value of layer during initialization.                      
        $("#container").ejMap({layers:[{labelSettings: { smartLabelSize: 'fixed'}}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the smartLabelSize value after initialization:
  //Gets the smartLabelSize value 
  var labelSettings =$("#container").data("ejMap").model.layers[layerIndex].labelSettings.smartLabelSize;
  //Sets the smartLabelSize value
  $("#container").data("ejMap").model.layers[layerIndex].labelSettings = { smartLabelSize: 'fixed'};                    {% endhighlight %}







### shapeLayer.layerType<span class="type-signature type enum">enum</span>
{:#members:shapelayer-layertype}








Specifies the map type.




Default Value:
{:.param}






* 'geometry'








Example
{:.example}


{% highlight html %}
  
// Set the layerType during initialization.                     
        $("#container").ejMap({layers: [{ layerType:'geometry' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the layerType after initialization:
  //Gets the layerType from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].layerType;
  //Sets the layerType to map.
  $("#container").data("ejMap").model.layers[layerIndex].layerType  = 'geometry';{% endhighlight %}







### shapeLayer.legendSettings<span class="type-signature type object">object</span>
{:#members:shapelayer-legendsettings}








Options for enabling and configuring legendSettings position, height, width, mode, type etc.,











### shapeLayer.legendSettings.dockOnMap<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-legendsettings-dockonmap}








Determines whether the legend should be placed outside or inside the map bounds




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set dockOnMap API value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {dockOnMap:false} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the dockOnMap API, after initialization:
        //Gets the dockOnMap value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.dockOnMap;        
        //Sets the dockOnMap value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {dockOnMap:false};{% endhighlight %}







### shapeLayer.legendSettings.dockPosition<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-dockposition}








Determines the legend placement and it is valid only when dockOnMap is true




Default Value:
{:.param}






* "top"








Example
{:.example}


{% highlight html %}
 
//To set dockPosition value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {dockPosition:"top"} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set dockPosition value after initialization:
        //Gets the dockPosition value
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.dockPosition;     
        //Sets the dockPosition value value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {dockPosition:"top"};{% endhighlight %}







### shapeLayer.legendSettings.height<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-height}








height value for legend setting




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//To set height value for legend during initialization 
        $("#container").ejMap({layers: [{legendSettings: {height:20} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the height value for legend, after initialization:
        //Gets the height value for legend value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.height;   
        //Sets the height value for legend value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {height:20};{% endhighlight %}







### shapeLayer.legendSettings.icon<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-icon}








to get icon value for legend setting




Default Value:
{:.param}






* "rectangle"








Example
{:.example}


{% highlight html %}
 
//To set icon value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {icon:"rectangle"} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set icon value after initialization:
        //Gets the icon value value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.icon;     
        //Sets the icon value value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {icon:"rectangle"};{% endhighlight %}







### shapeLayer.legendSettings.iconHeight<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-iconheight}








icon height value for legend setting




Default Value:
{:.param}






* 20








Example
{:.example}


{% highlight html %}
 
//To set iconHeight value for legend during initialization 
        $("#container").ejMap({layers: [{legendSettings: {iconHeight:20} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the iconHeight value for legend, after initialization:
        //Gets the iconHeight value for legend value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.iconHeight;       
        //Sets the iconHeight value for legend value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {iconHeight:20};{% endhighlight %}







### shapeLayer.legendSettings.iconWidth<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-iconwidth}








icon Width value for legend setting




Default Value:
{:.param}






* 20








Example
{:.example}


{% highlight html %}
 
//To set iconWidth value for legend during initialization 
        $("#container").ejMap({layers: [{legendSettings: {iconWidth:20} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the iconWidth value for legend, after initialization:
        //Gets the iconWidth value for legend value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.iconWidth;        
        //Sets the iconWidth value for legend value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {iconWidth:20};{% endhighlight %}







### shapeLayer.legendSettings.labelOrientation<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-labelorientation}








set the orientation of legend labels




Default Value:
{:.param}






* vertical








Example
{:.example}


{% highlight html %}
 
//To set label orientaion API value for legend setting during initialization 
        $("#container").ejMap({layers: [{legendSettings: {labelOrientation: "vertical"} }]})                      {% endhighlight %}


{% highlight html %}
 
//Get or set the label orientation API, after initialization:
        //Gets the label orientation value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.labelOrientation; 
        //Sets the label orientation value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {labelOrientation: "vertical"};{% endhighlight %}







### shapeLayer.legendSettings.leftLabel<span class="type-signature type string">string</span>
{:#members:shapelayer-legendsettings-leftlabel}








to get leftLabel value for legend setting




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set leftLabel value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {leftLabel:""} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set leftLabel value after initialization:
        //Gets the leftLabel value value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.leftLabel;        
        //Sets the leftLabel value value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {leftLabel:""};{% endhighlight %}







### shapeLayer.legendSettings.mode<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-mode}








to get mode of legend setting




Default Value:
{:.param}






* "default"








Example
{:.example}


{% highlight html %}
 
//To set legend mode during initialization 
        $("#container").ejMap({layers: [{legendSettings: {mode:"default"} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the legend mode after initialization:
        //Gets the legend mode value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.mode;     
        //Sets the legend mode value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {mode:"default"};{% endhighlight %}







### shapeLayer.legendSettings.position<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-position}








set the position of legend settings




Default Value:
{:.param}






* topleft








Example
{:.example}


{% highlight html %}
 
//To set legend position API value for legend setting during initialization 
        $("#container").ejMap({layers: [{legendSettings: {position: "topleft"} }]})                      {% endhighlight %}


{% highlight html %}
 
//Get or set the legend position API, after initialization:
        //Gets the legend position value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.position; 
        //Sets the legend position value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {position: "topleft"};{% endhighlight %}







### shapeLayer.legendSettings.positionX<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-positionx}








x position value for legend setting




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//To set x position value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {positionX: 0} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the x position, after initialization:
        //Gets the x position value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.positionX;        
        //Sets the x position value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {positionX: 0};{% endhighlight %}







### shapeLayer.legendSettings.positionY<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-positiony}








y position value for legend setting




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//To set y position value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {positionY: 0} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the y position, after initialization:
        //Gets the y position value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.positionY;        
        //Sets the y position value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {positionY: 0};{% endhighlight %}







### shapeLayer.legendSettings.rightLabel<span class="type-signature type string">string</span>
{:#members:shapelayer-legendsettings-rightlabel}








to get rightLabel value for legend setting




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set rightLabel value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {rightLabel:""} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set rightLabel value after initialization:
        //Gets the rightLabel value value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.rightLabel;       
        //Sets the rightLabel value value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {rightLabel:""};{% endhighlight %}







### shapeLayer.legendSettings.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-legendsettings-showlabels}








Enables or Disables the showLabels




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set showLabels API value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {showLabels:false} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the showLabels API, after initialization:
        //Gets the showLabels value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.showLabels;       
        //Sets the showLabels value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {showLabels:false};{% endhighlight %}







### shapeLayer.legendSettings.showLegend<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-legendsettings-showlegend}








Enables or Disables the showLegend




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set showLegend API value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {showLegend:false} }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showLegend API, after initialization:
        //Gets the showLegend value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.showLegend;       
        //Sets the showLegend value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {showLegend:false};{% endhighlight %}







### shapeLayer.legendSettings.title<span class="type-signature type string">string</span>
{:#members:shapelayer-legendsettings-title}








to get title of legend setting




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set legend title during initialization 
        $("#container").ejMap({layers: [{legendSettings: {title: ""} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the legend title after initialization:
        //Gets the legend title value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.title;    
        //Sets the legend title value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {title: ""};{% endhighlight %}







### shapeLayer.legendSettings.type<span class="type-signature type enum">enum</span>
{:#members:shapelayer-legendsettings-type}








to get type of legend setting




Default Value:
{:.param}






* "layers"








Example
{:.example}


{% highlight html %}
 
//To set legend type value during initialization 
        $("#container").ejMap({layers: [{legendSettings: {type:"layers"} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the legend type value after initialization:
        //Gets the legend type value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.type;     
        //Sets the legend type value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {type:"layers"};{% endhighlight %}







### shapeLayer.legendSettings.width<span class="type-signature type number">number</span>
{:#members:shapelayer-legendsettings-width}








width value for legend setting




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
//To set width value for legend during initialization 
        $("#container").ejMap({layers: [{legendSettings: {width:20} }]})           {% endhighlight %}


{% highlight html %}
 
//Get or set the width value for legend, after initialization:
        //Gets the width value for legend value 
        var property = =$("#container").data("ejMap").model.layers[layerIndex].legendSettings.width;    
        //Sets the width value for legend value 
  $("#container").data("ejMap").model.layers[layerIndex].legendSettings  = {width:20};{% endhighlight %}







### shapeLayer.mapItemsTemplate<span class="type-signature type string">string</span>
{:#members:shapelayer-mapitemstemplate}








Specifies the map items template for shapes.





Example
{:.example}


{% highlight html %}
// Set the mapItemsTemplate of layer during initialization.                  
        $("#container").ejMap({layers: [{ layerType: "geometry", mapItemsTemplate: "Template",  shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the mapItemsTemplate after initialization:
  //Gets the mapItemsTemplate from map.
  var mapItemsTemplate =$("#container").data("ejMap").model.layers[layerIndex].mapItemsTemplate;
  //Sets the mapItemsTemplate to map.
  $("#container").data("ejMap").model.layers[layerIndex].mapItemsTemplate  = "Template";{% endhighlight %}







### shapeLayer.markers<span class="type-signature type marker">marker</span>
{:#members:shapelayer-markers}








Specify markers for shape layer.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
  
// Set the markers during initialization.                       
        $("#container").ejMap({layers: [{markers:[{label : "chennai",latitude : 13.08 ,longitude : 80.27}]}]}){% endhighlight %}


{% highlight html %}
 
//Get or set the markers after initialization:
  //Gets the markers from map.
  var marker =$("#container").data("ejMap").model.layers[layerIndex].markers[markerIndex];
  //Sets the marker to map.
  $("#container").data("ejMap").model.layers[layerIndex].markers[markerIndex]  = {label : "chennai",latitude : 13.08 ,longitude : 80.27};{% endhighlight %}







### shapeLayer.markerTemplate<span class="type-signature type string">string</span>
{:#members:shapelayer-markertemplate}








Specifies the map marker template for map layer.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
// Set the markerTemplate of layer during initialization.                    
        $("#container").ejMap({layers: [{ layerType: "geometry", markerTemplate: "Template",  shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the markerTemplate after initialization:
  //Gets the markerTemplate from map.
  var markerTemplate =$("#container").data("ejMap").model.layers[layerIndex].markerTemplate;
  //Sets the markerTemplate to map.
  $("#container").data("ejMap").model.layers[layerIndex].markerTemplate  = "Template";{% endhighlight %}







### shapeLayer.selectedMapShapes<span class="type-signature type object">object</span>
{:#members:shapelayer-selectedmapshapes}








Specify selectedMapShapes for shape layer




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
//Gets the selectedMapShapes from map 
        var selectedShapes =$("#container").data("ejMap").model.layers[layerIndex].selectedMapShapes;         {% endhighlight %}







### shapeLayer.selectionMode<span class="type-signature type enum">enum</span>
{:#members:shapelayer-selectionmode}








Specifies the selection mode of the map. Accepted selection mode values are Default and Multiple.




Default Value:
{:.param}






* "default"








Example
{:.example}


{% highlight html %}
  
// Set the selection mode during initialization.                        
        $("#container").ejMap({layers: [{ selectionMode:'default' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the selection mode after initialization:
  //Gets the selection mode from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].selectionMode;
  //Sets the selection mode to map.
  $("#container").data("ejMap").model.layers[layerIndex].selectionMode  = 'default';{% endhighlight %}







### shapeLayer.shapeData<span class="type-signature type object">object</span>
{:#members:shapelayer-shapedata}








Specifies the shape data for the shape layer





Example
{:.example}


{% highlight html %}
// Set the shapeData of layer during initialization.                         
        $("#container").ejMap({layers: [{ layerType: "geometry", shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the data after initialization:
  //Gets the data from map layer.
  var data =$("#container").data("ejMap").model.layers[layerIndex].shapeData;
  //Sets the data to map layer.
  $("#container").data("ejMap").model.layers[layerIndex].shapeData  = mapShapeData;{% endhighlight %}







### shapeLayer.shapeSettings<span class="type-signature type object">object</span>
{:#members:shapelayer-shapesettings}








Specifies the shape settings of map layer





Example
{:.example}


{% highlight html %}
// Set the shapeSettings of layer during initialization.                     
        $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the shapeSettings after initialization:
  //Gets the shapeSettings from map.
  var shapeSettings =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings;
  //Sets the shapeSettings to map.
  $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" }, shapeData: Africa };{% endhighlight %}







### shapeLayer.shapeSettings.autoFill<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-shapesettings-autofill}








Enables or Disables the auto fill colors for shape layer in map. When this property value set to true, shapes will be filled with palette colors.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set autoFill API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {autoFill:false}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the autoFill API, after initialization:
        //Gets the autoFill value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.autoFill;
         
        //Sets the autoFill value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.autoFill=false; {% endhighlight %}







### shapeLayer.shapeSettings.colorMappings<span class="type-signature type object">object</span>
{:#members:shapelayer-shapesettings-colormappings}








Specifies the colorMappings of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set colorMappings API value during initialization 
  $("#container").ejMap({layers:{ shapeSettings: {colorMappings:{rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorMappings API, after initialization:
        //Gets the colorMappings value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorMappings;
    
        //Sets the colorMappings value 
        $("#container").data("ejMap").model.layers[0].shapeSettings.colorMappings={rangeColorMapping:{from: 0,to: 100000,gradientColors: ["#9CBF4E", "#B8CE7B"]}}; {% endhighlight %}







### shapeLayer.shapeSettings.colorPalette<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-colorpalette}








Specifies the shape color palette value of the shape layer in map. Accepted colorPalette values are palette1, palette2, palette3 and custompalette.




Default Value:
{:.param}






* "palette1"








Example
{:.example}


{% highlight html %}
 
//To set colorPalette API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {colorPalette:'palette1'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorPalette API, after initialization:
        //Gets the colorPalette value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorPalette;
     
        //Sets the colorPalette value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.colorPalette='palette1'; {% endhighlight %}







### shapeLayer.shapeSettings.colorValuePath<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-colorvaluepath}








Specifies the shape color valuePath of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set colorValuePath  API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {colorValuePath :'sales'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorValuePath  API, after initialization:
        //Gets the colorValuePath  value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.colorValuePath ;
  
        //Sets the colorValuePath  value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.colorValuePath ='sales'; {% endhighlight %}







### shapeLayer.shapeSettings.enableGradient<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-shapesettings-enablegradient}








Enables or Disables the gradient colors for map shapes.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set enableGradient API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {enableGradient:false}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableGradient API, after initialization:
        //Gets the enableGradient value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.enableGradient;
   
        //Sets the enableGradient value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.enableGradient=false; {% endhighlight %}







### shapeLayer.shapeSettings.fill<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-fill}








Specifies the shape fill color of the shape layer in map




Default Value:
{:.param}






* "#E5E5E5"








Example
{:.example}


{% highlight html %}
 
//To set fill API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {fill:'#E5E5E5'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the fill API, after initialization:
        //Gets the fill value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.fill;
     
        //Sets the fill value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.fill='#E5E5E5'; {% endhighlight %}







### shapeLayer.shapeSettings.highlightBorderWidth<span class="type-signature type number">number</span>
{:#members:shapelayer-shapesettings-highlightborderwidth}








Specifies the mouse over width of the shape layer in map




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set highlightBorderWidth API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {highlightBorderWidth:1}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightBorderWidth API, after initialization:
        //Gets the highlightBorderWidth value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightBorderWidth;
     
        //Sets the highlightBorderWidth value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.highlightBorderWidth=1; {% endhighlight %}







### shapeLayer.shapeSettings.highlightColor<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-highlightcolor}








Specifies the mouse hover color of the shape layer in map




Default Value:
{:.param}






* "gray"








Example
{:.example}


{% highlight html %}
 
//To set highlightColor API value during initialization 
  $("#container").ejMap({layers:{shapeSettings: {highlightColor:'gray'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightColor API, after initialization:
        //Gets the highlightColor value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightColor;
   
        //Sets the highlightColor value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.highlightColor='gray'; {% endhighlight %}







### shapeLayer.shapeSettings.highlightStroke<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-highlightstroke}








Specifies the mouse over stroke color of the shape layer in map




Default Value:
{:.param}






* "#C1C1C1"








Example
{:.example}


{% highlight html %}
 
//To set highlightStroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {highlightStroke:'#C1C1C1'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightStroke API, after initialization:
        //Gets the highlightStroke value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.highlightStroke;
  
        //Sets the highlightStroke value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.highlightStroke='#C1C1C1'; {% endhighlight %}







### shapeLayer.shapeSettings.selectionColor<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-selectioncolor}








Specifies the shape selection color of the shape layer in map




Default Value:
{:.param}






* "gray"








Example
{:.example}


{% highlight html %}
 
//To set selectionColor API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionColor:'gray'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionColor API, after initialization:
        //Gets the selectionColor value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionColor;
   
        //Sets the selectionColor value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.selectionColor='gray'; {% endhighlight %}







### shapeLayer.shapeSettings.selectionStroke<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-selectionstroke}








Specifies the shape selection stroke color of the shape layer in map




Default Value:
{:.param}






* "#C1C1C1"








Example
{:.example}


{% highlight html %}
 
//To set selectionStroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionStroke:'#C1C1C1'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionStroke API, after initialization:
        //Gets the selectionStroke value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionStroke;
  
        //Sets the selectionStroke value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.selectionStroke='#C1C1C1'; {% endhighlight %}







### shapeLayer.shapeSettings.selectionStrokeWidth<span class="type-signature type number">number</span>
{:#members:shapelayer-shapesettings-selectionstrokewidth}








Specifies the shape selection stroke width of the shape layer in map




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set selectionStrokeWidth API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {selectionStrokeWidth:1}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the selectionStrokeWidth API, after initialization:
        //Gets the selectionStrokeWidth value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.selectionStrokeWidth;
     
        //Sets the selectionStrokeWidth value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.selectionStrokeWidth=1; {% endhighlight %}







### shapeLayer.shapeSettings.stroke<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-stroke}








Specifies the shape stroke color of the shape layer in map




Default Value:
{:.param}






* "#C1C1C1"








Example
{:.example}


{% highlight html %}
 
//To set stroke API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {stroke:'#C1C1C1'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the stroke API, after initialization:
        //Gets the stroke value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.stroke;
   
        //Sets the stroke value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.stroke='#C1C1C1'; {% endhighlight %}







### shapeLayer.shapeSettings.strokeThickness<span class="type-signature type number">number</span>
{:#members:shapelayer-shapesettings-strokethickness}








Specifies the shape stroke thickness value of the shape layer in map




Default Value:
{:.param}






* "0.2"








Example
{:.example}


{% highlight html %}
 
//To set strokeThickness API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {strokeThickness:'0.2'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the strokeThickness API, after initialization:
        //Gets the strokeThickness value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.strokeThickness;
  
        //Sets the strokeThickness value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.strokeThickness='0.2'; {% endhighlight %}







### shapeLayer.shapeSettings.valuePath<span class="type-signature type string">string</span>
{:#members:shapelayer-shapesettings-valuepath}








Specifies the shape valuePath of the shape layer in map




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set valuePath API value during initialization 
  $("#container").ejMap({layers: {shapeSettings: {valuePath:'name'}}});{% endhighlight %}


{% highlight html %}
 
//Get or set the valuePath API, after initialization:
        //Gets the valuePath value 
  var shapeProperty =$("#container").data("ejMap").model.layers[layerIndex].shapeSettings.valuePath;
        
        //Sets the valuePath value 
         $("#container").data("ejMap").model.layers[0].shapeSettings.valuePath='name'; {% endhighlight %}







### shapeLayer.showMapItems<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-showmapitems}








Shows or hides the map items.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
  
// Set the showMapItems during initialization.                  
        $("#container").ejMap({layers: [{ showMapItems:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showMapItems after initialization:
  //Gets the showMapItems from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].showMapItems;
  //Sets the showMapItems to map.
  $("#container").data("ejMap").model.layers[layerIndex].showMapItems  = false;{% endhighlight %}







### shapeLayer.showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:shapelayer-showtooltip}








Shows or hides the tooltip for shapes




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
  
// Set the showTooltip during initialization.                   
        $("#container").ejMap({layers: [{ showTooltip:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showTooltip after initialization:
  //Gets the showTooltip from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].showTooltip;
  //Sets the showTooltip to map.
  $("#container").data("ejMap").model.layers[layerIndex].showTooltip  = false;{% endhighlight %}







### shapeLayer.subLayers<span class="type-signature type shapelayer">shapeLayer</span>
{:#members:shapelayer-sublayers}








Specifies the sub shape layers




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
  
// Set the subLayers during initialization.                     
        $("#container").ejMap({layers: [{ layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },subLayers: [{shapeDataPath: "pathName", shapePropertyPath: "tableFieldName", mapItemsTemplate: 'Template', showMapItems: true, enableMouseHover: true, dataSource: mapDataSource, shapeSettings: { fill: "#9FD0D3", strokeThickness: "0.2", stroke: "white", highlightColor: "#63B7B7", },  shapeData: mapShapeData }, shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the layer after initialization:
  //Gets the layer from map.
  var layer =$("#container").data("ejMap").model.layers[layerIndex];
  //Sets the layer to map.
  $("#container").data("ejMap").model.layers[layerIndex]  = { layerType: "geometry", enableMouseHover: true, shapeSettings: { stroke: "black", fill: "#C3E6ED", highlightColor: "#63B7B7", selectionColor: "#207BB2", strokeThickness: "0.5" },subLayers: [{shapeDataPath: "pathName", shapePropertyPath: "tableFieldName", mapItemsTemplate: 'Template', showMapItems: true, enableMouseHover: true, dataSource: mapDataSource, shapeSettings: { fill: "#9FD0D3", strokeThickness: "0.2", stroke: "white", highlightColor: "#63B7B7", },  shapeData: mapSubShapeData }, shapeData: mapShapeData };{% endhighlight %}







### shapeLayer.tooltipTemplate<span class="type-signature type string">string</span>
{:#members:shapelayer-tooltiptemplate}








Specifies the tooltip template for shapes.





Example
{:.example}


{% highlight html %}
// Set the tooltipTemplate of layer during initialization.                   
        $("#container").ejMap({layers: [{ layerType: "geometry", tooltipTemplate: "Template",  shapeData: mapShapeData }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the tooltipTemplate after initialization:
  //Gets the tooltipTemplate from map.
  var tooltipTemplate =$("#container").data("ejMap").model.layers[layerIndex].tooltipTemplate;
  //Sets the tooltipTemplate to map.
  $("#container").data("ejMap").model.layers[layerIndex].tooltipTemplate  ="Template";{% endhighlight %}







### shapeLayer.urlTemplate<span class="type-signature type string">string</span>
{:#members:shapelayer-urltemplate}








Specifies the url template for the OSM type map.




Default Value:
{:.param}






* 'http://a.tile.openstreetmap.org/level/tileX/tileY.png'








Example
{:.example}


{% highlight html %}
  
// Set the urlTemplate during initialization.                   
        $("#container").ejMap({layers: [{ urlTemplate:'http://a.tile.openstreetmap.org/level/tileX/tileY.png' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the urlTemplate after initialization:
  //Gets the urlTemplate from map.
  var property =$("#container").data("ejMap").model.layers[layerIndex].urlTemplate;
  //Sets the urlTemplate to map.
  $("#container").data("ejMap").model.layers[layerIndex].urlTemplate  = 'http://a.tile.openstreetmap.org/level/tileX/tileY.png';{% endhighlight %}







### zoomSettings<span class="type-signature type object">object</span>
{:#members:zoomsettings}








Enables or Disables the Zooming for map.









## Methods








### navigateTo<span class="signature">(latitude, longitude, level)</span>
{:#methods:navigateto}








Method for navigating to specific shape based on latitude, longitude and zoomlevel.

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
latitude{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the latitude value for map</td>
</tr>
<tr>
<td class="name">{% highlight html %}
longitude{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the longitude value for map</td>
</tr>
<tr>
<td class="name">{% highlight html %}
level{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the zoom level for map</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//navigateTo method for map
$("#container").ejMap("navigateTo", lat, lon, level);{% endhighlight %}







### pan<span class="signature">(direction)</span>
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
<td class="name">{% highlight html %}
direction{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Pass the direction in which map should be panned</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//pan method for map
$("#container").ejMap("pan", direction);{% endhighlight %}







### refresh<span class="signature">()</span>
{:#methods:refresh}








Method to reload the map.





Example
{:.example}


{% highlight html %}
 
//refresh method for map
$("#container").ejMap("refresh");{% endhighlight %}







### refreshLayers<span class="signature">()</span>
{:#methods:refreshlayers}








Method to reload the shapeLayers with updated values





Example
{:.example}


{% highlight html %}
 
//refresh layers method for map
$("#container").ejMap("refreshLayers");{% endhighlight %}







### refreshNavigationControl<span class="signature">(navigation)</span>
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
<td class="name">{% highlight html %}
navigation{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Pass the navigation control instance</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//Refresh navigation control method for map
$("#container").ejMap("refreshNavigationControl",navigation);{% endhighlight %}







### zoom<span class="signature">(level, isAnimate)</span>
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
<td class="name">{% highlight html %}
level{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Pass the zoom level for map to be zoomed</td>
</tr>
<tr>
<td class="name">{% highlight html %}
isAnimate{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Pass the boolean value to enable or disable animation while zooming</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//zoom method for map
$("#container").ejMap("zoom",level,isAnimate);{% endhighlight %}





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
<td class="name">{% highlight html %}
originalEvent.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns marker object.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//markerSelected event for map
$("#container").ejMap({
   markerSelected: function (event) {}
});{% endhighlight %}







### mouseleave
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
<td class="name">{% highlight html %}
originalEvent.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns hovered map shape object.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//mouseleave  event for map
$("#container").ejMap({
   mouseleave : function (event) {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns hovered map shape object.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//mouseover  event for map
$("#container").ejMap({
   mouseover : function (event) {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from map</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//onRenderComplete event for map
$("#container").ejMap({
   onRenderComplete: function () {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from map</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//panned event for map
$("#container").ejMap({
   panned: function (event) {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected shape object.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//shapeSelected event for map
$("#container").ejMap({
   shapeSelected: function (event) {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from map</td>
</tr>
<tr>
<td class="name">{% highlight html %}
zoomLevel{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns zoom level value for which the map is zoomed.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//zoomedIn event for map
$("#container").ejMap({
   zoomedIn: function (event) {}
});{% endhighlight %}







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
<td class="name">{% highlight html %}
originalEvent{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from map</td>
</tr>
<tr>
<td class="name">{% highlight html %}
zoomLevel{% endhighlight %}</td>
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
});{% endhighlight %}


