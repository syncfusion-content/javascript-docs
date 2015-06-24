---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Schedule
documentation: ug
---

# Context Menu

**Schedule** control is added with the context menu options that opens when you right-click over the cells or appointments. In addition to the default menu items available, it allows you to add the custom menu items and also the sub menu-items as per your requirement.

**contextMenuSettings**

It is a collection that holds the menu items data.

**enable**

It specifies whether to enable/disable the Context menu options.

**menuItems**

It holds the appointment and cell related menu and custom-menu options.

**appointment**

This collection accepts the id, text and parent Id of the menu items that are to be displayed when you right-click the appointments. It can also include custom-menu items.

**cells**

This collection accepts the id, text and parent Id of the menu items that are to be displayed when you right-click the **Schedule** cells. It  also include custom-menu items.

**Appointment Menu Items**

* By default, the appointment menu options are provided with 2 items namely **Open Appointment** and **Delete Appointment**. 

* If you want to customize and use your own custom menu items, then you can replace the appointment menu items with their desired collections as explained in the following code.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [
                    { id: "open", text: "Open Appointment" },
                    { id: "delete", text: "Delete Appointment" },
                  // Custom context menu items
                    { id: "customMenu3", text: "Menu Item 3" },
                    { id: "customMenu4", text: "Menu Item 4" }
                    ]
                }
            },
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



Execute the above code to render the following output.

{% include image.html url="/js/Schedule/Context-Menu_images/Context-Menu_img1.png" Caption=""%}


**Categorize** 

* A new default menu item is included in the appointment menu items to support the categorize option through context menu. 

* The categorize data collection that are passed through the categorizesettings is utilised in rendering the categorize options in the context menu. 

You can refer the following code example to render the categorize options in the context menu.\

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}

{% highlight js %}

 $(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    appointment: [
                    { id: "open", text: "Open Appointment" },
                    { id: "delete", text: "Delete Appointment" },
                    //  the categorize menu item
                      { id: "categorize", text: "Categorize" }
                    ]
                }
            },
            // categorize data collection
            categorizeSettings:
            {
                enable:true,
                dataSource: [
                { text: "Blue Category", id: 1, color: "#7499e1", fontColor: "red" },
                { text: "Green Category", id: 2, color: "#7cce6e", fontColor: "white" },
                { text: "Orange Category", id: 3, color: "#ffaa00", fontColor: "green" }
                ],
                text: "text", id: "id", color: "color",fontColor: "fontColor"**
                },

            appointmentSettings: {
                dataSource: dManager,
                id: "Id",
                currentDate: new Date (2014,4,5),
                subject: "Subject",
                startTime: "StartTime",
                endTime: "EndTime",
                allDay: "AllDay",
                recurrence: "Recurrence",
                recurrenceRule: "RecurrenceRule",

                // bind the resource id fields collection of each level
                categorize:"Categorize"
            }
        });
    });


{% endhighlight %}



Execute the above code to render the following output with categorized appointments. Also when you right click “Appointment”, the context menu with categorize option is displayed as follows.

{% include image.html url="/js/Schedule/Context-Menu_images/Context-Menu_img2.png" Caption=""%}

**Cells** 

* By default, the cells menu options are provided with 5 items namely **New Appointment, New Recurring Appointment, Today, Go to Date** and **Settings with sub-options for views, time-mode and highlighting business hours**. 

* You can customize and use your own custom menu itemsby replacing the cell menu items with the desired collection as explained in the following code example.

{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

$(function () {
        var dManager = ej.DataManager(window.Default).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            width: "100%",
            height: "525px",
            currentDate: new Date(2014, 4, 5),
            contextMenuSettings: {
                enable: true,
                menuItems: {
                    cells: [
                  { id: "new", text: "New Appointment" },
                  { id: "recurrence", text: "New Recurring Appointment" },
                  { id: "today", text: "Today" },
                  { id: "gotodate", text: "Go to date" },
                  { id: "settings", text: "Settings" },
                  { id: "view", text: "View", parentId: "settings" },
                  { id: "timemode", text: "TimeMode", parentId: "settings" },
                  { id: "view_Day", text: "Day", parentId: "view" },
                  { id: "view_Week", text: "Week", parentId: "view" },
                  { id: "view_Workweek", text: "Workweek", parentId: "view" },
                  { id: "view_Month", text: "Month", parentId: "view" },
                  { id: "timemode_Hour12", text: "12 Hours", parentId: "timemode" },
                  { id: "timemode_Hour24", text: "24 Hours", parentId: "timemode" },
                  { id: "businesshours", text: "Business Hours", parentId: "settings" },
                // Custom context menu items
                  { id: "customMenu1", text: "Menu Item 1" },
                  { id: "customMenu2", text: "Menu Item 2" }
                    ]
                }
            },
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


Execute the above code to render the following output when you right-click on the cells.

{% include image.html url="/js/Schedule/Context-Menu_images/Context-Menu_img3.png" Caption=""%}
