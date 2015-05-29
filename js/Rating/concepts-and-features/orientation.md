---
layout: post
title: orientation
description: orientation
platform: js
control: Rating
documentation: ug
---

# Orientation

**Rating** provides support for **vertical** orientation. By default **Rating** renders with **horizontal** orientation. You can the change the orientation by the ‘**orientation**’ property.

The following code example is used to render the **Rating** control with **vertical****orientation**.

* Add the following **HTML** to render **Rating** with **customized****orientation**.



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

**[JS]**
**// Add the following script to render Rating with customized orientation.**

<script type="text/javascript">
     $("#rating").ejRating({ orientation: "vertical" });
   </script>


{% endhighlight %}



[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Rating with customized orientation.



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").Orientation(Orientation.Vertical)

            &lt;/td&gt;

        &lt;/tr&gt;             

    &lt;/table&gt;

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Rating with customized orientation.



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

            &lt;table&gt;

                &lt;tr&gt;

                    <td valign="top">Rating:

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:Rating ID="Rating1" Orientation="Vertical" runat="server"&gt;&lt;/ej:Rating&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/table&gt;

        &lt;/div&gt;





The following screenshot illustrates the **Rating** with **vertical orientation**.



{% include image.html url="\js\Rating\concepts-and-features\orientation_images\orientation_img1.png" Caption="Figure 2618: Rating with vertical orientation"%}









