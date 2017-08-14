---
layout: post
title: Group by date
description: group by date
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

# Group by date

I> This feature is applicable for Relational datasource alone (in Client Mode).

Allows the user to categorize the date type field and showcase them based on year, quarter, month and day formats. 

{% highlight js %}

 $(function() {    
        $("#PivotGrid1").ejPivotGrid({
            dataSource: {
                //...
                columns: [{
                    fieldName: "Date",
                    fieldCaption: "Date",
                    format: "date",
                    formatString: "yyyy-MM-dd",
                    delimiter : "-",
                    groupByDate: { interval: ["yyyy", "qqq", "MMMM", "dd-MMM"] }
                }]
            }
        });
    });

  
{% endhighlight %}

The properties associated with group by date option is,

* format - To set the data type format. 
* formatString - Specifies the structure of the date format.
* delimiter - Specifies the separator of the date values.
* groupByDate.interval - Specifies the pattern in which date type to be displayed.

![](GroupByDate_images/group_by_date.png)
