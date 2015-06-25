---
layout: post
title: ejmGroupButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html GroupButton control.










$(element).ejmGroupButton<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
//Render groupbutton control by default with button behavior in unobtrusive way
&lt;div data-role="ejmgroupbutton"&gt;
&lt;button&gt;ipad&lt;/button&gt;
&lt;button&gt;ipod&lt;/button&gt;
&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
//Render groupbutton control by default with button behavior in obtrusive way
&lt;div id="grpbtn" &gt;
&lt;button&gt;ipad&lt;/button&gt;
&lt;button&gt;ipod&lt;/button&gt;
&lt;/div&gt;
&lt;script &gt;
$("#grpbtn").ejmGroupButton();
&lt;/script &gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Obtain radiobutton behavior for groupbutton control in unobtrusive way
&lt;div data-role="ejmgroupbutton"&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Render groupbutton control by default with radiobutton behavior in obtrusive way
&lt;div id="grpbtn" &gt;
&lt;label &gt;
&lt;input type="radio" data-role="none" /&gt;
ipad
&lt;/label &gt;
&lt;label &gt;
&lt;input type="radio" data-role="none" /&gt;
ipod
&lt;/label &gt;
&lt;/div &gt;
&lt;script &gt;
$("#grpbtn").ejmGroupButton();
&lt;/script &gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Obtain checkbox behavior for groupbutton control in unobtrusive way
&lt;div data-role="ejmgroupbutton"&gt;
&lt;label&gt;
&lt;input type="checkbox"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="checkbox"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Obtain checkbox behavior for groupbutton control in obtrusive way
&lt;div id="grpbtn" &gt;
&lt;label&gt;
&lt;input type="checkbox" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="checkbox" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script &gt;
$("#grpbtn").ejmGroupButton();
&lt;/script &gt;</code>
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








Sets the root class for GroupButton theme. This cssClass API helps to use custom skinning option for GroupButton control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the cssClass property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-cssclass="customclass" &gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the cssClass property in obtrusive way.
// To set cssClass API value 
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton ({ cssClass: "customclass" });
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the cssClass, after initialization:
// Get the cssClass API value.          
  $("#grpbtn").ejmGroupButton ("option", "cssClass");                   
// Set the cssClass API
  $("#grpbtn").ejmGroupButton ("option", "cssClass", "customclass");</code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Current model value to browser cookies for state maintenance. While refreshing the page, the model value applied from browser cookies retains.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-enablepersistence=true &gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the enablePersistence property in obtrusive way. 
// To set enablePersistence API value 
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton ({ enablePersistence: true });
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         
  $("#grpbtn").ejmGroupButton ("option", "enablePersistence");                  
// Set the enablePersistence API
  $("#grpbtn").ejmGroupButton ("option", "enablePersistence", true);</code>
</pre>






### imageclass<span class="type-signature type string">string</span>








Specifies the groupbutton imageclass.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the imageclass property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton"&gt;
&lt;label data-ej-imageclass="class-ipad"&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label data-ej-imageclass="class-ipod"&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;                </code>
</pre>






### imageurl<span class="type-signature type string">string</span>








Specifies the groupbutton imageurl.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the imageurl property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton"&gt;
&lt;label data-ej-imageurl="ipad.png"&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label data-ej-imageurl="ipod.png"&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>






### items<span class="type-signature type string">string</span>








Specifies the groupbutton items in angular JS.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the items imageurl property in obtrusive way.
&lt;div id="grpbtn"&gt;
&lt;script&gt;
&lt;/div&gt;
$("#group-button").ejmGroupButton({ items: [{ imageUrl: "style" }, { imageUrl: "image" }});
&lt;/script&gt;</code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Changes the rendering mode of the groupbutton. See <a href="global.html#RenderMode">RenderMode</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the renderMode property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-rendermode="auto"&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the renderMode property in obtrusive way. 
// To set renderMode API value 
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$(function(){
$("#grpbtn").ejmGroupButton ({ renderMode: ej.mobile.RenderMode.Auto });        
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the rendermode, after initialization:
// Get the renderMode API value.                
 $("#grpbtn").ejmGroupButton ("option", "renderMode");                  
// Set the renderMode API
$("#grpbtn").ejmGroupButton ("option", "renderMode", ej.mobile.RenderMode.Auto);            </code>
</pre>






### selectedItemIndex<span class="type-signature type number">number</span>








Specifies the item which one is to be selected initially.




Default Value:
{:.param}






* -1








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the selectedItemIndex property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-selecteditemindex=1&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set selectedItemIndex on initialization in obtrusive way
// To set selectedItemIndex API value in obtrusive way
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton ({ selectedItemIndex: 1 });
&lt;/script&gt;
</code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Changes the theme of the groupbutton. See <a href="global.html#Theme">Theme</a>




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-theme="auto"&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Set the theme property in obtrusive way.
// To set theme API value 
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$(function(){
$("#grpbtn").ejmGroupButton ({ theme: ej.mobile.Theme.Auto });
});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the theme, after initialization:
// Get the theme API value.             
  $("#grpbtn").ejmGroupButton ("option", "theme");                      
// Set the theme API
  $("#grpbtn").ejmGroupButton ("option", "theme", ej.mobile.Theme.Auto);</code>
</pre>






### windows








Section for windows rendermode specific functionalities.











### windows.renderDefault<span class="type-signature type boolean">boolean</span>








Specifies whether to render the groupbutton based on the windowsphone's current accent color and device theme.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set the windows mode renderDefault property in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-windows-renderdefault=false&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set the windows mode renderDefault property in obtrusive way.
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton({"windows.renderDefault": false});
&lt;/script&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Get or set the windows mode renderDefault API, after initialization:
// Get the windows mode renderDefault value  
$("#grpbtn").ejmGroupButton("option", "windows.renderDefault");   
// Set the windows mode renderDefault value 
$("#grpbtn").ejmGroupButton("option", "windows.renderDefault", false); </code>
</pre>




## Methods








### destroy<span class="signature">()</span>








destroy the GroupButton widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="grpbtn" &gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt; 
// Get the instance of the group button
var grpObj = $("#grpbtn").data("ejmGroupButton");
grpObj.destroy();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="grpbtn" data-role="ejmgroupbutton"&gt;
&lt;label&gt;
&lt;input type="radio" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
// destroy the GroupButton
$("#grpbtn").ejmGroupButton("destroy"); 
&lt;/script&gt;</code>
</pre>




## Events








### touchEnd








Event triggers when the touchend happens in the groupbutton

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
<td class="description last">Event parameters from groupbutton
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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the groupbutton model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the selected button text</td>
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
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-touchend="touchend"&gt;
&lt;label&gt;
&lt;input type="radio" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
// touchEnd event for groupbutton 
function touchend(args){ //handle the event 
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Define the touchend event in obtrusive way.
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton({
touchEnd: function (args) { //handle the event 
}
});           
&lt;/script&gt;</code>
</pre>






### touchStart








Event triggers when the touchstart happens in the groupbutton

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
<td class="description last">Event parameters from groupbutton
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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the groupbutton model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current button text</td>
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
// Define the touchStart event in unobtrusive way.
&lt;div id="grpbtn" data-role="ejmgroupbutton" data-ej-touchstart="touchstart"&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio"/&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
// touchStart event for groupbutton 
function touchstart(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Define the touchStart event in obtrusive way.
&lt;div id="grpbtn"&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipad
&lt;/label&gt;
&lt;label&gt;
&lt;input type="radio" data-role="none" /&gt;ipod
&lt;/label&gt;
&lt;/div&gt;
&lt;script&gt;
$("#grpbtn").ejmGroupButton({
touchStart: function (args) { //handle the event 
}
});     
&lt;/script&gt;
</code>
</pre>



