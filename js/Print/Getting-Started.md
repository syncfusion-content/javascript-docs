---
layout: post
title: Getting Started with Print widget for Essential JS
description: How to use the Print widget with the step-by-step instructions.
platform: js
control: Print
documentation: ug
keywords : ejPrint, js print, print, web print, essential javascript print, print widget,
---

# Getting Started

This section explains briefly about how to use the **Print** widget on your application. It allows either printing of an entire page or specific elements alone from a page. 

## Including Script and CSS

To get start with Print, create a new HTML file and add the required dependent CSS as well as script files to it.

**CSS file**

* [ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css) – includes all the widgets styles.

**External script files**

* [jQuery 1.7.1](http://jquery.com/#) and later versions.
* [jQuery.easing.js](http://gsgd.co.uk/sandbox/jquery/easing/#) - to support the animation effects.

**Internal script files**

<table>
<tr>
<th>
File</th><th>
Description</th></tr>
<tr>
<td>
ej.core.min.js<br/><br/></td><td>
Must be referred always before using all the JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.print.min.js<br/><br/></td><td>
The Print source file<br/><br/></td></tr>
</table>

The above mentioned internal script files can be individually referred on an application, if the Print control alone needs to be used. If in case, other controls also needs to be used on your application - then it is necessary to make use of the ‘ej.web.all.min.js’ file which encapsulates all the `ej` components and frameworks in a single file.

[ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js) – includes scripts of all widgets.


N>  In production, we highly recommend you to use our [custom script generator](http://helpjs.syncfusion.com/js/include-only-the-needed-widgets) to create custom script file with required controls and its dependencies only. Also to reduce the file size further, please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) in your server. 


Add reference links of the [CDN](http://helpjs.syncfusion.com/js/cdn) for the script and CSS file dependencies in the `head` section.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Print</title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>


{% endhighlight %}


## Using Print widget

To Print a Grid control, first the grid control needs to be defined and rendered on the page properly. Refer to the following code example.


{% highlight html %}

    <div id="control">
        <div id="Grid"></div>
    </div>
    <script>
        $(function () {
            $("#Grid").ejGrid({
                dataSource: shipDetails
            });
        });
        var shipDetails = [
              { Name: 'Hanari Carnes', City: 'Brazil' },
              { Name: 'Split Rail Beer & Ale', City: 'USA' },
              { Name: 'Ricardo Adocicados', City: 'Brazil' }
        ];
    </script>


{% endhighlight %}

Keep a separate button on a page and on it's click action, call the `ejPrint` function as depicted in the below code example to print the entire grid control.

{% highlight html %}

    <div id="control">
        <div id='Grid'></div>
        <br />
        <button class="button" id="print">Print the Grid</button>
    </div>
   

{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $('#Grid').ejGrid({
                dataSource: shipDetails
            });
            $("#print").ejButton({
                size: "normal", width: "113px", click: "onPrintPage"
            });
        })
        var shipDetails = [
              { Name: 'Hanari Carnes', City: 'Brazil' },
              { Name: 'Split Rail Beer & Ale', City: 'USA' },
              { Name: 'Ricardo Adocicados', City: 'Brazil' }
        ];
        function onPrintPage(e) {
            var ele = $("#Grid");
            if (!ele.hasClass("e-print")) {
                $("#Grid").ejPrint();
            } else {
                obj = $("#Grid").ejPrint("instance");
                obj.print();
            }
        }
        
{% endhighlight %}


