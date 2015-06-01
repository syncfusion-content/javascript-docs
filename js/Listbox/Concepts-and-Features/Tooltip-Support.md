---
layout: post
title: Tooltip-Support
description: tooltip support
platform: js
control: ListBox
documentation: ug
---

# Tooltip Support

The following steps explains you the configuration of **tooltip** properties in **ListBox**.

* In an **HTML** page, add a &lt;ul&gt; element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        var skillset = [        { skill: "ASP.NET", tooltip: "ASP.NET" }, { skill: "ActionScript", tooltip: "ActionScript" }, { skill: "Basic", tooltip: "Basic" },        { skill: "C++", tooltip: "C++" }, { skill: "C#", tooltip: "C#" }, { skill: "dBase", tooltip: "dBase" }, { skill: "Delphi", tooltip: "Delphi" },        { skill: "ESPOL", tooltip: "ESPOL" }, { skill: "F#", tooltip: "F#" }, { skill: "FoxPro", tooltip: "FoxPro" }, { skill: "Java", tooltip: "Java" },        { skill: "J#", tooltip: "J#" }, { skill: "Lisp", tooltip: "Lisp" }, { skill: "Logo", tooltip: "Logo" }, { skill: "PHP", tooltip: "PHP" }        ];        $("#listboxSample").ejListBox({            dataSource: skillset, <b>enableTooltip: true,</b>            fields: { text: "skill", <b>toolTipText: "tooltip"</b> }        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Tooltip-Support_images/Tooltip-Support_img1.png" Caption="Figure 23: ListBox with tooltip property"%}

