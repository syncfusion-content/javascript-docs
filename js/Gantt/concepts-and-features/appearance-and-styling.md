---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: Gantt
documentation: ug
---

# Appearance and Styling

You can customize the look and feel of the **Gantt** control by applying themes and formatting the schedule header.

## Schedule Header Customization

You can customize the week header format and day header format in the **Schedule** part of the **Gantt** control by using the following code example.



{% highlight js %}


$("#GanttContainer").ejGantt({
    //...
    scheduleHeaderSettings: {
        weekHeaderFormat: "MMM yyyy",
        dayHeaderFormat: "d",
        weekendBackground: '#F2F2F2'
    }
});


{% endhighlight %}







The following screenshot shows the customized format schedule header in **Gantt** control.



{% include image.html url="\js\Gantt\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img1.png" Caption="Figure 52: Schedule Header Customization"%}

## Taskbar Customization

You can customize the **Taskbar** based on the task information in **Gantt** control to highlight the task. The following code example shows how to customize the **Taskbar** in **Gantt** control.



{% highlight js %}


$("#GanttContainer").ejGantt({
        //...
        queryTaskbarInfo: function (args) {//QUQERYTASKBARINFO EVENT IT WILL FIRE WHILE TASK RENDERING

            if (args.data.level === 0) {
                args.parentTaskbarBackground = "pink";
                args.parentProgressbarBackground = "cyan";
            } else {
                if (args.data.status == "60") {
                    args.progressbarBackground = "red";
                } else if (args.data.status == "70") {
                    args.progressbarBackground = "yellow";
                } else if (args.data.status == "80") {
                    args.progressbarBackground = "green";
                }
            }
        }

    });


{% endhighlight %}







The following screenshot shows the customized taskbar in **Gantt** control.



{% include image.html url="\js\Gantt\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img2.png" Caption="Figure 53: Customized taskbar"%}

## Themes

 You are provided the following twelve different themes in **Gantt** control.

1. Flat Azure                           

2. Flat Azure Dark                  

3. Flat Lime                             

4. Flat Lime Dark                   

5. Flat Saffron                        

6. Flat Saffron Dark

7. Gradient Azure

8. Gradient Azure Dark

9. Gradient Lime

10. Gradient Lime Dark

11. Gradient Saffron

12. Gradient Saffron Dark

You can apply the theme (Gradient lime) to the **Gantt** control by using the style sheet from the online link as follows.



{% highlight js %}

<!DOCTYPE html>

<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Getting Started with Gantt Control for JavaScript</title>
<!-- style sheet for default theme(gradient lime) -->
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /> 
//…

</html>


{% endhighlight %}



The following screenshot shows the **Gantt** control with Gradient-lime theme.

{% include image.html url="\js\Gantt\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img3.png" Caption="Figure 54: Gantt with Gradient lime theme"%}

