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

The stacked headers helps you to group the logical columns in treegrid. It can be shown by setting [`showStackedHeader`](https://help.syncfusion.com/api/js/ejtreegrid#members:showstackedheader "showStackedHeader") as `true` and by defining [`stackedHeaderRows`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows "stackedHeaderRows").

## Adding Stacked header columns

To stack columns in stacked header, you need to define [`column`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns-column "column") property in [`stackedHeaderColumns`](https://help.syncfusion.com/api/js/ejtreegrid#members:stackedheaderrows-stackedheadercolumns "stackedHeaderColumns") with field names of visible columns.

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

## Stacked header column customization

we can customize the stacked header cells with more options as described below.

### CSS Class

You can provide external CSS styles to the stacked header with the help of cssClass property.

{% highlight html %}

<style>
  .temp {
            background-color: red; 
        }
</style>

<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
   showStackedHeader:true,
   stackedHeaderRows:
   [{
	   stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details", cssClass:"temp" 
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details"
                }
            ]
        ]
    }, 
   ]},  
});
</script> 

{% endhighlight %}

### Text Align

There is an option to align the stacked header text inside the header cell using `textAlign` property as follows.

{% highlight html %}

<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
   showStackedHeader:true,
   stackedHeaderRows:
   [{
	   stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details", textAlign: ej.TextAlign.Center 
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details"
                }
            ]
        ]
    },  
   ]},  
});
</script> 

{% endhighlight %}

### Tooltip

We can have the customized tooltip for the stacked header text with the help of `tooltip` property. JsRender template script id can be assigned to this property to get tooltip.

{% highlight html %}

<div id="treeGrid"></div> 
<script>
$("#treeGrid").ejTreeGrid({
   showStackedHeader:true,
   stackedHeaderRows:
   [{
	   stackedHeaderRows: [{
            stackedHeaderColumns: [{
                    column: "ID,Name,category,units",
                    headerText: "Shipment details", tooltip: "#tooltip"
                },
                {
                    column: "unitPrice,price",
                    headerText: "Price details"
                }
            ]
        ]
    },      
   ]},  
});
</script> 

{% endhighlight %}
