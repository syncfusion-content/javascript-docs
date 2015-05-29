---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: MaskEdit
documentation: ug
---

# Behavior Settings

**Decimal Places**

The command **decimalPlaces** declares the decimal point to the value of **Textbox** controls. The default value of **decimalPlaces** is 0 in **Textbox** controls.

**Configure Decimal Places**

The following steps explain the implementation of **decimalPlaces** in **Textboxes**.

In the **View** page use the corresponding Textbox helper****for rendering **Textbox** controls. 





**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**DecimalPlaces(3)**.Value("333")

@Html.EJ().PercentageTextbox("percent").**DecimalPlaces(2)**.Value("22")

@Html.EJ().CurrencyTextbox("currency").**DecimalPlaces(4)**.Value("555")







The output for **Textbox** with **decimalPlaces** is as follows.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img1.png" Caption="Figure 13: Textbox with decimalPlaces"%}

## Persistence Support

The MaskEditTextBox control provides state maintenance support. You can maintain the previous changes made in the control after a page loads. By default, the ‘**enablePersistence**’ property is set to ‘**false**’ in the **MaskEdit**.

The following steps explain the **State Maintenance** in the **MaskEdit** control.

1.  1.	In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 

2. The **Textbox** widgets provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

3. **Configure Persistence Support** 

4. The following steps explain the implementation of **enablePersistence** in **Textboxes**.

5. In the **View** page add MaskEditTextBox helper, and configure the **EnablePersistence** property as shown below.In the **View** page use the corresponding Textbox helper****for rendering **Textbox** controls. 



<table>
<tr>
<td>
6. <b>[HTML]</b>7.        &lt;table cellpadding="10"&gt;8.             &lt;tbody&gt;9.                 &lt;tr&gt;10.                     &lt;td&gt;11.                         <label for="numeric">Numeric</label>12.                     &lt;/td&gt;13.                     &lt;td&gt;14.                         &lt;input id="numeric" type="text" /&gt;15.                     &lt;/td&gt;16.                 &lt;/tr&gt;17.                 &lt;tr&gt;18.                     &lt;td&gt;19.                         <label for="percent">Percent</label>20.                     &lt;/td&gt;21.                     &lt;td&gt;22.                         &lt;input id="percent" type="text" /&gt;23.                     &lt;/td&gt;24.                 &lt;/tr&gt;25.                 &lt;tr&gt;26.                     &lt;td&gt;27.                         <label for="currency">Currency</label>28.                     &lt;/td&gt;29.                     &lt;td&gt;30.                         &lt;input id="currency" type="text" /&gt;31.                     &lt;/td&gt;32.                 &lt;/tr&gt;33.                 &lt;tr&gt;34.                     &lt;td&gt;35.                         <label for="maskedit">Mask Edit</label>36.                     &lt;/td&gt;37.                     &lt;td&gt;38.                         &lt;input id="maskedit" type="text" /&gt;39.                     &lt;/td&gt;40.                 &lt;/tr&gt;41.             &lt;/tbody&gt;42.         &lt;/table&gt;</td></tr>
<tr>
<td>
43. <b>[JavaScript]</b>44. // Set the <b>enablePersistence </b>property<b> </b>as<b> “True</b>” to the <b>Textbox</b> controls. The default value for <b>enablePersistence </b>is “<b>False</b>”45.     &lt;script type="text/javascript"&gt;46.         /* Numeric Textbox */47.         $("#numeric").ejNumericTextbox({48.             value: 11,49.             <b>enablePersistence: true</b>50.         });51.         /* Percent Textbox */52.         $("#percent").ejPercentageTextbox({53.             value: 22,54. <b>            enablePersistence: true</b>55.         });56.         /* Currency Textbox */57.         $("#currency").ejCurrencyTextbox({58.             value: 33,59. <b>            enablePersistence: true</b>60.         });61.         /* MaskEdit Textbox */62.         $("#maskedit").ejMaskEdit({                      63.             maskFormat: "99-999-99999",            64. <b>           enablePersistence: true</b>65.         });66.     &lt;/script&gt;</td></tr>
</table>


67. **[_cshtml]**

68. @* **Add the following code in your view page to render Textbox controls.***@



69.  @Html.EJ().NumericTextbox("numeric").Value("11").**EnablePersistence**(**true**)

70. @Html.EJ().PercentageTextbox("percent").Value("22").**EnablePersistence**(**true**)

71. @Html.EJ().CurrencyTextbox("currency").Value("33").**EnablePersistence**(**true**)

72. @Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**EnablePersistence**(**true**)





<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to enable the enablePersistence property of the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>enablePersistence: true,</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

 &lt;ej:NumericTextBox ID="numeric"  Value="11" EnablePersistence="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="22" EnablePersistence="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="33" EnablePersistence="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" EnablePersistence="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output of MaskEditTextBox with **eEnablePersistence** is as follows. 



1. {% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img2.png" Caption="Figure 4: MaskEditTextBox at initial load"%}

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img3.png" Caption="Figure 5: MaskEditTextBox after changing the value and after page refresh "%}

The output for **Textboxes** with **enablePersistence** is as follows. You can change the value of **Textboxes** and reload the web page.



2. {% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img4.png" Caption="Figure 14: Textboxes at initial load"%}

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img5.png" Caption="Figure 15: Textboxes after changing the value and a page load "%}

**Strict Mode Support**

The **Textbox** widget allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. When the Textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the Textbox value goes below **minValue**, it restricts the new value and returns the **minValue**.

**Configure Strict Mode Support** 

The following steps explain the implementation of **enableStrictMode** in **Textboxes**.

1. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableStrictMode </b>property<b> </b>as<b> “True</b>” to the <b>Textbox</b> controls. The default value for <b>enableStrictMode </b>is “<b>False</b>”    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11, //value(11) exceeds maxValue(5), so it will returns 5.<b>            minValue: -3,</b><b>            maxValue:5,</b><b>            enableStrictMode: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: -10,//value(-10) is under minValue(-5),so it will returns -5.<b>            minValue: -5,</b><b>            maxValue: 3,</b><b>            enableStrictMode: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 10, //value(10) exceeds maxValue(8), so it will returns 8.<b>            minValue: -1,</b><b>            maxValue: 8,</b><b>            enableStrictMode: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").MinValue(-3).MaxValue(5).**EnableStrictMode**(**true**)

@Html.EJ().PercentageTextbox("percent").MinValue(-5).MaxValue(3).**EnableStrictMode**(**true**)

2. @Html.EJ().CurrencyTextbox("currency").MinValue(-1).MaxValue(8).**EnableStrictMode**(**true**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  MinValue="-3" MaxValue="5" EnableStrictMode="true" runat="server" &gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  MinValue="5" MaxValue="8" EnableStrictMode="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  MinValue="-1" MaxValue="8" EnableStrictMode="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **Textboxes** when **enableStrictMode** is **“True”** is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img6.png" Caption="Figure 16: Textboxes with enableStrictMode"%}

## Enabled or Disabled

MaskEditTextBox has an option to enable or disable its element. You can set the **eEnabled** property as “**fFalse**” to enable the TextboxMaskEdit controls.

The **Textbox** control has an option to enable or disable its element. You can set the **enabled** property as “**True**” to enable the Textbox controls.

The following steps explain the **enabled** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to enable the enabled property of the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>enabled: false,</b>        });    });&lt;/script&gt;</td></tr>
</table>
**Configure Enabled or Disabled** 

The following steps explains the implementation of **enabled** in **Textboxes**.

3. In the **View** page add MaskEditTextBox helper, and configure the **Enabled** property.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enabled </b>property<b> </b>as<b> “True</b>” to the <b>Textbox</b> controls. The default value for <b>enabled</b> is true    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,<b>            enabled: true</b>                   });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,<b>            enabled: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>enabled: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({                                  maskFormat: "99-999-99999",                       <b>enabled: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**Enabled**(**true**)

@Html.EJ().PercentageTextbox("percent").Value("2").**Enabled**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("3").**Enabled**(**true**)

@Html.EJ().MaskEdit("mask").**Enabled**(**truefalse**).MaskFormat("99-999-99999")





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Value="1" Enabled="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="2" Enabled="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="3" Enabled="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Enabled="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output when **eEnabled** is **“falseTrue”** and when **eEnabled** is “**Falstrue**”**.**

4. {% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img7.png" Caption="The output for Textboxes when enabled is “True” and when enabled is “False”."%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img8.png" Caption="Figure 6:  17: TextboxesMaskEdit with enabled as falseTrue"%}



![](behavior-settings_images\behavior-settings_img9.png)

_Figure_ _18__7__:_ _Textboxes__MaskEdit_ _with enabled as_ _F__alse__true_

## Adjusting TextboxMaskEdit Size

**MaskEditTextBox** The **Textbox** size can be modified by using the **hHheight** and **wWwidth** properties. You can customize the size of **Textbox****MaskEdit** by using these properties.

**Configure Height and Width** 

The following steps explain the implementation of **height** and **width** in **Textboxes**.

MaskEditTextBox size can be modified by using the **Height** and **Width** properties. 

5. . 

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>height </b>and<b> width </b>property<b> </b>to the Textbox controls. The default value of <b>height</b> and <b>width</b> is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>            width: 100, height: 20           </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({<b>            width: 100, height: 20</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({<b>            width: 100, height: 20</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({<b>            width: 100, height: 20,</b>            maskFormat: "99-999-99999"                           });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]** 

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**Width**("100").**Height**("20")

@Html.EJ().PercentageTextbox("percent").**Width**("100").**Height**("20")

@Html.EJ().CurrencyTextbox("currency").**Width**("100").**Height**("20")

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**Width**("100").**Height**("520")

The following steps explain the **width** and **height** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to customize the MaskEdit control with height and width property.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>width: 150,</b><b>            height: 50</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Width="100" Height="20" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Width="100" Height="20" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Width="100" Height="20" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Width="100" Height="20" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output of MaskEditTextBox after setting “**hHeight**” and “**wWidth**” is as follows**.**



![](behavior-settings_images\behavior-settings_img10.png)

Figure 8: MaskEditTextBox with height and width                          The output for **Textboxes** after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img11.png" Caption="Figure 19: Textboxes with height and width                          		"%}

**Increment Step**

The **incrementStep** property is used to increase or decrease the amount of value in the Textbox controls. 

**Configure Increment Step**

The following steps explain the implementation of **incrementStep** in **Textboxes**.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls.

6. 

<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>incrementStep </b>property<b> </b>to the <b>Textbox</b> controls. The default value of <b>incrementStep </b>is 1    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value:1,<b>           incrementStep: 2       </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value:1,            <b>incrementStep: 3</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value:1,<b>           incrementStep: 4</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**IncrementStep**(**2**).Value("1")

@Html.EJ().PercentageTextbox("percent").**IncrementStep**(**3**).Value("1")

7. @Html.EJ().CurrencyTextbox("currency").**IncrementStep**(4**)**.Value("1")



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" IncrementStep="2" Value="1"  runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  IncrementStep="3" Value="1" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  IncrementStep="4" Value="1"  runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **Textboxes** with **incrementStep** is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img12.png" Caption="Figure 20: Textboxes at initial load"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img13.png" Caption="Figure 21: Textboxes after increasing one step"%}

**Define Name**

When you have placed the **Textboxes** in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

**Configure Name**

The following steps explain the implementation of **name** in **Textboxes**.

1. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls.

2. 

<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>name </b>property<b> </b>to the <b>Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>name: "numeric"            </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>name: "percent"         </b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            <b>name: "currency"            </b>        });         &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**Name**("**Numeric**")

@Html.EJ().PercentageTextbox("percent").**Name**("**Percentage**")

3. @Html.EJ().CurrencyTextbox("currency").**Name**("**Currency**")



**[aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Name="numeric" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Name="percentage" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Name="currency" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **Textboxes** with the **name** property is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img14.png" Caption="Figure 22: Textboxes with name"%}

## Define Value

The value of **MaskEditTextBox** can be assigned by using the **vValue** property. The default value for v**Value** property is null.

The value of **Textboxes** can be assigned by using the **value** property. The default value for **value** property is null.

The following steps explain the **value** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to customize the MaskEdit control with value property.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            <b>value: "1234567890",</b>        });    });&lt;/script&gt;</td></tr>
</table>
**Configure Value**

The following steps explain the implementation of **value** in **Textboxes**.

1. In the **View** page add MaskEditTextBox helper, and configure the **Value** property In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;               &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>value </b>property<b> </b>to the <b>Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>value: 12                 </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>value: 21               </b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            <b>value: 33              </b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            <b>value: 1234567890</b>        });     &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**Value**("**12**")

@Html.EJ().PercentageTextbox("percent").**Value**("**21**")

@Html.EJ().CurrencyTextbox("currency").**Value**("**33**")

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**Value**("**1234567890**")





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Value="12" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="21" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="33" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="Mask" MaskFormat="99-999-99999" Value="1234567890" runat="server"&gt;&lt;/ej:MaskEdit&gt;]



Output of MaskEditTextBox with the **value** property is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img15.png" Caption="The output for Textboxes with the value property is as follows."%}

{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img16.png" Caption="Figure 239: Textboxes MaskEditTextBox with value"%}

**Define maxValue and minValue**

**maxValue**

The maximum limit value can be assigned to the **Textboxes** by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

**minValue**

The minimum limit value can be assigned to the **Textboxes** by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

**Configure maxValue and minValue**

The following steps explain the implementation of **maxValue** and **minValue** in **Textboxes**.

1. In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls.

2. 

<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maxValue, </b>and<b> minValue </b>properties<b> </b>to the <b>Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({<b>            maxValue: 2,</b><b>            minValue: -1,</b>            value:2        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({<b>            maxValue: 3,</b><b>            minValue: -2,</b>            value:3        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({<b>            maxValue: 4,</b><b>            minValue: -3,</b>            value:4        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("2").**MinValue**(-**1**).**MaxValue**(**2**)

@Html.EJ().PercentageTextbox("percent").Value("3").**MinValue**(-**2**).**MaxValue**(**3**)

3. @Html.EJ().CurrencyTextbox("currency").Value("4").**MinValue**(-**3**).**MaxValue**(**4**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="2" MinValue="-1" MaxValue="2" runat="server" &gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="3" MinValue="-2" MaxValue="3" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="4" MinValue="-3" MaxValue="4" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;





The output for **Textboxes** with basic properties is as follows**.**



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img17.png" Caption="Figure 24: Textboxes with maxValue"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img18.png" Caption="Figure 25: Textboxes with minValue"%}

## Read Only Support

**MaskEditTextBox** supports read only option. When you enable the **rReadOnly** property to the control, the value cannot be changed in the **MaskEditTextBox**. You can set the **rReadOnly** property as “**tTrue”** to enable this option.

The following steps explain the **readOnly** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;nput i="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to customize the MaskEdit control with readOnly property.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            value: "123456",            <b>readOnly: true</b>        });    });&lt;/script&gt;</td></tr>
</table>
The **Textbox** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the **Textboxes**. You can set the **readOnly** property as “**True”** to enable this option.

 **Configure Read Only**

The following steps explain the implementation of **readOnly** in **Textboxes**.

4. In the **View** page add MaskEditTextBox helper, and configure the **ReadOnly** property.

1.  In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>readOnly </b>property as “<b>True” </b>to the <b>Textbox</b> controls. The default value of <b>readOnly</b> property is false    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                       value: 1,<b>            readOnly: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,           <b> readOnly: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,<b>            readOnly: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>readOnly: true,</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**ReadOnly**(**true**)

@Html.EJ().PercentageTextbox("percentage").Value("2").**ReadOnly**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("3").**ReadOnly**(**true**)

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("123456").**ReadOnly**(**true**)





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="1" ReadOnly="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage"  Value="2" ReadOnly="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="3" ReadOnly="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="123456" ReadOnly="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



Output of **MaskEditTextBox** when r**ReadOnly** is “**tTrue**” is as follows**.** MaskEditTextBox values cannot be edited or changed.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img19.png" Caption="Figure 10: MaskEditTextBox with readOnly		"%}

The output for **Textboxes** when **readOnly** is “**True**” is as follows**.** The **Textbox** values cannot be edited or changed.



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img20.png" Caption="Figure 26: Textboxes with readOnly		"%}

## Error Visibility

The **Mask Edit TextBbox** has an option that shows the error value with red colored text. It is used to validate the Mask Edit value. You can set the **sSshowError** property as “**tTrue”** to enable this option.

**Configure Error Visibility**

The following steps explain the implementation of **showError** in **Mask Edit Textbox**.

2. In the **View** page use the corresponding Textbox helper****for rendering **Textbox** controls. 

1. In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showError </b>property as “<b>True” </b>to the <b>Mask Edit Textbox</b> control. The default value of <b>showError </b>property is false    &lt;script type="text/javascript"&gt;        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>showError: true,</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("123456").**ShowError**(**true**)



The following steps explain the **showError** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input id="maskedit" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Add the following code example to enable the showError property of the MaskEdit control.&lt;script type="text/javascript"&gt;    $(function () {        $("#maskedit").ejMaskEdit(        {            name: "mask",            inputMode: ej.InputMode.Text,            maskFormat: "99-999-99999",            value: "123456",            <b>showError: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="123456" ShowError="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The oOutput for **MaskEditTextBox****Textboxes** when **sSshowError** is “**tTrue**” is as follows**.** 



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img21.png" Caption="Figure 2117: Textbox with showError"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img22.png" Caption="Figure 2117: Textbox with showError"%}



{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img23.png" Caption="Figure 2128: Textbox without error"%}{% include image.html url="\js\MaskEdit\concepts-and-features--maskedittextbox\behavior-settings_images\behavior-settings_img24.png" Caption="Figure 2128: Textbox without error"%}

