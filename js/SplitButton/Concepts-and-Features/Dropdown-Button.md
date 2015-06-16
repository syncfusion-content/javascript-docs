---
layout: post
title: Dropdown-Button
description: dropdown button
platform: js
control: Split Button
documentation: ug
---

# Dropdown Button

You can change the **Split Button** as **Dropdown Button** that consists of a single button that when clicked displays a drop-down list of mutually exclusive items. You can achieve this by using default functionality of **Split Button** with **buttonMode** as **ej.ButtonMode.Dropdown**. Initially the **targetID** is a mandatory one.

The following steps explain how to change the **Split Button** as **Dropdown Button.**

1. In the **HTML** page, add the following button elements to configure **Button** widget.

{% highlight html %}

<button id="dropdownbtn">login</button>
<ul id="menu">
    <li><span>User</span></li>
    <li><span>Guest</span></li>
    <li><span>Admin</span></li>
</ul>
{% endhighlight %}

{% highlight js %}

// Initialize the control in JavaScript

<script type="text/javascript">
    $(function () {
        $("#dropdownbtn").ejSplitButton({
            size: "medium",
            showRoundedCorner: true,
            buttonMode: ej.ButtonMode.Dropdown,
            targetID: "menu"
        });
    });
</script>


{% endhighlight %}



2. Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Dropdown-Button_images/Dropdown-Button_img1.png" Caption="Dropdown Button with content"%}

