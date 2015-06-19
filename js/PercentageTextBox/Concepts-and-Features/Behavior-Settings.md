---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: PercentageTextBox 
documentation: ug
---

# Behavior Settings

## Decimal Places

The command **decimalPlaces** declares the decimal point to the value of **PercentageTextBox** control. The default value of **decimalPlaces** is 0 in **PercentageTextBox** control.

### Configure Decimal Places

The following steps explain the implementation of **decimalPlaces** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>decimalPlaces</b> value in the <b>PercentageTextBox </b>control    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,<b>            decimalPlaces: 2</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with **decimalPlaces** is as follows.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Figure 5: PercentageTextBox with decimalPlaces"%}

## Persistence Support

The **PercentageTextBox** widgets provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

### Configure Persistence Support 

The following steps explain the implementation of **enablePersistence** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enablePersistence </b>property<b> </b>as<b> “true</b>” to the <b>PercentageTextBox </b>controls. The default value for <b>enablePersistence </b>is “<b>false</b>”    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 22,<b>            enablePersistence: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with **enablePersistence** is as follows. You can change the value of **PercentageTextBox** and reload the web page.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Figure 6: PercentageTextBox at initial load"%}

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Figure 7: PercentageTextBox after changing the value and a page load "%}





## Strict Mode Support

The **PercentageTextBox** widget allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. When the Textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the Textbox value goes below **minValue**, it restricts the new value and returns the **minValue**.

### Configure Strict Mode Support 

The following steps explain the implementation of **enableStrictMode** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableStrictMode </b>property<b> </b>as<b> “true</b>” to the <b>PercentageTextBox </b>controls. The default value for <b>enableStrictMode </b>is “<b>false</b>”    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: -10,//value(-10) is under minValue(-5),so Error class will be added.<b>            minValue: -5,</b><b>            maxValue: 3,</b><b>            enableStrictMode: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **enableStrictMode** is **“true”** is as follows**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="Figure 8: PercentageTextBox with enableStrictMode"%}

## Enabled or Disabled

The **PercentageTextBox** control has an option to enable or disable its element. You can set the **enabled** property as “**true**” to enable the **PercentageTextBox** control.

### Configure Enabled or Disabled 

The following steps explains the implementation of **enabled** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enabled </b>property<b> </b>as<b> “false</b>” to the <b>PercentageTextBox</b> control. The default value for <b>enabled</b> is true    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,<b>            enabled: false</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **enabled** is **“true”** and when **enabled** is “**false**”**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Figure 9: PercentageTextBox with enabled as true"%}

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img6.png" Caption="Figure 10: PercentageTextBox with enabled as false"%}

## Adjusting PercentageTextBox Size

The **PercentageTextBox** size can be modified by using the **height** and **width** properties. You can customize the size of **PercentageTextBox** by using these properties.

### Configure Height and Width 

The following steps explain the implementation of **height** and **width** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>height </b>and<b> width </b>property<b> </b>to the <b>PercentageTextBox </b>controls. The default value of <b>height</b> and <b>width</b> is empty string (“”)&lt;script type="text/javascript"&gt;    /* Percent Textbox */    $("#percent").ejPercentageTextbox({        value: 2,        <b>width: 100,</b><b>        height: 40</b>    });&lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="Figure 11: PercentageTextBox with height and width                          		"%}

## Increment Step

The **incrementStep** property is used to increase or decrease the amount of value in the **PercentageTextBox** control. 

### Configure Increment Step

The following steps explain the implementation of **incrementStep** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>incrementStep </b>property<b> </b>to the <b>PercentageTextBox </b>controls. The default value of <b>incrementStep </b>is 1    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value:1,            <b>incrementStep: 3</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with **incrementStep** is as follows**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img8.png" Caption="Figure 12: PercentageTextBox at initial load"%}



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img9.png" Caption="Figure 13: PercentageTextBox after increasing one step"%}

## Define Name

When you have placed the **PercentageTextBox** in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

### Configure Name

The following steps explain the implementation of **name** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>name </b>property<b> </b>to the <b>PercentageTextBox </b>controls    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>name: "percent"         </b>        });      &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with the **name** property is as follows**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img10.png" Caption="Figure 14: PercentageTextBox with name"%}

## Define Value

The value of **PercentageTextBox** can be assigned by using the **value** property. The default value for **value** property is null.

### Configure Value

The following steps explain the implementation of **value** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;               &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>value </b>property<b> </b>to the <b>PercentageTextBox </b>controls    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            <b>value: 21               </b>        });     &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with the **value** property is as follows**.**

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img11.png" Caption="Figure 15: PercentageTextBox with value"%}

## Define maxValue and minValue

### maxValue

The maximum limit value can be assigned to the **PercentageTextBox** by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

### minValue

The minimum limit value can be assigned to the **PercentageTextBox** by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

### Configure maxValue and minValue

The following steps explain the implementation of **maxValue** and **minValue** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maxValue, </b>and<b> minValue </b>properties<b> </b>to the <b>PercentageTextBox </b>control    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({<b>            maxValue: 3,</b><b>            minValue: -2,</b>            value:3        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** with basic properties is as follows**.**



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img12.png" Caption="Figure 16: PercentageTextBox with maxValue"%}



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img13.png" Caption="Figure 17: PercentageTextBox with minValue"%}

## Read Only Support

The **PercentageTextBox** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the **PercentageTextBox**. You can set the **readOnly** property as “**True”** to enable this option.

### Configure Read Only

The following steps explain the implementation of **readOnly** in **PercentageTextBox**.

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>readOnly </b>property as “<b>True” </b>to the <b>PercentageTextBox </b>controls. The default value of <b>readOnly</b> property is false    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 3,           <b> readOnly: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **readOnly** is “**True**” is as follows**.** The **PercentageTextBox** values cannot be edited or changed.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img14.png" Caption="Figure 18: PercentageTextBox with readOnly		"%}

## Appearance

### Theme

The **PercentageTextBox** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the **Textbox** control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **PercentageTextBox** control namely:

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

The **CSS** can be customized by using the **cssClass** in the **PercentageTextBox**. You can customize the **PercentageTextBox** with various **cssClass** properties to appear like your desired control.

### Configure CSS Class

The following steps explain the implementation of **cssClass** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass </b>property as custom CSS class name<b> </b>to the <b>PercentageTextBox </b>control. The default value of <b>cssClass</b> property is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>cssClass: "customCss"</b>        });    &lt;/script&gt;</td></tr>
</table>
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



The output for **PercentageTextBox** after applying **cssClass** is as follows.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img15.png" Caption="Figure 19: PercentageTextBox with cssClass"%}

## Rounded Corner Support

The **PercentageTextBox** provides you with rounded corner support whose appearance is different from normal textbox controls.

### Configure Rounded Corner Support

The following steps explain the implementation of **showRoundedCorner** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as “<b>true”</b> in the <b>PercentageTextBox </b>controls. The default value for <b>showRoundedCorner</b> property is false in <b>PercentageTextBox</b>    &lt;script&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showRoundedCorner: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **showRoundedCorner** is “**true**”.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img16.png" Caption="Figure 20: PercentageTextBox with showRoundedCorner"%}

## Spin Button Support

The **PercentageTextBox** provides you the option as to whether to display the split button in the widget or remove it from the control by using **showSpinButton** property.

### Configure Spin Button

The following steps explain the implementation of **showSpinButton** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showSpinButton</b> property as “<b>True”</b> in the <b>Textbox</b> controls. The default value for <b>showSpinButton</b> property is true in <b>Textboxes</b>    &lt;script&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({            value: 2,            <b>showSpinButton: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** when **showSpinButton** is “**True**”.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img17.png" Caption="Figure 21: PercentageTextBox with showSpinButton is true"%}

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img18.png" Caption="Figure 22: PercentageTextBox with showSpinButton is false"%}

## Water Mark Text Support

The **PercentageTextBox** provide water mark text support. You can display the initial value in the control by water mark.

### Configure Water Mark Text

The following steps explain the implementation of **watermarkText** in **PercentageTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **PercentageTextBox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;table cellpadding="10"&gt;            &lt;tbody&gt;                &lt;tr&gt;                    &lt;td&gt;                        <label for="percent">Percent</label>                    &lt;/td&gt;                    &lt;td&gt;                        &lt;input id="percent" type="text" /&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/tbody&gt;        &lt;/table&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>watermarkText</b> in the <b>PercentageTextBox </b>controls. The default value for <b>watermarkText</b> property is empty string (“”) in <b>PercentageTextBox</b>    &lt;script&gt;        /* Percent Textbox */        $("#percent").ejPercentageTextbox({                       <b>watermarkText: "Percentage"</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **PercentageTextBox** after applying **watermarkText** is as follows.



{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img19.png" Caption="Figure 23: PercentageTextBox with watermark text"%}

