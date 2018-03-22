---
layout: post
title: Behavior-Settings with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---

## Behavior Settings

You can find settings icon in the toolbar which has Speed and Quality customization. Media speed and quality can be modified according to the available options. 

## Speed

Speed can be set while rendering the control and it is applicable for both YouTube and other web media. Speed value is 1 for all media by default.


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
                    playSpeed: 1.5,
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


## Quality

Quality can be set through settings window and it is applicable only for YouTube videos. Value is **Auto** for all videos by default. These are the available quality values.

{% highlight html %}

ej.MediaPlayer.Quality = {
    "240p": "small",
    "360p": "medium",
    "480p": "large",
    "720p": "hd720",
    "1080p": "hd1080",
    "auto": "auto"
};

{% endhighlight %}


## Playlist

**Playlist** will be generated once you render the control with source collection. You can set visibility for play list while rendering, it is false by default. 


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
                    showPlaylist: true,
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

## Title

You can add media title for each file in source object. Title will be shown on top of the Player, also reflected in play list. You can show/hide the title by setting **showTitle** property, it is true by default.

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
                    showTitle: true,
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

## Poster

You can add media poster for each file in source object with **posterUrl**. This will be shown in play list thumbnail and in player for Audio files. You can show/hide the poster by setting **showPoster** property, it is true by default.


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
                    showPoster: true,
                    source: [
                        {
                        "url": "https://www.youtube.com/watch?v=7_hR16f7Drw",
                        "title": "Xamarin",
                        "author": "syncfusion
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



