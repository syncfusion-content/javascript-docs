---
layout: post
title: Data-Binding
description: data-binding
platform: js
control: TagCloud
documentation: ug
api: /api/js/ejtagcloud
---

# Data-Binding

To render the **TagCloud** widget, it is necessary to bind the data to it in a proper way. The following sub-properties provides you a way to bind local or remote data to the **TagCloud** widget by binding the appropriate data fields to the corresponding options.

## Fields 

### dataSource 

This property assigns the local **JSON** data or remote (URL binding) data to the **TagCloud** control.

### query 

It accepts the data of object type that is usually the query string to fetch the required data from a specific table based on certain conditions. As this property is optional, when it is not specified, then the entire records that are initially assigned through dataSource is taken into consideration.

### text

It maps the corresponding text field name from the data table or **JSON** data that is assigned to the dataSource with the text property of the **TagCloud** control. The text value that is fetched from the table renders the value to be displayed in the **TagCloud**.

### URL

URL field in the data table or **JSON** data assigned the datasource is mapped to the URL property of the **TagCloud** control. The URL property defines the link to be navigated on clicking the corresponding text item.

### frequency

It maps to the frequency field name from the data table or **JSON** data that is assigned to the dataSource. The frequency value that is fetched from the table should be a number to categorize the font size.

## Local Binding

Local data binding allows you to map **JSON** data to **TagCloud**, that the corresponding text, URL, and frequency fields are assigned with a local **JSON** data.

### Defining the Local data for TagCloud

The following steps explains you the local data binding to **TagCloud** widget using [dataSource](https://help.syncfusion.com/api/js/ejtagcloud#members:datasource),

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.

{% highlight html %}

<div id="website"></div>

{% endhighlight %}

{% highlight javascript %}


    // Define local data source elements with text, url and frequency fields.

    var websiteCollection = [
        { text: "Google", url: "http://www.google.com", frequency: 12 },
        { text: "All Things Digital", url: "http://allthingsd.com/", frequency: 3 },
        { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
        { text: "Business Week", url: "http://www.businessweek.com/", frequency: 2 },
        { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
        { text: "Center Networks",url: "http://www.centernetworks.com/", frequency: 5 },
        { text: "Crave", url: "http://news.cnet.com/crave/", frequency: 8 },
        { text: "Crunch Gear", url: "http://techcrunch.com/gadgets/", frequency: 20 },
        { text: "Daily Tech", url: "http://www.dailytech.com/", frequency: 1 },
        { text: "Electronista", url: "http://www.electronista.com/", frequency: 3 },
        { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
        { text: "GearLog", url: "http://www.gearlog.com/", frequency: 9 },
        { text: "Information Week",url:"http://www.informationweek.com/",frequency: 0 },
        { text: "PCWorld", url: "http://www.pcworld.com/", frequency: 11 },
        { text: "Tech Republic", url: "http://techrepublic.com/", frequency: 3 },
        { text: "ValleyWag", url: "http://valleywag.gawker.com/", frequency: 6 },
        { text: "Rediff", url: "http://in.rediff.com/", frequency: 9 },
        { text: "WebProNews", url: "http://www.webpronews.com/", frequency: 2 }
     ];

 
{% endhighlight %}

Map Local datasource to corresponding fields in **TagCloud** control as follows,


{% highlight javascript %}

    $("#website").ejTagCloud({
        dataSource: websiteCollection
    });


{% endhighlight %}



The following screenshot displays the **TagCloud** control with local data binding.

![](/js/TagCloud/Data-Binding_images/Data-Binding_img1.png)



## Remote Binding

**TagCloud** provides remote data binding support to populate **TagCloud** items and the values can be mapped to the **TagCloud** fields from a remote web service by using **DataManager** and **Query**. 

DataManager is used to manage relational data in **JavaScript**. It supports **CRUD** (Create, Read, Update, and Destroy) in individual requests and batch. DataManager use two different classes, ej.DataManager for processing, and ej.Query for serving data. ej.DataManager communicates with data source and ej.Query generates data queries that are read by DataManager.

### Configuring Remote data for TagCloud

The following steps explains you the local data binding to **TagCloud** widget.

In the **HTML** page, add a **&lt;div&gt;** element to configure **TagCloud** widget.



{% highlight html %}

 <div id="website"></div>


{% endhighlight %}



Define DataManager and assign remote data source to it. Initialize query for binding data to **TagCloud** text. Here DataManager renders the remote web service and filters the data by using Query. The **select** property of **ejQuery**, is used to retrieve the specified columns from the data source.



{% highlight javascript %}



    var dataManager = ej.DataManager({
        url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
    });
    // Query creation
    var query = ej.Query().from("Orders").take(10);


{% endhighlight %}



Assign [datasource](https://help.syncfusion.com/api/js/ejtagcloud#members:datasource) and [query](https://help.syncfusion.com/api/js/ejtagcloud#members:query) property values to bind the remote data. Map the corresponding fields to **TagCloud** control using [fields](https://help.syncfusion.com/api/js/ejtagcloud#members:fields) as follows:



{% highlight javascript %}


 
    $("#website").ejTagCloud({
        dataSource: dataManager,
        query: query,
        fields: { text: "CustomerID", frequency: "EmployeeID" }
    });


{% endhighlight %}



The following screenshot displays a **TagCloud** control with remote data binding.



![](/js/TagCloud/Data-Binding_images/Data-Binding_img2.png) 



## KnockoutJS binding

Two types of KnockoutJS binding is supported,

* One-way binding
* Two-way binding

One-way binding refers to the process of applying observable values to all available properties of the **TagCloud** widget, but the changes made in **TagCloud** widget is not reflected and triggered in turn to the observable collection. This kind of binding applies to all properties of the **TagCloud** widget.

Two-way binding supports both the processes – it applies the observable values to the **TagCloud** widget properties as well as the changes made in the **TagCloud** widget is also reflected back and triggered within the observable collections. 

For more information about the KnockoutJS binding, refer the following link location,

<https://help.syncfusion.com/js/knockoutjs>

The following code example depicts you the way to bind data to the **TagCloud** widget using Knockout support,

{% highlight html %}

<!doctype html>
<html>
   <head>
      <title>Essential Studio for JavaScript :  KO Support for Tagcloud</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
   </head>
   <body>
      <div class="content-container-fluid">
         <div class="row">
            <div id="website" data-bind="ejTagCloud: { dataSource: dataList, titleText: title }"></div>
         </div>
      </div>
      <script>
         $(function () { 
         var view = [
         { text: "Google", url: "http://www.google.com", frequency: 12 },
               { text: "a2zwebhelp", url: "http://www.a2zwebhelp.com", frequency: 3 },
               { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
               { text: "BxSlider", url: "http://bxslider.com/examples", frequency: 2 },
               { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
               { text: "Facebook", url: "https://www.facebook.com/", frequency: 5 },
               { text: "Crave", url: "http://news.cnet.com/crave/", frequency: 8 },
               { text: "Wikipedia", url: "http://www.wikipedia.org/", frequency: 20 },
               { text: "Amazon.com", url: "http://www.amazon.com/", frequency: 1 },
               { text: "Electronista", url: "http://www.electronista.com/", frequency: 3 },
               { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
               { text: "LinkedIn", url: "http://www.linkedIn.com/", frequency: 9 },
               { text: "Information Week",url:"http://www.informationweek.com/",frequency:0 },
               { text: "MenuCool", url: "http://www.menucool.com", frequency: 11 },
               { text: "Tech Republic", url: "http://techrepublic.com/", frequency: 3 },
               { text: "ValleyWag", url: "http://valleywag.gawker.com/", frequency: 6 },
               { text: "WOWslider", url: "http://wowslider.com", frequency: 9 },
               { text: "W3schools", url: "http://www.w3schools.com/", frequency: 2 }
           ];	
         	window.viewModel = { 
                       dataList: ko.observableArray(view),
                       title: ko.observable("Popular Sites"),
                   };	        		
                   ko.applyBindings(viewModel);
                });
      </script>
   </body>
</html>


{% endhighlight %}



Execute the above code to render the following output.

![](/js/TagCloud/Data-Binding_images/Data-Binding_img3.png)



## AngularJS binding

**TagCloud** widget is availed with two types of AngularJS support namely, 

* One way binding
* Two way binding 

One-way binding refers to the process of applying scope values to all available properties of the TagCloud widget, but the changes made in **TagCloud** widget is not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **TagCloud** widget.

Two-way binding supports both the processes – it applies the scope values to the **TagCloud** properties as well as the changes made in the **TagCloud** widget is also be reflected back and triggered within the AngularJS scope change function.

Apply the plugin and property assigning to the **TagCloud** widget element through the directive that starts with a letter **“e-“.**

To know more detail about the AngularJS binding, refer the following link location,

<https://help.syncfusion.com/js/angularjs>

The following example depicts you the way to bind data to the **TagCloud** widget using AngularJS support,

{% highlight html %}

<!doctype html>
<html lang="en" ng-app="tagApp">
   <head>
      <title>Essential Studio for JavaScript : AngularJS Support for Tagcloud </title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js">  </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
   </head>
   <body ng-controller="TagCtrl">
      <div id="website" ej-tagcloud e-datasource="dataList" e-title="popular sites" />
      <script>
         var list = [
         { text: "Google", url: "http://www.google.co.in", frequency: 12 },
             { text: "a2zwebhelp", url: "http://www.a2zwebhelp.com", frequency: 3 },
             { text: "Arts Technica", url: "http://arstechnica.com/", frequency: 8 },
             { text: "BxSlider", url: "http://bxslider.com/examples", frequency: 2 },
             { text: "Yahoo", url: "http://in.yahoo.com/", frequency: 12 },
             { text: "Facebook", url: "https://www.facebook.com/", frequency: 5 },
             { text: "BlogSpot", url: "http://www.blogspot.com/", frequency: 8 },
             { text: "Microsoft", url: "http://www.microsoft.com/", frequency: 20 },
             { text: "Amazon.com", url: "http://www.amazon.com/", frequency: 1 },
             { text: "MSN", url: "http://www.msn.com/", frequency: 3 },
             { text: "Engadget", url: "http://www.engadget.com/", frequency: 5 },
             { text: "LinkedIn", url: "http://www.linkedIn.com/", frequency: 9 },
             { text: "Twitter", url: "http://www.Twitter.com/", frequency: 0 },
             { text: "MenuCool", url: "http://www.menucool.com", frequency: 3 },
             { text: "BBC", url: "http://www.bbc.co.uk/", frequency: 11 },
             { text: "ValleyWag", url: "http://valleywag.gawker.com/", frequency: 6 },
             { text: "WOWslider", url: "http://wowslider.com", frequency: 9 },
             { text: "W3schools", url: "http://www.w3schools.com/", frequency: 2 }
         ];
             angular.module('tagApp', ['ejangular'])
             .controller('TagCtrl', function ($scope) {
                 $scope.dataList = list;
             });
      </script>
   </body>
</html>


{% endhighlight %}



The following screenshot illustrates a **TagCloud** control using AngularJS data binding,

![](/js/TagCloud/Data-Binding_images/Data-Binding_img4.png)



