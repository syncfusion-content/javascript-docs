---
layout: post
title: ejDatePicker
documentation: API
platform: js
metaname: 
metacontent: 
---

Date selection with the input field.










$(element).ejDatePicker<span class="signature">(options)</span>







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




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
// Create DatePicker
$("#datepicker").ejDatePicker();
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.datepicker.js




## Members








### buttonText<span class="type-signature type string">String</span>
{:#members-buttontext}








Set the text name for the today button in the datepicker popup.




Default Value:
{:.param}






* "Today"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set buttonText API during initialization  
        $("#datepicker").ejDatePicker({  buttonText : "Now" });
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">String</span>
{:#members-cssclass}








Set the root class for DatePicker theme. This cssClass API helps to use custom skinning option for DatePicker control.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set cssClass API during initialization  
        $("#datepicker").ejDatePicker({  cssClass: "gradient-lime" });
&lt;/script&gt;</code>
</pre>






### dateFormat<span class="type-signature type string">String</span>
{:#members-dateformat}








Specifies the date format to be displayed in the input textbox of Datepicker. The selected Datepicker value will be displayed in specified date format.




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set dateFormat API during initialization  
        $("#datepicker").ejDatePicker({  dateFormat: "dd/MM/yyyy" });
&lt;/script&gt;</code>
</pre>






### dayHeaderFormat<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members-dayheaderformat}








Specifies the header format of days in short, longer or min types. See <a href="global.html#Header">Header</a>




Default Value:
{:.param}






* ej.DatePicker.Header.ShowHeaderMin








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set dayHeaderFormat API value during initialization  
        $("#datepicker").ejDatePicker({  dayHeaderFormat: ej.DatePicker.Header.ShowHeaderShort });
&lt;/script&gt;</code>
</pre>






### depthLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members-depthlevel}








Specifies the start level view in DatePicker calendar. See <a href="global.html#Level">Level</a>




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set depthLevel API during initialization  
        $("#datepicker").ejDatePicker({  depthLevel: ej.DatePicker.Level.Year });
&lt;/script&gt;</code>
</pre>






### displayDefaultDate<span class="type-signature type boolean">Boolean</span>
{:#members-displaydefaultdate}








Allow to display default date value in input textbox.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set displayDefaultDate API during initialization  
        $("#datepicker").ejDatePicker({  displayDefaultDate: true });
&lt;/script&gt;</code>
</pre>






### displayInline<span class="type-signature type boolean">Boolean</span>
{:#members-displayinline}








Allows to embed the DatePicker in the page. Also associate DatePicker with div element instead of input.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set displayInline API during initialization  
        $("#datepicker").ejDatePicker({  displayInline: true });
&lt;/script&gt;</code>
</pre>






### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members-enableanimation}








Enable or disable the animation effect in datepicker.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
// Set the enableAnimation value during initialization.                         
        $("#datepicker").ejDatePicker({  enableAnimation : false });
&lt;/script&gt; 
</code>
</pre>






### enabled<span class="type-signature type boolean">Boolean</span>
{:#members-enabled}








Enables or disables the datepicker control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set enabled API during initialization  
        $("#datepicker").ejDatePicker({  enabled: false });
&lt;/script&gt;</code>
</pre>






### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members-enablepersistence}








Enables or disables the state maintenance of DatePicker.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set enablePersistence API during initialization  
        $("#datepicker").ejDatePicker({  enablePersistence: true });
&lt;/script&gt; </code>
</pre>






### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members-enablertl}








Display Right to Left direction of DatePicker calendar and input box.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set enableRTL API during initialization  
        $("#datepicker").ejDatePicker({  enableRTL : true });
&lt;/script&gt;</code>
</pre>






### enableStrictMode<span class="type-signature type boolean">Boolean</span>
{:#members-enablestrictmode}








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set enableStrictMode API during initialization  
        $("#datepicker").ejDatePicker({  enableStrictMode: true });
&lt;/script&gt; </code>
</pre>






### fields<span class="type-signature type object">object</span>
{:#members-fields}








Specify the fields mapping in datepicker




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set fields API value during initialization         
// declaration
$("#datepicker").ejDatePicker({ 
specialDates: window.spldays, fields: {date:"date",tooltip:"tooltip",icon:"icon"}});
&lt;/script&gt;</code>
</pre>






### fields.date<span class="type-signature type string">String</span>
{:#members-fields-date}








Specifies the date to datepicker.











### fields.icon<span class="type-signature type string">String</span>
{:#members-fields-icon}








Specifies the icon to date.











### fields.tooltip<span class="type-signature type string">String</span>
{:#members-fields-tooltip}








Specifies the tooltip to date.











### headerFormat<span class="type-signature type string">String</span>
{:#members-headerformat}








Specifies the header format to be displayed in the pop up of Datepicker.




Default Value:
{:.param}






* "MMMM yyyy"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set headerFormat API during initialization  
        $("#datepicker").ejDatePicker({  headerFormat : "MMMM yy" });
&lt;/script&gt; </code>
</pre>






### height<span class="type-signature type string">String</span>
{:#members-height}








Specifies the height of the datepicker input text.




Default Value:
{:.param}






* "28px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set height API during initialization  
        $("#datepicker").ejDatePicker({  height: 35 });
&lt;/script&gt; </code>
</pre>






### highlightSection<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members-highlightsection}








HighlightSection used to highlight current month, week, workdays. See <a href="global.html#HighlightSection">HighlightSection</a>




Default Value:
{:.param}






* "none"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set highlightSection API during initialization  
        $("#datepicker").ejDatePicker({  highlightSection: "week" });
&lt;/script&gt;</code>
</pre>






### highlightWeekend<span class="type-signature type boolean">Boolean</span>
{:#members-highlightweekend}








Week end will be displayed in bold, when this property is set to true.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set highlightWeekend API during initialization  
        $("#datepicker").ejDatePicker({  highlightWeekend : true });
&lt;/script&gt;</code>
</pre>






### htmlAttributes<span class="type-signature type object">object</span>
{:#members-htmlattributes}








Specifies the HTML Attributes of the DatePicker.




Default Value:
{:.param}






* {}








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//Set HtmlAttributes API during initialization  
        $("#datepicker").ejDatePicker({  htmlAttributes : {required:"required"}});
&lt;/script&gt;</code>
</pre>






### locale<span class="type-signature type string">String</span>
{:#members-locale}








Culture the language of DatePicker calendar.




Default Value:
{:.param}






* "en-US"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set locale API during initialization  
        $("#datepicker").ejDatePicker({  locale: "en-US" });
&lt;/script&gt;</code>
</pre>






### maxDate<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members-maxdate}








Specifies the maximum date range to be displayed in DatePicker calendar.




Default Value:
{:.param}






* new Date(2099, 11, 31)








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set maxDate value during initialization  
        $("#datepicker").ejDatePicker({  maxDate : new Date("5/30/2015") });
&lt;/script&gt;</code>
</pre>






### minDate<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members-mindate}








Specifies the minimum date range to be displayed in DatePicker calendar.




Default Value:
{:.param}






* new Date(1900, 00, 01)








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set minDate value during initialization  
        $("#datepicker").ejDatePicker({  minDate: new Date("5/1/2013") });
&lt;/script&gt;</code>
</pre>






### readOnly<span class="type-signature type boolean">Boolean</span>
{:#members-readonly}








Indicates that the datepicker value can only be read.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set readOnly API during initialization  
        $("#datepicker").ejDatePicker({  readOnly : true });
&lt;/script&gt; </code>
</pre>






### showFooter<span class="type-signature type boolean">Boolean</span>
{:#members-showfooter}








It allows to show footer in DatePicker calendar to select today date.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set showFooter API during initialization  
        $("#datepicker").ejDatePicker({  showFooter: false });
&lt;/script&gt;</code>
</pre>






### showOtherMonths<span class="type-signature type boolean">Boolean</span>
{:#members-showothermonths}








It allows to show days in other months of DatePicker calendar.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set showOtherMonths API during initialization  
        $("#datepicker").ejDatePicker({  showOtherMonths: false });
&lt;/script&gt; </code>
</pre>






### showPopupButton<span class="type-signature type boolean">Boolean</span>
{:#members-showpopupbutton}








Shows the date icon button at right side of textbox and shows DatePicker popup on clicking it.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set showPopupButton API during initialization  
        $("#datepicker").ejDatePicker({  showPopupButton: false });
&lt;/script&gt;</code>
</pre>






### showRoundedCorner<span class="type-signature type boolean">Boolean</span>
{:#members-showroundedcorner}








DatePicker input will be displayed in rounded corner style, when this property is set to true.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set showRoundedCorner API during initialization  
        $("#datepicker").ejDatePicker({  showRoundedCorner : true });
&lt;/script&gt;</code>
</pre>






### showTooltip<span class="type-signature type boolean">Boolean</span>
{:#members-showtooltip}








DatePicker Tooltip will be displayed, when this property is set to true.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set tooltip API during initialization  
        $("#datepicker").ejDatePicker({  showTooltip : false });
&lt;/script&gt;</code>
</pre>






### specialDates<span class="type-signature type object">object</span>
{:#members-specialdates}








Specify the special dates in datepicker




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set specialDates API value during initialization             
// declaration
$("#datepicker").ejDatePicker({specialDates:window.spldays});
&lt;/script&gt;</code>
</pre>






### startDay<span class="type-signature type number">Number</span>
{:#members-startday}








Specifies the start day of the week in DatePicker calendar.




Default Value:
{:.param}






* 0








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set startDay API during initialization  
        $("#datepicker").ejDatePicker({  startDay: 2 });
&lt;/script&gt;</code>
</pre>






### startLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members-startlevel}








Specifies the start level view in DatePicker calendar. See <a href="global.html#Level">Level</a>




Default Value:
{:.param}






* ej.DatePicker.Level.Month








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set startLevel API during initialization  
        $("#datepicker").ejDatePicker({  startLevel: ej.DatePicker.Level.Year });
&lt;/script&gt;</code>
</pre>






### stepMonths<span class="type-signature type number">Number</span>
{:#members-stepmonths}








Specifies the number of months to navigate at one click in next and previous button.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set stepMonths API during initialization  
        $("#datepicker").ejDatePicker({  stepMonths: 2 });
&lt;/script&gt;</code>
</pre>






### validationMessage<span class="type-signature type object">object</span>
{:#members-validationmessage}








Set the jquery validation error message in datepicker.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" name="datepick" /&gt;
&lt;script&gt;
//To set validationMessage API during initialization  
        $("#datepicker").ejDatePicker({
  validationRules:{                     
            required:true
        }                       
  validationMessage:{                   
                required: "Required Date value"
        }
});
&lt;/script&gt;</code>
</pre>






### validationRules<span class="type-signature type object">object</span>
{:#members-validationrules}








Set the jquery validation rule in datepicker.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" name="datepick" /&gt;
&lt;script&gt;
//To set validationRules API during initialization  
        $("#datepicker").ejDatePicker({  
  validationRules:{                     
          required:true
        }
});
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members-value}








Specifies the selected date value.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set the datepicker value during initialization  
        $("#datepicker").ejDatePicker({  value: new Date("5/5/2014") });
&lt;/script&gt;</code>
</pre>






### watermarkText<span class="type-signature type string">String</span>
{:#members-watermarktext}








Specifies the water mark text to be display in input text.




Default Value:
{:.param}






* "Select date"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set watermarkText during initialization  
        $("#datepicker").ejDatePicker({  watermarkText: "Enter date" });
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type string">String</span>
{:#members-width}








Specifies the width of the datepicker input text.




Default Value:
{:.param}






* "160px"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//To set width API during initialization  
        $("#datepicker").ejDatePicker({  width: 200 });
&lt;/script&gt; </code>
</pre>




## Methods








### disable<span class="signature">()</span>
{:#methods-disable}








Disables the datepicker control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.disable(); // disables the datepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// disables the datepicker
$("#datepicker").ejDatePicker("disable");
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>
{:#methods-enable}








Enables the datepicker control





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.enable(); // enables the datepicker
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// enables the datepicker
$("#datepicker").ejDatePicker("enable");
&lt;/script&gt;</code>
</pre>






### getValue<span class="signature">()</span>
{:#methods-getvalue}








Returns the current date value in the datepicker control





#### Returns:
{:#methods-returns:}

value


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.getValue(); // returns the date value
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
// returns the date value
$("#datepicker").ejDatePicker();
$("#datepicker").ejDatePicker("getValue");
&lt;/script&gt;</code>
</pre>






### hide<span class="signature">()</span>
{:#methods-hide}








Hides the datepicker popup, if in opended state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.hide(); // hides the datepicker popup
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// hides the datepicker popup
$("#datepicker").ejDatePicker("hide");
&lt;/script&gt;</code>
</pre>






### show<span class="signature">()</span>
{:#methods-show}








Opens the datepicker popup





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.show(); // shows the datepicker popup
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
$("#datepicker").ejDatePicker();
// shows the datepicker popup
$("#datepicker").ejDatePicker("show");
&lt;/script&gt;</code>
</pre>




## Events








### beforeDateCreate
{:#events-beforedatecreate}








Fires when each date is created in the DatePicker popup.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.date</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current created date object</td>
</tr>
<tr>
<td class="name"><code>argument.element</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current DOM object of the date from the Calendar</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//beforeDateCreate event for datepicker
$("#datepicker").ejDatePicker({
   beforeDateCreate: function (args) {}
});  
&lt;/script&gt;                         </code>
</pre>






### change
{:#events-change}








Fires when the datepicker input value is changed.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datepicker input value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//change event for datepicker
$("#datepicker").ejDatePicker({
   change: function (args) {}
});  
&lt;/script&gt;                         </code>
</pre>






### close
{:#events-close}








Fires when DatePicker popup closed.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//close event for datepicker
$("#datepicker").ejDatePicker({
   close: function (args) {}
});   
&lt;/script&gt;                         </code>
</pre>






### create
{:#events-create}








Fires when create DatePicker successfully.

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
<td class="description last">returns the DatePicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//create event for datepicker
$("#datepicker").ejDatePicker({
   create: function (args) {}
});
&lt;/script&gt;                         </code>
</pre>






### destroy
{:#events-destroy}








Fires when the DatePicker is destroyed successfully.

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
<td class="description last">returns the DatePicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//destroy event for datepicker
$("#datepicker").ejDatePicker({
   destroy: function (args) {}
}); 
&lt;/script&gt;                 </code>
</pre>






### focusIn
{:#events-focusin}








Fires when datePicker input gets focus.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//focusIn event for datepicker
$("#datepicker").ejDatePicker({
   focusIn: function (args) {}
}); 
&lt;/script&gt;                         </code>
</pre>






### focusOut
{:#events-focusout}








Fires when datePicker input losses the focus.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//focusOut event for datepicker
$("#datepicker").ejDatePicker({
   focusOut: function (args) {}
});
&lt;/script&gt;                         </code>
</pre>






### open
{:#events-open}








Fires when DatePicker popup opened.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the eventclose"</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//open event for datepicker
$("#datepicker").ejDatePicker({
   open: function (args) {}
});  
&lt;/script&gt;                         </code>
</pre>






### select
{:#events-select}








Fires when a date is selected from the datepicker popup.

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
<td class="description last">returns the datepicker model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value</td>
</tr>
<tr>
<td class="name"><code>argument.prevDate</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="datepicker" /&gt;
&lt;script&gt;
//select event for datepicker
$("#datepicker").ejDatePicker({
   select: function (args) {}
}); 
&lt;/script&gt;                         </code>
</pre>



