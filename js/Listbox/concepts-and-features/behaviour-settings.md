---
layout: post
title: behaviour-settings
description: behaviour settings
platform: js
control: ListBox
documentation: ug
---

# Behaviour Settings

The following are some miscellaneous properties that helps you to change the behaviour of **ListBox** control.

**Target ID**

You can append a list with **ListBox** by using **targetId** property. Define a **&lt;ul&gt;,****&lt; li&gt;** tag that you want to display on **ListBox** and then set the id of parent **&lt;ul&gt;** tag to **targetId** property. And its data type is string. 

The following steps explains you the configuration of **targetID** property in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a font style</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;    &lt;ul id="targetlist"&gt;        <li>Algerian</li>        <li>ARIAL</li>        <li>Bimini</li>        <li>Courier</li>        <li>Cursive</li>        <li>Fantasy</li>        <li>Georgia</li>        <li>Impact</li>        <li>New york</li>        <li>Sans-Serif</li>        <li>Scripts</li>        <li>Times</li>        <li>Times New Roman</li>        <li>Verdana</li>        <li>Western</li>        <li>Zapfellipt bt</li>    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>// </b>Initialize the control in <b>JavaScript</b><b> </b>&lt;script type="text/javascript"&gt;    $(function () {        $('#listboxSample').ejListBox({ <b>targetID: "targetlist"</b> });    });&lt;/script&gt;</td></tr>
</table>


**[View]**

// Add the following code in View page to configure ListBox widget

&lt;div id="control"&gt;

    &lt;h5 class="ctrllabel"&gt;

        Select a font style

    &lt;/h5&gt;

    @Html.EJ().ListBox("listboxsample").**TargetID("targetlist")**

    &lt;ul id="targetlist"&gt;

        <li>Algerian</li>

        <li>ARIAL</li>

        <li>Bimini</li>

        <li>Courier</li>

        <li>Cursive</li>

        <li>Fantasy</li>

        <li>Georgia</li>

        <li>Impact</li>

        <li>New york</li>

        <li>Sans-Serif</li>

        <li>Scripts</li>

        <li>Times</li>

        <li>Times New Roman</li>

        <li>Verdana</li>

        <li>Western</li>

        <li>Zapfellipt bt</li>

    &lt;/ul&gt;

&lt;/div&gt;





**[ASPX]**

// In an ASPX page, add a ListBox control

&lt;div id="control"&gt;

        &lt;div class="ctrllabel"&gt;

            Select a font style</div>

        &lt;ej:listbox id="listboxsample" targetid="targetlist" runat="server" width="240"&gt;&lt;/ej:listbox&gt;

        &lt;ul id="targetlist"&gt;

            <li>Algerian</li>

            <li>ARIAL</li>

            <li>Bimini</li>

            <li>Courier</li>

            <li>Cursive</li>

            <li>Fantasy</li>

            <li>Georgia</li>

            <li>Impact</li>

            <li>New york</li>

            <li>Sans-Serif</li>

            <li>Scripts</li>

            <li>Times</li>

            <li>Times New Roman</li>

            <li>Verdana</li>

            <li>Western</li>

            <li>Zapfellipt bt</li>

        &lt;/ul&gt;

    &lt;/div&gt;





Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\behaviour-settings_images\behaviour-settings_img1.png" Caption="Figure 1711: ListBox with target id property"%}

**Select the value by index** 

**ListBox** widget provides you support to select an item by mentioning the index of the item. The **selectedItemIndex** property helps you to select the particular item from the list. Its date type is number. 

The following steps explains you the configuration of **selectedItemIndex** property in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.



{% highlight html %}

**[HTML]**
<div id="control">
        <h5 class="ctrllabel">Select a skill</h5>
        <ul id="listboxsample"></ul>
    </div>

**[JavaScript]**  

<script type="text/javascript">
    $(function () {
        // JSON data declaration
        var skillset = [
        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        //Render ListBox by mapping fields with JSON data
        $("#listboxsample").ejListBox({
            width: "240", dataSource: skillset,
            fields: { text: "skill" }, **selectedItemIndex: 2**
        });
    });
</script>


{% endhighlight %}



**[View]**

&lt;div id="control"&gt;

    &lt;h5 class="ctrllabel"&gt;

        Select a skill

    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df

    => df.Text("text")).**SelectedItemIndex(2)**

&lt;/div&gt;





**[ASPX]**

&lt;div id="control"&gt;

    &lt;div class="ctrllabel"&gt;

        Select a skill</div>

&lt;ej:listbox id="listboxsample" DataTextField="Name" SelectedItemIndex="2" runat="server" width="240"&gt;&lt;/ej:listbox&gt;

&lt;/div&gt;





* Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\behaviour-settings_images\behaviour-settings_img2.png" Caption="Figure 1812: ListBox with selectedItemIndex property"%}

**Enable or Disable the ListBox Widget**

This features enables you to set the enable or disable options for **ListBox** by setting Boolean type value to **enabled** property. 

The following steps explains you the configuration of **enabled** property in **ListBox**.

* In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="control"&gt;    <h5 class="ctrllabel">Select a skill</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        // JSON data declaration        var skillset = [        { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },        { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },        { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },        { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }        ];        //Render ListBox by mapping fields with JSON data        $("#listboxSample").ejListBox({            width: "240", dataSource: skillset,            fields: { text: "skill" }, <b>enabled: false</b>        });    });&lt;/script&gt;</td></tr>
</table>


**[View]**

// Add the following code in View page to configure ListBox widget

&lt;div id="control"&gt;

    &lt;h5 class="ctrllabel"&gt;

        Select a skill

    &lt;/h5&gt;    @Html.EJ().ListBox("listboxsample").Width("240").Datasource((IEnumerable<ug_listbox.controllers.skillset>)ViewBag.datasource).ListBoxFields(df => df.Text("text")) **.Enabled(false)**

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
<b>[ASPX]</b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="ctrllabel"&gt;        Select a skill</div>    &lt;ej:listbox id="listboxsample" DataTextField="Name" Enabled="false" runat="server" width="240"&gt;&lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS] </b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {            listboxsample.DataSource = GetData();        }        private List<Languages> GetData()        {            List<Languages> data = new List<Languages>();            data.Add(new Languages() { Name = "ASP.NET" });            data.Add(new Languages() { Name = "ActionScript" });            data.Add(new Languages() { Name = "Basic" });            data.Add(new Languages() { Name = "C++" });            data.Add(new Languages() { Name = "C#" });            data.Add(new Languages() { Name = "dBase" });            data.Add(new Languages() { Name = "Delphi" });            data.Add(new Languages() { Name = "ESPOL" });            data.Add(new Languages() { Name = "F#" });            data.Add(new Languages() { Name = "FoxPro" });            data.Add(new Languages() { Name = "Java" });            data.Add(new Languages() { Name = "J#" });            data.Add(new Languages() { Name = "Lisp" });            data.Add(new Languages() { Name = "Logo" });            data.Add(new Languages() { Name = "PHP" });            return data;        }        public class Languages        {            public string Name;        }</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\behaviour-settings_images\behaviour-settings_img3.png" Caption="Figure 1913: ListBox with disabled"%}

