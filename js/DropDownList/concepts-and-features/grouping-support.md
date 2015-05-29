---
layout: post
title: grouping-support
description: grouping support
platform: js
control: DropDownList
documentation: ug
---

# Grouping Support

**Grouping Support using DataSource**

**Grouping****DropDownList** items can be done by using **category** field. Set the **category** field and define it in the **DataSource**. Then map the fields for the data items of the **DropDownList** and set **allowGrouping** property value to **true**.

The following steps explain you how to group data items in the **DropDownList** control by using **DataSource**.

1. In an **HTML** page, add a **&lt;input&gt;** element to configure **DropDownList** widget.



{% highlight html %}

**[HTML]**

<input type="text" id="categoryGrouping" />     


{% endhighlight %}



2. Configure the **DataSource** and initialize the **DropDownList** widget in the Script section as follows.

{% highlight js %}

**[Script]**

      $(function () {
            var countries = [
               { country: "Austria", group: "A" },
               { country: "Australia", group: "A" }, { country: "Antarctica", group: "A" },
               { country: "Bangladesh", group: "B" }, { country: "Belgium", group: "B" },
               { country: "Brazil", group: "B" },
               { country: "Canada", group: "C" }, { country: "China", group: "C" },
               { country: "Cuba", group: "C" },
               { country: "Denmark", group: "D" }, { country: "Dominica", group: "D" },
               { country: "Europe", group: "E" }, { country: "Egypt", group: "E" },
               { country: "England", group: "E" },
               { country: "India", group: "I" }, { country: "Indonesia", group: "I" },
               { country: "Ireland", group: "I" }, { country: "Italy", group: "I" },
               { country: "France", group: "F" }, { country: "Finland", group: "F" },
               { country: "Germany", group: "G" }, { country: "Greece", group: "G" },
               { country: "Greenland", group: "G" }, { country: "Georgia", group: "G" },
               { country: "Haiti", group: "H" }, { country: "Hong Kong", group: "H" }
            ];
            $('#categoryGrouping').ejDropDownList({
                **dataSource: countries,**
                **fields: { text: "country", category: "group" },**
                **allowGrouping: true,**
                width: "150px",
            });
});


{% endhighlight %}



3. The above code example illustrates the following output.



{% include image.html url="\js\DropDownList\concepts-and-features\grouping-support_images\grouping-support_img1.png" Caption="Figure 5529: Grouping support by using DateaSource"%}

**Grouping Support using UL and LI structure**

Another way to group **DropDownList** is by using **UL** and **LI structure**. Here, you have to specify the group category in the **&lt;span&gt;** tag. The ID of the **&lt;div&gt;** tag should be given as the **targetId** for the **DropDownList** control. The following code example illustrates how to achieve Grouping in **DropDownList** control by using **UL and LI structure**.

1. Add the input element and the UL and LI structures to group the **DropDownList** control.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;input type="text" id="vegetable" /&gt;                        &lt;div id="vegetablelist"&gt;                            &lt;ul&gt;                                <span>Leafy and Salad</span>                                <li>Cabbage</li>                                <li>Pea</li>                                <li>Spinach</li>                                <li>Wheatgrass</li>                                <li>Yarrow &lt;/li&gt;                                <span>Beans</span>                                <li>Chickpea</li>                                <li>Green bean</li>                                  <span>Bulb and Stem</span>                                <li>Garlic</li>                                <li>Garlic Chives</li>                                 <span>Root and Tuberous</span>                                <li>Beetroot</li>                                <li>Carrot</li>                            &lt;/ul&gt;                        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[Script]</b><b>// You can initialize the DropDownList control in the script section and add the Target ID to the DropDownList as follows.</b>$('#vegetable').ejDropDownList({                 <b>targetID: "vegetablelist",</b>                 width:"150px",             });</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example in CSHTML page.</b>@Html.EJ().DropDownList("selectCar").Datasource((IEnumerable<Check.Models.Books>)ViewBag.datasource).DropDownListFields(df => df.ID("id").Text("text").Category("category")).Width("200px").AllowGrouping(true)</td></tr>
<tr>
<td>
<b>[CS]</b><b>// Define the DataSource in the controller page as follows.</b>List<Books> book = new List<Books>();        public ActionResult Index()        {            book.Add(new Books { id = 1,  text= "Austria", category= "A"});            book.Add(new Books { id = 2, text= "Australia", category= "A" });            book.Add(new Books { id = 3, text =  "Bangladesh", category= "B"  });            book.Add(new Books { id = 4, text = "Belgium", category= "B"  });            book.Add(new Books { id = 5, text = "Canada", category= "C" });            book.Add(new Books { id = 6, text = "Denmark", category= "D" });            book.Add(new Books { id = 7, text = "Egypt", category= "E"});            book.Add(new Books { id = 8, text = "England", category= "E" });            book.Add(new Books { id = 9, text = "India", category= "I"  });            book.Add(new Books { id = 10, text = "Italy", category= "I"  });            book.Add(new Books { id = 11, text = "Haiti", category= "H" });            book.Add(new Books { id = 12, text = "Jordan", category= "J" });            book.Add(new Books { id = 13, text = "Jamaica", category= "J" });            ViewBag.datasource = book;            return View();        }        public class Books        {            public int id { get; set; }            public string text { get; set; }            public string category { get; set; }        }</td></tr>
</table>




<table>
<tr>
<td>
<b>[ASPX]</b><b>// Add the following code example in the ASPX page.</b>            &lt;ej:DropDownList ID="dropdownlist" Width="200px"  runat="server" DataIdField="Id" DataTextField="Text"&gt;&lt;/ej:DropDownList&gt;</td></tr>
<tr>
<td>
<b> [CS]</b><b>// Define the DataSource in the controller page as follows.</b>List<Books> book = new List<Books>();        public ActionResult Index()        {            book.Add(new Books { id = 1,  text= "Austria", category= "A"});            book.Add(new Books { id = 2, text= "Australia", category= "A" });            book.Add(new Books { id = 3, text =  "Bangladesh", category= "B"  });            book.Add(new Books { id = 4, text = "Belgium", category= "B"  });            book.Add(new Books { id = 5, text = "Canada", category= "C" });            book.Add(new Books { id = 6, text = "Denmark", category= "D" });            book.Add(new Books { id = 7, text = "Egypt", category= "E"});            book.Add(new Books { id = 8, text = "England", category= "E" });            book.Add(new Books { id = 9, text = "India", category= "I"  });            book.Add(new Books { id = 10, text = "Italy", category= "I"  });            book.Add(new Books { id = 11, text = "Haiti", category= "H" });            book.Add(new Books { id = 12, text = "Jordan", category= "J" });            book.Add(new Books { id = 13, text = "Jamaica", category= "J" });            ViewBag.datasource = book;            return View();        }        public class Books        {            public int id { get; set; }            public string text { get; set; }            public string category { get; set; }        }</td></tr>
</table>


{% include image.html url="\js\DropDownList\concepts-and-features\grouping-support_images\grouping-support_img2.png" Caption="Figure 5630: Grouping in Dropdownlist by using UL and LI structure "%}

