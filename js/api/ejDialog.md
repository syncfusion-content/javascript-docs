---
layout: post
title: ejDialog
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Dialog control.





$(element).ejDialog<span class="signature">(options)</span>




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
<td class="description last">settings for Dialog.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }});  
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.dialog.js

* module:ej.scroller.js

* module:ej.draggable.js


## Members




### actionButtons<span class="type-signature type stringarray">StringArray</span>
{:#members:actionbuttons}




Gives dialog window rounded corners.


Default Value:
{:.param}



* [&ldquo;close&rdquo;]




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//iconAction on initialization.  
         $("#dialog").ejDialog({ position: { X: 300, Y: 10 },actionButtons: ["close","collapsible","pin"]});
</script>{% endhighlight %}




### ajaxSettings<span class="type-signature type object">object</span>
{:#members:ajaxsettings}




Specifies the ajaxSettings option to load the content to the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">     
</div>
<script>
//loadUrl on initialization.  
           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax",contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html", ajaxSettings: { type: 'GET', cache: false, data: {}, dataType: "html", contentType: "html", async: true }  });
</script>{% endhighlight %}




### ajaxSettings.async<span class="type-signature type boolean">Boolean</span>
{:#members:ajaxsettings-async}




It specifies, whether to enable or disable asynchronous request.






### ajaxSettings.cache<span class="type-signature type boolean">Boolean</span>
{:#members:ajaxsettings-cache}




It specifies the page will be cached in the web browser.






### ajaxSettings.contentType<span class="type-signature type string">String</span>
{:#members:ajaxsettings-contenttype}




It specifies the type of data is send in the query string.






### ajaxSettings.data<span class="type-signature type object">Object</span>
{:#members:ajaxsettings-data}




It specifies the data as an object, will be passed in the query string.






### ajaxSettings.dataType<span class="type-signature type string">String</span>
{:#members:ajaxsettings-datatype}




It specifies the type of data that you're expecting back from the response.






### ajaxSettings.type<span class="type-signature type string">String</span>
{:#members:ajaxsettings-type}




It specifies the HTTP request type.






### allowDraggable<span class="type-signature type boolean">Boolean</span>
{:#members:allowdraggable}




To enable the dialog window to dragged within the page.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable draggable during initialization  
        $("#dialog").ejDialog({position: { X: 300, Y: 10 }, allowDraggable: false});                                    
</script>{% endhighlight %}




### allowKeyboardNavigation<span class="type-signature type boolean">Boolean</span>
{:#members:allowkeyboardnavigation}




Enables users to navigate right, left, up, and down in the control with keyboard action


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable  allowKeyboardNavigation on initialization.  
         $("#dialog").ejDialog({ position: { X: 300, Y: 10 },allowKeyboardNavigation: true});
</script>{% endhighlight %}




### closeIconTooltip<span class="type-signature type string">String</span>
{:#members:closeicontooltip}




Customizes the close button tooltip text.


Default Value:
{:.param}



* close




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//To set closeText API value during initialization  
        $("#dialog").ejDialog({position: { X: 300, Y: 10 },closeIconTooltip: "hide" });                         
</script>{% endhighlight %}




### closeOnEscape<span class="type-signature type boolean">Boolean</span>
{:#members:closeonescape}




Allows the Dialog window to be closed by pressing the Esc key.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Enable closeOnEscape during initialization  
         $("#dialog").ejDialog({position: { X: 300, Y: 10 }, closeOnEscape: false});                             
</script>{% endhighlight %}




### content<span class="type-signature type string">String</span>
{:#members:content}




Places the dialog in the given container.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
// Enable contentContainer on initialization.  
        $("#dialog").ejDialog({ position: { X: 300, Y: 10 },content: "#samplearea" });
</script>{% endhighlight %}




### contentType<span class="type-signature type string">String</span>
{:#members:contenttype}




To load the dialog content at run time, such as ajax, images, and iframe.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script> 
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//Enable content on initialization.  
           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax" });
</script>{% endhighlight %}




### contentUrl<span class="type-signature type string">String</span>
{:#members:contenturl}




Loads AJAX, image, and iframe content from a given location (URL).


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">     
</div>
<script>
//loadUrl on initialization.  
           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },contentType: "ajax",contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html" });
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}




Set the root class for the Dialog control theme.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//cssClass on initialization.  
        $("#dialog").ejDialog({position: { X: 300, Y: 10 }, cssClass: "gradient-lime" });
</script>{% endhighlight %}




### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}




Specifies the animation behavior of the Dialog.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//To set enableAnimation API value during initialization  
        $("#dialog").ejDialog({ enableAnimation: false});
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}




Enables or disables the Dialog control.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set enabled on initialization.  
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enabled: true });
</script>{% endhighlight %}




### enableModal<span class="type-signature type boolean">Boolean</span>
{:#members:enablemodal}




Allows the dialog window to be used as a modal form.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable modal during initialization  
            $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enableModal: true});
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}




Saves the current model value to browser cookies for maintaining state.


Default Value:
{:.param}



* False




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable persist on initialization.  
$("#dialog").ejDialog({position: { X: 300, Y: 10 }, enablePersistence: true});
</script>{% endhighlight %}




### enableResize<span class="type-signature type boolean">Boolean</span>
{:#members:enableresize}




Allows the dialog to be resized above the minimum height and minimum width values.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Allows the dialog to be resized during initialization  
            $("#dialog").ejDialog({ position: { X: 300, Y: 10 },enableResize: false});
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}




Displays dialog content from right to left when enabled


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable rtl on initialization.  
         $("#dialog").ejDialog({position: { X: 300, Y: 10 }, enableRTL: true});
</script>{% endhighlight %}




### faviconCSS<span class="type-signature type string">String</span>
{:#members:faviconcss}




Custom icons for custom actions can be provided by using a CSS class.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//customIconCss on initialization.  
         ("#dialog").ejDialog({ position: { X: 300, Y: 10 }, faviconCSS  : "custom-icon" });
</script>{% endhighlight %}




### height<span class="type-signature type string">String</span> <span class="type-signature type integer">integer</span>
{:#members:height}




Set the height for the dialog control.


Default Value:
{:.param}



* auto




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set Height during initialization  
        $("#dialog").ejDialog({position: { X: 300, Y: 10 }, height: 400 });                             
</script>{% endhighlight %}




### isResponsive<span class="type-signature type boolean">Boolean</span>
{:#members:isresponsive}




Enables the window resizing.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable windowResizing on initialization.  
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }, isResponsive: true });
</script>{% endhighlight %}




### maxHeight<span class="type-signature type integer">Integer</span>
{:#members:maxheight}




Set the maximum height for the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set maximum height during initialization  
          $("#dialog").ejDialog({position: { X: 300, Y: 10 }, maxHeight: 600 });                
</script>{% endhighlight %}




### maxWidth<span class="type-signature type integer">Integer</span>
{:#members:maxwidth}




Set the maximum width for the dialog control.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set maximum width during initialization  
           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },maxWidth: 600 });
</script>{% endhighlight %}




### minHeight<span class="type-signature type integer">Integer</span>
{:#members:minheight}




Set the minimum height for the dialog control.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set minimum Height during initialization  
        $("#dialog").ejDialog({position: { X: 300, Y: 10 }, minHeight: 400 });                          
</script>{% endhighlight %}




### minWidth<span class="type-signature type integer">Integer</span>
{:#members:minwidth}




Set the minimum width for the dialog control.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Set minimum Width during initialization  
         $("#dialog").ejDialog({position: { X: 300, Y: 10 }, minWidth: 400 });                  
</script>{% endhighlight %}




### position<span class="type-signature type jsonobject">JSONobject</span>
{:#members:position}




Displays the dialog window at the given X and Y position. X: Dialog set the left position value. Y: Dialog set the top position value.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable position during initialization  
            $("#dialog").ejDialog({position: { X: 300, Y: 10 }});
</script>{% endhighlight %}




### showHeader<span class="type-signature type boolean">Boolean</span>
{:#members:showheader}




Shows or hides the dialog header element.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Enable showHeader on initialization.  
           $("#dialog").ejDialog({ position: { X: 300, Y: 10 },showHeader: false});
</script>{% endhighlight %}




### showOnInit<span class="type-signature type boolean">Boolean</span>
{:#members:showoninit}




Enables the Dialog window to open automatically.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Enables the Dialog window to open automatically during initialization  
         $("#dialog").ejDialog({  position: { X: 500, Y: 26 },showOnInit:true});                                
</script>{% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">Boolean</span>
{:#members:showroundedcorner}




Gives dialog window rounded corners.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Enable roundedCorner on initialization.  
         $("#dialog").ejDialog({position: { X: 300, Y: 10 }, showRoundedCorner: true});
</script>{% endhighlight %}




### title<span class="type-signature type string">String</span>
{:#members:title}




Provides title text for the Dialog control.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Title on initialization.  
            $("#dialog").ejDialog({position: { X: 300, Y: 10 }, title: "Custom title" });
</script>{% endhighlight %}




### width<span class="type-signature type string">String</span>
{:#members:width}




Sets the width of the Dialog control.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//Width on initialization.  
         $("#dialog").ejDialog({ position: { X: 300, Y: 10 },width: 500 });
</script>{% endhighlight %}




### zIndex<span class="type-signature type integer">Integer</span>
{:#members:zindex}




Sets the z-index value of the control for the Dialog control.


Default Value:
{:.param}



* 1000




Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//zIndex on initialization.  
         $("#dialog").ejDialog({position: { X: 300, Y: 10 }, zIndex: 500 });
</script>{% endhighlight %}



## Methods




### close<span class="signature">()</span>
{:#methods:close}




To close the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script> 
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }});
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To close the dialog 
        dialogObj.close();
</script> {% endhighlight %}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script> 
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To close the dialog 
$("#dialog").ejDialog("close");
</script> {% endhighlight %}




### collapse<span class="signature">()</span>
{:#methods:collapse}




To Collapse the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.collapse();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("collapse");
</script>{% endhighlight %}




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the dialog widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 $("#dialog").ejDialog(); 
// Create Dialog control
 var dialogObj = $("#dialog").data("ejDialog"); //Initialize the Dialog object.
 dialogObj.destroy(); //Calls the destroy method of Dialog to destroy
</script>{% endhighlight %}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 //call destroy method
 $("#dialog").ejDialog("destroy"); 
</script>{% endhighlight %}




### expand<span class="signature">()</span>
{:#methods:expand}




To Expand the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.expand();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("expand");
</script>{% endhighlight %}




### isOpened<span class="signature">()</span>
{:#methods:isopened}




To get dialog control is opened or not



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
//To get the dialog status
        dialogObj.isOpened();
</script>{% endhighlight %}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To get the dialog status
$("#dialog").ejDialog("isOpened");
</script>{% endhighlight %}




### maximize<span class="signature">()</span>
{:#methods:maximize}




To Maximize the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.maximize();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("maximize");
</script>{% endhighlight %}




### minimize<span class="signature">()</span>
{:#methods:minimize}




To Minimize the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.minimize();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("minimize");
</script>{% endhighlight %}




### open<span class="signature">()</span>
{:#methods:open}




To open the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.open();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("open");
</script>{% endhighlight %}




### pin<span class="signature">()</span>
{:#methods:pin}




To pin the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.pin();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("pin");
</script>{% endhighlight %}




### restore<span class="signature">()</span>
{:#methods:restore}




To Restore the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.restore();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("restore");
</script>{% endhighlight %}




### unpin<span class="signature">()</span>
{:#methods:unpin}




To Unpin the dialog



Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//initialize the dialog object
        var dialogObj = $("#dialog").data("ejDialog");
        //To open the dialog 
        dialogObj.unpin();
</script>{% endhighlight %}


{% highlight html %}
 
         <div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// Create Dialog control
 $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 
//To open the dialog 
$("#dialog").ejDialog("unpin");
</script>{% endhighlight %}



## Events




### beforeOpen
{:#events:beforeopen}




Fires before dialog control is opened.

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
// beforeOpen event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
  beforeOpen: function (args) {}
});
</script>{% endhighlight %}




### ajaxError
{:#events:ajaxerror}




Fires after an AJAX content loading error

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the content location</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the content text</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//           ajaxError event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
            ajaxError: function (args) {}
});
</script>{% endhighlight %}




### ajaxSuccess
{:#events:ajaxsuccess}




Fires when AJAX content is loaded successfully

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the content location</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the content text</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//          ajaxSuccess event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
           ajaxSuccess: function (args) {}
});
</script>{% endhighlight %}




### beforeClose
{:#events:beforeclose}




Fires before dialog control is closed.

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
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the close icon click event args</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//beforeClose event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
 beforeClose: function (args) {}
});
</script>{% endhighlight %}




### Close
{:#events:close}




Fires after dialog control is closed.

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
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the close icon click event args</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//beforeClose event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
 Close: function (args) {}
});
</script>{% endhighlight %}




### contentLoad
{:#events:contentload}




Fires on AJAX content, iframe, or image load actions

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the content location</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.contentType{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the content type</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//         load event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
          contentLoad: function (args) {}
});
</script>{% endhighlight %}




### create
{:#events:create}




Fires after Create dialog successfully

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//           Create event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
            create: function (args) {}
});
</script>{% endhighlight %}




### destroy
{:#events:destroy}




Fires after Destroy event successfully

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//           destroy event for dialog
 $("#dialog").ejDialog({
            destroy: function (args) {}
});
</script>{% endhighlight %}




### drag
{:#events:drag}




Fires when dialog control is dragged.

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse move event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//   drag event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
    drag: function (args) {}
});
</script>{% endhighlight %}




### dragStart
{:#events:dragstart}




Fires when the dialog is starting to be dragged

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse down event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//    dragStart event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
     dragStart: function (args) {}
});
</script>{% endhighlight %}




### dragStop
{:#events:dragstop}




Fires after the dialog dragging stops

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse down event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//     dragStop event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
      dragStop: function (args) {}
});
</script>{% endhighlight %}




### open
{:#events:open}




Fires after dialog control is opened.

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
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
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//  open event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
   open: function (args) {}
});
</script>{% endhighlight %}




### resize
{:#events:resize}




Fires on dialog resize action

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse move event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//      resize event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
       resize: function (args) {}
});
</script>{% endhighlight %}




### resizeStart
{:#events:resizestart}




Fires on dialog resize start action

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse down event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//       resizeStart event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
        resizeStart: function (args) {}
});
</script>{% endhighlight %}




### resizeStop
{:#events:resizestop}




Fires on dialog resize stop action

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
<td class="description last">returns the cancel option value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the dialog model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the mouse leave event args</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<div id="dialog" title="WPF">
Developed by Microsoft, the Windows Presentation Foundation (or WPF) is a computer-software graphical subsystem for rendering user interfaces in Windows-based applications. WPF, previously known as "Avalon", was initially released as part of .NET Framework 3.0. Rather than relying on the older GDI subsystem, WPF uses DirectX. WPF attempts to provide a consistent programming model for building applications and separates the user interface from business logic. It resembles similar XML-oriented object models, such as those implemented in XUL and SVG.
</div>
<script>
//        resizeStop event for dialog
 $("#dialog").ejDialog({
        position: { X: 300, Y: 10 },
         resizeStop: function (args) {}
});
</script>{% endhighlight %}



