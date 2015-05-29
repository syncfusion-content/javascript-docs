---
layout: post
title: tooltip-support
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


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text").<b>ToolTipText("tooltip"))</b> .<b>EnableTooltip(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }            public string tooltip { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET", tooltip = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript", tooltip = "ActionScript"      });            skill.Add(new skillset { text = "Basic", tooltip = "Basic" });            skill.Add(new skillset { text = "C++", tooltip = "C++" });            skill.Add(new skillset { text = "C#", tooltip = "C#" });            skill.Add(new skillset { text = "dBase", tooltip = "dBase" });            skill.Add(new skillset { text = "Delphi", tooltip = "Delphi" });            skill.Add(new skillset { text = "ESPOL", tooltip = "ESPOL" });            skill.Add(new skillset { text = "F#", tooltip = "F#" });            skill.Add(new skillset { text = "FoxPro", tooltip = "FoxPro" });            skill.Add(new skillset { text = "Java", tooltip = "Java" });            skill.Add(new skillset { text = "J#", tooltip = "J#" });            skill.Add(new skillset { text = "Lisp", tooltip = "Lisp" });            skill.Add(new skillset { text = "Logo", tooltip = "Logo" });            skill.Add(new skillset { text = "PHP", tooltip = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" enabletooltip="true" runat="server"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b> [CS]  </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();            listboxsample.DataTextField = "Value";            listboxsample.ListBoxFields.ToolTipText = "Tooltip";        }        private List<ListboxData> GetData()        {            data.Add(new ListboxData() { Value = "ASP.NET", Tooltip = "ASP.NET" });            data.Add(new ListboxData() { Value = "ActionScript", Tooltip = "ActionScript" });            data.Add(new ListboxData() { Value = "Basic", Tooltip = "Basic" });            data.Add(new ListboxData() { Value = "C++", Tooltip = "C++" });            data.Add(new ListboxData() { Value = "C#", Tooltip = "C#" });            data.Add(new ListboxData() { Value = "dBase", Tooltip = "dBase" });            data.Add(new ListboxData() { Value = "Delphi", Tooltip = "Delphi" });            data.Add(new ListboxData() { Value = "ESPOL", Tooltip = "ESPOL" });            data.Add(new ListboxData() { Value = "F#", Tooltip = "F#" });            data.Add(new ListboxData() { Value = "FoxPro", Tooltip = "FoxPro" });            data.Add(new ListboxData() { Value = "Java", Tooltip = "Java" });            data.Add(new ListboxData() { Value = "J#", Tooltip = "J#" });            data.Add(new ListboxData() { Value = "Lisp", Tooltip = "Lisp" });            data.Add(new ListboxData() { Value = "Logo", Tooltip = "Logo" });            data.Add(new ListboxData() { Value = "PHP", Tooltip = "PHP" });            return data;        }        class ListboxData        {            public string Value, Tooltip;        }</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\tooltip-support_images\tooltip-support_img1.png" Caption="Figure 2923: ListBox with tooltip property"%}

