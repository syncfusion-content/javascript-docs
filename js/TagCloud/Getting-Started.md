---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TagCloud
documentation: ug
api: /api/js/ejtagcloud
---

# Getting Started

This section explains briefly about how to create a **TagCloud** in your application with **JavaScript**. The **TagCloud** can be easily configured to the div element in which the tags are placed. The following screenshot illustrates the functionality of a **TagCloud** widget with a list of the topmost search engines. 


![](/js/TagCloud/Getting-Started_images/Getting-Started_img1.png)

## Create TagCloud widget

 Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
   <head>
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <!--Add necessary HTML elements-->
      <!--Apply Scripts-->
   </body>
</html>


{% endhighlight %}



Add necessary **HTML** elements.



{% highlight html %}


 <div id="tagcloud"></div>


{% endhighlight %}



Add the following code example before **&lt;/body&gt;** tag to add list of items to the **TagCloud** and initialize the **TagCloud** widget using [dataSource](https://help.syncfusion.com/api/js/ejtagcloud#members:datasource) and [titleText](https://help.syncfusion.com/api/js/ejtagcloud#members:titletext) properties.



{% highlight javascript %}

    $("document").ready(function (event) {
         var websiteCollection = [
             { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
             { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
             { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
             { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
             { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
             { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
             { text: "InfoSpace", url: "http://infospace.com/", frequency: 8 },
             { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
             { text: "DogPile", url: "http://www.dogpile.com/", frequency: 4 },
    
             { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
             { text: "Info", url: "http://www.info.com/", frequency: 6 },
             { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
             { text: "ContenKo", url: "http://www.contenko.com/", frequency: 3 },
             { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
        ];
        $("#tagcloud").ejTagCloud({
            dataSource: websiteCollection,
            titleText: "Tech Sites"
        });
    });



{% endhighlight %}



The following screenshot displays the output of the above code example.



![](/js/TagCloud/Getting-Started_images/Getting-Started_img2.png) 

## Set Min and Max Font Size

In the above code example, the **frequency** properties are used to set the min and max font size to the **TagCloud** list item.

{% highlight javascript %}
   
    $("document").ready(function (event) {
         var websiteCollection = [
             { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
             { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
             { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
             { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
             { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
             { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
             { text: "InfoSpace", url: "http://infospace.com/", frequency: 8 },
             { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
             { text: "DogPile", url: "http://www.dogpile.com/", frequency: 4 },
    
             { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
             { text: "Info", url: "http://www.info.com/", frequency: 6 },
             { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
             { text: "ContenKo", url: "http://www.contenko.com/", frequency: 3 },
             { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
        ];
        $("#tagcloud").ejTagCloud({         
            dataSource: websiteCollection,
            titleText: "Tech Sites"
        });
    });
   


{% endhighlight %}



In the above code, the min font size is 3 and max font size is 24.

## Set event to perform an operation

Here, you can set the **TagCloud** events such as [create](https://help.syncfusion.com/api/js/ejtagcloud#events:create), [mouseover](https://help.syncfusion.com/api/js/ejtagcloud#events:mouseover), [mouseout](https://help.syncfusion.com/api/js/ejtagcloud#events:mouseout), [click](https://help.syncfusion.com/api/js/ejtagcloud#events:click).



{% highlight javascript %}

    $("document").ready(function (event) {
              var websiteCollection = [
                 { text: "Yahoo!", url: "http://search.yahoo.com/", frequency: 20 },
                 { text: "DuckDuckGo", url: "https://duckduckgo.com/", frequency: 5 },
                 { text: "Bing", url: "http://www.bing.com/", frequency: 23 },
                 { text: "Blekko", url: "http://blekko.com/", frequency: 4 },  
                 { text: "Alhea", url: "http://www.alhea.com/", frequency: 3 },
                 { text: "MyWebSearch", url: "http://home.mywebsearch.com/index.jhtml", frequency: 10 },
                 { text: "InfoSpace", url: "http://infospace.com/", frequency: 8 },
                 { text: "Google", url: "https://www.google.co.in/", frequency: 24 },
                 { text: "DogPile", url: "http://www.dogpile.com/", frequency: 4 },
        
                 { text: "Wow", url: "http://www.wow.com/", frequency: 14 },
                 { text: "Info", url: "http://www.info.com/", frequency: 6 },
                 { text: "WebCrawler", url: "http://www.webcrawler.com/", frequency: 12 },
                 { text: "ContenKo", url: "http://www.contenko.com/", frequency: 3 },
                 { text: "Aol Search", url: "http://search.aol.com", frequency: 16 },
            ];
            $("#tagcloud").ejTagCloud({
                dataSource: websiteCollection,
                titleText: "Tech Sites",
                create: "create",
                mouseover: "mouseover",
                mouseout: "mouseout",
                click: "click",
                width: "auto"
            });
    });
    function create(args) {
        alert();
    }
    function mouseover(args) {
        alert();
    }
    function mouseout(args) {
        alert();
    }
    function click(args) {
        alert();
    }



{% endhighlight %}



In the above code example, the **alert()** function is used  to show the events that happened.

