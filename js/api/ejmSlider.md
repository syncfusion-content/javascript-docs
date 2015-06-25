---
layout: post
title: ejmSlider
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html slider control.










$(element).ejmSlider<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create slider  
$("#slider").ejmSlider(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" &gt;&lt;/div&gt;
</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.mobile.application


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core


* module:ej.data


* module:ej.touch




## Members








### animationSpeed<span class="type-signature type int">int</span>








Specifies the animation speed when animation is enabled.




Default Value:
{:.param}






* 400








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the animationSpeed property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-animationSpeed=100 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider animationSpeed on initialization. 
//To set animationSpeed API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ animationSpeed: 400 });               
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider animationSpeed, after initialization:
// Get the animationSpeed API value.            
 $("#slider").ejmSlider ("option", "animationSpeed");                   
// Set the animationSpeed API
$("#slider").ejmSlider ("option", "animationSpeed", 400);  
&lt;/script&gt;</code>
</pre>






### enableAnimation<span class="type-signature type bool">bool</span>








Specifies whether to enable animation.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableanimation property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-enableanimation=true &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider enableanimation on initialization. 
//To set enableAnimation API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ enableAnimation: false });    
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider enableAnimation, after initialization:
// Get the enableAnimation API value.           
 $("#slider").ejmSlider ("option", "enableAnimation");                  
// Set the enableAnimation API
$("#slider").ejmSlider ("option", "enableAnimation", false);  
&lt;/script&gt;</code>
</pre>






### enabled<span class="type-signature type bool">bool</span>








Specifies whether to enable or disable the control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-enabled=true &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider enabled on initialization. 
//To set enabled API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ enabled: false });    
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider enabled, after initialization:
// Get the enabled API value.           
 $("#slider").ejmSlider ("option", "enabled");                  
// Set the enabled API
$("#slider").ejmSlider ("option", "enabled", true); 
&lt;/script&gt;</code>
</pre>






### enablePersistence<span class="type-signature type bool">bool</span>








Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-enablePersistence=false &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider enablePersistence on initialization. 
//To set persist API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ enablePersistence: false });  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#slider").ejmSlider ("option", "enablePersistence");                        
// Set the enablePersistence API
$("#slider").ejmSlider ("option", "enablePersistence", false);  
&lt;/script&gt;</code>
</pre>






### enableRange<span class="type-signature type bool">bool</span>








Specifies whether to enable range slider.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableRange property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-enablerange=false &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
// Set slider enableRange on initialization. 
//To set enableRange API value 
$("#slider").ejmSlider ({ enableRange: false });        
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider enableRange, after initialization:
// Get the enableRange API value.               
 $("#slider").ejmSlider ("option", "enableRange");                      
// Set the enableRange API
$("#slider").ejmSlider ("option", "enableRange", false);
&lt;/script&gt;</code>
</pre>






### incrementStep<span class="type-signature type int">int</span>








Specifies the step value for incrementation.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the incrementStep property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-incrementstep=1 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
// Set slider incrementStep on initialization. 
//To set incrementStep API value 
$("#slider").ejmSlider ({ incrementStep: 1 });
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider incrementStep, after initialization:
// Get the incrementStep API value.             
 $("#slider").ejmSlider ("option", "incrementStep");                    
// Set the incrementStep API
$("#slider").ejmSlider ("option", "incrementStep", 1);      
&lt;/script&gt;</code>
</pre>






### ios7








Section for ios7 mode specific functionalities.











### ios7.thumbStyle<span class="type-signature type enum">enum</span>








Specifies the thumb style in ios7 mode. See <a href="global.html#ThumbStyle">ThumbStyle</a>




Default Value:
{:.param}






* ej.mobile.Slider.ThumbStyle.Normal.








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the ios7 mode thumbStyle property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-rendermode="ios7" data-ej-ios7-thumbstyle="normal" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set ios7 mode thumbStyle property API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider({renderMode:"ios7", ios7:{thumbStyle: ej.mobile.Slider.ThumbStyle.Small}});   
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt; 
// Get or set the ios7 mode thumbStyle API, after initialization:
// Get the ios7 mode thumb style value  
$("#slider").ejmSlider("option", "ios7.thumbStyle");   
// Set the ios7 mode thumbStyle value 
$("#slider").ejmSlider("option", "ios7.thumbStyle", ej.mobile.Slider.ThumbStyle.Normal); 
&lt;/script&gt; </code>
</pre>






### maxValue<span class="type-signature type int">int</span>








Specifies the maximum value.




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the maxValue property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-maxValue=100 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider maxValue on initialization. 
//To set maxValue API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ maxValue: 100 });     
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider maxValue, after initialization:
// Get the maxValue API value.          
 $("#slider").ejmSlider ("option", "maxValue");                 
// Set the maxValue API
$("#slider").ejmSlider ("option", "maxValue", 100);    
&lt;/script&gt;</code>
</pre>






### minValue<span class="type-signature type int">int</span>








Specifies the minimum value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the minValue property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-minValue=0 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider minValue on initialization. 
//To set minValue API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ minValue: 0 });       
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider minValue, after initialization:
// Get the minValue API value.          
 $("#slider").ejmSlider ("option", "minValue");                 
// Set the minValue API
$("#slider").ejmSlider ("option", "minValue", 0);     
&lt;/script&gt;</code>
</pre>






### orientation<span class="type-signature type enum">enum</span>








Specifies whether the orientation is horizontal or vertical. See <a href="global.html#Orientation">Orientation</a>




Default Value:
{:.param}






* ej.mobile.Slider.Orientation.Horizontal.








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the orientation property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-orientation="horizontal" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider orientation on initialization. 
//To set orientation API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ orientation: ej.mobile.Slider.Orientation.Vertical });                        
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider orientation, after initialization:
// Get the orientation API value.               
 $("#slider").ejmSlider ("option", "orientation");                      
// Set the orientation API
$("#slider").ejmSlider ("option", "orientation", ej.mobile.Slider.Orientation.Horizontal);  
&lt;/script&gt;</code>
</pre>






### readOnly<span class="type-signature type bool">bool</span>








Specifies whether the control is read only.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the readOnly property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-readOnly=true &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider readOnly on initialization. 
//To set readOnly API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ readOnly: false });           
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider readOnly, after initialization:
// Get the readOnly API value.          
 $("#slider").ejmSlider ("option", "readOnly");                 
// Set the readOnly API
$("#slider").ejmSlider ("option", "readOnly", false);    
&lt;/script&gt;</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Specifies the rendering mode of the control. See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderMode property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-rendermode="auto" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider rendermode on initialization. 
//To set renderMode API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$(function(){
$("#slider").ejmSlider ({ renderMode: ej.mobile.RenderMode.Android });  
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt; 
//Get or set the slider rendermode, after initialization:
// Get the renderMode API value.                
 $("#slider").ejmSlider ("option", "renderMode");                       
// Set the renderMode API
$("#slider").ejmSlider ("option", "renderMode", ej.mobile.RenderMode.Android);      
&lt;/script&gt; </code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Specifies the theme. See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-theme="auto" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider theme on initialization. 
//To set theme API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$(function(){
$("#slider").ejmSlider ({ theme: ej.mobile.Theme.Dark });               
});
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider theme, after initialization:
// Get the theme API value.             
 $("#slider").ejmSlider ("option", "theme");                    
// Set the theme API
$("#slider").ejmSlider ("option", "theme", ej.mobile.Theme.Dark);        
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type int">int</span>








Specifies the current value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-value=0 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider value on initialization. 
//To set value API value 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$("#slider").ejmSlider ({ value: 50 }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider value, after initialization:
// Get the value API value.             
 $("#slider").ejmSlider ("option", "value");                    
// Set the value API
$("#slider").ejmSlider ("option", "value", 0);         
&lt;/script&gt;</code>
</pre>






### values<span class="type-signature type int[]">int[]</span>








Specifies the values when range slider is enabled.




Default Value:
{:.param}






* [20,80]








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the values property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-enablerange=true data-ej-values=[20,80] &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set slider values on initialization. 
//To set values API value
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
$(function(){
$("#slider").ejmSlider ({ enableRange: true,  values: [20,80] });
});
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the slider values, after initialization:
// Get the values API value.            
 $("#slider").ejmSlider ("option", "values");                   
// Set the values API
$("#slider").ejmSlider ("option", "values", [20,80]);  
&lt;/script&gt;</code>
</pre>






### windows








Section for windows mode specific functionalities.











### windows.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to render control based on the windowsphone's current accent color and device theme.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the windows mode renderDefault property in unobtrusive way.
&lt;div id="slider" data-role="ejmslider" data-ej-rendermode="windows" data-ej-windows-renderDefault=false &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
// To set windows mode renderDefault property API value 
$("#slider").ejmSlider({ renderMode:"windows", windows:{renderDefault: false}});   
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt; 
// Get or set the windows mode renderDefault API, after initialization:
// Get the windows mode renderDefault value  
$("#slider").ejmSlider("option", "windows.renderDefault");   
// Set the windows mode renderDefault value 
$("#slider").ejmSlider("option", "windows.renderDefault", false); 
&lt;/script&gt; </code>
</pre>




## Methods








### getValue<span class="signature">()</span>








To get the current value.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" &gt;&lt;/div&gt;
&lt;script&gt;
// Create slider
$(function(){
var slider = $("#slider").data("ejmSlider");
slider.getValue(); // returns the slider's current value
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider"&gt;&lt;/div&gt;
&lt;script&gt;
// get the slider's current value
$("#slider").ejmSlider();       
$(function(){
$("#slider").ejmSlider("getValue");     
});
&lt;/script&gt;</code>
</pre>




## Events








### change








Event triggers when the value changed.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from slider.
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current value of the control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" data-ej-change="onChange"&gt;&lt;/div&gt;
&lt;script&gt; 
// Change event for slider  
function onChange(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
//change event for slider
$("#slider").ejmSlider({
  change: function (args) { //handle the event 
}
});        
&lt;/script&gt;</code>
</pre>






### load








Event triggers before the control get loaded.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from slider.
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current value of the control.</td>
</tr>
<tr>
<td class="name"><code>values</code></td>
<td class="type"><span class="param-type">int[]</span></td>
<td class="description last">returns the current range values of the control when range slider feature is enabled.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" data-ej-load="onLoad" &gt;&lt;/div&gt;
&lt;script&gt; 
// Load event for slider  
function onLoad(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
//Load event for slider
$("#slider").ejmSlider({
  load: function (args) { //handle the event 
}
});    
&lt;/script&gt;</code>
</pre>






### slide








Event triggers when touch move happens on the control.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from slider.
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current value of the control.</td>
</tr>
<tr>
<td class="name"><code>values</code></td>
<td class="type"><span class="param-type">int[]</span></td>
<td class="description last">returns the current range values of the control when range slider feature is enabled.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" data-ej-slide="onslide"&gt;&lt;/div&gt;
&lt;script&gt; 
// slide event for slider  
function onslide(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
//Slide event for slider
$("#slider").ejmSlider({
  slide: function (args) { //handle the event 
}
});   
&lt;/script&gt;</code>
</pre>






### touchEnd








Event triggers when touch end happens on the control.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from slider.
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current value of the control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" data-ej-touchEnd="onStop"&gt;&lt;/div&gt;
&lt;script&gt; 
// touchEnd event for slider  
function onStop(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
//touchEnd event for slider
$("#slider").ejmSlider({
  touchEnd: function (args) { //handle the event 
}
});           
&lt;/script&gt;</code>
</pre>






### touchStart








Event triggers when touch start happens on the control.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from slider.
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current value of the control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="slider" data-role="ejmslider" data-ej-touchStart="onStart"&gt;&lt;/div&gt;
&lt;script&gt; 
// touchStart event for slider  
function onStart(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="slider" &gt;&lt;/div&gt;
&lt;script&gt;
//touchStart event for slider
$("#slider").ejmSlider({
  touchStart: function (args) { //handle the event 
}
});  
&lt;/script&gt;</code>
</pre>



