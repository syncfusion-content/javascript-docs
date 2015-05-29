---
layout: post
title: getting-started
description: getting started
platform: js
control: WaitingPopup
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **WaitingPopup** in your application with **JavaScript** and **ASP.NET MVC**.

## Create your first Waiting Popup in JavaScript

**Essential JavaScript Waiting Popup** provides support to display a **Waiting****Popup** within your webpage. From the following guidelines, you can learn how to create a **Waiting****Popup** in a real-time login page authentication scenario. 

The following screenshot illustrates the functionality of a **Waiting****Popup** with login page scenario.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img1.png" Caption="Figure 1: Waiting PopupWaitingPopup"%}{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img2.png" Caption="Figure 1: Waiting PopupWaitingPopup"%}

You can give the Username and Password in the **login page**. When you click the **Login** button, you get the **Waiting****Popup**. After loading, the alert box pops up with the message “Signed in successfully”.

### Create Username and Password

**Essential JavaScript ASP.NET MVC Waiting Popup** widget basically renders built-in features like blocking the other actions until the page is loaded. You can easily create the **Waiting****Popup** widget by using simple **&lt;div&gt;** element as follows.

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <!--- add waiting popup element here --->
</body>
</html>


{% endhighlight %}



* Add **&lt;div&gt;** element to render a **Waiting Popup**.



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
</div><div class="content-container-fluid">
    <div class="row">
        <div class="cols-sample-area">
            <table>
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
    </div>
</div>


{% endhighlight %}



* Initialize **Click function** using the following code example.



{% highlight js %}

<script type="text/javascript">
    $(document).ready(function () {
        $("#target").click(function () {
            /*Add waiting popup*/
        });
    });
</script>


{% endhighlight %}



* Apply the following styles to show the **Waiting PopupWaitingPopup**.



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







&lt;style type="text/css" class="cssStyles"&gt;

    #target {

        margin: 0 auto;

    }

    #target_WaitingPopup .e-image {

        display: block;

        height: 70px;

    }

    #popup {

        height: auto;

        width: auto;

        margin-top: 100px;

    }

&lt;/style&gt;


The following screenshot displays a User****login.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img3.png" Caption="Figure 2: Waiting PopupWaitingPopup"%}{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img4.png" Caption="Figure 2: Waiting PopupWaitingPopup"%}

### Add Waiting PopupWaitingPopup Widget

* In a real-time login page scenario, when you click the **Login** button, the **Waiting****PopupWaitingPopup** is displayed. 

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
</script><script type="text/javascript">
    $(document).ready(function () {
        $("#target").click(function () {
            $("#popup").ejWaitingPopup({
                showOnInit: true
            });
            function success() {
                alert("Signed in successfully");
            }
            setTimeout(success, 5000);
        });
    });
</script>


{% endhighlight %}



* The following screenshot shows the output of the above code example.

![](getting-started_images\getting-started_img5.png)![](getting-started_images\getting-started_img6.png)

_Figure_ _3__:_ _Waiting Popup__WaitingPopup_

## Create your first Waiting Popup in MVC

**ASP.NET MVC Waiting Popup** provides support to display **Waiting Popup** within your webpage. From the following guidelines, you can learn how to create a **Waiting Popup** in a real-time Login page scenario. This helps you in authentication model. The following screenshot illustrates the functionality of a **Waiting Popup** in a Login page scenario.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img7.png" Caption="Figure 4: Waiting Popup"%}



In the above screenshot, you can give the Username and Password. When you click the **Login** button, the **Waiting Popup** appears.  After loading, the alert box appears with a message “Signed in successfully”.

**Create Waiting Popup**

**ASP.NET MVC Waiting Popup** widget has a built-in feature to block all other actions until the page is loaded. You can easily create the **Waiting Popup** control by using simple **HTML** Helper element as follows

1. You can create an **MVC** Project and add necessary assemblies, styles, and scripts with the help of [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

**Create Login Page**

In a real-time Login page scenario, when you click on the **Login** button, the **Waiting Popup** is displayed. This is achieved by using the **btnClick** property.

1. Add the following code example to the corresponding view page to create Login page with username and password.





&lt;div class="content-container-fluid"&gt;

    &lt;div class="row"&gt;

        &lt;div class="cols-sample-area"&gt;

            &lt;table&gt;

                &lt;tr&gt;

                    <td>Username</td>

                    &lt;td&gt;&lt;input type="text"&gt;&lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    <td>Password</td>

                    &lt;td&gt;&lt;input type="password"&gt;&lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;&lt;/td&gt;                       

                 &lt;td&gt;                         @Html.EJ().Button("buttonnormal").Text("Login").Size(ButtonSize.Large).ClientSideEvents(e =>e.Create("btnload").Click("btnClick"))

                 &lt;/td&gt;                    

@Html.EJ().WaitingPopup("target").ShowOnInit(false)

                &lt;/tr&gt;

            &lt;/table&gt;

            &lt;div id="target"&gt;&lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;



2. Add the following styles in the view page to show the **Waiting Popup**.





&lt;style type="text/css" class="cssStyles"&gt;

    #target {

        margin: 0 auto;

    }

    #target_WaitingPopup .e-image {

        display: block;

        height: 70px;

    }

    #popup {

        height: auto;

        width: auto;

        margin-top: 100px;

    }

&lt;/style&gt;



3. Add the following script in the view page.





&lt;script&gt;

            function btnClick(e)

            {

                var wp = $("#target").data("ejWaitingPopup");

                wp.show();

                setTimeout(success, 5000);

            }

            function success()

            {

                alert("Signed in successfully");

                var popup = $("#target").ejWaitingPopup("hide");

            }                  

&lt;/script&gt;



4. The following screenshot displays the User****login.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img8.png" Caption="Figure 5: User Login"%}



5. The following screenshot shows the **Waiting Popup**



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img9.png" Caption="Figure 6: Waiting Popup"%}



The following screenshot displays an alert box displayed with the message “Signed in successfully” after loading.

{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img10.png" Caption="Figure 7: Sign in Successful message"%}



## Create your first Waiting Popup in ASP.NET   

**Essential ASP.NET Waiting Popup** provides support to display a **Waiting****Popup** within your webpage. From the following guidelines, you can learn how to create a **Waiting****Popup** in a real-time login page authentication scenario. 

The following screenshot illustrates the functionality of a **Waiting****Popup** with login page scenario.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img11.png" Caption="Figure 8: Waiting Popup"%}



You can give the Username and Password in the **login page**. When you click the **Login** button, you get the **Waiting****Popup**. After loading, the alert box pops up with the message “Signed in successfully”.

**Create Waiting Popup**

**ASP.NET Waiting Popup** has a built-in feature to block all other actions until the page is loaded. You can easily create the **Waiting Popup** control by using simple **HTML** Helper element as follows

1. You can create a **WEB** Project and add necessary assemblies, styles, and scripts with the help of [ASP-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Create an aspx page and add the following code to the aspx file.



**[ASPX]**

&lt;div class="content-container-fluid"&gt;

        &lt;div class="row"&gt;

            &lt;div class="cols-sample-area"&gt;

                &lt;table&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            Username

                        &lt;/td&gt;

                        &lt;td&gt;

                            &lt;input type="text"&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            Password

                        &lt;/td&gt;

                        &lt;td&gt;

                            &lt;input type="password"&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                        &lt;/td&gt;

                        &lt;td&gt;

                            <ej:Button ID="buttonnormal" runat="server" Type="Button" Text="login" Size="Large"

                                ShowRoundedCorner="true" ClientSideOnClick="btnClick">

                            &lt;/ej:Button&gt;

                        &lt;/td&gt;

                        &lt;ej:WaitingPopup ID="target" runat="server" ShowOnInit="false"&gt;

                        &lt;/ej:WaitingPopup&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

                &lt;div id="target" class="targetpostion"&gt;

                &lt;/div&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



3. Add the following styles in the aspx page to show the **Waiting Popup**.



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

        .content-container-fluid

        {

            margin: 100px 10px 10px 100px;

        }



        #target_WaitingPopup .e-image

        {

            display: block;

            height: 70px;

            top: 120px !important;

        }

    &lt;/style&gt;



The following screenshot displays the User****login.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img12.png" Caption="Figure 9: User Login"%}



**Add Waiting Popup Widget**

In a real-time login page scenario, when you click the **Login** button, the **Waiting****Popup** is displayed. 

**[Script]**



&lt;script type="text/javascript"&gt;

        function btnClick(e) {

            var wp = $("#target").data("ejWaitingPopup");

            wp.show();

            setTimeout(success, 5000);

        }

        function success() {

            alert("Signed in successfully");

            $("#target").ejWaitingPopup("hide");

        }

    &lt;/script&gt;





The following screenshot shows the output of the above code example.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img13.png" Caption="Figure 10: Waiting Popup"%}



The following screenshot displays an alert box displayed with the message “Signed in successfully” after loading.



{% include image.html url="\js\WaitingPopup\getting-started_images\getting-started_img14.png" Caption="Figure 11: Sign in Successful message"%}

