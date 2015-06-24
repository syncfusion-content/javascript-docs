---
layout: post
title: getting-started
description: getting started
platform: js
control: Radial Menu
documentation: ug
---

# Getting Started

## Create your first Radial Menu control in JavaScript

In this section, you can learn how to create a simple **Radial Menu**.      

![](getting-started_images\getting-started_img1.png)

**Create a simple Radial Menu**

The following steps guide you to add a **Radial Menu** control.

Create an **HTML** file and paste the following template for web layout.

{% highlight html %}


<html>
<head>
    <title>Radial Menu</title>
<link href="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
<script src="[http://code.jquery.com/jquery-1.10.2.min.js](http://code.jquery.com/jquery-1.10.2.min.js)"></script>
<script src="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
</head>
<body>
        <!-- Adds Radial Menu control Here -->
        <!-- Adds Radial Menu target content Here -->
</body>
</html>


{% endhighlight %}



Create a **div** element that is a container for **Radial Menu**. You can set the images for each item by giving the image **url** with the **data-ej-imageurl** attribute in the inner list element and text with **data-ej-text** attribute. Refer to the following code example.



{% highlight html %}

<div id="radialmenu">
        <ul>
              <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/copy.png"    
              data-ej-text="Copy">
              </li>
              <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/paste.png"
              data-ej-text="Paste">      
              </li>
              <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/redo.png" 
              data-ej-text="Redo">
              </li>
              <li data-ej-imageurl="http://js.syncfusion.com/ug/web/content/radial/undo.png" 
              data-ej-text="Undo"> 
              </li>      
        </ul>
  </div>


{% endhighlight %}



Refer to the following code example to add target content to the **Radial Menu**.



{% highlight html %}


<div id="radialtarget">  
              <textarea id="textarea">
Syncfusion Essential JavaScript Studio for Mobile contains the following built-in theme support with that you can achieve the native appearance and functionality of iOS7, android and windows platforms in your mobile applications.

1.   iOS7

2.   Android

3.   Windows

4.   Flat

By default, the respective render modes are chosen based on the device where the application runs. You can also force and use a particular theme to a control or the whole application that is discussed in later sections. All of the above widgets are highly customizable and also designed with high performance in mind.
            </textarea>
 </div>

<!--Adds Style for Content-->
    <style type="text/css" class="cssStyles">
        #textarea {
            width: 100%;
            height: 270px;
        }
    </style>



{% endhighlight %}



Initialize **Radial Menu** control with the **div** element and set its target content as follows.



{% highlight html %}


<script type="text/javascript">
  $(function () {
            $('#radialmenu').ejRadialMenu({ targetElementId: "radialtarget" });
        });
 </script>



{% endhighlight %}



You can display the **Radial Menu** by performing desired action on the target content while selecting the text inside the target. Therefore, call the **show** method in the select action of the content. Refer to the following code example and add it to the script section.



{% highlight html %}


<script type="text/javascript">
  $(function () {
        $("#textarea").select(function (e) {
            $('#radialmenu').ejRadialMenu("show");
        });
  });
</script>



{% endhighlight %}



Run the above code and select any text inside the target. The settings icon is displayed. Click that icon to render the following output.



![](getting-started_images\getting-started_img2.png)

