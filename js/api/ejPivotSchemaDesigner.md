---
layout: post
title: ejPivotSchemaDesigner
documentation: API
platform: js
keywords: ejPivotSchemaDesigner, API, Essential JS PivotSchemaDesigner
metaname: 
metacontent: 
---

# PivotSchemaDesigner

PivotSchemaDesigner, also known as PivotTable Field List, is automatically populated with fields from the bound datasource and allows end user to drag fields, filter them, and create pivot views at run-time.

#### Syntax

{% highlight js %}

$(element).ejPivotSchemaDesigner()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="PivotSchemaDesigner1"> </div> 
 
<script>
// Create PivotSchemaDesigner
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner(...);   
</script>

{% endhighlight %}


#### Requires

* module:jQuery
* module:ej.common.all
* module:ej.tools.js

## Members

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotSchemaDesigner to achieve custom theme.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({cssClass: "gradient-lime"});

{% endhighlight %}


### filters `array`
{:#members:filters}

Allows the user to set the list of filters in filter section.

**Default Value:** new Array()

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({filters: []});

{% endhighlight %}

### height `string`
{:#members:height}

Sets the height for PivotSchemaDesigner.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({height: "630px"});     

{% endhighlight %}

### pivotCalculations `array`
{:#members:pivotcalculations}

Allows the user to set list of PivotCalculations in values section.

**Default Value:** new Array()

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotCalculations: []});

{% endhighlight %}


### pivotColumns `array`
{:#members:pivotcolumns}

Allows the user to set the list of PivotItems in column section.

**Default Value:** new Array()

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotColumns: []});

{% endhighlight %}


### pivotControl `object`
{:#members:pivotcontrol}

Sets the Pivot control bound with this PivotSchemaDesigner.

**Default Value:** null

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotControl: controlObject});

{% endhighlight %}

### pivotRows `array`
{:#members:pivotrows}

Allows the user to set the list of PivotItems in row section.

**Default Value:** new Array()

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotRows: []});

{% endhighlight %}

### pivotTableFields `array`
{:#members:pivottablefields}

Allows the user to arrange the fields inside Field List of PivotSchemaDesigner.

**Default Value:** new Array()

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotTableFields: []});

{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({url: "/wcf/PivotService.svc"});

{% endhighlight %}

### width `string`
{:#members:width}

Sets the width for PivotSchemaDesigner.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({width: "415px"}); 

{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="PivotSchemaDesigner1"></div> 
 
<script>
var gridObj = $("#PivotSchemaDesigner1").data("ejPivotSchemaDesigner");
gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
</script>

{% endhighlight %}



