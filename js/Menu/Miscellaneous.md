---
layout: post
title: Miscellaneous | Syncfusion | Menu
description: miscellaneous
platform: js
control: Menu
documentation: ug
api: /api/js/ejmenu
---

# Miscellaneous

## Height

Specifies the height of the root menu. You can customize the height of the **Menu** control by using [height](https://help.syncfusion.com/api/js/ejmenu#members:height) property. 

You can specify the height of the **Menu** control in the script as follows.


{% highlight javascript %}


    jQuery(function($) {
        $("#menu").ejMenu({
            height: 50
        });
    });


{% endhighlight %}

## Width

Specifies the width of the main menu. You can customize the width of the **Menu** control by using [width](https://help.syncfusion.com/api/js/ejmenu#members:width) property.

You can specify the width of the **Menu** control in the script as follows.

{% highlight javascript %}


    jQuery(function($) {
        $("#menu").ejMenu({
            width: 700
        });
    });


{% endhighlight %}

## Open on click

Specifies the sub menu items to be show or open only on click. It accepts the Boolean value. Its default value is false. If we set [openOnClick](https://help.syncfusion.com/api/js/ejmenu#members:openonclick) property to true then the submenu items will open only on click. By default the submenu will open when we hover on menu items.

Add the following **&lt;script&gt;** in the above code sample. 



{% highlight javascript %}



    jQuery(function($) {
        $("#menu").ejMenu({
            width: 612,
            openOnClick: true
        });
    });



{% endhighlight %}



Output screenshot for the above code example is as follows.

![menu](Miscellaneous_images/Miscellaneous_img1.png)


## Animation

[AnimationType](https://help.syncfusion.com/api/js/ejmenu#members:animationtype) is used to enable or disable the Animation when hover or click on menu items. Its value type is string. It accepts two values such as “none” and “default”. Support to disable the **AnimationType** when hover or click on menu items is none. Support to enable the Animation Type when hover or click on menu items is default. 

Add the following **&lt;script&gt;** in the above sample code. 

N> For animation, [enableAnimation](https://help.syncfusion.com/api/js/ejmenu#members:enableanimation) set to true

{% highlight javascript %}


    jQuery(function ($) {
        $("#menu").ejMenu({
            width: 612,
            animationType: ej.AnimationType.Default
        });
    });



{% endhighlight %}


Output screenshot for the above code sample is as follows.

![animation](Miscellaneous_images/Miscellaneous_img2.png)


## Title text

Specifies the title to the responsive menu. You can provide title to the **Menu** control by using [titleText](https://help.syncfusion.com/api/js/ejmenu#members:titletext) property. 

You can specify the title of the **Menu** control in the script as follows.



{% highlight javascript %}


    jQuery(function ($) {
        $("#menu").ejMenu({
            titleText: "Title of the Menu"
        });
    });



{% endhighlight %}



The following screenshot displays the output of the above code.

![title](Miscellaneous_images/Miscellaneous_img3.png)


## Show root level arrows

Specifies the main menu item arrows to display only when it contains child menu items. You can use [showRootLevelArrows](https://help.syncfusion.com/api/js/ejmenu#members:showRootLevelArrows) property to display the arrows of main menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

Add the following **&lt;script&gt;** in the above code sample.



{% highlight javascript %}



        jQuery(function($) {
            $("#menu").ejMenu({
                width: 500,
                showRootLevelArrows: false
            });
        });



{% endhighlight %}



The following screenshot displays the output of the above code.

![arrows](Miscellaneous_images/Miscellaneous_img4.png)


## Show sub level arrows

Specifies the sub menu items arrows to display only when it contains child menu items. You can use [showSubLevelArrows](https://help.syncfusion.com/api/js/ejmenu#members:showsublevelarrows) property to show the arrows of sub menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

Add the following **&lt;script&gt;** in the sample code.



{% highlight javascript %}


        jQuery(function($) {
            $("#menu").ejMenu({
                width: 500,
                showSubLevelArrows: false
            });
        });



{% endhighlight %}



The following screenshot displays the output of the above code.

![sublevel](Miscellaneous_images/Miscellaneous_img5.png)

## Show context menu on button click

Context menu can be opened through button click using `show` method of Menu. Invoke the show method in the button click handler and pass the target element as well as its position by calculating the X position based on window width and element width as a parameter to display the context menu.

Add the following **&lt;script&gt;** in the sample code.

{% highlight javascript %}

       $("#target").on("click", function(e){ 
           var instance =  $("#context").data("ejMenu"); 
           var locationX = (e.clientX + instance.element.width() < $(window).width()) ? e.pageX : e.pageX - instance.element.width(); 
           instance.show(locationX,e.clientY,e.currentTarget,e); 
       }); 


{% endhighlight %}

Refer [here](https://jsplayground.syncfusion.com/3vz0pyvz) for sample.