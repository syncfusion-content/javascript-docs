---
layout: post
title: Start-and-Depth-navigation
description: start and depth navigation
platform: js
control: DatePicker
documentation: ug
---

# Start and Depth navigation

## Start Level

It specifies the **Start Level** view in **DatePicker** calendar. By default “**startLevel”** property is set to **ej.DatePicker.Level.Month.**

Start level

<table>
   <tr>
      <th>Name</th>
      <th>Description</th>
   </tr>
   <tr>
      <td>
         month
      </td>
      <td>
         Starts from month level view.
      </td>
   </tr>
   <tr>
      <td>
         year
      </td>
      <td>
         Starts from year level view.
      </td>
   </tr>
   <tr>
      <td>
         decade
      </td>
      <td>
         Starts from decade level view.
      </td>
   </tr>
   <tr>
      <td>
         century
      </td>
      <td>
         Starts from century level view.
      </td>
   </tr>
</table>


The following steps explain you how to specify the **Start Level** view in **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to specify the Start Level view in DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          startLevel: ej.DatePicker.Level.Century
       });
    });

{% endhighlight %}

The following screenshot displays the output for the above code.

![](/js/DatePicker/Start-and-Depth-navigation_images/Start-and-Depth-navigation_img1.png)

## Depth Level

It specifies the drill down level of **DatePicker**. You can restrict the drill down **Depth Level** using “**depthLevel”** property. 

It accepts the following values. 

Depth level

<table>
   <tr>
      <th>Value</th>
      <th>Description</th>
   </tr>
   <tr>
      <td>
         month
      </td>
      <td>
         Starts from month level view.
      </td>
   </tr>
   <tr>
      <td>
         year
      </td>
      <td>
         Starts from year level view.
      </td>
   </tr>
   <tr>
      <td>
         decade
      </td>
      <td>
         Starts from year decade level view.
      </td>
   </tr>
   <tr>
      <td>
         century
      </td>
      <td>
         Starts from century level view. 
      </td>
   </tr>
</table>


The following steps explain you how to get the **Depth Level.**

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget

{% highlight html %}

<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to render the Depth Level
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          startLevel: ej.DatePicker.Level.Century,
          depthLevel: ej.DatePicker.Level.Year
       });
    });

{% endhighlight %}

The following screenshot displays the output for the above code.

![](/js/DatePicker/Start-and-Depth-navigation_images/Start-and-Depth-navigation_img2.png)

