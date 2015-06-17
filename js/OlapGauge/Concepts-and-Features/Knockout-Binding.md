---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: OLAP Gauge
documentation: ug
---

### Knockout Binding

Knockout Binding allows you to bind HTML elements against any data model. It uses a Model-View-ViewModel(MVVM) design pattern, where the Model is your stored data, View is the visual representation of that data (UI), and ViewModel acts as the intermediary between Model and View.

When using Knockout, the view page is simply a HTML document with declarative bindings that you can link to the ViewModel. ViewModel is nothing but an object, holding a list of items for creating the OlapGauge control by using Knockout Binding. When you call ko.applyBindings with a specific element it binds everything under that element.

The following code example illustrates how to bind data to the OlapGauge through Knockout Binding.

{% highlight js %}

var scale = [{
showRanges: true,
radius: 150, showScaleBar: true, size: 1,
border: {
width: 0.5
},
showIndicators: true, showLabels: true,
pointers: [{
showBackNeedle: true,
backNeedleLength: 20,
length: 125,
width: 7
},
{
type: "marker",
markerType: "diamond",
distanceFromScale: 5,
placement: "center",
backgroundColor: "#29A4D9",
length: 25,
width: 15
}],
ticks: [{
type: "major",
distanceFromScale: 2,
height: 16,
width: 1, color: "#8c8c8c"
}, {
type: "minor",
height: 6,
width: 1,
distanceFromScale: 2,
color: "#8c8c8c"
}],
labels: [{
color: "#8c8c8c"
}],
ranges: [{
distanceFromScale: -5,
backgroundColor: "#fc0606",
border: {
color: "#fc0606"
}
}, {
distanceFromScale: -5
}],
customLabels: [{
position: { x: 180, y: 290 },
font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
}, {
position: { x: 180, y: 320 },
font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
}, {
position: { x: 180, y: 150 },
font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
}]
}];
window.viewModel = {
url: ko.observable("../wcf/OlapGaugeService.svc"),
enableTooltip: ko.observable(true),
rowsCount: ko.observable(2),
columnsCount: ko.observable(3),
scales: ko.observable(scale),
background: ko.observable("transparent")
};
$(function () {
ko.applyBindings(viewModel);
});


{% endhighlight %}

{% highlight html %}

<div id="OlapGauge" data-bind="ejOlapGauge: { url: url, enableTooltip: enableTooltip, backgroundColor: background, scales: scales, rowsCount: rowsCount, columnsCount: columnsCount, load: 'loadGaugeTheme'}" />

<div>
     <input type="text" value="" data-bind="ejNumericTextbox: {value:rowsCount, minValue: 1 ,maxValue:3, width: '100px' }" data-bind="value:rowsCount" />
</div>
					
<div>
     <input type="text" value="" data-bind="ejNumericTextbox: {value:columnsCount, minValue: 1 ,maxValue:3, width: '100px' }" data-bind="value:columnsCount" />
</div>
					
{% endhighlight %}


