---
layout: post
title: getting-started
description: getting started
platform: js
control: Navigation Drawer
documentation: ug
api: /api/js/ejnavigationdrawer
---

# Getting Started

In this section, you can learn how to create a simple navigation drawer.                       

![](getting-started_images\getting-started_img1.png)

## Create Navigation Drawer Widget

The following steps guide you in adding a **Navigation Drawer** control for a web application that displays a list of items such as home, profile, photos and location where you can navigate to desired page by clicking on the option available in the drawer. 

Create an **HTML** file and paste the following template for web layout.       

{% highlight html %}

<html>
<head>
<title>Navigation Drawer</title>
<link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
<script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>
<script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js" type="text/javascript"></script>
<script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
</head>
<body>
        <!-- Add Navigation Drawer control Here -->
        <!-- Add Page Content content Here -->
</body>
</html>

{% endhighlight %}



Create a **div** element that acts as a container for **Navigation Drawer**. Refer to the following code example.

{% highlight html %}

    <div id="navigationPane">
        <ul>
            <li data-ej-text="Home"></li>
            <li data-ej-text="Profile"></li>
            <li data-ej-text="Photos"></li>
            <li data-ej-text="Location"></li>
        </ul>
    </div>

{% endhighlight %}



Create the target element as follows to display the drawer by clicking target icon.

{% highlight html %}

    <div class="navi">
        <div id="target" class="icon-target"> Drawer</div>
    </div>

{% endhighlight %}



To set the target icon image from sprite and to position the target icon properly use the following styles.

{% highlight css %}

    <style>
        [class*="icon-"] {
            background-image: url("http://js.syncfusion.com/ug/web/content/drawer/sprite.png");
        }

        .icon-target {
            background-position: 0 -338px;
            font-size: 34px;
            height: 48px;
            position: absolute;
            text-indent: 50px;
            top: -3px;
            width: 48px;
            z-index: 3;
        }

        .navi {
            background: none repeat scroll 0 0 #C4C4B4;
            color: #fff;
            height: 45px;
            padding-left: 5px;
            width: 100%;
        }

        body {
            background: none repeat scroll 0 0 #ece9d8;
        }
    </style>

{% endhighlight %}


Create the navigation drawer control as follows. You can display the navigation items as a list (or it can be any template) by using the ListView control. This is achieved by setting the [enableListView](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:enablelistview) property to true. Also you can open the drawer by clicking on target element by setting the [targetId](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:targetid) property. 

Add the following code in the **script** tag.

{% highlight javascript %}

    $(function () {
        $("#navigationPane").ejNavigationDrawer({ enableListView: true, targetId: "target" });
    });
    
{% endhighlight %}


You can display the drawer either by clicking on the target icon or by swiping from left on the page. Refer to the following screenshot.


![](getting-started_images\getting-started_img2.png)

You can set the images for Navigation Drawer by using the **data-ej-imageClass** attribute in the inner list elements.

{% highlight html %}

    <div id="navigationPane">
        <ul>
            <li data-ej-imageclass="e-icon e-home" data-ej-text="Home"></li>
            <li data-ej-imageclass="e-icon e-profile" data-ej-text="Profile"></li>
            <li data-ej-imageclass="e-icon e-photo" data-ej-text="Photos"></li>
            <li data-ej-imageclass="e-icon e-location" data-ej-text="Location"></li>
        </ul>
    </div>
    
{% endhighlight %}



You can define the image classes specified for the list items as follows.

{% highlight css %}

    <style>
    @font-face { 
        font-family: 'ej-font'; 
        src: url('../../common-images/tools/icons.eot'); 
        src: url('../../common-images/tools/icons.eot') format('embedded-opentype'), url('../../common-images/tools/icons.woff') format('woff'),url('../../common-images/tools/icons.woff') format('woff'), url('../../common-images/tools/icons.ttf') format('truetype'), url('../../common-images/tools/icons.svg') format('svg'); 
        font-weight: normal; 
        font-style: normal; 
    } 
 
    .e-home:before { 
        font-family: "ej-font"; 
        content: "\e900"; 
    } 
 
    .e-profile:before { 
        font-family: "ej-font"; 
        content: "\e901"; 
    } 
 
    .e-photo:before { 
        font-family: "ej-font"; 
        content: "\e903"; 
    } 
 
    .e-location:before { 
        font-family: "ej-font"; 
        content: "\e905"; 
    } 

    .e-people:before { 
        font-family: "ej-font"; 
        content: "\e902"; 
    } 
 
    .e-communities:before { 
        font-family: "ej-font"; 
        content: "\e904"; 
    }

    .e-home, .e-profile, .e-people, .e-photo, .e-communities, .e-location { 
        font-size: 24px; 
        color: black; 
    } 
    </style>

{% endhighlight %}



Run the above code to render the following output.

![](getting-started_images\getting-started_img3.png)

You can add desired page content while selecting the options in navigation drawer as follows.



{% highlight html %}

    <!-- Home Page Content-->
    <div id="Home">
        The Home screen allows you to choose the specific content type displayed.
    </div>
    <!-- Profile Page Content-->
    <div id="Profile" style="display: none">
        The Profile page content is displayed.
    </div>
    <!-- Photos Page Content-->
    <div id="Photos" style="display: none">
        The Photos page content is displayed.
    </div>
    <!-- Location Page Content-->
    <div id="Location" style="display: none">
        The Location page content is displayed.
    </div>

{% endhighlight %}



You can load the appropriate content for the navigation items by updating the content through mouseDown handler of ListView. You can define the handler and pass the method name with [mouseDown](https://help.syncfusion.com/api/js/ejlistview#events:mousedown) attribute through [listViewSettings](https://help.syncfusion.com/api/js/ejnavigationdrawer#members:listviewsettings). Also to view which item’s content is being loaded in the page, make the list selection to persist in the drawer by setting [persistSelection](https://help.syncfusion.com/api/js/ejlistview#members:persistselection) as true. Refer to the following code example.

Add the following code in the **script** tag.

{% highlight javascript %}

      $(function () {
           $("#navigationPane").ejNavigationDrawer({ enableListView: true, targetId: "target", listViewSettings: { mouseDown: 'slideMenuClick', persistSelection: true } });
      });

{% endhighlight %}


In the mouse down handler, you can hide the other content and display the respective selected item’s content.


{% highlight javascript %}

    function slideMenuClick(e) {
            $('#Home, #Profile, #Photos, #Location').hide(); //Hiding all other contents
            $('#' + e.text).show(); //Displaying the content based on the text of item selected
            $("#navigationPane").ejNavigationDrawer("close");
        }

{% endhighlight %}

Run the above code to render the following output. 

![](getting-started_images\getting-started_img4.png)

