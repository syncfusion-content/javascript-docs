---
layout: post
title: Cascading-Support
description: cascading support 
platform: js
control: ListBox
documentation: ug
---

# Cascading Support 

Using cascade option, you can create a behaviour of cascade between **ListBox** controls. For this, create a database with single field that is common between two **ListBox** data fields and then mention that column id in value field. With this, you can set second **ListBox** id in **cascadeTo** property in first **ListBox**. 

In the following code example, in the first and second ListBox, "categoryid" is the common field. 

The "categoryid" value of the selected item in the First **Listbox** that matches with "categoryid" value in the second Listbox, is retreived and the item is loaded.


> {% include image.html url="/js/Listbox/Concepts-and-Features/Cascading-Support_images/Cascading-Support_img1.png" Caption=""%}

_**Note: In case the second ListBox is to be disabled, until the first one is selected, you can set enable property as false in second ListBox that enables automatically once the value is selected in first one.**_ 

You can add any number of cascading **ListBoxes**. For this, create a Datasource with single field value that is common between the two consecutive cascading ListBoxes and cascading is achieved based on that common field.”  

The following steps explains you the behaviour of cascade **ListBox**. 

* In an **HTML** page, add a **&lt;ul&gt; element** to configure **ListBox** widget.

{% highlight html %}


<div id="control">
    
<div class="controlitem">
    <h6>Cascading Listboxes</h6>

    <ul id="groupsList"></ul>
    </div>
    <div class="controlitem">
        <ul id="subcategoryList"></ul>
    </div>
    <div class="controlitem">
        <ul id="productList"></ul>
    </div>
    <div class="controlitem">
        <ul id="subproductList"></ul>
    </div>
</div>

{% endhighlight %}

{% highlight js %}

  
// Initialize the control in JavaScript

  <script type="text/javascript">
    var target;
    $(function () {
        // declaration
        var groups = [
        { categoryid: 'a', text: "Clothing" },
        { categoryid: 'b', text: "Furniture" }]

        //first level child
        var category = [{ subcategoryid: 11, categoryid: 'a', text: "Men" },
        { subcategoryid: 12, categoryid: 'a', text: "Women" },
        { subcategoryid: 13, categoryid: 'b', text: "Home furniture" },
        { subcategoryid: 14, categoryid: 'b', text: "Bedding" },
        ]
        //second level child

        var subcategory = [{ productid: 101, subcategoryid: 11, text: "men shirts" },
        { productid: 102, subcategoryid: 11, text: "men pants" },
        { productid: 103, subcategoryid: 12, text: "Women shirts" },
        { productid: 104, subcategoryid: 12, text: "Women pants" },
        { productid: 105, subcategoryid: 13, text: "sofa" },
        { productid: 106, subcategoryid: 13, text: "chairs" },
        { productid: 107, subcategoryid: 14, text: "bedsheets" },
        { productid: 108, subcategoryid: 14, text: "pillows" },
        ]

        //third level child
        var subproduct = [{ productid: 101, text: "red men shirts" },
        { productid: 101, text: "blue men shirts" },
        { productid: 102, text: "red men pants" },
        { productid: 102, text: "blue men pants" },
        { productid: 103, text: "blueWomen shirts" },
        { productid: 103, text: "red Women shirts" },
        { productid: 104, text: "red women pants" },
        { productid: 104, text: "blue women pants" },
        { productid: 105, text: "red sofa" },
        { productid: 105, text: "blue sofa" },
        { productid: 106, text: "red chairs" },
        { productid: 106, text: "blue chairs" },
        { productid: 107, text: "red bedsheets" },
        { productid: 107, text: "blue bedsheets" },
        { productid: 108, text: "red pillows" },
        { productid: 108, text: "blue pillows" }
        ]
        $('#groupsList').ejListBox({
            dataSource: groups,
            fields: { value: "categoryid" },
            cascadeTo: 'subcategoryList'
        });
        $('#subcategoryList').ejListBox({
            dataSource: category,
            fields: { value: "subcategoryid" },
            enabled: false,
            cascadeTo: 'productList'
        });

        $('#productList').ejListBox({
            dataSource: subcategory,
            fields: { value: "productid" },
            enabled: false,
            cascadeTo: 'subproductList'
        });
        $('#subproductList').ejListBox({
            dataSource: subproduct,
            enabled: false,
        });
    });
</script>

{% endhighlight %}

Configure the styles as follows.



{% highlight css %}

<style>
    .controlitem {
        margin-left: 50px;
        display: inline-block;
    }
</style>


{% endhighlight %}



Output of the above steps.



{% include image.html url="/js/Listbox/Concepts-and-Features/Cascading-Support_images/Cascading-Support_img2.png" Caption="Figure 24: ListBox with cascade property"%}

