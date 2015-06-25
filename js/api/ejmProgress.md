---
layout: post
title: ejmProgress
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Progressbar control.










$(element).ejmProgress<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create progressbar  
$("#progress").ejmProgress(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="progress" data-role="ejmprogress" &gt;&lt;/div&gt;
</code>
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








### enableCustomText<span class="type-signature type bool">bool</span>








Specifies whether to accept custom text or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enableCustomText property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-enablecustomtext=false &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set enable custom text on initialization. 
//To set enable custom text API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create progressbar  
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ enableCustomText: false });                       
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enable custom text, after initialization:
// Get the enable custom text API value.                
 $("#progress").ejmProgress ("option", "enableCustomText");                     
// Set the enable custom text API
$("#progress").ejmProgress ("option", "enableCustomText", false);            </code>
</pre>






### enabled<span class="type-signature type bool">bool</span>








Specifies whether the control is enabled or disabled.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-enabled=true &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set enabled on initialization. 
//To set enabled API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create progressbar  
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ enabled: false});
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enabled, after initialization:
// Get the enabled API value.           
 $("#progress").ejmProgress ("option", "enabled");                      
// Set the enabled API
$("#progress").ejmProgress ("option", "enabled", true);            </code>
</pre>






### enablePersistence<span class="type-signature type bool">bool</span>








Saves current model value to browser cookies for state maintainance. While refreshing the page it retains the model value and applies from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-enablepersistence=false &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set progressbar enablePersistence on initialization. 
//To set enablePersistence API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create progressbar  
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ enablePersistence: false });
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         
 $("#progress").ejmProgress ("option", "enablePersistence");                    
// Set the enablePersistence API
$("#progress").ejmProgress ("option", "enablePersistence", false);            </code>
</pre>






### height<span class="type-signature type int">int</span>








Specifies the Height.




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the height property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-height=10 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set height on initialization. 
//To set height API value
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;   
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ height: 10 });
&lt;/script&gt;         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the height, after initialization:
// Get the height API value.            
 $("#progress").ejmProgress ("option", "height");                       
// Set the height API
$("#progress").ejmProgress ("option", "height", 10);            </code>
</pre>






### incrementStep<span class="type-signature type int">int</span>








Specifies the value to be added in each step of increment.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the incrementStep property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-incrementstep=2 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set incrementStep on initialization. 
//To set incrementStep API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;             
$("#progress").ejmProgress ({ incrementStep: 2 });
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the incrementStep, after initialization:
// Get the incrementStep API value.             
 $("#progress").ejmProgress ("option", "incrementStep");                        
// Set the incrementStep API
$("#progress").ejmProgress ("option", "incrementStep", 2);            </code>
</pre>






### maxValue<span class="type-signature type int">int</span>








Specifies the maximum value.




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the maxValue property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-maxvalue=90 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set maxValue on initialization. 
//To set maximum API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;  
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ maxValue: 90 });
&lt;/script&gt;         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxValue, after initialization:
// Get the maximum API value.           
 $("#progress").ejmProgress ("option", "maxValue");                     
// Set the maxValue API
$("#progress").ejmProgress ("option", "maxValue", 90);            </code>
</pre>






### minValue<span class="type-signature type int">int</span>








specifies the minimum value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the minValue property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-minvalue=10 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set minValue on initialization. 
//To set minimum API value
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;  
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ minValue: 10 });
&lt;/script&gt;                         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minValue, after initialization:
// Get the minimum API value.
 $("#progress").ejmProgress ("option", "minValue");                     
// Set the minValue API
$("#progress").ejmProgress ("option", "minValue", 10);            </code>
</pre>






### orientation<span class="type-signature type enum">enum</span>








Specifies the orientation whether it is horizontal or vertical. See <a href="global.html#Orientation">Orientation</a>




Default Value:
{:.param}






* ej.mobile.Progress.Orientation.Horizontal








Example
{:.example}

<pre class="prettyprint">
<code>//Set the orientation property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-orientation="horizontal" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set orientation on initialization. 
//To set orientation API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
$(function(){
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ orientation: ej.mobile.Progress.Orientation.Horizontal });
});
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the orientation, after initialization:
// Get the orientation API value.               
 $("#progress").ejmProgress ("option", "orientation");                  
// Set the orientation API
$("#progress").ejmProgress ("option", "orientation", ej.mobile.Progress.Orientation.Horizontal);            </code>
</pre>






### percentage<span class="type-signature type int">int</span>








Specifies the initial value in percentage.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the percentage property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-percentage=35 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set percentage on initialization. 
//To set percentage API value
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;   
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ percentage: 35 });
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the percentage, after initialization:
// Get the percentage API value.                
 $("#progress").ejmProgress ("option", "percentage");                   
// Set the percentage API
$("#progress").ejmProgress ("option", "percentage", 35);            </code>
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
//Set the renderMode property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-rendermode="auto" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set renderMode on initialization. 
//To set renderMode API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
$(function(){
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ renderMode: ej.mobile.RenderMode.Auto });
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the renderMode, after initialization:
// Get the renderMode API value.        
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
 $("#progress").ejmProgress ("option", "renderMode");                   
// Set the renderMode API
$("#progress").ejmProgress ("option", "renderMode", ej.mobile.RenderMode.Auto);            </code>
</pre>






### text<span class="type-signature type string">string</span>








Applies custom text to notify it's current actions.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the text property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-enablecustomtext=true data-ej-text="in-progress" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set text on initialization. 
//To set text API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ enableCustomText: true });
$("#progress").ejmProgress ({ text: "in-progress" });                   
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the text, after initialization:
// Get the text API value.              
 $("#progress").ejmProgress ("option", "text");                 
// Set the text API
$("#progress").ejmProgress ("option", "text", "in-progress");            </code>
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
&lt;div id="progress" data-role="ejmprogress" data-ej-theme="auto" &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set progressbar theme on initialization. 
//To set theme API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create progressbar 
$(function(){
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ theme: ej.mobile.Theme.Auto });
});
&lt;/script&gt;                 </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the theme, after initialization:
// Get the theme API value.             
 $("#progress").ejmProgress ("option", "theme");                        
// Set the theme API
$("#progress").ejmProgress ("option", "theme", ej.mobile.Theme.Auto);            </code>
</pre>






### value<span class="type-signature type int">int</span>








Specifies the initial value.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-value=35 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set value on initialization. 
//To set value API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt;   
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ value: 35 });
&lt;/script&gt;         </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the value, after initialization:
// Get the value API value.                                                
$("#progress").ejmProgress ("option", "value");           
// Set the value API
$("#progress").ejmProgress ("option", "value", 35);            </code>
</pre>






### width<span class="type-signature type int">int</span>








Specifies the width.




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the width property in unobtrusive way.
&lt;div id="progress" data-role="ejmprogress" data-ej-width=350 &gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
// Set width on initialization. 
//To set width API value 
&lt;div id="progress" &gt;&lt;/div&gt;
&lt;script&gt; 
$("#progress").ejmProgress(); 
$("#progress").ejmProgress ({ width: 350 });    
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the width, after initialization:
// Get the width API value.             
 $("#progress").ejmProgress ("option", "width");                        
// Set the width API
$("#progress").ejmProgress ("option", "width", 350);            </code>
</pre>




## Methods








### getPercentage<span class="signature">()</span>








Get current value in percentage





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Create progressbar
var progress = $("#progress").data("ejmProgress");
progress.getPercentage(); // returns the progressbar current percent value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Get the current percent value
$("#progress").ejmProgress("getPercentage");    
&lt;/script&gt;</code>
</pre>






### getValue<span class="signature">()</span>








Gets the currentvalue.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Create progressbar
var progress = $("#progress").data("ejmProgress");
progress.getValue(); // returns the progressbar current value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Get the current value
$("#progress").ejmProgress("getValue"); 
&lt;/script&gt;</code>
</pre>






### setCustomText<span class="signature">()</span>








Set the custom text on each action conplete.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Create progressbar
var progress = $("#progress").data("ejmProgress");
progress.setCustomText("Downloading.."); // Set the progressbar custom text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt;
// Set the custom text
$("#progress").ejmProgress("setCustomText", "Downloading..");   
&lt;/script&gt;</code>
</pre>




## Events








### change








Event triggers when the value change happens.

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
<td class="description last">event parameters from progressbar
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
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current element associated value</td>
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
&lt;div id="progress" data-role="ejmprogress" data-ej-change="onChange"&gt;&lt;/div&gt;
&lt;script&gt; 
// change event   
function onChange(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//change event 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#progress").ejmProgress({
  change: function (args) { //handle the event 
}
});  
&lt;/script&gt;</code>
</pre>






### complete








Event triggers when the complete happens.

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
<td class="description last">event parameters from progressbar
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
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current element associated value</td>
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
&lt;div id="progress" data-role="ejmprogress" data-ej-complete="onComplete"&gt;&lt;/div&gt;
&lt;script&gt; 
// complete event 
function onComplete(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt; 
//complete event 
$("#progress").ejmProgress({
  complete: function (args) { //handle the event
}
}); 
&lt;/script&gt;</code>
</pre>






### create








Event triggers when the create happens.

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
<td class="description last">event parameters from progressbar
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
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current element associated value</td>
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
&lt;div id="progress" data-role="ejmprogress" data-ej-create="onCreate"&gt;&lt;/div&gt;
&lt;script&gt; 
// Create event   
function onCreate(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//create event 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#progress").ejmProgress({
  create: function (args) { //handle the event 
}
}); 
&lt;/script&gt;</code>
</pre>






### start








Event triggers when the start happens.

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
<td class="description last">event parameters from progressbar
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
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the progressbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">int</span></td>
<td class="description last">returns the current element associated value</td>
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
&lt;div id="progress" data-role="ejmprogress" data-ej-start="onStart"&gt;&lt;/div&gt;
&lt;script&gt; 
// start event 
function onStart(args){ //handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//start event 
&lt;div id="progress"&gt;&lt;/div&gt;
&lt;script&gt; 
$("#progress").ejmProgress({
  start: function (args) { //handle the event 
}
});  
&lt;/script&gt;</code>
</pre>



