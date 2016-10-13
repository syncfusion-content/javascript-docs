---
layout: post
title: ejPivotCommon
documentation: API
platform: js
keywords: ejPivotCommon, API, Essential JS PivotCommon
metaname: 
metacontent: 
---

# PivotCommon
<ts  isFrameWork="true" />

#### Requires

* module:jQuery-3.0.0.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.menu.js
* module:ej.dialog.js
* module:ej.pivot.common.js

## Methods

### addReportItem()
{:#methods:addreportitem}

This function adds an item to the specified axis in specified position when the control is operated in ClientMode.

**Example:**

{% highlight javascript %}

    var args = {
        droppedFieldName : "Country",
        droppedFieldCaption : "Country",
        droppedAxis : "column",
        droppedPosition : 2,
        isMeasuresDropped : false //set to true on adding a measure in connection with OLAP database.
    };
    ej.Pivot.addReportItem(dataSource, args);
{% endhighlight %}

### removeReportItem()
{:#methods:removereportitem}

This function removes the specified item from the report.

**Example:**

{% highlight javascript %}

    var isMeasuresDropped = false;//set to true on removing a measure in connection with OLAP database.
    ej.Pivot.addReportItem(dataSource, "Country", isMeasuresDropped);
{% endhighlight %}

### getReportItemByFieldName()
{:#methods:getreportitembyfieldname}

This function returns the field object with the given field name.

**Example:**

{% highlight javascript %}

    var fieldObj = ej.Pivot.getReportItemByFieldName("Country", dataSource);
{% endhighlight %}

### getReportItemByFieldCaption()
{:#methods:getreportitembyfieldcaption}

This function returns the field object with the given field caption.

**Example:**

{% highlight javascript %}

    var fieldObj = ej.Pivot.getReportItemByFieldCaption("Country", dataSource);
{% endhighlight %}

### onPreventPanelClose()
{:#methods:onpreventpanelclose}

This function removes the overlay added to the control.

**Example:**

{% highlight javascript %}

    ej.Pivot.onPreventPanelClose(controlObject);
{% endhighlight %}

### getNodesState()
{:#methods:getnodesstate}

This function returns the list of checked and unchecked nodes from member editor tree.

**Example:**

{% highlight javascript %}

    var nodesState = ej.Pivot.getNodesState(treeViewObject);
{% endhighlight %}

## Enumerations

### AnalysisMode `enum`
{:#enum:analysismode}

<ts name = "ej.Pivot.AnalysisMode" />

Sets the mode for the component for binding either OLAP or Relational data source.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Pivot</td>
            <td class="description">To bind Relational datasource</td>
        </tr>
        <tr>
            <td class="name">Olap</td>
            <td class="description">To bind OLAP datasource</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotGrid1").ejPivotGrid({ analysisMode : ej.Pivot.AnalysisMode.Olap });
{% endhighlight %}

### OperationalMode `enum`
{:#enum:operationalmode}

<ts name = "ej.Pivot.OperationalMode" />

Sets the mode for the component for binding data source either in server-side or client-side.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ClientMode</td>
            <td class="description">To bind data source completely from client-side.</td>
        </tr>
        <tr>
            <td class="name">ServerMode</td>
            <td class="description">To bind data source completely from server-side.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}

    $("#PivotGrid1").ejPivotGrid({ analysisMode : ej.Pivot.AnalysisMode.Olap });
{% endhighlight %}