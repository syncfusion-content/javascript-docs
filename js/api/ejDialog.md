---
layout: post
title: Properties, Methods and Events of ejDialog Widget
description: Methods, members, events available in ejDialog
documentation: API
platform: js
keywords: ejDialog, API, Essential JS Dialog
---

# ejDialog

The Dialog control displays a Dialog window within a web page. The Dialog enables a message to be displayed, such as supplementary content like images and text, and an interactive content like forms.

#### Syntax

{% highlight javascript %}

    $(element).ejDialog(options)

{% endhighlight %}

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
options</td><td>
object</td><td>
Settings for Dialog.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}
    
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


### actionButtons `String[]`
{:#members:actionbuttons}

Adds action buttons like close, minimize, pin, maximize in the dialog header.

Default Value:
{:.param}
[&ldquo;close&rdquo;]

Example 
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({actionButtons: ["close","collapsible","pin"]}); 
    
 {% endhighlight %}


### allowDraggable `Boolean`
{:#members:allowdraggable}

Enables or disables draggable.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight javascript %}

     $("#dialog").ejDialog({allowDraggable: false});
         
{% endhighlight %}

### allowKeyboardNavigation `Boolean`
{:#members:allowkeyboardnavigation}

Enables or disables keyboard interaction.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({allowKeyboardNavigation: true}); 

{% endhighlight %}


### animation `object`
{:#members:animation}

Customizes the Dialog widget animations. The Dialog widget can be animated while opening and closing the dialog. In order to customize animation effects, you need to set “[enableAnimation](#members:enableanimation)” as true. It contains the following sub properties.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Default</th><th>
Description</th></tr>
<tr>
<td>
show.effect</td><td>
String</td><td>
fade</td><td>
The animation effect when the dialog is opened. The possible values are fade and slide.</td></tr>
<tr>
<td>
show.duration</td><td>
integer </td><td>
400</td><td>
The duration for the animation effect when the dialog is opened.</td></tr>
<tr>
<td>
hide.effect</td><td>
String</td><td>
fade</td><td>
The animation effect when the dialog is closed. The possible values are fade and slide.</td></tr>
<tr>
<td>
hide.duration</td><td>
integer</td><td>
400</td><td>
The duration for the animation effect when the dialog is closed.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}

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
              
{% endhighlight %}


### closeOnEscape `Boolean`
{:#members:closeonescape}

Closes the dialog widget on pressing the <kbd>ESC</kbd> key when it is set to true.

Default Value:
{:.param}
 true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({closeOnEscape: false}); 
    
{% endhighlight %}


### containment `String`
{:#members:containment}

The selector for the container element. If the property is set, then dialog will append to the selected element and it is restricted to move only within the specified container element.

N> This property is similar to the “[target](#methods:target)” property but this additionally sets the drag area for dialog. Also this property overrides target property if both are set.

Default Value:
{:.param}
“”

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({containment: "#dragarea"}); 

{% endhighlight %}


### contentType `String`
{:#members:contenttype}

The content type to load the dialog content at run time. The possible values are null, AJAX, iframe and image. When it is null (default value), the content inside dialog element will be displayed as content and when it is not null, the content will be loaded from the URL specified in the [contentUrl](#members:contenturl) property.

Default Value:
{:.param}

 null

Examples
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({contentType: "ajax" }); 

{% endhighlight %}


### contentUrl `String`
{:#members:contenturl}

The URL to load the dialog content (such as AJAX, image, and iframe). In order to load content from URL, you need to set [contentType](#members:contenttype) as ‘ajax’ or ‘iframe’ or ‘image’.

Default Value:
{:.param}
null

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({contentType: "ajax",

    contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html" }); 

{% endhighlight %}


### cssClass `String`
{:#members:cssclass}

The root class for the Dialog widget to customize the existing theme.

Default Value:
{:.param}
 ””

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({ cssClass: "gradient-lime" }); 
    
{% endhighlight %}


### enableAnimation `Boolean`
{:#members:enableanimation}

Enable or disables animation when the dialog is opened or closed.

Default Value:
{:.param} 
 true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({ enableAnimation: false}); 

{% endhighlight %}


### enabled `Boolean`
{:#members:enabled}

Enables or disables the Dialog widget.

Default Value: 
{:.param}
 true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({ enabled: true }); 

{% endhighlight %}


### enableModal `Boolean`
{:#members:enablemodal}

Enable or disables modal dialog. The [modal dialog](https://en.wikipedia.org/wiki/Modal_window#) acts like a child window that is displayed on top of the main window/screen and disables the main window interaction until it is closed.

Default Value:
{:.param}
 false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({enableModal: true}); 

{% endhighlight %}


### enablePersistence `Boolean`
{:#members:enablepersistence}

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true.

N>[Local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is supported only in Html5 supported browsers.If the browsers don’t have support for local storage,browser cookies will be used to maintain the state.

Default Value:

{:.param}
false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({enablePersistence: true}); 

{% endhighlight %}


### enableResize `Boolean`
{:#members:enableresize}

Allows the dialog to be resized. The dialog cannot be resized less than the minimum height, width values and greater than the maximum height and width.

Default Value: 
{:.param}
 true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({enableResize: false}); 

{% endhighlight %}


### enableRTL `Boolean`
{:#members:enablertl}

Displays dialog content from right to left when set to true.

Default Value: 
{:.param}
false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({enableRTL: true}); 

{% endhighlight %}


### faviconCSS `String`
{:#members:faviconcss}

The CSS class name to display the favicon in the dialog header. In order to display favicon, you need to set [showHeader](#members:showheader) as true since the favicon will be displayed in the dialog header.

Default Value: 
{:.param}
 null

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({faviconCSS : "custom-icon" }); 

{% endhighlight %}


### height `String` `Number`
{:#members:height}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type.

Default Value:
{:.param}
auto

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({height: 400 }); 

{% endhighlight %}


### isResponsive `Boolean` 
{:#members:isresponsive}

Enable or disables responsive behavior.

N>Once the dialog is resized or dragged,then the responsive behavior won’t work.

Default Value:
{:.param}
false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({isResponsive: true }); 

{% endhighlight %}

### locale `Number`
{:#members:locale}
Set the localization culture for Dialog Widget.

Default Value:
{:.param}
“en-US”

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({locale: "en-US"});

{% endhighlight %}



### maxHeight `Number`
{:#members:maxheight}

Sets the maximum height for the dialog widget.

Default Value: 
{:.param}
 null

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({maxHeight: 600 }); 

{% endhighlight %}


### maxWidth `Number`
{:#members:maxwidth}

Sets the maximum width for the dialog widget.

Default Value:
{:.param} 
null

Example
{:.example}
    
{% highlight javascript %}

    $("#dialog").ejDialog({maxWidth: 600 }); 

{% endhighlight %}


### minHeight `Number`
{:#members:minheight}

Sets the minimum height for the dialog widget.

Default Value:
{:.param}
120

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({minHeight: 400 }); 

{% endhighlight %}

### minWidth `Number`
{:#members:minwidth}

Sets the minimum width for the dialog widget.

Default Value:
{:.param}
 200

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({minWidth: 400 }); 

{% endhighlight %}


### position `object`   
{:#members:position}

Displays the Dialog widget at the given X and Y position. 

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Default</th><th>
Description</th></tr>
<tr>
<td>
X</td><td>
string</td><td>
null</td><td>
Sets the left position of the Dialog widget.</td></tr>
<tr>
<td>
Y</td><td>
string</td><td>
null</td><td>
Sets the top position of the Dialog widget.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 

{% endhighlight %}


### showHeader `Boolean`
{:#members:showheader}

Shows or hides the dialog header.

Default Value:
{:.param}
true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({showHeader: false}); 

{% endhighlight %}


### showOnInit `Boolean`
{:#members:showoninit}

The Dialog widget can be opened by default i.e. on initialization, when it is set to true.

Default Value:
{:.param}
true

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({showOnInit:true}); 

{% endhighlight %}


### showRoundedCorner `Boolean`
{:#members:showroundedcorner}

Enables or disables the rounder corner.

Default Value: 
{:.param}
 false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({showRoundedCorner: true}); 

{% endhighlight %}


### target `String`
{:#members:target}

The selector for the container element. If this property is set, the dialog will be displayed (positioned) based on its container.

Default Value:
{:.param}
 null

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({target: "#samplearea" }); 

{% endhighlight %}


### title `String`
{:#members:title}

The title text to be displayed in the dialog header. In order to set title, you need to set [showHeader](#members:showheader) as true since the title will be displayed in the dialog header.

Default Value:
{:.param}
””

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({title: "Custom title" }); 

{% endhighlight %}

### tooltip `object`
{:#members:tooltip}

Add or configure the tooltip text for [actionButtons](#members:actionbuttons) in the dialog header.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Default</th><th>
Description</th></tr>
<tr>
<td>
close</td><td>
String</td><td>
“Close”</td><td>
Sets the tooltip for close button.</td></tr>
<tr>
<td>
collapse</td><td>
String</td><td>
“Collapse”</td><td>
Sets the tooltip for collapse button.</td></tr>
<tr>
<td>
restore</td><td>
String</td><td>
“Restore”</td><td>
Sets the tooltip for restore button.</td></tr>
<tr>
<td>
maximize</td><td>
String</td><td>
“Maximize”</td><td>
Sets the tooltip for maximize button. </td></tr>
<tr>
<td>
minimize</td><td>
String</td><td>
“Minimize”</td><td>
Sets the tooltip for minimize button.</td></tr>
<tr>
<td>
expand</td><td>
String</td><td>
“Expand”</td><td>
Sets the tooltip for expand button.</td></tr>
<tr>
<td>
unpin</td><td>
String</td><td>
“Unpin”</td><td>
Sets the tooltip for unpin button.</td></tr>
<tr>
<td>
pin</td><td>
String</td><td>
“Pin”</td><td>
Sets the tooltip for pin button.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({tooltip: { close: "Exit" }}); 

{% endhighlight %}


### width `String` `Number`
{:#members:width}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type.

Default Value:
{:.param}
””

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({width: 500 }); 

{% endhighlight %}


### zIndex `Number`
{:#members:zindex}

Sets the z-index value for the Dialog widget.

Default Value:
{:.param} 
 1000

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({zIndex: 500 }); 

{% endhighlight %}


### showFooter `Boolean`
{:#members:showfooter}

Sets the Footer for the Dialog widget.

Default Value:
{:.param} 
 false

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({showFooter: true }); 

{% endhighlight %}


### footerTemplateId `String`
{:#members:footertemplateid}

Sets the FooterTemplate for the Dialog widget.

Default Value:
{:.param} 
 null

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog({showFooter: true,footerTemplateId:"sample"}); 

{% endhighlight %}


## Methods

### close<span class="signature">()</span>
{:#methods:close}

Closes the dialog widget dynamically.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("close"); 

{% endhighlight %}

### collapse<span class="signature">()</span>
{:#methods:collapse}

Collapses the content area when it is expanded.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("collapse"); 

{% endhighlight %}


### destroy<span class="signature">()</span>
{:#methods:destroy}

Destroys the Dialog widget. 

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("destroy"); 

{% endhighlight %}


### expand<span class="signature">()</span>
{:#methods:expand}

Expands the content area when it is collapsed.

Example 
{:.example}   

{% highlight javascript %}

    $("#dialog").ejDialog("collapse");

{% endhighlight %}


### isOpen<span class="signature">()</span>
{:#methods:isopen}

Checks whether the Dialog widget is opened or not. This methods returns Boolean value.

Example
{:.example}

{% highlight javascript %}

    var isOpen = $("#dialog").ejDialog("isOpen"); 

{% endhighlight %}


### maximize<span class="signature">()</span>
{:#methods:maximize}

Maximizes the Dialog widget.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("maximize"); 

{% endhighlight %}


### minimize<span class="signature">()</span>
{:#methods:minimize}

Minimizes the Dialog widget.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("minimize"); 

{% endhighlight %}


### open<span class="signature">()</span>
{:#methods:open}

Opens the Dialog widget.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("open"); 

{% endhighlight %}

### pin<span class="signature">()</span>
{:#methods:pin}

Pins the dialog in its current position.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("pin"); 

{% endhighlight %}


### restore<span class="signature">()</span>
{:#methods:restore}

Restores the dialog.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("maximize");

{% endhighlight %}


### unpin<span class="signature">()</span>
{:#methods:unpin}

Unpins the Dialog widget.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("unpin"); 

{% endhighlight %}


### setTitle<span class="signature">(title)</span>
{:#methods:settitle}

Sets the title for the Dialog widget.

<table>
<tr>
<th>
<b>Parameters</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td>
Title</td><td>
string</td><td>
The title for the dialog widget.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("setTitle","The Dialog"); 

{% endhighlight %}


### setContent<span class="signature">(content)</span>
{:#methods:setcontent}

Sets the content for the Dialog widget dynamically. 

<table>
<tr>
<th>
<b>Parameters</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td>
content</td><td>
string</td><td>
The content for the dialog widget. It accepts both string and HTML string.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("setContent","custom content"); 

{% endhighlight %}


### focus<span class="signature">()</span>
{:#methods:focus}

Sets the focus on the Dialog widget.

Example
{:.example}

{% highlight javascript %}

    $("#dialog").ejDialog("focus"); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
String</td><td>
Name of the event</td></tr>
</table>


Example
{:.example}

{% highlight javascript %}


        $("#dialog").ejDialog({ beforeOpen: function (args) {} }); 

{% endhighlight %}


###ajaxError
{:#events:ajaxerror}

This event is triggered whenever the AJAX request fails to retrieve the dialog content.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
URL</td><td>
string</td><td>
URL of the content.</td></tr>
<tr>
<td class="name">data</td>
<td class="type"><ts ref="ej.Dialog.Model"/><span class="param-type">Object</span></td>
<td class="description last">
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
<td class="name">responseText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Error page content.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Error code.</td>
</tr>
<tr>
<td class="name">statusText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">The corresponding error description.</td>
</tr>
</tbody>
</table>
</td>
</td>
</tr>
</table>

Example
{:.example}


{% highlight javascript %}


        $("#dialog").ejDialog({ ajaxError: function (args){} }); 

{% endhighlight %}


### ajaxSuccess
{:#events:ajaxsuccess}

This event is triggered whenever the AJAX request to retrieve the dialog content, gets succeed.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
URL</td><td>
string</td><td>
URL of the content.</td></tr>
<tr>
<td>
data</td><td>
string</td><td>
Response content.</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}


    $("#dialog").ejDialog({ ajaxSuccess: function (args){}});

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
event</td><td>
Object</td><td>
Current event object.</td></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>


Example
{:.example}


{% highlight javascript %}


    $("#dialog").ejDialog({ beforeClose: function(args){}});

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
event</td><td>
Object</td><td>
Current event object.</td></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
String</td><td>
Name of the event</td></tr>
</table>

Example
{:.example}



{% highlight javascript %}

    $("#dialog").ejDialog({ close: function (args) {} }); 

{% endhighlight %}



###contentLoad
{:#events:contentload}

Triggered after the dialog content is loaded in DOM.

N> This event is triggered only when the [contentType](#members:contenttype) is set to image or iframe.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
URL</td><td>
String</td><td>
URL of the content.</td></tr>
<tr>
<td>
contentType</td><td>
Object</td><td>
Content type</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}

    $("#dialog").ejDialog({ contentLoad: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}

    $("#dialog").ejDialog({ create: function (args) {} }); 

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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}


    $("#dialog").ejDialog({ destroy: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}

    $("#dialog").ejDialog({ drag: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}

$("#dialog").ejDialog({ dragStart: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>
Example
{:.example}


{% highlight javascript %}

    $("#dialog").ejDialog({ dragStop: function (args) {} }); 

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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}


           $("#dialog").ejDialog({ open: function (args) {} }); 

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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}


{% highlight javascript %}

    $("#dialog").ejDialog({ resize: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}


    $("#dialog").ejDialog({ resizeStart: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
String</td><td>
Name of the event</td></tr>
<tr>
<td>
event</td><td>
Object</td><td>
Current event object.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}


    $("#dialog").ejDialog({ resizeStop: function (args) {} }); 

{% endhighlight %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}

{% highlight javascript %}


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
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
</table>

Example
{:.example}



{% highlight javascript %}

$("#dialog").ejDialog({ 

	actionButtons: ["close","collapse","expand"], 

	collapse: function (args) {} 

}); 

{% endhighlight %}


###actionButtonClick
{:#events:actionbuttonclick}

Triggered when the custom action button clicked.

<table>
<tr>
<th>
Name</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
cancel</td><td>
boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
buttonID</td><td>
string</td><td>
Name of the event target attribute.</td></tr>
<tr>
<td>
type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
model</td><td><ts ref="ej.Dialog.Model"/>
object</td><td>
Instance of the dialog model object.</td></tr>
<tr>
<td>
currentTarget</td><td>
string</td><td>
Name of the event current target title.</td></tr>
</table>

Example
{:.example}



{% highlight javascript %}

$("#dialog").ejDialog({ 

	actionButtonClick: function (args) {
        
    } 

}); 

{% endhighlight %}