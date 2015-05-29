---
layout: post
title: template-support
description: template support
platform: js
control: DropDownList
documentation: ug
---

# Template Support

**Dropdown** widget provides the template support for the **Dropdownlist**, when binding the data’s for the dropdown. For this behaviour you need to set the common syntax /element in template property. You can add any Html mark-up element inside of dropdown list using this property.

The following steps explains you the behaviour of template support with **Dropdownlist**

* In an **HTML** page, add a **&lt;input&gt;** element to configure **Dropdownlist** widget

> ![C:\Users\ApoorvahR\Desktop\Note.png](template-support_images\template-support_img1.png)_**Note: Images for this sample are available in ‘installed location /themes/images’**_ 


<table>
<tr>
<td>
<b>[HTML]   </b>     &lt;div class="control"&gt;            <div class="ctrllabel">Select an expert</div>            &lt;input type="text" id="dropdownlist" /&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b>// Initialize the control in <b>JavaScript</b><b> </b>   &lt;script type="text/javascript"&gt;        var empList = [                { text: "Erik Linden", eimg: "3", desig: "Representative", country: "England" }, { text: "John Linden", eimg: "6", desig: "Representative", country: "Norway" },                { text: "Louis", eimg: "7", desig: "Representative", country: "Australia" }, { text: "Lawrence", eimg: "8", desig: "Representative", country: "India" }        ];        $(function () {            $('#dropdownlist').ejDropDownList({                dataSource: empList,                width: "200px",<b>                template: '&lt;img class="eimg" src="../images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +</b><b>                        '&lt;div class="customalign"&gt;&lt;div class="ename"&gt; ${text} &lt;/div&gt;&lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;&lt;/div&gt;'</b>            });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]   </b>// Add a DropDownList element using the helper class in CSHTML&lt;div class="control"&gt;<div class="ctrllabel">Select an expert</div>@Html.EJ().DropDownList("dropdownlist").Datasource((IEnumerable<EmpData>)ViewData["emp"]).Width("200px").<b>Template</b>("&lt;img class='eimg' src='../images/Employee/${eimg}.png' alt='employee' height='50px' width='50px'/&gt;" +"&lt;div class="customalign"&gt;&lt;div class='ename'&gt; ${Text} &lt;/div&gt;&lt;div class='desig'&gt; ${Designation} &lt;/div&gt;&lt;div class='cont'&gt; ${Country} &lt;/div&gt;&lt;/div&gt;")&lt;/div&gt;</td></tr>
<tr>
<td>
[CS]  // Initialize the control in controllerpublic ActionResult Property(){             List<EmpData> emp = new List<EmpData>();   emp.Add(new EmpData() { Text = "Erik Linden", Img = "3", Designation = "Representative", Country = "England" });   emp.Add(new EmpData() { Text = "John Linden", Img = "6", Designation = "Representative", Country = "Norway" });   emp.Add(new EmpData() { Text = "Louis", Img = "7", Designation = "Representative", Country = "Australia" });   emp.Add(new EmpData() { Text = "Lawrence", Img = "8", Designation = "Representative", Country = "India" });   ViewData["emp"] = emp;   return View();}public class EmpData{ public string Text { get; set; } public string Img { get; set; } public string Designation { get; set; } public string Country { get; set; }}</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]   </b>// Add Dropdown list widget in ASPX page&lt;div class="control"&gt;      &lt;ej:DropDownList ID="dropdownlist" Template="&lt;img class='eimg' src='../Content/images/Employee/${eimg}.png' alt='employee' height='50px' width='50px'/&gt;&lt;div class='customalign'&gt;&lt;div class='ename'&gt; ${text} &lt;/div&gt;&lt;div class='desig'&gt; ${desig} &lt;/div&gt;&lt;div class='cont'&gt; ${country}&lt;/div&gt;&lt;/div&gt;"  Width="200px" runat="server">      &lt;/ej:DropDownList&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
[C#]  // Initialize the control in CS pageprotected void Page_Load(object sender, EventArgs e)        {            List<employee> EmpList = new List<employee>();            EmpList.Add(new employee() { Text = "Erik Linden", Image = "3", Designation = " Representative", Country = "England" });            EmpList.Add(new employee() { Text = "John Linden", Image = "6", Designation = "Representative", Country = "Norway" });            EmpList.Add(new employee() { Text = "Louis", Image = "7", Designation = "Representative", Country = "Australia" });            EmpList.Add(new employee() { Text = "Lawrence", Image = "8", Designation = "Representative", Country = "India" });            dropdownlist.DataSource = EmpList;                  }   public class employee        {            public string Image{get; set;}            public string Text {get; set;}            public string Designation{ get; set;}            public string Country{get;set; }        }</td></tr>
</table>


* Customize the template in CSS. 


{% highlight css %}

[CSS]  
  <style type="text/css">
        .customalign {
            display: inline;
            float: right;
        }
    </style>


{% endhighlight %}



* Output of the above steps.


![](template-support_images\template-support_img2.png)

_Figure_ _57__31__: Dropdown with template support_  

