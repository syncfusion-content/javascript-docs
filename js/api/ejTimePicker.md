---
layout: post
title: Properties, Methods and Events of ejTimePicker Widget
description: API reference for ejTimePicker
documentation: API
platform: js
keywords: TimePicker, ejTimePicker, syncfusion, TimePicker api  
---

# ejTimePicker



The TimePicker control for JavaScript allows users to select a time value. The available times can be restricted to a range by setting minimum and maximum time values. The TimePicker sets the time as a mask to prevent users from entering invalid values.



#### Syntax

{% highlight javascript %}

$(element).ejTimePicker()

{% endhighlight %}




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Create TimePicker
$("#timepicker").ejTimePicker();
</script>

{% endhighlight %}



#### Requires


* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.globalize.js


* module:ej.core.js


* module:ej.timepicker.js


* module:ej.scroller.js




## Members








### cssClass `string`
{:#members:cssclass}







Sets the root CSS class for the TimePicker theme, which is used to customize.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the CSS class during initialization.                     
        $("#timepicker").ejTimePicker({  cssClass : "gradient-lime" });
</script>
 
{% endhighlight %}



### disableTimeRanges `object`
{:#members:disabletimeranges}






Specifies the list of time range to be disabled.



### Default value





* {}






#### Example




{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the disableTimeRanges value during initialization.                  
        $("#timepicker").ejTimePicker({  disableTimeRanges: [{ startTime: "3:00 AM", endTime: "6:00 AM" },
                    { startTime: "1:00 PM", endTime: "3:00 PM" },
                    { startTime: "8:00 PM", endTime: "10:00 PM" }] });
</script> 

{% endhighlight %}



### enableAnimation `boolean`
{:#members:enableanimation}








Specifies the animation behavior in TimePicker.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#timepicker").ejTimePicker({  enableAnimation : false });
</script>
 
{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








When this property is set to false, it disables the TimePicker control.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enabled value during initialization.                         
        $("#timepicker").ejTimePicker({  enabled : false });
</script>
 
{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Save current model value to browser cookies for maintaining states. When refreshing the TimePicker control page, the model value is applied from browser cookies or HTML 5
local storage.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enablePersistence value during initialization.                       
        $("#timepicker").ejTimePicker({  enablePersistence : true });
</script> 

{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Displays the TimePicker as right to left alignment.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enableRTL value during initialization.                       
        $("#timepicker").ejTimePicker({  enableRTL : true });
</script> 

{% endhighlight %}







### enableStrictMode `boolean`
{:#members:enablestrictmode}








When the enableStrictMode is set as true it allows the value outside of the range and also indicate with red color border, otherwise it internally changed to the min or max range value based an input value.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//To set enableStrictMode API during initialization  
        $("#timepicker").ejTimePicker({  enableStrictMode: true });
        
</script> {% endhighlight %}














### height `string|number`
{:#members:height}








Defines the height of the TimePicker textbox.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the height value during initialization.                  
        $("#timepicker").ejTimePicker({  height : "35" });
</script> 

{% endhighlight %}







### hourInterval `number`
{:#members:hourinterval}








Sets the step value for increment an hour value through arrow keys or mouse scroll.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the hourInterval value during initialization.                    
        $("#timepicker").ejTimePicker({  hourInterval : 2 });
</script> 

{% endhighlight %}







### htmlAttributes `object`
{:#members:htmlattributes}








It allows to define the characteristics of the TimePicker control. It will helps to extend the capability of an HTML element.




#### Default Value







* {}








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// To Set HtmlAttributes value during initialization.                   
        $("#timepicker").ejTimePicker({htmlAttributes : {required:"required"});
</script> 

{% endhighlight %}







### interval `number`
{:#members:interval}








Sets the time interval between the two adjacent time values in the popup.




#### Default Value







* 30








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the interval value during initialization.                        
        $("#timepicker").ejTimePicker({  interval : 60 });
</script> 

{% endhighlight %}







### locale `string`
{:#members:locale}








Defines the localization info used by the TimePicker.




#### Default Value







* "en-US"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the locale value during initialization.                  
        $("#timepicker").ejTimePicker({  locale : "en-US" });
</script> 

{% endhighlight %}







### maxTime `string`
{:#members:maxtime}








Sets the maximum time value to the TimePicker.




#### Default Value







* "11:59:59 PM"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the maxTime value during initialization.                         
        $("#timepicker").ejTimePicker({  maxTime : "5:00 PM" });
</script> 

{% endhighlight %}







### minTime `string`
{:#members:mintime}








Sets the minimum time value to the TimePicker.




#### Default Value







* "12:00:00 AM"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the minTime value during initialization.                         
        $("#timepicker").ejTimePicker({  minTime : "8:00 AM" });
</script> 

{% endhighlight %}







### minutesInterval `number`
{:#members:minutesinterval}








Sets the step value for increment the minute value through arrow keys or mouse scroll.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the minute interval value during initialization.                         
        $("#timepicker").ejTimePicker({  minutesInterval : 5 });
</script> 

{% endhighlight %}







### popupHeight `string|number`
{:#members:popupheight}








Defines the height of the TimePicker popup.




#### Default Value







* "191px"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the popupHeight value during initialization.                     
        $("#timepicker").ejTimePicker({  popupHeight : "250px" });
</script> 

{% endhighlight %}







### popupWidth `string|number`
{:#members:popupwidth}








Defines the width of the TimePicker popup.




#### Default Value







* "auto"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the popupWidth value during initialization.                      
        $("#timepicker").ejTimePicker({  popupWidth : "150px" });
</script> 
{% endhighlight %}







### readOnly `boolean`
{:#members:readonly}








Toggles the readonly state of the TimePicker




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the readOnly value during initialization.                        
        $("#timepicker").ejTimePicker({  readOnly : false });
</script> 

{% endhighlight %}







### secondsInterval `number`
{:#members:secondsinterval}








Sets the step value for increment the seconds value through arrow keys or mouse scroll.




#### Default Value







* 1








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the seconds interval value during initialization.                        
        $("#timepicker").ejTimePicker({ timeFormat : "h:mm:ss tt",secondsInterval : 5 });
</script> 

{% endhighlight %}







### showPopupButton `boolean`
{:#members:showpopupbutton}








shows or hides the drop down button in TimePicker.




#### Default Value







* true








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the showPopupButton property during initialization.                      
        $("#timepicker").ejTimePicker({  showPopupButton : false });
</script> 

{% endhighlight %}







### showRoundedCorner `boolean`
{:#members:showroundedcorner}








TimePicker is displayed with rounded corner when this property is set to true.




#### Default Value







* false








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the showRoundedCorner value during initialization.                       
        $("#timepicker").ejTimePicker({  showRoundedCorner : true });
</script> 

{% endhighlight %}







### timeFormat `string`
{:#members:timeformat}








Defines the time format displayed in the TimePicker.




#### Default Value







* "h:mm tt"








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the timeFormat during initialization.                    
        $("#timepicker").ejTimePicker({  timeFormat : "h:mm:ss tt" });
</script> 

{% endhighlight %}







### value `string|Date`
{:#members:value}








Sets a specified time value on the TimePicker.




#### Default Value







* null








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the time value during initialization.                    
        $("#timepicker").ejTimePicker({  value : "5:10 PM" });
</script> 

{% endhighlight %}







### width `string|number`
{:#members:width}








Defines the width of the TimePicker textbox.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the width value during initialization.                   
        $("#timepicker").ejTimePicker({  width : "120" });
</script> 

{% endhighlight %}





## Methods








### disable()
{:#methods:disable}








Allows you to disable the TimePicker. 





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.disable(); // disable the timepicker
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// disable the time picker
$("#timepicker").ejTimePicker("disable");
</script>

{% endhighlight %}







### enable()
{:#methods:enable}








Allows you to enable the TimePicker. 





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.enable(); // enables the time picker
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// enables the time picker
$("#timepicker").ejTimePicker("enable");
</script>

{% endhighlight %}







### getValue()
{:#methods:getvalue}








It returns the current time value.


#### Returns:

string





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.getValue(); // returns the time picker value
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// to get the time value
$("#timepicker").ejTimePicker("getValue");
</script>

{% endhighlight %}



### hide()
{:#methods:hide}








This method will hide the TimePicker control popup.





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.hide(); // hide the time picker popup
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// to hide the time picker popup
$("#timepicker").ejTimePicker("hide");
</script>

{% endhighlight %}



### setCurrentTime()
{:#methods:setcurrenttime}








Updates the current system time in TimePicker.





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.setCurrentTime(); // updates the current system
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// updates the current system
$("#timepicker").ejTimePicker("setCurrentTime");
</script>

{% endhighlight %}


### show()
{:#methods:show}








This method will show the TimePicker control popup.





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.show(); // show the time picker popup
</script>

{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// to show the time picker popup
$("#timepicker").ejTimePicker("show");
</script>

{% endhighlight %}



## Events








### beforeChange
{:#events:beforechange}








Fires when the time value changed in the TimePicker.


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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the modified time value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//change event for timepicker
$("#timepicker").ejTimePicker({
   beforeChange: function (args) {}
});  
</script> 
 {% endhighlight %}







### beforeOpen
{:#events:beforeopen}








Fires when the TimePicker popup before opened.

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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//beforeOpen event for timepicker
$("#timepicker").ejTimePicker({
   beforeOpen: function (args) {}
});   
</script> 
                                   
 {% endhighlight %}







### change
{:#events:change}








Fires when the time value changed in the TimePicker.


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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
isInteraction</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the value changed by user interaction otherwise returns false</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the modified time value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//change event for timepicker
$("#timepicker").ejTimePicker({
   change: function (args) {}
});  
</script> 
                   
 {% endhighlight %}







### close
{:#events:close}








Fires when the TimePicker popup closed.

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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//close event for timepicker
$("#timepicker").ejTimePicker({
   close: function (args) {}
});   
</script> 
                                   
  {% endhighlight %}







### create
{:#events:create}








Fires when create TimePicker successfully.

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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//create event for TimePicker
$("#timepicker").ejTimePicker({
   create: function (args) {}
});   
</script> 
 {% endhighlight %}







### destroy
{:#events:destroy}








Fires when the TimePicker is destroyed successfully.

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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//destroy event for TimePicker
$("#timepicker").ejTimePicker({
   destroy: function (args) {}
});   
</script> 
 {% endhighlight %}







### focusIn
{:#events:focusin}








Fires when the TimePicker control gets focus.


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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current time value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//focusIn event for TimePicker
$("#timepicker").ejTimePicker({
   focusIn: function (args) {}
});      
</script> 
{% endhighlight %}







### focusOut
{:#events:focusout}








Fires when the TimePicker control get lost focus.


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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current time value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//focusOut event for TimePicker
$("#timepicker").ejTimePicker({
   focusOut: function (args) {}
}); 
</script> 
{% endhighlight %}







### open
{:#events:open}








Fires when the TimePicker popup opened.

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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
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
<td class="description">returns the time value</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//open event for TimePicker
$("#timepicker").ejTimePicker({
   open: function (args) {}
});   
</script> 
 {% endhighlight %}







### select
{:#events:select}








Fires when the value is selected from the TimePicker dropdown list.


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
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.TimePicker.Model"/><span class="param-type">object</span></td>
<td class="description">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
prevTime</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the previously selected time value</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the selected time value</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//select event for TimePicker
$("#timepicker").ejTimePicker({
   select: function (args) {}
});   
</script> 
 {% endhighlight %}




