---
layout: post
title: Getting started with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---
# Getting Started

This section explains you the steps required to create a simple Media Player component and configure its available functionalities.

## Dependencies

* ejButton
* ejToggleButton
* ejSlider
* ejWaitingPopup
* ejListView
* ejListBox

You can make use of **ej.web.all.min.js** file which encapsulates all **ej** web components and frameworks in single file.

* [ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js) – includes all web widgets.


## Adding CSS reference



Need to add the following css references for the media player component like other JS 1 controls.

{% highlight html %}

    <link href="../content/bootstrap.min.css" rel="stylesheet">
    <link href="../content/ejthemes/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <link href="../content/default.css" rel="stylesheet" />
    <link href="../content/default-responsive.css" rel="stylesheet" />
    <link href="../content/ejthemes/responsive-css/ej.responsive.css" rel="stylesheet" />

{% endhighlight %}


## Adding JS reference


Need to add the following js references for the media player component like other JS 1 controls.

{% highlight html %}

    <script src="../scripts/jquery-3.1.1.min.js" type="text/javascript"> </script>
    <script src="../scripts/jsrender.min.js" type="text/javascript"></script>
    <script src="../scripts/ej.web.all.min.js" type="text/javascript"></script>
    <script src="../scripts/properties.js" type="text/javascript"></script>

{% endhighlight %}



## Adding Media Player component


Now, you can start adding Essential JS 1 Media Player component in the application. 
Add the HTML <div> element for Media Player component into your index.html

{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
      <title>Essential Studio for JavaScript : Media Player </title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />  
  </head>
    <body>
      <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
       <!--Element which will render as Media Player-->
                <div id="basicPlayer"></div>
            </div>
        </div>
     </div>

     <script type="text/javascript">
        jQuery(function ($) {
            if (!(ej.browserInfo().name === "msie" && Number(ej.browserInfo().version) < 9))        {
       <!--Media Player rendering-->
                $("#basicPlayer").ejMediaPlayer({
                    width: "500px",
                    height: "400px",
                    source: [
                        {
                            "url": "http://files2.syncfusion.com/Videos/samples/Data+Driven+%231+Internet+of+Things.mp4",
                            "title": "Internet of things",
                            "author": "Syncfusion"
                        }
                    ]
                });
            }
            else {
                alert("Media Player (HTML5) will not be supported in IE Version < 9");
            }
        });
     </script>
    </body>
</html> 

{% endhighlight %}

Execute the above code to render the following output.

![](/js/MediaPlayer/Display_images/Getting_img1.png)



