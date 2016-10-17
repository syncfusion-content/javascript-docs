---
layout: post
title: Properties,Methods and Events of ejDatePicker Widget
description: API reference for ejDatePicker
documentation: API
platform: js
keywords: datePicker, ejDatePicker, syncfusion, datePicker api 
---

# ejDatePicker

Input field that display the DatePicker calendar as popup to select and set the date value


#### Syntax

{% highlight javascript %}

$(element).ejDatePicker(options)

{% endhighlight %}




<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">settings for Date Picker.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
// Create DatePicker
$("#datepicker").ejDatePicker();
</script>{% endhighlight %}



#### Requires



* module:jQuery


* module:ej.globalize.js


* module:ej.core.js


* module:ej.datepicker.js


N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.



## Members






### allowEdit `boolean`
{:#members:allowedit}


Used to allow or restrict the editing in DatePicker input field directly. By setting false to this API, You can only pick the date from DatePicker popup.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set allowEdit API during initialization  
        $("#datepicker").ejDatePicker({   allowEdit : true });
</script>{% endhighlight %}






### allowDrillDown `boolean`
{:#members:allowdrildown}

allow or restrict the drill down to multiple levels of view (month/year/decade) in DatePicker calendar




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set allowDrillDown API during initialization  
        $("#datepicker").ejDatePicker({   allowDrillDown : true });
</script>{% endhighlight %}




### blackoutDates `object`
{:#members:blackoutdates}

Disable the list of specified date value.




### Default value




* {}







{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set blackoutDates API during initialization  
        $("#datepicker").ejDatePicker({blackoutDates: [new Date(2016, 4, 10), new Date(2016, 4, 15), new Date(2016, 4, 20), new Date(2016, 4, 22), new Date(2016, 5, 12), new Date(2016, 5, 24)] });
</script>

{% endhighlight %}






### buttonText `string`
{:#members:buttontext}


Sets the specified text value to the today button in the DatePicker calendar.




#### Default Value







* "Today"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set buttonText API during initialization  
        $("#datepicker").ejDatePicker({  buttonText : "Now" });
</script>{% endhighlight %}






### cssClass `string`
{:#members:cssclass}








Sets the root CSS class for DatePicker theme, which is used customize.



#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set cssClass API during initialization  
        $("#datepicker").ejDatePicker({  cssClass: "gradient-lime" });
</script>{% endhighlight %}







### dateFormat `string`
{:#members:dateformat}



Formats the value of the DatePicker in to the specified date format. If this API is not specified, dateFormat will be set based on the current culture of DatePicker.




#### Default Value







* "MM/dd/yyyy"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set dateFormat API during initialization  
        $("#datepicker").ejDatePicker({  dateFormat: "dd/MM/yyyy" });
</script>{% endhighlight %}







### dayHeaderFormat `string | enum`
{:#members:dayheaderformat}



<ts name="ej.DatePicker.Header"/>




Specifies the header format of days in DatePicker calendar. See below to get available Headers options


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<tr>
<td class="name">
Long</td>
<td class="description">sets the Min format of day name (like Sunday) in header format DatePicker</td>
</tr>
<td class="name">
None</td>
<td class="description">Removes day header in DatePicker</td>
</tr>
<tr>
<td class="name">
Short</td>
<td class="description">sets  the short format of day name (like Sun) in header in DatePicker</td>
</tr>
<tr>
<td class="name">
Min</td>
<td class="description">sets  the Min format of day name (like su) in header format DatePicker</td>
</tr>

</tbody>
</table>

#### Default Value







* ej.DatePicker.Header.Short








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set dayHeaderFormat API value during initialization  
        $("#datepicker").ejDatePicker({  dayHeaderFormat: ej.DatePicker.Header.Short });
</script>{% endhighlight %}







### depthLevel `string | enum`
{:#members:depthlevel}


<ts name="ej.DatePicker.Level"/>

Specifies the navigation depth level in DatePicker calendar. This option is not applied when start level view option is lower than depth level view. See below to know available levels in DatePicker Calendar


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<tr>
<td class="name">
Month</td>
<td class="description">allow  navigation upto month level in  DatePicker</td>
</tr>
<td class="name">
Year</td>
<td class="description">allow  navigation upto year level in  DatePicker</td>
</tr>
<tr>
<td class="name">
Decade</td>
<td class="description">allow  navigation upto decade level in  DatePicker</td>
</tr>
<tr>
<td class="name">
Century</td>
<td class="description">allow  navigation upto Century level in  DatePicker</td>
</tr>

</tbody>
</table>

#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set depthLevel API during initialization  
        $("#datepicker").ejDatePicker({  depthLevel: ej.DatePicker.Level.Year });
</script>{% endhighlight %}










### displayInline `boolean`
{:#members:displayinline}








Allows to embed the DatePicker calendar in the page. Also associates DatePicker with div element instead of input.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set displayInline API during initialization  
        $("#datepicker").ejDatePicker({  displayInline: true });
</script>{% endhighlight %}







### enableAnimation `boolean`
{:#members:enableanimation}



Enables or disables the animation effect with DatePicker calendar.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#datepicker").ejDatePicker({  enableAnimation : false });
</script> 
{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








Enable or disable the DatePicker control.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enabled API during initialization  
        $("#datepicker").ejDatePicker({  enabled: false });
</script>{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Sustain the entire widget model of DatePicker even after form post or browser refresh 




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enablePersistence API during initialization  
        $("#datepicker").ejDatePicker({  enablePersistence: true });
</script> {% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}



Displays DatePicker calendar along with DatePicker input field in Right to Left direction.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enableRTL API during initialization  
        $("#datepicker").ejDatePicker({  enableRTL : true });
</script>{% endhighlight %}







### enableStrictMode `boolean`
{:#members:enablestrictmode}



Allows to enter valid or invalid date in input textbox and indicate as error if it is invalid value, when this API value is set to true. For false value, invalid date is not allowed to input field and corrected to valid date automatically, even if invalid date is given.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set enableStrictMode API during initialization  
        $("#datepicker").ejDatePicker({  enableStrictMode: true });
</script> {% endhighlight %}







### fields `object`
{:#members:fields}








Used  the required fields for special Dates in DatePicker in order to customize the special dates in a calendar.




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set fields API value during initialization     
var today = new Date(), year = today.getFullYear(), month = today.getMonth(),
spldays = [
           { date: new Date(year, month, 8), tooltip: "In Australia", iconClass: "flags sprite-Australia" },
           { date: new Date(year, month, 21), tooltip: "In France", iconClass: "flags sprite-France" },
           { date: new Date(year, month, 17), tooltip: "In USA", iconClass: "flags sprite-USA" },
           { date: new Date(year, month + 1, 15), tooltip: "In Germany", iconClass: "flags sprite-Germany" },
           { date: new Date(year, month - 1, 22), tooltip: "In India", iconClass: "flags sprite-India" },
]
// declaration
$("#datepicker").ejDatePicker({ 
specialDates: spldays, fields: {date:"date",tooltip:"tooltip",iconClass:"iconClass"}});
</script>{% endhighlight %}







### fields.date `string`
{:#members:fields-date}








Specifies the specials dates











### fields.iconClass `string`
{:#members:fields-iconClass}








Specifies the icon class to special dates.











### fields.tooltip `string`
{:#members:fields-tooltip}








Specifies the tooltip to special dates.




### fields.cssClass `string`
{:#members:fields-cssclass}


Specifies the CSS class to customize the date.




### headerFormat `string`
{:#members:headerformat}








Specifies the header format to be displayed in the DatePicker calendar.




#### Default Value







* "MMMM yyyy"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set headerFormat API during initialization  
        $("#datepicker").ejDatePicker({  headerFormat : "MMMM yy" });
</script> {% endhighlight %}







### height `string`
{:#members:height}








Specifies the height of the DatePicker input text.




#### Default Value







* "28px"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set height API during initialization  
        $("#datepicker").ejDatePicker({  height: 35 });
</script> {% endhighlight %}







### highlightSection `string | enum`
{:#members:highlightsection}



<ts name="ej.DatePicker.HighlightSection"/>

HighlightSection is used to highlight currently selected date's month/week/workdays. See below to get available HighlightSection options


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<tr>
<td class="name">
Month</td>
<td class="description">Highlight the month of the currently selected date in DatePicker popup calendar  </td>
</tr>
<td class="name">
Week</td>
<td class="description">Highlight the week of the currently  selected date in DatePicker popup calendar  </td>
</tr>
<tr>
<td class="name">
WorkDays</td>
<td class="description">Highlight the workdays in a currently  selected date's week in DatePicker popup calendar </td>
</tr>
<tr>
<td class="name">
None</td>
<td class="description">Nothing will be highlighted, remove highlights from DatePicker popup calendar if already exists</td>
</tr>

</tbody>
</table>

#### Default Value







* "none"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set highlightSection API during initialization  
        $("#datepicker").ejDatePicker({  highlightSection: "week" });
</script>{% endhighlight %}







### highlightWeekend `boolean`
{:#members:highlightweekend}








Weekend  dates will be highlighted when this property is set to true.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set highlightWeekend API during initialization  
        $("#datepicker").ejDatePicker({  highlightWeekend : true });
</script>{% endhighlight %}







### htmlAttributes `object`
{:#members:htmlattributes}








Specifies the HTML Attributes of the DatePicker.




#### Default Value







* {}








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//Set HtmlAttributes API during initialization  
        $("#datepicker").ejDatePicker({  htmlAttributes : {required:"required"}});
</script>{% endhighlight %}







### locale `string`
{:#members:locale}








Change the DatePicker calendar and date format based on given culture.




#### Default Value







* "en-US"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set locale API during initialization  
        $("#datepicker").ejDatePicker({  locale: "en-US" });
</script>{% endhighlight %}







### maxDate `string | date`
{:#members:maxdate}








Specifies the maximum date in the calendar that the user can select.




#### Default Value







* new Date(2099, 11, 31)








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set maxDate value during initialization  
        $("#datepicker").ejDatePicker({  maxDate : new Date("5/30/2015") });
</script>{% endhighlight %}







### minDate `string | date`
{:#members:mindate}








Specifies the minimum date in the calendar that the user can select.




#### Default Value







* new Date(1900, 00, 01)








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set minDate value during initialization  
        $("#datepicker").ejDatePicker({  minDate: new Date("5/1/2013") });
</script>{% endhighlight %}







### readOnly `boolean`
{:#members:readonly}





Allows to toggles the read only state of the DatePicker. When the widget is readOnly, it doesn't allow your input.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set readOnly API during initialization  
        $("#datepicker").ejDatePicker({  readOnly : true });
</script> {% endhighlight %}







### showDisabledRange `boolean`
{:#members:showdisabledrange}





It allow to show/hide the disabled date ranges




#### Default Value







* true








#### Example





{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showDisabledRange API during initialization  
        $("#datepicker").ejDatePicker({  showDisabledRange: false });
</script>{% endhighlight %}







### showFooter `boolean`
{:#members:showfooter}








It allows to display footer in DatePicker calendar.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showFooter API during initialization  
        $("#datepicker").ejDatePicker({  showFooter: false });
</script>{% endhighlight %}







### showOtherMonths `boolean`
{:#members:showothermonths}








It allows to display/hides the other months days from the current month calendar in a DatePicker.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showOtherMonths API during initialization  
        $("#datepicker").ejDatePicker({  showOtherMonths: false });
</script> {% endhighlight %}







### showPopupButton `boolean`
{:#members:showpopupbutton}








Shows/hides the date icon button at right side of textbox, which is used to open or close the DatePicker calendar popup.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showPopupButton API during initialization  
        $("#datepicker").ejDatePicker({  showPopupButton: false });
</script>{% endhighlight %}







### showRoundedCorner `boolean`
{:#members:showroundedcorner}




DatePicker input is displayed with rounded corner when this property is set to true.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set showRoundedCorner API during initialization  
        $("#datepicker").ejDatePicker({  showRoundedCorner : true });
</script>{% endhighlight %}







### showTooltip `boolean`
{:#members:showtooltip}








Used to show the tooltip when hovering on the days in the DatePicker calendar.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set tooltip API during initialization  
        $("#datepicker").ejDatePicker({  showTooltip : false });
</script>{% endhighlight %}







### specialDates `object`
{:#members:specialdates}








Specifies the special dates in DatePicker.




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set specialDates API value during initialization
var today = new Date(), year = today.getFullYear(), month = today.getMonth(),
spldays = [
           { date: new Date(year, month, 8), tooltip: "In Australia", iconClass: "flags sprite-Australia" },
           { date: new Date(year, month, 21), tooltip: "In France", iconClass: "flags sprite-France" },
           { date: new Date(year, month, 17), tooltip: "In USA", iconClass: "flags sprite-USA" },
           { date: new Date(year, month + 1, 15), tooltip: "In Germany", iconClass: "flags sprite-Germany" },
           { date: new Date(year, month - 1, 22), tooltip: "In India", iconClass: "flags sprite-India" },
]
// declaration
$("#datepicker").ejDatePicker({specialDates: spldays});
</script>{% endhighlight %}







### startDay `number`
{:#members:startday}








Specifies the start day of the week in DatePicker calendar.




#### Default Value







* 0








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set startDay API during initialization  
        $("#datepicker").ejDatePicker({  startDay: 2 });
</script>{% endhighlight %}







### startLevel `string | enum`
{:#members:startlevel}


<ts name= "ej.DatePicker.Level"/>





Specifies the start level view in DatePicker calendar. See below available Levels

<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<tr>
<td class="name">
Month</td>
<td class="description">Start the view level from month view in DatePicker calendar </td>
</tr>
<td class="name">
Year</td>
<td class="description">Start the view level from year view in DatePicker calendar </td>
</tr>
<tr>
<td class="name">
Decade</td>
<td class="description">Start the view level from decade view in DatePicker calendar </td>
</tr>
<tr>
<td class="name">
Century</td>
<td class="description">Start the view level from century view in DatePicker calendar </td>
</tr>

</tbody>
</table>



#### Default Value







* ej.DatePicker.Level.Month








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set startLevel API during initialization  
        $("#datepicker").ejDatePicker({  startLevel: ej.DatePicker.Level.Year });
</script>{% endhighlight %}







### stepMonths `number`
{:#members:stepmonths}



Specifies the number of months to be navigate for one click of next and previous button in a DatePicker Calendar.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set stepMonths API during initialization  
        $("#datepicker").ejDatePicker({  stepMonths: 2 });
</script>{% endhighlight %}





### tooltipFormat `string`
{:#members:tooltipformat}








Provides option to customize the tooltip format.




#### Default Value







* "ddd MMM dd yyyy"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set tooltipFormat API during initialization  
        $("#datepicker").ejDatePicker({  tooltipFormat : "dd/MM/yyyy" });
</script>{% endhighlight %}









### validationMessage `object`
{:#members:validationmessage}








Sets the jQuery validation support to DatePicker Date value. See [validation](http://help.syncfusion.com/js/datepicker/validation)




#### Default Value







* null








#### Example



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







### validationRules `object`
{:#members:validationrules}








Sets the jQuery validation custom rules to the DatePicker. see [validation](http://help.syncfusion.com/js/datepicker/validation)




#### Default Value







* null








#### Example



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







### value `string | date`
{:#members:value}








sets or returns the current value of DatePicker




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set the DatePicker value during initialization  
        $("#datepicker").ejDatePicker({  value: new Date("5/5/2014") });
</script>{% endhighlight %}







### watermarkText `string`
{:#members:watermarktext}








Specifies the water mark text to be displayed in input text.




#### Default Value







* "Select date"








#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set watermarkText during initialization  
        $("#datepicker").ejDatePicker({  watermarkText: "Enter date" });
</script>{% endhighlight %}







### width `string`
{:#members:width}



Specifies the width of the DatePicker input text.




#### Default Value


* "160px"


#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//To set width API during initialization  
        $("#datepicker").ejDatePicker({  width: 200 });
</script> {% endhighlight %}





## Methods


### disable()
{:#methods:disable}


Disables the DatePicker control.

#### Example



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







### enable()
{:#methods:enable}

Enable the DatePicker control, if it is in disabled state.





#### Example



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







### getValue()
{:#methods:getvalue}








Returns the current date value in the DatePicker control.





#### Returns:


string


#### Example



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







### hide()
{:#methods:hide}








Close the DatePicker popup, if it is in opened state.





#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.hide(); // hides the DatePicker popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// hides the DatePicker popup
$("#datepicker").ejDatePicker("hide");
</script>{% endhighlight %}







### show()
{:#methods:show}








Opens the DatePicker popup.





#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// Create DatePicker instance
var dateObj = $("#datepicker").data("ejDatePicker");
dateObj.show(); // shows the DatePicker popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
$("#datepicker").ejDatePicker();
// shows the DatePicker popup
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
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
events</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event parameters from DatePicker.</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">returns the DatePicker popup.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeClose event for datepicker
$("#datepicker").ejDatePicker({
   beforeClose: function (args) {}
});  
</script>

{% endhighlight %}



### beforeDateCreate
{:#events:beforedatecreate}


Fires when each date is created in the DatePicker popup calendar.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
date</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the currently created date object.</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">returns the current DOM object of the date from the Calendar.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the currently created date as string type.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeDateCreate event for datepicker
$("#datepicker").ejDatePicker({
   beforeDateCreate: function (args) {}
});  
</script>

{% endhighlight %}




### beforeOpen
{:#events:beforeopen}


Fires before opening the DatePicker popup.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
events</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event parameters from DatePicker.</td>
</tr>
<tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">Element</span></td>
<td class="description">returns the DatePicker popup.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//beforeOpen event for datepicker
$("#datepicker").ejDatePicker({
   beforeOpen: function (args) {}
});  
</script>

{% endhighlight %}



### change
{:#events:change}


Fires when the DatePicker input value is changed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the DatePicker input value.</td>
</tr>
<tr>
<td class="name">
prevDate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//change event for datepicker
$("#datepicker").ejDatePicker({
   change: function (args) {}
});  
</script> 

{% endhighlight %}







### close
{:#events:close}


Fires when DatePicker popup is closed.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
date</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current date object.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current date value.</td>
</tr>
<tr>
<td class="name">
prevDate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//close event for datepicker
$("#datepicker").ejDatePicker({
   close: function (args) {}
});   
</script>

{% endhighlight %}







### create
{:#events:create}


Fires when the DatePicker is created successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//create event for datepicker
$("#datepicker").ejDatePicker({
   create: function (args) {}
});
</script>

{% endhighlight %}


### destroy
{:#events:destroy}


Fires when the DatePicker is destroyed successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//destroy event for datepicker
$("#datepicker").ejDatePicker({
   destroy: function (args) {}
}); 
</script>

{% endhighlight %}







### focusIn
{:#events:focusin}
Fires when DatePicker input gets focus.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the currently selected date value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//focusIn event for datepicker
$("#datepicker").ejDatePicker({
   focusIn: function (args) {}
}); 
</script> 

{% endhighlight %}







### focusOut
{:#events:focusout}


Fires when DatePicker input loses the focus.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the currently selected date value.</td>
</tr>
<tr>
<td class="name">
prevDate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected date value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//focusOut event for datepicker
$("#datepicker").ejDatePicker({
   focusOut: function (args) {}
});
</script>

{% endhighlight %}





### navigate
{:#events:navigate}


Fires when calender view navigates to month/year/decade/century.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
date</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current date object.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
navigateFrom</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previous view state of calendar.</td>
</tr>
<tr>
<td class="name">
navigateTo</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current view state of calendar.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current date value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//navigate event for datepicker
$("#datepicker").ejDatePicker({
   navigate: function (args) {}
});  
</script>

{% endhighlight %}





### open
{:#events:open}


Fires when DatePicker popup is opened.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
date</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current date object.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current date value.</td>
</tr>
<tr>
<td class="name">
prevDate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected value.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//open event for datepicker
$("#datepicker").ejDatePicker({
   open: function (args) {}
});  
</script>

{% endhighlight %}







### select
{:#events:select}


Fires when a date is selected from the DatePicker popup.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Set to true when the event has to be canceled, else false.</td>
</tr>
<tr>
<td class="name">
date</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the selected date object.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.DatePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the DatePicker model.</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current date value.</td>
</tr>
<tr>
<td class="name">
prevDate</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected value.</td>
</tr>
<tr>
<td class="name">
isSpecialDay</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns whether the  currently selected date is special date or not.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datepicker" />
<script>
//select event for datepicker
$("#datepicker").ejDatePicker({
   select: function (args) {}
}); 
</script>


{% endhighlight %}




