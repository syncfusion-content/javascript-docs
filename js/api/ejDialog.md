---
layout: post
title: API reference for ejDialog
description: What are the options, methods and events available in Essential JavaScript Dialog.
documentation: API
platform: js
keywords: ejDialog, API, Essential JS Dialog, Dialog

---

# ejDialog


The Dialog control displays a Dialog window within a webpage. The Dialog enables a message to be displayed, such as supplementary content like images and text, and an interactive content like forms.


#### Syntax

{% highlight js %}

$(element).ejDialog(options)

{% endhighlight %}



<table>
<tr>
<th>
Name<br/><br/></th><th>
Type<br/><br/></th><th>
Description<br/><br/></th></tr>
<tr>
<td class="name">
options<br/><br/></td><td class="tyoe">
object<br/><br/></td><td class="description">
Settings for Dialog.<br/><br/></td></tr>
</table>

#### Example


{% highlight js %}
    
    // Create the Dialog widget

    $("#dialog").ejDialog(); 
    
{% endhighlight %}

#### Requires


* module:jQuery
* module:jquery.easing.1.3.js
* module:ej.core.js
* module:ej.dialog.js
* module:ej.scroller.js
* module:ej.button.js
* module:ej.draggable.js

##Members


### actionButtons `StringArray`
{:#members:actionbuttons}

Adds action buttons like close, minimize, pin, maximize in the dialog header.

#### Default Value

* 'close'

#### Example 


{% highlight js %}

    $("#dialog").ejDialog({actionButtons: ["close","collapsible","pin"]}); 
    
 {% endhighlight %}


### allowDraggable `boolean`
{:#members:allowdraggable}

Enables or disables draggable.

#### Default Value

 * true

#### Example


{% highlight js %}

     $("#dialog").ejDialog({allowDraggable: false});
         
{% endhighlight %}

### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}

Enables or disables keyboard interaction.

#### Default Value

 * true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({allowKeyboardNavigation: true}); 

{% endhighlight %}


### animation `JSONobject`
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
<td class="name">
show.effect<br/><br/></td><td class="type">
String<br/><br/></td><td class="default">
fade<br/><br/></td><td class="description">
The animation effect when the dialog is opened. The possible values are fade and slide.<br/><br/></td></tr>
<tr>
<td class="name">
show.duration<br/><br/></td><td class="type">
integer <br/><br/></td><td class="default">
400<br/><br/></td><td class="description">
The duration for the animation effect when the dialog is opened.<br/><br/></td></tr>
<tr>
<td class="name">
hide.effect<br/><br/></td><td class="type">
String<br/><br/></td><td class="default">
fade<br/><br/></td><td>
The animation effect when the dialog is closed. The possible values are fade and slide.<br/><br/></td></tr>
<tr>
<td class="name">
hide.duration<br/><br/></td><td class="type">
integer<br/><br/></td><td class="default">
400<br/><br/></td><td class="description">
The duration for the animation effect when the dialog is closed.<br/><br/></td></tr>
</table>

#### Example


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
              
{% endhighlight %}


### closeIconTooltip `string`
{:#members:closeicontooltip}

The tooltip text for the dialog close button.

#### Default Value

 * close

#### Example


{% highlight js %}

    $("#dialog").ejDialog({closeIconTooltip: "close" }); 

{% endhighlight %}


### closeOnEscape `boolean`
{:#members:closeonescape}

Closes the dialog widget on pressing the <kbd>ESC</kbd> key when it is set to true.

#### Default Value

  * true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({closeOnEscape: false}); 
    
{% endhighlight %}


### content[Deprecated] `string`
{:#members:content}

The selector for the container element. If this property is set, the dialog will be displayed (positioned) based on its container.

N>Since it is deprecated we suggest to use the API “[target](#methods:target)”.

#### Default Value

  * null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({content: "#samplearea" }); 

{% endhighlight %}


### contentType `string`
{:#members:contenttype}

The content type to load the dialog content at run time. The possible values are null, ajax, iframe and image. When it is null (default value), the content inside dialog element will be displayed as content and when it is not null, the content will be loaded from the URL specified in the [contentUrl](http://docs.syncfusion.com/js/api/ejdialog#members:contenturl) property.

#### Default Value


  * null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({contentType: "ajax" }); 

{% endhighlight %}


### contentUrl `string`
{:#members:contenturl}

The URL to load the dialog content (such as AJAX, image, and iframe). In order to load content from URL, you need to set [contentType](http://docs.syncfusion.com/js/api/ejdialog#members:contenttype) as ‘ajax’ or ‘iframe’ or ‘image’.

#### Default Value

 * null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({contentType: "ajax",

    contentUrl: "http://js.syncfusion.com/demos/web/dialog/ajaxcontent.html" }); 

{% endhighlight %}


### cssClass `string`
{:#members:cssclass}

The root class for the Dialog widget to customize the existing theme.

#### Default Value

  * ””

#### Example


{% highlight js %}

    $("#dialog").ejDialog({ cssClass: "gradient-lime" }); 
    
{% endhighlight %}


### enableAnimation `boolean`
{:#members:enableanimation}

Enable or disables animation when the dialog is opened or closed.

#### Default Value

 * true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({ enableAnimation: false}); 

{% endhighlight %}


### enabled `boolean`
{:#members:enabled}

Enables or disables the Dialog widget.

#### Default Value

 * true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({ enabled: true }); 

{% endhighlight %}


### enableModal `boolean`
{:#members:enablemodal}

Enable or disables modal dialog. The [modal dialog](https://en.wikipedia.org/wiki/Modal_window#) acts like a child window that is displayed on top of the main window/screen and disables the main window interaction until it is closed.

#### Default Value

 * false

#### Example


{% highlight js %}

    $("#dialog").ejDialog({enableModal: true}); 

{% endhighlight %}


### enablePersistence `boolean`
{:#members:enablepersistence}

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true.

N>[Local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is supported only in Html5 supported browsers.If the browsers don’t have support for local storage,browser cookies will be used to maintain the state.

#### Default Value


 * false

#### Example


{% highlight js %}

    $("#dialog").ejDialog({enablePersistence: true}); 

{% endhighlight %}


### enableResize `boolean`
{:#members:enableresize}

Allows the dialog to be resized. The dialog cannot be resized less than the minimum height and minimum width values.

#### Default Value

  * true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({enableResize: false}); 

{% endhighlight %}


### enableRTL `boolean`
{:#members:enablertl}

Displays dialog content from right to left when set to true.

#### Default Value

 * false

#### Example


{% highlight js %}

    $("#dialog").ejDialog({enableRTL: true}); 

{% endhighlight %}


### faviconCSS `string`
{:#members:faviconcss}

The CSS class name to display the favicon in the dialog header. In order to display fav icon, you need to [showHeader](http://docs.syncfusion.com/js/api/ejdialog#members:showheader) as true since the favicon will be displayed in the dialog header.

#### Default Value

  * null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({faviconCSS : "custom-icon" }); 

{% endhighlight %}


### height `string`  `integer` 
{:#members:height}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type. The unit of integer type value is “px”.

#### Default Value

 * auto

#### Example


{% highlight js %}

    $("#dialog").ejDialog({height: 400 }); 

{% endhighlight %}


### isResponsive `boolean` 
{:#members:isresponsive}

Enable or disables responsive behavior.

N>Once the dialog is resized or dragged,then the responsive behavior won’t work.

#### Default Value

 * false

#### Example


{% highlight js %}

    $("#dialog").ejDialog({isResponsive: true }); 

{% endhighlight %}


### maxHeight `integer` 
{:#members:maxheight}

Sets the maximum height for the dialog widget.

#### Default Value

  * null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({maxHeight: 600 }); 

{% endhighlight %}


### maxWidth `integer` 
{:#members:maxwidth}

Sets the maximum width for the dialog widget.

#### Default Value

 * null

#### Example

    
{% highlight js %}

    $("#dialog").ejDialog({maxWidth: 600 }); 

{% endhighlight %}


### minHeight `integer` 
{:#members:minheight}

Sets the minimum height for the dialog widget.

#### Default Value

 * 120

#### Example


{% highlight js %}

    $("#dialog").ejDialog({minHeight: 400 }); 

{% endhighlight %}

### minWidth `integer` 
{:#members:minwidth}

Sets the minimum width for the dialog widget.

#### Default Value

 * 200

#### Example


{% highlight js %}

    $("#dialog").ejDialog({minWidth: 400 }); 

{% endhighlight %}


### position `JSONobject`   
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
<td class="name">
X<br/><br/></td><td class="type">
string<br/><br/></td><td class="default">
null<br/><br/></td><td class="description">
Sets the left position of the Dialog widget.<br/><br/></td></tr>
<tr>
<td  class="name">
Y<br/><br/></td><td class="type">
string<br/><br/></td><td class="default">
null<br/><br/></td><td class="description">
Sets the top position of the Dialog widget.<br/><br/></td></tr>
</table>

#### Example


{% highlight js %}

    $("#dialog").ejDialog({position: { X: 300, Y: 10 }}); 

{% endhighlight %}


### showHeader `boolean`    
{:#members:showheader}

Shows or hides the dialog header.

#### Default Value

* true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({showHeader: false}); 

{% endhighlight %}


### showOnInit `boolean` 
{:#members:showoninit}

The Dialog widget can be opened by default i.e. on initialization, when it is set to true.

#### Default Value

* true

#### Example


{% highlight js %}

    $("#dialog").ejDialog({showOnInit:true}); 

{% endhighlight %}


### showRoundedCorner `boolean` 
{:#members:showroundedcorner}

Enables or disables the rounder corner.

#### Default Value

* false

#### Example


{% highlight js %}

    $("#dialog").ejDialog({showRoundedCorner: true}); 

{% endhighlight %}


### target  `string` 
{:#members:target}

The selector for the container element. If this property is set, the dialog will be displayed (positioned) based on its container.

#### Default Value

* null

#### Example


{% highlight js %}

    $("#dialog").ejDialog({target: "#samplearea" }); 

{% endhighlight %}


### title  `string` 
{:#members:title}

The title text to be displayed in the dialog header. In order to set title, you need to set [showHeader](http://docs.syncfusion.com/js/api/ejdialog#members:showheader) as true since the title will be displayed in the dialog header.

#### Default Value

* ””

#### Example


{% highlight js %}

    $("#dialog").ejDialog({title: "Custom title" }); 

{% endhighlight %}


### width  `string`  `integer` 
{:#members:width}

Sets the height for the dialog widget. It accepts both string and integer values. For example, it can accepts values like “auto”, “100%”, “100px” as string type and “100”, “500” as integer type. The unit of integer type value is “px”.

#### Default Value

* ””

#### Example


{% highlight js %}

    $("#dialog").ejDialog({width: 500 }); 

{% endhighlight %}


### zIndex `integer`
{:#members:zindex}

Sets the z-index value for the Dialog widget.

#### Default Value

* 1000

#### Example


{% highlight js %}

    $("#dialog").ejDialog({zIndex: 500 }); 

{% endhighlight %}

## Methods

### close()
{:#methods:close}

Closes the dialog widget dynamically.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("close"); 

{% endhighlight %}

### collapse()
{:#methods:collapse}

Collapses the content area when it is expanded.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("collapse"); 

{% endhighlight %}


### destroy()
{:#methods:destroy}

Destroys the Dialog widget. 

#### Example


{% highlight js %}

    $("#dialog").ejDialog("destroy"); 

{% endhighlight %}


### expand()
{:#methods:expand}

Expands the content area when it is collapsed.

#### Example 
   

{% highlight js %}

    $("#dialog").ejDialog("collapse");

{% endhighlight %}


### isOpened() [Deprecated]
{:#methods:isopened}

Checks whether the Dialog widget is opened or not. This methods returns Boolean value.

N>Since it is deprecated we suggest to use the method “[isOpen](#methods:isopen)”.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("isOpened"); 

{% endhighlight %}


### isOpen()
{:#methods:isopen}

Checks whether the Dialog widget is opened or not. This methods returns Boolean value.

#### Example


{% highlight js %}

    var isOpen = $("#dialog").ejDialog("isOpen"); 

{% endhighlight %}


### maximize()
{:#methods:maximize}

Maximizes the Dialog widget.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("maximize"); 

{% endhighlight %}


### minimize()
{:#methods:minimize}

Minimizes the Dialog widget.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("minimize"); 

{% endhighlight %}


### open()
{:#methods:open}

Opens the Dialog widget.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("open"); 

{% endhighlight %}

### pin()
{:#methods:pin}

Pins the dialog in its current position.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("pin"); 

{% endhighlight %}


### restore()
{:#methods:restore}

Restores the dialog.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("maximize");

{% endhighlight %}


### unpin()
{:#methods:unpin}

Unpins the Dialog widget.

#### Example


{% highlight js %}

    $("#dialog").ejDialog("unpin"); 

{% endhighlight %}


### setTitle(title)</span>
{:#methods:settitle}

Sets the title for the Dialog widget.

<table>
<tr>
<th>
<b>Parameters</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td class="name">
Title<br/><br/></td><td class="type">
string<br/><br/></td><td class="description">
The title for the dialog widget.<br/><br/></td></tr>
</table>

#### Example


{% highlight js %}

    $("#dialog").ejDialog("setTitle","The Dialog"); 

{% endhighlight %}


### setContent(content)</span>
{:#methods:setcontent}

Sets the content for the Dialog widget dynamically. 

<table>
<tr>
<th>
<b>Parameters</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td class="name">
content<br/><br/></td><td class="type">
string<br/><br/></td><td class="description">
The content for the dialog widget. It accepts both string and html string.<br/><br/></td></tr>
</table>

#### Example


{% highlight js %}

    $("#dialog").ejDialog("setContent","custom content"); 

{% endhighlight %}


### focus()
{:#methods:focus}

Sets the focus on the Dialog widget.

#### Example


{% highlight js %}

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
<td  class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
String</td><td class="description">
Name of the event</td></tr>
</table>


#### Example


{% highlight js %}


        $("#dialog").ejDialog({ beforeOpen: function (args) {} }); 

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.url</td><td class="type">
string</td><td class="description">
URL of the content.</td></tr>
<tr>
<td class="name">
argument.data.responseText</td><td class="type">
string</td><td class="description">
Error page content</td></tr>
<tr>
<td class="name">
argument.data.status</td><td class="type">
integer</td><td class="description">
Error code</td></tr>
<tr>
<td class="name">
Argument.data.statusText</td><td class="type">
string</td><td class="description">
The corresponding error description.</td></tr>
</table>


#### Example



{% highlight js %}


        $("#dialog").ejDialog({ ajaxError: function (args){} }); 

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.url</td><td class="type">
string</td><td class="description">
URL of the content.</td></tr>
<tr>
<td class="name">
argument.data</td><td class="type">
string</td><td class="description">
Response content.</td></tr>
</table>

#### Example



{% highlight js %}


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
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
<tr>
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>


#### Example



{% highlight js %}


    $("#dialog").ejDialog({ beforeClose: function(args){}});

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
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
<tr>
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
String</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example




{% highlight js %}

    $("#dialog").ejDialog({ Close: function (args) {} }); 

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
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
<tr>
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
String</td><td class="description">
Name of the event</td></tr>
</table>

#### Example




{% highlight js %}

    $("#dialog").ejDialog({ close: function (args) {} }); 

{% endhighlight %}



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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
String</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.url</td><td class="type">
String</td><td class="description">
URL of the content.</td></tr>
<tr>
<td class="name">
argument.contentType</td><td class="type">
Object</td><td class="description">
Content type</td></tr>
</table>

#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example


{% highlight js %}


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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>

#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>

#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>
#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example


{% highlight js %}


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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>

#### Example



{% highlight js %}

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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>

#### Example


{% highlight js %}


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
<td class="name">
argument.cancel</td><td class="type">
Boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
String</td><td class="description">
Name of the event</td></tr>
<tr>
<td class="name">
argument.event</td><td class="type">
Object</td><td class="description">
Current event object.</td></tr>
</table>

#### Example


{% highlight js %}


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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example


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
<td class="name">
argument.cancel</td><td class="type">
boolean</td><td class="description">
Set this option to true to cancel the event.</td></tr>
<tr>
<td class="name">
argument.model</td><td class="type">
object</td><td class="description">
Instance of the dialog model object.</td></tr>
<tr>
<td class="name">
argument.type</td><td class="type">
string</td><td class="description">
Name of the event.</td></tr>
</table>

#### Example




{% highlight js %}

$("#dialog").ejDialog({ 

	actionButtons: ["close","collapse","expand"], 

	collapse: function (args) {} 

}); 

{% endhighlight %}
