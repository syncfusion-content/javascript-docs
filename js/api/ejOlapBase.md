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

#### Requires

* module:jQuery-3.0.0.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotgrid.js
* module:ej.pivotpager.js
* module:ej.olap.base.js


## Methods

### getJSONData()
{:#methods:getjsondata}

This function gets the datasource, action and grid layout for rendering the PivotGrid.

**Example:**

{% highlight javascript %}

    var args = controlInfo;//contains the information about the action performed
    ej.olap.getJSONData(args, dataSource, controlObj);
{% endhighlight %}