---
layout: post
title: dropdown-button
description: dropdown button
platform: js
control: Split Button
documentation: ug
---

# Dropdown Button

You can change the **Split Button** as **Dropdown Button** that consists of a single button that when clicked displays a drop-down list of mutually exclusive items. You can achieve this by using default functionality of **Split Button** with **buttonMode** as **ej.ButtonMode.Dropdown**. Initially the **targetID** is a mandatory one.

The following steps explain how to change the **Split Button** as **Dropdown Button.**

* In the **HTML** page, add the following button elements to configure **Button** widget.



{% highlight html %}

**[HTML]**
<button id="dropdownbtn">login</button>
<ul id="menu">
    <li><span>User</span></li>
    <li><span>Guest</span></li>
    <li><span>Admin</span></li>
</ul>

**[JavaScript]**
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



**[CSHTML]** @Html.EJ().SplitButton("dropdownbtn").Text("login").ShowRoundedCorner(true).Size(ButtonSize.Medium).ContentType(ContentType.TextOnly).TargetID("menu").ButtonMode(ButtonMode.Dropdown)

&lt;ul id="menu"&gt;

    &lt;li&gt;<span>User</span>&lt;/li&gt;

    &lt;li&gt;<span>Guest</span>&lt;/li&gt;

    &lt;li&gt;<span>Admin</span>&lt;/li&gt;

&lt;/ul&gt;



**[aspx]**

&lt;ej:SplitButton ID="dropdownbtn" runat="server" Text="login" Size="Medium" ShowRoundedCorner="true" ContentType="TextOnly" ButtonMode="Dropdown"&gt;

    &lt;Items&gt;

        &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

    &lt;/Items&gt;

&lt;/ej:SplitButton&gt;



Execute the above code to render the following output.



{% include image.html url="\js\SplitButton\concepts-and-features\dropdown-button_images\dropdown-button_img1.png" Caption="Figure 118: Dropdown Button with content"%}

