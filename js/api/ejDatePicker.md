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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for Date Picker.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
// Create DatePicker
$("#datepicker").ejDatePicker();
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.datepicker.js




## Members






### allowEdit<span class="type-signature type boolean">Boolean</span>
{:#members:allowedit}








When allowEdit is set to false, you cannot able to type in datePicker textbox and you can only pick the date from datpicker popup. When this API is set to true, you can edit the values and also pick the date from datpicker popup.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set allowEdit API during initialization  
        $("#datepicker").ejDatePicker({   allowEdit : true });
</script>{% endhighlight %}






### allowDrilDown<span class="type-signature type boolean">Boolean</span>
{:#members:allowdrildown}








Determines whether you can change the popup view to month/year/decade while clicking on the popup title.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set allowDrilDown API during initialization  
        $("#datepicker").ejDatePicker({   allowDrilDown : true });
</script>{% endhighlight %}










### buttonText<span class="type-signature type string">String</span>
{:#members:buttontext}








Sets the text name for the today button in the datepicker calendar.




Default Value:
{:.param}






* "Today"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set buttonText API during initialization  
        $("#datepicker").ejDatePicker({  buttonText : "Now" });
</script>{% endhighlight %}






### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Sets the root class for DatePicker theme. This cssClass API allows to use custom skinning option for DatePicker control.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set cssClass API during initialization  
        $("#datepicker").ejDatePicker({  cssClass: "gradient-lime" });
</script>{% endhighlight %}







### dateFormat<span class="type-signature type string">String</span>
{:#members:dateformat}








Specifies the format that is used to format the value of the DatePicker displayed in the input. The format is also used to parse the input. The default value of dateFormat is based on the culture.




Default Value:
{:.param}






* "MM/dd/yyyy"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set dateFormat API during initialization  
        $("#datepicker").ejDatePicker({  dateFormat: "dd/MM/yyyy" });
</script>{% endhighlight %}







### dayHeaderFormat<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:dayheaderformat}








Specifies the header format of datepicker calendar in short, longer or min types. See <a href="global.html#Header">Header</a>




Default Value:
{:.param}






* ej.DatePicker.Header.Min








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set dayHeaderFormat API value during initialization  
        $("#datepicker").ejDatePicker({  dayHeaderFormat: ej.DatePicker.Header.Short });
</script>{% endhighlight %}







### depthLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:depthlevel}








Specifies the navigation depth in DatePicker calendar. This option is not applied when start option is lower than depth. Always set both and start and depth options. See <a href="global.html#Level">Level</a>




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set depthLevel API during initialization  
        $("#datepicker").ejDatePicker({  depthLevel: ej.DatePicker.Level.Year });
</script>{% endhighlight %}







### displayDefaultDate<span class="type-signature type boolean">Boolean</span>
{:#members:displaydefaultdate}








Allows to display the default date value in input textbox.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set displayDefaultDate API during initialization  
        $("#datepicker").ejDatePicker({  displayDefaultDate: true });
</script>{% endhighlight %}







### displayInline<span class="type-signature type boolean">Boolean</span>
{:#members:displayinline}








Allows to embed the DatePicker in the page. Also associates DatePicker with div element instead of input.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set displayInline API during initialization  
        $("#datepicker").ejDatePicker({  displayInline: true });
</script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members:enableanimation}








Enables or disables the animation effect when opening the datepicker calendar in datepicker. Setting the enableAnimation option to false, disables the opening and closing animations. As a result, the calendar popup opens and closes instantly.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#datepicker").ejDatePicker({  enableAnimation : false });
</script> 
{% endhighlight %}







### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}








Enables or disables the datepicker control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enabled API during initialization  
        $("#datepicker").ejDatePicker({  enabled: false });
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}








Specifies the enablePersistence to editor to DatePicker current model value to browser cookies for state maintains.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enablePersistence API during initialization  
        $("#datepicker").ejDatePicker({  enablePersistence: true });
</script> {% endhighlight %}







### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}








Displays Right to Left direction of DatePicker calendar and input box.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enableRTL API during initialization  
        $("#datepicker").ejDatePicker({  enableRTL : true });
</script>{% endhighlight %}







### enableStrictMode<span class="type-signature type boolean">Boolean</span>
{:#members:enablestrictmode}








When enableStrictMode is true, it allows the value outside the range also, otherwise it internally changes to the correct value.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enableStrictMode API during initialization  
        $("#datepicker").ejDatePicker({  enableStrictMode: true });
</script> {% endhighlight %}







### fields<span class="type-signature type object">object</span>
{:#members:fields}








Specifies the fields mapping for special Dates in datepicker.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set fields API value during initialization         
// declaration
$("#datepicker").ejDatePicker({ 
specialDates: window.spldays, fields: {date:"date",tooltip:"tooltip",icon:"icon"}});
</script>{% endhighlight %}







### fields.date<span class="type-signature type string">String</span>
{:#members:fields-date}








Specifies the date.











### fields.icon<span class="type-signature type string">String</span>
{:#members:fields-icon}








Specifies the icon to date.











### fields.tooltip<span class="type-signature type string">String</span>
{:#members:fields-tooltip}








Specifies the tooltip to date.











### headerFormat<span class="type-signature type string">String</span>
{:#members:headerformat}








Specifies the header format to be displayed in the Datepicker calendar.




Default Value:
{:.param}






* "MMMM yyyy"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set headerFormat API during initialization  
        $("#datepicker").ejDatePicker({  headerFormat : "MMMM yy" });
</script> {% endhighlight %}







### height<span class="type-signature type string">String</span>
{:#members:height}








Specifies the height of the datepicker input text.




Default Value:
{:.param}






* "28px"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set height API during initialization  
        $("#datepicker").ejDatePicker({  height: 35 });
</script> {% endhighlight %}







### highlightSection<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:highlightsection}








HighlightSection is used to highlight current month, week, workdays. See <a href="global.html#HighlightSection">HighlightSection</a>




Default Value:
{:.param}






* "none"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set highlightSection API during initialization  
        $("#datepicker").ejDatePicker({  highlightSection: "week" });
</script>{% endhighlight %}







### highlightWeekend<span class="type-signature type boolean">Boolean</span>
{:#members:highlightweekend}








Weekend is highlighted when this property is set to true.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set highlightWeekend API during initialization  
        $("#datepicker").ejDatePicker({  highlightWeekend : true });
</script>{% endhighlight %}







### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}








Specifies the HTML Attributes of the DatePicker.




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//Set HtmlAttributes API during initialization  
        $("#datepicker").ejDatePicker({  htmlAttributes : {required:"required"}});
</script>{% endhighlight %}







### locale<span class="type-signature type string">String</span>
{:#members:locale}








Specifies the culture info used by the widget.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set locale API during initialization  
        $("#datepicker").ejDatePicker({  locale: "en-US" });
</script>{% endhighlight %}







### maxDate<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:maxdate}








Specifies the maximum date, the calendar can display.




Default Value:
{:.param}






* new Date(2099, 11, 31)








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set maxDate value during initialization  
        $("#datepicker").ejDatePicker({  maxDate : new Date("5/30/2015") });
</script>{% endhighlight %}







### minDate<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:mindate}








Specifies the minimum date, the calendar can display.




Default Value:
{:.param}






* new Date(1900, 00, 01)








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set minDate value during initialization  
        $("#datepicker").ejDatePicker({  minDate: new Date("5/1/2013") });
</script>{% endhighlight %}







### readOnly<span class="type-signature type boolean">Boolean</span>
{:#members:readonly}








Toggles the readonly state of the widget. When the widget is readonly, it doesn't allow your input.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set readOnly API during initialization  
        $("#datepicker").ejDatePicker({  readOnly : true });
</script> {% endhighlight %}







### showFooter<span class="type-signature type boolean">Boolean</span>
{:#members:showfooter}








It allows to display footer in DatePicker calendar to select today date.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showFooter API during initialization  
        $("#datepicker").ejDatePicker({  showFooter: false });
</script>{% endhighlight %}







### showOtherMonths<span class="type-signature type boolean">Boolean</span>
{:#members:showothermonths}








It allows to display days in other months of DatePicker calendar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showOtherMonths API during initialization  
        $("#datepicker").ejDatePicker({  showOtherMonths: false });
</script> {% endhighlight %}







### showPopupButton<span class="type-signature type boolean">Boolean</span>
{:#members:showpopupbutton}








Shows/Hides the date icon button at right side of textbox that is used to display the DatePicker calendar. While clicking on DateIcon it displays the Datepicker calendar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showPopupButton API during initialization  
        $("#datepicker").ejDatePicker({  showPopupButton: false });
</script>{% endhighlight %}







### showRoundedCorner<span class="type-signature type boolean">Boolean</span>
{:#members:showroundedcorner}








DatePicker input is displayed in rounded corner style when this property is set to true.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showRoundedCorner API during initialization  
        $("#datepicker").ejDatePicker({  showRoundedCorner : true });
</script>{% endhighlight %}







### showTooltip<span class="type-signature type boolean">Boolean</span>
{:#members:showtooltip}








Specifies the property value as true. It displays the tooltip when hovering on the days in the datepicker calendar.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set tooltip API during initialization  
        $("#datepicker").ejDatePicker({  showTooltip : false });
</script>{% endhighlight %}







### specialDates<span class="type-signature type object">object</span>
{:#members:specialdates}








Specifies the special dates in DatePicker.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set specialDates API value during initialization             
// declaration
$("#datepicker").ejDatePicker({specialDates:window.spldays});
</script>{% endhighlight %}







### startDay<span class="type-signature type number">Number</span>
{:#members:startday}








Specifies the start day of the week in DatePicker calendar.




Default Value:
{:.param}






* 0








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set startDay API during initialization  
        $("#datepicker").ejDatePicker({  startDay: 2 });
</script>{% endhighlight %}







### startLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:startlevel}








Specifies the start level view in DatePicker calendar. See <a href="global.html#Level">Level</a>




Default Value:
{:.param}






* ej.DatePicker.Level.Month








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set startLevel API during initialization  
        $("#datepicker").ejDatePicker({  startLevel: ej.DatePicker.Level.Year });
</script>{% endhighlight %}







### stepMonths<span class="type-signature type number">Number</span>
{:#members:stepmonths}








Specifies the number of months to navigate at one click in next and previous button.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set stepMonths API during initialization  
        $("#datepicker").ejDatePicker({  stepMonths: 2 });
</script>{% endhighlight %}





### tooltipFormat<span class="type-signature type string">String</span>
{:#members:tooltipformat}








Sets formatting to the tooltip.




Default Value:
{:.param}






* "ddd MMM dd yyyy"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set tooltipFormat API during initialization  
        $("#datepicker").ejDatePicker({  tooltipFormat : "dd/MM/yyyy" });
</script>{% endhighlight %}









### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}








Sets the jQuery validation error message in datepicker. This property works when the widget is present inside the form. Include jquery.validate.min.js plugin additionally.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" name="datepick" />
<script>
//To set validationMessage API during initialization  
        $("#datepicker").ejDatePicker({
  validationRules:{                     
            required:true
        }                       
  validationMessage:{                   
                required: "Required Date value"
        }
});
</script>{% endhighlight %}







### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}








Sets the jQuery validation rules to the datepicker. This property works when the widget is present inside the form. Include jquery.validate.min.js plugin additionally.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" name="datepick" />
<script>
//To set validationRules API during initialization  
        $("#datepicker").ejDatePicker({  
  validationRules:{                     
          required:true
        }
});
</script>{% endhighlight %}







### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:value}








Specifies the selected date.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set the datepicker value during initialization  
        $("#datepicker").ejDatePicker({  value: new Date("5/5/2014") });
</script>{% endhighlight %}







### watermarkText<span class="type-signature type string">String</span>
{:#members:watermarktext}








Specifies the water mark text to be displayed in input text.




Default Value:
{:.param}






* "Select date"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set watermarkText during initialization  
        $("#datepicker").ejDatePicker({  watermarkText: "Enter date" });
</script>{% endhighlight %}







### width<span class="type-signature type string">String</span>
{:#members:width}








Specifies the width of the datepicker input text.




Default Value:
{:.param}






* "160px"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set width API during initialization  
        $("#datepicker").ejDatePicker({  width: 200 });
</script> {% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








Disables the DatePicker control.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.disable(); // disables the datepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// disables the datepicker
$("#datepicker").ejDatePicker("disable");
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








Enables the DatePicker control.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.enable(); // enables the datepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// enables the datepicker
$("#datepicker").ejDatePicker("enable");
</script>{% endhighlight %}







### getValue<span class="signature">()</span>
{:#methods:getvalue}








Returns the current date value in the DatePicker control.





#### Returns:
{:#methods:returns:}

value


Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.getValue(); // returns the date value
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
// returns the date value
$("#datepicker").ejDatePicker();
$("#datepicker").ejDatePicker("getValue");
</script>{% endhighlight %}







### hide<span class="signature">()</span>
{:#methods:hide}








Hides the DatePicker popup, when in opened state.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.hide(); // hides the datepicker popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// hides the datepicker popup
$("#datepicker").ejDatePicker("hide");
</script>{% endhighlight %}







### show<span class="signature">()</span>
{:#methods:show}








Opens the DatePicker popup.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.show(); // shows the datepicker popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// shows the datepicker popup
$("#datepicker").ejDatePicker("show");
</script>{% endhighlight %}





## Events









### beforeClose
{:#events:beforeclose}








Fires before closing the DatePicker popup.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.events{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event parameters from datepicker.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker popup.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeClose event for datepicker
$("#datepicker").ejDatePicker({
   beforeClose: function (args) {}
});  
</script>                         {% endhighlight %}









### beforeDateCreate
{:#events:beforedatecreate}








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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.date{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current created date object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current DOM object of the date from the Calendar.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeDateCreate event for datepicker
$("#datepicker").ejDatePicker({
   beforeDateCreate: function (args) {}
});  
</script>                         {% endhighlight %}




### beforeOpen
{:#events:beforeopen}








Fires before opening the DatePicker popup.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.events{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event parameters from datepicker.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.element{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker popup.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeOpen event for datepicker
$("#datepicker").ejDatePicker({
   beforeOpen: function (args) {}
});  
</script>                         {% endhighlight %}










### change
{:#events:change}








Fires when the DatePicker input value is changed.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datepicker input value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//change event for datepicker
$("#datepicker").ejDatePicker({
   change: function (args) {}
});  
</script>                         {% endhighlight %}







### close
{:#events:close}








Fires when DatePicker popup is closed.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//close event for datepicker
$("#datepicker").ejDatePicker({
   close: function (args) {}
});   
</script>                         {% endhighlight %}







### create
{:#events:create}








Fires when the DatePicker is created successfully.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//create event for datepicker
$("#datepicker").ejDatePicker({
   create: function (args) {}
});
</script>                         {% endhighlight %}







### destroy
{:#events:destroy}








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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//destroy event for datepicker
$("#datepicker").ejDatePicker({
   destroy: function (args) {}
}); 
</script>                 {% endhighlight %}







### focusIn
{:#events:focusin}








Fires when DatePicker input gets focus.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//focusIn event for datepicker
$("#datepicker").ejDatePicker({
   focusIn: function (args) {}
}); 
</script>                         {% endhighlight %}







### focusOut
{:#events:focusout}








Fires when DatePicker input looses the focus.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//focusOut event for datepicker
$("#datepicker").ejDatePicker({
   focusOut: function (args) {}
});
</script>                         {% endhighlight %}







### open
{:#events:open}








Fires when DatePicker popup is opened.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the eventclose.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//open event for datepicker
$("#datepicker").ejDatePicker({
   open: function (args) {}
});  
</script>                         {% endhighlight %}







### select
{:#events:select}








Fires when a date is selected from the DatePicker popup.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Set to true when the event has to be cancelled, else false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the datepicker model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current date value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDate{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected value.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//select event for datepicker
$("#datepicker").ejDatePicker({
   select: function (args) {}
}); 
</script>                         {% endhighlight %}




