---
layout: post
title: Load-on-Demand-support
description: load-on-demand support 
platform: js
control: ListBox
documentation: ug
---

# Load-on-Demand support 

**ListBox** widget provides the Load-onDemand support, when binding the remote data for the **ListBox**. It loads partially, only a set of data from remote server loaded initially, and imports data further upon loading. To enable Load-onDemand support, set the **enableLoadOnDemand** property as true. You can set **itemsCount** that specifies number of items in the **ListBox**. You can load any number of items upon request with **itemRequest** ClientSide Event.

The following steps explains you the behaviour of Load-onDemand support in **ListBox**.

* In an **HTML** page, add a **&lt;li&gt; element** to configure **ListBox** widget.


{% highlight html %}


<div class="control">
    <h5 class="ctrllabel"> Select Customer ID</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


// Initialize the control in JavaScript
<script type="text/javascript">
    jQuery(function ($) {
        var dataManger = ej.DataManager({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        // Query creation
        var query = ej.Query()
                .from("Customers");

        $('#listboxSample').ejListBox({
            dataSource: dataManger,
            fields: { text: "CustomerID" },
            query: query, enableLoadOnDemand: true, itemsCount: 91, itemRequest: "itemRequested"
        });
});
//Load set of items in itemRequested client-side method
    function itemRequested(args) {
        var target = $("#selectCar").data("ejListBox");
        target.model.query = ej.Query().from("Customers").range(args.start, args.start + 20);
        this.model.itemsCount = 20; //to load 20 items

    }
</script>

{% endhighlight %}

Output of the above steps.


{% include image.html url="/js/Listbox/Concepts-and-Features/Load-on-Demand-support_images/Load-on-Demand-support_img1.png" Caption="Figure 25: ListBox with Load-onDemand"%}

