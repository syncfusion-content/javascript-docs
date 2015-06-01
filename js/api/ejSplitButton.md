---
layout: post
title: ejSplitButton
documentation: API
platform: js
metaname: 
metacontent: 
---

The Split button allows you to perform an action using clicking the button and choosing extra options from the dropdown button. The Split button also can display both text and images.










#### $(element).ejSplitButton<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// simple control creation
 $("#sbutton").ejSplitButton({targetID:"target",width:100});
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing


* module:ej.core.js


* module:ej.data.js


* module:ej.splitbutton.js


* module:ej.menu.js


* module:ej.checkbox.js




### Members








#### arrowPosition<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the arrowPosition of the Split or Dropdown Button.See arrowPosition




Default Value:






* ej.ArrowPosition.Right








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set arrowPosition API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  buttonMode: ej.ButtonMode.Dropdown, arrowPosition: ej.ArrowPosition.Left, prefixIcon:"e-uiLight e-icon e-handup"});
&lt;/script&gt;</code>
</pre>






#### buttonMode<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the buttonMode like Split or Dropdown Button.See <a href="global.html#ButtonMode">ButtonMode</a>




Default Value:






* ej.ButtonMode.Split








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set buttonMode API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  buttonMode: ej.ButtonMode.Dropdown, prefixIcon:"e-uiLight e-icon e-handup"});
&lt;/script&gt;</code>
</pre>






#### contentType<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the contentType of the Split Button.See <a href="global.html#ContentType">ContentType</a>




Default Value:






* ej.ContentType.TextOnly








##### Example

<pre class="prettyprint">
<code>&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt; 
//To set contentType API value during initialization  
$("#sbutton").ejSplitButton({ targetID: "target",width:100, contentType:  ej.ContentType.TextOnly}); 
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">String</span>








Set the root class for Split Button control theme




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set cssClass API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,cssClass: "gradient-lime"});
&lt;/script&gt;</code>
</pre>






#### enabled<span class="type-signature type boolean">Boolean</span>








Specifies the disabling of Split Button if enabled is set to false.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set enabled API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100,enabled:  true });          
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">Boolean</span>








Specifies the enableRTL property for Split Button while initialization.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set enableRTL API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,enableRTL : true});
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Specifies the height of the Split Button.




Default Value:






* &ldquo;28&rdquo; pixel








##### Example

<pre class="prettyprint">
<code>&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt; 
//To set height API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100,height: 28 });                       
&lt;/script&gt;</code>
</pre>






#### imagePosition<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the imagePosition of the Split Button.See imagePositions




Default Value:






* ej.ImagePosition.ImageRight








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set imagePositions API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100, contentType: ej.ContentType.TextAndImage,
  imagePosition: ej.ImagePosition.ImageRight,prefixIcon:"e-uiLight e-icon e-handup"});
&lt;/script&gt;</code>
</pre>






#### prefixIcon<span class="type-signature type string">String</span>








Specifies the image content for Split Button while initialization.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set prefixIcon API value during initialization  
$("#sbutton").ejSplitButton({targetID: "target",width:100,contentType: "imageonly",prefixIcon:"e-uiLight e-icon e-handup" });
&lt;/script&gt;</code>
</pre>






#### showRoundedCorner<span class="type-signature type string">String</span>








Specifies the showRoundedCorner property for Split Button while initialization.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set showRoundedCorner API value during initialization  
$("#sbutton").ejSplitButton({ targetID:"target",width:100,showRoundedCorner: true});
&lt;/script&gt;</code>
</pre>






#### size<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the size of the Button. See <a href="global.html#ButtonSize">ButtonSize</a>




Default Value:






* ej.ButtonSize.Normal








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set size API value during initialization  
        $("#sbutton").ejSplitButton({ targetID:"target",width:100, size: ej.ButtonSize.Mini});                  
&lt;/script&gt;</code>
</pre>






#### suffixIcon<span class="type-signature type string">String</span>








Specifies the image content for Split Button while initialization.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set suffixIcon API value during initialization  
$("#sbutton").ejSplitButton({targetID:"target",width:100,contentType:"imageboth",prefixIcon:"e-uiLight e-icon-handup",suffixIcon:"e-uiLight e-icon-padlockclosed"});
&lt;/script&gt;</code>
</pre>






#### targetID<span class="type-signature type string">String</span>








Specifies the list content for Split Button while initialization




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set targetID API value during initialization  
$("#sbutton").ejSplitButton({targetID:"target",width:100 });
&lt;/script&gt;</code>
</pre>






#### text<span class="type-signature type string">String</span>








Specifies the text content for Split Button while initialization.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set text API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100, text: "New" });             
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Specifies the width of the Split Button.




Default Value:






* &ldquo;28&rdquo; pixel








##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To set width API value during initialization  
$("#sbutton").ejSplitButton({  targetID: "target",width:100 });                 
&lt;/script&gt;</code>
</pre>




### Methods








#### destroy<span class="signature">()</span>








destroy the split button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





##### Examples

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To Destroy the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.destroy();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// to destroy the button                
$("#sbutton").ejSplitButton({targetID: "target",width:100});    
$("#sbutton").ejSplitButton("destroy");
&lt;/script&gt;</code>
</pre>






#### disable<span class="signature">()</span>








To disable the split button





##### Examples

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To Disable the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.disable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To Disable the Split Button control.          
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("disable");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








To Enable the split button





##### Examples

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To Enable the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
var SptObj=$("#sbutton").data("ejSplitButton");
SptObj.enable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//To Enable the Split Button control.           
$("#sbutton").ejSplitButton({targetID: "target",width:100});
$("#sbutton").ejSplitButton("enable");
&lt;/script&gt;</code>
</pre>




### Events








#### beforeOpen








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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// beforeOpen event for menu of split button control
 $("#sbutton").ejSplitButton({targetID: "target",width:100,
  beforeOpen: function (args) {}});
&lt;/script&gt;</code>
</pre>






#### click








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//click event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     click: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### create








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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splite button model</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//create event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     create: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### destroy








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//destroy event for split button
$("#sbutton"). ejSplitButton ({
               targetID: "target",width:100,
     destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### itemMouseOut








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
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
<td class="name"><code>ID</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu item id</td>
</tr>
<tr>
<td class="name"><code>Text</code></td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//itemMouseOut event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     itemMouseOut: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### itemMouseOver








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>event</code></td>
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
<td class="name"><code>ID</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu item id</td>
</tr>
<tr>
<td class="name"><code>Text</code></td>
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




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//itemMouseOver event for split button
$("#sbutton"). ejSplitButton ({
                targetID: "target",width:100,
     itemMouseOver: function (args) {}
});
&lt;/script&gt;</code>
</pre>






#### itemSelected








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the split button model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>event.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the clicked menu item element</td>
</tr>
<tr>
<td class="name"><code>selectedItem</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected item</td>
</tr>
<tr>
<td class="name"><code>event.menuId</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the menu id</td>
</tr>
<tr>
<td class="name"><code>event.menuText</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">return the clicked menu item text</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;button id="sbutton"&gt;File&lt;/button&gt;
&lt;ul id="target"&gt;
   &lt;li&gt;&lt;a href="#"&gt;Open..&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Save&lt;/a&gt;&lt;/li&gt;
   &lt;li&gt;&lt;a href="#"&gt;Delete&lt;/a&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//itemSelected event for split button
$("#sbutton"). ejSplitButton ({
               targetID: "target",width:100,
     itemSelected: function (args) {}
});
&lt;/script&gt;</code>
</pre>



