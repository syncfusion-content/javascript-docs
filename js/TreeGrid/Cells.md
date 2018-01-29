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

In TreeGrid, tooltip can be enabled using the [`showGridCellTooltip`](/api/js/ejtreegrid#members:showgridcelltooltip) property. Using this property tooltip can be enabled for cells both header and content.

Please find the example describes the above behavior.

{% highlight js %}

  $(function() {
      $("#TreeGridContainer").ejTreeGrid({
          //...
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


### Tooltip Template

It is possible to display a custom tooltip across all the TreeGrid cells using the property [`cellTooltipTemplate`](/api/js/ejtreegrid#members:celltooltiptemplate) with the property [`showGridCellTooltip`](/api/js/ejtreegrid#members:showgridcelltooltip) enabled. We need to set the template of the custom tooltip to this property.

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
    //...
    showGridCellTooltip: true,
    cellTooltipTemplate: "cellTooltipTemplate",
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/gridcelltemplate.png)

### Column tooltip

By using the property [`tooltip`](/api/js/ejtreegrid#members:columns-tooltip "columns.tooltip") it is possible to display a custom tooltip for a specific column. The ID of the script template must be set to the [`tooltip`](/api/js/ejtreegrid#members:columns-tooltip "columns.tooltip") property.

Please refer to the following code example for setting a custom tooltip for a specific column.

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
        {
            field: "taskName",
            headerText: "Task Name",
            tooltip: "template"
        },
        //...
    ]
});

{% endhighlight %}

The following output shows the output of above code snippets.

![](/js/TreeGrid/Cell/cellTooltipTemplate.png)

N> Template element should be enclosed with `<script>` tag with type as `“text/x-jsrender”`.

### Header tooltip

By using the property [`headerTooltip`](/api/js/ejtreegrid#members:columns-headertooltip "columns.headerTooltip") it is possible to display a custom tooltip for a specific column header. The ID of the script template must be set to the [`headerTooltip`](/api/js/ejtreegrid#members:columns-headertooltip "columns.headerTooltip") property.

Please refer to the following code example for setting a custom tooltip for a specific column header.

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
        {
            field: "taskID",
            headerText: "Task Id",
            headerTooltip: "template"
        },
        //...
    ]
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/headetTooltipTemplate.png)

### Expander column tooltip

It is possible to enable the tooltip only for expander column using [`showGridExpandCellTooltip`](/api/js/ejtreegrid#members:showgridexpandcelltooltip) property also need to enable the [`showGridCellTooltip`](/api/js/ejtreegrid#members:showgridcelltooltip) property.

The below code snippet explains enabling tooltip only for expander column

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    
        //...
        showGridCellTooltip: true,
        showGridExpandCellTooltip: true
        //...
    ]
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/expander_tooltip.png)


## Clip Mode

Clip mode enables the TreeGrid to clip cell content and header content when the content exceeds the boundary of the cell width. 

We can specify the type of clip mode using the [`clipMode`](/api/js/ejtreegrid#members:columns-clipmode "columns.clipMode") property, clip mode will be enabled for both TreeGrid content and header of that specific column.

The below are the available clipping modes in TreeGrid.

1. Clip
2. Ellipsis

### Clip

When the [`clipMode`](/api/js/ejtreegrid#members:columns-clipmode "columns.clipMode") of Columns property is set as `ej.TreeGrid.ClipMode.Clip`, then it truncates the overflown text in the cell.

N> 1. By default the `clipMode` will be set as `Clip`.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    columns: [{
        field: "taskName",
        headerText: "Task Name",
        clipMode: ej.TreeGrid.ClipMode.Clip
    }, ]
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/clipmode.png)

### Ellipsis

When the [`clipMode`](/api/js/ejtreegrid#members:columns-clipmode "columns.clipMode") property is set as `ej.TreeGrid.ClipMode.Ellipsis` then it shows ellipsis for the overflown cell.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    columns: [{
        field: "taskName",
        headerText: "Task Name",
        clipMode: ej.TreeGrid.ClipMode.Ellipsis
    }, ]
});

{% endhighlight %}

The following output is shows the result of the above code example.

![](/js/TreeGrid/Cell/ellipsisMode.png)

## Text Wrap
Text wrap enables the TreeGrid to wrap cell content or header content to next line when the content exceeds the cell width.

### Header Text Wrap

To enable header cell text wrap, set the [`headerTextOverflow`](/api/js/ejtreegrid#members:headertextoverflow) property as `wrap`.

N> By default the `headerTextOverflow` will be set as `none`.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    headerTextOverflow: 'wrap',
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/headerTextOverflow.png)

### Content Text Wrap

To enable cell text wrap, set the [`allowTextWrap`](/api/js/ejtreegrid#members:allowtextwrap) property as `true`.

N> 1.By default the `allowTextWrap` will be set as `false`.

N> 2.The text wrap feature provide only limited support in virtualization mode.

The following code example describes the above behavior.

{% highlight js %}

$("#TreeGridContainer").ejTreeGrid({
    //...
    allowTextWrap: true,
});

{% endhighlight %}

The following output shows the result of above code example.

![](/js/TreeGrid/Cell/textWrap.png)