---
layout: post
title: ejTab
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Tab control.





#### $(element).ejTab<span class="signature">()</span>






##### Example
<pre class="prettyprint"><code>&lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $(function () {             // document ready            // Initialize Tab control creation             $("#tab").ejTab({width:"300px"});         }); &lt;/script&gt;     </code></pre>



### Requires


* module:jQuery

* module:jquery.easing.1.3.min.js

* module:ej.core.js

* module:ej.tab.js


### Members




#### ajaxSettings<span class="type-signature type object">object</span>




Specifies the ajaxSettings option to load the content to the Tab control.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="http://en.wikipedia.org/wiki/C_Sharp_(programming_language)"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="http://en.wikipedia.org/wiki/Visual_Basic_.NET"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;/div&gt;&lt;script type="text/javascript"&gt;         //To set enableAnimation API value during initialization    $("#tab").ejTab({ ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true } });&lt;/script&gt;</code></pre>



#### ajaxSettings.async<span class="type-signature type boolean">Boolean</span>




It specifies, whether to enable or disable asynchronous request.






#### ajaxSettings.cache<span class="type-signature type boolean">Boolean</span>




It specifies the page will be cached in the web browser.






#### ajaxSettings.contentType<span class="type-signature type string">String</span>




It specifies the type of data is send in the query string.






#### ajaxSettings.data<span class="type-signature type object">Object</span>




It specifies the data as an object, will be passed in the query string.






#### ajaxSettings.dataType<span class="type-signature type string">String</span>




It specifies the type of data that you're expecting back from the response.






#### ajaxSettings.type<span class="type-signature type string">String</span>




It specifies the HTTP request type.






#### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>




Tab items interaction with keyboard keys, like headers active navigation.


Default Value:



* true




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the allowKeyboardNavigation during initialization.                               $("#tab").ejTab({width:"300px",allowKeyboardNavigation: false }); &lt;/script&gt;  </code></pre>



#### collapsible<span class="type-signature type boolean">boolean</span>




Allow to collapsing the active item, while click on the active header.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the collapsible during initialization.                           $("#tab").ejTab({width:"300px",collapsible: true }); &lt;/script&gt;  </code></pre>



#### cssClass<span class="type-signature type string">string</span>




Set the root class for Tab theme. This cssClass API helps to use custom skinning option for Tab control.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the CSS class during initialization.                             $("#tab").ejTab({width:"300px",cssClass: "gradient-lime" }); &lt;/script&gt;  </code></pre>



#### disabledItemIndex<span class="type-signature type integerarray">IntegerArray</span>




Disables the given tab headers and content panels.


Default Value:



* []




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;   &lt;script type="text/javascript"&gt;         // Set the disabledItemIndex during initialization.                             $("#tab").ejTab({width:"300px",disabledItemIndex: [1,2] }); &lt;/script&gt;  </code></pre>



#### enableAnimation<span class="type-signature type boolean">boolean</span>




Specifies the animation behavior of the tab.


Default Value:



* true




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         //To set enableAnimation API value during initialization          $("#tab").ejTab({ enableAnimation: false});&lt;/script&gt;</code></pre>



#### enabled<span class="type-signature type boolean">boolean</span>




When this property is set to false, it disables the tab control.


Default Value:



* true




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the enabled during initialization.                               $("#tab").ejTab({width:"300px",enabled: false }); &lt;/script&gt;  </code></pre>



#### enabledItemIndex<span class="type-signature type integerarray">IntegerArray</span>




Enables the given tab headers and content panels.


Default Value:



* []




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;   &lt;script type="text/javascript"&gt;         // Set the enabledItemIndex during initialization.         $("#tab").ejTab({width:"300px",disabledItemIndex: [0,1,2] }); $("#tab").ejTab({width:"300px",enabledItemIndex: [0,1] }); &lt;/script&gt;  </code></pre>



#### enablePersistence<span class="type-signature type boolean">boolean</span>




Save current model value to browser cookies for state maintains. While refresh the Tab control page the model value apply from browser cookies.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt; &lt;script type="text/javascript"&gt;         // Set the enablePersistence during initialization.                             $("#tab").ejTab({width:"300px",enablePersistence: false }); &lt;/script&gt;  </code></pre>



#### enableRTL<span class="type-signature type boolean">boolean</span>




Display Right to Left direction for headers and panels text.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the rtl during initialization.                           $("#tab").ejTab({width:"300px",enableRTL: true }); &lt;/script&gt;  </code></pre>



#### enableTabScroll<span class="type-signature type boolean">boolean</span>




Specify to enable scrolling for Tab header.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the enableTabScroll during initialization.                               $("#tab").ejTab({width:"300px",enableTabScroll: true }); &lt;/script&gt;  </code></pre>



#### events<span class="type-signature type string">string</span>




The event API to bind the action for active the tab items.


Default Value:



* "click"




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;     &lt;script type="text/javascript"&gt;         // Set the events during initialization.                                $("#tab").ejTab({width:"300px",events: "click" }); &lt;/script&gt;  </code></pre>



#### headerPosition<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>




Tab header display top,bottom,left or right .See <a href="global.html#Position">Position</a>


Default Value:



* "top"




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the headerPosition during initialization.                                $("#tab").ejTab({width:"500px",headerPosition: "left" }); &lt;/script&gt;  </code></pre>



#### headerSize<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>




Set the height of the tab header element. Default this property value is null, so height take content height.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the height during initialization.                                $("#tab").ejTab({headerSize: "100px" }); &lt;/script&gt;  </code></pre>



#### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>




Height set the outer panel element. Default this property value is null, so height take content height.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the height during initialization.                                $("#tab").ejTab({width:"300px",height: "320px" }); &lt;/script&gt;  </code></pre>



#### heightAdjustMode<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>




Adjust the content panel height for given option (content, auto and fill), by default panels height adjust based on the content.See <a href="global.html#HeightAdjustMode">HeightAdjustMode</a>


Default Value:



* "content"




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt; &lt;script type="text/javascript"&gt;         // Set the heightAdjustMode  during initialization.                             $("#tab").ejTab({width:"300px",heightAdjustMode : ej.Tab.HeightAdjustMode.Content }); &lt;/script&gt;  </code></pre>



#### idPrefix<span class="type-signature type string">string</span>




The idPrefix property appends the give string on runtime added tab item id&rsquo;s.


Default Value:



* "ej-tab-"




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the idPrefix during initialization.                              $("#tab").ejTab({width:"300px",idPrefix: "ej-tab-" }); &lt;/script&gt;  </code></pre>



#### selectedItemIndex<span class="type-signature type number">number</span>




Tab header to active for given index value.


Default Value:



* 0




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the selectedItemIndex  during initialization.                            $("#tab").ejTab({width:"300px",selectedItemIndex : 1 }); &lt;/script&gt;  </code></pre>



#### showCloseButton<span class="type-signature type boolean">boolean</span>




Display the close button for each tab items. While click on the close icon particular tab item removed.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;   &lt;script type="text/javascript"&gt;         // Set the showCloseButton during initialization.                               $("#tab").ejTab({width:"500px",showCloseButton: true }); &lt;/script&gt;  </code></pre>



#### showReloadIcon<span class="type-signature type boolean">boolean</span>




Display the Reload button for each tab items.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the showReloadIcon during initialization.                                $("#tab").ejTab({width:"500px",showReloadIcon: true }); &lt;/script&gt;  </code></pre>



#### showRoundedCorner<span class="type-signature type boolean">boolean</span>




Tab panels and headers to display the rounded corner style.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the roundedCorner during initialization.                                 $("#tab").ejTab({width:"300px",showRoundedCorner: false }); &lt;/script&gt;  </code></pre>



#### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>




Set the width for outer panel element, if not it&rsquo;s take parent width.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         // Set the width during initialization.                                 $("#tab").ejTab({width: "600px" }); &lt;/script&gt;  </code></pre>


### Methods




#### addItem<span class="signature">(url, displayLabel, index)</span>




Add new tab items with given name, url and given index position, if index null it&rsquo;s add last item.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>url</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">URL name / tab id.</td></tr><tr><td class="name"><code>displayLabel</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">Tab Display name.</td></tr><tr><td class="name"><code>index</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">Index position to placed , this is optional.</td></tr></tbody></table>


##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;&lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;  &lt;div id="new"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;             &lt;/div&gt;&lt;script type="text/javascript"&gt;         //initialize the tab object$("#tab").ejTab({width:"400px"});        var tabObj = $("#tab").data("ejTab");        // Add new tab items with given list        tabObj.addItem("#new","New Item",3);&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt; &lt;div id="new"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;  $("#tab").ejTab({width:"400px"});       $("#tab").ejTab("addItem","#new","New Item",3); &lt;/script&gt;  </code></pre>



#### disable<span class="signature">()</span>




To disable the tab control.



##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;  $("#tab").ejTab({width:"300px"});      //initialize the tab objectvar tabObj = $("#tab").data("ejTab");        // disable the tab control        tabObj.disable();&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;  $("#tab").ejTab({width:"300px"});       $("#tab").ejTab("disable");&lt;/script&gt;  </code></pre>



#### enable<span class="signature">()</span>




To enable the tab control.



##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;   $("#tab").ejTab({width:"300px"});      //initialize the tab object        var tabObj = $("#tab").data("ejTab");        // enable the tab control        tabObj.enable();&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;     $("#tab").ejTab({width:"300px"});    $("#tab").ejTab("enable");&lt;/script&gt;  </code></pre>



#### getItemsCount<span class="signature">()</span>




This function get the number of tab rendered



##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;    $("#tab").ejTab({width:"300px"});     //initialize the tab object        var tabObj = $("#tab").data("ejTab");        // get the number of tab rendered        tabObj.getItemsCount();&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;    $("#tab").ejTab({width:"300px"});     $("#tab").ejTab("getItemsCount");&lt;/script&gt;  </code></pre>



#### hide<span class="signature">()</span>




This function hides the tab control.



##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;   $("#tab").ejTab({width:"300px"});      //initialize the tab object        var tabObj = $("#tab").data("ejTab");        // To hide the tab control..        tabObj.hide();&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;   $("#tab").ejTab({width:"300px"});      $("#tab").ejTab("hide"); &lt;/script&gt;  </code></pre>



#### removeItem<span class="signature">(index)</span>




Remove the given index tab item.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>index</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">index of tab item.</td></tr></tbody></table>


##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;    $("#tab").ejTab({width:"300px"});     //initialize the tab object        var tabObj = $("#tab").data("ejTab");        // Remove the given index tab item.        tabObj.removeItem(1);&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt; $("#tab").ejTab({width:"300px"});        $("#tab").ejTab("removeItem",1); &lt;/script&gt;  </code></pre>



#### show<span class="signature">()</span>




This function is to show the tab control.



##### Examples
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt; $("#tab").ejTab({width:"300px"});        //initialize the tab object        var tabObj = $("#tab").data("ejTab");        // To show the tab control.        tabObj.show();&lt;/script&gt;  </code></pre><pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;    $("#tab").ejTab({width:"300px"});     $("#tab").ejTab("show"); &lt;/script&gt;  </code></pre>


### Events




#### active




Triggered after a tab item activated.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   itemActive: function (args) {}});      &lt;/script&gt;  </code></pre>



#### ajaxBeforeLoad




Triggered before ajax content load action.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width:"300px",   ajaxBeforeLoad: function (args) {}});      &lt;/script&gt;  </code></pre>



#### ajaxError




Triggered after a tab item activated.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   ajaxError: function (args) {}});      &lt;/script&gt;  </code></pre>



#### ajaxLoad




Triggered after ajax content load action.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>url</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the url</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width:"300px",   ajaxLoad: function (args) {}});      &lt;/script&gt;  </code></pre>



#### ajaxSuccess




Triggered after a tab item activated.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   ajaxSuccess: function (args) {}});      &lt;/script&gt;  </code></pre>



#### beforeActive




Triggered before a tab item activated.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>prevActiveHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns previous active tab header.</td></tr><tr><td class="name"><code>prevActiveIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns previous active index.</td></tr><tr><td class="name"><code>activeHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns current active tab header .</td></tr><tr><td class="name"><code>activeIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current active index.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   beforeActive: function (args) {}});      &lt;/script&gt;  </code></pre>



#### beforeItemRemove




Triggered before a tab item remove.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>index</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current tab item index</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   beforeItemRemove: function (args) {}});      &lt;/script&gt;  </code></pre>



#### create




Triggered before a tab item Create.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>deleteIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current tab item index</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   create: function (args) {}});      &lt;/script&gt;  </code></pre>



#### destroy




Triggered before a tab item destroy.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>deleteIndex</code></td><td class="type"><span class="param-type">number</span></td><td class="description last">returns current tab item index</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   destroy: function (args) {}});      &lt;/script&gt;  </code></pre>



#### itemAdd




Triggered after new tab item add
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>tabHeader</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns new added tab header.</td></tr><tr><td class="name"><code>tabContent</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns new added tab content panel.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   itemAdd: function (args) {}});      &lt;/script&gt;  </code></pre>



#### itemRemove




Triggered after tab item removed.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the tab model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>removedTab</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns removed tab header.</td></tr><tr><td class="name"><code>removedPanel</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns removed tab content panel.</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;div id="tab"&gt;                  &lt;ul&gt;                      &lt;li&gt;&lt;a href="#javaScript"&gt;JavaScript&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#cSharp"&gt;C Sharp (C#)&lt;/a&gt;&lt;/li&gt;                      &lt;li&gt;&lt;a href="#vb"&gt;VB.Net&lt;/a&gt;&lt;/li&gt;                  &lt;/ul&gt;                  &lt;div id="javaScript"&gt; JavaScript (JS) is an interpreted computer programming language. It was originally implemented as part of web browsers so that client-side scripts could interact with the user, control the browser, communicate asynchronously, and alter the document content that was displayed. More recently, however, it has become common in both game development and the creation of desktop applications.                  &lt;/div&gt;                  &lt;div id="cSharp"&gt; C# is intended to be a simple, modern, general-purpose, object-oriented programming language. Its development team is led by Anders Hejlsberg. The most recent version is C# 5.0, which was released on August 15, 2012.                  &lt;/div&gt;                  &lt;div id="vb"&gt; The command-line compiler, VBC.EXE, is installed as part of the freeware .NET Framework SDK. Mono also includes a command-line VB.NET compiler. The most recent version is VB 2012, which was released on August 15, 2012.                  &lt;/div&gt;              &lt;/div&gt;&lt;script type="text/javascript"&gt;         $("#tab").ejTab({width: "300px",   itemRemove: function (args) {}});      &lt;/script&gt;  </code></pre>


