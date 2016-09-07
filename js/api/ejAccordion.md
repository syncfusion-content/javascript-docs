---
layout: post
title: Properties, Methods and Events of ejAccordion Widget
description: API reference for ejAccordion
documentation: API
platform: js
keywords: accordion, ejAccordion, syncfusion, accordion api

---

# ejAccordion

The Accordion control is an interface where lists of items can be collapsed or expanded. It has several collapsible panels where only one can be expanded at a time that is useful for dashboards where space is limited. Each Accordion control has a template for its header and its content.

#### Syntax

{% highlight javascript %}

$(element).ejAccordion()

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language.
                        It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
       $(function () {
           // Initialize Accordion control creation.
           $("#accordion").ejAccordion();
       });
   </script>
   
 {% endhighlight %}


#### Requires

* module:jQuery

* module:jquery.easing.1.3.min.js

* module:ej.core.js

* module:ej.accordion.js


## Members

### ajaxSettings  `object`
{:#members:ajaxsettings}

Specifies the ajaxSettings option to load the content to the accordion control.

#### Default Value

* null

#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Set the ajaxSettings options during initialization.                  
        $("#accordion").ejAccordion({  ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true } });
</script> 
{% endhighlight %}


### ajaxSettings.async `Boolean`
{:#members:ajaxsettings-async}

It specifies, whether to enable or disable asynchronous request.

### ajaxSettings.cache `Boolean`
{:#members:ajaxsettings-cache}

It specifies the page will be cached in the web browser.

### ajaxSettings.contentType `String`
{:#members:ajaxsettings-contenttype}

It specifies the type of data is send in the query string.

### ajaxSettings.data `Object`
{:#members:ajaxsettings-data}

It specifies the data as an object, will be passed in the query string.

### ajaxSettings.dataType `String`
{:#members:ajaxsettings-datatype}

It specifies the type of data that you're expecting back from the response.

### ajaxSettings.type `String`
{:#members:ajaxsettings-type}

It specifies the HTTP request type.

### allowKeyboardNavigation `Boolean`
{:#members:allowkeyboardnavigation}

Accordion headers can be expanded and collapsed on keyboard action.

#### Default Value

* true

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Enable allowKeyboardNavigation on initialization.
        $("#accordion").ejAccordion({ allowKeyboardNavigation: true});
</script>{% endhighlight %}


### collapseSpeed `number`
{:#members:collapsespeed}

To set the Accordion headers Collapse Speed.

#### Default Value

* 300

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Set collapseSpeed on initialization.
        $("#accordion").ejAccordion({ collapseSpeed: 500});
</script>{% endhighlight %}


### collapsible `boolean`
{:#members:collapsible}

Specifies the collapsible state of accordion control.

#### Default Value

* false

#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
// Allow to collapsible on initialization. 
        //To set collapsible API value 
         $("#accordion").ejAccordion({ collapsible: true});
</script>{% endhighlight %}

### cssClass `String`
{:#members:cssclass}

Sets the root CSS class for Accordion theme, which is used customize. 

#### Default Value

* ""

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
 //cssClass on initialization.
        $("#accordion").ejAccordion({cssClass: "gradient-lime" });
</script>{% endhighlight %}


### customIcon `object`
{:#members:customicon}

Allows you to set the custom header Icon. It accepts two key values “header”, ”selectedHeader”.

1. header - The collapsing header CSS class name. 
2. selectedHeader - The active header CSS class name.


#### Default Value

* "{ header: "e-collapse", selectedHeader: "e-expand" }"

### customIcon.header `String`
{:#members:customicon-header}

This class name set to collapsing header. 

### customIcon.selectedHeader `String`
{:#members:customicon-selectedheader}

This class name set to expanded (active) header. 

#### Example


{% highlight html %}
        
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">           
//customIcon on initialization. 
  $("#accordion").ejAccordion({
                customIcon: {
                        header: "header-close",
                        selectedHeader: "header-expand"
                }
        });
</script>{% endhighlight %}

### disabledItems `number[]`
{:#members:disableditems}

Disables the specified indexed items in accordion.

N> The disabledItems is a dependent property of enableMultipleOpen. The enableMultipleOpen property should be set as true.


#### Default Value

* []

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // disabledItems on initialization.
        $("#accordion").ejAccordion({ disabledItems: [0,1] });
</script>{% endhighlight %}


### enableAnimation `Boolean`
{:#members:enableanimation}

Specifies the animation behavior in accordion.

#### Default Value:

* true

#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Set the enableAnimation value during initialization.                         
        $("#accordion").ejAccordion({  enableAnimation : false });
</script> 
{% endhighlight %}


### enabled `Boolean`
{:#members:enabled}

With this enabled property, you can enable or disable the Accordion.

#### Default Value

* true

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Enable accordion on initialization.
        $("#accordion").ejAccordion({ enabled: true});
</script>{% endhighlight %}

### enabledItems `number[]`
{:#members:enableditems}

Used to enable the disabled items in accordion.

N> The enabledItems is a dependent property of enableMultipleOpen. The enableMultipleOpen property should be set as true.


#### Default Value

* []

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // enabledItems on initialization.
        $("#accordion").ejAccordion({ enabledItems: [0,1] });
</script>{% endhighlight %}

### enableMultipleOpen `Boolean`
{:#members:enablemultipleopen}

Multiple content panels to activate at a time.

#### Default Value

* false

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enableMultipleOpen on initialization.
        $("#accordion").ejAccordion({ enableMultipleOpen: true});
</script>{% endhighlight %}


### enablePersistence `Boolean`
{:#members:enablepersistence}

Save current model value to browser cookies for maintaining states. When refreshing the accordion control page, the model value is applied from browser cookies or HTML 5
local storage.

#### Default Value

* false

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enablePersistence on initialization.
        $("#accordion").ejAccordion({ enablePersistence: true});
</script>{% endhighlight %}


### enableRTL `Boolean`
{:#members:enablertl}

Display headers and panel text from right-to-left.

#### Default Value

* false

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Enable enableRTL on initialization.
        $("#accordion").ejAccordion({ enableRTL: true});
</script>{% endhighlight %}

### events `String`
{:#members:events}

The events API binds the action for activating the accordion header. Users can activate the header by using mouse actions such as mouse-over, mouse-up, mouse-down, and so
on.

#### Default Value

* "click"

#### Example

{% highlight html %}
                       
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
// Bind events API on initialization. 
$("#accordion").ejAccordion({ events: "mouseover" });
</script>{% endhighlight %}

### expandSpeed `number`
{:#members:expandspeed}

To set the Accordion headers Expand Speed.

#### Default Value:

* 300

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // Set expandSpeed on initialization.
        $("#accordion").ejAccordion({ expandSpeed: 500});
</script>{% endhighlight %}


### headerSize `number|string`
{:#members:headersize}

Sets the height for Accordion items header.

#### Example

{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">           
//header on initialization. 
  $("#accordion").ejAccordion({
                        headerSize: "40px"
        });
</script>{% endhighlight %}

### height `number|string`
{:#members:height}

Specifies height of the accordion.

#### Default Value:

* null

#### Example

{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">           
//header on initialization. 
  $("#accordion").ejAccordion({
                        height: "500px"
        });
</script>{% endhighlight %}

### heightAdjustMode `enum|string`
{:#members:heightadjustmode}

<ts name="ej.Accordion.HeightAdjustMode" />

Adjusts the content panel height based on the given option (content, auto, or fill). By default, the panel heights are adjusted based on the content. 


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Content</td>
<td class="description">Height fit to the content in the panel</td>
</tr>
<tr>
<td class="name">
Auto</td>
<td class="description">Height set to the largest content in the panel</td>
</tr>
<tr>
<td class="name">
Fill</td>
<td class="description">Height filled to the content of the panel</td>
</tr>
</tbody>
</table>


#### Default Value

* "content"

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//heightAdjustMode  for content div on initialization. 
$("#accordion").ejAccordion({ heightAdjustMode : ej.Accordion.HeightAdjustMode.Auto }); //enum 
</script>{% endhighlight %}


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//Pass value on string type. 
$("#accordion").ejAccordion({ heightAdjustMode : "auto" }); 
</script>{% endhighlight %}

### htmlAttributes `object`
{:#members:htmlattributes}

It allows to define the characteristics of the Accordion control. It will helps to extend the capability of an HTML element.

#### Default Value

* {}

#### Example

{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script type="text/javascript">           
    //HtmlAttributes on initialization. 
    $("#accordion").ejAccordion({
        htmlAttributes: { title: "Demo" }
    });
</script>{% endhighlight %}


### selectedItemIndex `number`
{:#members:selecteditemindex}

The given index header will activate (open). If collapsible is set to true, and a negative value is given, then all headers are collapsed. Otherwise, the first panel is
activated.

#### Default Value

* 0

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
 //Activate given header on initialization.
        $("#accordion").ejAccordion({ selectedItemIndex : 1 });
</script>{% endhighlight %}

### selectedItems `number[]`
{:#members:selecteditems}

Activate the specified indexed items of the accordion

N> The selectedItems is a dependent property of enableMultipleOpen. The enableMultipleOpen property should be set as true.


#### Default Value

* [0]

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
  // selectedItems on initialization.
        $("#accordion").ejAccordion({ selectedItems: [0,1] });
</script>{% endhighlight %}

### showCloseButton `Boolean`
{:#members:showclosebutton}

Used to determines the close button visibility an each accordion items. This close button helps to remove the accordion item from the control.  

#### Default Value

* false

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script type="text/javascript">
        // selectedItems on initialization.
        $("#accordion").ejAccordion({ showCloseButton: true });
</script>{% endhighlight %}

### showRoundedCorner `boolean`
{:#members:showroundedcorner}

Displays rounded corner borders on the Accordion control's panels and headers.

#### Default Value

* false

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script type="text/javascript">
        // Enable showRoundedCorner on initialization.
        $("#accordion").ejAccordion({ showRoundedCorner: true});
</script>{% endhighlight %}

### width `number|string`
{:#members:width}

Specifies width of the accordion.

#### Default Value:

* null

#### Example

{% highlight html %}
      
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">           
  //Accordion initialization. 
  $("#accordion").ejAccordion({
                width: "500px"
        });
</script>{% endhighlight %}


## Methods

### addItem(header_name, content, index, isAjaxReq)
{:#methods:additem}

AddItem method is used to add the panel in dynamically. It receives the following parameters


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
header_name</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">specify the name of the header</td>
</tr>
<tr>
<td class="name">
content</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">content of the new panel</td>
</tr>
<tr>
<td class="name">
index</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">insertion place of the new panel</td>
</tr>
<tr>
<td class="name">
isAjaxReq</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">Enable or disable the AJAX request to the added panel</td>
</tr>
</tbody>
</table>



#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call addItem method.
$("#accordion").ejAccordion("addItem", "New Item", "The accordion content", 2);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// addItem the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.addItem("New item", "The accordion content", 2); //Calls the addItem method of Accordion.   
</script>{% endhighlight %}


### collapseAll()
{:#methods:collapseall}

This method used to collapse the all the expanded items in accordion at a time.

N>  Before we call this method, we must set "collapsible" is true. Then only collapseAll method will working.


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Call collapseAll method.
$("#accordion").ejAccordion();
$("#accordion").ejAccordion("collapseAll");
</script>{% endhighlight %}


{% highlight html %}
 
  <div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// collapse All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.collapseAll(); //Calls the collapseAll method of Accordion.      
</script>{% endhighlight %}


### collapsePanel()
{:#methods:collapsepanel}

This method used to Collapses the specified items in accordion at a time.


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Call collapsePanel method.
$("#accordion").ejAccordion();
$("#accordion").ejAccordion("collapsePanel",0);
</script>{% endhighlight %}


{% highlight html %}
 
  <div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// collapse Panel the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.collapsePanel(0); //Calls the collapsePanel method of Accordion.      
</script>{% endhighlight %}


### destroy()
{:#methods:destroy}

destroy the Accordion widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.destroy(); //Calls the destroy method of Accordion.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// destroy the Accordion
$("#Accordion").ejAccordion("destroy"); 
</script>{% endhighlight %}


### disable()
{:#methods:disable}

Disables the accordion widget includes all the headers and content panels.

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Call disable method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("disable");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// disable the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disable(); //Calls the disable method of Accordion.      
</script>{% endhighlight %}


### disableItems(index)
{:#methods:disableitems}

Disable the accordion widget item based on specified header index.


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
index</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">index values to disable the panels</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call disableItems method.
$("#accordion").ejAccordion("disableItems", [1]);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// disableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems([1]); //Calls the disableItems method of Accordion.   
</script>{% endhighlight %}


### enable()
{:#methods:enable}


Enable the accordion widget includes all the headers and content panels.


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call enable method.
$("#accordion").ejAccordion("enable");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// destroy the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.enable(); //Calls the enable method of Accordion.        
</script>{% endhighlight %}




### enableItems(index)
{:#methods:enableitems}

Enable the accordion widget item based on specified header index.


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
index</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description">index values to enable the panels</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call enableItems method.
$("#accordion").ejAccordion("disableItems", [0]); 
$("#accordion").ejAccordion("disableItems", [1]); 
$("#accordion").ejAccordion("enableItems", [1]);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// enableItems the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.disableItems([0]);
accObj.disableItems([1]);
accObj.enableItems([1]); //Calls the enable method of Accordion.  
</script>{% endhighlight %}




### expandAll()
{:#methods:expandall}

To expand all the accordion widget items.

N>  Before we call this method, we must set "enableMultipleOpen" is true. Then only expandAll method will working.


#### Example


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Call expandAll method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("expandAll");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// expand All the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.expandAll(); //Calls the expandAll method of Accordion.  
</script>{% endhighlight %}



### expandPanel()
{:#methods:expandpanel}

This method used to Expand the specified items in accordion at a time.

#### Example


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// Call expandPanel method.
 $("#accordion").ejAccordion();
$("#accordion").ejAccordion("expandPanel",1);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// expand Panel the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.expandPanel(1); //Calls the expandPanel method of Accordion.  
</script>{% endhighlight %}



### getItemsCount()
{:#methods:getitemscount}

Returns the total number of panels in the control.


#### Returns:
{:#methods:returns:}

number


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call getItemsCount method.
$("#accordion").ejAccordion("getItemsCount");
</script>{% endhighlight %}


{% highlight html %}

<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// getItemsCount the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.getItemsCount(); //Calls the getItemsCount method of Accordion.  
</script>{% endhighlight %}




### hide()
{:#methods:hide}

Hides the visible Accordion control.

#### Example


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call hide method.
$("#accordion").ejAccordion("hide");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// hide the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.hide(); //Calls the hide method of Accordion.    
</script>{% endhighlight %}

### refresh()
{:#methods:refresh}

The refresh method is used to adjust the control size based on the parent element dimension.

#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call refresh method.
$("#accordion").ejAccordion("refresh");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// refresh the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.refresh(); //Calls the refresh method of Accordion.   
</script>{% endhighlight %}


### removeItem(index)
{:#methods:removeitem}

RemoveItem method is used to remove the specified index panel.It receives the parameter as number.
  

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
index </td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">specify the index value for remove the accordion panel.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call removeItem method.
$("#accordion").ejAccordion("removeItem", 2);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// removeItem the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.addItem(2); //Calls the removeItem method of Accordion.   
</script>{% endhighlight %}


### show()
{:#methods:show}


Shows the hidden Accordion control.


#### Example


{% highlight html %}
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
           $("#accordion").ejAccordion();
// Call show method.
$("#accordion").ejAccordion("show");
</script>{% endhighlight %}


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
<script>
// show the Accordion
$("#accordion").ejAccordion();
var accObj = $("#accordion").data("ejAccordion");
accObj.show(); //Calls the show method of Accordion.    
</script>{% endhighlight %}



## Events

### activate
{:#events:activate}


Triggered after a Accordion item is active or inactive. Argument values are activeIndex, activeHeader, inActiveHeader, inActiveIndex and current model value.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 activeIndex </td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns active index</td>
</tr>
<tr>
<td class="name">
 activeHeader </td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active header</td>
</tr>
<tr>
<td class="name">
 isInteraction </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the Accordion index activated by user interaction otherwise returns false</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ activate: function (args) {}
});
</script>{% endhighlight %}




### ajaxBeforeLoad
{:#events:ajaxbeforeload}

Triggered before the AJAX content is loaded in a content panel. Arguments have location of the content (URL) and current model value.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 URL </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns current AJAX content location</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxBeforeLoad event
        $("#accordion").ejAccordion({ ajaxBeforeLoad: function (args) {}
});
</script>{% endhighlight %}




### ajaxError
{:#events:ajaxerror}


Triggered after AJAX load failed action. Arguments have URL, error message, and current model value.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 URL </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns current AJAX content location</td>
</tr>
<tr>
<td class="name">
 data </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the failed data sent.</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxError event
        $("#accordion").ejAccordion({ ajaxError: function (args) {}
});
</script>{% endhighlight %}

### ajaxLoad
{:#events:ajaxload}


Triggered after the AJAX content loads. Arguments have current model values.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 URL </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the URL</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxLoad event
        $("#accordion").ejAccordion({ ajaxLoad: function (args) {}
});
</script>{% endhighlight %}




### ajaxSuccess
{:#events:ajaxsuccess}


Triggered after AJAX success action. Arguments have URL, content, and current model values.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 URL </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns current AJAX content location</td>
</tr>
<tr>
<td class="name">
 data </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the successful data sent.</td>
</tr>
<tr>
<td class="name">
 content </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the AJAX content.</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial ajaxSuccess event
        $("#accordion").ejAccordion({ ajaxSuccess: function (args) {}
});
</script>{% endhighlight %}




### beforeActivate
{:#events:beforeactivate}




Triggered before a tab item is active. Arguments have active index and model values.

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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 activeIndex </td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns active index</td>
</tr>
<tr>
<td class="name">
 isInteraction </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the Accordion index activated by user interaction otherwise returns false</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial beforeActivate event
        $("#accordion").ejAccordion({ beforeActivate: function (args) {}
});
</script>{% endhighlight %}


### beforeInactivate
{:#events:beforeinactivate}

Triggered after a Accordion item is active or inactive. Argument values are activeIndex, activeHeader, inActiveHeader, inActiveIndex and current model value.

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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 inActiveIndex </td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns active index</td>
</tr>
<tr>
<td class="name">
 isInteraction </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the Accordion index activated by user interaction otherwise returns false</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ beforeInactivate: function (args) {}
});
</script>{% endhighlight %}


### create
{:#events:create}

Triggered after Accordion control creation.

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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial create event
        $("#accordion").ejAccordion({ create: function (args) {}
});
</script>{% endhighlight %}


### destroy
{:#events:destroy}

Triggered after Accordion control destroy.

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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial destroy event
        $("#accordion").ejAccordion({ destroy: function (args) {}
});
</script>{% endhighlight %}


### inActivate
{:#events:inactivate}

Triggered after a Accordion item is active or inactive. Argument values are activeIndex, activeHeader, inActiveHeader, inActiveIndex and current model value.


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
 cancel </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
 model </td>
<td class="type"><ts ref="ej.Accordion.Model"/><span class="param-type">object</span></td>
<td class="description">returns the accordion model</td>
</tr>
<tr>
<td class="name">
 type </td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
 inActiveIndex </td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns active index</td>
</tr>
<tr>
<td class="name">
 inActiveHeader </td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns in active element</td>
</tr>
<tr>
<td class="name">
 isInteraction </td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the Accordion index activated by user interaction otherwise returns false</td>
</tr>
</tbody>
</table>



#### Example

{% highlight html %}
 
<div id="accordion">
       <h3>
           <a href="#">ASP.NET</a></h3>
       <div>
Microsoft ASP.NET is a set of technologies in the Microsoft .NET Framework for building Web applications and XML Web services. ASP.NET pages execute on the server and generate markup such as HTML, WML, or XML that is sent to a desktop or mobile browser.
       </div>
       <h3>
           <a href="#">ASP.NET MVC</a></h3>
       <div>
The Model-View-Controller (MVC) architectural pattern separates an application into three main components: the model, the view, and the controller. The ASP.NET MVC framework provides an alternative to the ASP.NET Web Forms pattern for creating Web applications.
       </div>
       <h3>
           <a href="#">Javascript</a></h3>
       <div>
JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed.
       </div>
   </div>
 <script type="text/javascript">
//initial activate event
        $("#accordion").ejAccordion({ inActivate: function (args) {}
});
</script>{% endhighlight %}



