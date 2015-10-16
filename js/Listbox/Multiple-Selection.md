---
layout: post
title: Multiple-Selection
description: multiple selection
platform: js
control: ListBox
documentation: ug
---

# Multiple Selection

## Allow multiple selection

**ListBox** widget allows you to select multiple values from the list Items using **allowMultiSelection** property. You can select multiple list items along with Control key and Shift key press. To select multiple values we need to set **allowMultiSelection** value to **true**.

### Configuring multiple selection

The following steps explain you the configuration of the **allowMultiSelection** for a **ListBox**.

In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       // JSON data declaration
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       //Render ListBox by mapping fields with JSON data
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          allowMultiSelection: true
       });
    });

{% endhighlight %}


Output for **ListBox** control that provides multiple selection is as follows.

![](/js/ListBox/Multiple-Selection_images/Multiple-Selection_img1.png)

## Multiple selection through index

You can select the list of items from the **ListBox** using **selectedItemlist** property. Its data type is array. To achieve this, you need to set true to **allowMultiSelection** property in **ListBox**. 

The following steps explains you the configuration of **selectedItemlist** property in **ListBox**

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       // JSON data declaration
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       //Render ListBox by mapping fields with JSON data
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          selectedItemlist: [0, 3],
          allowMultiSelection: true
       });
    });

{% endhighlight %}


Output of the above steps.

![](/js/ListBox/Multiple-Selection_images/Multiple-Selection_img2.png)

# Checkbox Support

## Show Checkbox

You can enable the checkbox in the **ListBox** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its **ListBox** client side events.  

### Defining the Checkbox support

The following steps explains you the configuration of checkbox options in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       // JSON data declaration
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       //Render ListBox by mapping fields with JSON data
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          showCheckbox: true
       });
    });

{% endhighlight %}


Output of the above steps.

![](/js/ListBox/Multiple-Selection_images/Multiple-Selection_img3.png)

## Check All

You can check all the check box in the list by using this property. The data type of **checkAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

The following steps explains you the configuration of checkbox options in **ListBox.**

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
   <h5 class="ctrllabel">Select a skill</h5>
   <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function() {
       // JSON data declaration
       var skillset = [{
          skill: "ASP.NET"
       }, {
          skill: "ActionScript"
       }, {
          skill: "Basic"
       }, {
          skill: "C++"
       }, {
          skill: "C#"
       }, {
          skill: "dBase"
       }, {
          skill: "Delphi"
       }, {
          skill: "ESPOL"
       }, {
          skill: "F#"
       }, {
          skill: "FoxPro"
       }, {
          skill: "Java"
       }, {
          skill: "J#"
       }, {
          skill: "Lisp"
       }, {
          skill: "Logo"
       }, {
          skill: "PHP"
       }];
       //Render ListBox by mapping fields with JSON data
       $("#listboxSample").ejListBox({
          width: "350",
          dataSource: skillset,
          fields: {
             text: "skill"
          },
          showCheckbox: true,
          checkAll: true
       });
    });

{% endhighlight %}


Output of the above steps.

![](/js/ListBox/Multiple-Selection_images/Multiple-Selection_img4.png)

## Uncheck All

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

