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

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;  can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
         It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt;     
&lt;/div&gt; 
 
&lt;script&gt;
// Create Scroller
$('#scrollcontent').ejScroller();       
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.draggable.js


## Members




### buttonSize<span class="type-signature type number">number</span>
{:#buttonsize}
{:#buttonSize}




Specifies the button height for vertical scrollbar; for horizontal scrollbar specifies the width of the button in the scrollbar.


Default Value:
{:.param}



* 18




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set Button Size of Scroller during initialization
        $("#scrollcontent").ejScroller({buttonSize: 20 });      
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#enabled}
{:#enabled}




Specifies to enable or disable the scroller


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//Enable or disable scroller API on initialization
        $("#scrollcontent").ejScroller({enabled: true });       
&lt;/script&gt; </code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#enablepersistence}
{:#enablePersistence}




Save current model value to browser cookies for state maintanence. While refresh the page Rating control values are retained.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//Enable enablePersistence API on initialization
        $("#scrollcontent").ejScroller({enablePersistence: true });
&lt;/script&gt; </code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#enablertl}
{:#enableRTL}




Indicates the Right to Left direction to scroller


Default Value:
{:.param}



* undefined




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//Enable enableRTL API on initialization
        $("#scrollcontent").ejScroller({enableRTL: true });     
&lt;/script&gt; </code>
</pre>



### enableTouchScroll<span class="type-signature type boolean">boolean</span>
{:#enabletouchscroll}
{:#enableTouchScroll}




Enables or Disbale the touch Scroll


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//Disable Touch Scroll API on initialization
        $("#scrollcontent").ejScroller({enableTouchScroll: false });    
&lt;/script&gt; </code>
</pre>



### height<span class="type-signature type number">number</span>
{:#height}
{:#height}




Specifies the height of Scroll panel and scrollbars.


Default Value:
{:.param}



* 250




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set height API value during initialization  
        $("#scrollcontent").ejScroller({height: 200 }); 
&lt;/script&gt;</code>
</pre>



### scrollerSize<span class="type-signature type number">number</span>
{:#scrollersize}
{:#scrollerSize}




Set the Scrollbar height and width for this API; if vertical scrollbar,apply the width else apply the height.


Default Value:
{:.param}



* 18




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//Enable scrollerSize on initialization 
        //To set scroller Size API value 
        $("#scrollcontent").ejScroller({scrollerSize: 20 });    
&lt;/script&gt;</code>
</pre>



### scrollLeft<span class="type-signature type number">number</span>
{:#scrollleft}
{:#scrollLeft}




The Scroller content and scrollbars move left with given value.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set Scroll left API during initialization
        $("#scrollcontent").ejScroller({scrollLeft: 40 });      
&lt;/script&gt;</code>
</pre>



### scrollOneStepBy<span class="type-signature type number">number</span>
{:#scrollonestepby}
{:#scrollOneStepBy}




While press on the arrow key the scrollbar position added to the given pixel value.


Default Value:
{:.param}



* 57




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set scrollOneStepBy API value during initialization
        $("#scrollcontent").ejScroller({scrollOneStepBy: 40 }); 
&lt;/script&gt;</code>
</pre>



### scrollTop<span class="type-signature type number">number</span>
{:#scrolltop}
{:#scrollTop}




The Scroller content and scrollbars move to top position with specified value.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set Scroll top API during initialization
        $("#scrollcontent").ejScroller({scrollTop: 40 });       
&lt;/script&gt;</code>
</pre>



### targetPane<span class="type-signature type string">string</span>
{:#targetpane}
{:#targetPane}




Indicates the target area to which scroller have to appear.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set Scroller for the specified target panel during initialization
        $("#scrollcontent").ejScroller({targetPane: "contentarea" });   
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type number">number</span>
{:#width}
{:#width}




Specifies the width of Scroll panel and scrollbars.


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//To set width API value during initialization
        $("#scrollcontent").ejScroller({width: 500 });  
&lt;/script&gt;</code>
</pre>


## Methods




### destroy<span class="signature">()</span>
{:#destroy}
{:#destroy}




destroy the Scroller control all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;&lt;li&gt;
&lt;b&gt;A controller&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// Destroy Scroller
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.destroy(); // destroy the scroller
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;*&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// destroy the scroller
$("#scrollcontent").ejScroller("destroy");      
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#disable}
{:#disable}




User disables the Scroller control at any time.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// To disable the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.disable(); // disable the Scroller control at any time
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// disable the scroller control
$("#scrollcontent").ejScroller("disable");      
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#enable}
{:#enable}




User enables the Scroller control at any time.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// To enable the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.enable(); // enable the Scroller control at any time
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// enables the scroller control
$("#scrollcontent").ejScroller("enable");       
&lt;/script&gt;</code>
</pre>



### isHScroll<span class="signature">()</span>
{:#ishscroll}
{:#isHScroll}




Returns horizontal scrollbar is shown or not.



#### Returns:
{:#returns:}
{:#Returns:}

value

Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
// To check horizontal scrollbar is rendered or not
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.isHScroll(); // Returns horizontal scrollbar is shown or not.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
// To check horizontal scrollbar is rendered or not
$("#scrollcontent").ejScroller("isHScroll");    
&lt;/script&gt;</code>
</pre>



### isVScroll<span class="signature">()</span>
{:#isvscroll}
{:#isVScroll}




Returns vertical scrollbar is shown or not.



#### Returns:
{:#returns:}
{:#Returns:}

value

Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// To check vertical scrollbar is rendered or not
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.isVScroll(); // Returns vertical scrollbar is shown or not.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;"&gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// To check vertical scrollbar is rendered or not
$("#scrollcontent").ejScrollBar("isVScroll");   
&lt;/script&gt;</code>
</pre>



### refresh<span class="signature">()</span>
{:#refresh}
{:#refresh}




User refreshes the Scroller control at any time.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// To refresh the Scroller control at any time.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.refresh(); // refreshes the Scroller control at any time
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// Refresh the scroller control
$("#scrollcontent").ejScroller("refresh");      
&lt;/script&gt;</code>
</pre>



### scrollX<span class="signature">()</span>
{:#scrollx}
{:#scrollX}




Scroller moves to given pixel in X (left) position. We can also specify the animation speed,in which the scroller has to move while re-positioning it.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// Moves scroller to given pixel in X (left) position.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.scrollX(25); // call scrollX method(with animation disabled)
scrollObj.scrollX(25,false,1000); // call scrollX method(with animation enabled. the third parameter "1000" indicates the animation speed while re-positioning the scroller)
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
//Moves scroller to given pixel in X (left) position.
$("#scrollcontent").ejScroller("scrollX", 25, true);    // call scrollX method(with animation disabled. "true" indicates animation is off)
$("#scrollcontent").ejScroller("scrollX", 25,false,1000);       // call scrollX method(with animation enabled. Here, the fourth parameter "1000" indicates the animation speed while re-positioning the scroller)
&lt;/script&gt;</code>
</pre>



### scrollY<span class="signature">()</span>
{:#scrolly}
{:#scrollY}




Scroller moves to given pixel in Y (top) position. We can also specify the animation speed,in which the scroller has to move while re-positioning it.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
// Moves scroller to given pixel in Y (top) position.
var scrollerObj  = $("#scrollcontent").data("ejScroller");
scrollerObj.scrollY(25); // call scrollY method(with animation disabled)
scrollObj.scrollY(25,false,1000); // call scrollY method(with animation enabled. the third parameter "1000" indicates the animation speed while re-positioning the scroller)
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
$('#scrollcontent').ejScroller();       
//Moves scroller to given pixel in Y (top) position.
$("#scrollcontent").ejScroller("scrollY", 25, true);    // call scrollY method(with animation disabled. "true" indicates animation is off)
$("#scrollcontent").ejScroller("scrollY", 25,false,1000);       // call scrollY method(with animation enabled. Here, fourth parameter "1000" indicates the animation speed while re-positioning the scroller)
&lt;/script&gt;</code>
</pre>


## Events




### create
{:#create}
{:#create}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the scroller model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//create event for scroller
$("#scrollcontent").ejScroller({
   create: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>



### destroy
{:#destroy}
{:#destroy}




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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the scroller model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;div id="scrollcontent" style="width:900px;" &gt;
&lt;p&gt;Model&ndash;view&ndash;controller (MVC) is a software architecture pattern which separates the
representation of information from the user's interaction with it.
The model consists of application data, business rules, logic, and functions. A view can be any
output representation of data, such as a chart or a diagram. Multiple views of the same data 
are possible, such as a bar chart for management and a tabular view for accountants. 
The controller mediates input, converting it to commands for the model or view.The central 
ideas behind MVC are code reusability and n addition to dividing the application into three 
kinds of components, the MVC design defines the interactions between them.

&lt;ul&gt;
&lt;li&gt;
&lt;b&gt;A controller*&lt;/b&gt;can send commands to its associated view to change the view's presentation of the model (e.g., by scrolling through a document). 
It can also send commands to the model to update the model's state (e.g., editing a document).
&lt;/li&gt;
&lt;/ul&gt; 
&lt;/div&gt; 
 
&lt;script&gt;
//destroy event for scroller
$("#scrollcontent").ejScroller({
   destroy: function (args) {}
});  
&lt;/script&gt;     </code>
</pre>


