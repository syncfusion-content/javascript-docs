---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: MaskEdit
documentation: ug
---

# Behavior Settings

## Persistence Support

The MaskEdit control provides state maintenance support. You can maintain the previous changes made in the control after a page loads. By default, the ‘**enablePersistence**’ property is set to ‘**false**’ in the **MaskEdit**.

The following steps explain the **State Maintenance** in the **MaskEdit** control.

 In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 

{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
        $(function () {
        $("#maskedit").ejMaskEdit(
        {
            name: "mask",
            inputMode: ej.InputMode.Text,
            maskFormat: "99-999-99999",
            enablePersistence: true,
        });
    });
</script>

{% endhighlight %}


Output of MaskEdit with **enablePersistence** is as follows. 



1. {% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img1.png" Caption="Figure 4: MaskEdit at initial load"%}

{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img2.png" Caption="Figure 5: MaskEdit after changing the value and after page refresh "%}

## Enabled or Disabled

MaskEdit has an option to enable or disable its element. You can set the **enabled** property as “**false**” to enable the MaskEdit controls.

The following steps explain the **enabled** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 



{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
        $(function () {
        $("#maskedit").ejMaskEdit(
        {
            name: "mask",
            inputMode: ej.InputMode.Text,
            maskFormat: "99-999-99999",
            enabled: false,
        });
    });
</script>

{% endhighlight %}


Output when **enabled** is **“false”** and when **enabled** is “**true**”**.**

2. {% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img3.png" Caption="Figure 6: MaskEdit with enabled as false"%}

{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img4.png" Caption=""%}_Figure 7: MaskEdit with enabled as true_

## Adjusting MaskEdit Size

**MaskEdit** size can be modified by using the **height** and **width** properties. You can customize the size of **MaskEdit** by using these properties.

The following steps explain the **width** and **height** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
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
</script>

{% endhighlight %}




Output of MaskEdit after setting “**height**” and “**width**” is as follows**.**



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img5.png" Caption="Figure 8: MaskEdit with height and width                                            		"%}

## Define Value

The value of **MaskEdit** can be assigned by using the **value** property. The default value for v**alue** property is null.

The following steps explain the **value** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
        $(function () {
        $("#maskedit").ejMaskEdit(
        {
            name: "mask",
            inputMode: ej.InputMode.Text,
            maskFormat: "99-999-99999",
            value: "1234567890",
        });
    });
</script>

{% endhighlight %}




Output of MaskEdit with the **value** property is as follows**.**



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img6.png" Caption=""%}_Figure_ _9__:_ _MaskEdit____with value_

## Read Only Support

**MaskEdit** supports read only option. When you enable the **readOnly** property to the control, the value cannot be changed in the **MaskEdit**. You can set the **readOnly** property as “**true”** to enable this option.

The following steps explain the **readOnly** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input i="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
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
</script>

{% endhighlight %}


****Output of **MaskEdit** when r**eadOnly** is “**true**” is as follows**.** MaskEdit values cannot be edited or changed.



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img7.png" Caption="Figure 10: MaskEdit with readOnly		"%}

## Error Visibility

The **MaskEdit** has an option that shows the error value with red colored text. It is used to validate the Mask Edit value. You can set the **showError** property as “**true”** to enable this option.

The following steps explain the **showError** property in the **MaskEdit** control.

* In the **HTML** page, add a **&lt;div&gt;** element to render the **MaskEdit** widget. 


{% highlight html %}

<input id="maskedit" type="text" />
    
{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
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
</script>

{% endhighlight %}




Output for **MaskEdit** when **showError** is “**true**” is as follows**.** 



{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img8.png" Caption="Figure 11: Textbox with showError"%}

{% include image.html url="/js/MaskEdit/Concepts-and-Features/Behavior-Settings_images/Behavior-Settings_img9.png" Caption="Figure 12: Textbox without error"%}

