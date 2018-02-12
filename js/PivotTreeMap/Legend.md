---
layout: post
title: Legend
description: legend
platform: js
control: PivotTreeMap
documentation: ug
api: /api/js/ejpivottreemap
---

#Legend

##Legend visibility

The legend shows the value range differences and color occurrence in the respective leaf node while hovering it with a cursor.

N> By default, the legend is visible in the pivot tree map.

![](Legend_images/Legend_img1.png)

You can disable the legend by setting the property **showLegend** as **false**. The following code example illustrates how to disable the legend:

{% highlight js %}

 $(function() { 
        $("#PivotTreeMap1").ejPivotTreeMap({ 
            ....
            renderSuccess: showLegend 
       }); 
});
function showLegend(args) {	
        pivotTreeMap = $("#PivotTreeMap1TreeMapContainer").data("ejTreeMap");
        pivotTreeMap.model.showLegend = false;
        pivotTreeMap.refresh();
} 
</script>

<! --Tooltip labels can be localized here-->
<script id="tooltipTemplate" type="application/jsrender">
    <div style="background:White; color:black; font-size:12px; font-weight:normal; border: 1px solid #4D4D4D; white-space: nowrap;border-radius: 2px; margin-right: 25px; min-width: 110px;padding-right: 5px; padding-left: 5px; padding-bottom: 2px ;width: auto; height: auto;">
        <div>Measure(s) : {{:~Measures(#data)}}</div><div>Row : {{:~Row(#data)}}</div><div>Column : {{:~Column(#data)}}</div><div>Value : {{:~Value(#data)}}</div>
    </div>
</script>

{% endhighlight %}

![](Legend_images/Legend_img2.png)