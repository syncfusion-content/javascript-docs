---
layout: post
title: ejPivotAnalysisBase
documentation: API
platform: js
keywords: ejPivotAnalysisBase, API, Essential JS PivotAnalysisBase
metaname: 
metacontent: 
---

# PivotAnalysisBase
<ts  isFrameWork="true" />

This section contains the properties and methods available for all the Pivot Controls operated in client mode with Relational data. 

#### Requires

* module:jQuery-3.0.0.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.pivot.common.js
* module:ej.pivotanalysis.base.js

## Methods

### setFieldCaptions()
{:#methods:setfieldcaptions}

This function sets the caption for all fields in datasource is it is not set.

**Example:**

{% highlight javascript %}

    ej.PivotAnalysis.setFieldCaptions(dataSourceObj);
{% endhighlight %}

### getTreeViewData()
{:#methods:gettreeviewdata}

This function returns the data required to render the field list formed from the raw data source.

**Example:**

{% highlight javascript %}

    var treeViewData = ej.PivotAnalysis.getTreeViewData(dataSourceObj);
{% endhighlight %}

### pivotEnginePopulate()
{:#methods:pivotenginepopulate}

This function forms the pivot engine and JSON data required to render the Pivot Controls from the datasource.

**Example:**

{% highlight javascript %}

    var jsonData = ej.PivotAnalysis.pivotEnginePopulate(pivotControlModel);
{% endhighlight %}

### getMembers()
{:#methods:getmembers}

This function returns the list of members available in the given field.

**Example:**

{% highlight javascript %}

    var fieldMembers = ej.PivotAnalysis.getMembers(fieldObj);
{% endhighlight %}