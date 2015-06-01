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


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>enableRTL: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/RTL-Support_images/RTL-Support_img1.png" Caption="Figure 28: ListBox with RTL"%}

