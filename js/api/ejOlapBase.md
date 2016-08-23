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


## Enumeration

### SortOrder  `enum`
{:#enum:sortorder}

<ts name = "ej.olap.SortOrder"/>

Sets the sort order for the specified row/column values.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">To arrange the specified row/column values without any sorting.</td>
        </tr>
        <tr>
            <td class="name">Ascending</td>
            <td class="description">To arrange the specified row/column values in ascending order.</td>
        </tr>
		<tr>
            <td class="name">Descending</td>
            <td class="description">To arrange the specified row/column values in descending order.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ sortOrder : ej.olap.SortOrder.Ascending }]}});

{% endhighlight %}


### AdvancedFilterType  `enum`
{:#enum:advancedfiltertype}

<ts name = "ej.olap.AdvancedFilterType"/>

Sets the type of filter while doing advanced filtering (excel-like) in OLAP client-side components.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">LabelFilter</td>
            <td class="description">To filter the members of an hierarchy element by its names.</td>
        </tr>
        <tr>
            <td class="name">ValueFilter</td>
            <td class="description">To filter the members of an hierarchy element by its total value.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{advancedFilterType:  ej.olap.AdvancedFilterType.LabelFilter}]}]}});

{% endhighlight %}


### ValueFilterOptions  `enum`
{:#enum:valuefilteroptions}

<ts name = "ej.olap.ValueFilterOptions"/>

Sets the options for value filter in advanced filtering (excel-like) concept available in OLAP client-side components.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">Doesn't allow the value filtering operation.</td>
        </tr>
        <tr>
            <td class="name">Equals</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is equal to the provided value.</td>
        </tr>
		<tr>
            <td class="name">NotEquals</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is not equal to the provided value.</td>
        </tr>
        <tr>
            <td class="name">GreaterThan</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is greater than the provided value.</td>
        </tr>
		<tr>
            <td class="name">GreaterThanOrEqualTo</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is greater than or equal to the provided value.</td>
        </tr>
        <tr>
            <td class="name">LessThan</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is less than the provided value.</td>
        </tr>
		<tr>
            <td class="name">LessThanOrEqualTo</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is less than or equal to the provided value.</td>
        </tr>
		<tr>
            <td class="name">Between</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is in-between the provided values.</td>
        </tr>
        <tr>
            <td class="name">NotBetween</td>
            <td class="description">To filter the members of a hierarchy element by its total value which is not between the provided values.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{valueFilterOperator: ej.olap.ValueFilterOptions.Between}]}]}});

{% endhighlight %}


### LabelFilterOptions  `enum`
{:#enum:labelfilteroptions}

<ts name = "ej.olap.LabelFilterOptions"/>

Sets the options for label filter in advanced filtering (excel-like) concept available in OLAP client-side components.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">None</td>
            <td class="description">Doesn't allow the label filtering operation.</td>
        </tr>
        <tr>
            <td class="name">BeginsWith</td>
            <td class="description">To filter the members of a hierarchy element by its name which begins with the provided string.</td>
        </tr>
		<tr>
            <td class="name">NotBeginsWith</td>
            <td class="description">To filter the members of a hierarchy element by its name which doesn't begins with the provided string.</td>
        </tr>
        <tr>
            <td class="name">EndsWith</td>
            <td class="description">To filter the members of a hierarchy element by its name which ends with the provided string.</td>
        </tr>
		<tr>
            <td class="name">NotEndsWith</td>
            <td class="description">To filter the members of a hierarchy element by its name which doesn't ends with the provided string.</td>
        </tr>
        <tr>
            <td class="name">Contains</td>
            <td class="description">To filter the members of a hierarchy element by its name which contains the provided string.</td>
        </tr>
		<tr>
            <td class="name">NotContains</td>
            <td class="description">To filter the members of a hierarchy element by its name which doesn't contains the provided string.</td>
        </tr>
		<tr>
            <td class="name">Equals</td>
            <td class="description">To filter the members of a hierarchy element by its name which equals to the provided string.</td>
        </tr>
        <tr>
            <td class="name">NotEquals</td>
            <td class="description">To filter the members of a hierarchy element by its name which doesn't equals to the provided string.</td>
        </tr>
		<tr>
            <td class="name">GreaterThan</td>
            <td class="description">To filter the members of a hierarchy element by its name where its first letter is next to the first letter of the provided member name in alphabetical order.</td>
        </tr>
		<tr>
            <td class="name">GreaterThanOrEqualTo</td>
            <td class="description">To filter the members of a hierarchy element by its name where its first letter is next or equal to the first letter of the provided member name in alphabetical order.</td>
        </tr>
        <tr>
            <td class="name">LessThan</td>
            <td class="description">To filter the members of a hierarchy element by its name where its first letter is before to the first letter of the provided member name in alphabetical order.</td>
        </tr>
		<tr>
            <td class="name">LessThanOrEqualTo</td>
            <td class="description">To filter the members of a hierarchy element by its name where its first letter is before or equal to the first letter of the provided member name in alphabetical order.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotGrid1").ejPivotGrid({dataSource: {columns: [{ advancedFilter : [{labelFilterOperator: ej.olap.LabelFilterOptions.EndsWith}]}]}});

{% endhighlight %}


### AxisName  `enum`
{:#enum:axisname}

<ts name = "ej.olap.AxisName"/>

Allows the user to set the axis position to place the value items available in the report.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Row</td>
            <td class="description">To place the value items in row axis.</td>
        </tr>
        <tr>
            <td class="name">Column</td>
            <td class="description">To place the value items in column axis.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotGrid1").ejPivotGrid({dataSource: {values: [{axis : ej.olap.AxisName.Row}]}});

{% endhighlight %}
