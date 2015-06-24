---
layout: post
title: Display-Format
description: display format
platform: js
control: DatePicker
documentation: ug
---

# Display Format

## Date format

**Date format** defines a format or structure of the displayed date in the textbox. You can change the **Date** **format** by using **“dateFormat”** property.

The standard formats are listed as follows,

Date format

<table>
   <tr>
      <th>Format Name</th>
      <th>Formats</th>
   </tr>
   <tr>
      <td>
         Default
      </td>
      <td>
         MM/dd/yyyy
      </td>
   </tr>
   <tr>
      <td>
         Short
      </td>
      <td>
         d M, y
      </td>
   </tr>
   <tr>
      <td>
         Medium
      </td>
      <td>
         d MM, y
      </td>
   </tr>
   <tr>
      <td>
         Full
      </td>
      <td>
         dddd,d MMMM,yy
      </td>
   </tr>
   <tr>
      <td>
         UTC
      </td>
      <td>
         yyyy-MM-dd
      </td>
   </tr>
</table>


You can display the date value depending on culture using above specified **dateformat**.

The following steps explain you how to set the date format as "**d MM, y**"

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget


{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to set the date format as "d MM, y" for DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          dateFormat: "d MM, y"
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Display-Format_images/Display-Format_img1.png"%}

## Day header format

It specifies the **header format** of days in short, long or min types. You can set the **DatePicker** **day** **header format** by using **“dayHeaderFormat”** property. By default “**dayHeaderFormat**” property is set as “**ShowHeaderMin**” in **DatePicker** widget. 

Enum for DatePicker day header format

<table>
   <tr>
      <th>Day header</th>
      <th>Description</th>
   </tr>
   <tr>
      <td>
         ShowHeaderShort
      </td>
      <td>
         It shows the day header format in short
      </td>
   </tr>
   <tr>
      <td>
         ShowHeaderMin
      </td>
      <td>
         It shows the header format in min
      </td>
   </tr>
   <tr>
      <td>
         ShowHeaderLong
      </td>
      <td>
         It shows the day header format in long
      </td>
   </tr>
   <tr>
      <td>
         ShowHeaderNone
      </td>
      <td>
         Removes the day header
      </td>
   </tr>
</table>


The following steps explain you how to get the **dayHeaderFormat** for **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget


{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to get the dayHeaderFormat of DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          dayHeaderFormat: ej.DatePicker.Header.ShowHeaderLong
       });
    });
    
{% endhighlight %}

The following screenshot displays the output for the above code.


{% include image.html url="/js/DatePicker/Display-Format_images/Display-Format_img2.png"%}

## Header format

It specifies the **Header format** to be displayed in the pop up of **DatePicker**. The header in the **DatePicker** popup is displayed in the specified format.  By default “**dayHeaderFormat**” property is set as “**MMMM/yyyy**” in **DatePicker** widget. 

The following steps explain you how to the header format to be displayed in the pop up of **DatePicker**

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to set the header format to be displayed in the pop up of DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          headerFormat: "MMMM/yy"
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code.



{% include image.html url="/js/DatePicker/Display-Format_images/Display-Format_img3.png"%}

