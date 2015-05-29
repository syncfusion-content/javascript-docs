---
layout: post
title: getting-started
description: getting started
platform: js
control: Rotator
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Rotator** in your application with **JavaScript,****ASP.NET MVC** and **ASP.NET**.

## Create your first Rotator  in JavaScript

**Essential****JavaScript****Image Rotator** comes with a visual that has a spectacular zoom in and fade out effect. A single line of code invokes the **JavaScript****Rotator** effect. Using the following guidelines you can create **Rotator** widget for a real-time website banner. It has five images that slide automatically. When you click the center button, image slides in a rotating manner and on second click the rotation stops.

The following screenshot demonstrates the functionality of **Rotator** widget.



{% include image.html url="\js\Rotator\getting-started_images\getting-started_img1.png" Caption="Figure 1: Rotator"%}

### Create Rotator Widget

A **Rotator** widget can be made by the following steps.

* Create an **HTML** file and add the following template in the **HTML** file.



{% highlight html %}


<!doctype html>

<html>
<head>
    <title>Essential Studio for JavaScript : Rotator Default Functionalities</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
          <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- Add Rotator element here. -->
</body>
</html>


{% endhighlight %}



### Configure Images

The following guidelines help you to configure images.

* Copy the following codes in the **HTML** file. 

* Ensure you have saved images in the **Rotator/imi** folder.



{% highlight html %}

<div class="content-container-fluid">
<div class="row">
<div class="cols-sample-area">
<div class="frame">
<ul id="sliderContent">
   <li><img class="image" src="../imi/Untitled.png"/></li>
   <li><img class="image" src="../imi/Untitled1.png"/></li>
   <li><img class="image" src="../imi/Untitled2.png"/></li>
   <li><img class="image" src="../imi/Untitled3.png"/></li>
   <li><img class="image" src="../imi/Untitled4.png"/></li>
</ul>
</div>
</div>
</div>
</div>



{% endhighlight %}

### Configure Styles

Add the following style in the **HTML** file.


{% highlight css %}

<style type="text/css" class="cssStyles">
  .frame 
    {
        width: 600px;
    }

    #sliderContent > li .image 
    {
        width: 600px;
        height: 350px;
    }
</style>


{% endhighlight %}

### Set Actions

Add the following script in the **HTML** file.



{% highlight js %}


<script type="text/javascript">

    $(function () {

        // declaration


        $("#sliderContent").ejRotator({

            slideWidth: "600px",

            frameSpace: "0px",

            displayItemsCount: "1",

            slideHeight: "350px",

            navigateSteps: "1",

            enableResize: true,

            pagerPosition: ej.Rotator.PagerPosition.Outside,

            orientation: ej.Orientation.Horizontal,

            showPager: true,

            enabled: true,

            showCaption: true,

            allowKeyboardNavigation: true,

            showPlayButton: true,

            enableRTL: true,

            animationType: "slide"
        });
    });
</script>



{% endhighlight %}



The above code gives the output displayed in following screenshot.





{% include image.html url="\js\Rotator\getting-started_images\getting-started_img2.png" Caption="Figure 2: Rotator"%}

## Create your first Rotator in MVC

**ASP.NET MVC Rotator** provides support to display the provided number of images within your webpage in a rotating manner. Refer the following guidelines to create a **Rotator** widget for a real-time website banner scenario that has five images that slide automatically. When you click the center button, images slide in a rotating manner and on second click, the rotation stops.

The following screenshot illustrates a **Rotator** widget.





{% include image.html url="\js\Rotator\getting-started_images\getting-started_img3.png" Caption="Figure 3: Rotator"%}

**Create a Rotator**

**Essential Studio ASP.NET MVC****Rotator** widget has built-in features such as unobtrusive and flexible APIs. You can easily create the **Rotator** widget using simple **HTML** helper as follows.

1. Create a **MVC** Project and add necessary assemblies, styles, and scripts to it.
Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).

2. Add the following code example to the corresponding view page to render **Rotator**. Move the images under the folder **~/Images/rotator.**





&lt;div class="frame"&gt;

    @{Html.EJ().Rotator("content").Items(itemElement =>

    {

      itemElement.Add().ContentTemplate(@&lt;div&gt;

      &lt;img class="image" src="@Url.Content("~/Images/rotator/Untitled.png")" /&gt;

  &lt;/div&gt;);

      itemElement.Add().ContentTemplate(@&lt;div&gt;

      &lt;a href="~/Views/Home/Index.cshtml"&gt;&lt;/a&gt;

      &lt;img class="image" src="@Url.Content("~/Images/rotator/Untitled1.png")" /&gt; 

      &lt;/div&gt;);

      itemElement.Add().ContentTemplate(@&lt;div&gt;

      &lt;img class="image" src="@Url.Content("~/Images/rotator/Untitled2.png")" /&gt;

      &lt;/div&gt;);

      itemElement.Add().ContentTemplate(@&lt;div&gt;

      &lt;img class="image" src="@Url.Content("~/Images/rotator/Untitled3.png")" /&gt;

      &lt;/div&gt;);

      itemElement.Add().ContentTemplate(@&lt;div&gt;

      &lt;img class="image" src="@Url.Content("~/Images/rotator/Untitled4.png")" /&gt;

      &lt;/div&gt;);

      }) .SlideWidth("600px").SlideHeight("350px").ShowPlayButton(true).Render();}



  &lt;/div&gt;



3. Add the following styles in the corresponding view page.



  &lt;style type="text/css" class="cssStyles"&gt;

    .frame 

     {

        width: 600px;

     }



    #sliderContent > li .image 

     {

        width: 600px;

        height: 350px;

     }

  &lt;/style&gt; 



4. The following banner is displayed as output.



{% include image.html url="\js\Rotator\getting-started_images\getting-started_img4.png" Caption="Figure 4: Rotator"%}

## Create your first Rotator in ASP.NET

**ASP.NET Image Rotator** comes with a visual that has a spectacular zoom in and fade out effect. A single line of code invokes the **Rotator** effect. Using the following guidelines you can create **Rotator** control for a real-time website banner. It has five images that slide automatically. If you click the center button, image slides in a rotating manner and on second click the rotation stops.

The following screenshot demonstrates the functionality of **Rotator** control.





{% include image.html url="\js\Rotator\getting-started_images\getting-started_img5.png" Caption="Figure 5: Rotator"%}

**Create a Rotator**

**ASP.NET Rotator** widget has built-in features such as unobtrusive and flexible APIs. You can easily create the **Rotator** widget using simple **Rotator** tag as follows.

1. You can create an **ASP.NET** Project and add necessary **Dll’s** and scripts with the help of the given [ ASP.NET -Getting Started Documentation](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).

2. Add the following code example to the corresponding **ASPX** page to render **Rotator**. Place the images under the folder “/Images/rotator”.



**[ASPX]**

&lt;div class="frame"&gt;

        &lt;ej:Rotator ID="RotatorContent" SlideWidth="600px" SlideHeight="350px" ShowPlayButton="true" runat="server"&gt;

            &lt;Items&gt;

                &lt;ej:RotatorItem Url="/images/rotator/EssentialJS.png"&gt;

                &lt;/ej:RotatorItem&gt;

                &lt;ej:RotatorItem Url="/images/rotator/EssentialStudio.png"&gt;

                &lt;/ej:RotatorItem&gt;

                &lt;ej:RotatorItem Url="/images/rotator/EnterpriseEdition.png"&gt;

                &lt;/ej:RotatorItem&gt;

                &lt;ej:RotatorItem Url="/images/rotator/BusinessIntelligence.png"&gt;

                &lt;/ej:RotatorItem&gt;

                &lt;ej:RotatorItem Url="/images/rotator/WinRT.png"&gt;

                &lt;/ej:RotatorItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Rotator&gt;

    &lt;/div&gt;



3. Add the following styles in the corresponding view page.



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

        .frame

        {

            width: 600px;

        }

        #RotatorContent > li img

        {

            width: 610px;

        }

    &lt;/style&gt;



The following banner is displayed as output.

{% include image.html url="\js\Rotator\getting-started_images\getting-started_img6.png" Caption="Figure 6: Rotator"%}

