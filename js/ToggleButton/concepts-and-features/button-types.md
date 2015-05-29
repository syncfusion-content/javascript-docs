---
layout: post
title: button-types
description: button types
platform: js
control: Toggle Button
documentation: ug
---

# Button types

**Toggle Button** is used as normal clickable button, submitting form data, resetting the form data to its initial value. According to the usage of button, you can render the **Toggle Button** in the following three types by using the **type** property.

_Table_ _5__: Toggle Button Types_

<table>
<tr>
<td>
<b>button</b></td><td>
The button is a clickable button </td></tr>
<tr>
<td>
<b>submit</b></td><td>
The button is a submit button (submits form-data)</td></tr>
<tr>
<td>
<b>reset    </b></td><td>
The button is a reset button (resets the form-data to its initial values)</td></tr>
</table>


The following steps explains you the details about rendering the **Toggle Button** with above mentioned types. 

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;table&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="type_button" /&gt;                         &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="type_submit" /&gt;                            &lt;/td&gt;        &lt;/tr&gt;        &lt;tr&gt;            &lt;td class="btnsht"&gt;                &lt;input type="checkbox" id="type_mini" /&gt;                            &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>//Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;      $(function () {          //type property is used to render different type of toggle buttons          $("#type_button").ejToggleButton({              size: "mini",<b>              type: "button",</b>              showRoundedCorner: true,              defaultText: "Play",              activeText: "Next",          });          $("#type_submit").ejToggleButton({              size: "mini",<b>              type: "submit",</b>              showRoundedCorner: true,              defaultText: "submit",              activeText: "submited",          });          $("#type_mini").ejToggleButton({              size: "mini",<b>              type: "reset",</b>              showRoundedCorner: true,              defaultText: "reset",              activeText: "reseted",          });      });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

//Add the code in CSHTML page to configure the widget and initialize the control



    &lt;div class="one"&gt;

        @*set toggle button type using type property*@

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td class="btnsht"&gt;

                    @Html.EJ().ToggleButton("toggleButton_button").Size(ButtonSize.Mini).ShowRoundedCorner(true).ContentType(ContentType.TextOnly).DefaultText("button").ActiveText("Next").**Type(ButtonType.Button)**

                &lt;/td&gt;

                &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="btnsht"&gt;

                    @Html.EJ().ToggleButton("toggleButton_submit").Size(ButtonSize.Mini).ShowRoundedCorner(true).ContentType(ContentType.TextOnly).DefaultText("submit").ActiveText("Next")**.Type(ButtonType.Submit)**

                &lt;/td&gt;

                &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td class="btnsht"&gt;

                    @Html.EJ().ToggleButton("toggleButton_reset").Size(ButtonSize.Mini).ShowRoundedCorner(true).ContentType(ContentType.TextOnly).DefaultText("reset").ActiveText("Next")**.Type(ButtonType.Reset)**

                &lt;/td&gt;



            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



**[aspx]**

// Add the code in ASPX page to configure Toggle Button widget

&lt;%--set toggle button type using type property--%&gt;



    &lt;ej:ToggleButton ID="ToggleButton" runat="server" Size="Mini" ShowRoundedCorner="true" DefaultText="button" ActiveText="done" Type="Button"&gt;&lt;/ej:ToggleButton&gt;

    &lt;br /&gt;

    &lt;ej:ToggleButton ID="Submit_ToggleButton" runat="server" Size="Mini" ShowRoundedCorner="true" DefaultText="submit" ActiveText="done" Type="Submit"&gt;&lt;/ej:ToggleButton&gt;

    &lt;br /&gt;

    &lt;ej:ToggleButton ID="Reset_ToggleButton" runat="server" Size="Mini" ShowRoundedCorner="true" DefaultText="reset" ActiveText="done" Type="Reset"&gt;&lt;/ej:ToggleButton&gt;



Execute the above code to render the following output.

![](button-types_images\button-types_img1.png)

_Figure_ _17__11__: Types of Toggle button_

