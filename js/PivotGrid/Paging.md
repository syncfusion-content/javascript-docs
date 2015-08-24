---
layout: post
title: Paging
description: paging
platform: js
control: PivotGrid
documentation: ug
---

# Paging



##Pager

The **PivotGrid** is viewed page-by-page through [Pager](/js/api/ejPivotPager#members:mode) option. The **Pager** is set to **PivotGrid** using following code example.

{% highlight html %}
<div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto">
</div>
<div id="Pager1" style="margin-top:10px; overflow: auto"></div>         

{% endhighlight %}

{% highlight js %}
$("#PivotGrid1").ejPivotGrid({
    url: "../wcf/PivotGridService.svc",
});
$("#Pager1").ejPivotPager({
    mode: ej.PivotPager.Mode.Both,
    targetControlID: "PivotGrid1"
});
{% endhighlight %}

N>  This feature is applicable only for OLAP datasource.

The page size for categorical and series axes are set in the **OlapReport**. **Pager** is loaded with current page and total pages of **PivotGrid** is automatically displayed as illustrated in the following screenshot. The icons to move pages to next, last, previous and first are added.  Also you can directly navigate to the desired page by entering the appropriate numeric value into the text box.

{% include image.html url="/js/PivotGrid/Paging_images/Paging_img1.png" %}

##Virtual Paging

The large **PivotGrid** data content is viewed page-by-page using **Virtual Paging** . The page size for categorical and series axes are set in **OlapReport**. By enabling [Virtual Scrolling](/js/api/ejPivotGrid#members:enablevirtualscrolling) , the number of rows and columns for the **PivotGrid** are set as entered in the **OlapReport**. By scrolling the horizontal and vertical scrollbars, the categorical and series page numbers are obtained and **PivotGrid** contents are refreshed accordingly.

{% highlight js %}
$("#PivotGrid1").ejPivotGrid({
    url: "../wcf/PivotGridService.svc",
    enableVirtualScrolling: true
});   

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Paging_images/Paging_img2.png" Caption="PivotGrid with Virtual Scroller"%}

{% include image.html url="/js/PivotGrid/Paging_images/Paging_img3.png" Caption="Page indication while scrolling"%}

##OLAP Report for Paging and Virtual Scrolling

{% highlight c# %}

OlapReport olapReport = new OlapReport();
olapReport.CurrentCubeName = "Adventure Works";
olapReport.Name = "Default Report";

//NOTE: Below code enables the paging option and also sets the page size.
olapReport.EnablePaging = true;
olapReport.PagerOptions.SeriesPageSize = 5;
olapReport.PagerOptions.CategorialPageSize = 4;

DimensionElement dimensionElementColumn = new DimensionElement() { Name ="Customer" };
dimensionElementColumn.AddLevel("City", "City");
olapReport.CategoricalElements.Add(dimensionElementColumn);

DimensionElement dimensionElementRow = new DimensionElement() { Name = "Date"};
dimensionElementRow.AddLevel("Fiscal", "Fiscal Year");
olapReport.SeriesElements.Add(dimensionElementRow);

dimensionElementRow = new DimensionElement() { Name = "Product" };
dimensionElementRow.AddLevel("Category", "Category");
olapReport.SeriesElements.Add(dimensionElementRow);

MeasureElements measureElementColumn = new MeasureElements();
measureElementColumn.Elements.Add(new MeasureElement { Name = "Sales Amount"});
olapReport.CategoricalElements.Add(measureElementColumn);

{% endhighlight %}



