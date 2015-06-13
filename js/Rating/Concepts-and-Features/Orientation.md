---
layout: post
title: Orientation
description: orientation
platform: js
control: Rating
documentation: ug
---

# Orientation

**Rating** provides support for **vertical** orientation. By default **Rating** renders with **horizontal** orientation. You can the change the orientation by the ‘**orientation**’ property.

The following code example is used to render the **Rating** control with **vertical** **orientation**.

1. Add the following HTML to render Rating with customized orientation.

{% highlight html %}

**[HTML]**
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

[JS]
// Add the following script to render Rating with customized orientation.

<script type="text/javascript">
     $("#rating").ejRating({ orientation: "vertical" });
   </script>


{% endhighlight %}



The following screenshot illustrates the **Rating** with **vertical orientation**.

{% include image.html url="/js/Rating/Concepts-and-Features/Orientation_images/Orientation_img1.png" Caption="Rating with vertical orientation"%}

