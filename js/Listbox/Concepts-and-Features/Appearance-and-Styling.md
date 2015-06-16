---
layout: post
title: Appearance-and-Styling
description: appearance and styling
platform: js
control: ListBox
documentation: ug
---

# Appearance and Styling

**Adjusting ListBox size**

**Width**

**ListBox** widget provides you support to customize the dimensions of the **ListBox**. By using **width** property you can set the width of the **ListBox**. Its data type is string.

**Height**

**ListBox** widget provides you support to customize the dimensions of the **ListBox**. By using **height** property, you can set the height of the **ListBox**. Its data type is string.

**Defining the ListBox size properties**

The following steps explains you the configuration of **height** & **width** properties in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

**[HTML]**

<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Initialize the control in JavaScript 
<script type="text/javascript">
    $(function () {
        // JSON data declaration
        var skillset = [
        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        //Render ListBox by mapping fields with JSON data
        $("#listboxSample").ejListBox({
            width: "240", height: "302", dataSource: skillset,
            fields: { text: "skill" }
        });
    });
</script>

{% endhighlight %}

Output of the above steps


{% include image.html url="/js/Listbox/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Figure 18: ListBox with specified width and height"%}

**Enabling Rounded corner**

**ListBox** widget provides you support to change the appearance of **ListBox**. By using **showRoundedCorner** you can create a rounded corner on the **ListBox**. Its data type is Boolean.

The following steps explains you the configuration of Rounded corner of the **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}

**[HTML]**

<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

**[JavaScript]**

// Initialize the control in JavaScript
<script type="text/javascript">
    $(function () {
        var skillset = [
        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        $("#listboxSample").ejListBox({
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, showRoundedCorner: true
        });
    });
</script>

{% endhighlight %}
Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Figure 19: ListBox with Rounded corner"%}

