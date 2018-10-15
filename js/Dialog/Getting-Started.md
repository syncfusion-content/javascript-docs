---
layout: post
title: Getting Started with Dialog widget for Essential JS
description: How to create Dialog widget with the step-by-step instructions.
platform: js
control: Dialog
documentation: ug
keywords : ejdialog, js dialog, jquery dialog, dialog, dialog ui, web dialog, ej dialog, essential javascript dialog, dialog widget,
api: /api/js/ejdialog
---

# Getting Started

This section helps to understand the getting started of the Dialog widget with the step-by-step instructions.

## Script/CSS reference

Create a new HTML file and include the below code

{% highlight html %}
 
<!DOCTYPE html>
<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
</head>
<body>

</body>
</html> 


{% endhighlight %}



Add link to the CSS file from the specific [theme](https://help.syncfusion.com/js/theming-in-essential-javascript-components) folder to your HTML file within the head section. 

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Dialog </title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
</head>


{% endhighlight %}



Add links to the [CDN](https://help.syncfusion.com/js/cdn) Script files with dependencies.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Dialog</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>


{% endhighlight %}



N>To reduce the file size further please use [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) compression in your server. 
{%seealso%}[custom script generator](https://help.syncfusion.com/js/custom-script-generator) {%endseealso%}

## Create Dialog

Add a div element in the &lt;body&gt; tag as below.

{% highlight html %}

        <div id="dialog">

        </div>  


{% endhighlight %}



Initialize the Dialog widgets by adding the script section as below.

{% highlight javascript %}

        $(function () {
            $("#dialog").ejDialog();
        });


{% endhighlight %}



![Create Dialog](getting-started_images\getting-started_img1.png)

### Add dialog content

Add the contents for the dialog as below.

{% highlight html %}

        <div id="dialog">
            <!--dialog content-->
            <p>This is a simple dialog</p>
        </div>


{% endhighlight %}



![Add dialog content](getting-started_images\getting-started_img2.png)

### Set the title

To set the title to Dialog widget’s using [title](https://help.syncfusion.com/api/js/ejdialog#members:title) property as follows.

{% highlight javascript %}

        $(function () {
            $("#dialog").ejDialog({ title: "Dialog" });
        });


{% endhighlight %}



N>The title can be also set through the title attribute for the dialog’s div element (&lt;div id="dialog" title="Dialog"&gt;)

![Set the title](getting-started_images\getting-started_img3.png)

### Open Dialog dynamically

In most cases, the Dialog widgets are needed only in dynamic actions like showing some messages on clicking a button, to provide alert, etc. So the Dialog widget provides [open](https://help.syncfusion.com/api/js/ejdialog#methods:open) and [close](https://help.syncfusion.com/api/js/ejdialog#methods:close) methods to open/close the dialogs dynamically.

The Dialog widget can be hidden on initialize using [showOnInit](https://help.syncfusion.com/api/js/ejdialog#members:showoninit) property which should be set to false. 

Refer the below example. The dialog will be opened on clicking the Button widget. 

{%seealso%} [Button](http://docs.syncfusion.com/js/button/overview)
{%endseealso%}

{% highlight html %}


    <!--button widget-->
    <button id="button">Open Dialog</button>

    <div id="dialog" title="Dialog">
        <!--dialog content-->
        <p>This is a Dialog</p>
    </div>
    <script>
        $(function () {
            //create button widget
            $("#button").ejButton({ click: "openDialog" });
            //create dialog widget
            $("#dialog").ejDialog({ showOnInit: false });
        });
        function openDialog() {
            $("#dialog").ejDialog("open");
        }
    </script>


{% endhighlight %}



![Open-Dialog-dynamically](getting-started_images\getting-started_img4.png)

