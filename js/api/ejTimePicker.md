---
layout: post
title: ejTimePicker
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejTimePicker






The TimePicker control for JavaScript allows users to select a time value. The available times can be restricted to a range by setting minimum and maximum time values. The TimePicker sets the time as a mask to prevent users from entering invalid values.










$(element).ejTimePicker<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Create TimePicker
$("#timepicker").ejTimePicker();
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.core.js


* module:ej.timepicker.js


* module:ej.scroller.js




## Members








### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}








Specify the CSS class to timepicker to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the CSS class during initialization.                     
        $("#timepicker").ejTimePicker({  cssClass : "gradient-lime" });
</script> 
{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members:enableanimation}








Specifies the animation behavior in timepicker.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enableAnimation value during initialization.                         
        $("#timepicker").ejTimePicker({  enableAnimation : false });
</script> 
{% endhighlight %}







### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}








When this property is set to false, it disables the timepicker control.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enabled value during initialization.                         
        $("#timepicker").ejTimePicker({  enabled : false });
</script> 
{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}








Enables or disables the state maintenance of TimePicker.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enablePersistence value during initialization.                       
        $("#timepicker").ejTimePicker({  enablePersistence : true });
</script> 
{% endhighlight %}







### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}








Sets the TimePicker direction as right to left alignment.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the enableRTL value during initialization.                       
        $("#timepicker").ejTimePicker({  enableRTL : true });
</script> 
{% endhighlight %}







### enableStrictMode<span class="type-signature type boolean">Boolean</span>
{:#members:enablestrictmode}








When enableStrictMode true it allows the value outside of the range also, otherwise it internally changed to the correct value.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//To set enableStrictMode API during initialization  
        $("#timepicker").ejTimePicker({  enableStrictMode: true });
</script> {% endhighlight %}







### height<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:height}








Defines the height of the TimePicker textbox.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the height value during initialization.                  
        $("#timepicker").ejTimePicker({  height : "35" });
</script> 
{% endhighlight %}







### hourInterval<span class="type-signature type number">Number</span>
{:#members:hourinterval}








Sets the step value for increment an hour value through arrow keys or mouse scroll.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the hourInterval value during initialization.                    
        $("#timepicker").ejTimePicker({  hourInterval : 2 });
</script> 
{% endhighlight %}







### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}








Specifies the HTML Attributes of the ejTimePicker




Default Value:
{:.param}






* {}








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// To Set HtmlAttributes value during initialization.                   
        $("#timepicker").ejTimePicker({htmlAttributes : {required:"required"});
</script> 
{% endhighlight %}







### interval<span class="type-signature type number">Number</span>
{:#members:interval}








Sets the time interval between the two adjacent time values in the popup.




Default Value:
{:.param}






* 30








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the interval value during initialization.                        
        $("#timepicker").ejTimePicker({  interval : 60 });
</script> 
{% endhighlight %}







### locale<span class="type-signature type string">String</span>
{:#members:locale}








Defines the localization locale for TimePicker.




Default Value:
{:.param}






* "en-US"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the locale value during initialization.                  
        $("#timepicker").ejTimePicker({  locale : "en-US" });
</script> 
{% endhighlight %}







### maxTime<span class="type-signature type string">String</span>
{:#members:maxtime}








Sets the maximum time value to the TimePicker.




Default Value:
{:.param}






* "11:59:59 PM"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the maxTime value during initialization.                         
        $("#timepicker").ejTimePicker({  maxTime : "5:00 PM" });
</script> 
{% endhighlight %}







### minTime<span class="type-signature type string">String</span>
{:#members:mintime}








Sets the minimum time value to the TimePicker.




Default Value:
{:.param}






* "12:00:00 AM"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the minTime value during initialization.                         
        $("#timepicker").ejTimePicker({  minTime : "8:00 AM" });
</script> 
{% endhighlight %}







### minutesInterval<span class="type-signature type number">Number</span>
{:#members:minutesinterval}








Sets the step value for increment the minute value through arrow keys or mouse scroll.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the minute interval value during initialization.                         
        $("#timepicker").ejTimePicker({  minutesInterval : 5 });
</script> 
{% endhighlight %}







### popupHeight<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:popupheight}








Defines the height of the TimePicker popup.




Default Value:
{:.param}






* "191px"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the popupHeight value during initialization.                     
        $("#timepicker").ejTimePicker({  popupHeight : "250px" });
</script> 
{% endhighlight %}







### popupWidth<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:popupwidth}








Defines the width of the TimePicker popup.




Default Value:
{:.param}






* "auto"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the popupWidth value during initialization.                      
        $("#timepicker").ejTimePicker({  popupWidth : "150px" });
</script> 
{% endhighlight %}







### readOnly<span class="type-signature type boolean">Boolean</span>
{:#members:readonly}








Indicates that the timepicker value can only be read.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the readOnly value during initialization.                        
        $("#timepicker").ejTimePicker({  readOnly : false });
</script> 
{% endhighlight %}







### secondsInterval<span class="type-signature type number">Number</span>
{:#members:secondsinterval}








Sets the step value for increment the seconds value through arrow keys or mouse scroll.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the seconds interval value during initialization.                        
        $("#timepicker").ejTimePicker({ timeFormat : "h:mm:ss tt",secondsInterval : 5 });
</script> 
{% endhighlight %}







### showPopupButton<span class="type-signature type boolean">Boolean</span>
{:#members:showpopupbutton}








Shows or hides the arrow button from the TimePicker textbox.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the showPopupButton property during initialization.                      
        $("#timepicker").ejTimePicker({  showPopupButton : false });
</script> 
{% endhighlight %}







### showRoundedCorner<span class="type-signature type boolean">Boolean</span>
{:#members:showroundedcorner}








Changes the sharped edges into rounded corner for the TimePicker textbox and popup.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the showRoundedCorner value during initialization.                       
        $("#timepicker").ejTimePicker({  showRoundedCorner : true });
</script> 
{% endhighlight %}







### timeFormat<span class="type-signature type string">String</span>
{:#members:timeformat}








Defines the time format displayed in the TimePicker.




Default Value:
{:.param}






* "h:mm tt"








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the timeFormat during initialization.                    
        $("#timepicker").ejTimePicker({  timeFormat : "h:mm:ss tt" });
</script> 
{% endhighlight %}







### value<span class="type-signature type string">String</span> <span class="type-signature type dateobject">DateObject</span>
{:#members:value}








Sets a specified time value on the TimePicker.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the time value during initialization.                    
        $("#timepicker").ejTimePicker({  value : "5:10 PM" });
</script> 
{% endhighlight %}







### width<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>
{:#members:width}








Defines the width of the TimePicker textbox.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
// Set the width value during initialization.                   
        $("#timepicker").ejTimePicker({  width : "120" });
</script> 
{% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








To disable the timepicker





Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.disable(); // disable the timepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// disable the timepicker
$("#timepicker").ejTimePicker("disable");
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








To enable the timepicker





Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.enable(); // enables the timepicker
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// enables the timepicker
$("#timepicker").ejTimePicker("enable");
</script>{% endhighlight %}







### getValue<span class="signature">()</span>
{:#methods:getvalue}








returns the current time value





Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.getValue(); // returns the timepicker value
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// to get the time value
$("#timepicker").ejTimePicker("getValue");
</script>{% endhighlight %}







### setCurrentTime<span class="signature">()</span>
{:#methods:setcurrenttime}








updates the current system time to timepicker





Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// Create TimePicker instance
var timeObj = $("#timepicker").data("ejTimePicker");
timeObj.setCurrentTime(); // updates the current system
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
$("#timepicker").ejTimePicker();
// updates the current system
$("#timepicker").ejTimePicker("setCurrentTime");
</script>{% endhighlight %}





## Events








### beforeChange
{:#events:beforechange}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified time value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the modified time value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


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
<td class="description last">returns the TimePicker model</td>
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
 
<input type="text" id="timepicker" />
<script>
//create event for timepicker
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
<td class="description last">returns the TimePicker model</td>
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
 
<input type="text" id="timepicker" />
<script>
//destroy event for timepicker
$("#timepicker").ejTimePicker({
   destroy: function (args) {}
});   
</script> 
                                    {% endhighlight %}







### focusIn
{:#events:focusin}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current time value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//focusIn event for timepicker
$("#timepicker").ejTimePicker({
   focusIn: function (args) {}
});      
</script> 
{% endhighlight %}







### focusOut
{:#events:focusout}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the current time value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//focusOut event for timepicker
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
<td class="description last">returns the TimePicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the previous value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the time value</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//open event for timepicker
$("#timepicker").ejTimePicker({
   open: function (args) {}
});   
</script> 
                                    {% endhighlight %}







### select
{:#events:select}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the timepicker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected time value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<input type="text" id="timepicker" />
<script>
//select event for timepicker
$("#timepicker").ejTimePicker({
   select: function (args) {}
});   
</script> 
                    {% endhighlight %}




