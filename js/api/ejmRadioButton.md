---
layout: post
title: ejmRadioButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html RadioButton control.










$(element).ejmRadioButton<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
// Create radiobutton control in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="radio" id="radbtn" /&gt;
&lt;script&gt; 
  // Create RadioButton  
  $("#radbtn").ejmRadioButton(); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.mobile.application


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core


* module:ej.data


* module:ej.touch




## Members








### checked<span class="type-signature type boolean">boolean</span>








Specifies the checked attribute.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the checked property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-checked=false /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set checked API value during initialization  
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
 $("#radbtn").ejmRadioButton({ checked:  true });                                       
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checked API, after initialization:
 //Gets the checked value  
 $("#radbtn").ejmRadioButton("option", "checked");
                  
 //Sets the checked value 
 $("#radbtn").ejmRadioButton("option", "checked",  false );  </code>
</pre>






### cssClass<span class="type-signature type string">string</span>








Sets the root class for RadioButton theme. This cssClass API helps to use custom skinning option for RadioButton control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the cssClass property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-cssclass="customclass" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set RadioButton cssClass on initialization. 
// To set renderMode API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
$(function() {
$("#radbtn").ejmRadioButton ({ cssClass: "customclass" });              
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the cssClass property, after initialization:
  // Gets the cssClass API value.               
  $("#radbtn").ejmRadioButton ("option", "cssClass");                   
  // Sets the cssClass API
  $("#radbtn").ejmRadioButton ("option", "cssClass", "customclass"); </code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>








Specifies whether the control is enabled or not.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-enabled=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Enabled RadioButton on initialization. 
  // To set width API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
        $("#radbtn").ejmRadioButton ({ enabled: true });                        
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the enabled state, after initialization:
  // Gets the Enabled API value.                
        $("#radbtn").ejmRadioButton ("option", "enabled");                      
  // Sets the Enabled API
        $("#radbtn").ejmRadioButton ("option", "enabled", true);</code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Saves current model value to browser cookies for state maintains. While refreshing the page retains the model value apply from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the enablePersistence property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-enablepersistence=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set enablePersistence API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
  $("#radbtn").ejmRadioButton({ enablePersistence: true});               
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the enablePersistence API, after initialization:
  // Gets the enablePersistence value  
  $("#radbtn").ejmRadioButton("option", "enablePersistence");                   
  // Sets the enablePersistence value 
  $("#radbtn").ejmRadioButton("option", "enablePersistence", true ); </code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Changes the rendering mode. See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the renderMode property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-rendermode="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set RadioButton rendermode on initialization. 
// To set renderMode API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
$(function() {
$("#radbtn").ejmRadioButton ({ renderMode: ej.mobile.RenderMode.Auto });                
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the renderMode property, after initialization:
  // Gets the renderMode API value.             
  $("#radbtn").ejmRadioButton ("option", "renderMode");                 
  // Sets the renderMode API
  $("#radbtn").ejmRadioButton ("option", "renderMode", ej.mobile.RenderMode.Auto); </code>
</pre>






### text<span class="type-signature type string">string</span>








Specifies the text content.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the text property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-text="RadioButton" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set text API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
  $("#radbtn").ejmRadioButton({ text: "Hello World"});           
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the text API, after initialization:
  // Gets the text value  
  $("#radbtn").ejmRadioButton("option", "text");                        
  // Sets the text value 
  $("#radbtn").ejmRadioButton("option", "text", "Hello World" ); </code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Changes the theme. See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-theme="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set theme property on initialization. 
  // To set theme API value 
&lt;input type="radio" id="radbtn"/&gt;
&lt;script&gt;
$(function(){
  $("#radbtn").ejmRadioButton ({ theme: ej.mobile.Theme.Auto });                        
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the theme API value, after initialization:
  // Gets the theme API value.          
  $("#radbtn").ejmRadioButton ("option", "theme");                      
  // Sets the theme API
  $("#radbtn").ejmRadioButton ("option", "theme", ej.mobile.Theme.Auto);</code>
</pre>




## Methods








### disable<span class="signature">()</span>








To disable the radio button.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" /&gt;
&lt;script&gt;
        $("#radbtn").ejmRadioButton ("disable");                        
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>








To enable the radio button





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" /&gt;
&lt;script&gt;
        $("#radbtn").ejmRadioButton ("enable");                 
&lt;/script&gt;</code>
</pre>




## Events








### change








Event triggers when the selection in radiobutton is changed.

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
<td class="description last">Event parameters from RadioButton
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
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element associated value</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the element</td>
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
// Define the change event in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-change="change" /&gt;
&lt;script&gt; 
// change event for RadioButton            
function change(args){ 
//handle the event here
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// change event for RadioButton
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton"/&gt;
&lt;script&gt; 
$("#radbtn").ejmRadioButton({
 change: function (args) { 
      //handle the event 
  }
});     
&lt;/script&gt; </code>
</pre>






### touchEnd








Event triggers when the touch end happens in the RadioButton.

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
<td class="description last">Event parameters from RadioButton
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
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element associated value</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the element</td>
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
// Define the touchend event in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-touchend="touchend" /&gt;
&lt;script&gt; 
// touchEnd event for RadioButton            
function touchend(args){ 
//handle the event here
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// touchEnd event for RadioButton
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton"/&gt;
&lt;script&gt; 
$("#radbtn").ejmRadioButton({
  touchEnd: function (args) { 
      //handle the event 
  }
});     
&lt;/script&gt; </code>
</pre>






### touchStart








event triggers when the touch start happens in the RadioButton.

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
<td class="description last">Event parameters from RadioButton
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
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element associated value</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the element</td>
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
// Define the touchstart event in Unobtrusive way.
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton" data-ej-touchstart="touchstart" /&gt;
&lt;script&gt; 
  // touchStart event for RadioButton 
  function touchstart(args){ 
      //handle the event 
  }
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// touchStart event for RadioButton
&lt;input type="radio" id="radbtn" data-role="ejmradiobutton"/&gt;
&lt;script&gt; 
$("#radbtn").ejmRadioButton({
  touchStart: function (args) { 
        //handle the event 
  }
});           
&lt;/script&gt; </code>
</pre>



