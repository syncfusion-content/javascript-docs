---
layout: post
title: Theming-in-Essential-JavaScript-Components
description: theming in essential javascript components
platform: js
control: Introduction
documentation: ug
---

# Built-in Themes

All our EJ components are developed with a unique theme and different styling effects to improve its appearance and to have the unique look and feel. It is possible to easily customize the default available themes through the API provided by **Essential JavaScript**.

By default, there are **13** kinds of theming supports available for **Essential JavaScript** components. 

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* bootstrap-theme

The **Essential Studio** Suite provides a css file named **ej.web.all.min.css** for each of the above specified theme, which can be referred in your application, in order to apply the appropriate theming styles to the **EJ web components**. All the above specified theme files are available within the **css** folder which is depicted [here](/js/installation-and-deployment#assets).

## Adding specific theme to your application

To use only a single theme related stuffs in your application, it is not necessary to copy all the theme folders into your application. Just copy only the required files from the installed location and paste it within the **ej** folder present within the **Content** folder of your application. 

For example – Here, we are showing you how to refer only the **flat-saffron** theme to be applied to the **EJ** components in your application. Likewise, you can choose whatever themes you want. The **common-images** folder and **ej.widgets.core.min.css** file are mandatory for any application and is commonly applicable for whatever theme selected. 
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img1.png" %}

>   **Note**: The **common-images** folder is needed to be copied into your application mandatorily for any of the theme selection, as it includes all the common font icons and other images required for the control to render.

The below image depicts the files that are copied into the **Content** folder of your JS application,
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img2.png" Caption="Folder structure depicting the copied theme files in the application"%}

In the above image, **flat-saffron** folder is added to include the theme and styling related to it. If in case, you need to refer the **flat-lime** theme in your application, then you can replace the flat-saffron folder with flat-lime (copying it from the above specified location) - keeping the **common-images** folder and **ej.widgets.core.min.css** file as it is.

Once the required theme folders are copied into your application, it is necessary to refer the **ej.web.all.min.css** file in your HTML page within the &lt;head&gt; section before making any script reference as shown below,

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/flat-saffron/ej.web.all.min.css" rel="stylesheet" />
    <!-- Other required SCRIPT REFERENCES -->
</head>
<body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker();
        });
     </script>
</body>
</html> 

{% endhighlight %}

>   **Note**: The **ej.web.all.min.css** file is available separately for all the **13** available themes in their respective theme folders.
>   It is the combination of two files namely, **ej.theme.min.css** file (available separately within each of the theme folders) and **ej.widgets.core.min.css** – which is shown in the below image,   
>   {% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img3.png" %}
Since, **ej.web.all.min.css** file is a combination of two files (**ej.theme.min.css & ej.widgets.core.min.css**), therefore it is also possible to refer these two files directly in the place of its reference as shown below, 

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/ej.widgets.core.min.css" rel="stylesheet" />
    <link href="Content/ej/web/flat-saffron/ej.theme.min.css" rel="stylesheet" />
    <!-- Other required SCRIPT REFERENCES -->
</head>
<body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker();
        });
    </script>
</body>
</html>  

{% endhighlight %}

## Custom CSS

Essential JavaScript provides a default API namely **cssClass**, which accepts the custom CSS class name defined with specific user-defined styles and themes to be applied for the partial/whole parts of the EJ components.

### Applying CustomCSS to DatePicker control

Most of our EJ web components (like grid, schedule, datepicker and other tools controls) are built and developed by using one or more combinations of HTML child elements and some other components (dataVisualization controls like gauges, chart & bulletgraph) makes use of other elements like canvas, SVG and others. Therefore, each child-elements that are used to build a component is provided with a unique class name based on its purpose and usage. 

By default, the root element of each web components are given a unique class name which indicates the control name prefixed with **e-** (For example, DatePicker widget has a root element with a class name **e-datepicker** and the grid component contains its root element named with a class **e-grid** & so on). 

There are two possible ways to customize the theming of the component either by – 

* Overwriting the styles of specific child elements of a component by defining the customized styles explicitly in the sample side. 
* Replacing the entire css file with the Customized CSS class name and referring it in the application.

#### Overwriting the styles of specific child elements of a DatePicker widget:

By default, the header element of the DatePicker control which displays the Month name and year (outlined with blue line border in the below image) is defined by the class name **e-header** as depicted in the below image,
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img4.png" Caption="DatePicker control with header color displayed based on the theme applied."%}

To change the background-color of the above header element of the DatePicker, define the customized css styles to be applied for the header element (**e-header**) of the DatePicker within the **Style** section of the HTML page as shown below, 

{% highlight css %}

.customStyles .e-header {
   background-color: yellowgreen;
}

{% endhighlight %}

Now you need to assign the user-defined CSS class name to the DatePicker component’s property **cssClass** as depicted below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/flat-saffron/ej.web.all.min.css" rel="stylesheet" />
    <!-- Other required SCRIPT REFERENCES -->
  </head>
  <body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker({ cssClass: "customStyles" });
        });
    </script>
    <style>
        .customStyles .e-header {
            background-color: yellowgreen;
        }
    </style>
  </body>
</html>  

{% endhighlight %}

When you run the above code, the background color for the header element (**e-header**) of the DatePicker component will be customized with its background color changed to **yellowgreen** as shown below,
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img5.png" %}

Likewise, you can customize any of the specific child elements present within the component by using its class name preceded with the user-defined Custom CSS class name. The user-defined Custom CSS class name will be added to the root element of the Syncfusion widget (for the purpose of overwriting the default styles present in the theme initially applied to the widget) which can be seen in the above highlighted image.

Also, refer the required css file (**ej.web.all.min.css**) in your application as specified earlier, so as to include the default styling effects, font icon images and the other theming effects for the remaining classes of the component that are not customized explicitly with the custom CSS class name. 

#### Replacing the entire css file with the Customized CSS class name

To replace the entire css file with your own customized CSS class name, you need to copy the non-minified version (Src->**assets-src** folder) of the required theme file into your application and then modify it as per your needs. Also, make sure that the reference to it has been made in the HTML page and also the Customized class name set to the **cssClass** property of the EJ components. 

The non-minified version of the css files are present within the **assets-src** folder, as mentioned earlier in this [section](/js/installation-and-deployment#src). 

To customize the entire css file and refer it in your HTML page - Follow the usual steps as specified earlier for CSS reference, additionally copy and paste the non-minified version of the required css file into your application and refer it in the HTML page as depicted below, (For example, we have copied the **ej.theme.css** (non-minified) file present within the **flat-saffron** theme folder in our application)
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img6.png" %}

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My first HTML page</title>
    <link href="~/Content/ej/web/ej.widgets.core.min.css" rel="stylesheet" />
    <link href="~/Content/ej/web/flat-saffron/ej.theme.css" rel="stylesheet" />
    <!-- Other required SCRIPT REFERENCES -->
  </head>
  <body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker();
        });
    </script>
  </body>
</html>  

{% endhighlight %}

Now, to make particular changes in that file, you can directly open it and start making modifications. For example, The DatePicker control has its default root class name as **e-datepicker**. You can change it manually with the user-specified root class name such as **e-cutomdatepicker** in the css file as shown below,
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img7.png" Caption="CSS file with default root e-datepicker name"%}

{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img8.png" Caption="CSS file with Customized root class name"%}

To change/customize further the styles of the other child elements of the datepicker widget like header (**e-header** class), current-month and other-month, you need to modify the appropriate css properties within the **ej.theme.css** file as shown below,

**e-header** element with newly customized background-color
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img9.png" %}

**current-month** element with newly customized background-color
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img10.png" %}

**other-month** element with newly customized text color
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img11.png" %}

Save the changes made in the css file and then set the user-specified custom css class name(**e-customdatepicker**) to the **cssClass** property of the datepicker widget as shown below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My first HTML page</title>
    <link href="~/Content/ej/web/ej.widgets.core.min.css" rel="stylesheet" />
    <link href="~/Content/ej/web/flat-saffron/ej.theme.css" rel="stylesheet" />
    <!-- Other required SCRIPT REFERENCES -->
  </head>
  <body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker({ cssClass: "e-customdatepicker" });
        });
    </script>
  </body>
</html>  

{% endhighlight %}

Run the above code, you can see the datepicker widget with one or more customized child-elements according to the changes done in the css files as shown below,
{% include image.html url="/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img12.png" %}

Thus, the **cssClass** property of the EJ components can be used as per the user convenient to customize the widget style to improve its look and feel while using it within the application.































