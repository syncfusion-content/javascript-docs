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


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript </b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            <b>width: "240", height: "302"</b>, dataSource: skillset,            fields: { text: "skill" }        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps


{% include image.html url="/js/Listbox/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img1.png" Caption="Figure 18: ListBox with specified width and height"%}

**Enabling Rounded corner**

**ListBox** widget provides you support to change the appearance of **ListBox**. By using **showRoundedCorner** you can create a rounded corner on the **ListBox**. Its data type is Boolean.

The following steps explains you the configuration of Rounded corner of the **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>showRoundedCorner: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Appearance-and-Styling_images/Appearance-and-Styling_img2.png" Caption="Figure 19: ListBox with Rounded corner"%}

