---
layout: post
title: drag-and-drop-support
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


<table>
<tr>
<td>
<b>[View]  </b>// Add the following code in View page to configure ListBox widget &lt;div class="control1"&gt;    &lt;h5 class="ctrllabel"&gt;        Drag and drop skills    &lt;/h5&gt;@Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) .<b>AllowDragAndDrop(true)</b>&lt;/div&gt;&lt;div class="control2"&gt;     @Html.EJ().ListBox("dragsample").<b>AllowDragAndDrop(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]	</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]  </b>// In an ASPX page, add a ListBox control&lt;div class="control"&gt;    &lt;div class="ctrllabel"&gt;        Drag and drop skills</div>    &lt;div class="control1" style="float: left;"&gt;        &lt;ej:listbox id="listboxsample" DataTextField="Name"  allowdraganddrop="true" runat="server" width="240"&gt;&lt;/ej:listbox&gt;    &lt;/div&gt;    &lt;div class="control2"&gt;        &lt;ej:listbox id="draganddrop" allowdraganddrop="true" runat="server" width="240"&gt;&lt;/ej:listbox&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]  </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        } </td></tr>
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

{% include image.html url="\js\Listbox\concepts-and-features\drag-and-drop-support_images\drag-and-drop-support_img1.png" Caption="Figure 3226: ListBox with Drag and Drop support"%}

