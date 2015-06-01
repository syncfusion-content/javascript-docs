---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: NumericTextbox
documentation: ug
---

# Behavior Settings

## Decimal Places

**decimalPlaces** property specifies number of values allowed after the decimal point.The default value of **decimalPlaces** property is 0 i.e., by default you cannot specify decimal value in NumericTextBox. We need to add this property to allow decimal values.

### Configure Decimal Places

The following steps explain the implementation of **decimalPlaces** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>     &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>decimalPlaces</b> value in the Numeric Textbox control    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 333,<b>            decimalPlaces: 3</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** with **decimalPlaces** is as follows.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Figure 5: NumericTextBox with decimalPlaces"%}

## Persistence Support

The **NumericTextBox** widgets provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

### Configure Persistence Support 

The following steps explain the implementation of **enablePersistence** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>     &lt;input id="numeric" type="text" /&gt;                  </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enablePersistence </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox </b>controls. The default value for <b>enablePersistence </b>is “<b>False</b>”    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 11,            <b>enablePersistence: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** with **enablePersistence** is as follows. You can change the value of **NumericTextBox** and reload the web page.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Figure 6: NumericTextBox at initial load"%}

{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Figure 7: NumericTextBox after changing the value and after page refresh "%}

## Strict Mode Support

NumericTextBox allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. Default value of this property is **false**. When the textbox value exceeds the **maxValue**, it restricts the exceeded value and returns the **maxValue**. Likewise when the textbox value goes below **minValue**, it restricts the new value and returns the **minValue**. When this property is enabled, it will not restrict the specified value and an error class will be added to indicate wrong value is provided to the NumericTextBox.

### Configure Strict Mode Support 

The following steps explain the implementation of **enableStrictMode** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="numeric" type="text" /&gt;                    </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enableStrictMode </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox </b>controls. The default value for <b>enableStrictMode </b>is “<b>False</b>”    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 10, //value(10) exceeds maxValue(5), so it will returns 5.<b>            minValue: -3,</b><b>            maxValue:5,</b><b>            enableStrictMode: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** when **enableStrictMode** is **“True”** is as follows**.**





{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption=""%}



_Figure_ _8__:_ _NumericTextBox__****__with enableStrictMode_

## Enabled or Disabled

The NumericTextBox****control has an option to enable or disable its element. You can set the **enabled** property as “**True**” to enable the NumericTextBox****control.

### Configure Enabled or Disabled 

The following steps explains the implementation of **enabled** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>   &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>enabled </b>property<b> </b>as<b> “True</b>” to the <b>NumericTextBox </b>controls. The default value for <b>enabled</b> is true    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,<b>            enabled: true</b>                   });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** when **enabled** is **“True”** and when **enabled** is “**False**”**.**





{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Figure 9: NumericTextBox with enabled as False"%}



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img6.png" Caption="Figure 10: NumericTextBox with enabled as True"%}

## Adjusting Textbox Size

The **NumericTextBox** size can be modified by using the **height** and **width** properties. You can customize the size of NumericTextBox by using these properties.

### Configure Height and Width 

The following steps explain the implementation of **height** and **width** in NumericTextBox .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering NumericTextBox control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>height </b>and<b> width </b>property<b> </b>to the NumericTextBox controls. The default value of <b>height</b> and <b>width</b> is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>            width: 100, height: 50,value:1           </b>        });    &lt;/script&gt;</td></tr>
</table>


The output for NumericTextBox after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="Figure 11: NumericTextBox with height and width                          		"%}

## Increment Step

The **incrementStep** property is used to increase or decrease the amount of value in the NumericTextBox control. 

### Configure Increment Step

The following steps explain the implementation of **incrementStep** in NumericTextBox .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering NumericTextBox control.



<table>
<tr>
<td>
<b>[HTML]</b>                &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>incrementStep </b>property<b> </b>to the <b>NumericTextBox </b>controls. The default value of <b>incrementStep </b>is 1    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value:1,<b>           incrementStep: 2       </b>        });    &lt;/script&gt;</td></tr>
</table>


Output of Numeric textbox with **incrementStep** is as follows**.**



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img8.png" Caption="Figure 12: NumericTextBox at initial load"%}



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img9.png" Caption="Figure 13: NumericTextBox after increasing two step"%}

## Define Name

When you have placed the **NumericTextBox** in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

### Configure Name

The following steps explain the implementation of **name** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>     &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>name </b>property<b> </b>to the <b>NumericTextBox </b>controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value:12,<b>name: "numeric"       </b>        });     &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** with the **name** property is as follows**.**



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img10.png" Caption="Figure 14: NumericTextBox with name"%}

## Define Value

The value of **NumericTextBox** can be assigned by using the **value** property. The default value for **value** property is null.

### Configure Value

The following steps explain the implementation of **value** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>value </b>property<b> </b>to the <b>NumericTextBox </b>controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            <b>value: 12                 </b>        });     &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** with the **value** property is as follows**.**

{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img11.png" Caption="Figure 15: NumericTextBox with value"%}

## Define maxValue and minValue

### maxValue

The maximum limit value can be assigned to the **NumericTextBox** by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

### minValue

The minimum limit value can be assigned to the **NumericTextBox** by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

### Configure maxValue and minValue

The following steps explain the implementation of **maxValue** and **minValue** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control.



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>maxValue, </b>and<b> minValue </b>properties<b> </b>to the <b>NumericTextBox </b>controls    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({<b>            maxValue: 2,</b><b>            minValue: -1,</b>            value:2        });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** with basic properties is as follows**.**

{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img12.png" Caption="Figure 16: NumericTextBox with maxValue"%}



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img13.png" Caption="Figure 17: NumericTextBox with minValue"%}

## Read Only Support

The **NumericTextBox** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the NumericTextBox . You can set the **readOnly** property as “**True”** to enable this option.

### Configure Read Only

The following steps explain the implementation of **readOnly** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input id="numeric" type="text" /&gt;                   </td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>readOnly </b>property as “<b>True” </b>to the <b>NumericTextBox </b>controls. The default value of <b>readOnly</b> property is false    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                       value: 1,<b>            readOnly: true</b>        });            &lt;/script&gt;</td></tr>
</table>


The output for NumericTextBox when **readOnly** is “**True**” is as follows**.** The NumericTextBox value cannot be edited or changed.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img14.png" Caption="Figure 18: NumericTextBox with readOnly		"%}

## Appearance

### Theme

The NumericTextBox control style and appearance can be controlled based on CSS classes. In order to apply styles to the NumericTextBox control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

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

The **CSS** can be customized by using the **cssClass** in the NumericTextBox . You can customize the NumericTextBox with various **cssClass** properties to appear like your desired control.

### Configure CSS Class

The following steps explain the implementation of **cssClass** in NumericTextBox .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>cssClass </b>property as custom CSS class name<b> </b>to the <b>NumericTextBox </b>controls. The default value of <b>cssClass</b> property is empty string (“”)    &lt;script type="text/javascript"&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>cssClass: "customCss"</b>        });    &lt;/script&gt;</td></tr>
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



The output for NumericTextBox after applying **cssClass** is as follows.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img15.png" Caption="Figure 19: NumericTextBox with cssClass"%}

## Rounded Corner Support

The NumericTextBox provides you with rounded corner support whose appearance is different from normal textbox controls.

**Configure Rounded Corner Support**

The following steps explain the implementation of **showRoundedCorner** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>      &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showRoundedCorner</b> property as “<b>True”</b> in the <b>NumericTextBox </b>controls. The default value for <b>showRoundedCorner</b> property is false in <b>NumericTextBox</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showRoundedCorner: true</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for NumericTextBox when **showRoundedCorner** is “**True**”.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img16.png" Caption="Figure 20: NumericTextBox with showRoundedCorner"%}

## Spin Button Support

The NumericTextBox provides you the option as to whether to display the split button in the widget or remove it from the control by using **showSpinButton** property.

### Configure Spin Button

The following steps explain the implementation of **showSpinButton** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** controls. 



<table>
<tr>
<td>
<b>[HTML]</b>       &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>showSpinButton</b> property as “<b>True”</b> in the <b>NumericTextBox </b>controls. The default value for <b>showSpinButton</b> property is true in <b>NumericTextBox</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({            value: 1,            <b>showSpinButton: false</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for **NumericTextBox** when **showSpinButton** is “**False**”.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img17.png" Caption="Figure 21: NumericTextBox with showSpinButton is False"%}

## Water Mark Text Support

The NumericTextBox provide water mark text support. You can display the initial value in the control by water mark.

### Configure Water Mark Text

The following steps explain the implementation of **watermarkText** in **NumericTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **NumericTextBox** control. 



<table>
<tr>
<td>
<b>[HTML]</b>         &lt;input id="numeric" type="text" /&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>watermarkText</b> in the <b>NumericTextBox </b>controls. The default value for <b>watermarkText</b> property is empty string (“”) in <b>NumericTextBox</b>    &lt;script&gt;        /* Numeric Textbox */        $("#numeric").ejNumericTextbox({                        <b>watermarkText: "Numeric"</b>        });    &lt;/script&gt;</td></tr>
</table>


The output for NumericTextBox after applying **watermarkText** is as follows.



{% include image.html url="/js/Numeric/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img18.png" Caption="Figure 22: NumericTextBox with watermark text"%}

