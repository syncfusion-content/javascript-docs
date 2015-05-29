---
layout: post
title: appearance-and-styling
description: appearance and styling
platform: js
control: ListBox
documentation: ug
---

# Appearance and Styling

**Adjusting ListBox size**

**Width**

**ListBox** widget provides you support to customize the dimensions of the **ListBox**. By using **width** property you can set the width of the **ListBox**. Its data type is string.

**Height**

**ListBox** widget provides you support to customize the dimensions of the **ListBox**. By using **height** property, you can set the height of the **ListBox**. Its data type is string.

**Defining the ListBox size properties**

The following steps explains you the configuration of **height** & **width** properties in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript </b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            <b>width: "240", height: "302"</b>, dataSource: skillset,            fields: { text: "skill" }        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").<b>Width("240").Height("302")</b>.Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df    => df.Text("text"))&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" Width="240" Height="302" DataTextField="Name" runat="server"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b> [CS]   </b><b>// </b>Initialize the control in <b>CS    </b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }        </td></tr>
</table>


Output of the above steps


{% include image.html url="\js\Listbox\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img1.png" Caption="Figure 2418: ListBox with specified width and height"%}

**Enabling Rounded corner**

**ListBox** widget provides you support to change the appearance of **ListBox**. By using **showRoundedCorner** you can create a rounded corner on the **ListBox**. Its data type is Boolean.

The following steps explains you the configuration of Rounded corner of the **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>showRoundedCorner: true</b>        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) .<b>ShowRoundedCorner(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" showroundedcorner="true" DataTextField=" Name" runat="server"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<br><b> [CS]  </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\appearance-and-styling_images\appearance-and-styling_img2.png" Caption="Figure 2519: ListBox with Rounded corner"%}

