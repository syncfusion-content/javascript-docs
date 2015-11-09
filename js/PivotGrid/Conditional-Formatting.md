---
layout: post
title: Conditional-Formatting
description: conditional formatting
platform: js
control: PivotGrid
documentation: ug
---

#Conditional Formatting

Conditional formatting in the PivotGrid control allows you to define conditions on meeting that the cells are formatted with font, color and border settings. Conditional formatting dialog provides options at the UI-level to customize the appearance of the PivotGrid when conditions are satisfied. 

![](/js/PivotGrid/Conditional-Formatting_images/Conditional-Formatting_img1.png) 

Conditional formatting dialog can be launched by clicking a simple button in the application. The following code example illustrates how to launch the conditional formatting dialog.

{% highlight html %}

<button id="Button1">Export Grid</button>
<div id="PivotGrid1" style="height: 350px; width: 100%; overflow: auto"> </div> 

{% endhighlight %}

{% highlight js %}

$(function () {
    $("#PivotGrid1").ejPivotGrid({
         url: "../wcf/PivotGridService.svc",
         enableConditionalFormatting : true 
    });
    $("#Button1").ejButton({size: "normal",roundedCorner: true,click: "btnClick"});
});
function btnClick(e) {
   var pivotGridObj = $('#PivotGrid').data("ejPivotGrid");
   if (pivotGridObj.model.enableConditionalFormatting) {
       pivotGridObj.createConditionalDialog();
   }
}

{% endhighlight %}

The PivotGrid below is formatted with the following three conditions:

* Value < 10000 is marked in light brown.
* Value > 2500000 and Value < 3000000 are marked in green.
* Value > 5000000 is marked in yellow.


![](/js/PivotGrid/Conditional-Formatting_images/Conditional-Formatting_img2.png) 
