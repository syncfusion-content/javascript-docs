---
layout: post
title: Print
description: print
platform: js
control: Schedule
documentation: ug
---

# Print

**Schedule** control is provided with the Print feature. You can print the entire **Schedule** control or separately print the appointment based on your requirement.

**Schedule Print**

You can print the **Schedule** control by using **print()** method. Use the following code example to print the **Schedule** control.



{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>Schedule JS Print Sample</title>
    <!-- Refer the necessary scripts here-->
</head>
<body>
    <input class="print" type="button" value="Print" />
    <div style="float: left" id="Div1" />
    <div id="Div2"></div>
</body>
</html>

{% endhighlight %}

{% highlight js %}

$(function () {
        var dManager = ej.DataManager(window.Timemode).executeLocal(ej.Query().take(10));
        $("#Schedule1").ejSchedule({
            // Add the necessary schedule properties here
        });
        // function to bind the click event to the button
        $('.print').bind("click", function () {
            var obj = $("#Schedule1").data("ejSchedule");
            // Public method to print the schedule
             obj.print();
            });
    });


{% endhighlight %}



Execute the above code to render the following output.

 {% include image.html url="/js/Schedule/Print_images/Print_img1.png" Caption="schedule with print button."%}

Click the print button to render the following output.


{% include image.html url="/js/Schedule/Print_images/Print_img2.png" Caption="schedule with Print window."%}


**Appointment Print**

* In **Schedule** control, you can print the appointment alone by using context menu. Add print as menu item in the context menu settings as in the following code example.


{% highlight html %}

<div id="Schedule1"></div>

{% endhighlight %}


{% highlight js %}

 $(function () {
        var dManager =
        ej.DataManager(window.Default).executeLocal(ej.Query().take(10));

        $("#Schedule1").ejSchedule({
            // To Add the Context menu settings
            contextMenuSettings: {
                // To Enable the Context menu
                enable: true,
                // To Add menu items
                menuItems: {
                    appointment: [
                    { id: "open", text: "Open Appointment" },
                    { id: "delete", text: "Delete Appointment" },
                    // To Add print item in that collection.
                    { id: "print", text: "Print Appointment" }
                    ]
                }
            },
            // Add the Appointment setting collection here
        });
    });



{% endhighlight %}


Right click on the appointment and select print appointment in the context menu as follows.

{% include image.html url="/js/Schedule/Print_images/Print_img3.png" Caption="schedule with Print option in Context Menu."%}

 Now, the widow is promoted to new document with appointment details and print window opens.

{% include image.html url="/js/Schedule/Print_images/Print_img4.png" Caption="schedule with Appointment Print."%}

