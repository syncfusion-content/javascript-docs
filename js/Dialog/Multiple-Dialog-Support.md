---
layout: post
title: Multiple-Dialog-Support
description: multiple dialog support
platform: js
control: Dialog
documentation: ug
---

# Multiple Dialog Support

The **Dialog** supports multiple controls in the same web page. You can use more number of **Dialog** control with different content and different functionalities in the same web page.

## Configure Multiple Dialog

The following steps explains the implementation of multiple **Dialog** in the same web page. 

In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 

{% highlight html %}



<div id="mvcDialog" title="MVC">
   <p>
      Essential Studio for ASP.NET MVC contains all the controls you need to build line-of-business web applications including grids, charts, gauges, menus, calendars, editors, and much more.
   </p>
</div>
<div id="orubaseDialog" title="Orubase">
   <p>
      Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe. 
   </p>
</div>
<div id="winrtDialog" title="WinRT">
   <p>
      Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. 
      It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.
   </p>
</div>




{% endhighlight %}

{% highlight js %}


    // Write multiple Dialog control in a single web page
    $("#mvcDialog").ejDialog({
        position: {
            X: 20,
            Y: 26
        }
    });
    $("#orubaseDialog").ejDialog({
        position: {
            X: 521,
            Y: 20
        }
    });
    $("#winrtDialog").ejDialog({
        position: {
            X: 296,
            Y: 207
        }
    });


{% endhighlight %}

The output of multiple **Dialog** control is as follows.

![]("/js/Dialog/Multiple-Dialog-Support_images/Multiple-Dialog-Support_img1.png") 

