---
layout: post
title: How to - Tab widget for Syncfusion Essential JS
description: How To Section in Tab widget for Syncfusion Essential JS
platform: js
control: Tab
documentation: ug
keywords: Tab, height, customization
api: /api/js/ejtab
---

# How To

## Set 100% height to tab content.

You can set the height of tab control to the parent element's height by setting the `heightAdjustMode` property value as `fill`. Hence, please set the static height for the parent element so that heightAdjustMode will work.

{% highlight html %}

    <div id="Tab" style="background-Color:#F3D5AE; position:absolute; height:100%">
    <ul>
        <li>
            <a href="#tools">Essential Tools</a>
        </li>
        <li>
            <a href="#chart">Essential Chart</a>
        </li>
    </ul>
     <div id="tools" style="background-Color:#DCF8FA">
        Essential Tools is an collection of user interface components used to create interactive
        ASP.NET MVC applications. 
     </div>
     <div id="chart">
        Essential Chart is a business-oriented charting component. It offers an innovative
        data object model that makes it easy to populate the chart with any kind of data
        source.
     </div>
    </div>
{% endhighlight %}

{% highlight javascript %}
 
      <script type="text/javascript">
        $(function () {
            // declaration
            $("#Tab").ejTab({ heightAdjustMode: "fill"});
         });
      </script>

{% endhighlight %}

Refer to the sample [here](http://jsplayground.syncfusion.com/zzmrhmwa)

