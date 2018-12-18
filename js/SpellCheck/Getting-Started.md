---
title: Getting started with Syncfusion SpellCheck component	
description: Rendering a basic SpellCheck
platform: js
control: spellcheck
documentation: ug
keywords: ejSpellCheck, spellcheck, spellcheck widget, js spellcheck, getting started, initialization, service reference
api: /api/js/ejspellcheck 
---
# Getting Started

To render the SpellCheck control, the following list of external dependencies are needed, 

* [jQuery](http://jquery.com) - 1.7.1 and later versions

The other required internal dependencies are tabulated below,

<table>
<tr>
<th>
File<br/><br/></th><th>
Description/Usage<br/><br/></th></tr>
<tr>
<td>
ej.core.min.js<br/><br/></td><td>
Must be referred always first before using all the JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.data.min.js<br/><br/></td><td>
Used to handle data operation and should be used while binding data to JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.spellcheck.min.js<br/><br/></td><td>
SpellCheck core script file.<br/><br/></td></tr>
<tr>
<td>
ej.scroller.js<br/><br/>ej.button.js<br/><br/>ej.dialog.js<br/><br/>ej.menu.js<br/><br/>ej.listbox.js<br/><br/>ej.draggable.js<br/><br/>ej.globalize.js<br/><br/></td><td>
These files are referred for proper working of the sub-controls used within SpellCheck.<br/><br/></td></tr>
</table>

N> SpellCheck uses one or more sub-controls, therefore refer the `ej.web.all.min.js` (which encapsulates all the `ej` controls and frameworks in a single file) in the application instead of referring all the above specified internal dependencies. 

To get the real appearance of the SpellChecker, the dependent CSS file `ej.web.all.min.css` (which includes styles of all the widgets) should also needs to be referred.


## Script/CSS Reference

Create a new HTML file and include the below initial code.

{% highlight html %}

<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <meta charset="utf-8" />
        <title> </title>
    </head>
    <body>
    </body>
</html>

{% endhighlight %}

Refer the CSS file from the specific theme folder to your HTML file within the head section. Refer the built-in available themes from [here](/js/theming-in-essential-javascript-components).

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - SpellCheck</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
</head>

{% endhighlight %}

Add links to the [CDN](/js/cdn) Script files with other required external dependencies.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - SpellCheck</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>

{% endhighlight %}

N> Uncompressed version of library files are also available which is used for development or debugging purpose and can be generated from the custom script [here](http://csg.syncfusion.com).


## Control Initialization

Create a div element within the body section of the HTML document, where the SpellCheck needs to be rendered.

{% highlight html %}

<body>
	<div id="SpellCheck"></div>
</body>

{% endhighlight %}

Initialize the SpellCheck control by adding the following script code to the body section of the HTML document.

{% highlight html %}
<!--Container for ejSpellCheck widget-->
<div id="SpellCheck"></div>
	
<script type="text/javascript">
$(function() { // Document is ready    
    $("#SpellCheck").ejSpellCheck();
});	
</script>

{% endhighlight %}

## Service Reference

Assign the service method (CheckWords) path reference to the property [dictionaryUrl](/api/js/ejspellcheck#members:dictionarysettings-dictionaryurl) of [`dictionarySettings`](/api/js/ejspellcheck#members:dictionarysettings), which is mandatory to check the spelling of the word.

The CheckWords method will perform the splitting of target sentence into separate words and check each word is that an erroneous or not. If the word is erroneous fetching the possible suggestions for it and returns those details as a result. 

{% highlight html %}
<!--Container for ejSpellCheck widget-->
<div id="SpellCheck"></div>
	
<script type="text/javascript">
$(function() { // Document is ready    
    $("#SpellCheck").ejSpellCheck({
        dictionarySettings: {
            dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords"
        }
    });
});	
</script>
{% endhighlight %}

## Spell Checking

To spell check the content of the target element, you need to add one button and calling any one of the SpellCheck method [showInDialog](/api/js/ejspellcheck#methods:showindialog) or [validate](/api/js/ejspellcheck#methods:validate) by clicking the button to highlight the error words.

The following code example depicts that checking the spelling of the target element through the "validate" method.

{% highlight html %}

<div id="TextArea">
  It is a concept vehicle with Liquid Silver body color, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)
  and 400  (295.02 lbf ft), diesel particulate filter and BlueTec emission control system, quattro permanent four-wheel drive system,
  Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
  MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.
</div>
<div>
      <input type="button" id="SpellCheck"/>
</div>
    
<script type="text/javascript">
            $("#TextArea").ejSpellCheck({
                 dictionarySettings: {
                     dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                     customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                 }
            });
            $("#SpellCheck").ejButton({ width: "200px", height: "25px", click: "showInContextMenu", text: "Spell check" });
            
            function showInContextMenu() {
                var spellObj = $("#TextArea").data("ejSpellCheck");
                spellObj.validate(); // highlighting the error word in the target area itself
            }
</script>

{% endhighlight %}

You can find the sample to getting start with the spellchecker [here](http://jsplayground.syncfusion.com/Sync_5c5angwy), which is prepared by following the above steps.