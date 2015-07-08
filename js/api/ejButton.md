---
layout: post
title: ejButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Button control.





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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for button</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Create Button
$('#button1').ejButton();       
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.button.js


## Members




### contentType<span class="type-signature type enum">enum</span>
{:#members-contenttype}




Specifies the contentType of the Button. See <a href="global.html#ContentType">ContentType</a>


Default Value:
{:.param}



* ej.ContentType.TextOnly




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the button contentType on initialization.                        
        $("#button1").ejButton({  contentType : ej.ContentType.ImageOnly,prefixIcon: "e-uiLight e-icon e-handup" });                    
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}




Specify the cssClass to button to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the cssClass during initialization.                      
        $("#button1").ejButton({  cssClass : "gradient-lime" });                        
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#members-enabled}




Specifies the button control state.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Enable Button on initialization. 
        $("#button1").ejButton({ enabled:true });       
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members-enablertl}




Specify the Right to Left direction to button


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the enableRTL during initialization.                     
        $("#button1").ejButton({ contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageLeft,
   prefixIcon: "e-uiLight e-login", enableRTL : true });        
&lt;/script&gt;                                 </code>
</pre>



### height<span class="type-signature type number">number</span>
{:#members-height}




Specifies the height of the Button.


Default Value:
{:.param}



* 28




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//To set height API value during initialization  
        $("#button1").ejButton({ height:"30px" });      
&lt;/script&gt;                 </code>
</pre>



### htmlAttributes<span class="type-signature type object">object</span>
{:#members-htmlattributes}




Specifies the HTML Attributes of the ejButton


Default Value:
{:.param}



* {}




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set HtmlAttributes to Button on initialization. 
        $("#button1").ejButton({htmlAttributes : {disabled:"disabled"}});       
&lt;/script&gt;</code>
</pre>



### imagePosition<span class="type-signature type enum">enum</span>
{:#members-imageposition}




Specifies the image position of the Button. This image position is applicable only with the textandimage contentType property. The images can be positioned in both imageLeft and imageRight options. See <a href="global.html#ImagePosition">ImagePosition</a>


Default Value:
{:.param}



* ej.ImagePosition.ImageLeft




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the image position for button during initialization.                     
        $("#button1").ejButton(
{
   contentType: ej.ContentType.TextAndImage,
   imagePosition: ej.ImagePosition.ImageRight,
        prefixIcon: "e-uiLight e-icon e-handup" //Specifies the primary icon for Button
});     
&lt;/script&gt;                 </code>
</pre>



### prefixIcon<span class="type-signature type string">string</span>
{:#members-prefixicon}




Specifies the primary icon for Button. This is applicable for the content type&rsquo;s imageOnly, textandimage, imagetextimage and imageboth.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the primary icon during initialization.                  
        $("#button1").ejButton(
 {
    contentType: "imageonly",
    prefixIcon: "e-uiLight e-icon e-handup"
 });            
&lt;/script&gt;</code>
</pre>



### repeatButton<span class="type-signature type boolean">boolean</span>
{:#members-repeatbutton}




Convert the button as repeat button. It raises the 'Click' event repeattedly from the it is pressed until it is released.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Create repeat button during initialization.                  
        $("#button1").ejButton({  repeatButton : true });
&lt;/script&gt;                 </code>
</pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members-showroundedcorner}




Specify the rounded corner to button


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the showRoundedCorner during initialization.                     
        $("#button1").ejButton({  showRoundedCorner : true });                  
&lt;/script&gt;                 </code>
</pre>



### size<span class="type-signature type enum">enum</span>
{:#members-size}




Specifies the size of the Button. See <a href="global.html#ButtonSize">ButtonSize</a>


Default Value:
{:.param}



* ej.ButtonSize.Normal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//To set size API value during initialization  
        $("#button1").ejButton({  size: ej.ButtonSize.Mini});   
&lt;/script&gt;</code>
</pre>



### suffixIcon<span class="type-signature type string">string</span>
{:#members-suffixicon}




Specifies the secondary icon for Button. This is applicable for the content type&rsquo;s imagetextimage and imageboth.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the secondary icon during initialization.                        
        $("#button1").ejButton(
 {
      contentType: "imageonly",
                prefixIcon: "e-uiLight e-icon e-handup",
            suffixIcon: "e-uiLight e-icon e-padlockclosed"
 });            
&lt;/script&gt;</code>
</pre>



### text<span class="type-signature type string">string</span>
{:#members-text}




Specifies the text content for Button.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set the button text on initialization.                       
        $("#button1").ejButton({  text: "Hello Word" });
&lt;/script&gt;                 </code>
</pre>



### timeInterval<span class="type-signature type string">string</span>
{:#members-timeinterval}




Specified the timeInterval between two 'click' events while button in repeat button mode.


Default Value:
{:.param}



* "150"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Set interval during initialization.                  
        $("#button1").ejButton({  
                        repeatButton : true,
                        timeInterval : "100" });
&lt;/script&gt;</code>
</pre>



### type<span class="type-signature type enum">enum</span> <span class="type-signature type string">string</span>
{:#members-type}




Specifies the Type of the Button. See <a href="global.html#ButtonType">ButtonType</a>


Default Value:
{:.param}



* ej.ButtonType.Submit




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//To set type API value during initialization  
        $("#button1").ejButton({type: ej.ButtonType.Submit});   
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type number">number</span>
{:#members-width}




Specifies the width of the Button.


Default Value:
{:.param}



* 100




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//To set width API value during initialization  
        $("#button1").ejButton({width: "150px"});       
&lt;/script&gt;</code>
</pre>


## Methods




### destroy<span class="signature">()</span>
{:#methods-destroy}




destroy the button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.destroy(); // destroy the button
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// enable the button
$("#button1").ejButton();
$("#button1").ejButton("destroy");      
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#methods-disable}




To disable the button



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.disable(); // disable the button
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// disable the button
$("#button1").ejButton();
$("#button1").ejButton("disable");      
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#methods-enable}




To enable the button



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// Create Button
$("#button1").ejButton();
var btnObj = $("#button1").data("ejButton");
btnObj.enable(); // enable the button
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
// enable the button
$("#button1").ejButton();
$("#button1").ejButton("enable");       
&lt;/script&gt;</code>
</pre>


## Events




### click
{:#events-click}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
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

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//click event for button
$("#button1").ejButton({
   click: function (args) {
// Write a code block to perform operation while click on button.
}
});
&lt;/script&gt;                  </code>
</pre>



### create
{:#events-create}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//create event for button
$("#button1").ejButton({
   create: function (args) {
// Write a code block to perform operation after creating the button.
}
});
&lt;/script&gt;</code>
</pre>



### destroy
{:#events-destroy}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;button id="button1"&gt;Button&lt;/button&gt; 
 
&lt;script&gt;
//destroy event for button
$("#button1").ejButton({
   destroy: function (args) {
// Write a code block to perform operation after destroy the button.
}
});
&lt;/script&gt;</code>
</pre>




<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>



<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
