---
layout: post
title: Paging
description: paging
platform: js
control: PivotGrid
documentation: ug
---

# Paging

I> This feature is applicable only for OLAP datasource only at Server Mode.

## Pager 
Paging helps to improve the rendering performance of the PivotGrid control by breaking large amount of data into sections and displaying them.
 
In-order to initialize a "Pager", first you need to define a "div" tag with an appropriate "id" attribute which acts as a container for the widget. Then you need to initialize the widget using **“ejPivotPager”** method.

Inside the **“ejPivotPager”** method, the enumeration property [`mode`](/js/api/ejpivotpager#members:mode) needs to be set to **“ej.PivotPager.Mode.Both”** in-order to display both categorical pager and series pager. The other enumerations such as **“ej.PivotPager.Mode.Categorical”** and **“ej.PivotPager.Mode.Series”** will display only categorical pager and series pager respectively.


{% highlight html %}

<html>
//...

<body>
    <div id="PivotGrid1" style="height:350px; width:100%; overflow: auto"></div>

    <!--Create a tag which acts as a container for Pager. -->
    <div id="Pager1" style="margin-top: 10px; overflow: auto"></div>

    <script type="text/javascript">
        $(function() {
            $("#PivotGrid1").ejPivotGrid({
                url: "/OLAPService.svc"
            });
            $("#Pager1").ejPivotPager({
                mode: ej.PivotPager.Mode.Both,
                targetControlID: "PivotGrid1"
            });
        });
    </script>
</body>

</html>

{% endhighlight %}

Following are the navigation option available in Pager.

* Move First - Navigates to the first page.
* Move Previous - Navigates to the previous page from the current page.
* Move Next - Navigates to the next page from the current page.
* Move Last - Navigates to the last page. 
* Numeric Box - Navigates to the desired page by entering an appropriate numeric value.

![](Paging_images/paging.png)

## Virtual Scrolling
Virtual Scrolling is a technique that allows user to scroll vertically and horizontally the scroll bar to view the paged information. You can enable Virtual Scrolling option in PivotGrid by setting the [`enableVirtualScrolling`](/js/api/ejpivotgrid#members:enablevirtualscrolling) property to true.

{% highlight js %}

$("#PivotGrid1").ejPivotGrid({
    url: "/OLAPService.svc",
    enableVirtualScrolling: true
});

{% endhighlight %}

![](Paging_images/virtual-scrolling.png)

## Page Setting (Report)
The page setting for categorical and series axes are mandatorily needs to be done in OlapReport class by using the following properties.

* EnablePaging - Specifies a value indicating whether to enable or disable paging in PivotGrid control.
* PagerOptions.CategoricalPageSize - Specifies the number of categorical columns to be displayed within a page of the PivotGrid control.
* PagerOptions.SeriesPageSize - Specifies the number of series rows to be displayed within a page of the PivotGrid control.
* PagerOptions.CategoricalCurrentPage - Set the current page of the categorical axis in PivotGrid control.
* PagerOptions.SeriesCurrentPage - Set the current page of the series axis in PivotGrid control.

{% highlight c# %}

            OlapReport olapReport = new OlapReport();
            olapReport.CurrentCubeName = "Adventure Works";
            olapReport.EnablePaging = true;
            olapReport.PagerOptions.SeriesPageSize = 4;
            olapReport.PagerOptions.CategorialPageSize = 5;

            DimensionElement dimensionElement = new DimensionElement() { Name = "Customer" };
            dimensionElement.AddLevel("Customer", "Customer");
            olapReport.CategoricalElements.Add(dimensionElement);

            DimensionElement dimensionElementRow = new DimensionElement() { Name = "Customer", HierarchyName = "Customer" };
            dimensionElementRow.AddLevel("Customer Geography", "Country");
            olapReport.SeriesElements.Add(dimensionElementRow);

            MeasureElements measureElementColumn = new MeasureElements();
            measureElementColumn.Elements.Add(new MeasureElement { Name = "Internet Sales Amount" });
            olapReport.CategoricalElements.Add(measureElementColumn);

{% endhighlight %}



