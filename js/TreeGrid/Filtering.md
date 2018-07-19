---
layout: post
title: Filtering
description: filtering
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---

# Filtering

Filtering helps to view specific or related records from data source which meets a given filtering criteria. To enable filtering in TreeGrid, set the [`allowFiltering`](/api/js/ejtreegrid#members:allowfiltering)  as `true`.
The [`filterSettings`](/api/js/ejtreegrid#members:filtersettings) property is used to customize the filtering in tree grid.

TreeGrid provides support for the following filtering modes.

* Filter bar
* Menu
* Excel

Also, the following filtering types are available in TreeGrid.

* String
* Boolean
* Date
* Numeric
* Dropdown

The below code explains how to enable filtering in TreeGrid.

{% highlight js %}

   $("#TreeGridContainer").ejTreeGrid({
        //...
        allowFiltering: true,
   });

{% endhighlight %}

The output of the TreeGrid with filtering enabled is as follows.

![](/js/TreeGrid/Filtering_images/Filtering_img1.png)

The TreeGrid allows the user to filter the columns with custom actions by using the method [`filterColumn`](/api/js/ejtreegrid#methods:filtercolumn). And it is possible to clear the filter for a specific column by using the method [`clearFilter`](/api/js/ejtreegrid#methods:clearfilter "clearFilter").

## Filtering Modes

### Filter Bar 

This is the default filtering mode in TreeGrid. It can also be enabled by setting the [`filterType`](/api/js/ejtreegrid#members:filtersettings-filtertype "filterSettings.filterType") as `filterbar`. When this filtering mode is enabled, a filter row will be displayed below the column header, in which we can provide the filter query.

There are two types of actions available to initiate the filtering process in the filter bar mode, we can set the filter bar mode using [`filterBarMode`](/api/js/ejtreegrid#members:filtersettings-filterbarmode "filterSettings.filterBarMode") property.

`immediate`: Filtering action will be initiated immediately on key press, for each character being typed in the filter bar.

`onEnter`: Filtering action will be initiated only on enter key press in the filter bar.

The below code snippet explains the above behavior.

{% highlight js %}
 
 $("#TreeGridContainer").ejTreeGrid({
     //...
     filterSettings: {
         filterType: ej.TreeGrid.FilterType.FilterBar
         filterBarMode: "onEnter"
     }
 });

{% endhighlight %}

The output of the filtering with filter bar enabled is as follows.

![](/js/TreeGrid/Filtering_images/Filtering_img2.png)

### Menu filtering
Menu filtering can be enabled by setting the [`filterType`](/api/js/ejtreegrid#members:filtersettings-filtertype "filterSettings.filterType") property as `menu`. The below code snippet explains how to enable menu filtering in TreeGrid.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
     //...
     filterSettings: {
         filterType: ej.TreeGrid.FilterType.Menu
     }
 });

{% endhighlight %}

The output of the filtering with filter menu enabled is as follows.

![](/js/TreeGrid/Filtering_images/Filtering_img3.png)

### Excel Filtering
Excel filtering can be enabled by setting the [`filterType`](/api/js/ejtreegrid#members:filtersettings-filtertype "filterSettings.filterType") property as `excel`. The excel menu contains options such as sorting, clear filter and advance filtering options.
The below code snippet explains how to enable excel filtering in TreeGrid.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
     //...
     allowFiltering:true,
      filterSettings:{
             filterType: ej.TreeGrid.FilterType.Excel,
      }
    //...
 });

{% endhighlight %}

The output of the filtering with excel filter enabled is as follows.

![](/js/TreeGrid/Filtering_images/Filtering_img5.png)

#### Checkbox list generation

By default, the checkbox list is generated from distinct values of the filter column from dataSource which gives an option to search and select the required items. 
If the number of distinct values are greater than 1000, then the excel filter will display only first 1000 values and show "Not all items shown" label to ensure the best performance on rendering and searching. However, this limit has been customized according to your requirement by setting the [`maxFilterChoices`](/api/js/ejtreegrid#members:filtersettings-maxfilterchoices "filterSettings.maxFilterChoices") with required limit in integer.
The below code snippet explains how to change the max filter choices value.

{% highlight js %}

$("#Treegrid ").ejTreeGrid ({
      //...
      filterSettings:{
             maxFilterChoices: 5,
      }
     //...
});
{% endhighlight %}
![](/js/TreeGrid/Filtering_images/Filtering_img6.png)
The above screen shot shows TreeGrid with maxFilterChoices as 5.

#### Case Sensitivity

To perform filter operation with case sensitive in excel styled filter menu mode by setting the [`enableCaseSensitivity`](/api/js/ejtreegrid#members:filtersettings-enablecasesensitivity "filterSettings.enableCaseSensitivity") as `true`.
The below code snippet explains how to enable the case sensitivity in excel filter.

{% highlight js %}

$("#Treegrid ").ejTreeGrid ({
      //...
      filterSettings:{
             enableCaseSensitivity: true,
      }
     //...
});

{% endhighlight %}
![](/js/TreeGrid/Filtering_images/Filtering_img7.png)
The above screen shot shows TreeGrid with `enableCaseSensitivity` set as false in search action.

### Change filter mode for specific column

TreeGrid provides option for changing the filter mode for specific column by using [`filterType`](/api/js/ejtreegrid#members:columns-filtertype "columns.filterType") property. Using this property we can either set `Menu` or `Excel` filter mode when [`filterType`](/api/js/ejtreegrid#members:filtersettings-filtertype "filterSettings.filterType") property as `Menu` or `Excel`.

The following code example show, how to change filter mode for specific column.

{% highlight js %}

$("#Treegrid ").ejTreeGrid ({
      //...
      columns: [{
         field: "taskName",
         headerText: "Task Name",
         filterType:"excel"
     }, ]
      filterSettings:{
             filterType: ej.TreeGrid.FilterType.Menu,
      }
     //...
});
{% endhighlight %}

![](/js/TreeGrid/Filtering_images/Filtering_img10.png)

The above screen shot shows TreeGrid with excel filter mode for `Task Name` column only.  

### Filtering blank values in Excel filter type
In TreeGrid, it is possible to filter the null or empty string value for all the columns when filter type is menu by setting [`enableComplexBlankFilter`](/api/js/ejtreegrid#members:filtersettings-enablecomplexblankfilter "filterSettings.enableComplexBlankFilter") as `true` in the filter settings definition.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
     allowFiltering: true,
     filterSettings:{
             filterType: ej.TreeGrid.FilterType.Menu,
             enableComplexBlankFilter:true,
      }
    //...
 })

{% endhighlight %}

## Filtering types
By default, the filtering type for a column is inherited from the [`editType`](/api/js/ejtreegrid#members:columns-edittype "columns.editType") property. You can also define a specific filtering type for a column using the [`filterEditType`](/api/js/ejtreegrid#members:columns-filteredittype "columns.filterEditType") property.
The below code snippet explains on how to set a filtering type for a column.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({

     allowFiltering: true,
     columns: [{
             field: "taskID",
             allowFiltering: false,
         },
         {
             field: "taskName",
             editType: "stringedit",
             filterEditType: "stringedit"
         },
         {
             field: "startDate",
             editType: "datepicker",
             filterEditType: "datepicker",
             format: dateFormat
         },
         {
             field: "priority",
             editType: "dropdownedit",
             filterEditType: "dropdownedit",
             dropdownData: stageData,
             editParams: {
                 fields: {
                     text: "text",
                     value: "value"
                 },
                 showCheckbox: false
             }
         },
         {
             field: "progress",
             editType: "numericedit",
             filterEditType: "numericedit"
         }
     ],

 })

{% endhighlight %}

### Filtering blank values in drop down filtering
In TreeGrid, it is possible to filter the null or empty string value in drop down filter type by setting [`allowFilteringBlankContent`](/api/js/ejtreegrid#members:columns-allowfilteringblankcontent "columns.allowFilteringBlankContent") as `true` in the column definition.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
     allowFiltering: true,
     columns: [
         {
            field: "priority",
            headerText:"Priority",
            filterEditType:"dropdownedit",
            allowFilteringBlankContent: true,
        },
    ]
    //...
 })

{% endhighlight %}

![](/js/TreeGrid/Filtering_images/Filtering_img9.png)

The above screenshot shows TreeGrid with filtering blank content.
{:.caption}

### Filter Hierarchy Modes

TreeGrid provides support for a set of filtering modes with [`filterHierarchyMode`](/api/js/ejtreegrid#members:filtersettings-filterhierarchymode "filterSettings.filterHierarchyMode") property.
The below are the type of filter mode available in TreeGrid.

`Parent `: This is the default filter hierarchy mode in TreeGrid. The filtered record displayed with its parent records, if the filtered records not have any parent record then the filtered record only displayed.

`Child`  : The filtered record displayed with its child record, if the filtered records not have any child record then the filtered record only displayed.

`Both`   : The filtered record displayed with its both parent and child record, if the filtered records not have any parent and child record then the filtered record only displayed.

`None`   : The filtered record only displayed.

The following code example shows how to set filter mode in TreeGrid.
{% highlight js %}

$("#TreeGridContainer").ejTreeGrid(
   {
          //..
         filterSettings: {
                filterHierarchyMode: ej.TreeGrid.FilterHierarchyMode.Child
          }

});

{% endhighlight %}

![](/js/TreeGrid/Filtering_images/filterHierarchyMode.png)

The above screenshot shows TreeGrid filter with `child` filter mode.

## Filter columns at initial load
It is also possible to filter one or more columns at load time by providing the [`field`](/api/js/ejtreegrid#members:filtersettings-filteredcolumns-field "filterSettings.filteredColumns.field"), [`value`](/api/js/ejtreegrid#members:filtersettings-filteredcolumns-value "filterSettings.filteredColumns.value"), [`predicate`](/api/js/ejtreegrid#members:filtersettings-filteredcolumns-predicate "filterSettings.filteredColumns.predicate") and [`operator`](/api/js/ejtreegrid#members:filtersettings-filteredcolumns-operator "filterSettings.filteredColumns.operator") to the [`filteredColumns`](/api/js/ejtreegrid#members:filtersettings-filteredcolumns "filterSettings.filteredColumns") property. The following code example explains how to filter a column on initial load.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    allowFiltering: false,
    filterSettings: {
        filteredColumns: [{
            value: "plan",
            field: "taskName",
            predicate: "and",
            operator: "startswith"
        }]
    },
});

{% endhighlight %}

## Disabling filtering for a specific column 
It is possible to disable filtering for a specific column by setting the [`allowFiltering`](/api/js/ejtreegrid#members:columns-allowfiltering "columns.allowFiltering") as `false` in the column definition.
The below code snippet explains the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
     allowFiltering: true,
     columns: [{
         field: "taskID",
         allowFiltering: false,
     }, ]
 })

{% endhighlight %}

The output of the filtering enabled for only one column is as follows.

![](/js/TreeGrid/Filtering_images/Filtering_img4.png)

[Click here](http://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/columnfiltering) to find the demo sample for filtering in TreeGrid

## Filtering multiple columns dynamically

It is possible to filtering multiple columns dynamically by using the [`filterContent`](/api/js/ejtreegrid#methods:filtercontent) method. 
The below code snippet explains how to filter multiple columns dynamically in TreeGrid.

{% highlight js %}

<button id="filterContent">filterContent</button>

<script type="text/javascript">
$("#TreeGridContainer").ejTreeGrid({
    filterSettings: { filterType: ej.TreeGrid.FilterType.Menu},
    //...    
})

$("#filterContent").click(function (args) {
       var treeObj = $("#TreeGridContainer").ejTreeGrid("instance");
       var predicate = ej.Predicate("taskName", ej.FilterOperators.startsWith, "Plan", true)
                             .or("taskName", ej.FilterOperators.equal, "Software Specification", true)
                             .and("progress", ej.FilterOperators.notEqual, 0, true);
           treeObj.filterContent(predicate);
})
</script>

{% endhighlight %}
The below screenshot shows the output of above code example.

![](/js/TreeGrid/Filtering_images/Filtering_img11.png)

## Toolbox searching

The TreeGrid control has an option to search its content using toolbar search box. The toolbar search box can be enabled by using the `toolbarSettings.toolbarItems` property.
The following code example explains how to integrate search text box in toolbar.

{% highlight js %}

$("#Treegrid ").ejTreeGrid ({
      //...
      toolbarSettings:{
             showToolbar: true,
             toolbarItems:  [ ej.TreeGrid.ToolbarItems.Search ],
      }
     //...
});

{% endhighlight %}

![](/js/TreeGrid/Filtering_images/Filtering_img8.png)

The above screen shot shows TreeGrid search with ‘Plan’ key word.

The toolbox searching can be customized using the [`searchSettings`](/api/js/ejtreegrid#members:searchsettings "searchSettings") property. It is possible to search the TreeGrid content with the specific column values as the query for searching, using the property [`searchSettings.field`](/api/js/ejtreegrid#members:searchsettings-fields "searchSettings.field").
The below code example explains searching the TreeGrid content across the "TaskId" and "TaskName" columns.

{% highlight js %}
        $("#treegrid").ejTreeGrid({
            searchSettings: {
                fields: ["TaskId", "TaskName"],
            }
        });
        
{% endhighlight %}

It is possible to filter the TreeGrid contents at initial load using the toolbar search, with the [`searchSettings.key`](/api/js/ejtreegrid#members:searchsettings-key "searchSettings.key") property.
The below code example explains filtering the TreeGrid contents at initial load with a search key, which will be applied across all the columns.

{% highlight js %}
        $("#treegrid").ejTreeGrid({
            searchSettings: {
                key: "task 1",
            }
        });
{% endhighlight %}

TreeGrid provides support for conditional searching with operators in toolbar search using the property [`searchSettings.operator`](/api/js/ejtreegrid#members:searchsettings-operator "searchSettings.operator"). And case sensitivity for the search query can be ignored using the property [`searchSettings.ignoreCase`](/api/js/ejtreegrid#members:searchsettings-ignorecase "searchSettings.ignoreCase").
The below code example explains filtering the TreeGrid content using toolbar search with operators

{% highlight js %}

        $("#treegrid").ejTreeGrid({
            searchSettings: {
                fields: ["TaskName"],
                key: "Task 1",
                operator: "startsWith",
                ignoreCase: false
            }
        });
        
{% endhighlight %}

If the toolbar search textbox is not enabled in TreeGrid, and still if the contents need to be filtered at initial load using the `searchSettings` property, then the user should enable the [`allowSearching`](/api/js/ejtreegrid#members:allowsearching "allowSearching") property along with search settings.

{% highlight js %}

        $("#treegrid").ejTreeGrid({
            //...
            allowSearching: true,
            searchSettings: {
                key: "Plan"
            },
        });
        
{% endhighlight %}
