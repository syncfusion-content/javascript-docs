---
layout: post
title: load-on-demand-support-
description: load-on-demand support 
platform: js
control: ListBox
documentation: ug
---

# Load-on-Demand support 

**ListBox** widget provides the Load-onDemand support, when binding the remote data for the **ListBox**. It loads partially, only a set of data from remote server loaded initially, and imports data further upon loading. To enable Load-onDemand support, set the **enableLoadOnDemand** property as true. You can set **itemsCount** that specifies number of items in the **ListBox**. You can load any number of items upon request with **itemRequest** ClientSide Event.

The following steps explains you the behaviour of Load-onDemand support in **ListBox**.

* In an **HTML** page, add a **&lt;li&gt; element** to configure **ListBox** widget.

_****_

<table>
<tr>
<td>
<b>[HTML]   </b>&lt;div class="control"&gt;    &lt;h5 class="ctrllabel"&gt; Select Customer ID</h5>    &lt;ul id="listboxSample"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript] </b><b>// </b>Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    jQuery(function ($) {        var dataManger = ej.DataManager({            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"        });        // Query creation        var query = ej.Query()                .from("Customers");        $('#listboxSample').ejListBox({            dataSource: dataManger,            fields: { text: "CustomerID" },            query: query, enableLoadOnDemand: true, itemsCount: 91, itemRequest: "itemRequested"        });});//Load set of items in itemRequested client-side method    function itemRequested(args) {        var target = $("#selectCar").data("ejListBox");        target.model.query = ej.Query().from("Customers").range(args.start, args.start + 20);        this.model.itemsCount = 20; //to load 20 items    }&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[View]  </b>// Add the following code in View page to configure ListBox widget&lt;div class="control"&gt;    &lt;h5 class="ctrllabel"&gt; Select Customer ID</h5>    @Html.EJ().ListBox("customerList").Datasource(ds => ds.URL("http://mvc.syncfusion.com/Services/Northwnd.svc/")).Query("ej.Query().from('Customers')").ListBoxFields(f => f.Text("CustomerID")).ItemsCount(91) .<b>EnableLoadOnDemand(true)</b>.ClientSideEvents(e => e.ItemRequest("itemRequested"))&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]  </b>// Initialize the control in JavaScript&lt;script type="text/javascript"&gt;    function itemRequested(args) {        var target = $("#customerList").data("ejListBox");        //to load 20 items        target.model.query = ej.Query().from('Customers').range(args.start, args.start + 20);        this.model.itemsCount = 20;    }&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX] </b>// In an ASPX page, add a ListBox control&lt;div class="control"&gt;    &lt;div class="ctrllabel"&gt;        Select Customer ID</div>    &lt;div class="control1" style="float: left;"&gt;        <ej:listbox id="listboxsample" DataTextField="CustomerID"  clientsideonitemrequest="itemRequested" <b>enableloadondemand="true"</b>itemscount="91" runat="server"> &lt;/ej:listbox&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[CS] </b><b>// </b>Add dataSource for the control in <b>CS</b><b> </b>        protected void Page_Load(object sender, EventArgs e)        {            this.listboxsample.DataSource = "http://mvc.syncfusion.com/Services/Northwnd.svc/";            this.listboxsample.Query = "ej.Query().from('Customers')";            }</td></tr>
<tr>
<td>
<b>[Javascript]  </b>// Load set of items in <b>itemRequested</b> client-side method&lt;script type="text/javascript"&gt;    function itemRequested(args) {        var target = $("#listboxsample").data("ejListBox");        target.model.query = ej.Query().from("Customers").range(args.start, args.start + 20);        this.model.itemsCount = 20; //to load 20 items    }&lt;/script&gt;</td></tr>
</table>


Output of the above steps.


{% include image.html url="\js\Listbox\concepts-and-features\load-on-demand-support-_images\load-on-demand-support-_img1.png" Caption="Figure 3125: ListBox with Load-onDemand"%}

