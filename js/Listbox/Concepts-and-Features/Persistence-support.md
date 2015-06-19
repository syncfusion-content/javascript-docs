---
layout: post
title: Persistence-support
description: persistence support 
platform: js
control: ListBox
documentation: ug
---

# Persistence support 

This features enables you to save current model value to browser cookies for state maintains. When you refresh the **ListBox** control page, it retains the model value apply from browser cookies. The date type of **enablePersistence** is Boolean type. 

The following steps explains you the configuration of **enablePersistence** property in **ListBox**.

In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in JavaScript&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, enablePersistence: true        });    });&lt;/script&gt;</td></tr>
</table>


