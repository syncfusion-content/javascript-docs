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



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Configure <b>allowMultiSelection</b> option for <b>ListBox</b> control as follows&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>allowMultiSelection: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output for **ListBox** control that provides multiple selection is as follows.


{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img1.png" Caption="Figure 14: ListBox with Multiple Selection"%}

**Multiple selection through index** 

You can select the list of items from the **ListBox** using **selectedItemlist** property. Its data type is array. To achieve this, you need to set true to **allowMultiSelection** property in **ListBox**. 

The following steps explains you the configuration of **selectedItemlist** property in **ListBox**

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>selectedItemlist: [0, 3], allowMultiSelection: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img2.png" Caption="Figure 15: ListBox with selectedItemlist property"%}

**Checkbox Support**

**Show Checkbox** 

You can enable the checkbox in the **ListBox** with this property. The data type of **showCheckbox** value is Boolean type. It maintains multiple selection and gets the checked items on its **ListBox** client side events.  

**Defining the Checkbox support**

The following steps explains you the configuration of checkbox options in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>showCheckbox: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.



{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img3.png" Caption="Figure 16: ListBox with checkbox "%}

**Check All** 

You can check all the check box in the list by using this property. The data type of **checkAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

The following steps explains you the configuration of checkbox options in **ListBox.**

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" <b>}, showCheckbox: true,</b><b>            checkAll: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


Output of the above steps.



{% include image.html url="/js/Listbox/Concepts-and-Features/Multiple-Selection_images/Multiple-Selection_img4.png" Caption="Figure 17: ListBox with checkbox property"%}

**Uncheck All**

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

