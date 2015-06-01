---
layout: post
title: Theme
description: theme
platform: js
control: ListBox
documentation: ug
---

# Theme

**ListBox** control’s style and appearance can be controlled based on **CSS** classes. In order to apply styles to the **ListBox** control, you can refer to two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer to the file **ej.widgets.all.min.css,** it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **ListBox** control namely,

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

The following screenshot illustrates the **ListBox** with Flat-lime and Flat-Saffron built-in themes.

{% include image.html url="/js/Listbox/Concepts-and-Features/Theme_images/Theme_img1.png" Caption="Figure 20: ListBox with Flat-lime Theme"%}

{% include image.html url="/js/Listbox/Concepts-and-Features/Theme_images/Theme_img2.png" Caption="Figure 21: ListBox with Flat-Saffron Theme"%}

**Custom class with ListBox** 

**CSS** class can be used to customize the **ListBox** control appearance. Define a **CSS** class as per your requirement and assign the class name to **cssClass** property. The data type of **cssClass** property is string. 

**Configuring the Custom CSS property**

The following steps explains you the configuration of **cssClass** properties in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>cssClass: "customclass"</b>        });    });&lt;/script&gt;</td></tr>
</table>


Configure the **CSS** styles to apply on **ListBox**.



{% highlight css %}

[CSS]  
<style>
    .customclass {
        background-color: #FFFFCC;
        font-weight: bold;
        font-family: sans-serif;
    }
</style>


{% endhighlight %}



Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Theme_images/Theme_img3.png" Caption="Figure 22: ListBox with cssClass property"%}

