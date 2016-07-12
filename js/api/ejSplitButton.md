---
layout: post
title: Properties, Methods and Events of ejSplitButton Widget
description: API reference for ejSplitButton
documentation: API
platform: js
keywords: SplitButton, ejSplitButton, syncfusion, SplitButton api 
---

# ejSplitButton



The Split button allows you to perform an action using clicking the button and choosing extra options from the dropdown button. The Split button also can display both text and images.








#### Syntax

{% highlight javascript %}

$(element).ejSplitButton()

{% endhighlight %}












#### Example



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







#### Requires


* module:jQuery


* module:jquery.easing


* module:ej.core.js


* module:ej.data.js


* module:ej.splitbutton.js


* module:ej.menu.js


* module:ej.checkbox.js




## Members








### arrowPosition `string|enum`
{:#members:arrowposition}


<ts name = "ej.ArrowPosition"/>








Specifies the arrowPosition of the Split or Dropdown Button.See arrowPosition



<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Left</td>
<td class="description">To set Left arrowPosition of the split button</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="description">To set Right arrowPosition of the split button</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="description">To set Top arrowPosition of the split button</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="description">To set Bottom arrowPosition of the split button</td>
</tr>
</tbody>
</table>







#### Default Value







* ej.ArrowPosition.Right








#### Example



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







### buttonMode `string|enum`
{:#members:buttonmode}


<ts name = "ej.ButtonMode"/>








Specifies the buttonMode like Split or Dropdown Button.See ButtonMode


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Split</td>
<td class="description">To specify  Split mode of the button type</td>
</tr>
<tr>
<td class="name">
Dropdown</td>
<td class="description">To specify Dropdown mode of the button type</td>
</tr>
</tbody>
</table>





#### Default Value







* ej.ButtonMode.Split








#### Example



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







### contentType `string|enum`
{:#members:contenttype}


<ts name = "ej.ContentType"/>








Specifies the contentType of the Split Button.See ContentType


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
TextOnly</td>
<td class="description">To specify the text contentType</td>
</tr>
<tr>
<td class="name">
ImageOnly</td>
<td class="description">To specify the image contentType</td>
</tr>
<tr>
<td class="name">
ImageBoth</td>
<td class="description">To specify the two images of contentType</td>
</tr>
<tr>
<td class="name">
TextAndImage</td>
<td class="description">To specify the Text and Image contentType</td>
</tr>
<tr>
<td class="name">
ImageTextImage</td>
<td class="description">To specify the image text and image contentType</td>
</tr>
</tbody>
</table>





#### Default Value







* ej.ContentType.TextOnly








#### Example



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







### cssClass `string`
{:#members:cssclass}








Set the root class for Split Button control theme




#### Default Value







* ""








#### Example



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







### enabled `boolean`
{:#members:enabled}








Specifies the disabling of Split Button if enabled is set to false.




#### Default Value







* true








#### Example



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







### enableRTL `boolean`
{:#members:enablertl}








Specifies the enableRTL property for Split Button while initialization.




#### Default Value







* false








#### Example



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







### height `string|number`
{:#members:height}








Specifies the height of the Split Button.




#### Default Value







* &ldquo;&rdquo;








#### Example



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







### htmlAttributes `object`
{:#members:htmlattributes}








Specifies the HTML Attributes of the Split Button.




#### Default Value







* {}








#### Example



{% highlight html %}
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script> 
//To set htmlAttributes API value during initialization  
$("#sbutton").ejSplitButton({  htmlAttributes : {disabled:"disabled"} });                       
</script>{% endhighlight %}







### imagePosition `string|enum`
{:#members:imageposition}


<ts name = "ej.ImagePosition"/>








Specifies the imagePosition of the Split Button.See imagePositions


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
ImageRight</td>
<td class="description">To specify Left position of the split button</td>
</tr>
<tr>
<td class="name">
ImageLeft</td>
<td class="description">To specify Right position of the split button</td>
</tr>
<tr>
<td class="name">
ImageTop</td>
<td class="description">To specify Top position of the split button</td>
</tr>
<tr>
<td class="name">
ImageBottom</td>
<td class="description">To specify Bottom position of the split button</td>
</tr>
</tbody>
</table>




#### Default Value







* ej.ImagePosition.ImageRight








#### Example



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







### prefixIcon `string`
{:#members:prefixicon}








Specifies the image content for Split Button while initialization.




#### Default Value







* ""








#### Example



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







### showRoundedCorner `string`
{:#members:showroundedcorner}








Specifies the showRoundedCorner property for Split Button while initialization.




#### Default Value







* false








#### Example



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







### size `string|enum`
{:#members:size}


<ts name = "ej.ButtonSize"/>








Specifies the size of the Button. See ButtonSize


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Mini</td>
<td class="description">To specify the minimum size of the split button</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="description">To specify the small size of the split button</td>
</tr>
<tr>
<td class="name">
Medium</td>
<td class="description">To specify the medium size of the split button</td>
</tr>
<tr>
<td class="name">
Large</td>
<td class="description">To specify the large size of the split button</td>
</tr>
<tr>
<td class="name">
Normal</td>
<td class="description">To specify the normal size of the split button</td>
</tr>
</tbody>
</table>




#### Default Value







* ej.ButtonSize.Normal








#### Example



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







### suffixIcon `string`
{:#members:suffixicon}








Specifies the image content for Split Button while initialization.




#### Default Value







* ""








#### Example



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







### targetID `string`
{:#members:targetid}








Specifies the list content for Split Button while initialization




#### Default Value







* ""








#### Example



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







### text `string`
{:#members:text}








Specifies the text content for Split Button while initialization.




#### Default Value







* ""








#### Example



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







### width `string|number`
{:#members:width}








Specifies the width of the Split Button.




#### Default Value







* &ldquo;&rdquo;








#### Example



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








### destroy()
{:#methods:destroy}








destroy the split button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





#### Example



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







### disable()
{:#methods:disable}








To disable the split button





#### Example



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







### enable()
{:#methods:enable}








To Enable the split button





#### Example



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







### hide()
{:#methods:hide}








To hide the list content of the split button.





#### Example



{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Hide the list content of the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.hide();
</script>{% endhighlight %}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To hide the list content of the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("hide");
</script>{% endhighlight %}







### show()
{:#methods:show}








To show the list content of the split button.





#### Example



{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To Show the list content of the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.show();
</script>{% endhighlight %}


{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//To show the list content of the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("show");
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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">
status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the button state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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







### close
{:#events:close}








Fires before the list content of Button control is closed

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//close event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     close: function (args) {}
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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
ID</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the menu item id</td>
</tr>
<tr>
<td class="name">
Text</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the clicked menu item text</td>
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




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
ID</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the menu item id</td>
</tr>
<tr>
<td class="name">
Text</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the clicked menu item text</td>
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




#### Example



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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name">
selectedItem</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected item</td>
</tr>
<tr>
<td class="name">
menuId</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the menu id</td>
</tr>
<tr>
<td class="name">
menuText</td>
<td class="type"><span class="param-type">String</span></td>
<td class="description">return the clicked menu item text</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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







### open
{:#events:open}








Fires before the list content of Button control is opened

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from split button
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the cancel option value</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.SplitButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the split button model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<button id="sbutton">File</button>
<ul id="target">
   <li><a href="#">Open..</a></li>
   <li><a href="#">Save</a></li>
   <li><a href="#">Delete</a></li>
</ul>
<script>
//open event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     open: function (args) {}
});
</script>{% endhighlight %}




