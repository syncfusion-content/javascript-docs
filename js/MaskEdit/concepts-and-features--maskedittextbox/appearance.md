---
layout: post
title: appearance
description: appearance
platform: js
control: MaskEdit
documentation: ug
---

# Appearance

## Theme

The **MaskEditTextBox****Textbox** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Textbox** control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **MaskEditTextbox** control namely:

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

## CSS Class

The **CSS** can be customized by using the **cCssClass** in the **MaskEditTextBox**. You can customize the **MaskEditTextBox** with **cCssClass** property to appear like your desired control.

The following steps explain the implementation of MaskEdit with **cssClass** property.

In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget. 

The **CSS** can be customized by using the **cssClass** in the **Textboxes**. You can customize the **Textboxes** with various **cssClass** properties to appear like your desired control.

**Configure CSS Class**

The following steps explain the implementation of **cssClass** in **Textboxes**.

In the **View** page add MaskEditTextBox helper, and configure the **CssClass** property. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass </b>property as custom CSS class name<b> </b>to the <b>Textbox</b> controls. The default value of <b>cssClass</b> property is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>cssClass: "customCss"</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>cssClass: "customCss"</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>cssClass: "customCss"</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>cssClass: "customCss",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;<b> [_cshtml] </b>@*<b> Add the following code in your view page to render Textbox controls.</b>*@@Html.EJ().NumericTextbox("numeric").Value("1").<b>CssClass</b>("<b>customCss</b>")@Html.EJ().PercentageTextbox("percentage").Value("2").<b>CssClass</b>("<b>customCss</b>")@Html.EJ().CurrencyTextbox("currency").Value("3").<b>CssClass</b>("<b>customCss</b>")@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("123456").<b>CssClass</b>("<b>customCss</b>")</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>cssClass: "customCss"</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" cssClass="customCss" Value="1"  runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="2" cssClass="customCss" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="3" cssClass="customCss" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="123456" cssClass="customCss" runat="server"&gt;&lt;/ej:MaskEdit&gt;

* Customize the CSS properties in custom CSS class.



{% highlight css %}

**[CSS]**

    <style>
        .customCss .e-box {
            border-color: #9d241b;
        }
        .customCss .e-input {
            background-color: #f6db8d;            
        }
        .customCss .e-select {
            background-color: #ecf6ac;
            border-color: #3c36e7;
        }
    </style>



{% endhighlight %}



The output for MaskEditTextBox Textboxes after applying **cCcssClass** is as follows.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img1.png" Caption="Figure  1834: Textboxes MaskEdit with cssClass"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img2.png" Caption="Figure  1834: Textboxes MaskEdit with cssClass"%}

## Rounded Corner Support

MaskEditTextBox provides you with rounded corner support whose appearance is different from normal textbox controls.

The following steps explain the implementation of MaskEdit with **showRoundedCorner** property.



In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget

The **Textbox** provides you with rounded corner support whose appearance is different from normal textbox controls.

**Configure Rounded Corner Support**

The following steps explain the implementation of **showRoundedCorner** in **Textboxes**.

In the **View** page add MaskEditTextBox helper, and configure the **ShowRoundedCorner** property. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as “<b>True”</b> in the <b>Textbox</b> controls. The default value for <b>showRoundedCorner</b> property is false in <b>Textboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showRoundedCorner: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showRoundedCorner: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>showRoundedCorner: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>showRoundedCorner: true,</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;<b>[_cshtml] </b>@*<b> Add the following code in your view page to render Textbox controls.</b>*@@Html.EJ().NumericTextbox("numeric").Value("1").<b>ShowRoundedCorner</b>(<b>true</b>)@Html.EJ().PercentageTextbox("percentage").Value("2").<b>ShowRoundedCorner</b>(<b>true</b>)@Html.EJ().CurrencyTextbox("currency").Value("3").<b>ShowRoundedCorner</b>(<b>true</b>)@Html.EJ().MaskEdit("mask").Value("123456").<b>ShowRoundedCorner</b>(<b>true</b>)</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>showRoundedCorner: true,</b>            value: "123456"        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="1" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="2" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"   Value="3" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999"  Value="123456" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output of MaskEditTextBox when **sShowRoundedCorner** is “**tTrue**”.

The output for Textboxes when **showRoundedCorner** is “**True**”.





{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img3.png" Caption="Figure 3519: Textboxes MaskEdit with showRoundedCorner"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img4.png" Caption="Figure 3519: Textboxes MaskEdit with showRoundedCorner"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img5.png" Caption="Figure 3519: Textboxes MaskEdit with showRoundedCorner"%}

**Spin Button Support**

The **Textbox** provides you the option as to whether to display the split button in the widget or remove it from the control by using **showSpinButton** property.

**Configure Spin Button**

The following steps explain the implementation of **showSpinButton** in **Textboxes**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showSpinButton</b> property as “<b>True”</b> in the <b>Textbox</b> controls. The default value for <b>showSpinButton</b> property is true in <b>Textboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showSpinButton: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showSpinButton: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>showSpinButton: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**ShowSpinButton**(**true**)

@Html.EJ().PercentageTextbox("percentage").Value("2").**ShowSpinButton**(**true**)

1. @Html.EJ().CurrencyTextbox("currency").Value("3").**ShowSpinButton**(**true**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="1" ShowSpinButton="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="2" ShowSpinButton="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"   Value="3" ShowSpinButton="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **Textboxes** when **showSpinButton** is “**True**”.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img6.png" Caption="Figure 36: Textboxes with showSpinButton is True"%}

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img7.png" Caption="Figure 37: Textboxes with showSpinButton is False"%}

## Waterm Mark Text Support

The **Textboxes MaskEdit** control provide water mark text support. You can display the initial value in the control by water mark.

The following steps explain the implementation of MaskEdit with **watermarkText** property.

In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget.

**Configure Water Mark Text**

The following steps explain the implementation of **watermarkText** in **Textboxes**.

1. In the **View** page use the corresponding Textbox helper****for rendering **Textbox** controls. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>watermarkText</b> in the <b>Textbox</b> controls. The default value for <b>watermarkText</b> property is empty string (“”) in <b>Textboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                        <b>watermarkText: "Numeric"</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({                       <b>watermarkText: "Percentage"</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({                       <b>watermarkText: "Currency"</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({                        <b>watermarkText: "MaskEdit",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;<b>[_cshtml]</b>@*<b> Add the following code in your view page to render Textbox controls.</b>*@@Html.EJ().NumericTextbox("numeric").<b>WatermarkText</b>("<b>Numeric</b>")@Html.EJ().PercentageTextbox("percentage").<b>WatermarkText</b>("<b>Percentage</b>")@Html.EJ().CurrencyTextbox("currency").<b>WatermarkText</b>("<b>Currency</b>")2. @Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").<b>WatermarkText</b>("<b>MaskEdit</b> ")</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>watermarkText: "Enter the Mask"</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" WaterMarkText="Numeric" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" WaterMarkText="Percentage" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency" WaterMarkText="Currency" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" WaterMarkText="MaskEdit" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output of MaskEditTextBox when **sShowRoundedCorner** is “**tTrue**”.

The output for **Textboxes** after applying **watermarkText** is as follows.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img8.png" Caption="Figure 3820: Textboxes MaskEditTextBox  with watermark text"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img9.png" Caption="Figure 3820: Textboxes MaskEditTextBox  with watermark text"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img10.png" Caption="Figure 3820: Textboxes MaskEditTextBox  with watermark text"%}

## Text Alignment Support

The **Mask Edit TextBbox** provides text alignment support that allows you to set the alignment of text in the control by using the **tTtextAlign** property.

The following steps explain the implementation of MaskEdit with **textAlign** property.

* In the HTML page, add a &lt;div&gt; element to render the MaskEdit widget

**Configure Text Alignment**

The following steps explain the implementation of **textAlign** in **Textboxes**.

1. In the **View** page use the corresponding MaskEdit helper****for rendering **MaskEdit** control. In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>textAlign</b> property in the <b>Textbox</b> controls. The default value for <b>textAlign</b> property is left in <b>Textboxes</b>    &lt;script&gt;/* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 12345677,            <b>textAlign: "right",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;<b>[_cshtml]</b>@*<b> Add the following code in your view page to render Textbox controls.</b>*@@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("12345677").<b>TextAlign</b>(<b>TextAlign.Right</b>)</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to render the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>textAlign: ej.TextAlign.Right</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="12345677" TextAlign="Right" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for Textboxes when t**TtextAlign** is set to **“right”**.

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img11.png" Caption="Figure 21: MaskEdit with textAlign"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img12.png" Caption="Figure 21: MaskEdit with textAlign"%}

_Figure_ _3__21__9__:_ _MaskEdit Textbox__MaskEdit__TextBox_ _with textAlign_



**HTML Attributes Support**

2. The **MaskEditTextBox** provides support for adding HTML attributes to the component. ‘**HtmlAttributes**’ property is used to add HTML attributes like, id, class etc.. to the components. We need to use **IDictionary<string,object>** to specify the HTML attributes. Please check the below code.

**Configure HTMLAttributes property**



1. In the **View** page add MaskEditTextBox helper, and configure the **HtmlAttributes**property. Here we have added the [Access key](http://en.wikipedia.org/wiki/Access_key) attribute. While pressing the “AccessKey” and “J” keys, MaskEditTextBox will gain focus.



**[_cshtml]**

@{IDictionary<string, object> maskAttribute = new Dictionary<string, object>();

maskAttribute.Add("accesskey", "j");

}



3. @Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").HtmlAttributes(maskAttribute)





2. Add the following JavaScript code to focus the MaskEditTextBox

**[JavaScript]**



    &lt;script type="text/javascript"&gt;

    $(function () {

        $(document).on("keydown", function (e) {

            if (e.altKey && e.keyCode === 74) { // j- key code.

                $("#mask").focus();

            }

        });

    });

&lt;/script&gt;



3. The output for MaskEditTextBox after configuring the **HtmlAttributes** property

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\appearance_images\appearance_img13.png" Caption="Figure 22: MaskEditTextBox with focus"%}





