---
layout: post
title: Horizontal-View
description: horizontal view
platform: js
control: Schedule
documentation: ug
---

# Horizontal View

* You can customize the appearance of the **Schedule** control by using schedule modes. This can change the view of the schedule. 

* It is possible to change the mode of the schedule. It can be customized by using **orientation** property.



**Orientation**

* It defines the orientation type of the **Schedule** control. It renders the **Schedule** either in horizontal mode or vertical mode. By default, orientation property is set as **Vertical**. 

* **ej.Schedule.Orientation.Vertical, ej.Schedule.Orientation.Horizontal** are the valid enum values that are accepted by **orientation** property.

* You can set the **Schedule** control to horizontal mode using the following code example.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            //Set Orientation as Horizontal mode
            orientation: ej.Schedule.Orientation.Horizontal
        });
    });


{% endhighlight %}



Execute the above code to render the following output.


![]("/js/Schedule/Horizontal-View_images/Horizontal-View_img1.png" Caption="schedule with horizontal view.")


The above example illustrates the horizontal view of **Schedule** control. Similarly you can also set the mode of the **Schedule** as “vertical”.



{% highlight html %}

<!DOCTYPE html>

<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <div style="float: left" id="Div1">
            </div>
        </div>
    </div>
</div>
<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            //Setting Orientation as Vertical mode
         orientation: ej.Schedule.Orientation.Vertical,

});
    });


{% endhighlight %}



Execute the above code to render the following output.

![]("/js/Schedule/Horizontal-View_images/Horizontal-View_img2.png" Caption="schedule with vertical view.")


**Resources**

**Horizontal Multiple Resources**

* **Horizontal Multiple Resource** feature provides support for rendering multiple resources on the **Schedule** control. You can group multiple resources under certain categories. You can also save the appointments simultaneously on multiple resources or within the multiple categories using **allowMultiple** property enabled for different levels of resources.

* Horizontal Multiple Resources is varied from Multiple resources by including the **orientation** property.It can change the appearance of the **Schedule**.

* Horizontal view contains another property as **resourceHeaderTemplateId.** It allows you to render the resource header of the **Schedule**. When the orientation is in horizontal mode, **resourceHeaderTemplateId** can be applied.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.HorizontalResourcesData).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            currentDate: new Date (2014,4,5),
            currentView:”month”,
            //Setting Orientation as Horizontal mode
          orientation: ej.Schedule.Orientation.Horizontal,
            group: {
                resources: ["Owners"]
            },
            //Setting multiple resources
          resources: [
          {
          field: "ownerId",
          title: "Owner",
          name: "Owners", allowMultiple: true,
          resourceSettings: {
          dataSource: [
          { text: "Nancy", id: 1, groupId: 1, color: "#f8a398" },
          { text: "Steven", id: 3, groupId: 2, color: "#56ca85" },
          { text: "Michael", id: 5, groupId: 1, color: "#51a0ed" }
          ],
          text: "text", id: "id", groupId: "groupId", color: "color"
          }
          }],
            //Setting Appointments
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule",
                resourceFields: "ownerId"
            }
        });
    });


{% endhighlight %}

Execute the above code to render the following output.

![]("/js/Schedule/Horizontal-View_images/Horizontal-View_img3.png" Caption="")


**Horizontal Resource Grouping**

* The **Schedule** control supports another important property as **group** related to the multiple resources that accepts the unique name assigned to each resources in the resource collection. The names that are all listed in this option is grouped in the **Schedule** control.

* It is possible to change the **orientation** in horizontal resource grouping. Horizontal view has another one property as **resourceHeaderTemplateId.** It allows to render the resource header of the schedule. When the orientation is in horizontal mode, **resourceHeaderTemplateId** can be applied.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

$(function () {
        width: "100%",
        currentDate: new Date (2014,4,5),
        currentView: "week",
        var dManager = ej.DataManager(window.HorizontalResourcesData).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            //Setting orientation as horizontal mode
          orientation: ej.Schedule.Orientation.Horizontal,
            //Grouping resources
          group: {
          resources: ["Rooms", "Owners"]
          },
            //Setting resources
          resources: [
          {
          field: "roomId",
          title: "Room",
          name: "Rooms", allowMultiple: false,
          resourceSettings: {
          dataSource: [
          { text: "Room1", id: 1, groupId: 1, color: "#cb6bb2" },
          { text: "Room2", id: 2, groupId: 1, color: "#56ca85" }],
          text: "text", id: "id", groupId: "groupId", color: "color"
          }
          }, {
          field: "ownerId",
          title: "Owner",
          name: "Owners", allowMultiple: true,
          resourceSettings: {
          dataSource: [
          { text: "Nancy", id: 1, groupId: 1, color: "#ffaa00" },
          { text: "Steven", id: 3, groupId: 2, color: "#f8a398" },
          { text: "Michael", id: 5, groupId: 1, color: "#51a0ed" },
          { text: "Laura", id: 7, groupId: 2, color: "#ffaa00" },
          { text: "Robert", id: 8, groupId: 1, color: "#f8a398" },
          { text: "Janet", id: 4, groupId: 2, color: "#51a0ed" }
          ],
          text: "text", id: "id", groupId: "groupId", color: "color"
          }
          }],
            //Setting appointments
            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule",
                resourceFields: "roomId,ownerId"
            }
        });
    });


{% endhighlight %}



Execute the above code to render the following output.

![]("/js/Schedule/Horizontal-View_images/Horizontal-View_img4.png" Caption="")
