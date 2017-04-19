---
layout: post
title: Getting-Started
description: getting started
platform: js
control: Tile
documentation: ug
api: /api/js/ejtile
---

# Getting Started

The **Essential Studio JavaScript Tiles** are simple, opaque rectangles or squares that are arrayed on the Start screen in a grid-like pattern and it can be either static or live. Tapping or selecting a **Tile** launches the app or other experience that is represented by the **Tile**.                                               

![](/js/Tile/Getting-Started_images/Getting-Started_img1.png)

## Create Tile Widget

The following steps guide you to add group of **Tiles** for creating a home page that displays all the available applications.

Create an HTML file and paste the following template for web layout.

{% highlight html %}

    <!DOCTYPE html>
    <html>
    <head>
        <!-- style sheet for default theme(flat azure) -->
        <link href="[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css)" rel="stylesheet" />
        <!--scripts-->
        <script src="[http://code.jquery.com/jquery-1.10.2.min.js](http://code.jquery.com/jquery-1.10.2.min.js)"></script>
        <script src="[http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js](http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js)"></script>
        <script src="[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js)"> </script>
    </head>
    <body>
        <!— Adding Tile Control here -->
    </body>

{% endhighlight %}



Create a div element that acts as a container for Tile control. Initialize ejTile as in the following code example and specify the tile text, size and image URL.



{% highlight html %}

    <div id="tile1"></div>

{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}
 
    $(function ()
    {
     $("#tile1").ejTile({ text: "Map", tileSize: "medium", imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/map.png' });
    });
 
{% endhighlight %}

Run the above code to render the following output. 

![](/js/Tile/Getting-Started_images/Getting-Started_img2.png)

In this scenario, a home page is designed using tile for easy navigation. Therefore, you require many different sizes of tiles aligned in a grid-like manner. To align the tiles automatically, define the necessary tile elements inside the wrapper element that contains a ‘**column’** class. You can define all columns elements under the wrapper element with ‘**group’** class to make ‘n’ number of tiles as a grouped tile.

Refer to the following code example.



{% highlight html %}
    
    <div id="tile" style="margin-top: 45px;">
                <div class="e-tile-group">
                    <div class="e-tile-column">
                    <div id="tile1" ></div>
                    <div class="e-tile-small-col-2">
                        <div id="tile2" >
                        </div>
                        <div id="tile3" >
                        </div>
                        <div id="tile4">
                        </div>
                        <div id="tile5" >
                        </div>
                    </div>
                    <div id="tile6">
                    </div>
                    <div id="tile7" >
                    </div>
                </div>
                <div class="e-tile-column">
                    <div id="tile8" >
                    </div>
                    <div id="tile9">
                    </div>
                    <div id="tile10">
                    </div>
                </div>
            </div>
        </div>
{% endhighlight %}

Add the following code inside the **script** tag.

{% highlight javascript %}

        $(function () {
            $("#tile1").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/people_1.png', imagePosition: "fill", tileSize: "medium", text: "People" });
            $("#tile2").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/alerts.png'});
            $("#tile3").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/bing.png'});
            $("#tile4").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/camera.png'});
            $("#tile5").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/messages.png'});
            $("#tile6").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/games.png', tileSize: "medium", text: "Play" });
            $("#tile7").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/map.png', tileSize: "medium", text: "Maps" });
            $("#tile8").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/people_2.png', imagePosition: "fill", tileSize: "medium", text: "People" });
            $("#tile9").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/pictures.png', tileSize: "medium", text: "Photo" });
            $("#tile10").ejTile({ imageUrl: 'http://js.syncfusion.com/ug/web/content/tile/weather.png',  tileSize: "wide", text: "Weather" });
        });
 
{% endhighlight %}



Run the above code to render the following output.

![](/js/Tile/Getting-Started_images/Getting-Started_img3.png)

