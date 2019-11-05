---
layout: post
title: Paging with PivotClient widget for Syncfusion Essential JS
description: This document illustrates that how to define paging with respective to the modes in JavaScript PivotClient control
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Paging

I> This feature is applicable only for the OLAP data source.

Paging helps to improve the rendering performance of the pivot client control by dividing the large amount of the data into several sections and displaying one section at a time.

## Using pager

You can enable the pager in the pivot client by setting the [`enablePaging`](/api/js/ejpivotclient#members:enablepaging) property to true. You can provide the page size and current page details for each axis through the [`pagerOptions`](/api/js/ejpivotclient#members:datasource-pageroptions) property.

### Client Mode

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $("#PivotClient1").ejPivotClient({
        //...
        dataSource: {
            //...
            pagerOptions: {
                categoricalPageSize: 3,
                seriesPageSize: 3,
                categoricalCurrentPage: 1,
                seriesCurrentPage: 1
            }
        },
        enablePaging : true
    });
</script>
{% endhighlight %}

### Server mode

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    url: "/OlapService.svc",
    enablePaging: true
});

{% endhighlight %}

The following are the navigation option available in the pager:

* Move first - Navigates to the first page.
* Move last - Navigates to the last page.
* Move previous - Navigates to the previous page from the current page.
* Move next - Navigates to the next page from the current page.
* Numeric box - Navigates to the desired page by entering an appropriate page number in the numeric value.

![Paging in JavaScript pivot client control](Paging_images/paging.png)


## Using virtual scrolling

The virtual scrolling is a technique that allows you to view the pivot client information in page by page with the use of the vertical and horizontal scrollbar. You can enable the virtual scrolling option in the pivot client by setting the [`enableVirtualScrolling`](/api/js/ejpivotclient#members:enablevirtualscrolling) property to true. You can provide the page size and current page details for each axis through the [`pagerOptions`](/api/js/ejpivotclient#members:datasource-pageroptions) property.

### Client mode

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    dataSource: {
        //...
        pagerOptions: {
            categoricalPageSize: 3,
            seriesPageSize: 3,
            categoricalCurrentPage: 1,
            seriesCurrentPage: 1
        }
    },
    enableVirtualScrolling : true
});

{% endhighlight %}

### Server mode

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    url: "/OlapService.svc",
    enableVirtualScrolling: true
});

{% endhighlight %}

![Virtual scrolling in JavaScript pivot client control](Paging_images/virtual-scrolling.png)

## Page settings

The properties associated to paging are:
* EnablePaging – This property is used to enable/disable the paging in the pivot client control.
* PagerOptions.CategoricalPageSize - Specifies the number of categorical columns to be displayed within a page of the pivot client control.
* PagerOptions.SeriesPageSize - Specifies the number of series rows to be displayed within a page of the pivot client control.
* PagerOptions.CategoricalCurrentPage - Sets the current page of the categorical axis in the pivot client control.
* PagerOptions.SeriesCurrentPage - Sets the current page of the series axis in the pivot client control.

In client mode, the page setting for categorical and series axes is needed for setting in the data source property by using the following properties:

[`categoricalPageSize`](/api/js/ejpivotclient#members:datasource-pageroptions-categoricalpagesize) - Allows to set the number of categorical columns to be displayed in each page by applying the paging.

[`seriesPageSize`](/api/js/ejpivotclient#members:datasource-pageroptions-seriespagesize) - Allows to set the number of series rows to be displayed in each page by applying the paging.

[`categoricalCurrentPage`](/api/js/ejpivotclient#members:datasource-pageroptions-categoricalcurrentpage) - Allows to set the page number to be loaded in the categorical axis by default.

[`seriesCurrentPage`](/api/js/ejpivotclient#members:datasource-pageroptions-seriescurrentpage) - Allows to set the page number to be loaded in the series axis by default.

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    dataSource: {
        //...
        pagerOptions: {
            categoricalPageSize: 3,
            seriesPageSize: 3,
            categoricalCurrentPage: 1,
            seriesCurrentPage: 1
        }
    },
    enablePaging : true
});

{% endhighlight %}

In server mode, the page settings for categorical and series axes are done only through the OlapReport object that is created in the WebAPI or WCF file.

{% highlight c# %}

OlapReport olapReport = new OlapReport();
olapReport.CurrentCubeName = "Adventure Works";
olapReport.EnablePaging = true;
olapReport.PagerOptions.SeriesPageSize = 4;
olapReport.PagerOptions.CategoricalPageSize = 5;

{% endhighlight %}