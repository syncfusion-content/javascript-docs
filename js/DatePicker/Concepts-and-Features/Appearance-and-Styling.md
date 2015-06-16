---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: DatePicker
documentation: ug
---

# Appearance and Styling

## Theme

**DatePicker** control’s style and appearance are controlled based on **CSS****classes**. In order to apply **Theme** to the **DatePicker** widget, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project, as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes support available for **DatePicker** widget namely,

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

## Custom CSS

To apply custom styles to your **DatePicker** widget, you can specify **CssClass** property. The specified **CSS** name is added in the root of the **DatePicker** widget.

The following code example is used to render the **DatePicker** widget with customized style.

* In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget



 {% highlight html %}
  
  **[HTML]**
  
      <input id="datepicker" type="text" />
      
  {% endhighlight %}
  
  {% highlight js %}

  **[JavaScript]**

// Add the class for DatePicker widget

<script type="text/javascript">
    $(function () {
        // declaration
        $("#datepicker").ejDatePicker({
            cssClass: "custom"
        });
    });
    </script>

  {% endhighlight %}



*  Add the following styles to render **DatePicker** with customized style.

{% highlight css %}

<style type="text/css">
    .custom .e-header {
      background-color:blue;
    }

</style>


{% endhighlight %}



* The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Figure 24: Custom Css in DatePicker"%}

## Keyboard Navigation



With the **Keyboard Navigation** **enabled** in the **DatePicker** widget, it is possible to widget the actions of the **DatePicker** with the provided shortcut keys. Almost all the **DatePicker** actions that are done through mouse are controlled with shortcut keys. By default, the **keyboard navigation** is set to ‘**true**’ for the widget and it is controlled with the property “**allowKeyboardNavigation**”.

The various keyboard shortcuts available within the **DatePicker** widget are discussed in the following table.

_Table_ _5__: Keyboard navigation_

<table>
<tr>
<td>
<b>Keys</b></td><td>
<b>Function</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a><b> </b><b>+j</b></td><td>
Focuses the control</td></tr>
<tr>
<td>
<b>Alt + Down</b></td><td>
Opens the popup</td></tr>
<tr>
<td>
<b>Left</b><b>Right</b></td><td>
Moves to previous dateMoves to next date</td></tr>
<tr>
<td>
<b>Up</b></td><td>
Moves one week upward</td></tr>
<tr>
<td>
<b>Down</b></td><td>
Moves one week downward</td></tr>
<tr>
<td>
<b>Enter</b></td><td>
Selects the focused date</td></tr>
<tr>
<td>
<b>Esc</b></td><td>
Closes the popup</td></tr>
<tr>
<td>
<b>Ctrl + Up</b></td><td>
Navigates to top view</td></tr>
<tr>
<td>
<b>Ctrl + Down</b></td><td>
Navigates to lower view</td></tr>
<tr>
<td>
<b>Ctrl + Left</b></td><td>
Navigates to previous month</td></tr>
<tr>
<td>
<b>Ctrl + Right</b></td><td>
Navigates to next month</td></tr>
</table>


The following steps explain you to enable keyboard interaction for **DatePicker** widget

* In the **HTML** page, add a **&lt;input&gt;** element to configure **DatePicker** widget and enable keyboard interaction by setting the **accesskey** property


 {% highlight html %}
  
  **[HTML]**
  
      <input id="datepicker" type="text" />
      
  {% endhighlight %}
  
  {% highlight js %}

  **[JavaScript]**

 // Render DatePicker widget

   <script type="text/javascript">
        $(function () {
            // declaration
            $("#datepicker").ejDatePicker();
        });
    </script>

  {% endhighlight %}



* Run the sample, press **Alt + J** to focus in the **DatePicker** widget that enables it and you can navigate using arrow keys and Esc key to close the popup.

{% include image.html url="/js/DatePicker/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Figure 25: DatePicker focused with Keyboard shortcut                                            "%}

