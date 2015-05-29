---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: Editors NumericTextbox
documentation: ug
---

# Behavior Settings

## Decimal Places

**decimalPlaces** property specifies number of values allowed after the decimal point.The default value of **decimalPlaces** property is 0 i.e., by default you cannot specify decimal value in NumericTextBox. We need to add this property to allow decimal values.

The command **decimalPlaces** declares the decimal point to the value of **Textbox** controls. The default value of **decimalPlaces** is 0 in **Textbox** controls.

### Configure Decimal Places

The following steps explain the implementation of **decimalPlaces** in **NumericTextBox Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>decimalPlaces</b> value in the Numeric Textbox <b>Textbox</b> control    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 333,<b>            decimalPlaces: 3</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,<b>            decimalPlaces: 2</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 555,<b>            decimalPlaces: 4</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**DecimalPlaces(3)**.Value("333")

@Html.EJ().PercentageTextbox("percent").**DecimalPlaces(2)**.Value("22")

@Html.EJ().CurrencyTextbox("currency").**DecimalPlaces(4)**.Value("555")





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" DecimalPlaces="3" Value="333" runat="server" &gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent" DecimalPlaces="2" Value="22" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency" DecimalPlaces="4" Value="555" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **NumericTextBox****Textbox** with **decimalPlaces** is as follows.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img1.png" Caption="Figure 513: NumericTextBox Textbox with decimalPlaces"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img2.png" Caption="Figure 513: NumericTextBox Textbox with decimalPlaces"%}

## Persistence Support

The **NumericTextBox****Textbox** widgets provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

### Configure Persistence Support 

The following steps explain the implementation of **enablePersistence** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enablePersistence </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox Textbox</b> controls. The default value for <b>enablePersistence </b>is “<b>False</b>”    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11,            <b>enablePersistence: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,<b>            enablePersistence: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 33,<b>            enablePersistence: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({                                  maskFormat: "99-999-99999",            <b>           enablePersistence: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@



 @Html.EJ().NumericTextbox("numeric").Value("11").**EnablePersistence**(**true**)

@Html.EJ().PercentageTextbox("percent").Value("22").**EnablePersistence**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("33").**EnablePersistence**(**true**)

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**EnablePersistence**(**true**)





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

 &lt;ej:NumericTextBox ID="numeric"  Value="11" EnablePersistence="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="22" EnablePersistence="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="33" EnablePersistence="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" EnablePersistence="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for **NumericTextBox Textboxes** with **enablePersistence** is as follows. You can change the value of **NumericTextBox Textboxes** and reload the web page.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img3.png" Caption="Figure 6: NumericTextBox at initial load"%}

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img4.png" Caption="Figure 7: NumericTextBox after changing the value and after page refresh "%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img5.png" Caption="Figure 614: Textboxes at initial load"%}

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img6.png" Caption="Figure 715: Textboxes after changing the value and a page load "%}

## Strict Mode Support

NumericTextBox allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. Default value of this property is **false**. When the textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the textbox value goes below **minValue**, it restricts the new value and returns the **minValue**. When this property is enabled, it will not restrict the specified value and an error class will be added to indicate wrong value is provided to the NumericTextBox.

The **Textbox** widget allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. When the Textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the Textbox value goes below **minValue**, it restricts the new value and returns the **minValue**.

### Configure Strict Mode Support 

The following steps explain the implementation of **enableStrictMode** in **NumericTextBox Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableStrictMode </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox Textbox</b> controls. The default value for <b>enableStrictMode </b>is “<b>False</b>”    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 101, //value(101) exceeds maxValue(5), so it will returns 5.<b>            minValue: -3,</b><b>            maxValue:5,</b><b>            enableStrictMode: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: -10,//value(-10) is under minValue(-5),so it will returns -5.<b>            minValue: -5,</b><b>            maxValue: 3,</b><b>            enableStrictMode: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 10, //value(10) exceeds maxValue(8), so it will returns 8.<b>            minValue: -1,</b><b>            maxValue: 8,</b><b>            enableStrictMode: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").MinValue(-3).MaxValue(5).**EnableStrictMode**(**true**)

@Html.EJ().PercentageTextbox("percent").MinValue(-5).MaxValue(3).**EnableStrictMode**(**true**)

@Html.EJ().CurrencyTextbox("currency").MinValue(-1).MaxValue(8).**EnableStrictMode**(**true**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  MinValue="-3" MaxValue="5" EnableStrictMode="true" runat="server" &gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  MinValue="5" MaxValue="8" EnableStrictMode="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  MinValue="-1" MaxValue="8" EnableStrictMode="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **NumericTextBox Textboxes** when **enableStrictMode** is **“True”** is as follows**.**



![](behavior-settings_images\behavior-settings_img7.png)

![](behavior-settings_images\behavior-settings_img8.png)



_Figure_ _8__16__:_ _NumericTextBox__****__Textboxes_ _with enableStrictMode_

## Enabled or Disabled

The NumericTextBox **Textbox** control has an option to enable or disable its element. You can set the **enabled** property as “**True**” to enable the NumericTextBox****Textbox controls.

### Configure Enabled or Disabled 

The following steps explains the implementation of **enabled** in **NumericTextBox Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td   &gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enabled </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox Textbox</b> controls. The default value for <b>enabled</b> is true    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,<b>            enabled: true</b>                   });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,<b>            enabled: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>enabled: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({                                  maskFormat: "99-999-99999",                       <b>enabled: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**Enabled**(**true**)

@Html.EJ().PercentageTextbox("percent").Value("2").**Enabled**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("3").**Enabled**(**true**)

@Html.EJ().MaskEdit("mask").**Enabled**(**true**).MaskFormat("99-999-99999")





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Value="1" Enabled="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="2" Enabled="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="3" Enabled="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Enabled="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for **NumericTextBox Textboxes** when **enabled** is **“True”** and when **enabled** is “**False**”**.**





{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img9.png" Caption="Figure 9: NumericTextBox with enabled as False"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img10.png" Caption="Figure 10: NumericTextBox with enabled as True"%}

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img11.png" Caption="Figure 917: Textboxes with enabled as True"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img12.png" Caption="Figure 180: Textboxes with enabled as False"%}

## Adjusting Textbox Size

The **NumericTextBox****Textbox** size can be modified by using the **height** and **width** properties. You can customize the size of NumericTextBox **Textbox** by using these properties.

### Configure Height and Width 

The following steps explain the implementation of **height** and **width** in NumericTextBox **Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering NumericTextBox **Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>height </b>and<b> width </b>property<b> </b>to the NumericTextBox Textbox controls. The default value of <b>height</b> and <b>width</b> is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>            width: 100, height: 520,value:1           </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({<b>            width: 100, height: 20</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({<b>            width: 100, height: 20</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({<b>            width: 100, height: 20,</b>            maskFormat: "99-999-99999"                           });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**Width**("100").**Height**("20")

@Html.EJ().PercentageTextbox("percent").**Width**("100").**Height**("20")

@Html.EJ().CurrencyTextbox("currency").**Width**("100").**Height**("20")

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**Width**("100").**Height**("20")



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Width="100" Height="20" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Width="100" Height="20" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Width="100" Height="20" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Width="100" Height="20" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for NumericTextBox **Textboxes** after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img13.png" Caption="Figure 191: NumericTextBox Textboxes with height and width                          		"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img14.png" Caption="Figure 191: NumericTextBox Textboxes with height and width                          		"%}

## Increment Step

The **incrementStep** property is used to increase or decrease the amount of value in the NumericTextBox Textbox controls. 

### Configure Increment Step

The following steps explain the implementation of **incrementStep** in NumericTextBox **Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering NumericTextBox **Textbox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>incrementStep </b>property<b> </b>to the <b>NumericTextBox Textbox</b> controls. The default value of <b>incrementStep </b>is 1    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value:1,<b>           incrementStep: 2       </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value:1,            <b>incrementStep: 3</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value:1,<b>           incrementStep: 4</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**IncrementStep**(**2**).Value("1")

@Html.EJ().PercentageTextbox("percent").**IncrementStep**(**3**).Value("1")

@Html.EJ().CurrencyTextbox("currency").**IncrementStep**(4**)**.Value("1")



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" IncrementStep="2" Value="1"  runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  IncrementStep="3" Value="1" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  IncrementStep="4" Value="1"  runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



Output of Numeric textbox with **incrementStep** is as follows**.**



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img15.png" Caption="Figure 12: NumericTextBox at initial load"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img16.png" Caption="Figure 13: NumericTextBox after increasing two step"%}

The output for **Textboxes** with **incrementStep** is as follows**.**



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img17.png" Caption="Figure 120: Textboxes at initial load"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img18.png" Caption="Figure 213: Textboxes after increasing one step"%}

## Define Name

When you have placed the **NumericTextBox****Textboxes** in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

### Configure Name

The following steps explain the implementation of **name** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>name </b>property<b> </b>to the <b>NumericTextBox Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value:12,<b>name: "numeric"            </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>name: "percent"         </b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            <b>name: "currency"            </b>        });         &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**Name**("**Numeric**")

@Html.EJ().PercentageTextbox("percent").**Name**("**Percentage**")

@Html.EJ().CurrencyTextbox("currency").**Name**("**Currency**")



**[aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric"  Name="numeric" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Name="percentage" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Name="currency" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **NumericTextBox****Textboxes** with the **name** property is as follows**.**



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img19.png" Caption="Figure 1422: NumericTextBox Textboxes with name"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img20.png" Caption="Figure 1422: NumericTextBox Textboxes with name"%}

## Define Value

The value of **NumericTextBox****Textboxes** can be assigned by using the **value** property. The default value for **value** property is null.

### Configure Value

The following steps explain the implementation of **value** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;               &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>value </b>property<b> </b>to the <b>NumericTextBox Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>value: 12                 </b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>value: 21               </b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            <b>value: 33              </b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            <b>value: 1234567890</b>        });     &lt;/script&gt;</td></tr>
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



The output for **NumericTextBox****Textboxes** with the **value** property is as follows**.**

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img21.png" Caption="Figure 1523: NumericTextBox Textboxes with value"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img22.png" Caption="Figure 1523: NumericTextBox Textboxes with value"%}

## Define maxValue and minValue

### maxValue

The maximum limit value can be assigned to the **NumericTextBox****Textboxes** by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

### minValue

The minimum limit value can be assigned to the **NumericTextBox****Textboxes** by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

### Configure maxValue and minValue

The following steps explain the implementation of **maxValue** and **minValue** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maxValue, </b>and<b> minValue </b>properties<b> </b>to the <b>NumericTextBox Textbox</b> controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({<b>            maxValue: 2,</b><b>            minValue: -1,</b>            value:2        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({<b>            maxValue: 3,</b><b>            minValue: -2,</b>            value:3        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({<b>            maxValue: 4,</b><b>            minValue: -3,</b>            value:4        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("2").**MinValue**(-**1**).**MaxValue**(**2**)

@Html.EJ().PercentageTextbox("percent").Value("3").**MinValue**(-**2**).**MaxValue**(**3**)

@Html.EJ().CurrencyTextbox("currency").Value("4").**MinValue**(-**3**).**MaxValue**(**4**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="2" MinValue="-1" MaxValue="2" runat="server" &gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percent"  Value="3" MinValue="-2" MaxValue="3" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"  Value="4" MinValue="-3" MaxValue="4" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;





The output for **NumericTextBox****Textboxes** with basic properties is as follows**.**

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img23.png" Caption="Figure 16: NumericTextBox with maxValue"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img24.png" Caption="Figure 17: NumericTextBox with minValue"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img25.png" Caption="Figure 1624: Textboxes with maxValue"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img26.png" Caption="Figure 1725: Textboxes with minValue"%}

## Read Only Support

The **NumericTextBox****Textbox** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the NumericTextBox Textboxes. You can set the **readOnly** property as “**True”** to enable this option.

### Configure Read Only

The following steps explain the implementation of **readOnly** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>readOnly </b>property as “<b>True” </b>to the <b>NumericTextBox Textbox</b> controls. The default value of <b>readOnly</b> property is false    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                       value: 1,<b>            readOnly: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,           <b> readOnly: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,<b>            readOnly: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>readOnly: true,</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
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



The output for NumericTextBox **Textboxes** when **readOnly** is “**True**” is as follows**.** The NumericTextBox **Textbox** value s cannot be edited or changed.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img27.png" Caption="Figure 1826: NumericTextBox Textboxes with readOnly		"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img28.png" Caption="Figure 1826: NumericTextBox Textboxes with readOnly		"%}

**Error Visibility**

The **Mask Edit Textbox** has an option that shows the error value with red colored text. It is used to validate the Mask Edit value. You can set the **showError** property as “**True”** to enable this option.

**Configure Error Visibility**

The following steps explain the implementation of **showError** in **Mask Edit Textbox**.

* In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



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





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="123456" ShowError="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for **Textboxes** when **showError** is “**True**” is as follows**.** 



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img29.png" Caption="Figure 1927: Textbox with showError"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img30.png" Caption="Figure 280: Textbox without error"%}

**Mask Edit Properties**

**Custom Character**

The **Mask Edit** allows you to use the custom character option. The specified character is allowed to enter in the Mask Edit Textbox by using the **customCharacter** property.

**Hide Prompt On Leave**

The **Mask Edit Textbox** provides the option to hide the prompt when you focus out from the control. The mask prompt is visible when you focus again to the control. The default value of **hidePromptOnLeave** is false.

**Input Mode**

The **Mask Edit** supports two type of inputs such as text and password that have been assigned by using the enum values **ej.InputMode.Text** and **ej.InputMode.Password**. The default value for **inputMode** is text in **Mask Edit**.

**Mask Format**

The **Mask Edit** provides the option to define the **maskFormat** to the value. The default value for **maskFormat** property is empty string.

The following steps explain the implementation of **Mask Edit Properties**.

* In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maskEdit</b> property in the <b>ejMaskEdit</b> function    &lt;script type="text/javascript"&gt;        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            <b>            customCharacter: "r",           </b><b>            hidePromptOnLeave: true,</b><b>            inputMode: ej.InputMode.Text,</b><b>            maskFormat: "99-999-CCCC"</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@{Html.EJ().MaskEdit("mask")

.**MaskFormat**("99-999-CCCC").**CustomCharacter**("r").

**HidePromptOnLeave**(true).**InputMode**(InputMode.Text).Render();}





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-CCCC" CustomCharacter="r" HidePromptOnLeave="true" InputMode="Text"  runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for **Mask Edit Textbox** with its properties is as follows.

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img31.png" Caption="Figure 291: MaskEdit with maskFormat"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img32.png" Caption="Figure 2230: MaskEdit with hidePromtOnLeave"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img33.png" Caption="Figure 2331: MaskEdit with prompt focus"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img34.png" Caption="Figure 2432: MaskEdit with inputMode text"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img35.png" Caption="Figure 2533: MaskEdit with customCharacter"%}

## Appearance

### Theme

The NumericTextBox **Textbox** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the NumericTextBox **Textbox** control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Textbox** control namely:

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

### CSS Class

The **CSS** can be customized by using the **cssClass** in the NumericTextBox **Textboxes**. You can customize the NumericTextBox **Textboxes** with various **cssClass** properties to appear like your desired control.

### Configure CSS Class

The following steps explain the implementation of **cssClass** in NumericTextBox **Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass </b>property as custom CSS class name<b> </b>to the <b>NumericTextBox Textbox</b> controls. The default value of <b>cssClass</b> property is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>cssClass: "customCss"</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>cssClass: "customCss"</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>cssClass: "customCss"</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>cssClass: "customCss",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**CssClass**("**customCss**")

@Html.EJ().PercentageTextbox("percentage").Value("2").**CssClass**("**customCss**")

@Html.EJ().CurrencyTextbox("currency").Value("3").**CssClass**("**customCss**")

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("123456").**CssClass**("**customCss**")



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



The output for NumericTextBox Textboxes after applying **cssClass** is as follows.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img36.png" Caption="Figure 261934: NumericTextBox Textboxes with cssClass"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img37.png" Caption="Figure 261934: NumericTextBox Textboxes with cssClass"%}

## Rounded Corner Support

The NumericTextBox **Textbox** provides you with rounded corner support whose appearance is different from normal textbox controls.

**Configure Rounded Corner Support**

The following steps explain the implementation of **showRoundedCorner** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as “<b>True”</b> in the <b>NumericTextBox Textbox</b> controls. The default value for <b>showRoundedCorner</b> property is false in <b>NumericTextBoxTextboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showRoundedCorner: true</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showRoundedCorner: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>showRoundedCorner: true</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 123456,            <b>showRoundedCorner: true,</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**ShowRoundedCorner**(**true**)

@Html.EJ().PercentageTextbox("percentage").Value("2").**ShowRoundedCorner**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("3").**ShowRoundedCorner**(**true**)

@Html.EJ().MaskEdit("mask").Value("123456").**ShowRoundedCorner**(**true**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="1" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="2" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"   Value="3" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999"  Value="123456" ShowRoundedCorner="true" runat="server"&gt;&lt;/ej:MaskEdit&gt;





The output for NumericTextBox Textboxes when **showRoundedCorner** is “**True**”.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img38.png" Caption="Figure 272035: NumericTextBox Textboxes with showRoundedCorner"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img39.png" Caption="Figure 272035: NumericTextBox Textboxes with showRoundedCorner"%}

## Spin Button Support

The NumericTextBox **Textbox** provides you the option as to whether to display the split button in the widget or remove it from the control by using **showSpinButton** property.

### Configure Spin Button

The following steps explain the implementation of **showSpinButton** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showSpinButton</b> property as “<b>True”</b> in the <b>NumericTextBox Textbox</b> controls. The default value for <b>showSpinButton</b> property is true in <b>NumericTextBoxTextboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showSpinButton: falsetrue</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showSpinButton: true</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({            value: 3,            <b>showSpinButton: true</b>        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").Value("1").**ShowSpinButton**(**true**)

@Html.EJ().PercentageTextbox("percentage").Value("2").**ShowSpinButton**(**true**)

@Html.EJ().CurrencyTextbox("currency").Value("3").**ShowSpinButton**(**true**)



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" Value="1" ShowSpinButton="true" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" Value="2" ShowSpinButton="true" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency"   Value="3" ShowSpinButton="true" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;



The output for **NumericTextBox****Textboxes** when **showSpinButton** is “**TrueFalse**”.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img40.png" Caption="Figure 21: NumericTextBox with showSpinButton is False"%}



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img41.png" Caption="Figure 3628: Textboxes with showSpinButton is True"%}

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img42.png" Caption="Figure 2937: Textboxes with showSpinButton is False"%}

## Water Mark Text Support

The NumericTextBox Textboxes provide water mark text support. You can display the initial value in the control by water mark.

### Configure Water Mark Text

The following steps explain the implementation of **watermarkText** in **NumericTextBox****Textboxes**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox****Textbox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="numeric">Numeric</label>                    &lt;/td&gt;                    &lt;td&gt;                          &lt;input id="numeric" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="currency">Currency</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="currency" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>watermarkText</b> in the <b>NumericTextBox Textbox</b> controls. The default value for <b>watermarkText</b> property is empty string (“”) in <b>NumericTextBoxTextboxes</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                        <b>watermarkText: "Numeric"</b>        });        /* Percent Textbox */        $("#percent").ejPercentageTextbox({                       <b>watermarkText: "Percentage"</b>        });        /* Currency Textbox */        $("#currency").ejCurrencyTextbox({                       <b>watermarkText: "Currency"</b>        });        /* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({                        <b>watermarkText: "MaskEdit",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().NumericTextbox("numeric").**WatermarkText**("**Numeric**")

@Html.EJ().PercentageTextbox("percentage").**WatermarkText**("**Percentage**")

@Html.EJ().CurrencyTextbox("currency").**WatermarkText**("**Currency**")

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").**WatermarkText**("**MaskEdit** ")



**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:NumericTextBox ID="numeric" WaterMarkText="Numeric" runat="server"&gt;&lt;/ej:NumericTextBox&gt;

&lt;ej:PercentageTextBox ID="percentage" WaterMarkText="Percentage" runat="server"&gt;&lt;/ej:PercentageTextBox&gt;

&lt;ej:CurrencyTextBox ID="currency" WaterMarkText="Currency" runat="server"&gt;&lt;/ej:CurrencyTextBox&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" WaterMarkText="MaskEdit" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for NumericTextBox **Textboxes** after applying **watermarkText** is as follows.



{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img43.png" Caption="Figure 30822: NumericTextBox Textboxes with watermark text"%}{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img44.png" Caption="Figure 30822: NumericTextBox Textboxes with watermark text"%}

**Text Alignment Support**

The **Mask Edit Textbox** provides text alignment support that allows you to set the alignment of text in the control by using the **textAlign** property.

**Configure Text Alignment**

The following steps explain the implementation of **textAlign** in **Textboxes**.

* In the **HTML** page set the **&lt;input&gt;** element for rendering **Mask Edit Textbox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="maskedit">Mask Edit</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="maskedit" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>textAlign</b> property in the <b>Textbox</b> controls. The default value for <b>textAlign</b> property is left in <b>Textboxes</b>    &lt;script&gt;/* MaskEdit Textbox */        $("#maskedit").ejMaskEdit({            value: 12345677,            <b>textAlign: "right",</b>            maskFormat: "99-999-99999"        });    &lt;/script&gt;</td></tr>
</table>


**[_cshtml]**

@* **Add the following code in your view page to render Textbox controls.***@

@Html.EJ().MaskEdit("mask").MaskFormat("99-999-99999").Value("12345677").**TextAlign**(**TextAlign.Right**)





**[_aspx]**

&lt;%-- Add the following code in your aspx page to render Textbox controls.--%&gt;

&lt;ej:MaskEdit ID="mask" MaskFormat="99-999-99999" Value="12345677" TextAlign="Right" runat="server"&gt;&lt;/ej:MaskEdit&gt;



The output for Textboxes when **textAlign** is set to **“right”**.

{% include image.html url="\js\Numeric\concepts-and-features\behavior-settings_images\behavior-settings_img45.png" Caption="Figure 391: MaskEdit Textbox with textAlign"%}

