---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: DatePicker
documentation: ug
---

# Miscellaneous

## Define height

It specifies the **height** of the **DatePicker** input text. The “**height”** property allows you to set the maximum **height** of the **DatePicker**. The value set to this property should be **string or Numer** type.

The following steps explain you how to specify the **height** of the **DatePicker** input text

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to specify the <b>height</b> of the <b>DatePicker</b> input text&lt;script type="text/javascript"&gt;        $(function () {            // declaration             $("#datepicker").ejDatePicker({             //Number<b>                height: 22</b>            });        });    &lt;/script&gt;<b>[OR]</b>&lt;script type="text/javascript"&gt;        $(function () {            // declaration             $("#datepicker").ejDatePicker({                 //String<b>                height: “22px”</b>            });        });    &lt;/script&gt;</td></tr>
</table>
## Define width

It specifies the **width** of the **DatePicker** input text. The “**width”** property allows you to set the maximum **width** of **DatePicker**. The value set to this property should be **string or Numer** type

The following steps explain you how to specify the **width** of the **DatePicker** input text

* In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to specify the <b>width</b> (Number) of the <b>DatePicker</b> input text&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({                //Number<b>                width: 200 </b>            });        });    &lt;/script&gt;</td></tr>
<tr>
<td>
     <b>[OR]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            width:"200px"        });    });    &lt;/script&gt;</td></tr>
</table>
## Highlight Section

**Highlight section** highlights the current month, current week, current workdays. You can highlight a week, month, and work days by using “**highlightSection”** property.

_Table_ _6__: Highlight Selection_

<table>
<tr>
<td>
<b>Name </b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
month</td><td>
Highlight the Current Month.</td></tr>
<tr>
<td>
week</td><td>
Highlight the Current Week.</td></tr>
<tr>
<td>
workdays</td><td>
Highlight the Current Workdays</td></tr>
<tr>
<td>
none</td><td>
Don’t Highlight Anything</td></tr>
</table>


The following steps explain you how to **highlight** the current week section

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to <b>highlight</b> the current Week in the <b>DatePicker</b> Calendar&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#datepicker").ejDatePicker({            <b>highlightSection: "week"</b>        });    });&lt;/script&gt;</td></tr>
</table>




*  The following screenshot displays the output for the above code.   

{% include image.html url="/js/DatePicker/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img1.png" Caption="Figure 26: Highlight a current week in DatePicker"%}



## ReadOnly

**Readonly** property indicates that the **DatePicker** value can only be read. You can’t edit the value in **DatePicker** and also the **DatePicker** calendar popup is not shown. By default “**readOnly**” Boolean value is set to **‘false’**.

The following steps explain you how to set the **DatePicker** value as **readonly**

* In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to set the <b>DatePicker</b> value as <b>readonly</b>&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                readOnly : true</b>            });        });&lt;/script&gt;</td></tr>
</table>
## Show Footer

It allows to **Show Footer** in **DatePicker** calendar to select today date. By default “**showFooter**” property is set as ‘**true**’ in **DatePicker** widget. You can hide footer in the **DatePicker** when this property is set to “**false**”.

The following steps explain you how to hide footer in the **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to hide footer in the <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                showFooter: false</b>            });        });    &lt;/script&gt;</td></tr>
</table>
## Show popup button

It shows the date icon button at right side of textbox and shows **DatePicker** popup on clicking it that can be achieved by using “**showPopupButton** “property. By default “**showPopupButton**” property is set as “**true**” in **DatePicker** widget. 

The following steps explain you how to hide the **popupbutton** in the **DatePicker** widget.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to hide <b>popupbutton</b> footer in the <b>DatePicker</b>&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                showPopupButton: false</b>            });        });    &lt;/script&gt;</td></tr>
</table>


* The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img2.png" Caption="Figure 27: Showpopupbutton in DatePicker"%}

## Show rounded corner

**DatePicker** input is displayed in rounded corner style, when this property is set to **‘true’**. By default “**showRoundedCorner**” property is set as “**false**” in **DatePicker** widget.

The following steps explain you how to show **Roundedcorner** in the **DatePicker**

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to show <b>Roundedcorner</b> in the <b>DatePicker</b>&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                showRoundedCorner : true</b>            });        });    &lt;/script&gt;</td></tr>
</table>


*  The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img3.png" Caption="Figure 28: Rounded corner style in DatePicker"%}

## Show Tooltip

**DatePicker****Tooltip** is displayed while you hover the date. By default “**showTooltip**” property as “**true**” in **DatePicker** widget.

The following steps explain you how to hide the **ToolTip** in the **DatePicker**.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="datepicker" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Add the code to hide the <b>ToolTip</b> in the <b>DatePicker</b> widget&lt;script type="text/javascript"&gt;        $(function () {            // declaration            $("#datepicker").ejDatePicker({<b>                showTooltip : false</b>            });        });    &lt;/script&gt;</td></tr>
</table>
* The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img4.png" Caption="Figure 29: Hide the Tooltip in DatePicker"%}













