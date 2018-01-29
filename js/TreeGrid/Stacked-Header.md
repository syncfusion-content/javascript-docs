---
layout: post
title: Stacked Headers with TreeGrid widget for Syncfusion Essential JS
description: How to stack column Header and customize it
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---
# Stacked Headers

The stacked headers helps you to group the logical columns in TreeGrid. It can be shown by setting the [`showStackedHeader`](https://help.syncfusion.com/api/js/ejtreegrid#members:showstackedheader "showStackedHeader") as `true` and by defining the [`stackedHeaderRows`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows "stackedHeaderRows").

## Adding Stacked header columns

To stack columns in stacked header, you need to define the [`column`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-column "column") property in [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns "stackedHeaderColumns") with field names of visible columns.

{% highlight html %}

<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
    showStackedHeader: true,
    stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details"
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details"
                }
            ]
        ]
    },
    columns: [{ field: "ID", headerText: "S.No", width: columnWidth },
              { field: "Name", headerText: "Shipment Name", isFrozen: true },
              { field: "category", headerText: "Category" },
              { field: "units", headerText: "Units" },
              { field: "unitPrice", headerText: "Unit Price($)" },
              { field: "price", headerText: "Price($)" }
             ]
});
</script> 

{% endhighlight %}

![](Stacked-header_images/Stacked-Header-img1.png)

### Stacked header text

Using [`headerText`](/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-headertext "stackedHeaderRows.stackedHeaderColumns.headerText") property you can provide title for the specific stacked header column.

The following code example explains how to set header text for stacked header

{% highlight js %}

      $("#treegrid").ejTreeGrid({
          //...     
          showStackedHeader: true,
          stackedHeaderRows: [{
              stackedHeaderColumns: [{
                        column: "ID,Name,units",
                        headerText: "Shipment details"
                    },
                    {
                        column: "unitPrice,price",
                        headerText: "Price details"
                    }
                ]
            ]
          },
          // ...
    });

{% endhighlight %}

The following screenshot shows TreeGrid with stacked header text

![](Stacked-header_images/Stacked-Header-img5.png)


## Stacked header column customization

The stacked header cells can be customized with more options as described below.

### CSS Class

You can provide external CSS styles to the stacked header with the help of the [`cssClass`](/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-cssclass "stackedHeaderRows.stackedHeaderColumns.cssClass") property.

{% highlight html %}

<style>
  .stack {
            background-color: #ffb3b3; 
        }
</style>

<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
    showStackedHeader: true,
    stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details",
		    cssClass: "stack"
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details"
                }
            ]
        ]
    },
});
</script> 

{% endhighlight %}

![](Stacked-header_images/Stacked-Header-img2.png)

### Text Align

There is an option to align the stacked header text inside the header cell using the [`textAlign`](/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-textalign "stackedHeaderRows.stackedHeaderColumns.textAlign") property as follows.

{% highlight html %}
<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
    showStackedHeader: true,
    stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details",
		    textAlign:ej.TextAlign.Left 
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details",
		    textAlign: ej.TextAlign.Right 
                }
            ]
        ]
    },
});
</script> 

{% endhighlight %}

![](Stacked-header_images/Stacked-Header-img4.png)

### Tooltip

We can have the customized tooltip for the stacked header text with the help of the [`tooltip`](/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-tooltip "stackedHeaderRows.stackedHeaderColumns.tooltip") property. The JsRender template script id can be assigned to this property to get tooltip.

{% highlight html %}

<div id="treeGrid"></div> 
<script id="tooltip" type="text/x-jsrender">
        <div>Custom Tooltip</div>
</script>
<script>
$("#treeGrid").ejTreeGrid({
    showStackedHeader: true,
    stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details",
		   
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details",
		    tooltip: "#tooltip" 
                }
            ]
        ]
    },
});
</script> 

{% endhighlight %}

![](Stacked-header_images/Stacked-Header-img3.png)

N>
To enable stacked header tooltip we need to set the `showGridCellTooltip` as `true`.

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/columns/stackedheader) here to view the demo sample for stacked header.