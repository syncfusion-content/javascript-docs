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



{% highlight js %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Schedule JS Print Sample</title>
<!-- Refer the necessary scripts here-->
</head>
<body>
<input class="print" type="button" value="Print" />
<div style="float: left" id="Schedule1" />
<div id="Schedule1"> </div>
<script type="text/javascript">
$(function () {
var dManager = ej.DataManager(window.Timemode).executeLocal(ej.Query().take(10));
$("#Schedule1").ejSchedule({
// Add the necessary schedule properties here
});
// function to bind the click event to the button
$('.print').bind("click", function () {
var obj = $("#Schedule1").data("ejSchedule");
// Public method to print the schedule
**obj.print();**
});
});

</script>
</body>
</html>



{% endhighlight %}



Execute the above code to render the following output.

![](Print_images/Print_img1.png)
{:.image }


{:.caption }


_Figure_ _121__: Schedule with print button_

Click the print button to render the following output.



![](Print_images/Print_img2.png)
{:.image }


{:.caption }


_Figure_ _122__: Schedule with Print window_

**Appointment Print**

* In **Schedule** control, you can print the appointment alone by using context menu. Add print as menu item in the context menu settings as in the following code example.



{% highlight js %}

<div id="Schedule1"> </div>
<script>
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
**{ id: "print", text: "Print Appointment" }**
]
}
},
// Add the Appointment setting collection here
});
});
</script>



{% endhighlight %}



* Right click on the appointment and select print appointment in the context menu as follows.



![](Print_images/Print_img3.png)
{:.image }


{:.caption }


_Figure_ _123__: Schedule with Print option in Context Menu_

* Now, the widow is promoted to new document with appointment details and print window opens.



![](Print_images/Print_img4.png)
{:.image }


{:.caption }


_Figure_ _124__: Schedule with Appointment Print_



