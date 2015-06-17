---
layout: post
title: Multiple-Selection
description: multiple selection
platform: js
control: ListBox
documentation: ug
---

# Multiple Selection

**Allow multiple selection**

**ListBox** widget allows you to select multiple values from the list Items using **allowMultiSelection** property. You can select multiple list items along with Control key and Shift key press. To select multiple values we need to set **allowMultiSelection** value to **true**.

**Configuring multiple selection**

The following steps explain you the configuration of the **allowMultiSelection** for a **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}


<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


// Configure allowMultiSelection option for ListBox control as follows
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
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, allowMultiSelection: true
        });
    });
</script>

{% endhighlight %}

Output for **ListBox** control that provides multiple selection is as follows.


{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img1.png" Caption="Figure 14: ListBox with Multiple Selection"%}

**Multiple selection through index** 

You can select the list of items from the **ListBox** using **selectedItemlist** property. Its data type is array. To achieve this, you need to set true to **allowMultiSelection** property in **ListBox**. 

The following steps explains you the configuration of **selectedItemlist** property in **ListBox**

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget

{% highlight html %}


<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>


{% endhighlight %}

{% highlight js %}


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
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, selectedItemlist: [0, 3], allowMultiSelection: true
        });
    });
</script>

{% endhighlight %}

Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img2.png" Caption="Figure 15: ListBox with selectedItemlist property"%}

**Checkbox Support**

**Show Checkbox** 

You can enable the checkbox in the **ListBox** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its **ListBox** client side events.  

**Defining the Checkbox support**

The following steps explains you the configuration of checkbox options in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}


<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


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
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, showCheckbox: true
        });
    });
</script>

{% endhighlight %}

Output of the above steps.



{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img3.png" Caption="Figure 16: ListBox with checkbox "%}

**Check All** 

You can check all the check box in the list by using this property. The data type of **checkAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

The following steps explains you the configuration of checkbox options in **ListBox.**

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}


<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


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
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, showCheckbox: true,
            checkAll: true
        });
    });
</script>

{% endhighlight %}


Output of the above steps.



{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img4.png" Caption="Figure 17: ListBox with checkbox property"%}

**Uncheck All**

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

