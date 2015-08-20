---
layout: post
title: ejScroller
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Scroller control.





$(element).ejScroller<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>  can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
         It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul>     
</div> 
 
<script>
// Create Scroller
$('#scrollcontent').ejScroller();       
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.draggable.js


## Members




### buttonSize<span class="type-signature type number">number</span>
{:#members:buttonsize}




Specifies the button height for vertical scrollbar; for horizontal scrollbar specifies the width of the button in the scrollbar.


Default Value:
{:.param}



* 18




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set Button Size of Scroller during initialization
        $("#scrollcontent").ejScroller({buttonSize: 20 });      
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Specifies to enable or disable the scroller


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//Enable or disable scroller API on initialization
        $("#scrollcontent").ejScroller({enabled: true });       
</script> {% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintanence. While refresh the page Rating control values are retained.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//Enable enablePersistence API on initialization
        $("#scrollcontent").ejScroller({enablePersistence: true });
</script> {% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Indicates the Right to Left direction to scroller


Default Value:
{:.param}



* undefined




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//Enable enableRTL API on initialization
        $("#scrollcontent").ejScroller({enableRTL: true });     
</script> {% endhighlight %}




### enableTouchScroll<span class="type-signature type boolean">boolean</span>
{:#members:enabletouchscroll}




Enables or Disbale the touch Scroll


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//Disable Touch Scroll API on initialization
        $("#scrollcontent").ejScroller({enableTouchScroll: false });    
</script> {% endhighlight %}




### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height of Scroll panel and scrollbars.


Default Value:
{:.param}



* 250




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set height API value during initialization  
        $("#scrollcontent").ejScroller({height: 200 }); 
</script>{% endhighlight %}




### scrollerSize<span class="type-signature type number">number</span>
{:#members:scrollersize}




Set the Scrollbar height and width for this API; if vertical scrollbar,apply the width else apply the height.


Default Value:
{:.param}



* 18




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//Enable scrollerSize on initialization 
        //To set scroller Size API value 
        $("#scrollcontent").ejScroller({scrollerSize: 20 });    
</script>{% endhighlight %}




### scrollLeft<span class="type-signature type number">number</span>
{:#members:scrollleft}




The Scroller content and scrollbars move left with given value.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set Scroll left API during initialization
        $("#scrollcontent").ejScroller({scrollLeft: 40 });      
</script>{% endhighlight %}




### scrollOneStepBy<span class="type-signature type number">number</span>
{:#members:scrollonestepby}




While press on the arrow key the scrollbar position added to the given pixel value.


Default Value:
{:.param}



* 57




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set scrollOneStepBy API value during initialization
        $("#scrollcontent").ejScroller({scrollOneStepBy: 40 }); 
</script>{% endhighlight %}




### scrollTop<span class="type-signature type number">number</span>
{:#members:scrolltop}




The Scroller content and scrollbars move to top position with specified value.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set Scroll top API during initialization
        $("#scrollcontent").ejScroller({scrollTop: 40 });       
</script>{% endhighlight %}




### targetPane<span class="type-signature type string">string</span>
{:#members:targetpane}




Indicates the target area to which scroller have to appear.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set Scroller for the specified target panel during initialization
        $("#scrollcontent").ejScroller({targetPane: "contentarea" });   
</script>{% endhighlight %}




### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width of Scroll panel and scrollbars.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//To set width API value during initialization
        $("#scrollcontent").ejScroller({width: 500 });  
</script>{% endhighlight %}



## Methods




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the Scroller control all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul><li>
<b>A controller</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// Destroy Scroller
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.destroy(); // destroy the scroller
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>*<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// destroy the scroller
$("#scrollcontent").ejScroller("destroy");      
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




User disables the Scroller control at any time.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// To disable the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.disable(); // disable the Scroller control at any time
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// disable the scroller control
$("#scrollcontent").ejScroller("disable");      
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




User enables the Scroller control at any time.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// To enable the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.enable(); // enable the Scroller control at any time
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// enables the scroller control
$("#scrollcontent").ejScroller("enable");       
</script>{% endhighlight %}




### isHScroll<span class="signature">()</span>
{:#methods:ishscroll}




Returns horizontal scrollbar is shown or not.



#### Returns:
{:#methods:returns:}

value

Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
// To check horizontal scrollbar is rendered or not
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.isHScroll(); // Returns horizontal scrollbar is shown or not.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
// To check horizontal scrollbar is rendered or not
$("#scrollcontent").ejScroller("isHScroll");    
</script>{% endhighlight %}




### isVScroll<span class="signature">()</span>
{:#methods:isvscroll}




Returns vertical scrollbar is shown or not.



#### Returns:
{:#methods:returns:}

value

Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// To check vertical scrollbar is rendered or not
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.isVScroll(); // Returns vertical scrollbar is shown or not.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;">
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// To check vertical scrollbar is rendered or not
$("#scrollcontent").ejScrollBar("isVScroll");   
</script>{% endhighlight %}




### refresh<span class="signature">()</span>
{:#methods:refresh}




User refreshes the Scroller control at any time.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// To refresh the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.refresh(); // refreshes the Scroller control at any time
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// Refresh the scroller control
$("#scrollcontent").ejScroller("refresh");      
</script>{% endhighlight %}




### scrollX<span class="signature">()</span>
{:#methods:scrollx}




Scroller moves to given pixel in X (left) position. We can also specify the animation speed,in which the scroller has to move while re-positioning it.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// Moves scroller to given pixel in X (left) position.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.scrollX(25); // call scrollX method(with animation disabled)
scrollObj.scrollX(25,false,1000); // call scrollX method(with animation enabled. the third parameter "1000" indicates the animation speed while re-positioning the scroller)
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
//Moves scroller to given pixel in X (left) position.
$("#scrollcontent").ejScroller("scrollX", 25, true);    // call scrollX method(with animation disabled. "true" indicates animation is off)
$("#scrollcontent").ejScroller("scrollX", 25,false,1000);       // call scrollX method(with animation enabled. Here, the fourth parameter "1000" indicates the animation speed while re-positioning the scroller)
</script>{% endhighlight %}




### scrollY<span class="signature">()</span>
{:#methods:scrolly}




Scroller moves to given pixel in Y (top) position. We can also specify the animation speed,in which the scroller has to move while re-positioning it.



Example
{:.example}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
// Moves scroller to given pixel in Y (top) position.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.scrollY(25); // call scrollY method(with animation disabled)
scrollObj.scrollY(25,false,1000); // call scrollY method(with animation enabled. the third parameter "1000" indicates the animation speed while re-positioning the scroller)
</script>{% endhighlight %}


{% highlight html %}
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
$('#scrollcontent').ejScroller();       
//Moves scroller to given pixel in Y (top) position.
$("#scrollcontent").ejScroller("scrollY", 25, true);    // call scrollY method(with animation disabled. "true" indicates animation is off)
$("#scrollcontent").ejScroller("scrollY", 25,false,1000);       // call scrollY method(with animation enabled. Here, fourth parameter "1000" indicates the animation speed while re-positioning the scroller)
</script>{% endhighlight %}



## Events




### create
{:#events:create}




Fires when Scroller control is created.

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
<td class="description last">Event parameters from scroller
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
<td class="description last">returns the scroller model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//create event for scroller
$("#scrollcontent").ejScroller({
   create: function (args) {}
});   
</script>   {% endhighlight %}




### destroy
{:#events:destroy}




Fires when Scroller control is destroyed.

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
<td class="description last">Event parameters from scroller
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
<td class="description last">returns the scroller model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
 
<div id="scrollcontent" style="width:900px;" >
<p>Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

<ul>
<li>
<b>A controller*</b>can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
</li>
</ul> 
</div> 
 
<script>
//destroy event for scroller
$("#scrollcontent").ejScroller({
   destroy: function (args) {}
});  
</script>     {% endhighlight %}



