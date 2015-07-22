---
layout: post
title: Getting-Started
description: getting started 
platform: js
control: Menu
documentation: ug
---

# Getting Started 

This section explains briefly about how to create a **Menu** control in your application with **JavaScript**. The **Essential JavaScript** **Menu** supports displaying a **Menu** of list-out items. This **Menu** is based on ul-li hierarchy, where the sub-list items are rendered as the sub-menu items. The **Menu** control can also be rendered with local and remote data source.  From the following guidelines, you can learn how to customize the **Menu** control for a website. In this case, **Syncfusion’s** website **Menu** is discussed. The following screenshot displays the appearance of **Menu**.


{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img1.png" %}

## Create a Menu

**Essential JavaScript** **Menu** widgets are basically provided with built-in features like keyboard navigation, show and hide **Menu** items with animations, and flexible API’s. From the following guidelines, you can learn how to render **Menu** control with Remote data source value.

Create an **HTML** file and add the following template into it for **Menu** creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-2.1.4.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add menu element here -->
</body>
</html>



{% endhighlight %}


Adding **Ul** element for **Menu** rendering.


{% highlight html %}


<ul id="syncfusionProducts"></ul>



{% endhighlight %}



Initialize the **Menu** control in &lt;script&gt; tag. 

{% highlight js %}

        $(function () {
            // document ready
            // simple Menu control creation
            $("#syncfusionProducts").ejMenu();
        });
        

{% endhighlight %}



Output of the above steps.

{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img2.png" %}

## Configure parent Menu items

Every **Menu** has a list of **Menu** items with list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the root level elements of **Menu** control with Local data source value.  Initialize the **Menu** with data source value as illustrated in the following code example. 

{% highlight js %}


        var data = [
            { id: 1, text: "Products", parentId: null },
            { id: 2, text: "Support", parentId: null },
            { id: 3, text: "Purchase", parentId: null },
            { id: 4, text: "Downloads", parentId: null },
            { id: 5, text: "Resources", parentId: null },
			 { id: 6, text: "Company", parentId: null },
            //first level child
            { id: 11, parentId: 1, text: "ASP.NET" },
            { id: 12, parentId: 1, text: "ASP.NET MVC" },
            { id: 13, parentId: 1, text: "Mobile MVC" },
            { id: 14, parentId: 1, text: "Silverlight" },
            { id: 15, parentId: 1, text: "Windows Forms" },
            { id: 16, parentId: 1, text: "Windows Phone" },
            { id: 17, parentId: 1, text: "WinRT (XMAL)" },
            { id: 18, parentId: 1, text: "WPF" },
            { id: 19, parentId: 1, text: "Orubase Studio" },
            { id: 20, parentId: 1, text: "Metro Studio" },
            { id: 21, parentId: 1, text: "What's New" },
            { id: 22, parentId: 2, text: "Direct-Trac Support" },
            { id: 23, parentId: 2, text: "Community Forums" },
            { id: 24, parentId: 2, text: "Knowledge Base" },
            { id: 25, parentId: 2, text: "Online Documentation" },
            { id: 26, parentId: 2, text: "Services" },
			{ id: 27, parentId: 4, text: "Evaluation" },
			{ id: 28, parentId: 4, text: "Free E-Books" },
			{ id: 29, parentId: 4, text: "Metro Studio" },
			{ id: 30, parentId: 4, text: "Latest Version" },
			{ id: 31, parentId: 4, text: "Version History" },
			{ id: 32, parentId: 5, text: "Technology Resource Portal " },
			{ id: 33, parentId: 5, text: "Case Studies" },
			{ id: 34, parentId: 5, text: "Bouchers & Datasheets" },
			{ id: 35, parentId: 5, text: "FAQ" },
            //second level child
            {id: 111, parentId: 21, text: "WinRT (XMAL)" },
            { id: 112, parentId: 21, text: "WPF" },
            { id: 113, parentId: 21, text: "Silverlight" },
            { id: 114, parentId: 21, text: "Windows Forms" },
            { id: 115, parentId: 21, text: "Windows Phone" }
            
        ];
        jQuery(function ($) {
            $("#syncfusionProducts").ejMenu({
                fields: { dataSource: data, id: "id", parentId: "parentId", text: "text" }
            });
        });


{% endhighlight %}



The following screenshot displays output.

{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img3.png" %}

## Initialize sub-level Menu items

Every **Menu** items have a list of sub level **Menu** items. From the following guidelines, you can learn how to initialize the sub level items of **Menu** control. The **parentId** field is used to map root level **Menu** item to its sub level **Menu** item.								

The following code example describes how to initialize first level sub menu items of product **Menu** item.

{% highlight js %}


       var data = [
            { id: 1, text: "Products", parentId: null },
            { id: 2, text: "Support", parentId: null },
            { id: 3, text: "Purchase", parentId: null },
            { id: 4, text: "Downloads", parentId: null },
            { id: 5, text: "Resources", parentId: null },
			 { id: 6, text: "Company", parentId: null },
            //first level child
            { id: 11, parentId: 1, text: "ASP.NET" },
            { id: 12, parentId: 1, text: "ASP.NET MVC" },
            { id: 13, parentId: 1, text: "Mobile MVC" },
            { id: 14, parentId: 1, text: "Silverlight" },
            { id: 15, parentId: 1, text: "Windows Forms" },
            { id: 16, parentId: 1, text: "Windows Phone" },
            { id: 17, parentId: 1, text: "WinRT (XMAL)" },
            { id: 18, parentId: 1, text: "WPF" },
            { id: 19, parentId: 1, text: "Orubase Studio" },
            { id: 20, parentId: 1, text: "Metro Studio" },
            { id: 21, parentId: 1, text: "What's New" },
            { id: 22, parentId: 2, text: "Direct-Trac Support" },
            { id: 23, parentId: 2, text: "Community Forums" },
            { id: 24, parentId: 2, text: "Knowledge Base" },
            { id: 25, parentId: 2, text: "Online Documentation" },
            { id: 26, parentId: 2, text: "Services" },
			{ id: 27, parentId: 4, text: "Evaluation" },
			{ id: 28, parentId: 4, text: "Free E-Books" },
			{ id: 29, parentId: 4, text: "Metro Studio" },
			{ id: 30, parentId: 4, text: "Latest Version" },
			{ id: 31, parentId: 4, text: "Version History" },
			{ id: 32, parentId: 5, text: "Technology Resource Portal " },
			{ id: 33, parentId: 5, text: "Case Studies" },
			{ id: 34, parentId: 5, text: "Bouchers & Datasheets" },
			{ id: 35, parentId: 5, text: "FAQ" },
            //second level child
            {id: 111, parentId: 21, text: "WinRT (XMAL)" },
            { id: 112, parentId: 21, text: "WPF" },
            { id: 113, parentId: 21, text: "Silverlight" },
            { id: 114, parentId: 21, text: "Windows Forms" },
            { id: 115, parentId: 21, text: "Windows Phone" }
            
        ];
        jQuery(function ($) {
            $("#syncfusionProducts").ejMenu({
                fields: { dataSource: data, id: "id", parentId: "parentId", text: "text" }
            });
        });


{% endhighlight %}



Execute the above code example to render the following output.



{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img4.png" %}

## Define multiple level Menu items

You can define the sub-menu items to multiple levels in **Menu** control. You need to specify the parent Id value to render sub level **Menu** item for the **Menu** items.

To initialize multiple levels sub menu items, use the following code example.


{% highlight js %}


        var data = [
            { id: 1, text: "Products", parentId: null },
            { id: 2, text: "Support", parentId: null },
            { id: 3, text: "Purchase", parentId: null },
            { id: 4, text: "Downloads", parentId: null },
            { id: 5, text: "Resources", parentId: null },
			 { id: 6, text: "Company", parentId: null },
            //first level child
            { id: 11, parentId: 1, text: "ASP.NET" },
            { id: 12, parentId: 1, text: "ASP.NET MVC" },
            { id: 13, parentId: 1, text: "Mobile MVC" },
            { id: 14, parentId: 1, text: "Silverlight" },
            { id: 15, parentId: 1, text: "Windows Forms" },
            { id: 16, parentId: 1, text: "Windows Phone" },
            { id: 17, parentId: 1, text: "WinRT (XMAL)" },
            { id: 18, parentId: 1, text: "WPF" },
            { id: 19, parentId: 1, text: "Orubase Studio" },
            { id: 20, parentId: 1, text: "Metro Studio" },
            { id: 21, parentId: 1, text: "What's New" },
            { id: 22, parentId: 2, text: "Direct-Trac Support" },
            { id: 23, parentId: 2, text: "Community Forums" },
            { id: 24, parentId: 2, text: "Knowledge Base" },
            { id: 25, parentId: 2, text: "Online Documentation" },
            { id: 26, parentId: 2, text: "Services" },
			{ id: 27, parentId: 4, text: "Evaluation" },
			{ id: 28, parentId: 4, text: "Free E-Books" },
			{ id: 29, parentId: 4, text: "Metro Studio" },
			{ id: 30, parentId: 4, text: "Latest Version" },
			{ id: 31, parentId: 4, text: "Version History" },
			{ id: 32, parentId: 5, text: "Technology Resource Portal " },
			{ id: 33, parentId: 5, text: "Case Studies" },
			{ id: 34, parentId: 5, text: "Bouchers & Datasheets" },
			{ id: 35, parentId: 5, text: "FAQ" },
            //second level child
            {id: 111, parentId: 21, text: "WinRT (XMAL)" },
            { id: 112, parentId: 21, text: "WPF" },
            { id: 113, parentId: 21, text: "Silverlight" },
            { id: 114, parentId: 21, text: "Windows Forms" },
            { id: 115, parentId: 21, text: "Windows Phone" }
            
        ];
        jQuery(function ($) {
            $("#syncfusionProducts").ejMenu({
                fields: { dataSource: data, id: "id", parentId: "parentId", text: "text" }
            });
        });


{% endhighlight %}



The following screenshot is the output.



{% include image.html url="/js/Menu/Getting-Started_images/Getting-Started_img5.png" %}

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items through online data source. You can simply customize the **Menu** widget in an efficient manner.

In summary of this getting started, you have now simulated the **Syncfusion’s** website **Menu** with **Essential JavaScript Menu**. You have utilized and learnt the appearance customization etc.  

By following the above mentioned steps, you can render the **Menu** control with multiple level sub items. You can simply customize the **Menu** in an efficient manner.

