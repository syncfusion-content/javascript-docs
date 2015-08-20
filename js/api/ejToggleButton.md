---
layout: post
title: ejToggleButton
documentation: API
platform: js
metaname: 
metacontent: 
---

The Toggle Button allows you to perform the toggle option by using checked and unchecked state. This Toggle Button can be helpful to user to check their states. The Toggle Button control displays both text and images.





$(element).ejToggleButton<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Create ToggleButton 
$('#toggle').ejToggleButton({defaultText:"Play",activeText:"Pause"});   
    
</script> 
{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.togglebutton.js

* module:ej.checkbox.js


## Members




### activePrefixIcon<span class="type-signature type string">string</span>
{:#members:activeprefixicon}




Specify the activePrefixIcon to toggle button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


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
</script> {% endhighlight %}




### activeSuffixIcon<span class="type-signature type string">string</span>
{:#members:activesuffixicon}




Specify the activeSuffixIcon to toggle button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### activeText<span class="type-signature type string">string</span>
{:#members:activetext}




Specifies the activeText of the ToggleButton.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set activeText API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                                   
</script> 
    {% endhighlight %}




### contentType<span class="type-signature type enum">enum</span>
{:#members:contenttype}




Specifies the contentType of the ToggleButton. See <a href="global.html#ContentType">ContentType</a>


Default Value:
{:.param}



* ej.ContentType.TextOnly




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the button contentType on initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",contentType : ej.ContentType.TextOnly });                    
</script> 
{% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Specify the CSS class to toggle button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the CSS class during initialization.                     
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",cssClass : "gradient-lime" });                        
</script> 
{% endhighlight %}




### defaultPrefixIcon<span class="type-signature type string">string</span>
{:#members:defaultprefixicon}




Specify the defaultPrefixIcon to toggle button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### defaultSuffixIcon<span class="type-signature type string">string</span>
{:#members:defaultsuffixicon}




Specify the defaultSuffixIcon to toggle button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### defaultText<span class="type-signature type string">string</span>
{:#members:defaulttext}




Specifies the defaultText of the ToggleButton.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set defaultText API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                           
</script> 
            {% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Specifies the state of the ToggleButton.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set enabled API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enabled: true });                                            
</script> 
            {% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Specify the enablePersistence to Togglebutton to save current model value to browser cookies for state maintains


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the rounded corner during initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",enablePersistence : true });                         
</script> 
{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Specify the Right to Left Direction to Togglebutton


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the enableRTL during initialization.                     
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enableRTL : true });                  
</script> 
{% endhighlight %}




### height<span class="type-signature type string">String</span>
{:#members:height}




Specifies the height of the ToggleButton.


Default Value:
{:.param}



* 28pixel




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set height API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",height: "28px" });                                           
</script>         {% endhighlight %}




### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}




Specifies the HTML Attributes of the ToggleButton


Default Value:
{:.param}



* {}




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// To Set HtmlAttributes on initialization.                     
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",htmlAttributes: {disabled:"disabled"} });                    
</script> 
{% endhighlight %}




### imagePosition<span class="type-signature type enum">enum</span>
{:#members:imageposition}




Specifies the image position of the ToggleButton. This image position is applicable only with the textandimage contentType property. The images can be positioned in both imageLeft and imageRight options. See imagePositions


Default Value:
{:.param}



* ej.ImagePosition.ImageLeft




Example
{:.example}


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




### preventToggle<span class="type-signature type boolean">boolean</span>
{:#members:preventtoggle}




Specifies the preventToggle of the ToggleButton.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set preventToggle API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",preventToggle: false});                                              
</script> 
            {% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Specify the rounded corner to Togglebutton


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
// Set the rounded corner during initialization.                        
        $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",showRoundedCorner : true });                         
</script> 
{% endhighlight %}




### size<span class="type-signature type enum">enum</span>
{:#members:size}




Specifies the size of the ToggleButton. See <a href="global.html#ButtonSize">ButtonSize</a>


Default Value:
{:.param}



* ej.ButtonSize.Normal




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set size API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",size: ej.ButtonSize.Mini});                                                                  
</script> 
{% endhighlight %}




### toggleState<span class="type-signature type boolean">boolean</span>
{:#members:togglestate}




Specifies the toggleState of the ToggleButton.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set toggleState API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",toggleState: false });       
</script> 
    {% endhighlight %}




### type<span class="type-signature type enum">enum</span>
{:#members:type}




Specifies the type of the ToggleButton. See <a href="global.html#ButtonType">ButtonType</a>


Default Value:
{:.param}



* ej.ButtonType.Button




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set type API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",type:ej.ButtonType.Submit});                                                                 
</script> 
{% endhighlight %}




### width<span class="type-signature type string">String</span>
{:#members:width}




Specifies the width of the ToggleButton.


Default Value:
{:.param}



* 100pixel




Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//To set width API value during initialization  
        $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",width: "100px" });                                           
</script> 
                    {% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




To destroy the toggle button



Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.destroy(); // destroy the toggle button
</script>{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// destroy the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("destroy"); 
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the toggle button



Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.disable(); // disable the toggle button
</script>{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// disable the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("disable"); 
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the toggle button



Example
{:.example}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// Create toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
var toggleObj = $("#toggle").data("ejToggleButton");
toggleObj.enable(); // enable the toggle button
</script>{% endhighlight %}


{% highlight html %}
 
<input id="toggle" type="checkbox" / > 
 
<script>
// enable the toggle button
$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});
$("#toggle").ejToggleButton("enable");  
</script>{% endhighlight %}



## Events




### change
{:#events:change}




Fires when ToggleButton control state is changed successfully.

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
<td class="description last">Event parameters from toggle button
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the toggle button checked state</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the toggle button model</td>
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from toggle button
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the toggle button checked state</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the toggle button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the toggle button state</td>
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from toggle button
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the toggle button model</td>
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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from toggle button
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the toggle button model</td>
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
 
<input id="toggle" type="checkbox" /> 
        
<script> 
//destroy event for toggle button
$("#toggle").ejToggleButton({
   defaultText:"Play",activeText:"Pause",
   destroy: function (args) {}
});  
</script> 
    {% endhighlight %}



