---
layout: post
title: easy-customization
description: easy customization
platform: js
control: RadioButton
documentation: ug
---

# Easy Customization

## Checked status

You have options to set the state of the radio button as either checked or unchecked. When you select any option from the group of radio buttons, a dot mark appears inside the circle. This is called the **checked****state**. Previously selected radio buttons in this group are unselected that is they go to the **unchecked state**. The **checked** property is used to set the state of the radio button.

The following steps explain the details about rendering the **Radio buttonRadioButton** with the **checked** option

* In the **HTML** page, add the following input elements to configure **Radio buttonRadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_checked" /&gt;                &lt;/td&gt;                &lt;td&gt;                    <label for="Radio_checked" >Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_unchecked" /&gt;                &lt;/td&gt;                &lt;td&gt;                    <label for="Radio_unchecked">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b> [JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b> &lt;script type="text/javascript"&gt;        $(function () {            // Here we render checked and unchecked type of radio buttons in same group            // set checked state of radio button as follows            $("#Radio_checked").ejRadioButton({ name: "Gender", <b>checked: true</b> });            $("#Radio_unchecked").ejRadioButton({ name: "Gender" });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the code in CSHTML page to configure Radio Button

@* Here checked and unchecked type of radio buttons are rendered in same group

    set checked state of radio button as follows*@



    @Html.EJ().RadioButton("Radio_checked").Name("Gender").Size(RadioButtonSize.Small).**Checked(true)**

    <label for="Radio_checked" class="clslab">Male</label>

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio_unchecked").Name("Gender").Size(RadioButtonSize.Small).**Checked(false)**

    <label for="Radio_unchecked" class="clslab">Female</label>



[aspx]

// Add the code in ASPX page to configure Radio Button

  <%--Here checked and unchecked type of radio buttons are rendered in same group

    set checked state of radio button as follows--%>



    &lt;ej:RadioButton Name="Gender" ID="Radio_checked" runat="server" Size="Small" Checked="true"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio_checked" class="clslab">Male</label>

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="Radio_unchecked" runat="server" Size="Small" Checked="false"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio_unchecked" class="clslab">Female</label>



* Configure the CSS styles to align the radio buttons.



{% highlight css %}

**[CSS]**
     <style>
        .page-align {
            margin: 100px;
        }

    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img1.png" Caption="Figure 13: State of Radio buttonRadioButtons with labels"%}{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img2.png" Caption="Figure 13: State of Radio buttonRadioButtons with labels"%}

## Text

Specifies the text content for the radio button. In previous programs, separate labels were created for each radio button. But now you have the option to set the text for radio button using the **text** property. So here you do not have to add a label tag for each radio button in the **HTML** code.

The following steps explain the details about rendering the **Radio buttonRadioButton** with **text** and without using the label tag options.

* In the **HTML** page, add the following input elements to configure the **Radio buttonRadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;!--here we did not use label tag--&gt;                    &lt;input type="radio" id="RadBtn_male" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                   &lt;!-- here we did not use label tag--&gt;                    &lt;input type="radio" id="RadBtn_female" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            // radio button with text property            $("#RadBtn_male").ejRadioButton({ name: "Gender", checked: true, <b>text: "Male" </b>});            $("#RadBtn_female").ejRadioButton({ name: "Gender", <b>text: "Female"</b> });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the code in CSHTML page to configure Radio Button



@*radio button with text property*@

      @Html.EJ().RadioButton("RadBtn_male").Name("Gender").Size(RadioButtonSize.Small).Checked(true).**Text("Male")**

    &lt;br /&gt;

    @Html.EJ().RadioButton("RadBtn_female").Name("Gender").Size(RadioButtonSize.Small).Checked(false).**Text("Female")**



[aspx]

// Add the code in ASPX page to configure Radio Button



&lt;%--radio button with text property--%&gt;



   &lt;ej:RadioButton Name="Gender" ID="RadBtn_male" runat="server" Size="Small" Checked="true" Text="Male"&gt;&lt;/ej:RadioButton&gt;

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="RadBtn_female" runat="server" Size="Small" Checked="false" Text="Female"&gt;&lt;/ej:RadioButton&gt;



* Configure the CSS styles to align the radio buttons.



{% highlight css %}

**[CSS]**
   <style>
        .page-align {
            margin: 100px;
        }

    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.

{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img3.png" Caption="Figure 14: Radio buttonRadioButton with text property"%}{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img4.png" Caption="Figure 14: Radio buttonRadioButton with text property"%}

## Size

You can render the **Radio buttonRadioButton** in different sizes. There are some predefined size options available for rendering a **Radio buttonRadioButton** in an easy way. Each size option has different height and width. It mainly avoids the complexity in rendering **Radio buttonRadioButton** with complex CSS class. 

_Table_ _1__: Size_

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


The following steps explain the details about rendering **Radio buttonRadioButton** with different size options.

* In the **HTML** page, add the following input elements to configure **Radio buttonRadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table&gt;            &lt;tr&gt;                <td>Small size Radio buttons                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_Male" /&gt;                    <label for="Radio_Male">Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio_Female" /&gt;                    <label for="Radio_Female">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;        &lt;table&gt;            &lt;tr&gt;                <td>Medium size Radio buttons                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio1_Male" /&gt;                    <label for="Radio1_Male">Male</label>                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="Radio1_Female" /&gt;                    <label for="Radio1_Female">Female</label>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            // small size of radio buttons in same group                      $("#Radio_Male").ejRadioButton({ name: "Gender", <b>size: "small"</b>, checked: true });            $("#Radio_Female").ejRadioButton({ name: "Gender", <b>size: "small"</b> });            // Medium size of radio buttons in same group                      $("#Radio1_Male").ejRadioButton({ name: "Gender1", <b>size: "medium"</b>, checked: true });            $("#Radio1_Female").ejRadioButton({ name: "Gender1", <b>size: "medium"</b> });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the code in CSHTML page to configure Radio Button



@* small and medium size of radio buttons in same group

            By default, here no one radio button is checked*@



    Small size radio buttons

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio_Male").Name("Gender").**Size(RadioButtonSize.Small)**.Checked(true)

    <label for="Radio_Male" >Male</label>

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio_Female").Name("Gender").**Size(RadioButtonSize.Small)**.Checked(false)

    <label for="Radio_Female" >Female</label>

    &lt;br /&gt;

    Medium size radio buttons

    &lt;br /&gt;

      @Html.EJ().RadioButton("Radio1_Male").Name("Gender1").**Size(RadioButtonSize.Medium)**.Checked(true)

    <label for="Radio1_Male">Male</label>

    &lt;br /&gt;

    @Html.EJ().RadioButton("Radio1_Female").Name("Gender1").**Size(RadioButtonSize.Medium)**.Checked(false)

    <label for="Radio1_Female" >Female</label>



[aspx]

// Add the code in ASPX page to configure Radio Button



<%-- small and medium size of radio buttons in same group

            By default, here no one radio button is checked--%>



Small size Radio buttons

     &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="Radio_Male" runat="server" Size="Small" Checked="true"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio_Male">Male</label>

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender" ID="Radio_Female" runat="server" Size="Small"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio_Female">Female</label>

    &lt;br /&gt;



    Medium size Radio buttons

     &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender1" ID="Radio1_Male" runat="server" Size="Medium" Checked="true"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio1_Male">Male</label>

    &lt;br /&gt;

    &lt;ej:RadioButton Name="Gender1" ID="Radio1_Female" runat="server" Size="Medium"&gt;&lt;/ej:RadioButton&gt;

    <label for="Radio1_Female">Female</label>



* Configure the CSS styles to align the radio buttons.


{% highlight css %}

 **[CSS]**
   <style>
        .page-align {
            margin: 100px;
        }
    </style>


{% endhighlight %}



The following image is displayed as the output for the above steps.



{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img5.png" Caption="Figure 15: Radio button in different sizes"%}{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img6.png" Caption="Figure 15: Radio button in different sizes"%}

## RTL Support 

In some cases you need to use right-to-left alignment. You can give RTL support by using **enableRTL** property.  **RTL** mode works when you use the **text** property in **Radio buttonRadioButton**. The **Radio buttonRadioButtons** and text are aligned in the right-to-left format. For example, when text is right-aligned and Radio buttonRadioButton is left-aligned, after you apply right-to-left alignment, these positions are interchanged. 

The following steps explain the details about rendering the **Radio buttonRadioButton** with right-to-left alignment support. Here the **text** property is necessary.

* In the **HTML** page, add the following button elements to configure **Radio buttonRadioButton** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="page-align"&gt;        &lt;table class="rightAlign"&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="RadBtn_male" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td&gt;                    &lt;input type="radio" id="RadBtn_female" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control<b> </b>in<b> JavaScript</b>&lt;script type="text/javascript"&gt;        $(function () {            //set radio button with right to left format            $("#RadBtn_male").ejRadioButton({ name: "Gender", checked: true, text: "Male", <b>enableRTL: true</b> });            $("#RadBtn_female").ejRadioButton({ name: "Gender", text: "Female", <b>enableRTL: true</b> });        });    &lt;/script&gt;</td></tr>
</table>


[CSHTML]

// Add the code in CSHTML page to configure Radio Button



@*set radio button with right to left format*@

     &lt;div class="page-align"&gt;

        &lt;table class="rightAlign"&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    @Html.EJ().RadioButton("RadBtn_male").Name("Gender").Size(RadioButtonSize.Small).Checked(true).Text("Male").**EnableRTL(true)**

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    @Html.EJ().RadioButton("RadBtn_female").Name("Gender").Size(RadioButtonSize.Small).Checked(false).Text("Female").**EnableRTL(true)**

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



[aspx]

// Add the code in ASPX page to configure Radio Button



&lt;%--set radio button with right to left format--%&gt;



    &lt;div class="page-align"&gt;

        &lt;table class="rightAlign"&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="Gender" ID="RadBtn_male" runat="server" Size="Small" Text="Male" EnableRTL="true"&gt;&lt;/ej:RadioButton&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td&gt;

                    &lt;ej:RadioButton Name="Gender" ID="RadBtn_female" runat="server" Size="Small" Text="Female" EnableRTL="true"&gt;&lt;/ej:RadioButton&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt; 



In the above mentioned code, the **text** property has been used. In **LTR** format, the **Radio****bButton** is on the left side. In **RTL** format, the **Radio****buttonRadioButton** appears on the right side. Here the **text** property is used and the **enableRTL** property is set as “**True**”**.** It changes the alignment to right-to-left.

* Configure the CSS styles to align the **Radio****buttonRadioButtons.**



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



{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img7.png" Caption="Figure 16: Radio buttonRadioButton with text in RTL format"%}{% include image.html url="\js\RadioButton\concepts-and-features\easy-customization_images\easy-customization_img8.png" Caption="Figure 16: Radio buttonRadioButton with text in RTL format"%}

