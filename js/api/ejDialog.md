---
layout: post
title: ejDialog
documentation: API
platform: js
metaname: 
metacontent: 
---

## Custom Design for Html Dialog widget.
$(element).ejDialog<span class="signature">(options)</span>

<table>
<tr>
<th>
Name<br/><br/></th><th>
Type<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
options<br/><br/></td><td>
object<br/><br/></td><td>
Settings for Dialog.<br/><br/></td></tr>
</table>

Example
{:.example}

{% highlight js %}
    
    // Create the Dialog widget

    $("#dialog").ejDialog(); 
    
{% endhighlight %}

Requires
{:.require}

* module:jQuery
* module:jquery.easing.1.3.js
* module:ej.core.js
* module:ej.dialog.js
* module:ej.scroller.js
* module:ej.button.js
* module:ej.draggable.js

##Members


### actionButtons<span class="type-signature type stringarray">StringArray<span>
{:#members:actionbuttons}

Adds action buttons like close, minimize, pin, maximize in the dialog header.

Default Value:
{:.param}
[&ldquo;close&rdquo;]

Example 
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({actionButtons: ["close","collapsible","pin"]}); 
    
 {% endhighlight  %}

### allowDraggable<span class="type-signature type object">Boolean
{:#members:allowdraggable}

Enables or disables draggable.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight js %}

     $("#dialog").ejDialog({allowDraggable: false});
         
{% endhighlight  %}

### allowKeyboardNavigation<span class="type-signature type boolean">Boolean</span>
{:#members:allowkeyboardnavigation}

Enables or disables keyboard interaction.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({allowKeyboardNavigation: true}); 

{% endhighlight  %}

### animation<span class="type-signature type JSONobject">JSONobject</span>
{:#members:animation}

Customizes the Dialog widget animations. The Dialog widget can be animated while opening and closing the dialog. In order to customize animation effects, you need to set “[enableAnimation](http://docs.syncfusion.com/js/api/ejdialog#members:enableanimation)” as true. It contains the following sub properties.

<table>
<tr>
<th>
Name<br/><br/></th><th>
Type<br/><br/></th><th>
Default<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
show.effect<br/><br/></td><td>
String<br/><br/></td><td>
fade<br/><br/></td><td>
The animation effect when the dialog is opened. The possible values are fade and slide.<br/><br/></td></tr>
<tr>
<td>
show.duration<br/><br/></td><td>
integer <br/><br/></td><td>
400<br/><br/></td><td>
The duration for the animation effect when the dialog is opened.<br/><br/></td></tr>
<tr>
<td>
hide.effect<br/><br/></td><td>
String<br/><br/></td><td>
fade<br/><br/></td><td>
The animation effect when the dialog is closed. The possible values are fade and slide.<br/><br/></td></tr>
<tr>
<td>
hide.duration<br/><br/></td><td>
integer<br/><br/></td><td>
400<br/><br/></td><td>
The duration for the animation effect when the dialog is closed.<br/><br/></td></tr>
</table>

Example
{:.example}

{% highlight js %}

        $("#dialog").ejDialog({
        
        enableAnimation: true,
        
        animation: {
        
        //animation settings while opening the dialog
        
        show: {
        
        effect: "slide",
        
        duration: 500
        
        },
        
        //animation settings while closing the dialog
        
        hide: {
        
        effect: "fade",
        
        duration: 500
        
        }
        
        }
        
        });   
              
{% endhighlight  %}

### closeIconTooltip<span class="type-signature type string">String</span>
{:#members:closeicontooltip}

The tooltip text for the dialog close button.

Default Value:
{:.param}
close

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({closeIconTooltip: "close" }); 

{% endhighlight  %}

### closeOnEscape<span class="type-signature type boolean">Boolean</span>
{:#members:closeonescape}

Closes the dialog widget on pressing the <kbd>ESC</kbd> key when it is set to true.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({closeOnEscape: false}); 
    
{% endhighlight  %}

### content[Deprecated]<span class="type-signature type string">String</span>
{:#members:content}

The selector for the container element. If this property is set, the dialog will be displayed (positioned) based on its container.

N>Since it is deprecated we suggest to use the API “[target](#methods:isopen)”.

Default Value: 
{:.param}
 null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({content: "#samplearea" }); 

{% endhighlight  %}

### contentType<span class="type-signature type string">String</span>
{:#members:contenttype}

The content type to load the dialog content at run time. The possible values are null, ajax, iframe and image. When it is null (default value), the content inside dialog element will be displayed as content and when it is not null, the content will be loaded from the URL specified in the [contentUrl](http://docs.syncfusion.com/js/api/ejdialog#members:contenturl) property.

Default Value:
{:.param}

 null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({contentType: "ajax" }); 

{% endhighlight %}

### contentUrl<span class="type-signature type string">String</span>
{:#members:contenturl}

The URL to load the dialog content (such as AJAX, image, and iframe). In order to load content from URL, you need to set [contentType](http://docs.syncfusion.com/js/api/ejdialog#members:contenttype) as ‘ajax’ or ‘iframe’ or ‘image’.

Default Value:
{:.param}
null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({contentType: "ajax",

    contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html" }); 

{% endhighlight  %}

### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}

The root class for the Dialog widget to customize the existing theme.

Default Value:
{:.param}
 ””

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({ cssClass: "gradient-lime" }); 
    
{% endhighlight  %}


### enableAnimation<span class="type-signature type boolean">Boolean</span>
{:#members:enableanimation}

Enable or disables animation when the dialog is opened or closed.

Default Value:
{:.param} 
 true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({ enableAnimation: false}); 

{% endhighlight  %}

### enabled<span class="type-signature type boolean">Boolean</span>
{:#members:enabled}

Enables or disables the Dialog widget.

Default Value: 
{:.param}
 true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({ enabled: true }); 

{% endhighlight  %}

### enableModal<span class="type-signature type boolean">Boolean</span>
{:#members:enablemodal}

Enable or disables modal dialog. The [modal dialog](https://en.wikipedia.org/wiki/Modal_window#) acts like a child window that is displayed on top of the main window/screen and disables the main window interaction until it is closed.

Default Value:
{:.param}
 false

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({enableModal: true}); 

{% endhighlight  %}

### enablePersistence<span class="type-signature type boolean">Boolean</span>
{:#members:enablepersistence}

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true.

N>[Local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is supported only in Html5 supported browsers.If the browsers don’t have support for local storage,browser cookies will be used to maintain the state.

Default Value:

{:.param}
false

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({enablePersistence: true}); 

{% endhighlight  %}

### enableResize<span class="type-signature type boolean">Boolean</span>
{:#members:enableResize}

Allows the dialog to be resized. The dialog cannot be resized less than the minimum height and minimum width values.

Default Value: 
{:.param}
 true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({enableResize: false}); 

{% endhighlight  %}

### enableRTL<span class="type-signature type boolean">Boolean</span>
{:#members:enablertl}

Displays dialog content from right to left when set to true.

Default Value: 
{:.param}
false

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({enableRTL: true}); 

{% endhighlight  %}

### faviconCSS<span class="type-signature type string">String</span>
{:#members:faviconcss}

The CSS class name to display the favicon in the dialog header. In order to display fav icon, you need to [showHeader](http://docs.syncfusion.com/js/api/ejdialog#members:showheader) as true since the favicon will be displayed in the dialog header.

Default Value: 
{:.param}
 null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({faviconCSS : "custom-icon" }); 

{% endhighlight  %}

### height<span class="type-signature type string">String</span> <span class="type-signature type integer">Integer</span> 
{:#members:height}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type. The unit of integer type value is “px”.

Default Value:
{:.param}
auto

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({height: 400 }); 

{% endhighlight  %}

### isResponsive<span class="type-signature type boolean">Boolean</span> 
{:#members:isresponsive}

Enable or disables responsive behavior.

N>Once the dialog is resized or dragged,then the responsive behavior won’t work.

Default Value:
{:.param}
false

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({isResponsive: true }); 

{% endhighlight  %}

### maxHeight<span class="type-signature type integer">Integer</span> 
{:#members:maxheight}

Sets the maximum height for the dialog widget.

Default Value: 
{:.param}
 null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({maxHeight: 600 }); 

{% endhighlight  %}

### maxWidth<span class="type-signature type integer">Integer</span> 
{:#members:maxwidth}

Sets the maximum width for the dialog widget.

Default Value:
{:.param} 
null

Example
{:.example}
    
{% highlight js %}

    $("#dialog").ejDialog({maxWidth: 600 }); 

{% endhighlight  %}

### minHeight<span class="type-signature type integer">Integer</span> 
{:#members:minheight}

Sets the minimum height for the dialog widget.

Default Value:
{:.param}
120

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({minHeight: 400 }); 

{% endhighlight  %}

### minWidth<span class="type-signature type integer">Integer</span> 
{:#members:minwidth}

Sets the minimum width for the dialog widget.

Default Value:
{:.param}
 200

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({minWidth: 400 }); 

{% endhighlight  %}

### position<span class="type-signature type JSONobject">JSONobject</span>   
{:#members:position}

Displays the Dialog widget at the given X and Y position. 

<table>
<tr>
<th>
Name<br/><br/></th><th>
Type<br/><br/></th><th>
Default<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td>
X<br/><br/></td><td>
string<br/><br/></td><td>
null<br/><br/></td><td>
Sets the left position of the Dialog widget.<br/><br/></td></tr>
<tr>
<td>
Y<br/><br/></td><td>
string<br/><br/></td><td>
null<br/><br/></td><td>
Sets the top position of the Dialog widget.<br/><br/></td></tr>
</table>

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 

{% endhighlight  %}

### showHeader<span class="type-signature type boolean">Boolean</span>    
{:#members:showheader}

Shows or hides the dialog header.

Default Value:
{:.param}
true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({showHeader: false}); 

{% endhighlight  %}

### showOnInit<span class="type-signature type boolean">Boolean</span> 
{:#members:showoninit}

The Dialog widget can be opened by default i.e. on initialization, when it is set to true.

Default Value:
{:.param}
true

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({showOnInit:true}); 

{% endhighlight  %}

### showRoundedCorner<span class="type-signature type boolean">Boolean</span> 
{:#members:showroundedcorner}

Enables or disables the rounder corner.

Default Value: 
{:.param}
 false

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({showRoundedCorner: true}); 

{% endhighlight  %}


### target <span class="type-signature type string">String</span> 
{:#members:target}

The selector for the container element. If this property is set, the dialog will be displayed (positioned) based on its container.

Default Value:
{:.param}
 null

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({target: "#samplearea" }); 

{% endhighlight  %}

### title <span class="type-signature type string">String</span> 
{:#members:title}

The title text to be displayed in the dialog header. In order to set title, you need to set [showHeader](http://docs.syncfusion.com/js/api/ejdialog#members:showheader) as true since the title will be displayed in the dialog header.

Default Value:
{:.param}
””

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({title: "Custom title" }); 

{% endhighlight  %}
### width <span class="type-signature type string">String</span> <span class="type-signature type integer">Integer</span> 
{:#members:width}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type. The unit of integer type value is “px”.

Default Value:
{:.param}
””

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({width: 500 }); 

{% endhighlight  %}

### zIndex<span class="type-signature type integer">Integer</span>
{:#members:zindex}

Sets the z-index value for the Dialog widget.

Default Value:
{:.param} 
 1000

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog({zIndex: 500 }); 

{% endhighlight  %}

## Methods

### close<span class="signature">()</span>
{:#methods:close}

Closes the dialog widget dynamically.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("close"); 

{% endhighlight  %}

### collapse<span class="signature">()</span>
{:#methods:collapse}

Collapses the content area when it is expanded.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("collapse"); 

{% endhighlight  %}

### destroy<span class="signature">()</span>
{:#methods:destroy}

Destroys the Dialog widget. 

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("destroy"); 

{% endhighlight  %}

### expand<span class="signature">()</span>
{:#methods:expand}

Expands the content area when it is collapsed.

Example 
{:.example}   

{% highlight js %}

    $("#dialog").ejDialog("collapse");

{% endhighlight  %}


### isOpened<span class="signature">()</span> [Deprecated]
{:#methods:isopened}

Checks whether the Dialog widget is opened or not. This methods returns Boolean value.

N>Since it is deprecated we suggest to use the method “[isOpen](#methods:isopen)”.

Example
{:.example}

{% highlight js %}

$("#dialog").ejDialog("isOpened"); 

{% endhighlight  %}

### isOpen<span class="signature">()</span>
{:#methods:isopen}

Checks whether the Dialog widget is opened or not. This methods returns Boolean value.

Example
{:.example}

{% highlight js %}

    var isOpen = $("#dialog").ejDialog("isOpen"); 

{% highlight js %}

### maximize<span class="signature">()</span>
{:#methods:maximize}

Maximizes the Dialog widget.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("maximize"); 

{% endhighlight  %}

### minimize<span class="signature">()</span>
{:#methods:minimize}

Minimizes the Dialog widget.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("minimize"); 

{% endhighlight  %}

### open<span class="signature">()</span>
{:#methods:open}

Opens the Dialog widget.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("open"); 

{% endhighlight  %}

### pin<span class="signature">()</span>
{:#methods:pin}

Pins the dialog in its current position.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("pin"); 

{% endhighlight  %}


### restore<span class="signature">()</span>
{:#methods:restore}

Restores the dialog.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("maximize");

{% endhighlight  %}


### unpin<span class="signature">()</span>
{:#methods:unpin}

Unpins the Dialog widget.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("unpin"); 

{% endhighlight  %}


### setTitle<span class="signature">(title)</span>
{:#methods:settitle}

Sets the title for the Dialog widget.

<table>
<tr>
<td>
Parameters<br/><br/></td><td>
Type<br/><br/></td><td>
Description<br/><br/></td></tr>
<tr>
<td>
Title<br/><br/></td><td>
string<br/><br/></td><td>
The title for the dialog widget.<br/><br/></td></tr>
</table>

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("setTitle","The Dialog"); 

{% endhighlight  %}


### setContent<span class="signature">(content)</span>
{:#methods:setcontent}

Sets the content for the Dialog widget dynamically. 

<table>
<tr>
<td>
Parameters<br/><br/></td><td>
Type<br/><br/></td><td>
Description<br/><br/></td></tr>
<tr>
<td>
content<br/><br/></td><td>
string<br/><br/></td><td>
The content for the dialog widget. It accepts both string and html string.<br/><br/></td></tr>
</table>

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("setContent","custom content"); 

{% endhighlight  %}


### focus<span class="signature">()</span>
{:#methods:focus}

Sets the focus on the Dialog widget.

Example
{:.example}

{% highlight js %}

    $("#dialog").ejDialog("focus"); 

{% endhighlight  %}


## Events

### beforeOpen 
{:#events:beforeopen}

This event is triggered before the dialog widgets gets open.

<table>
<tr>
<th>
<b>Event arguments</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event</td></tr>
</table>


Example
{:.example}

{% highlight js %}


        $("#dialog").ejDialog({ 	beforeOpen: function (args) {} }); 

{% endhighlight %}


###ajaxError
{:#events:ajaxerror}

This event is triggered whenever the Ajax request fails to retrieve the dialog content.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.url</td><td>
string</td><td>
URL of the content.</td></tr>
<tr>
<td>
argument.data.responseText</td><td>
string</td><td>
Error page content</td></tr>
<tr>
<td>
argument.data.status</td><td>
integer</td><td>
Error code</td></tr>
<tr>
<td>
Argument.data.statusText</td><td>
string</td><td>
returns the corresponding error text for error code </td></tr>
</table>


Example
{:.example}


{% highlight js %}


        $("#dialog").ejDialog({ 	ajaxError: function (args){} }); 

{% endhighlight %}


### ajaxSuccess
{:#events:ajaxsuccess}

This event is triggered whenever the Ajax request to retrieve the dialog content, gets succeed.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.url</td><td>
string</td><td>
URL of the content.</td></tr>
<tr>
<td>
argument.data</td><td>
string</td><td>
Response content.</td></tr>
</table>

Example
{:.example}


{% highlight js %}


$("#dialog").ejDialog({ 	ajaxSuccess: function (args){}});

{% endhighlight %}


###beforeClose
{:#events:beforeclose}

This event is triggered before the dialog widgets get closed.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>


Example
{:.example}


{% highlight js %}


    $("#dialog").ejDialog({ 	beforeClose: function(args){}});

{% endhighlight %}


###Close [Deprecated]
{:#events:closedeprecated}

This event is triggered after the dialog widget is closed.

N>Since it is deprecated use the method “close”. Here casing is the difference between two methods.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}



{% highlight js %}

    $("#dialog").ejDialog({ 	Close: function (args) {} }); 

{% endhighlight %}


###close 
{:#events:close}

This event is triggered after the dialog widget is closed.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event</td></tr>
</table>

Example
{:.example}



{% highlight js %}

    $("#dialog").ejDialog({ 	close: function (args) {} }); 

{% endhighlight  %}



###contentLoad
{:#events:contentload}

Triggered after the dialog content is loaded in DOM.

N> This event is triggered only when the [contentType](http://docs.syncfusion.com/js/api/ejdialog) is set to image or iframe.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.url</td><td>
String</td><td>
URL of the content.</td></tr>
<tr>
<td>
argument.contentType</td><td>
Object</td><td>
Content type</td></tr>
</table>

Example
{:.example}


{% highlight js %}

    $("#dialog").ejDialog({ contentLoad: function (args) {} }); 

{% endhighlight  %}


###create
{:#events:create}

Triggered after the dialog is created successfully

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}


{% highlight js %}

    $("#dialog").ejDialog({ 	create: function (args) {} }); 

{% endhighlight %}


###destroy
{:#events:destroy}

Triggered after the dialog widget is destroyed successfully

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight js %}


    $("#dialog").ejDialog({ 	destroy: function (args) {} }); 

{% endhighlight  %}


###drag
{:#events:drag}

Triggered while the dialog is dragged.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight js %}

$("#dialog").ejDialog({ 	drag: function (args) {} }); 

{% endhighlight  %}


###dragStart
{:#events:dragstart}

Triggered when the user starts dragging the dialog.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight js %}

$("#dialog").ejDialog({ 	dragStart: function (args) {} }); 

{% endhighlight  %}


###dragStop
{:#events:dragstop}

Triggered when the user stops dragging the dialog.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>
Example
{:.example}


{% highlight js %}

    $("#dialog").ejDialog({ 	dragStop: function (args) {} }); 

{% endhighlight %}


###open
{:#events:open}

Triggered after the dialog is opened.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight js %}


$("#dialog").ejDialog({ 	open: function (args) {} }); 

{% endhighlight %}


###resize
{:#events:resize}

Triggered while the dialog is resized.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight js %}

$("#dialog").ejDialog({ 	resize: function (args) {} }); 

{% endhighlight  %}


###resizeStart
{:#events:resizestart}

Triggered when the user starts resizing the dialog.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}

{% highlight js %}


    $("#dialog").ejDialog({ 	resizeStart: function (args) {} }); 

{% endhighlight  %}


###resizeStop
{:#events:resizestop}

Triggered when the user stops resizing the dialog.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event</td></tr>
<tr>
<td>
argument.event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}

{% highlight js %}


    $("#dialog").ejDialog({ 	resizeStop: function (args) {} }); 

{% endhighlight  %}


###expand
{:#events:expand}

Triggered when the dialog content is expanded.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight js %}


        $("#dialog").ejDialog({ 
        
            actionButtons: ["close","collapse","expand"], 
        
            expand: function (args) {} 
        
        }); 

{% endhighlight %}


###collapse
{:#events:collapse}

Triggered when the dialog content is collapsed.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}



{% highlight js %}

$("#dialog").ejDialog({ 

	actionButtons: ["close","collapse","expand"], 

	collapse: function (args) {} 

}); 

{% endhighlight %}