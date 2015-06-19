---
layout: post
title: Getting-started
description: getting started
platform: js
control: Schedule
documentation: ug
---

# Getting started

****

* This section encompasses on how to configure the **Schedule** control for your business requirements. You can pass any data that are bound to the **Schedule** control through various API’s available within it.

*  The most important data used in the **Schedule** control is the appointment data that is bound to it through the **appointmentSettings** and **DataSource** property. The appointment data can either be passed locally or remotely to the **Schedule** control.

* In addition, there are several options available in the **Schedule** control to customize the appearance and behaviour of it. In this example, you can see how to add a **Schedule** control to an application to manage some of the important activities in a worksheet.  

The following screenshot displays the **Schedule** control with daily important activities

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img1.png" Caption="Schedule Control with Daily Important Activities."%}



**Create a Schedule**

* Create an **HTML** file and then add the following references to the required libraries.



{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta charset="utf-8" />
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
</head>



{% endhighlight %}

 Now, add a &lt;div&gt; element within the **body** section which will act as a container for **ejSchedule** widget.



{% highlight html %}

	<body>
		<div id="Schedule1"></div>
	</body>
	</html>


{% endhighlight %}


Once the container is added, create the **ejSchedule** widget within the **script** section as follows,



{% highlight js %}


$(function () {
        $("#Schedule1").ejSchedule();
    });



{% endhighlight %}


You can run the above code example and an empty **Scheduler** is displayed without appointments. In order, to display the appointments in the **Schedule**, you need to pass data to it. 

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img2.png" Caption="Empty Scheduler without Appointments."%}


**Pass data to Schedule control**

* You can add appointment to the **Schedule** control by passing data to the **Schedule** control either locally or remotely. In the following code example, you can see how to bind the remote data to the **Schedule** control.

* In order to bind the remote data to the **Schedule** control from the **OdataServices**, assign the remote service **URL** to the **DataSource** property of the **Scheduler** as follows.



{% highlight js %}

  var dManager = ej.DataManager({
        url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc"
    });    // DataManager creation
    var queryString = ej.Query().from("Events").take(10);   // Query creation
    $(function () {
        $("#Schedule1").ejSchedule({
            appointmentSettings: {
                dataSource: dManager, query: queryString
            }
        });
    });


{% endhighlight %}


When the **DataSource** property is assigned with the specific service **URL**, assign the **queryString** to the **query** property, which specifies the table from where the records should be retrieved.You can also bind the field names used in the referred table “**Events**” with the corresponding **appointmentSettings** property of the **Scheduler** as shown in the following code example.



{% highlight js %}


 $(function () {
        $("#Schedule1").ejSchedule({
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                query: queryString,
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



The following screenshot displays a **Schedule** control with the appointments in a normal style.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img3.png" Caption="Schedule Control with Appoinments in Simple Style."%}


You can also customize the appointments within the **Scheduler** using the **template** support discussed in the following sections.

**Add Templates to the appointments**

* You can change the appearance of the appointments and add images for visually appealing look-and-feel of the appointments. You can use the template concept to achieve this.

* In order to add templates to the **Schedule** appointments, you need to pass the **id** of the template to the “**appointmentTemplateId”** property. 



{% highlight js %}


$(function () {
        $("#Schedule1").ejSchedule({
            appointmentTemplateId: "#apptemplate",
            width: "100%", height: "550px",
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                query: queryString,
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
    $.views.helpers({ format: _getImages });
    function _getImages(date) {     // Method to choose images for the appointments
        switch (new Date(date).getDay()) {
            case 0:
                return "<img src='Images/cake.png'/>"
                break;
            case 1:
                return "<img src='Images/basketball.png'/>"
                break;
            case 2:
                return "<img src='Images/rugby.png'/>"
                break;
            case 3:
                return "<img src='Images/guitar.png'/>"
                break;
            case 4:
                return "<img src='Images/music.png'/>"
                break;
            case 5:
                return "<img src='Images/doctor.png'/>"
                break;
            case 6:
                return "<img src='Images/beach.png'/>"
                break;
        }
    }
	

	{% endhighlight %}
	
{% highlight html %}

<div style="height: 100%">
    <div style='float: left; width: 50px;'>
        {{:~format(StartTime)}}
    </div>
    <div>
        <div>{{:Subject}}</div>
    </div>
</div>

{% endhighlight %}


> Important: The images in the above code snippet are taken from the installation location of the Essential JavaScript Studio in your machine,
> For example: $system drive: \Program Files\ Syncfusion\EssentialStudio\12.1.0.43\JavaScript\samples\web\images\schedule
> You can create a folder named “Images” in the same location as your newly created HTML file and then move all the images from the installation folder to the newly created “Images” folder. This helps you in referring appointments appropriately within the Schedule control.

Once you set the template for the appointments, the **Scheduler** is displayed with the customized appointments as shown in the following screenshot.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img4.png" Caption="Scheduler with Customized Appointments."%}



**Change the Schedule View**

* You can change the view of the **Schedule** from **week** to **month** by using the **currentView** property. By default, the **Schedule** control is displayed in a **“week”** view.



{% highlight js %}


 $(function () {
        // DataManager creation
        var dManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc"
        });
        // Query creation
        var queryString = ej.Query().from("Events").take(10);
        $("#Schedule1").ejSchedule({
            appointmentTemplateId: "#apptemplate",
            width: "100%", height: "550px", currentView: "month",
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                query: queryString,
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
    $.views.helpers({ format: _getImages });
    function _getImages(date) {    // method to choose images for the appointments
        switch (new Date(date).getDay()) {
            case 0:
                return "<img src='Images/cake.png'/>"
                break;
            case 1:
                return "<img src='Images/basketball.png'/>"
                break;
            case 2:
                return "<img src='Images/rugby.png'/>"
                break;
            case 3:
                return "<img src='Images/guitar.png'/>"
                break;
            case 4:
                return "<img src='Images/music.png'/>"
                break;
            case 5:
                return "<img src='Images/doctor.png'/>"
                break;
            case 6:
                return "<img src='Images/beach.png'/>"
                break;
        }
    }

{% endhighlight %}

{% highlight html %}


<div style="height: 100%">
    <div style='float: left; width: 50px;'>
        {{:~format(StartTime)}}
    </div>
    <div>
        <div>{{:Subject}}</div>
    </div>
</div>

{% endhighlight %}


When you execute the above code example, a **Scheduler** is displayed as follows with the fixed appointment height in a **month** view. 

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img5.png" Caption="Scheduler with the fixed appointment height in a month view."%}



**Change the appointment height through CSS**

* The default height of an appointment is always suitable for the text.  In order to display an image and text in the appointment, you can change the height of the appointments in a **month** view, through **css** styles manually as shown in the following code example.  You can set the appointment height to **auto** to display the images within it.



{% highlight css %}

.e-monthappointment
{
	height:auto !important;
}

{% endhighlight %}




{% highlight js %}


 $(function () {

        // DataManager creation
        var dManager = ej.DataManager({
            url: "http://mvc.syncfusion.com/OdataServices/Northwnd.svc"
        });
        // Query creation
        var queryString = ej.Query().from("Events").take(10);
        $("#Schedule1").ejSchedule({
            appointmentTemplateId: "#apptemplate",
            width: "100%", height: "550px", currentView: "month",
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                query: queryString,
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
    $.views.helpers({ format: _getImages });
    function _getImages(date) {    // Method to choose images for the appointments
        switch (new Date(date).getDay()) {
            case 0:
                return "<img src='Images/cake.png'/>"
                break;
            case 1:
                return "<img src='Images/basketball.png'/>"
                break;
            case 2:
                return "<img src='Images/rugby.png'/>"
                break;
            case 3:
                return "<img src='Images/guitar.png'/>"
                break;
            case 4:
                return "<img src='Images/music.png'/>"
                break;
            case 5:
                return "<img src='Images/doctor.png'/>"
                break;
            case 6:
                return "<img src='Images/beach.png'/>"
                break;
        }
    }

{% endhighlight %}

{% highlight html %}

<div style="height: 100%">
    <div style='float: left; width: 50px;'>
        {{:~format(StartTime)}}
    </div>
    <div>
        <div>{{:Subject}}</div>
    </div>
</div>

{% endhighlight %}



After setting the height for appointments in **month** view, the **Schedule** control is rendered as follows,

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img6.png" Caption="Scheduler with appointments in month view."%}


**Manipulate the Appointments**

**Appointment Creation**

* Initially, you looked at how the appointments are rendered by binding the remote data. In order to add the appointments through the user interface (run-time) to the **Schedule** control, double-click on the appropriate **Schedule** cell and provide the required details in the appointment window pop-up.

* You can quickly create an appointment by clicking on the exact **Schedule** cell with appropriate time slot and then fill only the subject of that appointment in a quick appointment pop up. 



> Important: While adding new appointments to the Schedule control either by using local or remote data, the new appointment data is saved automatically to the appointment collection.



The following screenshot displays an appointment window pop- up that appears when you double-click on the **Schedule** cells.


{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img7.png" Caption="Appointment with Pop-up Dialog."%}


The following screenshot illustrates a quick appointment pop-up window.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img8.png" Caption="Quick Appointment Pop-up Window."%}


> Important: In case, you need to manipulate with newly created or edited appointments, you can use the events available within the Schedule control.


* The event named **appointmentSaved** is triggered while saving a new appointment to the **Schedule** control. It provides the new appointment data as an argument that helps you to retrieve the newly entered appointment data through a function. 

**Edit/Delete Appointments**

* You can edit or delete the appointments in the **Schedule** control and access the data using events namely “**appointmentEdited**” and “**appointmentDeleted**” respectively. 

* In order to edit the appointments, double-click the desired appointment, and then edit the required fields in the appointment pop-up as shown in the following screenshot.


{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img9.png" Caption="Edit Appointments Pop-up."%}


To delete an appointment, click the appointment, and then click **delete** icon in the quick appointment pop-up as shown in the following screenshot.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img10.png" Caption="Delete Appointments Pop-up Window."%}


* You can also delete the appointment by selecting the required appointment in the **Schedule** control and click the delete key option. This works only when you set “**allowKeyboardNavigation**” option to **“True”**.

**Manipulate Recurrence Appointments**

**Add Recurrence Appointment**

* To add **recurrence** appointments, you need to check the “**repeat**” option in the appointment window as shown in the following screenshot.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img11.png" Caption="Repeat Appointments."%}


When you check the **repeat** option, the sub-options available in the recurrence category are shown in the appointment pop-up as follows.


{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img12.png" Caption="Options in Recurrence Dialog."%}


You can choose the required recurrence pattern from the available options and then click **Done**. The main appointment pop-up appears as shown in the following screenshot.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img13.png" Caption="Main Appointment Dialog."%}


Click **Done**. The recurrence appointment with daily pattern is created for every two days that ends after 10 occurrences.

{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img14.png" Caption="recurrence appointment with daily pattern."%}


* You can store the chosen recurrence options usually in a **RecurrenceRule** field in a string format.  Also, the **Recurrence** field indicates whether the appointments created are normal or recurrence type. You can create appointments in a **recurrence** type by setting **Boolean** type to **“True”**.

**Edit/Delete Recurrence Appointment**

* You can follow the same procedure of normal appointments for editing/deleting recurrence appointments too. But in **recurrence****appointment**, you can either edit/delete the single occurrence of the appointment or the entire series in an intermediate confirmation pop-up.

* When you double-click the **recurrence** appointment a pop-up window appears as shown in the following screenshot. 


{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img15.png" Caption="Double-Click the Recurrence Appointment."%}


When you click the recurrence appointment, a quick appointment window opens with the following options: **Edit Appointment** and **Edit Series** for editing the appointments - **delete** icon for deleting the appointments.


{% include image.html url="/js/Schedule/Getting-started_images/Getting-started_img16.png" Caption="Quick Appointment Window."%}


**Behaviour Customization using the events**

**Restrict the display of appointment window**

* You can restrict creation of the appointments during weekends in **Schedule** **JS** using the events and validating its arguments such as **starttime** and **endtime**.

* For example, you can block the appointment pop-up on all the weekends (Default week start date is Monday) using the following code sample with **appointmentWindowOpen** event. 



{% highlight js %}

$(function () {
        $("#Schedule1").ejSchedule({
            appointmentTemplateId: "#apptemplate",
            width: "100%", height: "550px",
            currentDate: new Date(2014, 4, 5),
            appointmentSettings: {
                dataSource: dManager,
                query: queryString,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule"
            },
            appointmentWindowOpen: "onAppointmentBeforeOpen"
        });
    });
    function onAppointmentBeforeOpen(args) {
        if (new Date(args.startTime).getDay() == 0 || new Date(args.startTime).getDay() == 6)
            args.cancel = true; // prevents display of appointment pop-up
    }

{% endhighlight %}

