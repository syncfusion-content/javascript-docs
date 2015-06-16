---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: Menu
documentation: ug
---

# Miscellaneous

##Height

Specifies the height of the root menu. You can customize the height of the **Menu** control by using height property. 

* You can specify the height of the **Menu** control in the script as follows.


{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
**height: 50**
        });
    });
</script>


{% endhighlight %}

##Width

Specifies the width of the main menu. You can customize the width of the **Menu** control by using width property.

* You can specify the width of the **Menu** control in the script as follows.

{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 700
        });
    });
</script>


{% endhighlight %}

##Open on click

Specifies the sub menu items to be show or open only on click. It accepts the Boolean value. Its default value is false. If we set “**openOnClick**” property to true then the submenu items will open only on click. By default the submenu will open when we hover on menu items.

* Add the following **&lt;script&gt;** in the above code sample. 



{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 612,
**openOnClick: true**
        });
    });
</script>


{% endhighlight %}



Output screenshot for the above code example is as follows.

{% include image.html url="/js/Menu/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img1.png" Caption=""%}

_Figure_ _41__: Sub menu items to open on click_

##Animation

**AnimationType** is used to enable or disable the Animation when hover or click on menu items. Its value type is string. It accepts two values such as “none” and “default”. Support to disable the **AnimationType** when hover or click on menu items is none. Support to enable the Animation Type when hover or click on menu items is default. 

* Add the following **&lt;script&gt;** in the above sample code. 



{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            width: 612,
**animationType: ej.AnimationType.Default**
        });
    });
</script>


{% endhighlight %}


Output screenshot for the above code sample is as follows.

{% include image.html url="/js/Menu/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img2.png" Caption=""%}

_Figure 27: Animation_

##Title text

Specifies the title to the responsive menu. You can provide title to the **Menu** control by using **titleText** property. 

* You can specify the title of the **Menu** control in the script as follows.



{% highlight js %}


<script type="text/javascript">
    jQuery(function ($) {
        $("#menucontrol").ejMenu({
            titleText: "Title of the Menu"
        });
    });
</script>


{% endhighlight %}



The following screenshot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img3.png" Caption=""%}

_Figure 28: Title text for Responsive Layout_

##Show root level arrows

Specifies the main menu item arrows to display only when it contains child menu items. You can use “**showRooltLevelArrows**” property to display the arrows of main menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

* Add the following **&lt;script&gt;** in the above code sample.



{% highlight js %}


<script type="text/javascript">
        jQuery(function ($) {
            $("#menucontrol").ejMenu({
                width: 500,
                showRooltLevelArrows: false
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img4.png" Caption=""%}

_Figure 29: Show root level arrows_

##Show sub level arrows

Specifies the sub menu items arrows to display only when it contains child menu items. You can use “**showSubLevelArrows**” property to show the arrows of sub menu items only when it contains child menu items. This property accepts Boolean value. Its default value is true. 

* Add the following **&lt;script&gt;** in the sample code.



{% highlight js %}


<script type="text/javascript">
        jQuery(function ($) {
            $("#menucontrol").ejMenu({
                width: 500,
                showSubLevelArrows: false
            });
        });
    </script>


{% endhighlight %}



The following screenshot displays the output of the above code.

{% include image.html url="/js/Menu/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img5.png" Caption=""%}

_Figure 30: Show sub level arrows_

