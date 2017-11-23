---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Rating
documentation: ug
api: /api/js/ejrating
---

# Getting Started

This section explains briefly about how to create a **Rating** control in your application with **JavaScript**. **Essential JavaScript** **Rating** helps to select the number of stars that represent Rating. Here, you can learn how to create **Rating** control in a real-time movie download application and also learn how to rate the application.

The following screenshot illustrates the functionality of a Rating widget with a Rating range of 0 to 5. 

![](/js/Rating/Getting-Started_images/Getting-Started_img1.png) 

##Create a Rating Widget

**Essential JavaScript Rating** widget is provided with built-in features such as precision, orientation and flexible API’s. You can create the **Rating** widget by using input textbox element as follows:

 Create an HTML file and add the following template to the HTML file. You can set the value of the rating widget by using [value](https://help.syncfusion.com/api/js/ejrating#members:value) property.

{% highlight html %}

<!doctype html>
<html>
   <head>
      <meta name="viewport" content="width=device-width, initial-scale=1.0"charset="utf-8"  />
      <!-- Style sheet for default theme (flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet"/>
      <!--Scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <!--Add custom scripts here -->
   </head>
   <body>
      <! -- add rating element here -->
   </body>
</html>


{% endhighlight %}



 Add movies list in the table to render Rating control. Here, you can add corresponding images in the images folder and give the accurate image path.

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



 Initialize Rating in script.

{% highlight javascript %}

    $(function() {
        $("#moviesTab").ejTab();
        $("#mosRating").ejRating({
            value: 2
        });
        $("#wwzRating").ejRating({
            value: 4
        });
        $("#univRating").ejRating({
            value: 4
        });
    });

{% endhighlight %}


 Apply the following styles to show the Rating widget in the horizontal order.

{% highlight css %}

<style type="text/css" class="cssStyles">
    .movies-img {
        width: 125px;
    }
    
    .movie-header {
        font-size: 20px;
        font-weight: 600;
    }
</style>


{% endhighlight %}



 The following screenshot displays a Rating widget.

![](/js/Rating/Getting-Started_images/Getting-Started_img2.png) 

##Set the Min and Max Value

In a real-time scenario, you can extend the range by using the properties [minValue](https://help.syncfusion.com/api/js/ejrating#members:maxvalue) and [maxValue](https://help.syncfusion.com/api/js/ejrating#members:maxvalue) in the **Rating** widget. 

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

![](/js/Rating/Getting-Started_images/Getting-Started_img3.png)

##Set Precision

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

![](/js/Rating/Getting-Started_images/Getting-Started_img4.jpeg)

You can also add additional functionalities such as orientation, event tracer and API’s to the **Rating**. 

