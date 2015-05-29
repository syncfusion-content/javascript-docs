---
layout: post
title: template-support
description: template support
platform: js
control: ListBox
documentation: ug
---

# Template Support

**ListBox** widget provides the template support, when binding the data for the **ListBox**. For this behaviour, set the common syntax /element in template property. You can add any **HTML** mark-up element inside the **ListBox** using this property.

The following steps explains you the behaviour of template support with **ListBox**.

* In an **HTML** page, add a **&lt;li&gt; element** to configure **ListBox** widget.

> ![Note](template-support_images\template-support_img1.png)_**Note: Images for this sample are available in ‘installed location/images/Employee’**_ 


<table>
<tr>
<td>
<b>[HTML]   </b>&lt;div id="controlitem"&gt;    <h3>Template Support</h3>    &lt;div id="selectexperts"&gt;&lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>// </b>Initialize the control in <b>JavaScript </b>&lt;script type="text/javascript"&gt;    var target;    var empList = [       { text: "Erik Linden", eimg: "3", desig: "Representative", tooltip: "Representative", country: "England" }, { text: "John Linden", eimg: "6", tooltip: "Manager", desig: "Representative", country: "Norway" },          { text: "Louis", eimg: "7", tooltip: "CEO", desig: "Representative", country: "Australia" }, { text: "Lawrence", eimg: "8", tooltip: "President", desig: "Representative", country: "India" }];    $(function () {        $('#selectexperts').ejListBox({            dataSource: empList, height: "245", enableTooltip: true,            <b>template: '&lt;div title="${tooltip}"&gt;&lt;img class="eimg" src="images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +</b><b>                        '&lt;div class="ename"&gt; ${text} &lt;/div&gt; &lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;&lt;/div&gt;'</b>        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]  </b>// Add the following code in View page to configure ListBox widget  &lt;div class="control"&gt;    &lt;div class="ctrllabel"&gt;        Template support    &lt;/div&gt;    @Html.EJ().ListBox("listboxsample").Datasource((IEnumerable<employeespecialists>)ViewBag.datasource).Height("238").Template("&lt;img class='eimg' src='../../Content/images/Employees/${eimg}.png' alt='employee' height='50px' width='50px'/&gt;&lt;div class='ename'&gt; ${text} &lt;/div&gt;&lt;div class='desig'&gt; ${desig} &lt;/div&gt;&lt;div class='cont'&gt; ${country} &lt;/div&gt;")&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]  </b><b>//</b> Add the following code to add list items in the controller page        public class EmployeeSpecialists        {            public string text { get; set; }            public string eimg { get; set; }            public string desig { get; set; }            public string country { get; set; }        }        public ActionResult Index()        {            List<EmployeeSpecialists> empl = new List<EmployeeSpecialists>();            empl.Add(new EmployeeSpecialists { text = "Erik Linden", eimg = "3", desig = "Representative", country = "England" });            empl.Add(new EmployeeSpecialists { text = "John Linden", eimg = "6", desig = "Representative", country = "Norway" });            empl.Add(new EmployeeSpecialists { text = "Louis", eimg = "7", desig = "Representative", country = "Australia" });            empl.Add(new EmployeeSpecialists { text = "Lawrence", eimg = "8", desig = "Representative", country = "India" });            ViewBag.datasource = empl;            return View();        }</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]   </b>// In an ASPX page, add a ListBox control&lt;div id="controlitem"&gt;    &lt;div&gt;        Template Support</div>    &lt;ej:listbox id="selectExperts" runat="server" height="240" itemscount="5" template="&lt;img class='eimg' src='/Content/images/Employee/${eimg}.png' alt='employee' height='50px' width='50px'/&gt;&lt;div class='ename'&gt; ${text} &lt;/div&gt;&lt;div class='desig'&gt; ${desig} &lt;/div&gt;&lt;div class='cont'&gt; ${country} &lt;/div&gt;">                        &lt;/ej:listbox&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>// </b>Initialize the control in <b>CS</b>        protected void Page_Load(object sender, EventArgs e)        {      List<EmployeeSpecialists> empl = new List<EmployeeSpecialists>();      empl.Add(new EmployeeSpecialists { text = "Erik Linden", eimg = "3", desig = "Representative", country = "England" });      empl.Add(new EmployeeSpecialists { text = "John Linden", eimg = "6", desig = "Representative", country = "Norway" });      empl.Add(new EmployeeSpecialists { text = "Louis", eimg = "7", desig = "Representative", country = "Australia" });      empl.Add(new EmployeeSpecialists { text = "Lawrence", eimg = "8", desig = "Representative", country = "India" });      empl.Add(new EmployeeSpecialists { text = "Erik Linden", eimg = "3", desig = "Representative", country = "England" });      empl.Add(new EmployeeSpecialists { text = "John Linden", eimg = "6", desig = "Representative", country = "Norway" });      empl.Add(new EmployeeSpecialists { text = "Louis", eimg = "7", desig = "Representative", country = "Australia" });      empl.Add(new EmployeeSpecialists { text = "Lawrence", eimg = "8", desig = "Representative", country = "India" });      selectExperts.DataSource = empl;        }        public class EmployeeSpecialists        {            public string text { get; set; }            public string eimg { get; set; }            public string desig { get; set; }            public string country { get; set; }        } </td></tr>
</table>


Customize the template in **CSS**. 


{% highlight css %}

[CSS]  
<style>
    .eimg {
        margin: 0;
        padding: 3px 10px 3px 3px;
        border: 0 none;
        width: 60px;
        height: 60px;
        float: left;
    }

    .ename {
        font-weight: bold;
        padding: 6px 3px 1px 3px;
    }

    .desig, .cont {
        font-size: smaller;
        padding: 3px 3px -1px 0px;
    }

    #selectexperts li {
        width: 200px;
        height: 70px;
        padding: 5px;
    }
</style>



{% endhighlight %}



Output of the above steps.




{% include image.html url="\js\Listbox\concepts-and-features\template-support_images\template-support_img2.png" Caption="Figure 3327: ListBox with template support"%}

