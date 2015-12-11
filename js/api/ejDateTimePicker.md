---
layout: post
title: ejDateTimePicker
description: API reference for ejDateTimePicker
documentation: API
platform: js
keywords: DateTimePicker, ejDateTimePicker, syncfusion, DateTimePicker api

---


# ejDateTimePicker


The DateTimePicker control is used to input the date and time with a specific format. It combines the DatePicker and TimePicker controls so that users can select the date and time with their desired format.


#### Syntax

{% highlight js %}

$(element).ejDateTimePicker(options)

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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">settings for Date Picker.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
// Create DateTimePicker
$("#datetime").ejDateTimePicker();
</script>{% endhighlight %}



#### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.datetimepicker.js


* module:ej.datepicker.js


* module:ej.timepicker.js


* module:ej.scroller.js




## Members


### buttonText `JSONobject`
{:#members:buttontext}



Displays the custom text for the buttons inside the DateTimePicker popup. when the culture value changed, we can change the buttons text based on the culture.


#### Default Value



* { today: "Today", timeNow: "Time Now", done: "Done", timeTitle: "Time" }




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({  buttonText: { done: "&#20570;&#36807;" } });
</script>{% endhighlight %}







### buttonText.done `string`
{:#members:buttontext-done}








Sets the text for the Done button inside the datetime popup.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { done: "Done" }});
</script>{% endhighlight %}







### buttonText.timeNow `string`
{:#members:buttontext-timenow}








Sets the text for the Now button inside the datetime popup.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { timeNow: "Current Time" }});
</script>{% endhighlight %}







### buttonText.timeTitle `string`
{:#members:buttontext-timetitle}








Sets the header text for the Time dropdown.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { timeTitle: "Time" }});
</script>{% endhighlight %}







### buttonText.today `string`
{:#members:buttontext-today}








Sets the text for the Today button inside the datetime popup.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { today: "Today" }});
</script>{% endhighlight %}







### cssClass `string`
{:#members:cssclass}








Set the root class for DateTimePicker theme. This cssClass API helps to use custom skinning option for DateTimePicker control.




#### Default Value







* ""








#### Example



{% highlight html %}
<input type="text" id="datetime" />
<script>                  
//To set cssClass API during initialization  
        $("#datetime").ejDateTimePicker({  cssClass: "gradient-lime" });
</script>{% endhighlight %}







### dateTimeFormat `string`
{:#members:datetimeformat}








Defines the datetime format displayed in the DateTimePicker. The value should be a combination of date format and time format.




#### Default Value







* "M/d/yyyy h:mm tt"








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set dateTimeFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dateTimeFormat: "d/M/yyyy tt h:mm" });
</script> {% endhighlight %}







### dayHeaderFormat `string / enum`
{:#members:dayheaderformat}








Specifies the header format of the datepicker inside the DateTimePicker popup. See DatePicker.Level




#### Default Value







* ej.DatePicker.Header.Min








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set dayHeaderFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dayHeaderFormat: "short" });
</script>{% endhighlight %}







### depthLevel `enum`
{:#members:depthlevel}








Specifies the drill down level in datepicker inside the DateTimePicker popup. See ej.DatePicker.Level




#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set depthLevel API during initialization  
        $("#datetime").ejDateTimePicker({  depthLevel: "decade" });
</script>{% endhighlight %}







### enableAnimation `boolean`
{:#members:enableanimation}








Enable or disable the animation effect in DateTimePicker.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#datetime").ejDateTimePicker({  enableAnimation : false });
</script> 
{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








When this property is set to false, it disables the DateTimePicker control.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enabled API during initialization  
        $("#datetime").ejDateTimePicker({  enabled: true });
</script>{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Enables or disables the state maintenance of DateTimePicker.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enablePersistence API during initialization  
        $("#datetime").ejDateTimePicker({  enablePersistence: true });
</script>{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Sets the DateTimePicker direction as right to left alignment.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enableRTL API during initialization  
        $("#datetime").ejDateTimePicker({  enableRTL: true });
</script> {% endhighlight %}







### enableStrictMode `boolean`
{:#members:enablestrictmode}








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enableStrictMode API during initialization  
        $("#datetime").ejDateTimePicker({  enableStrictMode: true });
</script> {% endhighlight %}







### headerFormat `string`
{:#members:headerformat}








Specifies the header format to be displayed in the DatePicker calendar inside the DateTimePicker popup.




#### Default Value







* "MMMM yyyy"








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set headerFormat API during initialization  
        $("#datetime").ejDateTimePicker({  headerFormat: "MM - yyyy" });
</script>{% endhighlight %}







### height `string / number`
{:#members:height}








Defines the height of the DateTimePicker textbox.




#### Default Value







* 30








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set height API during initialization  
        $("#datetime").ejDateTimePicker({  height: 40 });
</script> {% endhighlight %}







### htmlAttributes `object`
{:#members:htmlattributes}








Specifies the HTML Attributes of the ejDateTimePicker




#### Default Value







* {}








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To Set HtmlAttributes API during initialization  
        $("#datetime").ejDateTimePicker({ htmlAttributes : {required:"required"}});
</script>{% endhighlight %}







### interval `number`
{:#members:interval}








Sets the time interval between the two adjacent time values in the time popup.




#### Default Value







* 30








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set interval API during initialization  
        $("#datetime").ejDateTimePicker({  interval: 60 });
</script>{% endhighlight %}







### locale `string`
{:#members:locale}








Defines the localization culture for DateTimePicker.




#### Default Value







* "en-US"








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set locale API during initialization  
        $("#datetime").ejDateTimePicker({  locale: "en-US" });
</script>{% endhighlight %}







### maxDateTime `string`  `DateObject`
{:#members:maxdatetime}








Sets the maximum value to the DateTimePicker. Beyond the maximum value an error class is added to the wrapper element.




#### Default Value







* new Date("12/31/2099 11:59:59 PM")








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set maxDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  maxDateTime: new Date("12/10/2050 8:00:00 PM") });
</script>{% endhighlight %}







### minDateTime `string`  `DateObject`
{:#members:mindatetime}








Sets the minimum value to the DateTimePicker. Behind the minimum value an error class is added to the wrapper element.




#### Default Value







* new Date("1/1/1900 12:00:00 AM")








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set minDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  minDateTime: new Date("5/5/2010 12:00:00 AM") });
</script>{% endhighlight %}







### readOnly `boolean`
{:#members:readonly}








Indicates that the DateTimePicker value can only be read and can&rsquo;t change.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set readOnly API during initialization  
        $("#datetime").ejDateTimePicker({  readOnly: true });
</script>{% endhighlight %}







### showOtherMonths `boolean`
{:#members:showothermonths}








It allows showing days in other months of DatePicker calendar inside the DateTimePicker popup.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showOtherMonths API during initialization  
        $("#datetime").ejDateTimePicker({  showOtherMonths: false });
</script> {% endhighlight %}







### showPopupButton `boolean`
{:#members:showpopupbutton}








Shows or hides the arrow button from the DateTimePicker textbox. When the button disabled, the DateTimePicker popup opens while focus in the textbox and hides while focusout from the textbox.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showPopupButton API during initialization  
        $("#datetime").ejDateTimePicker({  showPopupButton: false });
</script>{% endhighlight %}







### showRoundedCorner `boolean`
{:#members:showroundedcorner}








Changes the sharped edges into rounded corner for the DateTimePicker textbox and popup.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showRoundedCorner API during initialization  
        $("#datetime").ejDateTimePicker({  showRoundedCorner: true });
</script> {% endhighlight %}







### startDay `number`
{:#members:startday}








Specifies the start day of the week in datepicker inside the DateTimePicker popup.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set startDay API during initialization  
        $("#datetime").ejDateTimePicker({  startDay: 2 });
</script>{% endhighlight %}







### startLevel `string`  `enum`
{:#members:startlevel}








Specifies the start level view in datepicker inside the DateTimePicker popup. See DatePicker.Level




#### Default Value







* ej.DatePicker.Level.Month or "month"








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set startLevel API during initialization  
        $("#datetime").ejDateTimePicker({  startLevel:ej.DatePicker.Level.Year });
</script> {% endhighlight %}







### stepMonths `number`
{:#members:stepmonths}








Specifies the number of months to navigate at one click of next and previous button in datepicker inside the DateTimePicker popup.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set stepMonths API during initialization  
        $("#datetime").ejDateTimePicker({  stepMonths: 2 });
</script>{% endhighlight %}







### timeDisplayFormat `string`
{:#members:timedisplayformat}








Defines the time format displayed in the time dropdown inside the DateTimePicker popup.




#### Default Value







* "h:mm tt"








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set timeDisplayFormat API during initialization  
        $("#datetime").ejDateTimePicker({  timeDisplayFormat: "HH:mm" });
</script> {% endhighlight %}







### timePopupWidth `string / number`
{:#members:timepopupwidth}








Defines the width of the time dropdown inside the DateTimePicker popup.




#### Default Value







* 100








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set timePopupWidth API during initialization  
        $("#datetime").ejDateTimePicker({  timePopupWidth: 150 });
</script> {% endhighlight %}







### validationMessage `object`
{:#members:validationmessage}








Set the jquery validation error message in datetimepicker.




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="datetime" name="datetime" />
<script>
//To set validationMessage API during initialization  
 $("#datetime").ejDateTimePicker({  
  validationRules:{                     
           required:true
   },
        validationMessage: {
           required: "Required DateTime value"
        }
});
</script>{% endhighlight %}







### validationRules `object`
{:#members:validationrules}








Set the jquery validation rules in datetimepicker.




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="datetime" name="datetime" />
<script>
//To set validationRules API during initialization  
 $("#datetime").ejDateTimePicker({  
  validationRules:{                     
          required:true
        }
});
</script>{% endhighlight %}







### value `string / dateobject`
{:#members:value}








Sets the DateTime value to the control.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set value API during initialization  
        $("#datetime").ejDateTimePicker({  value:"6/2/2014 6:00 AM" });
</script> {% endhighlight %}







### width `string / number`
{:#members:width}








Defines the width of the DateTimePicker textbox.




#### Default Value







* 143








#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set width API during initialization  
        $("#datetime").ejDateTimePicker({  width: 210 });
</script> {% endhighlight %}





## Methods








### disable()
{:#methods:disable}








Disables the DateTimePicker control.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.disable(); // disables the datetimepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// disables the datetimepicker
$("#datetime").ejDateTimePicker("disable");
</script>{% endhighlight %}







### enable()
{:#methods:enable}








Enables the DateTimePicker control.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.enable(); // enables the datetimepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// enables the datetimepicker
$("#datetime").ejDateTimePicker("enable");
</script>{% endhighlight %}







### getValue()
{:#methods:getvalue}








Returns the current datetime value in the DateTimePicker.





#### Returns:
{:#methods:returns:}

value


#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.getValue(); // returns the datetime value
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// returns the datetime value
$("#datetime").ejDateTimePicker("getValue");
</script>{% endhighlight %}







### hide()
{:#methods:hide}








Hides or closes the DateTimePicker popup.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.hide(); // hides the datetime popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// hides the datetime popup
$("#datetime").ejDateTimePicker("hide");
</script>{% endhighlight %}







### setCurrentDateTime()
{:#methods:setcurrentdatetime}








Updates the current system date value and time value to the DateTimePicker.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.setCurrentDateTime(); // updates the current datetime value
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// updates the current datetime value
$("#datetime").ejDateTimePicker("setCurrentDateTime");
</script>{% endhighlight %}







### show()
{:#methods:show}








Shows or opens the DateTimePicker popup.





#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// Create DateTimePicker instance
var datetimeObj = $("#datetime").data("ejDateTimePicker");
datetimeObj.show(); // opens the datetime popup
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
$("#datetime").ejDateTimePicker();
// opens the datetime popup
$("#datetime").ejDateTimePicker("show");
</script>{% endhighlight %}





## Events








### change
{:#events:change}








Fires when the datetime value changed in the DateTimePicker textbox.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isValidState{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the current value is valid or not</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//change event for datetimepicker
$("#datetime").ejDateTimePicker({
   change: function (args) {}
}); 
</script>                 {% endhighlight %}







### close
{:#events:close}








Fires when DateTimePicker popup closes.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//close event for datetimepicker
$("#datetime").ejDateTimePicker({
   close: function (args) {}
}); 
</script>                 {% endhighlight %}







### create
{:#events:create}








Fires after DateTimePicker control is created.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DateTimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//create event for datetimepicker
$("#datetime").ejDateTimePicker({
   create: function (args) {}
}); 
</script>                         {% endhighlight %}







### destroy
{:#events:destroy}








Fires when the DateTimePicker is destroyed successfully

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the DateTimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//destroy event for datetimepicker
$("#datetime").ejDateTimePicker({
   destroy: function (args) {}
}); 
</script>                         {% endhighlight %}







### focusIn
{:#events:focusin}








Fires when the focus-in happens in the DateTimePicker textbox.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//focusIn event for datetimepicker
$("#datetime").ejDateTimePicker({
   focusIn: function (args) {}
}); 
</script>                 {% endhighlight %}







### focusOut
{:#events:focusout}








Fires when the focus-out happens in the DateTimePicker textbox.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//focusOut event for datetimepicker
$("#datetime").ejDateTimePicker({
   focusOut: function (args) {}
}); 
</script>                 {% endhighlight %}







### open
{:#events:open}








Fires when DateTimePicker popup opens.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//open event for datetimepicker
$("#datetime").ejDateTimePicker({
   open: function (args) {}
});      
</script>{% endhighlight %}




