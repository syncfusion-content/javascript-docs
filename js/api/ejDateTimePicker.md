---
layout: post
title: ejDateTimePicker
documentation: ug
platform: js
metaname: 
metacontent: 
---

Date and Time selection with the input field.










#### $(element).ejDateTimePicker<span class="signature">(options)</span>







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
<td class="description last">settings for Date Picker.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
// Create DateTimePicker
$("#datetime").ejDateTimePicker();
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.datetimepicker.js


* module:ej.datepicker.js


* module:ej.timepicker.js


* module:ej.scroller.js




### Members








#### buttonText<span class="type-signature type jsonobject">JSONObject</span>








Displays the custom text for the buttons inside the DateTimePicker popup. when the culture value changed, we can change the buttons text based on the culture.




Default Value:






* { today: "Today", now: "Now", done: "Done", timeTitle: "Time" }








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({  buttonText: { done: "&#20570;&#36807;" } });
&lt;/script&gt;</code>
</pre>






#### buttonText.done<span class="type-signature type string">String</span>








Sets the text for the Done button inside the datetime popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { done: "Done" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.now<span class="type-signature type string">String</span>








Sets the text for the Now button inside the datetime popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { now: "Now" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.timeTitle<span class="type-signature type string">String</span>








Sets the header text for the Time dropdown.





##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { timeTitle: "Time" }});
&lt;/script&gt;</code>
</pre>






#### buttonText.today<span class="type-signature type string">String</span>








Sets the text for the Today button inside the datetime popup.





##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { today: "Today" }});
&lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Set the root class for DateTimePicker theme. This cssClass API helps to use custom skinning option for DateTimePicker control.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code>&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;                  
//To set cssClass API during initialization  
        $("#datetime").ejDateTimePicker({  cssClass: "gradient-lime" });
&lt;/script&gt;</code>
</pre>






#### dateTimeFormat<span class="type-signature type string">String</span>








Defines the datetime format displayed in the DateTimePicker. The value should be a combination of date format and time format.




Default Value:






* "M/d/yyyy h:mm tt"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set dateTimeFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dateTimeFormat: "d/M/yyyy tt h:mm" });
&lt;/script&gt; </code>
</pre>






#### dayHeaderFormat<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the header format of the datepicker inside the DateTimePicker popup. See DatePicker.Level




Default Value:






* ej.DatePicker.Header.ShowHeaderMin








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set dayHeaderFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dayHeaderFormat: "showheadershort" });
&lt;/script&gt;</code>
</pre>






#### depthLevel<span class="type-signature type enum">enum</span>








Specifies the drill down level in datepicker inside the DateTimePicker popup. See ej.DatePicker.Level




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set depthLevel API during initialization  
        $("#datetime").ejDateTimePicker({  depthLevel: "decade" });
&lt;/script&gt;</code>
</pre>






#### enableAnimation<span class="type-signature type boolean">Boolean</span>








Enable or disable the animation effect in DateTimePicker.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
// Set the enableAnimation value during initialization.                         
        $("#datetime").ejDateTimePicker({  enableAnimation : false });
&lt;/script&gt; 
</code>
</pre>






#### enabled<span class="type-signature type boolean">Boolean</span>








When this property is set to false, it disables the DateTimePicker control.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set enabled API during initialization  
        $("#datetime").ejDateTimePicker({  enabled: true });
&lt;/script&gt;</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">Boolean</span>








Enables or disables the state maintenance of DateTimePicker.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set enablePersistence API during initialization  
        $("#datetime").ejDateTimePicker({  enablePersistence: true });
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">Boolean</span>








Sets the DateTimePicker direction as right to left alignment.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set enableRTL API during initialization  
        $("#datetime").ejDateTimePicker({  enableRTL: true });
&lt;/script&gt; </code>
</pre>






#### enableStrictMode<span class="type-signature type boolean">Boolean</span>








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set enableStrictMode API during initialization  
        $("#datetime").ejDateTimePicker({  enableStrictMode: true });
&lt;/script&gt; </code>
</pre>






#### headerFormat<span class="type-signature type string">String</span>








Specifies the header format to be displayed in the DatePicker calendar inside the DateTimePicker popup.




Default Value:






* "MMMM yyyy"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set headerFormat API during initialization  
        $("#datetime").ejDateTimePicker({  headerFormat: "MM - yyyy" });
&lt;/script&gt;</code>
</pre>






#### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the height of the DateTimePicker textbox.




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set height API during initialization  
        $("#datetime").ejDateTimePicker({  height: 40 });
&lt;/script&gt; </code>
</pre>






#### htmlAttributes<span class="type-signature type object">object</span>








Specifies the HTML Attributes of the ejDateTimePicker




Default Value:






* {}








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To Set HtmlAttributes API during initialization  
        $("#datetime").ejDateTimePicker({ htmlAttributes : {required:"required"}});
&lt;/script&gt;</code>
</pre>






#### interval<span class="type-signature type number">Number</span>








Sets the time interval between the two adjacent time values in the time popup.




Default Value:






* 30








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set interval API during initialization  
        $("#datetime").ejDateTimePicker({  interval: 60 });
&lt;/script&gt;</code>
</pre>






#### locale<span class="type-signature type string">string</span>








Defines the localization culture for DateTimePicker.




Default Value:






* "en-US"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set locale API during initialization  
        $("#datetime").ejDateTimePicker({  locale: "en-US" });
&lt;/script&gt;</code>
</pre>






#### maxDateTime<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>








Sets the maximum value to the DateTimePicker. Beyond the maximum value an error class is added to the wrapper element.




Default Value:






* new Date("12/31/2099 11:59:59 PM")








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set maxDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  maxDateTime: new Date("12/10/2050 8:00:00 PM") });
&lt;/script&gt;</code>
</pre>






#### minDateTime<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>








Sets the minimum value to the DateTimePicker. Behind the minimum value an error class is added to the wrapper element.




Default Value:






* new Date("1/1/1900 12:00:00 AM")








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set minDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  minDateTime: new Date("5/5/2010 12:00:00 AM") });
&lt;/script&gt;</code>
</pre>






#### readOnly<span class="type-signature type boolean">Boolean</span>








Indicates that the DateTimePicker value can only be read and can&rsquo;t change.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set readOnly API during initialization  
        $("#datetime").ejDateTimePicker({  readOnly: true });
&lt;/script&gt;</code>
</pre>






#### showOtherMonths<span class="type-signature type boolean">Boolean</span>








It allows showing days in other months of DatePicker calendar inside the DateTimePicker popup.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set showOtherMonths API during initialization  
        $("#datetime").ejDateTimePicker({  showOtherMonths: false });
&lt;/script&gt; </code>
</pre>






#### showPopupButton<span class="type-signature type boolean">Boolean</span>








Shows or hides the arrow button from the DateTimePicker textbox. When the button disabled, the DateTimePicker popup opens while focus in the textbox and hides while focusout from the textbox.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set showPopupButton API during initialization  
        $("#datetime").ejDateTimePicker({  showPopupButton: false });
&lt;/script&gt;</code>
</pre>






#### showRoundedCorner<span class="type-signature type boolean">Boolean</span>








Changes the sharped edges into rounded corner for the DateTimePicker textbox and popup.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set showRoundedCorner API during initialization  
        $("#datetime").ejDateTimePicker({  showRoundedCorner: true });
&lt;/script&gt; </code>
</pre>






#### startDay<span class="type-signature type number">Number</span>








Specifies the start day of the week in datepicker inside the DateTimePicker popup.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set startDay API during initialization  
        $("#datetime").ejDateTimePicker({  startDay: 2 });
&lt;/script&gt;</code>
</pre>






#### startLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Specifies the start level view in datepicker inside the DateTimePicker popup. See DatePicker.Level




Default Value:






* ej.DatePicker.Level.Month or "month"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set startLevel API during initialization  
        $("#datetime").ejDateTimePicker({  startLevel:ej.DatePicker.Level.Year });
&lt;/script&gt; </code>
</pre>






#### stepMonths<span class="type-signature type number">Number</span>








Specifies the number of months to navigate at one click of next and previous button in datepicker inside the DateTimePicker popup.




Default Value:






* 1








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set stepMonths API during initialization  
        $("#datetime").ejDateTimePicker({  stepMonths: 2 });
&lt;/script&gt;</code>
</pre>






#### timeDisplayFormat<span class="type-signature type string">String</span>








Defines the time format displayed in the time dropdown inside the DateTimePicker popup.




Default Value:






* "h:mm tt"








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set timeDisplayFormat API during initialization  
        $("#datetime").ejDateTimePicker({  timeDisplayFormat: "HH:mm" });
&lt;/script&gt; </code>
</pre>






#### timePopupWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the width of the time dropdown inside the DateTimePicker popup.




Default Value:






* 100








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set timePopupWidth API during initialization  
        $("#datetime").ejDateTimePicker({  timePopupWidth: 150 });
&lt;/script&gt; </code>
</pre>






#### validationMessage<span class="type-signature type object">object</span>








Set the jquery validation error message in datetimepicker.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" name="datetime" /&gt;
&lt;script&gt;
//To set validationMessage API during initialization  
 $("#datetime").ejDateTimePicker({  
  validationRules:{                     
           required:true
   },
        validationMessage: {
           required: "Required DateTime value"
        }
});
&lt;/script&gt;</code>
</pre>






#### validationRules<span class="type-signature type object">object</span>








Set the jquery validation rules in datetimepicker.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" name="datetime" /&gt;
&lt;script&gt;
//To set validationRules API during initialization  
 $("#datetime").ejDateTimePicker({  
  validationRules:{                     
          required:true
        }
});
&lt;/script&gt;</code>
</pre>






#### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>








Sets the DateTime value to the control.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set value API during initialization  
        $("#datetime").ejDateTimePicker({  value:"6/2/2014 6:00 AM" });
&lt;/script&gt; </code>
</pre>






#### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Defines the width of the DateTimePicker textbox.




Default Value:






* 143








##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//To set width API during initialization  
        $("#datetime").ejDateTimePicker({  width: 210 });
&lt;/script&gt; </code>
</pre>




### Methods








#### disable<span class="signature">()</span>








Disables the DateTimePicker control.





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.disable(); // disables the datetimepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// disables the datetimepicker
$("#datetime").ejDateTimePicker("disable");
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








Enables the DateTimePicker control.





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.enable(); // enables the datetimepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// enables the datetimepicker
$("#datetime").ejDateTimePicker("enable");
&lt;/script&gt;</code>
</pre>






#### getValue<span class="signature">()</span>








Returns the current datetime value in the DateTimePicker.





##### Returns:

value


##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.getValue(); // returns the datetime value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// returns the datetime value
$("#datetime").ejDateTimePicker("getValue");
&lt;/script&gt;</code>
</pre>






#### hide<span class="signature">()</span>








Hides or closes the DateTimePicker popup.





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.hide(); // hides the datetime popup
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// hides the datetime popup
$("#datetime").ejDateTimePicker("hide");
&lt;/script&gt;</code>
</pre>






#### setCurrentDateTime<span class="signature">()</span>








Updates the current system date value and time value to the DateTimePicker.





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.setCurrentDateTime(); // updates the current datetime value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// updates the current datetime value
$("#datetime").ejDateTimePicker("setCurrentDateTime");
&lt;/script&gt;</code>
</pre>






#### show<span class="signature">()</span>








Shows or opens the DateTimePicker popup.





##### Examples

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.show(); // opens the datetime popup
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
$("#datetime").ejDateTimePicker();
// opens the datetime popup
$("#datetime").ejDateTimePicker("show");
&lt;/script&gt;</code>
</pre>




### Events








#### change








Fires when the datetime value changed in the DateTimePicker textbox.

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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.isValidState</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current value is valid or not</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDateTime</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//change event for datetimepicker
$("#datetime").ejDateTimePicker({
   change: function (args) {}
}); 
&lt;/script&gt;                 </code>
</pre>






#### close








Fires when DateTimePicker popup closes.

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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDateTime</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//close event for datetimepicker
$("#datetime").ejDateTimePicker({
   close: function (args) {}
}); 
&lt;/script&gt;                 </code>
</pre>






#### create








Fires after DateTimePicker control is created.

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
<td class="description last">returns the DateTimePicker model</td>
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
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//create event for datetimepicker
$("#datetime").ejDateTimePicker({
   create: function (args) {}
}); 
&lt;/script&gt;                         </code>
</pre>






#### destroy








Fires when the DateTimePicker is destroyed successfully

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
<td class="description last">returns the DateTimePicker model</td>
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
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//destroy event for datetimepicker
$("#datetime").ejDateTimePicker({
   destroy: function (args) {}
}); 
&lt;/script&gt;                         </code>
</pre>






#### focusIn








Fires when the focus-in happens in the DateTimePicker textbox.

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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//focusIn event for datetimepicker
$("#datetime").ejDateTimePicker({
   focusIn: function (args) {}
}); 
&lt;/script&gt;                 </code>
</pre>






#### focusOut








Fires when the focus-out happens in the DateTimePicker textbox.

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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//focusOut event for datetimepicker
$("#datetime").ejDateTimePicker({
   focusOut: function (args) {}
}); 
&lt;/script&gt;                 </code>
</pre>






#### open








Fires when DateTimePicker popup opens.

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
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDateTime</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datetime" /&gt;
&lt;script&gt;
//open event for datetimepicker
$("#datetime").ejDateTimePicker({
   open: function (args) {}
});      
&lt;/script&gt;</code>
</pre>



