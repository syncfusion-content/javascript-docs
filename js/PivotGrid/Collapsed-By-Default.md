---
layout: post
title: Collapse by default
description: Collapse by default
platform: js
control: PivotGrid
documentation: ug
api: /api/js/ejpivotgrid
---

I> These features are applicable only for the relational datasource.

# Collapse by default

Allows you to collapse all members displayed in the grid. You can enable collapsing all members by default in the PivotGrid by setting the [`enableCollapseByDefault`](/api/js/ejpivotgrid#members:enablecollapsebydefault) property to true.

{% highlight js %}
   
    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //..
            enableCollapseByDefault:true
        });
    });

{% endhighlight %}

![](Collapsed-By-Default_images/Collapse-members.png)

# Collapsed Members
Allows you to collapse the specified members in each field of PivotGrid control. You can collapse desired members in Pivotgrid by setting the [`collapsedMembers`](/api/js/ejpivotgrid#members:collapsedmembers).

{% highlight js %}

    $(function() {
        $("#PivotGrid1").ejPivotGrid({
            //..
            rows: [
                    {
                      fieldName: "Country",
                      fieldCaption: "Country"
                    },
                    {
                      fieldName: "State",
                      fieldCaption: "State"
                    }
                ]
                //..
            collapsedMembers: { Country: ["Canada", "France"] }
        });
    });

{% endhighlight %}

![](Collapsed-By-Default_images/collapsedMembers.png)
