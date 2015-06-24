---
layout: post
title: ejDialog
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Dialog control.





## $(element).ejDialog<span class="signature">(options)</span>



<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>options</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">settings for Dialog.</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>&lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }});  &lt;/script&gt;</code></pre>



## Requires


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.dialog.js

* module:ej.scroller.js

* module:ej.draggable.js


## Members




### actionButtons<span class="type-signature type stringarray">StringArray</span>




Gives dialog window rounded corners.


Default Value:
{:.param}



* [&ldquo;close&rdquo;]




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//iconAction on initialization.           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },actionButtons: ["close","collapsible","pin"]});&lt;/script&gt;</code></pre>



### ajaxSettings<span class="type-signature type object">object</span>




Specifies the ajaxSettings option to load the content to the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;     &lt;/div&gt;&lt;script&gt;//loadUrl on initialization.             $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax",contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html", ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true }  });&lt;/script&gt;</code></pre>



### ajaxSettings.async<span class="type-signature type boolean">Boolean</span>




It specifies, whether to enable or disable asynchronous request.






### ajaxSettings.cache<span class="type-signature type boolean">Boolean</span>




It specifies the page will be cached in the web browser.






### ajaxSettings.contentType<span class="type-signature type string">String</span>




It specifies the type of data is send in the query string.






### ajaxSettings.data<span class="type-signature type object">Object</span>




It specifies the data as an object, will be passed in the query string.






### ajaxSettings.dataType<span class="type-signature type string">String</span>




It specifies the type of data that you're expecting back from the response.






### ajaxSettings.type<span class="type-signature type string">String</span>




It specifies the HTTP request type.






### allowDraggable<span class="type-signature type boolean">Boolean</span>




To enable the dialog window to dragged within the page.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable draggable during initialization          $("#dialog").ejDialog({position: { X: 300, Y: 10 }, allowDraggable: false});                                    &lt;/script&gt;</code></pre>



### allowKeyboardNavigation<span class="type-signature type boolean">Boolean</span>




Enables users to navigate right, left, up, and down in the control with keyboard action


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable  allowKeyboardNavigation on initialization.           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },allowKeyboardNavigation: true});&lt;/script&gt;</code></pre>



### closeIconTooltip<span class="type-signature type string">String</span>




Customizes the close button tooltip text.


Default Value:
{:.param}



* close




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//To set closeText API value during initialization          $("#dialog").ejDialog({position: { X: 300, Y: 10 },closeIconTooltip: "hide" });                         &lt;/script&gt;</code></pre>



### closeOnEscape<span class="type-signature type boolean">Boolean</span>




Allows the Dialog window to be closed by pressing the Esc key.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Enable closeOnEscape during initialization           $("#dialog").ejDialog({position: { X: 300, Y: 10 }, closeOnEscape: false});                             &lt;/script&gt;</code></pre>



### content<span class="type-signature type string">String</span>




Places the dialog in the given container.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); // Enable contentContainer on initialization.          $("#dialog").ejDialog({ position: { X: 300, Y: 10 },content: "#samplearea" });&lt;/script&gt;</code></pre>



### contentType<span class="type-signature type string">String</span>




To load the dialog content at run time, such as ajax, images, and iframe.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>&lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;  $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //Enable content on initialization.             $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax" });&lt;/script&gt;</code></pre>



### contentUrl<span class="type-signature type string">String</span>




Loads AJAX, image, and iframe content from a given location (URL).


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;     &lt;/div&gt;&lt;script&gt;//loadUrl on initialization.             $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax",contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html" });&lt;/script&gt;</code></pre>



### cssClass<span class="type-signature type string">String</span>




Set the root class for the Dialog control theme.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//cssClass on initialization.          $("#dialog").ejDialog({position: { X: 300, Y: 10 }, cssClass: "gradient-lime" });&lt;/script&gt;</code></pre>



### enableAnimation<span class="type-signature type boolean">boolean</span>




Specifies the animation behavior of the Dialog.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//To set enableAnimation API value during initialization          $("#dialog").ejDialog({ enableAnimation: false});&lt;/script&gt;</code></pre>



### enabled<span class="type-signature type boolean">Boolean</span>




Enables or disables the Dialog control.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set enabled on initialization.   $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enabled: true });&lt;/script&gt;</code></pre>



### enableModal<span class="type-signature type boolean">Boolean</span>




Allows the dialog window to be used as a modal form.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable modal during initialization              $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enableModal: true});&lt;/script&gt;</code></pre>



### enablePersistence<span class="type-signature type boolean">Boolean</span>




Saves the current model value to browser cookies for maintaining state.


Default Value:
{:.param}



* False




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable persist on initialization.  $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enablePersistence: true});&lt;/script&gt;</code></pre>



### enableResize<span class="type-signature type boolean">Boolean</span>




Allows the dialog to be resized above the minimum height and minimum width values.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Allows the dialog to be resized during initialization              $("#dialog").ejDialog({ position: { X: 300, Y: 10 },enableResize: false});&lt;/script&gt;</code></pre>



### enableRTL<span class="type-signature type boolean">Boolean</span>




Displays dialog content from right to left when enabled


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable rtl on initialization.           $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enableRTL: true});&lt;/script&gt;</code></pre>



### faviconCSS<span class="type-signature type string">String</span>




Custom icons for custom actions can be provided by using a CSS class.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //customIconCss on initialization.           ("#dialog").ejDialog({ position: { X: 300, Y: 10 }, faviconCSS  : "custom-icon" });&lt;/script&gt;</code></pre>



### height<span class="type-signature type string">String</span> <span class="type-signature type integer">integer</span>




Set the height for the dialog control.


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set Height during initialization          $("#dialog").ejDialog({position: { X: 300, Y: 10 }, height: 400 });                             &lt;/script&gt;</code></pre>



### isResponsive<span class="type-signature type boolean">Boolean</span>




Enables the window resizing.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable windowResizing on initialization.   $("#dialog").ejDialog({position: { X: 300, Y: 10 }, isResponsive: true });&lt;/script&gt;</code></pre>



### maxHeight<span class="type-signature type integer">Integer</span>




Set the maximum height for the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set maximum height during initialization            $("#dialog").ejDialog({position: { X: 300, Y: 10 }, maxHeight: 600 });                &lt;/script&gt;</code></pre>



### maxWidth<span class="type-signature type integer">Integer</span>




Set the maximum width for the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set maximum width during initialization             $("#dialog").ejDialog({ position: { X: 300, Y: 10 },maxWidth: 600 });&lt;/script&gt;</code></pre>



### minHeight<span class="type-signature type integer">Integer</span>




Set the minimum height for the dialog control.


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set minimum Height during initialization          $("#dialog").ejDialog({position: { X: 300, Y: 10 }, minHeight: 400 });                          &lt;/script&gt;</code></pre>



### minWidth<span class="type-signature type integer">Integer</span>




Set the minimum width for the dialog control.


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Set minimum Width during initialization           $("#dialog").ejDialog({position: { X: 300, Y: 10 }, minWidth: 400 });                  &lt;/script&gt;</code></pre>



### position<span class="type-signature type jsonobject">JSONobject</span>




Displays the dialog window at the given X and Y position. X: Dialog set the left position value. Y: Dialog set the top position value.


Default Value:
{:.param}



* Null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable position during initialization              $("#dialog").ejDialog({position: { X: 300, Y: 10 }});&lt;/script&gt;</code></pre>



### showHeader<span class="type-signature type boolean">Boolean</span>




Shows or hides the dialog header element.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Enable showHeader on initialization.             $("#dialog").ejDialog({ position: { X: 300, Y: 10 },showHeader: false});&lt;/script&gt;</code></pre>



### showOnInit<span class="type-signature type boolean">Boolean</span>




Enables the Dialog window to open automatically.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Enables the Dialog window to open automatically during initialization           $("#dialog").ejDialog({  position: { X: 500, Y: 26 },showOnInit:true});                                &lt;/script&gt;</code></pre>



### showRoundedCorner<span class="type-signature type boolean">Boolean</span>




Gives dialog window rounded corners.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Enable roundedCorner on initialization.           $("#dialog").ejDialog({position: { X: 300, Y: 10 }, showRoundedCorner: true});&lt;/script&gt;</code></pre>



### title<span class="type-signature type string">String</span>




Provides title text for the Dialog control.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Title on initialization.              $("#dialog").ejDialog({position: { X: 300, Y: 10 }, title: "Custom title" });&lt;/script&gt;</code></pre>



### width<span class="type-signature type string">String</span>




Sets the width of the Dialog control.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//Width on initialization.           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },width: 500 });&lt;/script&gt;</code></pre>



### zIndex<span class="type-signature type integer">Integer</span>




Sets the z-index value of the control for the Dialog control.


Default Value:
{:.param}



* 1000




Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//zIndex on initialization.           $("#dialog").ejDialog({position: { X: 300, Y: 10 }, zIndex: 500 });&lt;/script&gt;</code></pre>


## Methods




### close<span class="signature">()</span>




To close the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;  $("#dialog").ejDialog({position: { X: 300, Y: 10 }});//initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To close the dialog         dialogObj.close();&lt;/script&gt; </code></pre><pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;  $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To close the dialog $("#dialog").ejDialog("close");&lt;/script&gt; </code></pre>



### collapse<span class="signature">()</span>




To Collapse the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.collapse();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("collapse");&lt;/script&gt;</code></pre>



### destroy<span class="signature">()</span>




destroy the dialog widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; $("#dialog").ejDialog(); // Create Dialog control var dialogObj = $("#dialog").data("ejDialog"); //Initialize the Dialog object. dialogObj.destroy(); //Calls the destroy method of Dialog to destroy&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; //call destroy method $("#dialog").ejDialog("destroy"); &lt;/script&gt;</code></pre>



### expand<span class="signature">()</span>




To Expand the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.expand();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("expand");&lt;/script&gt;</code></pre>



### isOpened<span class="signature">()</span>




To get dialog control is opened or not



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");//To get the dialog status        dialogObj.isOpened();&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt; $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To get the dialog status$("#dialog").ejDialog("isOpened");&lt;/script&gt;</code></pre>



### maximize<span class="signature">()</span>




To Maximize the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.maximize();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("maximize");&lt;/script&gt;</code></pre>



### minimize<span class="signature">()</span>




To Minimize the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.minimize();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("minimize");&lt;/script&gt;</code></pre>



### open<span class="signature">()</span>




To open the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.open();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("open");&lt;/script&gt;</code></pre>



### pin<span class="signature">()</span>




To pin the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.pin();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("pin");&lt;/script&gt;</code></pre>



### restore<span class="signature">()</span>




To Restore the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.restore();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("restore");&lt;/script&gt;</code></pre>



### unpin<span class="signature">()</span>




To Unpin the dialog



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //initialize the dialog object        var dialogObj = $("#dialog").data("ejDialog");        //To open the dialog         dialogObj.unpin();&lt;/script&gt;</code></pre><pre class="prettyprint"><code>          &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// Create Dialog control $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); //To open the dialog $("#dialog").ejDialog("unpin");&lt;/script&gt;</code></pre>


## Events




### beforeOpen




Fires before dialog control is opened.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;// beforeOpen event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },  beforeOpen: function (args) {}});&lt;/script&gt;</code></pre>



### ajaxError




Fires after an AJAX content loading error
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.url</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the content location</td></tr><tr><td class="name"><code>argument.data</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the content text</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//           ajaxError event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },            ajaxError: function (args) {}});&lt;/script&gt;</code></pre>



### ajaxSuccess




Fires when AJAX content is loaded successfully
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.url</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the content location</td></tr><tr><td class="name"><code>argument.data</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the content text</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//          ajaxSuccess event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },           ajaxSuccess: function (args) {}});&lt;/script&gt;</code></pre>



### beforeClose




Fires before dialog control is closed.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the close icon click event args</td></tr><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//beforeClose event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 }, beforeClose: function (args) {}});&lt;/script&gt;</code></pre>



### Close




Fires after dialog control is closed.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the close icon click event args</td></tr><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//beforeClose event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 }, Close: function (args) {}});&lt;/script&gt;</code></pre>



### contentLoad




Fires on AJAX content, iframe, or image load actions
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.url</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the content location</td></tr><tr><td class="name"><code>argument.contentType</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the content type</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//         load event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },          contentLoad: function (args) {}});&lt;/script&gt;</code></pre>



### create




Fires after Create dialog successfully
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//           Create event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },            create: function (args) {}});&lt;/script&gt;</code></pre>



### destroy




Fires after Destroy event successfully
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//           destroy event for dialog $("#dialog").ejDialog({            destroy: function (args) {}});&lt;/script&gt;</code></pre>



### drag




Fires when dialog control is dragged.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse move event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//   drag event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },    drag: function (args) {}});&lt;/script&gt;</code></pre>



### dragStart




Fires when the dialog is starting to be dragged
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse down event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//    dragStart event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },     dragStart: function (args) {}});&lt;/script&gt;</code></pre>



### dragStop




Fires after the dialog dragging stops
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse down event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//     dragStop event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },      dragStop: function (args) {}});&lt;/script&gt;</code></pre>



### open




Fires after dialog control is opened.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//  open event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },   open: function (args) {}});&lt;/script&gt;</code></pre>



### resize




Fires on dialog resize action
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse move event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//      resize event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },       resize: function (args) {}});&lt;/script&gt;</code></pre>



### resizeStart




Fires on dialog resize start action
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse down event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//       resizeStart event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },        resizeStart: function (args) {}});&lt;/script&gt;</code></pre>



### resizeStop




Fires on dialog resize stop action
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">returns the cancel option value</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the dialog model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>argument.event</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the mouse leave event args</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="dialog" title="WPF"&gt;Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.&lt;/div&gt;&lt;script&gt;//        resizeStop event for dialog $("#dialog").ejDialog({        position: { X: 300, Y: 10 },         resizeStop: function (args) {}});&lt;/script&gt;</code></pre>


