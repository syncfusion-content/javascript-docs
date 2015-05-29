---
layout: post
title: getting-started
description: getting started
platform: js
control: Progress Bar
documentation: ug
---

# Getting Started

This section briefly describes how to create a **Progress Bar** control using **Javascript** and **ASP.NET MVC** and and learn its  features.

## Create your first Progress Bar in JavaScript

**Essential JavaScript****Progress Bar** displays a **Progress Bar** within a webpage that allows you to show the progress of an event. Here, you can learn how to customize the progress and color of the **Progress****Bar** in a real-time application to indicate the strength of the password, where the progress changes with respect to the change in length of the password. This helps you to validate the password is typed. 

The following screenshot shows the **Progress Bar.**


{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img1.png" Caption="Figure 1: Progress Bar"%}

### Create a Progress Bar

**Essential JavaScript Progress Bar** widget is created using a simple **&lt;div&gt;** element. This element provides built-in features that allow you to change the progress, size and text of the control.

You can create the **Progress Bar** widget by using a simple input **&lt;div&gt;** element as follows:

* Create an **HTML** file and add the following template to the **HTML** file to create your **ProgressBar.** It also includes the necessary****scripts and styles.



{% highlight html %}

<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
          <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

    <!--Scripts-->
    <script 
src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Add custom scripts here -->
</head>
<body>
</body>



{% endhighlight %}

**Bar.** It also includes the necessary scripts and styles.




* Add **&lt;input&gt;** element inside the **&lt;body&gt;** tag of your file to create a **Progress Bar.**



{% highlight html %}


<div style="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                  <div class="frame">
                  <div class="wrap_up"> <!--Initializing password field*-->
                                <label for="startButton">Password</label>
                                <input type="password" id="password" style="border-radius:10px"/>
                                   </div>
                           <div class="control"> <!--initializing progress barProgressBar control-->
                                <div id="progressBar"></div>
                            </div>                            
                   </div>                 
            </div>          
        </div>
    </div>


{% endhighlight %}



It also includes a Password field and through that the progress of the **Progress****Bar** can be controlled

* Initialize **Progress Bar** in script.



{% highlight js %}

<script type="text/javascript">
  $(function () {   
             $("#progressBar").ejProgressBar({ 
                height: 20,    
                value: 30,  /*Specify the initial value of the progress in percentage*/  
                width: 200,
                            });
            progresObj = $("#progressBar").data("ejProgressBar");
            progresObj.option("text", "weak");
            $(".e-progress").css({ "background-color": "#DE0909", "border-radius":"10px" });          
            $(".e-progressbar").css({ "border-radius": "10px", "border": "1px solid black" });
});
</script>


{% endhighlight %}



Here, you can initialize the properties of the **Progress Bar** such as height, value, width, text that is applied to the control by default.

The following screenshot displays a **Progress Bar** control.



{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img2.png" Caption="Figure 2: Progress Bar"%}

* Include the following code within the **&lt;head&gt;** tag to change the page layout.





{% highlight css %}

<style type="text/css" class="cssStyles">
    /*applying styles */
    .frame {
        border: 1px solid #BBBCBB;
        border-radius: 10px 10px 10px 10px;
        padding: 50px 60px;
        margin-top: 40px;
        width: 400px;
        margin-left: 400px;
    }

    .control {
        margin-bottom: 5px;
        margin-left: 230px;
    }

    .wrap_up {
        margin-left: 105px;
        font-size: 18px;
    }

    #progressBar {
        margin-top: 10px;
    }
</style><style type="text/css" class="cssStyles"> /*applying styles */
        .frame {
            border: 1px solid #BBBCBB;
            border-radius: 10px 10px 10px 10px;
            padding: 50px 60px;
            margin-top: 40px;
            width: 400px;
            margin-left: 400px;
        }
        .control {
            margin-bottom: 5px;
             margin-left: 230px;
        }
        .wrap_up {
            margin-left: 105px;          
            font-size: 18px;
        }
         #progressBar
        {
        margin-top: 10px;
        }
</style>


{% endhighlight %}

### Progress Control using Length of the Password Field

In real-time scenario, the progress of **Progress Bar** is changed according to the length of text in the password field by binding the change in the properties of control and checking the length of the password field.

* Add the following code example inside the **&lt;script&gt;** tag of your **HTML** file.



{% highlight js %}

var progresObj, buttonObj, k = 10, timer = window.clearInterval(timer), i = 0, obj;
        $(document).keypress(function () { /*To capture the keypress inside the document*/            i = $("#password").val().length;
            if (i < 5) {
                weak();
            }
            else if (i > 5 && i < 7) {
                Strong();
            }
            else if(i>7) {
            var pwd = $("#password").val();
            if(/^[a-zA-Z0-9- ]*$/.test(pwd) == false);

            {
                very_strong();
            }

        } 
  });
            function Strong() { /*Change the width and text of the progress ... called when the length is greater than 5*/
            progresObj.option("text", "strong");
            progresObj.option("percentage", k + 50);
           $(".e-progress").css("background-color", "#0055FF");
            $(".e-progressbar").css("color", "#000000");       
 }
function very_strong() {/*Change the width and text of the progress ... called when the length is greater than 7*/
            progresObj.option("text", "Very strong");
            progresObj.option("percentage", k + 90);
$(".e-progress").css("background-color", "Green");
            $(".e-progressbar").css("color", "#000000");   
     }
function weak() {/*Change the width and text of the progress... called when the length is less than 5*/
            progresObj.option("text", "Weak");
            progresObj.option("percentage", k+20 );
            $(".e-progress").css("background-color", "#DE0909");
            $(".e-progressbar").css("border-radius", "10px");      
  }


{% endhighlight %}



You can calculate length of the password and call the appropriate function that changes the percentage property of **Progress BarProgressBar**.

* The **weak()** function changes the text inside the **Progress BarProgressBar** to **Weak** and percentage to 30, that is invoked when the length of the text is less than 5.

* The **strong()** function changes the text inside the **Progress BarProgressBar** to **Strong** and percentage to 60, that is invoked when the length of the text exceeds 5.

* The **very_strong()** function changes the text inside the **Progress BarProgressBar** to **Very****Strong** and percentage to 100, that is invoked when the length of the text exceeds 7 and the text contains a symbol in it.

You can change themes or appearance of the **Progress BarProgressBar** as required.

The final output is displayed as follows.



{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img3.png" Caption="Figure 3: For password length less than 5"%}

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img4.png" Caption="Figure 4: For password length less than 7"%}



{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img5.png" Caption="Figure 5: For password length greater than 7"%}

You can also bind an event at the start and finish of a **Progress BarProgressBar** by using the start, complete and change properties of the **Progress BarProgressBar**.

## Create your first Progress Bar in MVC

**ASP.NET MVC****Progress Bar** control provides support to display a **Progress Bar** that allows you to change the process of the **Progress****Bar** animations and flexible APIs. Using the following guidelines, you can create the **Progress****Bar** to validate the Password strength.

The following screenshot illustrates the functionality of a **Progress Bar** and displays the final result of the Password Strength Validation for your password using **Progress Bar.**

![](getting-started_images\getting-started_img6.png)![](getting-started_images\getting-started_img7.png)![](getting-started_images\getting-started_img8.png)

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img9.png" Caption="Figure 6: Progress Bar"%}

**Create a Textbox and Progress Bar**

**ASP.NET MVC Progress Bar** control indicates the current progress of an operation like uploading a document through a simple interface. You can easily create the **Progress bar** control using simple **HTML** helpers as follows.

1. Create an**MVC** Project and add necessary assemblies, scripts and styles to it.
Refer[MVC-Getting Started.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)



2. Add the following code to the corresponding view page to render **Progress Bar**.



&lt;div class="start" &gt;

         <label for="start">Password</label>

               &lt;input type="password" id="password" style="border-radius:10px" /&gt;

  @Html.EJ().ProgressBar("progressBar").Value(20).Height("20px").Width("180px") 

 &lt;/div&gt;



3. Add the following styles to show the **Progress Bar** and Textbox.



 &lt;style&gt;

 .start {

            margin-left: 105px;

            color: green;

            font-size: 18px;

        }

.control {

            margin-bottom: 5px;

             margin-left: 230px;

        }

 #progressBar

   {

    margin-top: 10px;

   }

&lt;/style&gt;



4. Execute the above code to render the following output. 



{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img10.png" Caption="Figure 7: Progress Bar with Textbox"%}

**Find the Strength of the Password**

In this scenario, the advancement of the **Progress Bar** is changed according to the length and special characters present in the text of the password field. This is achieved by binding the change in the properties of your control and by checking the length of the password field.


       &lt;script&gt; 

            var progresObj, k = 10, i = 0;

            $(document).keydown(function() {

                i = $("#password").val().length;

                if (i < 4) {

                    progress2();

                    $('.e-progress').css({ background: 'red' });

                } else if (i > 4 && i < 7) {

                    progress1();

                    $('.e-progress').css({ background: 'yellow' });

                } else if (i > 7) {

                    var pwd = $("#password").val();



                    if (/^[a-zA-Z0-9- ]*$/.test(pwd) == false) {

                        progress();

                        $('.e-progress').css({ background: 'green' });

                    }

                }

            });





            $(function () {

                progresObj = $("#progressBar").data("ejProgressBar");       

            });

            function progress() {

                progresObj.option("text", " verystrong");

                progresObj.option("percentage", k + 90);

            }

            function progress1() {

                progresObj.option("text", "strong");

                progresObj.option("percentage", k + 50);

            }

            function progress2() {

                progresObj.option("percentage", k + 10);

                progresObj.option("text", "weak");  



            }



        &lt;/script&gt;



* The **progress()** function changes the text inside the **Progress Bar** to Very Strong and percentage to 100, and it is invoked when the length of the text is more than 7 and the text contains a symbol in it. Then it shows the **Progress Bar** in violet color.

* The **progress1()** function changes the text inside the **Progress Bar** to Strong and percentage to 60, and it is invoked when the length of the text is more than 4. Then it shows the **Progress Bar** in green color

* The **progress 2()** function changes the text inside the **Progress Bar** to Weak and percentage to 30, and it is invoked when the length of the text is less than 4. Then it shows the **Progress****Bar** in red color.

The following screenshot displays a **Progress Bar** control for the above scenario.



{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img11.png" Caption="Figure 8: Weak Password	"%}

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img12.png" Caption="Figure 9: Strong Password"%}

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img13.png" Caption="Figure 10: Very Strong Password       "%}

## Create your first Progress Bar in ASP.NET

**ASP.NET ProgressBar** displays a **ProgressBar** within a webpage that allows you to show the progress of an event. Here, you can learn how to customize the progress and color of the **ProgressBar** in a real-time application to indicate the strength of the password, where the progress changes with respect to the change in length of the password. This enables you to validate the password is typed. 

The following screenshot shows the **ProgressBar.**

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img14.png" Caption="Figure 11: ProgressBar"%}

**Create a ProgressBar**

**ASP.NET ProgressBar** control is created using **&lt;ej:ProgressBar&gt;** tag. This element provides a built-in feature that allows you to change the progress, size and text of the control.

You can create the **ProgressBar** control by using the following steps.

* You can create an **ASP.NET Project** and add necessary **Dll** and script with the help of the given [ASP-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

* You can add the following code example to the corresponding **ASPX** page to render **ProgressBar**.



**[ASPX]**

    &lt;div style="content-container-fluid"&gt;

        &lt;div class="row"&gt;

            &lt;div class="cols-sample-area"&gt;

                &lt;div class="frame"&gt;

                    &lt;div class="wrap_up"&gt;

                        &lt;!--Initializing password field*--&gt;

                        &lt;label for="startButton"&gt;

                            Password</label>

                        &lt;input type="password" id="password" style="border-radius: 10px" /&gt;

                    &lt;/div&gt;

                    &lt;div class="control"&gt;

                        &lt;!--initializing progressbar control--&gt;

                        &lt;ej:ProgressBar ID="ProgressBar" Height="20px" Width="200px" Value="30" runat="server" Text="Weak"&gt;

                        &lt;/ej:ProgressBar&gt;

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



It also includes a Password field and through that the progress of the **ProgresBar** can be controlled

* Include the following **CSS** within the **&lt;head&gt;** tag to change the page layout.



**[CSS]**

    &lt;style type="text/css" class="cssStyles"&gt;

        /*applying styles */

        .frame

        {

            border: 1px solid #BBBCBB;

            border-radius: 10px 10px 10px 10px;

            padding: 50px 60px;

            margin-top: 40px;

            width: 400px;

            margin-left: 400px;

        }

        .control

        {

            margin-bottom: 5px;

            margin-left: 230px;

        }

        .wrap_up

        {

            margin-left: 105px;

            font-size: 18px;

        }

        #progressBar

        {

            margin-top: 10px;

        }

    &lt;/style&gt;



* Also include the following script.



**[SCRIPT]**

&lt;script type="text/javascript"&gt;

        $(function () {

            $(".e-progress").css({ "background-color": "#DE0909", "border-radius": "10px" });

            $(".e-progressbar").css({ "border-radius": "10px", "border": "1px solid black" });

        });

    &lt;/script&gt;



The following screenshot displays a **ProgressBar** control.


{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img15.png" Caption="Figure 12: ProgressBar"%}

**Progress Control using Length of the Password Field**

In real-time scenario, the progress of **ProgressBar** is changed according to the length of text in the password field by binding the change in the properties of control and checking the length of the password field.

Add the following code example inside the **&lt;script&gt;** tag of your **ASP.NET** web page.



**[SCRIPT]**

    &lt;script type="text/javascript"&gt;

        $(function () {

            $(".e-progress").css({ "background-color": "#DE0909", "border-radius": "10px" });

            $(".e-progressbar").css({ "border-radius": "10px", "border": "1px solid black" });

        });

        var progresObj, buttonObj, k = 10, timer = window.clearInterval(timer), i = 0, obj;

        $(document).keypress(function () { /*To capture the keypress inside the document*/

            i = $("#password").val().length;

            if (i < 5) {

                weak();

            }

            else if (i >= 5 && i < 7) {

                Strong();

            }

            else if (i > 7) {

                var pwd = $("input").val();

                if (/^[a-zA-Z0-9- ]*$/.test(pwd) == false);

                {

                    veryStrong();

                }

            }

        });

        function Strong() { /*Change the width and text of the progress ... called when the length is greater than 5*/

            progresObj.option("text", "strong");

            progresObj.option("percentage", k + 50);

            $(".e-progress").css("background-color", "#0055FF");

            $(".e-progressbar").css("color", "#000000");

        }

        function veryStrong() {/*Change the width and text of the progress ... called when the length is greater than 7*/

            progresObj.option("text", "Very strong");

            progresObj.option("percentage", k + 90);

            $(".e-progress").css("background-color", "Green");

            $(".e-progressbar").css("color", "#000000");

        }

        function weak() {/*Change the width and text of the progress... called when the length is less than 5*/

            progresObj.option("text", "Weak");

            progresObj.option("percentage", k + 20);

            $(".e-progress").css("background-color", "#DE0909");

            $(".e-progressbar").css("border-radius", "10px");

        }        

    &lt;/script&gt;



You can calculate length of the password and call the appropriate function that changes the percentage property of **ProgressBar**.

The **weak()** function changes the text inside the **ProgressBar** to **Weak** and percentage to 30, that is invoked when the length of the text is less than 5.

The **strong()** function changes the text inside the **ProgressBar** to **Strong** and percentage to 60, that is invoked when the length of the text exceeds 5.

The **veryStrong()** function changes the text inside the **ProgressBar** to **Very****Strong** and percentage to 100, that is invoked when the length of the text exceeds 7 and the text contains a symbol in it.

You can change themes or appearance of the **ProgressBar** as required.

The final output is displayed as follows.

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img16.png" Caption="Figure 13: For password length less than 5	"%}

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img17.png" Caption="Figure 14: For password length less than 7"%}

{% include image.html url="\js\ProgressBar\getting-started_images\getting-started_img18.png" Caption="Figure 15: For password length greater than 7"%}

You can also bind an event at the start and finish of a **ProgressBar** by using the start, complete and change properties of the **ProgressBar**.



