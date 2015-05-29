---
layout: post
title: cascading-support-
description: cascading support 
platform: js
control: ListBox
documentation: ug
---

# Cascading Support 

Using cascade option, you can create a behaviour of cascade between **ListBox** controls. For this, create a database with single field that is common between two **ListBox** data fields and then mention that column id in value field. With this, you can set second **ListBox** id in **cascadeTo** property in first **ListBox**. 

In the following code example, in the first and second ListBox, "categoryid" is the common field. 

The "categoryid" value of the selected item in the First **Listbox** that matches with "categoryid" value in the second Listbox, is retreived and the item is loaded.


> ![Note](cascading-support-_images\cascading-support-_img1.png)_**Note: In case the second ListBox is to be disabled, until the first one is selected, you can set enable property as false in second ListBox that enables automatically once the value is selected in first one.**_ 

You can add any number of cascading **ListBoxes**. For this, create a Datasource with single field value that is common between the two consecutive cascading ListBoxes and cascading is achieved based on that common field.”  

The following steps explains you the behaviour of cascade **ListBox**. 

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.


<table>
<tr>
<td>
<b>[HTML]  </b>&lt;div id="control"&gt;    &lt;div class="controlitem"&gt;    <h6>Cascading Listboxes</h6>    &lt;ul id="groupsList"&gt;&lt;/ul&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        &lt;ul id="subcategoryList"&gt;&lt;/ul&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        &lt;ul id="productList"&gt;&lt;/ul&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        &lt;ul id="subproductList"&gt;&lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    var target;    $(function () {        // declaration        var groups = [        { categoryid: 'a', text: "Clothing" },        { categoryid: 'b', text: "Furniture" }]        //first level child        var category = [{ subcategoryid: 11, categoryid: 'a', text: "Men" },        { subcategoryid: 12, categoryid: 'a', text: "Women" },        { subcategoryid: 13, categoryid: 'b', text: "Home furniture" },        { subcategoryid: 14, categoryid: 'b', text: "Bedding" },        ]        //second level child        var subcategory = [{ productid: 101, subcategoryid: 11, text: "men shirts" },        { productid: 102, subcategoryid: 11, text: "men pants" },        { productid: 103, subcategoryid: 12, text: "Women shirts" },        { productid: 104, subcategoryid: 12, text: "Women pants" },        { productid: 105, subcategoryid: 13, text: "sofa" },        { productid: 106, subcategoryid: 13, text: "chairs" },        { productid: 107, subcategoryid: 14, text: "bedsheets" },        { productid: 108, subcategoryid: 14, text: "pillows" },        ]        //third level child        var subproduct = [{ productid: 101, text: "red men shirts" },        { productid: 101, text: "blue men shirts" },        { productid: 102, text: "red men pants" },        { productid: 102, text: "blue men pants" },        { productid: 103, text: "blueWomen shirts" },        { productid: 103, text: "red Women shirts" },        { productid: 104, text: "red women pants" },        { productid: 104, text: "blue women pants" },        { productid: 105, text: "red sofa" },        { productid: 105, text: "blue sofa" },        { productid: 106, text: "red chairs" },        { productid: 106, text: "blue chairs" },        { productid: 107, text: "red bedsheets" },        { productid: 107, text: "blue bedsheets" },        { productid: 108, text: "red pillows" },        { productid: 108, text: "blue pillows" }        ]        $('#groupsList').ejListBox({            dataSource: groups,            fields: { value: "categoryid" },            cascadeTo: 'subcategoryList'        });        $('#subcategoryList').ejListBox({            dataSource: category,            fields: { value: "subcategoryid" },            enabled: false,            cascadeTo: 'productList'        });        $('#productList').ejListBox({            dataSource: subcategory,            fields: { value: "productid" },            enabled: false,            cascadeTo: 'subproductList'        });        $('#subproductList').ejListBox({            dataSource: subproduct,            enabled: false,        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View] </b>// Add the following code in View page to configure ListBox widget&lt;div class="controlitem"&gt;    <span class="txt">Cascading Listboxes</span>    @Html.EJ().ListBox("groupsList").Datasource((IEnumerable<groups>)ViewBag.datasource).ListBoxFields(df => df.Value("categoryid")).<b>CascadeTo</b>("subcategoryList")&lt;/div&gt;&lt;div class="controlitem"&gt;    @Html.EJ().ListBox("subcategoryList").Datasource((IEnumerable<category>)ViewBag.datasource1).ListBoxFields(df => df.Value("subcategoryid")).<b>CascadeTo("productList")</b>.Enabled(false)&lt;/div&gt;&lt;div class="controlitem"&gt;    @Html.EJ().ListBox("productList").Datasource((IEnumerable<subCategory>)ViewBag.datasource2).ListBoxFields(df => df.Value("productid")).<b>CascadeTo("subproductList")</b>.Enabled(false)&lt;/div&gt;&lt;div class="controlitem"&gt;    @Html.EJ().ListBox("subproductList").Datasource((IEnumerable<subProduct>)ViewBag.datasource3).Enabled(false)&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS] </b><b>//</b> Add the following code to add list items in the controller page  public partial class ListBoxController : Controller    {        List<groups> group = new List<groups>();        List<category> firstLevel = new List<category>();        List<subCategory> secondLevel = new List<subCategory>();        List<subProduct> thirdLevel = new List<subProduct>();        public ActionResult Cascading()        {            group.Add(new groups { categoryid = "a", text = "Clothing" });            group.Add(new groups { categoryid = "b", text = "Furniture" });            ViewBag.datasource = group;            //first level child            firstLevel.Add(new category { subcategoryid = 11, categoryid = "a", text = "Women" });            firstLevel.Add(new category { subcategoryid = 12, categoryid = "b", text = "Home furniture" });            firstLevel.Add(new category { subcategoryid = 13, categoryid = "b", text = "Bedding" });            ViewBag.datasource1 = firstLevel;            //second level child            secondLevel.Add(new subCategory { productid = 101, subcategoryid = 11, text = "men shirts" });            secondLevel.Add(new subCategory { productid = 102, subcategoryid = 11, text = "men pants" });            secondLevel.Add(new subCategory { productid = 103, subcategoryid = 12, text = "women shirts" });            secondLevel.Add(new subCategory { productid = 104, subcategoryid = 12, text = "women pants" });            secondLevel.Add(new subCategory { productid = 105, subcategoryid = 13, text = "sofa" });            secondLevel.Add(new subCategory { productid = 106, subcategoryid = 13, text = "chairs" });            secondLevel.Add(new subCategory { productid = 106, subcategoryid = 14, text = "bedsheets" });            secondLevel.Add(new subCategory { productid = 108, subcategoryid = 14, text = "pillows" });            ViewBag.datasource2 = secondLevel;            //third level child            thirdLevel.Add(new subProduct { productid = 101, text = "red men shirts" });            thirdLevel.Add(new subProduct { productid = 101, text = "blue men shirts" });            thirdLevel.Add(new subProduct { productid = 102, text = "red men pants" });            thirdLevel.Add(new subProduct { productid = 102, text = "blue men pants" });            thirdLevel.Add(new subProduct { productid = 103, text = "blue women shirts" });            thirdLevel.Add(new subProduct { productid = 103, text = "red women shirts" });            thirdLevel.Add(new subProduct { productid = 104, text = "red women pants" });            thirdLevel.Add(new subProduct { productid = 104, text = "blue women pants" });            thirdLevel.Add(new subProduct { productid = 105, text = "red sofa" });            thirdLevel.Add(new subProduct { productid = 105, text = "blue sofa" });            thirdLevel.Add(new subProduct { productid = 106, text = "red chairs" });            thirdLevel.Add(new subProduct { productid = 106, text = "blue chairs" });            thirdLevel.Add(new subProduct { productid = 107, text = "red bedsheets" });            thirdLevel.Add(new subProduct { productid = 107, text = "blue bedsheets" });            thirdLevel.Add(new subProduct { productid = 108, text = "red pillows" });            thirdLevel.Add(new subProduct { productid = 108, text = "blue pillows" });            ViewBag.datasource3 = thirdLevel;            return View();}</td></tr>
<tr>
<td>
<b>[Model]  </b>public class groups{    public string text { get; set; }    public string categoryid { get; set; }}public class category{    public string text { get; set; }    public string categoryid { get; set; }    public int subcategoryid { get; set; }}public class subCategory{    public string text { get; set; }    public int productid { get; set; }    public int subcategoryid { get; set; }}public class subProduct{    public string text { get; set; }    public int productid { get; set; }}</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]  </b>// In an ASPX page, add a ListBox control&lt;div id="control"&gt;    &lt;div class="controlitem"&gt;        &lt;h6&gt;            Cascading Listboxes</h6>        &lt;ej:listbox id="groupsList" datavaluefield="CategoryId" datatextfield="Text" cascadeto="subcategoryList" runat="server"&gt;&lt;/ej:listbox&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        <ej:listbox id="subcategoryList" <b>cascadeto="productList"</b> datavaluefield="SubcategoryId"            datatextfield="Text" enabled="false" runat="server">&lt;/ej:listbox&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        &lt;ej:listbox id="productList" cascadeto="subproductList" datavaluefield="ProductId" datatextfield="Text" enabled="false" runat="server"&gt;&lt;/ej:listbox&gt;    &lt;/div&gt;    &lt;div class="controlitem"&gt;        &lt;ej:listbox id="subproductList" datavaluefield="ProductId" datatextfield="Text" enabled="false" runat="server"&gt;&lt;/ej:listbox&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS]</b><b>// </b>Initialize the control in <b>CS</b>protected void Page_Load(object sender, EventArgs e)        {            groupsList.DataSource = GetGroup();            subcategoryList.DataSource = GetCategory();            productList.DataSource = GetSubCategory();            subproductList.DataSource = GetSubProduct();        }        private List<Groups> GetGroup()        {            List<Groups> datas = new List<Groups>();            datas.Add(new Groups() { CategoryId = "a", Text = "Clothing" });            datas.Add(new Groups() { CategoryId = "b", Text = "Furniture" });            return datas;        }        private List<Category> GetCategory()        {            List<Category> datas = new List<Category>();            datas.Add(new Category() { SubcategoryId = 11, CategoryId = "a", Text = "Men" });            datas.Add(new Category() { SubcategoryId = 12, CategoryId = "a", Text = "Women" });            datas.Add(new Category() { SubcategoryId = 13, CategoryId = "b", Text = "Home furniture" });            datas.Add(new Category() { SubcategoryId = 14, CategoryId = "b", Text = "Bedding" });            return datas;        }        private List<SubCategory> GetSubCategory()        {            List<SubCategory> datas = new List<SubCategory>();            datas.Add(new SubCategory() { ProductId = 101, SubcategoryId = 11, Text = "men shirts" });            datas.Add(new SubCategory() { ProductId = 102, SubcategoryId = 11, Text = "men pants" });            datas.Add(new SubCategory() { ProductId = 103, SubcategoryId = 12, Text = "Women shirts" });            datas.Add(new SubCategory() { ProductId = 104, SubcategoryId = 12, Text = "Women pants" });            datas.Add(new SubCategory() { ProductId = 105, SubcategoryId = 13, Text = "sofa" });            datas.Add(new SubCategory() { ProductId = 106, SubcategoryId = 13, Text = "chairs" });            datas.Add(new SubCategory() { ProductId = 107, SubcategoryId = 14, Text = "bedsheets" });            datas.Add(new SubCategory() { ProductId = 108, SubcategoryId = 14, Text = "pillows" });            return datas;        }        private List<SubProduct> GetSubProduct()        {            List<SubProduct> datas = new List<SubProduct>();            datas.Add(new SubProduct() { ProductId = 101, Text = "red men shirts" });            datas.Add(new SubProduct() { ProductId = 101, Text = "blue men shirts" });            datas.Add(new SubProduct() { ProductId = 102, Text = "red men pants" });            datas.Add(new SubProduct() { ProductId = 102, Text = "blue men pants" });            datas.Add(new SubProduct() { ProductId = 103, Text = "blueWomen shirts" });            datas.Add(new SubProduct() { ProductId = 103, Text = "red Women shirts" });            datas.Add(new SubProduct() { ProductId = 104, Text = "red women pants" });            datas.Add(new SubProduct() { ProductId = 104, Text = "blue women pants" });            datas.Add(new SubProduct() { ProductId = 105, Text = "red sofa" });            datas.Add(new SubProduct() { ProductId = 105, Text = "blue sofa" });            datas.Add(new SubProduct() { ProductId = 106, Text = "red chairs" });            datas.Add(new SubProduct() { ProductId = 106, Text = "blue chairs" });            datas.Add(new SubProduct() { ProductId = 107, Text = "red bedsheets" });            datas.Add(new SubProduct() { ProductId = 107, Text = "blue bedsheets" });            datas.Add(new SubProduct() { ProductId = 108, Text = "red pillows" });            datas.Add(new SubProduct() { ProductId = 108, Text = "blue pillows" });            return datas;        }        public class Groups        {          public string Text, CategoryId;        }        public class Category        {          public int SubcategoryId;          public string Text, CategoryId;        }        public class SubCategory        {          public int ProductId, SubcategoryId;          public string Text;        }        public class SubProduct        {          public int ProductId;          public string Text;        }</td></tr>
</table>


Configure the styles as follows.



{% highlight css %}

**[CSS]**  
<style>
    .controlitem {
        margin-left: 50px;
        display: inline-block;
    }
</style>


{% endhighlight %}



Output of the above steps.



{% include image.html url="\js\Listbox\concepts-and-features\cascading-support-_images\cascading-support-_img2.png" Caption="Figure 3024: ListBox with cascade property"%}

