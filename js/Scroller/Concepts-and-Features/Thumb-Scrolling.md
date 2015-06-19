---
layout: post
title: Thumb-Scrolling
description: thumb scrolling
platform: js
control: Scroller
documentation: ug
---

# Thumb Scrolling

Normally the scrollbar position can be changed by dragging the scrollbar handle or clicking the arrows. The **Scroller** control allows you for panning or dragging the scroll content area to drag by dragging inside the scroll content. To achieve this in your **Scroller** control, enable the **enableTouchScroll** to true_._ By default the value for__**enableTouchScroll** is true. When you want to prevent the panning or dragging the scroll content area, set **enableTouchScroll** as false.

The following steps explains you the configuration of **enableTouchScroll** property in **Scroller**. 

* In the **HTML** page, add a **&lt;div&gt;** element to configure **Scroller** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="scrollcontent"&gt;  &lt;div&gt;                              &lt;!--Wrapper div for Scroller.--&gt;     &lt;div id="innercontent"&gt;         &lt;!--Content div--&gt;        <h3>MVC &lt;/h3&gt;         &lt;p&gt;           Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart           or a diagram.         &lt;/p&gt;    &lt;/div&gt;  &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b> &lt;script type="text/javascript"&gt;    $(function () {        $("#scrollcontent").ejScroller({                height: 170,                width: 350,<b>               enableTouchScroll: false</b>        });    });    &lt;/script&gt;</td></tr>
</table>


The following screenshot displays **Scroller** control with disabled touch support.

{% include image.html url="/js/Scroller/Concepts-and-Features/Thumb-Scrolling_images/Thumb-Scrolling_img1.png" Caption=""%}

_Figure 4: Scroller control with disabled touch support_

