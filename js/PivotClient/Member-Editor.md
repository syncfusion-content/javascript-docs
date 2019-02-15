---
layout: post
title: Member Editor with PivotClient widget for Syncfusion Essential JS
description: Member editor in PivotClient control
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Member Editor

The member editor dialog displays the members of current field in a tree view structure, which is opened by clicking the pivot button available in axis elements. It helps to search, filter, and sort the field members available in the pivot client control.

![Member editor in JavaScript pivot client control](Member_Editor_images/member_editor.png)

## Member editor - Paging

The member editor paging helps you to improve the rendering performance of the dialog by dividing the large amounts of data into sections and displaying them.

You can enable the member editor paging and set the member editor page size in the pivot client control by setting the [`enableMemberEditorPaging`](/api/js/ejpivotclient#members:enablemembereditorpaging) and [`memberEditorPageSize`](/api/js/ejpivotclient#members:membereditorpagesize) properties.

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $("#PivotClient1").ejPivotClient({
        //...
        enableMemberEditorPaging : true,
        memberEditorPageSize : 100
    });
</script>

{% endhighlight %}

The following are the navigation options available in the member editor pager:

* Move first: Navigates to the first page.
* Move previous: Navigates to the previous page from the current page.
* Move next: Navigates to the next page from the current page.
* Move last: Navigates to the last page.
* Numeric box: Navigates to the desired page by entering an appropriate page number in a numeric value.


![Member editor paging in JavaScript pivot client control](Member_Editor_images/member_editor_paging.png)

## Member editor - Sorting

The sorting support in the member editor helps you to sort the field members in ascending or descending order.

You can enable the member editor sorting in the pivot grid control by setting the [`enableMemberEditorSorting`](/api/js/ejpivotclient#members:enablemembereditorsorting) property.

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $("#PivotClient1").ejPivotClient({
        //...
        enableMemberEditorSorting : true
    });
</script>

{% endhighlight %}

![Member editor sorting with ascending order in JavaScript pivot client control](Member_Editor_images/member_editor_sorting_ascending.png)

![Member editor sorting with descending order in JavaScript pivot client control](Member_Editor_images/member_editor_sorting_descending.png)