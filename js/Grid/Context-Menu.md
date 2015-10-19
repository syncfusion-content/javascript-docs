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

 **Header**

* Sort In Ascending Order

* Sort In Descending Order

* Grouping

* UnGrouping

 **Content**

* Add Record

* Edit Record

* Delete Record                  

 **Footer** 

* Next Page     

* Last Page

* Previous Page

* First Page

## Enable Context Menu 

To enable the default Context Menu feature using [`enableContextMenu`](/js/api/ejgrid#members:contextmenusettings-enablecontextmenu "enableContextMenu") property in [`contextMenuSettings`](/js/api/ejgrid#members:contextmenusettings "contextMenuSettings") at **Grid**. The following code example explains you on how to enable Context Menu in Grid .

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

![](/js/Grid/Context-Menu_images/Context-Menu_img1.png" Caption=")

_Context Menu in content_

**Header**

![](/js/Grid/Context-Menu_images/Context-Menu_img2.png" Caption=")

_Context Menu in Header_

**Footer**

![](/js/Grid/Context-Menu_images/Context-Menu_img3.png" Caption=")

_Context Menu in Footer_


##Context Menu Items

The Context Menu feature displays all the options by default . When you want to display only the selected items in the Context Menu, use [`contextMenuItems`](/js/api/ejgrid#members:contextmenusettings-contextmenuitems "contextMenuItems") property in [`contextMenuSettings`](/js/api/ejgrid#members:contextmenusettings "contextMenuSettings"). The following code example explains you on how to create Context Menu with selected items.
    
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

![](/js/Grid/Context-Menu_images/Context-Menu_img4.png" Caption=")

##Custom Context Menu

The Grid control has support to customize the context menu items by using the [`customContextMenuItems`](/js/api/ejgrid#members:contextmenusettings-customcontextmenuitems "customContextMenuItems") property of the [`contextMenuSettings`](/js/api/ejgrid#members:contextmenusettings "contextMenuSettings").To define the [`customContextMenuItems`](/js/api/ejgrid#members:contextmenusettings-customcontextmenuitems "customContextMenuItems") action, use [`contextClick`](/js/api/ejgrid#events:contextclick "contextClick") event in the Grid. The following code example explains you on how to create Custom Context Menu.

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
          contextMenuSettings : {enableContextMenu : true, customContextMenuItems:["HideColumns"]},
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

![](/js/Grid/Context-Menu_images/Context-Menu_img5.png" Caption=")