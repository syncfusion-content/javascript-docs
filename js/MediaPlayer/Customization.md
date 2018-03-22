---
layout: post
title: Customization with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---

# YouTube

You can embed any YouTube videos into media player by providing URL of the YouTube video in source object.

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
                    source: [
                        {
                        "url": "https://www.youtube.com/watch?v=7_hR16f7Drw",
                        "title": "Xamarin",
                        "author": "syncfusion"

                        }
                    ],
                    renderMode: "advanced"
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

![](/js/MediaPlayer/Display_images/Youtube_img1.png)


