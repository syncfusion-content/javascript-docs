---
layout: post
title: Orientation
description: orientation
platform: js
control: Rating
documentation: ug
api: /api/js/ejrating
---

# Orientation

**Rating** provides support for **vertical** orientation. By default Rating renders with **horizontal** orientation. You can the change the orientation by the [orientation](https://help.syncfusion.com/api/js/ejrating#members:orientation) property.

The following code example is used to render the Rating control with **vertical** **orientation**.

 Add the following HTML to render Rating with customized orientation.

{% highlight html %}

<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
    <table>
        <tr>
            <td valign="top">Rating:
               </td>
               <td>
                   <input id="rating" type="text" />
               </td>
           </tr>
      </table>
 </div>
    
 {% endhighlight %}

{% highlight javascript %}

      // Add the following script to render Rating with customized orientation.
    
      $("#rating").ejRating({ orientation: "vertical" });
  
{% endhighlight %}

The following screenshot illustrates the **Rating** with **vertical orientation**.

![](/js/Rating/Orientation_images/Orientation_img1.png) 

