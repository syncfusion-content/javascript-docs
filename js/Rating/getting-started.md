---
layout: post
title: getting-started
description: getting started
platform: js
control: Rating
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Rating** control in your application with **JavaScript**, **ASP.NET MVC** and **ASP.NET**. 

## Create your first Rating Widget in JavaScript

**Essential JavaScript****Rating** helps to select the number of stars that represent **Rating**. Here, you can learn how to create **Rating** control in a real-time movie download application and also learn how to rate the application.

The following screenshot illustrates the functionality of a **Rating** widget with a Rating range of 0 to 5. 



{% include image.html url="\js\Rating\getting-started_images\getting-started_img1.png" Caption="Figure 1: Rating"%}{% include image.html url="\js\Rating\getting-started_images\getting-started_img2.png" Caption="Figure 1: Rating"%}

### Create a Rating Widget

**Essential JavaScript Rating** widget is provided with built-in features such as precision, orientation and flexible API’s. You can create the **Rating** widget by using input textbox element as follows:

* Create an **HTML** file and add the following template to the **HTML** file.

{% highlight html %}

<!doctype html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0"charset="utf-8"  />
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
   <! -- add rating element here -->
</body>
</html>


{% endhighlight %}





Add movies list in the table to render **Rating** control. Here, you can add corresponding images in the images folder and give the accurate image path.



{% highlight html %}

<div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div style="width: 500px">
                    <div id="moviesTab">
                        <ul>
                            <li><a href="#steelman">Man of Steel</a></li>
                            <li><a href="#woldwar">World War Z</a></li>
                            <li><a href="#unive">Monsters University</a></li>
                        </ul>
                        <div id="steelman">
                            <div>
                                <table>
                                    <tr>
                                        <td class="movies-img" valign="top">
                                            <img src="../images/rating/mos.png" alt="mos" />
                                        </td>
                                        <td valign="top">
                                            <div>
                                                <span class="movie-header">Man of Steel</span><br />
                                                Rating :
                                                        <br />
                                                <input id="mosRating" type="text" class="rating" />
                                                <span>Movie Info:</span>
                                                <p>
                                                    A young boy learns that he has extraordinary powers and is not of this Earth.
                                                </p>
                                            </div>
                                        </td>
                                    </tr>
                                </table>
                            </div>
                        </div>
                        <div id="woldwar">
                            <table>
                                <tr>
                                    <td class="movies-img" valign="top">
                                        <img src="../images/rating/wwz.png" alt="mos" />
                                    </td>
                                    <td valign="top">
                                        <div>
                                            <span class="movie-header">World War Z</span><br />
                                            Rating :
                                                    <br />
                                            <input id="wwzRating" type="text" class="rating" />
                                            <span>Movie Info:</span>
                                            <p>
                                                The story revolves around United Nations employee Gerry Lane (Pitt).
                                            </p>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>
                        <div id="unive">
                            <table>
                                <tr>
                                    <td class="movies-img" valign="top">
                                        <img src="../images/rating/mu.png" alt="mos" />
                                    </td>
                                    <td valign="top">
                                        <div>
                                            <span class="movie-header">Monsters University</span><br />
                                            Rating :
                                                    <br />
                                            <input id="univRating" type="text" class="rating" />
                                            <span>Movie Info:</span>
                                            <p>
                                                Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case. 
                                            </p>
                                        </div>
                                    </td>
                                </tr>
                            </table>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>


{% endhighlight %}



Initialize **Rating** in script.



{% highlight js %}

<script type="text/javascript">
        $(function () {
            $("#moviesTab").ejTab();
            $("#mosRating").ejRating({ value: 2 });
            $("#wwzRating").ejRating({ value: 4 });
            $("#univRating").ejRating({ value: 4 });
        });
</script>


{% endhighlight %}



Apply the following styles to show the **Rating** widget in the horizontal order.



{% highlight css %}

    <style type="text/css" class="cssStyles">
        .movies-img
        {
            width: 125px;
        }

        .movie-header
        {
            font-size: 20px;
            font-weight: 600;
        }
    </style>


{% endhighlight %}



The following screenshot displays a **Rating** widget.



{% include image.html url="\js\Rating\getting-started_images\getting-started_img3.png" Caption="Figure 2: Rating"%}{% include image.html url="\js\Rating\getting-started_images\getting-started_img4.png" Caption="Figure 2: Rating"%}

### Set the Min and Max Value

In a real-time scenario, you can extend the range by using the properties **minValue** and **maxValue** in the **Rating** widget. 


{% highlight html %}

<body>
<div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <table>
                        <tr>
                            <td valign="top">Rate:
                            </td>
                            <td>
                                <input id="fullRating" type="text" class="rating" />
                            </td>
                            </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
<script type="text/javascript">
        $(function () {
            $("#fullRating").ejRating({ value:4, minValue:2, maxValue: 10 });
        }); // set the minValue and maxValue here
    </script>
    <style type="text/css" class="cssStyles">
        .frame
        {
            width: 277px;
        }
    </style>
</body>


{% endhighlight %}



The above code example displays the following output.

{% include image.html url="\js\Rating\getting-started_images\getting-started_img5.png" Caption="Figure 3: Setting Min and Max Values	"%}

### Set Precision

In a real-time movie **Rating** scenario, you can set precision in between two whole numbers, such as 2.5 or 3.7 and it is done using the property **precision** by changing the value to **ej.Rating.Precision.Half** or **ej.Rating.Precision.Exact.**



{% highlight html %}

<body>
<div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <table>
                        <tr>
                            <td valign="top">Full Precision :
                            </td>
                            <td>
                                <input id="fullRating" type="text" class="rating" />
                            </td>
                        </tr>
                        <tr>
                            <td valign="top">Half Precision :
                            </td>
                            <td>
                                <input id="halfRating" type="text" class="rating" />
                            </td>
                        </tr>
                        <tr>
                            <td valign="top">Exact Precision :
                            </td>
                            <td>
                                <input id="exactRating" type="text" class="rating" />
                            </td>
                        </tr>
                    </table>
                </div>
            </div>
        </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#fullRating").ejRating({ value: 4 });
            $("#halfRating").ejRating({ precision: ej.Rating.Precision.Half, value: 3.5 });
            $("#exactRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 3.7 });
        }); 
   // set the precision values here 
    </script>
    <style type="text/css" class="cssStyles">
        .frame
        {
            width: 277px;
        }
    </style>
</body>


{% endhighlight %}



The above code example displays the following output.



![C:\Users\mohanrao\Desktop\mv2.jpg](getting-started_images\getting-started_img6.jpeg)



_Figure_ _4__: Rating with accurate values_

You can also add additional functionalities such as orientation, event tracer and API’s to the **Rating**. 

## Create your first Rating control in MVC

**Essential Studio ASP.NET MVC****Rating** control provides support to display **Rating** bar within your webpage, and allows you to rate the products. Refer the following guidelines to customize **Rating** control for a real-time movie download application. You can use **Rating** control to rate a movie.

The following screenshot demonstrates the functionality of a **Rating** control with a Rating range of 0 to 5. 



{% include image.html url="\js\Rating\getting-started_images\getting-started_img7.png" Caption="Figure 5: Rating"%}

In the above screenshot, you can rate the movie by selecting a corresponding movie.

**Create a Rating** 

The **Essential Studio ASP.NET MVC****Rating** widget renders with built-in features like precision, orientation and flexible APIs. You can easily create the **Rating** widget using **HTML** helper class as follows.

* You can create an **MVC** Project and add the necessary assemblies, styles and scripts to it.
 Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).

Add the following code example to the corresponding view page to render **Rating**.



            &lt;div class="frame"&gt;  



            @{Html.EJ().Tab("moviesTab").Items(evt=> 

            {                

                 evt.Add().ID("steelman").Text("Man of Steel").ContentTemplate(

                     @&lt;div&gt;

                        &lt;table&gt;

                            &lt;tr&gt;

                                &lt;td class="movies-img" valign="top"&gt;                                    

                                    &lt;img src="@Url.Content("~/Images/rating/mos.png")" alt="mos" /&gt;

                                &lt;/td&gt;

                                &lt;td valign="top"&gt;

                                    &lt;div&gt;

                                        <span class="movie-header">Man of Steel</span>&lt;br /&gt;

                                        Rating :

                                                        &lt;br /&gt;



                                         @Html.EJ().Rating("univRating").Value(4)

                                        <span>Movie Info:&lt;/span&gt;

                                        &lt;p&gt;

                                            A young boy learns that he has extraordinary powers and is not of this Earth.

                                        &lt;/p&gt;

                                    &lt;/div&gt;

                                &lt;/td&gt;

                            &lt;/tr&gt;

                        &lt;/table&gt;

                    &lt;/div&gt;);



                 evt.Add().ID("woldwar").Text("World War Z").ContentTemplate(

                     @&lt;div&gt;

                    &lt;table&gt;

                        &lt;tr&gt;

                            &lt;td class="movies-img" valign="top"&gt;                                

                                &lt;img src="@Url.Content("~/Images/rating/wwz.png")" alt="mos" /&gt;

                            &lt;/td&gt;

                            &lt;td valign="top"&gt;

                                &lt;div&gt;

                                    <span class="movie-header">World War Z</span>&lt;br /&gt;

                                    Rating :

                                                    &lt;br /&gt;                                  

                                    @Html.EJ().Rating("wwzRating"). Value(4)

                                    <span>Movie Info:&lt;/span&gt;

                                    &lt;p&gt;

                                        The story revolves around United Nations employee Gerry Lane (Pitt).

                                    &lt;/p&gt;

                                &lt;/div&gt;

                            &lt;/td&gt;

                        &lt;/tr&gt;

                    &lt;/table&gt;

                &lt;/div&gt;);

                 evt.Add().ID("unive").Text("Monsters University").ContentTemplate(

                     @&lt;div&gt;

                    &lt;table&gt;

                        &lt;tr&gt;

                            &lt;td class="movies-img" valign="top"&gt;                                

                                &lt;img src="@Url.Content("~/Images/rating/mu.png")" alt="mos" /&gt;

                            &lt;/td&gt;

                            &lt;td valign="top"&gt;

                                &lt;div&gt;

                                    <span class="movie-header">Monsters University</span>&lt;br /&gt;

                                    Rating :

                                                    &lt;br /&gt;



                                    @Html.EJ().Rating("mosRating").Value(3)

                                    <span>Movie Info:&lt;/span&gt;

                                    &lt;p&gt;

                                        Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case. 

                                    &lt;/p&gt;

                                &lt;/div&gt;

                            &lt;/td&gt;

                        &lt;/tr&gt;

                    &lt;/table&gt;

                &lt;/div&gt;);

            }).Render();}

         &lt;/div&gt;





Add the following styles to the corresponding view page to show the **Rating** in horizontal order.


&lt;style type="text/css" class="cssStyles"&gt;

        .movies-img {

            width: 125px;

        }



        .movie-header {

            font-size: 20px;

            font-weight: 600;

        }

        .frame {

            width: 600px;

            height: 250px;

        }

    &lt;/style&gt;



Execute the above code to render the following output.





{% include image.html url="\js\Rating\getting-started_images\getting-started_img8.png" Caption="Figure 6: Rating"%}

![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img9.png)_**Note: Add necessary images to the mentioned directory.**_

> _**&lt;project directory&gt;/Images/rating/yourimage.png**_

**Set Min and Max Value**

In a real-time movie **Rating** scenario, you can extend the range using the properties **minValue** and **maxValue**. Only rates ranging between the **minValue** and **maxValue** appear in the **Rating**.

* Add the following code example to the corresponding view page to set **MinValue** and **MaxValue** to the **Rating**.







            &lt;div class="frame"&gt;  



            @{Html.EJ().Tab("moviesTab").Items(evt=> 

            {                

                 evt.Add().ID("steelman").Text("Man of Steel").ContentTemplate(

                     @&lt;div&gt;

                        &lt;table&gt;

                            &lt;tr&gt;

                                &lt;td class="movies-img" valign="top"&gt;                                    

                                    &lt;img src="@Url.Content("~/Images/rating/mos.png")" alt="mos" /&gt;

                                &lt;/td&gt;

                                &lt;td valign="top"&gt;

                                    &lt;div&gt;

                                        <span class="movie-header">Man of Steel</span>&lt;br /&gt;

                                        Rating :

                                                        &lt;br /&gt;



                                         @Html.EJ().Rating("univRating").Value(3).MinValue(0).MaxValue(10)

                                        <span>Movie Info:&lt;/span&gt;

                                        &lt;p&gt;

                                            A young boy learns that he has extraordinary powers and is not of this Earth.

                                        &lt;/p&gt;

                                    &lt;/div&gt;

                                &lt;/td&gt;

                            &lt;/tr&gt;

                        &lt;/table&gt;

                    &lt;/div&gt;);





                 evt.Add().ID("woldwar").Text("World War Z").ContentTemplate(

                     @&lt;div&gt;

                    &lt;table&gt;

                        &lt;tr&gt;

                            &lt;td class="movies-img" valign="top"&gt;                                

                                &lt;img src="@Url.Content("~/Images/rating/wwz.png")" alt="mos" /&gt;

                            &lt;/td&gt;

                            &lt;td valign="top"&gt;

                                &lt;div&gt;

                                    <span class="movie-header">World War Z</span>&lt;br /&gt;

                                    Rating :

                                                    &lt;br /&gt;                                  

                                    @Html.EJ().Rating("wwzRating").Value(4).MinValue(3).MaxValue(10)

                                    <span>Movie Info:&lt;/span&gt;

                                    &lt;p&gt;

                                        The story revolves around United Nations employee Gerry Lane (Pitt).

                                    &lt;/p&gt;

                                &lt;/div&gt;

                            &lt;/td&gt;

                        &lt;/tr&gt;

                    &lt;/table&gt;

                &lt;/div&gt;);





                 evt.Add().ID("unive").Text("Monsters University").ContentTemplate(

                     @&lt;div&gt;

                    &lt;table&gt;

                        &lt;tr&gt;

                            &lt;td class="movies-img" valign="top"&gt;                                

                                &lt;img src="@Url.Content("~/Images/rating/mu.png")" alt="mos" /&gt;

                            &lt;/td&gt;

                            &lt;td valign="top"&gt;

                                &lt;div&gt;

                                    <span class="movie-header">Monsters University</span>&lt;br /&gt;

                                    Rating :

                                                    &lt;br /&gt;



                                    @Html.EJ().Rating("mosRating").Value(3). MinValue(4).MaxValue(20)

                                    <span>Movie Info:&lt;/span&gt;

                                    &lt;p&gt;

                                        Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always the case. 

                                    &lt;/p&gt;

                                &lt;/div&gt;

                            &lt;/td&gt;

                        &lt;/tr&gt;

                    &lt;/table&gt;

                &lt;/div&gt;);

            }).Render();}

         &lt;/div&gt;




Execute the above code to render the following output.



{% include image.html url="\js\Rating\getting-started_images\getting-started_img10.png" Caption="Figure 7: Setting Min and Max values"%}

![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img11.png)_**Note: Add the necessary images to the mentioned directory.**_

> _**&lt;project directory&gt;/Images/rating/yourimage.png**_

**Set Precision**

In a real-time movie **Rating** scenario, you can rate the **Rating** between two whole numbers, such as 2.5 or 3.7 using the **Precision** property. You can also add additional functionalities such as **Orientation** and **APIs** to the **Rating**. 

* Add the following code example to the corresponding view page to set **Precision** to **Rating**.





       &lt;div class="frame"&gt;

            &lt;table&gt;

                &lt;tr&gt;

                    <td valign="top">Full Precision :

                    &lt;/td&gt;

                    &lt;td&gt;

                        @Html.EJ().Rating("fullRating").Value(4)

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    <td valign="top">Half Precision :

                    &lt;/td&gt;

                    &lt;td&gt;

                        @Html.EJ().Rating("halfRating").Value(3).Precision(Precision.Half)

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    <td valign="top">Exact Precision :

                    &lt;/td&gt;

                    &lt;td&gt;

                        @Html.EJ().Rating("exactRating").Value(4).Precision(Precision.Exact)

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/table&gt;

        &lt;/div&gt;



    &lt;style type="text/css" class="cssStyles"&gt;

        .frame {

            width: 350px;

            border:1px solid #ccc;

            border-radius:7px;

            padding:50px;        }

    &lt;/style&gt;





Execute the above code to render the following output.



{% include image.html url="\js\Rating\getting-started_images\getting-started_img12.jpeg" Caption="Figure 8: Rating with accurate values"%}

## Create your first Rating control in ASP.NET

**ASP.NET Rating** helps you to select the number of stars that represent Rating. Here, you can learn how to create **Rating** control in a real-time movie download application and also learn how to rate the application.

The following screenshot demonstrates the functionality of a **Rating** control with a Rating range of 0 to 5. 





{% include image.html url="\js\Rating\getting-started_images\getting-started_img13.png" Caption="Figure 9: Rating"%}

In the above screenshot, you can rate the movie by selecting a corresponding movie.

**Create a Rating** 

The **Essential Studio ASP.NET Rating** control renders with built-in features like precision, orientation and flexible **APIs**. You can easily create the **Rating** control using **Rating** tags as follows. 

* You can create an **ASP.NET Web Forms** Project and add necessary **Dll’s** and scripts with the help of the given [ ASP.NET -Getting Started Documentation.](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

Add the following code example to the corresponding **ASPX** page to render **Rating** control.

Refer the following link to know details on **Tab** control.

[http://help.syncfusion.com/ug/js/documents/createyourfirsttabco.htm](http://help.syncfusion.com/ug/js/documents/createyourfirsttabco.htm)



    &lt;div class="frame"&gt;

        &lt;ej:Tab ID="Tab1" runat="server" Width="550px"&gt;

            &lt;Items&gt;

                &lt;ej:TabItem Id="TabItem1" Text="Man Of Steel"&gt;

                    &lt;ContentSection&gt;

                        &lt;table&gt;

                            &lt;tr&gt;

                                &lt;td class="movies-img" valign="top"&gt;

                                    &lt;img src="../Content/images/rating/mos.png" alt="mos" /&gt;

                                &lt;/td&gt;

                                &lt;td valign="top"&gt;

                                    &lt;div&gt;

                                        <span class="movie-header">Man of Steel</span>&lt;br /&gt;

                                        Rating :

                                        &lt;br /&gt;

                                        &lt;ej:Rating ID="Rating8" Value="3" MinValue="0" MaxValue="5" runat="server"&gt;

                                        &lt;/ej:Rating&gt;

                                        <span>Movie Info:&lt;/span&gt;

                                        &lt;p&gt;

                                            A young boy learns that he has extraordinary powers and is not of this Earth.

                                        &lt;/p&gt;

                                    &lt;/div&gt;

                                &lt;/td&gt;

                            &lt;/tr&gt;

                        &lt;/table&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:TabItem&gt;

                &lt;ej:TabItem Id="TabItem2" Text="World War Z"&gt;

                    &lt;ContentSection&gt;

                        &lt;table&gt;

                            &lt;tr&gt;

                                &lt;td class="movies-img" valign="top"&gt;

                                    &lt;img src="../Content/images/rating/wwz.png" alt="mos" /&gt;

                                &lt;/td&gt;

                                &lt;td valign="top"&gt;

                                    &lt;div&gt;

                                        <span class="movie-header">World War Z</span>&lt;br /&gt;

                                        Rating :

                                        &lt;br /&gt;

                                        &lt;ej:Rating ID="Rating9" Value="4" MinValue="0" MaxValue="5" runat="server" CssClass="rating"&gt;

                                        &lt;/ej:Rating&gt;

                                        <span>Movie Info:&lt;/span&gt;

                                        &lt;p&gt;

                                            The story revolves around United Nations employee Gerry Lane (Pitt).

                                        &lt;/p&gt;

                                    &lt;/div&gt;

                                &lt;/td&gt;

                            &lt;/tr&gt;

                        &lt;/table&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:TabItem&gt;

                &lt;ej:TabItem Id="TabItem3" Text="Monsters University"&gt;

                    &lt;ContentSection&gt;

                        &lt;table&gt;

                            &lt;tr&gt;

                                &lt;td class="movies-img" valign="top"&gt;

                                    &lt;img src="../Content/images/rating/mu.png" alt="mos" /&gt;

                                &lt;/td&gt;

                                &lt;td valign="top"&gt;

                                    &lt;div&gt;

                                        <span class="movie-header">Monsters University</span>&lt;br /&gt;

                                        Rating :

                                        &lt;br /&gt;

                                        &lt;ej:Rating ID="Rating10" Value="4" MinValue="0" MaxValue="5" runat="server"&gt;

                                        &lt;/ej:Rating&gt;

                                        <span>Movie Info:&lt;/span&gt;

                                        &lt;p&gt;

                                            Mike Wazowski and James P. Sullivan are an inseparable pair, but that wasn't always

                                            the case.

                                        &lt;/p&gt;

                                    &lt;/div&gt;

                                &lt;/td&gt;

                            &lt;/tr&gt;

                        &lt;/table&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:TabItem&gt;

            &lt;/Items&gt;

        &lt;/ej:Tab&gt;

    &lt;/div&gt; 



Add the following styles to the corresponding view page to show the **Rating** in horizontal order.


&lt;style type="text/css" class="cssStyles"&gt;

        .movies-img

        {

            width: 125px;

        }        

        .movie-header

        {

            font-size: 20px;

            font-weight: 600;

        }

        .frame

        {

            width: 600px;

            height: 250px;

        }

    &lt;/style&gt;



Execute the above code to render the following output.



{% include image.html url="\js\Rating\getting-started_images\getting-started_img14.png" Caption="Figure 10: Rating"%}



![C:\Users\ApoorvahR\Desktop\Note.png](getting-started_images\getting-started_img15.png)_**Note: Add necessary images to the mentioned directory.**_

_**&lt;project directory&gt;/Images/rating/yourimage.png**_

**Set Min and Max Value**

In a real-time movie **Rating** scenario, you can extend the range using the properties **MinValue** and **MaxValue**. Only rates ranging between the **MinValue** and **MaxValue** appear in the **Rating**.

* Add the following code example to the corresponding **ASPX** page to set **MinValue** and **MaxValue** to the **Rating**.



    &lt;div class="frame"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td valign="top"&gt;

                    Rate:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating1" Value="4" MinValue="2" MaxValue="10" runat="server"&gt;

                    &lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



Execute the above code to render the following output.

{% include image.html url="\js\Rating\getting-started_images\getting-started_img16.png" Caption=" Figure 11: Setting Min and Max values"%}

**Set Precision**

In a real-time movie **Rating** scenario, you can rate the **Rating** between two whole numbers, such as 2.5 or 3.7 using the **Precision** property. You can also add additional functionalities such as **Orientation** and **APIs** to the **Rating**. 

* Add the following code example to the corresponding view page to set Precision to Rating.



  &lt;div class="frame"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                &lt;td valign="top"&gt;

                    Full Precision :

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating1" Value="4" Precision="Full" runat="server" CssClass="rating"&gt;

                    &lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td valign="top"&gt;

                    Half Precision :

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating2" Value="1.5" Precision="Half" runat="server" CssClass="rating"&gt;

                    &lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

            &lt;tr&gt;

                &lt;td valign="top"&gt;

                    Exact Precision :

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating3" Value="3.7" Precision="Exact" runat="server" CssClass="rating"&gt;

                    &lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



Execute the above code to render the following output.



{% include image.html url="\js\Rating\getting-started_images\getting-started_img17.png" Caption="Figure 12: Rating with accurate values"%}

