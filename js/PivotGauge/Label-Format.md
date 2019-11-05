---
layout: post
title: Label Format | JavaScript | PivotGauge | Syncfusion
description: This document illustrates that how to define label format feature and its functionalities in JavaScript PivotGauge control
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# Label format

You can customize the format of labels that is displayed in the pivot gauge control by using the [`labelFormatSettings`](/api/js/ejpivotgauge#members:labelformatsettings) property.

Following are the formats that can be applied to labels in the pivot gauge:

* [`numberFormat`](/api/js/ejpivotgauge#members:labelformatsettings-numberformat) - Allows you to change the number format of label values in the pivot gauge.
* [`decimalPlaces`](/api/js/ejpivotgauge#members:labelformatsettings-decimalplaces) - Allows you to set the number of digits that are displayed after the decimal point.
* [`prefixText `](/api/js/ejpivotgauge#members:labelformatsettings-prefixtext) - Allows you to add a text at the beginning of the label.
* [`suffixText `](/api/js/ejpivotgauge#members:labelformatsettings-suffixtext) - Allows you to add a text at the end of the label.

The number format for label values can be set to any of the following types:

* Default	
* Currency
* Percentage
* Fraction
* Scientific
* Text
* Notation

{% highlight js %}

$(function () {
    $("#PivotGauge").ejPivotGauge({
	  //...
      labelFormatSettings: { numberFormat: ej.PivotGauge.NumberFormat.Percentage, decimalPlaces: 2, prefixText: "#*", suffixText: "*#" },
     //... 
    });
});
{% endhighlight %}

![Label formats in JavaScript pivot gauge control](Label-Format_images/labelformat.png) 
