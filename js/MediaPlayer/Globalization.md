---
layout: post
title: Globalization with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---

## Look and Feel

Essential JavaScript controls feature 12 built-in themes, six flat and gradient effects, and supports custom skin options for user-defined themes.

16 themes support available for Media Player control namely,

* default-theme
* flat-azure-dark
* flat-lime
* flat-lime-dark
* flat-saffron
* flat-saffron-dark
* gradient-azure
* gradient-azure-dark
* gradient-lime
* gradient-lime-dark
* gradient-saffron
* gradient-saffron-dark
* high-contrast-01
* high-contrast-02
* material
* office-365

You Need to add this Css reference to apply the built in themes. 
Example:

{% highlight html %}

<link rel="stylesheet" href="css/content/themes/ flat-lime-dark/ej.web.all.min.css">

{% endhighlight %}

**Media Player** control also customizes its appearance using user-defined CSS and custom skin options (colors and backgrounds). To apply custom themes you can use the **cssClass** property. **cssClass** property sets the root class for Media Player control theme.


{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
      <title>Essential Studio for JavaScript : Media Player</title>
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
                    locale: "en-US",
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

## Localization

You can set the language for Media Player control with **locale** property. You can define your own set of display and hover text content with “ej.MediaPlayer.Locale” or you can also set the language code in model.

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
                    locale: "en-US",
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
