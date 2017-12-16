---
layout: post
title: Getting Started with AutoComplete widget for Essential JS
description: How to create Autocomplete widget with the step-by-step instructions.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
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



Add link to the CSS file from the specific [theme](https://help.syncfusion.com/js/theming-in-essential-javascript-components) folder to your HTML file within the head section. Refer the built-in theme which is mentioned [here](https://help.syncfusion.com/js/theming-in-essential-javascript-components). 

{% highlight html %}
        
        <head>
            <meta charset="utf-8" />
            <title>Getting Started - Dialog </title>
            <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
        </head>


{% endhighlight %}



Add links to the [CDN](https://help.syncfusion.com/js/cdn) Script files with dependencies.

{% highlight html %}

        <head>
            <meta charset="utf-8" />
            <title>Getting Started - Dialog</title>
            <link href="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
            <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
            <script src="http://cdn.syncfusion.com/{{site.releaseversion}}/js/web/ej.web.all.min.js"></script>
        </head>


{% endhighlight %}



N> In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/include-only-the-needed-widgets) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en) compression in your server.



## Create an AutoComplete

Add an input element in the HTML file for rendering Autocomplete widget 



{% highlight html %}

        
        <body>
                <input type="text" id="autocomplete" />
        </body>


{% endhighlight %}



Initialize the AutoComplete widget by adding the following code in script section

{% highlight javascript %}


    $('#autocomplete').ejAutocomplete();



{% endhighlight %}



## Data binding

The data for the suggestion list can be populated using the [dataSource](https://help.syncfusion.com/api/js/ejautocomplete#members:datasource) property. 

{%seealso%}[Data Binding](https://help.syncfusion.com/js/autocomplete/data-binding){%endseealso%}


{% highlight javascript %}


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

The [showPopupButton](https://help.syncfusion.com/api/js/ejautocomplete#members:showpopupbutton) property helps you to show all the available suggestions on clicking it instead of the search text.

{% highlight javascript %}

        
        $('#autocomplete').ejAutocomplete({ dataSource: carList, showPopupButton:true });
        


{% endhighlight %}

![Autocomplete-PopupButton](getting-started_images\getting-started_img2.png)

