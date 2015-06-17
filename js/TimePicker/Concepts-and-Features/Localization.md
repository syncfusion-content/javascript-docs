---
layout: post
title: Localization
description: localization
platform: js
control: TimePicker
documentation: ug
---

# Localization

**TimePicker** supports localization with different culture.

## Enabling Localization Support

The following steps explains you on how to enable **Localization** property for **TimePicker**.

* In an **HTML** page, add a **&lt;input&gt;** element to configure **TimePicker** widget.   


{% highlight html %}

         <input type="text" id="time" />


{% endhighlight %}



{% highlight html %}


**// You can enable localization property using the following code example.**

<html>
<head>
    <title>Essential Studio for JavaScript : Timepicker </title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
 <!-- Style sheet for default theme (flat azure) -->
<link href="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

   <script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js"> </script>
<script  src="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>


</head>
<body>
    <div class="content-container-fluid">      
            <div class="row">                
                <div class="cols-sample-area">                                  
<div class="frame">
                        <div class="control">
                           <input type="text" id="time" accesskey="j">
                        </div>
                    </div>		
</div>
</div>
     </div>
<script type="text/javascript">
        $(function () {
           $('#time').ejTimePicker({ 
                      locale: "zh-CN" 
                });
        });
</script>
</body>
</html>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/TimePicker/Concepts-and-Features/Localization_images/Localization_img1.png" Caption="TimePicker with zh-CN Localization"%}

