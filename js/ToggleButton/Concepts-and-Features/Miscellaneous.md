---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: Toggle Button
documentation: ug
---

# Miscellaneous

## Show Rounded Corner 

It sets the corner of **Toggle Button** in rounded shape. The **Toggle Button**, by default doesn’t have rounded corner. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Toggle Button** with Rounded corner support. 

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.

{% highlight html %}


   <input type="checkbox" id="toggle_roundedCorenr" />  

{% endhighlight %}

{% highlight html %}



//Initialize the control in JavaScript

   <script type="text/javascript">
        $(function () {
            $("#toggle_roundedCorenr").ejToggleButton({
                size: "small",
                contentType: "textandimage",
                //used to specify the rounded corner for toggle button
                showRoundedCorner: true,
                defaultText: "Play",
                activeText: "Next",
                defaultPrefixIcon: "e-mediaplay e-uiLight",
                activePrefixIcon: "e-mediapause e-uiLight"
            });
        });
    </script>

{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="/js/ToggleButton/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img1.png" Caption=""%}

_Figure 13: Toggle button with Rounder corner_

**Prevent Toggle**

This property is used to prevent the state change of **Toggle Button** when it is clicked. When you set **preventToggle** **property** as true, then the state of the **Toggle Button** is not changed even though it is clicked.

The following steps explains you the details about rendering the **Toggle Button** with **preventToggle** property enabled.

* In the **HTML** page, add the following button elements to configure **Toggle Button** widget.


{% highlight html %}


   <input type="checkbox" id="toggle_prevent" />

{% endhighlight %}

{% highlight html %}



//Initialize the control in JavaScript

   <script type="text/javascript">
        $(function () {
            $("#toggle_prevent").ejToggleButton({
                size: "small",
                contentType: "textandimage",
                defaultText: "Play",
                activeText: "Next",
                defaultPrefixIcon: "e-mediaplay e-uiLight",
                activePrefixIcon: "e-mediapause e-uiLight",
                //prevent changing state of toggle button
                preventToggle: true
            });
        });
    </script>


{% endhighlight %}


Execute the above code to render the following output.



{% include image.html url="/js/ToggleButton/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img2.png" Caption=""%}

_Figure 14: Toggle button with prevent_Toggle.

