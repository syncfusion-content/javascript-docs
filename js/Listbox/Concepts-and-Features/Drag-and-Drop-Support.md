---
layout: post
title: Drag-and-Drop-Support
description: drag and drop support
platform: js
control: ListBox
documentation: ug
---

# Drag and Drop Support

**ListBox** widget provides the Drag and Drop support. A list item can be dragged from a **ListBox** control and can be dropped in any droppable element. To enable Drag and Drop support, set the **allowDragAndDrop** property as true. In control, enable the **allowDragAndDrop** property where you want to drop list Item.

The following steps explains you the behaviour of template support with **ListBox**.

* In an **HTML** page, add a **&lt;li&gt; element** to configure **ListBox** widget.

<table>
<tr>
<td>
<br><b>[HTML]   </b>&lt;div class="control"&gt;    <div class="ctrllabel">Drag and drop skills</div>    &lt;div class="control1" style="float: left;"&gt;        &lt;ul id="listboxSample"&gt;        &lt;/ul&gt;    &lt;/div&gt;    &lt;div class="control2"&gt;        &lt;ul id="dragsample"&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [    { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },    { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },    { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },    { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>allowDragAndDrop: true</b>        });        $("#dragsample").ejListBox({ <b>allowDragAndDrop: true</b> });    });&lt;/script&gt;</td></tr>
</table>


Add the following class in CSS. 


{% highlight css %}

[CSS]  
<style type="text/css" class="cssStyles">
    .control {
        margin-left: 20px;
    }

    .ctrllabel {
        padding-bottom: 3px;
    }

    .control2 {
        padding-left: 350px;
    }
</style>



{% endhighlight %}



Output of the above steps.

{% include image.html url="/js/Listbox/Concepts-and-Features/Drag-and-Drop-Support_images/Drag-and-Drop-Support_img1.png" Caption="Figure 26: ListBox with Drag and Drop support"%}

