---
layout: post
title: Using Syncfusion Essential JS Built-in themes
description: How to use the built-in themes of essential js widgets in your application and customizing of the existing themes.
platform: js
control: Introduction
documentation: ug
---

# Built-in Themes

All our Syncfusion Essential JS widgets are developed with a unique theme and different styling effects to improve its appearance and to have the unique look and feel. It is possible to easily customize the default available themes through the APIs*.

By default, there are 13 themes available for Essential JavaScript widgets. 

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

Syncfusion provides a CSS file named **ej.web.all.min.css** for each of the above specified theme, which can be referred in your application, in order to apply the appropriate theming styles to the widgets. All the above specified theme files are available within the **css** folder which is mentioned [here](/js/installation-and-deployment#install-location).

## Adding specific theme to your application

To use only a single theme in your application, you can copy only the required files from the [installed location](/js/installation-and-deployment#install-location) and paste it in your application folder (for ex, Application\Content\ej). 

This section explains what are all the files required to refer and the steps to apply the **flat-saffron** theme. 

1. Create the following folders in the same structure under your application folder. 

N>   appfolder\Content\ej\flat-saffron

2. Copy **common-images** folder & **ej.widgets.core.min.css** file into the appfolder\Content\ej

N> Both of these folders and files are mandatory for any themes. 

3. Copy the CSS files available in the installed location of the flat-saffron folder into your app location appfolder\Content\ej\flat-saffron
4. Refer the **ej.web.all.min.css** file in your HTML page within the `<head>` section before making any script reference as shown below,

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

5. As **ej.web.all.min.css** file is a combination of **ej.theme.min.css & ej.widgets.core.min.css, it is also possible to refer these two files directly in the place of its reference as shown below, 

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

## Customizing themes

Each of Essential JavaScript widgets provide a default API `cssClass`, which accepts the custom CSS class name defined with specific user-defined styles and themes to be applied for the partial/whole parts of the Essential JS widgets.

### Applying Custom CSS to DatePicker control

By default, the root element of each web widgets are given a unique class name which indicates the control name prefixed with **e-** (For example, DatePicker widget has a root element with a class name `e-datepicker` and the grid component contains its root element named with a class `e-grid` & so on). 

There are two possible ways to customize the theming of the component either by – 

* Overwriting the styles of specific child elements of a component by defining the customized styles explicitly in the sample side. 
* Replacing the entire CSS file with the Customized CSS class name and referring it in the application.

#### Overwriting the styles of specific child elements of a DatePicker widget:

By default, the header element of the DatePicker control which displays the Month name and year (outlined with blue line border in the below image) is defined by the class name **e-header** as depicted in the below image,
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img4.png)

DatePicker control with header color displayed based on the theme applied.
{:.caption}

To change the background-color of the above header element of the DatePicker, define the customized CSS styles to be applied for the header element (**e-header**) of the DatePicker within the **Style** section of the HTML page as shown below, 

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

When you run the above code, the background color for the header element (**e-header**) of the DatePicker component will be customized with its background color changed to **yellow green** as shown below,
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img5.png) 

Likewise, you can customize any of the specific child elements present within the component by using its class name preceded with the user-defined Custom CSS class name. The user-defined Custom CSS class name will be added to the root element of the Syncfusion widget (for the purpose of overwriting the default styles present in the theme initially applied to the widget) which can be seen in the above highlighted image.

Also, refer the required CSS file (**ej.web.all.min.css**) in your application as specified earlier, so as to include the default styling effects, font icon images and the other theming effects for the remaining classes of the component that are not customized explicitly with the custom CSS class name. 

#### Replacing the entire CSS file with the Customized CSS class name

To replace the entire CSS file with your own customized CSS class name, you need to copy the uncompressed version (Src->**assets-src** folder) of the required theme file into your application and then modify it as per your needs. Also, make sure that the reference to it has been made in the HTML page and also the Customized class name set to the **cssClass** property of the EJ components. 

The non-minified version of the CSS files are present within the **assets-src** folder, as mentioned earlier in this [section](/js/installation-and-deployment#src). 

To customize the entire CSS file and refer it in your HTML page - Follow the usual steps as specified earlier for CSS reference, additionally copy and paste the uncompressed version of the required CSS file into your application and refer it in the HTML page as depicted below, (For example, we have copied the **ej.theme.css** (uncompressed) file present within the **flat-saffron** theme folder in our application)
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img6.png) 

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

Now, to make particular changes in that file, you can directly open it and start making modifications. For example, The DatePicker control has its default root class name as `e-datepicker`. You can change it manually with the user-specified root class name such as `e-cutomdatepicker` in the CSS file as shown below,
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img7.png)

CSS file with default root e-datepicker name
{:.caption}

![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img8.png)

CSS file with Customized root class name
{:.caption}

To change/customize further the styles of the other child elements of the datepicker widget like header (`e-header` class), current-month and other-month, you need to modify the appropriate CSS properties within the `ej.theme.css` file as shown below,

`e-header` element with newly customized background-color
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img9.png) 

`current-month` element with newly customized background-color
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img10.png) 

`other-month` element with newly customized text color
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img11.png) 

Save the changes made in the CSS file and then set the user-specified custom CSS class name(`e-customdatepicker`) to the `cssClass` property of the datepicker widget as shown below,

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

Run the above code, you can see the datepicker widget with one or more customized child-elements according to the changes done in the CSS files as shown below,
![](/js/Theming-in-Essential-JavaScript-Components_images/Theming-in-Essential-JavaScript-Components_img12.png) 
