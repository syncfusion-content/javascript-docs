---
layout: post
title: Change-Weekend
description: Display custom fields in General tab
platform: js
control: Gantt
documentation: ug
---

# Display custom fields in general tab
Gantt add and edit dialogs groups the data sources fields in five different tabs such as `General`, `Predecessors`, `Resources`, `Custom Fields` and `Notes`.

![](/js/Gantt/How-to/Change-Custom-Fields_images/dialog_all_tab.png)

The custom fields are usually displayed in `Custom Fields` tab, but it is also possible to display the custom fields in general tab using [`displayInGeneralTab`](/api/js/ejgantt#members:editdialogfields-displayingeneraltab "editDialogFields.displayInGeneralTab") property in Gantt. By default, its value is `false`.
The following code example explains how to display custom fields in general tab

{% highlight javascript %}

$("#Gantt ").ejGantt ({
       //...
   
      addDialogFields: [{ field: "taskID" }, { field: "taskName" }, { field: "startDate" }, { field: "endDate" }, { field: "duration" }, { field: "notes" }, { field: "expectedDate", displayInGeneralTab: true }],
      editDialogFields: [{ field: "taskID" }, { field: "taskName" }, { field: "startDate" }, { field: "endDate" }, { field: "duration" }, { field: "notes" }, { field: "expectedDate", displayInGeneralTab: true}]

       //...
});

{% endhighlight %}

![](/js/Gantt/How-to/Change-Custom-Fields_images/dialog_specific_tab.png)

The above screen shot shows custom column field “Expected Date” displayed in General tab.
{:.caption}