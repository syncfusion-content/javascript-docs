---
layout: post
title: rtl
description: rtl
platform: js
control: Scroller
documentation: ug
---

# RTL

**enableRTL** API provides right-to-left functionality and features for languages that work in a right-to-left for selecting, editing. Arabic and Hebrew are written from right to left. If you have a working style from right to left, you can use this feature in scroller. You can achieve this in your **Scroller** by using **enableRTL** property. Setting this property to true, the Scroller content text is displayed in the right to left format. The vertical scrollbar move to right to left side.

The following steps explains you the configuration of **enableRTL** property in **Scroller**.

* In the **HTML** page, add a **&lt;div&gt;** element to configure **Scroller** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="scrollcontent"&gt;  &lt;div&gt;                              &lt;!--Wrapper div for Scroller.--&gt;     &lt;div id="innercontent"&gt;         &lt;!--Content div--&gt;        <h3>MVC &lt;/h3&gt;         &lt;p&gt;           Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart or a diagram.         &lt;/p&gt;    &lt;/div&gt;  &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>&lt;script type="text/javascript"&gt;    $(function () {        $("#scrollcontent").ejScroller({                height: 170,                width: 350, <b>               enableRTL: true</b>        });    });    &lt;/script&gt;</td></tr>
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



@{Html.EJ().Scroller("scrollcontent").Height(170).Width(350).EnableRTL(true).Render();}



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



&lt;ej:Scroller ID="scrollcontent" runat="server" Height="170" Width="350" EnableRTL="true"&gt;&lt;/ej:Scroller&gt;



The following screenshot displays the **Scroller** control in **RTL** direction.

![](rtl_images\rtl_img1.png)

_Figure_ _8__6__:_ _Scroller_ _control in RTL direction_



