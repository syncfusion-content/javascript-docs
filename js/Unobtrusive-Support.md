---
layout: post
title: Using Syncfusion Essential JS in unobtrusive mode
description: How to use syncfusion essential js widgets in unobtrusive to achieve the clear separation of both HTML content and behavior.
platform: js
control: Introduction
documentation: ug
---

# Unobtrusive

Many uncertainties and difficulties are involved in a usual **JavaScript programming** environment like - some of the browsers may ignore the javascript codes under the scripts section completely or partially due to its complexity and so on. To overcome all such inconveniences, [Unobtrusive JavaScript](http://www.w3.org/wiki/The_principles_of_unobtrusive_JavaScript) support has been introduced in order to make it easier for the users to create all our Syncfusion components with basic level HTML tag-like structure. 

One of the main goal of the unobtrusive support is to achieve the clear separation of both the HTML content and behavior, so as to enhance the page loading time and to make the code updating easier. **Essential JavaScript** have separate integration library to achieve the **Unobtrusive JS** support. To make use of Unobtrusive support with our Essential JavaScript components, it is necessary to refer the **ej.unobtrusive.min.js** file in your application.

The **ej.unobtrusive.min.js** file can be accessed from the following location, which can then be copied and referred in your application.

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common
</td>
</tr>
<tr>
<td>
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common
</td>
</tr>
</table>


There are 3 levels of usage to achieve this Unobtrusive JavaScript in our Syncfusion components, which have the option to either turn on/off. They are listed as follows,

* Data role
* EJ role
* Directives

## Data role

Here, the **HTML5** syntax is used for defining any of the control and its properties, instead of manually converting the HTML elements into Syncfusion widgets through JavaScript. All the components can be initialized with usual HTML mark-up tags, by setting the name of the component to the **data-role** attribute in lowercase. 

The **data-role** type is enabled by default. Therefore, while making use of the data-role in control creation, **data-ej** keyword should be prepended to all the properties that we need to define for a control.

The demonstration of such **data-role** declaration with a simple **DatePicker** control creation is shown below,

Refer the **ej.unobtrusive.min.js** file in your application along with the other script and CSS reference section and add the code for defining the **DatePicker** control with the basic HTML mark-up tags along with its attributes defined with **data-ej** keyword prepended as shown below, 

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/ej.unobtrusive.min.js"></script>
  </head>
  <body> 
    <!--DatePicker Control creation with data-role-->
    <input id="myDatePicker" data-role="ejdatepicker" data-ej-value="05/07/2015" />
  </body>
</html>    

{% endhighlight %}

N>   In the above code, **value** is one of the DatePicker property to set the date value for the control, which is defined here with **data-ej** keyword prepended to it.
N>   The order of the reference to the script files made in the above section should be maintained in the same manner as mentioned above. Before making use of the unobtrusive script in your application, make sure that you have copied the **ej.unobtrusive.min.js** file from its installed location into the **scripts/ej** folder of your application.
N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

The output of the above code will look as the one shown below with the value set to the given date,
![](/js/Unobtrusive-Support_images/Unobtrusive-Support_img1.png) 

## EJ role

EJ role is another way of defining the control and its properties through HTML mark-up tags. Here, the HTML syntax simply varies with the **ej** keyword prepended to the control name. The controls are usually initialized through the HTML elements with the prefix **ej-** added to its name and then all its properties prepended with the **ej-** prefix.

An important thing to be noted while using EJ role is that, you need to add the **data-ejrole** attribute to the body tag and the control’s properties defined with **ej-** prefix added as shown in the below code snippet.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
 <head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/ej.unobtrusive.min.js"></script>
 </head>
 <body data-ejrole> 
    <!--DatePicker Control creation with ej-role-->
    <input id="myDatePicker" type="text" ej-datepicker ej-value= "01/01/2013" />
 </body>
</html>   

{% endhighlight %}

N>   In the above code, **value** is one of the DatePicker property to set the date value for the control, which is defined here with **ej-** keyword prepended to it. 
N>   Also, before proceeding with the property definition, it is necessary to define the control name with the **ej-** prefix, in order to instruct which control is needed to be created. (Here, ej-datepicker is defined first, before defining other properties of it.)

The output of the above code will look as the one shown below with the value set to the given date,
![](/js/Unobtrusive-Support_images/Unobtrusive-Support_img2.png) 

## Directives

This method allows to initialize any of the control by defining the control name as the tag name, instead of using the HTML elements. The other properties of the controls are defined as usual with **ej-** keyword prepended to its name as shown in the below example code.

While making use of directives, you need to add the **data-directive** attribute to the body tag and also the control’s properties defined with **ej-** prefix added as shown in the below code snippet.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/ej.unobtrusive.min.js"></script>
  </head>
  <body data-directive> 
    <!--DatePicker Control creation with data-directive-->
    <datepicker ej-value="01/01/2015" ></datepicker>
  </body>
</html>  

{% endhighlight %}

N>   In the above code, **value** is one of the available DatePicker property to set the value for the control, which is defined here with **ej-** keyword prepended to it. 
N>   Also, you can notice here that the HTML tag name is replaced by the control name to be created.

The output of the above code will look as the one shown below with the value set to the given date,
![](/js/Unobtrusive-Support_images/Unobtrusive-Support_img3.png) 

The unobtrusive support can be easily achieved with the above specified 3 types of control initialization methods and all the options (properties) available within the Syncfusion controls can be easily assigned with its required values in an unobtrusive way. Thus, the control creation can be entirely coded in plain HTML with this unobtrusive support, by maintaining the scripts and CSS references separately.

