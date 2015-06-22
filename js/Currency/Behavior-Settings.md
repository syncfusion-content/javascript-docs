---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: CurrencyTextBox  
documentation: ug
---

# Behavior Settings

## Decimal Places

The command **decimalPlaces** declares the decimal point to the value of **CurrencyTextBox** control. The default value of decimalPlaces is 0 in CurrencyTextBox control.

### Configure Decimal Places

The following steps explain the implementation of decimalPlaces in CurrencyTextBox.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}


        $("#currency").ejCurrencyTextbox({
            value: 555,
            decimalPlaces: 4
        });


{% endhighlight %}


The output for CurrencyTextBox with decimalPlaces is as follows.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="
 CurrencyTextBox with decimalPlaces"%}

## Persistence Support

The **CurrencyTextBox** widget provides the state maintenance support. You can maintain the previous changes made in the control after a page loads.

### Configure Persistence Support 

The following steps explain the implementation of **enablePersistence** in CurrencyTextBox.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering CurrencyTextBox control.


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}


        $("#currency").ejCurrencyTextbox({
            value: 33,
            enablePersistence: true
        });        


{% endhighlight %}

The output for **CurrencyTextBox** with **enablePersistence** is as follows. You can change the value of CurrencyTextBox and reload the web page.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="CurrencyTextBox at initial load"%}

{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="CurrencyTextBox after changing the value and a page load "%}

## Strict Mode Support
The CurrencyTextBox widget allows you to use the strict mode option by setting the **enableStrictMode** property. You can set the **minValue** and **maxValue** to the controls to enable strict mode functionality. When the CurrencyTextBox value exceeds the maxValue, it restricts the exceeded value and returns the **maxValue**. Likewise when the CurrencyTextBox value goes below **minValue**, it restricts the new value and returns the minValue.

### Configure Strict Mode Support 

The following steps explain the implementation of **enableStrictMode** in CurrencyTextBox .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            value: 10, //value(10) exceeds maxValue(8), so it will returns 8.
            minValue: -1,
            maxValue: 8,
            enableStrictMode: true
        });


{% endhighlight %}


The output for **CurrencyTextBox** when **enableStrictMode** is **“True”** is as follows**.**



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img4.png" Caption="CurrencyTextBox with enableStrictMode"%}

## Enabled or Disabled

The CurrencyTextBox control has an option to enable or disable its element. You can set the **enabled** property as “**True**” to enable the CurrencyTextBox control.

### Configure Enabled or Disabled 

The following steps explains the implementation of **enabled** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering CurrencyTextBox control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            value: 3,
            enabled: true
        });


{% endhighlight %}


The output for CurrencyTextBox when **enabled** is **“True”** and when **enabled** is “**False**”**.**



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="CurrencyTextBox with enabled as False"%}



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img6.png" Caption="CurrencyTextBox with enabled as True"%}

## Adjusting CurrencyTextBox Size

The CurrencyTextBox size can be modified by using the **height** and **width** properties. You can customize the size of CurrencyTextBox by using these properties.

### Configure Height and Width 

The following steps explain the implementation of **height** and **width** in CurrencyTextBox.

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering CurrencyTextBox control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}


        $("#currency").ejCurrencyTextbox({
            value: 1,
            width: 100, height: 50
        });

{% endhighlight %}


The output for CurrencyTextBox after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="CurrencyTextBox with height and width                          		"%}

## Increment Step

The **incrementStep** property is used to increase or decrease the amount of value in the CurrencyTextBox control. 

### Configure Increment Step

The following steps explain the implementation of **incrementStep** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control.


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            value:5,
            incrementStep: 4
        });

{% endhighlight %}


The output for CurrencyTextBox with **incrementStep** is as follows.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img8.png" Caption="CurrencyTextBox at initial load"%}



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img9.png" Caption="CurrencyTextBox after increasing one step"%}

## Define Name

When you have placed the CurrencyTextBox in a form, the **name** property is used to send the field value at form submission. The default value of the **name** property is null.

### Configure Name

The following steps explain the implementation of **name** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control.


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            name: "currency"            
        }); 

{% endhighlight %}


The output for **CurrencyTextBox** with the **name** property is as follows**.**



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img10.png" Caption="CurrencyTextBox with name"%}

## Define Value

The value of **CurrencyTextBox** can be assigned by using the **value** property. The default value for **value** property is null.

### Configure Value

The following steps explain the implementation of **value** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

  <input id="currency" type="text" />
      
{% endhighlight %}

{% highlight js %}


        $("#currency").ejCurrencyTextbox({
            value: 33              
        });

{% endhighlight %}


The output for **CurrencyTextBox** with the **value** property is as follows**.**

{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img11.png" Caption="CurrencyTextBox with value"%}

## Define maxValue and minValue

### maxValue

The maximum limit value can be assigned to the CurrencyTextBox by using the **maxValue** property. The default value of **maxValue** property is 1.7976931348623157e+308. 

### minValue

The minimum limit value can be assigned to the CurrencyTextBox by using the **minValue** property. The default value of **minValue** property is -1.7976931348623157e+308.

### Configure maxValue and minValue

The following steps explain the implementation of **maxValue** and **minValue** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control.


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}


        $("#currency").ejCurrencyTextbox({
            maxValue: 4,
            minValue: -3,
            value:4
        });

{% endhighlight %}


The output for **CurrencyTextBox** with basic properties is as follows.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img12.png" Caption="CurrencyTextBox with maxValue"%}



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img13.png" Caption="CurrencyTextBox with minValue"%}

## Read Only Support

The CurrencyTextBox supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the CurrencyTextBox. You can set the **readOnly** property as “**True”** to enable this option.

### Configure Read Only

The following steps explain the implementation of **readOnly** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

 
        $("#currency").ejCurrencyTextbox({
            value: 3,
            readOnly: true
        });

{% endhighlight %}


The output for CurrencyTextBox when **readOnly** is “**True**” is as follows. The CurrencyTextBox values cannot be edited or changed.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img14.png" Caption="CurrencyTextBox with readOnly"%}

## Appearance

### Theme

The **CurrencyTextBox** control’s style and appearance can be controlled based on CSS classes. In order to apply styles to the CurrencyTextBox control, you need to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. If the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files ej.widgets.core.min.css and ej.theme.min.css in your project, as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **CurrencyTextBox** control namely:

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

The **CSS** can be customized by using the **cssClass** in the CurrencyTextBox. You can customize the **CurrencyTextBox** with various **cssClass** properties to appear like your desired control.

### Configure CSS Class

The following steps explain the implementation of **cssClass** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

         $("#currency").ejCurrencyTextbox({
            value: 3,
            cssClass: "customCss"
        });

{% endhighlight %}

Customize the CSS properties in custom CSS class.

{% highlight css %}


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



The output for CurrencyTextBox after applying **cssClass** is as follows.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img15.png" Caption="CurrencyTextBox with cssClass"%}

## Rounded Corner Support

The CurrencyTextBox provides you with rounded corner support whose appearance is different from normal textbox controls.

### Configure Rounded Corner Support

The following steps explain the implementation of **showRoundedCorner** in **CurrencyTextBox** .

In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** controls. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            value: 3,
            showRoundedCorner: true
        });

{% endhighlight %}

The output for CurrencyTextBox when **showRoundedCorner** is “**True**”.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img16.png" Caption="CurrencyTextBox with showRoundedCorner"%}

## Spin Button Support

The **CurrencyTextBox** provides you the option as to whether to display the split button in the widget or remove it from the control by using **showSpinButton** property.

### Configure Spin Button

The following steps explain the implementation of **showSpinButton** in **CurrencyTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({
            value: 3,
            showSpinButton: true
        });

{% endhighlight %}


The output for **CurrencyTextBox** when **showSpinButton** is “**True**”.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img17.png" Caption="CurrencyTextBox with showSpinButton is True"%}

__{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img18.png" Caption="CurrencyTextBox with showSpinButton is False"%}

## Water Mark Text Support

The **CurrencyTextBox** provide water mark text support. You can display the initial value in the control by water mark.

### Configure Water Mark Text

The following steps explain the implementation of **watermarkText** in **CurrencyTextBox** .

* In the **HTML** page set the corresponding **&lt;input&gt;** elements for rendering **CurrencyTextBox** control. 


{% highlight html %}

<input id="currency" type="text" />
    
{% endhighlight %}

{% highlight js %}

        $("#currency").ejCurrencyTextbox({           
            watermarkText: "Currency"
        });

{% endhighlight %}


The output for CurrencyTextBox after applying **watermarkText** is as follows.



{% include image.html url="/js/Currency/Behavior-Settings_images/Behavior-Settings_img19.png" Caption="CurrencyTextBox with watermark text"%}

