---
layout: post
title: localization
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

**[HTML]**
         <input type="text" id="time" />


{% endhighlight %}



**JavaScript]**

**// You can enable localization property using the following code example.**



&lt;html&gt;

&lt;head&gt;

    <title>Essential Studio for JavaScript : Timepicker &lt;/title&gt;

    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  /&gt;

 &lt;!-- Style sheet for default theme (flat azure) --&gt;

&lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;



    &lt;!--Scripts--&gt;

    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"&gt;&lt;/script&gt;



    &lt;script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"&gt;&lt;/script&gt;



   &lt;script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/cultures/globalize.cultures.js"&gt; &lt;/script&gt;

&lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt;&lt;/script&gt;





&lt;/head&gt;

&lt;body&gt;

    &lt;div class="content-container-fluid"&gt;      

            &lt;div class="row"&gt;                

                &lt;div class="cols-sample-area"&gt;                                  

&lt;div class="frame"&gt;

                        &lt;div class="control"&gt;

                           &lt;input type="text" id="time" accesskey="j"&gt;

                        &lt;/div&gt;

                    &lt;/div&gt;		

&lt;/div&gt;

&lt;/div&gt;

     &lt;/div&gt;

&lt;script type="text/javascript"&gt;

        $(function () {

           $('#time').ejTimePicker({ 

                      locale: "zh-CN"“zh-CN” 

                });

        });

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



**[_cshtml]**

**// Add the following code in your view page to render TimePicker with Spanish****culture**.



         @Html.EJ().TimePicker("time").**Locale("es-ES")**



**[_**aspx**]**

**//** Add the code in ASPX page to render TimePicker

     &lt;ej:TimePicker ID="time" Locale="zh-CN" runat="server"&gt;&lt;/ej:TimePicker&gt;



Execute the above code to render the following output.

![](localization_images\localization_img1.png)

_Figure_ _8__21__:_ _TimePicker_ _with_ _zh__-CN Localization_

