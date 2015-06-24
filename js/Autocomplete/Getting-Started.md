---
layout: post
title: Getting-Started
description: getting started
platform: js
control: AutoComplete
documentation: ug
---

# Getting Started

This section explains briefly about how to create an AutoComplete in your application with JavaScript and helps you to configure the AutoComplete control in your application and also helps you to learn on how to pass the required data to it and to customize its various options according to your requirements. 

The following screenshot illustrates the AutoComplete control that searches the list of components available in the database. 

{% include image.html url="/js/Autocomplete/Getting-Started_images/Getting-Started_img1.png"%}

## Create an AutoComplete

 Create an HTML file and add the following references.

{% highlight html %}

<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0"  charset="utf-8"/>
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!-- Add autocomplete element here -->
   </body>
</html>

{% endhighlight %}



 Add a **&lt;input&gt;** element that acts as a container for AutoComplete widget.

{% highlight html %}

<div>Search customers</div>
<div class="control">
   <input type="text" id="customerList" />
</div>

{% endhighlight %}



 Create the AutoComplete control as follows.

{% highlight js %}

    //Simple Autocomplete creation
    $(function () {
        $("#customerList").ejAutocomplete();
    });

{% endhighlight %}



 Execute the above code to create the AutoComplete textbox as shown in the following screen shot.

{% include image.html url="/js/Autocomplete/Getting-Started_images/Getting-Started_img2.png"%}

## Populate Data to AutoComplete

The data provided to the AutoComplete can customize the list of data either locally or remotely.  

### Remote Data Binding

You can assign the required data from the remote URL as a variable **DataManager** using DataManager, to the **DataSource** property. You can generate a query to get the required data from the remote file using **Query()**, then assign it to the query property of AutoComplete as shown in the following code example.

{% highlight js %}
  
            var dataManger = ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // Query creation
            var query = ej.Query().from("Suppliers").select("SupplierID", "ContactName");

{% endhighlight %}

You can assign the **DataSource** property with the required values to bind the variable names in the **JSON** Data to the corresponding fields of AutoComplete as shown in the following code example. 

{% highlight js %}

    $('#customerList').ejAutocomplete({
        dataSource: dataManger,
        query: query,
        fields: { text: "ContactName", key: "SupplierID" },
        filterType: ej.filterType.StartsWith,
        width: 500
    });

{% endhighlight %}



You can also set some common customization changes to the **AutoComplete** textbox like enabling multiple-selection, highlight search and add dropdown icon in order to get the desired result. 

## Configure Visual Mode with filter option



By default, the AutoComplete is rendered with single value selection that can be set to multiple value selection using the property **multiSelectMode** as **visualMode** allowing you to select multiple Data. You can set the filterType option as startswith to sort the suggestion list based on the starting character.

{% highlight js %}

    $('#customerList').ejAutocomplete({
        dataSource: dataManger,
        query: query,
        fields: { text: "ContactName", key: "SupplierID" },
        filterType: ej.filterType.StartsWith,
        width: 500,
        multiSelectMode:ej.MultiSelectMode.VisualMode
    });

{% endhighlight %}



{% include image.html url="/js/Autocomplete/Getting-Started_images/Getting-Started_img3.png"%}

## Configure Highlight Search and Rounded corners

{% highlight js %}

        $('#customerList').ejAutocomplete({
            dataSource: dataManger,
            query: query,
            fields: { text: "ContactName", key: "SupplierID" },
            filterType: ej.filterType.StartsWith,
            width: 500,
            highlightSearch: true,
            showRoundedCorner: true,
        });

{% endhighlight %}



When you set the **highlightSearch** property to **“True”**, the characters typed in textbox gets highlighted in the suggestion list. To display textbox reforms from sharp ends to rounded ends, you can enable the **showRoundedCorner** property.

{% include image.html url="/js/Autocomplete/Getting-Started_images/Getting-Started_img4.png"%}

## Configure DropDown button

To enable the **Popup** button, you can set **showPopupButton** property to **“True”** that displays the **DropDown** icon at the end of text box. By default, search icon replaces other icons and so you need to override the **CSS** classes as follows. The source image is taken from the installation location.

**[Installed Drive]**:\Users\[user name]\AppData\Local\Syncfusion\EssentialStudio\{{ site.releaseversion }}\JS \Samples\ web\themes\images\icon-down.png 

Copy the “**icon-down.png**” from the above mentioned location and paste it in the folder location of your **HTML** sample page.

Now you can override the search icon class and replace the content to **DropDown** arrow icon and position the icon in the dropdown button.

{% highlight css %}

<style>
    .e-icon.e-search:before {
        content: url("common-images/icon-down.png") !important;
        margin: -3px 0 0 0 !important;
    }
</style>

{% endhighlight %}


{% highlight js %}

    $('#customerList').ejAutocomplete({
        dataSource: dataManger,
        query: query,
        fields: { text: "ContactName", key: "SupplierID" },
        filterType: ej.filterType.StartsWith,
        width: 200,
        highlightSearch: true,
        showRoundedCorner: true,
        multiSelectMode: ej.MultiSelectMode.VisualMode
    });

{% endhighlight %}



{% include image.html url="/js/Autocomplete/Getting-Started_images/Getting-Started_img6.png"%}

