---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: DatePicker
documentation: ug
---

# Miscellaneous

## Define height

It specifies the **height** of the **DatePicker** input text. The “**height”** property allows you to set the maximum **height** of the **DatePicker**. The value set to this property should be **string or Numer** type.

The following steps explain you how to specify the **height** of the **DatePicker** input text

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to specify the height of the DatePicker input text
    $(function() {
       // declaration 
       $("#datepicker").ejDatePicker({
          //Number
          height: 22
       });
    });

    [OR]

    $(function() {
       // declaration 
       $("#datepicker").ejDatePicker({
          //String
          height: “22 px”
       });
    });

{% endhighlight %}
  
## Define width

It specifies the **width** of the **DatePicker** input text. The “**width”** property allows you to set the maximum **width** of **DatePicker**. The value set to this property should be **string or Numer** type

The following steps explain you how to specify the **width** of the **DatePicker** input text

In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}
  
    // Add the code to specify the width (Number) of the DatePicker input text
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          //Number
          width: 200
       });
    });

    [OR]

    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          width: "200px"
       });
    });

{% endhighlight %}
  
## Highlight Section

**Highlight section** highlights the current month, current week, current workdays. You can highlight a week, month, and work days by using “**highlightSection”** property.

Highlight Selection

<table>
   <tr>
      <th>Name </th>
      <th>Description</th>
   </tr>
   <tr>
      <td>
         month
      </td>
      <td>
         Highlight the Current Month.
      </td>
   </tr>
   <tr>
      <td>
         week
      </td>
      <td>
         Highlight the Current Week.
      </td>
   </tr>
   <tr>
      <td>
         workdays
      </td>
      <td>
         Highlight the Current Workdays
      </td>
   </tr>
   <tr>
      <td>
         none
      </td>
      <td>
         Don’t Highlight Anything
      </td>
   </tr>
</table>


The following steps explain you how to **highlight** the current week section

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget


{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}
  
    // Add the code to highlight the current Week in the DatePicker Calendar
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          highlightSection: "week"
       });
    });

{% endhighlight %}



The following screenshot displays the output for the above code.   

![]("/js/DatePicker/Miscellaneous_images/Miscellaneous_img1.png")



## ReadOnly

**Readonly** property indicates that the **DatePicker** value can only be read. You can’t edit the value in **DatePicker** and also the **DatePicker** calendar popup is not shown. By default “**readOnly**” Boolean value is set to **‘false’**.

The following steps explain you how to set the **DatePicker** value as **readonly**

In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

{% highlight html %}
 
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to set the DatePicker value as readonly
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          readOnly: true
       });
    });

{% endhighlight %}
  
## Show Footer

It allows to **Show Footer** in **DatePicker** calendar to select today date. By default “**showFooter**” property is set as ‘**true**’ in **DatePicker** widget. You can hide footer in the **DatePicker** when this property is set to “**false**”.

The following steps explain you how to hide footer in the **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **Datepicker** widget

{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}
  
    // Add the code to hide footer in the DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          showFooter: false
       });
    });

{% endhighlight %}
  
## Show popup button

It shows the date icon button at right side of textbox and shows **DatePicker** popup on clicking it that can be achieved by using “**showPopupButton** “property. By default “**showPopupButton**” property is set as “**true**” in **DatePicker** widget. 

The following steps explain you how to hide the **popupbutton** in the **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to hide popupbutton footer in the DatePicker
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          showPopupButton: false
       });
    });

{% endhighlight %}

The following screenshot displays the output for the above code.



![]("/js/DatePicker/Miscellaneous_images/Miscellaneous_img2.png")

## Show rounded corner

**DatePicker** input is displayed in rounded corner style, when this property is set to **‘true’**. By default “**showRoundedCorner**” property is set as “**false**” in **DatePicker** widget.

The following steps explain you how to show **Roundedcorner** in the **DatePicker**

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}
    
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to show Roundedcorner in the DatePicker
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          showRoundedCorner: true
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code.



![]("/js/DatePicker/Miscellaneous_images/Miscellaneous_img3.png")


## Show Tooltip

**DatePicker** **Tooltip** is displayed while you hover the date. By default “**showTooltip**” property as “**true**” in **DatePicker** widget.

The following steps explain you how to hide the **ToolTip** in the **DatePicker**.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to hide the ToolTip in the DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          showTooltip: false
       });
    });

{% endhighlight %}
  
The following screenshot displays the output for the above code.



![]("/js/DatePicker/Miscellaneous_images/Miscellaneous_img4.png")













