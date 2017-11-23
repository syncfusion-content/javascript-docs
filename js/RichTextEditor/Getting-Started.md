---
layout: post
title: Getting started with RichTextEditor widget for Syncfusion Essential JS
description: Getting started with RichTextEditor and configure the toolbar and other functionalities.
platform: js
control: RTE
documentation: ug
keywords: RichTextEditor, Control Initialization, Setting and Getting Content
api: /api/js/ejrte
---
# Getting Started

This section helps to understand the getting started of RTE control with the step-by-step instruction.

## Script and CSS reference

Create a new HTML file and include the below code

{% highlight html %}

<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
</head>
<body>

</body>
</html>
{% endhighlight %}

Add link to the CSS file from the specific theme folder to your HTML file within the head section. Refer the built-in available themes from [here](https://help.syncfusion.com/js/theming-in-essential-javascript-components#). 

{% highlight html %}
<head>
   <meta charset ="utf-8" />
   <title>Getting Started - RichTextEditor</title>
   <link href ="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
</head>
{% endhighlight %}

Also add links to the [CDN](https://help.syncfusion.com/js/cdn#) Script files along with the other external dependencies as depicted below,

{% highlight html %}
<head>
   <meta charset="utf-8" />
   <title>Getting Started - RichTextEditor</title>
   <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
   <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
   <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
   <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
   <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
{% endhighlight %}

N> Uncompressed version of the required library files are available for the development or debugging purpose which can be generated from the custom script [here](http://csg.syncfusion.com/#). Also to reduce the file size further please use [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) compression in your server.

## Control Initialization

Create a **TextArea** element within the body of the HTML document where the widget needs to be rendered.

{% highlight html %}
<body>
   <textarea id ="editor"></textarea>
</body>
{% endhighlight %}

Initialize the editor by adding the following script to the HTML document.

{% highlight html %}
<body>
   <textarea id="editor"></textarea>
   
   <script type="text/javascript">
        $(function () {
            $("#editor").ejRTE();
        });
   </script>
</body>
{% endhighlight %}

## Toolbar–Configuration

You can configure a toolbar with the tools using [tools](https://help.syncfusion.com/api/js/ejrte#members:tools) and [toolsList](https://help.syncfusion.com/api/js/ejrte#members:toolslist) properties as your application requires.

{% highlight javascript %}
$(function () {
$("#editor").ejRTE({
toolsList: ["style", "lists", "doAction", "links", "images"],
tools: {
style: ["bold", "italic"],
lists: ["unorderedList", "orderedList"],
doAction: ["undo", "redo"],
links: ["createLink"],
images: ["image"]
}
});
});
{% endhighlight %}

## Setting and Getting Content

You can set the content of the editor using [value](https://help.syncfusion.com/api/js/ejrte#members:value) as follows.

{% highlight javascript %}

<textarea id="editor"></textarea>
   
<script type="text/javascript">
    $("#editor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
        " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
    });
</script>
{% endhighlight %}

To retrieve the editor contents,

{% highlight javascript %}
var currentValue = $("#editor").ejRTE("model.value");
{% endhighlight %}

You can find sample to quick start with the editor [here](http://jsplayground.syncfusion.com/Sync_nenmojvz#).

