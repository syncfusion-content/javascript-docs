---
layout: post
title: Cells
description: cells
platform: js
control: TreeGrid
documentation: ug
---

# Cell

## Tooltip

### Cell tooltip

When you move the cursor over the TreeGrid cells it provides the information about the grid cells and header cells. We can enable this support by set `showGridCellTooltip` as `true`.

N> 1. The `showGridCellTooltip` property is commanly applicable for all grid cells and header cells.

Please find the example describes the above behavior.

{% highlight js %}

    $(function () {
         $("#TreeGridContainer").ejTreeGrid({
             //… 
             showGridCellTooltip: true,                                   
        });
    });

{% endhighlight %}

The following output shows the result of above code example.
![](/js/TreeGrid/Cell/tooltip.png)

{:caption}
Cell Tooltip

![](/js/TreeGrid/Cell/headerTooltip.png)

{:caption}
Header Tooltip

### Grid cell tooltip

It describes the template design that applies to the column’s cell tooltip. To render tooltip with template for specific column’s cell set `tooltip` property of `column`.

Please refer the following code example for above behavior.

{% highlight js %}

<script type="text/x-jsrender" id="template">
   <div style='padding:10px;color:red;font-weight: bold;'>    
             {{"{{"}}:#data['record']['taskName']{{}}}}
</div>
</script>

{% endhighlight %}

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({                   
    columns: [
                      //...
              { field: "taskName", headerText: "Task Name",tooltip: "template"},
                      //...
             ]         
});

{% endhighlight %}

The following output shows the output of above code snippets.

![](/js/TreeGrid/Cell/cellTooltipTemplate.png)

N> 1. If we did not provide the value to `column.tooltip` property, cell value is shown in tooltip element.
N> 2. Template element should be enclosed with `<script>` tag with type as `“text/x-jsrender”`.

### Header cell tooltip

It describes the template design that applies to the column header cell tooltip. To render tooltip with template for specific column header set `headerTooltip` property of `column`.

The following code example describes the above behavior.

{% highlight js %}

<script type="text/x-jsrender" id="template">
   <div style='padding:10px;color:blue;font-weight: bold;'>
             {{"{{"}}:#data['column']['headerText']{{}}}}
</div>
</script> 

{% endhighlight %}

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({                   
    columns: [
                      //...
              { field: "taskID", headerText: "Task Id",headerTooltip: "template"},
                      //...
             ]         
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/headetTooltipTemplate.png)

N> 1. If we did not provide the value to `column.headerTooltip` property, headetText value is shown in tooltip element.
N> 2. Template element should be enclosed with `<script>` tag with type as `“text/x-jsrender”`.

### Tooltip Template

We can use JSRender Template for shows more information about the cell in tooltip. We can use this support by using `cellTooltipTemplate` property. The value of this property should be a valid JSRender template string or ID of JSRender element.

N> 1. The `cellTooltipTemplate` property is commanly applicable for all grid cells.

Please find code example describes the cell tooltip template support.

{% highlight js %}

<script type="text/x-jsrender" id="cellTooltipTemplate">
        <table>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    Task ID
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['taskID']{{}}}}
                </td>
            </tr>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    Task Name
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['taskName']{{}}}}
                </td>
            </tr>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    Start Date
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['startDate']{{}}}}
                </td>
            </tr>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    End Date
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['endDate']{{}}}}
                </td>
            </tr>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    Duration
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['duration']{{}}}}
                </td>
            </tr>
            <tr>
                <td style='padding:5px;font-weight: bold;'>
                    Progress
                </td>
                <td style='padding:5px;'>
                    : {{"{{"}}:#data['record']['progress']{{}}}}
                </td>
            </tr>
        </table>
    </script>

{% endhighlight %}

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
   //… 
   showGridCellTooltip: true,   
   cellTooltipTemplate:"cellTooltipTemplate",                                
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/gridcelltemplate.png)

## Clip Mode

Clip mode enables the TreeGrid to clip cell content and header content when the content exceeds the boundary of the cell width. 

We can specify the type of clip mode using clipMode property of the columns, Clip Mode will be enable for both TreeGrid content and header of that specific column.

Two types of clipMode are available and they are,

1. Clip
2. Ellipsis

### Clip

When clipMode of Columns property set as Clip then it truncates the overflown text in the cell.

N> 1. By default the clipMode will be set as clip.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
   //… 
       columns: [
              { field: "taskName", headerText: "Task Name",clipMode: ej.TreeGrid.ClipMode.Clip},
             ]        
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/clipmode.png)

### Ellipsis

When `clipMode` of `Columns` property set as `Ellipsis` then it shows ellipsis for the overflown cell.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
   //… 
       columns: [
              { field: "taskName", headerText: "Task Name",clipMode: ej.TreeGrid.ClipMode.Ellipsis},
             ]        
});

{% endhighlight %}

The following output is shows the result of the above code example.

![](/js/TreeGrid/Cell/ecllipsismode.png)