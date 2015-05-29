---
layout: post
title: keyboard-interaction
description: keyboard interaction
platform: js
control: ListBox
documentation: ug
---

# Keyboard interaction

You can use **Keyboard** shortcut keys as an alternative to the mouse on using **ListBox** widget. **ListBox** Widget allows you to perform all kind of actions using keyboard shortcuts.

_Table_ _4__: Keyboard shortcut keys_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a> + j	</td><td>
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

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget and enable keyboard interaction by setting the **accesskey** property.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Render Listbox control&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }        });        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                var target = $('#listboxSample').data("ejListBox");                target.selectItemByIndex(1);                <b>$("#listboxSample_container").focus();</b>            }        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;  @Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text"))&lt;/div&gt;</td></tr>
<tr>
<td>
<br><b>[JavaScript]</b>// Render ListBox control&lt;script type="text/javascript"&gt;    $(document).on("keydown", function (e) {        if (e.altKey && e.keyCode === 74) { // j- key code.            var target = $('#listboxsample').data("ejListBox");            target.selectItemByIndex(1);            $("#listboxsample_container").focus();        }    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" runat="server" DataTextField="Name"&gt;&lt;/ej:listbox&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[CS] </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Enable keyboard interaction using JavaScript&lt;script type="text/javascript"&gt;    $(function () {        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                var target = $('#listboxSample').data("ejListBox");                target.selectItemByIndex(1);                <b>$("#listboxSample_container").focus();</b>            }        });    });&lt;/script&gt;</td></tr>
</table>


Run the sample, press Alt + J to focus in the **ListBox** widget that enables it and you can navigate using arrow keys.


{% include image.html url="\js\Listbox\concepts-and-features\keyboard-interaction_images\keyboard-interaction_img1.png" Caption="Figure 3529: ListBox focused and moved with Keyboard shortcut"%}



























