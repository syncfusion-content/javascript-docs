---
layout: post
title: Cascading
description: cascading
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Cascading

We can dynamically populate data of a list box while selecting an item in another list box i.e. rendering child list box based on the item selection in parent list box. This can be achieved using [cascadeTo](https://help.syncfusion.com/api/js/ejlistbox#members:cascadeto) property.

Create the UL elements to render both the parent and the child ListBox widget as below.

{% highlight html %}

        <style>
         .e-parent-listbox, .childlistbox {
             padding: 10px;
             float: left;
         }
        </style>
        
        <div class="controlitem">
            <!--parent listbox element-->
            <ul id="category"></ul>
        </div>

        <div class="controlitem">
            <!-- child listbox element-->
            <ul id="subcategoryList"></ul>
        </div>



{% endhighlight %}



The parent child relationship should be defined in data sources of both the list boxes. I.e. both data sources should contain a common field for mapping (just like [primary key and foreign key definitions](https://msdn.microsoft.com/en-IN/library/ms179610.aspx)). 

Create the ListBox widgets as below. 

{% highlight javascript %}


        $(function () {
            // datasource for parent listbox
            var data = [
                { categoryId: 'a', text: "Clothing" },
                { categoryId: 'b', text: "Furniture" }
            ];

            //datasource for child listbox
            var firstLevelChildData = [{ subCategoryId: 11, categoryId: 'a', text: "Men" },
                { subCategoryId: 12, categoryId: 'a', text: "Women" },
                { subCategoryId: 13, categoryId: 'b', text: "Home furniture" },
                { subCategoryId: 14, categoryId: 'b', text: "Bedding" },
            ];

            //create parent listbox
            //cascadeTo property specifies the id of the child listbox (first level)
            $('#category').ejListBox({
                dataSource: data,
                fields: { value: "categoryId" },
                cascadeTo: 'subcategoryList'
            });

            //create child listbox
            //cascadeTo property specifies the id of the child listbox
            $('#subcategoryList').ejListBox({
                dataSource: firstLevelChildData,
                loadDataOnInit: false
            });
        });



{% endhighlight %}

![](Cascading_images\Cascading_img1.png)


The parent ListBox widget’s “cascadeTo” API should point to its child ListBox widget by specifying the id of the child ListBox widget. The child ListBox widget can be displayed with empty data on initialize by setting its “loadDataOnInit” property to false.

N>  In the below data source definition, the “categoryId” column will act as a primary key to define the parent-child relationship.

## Multilevel cascading

Please refer the below code snippets which is expanded from the above example, to achieve multi-level (three level here) cascading of the ListBox widgets.

Create the UL elements to render the parent and the child ListBox widgets as below.

{% highlight html %}

     <style>
         .controlitem {
             float: left;
             padding: 10px;
         }
     </style>
        <div class="controlitem">
            <!--parent listbox element-->
            <ul id="category"></ul>
        </div>

        <div class="controlitem">
            <!--first level child listbox element-->
            <ul id="subcategoryList"></ul>
        </div>

        <div class="controlitem">
            <!--second level child listbox element-->
            <ul id="productList"></ul>
        </div>

        <div class="controlitem">
            <!--third level child listbox element-->
            <ul id="subProductList"></ul>
        </div>


{% endhighlight %}


Create the ListBox widgets as below.

{% highlight javascript %}

        $(function () {
            // datasource for parent listbox
            var data = [
                { categoryId: 'a', text: "Clothing" },
                { categoryId: 'b', text: "Furniture" }
            ];

            //datasource for first level child
            var firstLevelChildData = [{ subCategoryId: 11, categoryId: 'a', text: "Men" },
                { subCategoryId: 12, categoryId: 'a', text: "Women" },
                { subCategoryId: 13, categoryId: 'b', text: "Home furniture" },
                { subCategoryId: 14, categoryId: 'b', text: "Bedding" },
            ];

            //datasource for second level child
            var secondLevelChildData = [{ productId: 101, subCategoryId: 11, text: "men shirts" },
                { productId: 102, subCategoryId: 11, text: "men pants" },
                { productId: 103, subCategoryId: 12, text: "Women shirts" },
                { productId: 104, subCategoryId: 12, text: "Women pants" },
                { productId: 105, subCategoryId: 13, text: "sofa" },
                { productId: 106, subCategoryId: 13, text: "chairs" },
                { productId: 107, subCategoryId: 14, text: "bedsheets" },
                { productId: 108, subCategoryId: 14, text: "pillows" },
            ];

            //datasource for third level child
            var thirdLevelChildData = [{ productId: 101, text: "red men shirts" },
                { productId: 101, text: "blue men shirts" },
                { productId: 102, text: "red men pants" },
                { productId: 102, text: "blue men pants" },
                { productId: 103, text: "blueWomen shirts" },
                { productId: 103, text: "red Women shirts" },
                { productId: 104, text: "red women pants" },
                { productId: 104, text: "blue women pants" },
                { productId: 105, text: "red sofa" },
                { productId: 105, text: "blue sofa" },
                { productId: 106, text: "red chairs" },
                { productId: 106, text: "blue chairs" },
                { productId: 107, text: "red bedsheets" },
                { productId: 107, text: "blue bedsheets" },
                { productId: 108, text: "red pillows" },
                { productId: 108, text: "blue pillows" }
            ]

            //create parent listbox
            //cascadeTo property specifies the id of the child listbox (first level)
            $('#category').ejListBox({
                dataSource: data,
                fields: { value: "categoryId" },
                cascadeTo: 'subcategoryList'
            });

            //create first level child listbox
            //cascadeTo property specifies the id of the child listbox (second level)
            $('#subcategoryList').ejListBox({
                dataSource: firstLevelChildData,
                fields: { value: "subCategoryId" },
                loadDataOnInit: false,
                cascadeTo: 'productList'
            });

            //create second level child listbox
            //cascadeTo property specifies the id of the child listbox (third level)
            $('#productList').ejListBox({
                dataSource: secondLevelChildData,
                fields: { value: "productId" },
                loadDataOnInit: false,
                cascadeTo: 'subProductList'
            });

            //create third level child listbox
            $('#subProductList').ejListBox({
                dataSource: thirdLevelChildData,
                loadDataOnInit: false,
            });
        });

{% endhighlight %}

![](Cascading_images\Cascading_img2.png)



