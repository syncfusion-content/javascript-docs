---
layout: post
title: Context-Menu
description: context menu
platform: js
control: Grid
documentation: ug
---

# Context Menu

**Context Menu** is one of the user interaction controls related with **Grid**. It is handy to use the **Context Menu** to trigger more actions. The default Context Menu items created for **Grid** are:

1. **Header**

* Sort In Ascending Order

* Sort In Descending Order

* Grouping

* UnGrouping

2. **Content**

* Add Record

* Edit Record

* Delete Record                  

3. **Footer** 

* Next Page     

* Last Page

* Previous Page

11. First Page

## Context Menu action

If you want to display only selected items in Context Menu to use `contextMenuItems` property in `contextMenuSettings`.  We can bind the actions of `contextMenuItems` in `contextClick` event at Grid. The following code example illustrates you on how to create Context Menu with selected items.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowPaging: true,
          allowGrouping: true,
          editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true, },
          contextMenuSettings : {enableContextMenu : true},
          columns: [
                  { field: "OrderID", headerText: "Order ID", textAlign:ej.TextAlign.Right },
                  { field: "CustomerID", headerText: "Employee ID" },
                  { field: " EmployeeID ", headerText: "Frieght", textAlign:ej.TextAlign.Right },
                  { field: "ShipCity", headerText: "Ship City", }
      ]
  
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

**Content**

{% include image.html url="/js/Grid/Context-Menu_images/Context-Menu_img1.png" Caption=""%}

_Context Menu in content_

**Header**

{% include image.html url="/js/Grid/Context-Menu_images/Context-Menu_img2.png" Caption=""%}

_Context Menu in Header_

**Footer**

{% include image.html url="/js/Grid/Context-Menu_images/Context-Menu_img3.png" Caption=""%}

_Context Menu in Footer_


##Context Menu Items

To enable the Context Menu feature, it shows all  options by default . If you want to display only selected items in Context Menu to use `contextMenuItems` property in `contextMenuSettings`. The following code example illustrates you on how to create Context Menu with selected items.
    
{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowPaging: true,
          allowGrouping: true,
          contextClick : "click",
          editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true, },
          contextMenuSettings : {enableContextMenu : true, contextMenuItems:["Add Record","Edit Record","Delete Record"]},
          columns: [
                  { field: "OrderID", headerText: "Order ID", textAlign:ej.TextAlign.Right },
                  { field: "CustomerID", headerText: "Employee ID" },
                  { field: " EmployeeID ", headerText: "Frieght", textAlign:ej.TextAlign.Right },
                  { field: "ShipCity", headerText: "Ship City", }
      ]
  
      });
  });
</script>


{% endhighlight %}

{% include image.html url="/js/Grid/Context-Menu_images/Context-Menu_img4.png" Caption=""%}

##Custom Context Menu

The Grid control has support to customize the context menu items using the `customContextMenuItems` property of the `contextMenuSettings`.To define the `customContextMenuItems` action by using `contextClick` event at Grid. The following code example illustrates you on how to create Custom Context Menu.

{% highlight html %}


<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowPaging: true,
          allowGrouping: true,
          contextClick : "click",
          editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true, },
          contextMenuSettings : {enableContextMenu : true, customContextMenuItems:["Add Record,Edit Record,Delete Record"]},
          columns: [
                  { field: "OrderID", headerText: "Order ID", textAlign:ej.TextAlign.Right },
                  { field: "CustomerID", headerText: "Employee ID" },
                  { field: " EmployeeID ", headerText: "Frieght", textAlign:ej.TextAlign.Right },
                  { field: "ShipCity", headerText: "Ship City", }
      ]
  
      });
  });
  function click(args){
      this.hideColumns("Order ID")
  }
</script>


{% endhighlight %}

{% include image.html url="/js/Grid/Context-Menu_images/Context-Menu_img5.png" Caption=""%}