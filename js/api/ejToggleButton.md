---
layout: post
title: ejToggleButton
description: API reference for ejToggleButton
documentation: API
platform: js
keywords: ToggleButton, ejToggleButton, syncfusion, ToggleButton api  
---

# ejToggleButton




The Toggle Button allows you to perform the toggle option by using checked and unchecked state. This Toggle Button can be helpful to user to check their states. The Toggle Button control displays both text and images.



#### Syntax

{% highlight js %}

$(element).ejToggleButton()

{% endhighlight %}








#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Create ToggleButton 
$('#toggle').ejToggleButton({defaultText:"Play",activeText:"Pause"});   
    
</script> 

{% endhighlight %}




#### Requires


* module:jQuery

* module:ej.core.js

* module:ej.togglebutton.js

* module:ej.checkbox.js


## Members




### activePrefixIcon `string`
{:#members:activeprefixicon}



Specify the icon in active state to the toggle button and it will be aligned from left margin of the button.

N>  This is applicable for the content type&rsquo;s imageonly, textandimage, imagetextimage and imageboth.


#### Default Value




* ""




#### Example



{% highlight html %}
 

<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the activePrefixIcon during initialization.                      
        $("#toggle").ejToggleButton({ 
   defaultText:"Play",activeText:"Pause",
   contentType: "textandimage",
   defaultPrefixIcon: "e-mediaplay e-uiLight",
   activePrefixIcon: "e-mediapause e-uiLight",
 });                    
</script>

 {% endhighlight %}




### activeSuffixIcon `string`
{:#members:activesuffixicon}




Specify the icon in active state to the toggle button and it will be aligned from right margin of the button.

N>  This is applicable for the content type&rsquo;s imageonly, textandimage, imagetextimage and imageboth.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the activeSuffixIcon during initialization.                      
        $("#toggle").ejToggleButton({ 
   contentType: "imageboth",
   defaultSuffixIcon: "e-mediaplay e-uiLight",
   activeSuffixIcon: "e-mediapause e-uiLight",
 });                    
</script> 

{% endhighlight %}




### activeText `string`
{:#members:activetext}




Sets the text when ToggleButton is in active state i.e.,checked state.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set activeText API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                                   
</script> 
    
 {% endhighlight %}




### contentType `enum`
{:#members:contenttype}




Specifies the contentType of the ToggleButton. See <a href="global.html#ContentType">ContentType</a>


#### Default Value




* ej.ContentType.TextOnly




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the button contentType on initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",contentType : ej.ContentType.TextOnly });                    
</script> 

{% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Specify the CSS class to the ToggleButton to achieve custom theme.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the CSS class during initialization.                     
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",cssClass : "gradient-lime" });                        
</script> 

{% endhighlight %}




### defaultPrefixIcon `string`
{:#members:defaultprefixicon}




Specify the icon in default state to the toggle button and it will be aligned from left margin of the button.

N>  This is applicable for the content type&rsquo;s imageonly, textandimage, imagetextimage and imageboth.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the defaultPrefixIcon during initialization.                     
        $("#toggle").ejToggleButton({ 
   defaultText:"Play",activeText:"Pause",
   contentType: "textandimage",
   defaultPrefixIcon: "e-mediaplay e-uiLight",
   activePrefixIcon: "e-mediapause e-uiLight",
 });                    
</script> 

{% endhighlight %}




### defaultSuffixIcon `string`
{:#members:defaultsuffixicon}




Specify the icon in default state to the toggle button and it will be aligned from right margin of the button.

N>  This is applicable for the content type&rsquo;s imageonly, textandimage, imagetextimage and imageboth.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the defaultSuffixIcon during initialization.                     
 $("#toggle").ejToggleButton({ 
   defaultText:"Play",activeText:"Pause",
   contentType: "textandimage",
   defaultSuffixIcon: "e-mediaplay e-uiLight",
   activeSuffixIcon: "e-mediapause e-uiLight",
 });                    
</script> 

{% endhighlight %}




### defaultText `string`
{:#members:defaulttext}




Specifies the text of the ToggleButton, when the control is a default state. i.e., unChecked state.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set defaultText API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                           
</script> 
            
  {% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Specifies the state of the ToggleButton.


#### Default Value




* true




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set enabled API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enabled: true });                                            
</script> 
           
 {% endhighlight %}




### enablePersistence `boolean`
{:#members:enablepersistence}



Save current model value to browser cookies for maintaining states. When refreshing the ToggleButton control page, the model value is applied from browser cookies or HTML 5
local storage.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the rounded corner during initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",enablePersistence : true });                         
</script> 

{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Specify the Right to Left direction of the Togglebutton.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the enableRTL during initialization.                     
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enableRTL : true });                  
</script> 

{% endhighlight %}




### height `number/string`
{:#members:height}




Specifies the height of the ToggleButton.


#### Default Value




* 28pixel




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set height API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",height: "28px" });                                           
</script>        

 {% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}




It allows to define the characteristics of the ToggleButton control. It will helps to extend the capability of an HTML element.


#### Default Value




* {}




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// To Set HtmlAttributes on initialization.                     
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",htmlAttributes: {disabled:"disabled"} });                    
</script> 

{% endhighlight %}




### imagePosition `enum`
{:#members:imageposition}




Specifies the image position of the ToggleButton. 

N>  This image position is applicable only with the contentType property value set as textandimage. The images can be positioned in both imageLeft and imageRight options.


#### Default Value




* ej.ImagePosition.ImageLeft




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the image position for toggle button during initialization.                      
        $("#toggle").ejToggleButton(
{
   contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageRight,
   defaultText:"Play",activeText:"Pause",
   defaultPrefixIcon: "e-mediaplay e-uiLight",
   activePrefixIcon: "e-mediapause e-uiLight"
});                     
</script> 

{% endhighlight %}




### preventToggle `boolean`
{:#members:preventtoggle}


Allows to prevents the control switched to checked (active) state.
 
#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set preventToggle API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",preventToggle: false});                                              
</script> 

 {% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Display the ToggleButton with rounded corners.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the rounded corner during initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",showRoundedCorner : true });                         
</script> 

{% endhighlight %}




### size `enum`
{:#members:size}




Specifies the size of the ToggleButton. See <a href="global.html#ButtonSize">ButtonSize</a>


#### Default Value




* ej.ButtonSize.Normal




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set size API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",size: ej.ButtonSize.Mini});                                                                  
</script> 

{% endhighlight %}




### toggleState `boolean`
{:#members:togglestate}



It allows to define the ToggleButton state to checked(Active) or unchecked(Default) at initial time.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set toggleState API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",toggleState: false });       
</script> 

{% endhighlight %}




### type `enum`
{:#members:type}




Specifies the type of the ToggleButton. See <a href="global.html#ButtonType">ButtonType</a>


#### Default Value




* ej.ButtonType.Button




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set type API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",type:ej.ButtonType.Submit});                                                                 
</script> 

{% endhighlight %}




### width ``number/string``
{:#members:width}




Specifies the width of the ToggleButton.


#### Default Value




* 100pixel




#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set width API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",width: "100px" });                                           
</script> 

 {% endhighlight %}



## Methods




### destroy()
{:#methods:destroy}




To destroy the toggle button widget, all events bound using this._on will be unbind automatically and bring the control to pre-init state.



#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.destroy(); // destroy the toggle button
</script>

{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// destroy the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("destroy"); 
</script>

{% endhighlight %}




### disable()
{:#methods:disable}




To disable the ToggleButton to prevent all user interactions.



#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.disable(); // disable the toggle button
</script>

{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// disable the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("disable"); 
</script>

{% endhighlight %}




### enable()
{:#methods:enable}




To enable the ToggleButton.



#### Example



{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.enable(); // enable the toggle button
</script>

{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
 
<script>
// enable the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("enable");  
</script>

{% endhighlight %}



## Events




### change
{:#events:change}




Fires when ToggleButton control state is changed successfully.


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
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the toggle button checked state</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the toggle button model</td>
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
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//change event for toggle button
$("#toggle").ejToggleButton({
   defaultText:"Play",activeText:"Pause",
   change: function (args) {}
});  
</script> 
   
{% endhighlight %}




### click
{:#events:click}




Fires when ToggleButton control is clicked successfully.


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
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the toggle button checked state</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the toggle button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the toggle button state</td>
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
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//click event for toggle button
$("#toggle").ejToggleButton({
defaultText:"Play",activeText:"Pause",
   click: function (args) {}
}); 
</script> 
     
{% endhighlight %}




### create
{:#events:create}




Fires when ToggleButton control is created successfully.


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
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the toggle button model</td>
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
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//create event for toggle button
$("#toggle").ejToggleButton({
   defaultText:"Play",activeText:"Pause",
   create: function (args) {}
});   
</script> 
   {% endhighlight %}




### destroy
{:#events:destroy}




Fires when ToggleButton control is destroyed successfully.


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
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the toggle button model</td>
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
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//destroy event for toggle button
$("#toggle").ejToggleButton({
   defaultText:"Play",activeText:"Pause",
   destroy: function (args) {}
});  
</script> 

 {% endhighlight %}



