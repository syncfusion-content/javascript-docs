---
layout: post
title: Easy-Customization
description: easy customization
platform: js
control: RadioButton
documentation: ug
---

# Easy Customization

## Checked status

You have options to set the state of the radio button as either checked or unchecked. When you select any option from the group of radio buttons, a dot mark appears inside the circle. This is called the **checked****state**. Previously selected radio buttons in this group are unselected that is they go to the **unchecked state**. The **checked** property is used to set the state of the radio button.

The following steps explain the details about rendering the **RadioButton** with the **checked** option

1. In the **HTML** page, add the following input elements to configure **RadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_checked" /&gt;                &lt;/td&gt;                &lt;td&gt;                    <label for="Radio_checked" >Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_unchecked" /&gt;                &lt;/td&gt;                &lt;td&gt;                    <label for="Radio_unchecked">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b> [JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b> &lt;script type="text/javascript"&gt;        $(function () {            // Here we render checked and unchecked type of radio buttons in same group            // set checked state of radio button as follows            $("#Radio_checked").ejRadioButton({ name: "Gender", <b>checked: true</b> });            $("#Radio_unchecked").ejRadioButton({ name: "Gender" });        });    &lt;/script&gt;</td></tr>
</table>


2. Configure the CSS styles to align the radio buttons.



{% highlight css %}

**[CSS]**
     <style>
        .page-align {
            margin: 100px;
        }

    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



{% include image.html url="/js/RadioButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img1.png" Caption="State of RadioButtons with labels"%}

## Text

Specifies the text content for the radio button. In previous programs, separate labels were created for each radio button. But now you have the option to set the text for radio button using the **text** property. So here you do not have to add a label tag for each radio button in the **HTML** code.

The following steps explain the details about rendering the **RadioButton** with **text** and without using the label tag options.

1. In the **HTML** page, add the following input elements to configure the **RadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;!--here we did not use label tag--&gt;                    &lt;input type="radio" id="RadBtn_male" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                   &lt;!-- here we did not use label tag--&gt;                    &lt;input type="radio" id="RadBtn_female" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            // radio button with text property            $("#RadBtn_male").ejRadioButton({ name: "Gender", checked: true, <b>text: "Male" </b>});            $("#RadBtn_female").ejRadioButton({ name: "Gender", <b>text: "Female"</b> });        });    &lt;/script&gt;</td></tr>
</table>


2. Configure the CSS styles to align the radio buttons.



{% highlight css %}

**[CSS]**
   <style>
        .page-align {
            margin: 100px;
        }
    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.

{% include image.html url="/js/RadioButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img2.png" Caption="RadioButton with text property"%}

## Size

You can render the **RadioButton** in different sizes. There are some predefined size options available for rendering a **RadioButton** in an easy way. Each size option has different height and width. It mainly avoids the complexity in rendering **RadioButton** with complex CSS class. 

_Size_

<table>
<tr>
<td>
<b>Property	</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
small</td><td>
Creates radio button with inbuilt small size height, width specified.</td></tr>
<tr>
<td>
medium</td><td>
Creates radio button with inbuilt medium size height, width specified.</td></tr>
</table>


The following steps explain the details about rendering **RadioButton** with different size options.

3. In the HTML page, add the following input elements to configure RadioButton widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                <td>Small size Radio buttons                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_Male" /&gt;                    <label for="Radio_Male">Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_Female" /&gt;                    <label for="Radio_Female">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;        &lt;table&gt;            &lt;tr&gt;                <td>Medium size Radio buttons                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio1_Male" /&gt;                    <label for="Radio1_Male">Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio1_Female" /&gt;                    <label for="Radio1_Female">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            // small size of radio buttons in same group                      $("#Radio_Male").ejRadioButton({ name: "Gender", <b>size: "small"</b>, checked: true });            $("#Radio_Female").ejRadioButton({ name: "Gender", <b>size: "small"</b> });            // Medium size of radio buttons in same group                      $("#Radio1_Male").ejRadioButton({ name: "Gender1", <b>size: "medium"</b>, checked: true });            $("#Radio1_Female").ejRadioButton({ name: "Gender1", <b>size: "medium"</b> });        });    &lt;/script&gt;</td></tr>
</table>


4. Configure the CSS styles to align the radio buttons.


{% highlight css %}

 **[CSS]**
   <style>
        .page-align {
            margin: 100px;
        }
    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



{% include image.html url="/js/RadioButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img3.png" Caption="Radio button in different sizes"%}

## RTL Support 

In some cases you need to use right-to-left alignment. You can give RTL support by using **enableRTL** property.  **RTL** mode works when you use the **text** property in **RadioButton**. The **RadioButtons** and text are aligned in the right-to-left format. For example, when text is right-aligned and RadioButton is left-aligned, after you apply right-to-left alignment, these positions are interchanged. 

The following steps explain the details about rendering the **RadioButton** with right-to-left alignment support. Here the **text** property is necessary.

1. In the HTML page, add the following button elements to configure RadioButton widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table class="rightAlign"&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="RadBtn_male" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="RadBtn_female" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //set radio button with right to left format            $("#RadBtn_male").ejRadioButton({ name: "Gender", checked: true, text: "Male", <b>enableRTL: true</b> });            $("#RadBtn_female").ejRadioButton({ name: "Gender", text: "Female", <b>enableRTL: true</b> });        });    &lt;/script&gt;</td></tr>
</table>


In the above mentioned code, the **text** property has been used. In **LTR** format, the **RadioButton** is on the left side. In **RTL** format, the **RadioButton** appears on the right side. Here the **text** property is used and the **enableRTL** property is set as “**True**”**.** It changes the alignment to right-to-left.

2. Configure the CSS styles to align the RadioButtons.



{% highlight css %}

**[CSS]**
  <style>
        .page-align {
            margin: 100px;
        }
        .rightAlign {
            text-align: right;
        }
    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



{% include image.html url="/js/RadioButton/Concepts-and-Features/Easy-Customization_images/Easy-Customization_img4.png" Caption="RadioButton with text in RTL format"%}

