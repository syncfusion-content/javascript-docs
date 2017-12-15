---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Accordion 
documentation: ug
api: /api/js/ejaccordion
---

# Getting Started

This section explains briefly about how to create an **Accordion** in your application with **JavaScript**.

## Configure Accordion

This section encompasses the details on how you can configure the **Accordion** control in your application and customize it with various properties such as multiple open, rounded corner and icons for the **Accordion** header according to your requirement.

The following screenshot illustrates you the usage of **Accordion** control in listing the controls under the Essential Studio products. 

![](/js/Accordion/Getting-Started_images/Getting-Started_img1.png) 

The usage of **Accordion** control is described in the following sections.

## Create a Simple Accordion

Create an HTML file and add the following references to the required libraries.

{% highlight html %}

<html>
<head>
    <title>Essential Studio for JavaScript : Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- Add Accordion element here. -->
</body>
</html>
    

{% endhighlight %}



Add a &lt;div&gt; element. It is a container for Accordion control. The [width](https://help.syncfusion.com/api/js/ejaccordion#members:width) property is used to define the width of the Accordion control.



{% highlight html %}


<div id="accordion" style="width: 500px">
    <h3>
        <a href="#">Essential Studio ASP.NET</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        <ul>
            <li>
                <h4>DocIO</h4>
            </li>
            <li>
                <h4>Pdf  </h4>
            </li>
            <li>
                <h4>Gauge  </h4>
            </li>
            <li>
                <h4>Schedule  </h4>
            </li>
            <li>
                <h4>Diagram  </h4>
            </li>
            <li>
                <h4>Tools </h4>
            </li>
        </ul>
    </div>
    <h3>
        <a href="#">Essential Studio ASP.NET MVC</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        <ul>
            <li>
                <h4>Chart </h4>
            </li>
            <li>
                <h4>Grid  </h4>
            </li>
            <li>
                <h4>Gantt  </h4>
            </li>
            <li>
                <h4>Schedule  </h4>
            </li>
            <li>
                <h4>Diagram  </h4>
            </li>
        </ul>
    </div>
    <h3>
        <a href="#">Essential Studio JavaScript</a>
    </h3>
    <div>
        <!-- add accordion contents here to load contents under this header -->
        <ul>
            <li>
                <h4>Chart </h4>
            </li>
            <li>
                <h4>Grid  </h4>
            </li>
            <li>
                <h4>Gantt  </h4>
            </li>
            <li>
                <h4>Schedule  </h4>
            </li>
            <li>
                <h4>Diagram  </h4>
            </li>
        </ul>
    </div>
</div>


{% endhighlight %}


Create the Accordion control as follows.

{% highlight javascript %}
  
    $(function () {
        // document ready
        // Initialize Accordion control creation.
        $("#accordion").ejAccordion();
    });

{% endhighlight %}

You can execute the above code example to display the Accordion control with simple control list.



![](/js/Accordion/Getting-Started_images/Getting-Started_img2.png) 

You can customize the Accordion control using various properties. The Accordion control properties and its default values are described in the following section.

## Configure Multiple Open

You can have multiple **Accordion** tabs opened to view all products at a time. To achieve this set the [enableMultipleOpen](https://help.syncfusion.com/api/js/ejaccordion#members:enablemultipleopen) property of the **Accordion** control to true.

N> enableMultipleOpen property is false by default.

You can also open all the panels during initialization using the [selectedItems](https://help.syncfusion.com/api/js/ejaccordion#members:selecteditems) property of the **Accordion** control. The following code sample illustrates the opening of multiple tabs by passing the tab index values of tab.

{% highlight javascript %}

    $(function () {
        $("#accordion").ejAccordion({
            enableMultipleOpen: true, /* To set the multiple content panels  active at a time   */
            selectedItems: [0, 1, 2]  /* To set the selected panels  active at a time   */
        });
    });   


{% endhighlight %}



**Accordion** control with **enableMultipleOpen** property is illustrated in the following screen shot.

![](/js/Accordion/Getting-Started_images/Getting-Started_img3.png) 

### Setting rounded corner

**Accordion** control, by default, is rendered in a regular rectangle. You can modify the regular rectangles with rounded corners by setting the [showRoundedCorner](https://help.syncfusion.com/api/js/ejaccordion#members:showroundedcorner) property to **True**. You can select the items on rendering by using [selectedItems](https://help.syncfusion.com/api/js/ejaccordion#members:selecteditems) property.

N> showRoundedCorner property is False by default.



{% highlight javascript %}

    $(function () {
        $("#accordion").ejAccordion({
            enableMultipleOpen: true,
            selectedItems: [0, 1, 2],
            showRoundedCorner: true /* To set rounded corner for the accordion headers   */
        });
    });       

{% endhighlight %}

The following screenshot illustrates the **Accordion** control with rounded corners.

![](/js/Accordion/Getting-Started_images/Getting-Started_img4.png) 

## Customize Icon

You can customize the **Header** icon using [customIcon](https://help.syncfusion.com/api/js/ejaccordion#members:customicon) property. This property has two features such as **header** and **selectedHeader**. By default, the classes of **header** and **selectedHeader** are **e-collapse** and **e-expand** respectively**.**

You can change the + and - symbols in the **Accordion** header, that are the default icons with Up or Down arrow icons. 

Up or Down arrow icons are available in **e-arrowheadup** and **e-arrowheaddown** classes respectively in the ej.widgets.core.min.css stylesheets from the sample. 

You can set the Up or Down arrow icon to **Accordion** header, by adding **e-arrowheadup** and **e-arrowheaddown** class to **selectedHeader** and **header** properties respectively.

{% highlight javascript %}

  
    $(function () {
        $("#accordion").ejAccordion({
            enableMultipleOpen: true,
            selectedItems: [0, 1, 2],
            showRoundedCorner: true,
            customIcon: {
                header: "e-arrowheaddown", /*  To set icon for the collapsed accordion headers  */
                selectedHeader: "e-arrowheadup" /*  To set icon for the selected accordion headers  */
            }
        });
    });
  


{% endhighlight %}



The following screenshot illustrates the customization of **selectedHeader** and **header** of the **Accordion** control.

![](/js/Accordion/Getting-Started_images/Getting-Started_img5.png) 

