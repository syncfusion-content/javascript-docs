---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: Schedule
documentation: ug
---

# Appearance and Styling

**Adaptive Schedule**

* The **Schedule** control has been provided with the built-in support for adaptive functionality. With this behaviour enabled, the **Schedule** control can be accessed in any of the mobile devices as per the screen size. 

* To enable the adaptive layout of the **Schedule** control, it is necessary to set the property **isResponsive** to **True.** By default, it is set to **false**. 

* When the **isResponsive** property is set to **true**, the **Schedule** control automatically chooses the appropriate rendering method to display it either on the mobile or desktop mode, based on the screen size it is rendered. Except the horizontal mode orientation, all the other default functionalities of the **Schedule** control are supported in this feature. 

**Dependencies**

For **Adaptive Schedule**, you can refer to the following **css** file in the application that can be downloaded from the link,

[http://www.syncfusion.com/downloads/support/directtrac/general/Responsive.zip](http://www.syncfusion.com/downloads/support/directtrac/general/Responsive.zip)


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}
 $(function () {
        var scheduleObj = $("#Schedule").ejSchedule({
            width: "100%",
            height: "500px",
            isResponsive: true,
            appointmentSettings: {
                dataSource: window.Default,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                description: "Description",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule",
            },
        });
    });


{% endhighlight %}

{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Schedule displaying default view in mobile mode."%}


{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Schedule displaying multiple resources in mobile mode."%}


* [Click here](http://js.syncfusion.com/demos/web/) to see the__working of__**Adaptive Schedule****.**



**Show/Hide All Day Show** 

* The all-day cells row in the Schedule control can be displayed or hidden from the user. When the showAllDayRow is set to false, the allday row is hidden from the user.

*  By default, this property is set to true.The following code example explains how to use the showAllDayRow property of the Schedule control.  


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            // Disables the showAllDayRow property to the schedule
            showAllDayRow:false,
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });
{% endhighlight %}



The following screenshot displays the **Schedule** control with all-day row hidden,

{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img3.png" Caption="Schedule with disabled all day row."%}


**Adjust Schedule Size**

**Height**

* The height of the **Schedule** control is handled using the **height** property that accepts only the pixel values.

* By default, the **Schedule** control is set with the height of 800px.

The following code eample explains how to change the height of the Schedule control.  

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "500px",
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });



{% endhighlight %}

The following screenshot displays the **Schedule** control with the height set to “500px”. 


{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img4.png" Caption="Adjusting schedule size height."%}

**width**

* The width of the **Schedule** control is handled with the **width** property that accepts both the pixel values as well as percentage values. 

* By default, the **schedule** control is set with the width of 800px.

The following code example explains how to change the width of the **Schedule** control,  


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}
$(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            width: "600px",
            height: "500px",
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            }
        });
    });



{% endhighlight %}


The following screenshot displays the **Schedule** control with the width set to “600px”.


{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img5.png" Caption="Adjusting schedule size width."%}

**Adjust Cell Size**

* The size of the cells within the **Schedule** control can be customized with two of the available options, **cellWidth** and **cellHeight**. 

* In order to view the appointments more clearly within the schedule control, you can enhance the height and width of the cells using these options.

**cellHeight**

* The cell height of the **Schedule** control is handled with the **cellHeight** property that accepts only the pixel values.

**cellWidth**

* The cell width of the **Schedule** control is handled with the **cellWidth** property that accepts only the pixel values.

The following code example explains how to change the cell height and width of the **Schedule** control.  


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}
 
    $(function () {
        var datamanager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#schedule").ejSchedule({
            width: "800px",
            height: "525px",
            // Setting the cell width and height of the schedule
            cellWidth: "160px",
            cellHeight: "60px",
            appointmentSettings: {
                dataSource: datamanager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule:"RecurrenceRule"
            },
        });
    });


{% endhighlight %}




The following screenshot displays the **Schedule** control with the cell width set to “160px” and cell height set to “60px”.

{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img6.png" Caption="Schedule with modified cellHeight and cellWidth."%}



**Theme**

* **Schedule** control’s style and appearance is controlled based on CSS classes. In order to apply styles to the **Schedule** control, you are required to refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. 

* When the **ej.widgets.all.min.css** file****is referred, it is not necessary to include the **ej.widgets.core.min.css** and **ej.theme.min.css** files in your project as **ej.widgets.all.min.css** is the combination of these two files. 

* By default, there are 12 theme support available for **Schedule** control namely,

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



Replace the following code in Create Schedule Step1 to apply different theme to schedule control.



{% highlight html %}

<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-saffron-dark/ej.web.all.min.css" rel="stylesheet" />

<!—You can replace the highlighted theme with any one of the above mentiond 12 themes-->

{% endhighlight %}



The schedule control will render as follows

{% include image.html url="/js/Schedule/Appearance-and-Styling_images/Appearance-and-Styling_img7.png" Caption="Schedule with applied theme."%}
