---
layout: post
title: Arrow-Position
description: arrow position
platform: js
control: Split Button
documentation: ug
---

# Arrow Position

To provide a good look and feel for **Split Button**, position of arrow in **Split Button** is important. Using **arrowPosition** property, you can easily customize the position of arrow inside **Split Button** without using any complex CSS. **arrowPosition** property is applicable for both **Split Button** and **Dropdown Button**. This property represent the position of arrow with menu content.

_List of arrow position_

<table>
<tr>
<td>
<b>left</b></td><td>
Support for arrow in left.</td></tr>
<tr>
<td>
<b>right</b></td><td>
Support for arrow in right. </td></tr>
<tr>
<td>
<b>top</b></td><td>
Support for arrow in top. </td></tr>
<tr>
<td>
<b>bottom</b></td><td>
Support for arrow in bottom.</td></tr>
</table>


The following steps explain you the details on rendering the **Split Button** with above mentioned arrow position options.

1. In the **HTML** page, add the following button elements to configure **Split Button** widget.

{% highlight html %}

**[HTML]**
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

{% highlight js %}

**[JavaScript]**

 // Initialize the control in JavaScript
<script type="text/javascript">
    $(function () {
        $("#spltbutton11").ejSplitButton({
            size: "large",
            showRoundedCorner: true,
            contentType: "imageonly",
            targetID: "Ul11",
            prefixIcon: "e-uiLight e-login",
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
</script>

{% endhighlight %}



2. Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Arrow-Position_images/Arrow-Position_img1.png" Caption=""%}

_Split button with arrowPosition_

