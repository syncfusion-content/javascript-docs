---
layout: post
title: multiple-selection
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


**[View]**

&lt;div id="control"&gt;

    &lt;h5 class="ctrllabel"&gt;

        Select a skill

    &lt;/h5&gt;

    @{List<int> indexList = new List<int>();



    indexList.Add(0);



    indexList.Add(3);



    }       @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")).**SelectedItemlist(indexList) .AllowMultiSelection(true)**

&lt;/div&gt;





<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div><ej:listbox id="listboxsample" DataTextField="Name" <b>AllowMultiSelection="true"</b> runat="server" width="240">&lt;/ej:listbox&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b> [CS] </b><b> // C</b>onfigure <b>allowMultiSelection</b> option for <b>ListBox</b> control as follows     protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output for **ListBox** control that provides multiple selection is as follows.


{% include image.html url="\js\Listbox\concepts-and-features\multiple-selection_images\multiple-selection_img1.png" Caption="Figure 2014: ListBox with Multiple Selection"%}

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


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @{List<int> indexList = new List<int>();    indexList.Add(1);    indexList.Add(4);    }       @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")).<b>SelectedItemlist(indexList) .AllowMultiSelection(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>&lt;ej:listbox id="listboxsample" AllowMultiSelection="true" DataTextField="Name" runat="server" width="240"&gt;&lt;/ej:listbox&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b> [CS]  </b><b>// </b>Initialize the control in <b>CS</b>        private List<int> indexList = new List<int>();        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();            indexList.Add(0);            indexList.Add(3);            <b>listboxsample.selectedItemlist = indexList;</b>        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\multiple-selection_images\multiple-selection_img2.png" Caption="Figure 2115: ListBox with selectedItemlist property"%}

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
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>showCheckbox: true</b>,        });    });&lt;/script&gt;</td></tr>
</table>


**[View]**

// Add the following code in View page to configure ListBox widget

&lt;div id="control"&gt;

    &lt;h5 class="ctrllabel"&gt;

        Select a skill

    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) .**ShowCheckbox(true)**

&lt;/div&gt;

**[CS]**

**//** Add the following code to add list items in the controller page

        public class skillset

        {

            public string text { get; set; }

        }

        public ActionResult Index()

        {

            List<skillset> skill = new List<skillset>();

            skill.Add(new skillset { text = "ASP.NET" });

            skill.Add(new skillset { text = "ActionScript" });

            skill.Add(new skillset { text = "Basic" });

            skill.Add(new skillset { text = "C++" });

            skill.Add(new skillset { text = "C#" });

            skill.Add(new skillset { text = "dBase" });

            skill.Add(new skillset { text = "Delphi" });

            skill.Add(new skillset { text = "ESPOL" });

            skill.Add(new skillset { text = "F#" });

            skill.Add(new skillset { text = "FoxPro" });

            skill.Add(new skillset { text = "Java" });

            skill.Add(new skillset { text = "J#" });

            skill.Add(new skillset { text = "Lisp" });

            skill.Add(new skillset { text = "Logo" });

            skill.Add(new skillset { text = "PHP" });

            ViewBag.datasource = skill;

            return View();

        }



<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" DataTextField="Name" ShowCheckbox="true" runat="server" width="240"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b> [CS]  </b><b>// </b>Initialize the control in <b>CS</b>protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\multiple-selection_images\multiple-selection_img3.png" Caption="Figure 2216: ListBox with checkbox "%}

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


<table>
<tr>
<td>
<b>[View]</b>// Add the following code in View page to configure ListBox widget&lt;div id="control"&gt;    &lt;h5 class="ctrllabel"&gt;        Select a skill    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) .ShowCheckbox(true).<b>CheckAll(true)</b>&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>//</b> Add the following code to add list items in the controller page        public class skillset        {            public string text { get; set; }        }        public ActionResult Index()        {            List<skillset> skill = new List<skillset>();            skill.Add(new skillset { text = "ASP.NET" });            skill.Add(new skillset { text = "ActionScript" });            skill.Add(new skillset { text = "Basic" });            skill.Add(new skillset { text = "C++" });            skill.Add(new skillset { text = "C#" });            skill.Add(new skillset { text = "dBase" });            skill.Add(new skillset { text = "Delphi" });            skill.Add(new skillset { text = "ESPOL" });            skill.Add(new skillset { text = "F#" });            skill.Add(new skillset { text = "FoxPro" });            skill.Add(new skillset { text = "Java" });            skill.Add(new skillset { text = "J#" });            skill.Add(new skillset { text = "Lisp" });            skill.Add(new skillset { text = "Logo" });            skill.Add(new skillset { text = "PHP" });            ViewBag.datasource = skill;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;     <div class="ctrllabel">Select a skill</div>&lt;ej:listbox id="listboxsample" DataTextField="Name" ShowCheckbox="true" CheckAll="true" runat="server" width="240"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]  </b><b>// </b>Initialize the control in <b>CS</b>protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\multiple-selection_images\multiple-selection_img4.png" Caption="Figure 2317: ListBox with checkbox property"%}

**Uncheck All**

You can uncheck all the check box in the list by using this property. The data type of **uncheckAll** is Boolean type. To achieve this, set **showCheckbox** property as true.

