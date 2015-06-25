---
layout: post
title: ejmDatePicker
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html DatePicker control.










$(element).ejmDatePicker<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt; 
// Create DatePicker  
$("#datepicker").ejmDatePicker(); 
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


* module:ej.mobile.menu


* module:ej.mobile.header


* module:ej.mobile.dialog


* module:ej.mobile.button


* module:ej.mobile.toolbar


* module:ej.mobile.scrollpanel


* module:ej.mobile.scrollbar




## Members








### cssClass<span class="type-signature type string">string</span>








Sets the root class for DatePicker theme. This cssClass API helps to use custom skinning option for DatePicker control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the cssClass property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-cssclass="customclass" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the cssClass on initialization. 
//To set cssClass API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ cssClass: "customclass" });            
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cssClass, after initialization:
// Get the cssClass API value.          
 $("#datepicker").ejmDatePicker("option", "cssClass");                  
// Set the enablePersistence API
$("#datepicker").ejmDatePicker("option", "cssClass", "customclass");            </code>
</pre>






### culture<span class="type-signature type string">string</span>








Specifies the localization culture to be used.




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the culture property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-culture="en-US" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the culture on initialization. 
//To set culture API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ culture: "en-US" });           
});
&lt;/script&gt;                         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the culture, after initialization:
// Get the culture API value.           
 $("#datepicker").ejmDatePicker("option", "culture");                   
// Set the culture API
$("#datepicker").ejmDatePicker("option", "culture", "en-US");            </code>
</pre>






### dateFormat<span class="type-signature type string">string</span>








Specifies the date format.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the dateFormat property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-dateformat="MMMM dd, yyyy" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the dateFormat on initialization. 
//To set dateFormat API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ dateFormat: "MMMM dd, yyyy" });                
});
&lt;/script&gt;         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the dateFormat, after initialization:
// Get the dateFormat API value.                
 $("#datepicker").ejmDatePicker("option", "dateFormat");                        
// Set the dateFormat API
$("#datepicker").ejmDatePicker("option", "dateFormat", "MM/dd/yyyy");            </code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>








Specifies whether to enable or disbale the control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-enabled=false /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the enabled on initialization. 
//To set enabled API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ enabled: false });             
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enabled, after initialization:
// Get the enabled API value.           
 $("#datepicker").ejmDatePicker("option", "enabled");                   
// Set the enabled API
$("#datepicker").ejmDatePicker("option", "enabled", false);            </code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-enablepersistence=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the enablePersistence on initialization. 
//To set enablePersistence API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ enablePersistence: true });            
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#datepicker").ejmDatePicker("option", "enablePersistence");                 
// Set the enablePersistence API
$("#datepicker").ejmDatePicker("option", "enablePersistence", true);            </code>
</pre>






### ios7








Section for ios7 rendermode specific functionalities.











### ios7.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to use ios7 native datepicker or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the ios7 mode renderDefault property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-rendermode="ios7" data-ej-ios7-renderdefault=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set ios7 mode renderDefault property API value
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ renderMode:"ios7", ios: {renderDefault: true }});              
});
&lt;/script&gt;                  </code>
</pre>
<pre class="prettyprint">
<code>// Get or set the ios7 mode renderDefault API, after initialization:
// Get the ios7 mode renderDefault value  
$("#datepicker").ejmDatePicker("option", "ios7.renderDefault");                 
// Set the ios7 mode renderDefault value 
$("#datepicker").ejmDatePicker("option", "ios7.renderDefault", true); </code>
</pre>






### maxDate<span class="type-signature type string">string</span>








Specifies the maximum selectable date.




Default Value:
{:.param}






* "12/31/2030"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the maxDate property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-maxdate="12/31/2030" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the maxDtae on initialization. 
//To set maxDate API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ maxDate: "12/31/2030" });              
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxDate, after initialization:
// Get the maxDate API value.           
 $("#datepicker").ejmDatePicker("option", "maxDate");                   
// Set the maxDate API
$("#datepicker").ejmDatePicker("option", "maxDate", "31/12/2030");            </code>
</pre>






### minDate<span class="type-signature type string">string</span>








Specifies the minimum selectable date.




Default Value:
{:.param}






* "01/01/2000"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the minDate property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-mindate="01/01/2000" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the minDate on initialization. 
//To set minDate API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ minDate: "01/01/2000" });              
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minDate, after initialization:
// Get the minDate API value.           
 $("#datepicker").ejmDatePicker("option", "minDate");                   
// Set the minDate API
$("#datepicker").ejmDatePicker("option", "minDate", "01/01/2000");            </code>
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
//Set the renderMode property in Unobtrusive way.
&lt;input  id="datepicker" type="date" data-role="ejmdatepicker" data-ej-rendermode="android" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the renderMode on initialization. 
//To set renderMode API value 
&lt;input  id="datepicker" type="date"/&gt;
                 
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ renderMode: "android" });              
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the renderMode, after initialization:
// Get the renderMode API value.                
 $("#datepicker").ejmDatePicker("option", "renderMode");                        
// Set the renderMode API
$("#datepicker").ejmDatePicker("option", "renderMode", "android" );            </code>
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
//Set the theme property in Unobtrusive way.
&lt;input  id="datepicker" type="date" data-role="ejmdatepicker" data-ej-theme="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the theme on initialization. 
//To set theme API value 
&lt;input  id="datepicker" type="date"/&gt;
                 
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ theme: "auto" });              
});
&lt;/script&gt;                                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the theme, after initialization:
// Get the theme API value.             
 $("#datepicker").ejmDatePicker("option", "theme");                     
// Set the theme API
$("#datepicker").ejmDatePicker("option", "theme", "auto" );            </code>
</pre>






### value<span class="type-signature type string">string</span>








Specifies the value.




Default Value:
{:.param}






* new Date().toString()








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-value="04/23/2010" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the value on initialization. 
//To set value API value 
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ value: "04/23/2010" });                
});
&lt;/script&gt;                         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the value, after initialization:
// Get the value API value.             
 $("#datepicker").ejmDatePicker("option", "value");                     
// Set the value API
$("#datepicker").ejmDatePicker("option", "value", "04/23/2010");            </code>
</pre>






### windows








Section for windows rendermode specific functionalities.











### windows.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to render the DatePicker based on the windowsphone's current theme or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the windows mode renderDefault property in Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-rendermode="windows" data-ej-windows-renderdefault=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set windows mode renderDefault property API value
&lt;input id="datepicker" data-role="none"/&gt;
             
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker({ renderMode:"windows", windows: { renderDefault: true }});              
});
&lt;/script&gt;                          </code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the windows mode renderDefault API, after initialization:
// Get the windows mode renderDefault value  
$("#datepicker").ejmDatePicker("option", "windows.renderDefault");                      
// Set the windows mode renderDefault value 
$("#datepicker").ejmDatePicker("option", "windows.renderDefault", true); </code>
</pre>




## Methods








### disable<span class="signature">()</span>








To disable the datpicker





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.disable();
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
// changes the DatePicker current state to disabled     
$(function(){
$("#datepicker").ejmDatePicker("disable");      
});
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>








To enable the datepicker





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.enable();
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// change the DatePicker current state to enabled       
$("#datepicker").ejmDatePicker("enable");
});
&lt;/script&gt;</code>
</pre>






### getValue<span class="signature">()</span>








Get the current value.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.getValue();
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
// get the DatePicker current value             
$(function(){
$("#datepicker").ejmDatePicker("getValue");     
});
&lt;/script&gt;</code>
</pre>






### hide<span class="signature">()</span>








To hide the DatePicker control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.hide();
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker("hide");
});
&lt;/script&gt;</code>
</pre>






### setCurrentDate<span class="signature">()</span>








Set the given date.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.setCurrentDate("12/31/2000");
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
// get the DatePicker current value             
$(function(){
$("#datepicker").ejmDatePicker("setCurrentDate", "12/31/2000");
});
&lt;/script&gt;         </code>
</pre>






### show<span class="signature">()</span>








To show the DatePicker control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
// Create DatePicker
var dpObj = $("#datepicker").data("ejmDatePicker");
dpObj.show();
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="ejmdatepicker"/&gt;
&lt;script&gt;
$(function(){
$("#datepicker").ejmDatePicker("show"); 
});
&lt;/script&gt;</code>
</pre>




## Events








### change








Event triggers when the value is changed while interaction.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the change event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-change="change" /&gt;
&lt;script&gt;
function change(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//change event for DatePicker
$("#datepicker").ejmDatePicker({
   change: function (args) {* //handle the event 
}
});
&lt;/script&gt;                 </code>
</pre>






### close








Event triggers when the control is closed after interaction.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the close event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-close="close" /&gt;
&lt;script&gt;
function close(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//close event for DatePicker
$("#datepicker").ejmDatePicker({
   close: function (args) {* //handle the event 
}
});
&lt;/script&gt;                 </code>
</pre>






### focusIn








Event triggers when the input element is focused.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the focusin event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-focusin="focusin" /&gt;
&lt;script&gt;
function focusin(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//focusIn event for DatePicker
$("#datepicker").ejmDatePicker({
   focusIn: function (args) { * //handle the event 
}
});
&lt;/script&gt;                 </code>
</pre>






### focusOut








Event triggers when the input element is focusedout or blurred.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the focusout event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-focusout="focusout" /&gt;
&lt;script&gt;
function focusout(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//focusOut event for DatePicker
$("#datepicker").ejmDatePicker({
   focusOut: function (args) {* //handle the event 
}
}); 
&lt;/script&gt;                 </code>
</pre>






### load








Event triggers when the control is loaded.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the load event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-load="load" /&gt;
&lt;script&gt;
function load(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//load event for DatePicker
$("#datepicker").ejmDatePicker({
   load: function (args) {* //handle the event 
}
}); 
&lt;/script&gt;                 </code>
</pre>






### open








Event triggers when the control is opened for selection.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the open event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-open="open" /&gt;
&lt;script&gt;
function open(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//open event for DatePicker
$("#datepicker").ejmDatePicker({
   open: function (args) {* //handle the event 
}
});
&lt;/script&gt;                 </code>
</pre>






### select








Event triggers when date value is selected.

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
<td class="description last">Event parameters from datepicker
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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the datepicker value</td>
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
//Bind the select event using Unobtrusive way.
&lt;input id="datepicker" data-role="ejmdatepicker" data-ej-select="select" /&gt;
&lt;script&gt;
function select(){}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="datepicker" data-role="none"/&gt;
&lt;script&gt;
//select event for DatePicker
$("#datepicker").ejmDatePicker({
   select: function (args) { * //handle the event 
}
}); 
&lt;/script&gt;                 </code>
</pre>



