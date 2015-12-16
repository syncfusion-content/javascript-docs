---
layout: post
title: ejTab
description: API reference for ejTab
documentation: API
platform: js
keywords: Tab, ejTab, syncfusion, Tab api 
---

# ejTab



The Tab control is an interface where list of items are expanded from a single item. Each Tab panel defines its header text or header template, as well as a content template. Tab items are dynamically added and removed. Tabs can be loaded with AJAX content that is useful for building dashboards where space is limited.




#### Syntax

{% highlight js %}

$(element).ejTab()

{% endhighlight %}







#### Example



{% highlight html %}
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$(function () {             
// document ready            
// Initialize Tab control creation             
$("#tab").ejTab({width:"300px"});         
}); </script>     {% endhighlight %}




#### Requires



* module:jQuery

* module:jquery.easing.1.3.min.js

* module:ej.core.js

* module:ej.tab.js


## Members




### ajaxSettings `object`
{:#members:ajaxsettings}




Specifies the ajaxSettings option to load the content to the Tab control.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="http://en.wikipedia.org/wiki/C_Sharp_(programming_language)">C Sharp (C#)</a></li>                      
<li><a href="http://en.wikipedia.org/wiki/Visual_Basic_.NET">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
</div>
<script type="text/javascript">         
//To set enableAnimation API value during initialization  
  $("#tab").ejTab({ ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true } });
</script>{% endhighlight %}




### ajaxSettings.async `boolean`
{:#members:ajaxsettings-async}




It specifies, whether to enable or disable asynchronous request.






### ajaxSettings.cache `boolean`
{:#members:ajaxsettings-cache}




It specifies the page will be cached in the web browser.






### ajaxSettings.contentType `string`
{:#members:ajaxsettings-contenttype}




It specifies the type of data is send in the query string.






### ajaxSettings.data `object`
{:#members:ajaxsettings-data}




It specifies the data as an object, will be passed in the query string.






### ajaxSettings.dataType `string`
{:#members:ajaxsettings-datatype}




It specifies the type of data that you're expecting back from the response.






### ajaxSettings.type `string`
{:#members:ajaxsettings-type}




It specifies the HTTP request type.






### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}




Tab items interaction with keyboard keys, like headers active navigation.


#### Default Value




* true




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the allowKeyboardNavigation during initialization.                       
        $("#tab").ejTab({width:"300px",allowKeyboardNavigation: false }); 
</script>  {% endhighlight %}




### collapsible `boolean`
{:#members:collapsible}




Allow to collapsing the active item, while click on the active header.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the collapsible during initialization.                   
        $("#tab").ejTab({width:"300px",collapsible: true }); 
</script>  {% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Set the root class for Tab theme. This cssClass API helps to use custom skinning option for Tab control.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the CSS class during initialization.                     
        $("#tab").ejTab({width:"300px",cssClass: "gradient-lime" }); 
</script>  {% endhighlight %}




### disabledItemIndex `integerarray`
{:#members:disableditemindex}




Disables the given tab headers and content panels.


#### Default Value




* []




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>   
<script type="text/javascript">         
// Set the disabledItemIndex during initialization.                     
        $("#tab").ejTab({width:"300px",disabledItemIndex: [1,2] }); 
</script>  {% endhighlight %}




### enableAnimation `boolean`
{:#members:enableanimation}




Specifies the animation behavior of the tab.


#### Default Value




* true




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
//To set enableAnimation API value during initialization  
        $("#tab").ejTab({ enableAnimation: false});
</script>{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




When this property is set to false, it disables the tab control.


#### Default Value




* true




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the enabled during initialization.                       
        $("#tab").ejTab({width:"300px",enabled: false }); 
</script>  {% endhighlight %}




### enabledItemIndex `integerarray`
{:#members:enableditemindex}




Enables the given tab headers and content panels.


#### Default Value




* []




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>   
<script type="text/javascript">         
// Set the enabledItemIndex during initialization. 
        $("#tab").ejTab({width:"300px",disabledItemIndex: [0,1,2] });
 $("#tab").ejTab({width:"300px",enabledItemIndex: [0,1] }); 
</script>  {% endhighlight %}




### enablePersistence `boolean`
{:#members:enablepersistence}




Save current model value to browser cookies for state maintains. While refresh the Tab control page the model value apply from browser cookies.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div> 
<script type="text/javascript">         
// Set the enablePersistence during initialization.                     
        $("#tab").ejTab({width:"300px",enablePersistence: false }); 
</script>  {% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Display Right to Left direction for headers and panels text.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the rtl during initialization.                   
        $("#tab").ejTab({width:"300px",enableRTL: true }); 
</script>  {% endhighlight %}




### enableTabScroll `boolean`
{:#members:enabletabscroll}




Specify to enable scrolling for Tab header.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the enableTabScroll during initialization.                       
        $("#tab").ejTab({width:"300px",enableTabScroll: true }); 
</script>  {% endhighlight %}




### events `string`
{:#members:events}




The event API to bind the action for active the tab items.


#### Default Value




* "click"




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>     
<script type="text/javascript">         
// Set the events during initialization.                        
        $("#tab").ejTab({width:"300px",events: "click" }); 
</script>  {% endhighlight %}




### headerPosition `string`  `enum`
{:#members:headerposition}




Tab header display top,bottom,left or right .See <a href="global.html#Position">Position</a>


#### Default Value




* "top"




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the headerPosition during initialization.                        
        $("#tab").ejTab({width:"500px",headerPosition: "left" }); 
</script>  {% endhighlight %}




### headerSize `string`  `number`
{:#members:headersize}




Set the height of the tab header element. Default this property value is null, so height take content height.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the height during initialization.                        
        $("#tab").ejTab({headerSize: "100px" }); 
</script>  {% endhighlight %}




### height `string`  `number`
{:#members:height}




Height set the outer panel element. Default this property value is null, so height take content height.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the height during initialization.                        
        $("#tab").ejTab({width:"300px",height: "320px" }); 
</script>  {% endhighlight %}




### heightAdjustMode `string`  `enum`
{:#members:heightadjustmode}




Adjust the content panel height for given option (content, auto and fill), by default panels height adjust based on the content.See <a href="global.html#HeightAdjustMode">HeightAdjustMode</a>


#### Default Value




* "content"




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div> 
<script type="text/javascript">         
// Set the heightAdjustMode  during initialization.                     
        $("#tab").ejTab({width:"300px",heightAdjustMode : ej.Tab.HeightAdjustMode.Content }); 
</script>  {% endhighlight %}




### idPrefix `string`
{:#members:idprefix}




The idPrefix property appends the give string on runtime added tab item id&rsquo;s.


#### Default Value




* "ej-tab-"




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the idPrefix during initialization.                      
        $("#tab").ejTab({width:"300px",idPrefix: "ej-tab-" }); 
</script>  {% endhighlight %}




### selectedItemIndex `number`
{:#members:selecteditemindex}




Tab header to active for given index value.


#### Default Value




* 0




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the selectedItemIndex  during initialization.                    
        $("#tab").ejTab({width:"300px",selectedItemIndex : 1 }); 
</script>  {% endhighlight %}




### showCloseButton `boolean`
{:#members:showclosebutton}




Display the close button for each tab items. While click on the close icon particular tab item removed.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>   
<script type="text/javascript">         
// Set the showCloseButton during initialization.                       
        $("#tab").ejTab({width:"500px",showCloseButton: true }); 
</script>  {% endhighlight %}




### showReloadIcon `boolean`
{:#members:showreloadicon}




Display the Reload button for each tab items.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the showReloadIcon during initialization.                        
        $("#tab").ejTab({width:"500px",showReloadIcon: true }); 
</script>  {% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Tab panels and headers to display the rounded corner style.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the roundedCorner during initialization.                         
        $("#tab").ejTab({width:"300px",showRoundedCorner: false }); 
</script>  {% endhighlight %}




### width `string`  `number`
{:#members:width}




Set the width for outer panel element, if not it&rsquo;s take parent width.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
// Set the width during initialization.                         
        $("#tab").ejTab({width: "600px" }); 
</script>  {% endhighlight %}



## Methods




### addItem(url, displayLabel, index)</span>
{:#methods:additem}




Add new tab items with given name, url and given index position, if index null it&rsquo;s add last item.

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
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">URL name / tab id.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
displayLabel{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Tab Display name.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">Index position to placed , this is optional.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>  
<div id="new"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>             
</div>
<script type="text/javascript">         
//initialize the tab object
$("#tab").ejTab({width:"400px"});
        var tabObj = $("#tab").data("ejTab");
        // Add new tab items with given list
        tabObj.addItem("#new","New Item",3);
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div> 
<div id="new"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">  
$("#tab").ejTab({width:"400px"});       
$("#tab").ejTab("addItem","#new","New Item",3); 
</script>  {% endhighlight %}




### disable()
{:#methods:disable}




To disable the tab control.



#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">  
$("#tab").ejTab({width:"300px"});      
//initialize the tab object
var tabObj = $("#tab").data("ejTab");
        // disable the tab control
        tabObj.disable();
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">  
$("#tab").ejTab({width:"300px"});       
$("#tab").ejTab("disable");
</script>  {% endhighlight %}




### enable()
{:#methods:enable}




To enable the tab control.



#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">   
$("#tab").ejTab({width:"300px"});      
//initialize the tab object
        var tabObj = $("#tab").data("ejTab");
        // enable the tab control
        tabObj.enable();
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">     
$("#tab").ejTab({width:"300px"});    
$("#tab").ejTab("enable");
</script>  {% endhighlight %}




### getItemsCount()
{:#methods:getitemscount}




This function get the number of tab rendered



#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">    
$("#tab").ejTab({width:"300px"});     
//initialize the tab object
        var tabObj = $("#tab").data("ejTab");
        // get the number of tab rendered
        tabObj.getItemsCount();
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">    
$("#tab").ejTab({width:"300px"});     
$("#tab").ejTab("getItemsCount");
</script>  {% endhighlight %}




### hide()
{:#methods:hide}




This function hides the tab control.



#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">   
$("#tab").ejTab({width:"300px"});      
//initialize the tab object
        var tabObj = $("#tab").data("ejTab");
        // To hide the tab control..
        tabObj.hide();
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">   
$("#tab").ejTab({width:"300px"});      
$("#tab").ejTab("hide"); 
</script>  {% endhighlight %}




### removeItem(index)</span>
{:#methods:removeitem}




Remove the given index tab item.

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
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">index of tab item.</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">    
$("#tab").ejTab({width:"300px"});     
//initialize the tab object
        var tabObj = $("#tab").data("ejTab");
        // Remove the given index tab item.
        tabObj.removeItem(1);
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript"> 
$("#tab").ejTab({width:"300px"});        
$("#tab").ejTab("removeItem",1); 
</script>  {% endhighlight %}




### show()
{:#methods:show}




This function is to show the tab control.



#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript"> 
$("#tab").ejTab({width:"300px"});        
//initialize the tab object
        var tabObj = $("#tab").data("ejTab");
        // To show the tab control.
        tabObj.show();
</script>  {% endhighlight %}


{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">    
$("#tab").ejTab({width:"300px"});     
$("#tab").ejTab("show"); 
</script>  {% endhighlight %}



## Events




### itemActive
{:#events:itemactive}




Triggered after a tab item activated.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   itemActive: function (args) {}
});      
</script>  {% endhighlight %}




### ajaxBeforeLoad
{:#events:ajaxbeforeload}




Triggered before ajax content load action.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width:"300px",
   ajaxBeforeLoad: function (args) {}
});      
</script>  {% endhighlight %}




### ajaxError
{:#events:ajaxerror}




Triggered after a tab item activated.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   ajaxError: function (args) {}
});      
</script>  {% endhighlight %}




### ajaxLoad
{:#events:ajaxload}




Triggered after ajax content load action.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the url</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width:"300px",
   ajaxLoad: function (args) {}
});      
</script>  {% endhighlight %}




### ajaxSuccess
{:#events:ajaxsuccess}




Triggered after a tab item activated.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   ajaxSuccess: function (args) {}
});      
</script>  {% endhighlight %}




### beforeActive
{:#events:beforeactive}




Triggered before a tab item activated.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns previous active tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
prevActiveIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns previous active index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns current active tab header .</td>
</tr>
<tr>
<td class="name">{% highlight html %}
activeIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current active index.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   beforeActive: function (args) {}
});      
</script>  {% endhighlight %}




### beforeItemRemove
{:#events:beforeitemremove}




Triggered before a tab item remove.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button.
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   beforeItemRemove: function (args) {}
});      
</script>  {% endhighlight %}




### create
{:#events:create}




Triggered before a tab item Create.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button.
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
deleteIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   create: function (args) {}
});      
</script>  {% endhighlight %}




### destroy
{:#events:destroy}




Triggered before a tab item destroy.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button.
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
deleteIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns current tab item index</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   destroy: function (args) {}
});      
</script>  {% endhighlight %}




### itemAdd
{:#events:itemadd}




Triggered after new tab item add

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tabHeader{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns new added tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
tabContent{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns new added tab content panel.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   itemAdd: function (args) {}
});      
</script>  {% endhighlight %}




### itemRemove
{:#events:itemremove}




Triggered after tab item removed.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tab model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
removedTab{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns removed tab header.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
removedPanel{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns removed tab content panel.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="tab">                  
<ul>                      
<li><a href="#javaScript">JavaScript</a></li>                      
<li><a href="#cSharp">C Sharp (C#)</a></li>                      
<li><a href="#vb">VB.Net</a></li>                  
</ul>                  
<div id="javaScript"> JavaScript (JS) is an interpreted computer programming language. 
It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  
</div>                  
<div id="cSharp"> C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  
</div>                  
<div id="vb"> The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  
</div>              
</div>
<script type="text/javascript">         
$("#tab").ejTab({
width: "300px",
   itemRemove: function (args) {}
});      
</script>  {% endhighlight %}



