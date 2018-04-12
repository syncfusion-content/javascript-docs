---
layout: post
title: Display format with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---

## Render Mode

There are three rendering layouts in Media Player such as Basic, Advanced and Mobile. You can get the available render modes in ej.MediaPlayer.RenderMode Object as follows.

{% highlight html %}

ej.MediaPlayer.RenderMode = {
    Basic: "basic",
    Advanced: "advanced",
    Mobile: "mobile"
};

{% endhighlight %}

### Basic Mode
Render mode is **Basic** by default in Media Player. It has the simple layout with necessary controls in the toolbar.

{% highlight html %}



<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
      <title>Essential Studio for JavaScript : Media Player - Default Functionalities</title>
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
                    width: "700px",
                    height: "400px",
                    renderMode: ej.MediaPlayer.RenderMode.Basic,
                    source: [
                        {
                            "url":"http://files2.syncfusion.com/Videos/samples/Syncfusion+Dashboard+SDK +and+Mobile+Application.mp4",
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

![](/js/MediaPlayer/Display_images/Basic_img1.png)


### Advanced Mode

**Advanced** mode has the complete layout with all the controls in the toolbar.

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
                    width: "700px",
                    height: "400px",
                    renderMode: ej.MediaPlayer.RenderMode.Advanced,
                    source: [
                         {
                            "url":"http://files2.syncfusion.com/Videos/samples/Syncfusion+Dashboard+SDK +and+Mobile+Application.mp4",
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

![](/js/MediaPlayer/Display_images/Advanced_img.png)



### Mobile Mode

**Mobile** mode has the simple layout especially designed for small size devices.

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
                    width: "700px",
                    height: "400px",
                    renderMode: ej.MediaPlayer.RenderMode.Mobile,
                    source: [
                         {
                           "url":"http://files2.syncfusion.com/Videos/samples/Syncfusion+Dashboard+SDK +and+Mobile+Application.mp4",
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

![](/js/MediaPlayer/Display_images/Mobile_img1.png)


