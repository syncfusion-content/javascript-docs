---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: OLAP Client
documentation: ug
---

### Knockout Binding

Knockout Binding allows you to bind HTML elements against any data model. It uses a Model-View-ViewModel(MVVM) design pattern, where the Model is your stored data, View is the visual representation of that data (UI), and ViewModel acts as the intermediary between Model and View.

When using Knockout, the view page is simply a HTML document with declarative bindings that you can link to the ViewModel. ViewModel is nothing but an object, holding a list of items for creating the OlapClient control by using Knockout Binding. When you call ko.applyBindings with a specific element it binds everything under that element.

The following code example illustrates how to bind data to the OlapClient through Knockout Binding.

{% highlight js %}

var layouts = [{ text: "Normal", value: "normal" }, { text: "NoSummaries", value: "nosummaries" }, { text: "NormalTopSummary", value: "normaltopsummary" }, { text: "ExcelLikeLayout", value: "excelLikeLayout" }];
var dispOptions = {
    mode: ej.olap.OlapClient.DisplayMode.ChartAndGrid,
    defaultView: ej.olap.OlapClient.DefaultView.Grid
}
window.viewModel = {
    url: ko.observable("../wcf/OlapClientService.svc"),
    title: ko.observable("OLAP Browser"),
    gridLayout: ko.observable(ej.PivotGrid.Layout.NoSummaries),
    displaySettings: ko.observable(dispOptions),
    layout: ko.observable(layouts),
    width: ko.observable("100px")
};
$(function () {
    ko.applyBindings(viewModel);            
});

{% endhighlight %}

{% highlight html %}

<div id="OlapClient" data-bind="ejOlapClient: { url: url, title: title, gridLayout: gridLayout, displaySettings: displaySettings, chartLoad: 'setChartProperties' }" />
    
<div>
     <input type="text" id="gLayout" name="name" data-bind="ejDropDownList: {dataSource: layout, value: gridLayout, width: width}" />
</div>

<div>
     <textarea type="text" name="slide" value="" data-bind="value: title"></textarea>
</div>

{% endhighlight %}



