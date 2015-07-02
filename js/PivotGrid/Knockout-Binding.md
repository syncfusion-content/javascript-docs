---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: PivotGrid
documentation: ug
---

# Knockout Binding


Knockout Binding allows you to bind HTML elements against any data model. It uses a Model-View-ViewModel(MVVM) design pattern, where the Model is your stored data, View is the visual representation of that data (UI), and ViewModel acts as the intermediary between Model and View.

The data-bind attribute that is added cannot be identified directly by the HTML tags and also the browser on which we run that page. In order to work with Knockout, we need to declare the ko.applyBindings() function at the end of the script, so that the data-bind attribute will get recognised. Such Knockout code needs to be wrapped in a jQuery function as shown below within the script section, to work properly

The following code example illustrates how to bind data to the PivotGrid through Knockout Binding.

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
     <input type="text" id="gLayout" name="name" data-bind="ejDropDownList: {dataSource: layout, value: gridLayout, width: width}"/>
</div>
											
{% endhighlight %}

> **Note:** This feature is applicable only for OLAP datasource.
