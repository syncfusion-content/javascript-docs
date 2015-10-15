---
layout: post
title: Behavior-Settings
description: behavior settings
platform: js
control: DatePicker
documentation: ug
---

# Behavior Settings

## Button Text

Set the display text for the **Button** in the **DatePicker** popup. The **buttonText** is set **Today** (String), by default. You can change this default value by using **ButtonText** property to change the **Button Text**.

The following steps explain how to set the **Button Text** for **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.


{% highlight html %}

<input id="datepicker" type="text" />
    
{% endhighlight %}


{% highlight js %}

    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          buttonText: "Todaydate"
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code example.



{% include image.html url="/js/DatePicker/Behavior-Settings_images/Behavior-Settings_img1.png"%}



## Enabled

You can **Enable** or **Disable** the **DatePicker** widget. The “**enabled**” property is set to ‘**true**’ in **DatePicker** widget, by default. You can disable the **DatePicker** widget by setting the “**enabled**” property as ‘**false**’.

The following steps explain you how to disable the **DatePicker** widget.

In the HTML page, add a **&lt;input&gt;** element to render **DatePicker** widget.

{% highlight html %}
  
<input id="datepicker" type="text" />
       
{% endhighlight %}

{% highlight js %}
       
    // Add the code to disable the DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          enabled: false
       });
    });

{% endhighlight %}
  
## Enable strict mode

When **enableStrictMode** is set to ‘**true**’, **DatePicker** doesn’t allow the value out of the range, it internally changes to the correct value. The “**enableStrictMode**” property is set as ‘**false**’ in **DatePicker**, by default.

The following steps explain you how to enable the “**enableStrictMode**” for **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** Widget.

{% highlight html %}

<input id="datepicker" type="text"/>

{% endhighlight %}


{% highlight js %}

    // Add the code to enable the enableStrictMode for DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          enableStrictMode: true
       });
    });

{% endhighlight %}


## Fields

You can specify the **fields** **mapping** in **DatePicker**. You can also provide the support to add image, image styles, sprite css class, query, and HTML attributes.

The **DatePicker** widget provides support to customize the particular date, that is, you can customize the date with image and tooltip options. The following table specifies the special date fields and its configuration.

Special dates fields

<table>
   <tr>
      <th>Name</th>
      <th>
         Description
      </th>
      <th>
         Default value
      </th>
      <th>
         Data type
      </th>
   </tr>
   <tr>
      <td>
         date
      </td>
      <td>
         The date that has to be customized. 
      </td>
      <td>
         Null 
      </td>
      <td>
         String 
      </td>
   </tr>
   <tr>
      <td>
         tooltip
      </td>
      <td>
         Shows the tooltip to mention date while mouse hovering. 
      </td>
      <td>
         Null 
      </td>
      <td>
         String 
      </td>
   </tr>
   <tr>
      <td>
         iconClass 
      </td>
      <td>
         You can set the customized css with this property.
      </td>
      <td>
         Null 
      </td>
      <td>
         String
      </td>
   </tr>
</table>
N>  Set the image as background url and its styles within this class.

The following steps explain you how to specify the **fields** **mapping** in **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.

{% highlight html %}
  
<input id="datepicker" type="text" />

{% endhighlight %}


{% highlight js %}

    // Add the code to specify the fields mapping in DatePicker widget
    $(function() {
       var today = new Date(),
          spldays = [{
             date: new Date(today.getFullYear(), today.getMonth(), 1),
             tooltip: "In America",
             iconClass: "flag-am"
          }, {
             date: new Date(today.getFullYear(), today.getMonth() + 1, 6),
             tooltip: "In Argendina",
             iconClass: "flag-ar"
          }, {
             date: new Date(today.getFullYear(), today.getMonth() + 1, 27),
             tooltip: "In Bangladesh",
             iconClass: "flag-bd"
          }, {
             date: new Date(today.getFullYear(), today.getMonth() - 1, 3),
             tooltip: "In Brasil",
             iconClass: "flag-br"
          }, {
             date: new Date(today.getFullYear(), today.getMonth() - 2, 22),
             tooltip: "In Canada",
             iconClass: "flag-ca"
          }, ]
          // declaration
       $("#datepicker").ejDatePicker({
          specialDates: spldays,
          fields: {
             date: "date",
             tooltip: "tooltip",
             iconClass: "iconClass"
          }
       });
    });

{% endhighlight %}

Add the following styles to specify the **fields mapping** in **DatePicker** widget.

N> Images for this example are available in ‘installed location /Content/images’ and define the images in mentioned CSS. Henceforth the images are displayed.



{% highlight css %}

<style type="text/css" class="cssStyles">
   .flag .e-image {
   background: url("../Content/flags.png") no-repeat scroll -50px -75px rgba(0, 0, 0, 0);
   float: left;
   height: 15px;
   margin-left: 5px;
   margin-top: 3px;
   width: 20px;
   }
   .e-datepicker.e-calendar {
   width: 350px;
   }
</style>

{% endhighlight %}


The following screenshot displays the output for the above code example.

{% include image.html url="/js/DatePicker/Behavior-Settings_images/Behavior-Settings_img2.png"%}

## Define start day of the week

It specifies the **start day of the week** in **DatePicker** calendar. The “**value**” is set to **0** (Sunday), by default. 

The following steps explain you how to specify the **start day of the week** in **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.

{% highlight html %}  
  
<input id="datepicker" type="text" />
      
{% endhighlight %}

{% highlight js %}

    // Add the code to specify the start day of the week in DatePicker widget
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          startDay: 2
       });
    });

{% endhighlight %}

The following screenshot displays the output for the above code example.

{% include image.html url="/js/DatePicker/Behavior-Settings_images/Behavior-Settings_img5.png"%}

## Step months

It specifies the number of months to navigate at one click in next and previous button that is achieved by “**stepMonths”** property**.** You can change the **step months** by changing the default value by using “**stepMonths”** property. 

The following steps explain you how to specify the number of months to navigate at one click.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.
 
{% highlight html %}

<input id="datepicker" type="text"/>

{% endhighlight %}


{% highlight js %}

    // Add the code to specify the number of months to navigate at one click
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          stepMonths: 2
       });
    });

{% endhighlight %}

## Define value

It specifies the selected date value. You can specify the selected date value by using the “**value”** property.

The following steps explain you how to specify the selected value.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.


{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}

    // Add the code to specify the selected date value
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          value: new Date("5/8/2014")
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code example.



{% include image.html url="/js/DatePicker/Behavior-Settings_images/Behavior-Settings_img6.png"%}

## Watermark Text

It specifies the **Watermark Text** to display the input text in **DatePicker**. The “**watermarkText”** property is set as “**select date**” in **DatePicker**, by default. 

The following steps explain how to specify the **watermark Text** in **DatePicker** widget.

In the **HTML** page, add a **&lt;input&gt;** element to render **DatePicker** widget.


{% highlight html %}
  
<input id="datepicker" type="text" />
      
{% endhighlight %}
  
{% highlight js %}
    
    // Add the code to specify Watermark Text to be display in input text
    $(function() {
       // declaration
       $("#datepicker").ejDatePicker({
          watermarkText: "Enter date"
       });
    });

{% endhighlight %}


The following screenshot displays the output for the above code example.



{% include image.html url="/js/DatePicker/Behavior-Settings_images/Behavior-Settings_img7.png"%}

