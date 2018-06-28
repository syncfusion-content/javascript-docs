---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: MaskEdit
documentation: ug
api: /api/js/ejmaskedit
---

# Behavior Settings

## Persistence Support

The MaskEdit control provides state maintenance support. You can maintain the previous changes made in the control after a page loads. By default, the ‘**enablePersistence**’ property is set to ‘**false**’ in the **MaskEdit**.

The following steps explain the **State Maintenance** in the **MaskEdit** control.

 In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 

{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function() {
            $("#maskedit").ejMaskEdit({
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                enablePersistence: true,
            });
        });

{% endhighlight %}


Output of MaskEdit with **enablePersistence** is as follows. 



![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img1.png)

![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img2.png)

## Enabled or Disabled

MaskEdit has an option to enable or disable its element. You can set the **enabled** property as “**false**” to disable the MaskEdit controls.

The following steps explain the **enabled** property in the **MaskEdit** control.

In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $("#maskedit").ejMaskEdit(
            {
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                enabled: false,
            });
        });

{% endhighlight %}


Output when **enabled** is **“false”** and when **enabled** is “**true**”**.**

![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img3.png)

MaskEdit with disabled state
{:.caption}

![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img4.png)

MaskEdit with default state
{:.caption}

## Adjusting MaskEdit Size

**MaskEdit** size can be modified by using the **height** and **width** properties. You can customize the size of **MaskEdit** by using these properties.

The following steps explain the **width** and **height** property in the **MaskEdit** control.

In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $("#maskedit").ejMaskEdit(
            {
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                width: 150,
                height: 50
            });
        });

{% endhighlight %}




Output of MaskEdit after setting “**height**” and “**width**” is as follows**.**



![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img5.png) 

## Define Value

The value of **MaskEdit** can be assigned by using the **value** property. The default value for **value** property is null.
Specify the [name](https://help.syncfusion.com/api/js/ejmaskedit#members:name) attribute value for the mask edit textbox.
You can get the raw value of **MaskEdit** without literals and prompt characters by using the [get_StrippedValue](https://help.syncfusion.com/api/js/ejmaskedit#methods:get_strippedvalue) method.
Also you get the value of **MaskEdit** with the masked format by using the [get_UnstrippedValue](https://help.syncfusion.com/api/js/ejmaskedit#methods:get_unstrippedvalue) method.

The following steps explain the **value** property in the **MaskEdit** control.

In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $("#maskedit").ejMaskEdit(
            {
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                value: "1234567890",
            });
        });

{% endhighlight %}




Output of MaskEdit with the **value** property is as follows**.**



![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img6.png) 

## Read Only Support

**MaskEdit** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the **MaskEdit**. You can set the **readOnly** property as “**true”** to enable this option.

The following steps explain the **readOnly** property in the **MaskEdit** control.

In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $("#maskedit").ejMaskEdit(
            {
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                value: "123456",
                readOnly: true
            });
        });

{% endhighlight %}


Output of **MaskEdit** when **readOnly** is “**true**” is as follows. MaskEdit values cannot be edited or changed.



![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img7.png)

## Error Visibility

The **MaskEdit** has an option that shows the error value with red colored text. It is used to validate the Mask Edit value. You can set the **showError** property as “**true”** to enable this option.

The following steps explain the **showError** property in the **MaskEdit** control.

In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight javascript %}

        $(function () {
            $("#maskedit").ejMaskEdit(
            {
                name: "mask",
                inputMode: ej.InputMode.Text,
                maskFormat: "99-999-99999",
                value: "123456",
                showError: true
            });
        });

{% endhighlight %}




Output for **MaskEdit** when **showError** is “**true**” is as follows**.** 



![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img8.png)

MaskEdit with error class
{:.caption}

![](/js/MaskEdit/Behavior-Settings_images/Behavior-Settings_img9.png)

MaskEdit with proper input value
{:.caption}

