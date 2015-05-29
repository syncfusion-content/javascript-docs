---
layout: post
title: cascading-support-
description: cascading support 
platform: js
control: DropDownList
documentation: ug
---

# Cascading Support 

Using **cascade** option, you can create a behaviour of cascade between dropdown list controls. For this, you need to create database with single field as common between two dropdown data fields and then mention that column id in field. With this, you need to set second dropdown id in **cascadeTo** property in first one. 


> ![C:\Users\ApoorvahR\Desktop\Note.png](cascading-support-_images\cascading-support-_img1.png)_**Note: In case the second dropdown is to disabled, until the first one is selected, you need to set enable property as false in second dropdown, which enables automatically once the value is selected in first one.**_ 


The following steps explains you the behaviour of cascade dropdown. 

* In an **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList****Dropdownlist** widget


<table>
<tr>
<td>
<b>[HTML]  </b>    &lt;div class="control" style="float: left;"&gt;        <span class="txt">Select Group</span>        &lt;input id="dropdownlist" type="text" /&gt;    &lt;/div&gt;    &lt;div class="control" style="float: left;"&gt;        <span class="txt">Select Country</span>        &lt;input id="dropdownlist1" type="text" /&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]   </b>// Initialize the control in <b>JavaScript</b>   &lt;script type="text/javascript"&gt;        $(function () {            // declaration            var groups = [          { Id: 'a', text: "Group A" },          { Id: 'b', text: "Group B" },          { Id: 'c', text: "Group C" },          { Id: 'd', text: "Group D" },          { Id: 'e', text: "Group E" }]            //first level child            var countries = [{ value: 11, Id: 'a', text: "Algeria", sprite: "flag-dz" },           { value: 12, Id: 'a', text: "Armenia" },           { value: 13, Id: 'a', text: "Bangladesh" },           { value: 14, Id: 'a', text: "Cuba" },           { value: 15, Id: 'b', text: "Denmark" },           { value: 16, Id: 'b', text: "Egypt" },           { value: 17, Id: 'c', text: "Finland" },           { value: 18, Id: 'c', text: "India" },           { value: 19, Id: 'c', text: "Malaysia" },           { value: 20, Id: 'd', text: "New Zealand" },           { value: 21, Id: 'd', text: "Norway" },           { value: 22, Id: 'd', text: "Poland" },           { value: 23, Id: 'e', text: "Romania" },           { value: 24, Id: 'e', text: "Singapore" },           { value: 25, Id: 'e', text: "Thailand" },           { value: 26, Id: 'e', text: "Ukraine" }]            $('#dropdownlist').ejDropDownList({                dataSource: groups,                fields: { value: "Id" },                <b>cascadeTo: "dropdownlist1"</b>            });            $('#dropdownlist1').ejDropDownList({                dataSource: countries,                enabled: false            });        });    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]  </b>// Add a DropDownList element using the helper class in CSHTML&lt;div class="control" style="float: left;"&gt;<span class="txt">Select Group</span>@Html.EJ().DropDownList("dropdownlist").Datasource((IEnumerable< Groups >) ViewData["groups"]).DropDownListFields(f=>f.Value("parentId")).<b>CascadeTo</b>("dropdownlist1")&lt;/div&gt;&lt;div class="control" style="float: left;"&gt;<span class="txt">Select Country</span>@Html.EJ().DropDownList("dropdownlist1").Datasource((IEnumerable<Countries>)ViewData["countries"]).Enabled(false)&lt;/div&gt;</td></tr>
<tr>
<td>
[CS]   // Initialize the control in controller public ActionResult Property() {                List<Groups> dataOne = new List<Groups>();    dataOne.Add(new Groups() { Id = "a", Text = "Group A" });    dataOne.Add(new Groups() { Id = "b", Text = "Group B" });    dataOne.Add(new Groups() { Id = "c", Text = "Group C" });    dataOne.Add(new Groups() { Id = "d", Text = "Group D" });    ViewData["groups"] = dataOne;    List<Countries> dataTwo = new List<Countries>();    dataTwo.Add(new Countries() { Value = 12, Id = "a", Text = "Armenia" });    dataTwo.Add(new Countries() { Value = 13, Id = "a", Text = "Bangladesh" });    dataTwo.Add(new Countries() { Value = 14, Id = "a", Text = "Cuba" });    dataTwo.Add(new Countries() { Value = 15, Id = "b", Text = "Denmark" });    dataTwo.Add(new Countries() { Value = 16, Id = "b", Text = "Egypt" });    dataTwo.Add(new Countries() { Value = 17, Id = "c", Text = "Finland" });    dataTwo.Add(new Countries() { Value = 18, Id = "c", Text = "India" });    dataTwo.Add(new Countries() { Value = 19, Id = "c", Text = "Malaysia" });    dataTwo.Add(new Countries() { Value = 20, Id = "d", Text = "New Zealand" });    dataTwo.Add(new Countries() { Value = 21, Id = "d", Text = "Norway" });    dataTwo.Add(new Countries() { Value = 22, Id = "d", Text = "Poland" });    dataTwo.Add(new Countries() { Value = 23, Id = "d", Text = "Romania" });    dataTwo.Add(new Countries() { Value = 24, Id = "d", Text = "Singapore" });    dataTwo.Add(new Countries() { Value = 25, Id = "d", Text = "Thailand" });    dataTwo.Add(new Countries() { Value = 26, Id = "d", Text = "Ukraine" });    ViewData["countries"] = dataTwo;               }    public class Groups  {        public string Id;        public string Text; } public class Countries {        public int Value;        public string Id;        public string Text; }        </td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]  </b>// Add Dropdown list widget in ASPX page&lt;div class="control" style="float: left;"&gt;            <span class="txt">Select Group</span>            &lt;ej:DropDownList ID="dropdownlist"  runat="server" DataValueField="parentId" CascadeTo="dropdownlist1"&gt;&lt;/ej:DropDownList&gt;        &lt;/div&gt; &lt;div class="control" style="float:left;"&gt;            <span class="txt">Select Country</span>            &lt;ej:DropDownList ID="dropdownlist1" runat="server"&gt;&lt;/ej:DropDownList&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
 [C#]   // Initialize the control in CS pageprotected void Page_Load(object sender, EventArgs e)        {            List<GroupsList> Groups = new List<GroupsList>();            Groups.Add(new GroupsList("a", "Group A"));            Groups.Add(new GroupsList("b", "Group B"));            Groups.Add(new GroupsList("c", "Group C"));            Groups.Add(new GroupsList("d", "Group D"));            Groups.Add(new GroupsList("e", "Group E"));            this.dropdownlist.DataSource = Groups;            List<CountryList> Countries = new List<CountryList>();            Countries.Add(new CountryList(11, "a", "Algeria", "flag-dz"));            Countries.Add(new CountryList(12, "a", "Armenia", "flag-am"));            Countries.Add(new CountryList(13, "a", "Bangladesh", "flag-bd"));            Countries.Add(new CountryList(14, "a", "Cuba", "flag-cu"));            Countries.Add(new CountryList(15, "b", "Denmark", "flag-dk"));            Countries.Add(new CountryList(16, "b", "Egypt", "flag-eg"));            Countries.Add(new CountryList(17, "c", "Finland", "flag-fi"));            Countries.Add(new CountryList(18, "c", "India", "flag-in"));            Countries.Add(new CountryList(19, "c", "Malaysia", "flag-my"));            Countries.Add(new CountryList(20, "d", "New Zealand", "flag-nz"));            Countries.Add(new CountryList(21, "d", "Norway", "flag-no"));            Countries.Add(new CountryList(22, "d", "Poland", "flag-pl"));            Countries.Add(new CountryList(23, "e", "Romania", "flag-ro"));            Countries.Add(new CountryList(24, "e", "Singapore", "flag-sg"));            Countries.Add(new CountryList(25, "e", "Thailand", "flag-th"));            Countries.Add(new CountryList(26, "e", "Ukraine", "flag-ua"));            this.dropdownlist1.DataSource = Countries;        }        [Serializable]        class CountryList        {            public int Value;            public string ParentId;            public string Text;            public string Sprite;            public CountryList(int cvalue, string cid, string ctext, string sprt)            {                this.Value = cvalue;                this.ParentId = cid;                this.Text = ctext;                this.Sprite = sprt;            }        }        [Serializable]        class GroupsList        {            public string ParentId;            public string Text;            public GroupsList(string gID, string gtext)            {                this.ParentId = gID;                this.Text = gtext;            }        }</td></tr>
</table>


Output of the above steps



![](cascading-support-_images\cascading-support-_img2.png)

_Figure_ _53__27__: Dropdown with cascade property_  

## Multiple Cascading support

Using multi cascade option, you can create a behavior of cascade between dropdown list controls. To achieve this, map the common field from table to “**fields**” property of all the dropdown lists. Also, specify the ID of cascading **DropDownList** in “**cascadeTo”** property of parent **DropDownList**. 

> ![C:\Users\ApoorvahR\Desktop\Note.png](cascading-support-_images\cascading-support-_img3.png)_**Note: In case, when you want to show the cascading dropdowns in disabled state initially, then set the value of enable property as “false” in each cascading dropdowns. It is then enabled automatically once a value is selected in parent (first) dropdown list.**_

The following steps explains you the behavior of multiple cascade dropdown.

* In an **HTML** page, add a &lt;input&gt; element to configure **DropDownList** widget.



{% highlight html %}

**[HTML]**
<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Continent</span>
    <input id="groupsList" type="text" />
</div>
<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Country</span>
    <input id="countryList" type="text" />
</div>
<div class="control" style="float: left; padding:10px;">
    <span class="txt">Select Capital</span>
    <input id="capitalList" type="text" />
</div>

**[JavaScript]**
<script type="text/javascript">
    $(function () {
        // declaration
        var groups = [
        { parentId: 'a', text: "Africa" },
        { parentId: 'b', text: "Asia" },
        { parentId: 'c', text: "Europe" },
        { parentId: 'd', text: "North America" },
        { parentId: 'e', text: "South America" },
        { parentId: 'f', text: "Oceania" },
        { parentId: 'g', text: "Antarctica" }]
        //Countries List
        var countries = [
        { value: 11, parentId: 'a', text: "Algeria" },
        { value: 12, parentId: 'a', text: "Egypt" },
        { value: 13, parentId: 'b', text: "Armenia" },
        { value: 14, parentId: 'b', text: "Bangladesh" },
        { value: 15, parentId: 'b', text: "India" },
        { value: 16, parentId: 'c', text: "Denmark" },
        { value: 17, parentId: 'c', text: "Finland" },
        { value: 18, parentId: 'd', text: "Cuba" },
        { value: 19, parentId: 'd', text: "USA" },
        { value: 20, parentId: 'e', text: "Brazil" },
        { value: 21, parentId: 'e', text: "Peru" },
        { value: 22, parentId: 'f', text: "Australia" },
        { value: 23, parentId: 'f', text: "New Zealand" },
        { value: 24, parentId: 'g', text: "French Southern" },
        { value: 25, parentId: 'g', text: "South Georgia" }]
        //Capital List
        var capital = [
        { value: 111, parentId: 'a', text: "Algiers" },
        { value: 112, parentId: 'a', text: "Cairo" },
        { value: 113, parentId: 'b', text: "Yerevan" },
        { value: 114, parentId: 'b', text: "Dhaka" },
        { value: 115, parentId: 'b', text: "New Delhi" },
        { value: 116, parentId: 'c', text: "Copenhagen" },
        { value: 117, parentId: 'c', text: "Helsinki" },
        { value: 118, parentId: 'd', text: "Havana" },
        { value: 119, parentId: 'd', text: "Washington, D.C." },
        { value: 120, parentId: 'e', text: "Brasília" },
        { value: 121, parentId: 'e', text: "Lima" },
        { value: 122, parentId: 'f', text: "Canberra" },
        { value: 123, parentId: 'f', text: "Wellington" },
        { value: 124, parentId: 'g', text: "Alfred Faure" },
        { value: 125, parentId: 'g', text: "King Edward Point" }]
        $('#groupsList').ejDropDownList({
            dataSource: groups,
            fields: { value: "parentId" },
**cascadeTo: 'countryList,capitalList'**
        });
        $('#countryList').ejDropDownList({
            dataSource: countries,
            fields: { value: "parentId" },
            enabled:false
        });
        $('#capitalList').ejDropDownList({
dataSource: capital,
fields: { value: "parentId" },
            enabled:false
        });
    });
</script>


{% endhighlight %}

****

**[CSHTML]**

&lt;div class="control" style="float: left; padding:10px;"&gt;

    <span class="txt">Select Continent</span>

    @Html.EJ().DropDownList("groupsList").Datasource((IEnumerable<groups>)ViewBag.datasource).DropDownListFields(f => f.Value("parentId")).CascadeTo("countryList,capitalList")

&lt;/div&gt;

&lt;div class="control" style="float: left; padding:10px;"&gt;

    <span class="txt">Select Country</span>

    @Html.EJ().DropDownList("countryList").Datasource((IEnumerable<Countries>)ViewBag.datasource1).Enabled(false)

&lt;/div&gt;

&lt;div class="control" style="float: left; padding:10px;"&gt;

    <span class="txt">Select Capital</span>

    @Html.EJ().DropDownList("capitalList").Datasource((IEnumerable<Countries>)ViewBag.datasource2).Enabled(false)

&lt;/div&gt;

**[CS]**        

public ActionResult Index()

{

    List<groups> group = new List<groups>();

    group.Add(new groups { parentId = "a", text = "Africa" });

    group.Add(new groups { parentId = "b", text = "Asia" });

    group.Add(new groups { parentId = "c", text = "Europe" });

    group.Add(new groups { parentId = "d", text = "North America" });

    group.Add(new groups { parentId = "e", text = "South America" });

    group.Add(new groups { parentId = "f", text = "Oceania" });

    group.Add(new groups { parentId = "g", text = "Antarctica" });

    ViewBag.datasource = group;

    List<Countries> country = new List<Countries>();

    country.Add(new Countries { value = 11, parentId = "a", text = "Algeria" });

    country.Add(new Countries { value = 12, parentId = "a", text = "Egypt" });

    country.Add(new Countries { value = 13, parentId = "b", text = "Armenia" });

    country.Add(new Countries { value = 14, parentId = "b", text = "Bangladesh" });

    country.Add(new Countries { value = 15, parentId = "b", text = "India" });

    country.Add(new Countries { value = 16, parentId = "c", text = "Denmark" });

    country.Add(new Countries { value = 17, parentId = "c", text = "Finland" });

    country.Add(new Countries { value = 18, parentId = "d", text = "Cuba" });

    country.Add(new Countries { value = 19, parentId = "d", text = "USA" });

    country.Add(new Countries { value = 20, parentId = "e", text = "Brazil" });

    country.Add(new Countries { value = 21, parentId = "e", text = "Peru" });

    country.Add(new Countries { value = 22, parentId = "f", text = "Australia" });

    country.Add(new Countries { value = 23, parentId = "f", text = "New Zealand" });

    country.Add(new Countries { value = 24, parentId = "g", text = "French Southern" });

    country.Add(new Countries { value = 25, parentId = "g", text = "South Georgia" });

    ViewBag.datasource1 = country;

    List<Countries> capital = new List<Countries>();

    capital.Add(new Countries { value = 111, parentId = "a", text = "Algiers" });

    capital.Add(new Countries { value = 112, parentId = "a", text = "Cairo" });

    capital.Add(new Countries { value = 113, parentId = "b", text = "Yerevan"});

    capital.Add(new Countries { value = 114, parentId = "b", text = "Dhaka" });

    capital.Add(new Countries { value = 115, parentId = "b", text = "New Delhi" });

    capital.Add(new Countries { value = 116, parentId = "c", text = "Copenhagen" });

    capital.Add(new Countries { value = 117, parentId = "c", text = "Helsinki" });

    capital.Add(new Countries { value = 118, parentId = "d", text = "Havana" });

    capital.Add(new Countries { value = 119, parentId = "d", text = "Washington, D.C." });

    capital.Add(new Countries { value = 120, parentId = "e", text = "Brasília" });

    capital.Add(new Countries { value = 121, parentId = "e", text = "Lima" });

    capital.Add(new Countries { value = 122, parentId = "f", text = "Canberra" });

    capital.Add(new Countries { value = 123, parentId = "f", text = "Wellington" });

    capital.Add(new Countries { value = 124, parentId = "g", text = "Alfred Faure" });

    capital.Add(new Countries { value = 125, parentId = "g", text = "King Edward Point" });

    ViewBag.datasource2 = capital;

    return View();

}



public class groups

{

    public string text { get; set; }

    public string parentId { get; set; }

}



public class Countries

{

    public string text { get; set; }

    public int value { get; set; }

    public string parentId { get; set; }

}





**[ASPX]**

// Add Dropdown list widget in ASPX page

&lt;asp:Content ID="BodyContent" runat="server" ContentPlaceHolderID="MainContent"&gt;

    &lt;div class="control" style="float: left; padding:10px;"&gt;

        <span class="txt">Select Continent</span>

        &lt;ej:DropDownList ID="groupsList" runat="server" DataValueField="parentId"&gt;&lt;/ej:DropDownList&gt;

    &lt;/div&gt;

    &lt;div class="control" style="float: left; padding:10px;"&gt;

        <span class="txt">Select Country</span>

        &lt;ej:DropDownList ID="countryList" runat="server" Enabled="false"&gt;&lt;/ej:DropDownList&gt;

    &lt;/div&gt;

    &lt;div class="control" style="float: left; padding:10px;"&gt;

        <span class="txt">Select Capital</span>

        &lt;ej:DropDownList ID="capitalList" runat="server" Enabled="false"&gt;&lt;/ej:DropDownList&gt;

    &lt;/div&gt;

&lt;/asp:Content&gt;

**[CS]**

// Initialize the control in CS page

        protected void Page_Load(object sender, EventArgs e)

        {

            List<string> cascade=new List<string>{"countryList", "capitalList"};

            List<GroupsList> groups = new List<GroupsList>();

            groups.Add(new GroupsList("a", "Africa"));

            groups.Add(new GroupsList("b", "Asia"));

            groups.Add(new GroupsList("c", "Europe"));

            groups.Add(new GroupsList("d", "North America"));

            groups.Add(new GroupsList("e", "South America"));

            groups.Add(new GroupsList("f", "Oceania"));

            groups.Add(new GroupsList("g", "Antarctica"));

            this.groupsList.DataSource = groups;

            this.groupsList.CascadeTo = "countryList,capitalList";



            List<CountryList> countries = new List<CountryList>();

            countries.Add(new CountryList (11, "a", "Algeria" ));

            countries.Add(new CountryList (12, "a", "Egypt" ));

            countries.Add(new CountryList (13, "b", "Armenia" ));

            countries.Add(new CountryList (14, "b", "Bangladesh" ));

            countries.Add(new CountryList (15, "b", "India" ));

            countries.Add(new CountryList (16, "c", "Denmark" ));

            countries.Add(new CountryList (17, "c", "Finland" ));

            countries.Add(new CountryList (18, "d", "Cuba" ));

            countries.Add(new CountryList (19, "d", "USA" ));

            countries.Add(new CountryList (20, "e", "Brazil" ));

            countries.Add(new CountryList (21, "e", "Peru" ));

            countries.Add(new CountryList (22, "f", "Australia" ));

            countries.Add(new CountryList (23, "f", "New Zealand" ));

            countries.Add(new CountryList (24, "g", "French Southern" ));

            countries.Add(new CountryList (25, "g", "South Georgia" ));

            this.countryList.DataSource = countries;



            List<CountryList> capital = new List<CountryList>();

            capital.Add(new CountryList (111, "a", "Algiers" ));

            capital.Add(new CountryList (112, "a", "Cairo" ));

            capital.Add(new CountryList (113, "b", "Yerevan" ));

            capital.Add(new CountryList (114, "b", "Dhaka" ));

            capital.Add(new CountryList (115, "b", "New Delhi" ));

            capital.Add(new CountryList (116, "c", "Copenhagen" ));

            capital.Add(new CountryList (117, "c", "Helsinki" ));

            capital.Add(new CountryList (118, "d", "Havana" ));

            capital.Add(new CountryList (119, "d", "Washington, D.C." ));

            capital.Add(new CountryList (120, "e", "Brasília" ));

            capital.Add(new CountryList (121, "e", "Lima" ));

            capital.Add(new CountryList (122, "f", "Canberra" ));

            capital.Add(new CountryList (123, "f", "Wellington" ));

            capital.Add(new CountryList (124, "g", "Alfred Faure" ));

            capital.Add(new CountryList (125, "g", "King Edward Point" ));

            this.capitalList.DataSource = capital;

        }

        class CountryList

        {

            public int value;

            public string parentId;

            public string text;

            public CountryList(int cvalue, string cid, string ctext)

            {

                this.value = cvalue;

                this.parentId = cid;

                this.text = ctext;

            }

        }

        [Serializable]

        class GroupsList

        {

            public string parentId;

            public string text;

            public GroupsList(string gID, string gtext)

            {

                this.parentId = gID;

                this.text = gtext;

            }

        }



The following screenshot displays the output of the above code example.

{% include image.html url="\js\DropDownList\concepts-and-features\cascading-support-_images\cascading-support-_img4.png" Caption="Figure 5428: Dropdown with multiple cascading"%}

