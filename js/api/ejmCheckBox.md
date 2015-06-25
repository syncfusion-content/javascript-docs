---
layout: post
title: ejmCheckBox
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html CheckBox control.










$(element).ejmCheckBox<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
// Create checkbox control in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Render checkbox on initialization
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
$("#chkbox").ejmCheckBox(); 
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








Specifies whether to check the control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the checked property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-checked=false /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set checked API value during initialization  
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
 $("#chkbox").ejmCheckBox({ checked:  true });                                  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the check API, after initialization:
//Get the checked value  
        $("#chkbox").ejmCheckBox("option", "checked");
                      
        //Set the checked value 
        $("#chkbox").ejmCheckBox("option", "checked",  false );  </code>
</pre>






### checkState<span class="type-signature type enum">enum</span>








Specifies the check CheckState of the control. See <a href="global.html#CheckState">CheckState</a>




Default Value:
{:.param}






* ej.mobile.CheckBox.CheckState.Uncheck








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the Checkstate property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-enabletristate=true data-ej-checkstate="indeterminate" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the Checkstate property on initialization.
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set Checkstate API value 
  $("#chkbox").ejmCheckBox({ enableTriState : true,checkState: ej.mobile.CheckBox.CheckState.Indeterminate });          
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the CheckState  API, after initialization
//Get the CheckState  value 
  $("#chkbox").ejmCheckBox("option", "checkState");     
// Set the CheckState  value 
  $("#chkbox").ejmCheckBox("option", "checkState", ej.mobile.CheckBox.CheckState.Indeterminate  ); </code>
</pre>






### cssClass<span class="type-signature type string">string</span>








Sets the root class for checkbox theme. This cssClass API helps to use custom skinning option for checkbox control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the cssClass property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-cssclass="customclass" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code>// Set checkbox cssClass on initialization. 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set cssClass API value 
$("#chkbox").ejmCheckBox ({ cssClass: "customclass"});                  
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checkbox cssClass, after initialization:
// Get the cssClass API value.          
 $("#chkbox").ejmCheckBox ("option", "cssClass");                       
// Set the cssClass API
$("#chkbox").ejmCheckBox ("option", "cssClass", "customclass");            </code>
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
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-enabled=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//Set enabled property checkbox on initialization. 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set enabled API value 
        $("#chkbox").ejmCheckBox ({ enabled: true });                   
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checkbox state, after initialization:
// Get the enabled API value.           
        $("#chkbox").ejmCheckBox ("option", "enabled");                 
// Set the enabled API
        $("#chkbox").ejmCheckBox ("option", "enabled", true);</code>
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
// Set the enablePersistence property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-enablepersistence=true /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set enablePersistence API value 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
  $("#chkbox").ejmCheckBox({ enablePersistence: true});          
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the enablePersistence API, after initialization:
// Get the enablePersistence value  
  $("#chkbox").ejmCheckBox("option", "enablePersistence");                      
// Set the enablePersistence value 
  $("#chkbox").ejmCheckBox("option", "enablePersistence", true ); </code>
</pre>






### enableTriState<span class="type-signature type boolean">boolean</span>








Specifies whether to render the control with tri state behavior.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableTriState property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-enabletristate="true" data-ej-checkstate="indeterminate" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enableTriState property on initialization.
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set enableTriState  API value 
  $("#chkbox").ejmCheckBox({ enableTriState : true, checkState:"indeterminate" });              
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the enableTriState  API, after initialization
//Get the  enableTriState  value 
  $("#chkbox").ejmCheckBox("option", "enableTriState"); 
// Set the  enableTriState  value 
  $("#chkbox").ejmCheckBox("option", "enableTriState", false  ); </code>
</pre>






### preventDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to prevent default actions in the control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the preventDefault property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-preventdefault="false" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set checkbox prevent default on initialization. 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set preventDefault API value 
$("#chkbox").ejmCheckBox ({ preventDefault: false });                   
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checkbox prevent default, after initialization:
// Get the preventDefault API value.            
 $("#chkbox").ejmCheckBox ("option", "preventDefault");                 
// Set the preventDefault API
$("#chkbox").ejmCheckBox ("option", "preventDefault", false);</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Specifies the rendering mode of the control.See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the renderMode property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-rendermode="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code>// Set checkbox rendermode on initialization. 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
// To set renderMode API value 
$("#chkbox").ejmCheckBox ({ renderMode: ej.mobile.RenderMode.Auto});                    
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checkbox rendermode, after initialization:
// Get the renderMode API value.                
 $("#chkbox").ejmCheckBox ("option", "renderMode");                     
// Set the renderMode API
$("#chkbox").ejmCheckBox ("option", "renderMode", ej.mobile.RenderMode.Auto);            </code>
</pre>






### text<span class="type-signature type string">string</span>








Specifies the text.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the text property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-text="Checkbox" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set text API value 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
  $("#chkbox").ejmCheckBox({ text: "Hello World"});              
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the text API, after initialization:
// Get the text value  
  $("#chkbox").ejmCheckBox("option", "text");                   
// Set the text value 
  $("#chkbox").ejmCheckBox("option", "text", "Hello World" ); </code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Specifies the theme.See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-theme="auto" /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set checkbox theme on initialization. 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt; 
// To set Theme API value 
  $("#chkbox").ejmCheckBox ({ theme: ej.mobile.Theme.Auto });                   
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the checkbox prevent default, after initialization:
// Get the theme API value.             
  $("#chkbox").ejmCheckBox ("option", "theme");                 
// Set the theme API
  $("#chkbox").ejmCheckBox ("option", "theme", ej.mobile.Theme.Auto);</code>
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
// Set the windows mode renderDefault property in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-windows-renderDefault=false /&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// To set windows mode renderDefault property API value 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;  
$("#chkbox").ejmCheckBox({ windows:{renderDefault: false}});             
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the windows mode renderDefault API, after initialization:
// Get the windows mode renderDefault value  
$("#chkbox").ejmCheckBox("option", "windows.renderDefault");                    
// Set the windows mode renderDefault value 
$("#chkbox").ejmCheckBox("option", "windows.renderDefault", false); </code>
</pre>




## Methods








### isChecked<span class="signature">()</span>








To change the checked state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;script&gt;
// Create checkbox
$("#chkbox").ejmCheckBox();
var chkObj = $("#chkbox").data("ejmCheckBox");
chkObj.isChecked(); // returns the checkbox current state
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox" /&gt;
&lt;script&gt;
// get the checkbox current state
$("#chkbox").ejmCheckBox();
$("#chkbox").ejmCheckBox("isChecked");  
&lt;/script&gt;</code>
</pre>




## Events








### touchEnd








Event triggers when touch end happens on the control.

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
<td class="description last">Event parameters from CheckBox.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element associated value.</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the control.</td>
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
// Define the touchend event in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-touchend="touchend" /&gt;
&lt;script&gt; 
// touchEnd event for checkbox 
function touchend(args){ 
//handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>  
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" /&gt;
// touchEnd event for checkbox
* &lt;script&gt;
$("#chkbox").ejmCheckBox({
  touchEnd: function (args) { 
//handle the event 
}
});           
* &lt;/script&gt;</code>
</pre>






### touchStart








Event triggers when touch start happens on the control.

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
<td class="description last">Event parameters from CheckBox.
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
<td class="description last">returns true if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the model value of the control.</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element associated value.</td>
</tr>
<tr>
<td class="name"><code>isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the control.</td>
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
// Define the touchstart event in unobtrusive way.
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" data-ej-touchstart="touchstart" /&gt;
&lt;script&gt; 
// touchStart event for checkbox 
function touchstart(args){ 
//handle the event 
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>  
&lt;input type="checkbox" id="chkbox" data-role="ejmcheckbox" /&gt;
// touchStart event for checkbox
* &lt;script&gt;
$("#chkbox").ejmCheckBox({
  touchStart: function (args) { 
//handle the event 
}
});           
&lt;/script&gt;</code>
</pre>



