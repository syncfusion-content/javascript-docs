---
layout: post
title: Toolbar
description: toolbar 
platform: js
control: Grid
documentation: ug
---

# Toolbar 

## Default buttons

**Toolbar** is one of the user interaction controls related with **Grid**. It is handy to use the **Toolbar** to trigger more actions. The default toolbar items created for **Grid** are:

* Add
* Edit
* Delete
* Update
* Cancel
* Search

If you want **Toolbar** items other than the above items, you can make it using **customToolBarItems.**

## Custom Toolbar action

**Custom Toolbar** is a key functionality, used to customize **Toolbar** elements. Here you can learn in detail about the **Toolbar** template and its actions in the **Custom Toolbar** category. In the following code example, **ejDropDownList** is used to filter records by category. Using `customToolBarItems` and `templateID` property to enable custom toolbar in grid.

{% highlight html %}

<div id="Grid"></div>
<script id="Refresh" type="text/x-jsrender">
  <select id="products">
      <option value="">All</option>
      <option value="2">Drinks</option>
      <option value="4">Dairy Products</option>
      <option value="3">Packages</option>
  </select>
</script>
<script type="text/javascript">
  $(function () {// Document is ready.
      var dataManager = ej.DataManager({
          url: "http://mvc.syncfusion.com/Services/Northwnd.svc/Products"
      });
      var gridObj = $("#Grid").ejGrid({
          dataSource: dataManager,
          toolbarSettings: { showToolbar: true, customToolbarItems: [{ templateID: "#Refresh" }] },
          scrollSettings: { height: 300, width: "auto" },
          allowScrolling: true,
          columns: [
              { field: "ProductID", headerText: "Product ID", textAlign: "right", width: 100 },
              { field: "ProductName", headerText: "Product Name", width: 200 },
              { field: "QuantityPerUnit", headerText: "Quantity", textAlign: "right", width: 100 },
              { field: "UnitsOnOrder", headerText: "UnitsOnOrder", textAlign: "right", width: 100 }
          ]
  
      }).data("ejGrid");
      $("#products").ejDropDownList({
          selectedItemIndex: 0,
          change: function (args) {
              if (this.getSelectedValue() != "")
                  $("#Grid").ejGrid("model.query", new ej.Query().where("CategoryID", ej.FilterOperators.equal, parseInt(this.getSelectedValue(), 10)));
              else
                  $("#Grid").ejGrid("model.query", new ej.Query());
              gridObj.refreshContent(true);
          }
      });
  });
  
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Toolbar_images/Toolbar_img1.png"%}

