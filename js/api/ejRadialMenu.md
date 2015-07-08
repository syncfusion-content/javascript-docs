---
layout: post
title: ejRadialMenu
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html radialmenu control.





$(element).ejRadialMenu<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code>// Create radialmenu in obtrusive way
&lt;script&gt; 
$(function(){
$("#defaultradialmenu").ejRadialMenu(); 
});
&lt;/script&gt;
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.core

* module:ej.unobtrusive

* module:ej.data

* module:ej.touch


## Members




### autoOpen<span class="type-signature type boolean">boolean</span>
{:#members-autoopen}




To show the Radial in intial render.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu autoOpen on initialization. 
//To set autoOpen API 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "autoOpen":true });      
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu autoOpen, after initialization:
&lt;script&gt;
// Gets the autoOpen API.               
$("#defaultradialmenu").ejRadialMenu ("option", "autoOpen");                    
// Sets the autoOpen API
$("#defaultradialmenu").ejRadialMenu ("option", "autoOpen", true);            
&lt;/script&gt;</code>
</pre>



### backImageClass<span class="type-signature type string">string</span>
{:#members-backimageclass}




Renders the back button Image for Radial using class.


Default Value:
{:.param}



* e-backimage




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu back button Image on initialization. 
//To set back button image API 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "backImageClass":"e-backimage" });       
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu backImageClass, after initialization:
&lt;script&gt;
// Gets the backImageClass API.         
$("#defaultradialmenu").ejRadialMenu ("option", "backImageClass");                      
// Sets the backImageClass API
$("#defaultradialmenu").ejRadialMenu ("option", "backImageClass", "e-backimage");            
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}




Sets the root class for RadialMenu theme. This cssClass API helps to use custom skinning option for RadialMenu control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu cssClass on initialization. 
//To set cssClass API 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "cssClass":"customclass" });     
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu cssClass, after initialization:
&lt;script&gt;
// Gets the cssClass API.               
$("#defaultradialmenu").ejRadialMenu ("option", "cssClass");                    
// Sets the cssClass API
$("#defaultradialmenu").ejRadialMenu ("option", "cssClass", "customclass");            
&lt;/script&gt;</code>
</pre>



### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members-enableanimation}




To enable Animation for Radial Menu.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu enableAnimation on initialization. 
//To set enableAnimation API 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "enableAnimation":true });       
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu enableAnimation, after initialization:
&lt;script&gt;
// Gets the enableAnimation API.                
$("#defaultradialmenu").ejRadialMenu ("option", "enableAnimation");                     
// Sets the enableAnimation API
$("#defaultradialmenu").ejRadialMenu ("option", "enableAnimation", true);            
&lt;/script&gt;</code>
</pre>



### imageClass<span class="type-signature type string">string</span>
{:#members-imageclass}




Renders the Image for Radial using Class.


Default Value:
{:.param}



* e-radialimage




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu Image on initialization. 
//To set image API  
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "imageClass":"e-radialimage" }); 
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu Image, after initialization:
&lt;script&gt;
// Gets the Image API.          
 $("#radialmenu").ejRadialMenu ("option", "imageClass");                        
// Sets the imageClass API
$("#radialmenu").ejRadialMenu ("option", "imageClass", "e-radialimage");            
&lt;/script&gt;</code>
</pre>



### radius<span class="type-signature type int">int</span>
{:#members-radius}




Specifies the radius of radial menu


Default Value:
{:.param}



* 150




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu radius on initialization. 
//To set radius API  
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "radius":150});  
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu radius, after initialization:
&lt;script&gt;
// Gets the radius API.         
 $("#radialmenu").ejRadialMenu ("option", "radius");                    
// Sets the radius API
$("#radialmenu").ejRadialMenu ("option", "radius", 150);            
&lt;/script&gt;</code>
</pre>



### targetElementId<span class="type-signature type string">string</span>
{:#members-targetelementid}




To show the Radial while clicking given target element.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
// Set Radialmenu targetelementid on initialization. 
//To set targetelementid API 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "targetElementId":"target" });   
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the Radialmenu targetelementid, after initialization:
&lt;script&gt;
// Gets the targetelementid API.                
$("#defaultradialmenu").ejRadialMenu ("option", "targetElementId");                     
// Sets the targetElementId API
$("#defaultradialmenu").ejRadialMenu ("option", "targetElementId", "target");            
&lt;/script&gt;</code>
</pre>


## Methods




### hide<span class="signature">()</span>
{:#methods-hide}




To hide the redialmenu



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu ("hide");
&lt;/script&gt;</code>
</pre>



### menuHide<span class="signature">()</span>
{:#methods-menuhide}




To hide the redialmenu items



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu ("menuHide");
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#methods-show}




To Show the redialmenu



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu ("show");
&lt;/script&gt;</code>
</pre>


## Events




### mouseDown
{:#events-mousedown}




Event triggers when the mouse down happens.

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
<td class="description last">Event parameters from Radialmenu
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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
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
//MouseDown event for Radialmenu
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu({
  mousedown: function (args) { //handle the event
}
});         
&lt;/script&gt;</code>
</pre>



### mouseUp
{:#events-mouseup}




Event triggers when the mouse up happens.

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
<td class="description last">Event parameters from Radialmenu
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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
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
//MouseUp event for Radialmenu
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu({
  mouseup: function (args) { //handle the event
}
});         
&lt;/script&gt;</code>
</pre>



### select
{:#events-select}




Event triggers when we select an item.

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
<td class="description last">Event parameters from Radialmenu
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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
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
//select event for Radialmenu
&lt;div &gt;
&lt;br /&gt;
&lt;p&gt;
Syncfusion is the enterprise technology partner of choice for Windows development
&lt;/p&gt;
&lt;/div&gt;  
&lt;div id="defaultradialmenu"&gt;
&lt;ul&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"&gt;&lt;/li&gt;
&lt;li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#defaultradialmenu").ejRadialMenu({
  select: function (args) { //handle the event
}
});         
&lt;/script&gt;</code>
</pre>


