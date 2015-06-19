---
layout: post
title: Scroller-Styles
description: scroller styles
platform: js
control: Scroller
documentation: ug
---

# Scroller Styles

The **Essential JavaScript****Scroller** control allows you to customize the look and function of scrollbars. You can vary it significantly by setting the scrollbar button size, scrollbar position, height and width of the **Scroller** control. This section describes you the custom styles to be used when creating **Scroller**.

## Button Size

In Scroller control, it allows you to customize the scroll arrows width and height. In horizontal **scroller** the **buttonSize** customizes the top and down arrow and in vertical **scroller** the **buttonSize** customizes the left and right arrow.

## Scroller Size

The **scrollerSize** property is used to customize the scrollbar width and height. It is applicable for both horizontal and vertical scroller.

## Scroll Top

The **scrollerTop** property is used to move the **Scroller** content and scrollbars in top position with the specified value. It is used for only vertical scroller.

## Scroll Left

The **scrollerLeft** property is used to move the **Scroller** content and scrollbars in left position with the specified value. It is used for only horizontal scroller.

## Height

The height property is used to set the height for **Scroller** outer wrapper.

## Width

The width property is used to set the width for **Scroller** outer wrapper.

The following steps explains you on how to apply styles in **Scroller** control. 

* In the **HTML** page, add a **&lt;div&gt;** element to configure **Scroller** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="scrollcontent"&gt;  &lt;div&gt;                              &lt;!--Wrapper div for Scroller.--&gt;     &lt;div id="innercontent"&gt;         &lt;!--Content div--&gt;        <h3>MVC &lt;/h3&gt;         &lt;p&gt;           Model–view–controller (MVC) is a software architecture pattern which              separates the representation of information from the user's interaction           with it. The model consists of application data, business rules, logic, and           functions. A view can be any output representation of data, such as a chart           or a diagram.         &lt;/p&gt;    &lt;/div&gt;  &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;    $(function () {        $("#scrollcontent").ejScroller({ <b>               height: 170, </b><b>               width: 350, </b><b>               scrollTop: 10, </b><b>               scrollLeft: 20, </b><b>               buttonSize: 20,</b>        });    });    &lt;/script&gt;</td></tr>
</table>


* Configure the styles 


{% highlight css %}

**[CSS]**

<style type="text/css">

    #innercontent {
        width: 400px;
        padding: 15px;
    }

    #scrollcontent {
        border: 1px solid grey;
    }

</style>


{% endhighlight %}



The following screenshot displays the **Scroller** control with basic styles

{% include image.html url="/js/Scroller/Concepts-and-Features/Scroller-Styles_images/Scroller-Styles_img1.png" Caption=""%}

_Figure 3: Scroller control rendered with basic styles_

