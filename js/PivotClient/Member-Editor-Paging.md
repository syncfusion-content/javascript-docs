---
layout: post
title: Member Editor Paging
description: memebr editor paging
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Member editor paging

The member editor paging helps you to improve the rendering performance of the dialog by dividing the large amount of data into sections and displaying them.

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

The following are the navigation option available in the member editor pager:
* Move first - Navigates to the first page.
* Move previous - Navigates to the previous page from the current page.
* Move next - Navigates to the next page from the current page.
* Move last - Navigates to the last page.
* Numeric box - Navigates to the desired page by entering an appropriate page number in a numeric value.


![](Member_Editor_images/member_editor.png)