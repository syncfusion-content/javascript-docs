---
layout: post
title: Keyboard-interaction
description: keyboard interaction
platform: js
control: ListBox
documentation: ug
---

# Keyboard interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **ListBox** widget. **ListBox** Widget allows you to perform all kind of actions using keyboard shortcuts.

Keyboard shortcut keys

<table>
<tr>
<th>Shortcut Key</th><th>Description</th></tr>
<tr>
<td>
<a href="http://en.wikipedia.org/wiki/Access_key">Access key</a> + j	</td><td>
Focuses into the ListBox text box</td></tr>
<tr>
<td>
Up</td><td>
Moves to previous item in the ListBox</td></tr>
<tr>
<td>
Down</td><td>
Moves to next item in the ListBox</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
<tr>
<td>
Left </td><td>
Moves to previous item in the ListBox</td></tr>
<tr>
<td>
Right </td><td>
Moves to next item in the ListBox</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item </td></tr>
<tr>
<td>
End</td><td>
Navigates to the end item </td></tr>
</table>

**Configure keyboard interaction**

The following steps explains you to enable keyboard interaction for a **ListBox**.

In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget and enable keyboard interaction by setting the **accesskey** property.

{% highlight html %}

	<div id="control">
	    <h5 class="ctrllabel">Select a skill</h5>
	    <ul id="listboxSample"></ul>
	</div>

{% endhighlight %}

{% highlight js %}


    $(function () {
        var skillset = [
        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        $("#listboxSample").ejListBox({
            width: "240", dataSource: skillset,
            fields: { text: "skill" }
        });
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                var target = $('#listboxSample').data("ejListBox");
                target.selectItemByIndex(1);
                $("#listboxSample_container").focus();
            }
        });
    });


{% endhighlight %}

Run the sample, press Alt + J to focus in the **ListBox** widget that enables it and you can navigate using arrow keys.

{% include image.html url="/js/ListBox/Keyboard-interaction_images/Keyboard-interaction_img1.png" Caption="ListBox focused and moved with Keyboard shortcut"%}































