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

1. Header

1. Sort In Ascending Order

2. Sort In Descending Order

3. Grouping

4. UnGrouping

2. Content

5. Add Record

6. Edit Record

7. Delete Record                  

3. Footer 

8. Next Page     

9. Last Page

10. Previous Page

11. First Page

## Context Menu action

To enable **Context Menu** in **Grid** use **enableContextMenu** property in **contextMenuSettings** at **Grid** initialize. The following code example illustrates you on how to set Context Menu.

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

{% include image.html url="/js/Grid/Concepts-and-Features/Context-Menu_images/Context-Menu_img1.png" Caption=""%}

_Context Menu in content_

**Header**

{% include image.html url="/js/Grid/Concepts-and-Features/Context-Menu_images/Context-Menu_img2.png" Caption=""%}

_Context Menu in Header_

**Footer**

{% include image.html url="/js/Grid/Concepts-and-Features/Context-Menu_images/Context-Menu_img3.png" Caption=""%}

_Context Menu in Footer_

