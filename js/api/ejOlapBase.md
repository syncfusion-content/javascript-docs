---
layout: post
title: ejOlapBase
documentation: API
platform: js
keywords: ejOlapBase, API, Essential JS OlapBase
metaname: 
metacontent: 
---

# OlapBase
<ts  isFrameWork="true" />

Support has been provided in PivotGrid to load OLAP Cube information at client-side directly through XML/A. 

#### Requires

* module:jQuery-1.10.2.min.js
* module:jQuery.easing.1.3.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotgrid.js
* module:ej.pivotpager.js
* module: ej.olap.base.js


## Methods

### getJSONData()
{:#methods:getjsondata}

This function gets the datasource, action and grid layout for rendering the PivotGrid.


## Members

### SortOrder  `string`
{:#members:sortorder}

<ts name = "ej.olap.SortOrder"/>

Sets the sort order for the specified row/column values.


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ sortOrder : ej.olap.SortOrder.Ascending }]}});

{% endhighlight %}


### AdvancedFilterType  `string`
{:#members:advancedfiltertype}

<ts name = "ej.olap.AdvancedFilterType"/>

Sets the type of filter while doing advanced filtering (excel-like) in OLAP client-side components.


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter}]}]}});

{% endhighlight %}


### ValueFilterOptions  `string`
{:#members:valuefilteroptions}

<ts name = "ej.olap.ValueFilterOptions"/>

Sets the options for value filter in advanced filtering (excel-like) concept available in OLAP client-side components.


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{valueFilterOperator: ej.olap.ValueFilterOptions.Between}]}]}});

{% endhighlight %}


### LabelFilterOptions  `string`
{:#members:labelfilteroptions}

<ts name = "ej.olap.LabelFilterOptions"/>

Sets the options for label filter in advanced filtering (excel-like) concept available in OLAP client-side components.


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith}]}]}});

{% endhighlight %}


### AxisName  `string`
{:#members:axisname}

<ts name = "ej.olap.AxisName"/>

Allows the user to set the axis position to place the value items available in the report.


**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{axis : ej.olap.AxisName.Row}]}});

{% endhighlight %}
