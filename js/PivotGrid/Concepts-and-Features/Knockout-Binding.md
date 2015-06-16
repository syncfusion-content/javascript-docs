---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: PivotGrid
documentation: ug
---

### Knockout Binding

>_**Note: This feature is applicable only for OLAP datasource.**_

Knockout binding allows you to bind HTML elements against any data model. It uses a Model-View-ViewModel(MVVM) design pattern, where the Model is your stored data, View is the visual representation of that data (UI), and ViewModel acts as the intermediary between the Model and the View.

When using KO, the view page is simply a HTML document with declarative bindings that you can link to the ViewModel. ViewModel is nothing but an object, holding a list of items for creating the OlapGauge control by using Knockout binding. When you call ko.applyBindings with a specific element, it binds everything under that element.

The following code example illustrates how to bind data to the OlapGauge through Knockout Support.

{% highlight js %}

var layouts = [{ text: "Normal", value: "normal" }, { text: "NoSummaries", value: "nosummaries" }, { text: "NormalTopSummary", value: "normaltopsummary" }, { text: "ExcelLikeLayout", value: "excelLikeLayout" }];
window.viewModel = {
        url: ko.observable("../wcf/OLAPService.svc"),
        layout: ko.observable(layouts),
        gridLayout: ko.observable(ej.PivotGrid.Layout.Normal),
        width: ko.observable("100px")
};
$(function () {
        ko.applyBindings(viewModel);                        
});

{% endhighlight %}

{% highlight html %}

<div id="PivotGrid" data-bind="ejPivotGrid: { url: url, layout: gridLayout}" />

<div>
     <input type="text" id="gLayout" name="name" data-bind="ejDropDownList: {dataSource: layout, value: gridLayout, width: width}" />
</div>
											
{% endhighlight %}


