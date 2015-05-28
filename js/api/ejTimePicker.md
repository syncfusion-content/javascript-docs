---
layout: post
title: ejTimePicker
documentation: ug
platform: js
metaname: 
metacontent: 
---

Time selection with the input field.










#### $(element).ejTimePicker<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Create TimePicker
$("#timepicker").ejTimePicker();
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.timepicker.js


* module:ej.scroller.js




### Members








#### cssClass<span class="type-signature type string">String</span>








Specify the CSS class to timepicker to achieve custom theme.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the CSS class during initialization.                     
        $("#timepicker").ejTimePicker({  cssClass : "gradient-lime" });
&lt;/script&gt; 
</code>
</pre>






#### enableAnimation<span class="type-signature type boolean">Boolean</span>








Specifies the animation behaviour in timepicker.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the enableAnimation value during initialization.                         
        $("#timepicker").ejTimePicker({  enableAnimation : false });
&lt;/script&gt; 
</code>
</pre>






#### enabled<span class="type-signature type boolean">Boolean</span>








When this property is set to false, it disables the timepicker control.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the enabled value during initialization.                         
        $("#timepicker").ejTimePicker({  enabled : false });
&lt;/script&gt; 
</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">Boolean</span>








Enables or disables the state maintenance of TimePicker.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the enablePersistence value during initialization.                       
        $("#timepicker").ejTimePicker({  enablePersistence : true });
&lt;/script&gt; 
</code>
</pre>






#### enableRTL<span class="type-signature type boolean">Boolean</span>








Sets the TimePicker direction as right to left alignment.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the enableRTL value during initialization.                       
        $("#timepicker").ejTimePicker({  enableRTL : true });
&lt;/script&gt; 
</code>
</pre>






#### enableStrictMode<span class="type-signature type boolean">Boolean</span>








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//To set enableStrictMode API during initialization  
        $("#timepicker").ejTimePicker({  enableStrictMode: true });
&lt;/script&gt; </code>
</pre>






#### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the height of the TimePicker textbox.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the height value during initialization.                  
        $("#timepicker").ejTimePicker({  height : "35" });
&lt;/script&gt; 
</code>
</pre>






#### hourInterval<span class="type-signature type number">Number</span>








Sets the step value for increment an hour value through arrow keys or mouse scroll.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the hourInterval value during initialization.                    
        $("#timepicker").ejTimePicker({  hourInterval : 2 });
&lt;/script&gt; 
</code>
</pre>






#### htmlAttributes<span class="type-signature type object">object</span>








Specifies the HTML Attributes of the ejTimePicker




Default Value:






* {}








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// To Set HtmlAttributes value during initialization.                   
        $("#timepicker").ejTimePicker({htmlAttributes : {required:"required"});
&lt;/script&gt; 
</code>
</pre>






#### interval<span class="type-signature type number">Number</span>








Sets the time interval between the two adjacent time values in the popup.




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the interval value during initialization.                        
        $("#timepicker").ejTimePicker({  interval : 60 });
&lt;/script&gt; 
</code>
</pre>






#### locale<span class="type-signature type string">String</span>








Defines the localization locale for TimePicker.




Default Value:






* "en-US"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the locale value during initialization.                  
        $("#timepicker").ejTimePicker({  locale : "en-US" });
&lt;/script&gt; 
</code>
</pre>






#### maxTime<span class="type-signature type string">String</span>








Sets the maximum time value to the TimePicker.




Default Value:






* "11:59:59 PM"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the maxTime value during initialization.                         
        $("#timepicker").ejTimePicker({  maxTime : "5:00 PM" });
&lt;/script&gt; 
</code>
</pre>






#### minTime<span class="type-signature type string">String</span>








Sets the minimum time value to the TimePicker.




Default Value:






* "12:00:00 AM"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the minTime value during initialization.                         
        $("#timepicker").ejTimePicker({  minTime : "8:00 AM" });
&lt;/script&gt; 
</code>
</pre>






#### minutesInterval<span class="type-signature type number">Number</span>








Sets the step value for increment the minute value through arrow keys or mouse scroll.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the minute interval value during initialization.                         
        $("#timepicker").ejTimePicker({  minutesInterval : 5 });
&lt;/script&gt; 
</code>
</pre>






#### popupHeight<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the height of the TimePicker popup.




Default Value:






* "191px"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the popupHeight value during initialization.                     
        $("#timepicker").ejTimePicker({  popupHeight : "250px" });
&lt;/script&gt; 
</code>
</pre>






#### popupWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the width of the TimePicker popup.




Default Value:






* "auto"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the popupWidth value during initialization.                      
        $("#timepicker").ejTimePicker({  popupWidth : "150px" });
&lt;/script&gt; 
</code>
</pre>






#### readOnly<span class="type-signature type boolean">Boolean</span>








Indicates that the timepicker value can only be read.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the readOnly value during initialization.                        
        $("#timepicker").ejTimePicker({  readOnly : false });
&lt;/script&gt; 
</code>
</pre>






#### secondsInterval<span class="type-signature type number">Number</span>








Sets the step value for increment the seconds value through arrow keys or mouse scroll.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the seconds interval value during initialization.                        
        $("#timepicker").ejTimePicker({ timeFormat : "h:mm:ss tt",secondsInterval : 5 });
&lt;/script&gt; 
</code>
</pre>






#### showPopupButton<span class="type-signature type boolean">Boolean</span>








Shows or hides the arrow button from the TimePicker textbox.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the showPopupButton property during initialization.                      
        $("#timepicker").ejTimePicker({  showPopupButton : false });
&lt;/script&gt; 
</code>
</pre>






#### showRoundedCorner<span class="type-signature type boolean">Boolean</span>








Changes the sharped edges into rounded corner for the TimePicker textbox and popup.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the showRoundedCorner value during initialization.                       
        $("#timepicker").ejTimePicker({  showRoundedCorner : true });
&lt;/script&gt; 
</code>
</pre>






#### timeFormat<span class="type-signature type string">String</span>








Defines the time format displayed in the TimePicker.




Default Value:






* "h:mm tt"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the timeFormat during initialization.                    
        $("#timepicker").ejTimePicker({  timeFormat : "h:mm:ss tt" });
&lt;/script&gt; 
</code>
</pre>






#### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>








Sets a specified time value on the TimePicker.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the time value during initialization.                    
        $("#timepicker").ejTimePicker({  value : "5:10 PM" });
&lt;/script&gt; 
</code>
</pre>






#### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the width of the TimePicker textbox.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
// Set the width value during initialization.                   
        $("#timepicker").ejTimePicker({  width : "120" });
&lt;/script&gt; 
</code>
</pre>




### Methods








#### disable<span class="signature">()</span>








To disable the timepicker





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.disable(); // disable the timepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// disable the timepicker
$("#timepicker").ejTimePicker("disable");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








To enable the timepicker





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.enable(); // enables the timepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// enables the timepicker
$("#timepicker").ejTimePicker("enable");
&lt;/script&gt;</code>
</pre>






#### getValue<span class="signature">()</span>








returns the current time value





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.getValue(); // returns the timepicker value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// to get the time value
$("#timepicker").ejTimePicker("getValue");
&lt;/script&gt;</code>
</pre>






#### setCurrentTime<span class="signature">()</span>








updates the current system time to timepicker





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.setCurrentTime(); // updates the current system
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
$("#timepicker").ejTimePicker();
// updates the current system
$("#timepicker").ejTimePicker("setCurrentTime");
&lt;/script&gt;</code>
</pre>




### Events








#### beforeChange








Fires when the time value changed in the TimePicker.

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
<td class="description last">Event parameters from timepicker
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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified time value</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//change event for timepicker
$("#timepicker").ejTimePicker({
   beforeChange: function (args) {}
});  
&lt;/script&gt; 
                    </code>
</pre>






#### beforeOpen








Fires when the TimePicker popup before opened .

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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//beforeOpen event for timepicker
$("#timepicker").ejTimePicker({
   beforeOpen: function (args) {}
});   
&lt;/script&gt; 
                                    </code>
</pre>






#### change








Fires when the time value changed in the TimePicker.

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
<td class="description last">Event parameters from timepicker
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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified time value</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//change event for timepicker
$("#timepicker").ejTimePicker({
   change: function (args) {}
});  
&lt;/script&gt; 
                    </code>
</pre>






#### close








Fires when the TimePicker popup closed.

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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//close event for timepicker
$("#timepicker").ejTimePicker({
   close: function (args) {}
});   
&lt;/script&gt; 
                                    </code>
</pre>






#### create








Fires when create TimePicker successfully.

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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//create event for timepicker
$("#timepicker").ejTimePicker({
   create: function (args) {}
});   
&lt;/script&gt; 
                                    </code>
</pre>






#### destroy








Fires when the TimePicker is destroyed successfully.

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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//destroy event for timepicker
$("#timepicker").ejTimePicker({
   destroy: function (args) {}
});   
&lt;/script&gt; 
                                    </code>
</pre>






#### focusIn








Fires when the timepicker control gets focus.

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
<td class="description last">Event parameters from timepicker
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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current time value</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//focusIn event for timepicker
$("#timepicker").ejTimePicker({
   focusIn: function (args) {}
});      
&lt;/script&gt; 
</code>
</pre>






#### focusOut








Fires when the timepicker control get lost focus.

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
<td class="description last">Event parameters from timepicker
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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current time value</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//focusOut event for timepicker
$("#timepicker").ejTimePicker({
   focusOut: function (args) {}
}); 
&lt;/script&gt; 
                     </code>
</pre>






#### open








Fires when the TimePicker popup opened.

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
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//open event for timepicker
$("#timepicker").ejTimePicker({
   open: function (args) {}
});   
&lt;/script&gt; 
                                    </code>
</pre>






#### select








Fires when the value is selected from the timepicker dropdownlist.

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
<td class="description last">Event parameters from timepicker
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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected time value</td>
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
&lt;input type="text" id="timepicker" /&gt;
&lt;script&gt;
//select event for timepicker
$("#timepicker").ejTimePicker({
   select: function (args) {}
});   
&lt;/script&gt; 
                    </code>
</pre>



