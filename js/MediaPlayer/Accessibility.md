---
layout: post
title: Accessibility with MediaPlayer
description: To get start with MediaPlayer by adding references.
platform: js
control: MediaPlayer
documentation: ug
api: /api/js/ejmediaplayer
---


## Keyboard Support

You can enable/disable keyboard short cuts by **disableKeys** property. It is false by default.

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
                   disableKeys: true,
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


### Keyboard shortcuts

The keyboard shortcuts for Media Player are as follows.

<table>
<tr>
<th>
File </th><th>
Description / Usage </th></tr>
<tr>
<td>
Play/Pause<br/><br/></td><td>
Space – Toggle play/pause function<br/><br/></td></tr>
<tr>
<td>
Forward <br/><br/></td><td>
Right arrow – Forward the media 3s from current time<br/><br/>
Alt + Right arrow – Forward the media 10s from current time<br/><br/>
Ctrl + Right arrow – Forward the media 60s from current time</td>
</tr>
<tr>
<td>
Rewind <br/><br/></td><td>
Left arrow – Rewind the media 3s from current time<br/><br/>
Alt + Left arrow – Rewind the media 10s from current time<br/><br/>
Ctrl + Left arrow – Rewind the media 60s from current time</td>
</tr>
<tr>
<td>
Play/Pause<br/><br/></td><td>
Mute/UnMute<br/><br/></td></tr>
<tr>
<td>
Volume<br/><br/></td><td>
Up arrow – increase the volume 1 from current volume<br/><br/>
Down arrow – decrease the volume 1 from current volume<br/><br/>
</tr>
<tr>
<td>
F11 <br/><br/></td><td>
Enable Full screen<br/><br/></td></tr>
<tr>
<td>
Esc<br/><br/></td><td>
Exit Full screen<br/><br/></td></tr>

</table>

