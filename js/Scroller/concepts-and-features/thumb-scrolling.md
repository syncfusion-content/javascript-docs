---
layout: post
title: thumb-scrolling
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


**[CSHTML]**

// In the **CSHTML** page, add a **&lt;div&gt;** element to configure **Scroller** widget and initialize the control.



&lt;div id="scrollcontent"&gt;

  &lt;div&gt;                              @*Wrapper div for Scroller.*@

     &lt;div id="innercontent"&gt;         @*Content div*@

        <h3>MVC &lt;/h3&gt;

         &lt;p&gt;

           Model–view–controller (MVC) is a software architecture pattern which   

           separates the representation of information from the user's interaction

           with it. The model consists of application data, business rules, logic, and

           functions. A view can be any output representation of data, such as a chart

           or a diagram.

         &lt;/p&gt;

    &lt;/div&gt;

  &lt;/div&gt;

&lt;/div&gt;



@{Html.EJ().Scroller("scrollcontent").Height(170).Width(350).**EnableTouchScroll(false)**.Render();}





[**ASPX**]

// In the ASPX page, add a &lt;div&gt; element to configure Scroller widget and initialize the control



&lt;div id="scrollcontent"&gt;

  &lt;div&gt;                              &lt;%--Wrapper div for Scroller.--%&gt;

     &lt;div id="innercontent"&gt;         &lt;%--Content div.--%&gt;

        <h3>MVC &lt;/h3&gt;

         &lt;p&gt;

           Model–view–controller (MVC) is a software architecture pattern which   

           separates the representation of information from the user's interaction

           with it. The model consists of application data, business rules, logic, and

           functions. A view can be any output representation of data, such as a chart

           or a diagram.

         &lt;/p&gt;

    &lt;/div&gt;

  &lt;/div&gt;

&lt;/div&gt;



&lt;ej:Scroller ID="scrollcontent" runat="server" Height="170" Width="350" EnableTouchScroll="false"&gt;&lt;/ej:Scroller&gt;





The following screenshot displays **Scroller** control with disabled touch support.

![](thumb-scrolling_images\thumb-scrolling_img1.png)

_Figure_ _6__4__:_ _Scroller_ _control with disabled touch support_

