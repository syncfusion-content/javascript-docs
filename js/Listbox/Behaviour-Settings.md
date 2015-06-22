---
layout: post
title: Behaviour-Settings
description: behaviour settings
platform: js
control: ListBox
documentation: ug
---

# Behaviour Settings

The following are some miscellaneous properties that helps you to change the behaviour of **ListBox** control.

**Target ID**

You can append a list with **ListBox** by using **targetId** property. Define a **&lt;ul&gt;**, **&lt; li&gt;** tag that you want to display on **ListBox** and then set the id of parent **&lt;ul&gt;** tag to **targetId** property. And its data type is string. 

The following steps explains you the configuration of **targetID** property in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

    <div id="control">
        <h5 class="ctrllabel">Select a font style</h5>
        <ul id="listboxSample"></ul>
    
        <ul id="targetlist">
            <li>Algerian</li>
            <li>ARIAL</li>
            <li>Bimini</li>
            <li>Courier</li>
            <li>Cursive</li>
            <li>Fantasy</li>
            <li>Georgia</li>
            <li>Impact</li>
            <li>New york</li>
            <li>Sans-Serif</li>
            <li>Scripts</li>
            <li>Times</li>
            <li>Times New Roman</li>
            <li>Verdana</li>
            <li>Western</li>
            <li>Zapfellipt bt</li>
        </ul>
    </div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        $('#listboxSample').ejListBox({ targetID: "targetlist" });
    });

{% endhighlight %}


Output of the above steps.

{% include image.html url="/js/ListBox/Behaviour-Settings_images/Behaviour-Settings_img1.png" Caption="ListBox with target id property"%}

**Select the value by index** 

**ListBox** widget provides you support to select an item by mentioning the index of the item. The **selectedItemIndex** property helps you to select the particular item from the list. Its date type is number. 

The following steps explains you the configuration of **selectedItemIndex** property in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}


    <div id="control">
        <h5 class="ctrllabel">Select a skill</h5>
        <ul id="listboxsample"></ul>
    </div>

 
{% endhighlight %}

{% highlight js %}


    $(function () {
        // JSON data declaration
        var skillset = [
        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        //Render ListBox by mapping fields with JSON data
        $("#listboxsample").ejListBox({
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, selectedItemIndex: 2
        });
    });


{% endhighlight %}

Output of the above steps.

{% include image.html url="/js/ListBox/Behaviour-Settings_images/Behaviour-Settings_img2.png" Caption="ListBox with selectedItemIndex property"%}

**Enable or Disable the ListBox Widget**

This features enables you to set the enable or disable options for **ListBox** by setting Boolean type value to **enabled** property. 

The following steps explains you the configuration of **enabled** property in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

    <div id="control">
        <h5 class="ctrllabel">Select a skill</h5>
        <ul id="listboxSample"></ul>
    </div>

{% endhighlight %}

{% highlight js %}

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
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, enabled: false
        });
    });

{% endhighlight %}


Output of the above steps.

{% include image.html url="/js/ListBox/Behaviour-Settings_images/Behaviour-Settings_img3.png" Caption="ListBox with disabled"%}

