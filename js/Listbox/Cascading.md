---
layout: post
title: Cascading in ListBox widget for Syncfusion Essential JS
description: Dynamically populate data in a ListBox while selecting an item in another ListBox.
platform: js
control: ListBox
documentation: ug
keywords: ejlistbox, listbox, listbox widget, js listbox, jquery listbox, listbox ui, ej listbox, essential javascript listbox, web listbox,
---

# Cascading

We can dynamically populate data of a list box while selecting an item in another list box i.e. rendering child list box based on the item selection in parent list box. This can be achieved using “cascadeTo” property.

Create the UL elements to render both the parent and the child ListBox widget as below.

{% highlight html %}


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

{% highlight js %}


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



The parent ListBox widget’s “cascadeTo” API should point to its child ListBox****widget by specifying the id of the child ListBox widget. The child ListBox widget can be displayed with empty data on initialize by setting its “loadDataOnInit” property to false.

N> In the below data source definition, the “categoryId” column will act as a primary key to define the parent-child relationship.

## Multilevel cascading

Please refer the below code snippets which is expanded from the above example, to achieve multi-level (three level here) cascading of the ListBox widgets.

Create the UL elements to render the parent and the child ListBox widgets as below.

{% highlight html %}


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
    <ul id="subproductList"></ul>
</div>


{% endhighlight %}


Create the ListBox widgets as below.

{% highlight js %}

$(function() {
      // datasource for parent listbox
      var data = [{
          categoryId: 'a',
          text: "Clothing"
      }, {
          categoryId: 'b',
          text: "Furniture"
      }];

      //datasource for first level child
      var firstLevelChildData = [{
          subCategoryId: 11,
          categoryId: 'a',
          text: "Men"
      }, {
          subCategoryId: 12,
          categoryId: 'a',
          text: "Women"
      }, {
          subCategoryId: 13,
          categoryId: 'b',
          text: "Home furniture"
      }, {
          subCategoryId: 14,
          categoryId: 'b',
          text: "Bedding"
      }, ];

      //datasource for second level child
      var secondLevelChildData = [{
          productid: 101,
          subCategoryId: 11,
          text: "men shirts"
      }, {
          productid: 102,
          subCategoryId: 11,
          text: "men pants"
      }, {
          productid: 103,
          subCategoryId: 12,
          text: "Women shirts"
      }, {
          productid: 104,
          subCategoryId: 12,
          text: "Women pants"
      }, {
          productid: 105,
          subCategoryId: 13,
          text: "sofa"
      }, {
          productid: 106,
          subCategoryId: 13,
          text: "chairs"
      }, {
          productid: 107,
          subCategoryId: 14,
          text: "bedsheets"
      }, {
          productid: 108,
          subCategoryId: 14,
          text: "pillows"
      }, ];

      //datasource for third level child
      var thirdLevelChildData = [{
          productid: 101,
          text: "red men shirts"
      }, {
          productid: 101,
          text: "blue men shirts"
      }, {
          productid: 102,
          text: "red men pants"
      }, {
          productid: 102,
          text: "blue men pants"
      }, {
          productid: 103,
          text: "blueWomen shirts"
      }, {
          productid: 103,
          text: "red Women shirts"
      }, {
          productid: 104,
          text: "red women pants"
      }, {
          productid: 104,
          text: "blue women pants"
      }, {
          productid: 105,
          text: "red sofa"
      }, {
          productid: 105,
          text: "blue sofa"
      }, {
          productid: 106,
          text: "red chairs"
      }, {
          productid: 106,
          text: "blue chairs"
      }, {
          productid: 107,
          text: "red bedsheets"
      }, {
          productid: 107,
          text: "blue bedsheets"
      }, {
          productid: 108,
          text: "red pillows"
      }, {
          productid: 108,
          text: "blue pillows"
      }]

      //create parent listbox
      //cascadeTo property specifies the id of the child listbox (first level)
      $('#category').ejListBox({
          dataSource: data,
          fields: {
              value: "categoryId"
          },
          cascadeTo: 'subcategoryList'
      });

      //create first level child listbox
      //cascadeTo property specifies the id of the child listbox (second level)
      $('#subcategoryList').ejListBox({
          dataSource: firstLevelChildData,
          fields: {
              value: "subCategoryId"
          },
          loadDataOnInit: false,
          cascadeTo: 'productList'
      });

      //create second level child listbox
      //cascadeTo property specifies the id of the child listbox (third level)
      $('#productList').ejListBox({
          dataSource: secondLevelChildData,
          fields: {
              value: "productid"
          },
          loadDataOnInit: false,
          cascadeTo: 'subproductList'
      });

      //create third level child listbox
      $('#subproductList').ejListBox({
          dataSource: thirdLevelChildData,
          loadDataOnInit: false,
      });
  });

{% endhighlight %}





