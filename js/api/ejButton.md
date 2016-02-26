---
layout: post
title: ejButton
description: API reference for ejButton
documentation: API
platform: js
keywords: Button, ejButton, syncfusion, button api
---

# ejButton

Custom Design for Html Button control.

#### Syntax

{% highlight js %}

$(element).ejButton(options)

{% endhighlight %}


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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">settings for button</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create Button
$('#button1').ejButton();       
</script>{% endhighlight %}


#### Requires


* module:jQuery

* module:ej.core.js

* module:ej.button.js


## Members




### contentType `enum`
{:#members:contenttype}




Specifies the contentType to be displayed over the Button. See <a href="global.html#ContentType">ContentType</a>


#### Default Value




* ej.ContentType.TextOnly




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the button contentType on initialization.                        
        $("#button1").ejButton({  contentType : ej.ContentType.ImageOnly,prefixIcon: "e-uiLight e-icon e-handup" });                    
</script>{% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Sets the root CSS class for Button theme, which is used customize. 


#### Default Value




* ""




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the cssClass during initialization.                      
        $("#button1").ejButton({  cssClass : "gradient-lime" });                        
</script>{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Specifies the button control state.


#### Default Value




* true




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Enable Button on initialization. 
        $("#button1").ejButton({ enabled:true });       
</script>{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Specify the Right to Left direction to button


#### Default Value




* false




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the enableRTL during initialization.                     
        $("#button1").ejButton({ contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageLeft,
   prefixIcon: "e-uiLight e-login", enableRTL : true });        
</script>                                 {% endhighlight %}




### height `number`
{:#members:height}




Specifies the height of the Button.


#### Default Value




* 28




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set height API value during initialization  
        $("#button1").ejButton({ height:"30px" });      
</script>                 {% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}




It allows to define the characteristics of the Button control. It will helps to extend the capability of an HTML element.


#### Default Value




* {}




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set HtmlAttributes to Button on initialization. 
        $("#button1").ejButton({htmlAttributes : {disabled:"disabled"}});       
</script>{% endhighlight %}




### imagePosition `enum`
{:#members:imageposition}




Specifies the image position of the Button. This image position is applicable only with the textandimage contentType property. The images can be positioned in both imageLeft and imageRight options. See <a href="global.html#ImagePosition">ImagePosition</a>


#### Default Value




* ej.ImagePosition.ImageLeft




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the image position for button during initialization.                     
        $("#button1").ejButton(
{
   contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageRight,
        prefixIcon: "e-uiLight e-icon e-handup" //Specifies the primary icon for Button
});     
</script>                 {% endhighlight %}




### prefixIcon `string`
{:#members:prefixicon}




Specifies the primary icon for Button. This icon will be displayed from the left margin of the button.

N>  This is applicable for the content type’s imageonly, textandimage, imagetextimage and imageboth.


#### Default Value




* null




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the primary icon during initialization.                  
        $("#button1").ejButton(
 {
    contentType: "imageonly",
    prefixIcon: "e-uiLight e-icon e-handup"
 });            
</script>{% endhighlight %}




### repeatButton `boolean`
{:#members:repeatbutton}




Convert the button as repeat button. It raises the 'Click' event repeattedly from the it is pressed until it is released.


#### Default Value




* false




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create repeat button during initialization.                  
        $("#button1").ejButton({  repeatButton : true });
</script>                 {% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Display the Button with rounded corners.


#### Default Value




* false




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the showRoundedCorner during initialization.                     
        $("#button1").ejButton({  showRoundedCorner : true });                  
</script>                 {% endhighlight %}




### size `enum`
{:#members:size}




Specifies the size of the Button. See <a href="global.html#ButtonSize">ButtonSize</a>


#### Default Value




* ej.ButtonSize.Normal




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set size API value during initialization  
        $("#button1").ejButton({  size: ej.ButtonSize.Mini});   
</script>{% endhighlight %}




### suffixIcon `string`
{:#members:suffixicon}



Specifies the secondary icon for Button. This icon will be displayed from the right margin of the button. 

N>   This is applicable for the content type’s imagetextimage and imageboth.


#### Default Value




* null




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the secondary icon during initialization.                        
        $("#button1").ejButton(
 {
      contentType: "imageonly",
                prefixIcon: "e-uiLight e-icon e-handup",
            suffixIcon: "e-uiLight e-icon e-padlockclosed"
 });            
</script>{% endhighlight %}




### text `string`
{:#members:text}




Specifies the text content for Button.


#### Default Value




* null




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the button text on initialization.                       
        $("#button1").ejButton({  text: "Hello Word" });
</script>                 {% endhighlight %}




### timeInterval `string`
{:#members:timeinterval}


Specified the time interval between two consecutive 'click' event on the button.

 N>   This is applicable for while the button in repeat button mode.


#### Default Value




* "150"




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set interval during initialization.                  
        $("#button1").ejButton({  
                        repeatButton : true,
                        timeInterval : "100" });
</script>{% endhighlight %}




### type `enum`  `string`
{:#members:type}




Specifies the Type of the Button. See <a href="global.html#ButtonType">ButtonType</a>


#### Default Value




* ej.ButtonType.Submit




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set type API value during initialization  
        $("#button1").ejButton({type: ej.ButtonType.Submit});   
</script>{% endhighlight %}




### width `number`
{:#members:width}




Specifies the width of the Button.


#### Default Value




* 100




#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set width API value during initialization  
        $("#button1").ejButton({width: "150px"});       
</script>{% endhighlight %}



## Methods




### destroy()
{:#methods:destroy}




destroy the button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.destroy(); // destroy the button
</script>{% endhighlight %}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// enable the button
$("#button1").ejButton();
$("#button1").ejButton("destroy");      
</script>{% endhighlight %}




### disable()
{:#methods:disable}




To disable the button



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.disable(); // disable the button
</script>{% endhighlight %}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// disable the button
$("#button1").ejButton();
$("#button1").ejButton("disable");      
</script>{% endhighlight %}




### enable()
{:#methods:enable}




To enable the button



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.enable(); // enable the button
</script>{% endhighlight %}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// enable the button
$("#button1").ejButton();
$("#button1").ejButton("enable");       
</script>{% endhighlight %}



## Events




### click
{:#events:click}




Fires when Button control is clicked successfully.Consider the scenario to perform any validation,modification of content or any other operations click on button,we can make use of this click event to achieve the scenario.


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the button state</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.e{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">return the event model for sever side processing. </td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//click event for button
$("#button1").ejButton({
   click: function (args) {
// Write a code block to perform operation while click on button.
}
});
</script>                  {% endhighlight %}




### create
{:#events:create}




Fires after Button control is created.If the user want to perform any operation after the button control creation then the user can make use of this create event.


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//create event for button
$("#button1").ejButton({
   create: function (args) {
// Write a code block to perform operation after creating the button.
}
});
</script>{% endhighlight %}




### destroy
{:#events:destroy}




Fires when the button is destroyed successfully.If the user want to perform any operation after the destroy button control then the user can make use of this destroy event.


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//destroy event for button
$("#button1").ejButton({
   destroy: function (args) {
// Write a code block to perform operation after destroy the button.
}
});
</script>{% endhighlight %}





<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>



<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
