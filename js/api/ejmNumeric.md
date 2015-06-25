---
layout: post
title: ejmNumeric
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Editor control.










$(element).ejmNumeric<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
// Create editor control in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Create editor control in obtrusive way.
&lt;input id="editor" type="number"/&gt;
&lt;script&gt;
$("#editor").ejmNumeric();
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








### cssClass<span class="type-signature type string">string</span>








Sets the root class for Editor theme. This cssClass API helps to use custom skinning option for Editor control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the cssClass property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-cssclass="customclass" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set cssClass on initialization. 
//To set cssClass API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ cssClass: "customclass" });
//Get or set the cssClass, after initialization:
// Get the cssClass API value.          
 $("#editor").ejmNumeric ("option", "cssClass");                
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Set the cssClass API
$("#editor").ejmNumeric ("option", "cssClass", "customclass");
&lt;/script&gt;</code>
</pre>






### decimalPlaces<span class="type-signature type number">number</span>








Specifies the decimal places to set the decimal(floating point) numbers.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the decimalPlaces property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-decimalPlaces="2" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set decimalPlaces on initialization. 
//To set decimalPlaces API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ decimalPlaces: 2 });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the decimalPlaces, after initialization:
// Get the decimalPlaces API value.             
 $("#editor").ejmNumeric ("option", "decimalPlaces");                   
// Set the decimalPlaces API
$("#editor").ejmNumeric ("option", " ", 2);     
&lt;/script&gt;</code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>








Specifies whether to enable or disable the control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-enabled="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set enabled on initialization. 
//To set enabled API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ enabled: false });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the enabled, after initialization:
// Get the enabled API value.           
 $("#editor").ejmNumeric ("option", "enabled");                 
// Set the enabled API
$("#editor").ejmNumeric ("option", "enabled", true);
&lt;/script&gt;</code>
</pre>






### enableStrictMode<span class="type-signature type boolean">boolean</span>








Specifies whether to restrict entering the values outside the defined range.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableStrictMode property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-minValue=0 data-ej-maxValue=100 data-ej-enableStrictMode="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set enableStrictMode on initialization. 
//To set enableStrictMode API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ maxValue: 100 , minValue: 0 , enableStrictMode: true });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the enableStrictMode, after initialization:
// Get the enableStrictMode API value.          
 $("#editor").ejmNumeric ("option", "enableStrictMode");                        
// Set the enableStrictMode API
$("#editor").ejmNumeric ("option", "enableStrictMode", true);
&lt;/script&gt;</code>
</pre>






### incrementStep<span class="type-signature type number">number</span>








Specifies the step value for incrementation.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the incrementStep property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-incrementStep="3" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set incrementStep on initialization. 
//To set incrementStep API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ incrementStep: 3 });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the incrementStep, after initialization:
// Get the incrementStep API value.             
 $("#editor").ejmNumeric ("option", "incrementStep");                   
// Set the incrementStep API
$("#editor").ejmNumeric ("option", "incrementStep", 3);
&lt;/script&gt;</code>
</pre>






### maxValue<span class="type-signature type number">number</span>








Specify the maximum value of the editor.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the maxValue property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-maxValue=500 /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set maxValue on initialization. 
//To setmaxValue API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ maxValue: 500 });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the maxValue, after initialization:
// Get the maxValue API value.          
 $("#editor").ejmNumeric ("option", "maxValue");                        
// Set the maxValue API
$("#editor").ejmNumeric ("option", "maxValue", 500);
&lt;/script&gt;</code>
</pre>






### minValue<span class="type-signature type number">number</span>








Specify the minimum value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the minValue property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-minValue=50 /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set minValue on initialization. 
//To set minValue API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ minValue: 50 });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the minValue, after initialization:
// Get the minValue API value.          
 $("#editor").ejmNumeric ("option", "minValue");                        
// Set the minValue API
$("#editor").ejmNumeric ("option", "minValue", 50);
&lt;/script&gt;</code>
</pre>






### name<span class="type-signature type string">string</span>








Specifies the name of the control.




Default Value:
{:.param}






* Sets id as name if it is null.








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the name property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-name="numeric" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set name on initialization. 
//To set name API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ name: "numeric" });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the name, after initialization:
// Get the name API value.              
 $("#editor").ejmNumeric ("option", "name");                    
// Set the name API
$("#editor").ejmNumeric ("option", "name", "numeric");
&lt;/script&gt;</code>
</pre>






### readOnly<span class="type-signature type boolean">boolean</span>








Specifies whether the control is read only to disable typing the value manually rather than updating by spin button.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the readOnly property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-readOnly="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set readOnly on initialization. 
//To set readOnly API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ readOnly: false });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the readOnly, after initialization:
// Get the readOnly API value.          
 $("#editor").ejmNumeric ("option", "readOnly");                        
// Set the readOnly API
$("#editor").ejmNumeric ("option", "readOnly", true);
&lt;/script&gt;</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Specifies the rendering mode of the control. See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderMode property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-renderMode="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set rendermode on initialization. 
//To set renderMode API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ renderMode: "auto" });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the rendermode after initialization:
// Get the renderMode API value.                
 $("#editor").ejmNumeric ("option", "renderMode");                      
// Set the renderMode API
$("#editor").ejmNumeric ("option", "renderMode", ej.mobile.RenderMode.Auto);
&lt;/script&gt;</code>
</pre>






### showBorder<span class="type-signature type boolean">boolean</span>








Specifies whether to show the border in the control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showBorder property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-showborder="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set showBorder on initialization. 
//To set showBorder API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ showBorder: false });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the showBorder, after initialization:
// Get the showBorder API value.                
 $("#editor").ejmNumeric ("option", "showBorder");                      
// Set the showBorder API
$("#editor").ejmNumeric ("option", "showBorder", true);
&lt;/script&gt;</code>
</pre>






### showSpinButton<span class="type-signature type boolean">boolean</span>








Specifies whether to show the spin button for incremention and decremention of the value.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showSpinButton property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-showSpinButton="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set showSpinButton on initialization. 
//To set showSpinButton API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ showSpinButton: false });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the showSpinButton, after initialization:
// Get the showSpinButton API value.            
 $("#editor").ejmNumeric ("option", "showSpinButton");                  
// Set the showSpinButton API
$("#editor").ejmNumeric ("option", "showSpinButton", true);
&lt;/script&gt;</code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Specifies the theme. See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-theme="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set theme on initialization. 
//To set theme API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ theme: ej.mobile.Theme.Auto });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the theme, after initialization:
// Get the theme API value.             
 $("#editor").ejmNumeric ("option", "theme");                   
// Set the theme API
$("#editor").ejmNumeric ("option", "theme", ej.mobile.Theme.Auto);
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type number">number</span>








Specifies the value of the editor.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-value="100" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set value on initialization. 
//To set value API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ value: 100 });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the value, after initialization:
// Get the value API value.             
 $("#editor").ejmNumeric ("option", "value");                   
// Set the value API
$("#editor").ejmNumeric ("option", "value", 100);
&lt;/script&gt;</code>
</pre>






### watermarkText<span class="type-signature type string">string</span>








Specifies the watermark text of the control.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the watermarkText property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-watermarkText="Enter the age" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set watermarkText on initialization. 
//To set watermarkText API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric ({ watermarkText: "Enter the age" });
//Get or set the watermarkText, after initialization:
// Get the watermarkText API value.             
 $("#editor").ejmNumeric ("option", "watermarkText");           
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
// Set the watermarkText API
$("#editor").ejmNumeric ("option", "watermarkText", "Enter the age");
&lt;/script&gt;</code>
</pre>






### windows








Section for windows mode specific functionalities.











### windows.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to render control based on the windowsphone's current accent color and device theme.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the windows mode renderDefault property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-renderMode="windows" data-ej-windows-renderDefault="true" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set windows mode renderDefault on initialization. 
//To set windows mode renderDefault API value 
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric({ renderMode:"windows",windows: { renderDefault: true } });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code>&lt;script&gt;
//Get or set the windows mode renderDefault, after initialization:
// Get the windows mode renderDefault API value.                
 $("#editor").ejmNumeric ("option", "windows.renderDefault");                   
// Set the windows mode renderDefault API
$("#editor").ejmNumeric ("option", "windows.renderDefault", true);
&lt;/script&gt;</code>
</pre>




## Methods








### disable<span class="signature">()</span>








To disable the numeric textbox.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Change the control status using disable method in obtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" /&gt;
&lt;script&gt;
// Call disable method.
$(document).ready(function(){
$("#editor").ejmNumeric("disable");
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>//Change the control status using disable method in obtrusive way.
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric("disable");
});
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>








To enable the numeric textbox.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Change the control status using enable method in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" /&gt;
&lt;script&gt;
// Call enable method.
$(document).ready(function(){
$("#editor").ejmNumeric("enable");
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>//Change the control status using enable method in obtrusive way.
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric("enable");
});
&lt;/script&gt;</code>
</pre>






### getValue<span class="signature">()</span>








To get the current value of the textbox.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Get the value using getValue function
&lt;input type="number" id="editor" data-role="ejmnumeric" /&gt;
&lt;script&gt;
// Call getValue method.
$(document).ready(function(){
$("#editor").ejmNumeric("getValue");
});
&lt;/script&gt;</code>
</pre>






### setValue<span class="signature">()</span>








Set value of the editor control.





Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value using setValue function 
&lt;input type="number" id="editor" data-role="ejmnumeric" /&gt;
&lt;script&gt;
$(document).ready(function(){
// Call setValue method.
$("#editor").ejmNumeric("setValue",50);
});
&lt;/script&gt;</code>
</pre>




## Events








### change








Event triggers after the control value gets changed.

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
<td class="description last">Event parameters from editors.
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the corresponding editor control value.</td>
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
//Set the windows mode renderDefault property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-change="change" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//Change event for editor
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric({
change: function (args) { //handle the event
}
});           
&lt;/script&gt;</code>
</pre>






### focusIn








Event triggers after the control gets focused.

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
<td class="description last">Event parameters from editors.
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">value</span></td>
<td class="description last">returns the corresponding editor control value.</td>
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
//Set the focusin property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-focusin="focusIn" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//focusIn event for editor
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric({
focusIn: function (args) { //handle the event
}
}); 
&lt;/script&gt;</code>
</pre>






### focusOut








Event triggers after the control gets focus out.

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
<td class="description last">Event parameters from editors.
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">value</span></td>
<td class="description last">returns the corresponding editor control value.</td>
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
//Set the focusin property in unobtrusive way.
&lt;input type="number" id="editor" data-role="ejmnumeric" data-ej-focusout="focusOut" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//focusOut event for editor
&lt;input type="number" id="editor" /&gt;
&lt;script&gt;
$(document).ready(function(){
$("#editor").ejmNumeric({
focusOut: function (args) { //handle the event
}
});   
&lt;/script&gt;</code>
</pre>



