---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: OLAP Chart
documentation: ug
---

### Knockout Binding

Knockout Binding allows you to bind HTML elements against any data model. It uses a Model-View-ViewModel(MVVM) design pattern, where the Model is your stored data, View is the visual representation of that data (UI), and ViewModel acts as the intermediary between Model and View.

When using Knockout, the view page is simply a HTML document with declarative bindings that you can link to the ViewModel. ViewModel is nothing but an object, holding a list of items for creating the OlapChart control by using Knockout Binding. When you call ko.applyBindings with a specific element it binds everything under that element.

The following code example illustrates how to bind data to the OlapChart through Knockout Binding.

{% highlight js %}

var cSize = { height: "460px", width: "650px" },
              PXaxis = { title: { text: "Fiscal Year" }, labelRotation: 0 },
              PYaxis = { title: { text: "Customer Count"} },
              cLegend = { visible: true, rowCount: 2 };
var chartTypes = [{ text: "Column", value: "column" }, { text: "Line", value: "line" }, { text: "Spline", value: "spline" }, { text: "Area", value: "area" }, { text: "Bar", value: "bar" },
              { text: "Pie", value: "pie" }, { text: "Pyramid", value: "pyramid" }, { text: "StepLine", value: "stepline" }, { text: "SplineArea", value: "splinearea" }, { text: "StepArea", value: "steparea" },
              { text: "StackingArea", value: "stackingarea" }, { text: "StackingColumn", value: "stackingcolumn" }, { text: "StackingBar", value: "stackingbar" }, { text: "Funnel", value: "funnel" }];
window.viewModel = {
              url: ko.observable("../wcf/OlapChartService.svc"),
              title: ko.observable("OLAP Chart in Essential JS"),
              type: ko.observable(ej.olap.OlapChart.ChartTypes.Column),
              showTooltip: ko.observable(true),
              animation: ko.observable(true),
              size: ko.observable(cSize),
              primaryYAxis: ko.observable(PYaxis),
              primaryXAxis: ko.observable(PXaxis),
              legend: ko.observable(cLegend),
              list: ko.observable(chartTypes),
              width: ko.observable("100px")
};
$(function () {
              ko.applyBindings(viewModel);
});

{% endhighlight %}

{% highlight html %}

<div id="OlapChart" data-bind="ejOlapChart: { url: url, title: {text: title}, showTooltip: showTooltip, animation: animation, commonSeriesOptions: {type: type, tooltip: {visible: showTooltip}}, size: size, primaryXAxis: primaryXAxis, primaryYAxis: primaryYAxis, legend: legend, load: 'loadTheme'}" />
    
<div>
     <input type="text" id="chartType" name="name" data-bind="ejDropDownList: {dataSource: list, value: type, width: width}" />
</div>

<div>
     <textarea type="text" name="slide" value="" data-bind="value: title">
     </textarea>
</div>

{% endhighlight %}



