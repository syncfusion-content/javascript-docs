---
layout: post
title: rtl-support
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


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")).<b>EnableRTL(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<br><b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" runat="server" DataTextField="Name"  enablertl="true"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]  </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\rtl-support_images\rtl-support_img1.png" Caption="Figure 3428: ListBox with RTL"%}

