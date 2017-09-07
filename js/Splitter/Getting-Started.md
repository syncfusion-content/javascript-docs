---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Splitter
documentation: ug
api: /api/js/ejsplitter
---

# Getting Started

This section explains briefly about how to create a **Splitter** in your application with **JavaScript**.

**Essential JavaScript Splitter** widget consists of movable split bar(s) that divides a container's display area into two or more resizable and collapsible panels. 

From the following guidelines, you can create a **Splitter**, add Tree view in the **Splitter** and set actions to view the image. It is used to split the document or image and Expand or Collapse in the **Splitter**. The following screenshot demonstrates the functionality of **Splitter** widget.

![](/js/Splitter/Getting-Started_images/Getting-Started_img1.png) 

## Create Splitter Control

Create an **HTML** file and add the following template in the **HTML** file.

{% highlight html %}

<!doctype html>

<html>
<head>
    <title>Essential Studio for JavaScript : Rotator Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>

<body>
    <!-- add Splitter element here -->
</body>
</html>

{% endhighlight %}

Add **&lt;input&gt;** element to create **Splitter**. Save the images in the corresponding location.

{% highlight html %}

<div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <!----------------Splitter Control---------------->
            <div id="outerSplitter">
                <div>
                    <div class="cont">
                        <h3 class="h3">JavaScript</h3>
                        <!-- Add the Tree View element here -->
                    </div>
                </div>
                <div>
                    <div class="cont">
                        <div class="_content">
                            Select any product from the tree to show the description.
                        </div>
                        <div class="tools des">
                            <h3>Mobile</h3>
                            <img src="galaxy.jpg" />
                        </div>
                        <div class="chart des">
                            <h3>Hard Disk</h3>
                            <img src="harddisk.jpg" />
                        </div>
                        <div class="grid des">
                            <h3>Logo</h3>
                            <img src="right.jpg" />
                        </div>
                    </div>
                </div>
            </div>
            <!------------------------------------------------->
        </div>
    </div>
</div>

{% endhighlight %}

Add the following styles to show the **Splitter** control in horizontal order.

{% highlight css %}

<style type="text/css" class="cssStyles">
   #outerSplitter {
       margin: 0 auto;
   }
   .cont {
       padding: 20px;
       min-width: 50px;
   }
   .cont #treeView_Container {
       margin-bottom: 0;
       border: none;
   }
   .h3 {
       font-size: 14px;
       margin: 0;
   }
   .des {
       display: none;
   }
</style>

{% endhighlight %}

## Configure Tree View 

Add the following code example in **HTML** file to configure Tree View.

{% highlight html %}

<ul id="treeView" class="visibleHide">
    <li>
        Mobile
        <ul>
            <li id="tools" class="_child">Galaxy</li>
        </ul>
    </li>
    <li>
        Hard Disk
        <ul>
            <li id="chart" class="_child">Seagate </li>
        </ul>
    </li>
    <li>
        Logo
        <ul>
            <li id="grid" class="_child">Amazon</li>
        </ul>
    </li>
</ul>

{% endhighlight %}

## Set Actions

Add the following code example in the view page to set the action to view the image.

{% highlight javascript %}

    $(function () {
        $("#treeView").ejTreeView({ nodeSelect: "treeClicked" });
        $("#outerSplitter").ejSplitter({
            height: 280, width: 501,
            properties: [{ paneSize: 200 }]
        });
    });
    function treeClicked(sender, args) {
        if (sender.currentElement.hasClass('_child')) {
            var content = $('.' + sender.currentElement[0].id).html();
            $('._content').html(content);
        }
    }

{% endhighlight %}

The following screenshot is the output for the above code.

![](/js/Splitter/Getting-Started_images/Getting-Started_img2.png) 

