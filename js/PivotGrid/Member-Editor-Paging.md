---
layout: post
title: Member Editor Paging
description: memebr editor paging
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Member editor paging

The member editor paging helps you to improve the rendering performance of the dialog by dividing the large amount of data into sections and displaying them.

You can enable the member editor paging and set the member editor page size in the pivot grid control by setting the [`enableMemberEditorPaging`](/api/js/ejpivotgrid#members:enablemembereditorpaging) and [`memberEditorPageSize`](/api/js/ejpivotgrid#members:membereditorpagesize) properties.

{% highlight html %}

<div id="PivotGrid1"></div>
<script>
    $("#PivotGrid1").ejPivotGrid({
        //...
        enableMemberEditorPaging : true, 
        memberEditorPageSize : 100
    });
</script>

{% endhighlight %}

Following are the navigation option available in the member editor pager.
* Move first: Navigates to the first page.
* Move previous: Navigates to the previous page from the current page.
* Move next: Navigates to the next page from the current page.
* Move last: Navigates to the last page.
* Numeric box: Navigates to the desired page by entering an appropriate page number in the numeric value.


![](Member_Editor_images/member_editor.png)