---
layout: post
title: getting-Started
description: getting started
platform: js
control: AutoComplete
documentation: ug
---

# Getting Started

This section helps to understand the getting started of the AutoComplete widget with the step-by-step instructions.

## Script/CSS reference

Create a new HTML file and include the below code

{% highlight html %}

<!DOCTYPE html>

<html lang="en" xmlns="http://www.w3.org/1999/xhtml">
<head>
    <meta charset="utf-8" />
    <title></title>
</head>
<body>

</body>
</html>


{% endhighlight %}



Add link to the CSS file from the specific [theme](http://helpjs.syncfusion.com/js/theming-in-essential-javascript-components) folder to your HTML file within the head section. Refer the built-in theme which is mentioned [here](http://helpjs.syncfusion.com/js/theming-in-essential-javascript-components). 

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Dialog </title>
    <link href="http://cdn.syncfusion.com/13.2.0.29/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
</head>


{% endhighlight %}



Add links to the [CDN](http://helpjs.syncfusion.com/js/cdn) Script files with dependencies.

{% highlight html %}

<head>
    <meta charset="utf-8" />
    <title>Getting Started - Dialog</title>
    <link href="http://cdn.syncfusion.com/13.2.0.29/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.2.0.29/js/web/ej.web.all.min.js"></script>
</head>


{% endhighlight %}



N> In production, we highly recommend you to use our [custom script generator](http://helpjs.syncfusion.com/js/include-only-the-needed-widgets) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) compression in your server.



## Create an AutoComplete

Add an input element in the &lt;body&gt; tag as below.



{% highlight html %}


<body>
        <input type="text" id="autocomplete" />
</body>


{% endhighlight %}



Initialize the AutoComplete widget by adding the following code in script section

{% highlight js %}


    $('#autocomplete').ejAutocomplete();



{% endhighlight %}



## Databinding

The data for the suggestion list can be populated using the dataSource property. 

{%seealso%}[Data Binding](http://help.syncfusion.com/js/autocomplete/data-binding){%endseealso%}


{% highlight js %}


        /*Local Data Source*/
        carList = [
               "Audi S6", "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
               "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
               "Chevrolet Camaro", "Cadillac ",
               "Duesenberg J ", "Dodge Sprinter",
               "Elantra", "Excavator",
               "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
               "GAZ Siber"];

        $('#autocomplete').ejAutocomplete({ dataSource: carList });


{% endhighlight %}

![Autocomplete-GettingStarted](getting-started_images\getting-started_img1.png)



## Enable Popup Button

This button helps you to show all the available suggestions on clicking it.

{% highlight js %}


   $('#autocomplete').ejAutocomplete({ dataSource: carList, showPopupButton:true });



{% endhighlight %}

![Autocomplete-PopupButton](getting-started_images\getting-started_img2.png)

