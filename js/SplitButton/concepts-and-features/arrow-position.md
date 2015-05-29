---
layout: post
title: arrow-position
description: arrow position
platform: js
control: Split Button
documentation: ug
---

# Arrow Position

To provide a good look and feel for **Split Button**, position of arrow in **Split Button** is important. Using **arrowPosition** property, you can easily customize the position of arrow inside **Split Button** without using any complex CSS. **arrowPosition** property is applicable for both **Split Button** and **Dropdown Button**. This property represent the position of arrow with menu content.

_Table_ _3__: List of arrow position_

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

* In the **HTML** page, add the following button elements to configure **Split Button** widget.



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
[JavaScript] // Initialize the control in JavaScript
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



**[CSHTML]**

@Html.EJ().SplitButton("spltbutton11").Text("login").ShowRoundedCorner(true).Size(ButtonSize.Large).ContentType(ContentType.ImageOnly).TargetID("Ul11").PrefixIcon("e-uiLight e-login").ArrowPosition(ArrowPosition.Left)

&lt;ul id="Ul11"&gt;

    &lt;li&gt;<span>User</span>&lt;/li&gt;

    &lt;li&gt;<span>Guest</span>&lt;/li&gt;

    &lt;li&gt;<span>Admin</span>&lt;/li&gt;

&lt;/ul&gt;

@Html.EJ().SplitButton("spltbutton21").Text("login").ShowRoundedCorner(true).Size(ButtonSize.Mini).ContentType(ContentType.TextOnly).TargetID("Ul21").ArrowPosition(ArrowPosition.Top)

&lt;ul id="Ul21"&gt;

    &lt;li&gt;<span>User</span>&lt;/li&gt;

    &lt;li&gt;<span>Guest</span>&lt;/li&gt;

    &lt;li&gt;<span>Admin</span>&lt;/li&gt;

&lt;/ul&gt;

@Html.EJ().SplitButton("spltbutton31").Text("login").ShowRoundedCorner(true).Size(ButtonSize.Small).ContentType(ContentType.TextOnly).TargetID("Ul31").ArrowPosition(ArrowPosition.Bottom)

&lt;ul id="Ul31"&gt;

    &lt;li&gt;<span>User</span>&lt;/li&gt;

    &lt;li&gt;<span>Guest</span>&lt;/li&gt;

    &lt;li&gt;<span>Admin</span>&lt;/li&gt;

&lt;/ul&gt;

@Html.EJ().SplitButton("spltbutton41").Text("login").ShowRoundedCorner(true).Size(ButtonSize.Medium).ContentType(ContentType.TextOnly).TargetID("Ul41").ArrowPosition(ArrowPosition.Right)

&lt;ul id="Ul41"&gt;

    &lt;li&gt;<span>User</span>&lt;/li&gt;

    &lt;li&gt;<span>Guest</span>&lt;/li&gt;

    &lt;li&gt;<span>Admin</span>&lt;/li&gt;

&lt;/ul&gt;



**[aspx]**

&lt;ej:SplitButton ID="spltbutton11" runat="server" Text="login" Size="Large" ShowRoundedCorner="true" ContentType="ImageOnly" ArrowPosition="Left" PrefixIcon="e-uiLight e-login"&gt;

    &lt;Items&gt;

        &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

    &lt;/Items&gt;

&lt;/ej:SplitButton&gt;

&lt;ej:SplitButton ID="spltbutton21" runat="server" Text="login" Size="Mini" ShowRoundedCorner="true" ContentType="TextOnly" ArrowPosition="Top"&gt;

    &lt;Items&gt;

        &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

    &lt;/Items&gt;

&lt;/ej:SplitButton&gt;

&lt;ej:SplitButton ID="spltbutton31" runat="server" Text="login" Size="Small" ShowRoundedCorner="true" ContentType="TextOnly" ArrowPosition="Bottom"&gt;

    &lt;Items&gt;

        &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

    &lt;/Items&gt;

&lt;/ej:SplitButton&gt;

&lt;ej:SplitButton ID="spltbutton41" runat="server" Text="login" Size="Medium" ShowRoundedCorner="true" ContentType="TextOnly" ArrowPosition="Right"&gt;

    &lt;Items&gt;

        &lt;ej:SplitItem Text="User"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Guest"&gt;&lt;/ej:SplitItem&gt;

        &lt;ej:SplitItem Text="Admin"&gt;&lt;/ej:SplitItem&gt;

    &lt;/Items&gt;

&lt;/ej:SplitButton&gt;



Execute the above code to render the following output.



{% include image.html url="\js\SplitButton\concepts-and-features\arrow-position_images\arrow-position_img1.png" Caption="Figure 129: Split button with arrowPosition"%}

