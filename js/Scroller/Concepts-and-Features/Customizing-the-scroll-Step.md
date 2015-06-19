---
layout: post
title: Customizing-the-scroll-Step
description: customizing the scroll step
platform: js
control: Scroller
documentation: ug
---

# Customizing the scroll Step

The **Scroller** control allows you to specify the scroll movement step in a pixel value, this step value is added to the scrollbar position when you press the arrow key. Based on position value, the scrollbar moves in its corresponding orientation. You can achieve this by using **scrollOneStepBy.**

The following steps explains you the configuration of **scrollOneStepBy** property in **Scroller**. 

* In the **HTML** page, add a **&lt;div&gt;** element to configure **Scroller** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="scrollcontent"&gt;  &lt;div&gt;                              &lt;!--Wrapper div for Scroller.--&gt;     &lt;div id="innercontent"&gt;         &lt;!--Content div--&gt;        <h3>MVC &lt;/h3&gt;         &lt;p&gt;           Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart or a diagram.         &lt;/p&gt;    &lt;/div&gt;  &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;    $(function () {        $("#scrollcontent").ejScroller({                height: 170,                width: 350,<b>               scrollOneStepBy: 50</b>        });    });    &lt;/script&gt;</td></tr>
</table>


The following screenshot displays the **Scroller** control with scroll step value.



{% include image.html url="/js/Scroller/Concepts-and-Features/Customizing-the-scroll-Step_images/Customizing-the-scroll-Step_img1.png" Caption=""%}

_Figure 5: Scroller Control with scroll step value_

