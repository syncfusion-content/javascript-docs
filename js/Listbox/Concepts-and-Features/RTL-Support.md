---
layout: post
title: RTL-Support
description: rtl support
platform: js
control: ListBox
documentation: ug
---

# RTL Support

This feature supports to change the left-to-right alignment of the **ListBox** widget to right-to-left (**RTL**). 

**Defining the RTL property**

The following steps explains you the configuration of **enableRTL** properties in **ListBox.**

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
            fields: { text: "skill" }, enableRTL: true
        });
    });
</script>

{% endhighlight %}

Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 28: ListBox with RTL"%}

