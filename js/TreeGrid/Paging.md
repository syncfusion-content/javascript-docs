---
layout: post
title: Paging
description: paging
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Paging

The TreeGrid control provides support for displaying records in paginated view. Paging can be enabled in TreeGrid by setting the [`allowPaging`](/api/js/ejtreegrid#members:allowpaging) property as `true`.

The below code snippet explains enabling paging in TreeGrid.

{% highlight html %}
<div id="TreeGridContainer"/>
{% endhighlight %}

{% highlight js %}
$("#TreeGridContainer").ejTreeGrid({
    //...
    allowPaging: true,
});
{% endhighlight %}

The output of the TreeGrid with paging enabled is displayed below.

![](/js/TreeGrid/Paging_images/Paging_img1.png)

## Paging settings

The paging in TreeGrid can be customized by using the [`pageSettings`](/api/js/ejtreegrid#members:pagesettings) property.
The number of records to be displayed per page can be limited by using the [`pageSize`](/api/js/ejtreegrid#members:pagesettings-pagesize "pageSettings.pageSize") property. 
The number of root nodes or the 0th level records to be displayed per page can be limited by setting the [`pageSizeMode`](/api/js/ejtreegrid#members:pagesettings-pagesizemode "pageSettings.pageSizeMode") property as `Root`. When the [`pageSizeMode`](/api/js/ejtreegrid#members:pagesettings-pagesizemode "pageSettings.pageSizeMode") property is set as `Root` the number of records to displayed per page which is defined in the The [`pageSize`](/api/js/ejtreegrid#members:pagesettings-pagesize "pageSettings.pageSize") property will be considered only for the root nodes or the 0th level records.
The [`pageCount`](/api/js/ejtreegrid#members:pagesettings-pagecount "pageSettings.pageCount") property is used to display the page number to be displayed in the pager.
The [`currentPage`](/api/js/ejtreegrid#members:pagesettings-currentpage "pageSettings.currentPage") property is used to set the active page to displayed initially.
The [`totalRecordsCount`](/api/js/ejtreegrid#members:pagesettings-totalrecordscount "pageSettings.totalRecordsCount") property is used to limit the total number of records from the data source to be displayed in TreeGrid.
 The following code example explains the properties in pageSettings. 

{% highlight js %}
$("#TreeGridContainer").ejTreeGrid({
    //...
    allowPaging: true,
    pageSettings: {
        pageCount: 5,
        currentPage: 3,
        totalRecordsCount: 50,
        pageSizeMode: "all",
        pageSize: "12",
    },
});
{% endhighlight %}

You can also find the demo for pageSettings [here](http://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/paging/pagingapi)


## Pager Template

It is possible to customize the default pager in TreeGrid by using the [`template`](/api/js/ejtreegrid#members:pagesettings-template "pageSettings.template") property.
The below code snippet explains how to customize the default pager with template

{% highlight html %}
<script type="text/x-jsrender" id="template">
    <div class="e-pagercontainer">
        <div class="e-first e-icon e-mediaback e-firstpagedisabled e-disable" title="Go to first page"></div>
        <div class="e-prev e-icon e-arrowheadleft-2x e-prevpagedisabled e-disable" style="border-right:none" title="Go to previous page"></div>
    </div>
    <div class="e-pagercontainer e-currentPageContainer" style="border-radius:0px">
        <input id="currentPage" class="e-pagercontainer" type="text" style="text-align:center; margin:0px;border:none;width:32px;height:23px" />
    </div>
    <div id="totalPages" class="e-pagercontainer" style="margin-left: 2px;margin-bottom:5px;border: none; ">
        <span></span>
    </div>
    <div class="e-pagercontainer">
        <div class="e-nextpage e-icon e-arrowheadright-2x e-default" title="Go to next page"></div>
        <div class="e-lastpage e-icon e-mediaforward e-default" title="Go to last page"></div>
    </div>
</script> 

{% endhighlight %}

{% highlight css %}
    #currentPage {
        background-color: white;
    }

    .e-currentPageContainer {
        border-bottom: 1px solid #e0e0e0!important;
    }

    .e-pagercontainer .e-icon {
        display: inline-block;
        height: 8px;
    }

    .e-pager .e-pagercontainer {
        margin: 0px;
        margin-left: 6px;
    }
{% endhighlight %}

{% highlight javascript %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    allowPaging: true,
    pageSettings: {
        template: "#template",
    },
});

//Code for navigating to the page 
$("#currentPage").keydown(function(e) {
    var obj = $("#TreeGridContainer").data("ejTreeGrid");
    var val = parseInt($("#currentPage").val());
    if (e.keyCode == 13) {
        if (val > obj.model.pageSettings.totalPages)
            val = obj.model.pageSettings.totalPages;
        if (val <= 0)
            val = 1;
        obj.gotoPage(val);
        return false;
    }
});

{% endhighlight %}

You can also find the demo for TreeGrid with pager template [here](http://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/paging/pagertemplate).

The below image displays TreeGrid with paging template.
![](/js/TreeGrid/Paging_images/Paging_img2.png)

It is possible to navigate to a specific page with a custom action instead from pager button click action, using the [`gotoPage`]( /api/js/ejtreegrid#methods:gotopage "gotoPage") method.

The below code snippet explains calling the method to navigate to the 3rd page in TreeGrid

{% highlight javascript %}

        var treeObject = $("#TreeGridContainer").data("ejTreeGrid");
        treeObject.gotoPage(3);

{% endhighlight %}

## Paging - Touch Option

With paging and responsive mode enabled in TreeGrid, it is possible to change the current page using swipe action.

The following code example describes how to enable multiple selection in TreeGrid.	

{% highlight js %}
$("#TreeGridContainer").ejTreeGrid({
    //...
    allowPaging: true,
    isResponsive: true,
});
{% endhighlight %}