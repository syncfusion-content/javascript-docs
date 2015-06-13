---
layout: post
title: Getting-Started
description: getting started
platform: js
control: WaitingPopup
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **WaitingPopup** in your application with **JavaScript**.

## Create your first WaitingPopup in JavaScript

**Essential JavaScript WaitingPopup** provides support to display a **WaitingPopup** within your webpage. From the following guidelines, you can learn how to create a **WaitingPopup** in a real-time login page authentication scenario. 

The following screenshot illustrates the functionality of a **WaitingPopup** with login page scenario.

{% include image.html url="/js/WaitingPopup/Getting-Started_images/Getting-Started_img1.png" Caption="WaitingPopup"%}

You can give the Username and Password in the **login page**. When you click the **Login** button, you get the **WaitingPopup**. After loading, the alert box pops up with the message “Signed in successfully”.

### Create Username and Password

**Essential JavaScript WaitingPopup** widget basically renders built-in features like blocking the other actions until the page is loaded. You can easily create the **WaitingPopup** widget by using simple **&lt;div&gt;** element as follows.

1. Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<link href="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<script src="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!--- add waiting popup element here --->
</body>
</html>


{% endhighlight %}



2. Add **&lt;div&gt;** element to render a **WaitingPopup**.



{% highlight html %}


<div id="targetElement">
    <table class="loginTable">
        <tr>
            <td>Username</td>
            <td><input type="text"></td>
        </tr>
        <tr>
            <td>Password</td>
            <td><input type="password"></td>
        </tr>
        <tr>
            <td></td>
            <td><button id="target">Login</button></td>
        </tr>
    </table>
    <div id="popup"></div>
</div>


{% endhighlight %}



3. Initialize **Click function** using the following code example.



{% highlight js %}

<script type="text/javascript">
    $(document).ready(function () {
        $("#target").click(function () {
            /*Add waiting popup*/
        });
    });
</script>


{% endhighlight %}



4. Apply the following styles to show the **WaitingPopup**.



{% highlight css %}


<style type="text/css" class="cssStyles">
    #targetElement {
        width: 500px;
        height: 200px;
        margin: 50px;
        border: 1px solid #dbdcdb;
    }
    .loginTable {
        margin: 60px auto;
    }
    #popup_WaitingPopup .e-image {
        display: block;
        height: 70px;
    }
</style>


{% endhighlight %}


The following screenshot displays a User****login.



{% include image.html url="/js/WaitingPopup/Getting-Started_images/Getting-Started_img2.png" Caption="WaitingPopup"%}

### Add WaitingPopup Widget

1. In a real-time login page scenario, when you click the Login button, the WaitingPopup is displayed. 

{% highlight js %}


<script type="text/javascript">
    $(document).ready(function () {
        $("#target").click(function () {
            $("#popup").ejWaitingPopup({
                showOnInit: true,
                target: "#targetElement"
            });
            function success() {
                var obj = $("#popup").data("ejWaitingPopup");
                alert("Signed in successfully");
                obj.hide();
            }
            setTimeout(success, 5000);
        });
    });
</script>


{% endhighlight %}



2. The following screenshot shows the output of the above code example.

{% include image.html url="/js/WaitingPopup/Getting-Started_images/Getting-Started_img3.png" Caption="WaitingPopup"%}

