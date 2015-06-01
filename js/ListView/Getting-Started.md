---
layout: post
title: Getting-Started
description: getting started
platform: js
control: ListView
documentation: ug
---

# Getting Started

This section explains briefly on how to create a **ListView** control in your application.

## Create your first ListView in JavaScript

The **Essential JavaScript ListView** widget builds an interactive list view interface. This control allows you to select an item from a list-like interface and provides the infrastructure to display a set of data items in different layouts or views. Lists display data, data navigation, result lists, and data entry.    __



{% include image.html url="/js/ListView/Getting-Started_images/Getting-Started_img1.png" Caption="List view Control "%}

**Create a simple ListView**

The following steps guide you to add a **ListView** control.

1. Create an **HTML** file and add the following references to the required libraries.



{% highlight javascript %}


<html>
<head>
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
<scriptsrc="[http://code.jquery.com/jquery-2.0.0.min.js](http://code.jquery.com/jquery-2.0.0.min.js)"></script>
<scriptsrc="[http://borismoore.github.io/jsrender/jsrender.min.js](http://borismoore.github.io/jsrender/jsrender.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>

</head>
<body>
        <!—Add Listview control template element here-->

</body>
</html>


{% endhighlight %}



2. Add a **&lt;div&gt;** element. It is a container for **ListView** control.



{% highlight javascript %}


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



3. Create the **ListView** control as follows.



{% highlight javascript %}

<head>
<!-- ... -->
<script type="text/javascript">
$(function () {
            $("#listview").ejListView();
          });
</script>
</head>


{% endhighlight %}



Run the above code to render the following output.

{% include image.html url="/js/ListView/Getting-Started_images/Getting-Started_img2.png" Caption="List view without header"%}

**Add Header** 

You can add a header for **ListView**. Refer to the following code example.



{% highlight javascript %}

<script type="text/javascript">

$(function () {
            $("#listview").ejListView({ **showHeader: true, headerTitle: "Mailbox"**});
});
</script>



{% endhighlight %}



Run the above code to render the following output.

{% include image.html url="/js/ListView/Getting-Started_images/Getting-Started_img3.png" Caption="List view Control with header"%}

