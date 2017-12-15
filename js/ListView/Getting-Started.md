---
layout: post
title: Getting-Started
description: getting started
platform: js
control: ListView
documentation: ug
api: /api/js/ejlistview
---

# Getting Started


The **Essential JavaScript ListView** widget builds an interactive list view interface. This control allows you to select an item from a list-like interface and provides the infrastructure to display a set of data items in different layouts or views. Lists display data, data navigation, result lists, and data entry.


![](/js/ListView/Getting-Started_images/Getting-Started_img1.png) 

## Create a simple ListView

The following steps guide you to add a **ListView** control.

Create a **HTML** file and add the following references to the required libraries.



{% highlight html %}


<html>
<head>
<link href="[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
<script src="[http://code.jquery.com/jquery-2.0.0.min.js](http://code.jquery.com/jquery-2.0.0.min.js)"></script>
<script src="[http://borismoore.github.io/jsrender/jsrender.min.js](http://borismoore.github.io/jsrender/jsrender.min.js)"></script>
<script src="[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js)"></script>

</head>
<body>
        <!-- Add Listview control template element here -->

</body>
</html>


{% endhighlight %}



Add a **&lt;div&gt;** element. It is a container for **ListView** control.



{% highlight html %}


    <div id="listview">
        <ul>
            <li data-ej-text="Inbox"></li>
            <li data-ej-text="VIP"></li>
            <li data-ej-text="Drafts"></li>
            <li data-ej-text="Sent"></li>
            <li data-ej-text="Junk"></li>
            <li data-ej-text="All mails"></li>
            <li data-ej-text="Mail"></li>
        </ul>
    </div>



{% endhighlight %}



Create the **ListView** control by adding script as follows.



{% highlight javascript %}


            $(function () {
                $("#listview").ejListView();
            });


{% endhighlight %}



Run the above code to render the following output.

![](/js/ListView/Getting-Started_images/Getting-Started_img2.png) 

**Add Header** 

You can add a header for **ListView** using [showHeader](https://help.syncfusion.com/api/js/ejlistview#members:showheader) property and change the title content using [headerTitle](https://help.syncfusion.com/api/js/ejlistview#members:headertitle) property. Refer to the following script.



{% highlight javascript %}

    $(function () {
        $("#listview").ejListView({ showHeader: true, headerTitle: "Mailbox"});
    });

{% endhighlight %}



Run the above code to render the following output.

![](/js/ListView/Getting-Started_images/Getting-Started_img3.png) 

