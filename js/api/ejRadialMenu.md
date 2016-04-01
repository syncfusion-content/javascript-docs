---
layout: post
title: Properties, Methods and Events of ejRadialMenu Widget
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html radialmenu control.





$(element).ejRadialMenu<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
// Create radialmenu in obtrusive way
<script> 
$(function(){
$("#defaultradialmenu").ejRadialMenu(); 
});
</script>
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.core

* module:ej.unobtrusive

* module:ej.data

* module:ej.touch


## Members




### autoOpen `boolean`
{:#members:autoopen}




To show the Radial in intial render.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu autoOpen on initialization. 
//To set autoOpen API 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "autoOpen":true });      
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu autoOpen, after initialization:
<script>
// Gets the autoOpen API.               
$("#defaultradialmenu").ejRadialMenu ("option", "autoOpen");                    
// Sets the autoOpen API
$("#defaultradialmenu").ejRadialMenu ("option", "autoOpen", true);            
</script>{% endhighlight %}




### backImageClass `string`
{:#members:backimageclass}




Renders the back button Image for Radial using class.


Default Value:
{:.param}



* e-backimage




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu back button Image on initialization. 
//To set back button image API 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "backImageClass":"e-backimage" });       
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu backImageClass, after initialization:
<script>
// Gets the backImageClass API.         
$("#defaultradialmenu").ejRadialMenu ("option", "backImageClass");                      
// Sets the backImageClass API
$("#defaultradialmenu").ejRadialMenu ("option", "backImageClass", "e-backimage");            
</script>{% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Sets the root class for RadialMenu theme. This cssClass API helps to use custom skinning option for RadialMenu control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu cssClass on initialization. 
//To set cssClass API 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "cssClass":"customclass" });     
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu cssClass, after initialization:
<script>
// Gets the cssClass API.               
$("#defaultradialmenu").ejRadialMenu ("option", "cssClass");                    
// Sets the cssClass API
$("#defaultradialmenu").ejRadialMenu ("option", "cssClass", "customclass");            
</script>{% endhighlight %}




### enableAnimation `boolean`
{:#members:enableanimation}




To enable Animation for Radial Menu.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu enableAnimation on initialization. 
//To set enableAnimation API 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "enableAnimation":true });       
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu enableAnimation, after initialization:
<script>
// Gets the enableAnimation API.                
$("#defaultradialmenu").ejRadialMenu ("option", "enableAnimation");                     
// Sets the enableAnimation API
$("#defaultradialmenu").ejRadialMenu ("option", "enableAnimation", true);            
</script>{% endhighlight %}




### imageClass `string`
{:#members:imageclass}




Renders the Image for Radial using Class.


Default Value:
{:.param}



* e-radialimage




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu Image on initialization. 
//To set image API  
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "imageClass":"e-radialimage" }); 
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu Image, after initialization:
<script>
// Gets the Image API.          
 $("#radialmenu").ejRadialMenu ("option", "imageClass");                        
// Sets the imageClass API
$("#radialmenu").ejRadialMenu ("option", "imageClass", "e-radialimage");            
</script>{% endhighlight %}




### radius `number`
{:#members:radius}




Specifies the radius of radial menu


Default Value:
{:.param}



* 150




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu radius on initialization. 
//To set radius API  
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "radius":150});  
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu radius, after initialization:
<script>
// Gets the radius API.         
 $("#radialmenu").ejRadialMenu ("option", "radius");                    
// Sets the radius API
$("#radialmenu").ejRadialMenu ("option", "radius", 150);            
</script>{% endhighlight %}




### targetElementId `string`
{:#members:targetelementid}




To show the Radial while clicking given target element.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
// Set Radialmenu targetelementid on initialization. 
//To set targetelementid API 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$(function () {
$("#defaultradialmenu").ejRadialMenu({ "targetElementId":"target" });   
});
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the Radialmenu targetelementid, after initialization:
<script>
// Gets the targetelementid API.                
$("#defaultradialmenu").ejRadialMenu ("option", "targetElementId");                     
// Sets the targetElementId API
$("#defaultradialmenu").ejRadialMenu ("option", "targetElementId", "target");            
</script>{% endhighlight %}



## Methods




### hide<span class="signature">()</span>
{:#methods:hide}




To hide the redialmenu



Example
{:.example}


{% highlight html %}
 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>{% endhighlight %}


{% highlight html %}
 
<script>
$("#defaultradialmenu").ejRadialMenu ("hide");
</script>{% endhighlight %}




### menuHide<span class="signature">()</span>
{:#methods:menuhide}




To hide the redialmenu items



Example
{:.example}


{% highlight html %}
 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>{% endhighlight %}


{% highlight html %}
 
<script>
$("#defaultradialmenu").ejRadialMenu ("menuHide");
</script>{% endhighlight %}




### show<span class="signature">()</span>
{:#methods:show}




To Show the redialmenu



Example
{:.example}


{% highlight html %}
 
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>{% endhighlight %}


{% highlight html %}
 
<script>
$("#defaultradialmenu").ejRadialMenu ("show");
</script>{% endhighlight %}



## Events




### mouseDown
{:#events:mousedown}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemName{% endhighlight %}</td>
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


{% highlight html %}
 
//MouseDown event for Radialmenu
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$("#defaultradialmenu").ejRadialMenu({
  mousedown: function (args) { //handle the event
}
});         
</script>{% endhighlight %}




### mouseUp
{:#events:mouseup}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemName{% endhighlight %}</td>
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


{% highlight html %}
 
//MouseUp event for Radialmenu
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$("#defaultradialmenu").ejRadialMenu({
  mouseup: function (args) { //handle the event
}
});         
</script>{% endhighlight %}




### select
{:#events:select}




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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Radialmenu model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
item{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
itemName{% endhighlight %}</td>
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


{% highlight html %}
 
//select event for Radialmenu
<div >
<br />
<p>
Syncfusion is the enterprise technology partner of choice for Windows development
</p>
</div>  
<div id="defaultradialmenu">
<ul>
<li data-ej-imageurl="../themes/sample/radialmenu/social.png"
data-ej-text="social"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/music.png" 
data-ej-text="music"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/direction.png" 
data-ej-text="direction"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/message.png" 
data-ej-text="message"></li>
<li data-ej-imageurl="../themes/sample/radialmenu/browser.png" 
data-ej-text="browser"></li>
</ul>
</div>
<script>
$("#defaultradialmenu").ejRadialMenu({
  select: function (args) { //handle the event
}
});         
</script>{% endhighlight %}



