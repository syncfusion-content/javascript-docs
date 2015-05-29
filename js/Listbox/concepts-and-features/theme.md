---
layout: post
title: theme
description: theme
platform: js
control: ListBox
documentation: ug
---

# Theme

**ListBox** control’s style and appearance can be controlled based on **CSS** classes. In order to apply styles to the **ListBox** control, you can refer to two files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer to the file **ej.widgets.all.min.css,** it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **ListBox** control namely,

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

The following screenshot illustrates the **ListBox** with Flat-lime and Flat-Saffron built-in themes.

{% include image.html url="\js\Listbox\concepts-and-features\theme_images\theme_img1.png" Caption="Figure 2620: ListBox with Flat-lime Theme"%}

{% include image.html url="\js\Listbox\concepts-and-features\theme_images\theme_img2.png" Caption="Figure 2721: ListBox with Flat-Saffron Theme"%}

**Custom class with ListBox** 

**CSS** class can be used to customize the **ListBox** control appearance. Define a **CSS** class as per your requirement and assign the class name to **cssClass** property. The data type of **cssClass** property is string. 

**Configuring the Custom CSS property**

The following steps explains you the configuration of **cssClass** properties in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>cssClass: "customclass"</b>        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) .<b>CssClass("customclass")</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    <ej:listbox id="listboxsample" <b>cssclass="customclass"</b> DataTextField="Name"        runat="server">&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS] </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        } </td></tr>
</table>


Configure the **CSS** styles to apply on **ListBox**.



{% highlight css %}

[CSS]  
<style>
    .customclass {
        background-color: #FFFFCC;
        font-weight: bold;
        font-family: sans-serif;
    }
</style>


{% endhighlight %}



Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\theme_images\theme_img3.png" Caption="Figure 2822: ListBox with cssClass property"%}

