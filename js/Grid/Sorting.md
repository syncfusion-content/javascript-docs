---
layout: post
title: Sorting
description: sorting
platform: js
control: Grid
documentation: ug
---

# Sorting

## Default Sorting

Sorting is a basic technique in **ejGrid**. It helps you view **Grid** records in ascending or descending, based on a particular column. If you want to enable sorting in **Grid** then use `allowSorting` property at **Grid** initialize. By default, sorting operation can be performed by **user interaction** (**UI**) on **Grid** header.

{% highlight html %}

<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowPaging: true,
      });
  });
</script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Sorting_images/Sorting_img1.png"%}

> _**Note**: EJGrid also has support to sort more than one column. This behavior is called as multi sorting. To enable this behavior in Grid then use `allowMultiSorting` in Grid._

## External Sorting

In **ejGrid**, you have an **API** to sort a column dynamically. The following code example shows you how to sort a column through **API**. 

{% highlight html %}


<select id="columns">
  <option value="OrderID">Order ID</option>
  <option value="CustomerID">Customer ID</option>
  <option value="EmployeeID">Employee ID</option>
  <option value="ShipCity">Ship City</option>
</select>
<br />
<select id="direction">
  <option>Ascending</option>
  <option>Descending</option>
</select>
<br />
<input type="button" value="sort" id="sort" />
<br />
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {// Document is ready.
      $("#Grid").ejGrid({
          dataSource: window.gridData,
          allowSorting: true,
          allowMultiSorting: true,
          allowPaging: true,
      });
      $("#columns,#direction").ejDropDownList();
      $("#sort").ejButton({
          click: function (args) {
              $("#Grid").ejGrid("sortColumn", $("#columns").ejDropDownList("getSelectedValue"), ej.sortOrder[$("#direction").ejDropDownList("getSelectedValue")]);
          }
      });
  });
</script>
{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Sorting_images/Sorting_img2.png"%}

