---
layout: post
title: ejButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejButton

Custom Design for Html Button control.


$(element).ejButton<span class="signature">(options)</span>


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
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for button</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create Button
$('#button1').ejButton();       
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.button.js


## Members




### contentType<span class="type-signature type enum">enum</span>
{:#members:contenttype}




Specifies the contentType of the Button. See <a href="global.html#ContentType">ContentType</a>


Default Value:
{:.param}



* ej.ContentType.TextOnly




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the button contentType on initialization.                        
        $("#button1").ejButton({  contentType : ej.ContentType.ImageOnly,prefixIcon: "e-uiLight e-icon e-handup" });                    
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Specify the cssClass to button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the cssClass during initialization.                      
        $("#button1").ejButton({  cssClass : "gradient-lime" });                        
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Specifies the button control state.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Enable Button on initialization. 
        $("#button1").ejButton({ enabled:true });       
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Specify the Right to Left direction to button


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the enableRTL during initialization.                     
        $("#button1").ejButton({ contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageLeft,
   prefixIcon: "e-uiLight e-login", enableRTL : true });        
</script>                                 {% endhighlight %}




### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height of the Button.


Default Value:
{:.param}



* 28




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set height API value during initialization  
        $("#button1").ejButton({ height:"30px" });      
</script>                 {% endhighlight %}




### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}




Specifies the HTML Attributes of the ejButton


Default Value:
{:.param}



* {}




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set HtmlAttributes to Button on initialization. 
        $("#button1").ejButton({htmlAttributes : {disabled:"disabled"}});       
</script>{% endhighlight %}




### imagePosition<span class="type-signature type enum">enum</span>
{:#members:imageposition}




Specifies the image position of the Button. This image position is applicable only with the textandimage contentType property. The images can be positioned in both imageLeft and imageRight options. See <a href="global.html#ImagePosition">ImagePosition</a>


Default Value:
{:.param}



* ej.ImagePosition.ImageLeft




Example
{:.example}


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




### prefixIcon<span class="type-signature type string">string</span>
{:#members:prefixicon}




Specifies the primary icon for Button. This is applicable for the content type&rsquo;s imageOnly, textandimage, imagetextimage and imageboth.


Default Value:
{:.param}



* null




Example
{:.example}


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




### repeatButton<span class="type-signature type boolean">boolean</span>
{:#members:repeatbutton}




Convert the button as repeat button. It raises the 'Click' event repeattedly from the it is pressed until it is released.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Create repeat button during initialization.                  
        $("#button1").ejButton({  repeatButton : true });
</script>                 {% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Specify the rounded corner to button


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the showRoundedCorner during initialization.                     
        $("#button1").ejButton({  showRoundedCorner : true });                  
</script>                 {% endhighlight %}




### size<span class="type-signature type enum">enum</span>
{:#members:size}




Specifies the size of the Button. See <a href="global.html#ButtonSize">ButtonSize</a>


Default Value:
{:.param}



* ej.ButtonSize.Normal




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set size API value during initialization  
        $("#button1").ejButton({  size: ej.ButtonSize.Mini});   
</script>{% endhighlight %}




### suffixIcon<span class="type-signature type string">string</span>
{:#members:suffixicon}




Specifies the secondary icon for Button. This is applicable for the content type&rsquo;s imagetextimage and imageboth.


Default Value:
{:.param}



* null




Example
{:.example}


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




### text<span class="type-signature type string">string</span>
{:#members:text}




Specifies the text content for Button.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set the button text on initialization.                       
        $("#button1").ejButton({  text: "Hello Word" });
</script>                 {% endhighlight %}




### timeInterval<span class="type-signature type string">string</span>
{:#members:timeinterval}




Specified the timeInterval between two 'click' events while button in repeat button mode.


Default Value:
{:.param}



* "150"




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
// Set interval during initialization.                  
        $("#button1").ejButton({  
                        repeatButton : true,
                        timeInterval : "100" });
</script>{% endhighlight %}




### type<span class="type-signature type enum">enum</span> <span class="type-signature type string">string</span>
{:#members:type}




Specifies the Type of the Button. See <a href="global.html#ButtonType">ButtonType</a>


Default Value:
{:.param}



* ej.ButtonType.Submit




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set type API value during initialization  
        $("#button1").ejButton({type: ej.ButtonType.Submit});   
</script>{% endhighlight %}




### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width of the Button.


Default Value:
{:.param}



* 100




Example
{:.example}


{% highlight html %}
 
<button id="button1">Button</button> 
 
<script>
//To set width API value during initialization  
        $("#button1").ejButton({width: "150px"});       
</script>{% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


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




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the button



Example
{:.example}


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




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the button



Example
{:.example}


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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
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
