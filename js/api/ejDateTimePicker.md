---
layout: post
title: ejDateTimePicker
documentation: API
platform: js
metaname: 
metacontent: 
---

Date and Time selection with the input field.










$(element).ejDateTimePicker<span class="signature">(options)</span>







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
 
<input type="text" id="datetime" />
<script>
// Create DateTimePicker
$("#datetime").ejDateTimePicker();
</script>{% endhighlight %}







Requires
{:.require}




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








### buttonText<span class="type-signature type jsonobject">JSONObject</span>
{:#members:buttontext}








Displays the custom text for the buttons inside the DateTimePicker popup. when the culture value changed, we can change the buttons text based on the culture.




Default Value:
{:.param}






* { today: "Today", timeNow: "Time Now", done: "Done", timeTitle: "Time" }








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({  buttonText: { done: "&#20570;&#36807;" } });
</script>{% endhighlight %}







### buttonText.done<span class="type-signature type string">String</span>
{:#members:buttontext-done}








Sets the text for the Done button inside the datetime popup.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { done: "Done" }});
</script>{% endhighlight %}







### buttonText.now<span class="type-signature type string">String</span>
{:#members:buttontext-timeNow}








Sets the text for the Now button inside the datetime popup.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { timeNow: "Current Time" }});
</script>{% endhighlight %}







### buttonText.timeTitle<span class="type-signature type string">String</span>
{:#members:buttontext-timetitle}








Sets the header text for the Time dropdown.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { timeTitle: "Time" }});
</script>{% endhighlight %}







### buttonText.today<span class="type-signature type string">String</span>
{:#members:buttontext-today}








Sets the text for the Today button inside the datetime popup.





Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set buttonText API during initialization  
        $("#datetime").ejDateTimePicker({ buttonText: { today: "Today" }});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Set the root class for DateTimePicker theme. This cssClass API helps to use custom skinning option for DateTimePicker control.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<input type="text" id="datetime" />
<script>                  
//To set cssClass API during initialization  
        $("#datetime").ejDateTimePicker({  cssClass: "gradient-lime" });
</script>{% endhighlight %}







### dateTimeFormat<span class="type-signature type string">String</span>
{:#members:datetimeformat}








Defines the datetime format displayed in the DateTimePicker. The value should be a combination of date format and time format.




Default Value:
{:.param}






* "M/d/yyyy h:mm tt"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set dateTimeFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dateTimeFormat: "d/M/yyyy tt h:mm" });
</script> {% endhighlight %}







### dayHeaderFormat<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:dayheaderformat}








Specifies the header format of the datepicker inside the DateTimePicker popup. See DatePicker.Level




Default Value:
{:.param}






* ej.DatePicker.Header.Min








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set dayHeaderFormat API during initialization  
        $("#datetime").ejDateTimePicker({  dayHeaderFormat: "short" });
</script>{% endhighlight %}







### depthLevel<span class="type-signature type enum">enum</span>
{:#members:depthlevel}








Specifies the drill down level in datepicker inside the DateTimePicker popup. See ej.DatePicker.Level




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set depthLevel API during initialization  
        $("#datetime").ejDateTimePicker({  depthLevel: "decade" });
</script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members:enableanimation}








Enable or disable the animation effect in DateTimePicker.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#datetime").ejDateTimePicker({  enableAnimation : false });
</script> 
{% endhighlight %}







### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}








When this property is set to false, it disables the DateTimePicker control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enabled API during initialization  
        $("#datetime").ejDateTimePicker({  enabled: true });
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}








Enables or disables the state maintenance of DateTimePicker.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enablePersistence API during initialization  
        $("#datetime").ejDateTimePicker({  enablePersistence: true });
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}








Sets the DateTimePicker direction as right to left alignment.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enableRTL API during initialization  
        $("#datetime").ejDateTimePicker({  enableRTL: true });
</script> {% endhighlight %}







### enableStrictMode<span class="type-signature type boolean">Boolean</span>
{:#members:enablestrictmode}








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set enableStrictMode API during initialization  
        $("#datetime").ejDateTimePicker({  enableStrictMode: true });
</script> {% endhighlight %}







### headerFormat<span class="type-signature type string">String</span>
{:#members:headerformat}








Specifies the header format to be displayed in the DatePicker calendar inside the DateTimePicker popup.




Default Value:
{:.param}






* "MMMM yyyy"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set headerFormat API during initialization  
        $("#datetime").ejDateTimePicker({  headerFormat: "MM - yyyy" });
</script>{% endhighlight %}







### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:height}








Defines the height of the DateTimePicker textbox.




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set height API during initialization  
        $("#datetime").ejDateTimePicker({  height: 40 });
</script> {% endhighlight %}







### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}








Specifies the HTML Attributes of the ejDateTimePicker




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To Set HtmlAttributes API during initialization  
        $("#datetime").ejDateTimePicker({ htmlAttributes : {required:"required"}});
</script>{% endhighlight %}







### interval<span class="type-signature type number">Number</span>
{:#members:interval}








Sets the time interval between the two adjacent time values in the time popup.




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set interval API during initialization  
        $("#datetime").ejDateTimePicker({  interval: 60 });
</script>{% endhighlight %}







### locale<span class="type-signature type string">string</span>
{:#members:locale}








Defines the localization culture for DateTimePicker.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set locale API during initialization  
        $("#datetime").ejDateTimePicker({  locale: "en-US" });
</script>{% endhighlight %}







### maxDateTime<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:maxdatetime}








Sets the maximum value to the DateTimePicker. Beyond the maximum value an error class is added to the wrapper element.




Default Value:
{:.param}






* new Date("12/31/2099 11:59:59 PM")








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set maxDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  maxDateTime: new Date("12/10/2050 8:00:00 PM") });
</script>{% endhighlight %}







### minDateTime<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:mindatetime}








Sets the minimum value to the DateTimePicker. Behind the minimum value an error class is added to the wrapper element.




Default Value:
{:.param}






* new Date("1/1/1900 12:00:00 AM")








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set minDateTime API during initialization  
        $("#datetime").ejDateTimePicker({  minDateTime: new Date("5/5/2010 12:00:00 AM") });
</script>{% endhighlight %}







### readOnly<span class="type-signature type boolean">Boolean</span>
{:#members:readonly}








Indicates that the DateTimePicker value can only be read and can&rsquo;t change.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set readOnly API during initialization  
        $("#datetime").ejDateTimePicker({  readOnly: true });
</script>{% endhighlight %}







### showOtherMonths<span class="type-signature type boolean">Boolean</span>
{:#members:showothermonths}








It allows showing days in other months of DatePicker calendar inside the DateTimePicker popup.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showOtherMonths API during initialization  
        $("#datetime").ejDateTimePicker({  showOtherMonths: false });
</script> {% endhighlight %}







### showPopupButton<span class="type-signature type boolean">Boolean</span>
{:#members:showpopupbutton}








Shows or hides the arrow button from the DateTimePicker textbox. When the button disabled, the DateTimePicker popup opens while focus in the textbox and hides while focusout from the textbox.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showPopupButton API during initialization  
        $("#datetime").ejDateTimePicker({  showPopupButton: false });
</script>{% endhighlight %}







### showRoundedCorner<span class="type-signature type boolean">Boolean</span>
{:#members:showroundedcorner}








Changes the sharped edges into rounded corner for the DateTimePicker textbox and popup.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set showRoundedCorner API during initialization  
        $("#datetime").ejDateTimePicker({  showRoundedCorner: true });
</script> {% endhighlight %}







### startDay<span class="type-signature type number">Number</span>
{:#members:startday}








Specifies the start day of the week in datepicker inside the DateTimePicker popup.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set startDay API during initialization  
        $("#datetime").ejDateTimePicker({  startDay: 2 });
</script>{% endhighlight %}







### startLevel<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>
{:#members:startlevel}








Specifies the start level view in datepicker inside the DateTimePicker popup. See DatePicker.Level




Default Value:
{:.param}






* ej.DatePicker.Level.Month or "month"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set startLevel API during initialization  
        $("#datetime").ejDateTimePicker({  startLevel:ej.DatePicker.Level.Year });
</script> {% endhighlight %}







### stepMonths<span class="type-signature type number">Number</span>
{:#members:stepmonths}








Specifies the number of months to navigate at one click of next and previous button in datepicker inside the DateTimePicker popup.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set stepMonths API during initialization  
        $("#datetime").ejDateTimePicker({  stepMonths: 2 });
</script>{% endhighlight %}







### timeDisplayFormat<span class="type-signature type string">String</span>
{:#members:timedisplayformat}








Defines the time format displayed in the time dropdown inside the DateTimePicker popup.




Default Value:
{:.param}






* "h:mm tt"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set timeDisplayFormat API during initialization  
        $("#datetime").ejDateTimePicker({  timeDisplayFormat: "HH:mm" });
</script> {% endhighlight %}







### timePopupWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:timepopupwidth}








Defines the width of the time dropdown inside the DateTimePicker popup.




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set timePopupWidth API during initialization  
        $("#datetime").ejDateTimePicker({  timePopupWidth: 150 });
</script> {% endhighlight %}







### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}








Set the jquery validation error message in datetimepicker.




Default Value:
{:.param}






* null








Example
{:.example}


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







### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}








Set the jquery validation rules in datetimepicker.




Default Value:
{:.param}






* null








Example
{:.example}


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







### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:value}








Sets the DateTime value to the control.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set value API during initialization  
        $("#datetime").ejDateTimePicker({  value:"6/2/2014 6:00 AM" });
</script> {% endhighlight %}







### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:width}








Defines the width of the DateTimePicker textbox.




Default Value:
{:.param}






* 143








Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//To set width API during initialization  
        $("#datetime").ejDateTimePicker({  width: 210 });
</script> {% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








Disables the DateTimePicker control.





Example
{:.example}


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







### enable<span class="signature">()</span>
{:#methods:enable}








Enables the DateTimePicker control.





Example
{:.example}


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







### getValue<span class="signature">()</span>
{:#methods:getvalue}








Returns the current datetime value in the DateTimePicker.





#### Returns:
{:#methods:returns:}

value


Example
{:.example}


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







### hide<span class="signature">()</span>
{:#methods:hide}








Hides or closes the DateTimePicker popup.





Example
{:.example}


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







### setCurrentDateTime<span class="signature">()</span>
{:#methods:setcurrentdatetime}








Updates the current system date value and time value to the DateTimePicker.





Example
{:.example}


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







### show<span class="signature">()</span>
{:#methods:show}








Shows or opens the DateTimePicker popup.





Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isValidState{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current value is valid or not</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DateTimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DateTimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the datetime value, which is in text box</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified datetime value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.prevDateTime{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previously selected date time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="datetime" />
<script>
//open event for datetimepicker
$("#datetime").ejDateTimePicker({
   open: function (args) {}
});      
</script>{% endhighlight %}




