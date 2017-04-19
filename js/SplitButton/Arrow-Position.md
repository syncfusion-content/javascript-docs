---
layout: post
title: Arrow-Position
description: arrow position
platform: js
control: Split Button
documentation: ug
api: /api/js/ejsplitbutton
---

# Arrow Position

To provide a good look and feel for **Split Button**, position of arrow in **Split Button** is important. Using **arrowPosition** property, you can easily customize the position of arrow inside **Split Button** without using any complex CSS. **arrowPosition** property is applicable for both **Split Button** and **Dropdown Button**. This property represent the position of arrow with menu content.

List of arrow position

<table><tr>
<th>
Arrow Position</th><th>Description</th></tr>
<tr>
<td>
left</td><td>
Support for arrow in left.</td></tr>
<tr>
<td>
right</td><td>
Support for arrow in right. </td></tr>
<tr>
<td>
top</td><td>
Support for arrow in top. </td></tr>
<tr>
<td>
bottom</td><td>
Support for arrow in bottom.</td></tr>
</table>


The following steps explain you the details on rendering the **Split Button** with above mentioned arrow position options.

In the **HTML** page, add the following button elements to configure **Split Button** widget.

{% highlight html %}

<div class="control">
    <button id="spltbutton11">login</button>
    <ul id="Ul11">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
    <button id="spltbutton21">login</button>
    <ul id="Ul21">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
    <button id="spltbutton31">login</button>
    <ul id="Ul31">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
    <button id="spltbutton41">login</button>
    <ul id="Ul41">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Initialize the control in JavaScript
    $(function () {
        $("#spltbutton11").ejSplitButton({
            size: "large",
            showRoundedCorner: true,
            contentType: "imageonly",
            targetID: "Ul11",
            prefixIcon: "e-icon e-login",
            arrowPosition: "left"
        });
        $("#spltbutton21").ejSplitButton({
            size: "mini",
            showRoundedCorner: true,
            targetID: "Ul21",
            arrowPosition: "top"
        });
        $("#spltbutton31").ejSplitButton({
            size: "small",
            showRoundedCorner: true,
            targetID: "Ul31",
            arrowPosition: "bottom"
        });
        $("#spltbutton41").ejSplitButton({
            size: "medium",
            showRoundedCorner: true,
            targetID: "Ul41",
            arrowPosition: "right"
        });
    });


{% endhighlight %}

{% highlight css %}
<style>
    .e-split {
        float: left;
        padding-left: 65px;
    }
</style>

{% endhighlight %}

Execute the above code to render the following output.

![](/js/SplitButton/Arrow-Position_images/Arrow-Position_img1.png) 



