---
layout: post
title: ejSplitButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejSplitButton



The Split button allows you to perform an action using clicking the button and choosing extra options from the dropdown button. The Split button also can display both text and images.










$(element).ejSplitButton<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
// simple control creation
 $("#sbutton").ejSplitButton({targetID:"target",width:100});
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing


* module:ej.core.js


* module:ej.data.js


* module:ej.splitbutton.js


* module:ej.menu.js


* module:ej.checkbox.js




## Members








### arrowPosition<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:arrowposition}








Specifies the arrowPosition of the Split or Dropdown Button.See arrowPosition




Default Value:
{:.param}






* ej.ArrowPosition.Right








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set arrowPosition API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  buttonMode: ej.ButtonMode.Dropdown, arrowPosition: ej.ArrowPosition.Left, prefixIcon:"e-uiLight e-icon e-handup"});
</script>{% endhighlight %}







### buttonMode<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:buttonmode}








Specifies the buttonMode like Split or Dropdown Button.See <a href="global.html#ButtonMode">ButtonMode</a>




Default Value:
{:.param}






* ej.ButtonMode.Split








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set buttonMode API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  buttonMode: ej.ButtonMode.Dropdown, prefixIcon:"e-uiLight e-icon e-handup"});
</script>{% endhighlight %}







### contentType<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:contenttype}








Specifies the contentType of the Split Button.See <a href="global.html#ContentType">ContentType</a>




Default Value:
{:.param}






* ej.ContentType.TextOnly








Example
{:.example}


{% highlight html %}
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script> 
//To set contentType API value during initialization  
$("#sbutton").ejSplitButton({ targetID: "target",width:100, contentType:  ej.ContentType.TextOnly}); 
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Set the root class for Split Button control theme




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set cssClass API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,cssClass: "gradient-lime"});
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}








Specifies the disabling of Split Button if enabled is set to false.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set enabled API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100,enabled:  true });          
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}








Specifies the enableRTL property for Split Button while initialization.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set enableRTL API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,enableRTL : true});
</script>{% endhighlight %}







### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:height}








Specifies the height of the Split Button.




Default Value:
{:.param}






* &ldquo;28&rdquo; pixel








Example
{:.example}


{% highlight html %}
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script> 
//To set height API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100,height: 28 });                       
</script>{% endhighlight %}







### imagePosition<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:imageposition}








Specifies the imagePosition of the Split Button.See imagePositions




Default Value:
{:.param}






* ej.ImagePosition.ImageRight








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set imagePositions API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  imagePosition: ej.ImagePosition.ImageRight,prefixIcon:"e-uiLight e-icon e-handup"});
</script>{% endhighlight %}







### prefixIcon<span class="type-signature type string">String</span>
{:#members:prefixicon}








Specifies the image content for Split Button while initialization.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set prefixIcon API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,contentType: "imageonly",prefixIcon:"e-uiLight e-icon e-handup" });
</script>{% endhighlight %}







### showRoundedCorner<span class="type-signature type string">String</span>
{:#members:showroundedcorner}








Specifies the showRoundedCorner property for Split Button while initialization.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set showRoundedCorner API value during initialization  
$("#sbutton").ejSplitButton({ targetID:"target",width:100,showRoundedCorner: true});
</script>{% endhighlight %}







### size<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:size}








Specifies the size of the Button. See <a href="global.html#ButtonSize">ButtonSize</a>




Default Value:
{:.param}






* ej.ButtonSize.Normal








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set size API value during initialization  
        $("#sbutton").ejSplitButton({ targetID:"target",width:100, size: ej.ButtonSize.Mini});                  
</script>{% endhighlight %}







### suffixIcon<span class="type-signature type string">String</span>
{:#members:suffixicon}








Specifies the image content for Split Button while initialization.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set suffixIcon API value during initialization  
$("#sbutton").ejSplitButton({targetID:"target",width:100,contentType:"imageboth",prefixIcon:"e-uiLight e-icon-handup",suffixIcon:"e-uiLight e-icon-padlockclosed"});
</script>{% endhighlight %}







### targetID<span class="type-signature type string">String</span>
{:#members:targetid}








Specifies the list content for Split Button while initialization




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set targetID API value during initialization  
$("#sbutton").ejSplitButton({targetID:"target",width:100 });
</script>{% endhighlight %}







### text<span class="type-signature type string">String</span>
{:#members:text}








Specifies the text content for Split Button while initialization.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set text API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100, text: "New" });             
</script>{% endhighlight %}







### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:width}








Specifies the width of the Split Button.




Default Value:
{:.param}






* &ldquo;28&rdquo; pixel








Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To set width API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100 });                 
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the split button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Destroy the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.destroy();
</script>{% endhighlight %}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
// to destroy the button                
$("#sbutton").ejSplitButton({targetID: "target",width:100});    
$("#sbutton").ejSplitButton("destroy");
</script>{% endhighlight %}







### disable<span class="signature">()</span>
{:#methods:disable}








To disable the split button





Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Disable the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.disable();
</script>{% endhighlight %}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Disable the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("disable");
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








To Enable the split button





Example
{:.example}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Enable the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.enable();
</script>{% endhighlight %}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Enable the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("enable");
</script>{% endhighlight %}





## Events








### beforeOpen
{:#events:beforeopen}








Fires before menu of the split button control is opened.

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
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
// beforeOpen event for menu of split button control
 $("#sbutton").ejSplitButton({targetID: "target",width:100,
  beforeOpen: function (args) {}});
</script>{% endhighlight %}







### click
{:#events:click}








Fires when Button control is clicked successfully

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
<td class="description last">Event parameters from split button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the button state</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//click event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     click: function (args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








Fires after Split Button control is created.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splite button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//create event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     create: function (args) {}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires when the Split Button is destroyed successfully

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
<td class="description last">Event parameters from split button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//destroy event for split button
$("#sbutton"). ejSplitButton ({
               targetID: "target",width:100,
     destroy: function (args) {}
});
</script>{% endhighlight %}







### itemMouseOut
{:#events:itemmouseout}








Fires when a menu item is Hovered out successfully

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
<td class="description last">Event parameters from split button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event
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
ID{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu item id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Text{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the clicked menu item text</td>
</tr>
</tbody>
</table>
</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//itemMouseOut event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     itemMouseOut: function (args) {}
});
</script>{% endhighlight %}







### itemMouseOver
{:#events:itemmouseover}








Fires when a menu item is Hovered in successfully

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
<td class="description last">Event parameters from split button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event
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
ID{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu item id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
Text{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the clicked menu item text</td>
</tr>
</tbody>
</table>
</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//itemMouseOver event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     itemMouseOver: function (args) {}
});
</script>{% endhighlight %}







### itemSelected
{:#events:itemselected}








Fires when a menu item is clicked successfully

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
<td class="description last">Event parameters from split button
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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
selectedItem{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event.menuId{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
event.menuText{% endhighlight %}</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the clicked menu item text</td>
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
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//itemSelected event for split button
$("#sbutton"). ejSplitButton ({
               targetID: "target",width:100,
     itemSelected: function (args) {}
});
</script>{% endhighlight %}




