---
layout: post
title: Properties, Methods and Events of ejPivotSchemaDesigner Widget
documentation: API
platform: js
keywords: ejPivotSchemaDesigner, API, Essential JS PivotSchemaDesigner
metaname: 
metacontent: 
---

# PivotSchemaDesigner

PivotSchemaDesigner, also known as PivotTable Field List, is automatically populated with fields from the bound datasource and allows end user to drag fields, filter them, and create pivot views at run-time.

#### Syntax

{% highlight javascript %}

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

* module:jQuery-3.0.0
* module:ej.common.all
* module:ej.tools.js
* module:ej.pivot.common.js

## Members

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotSchemaDesigner to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ cssClass: "gradient-lime" });
{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ customObject: { "MyObject": "Hi Syncfusion!!" } });
{% endhighlight %}


### enableWrapper `boolean`
{:#members:enablewrapper}

For ASP.NET and MVC Wrapper, PivotSchemaDesigner will be initialized and rendered empty initially. Once the connected pivot control widget is rendered completely, PivotSchemaDesigner will just be populated with data source by setting this property to “true”.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ enableWrapper : true });
{% endhighlight %}


### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view PivotTable Field List from right to left.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ enableRTL : true });
{% endhighlight %}

### olap `object`
{:#members:olap}

Sets the visibility of OLAP elements in PivotTable Field List. This is only applicable for OLAP datasource.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ olap: olapSettings });
{% endhighlight %}

### olap.showKPI `boolean`
{:#members:olap-showkpi}

Allows the user to view the KPI elements in tree-view inside PivotTable Field List. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ olap: { showKPI : true } });
{% endhighlight %}


### olap.showNamedSets `boolean`
{:#members:olap-shownamedsets}

Allows the user to view the named sets in tree-view inside PivotTable Field List. This is only applicable for OLAP datasource.

#### Default Value: false

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ olap: { showNamedSets : true } });
{% endhighlight %}


### enableDragDrop `boolean`
{:#members:enabledragdrop}

Allows the user to restrict drag and drop operation within the PivotTable Field List.

#### Default Value: true

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ enableDragDrop : true });
{% endhighlight %}


### filters `array`
{:#members:filters}

Allows the user to set the list of filters in filter section.

#### Default Value: new Array()

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ filters: [] });
{% endhighlight %}

### height `string`
{:#members:height}

Sets the height for PivotSchemaDesigner.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ height: "630px" });
{% endhighlight %}


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ locale: "en-US" });
{% endhighlight %}


### pivotCalculations `array`
{:#members:pivotcalculations}

Allows the user to set list of PivotCalculations in values section.

#### Default Value: new Array()

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ pivotCalculations: [] });
{% endhighlight %}


### pivotColumns `array`
{:#members:pivotcolumns}

Allows the user to set the list of PivotItems in column section.

#### Default Value: new Array()

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotColumns: []});

{% endhighlight %}


### pivotControl `object`
{:#members:pivotcontrol}

Sets the Pivot control bound with this PivotSchemaDesigner.

#### Default Value: null

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotControl: controlObject});

{% endhighlight %}

### pivotRows `array`
{:#members:pivotrows}

Allows the user to set the list of PivotItems in row section.

#### Default Value: new Array()

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotRows: []});

{% endhighlight %}

### pivotTableFields `array`
{:#members:pivottablefields}

Allows the user to arrange the fields inside Field List of PivotSchemaDesigner.

#### Default Value: new Array()

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({pivotTableFields: []});

{% endhighlight %}

### serviceMethod  `object`
{:#members:servicemethod}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

#### Default Value: {}

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { initialize: "InitializeGrid"} });
{% endhighlight %}


### serviceMethod.fetchMembers  `string`
{:#members:servicemethod-fetchmembers}

Allows the user to set the custom name for the service method that’s responsible for getting the values for the tree-view inside filter dialog.

#### Default Value: "FetchMembers"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod:  { fetchMembers: "FetchMembersMethod" } });
{% endhighlight %}


### serviceMethod.filtering  `string`
{:#members:servicemethod-filtering}

Allows the user to set the custom name for the service method that’s responsible for filtering operation in Field List.

#### Default Value: "Filtering"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod:  { filtering : "FilteringMethod" } });
{% endhighlight %}


### serviceMethod.memberExpand `string`
{:#members:servicemethod-memberexpand}

Allows the user to set the custom name for the service method that’s responsible for the server-side action, on expanding members in Field List.

#### Default Value: "MemberExpanded"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { memberExpand: "MemberExpandedMethod" } });
{% endhighlight %}



### serviceMethod.nodeDropped `string`
{:#members:servicemethod-nodedropped}

Allows the user to set the custom name for the service method that’s responsible for the server-side action, on dropping a node into Field List.

#### Default Value: "NodeDropped"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { nodeDropped: "nodedroppedMethod" } });
{% endhighlight %}

### serviceMethod.nodeStateModified  `string`
{:#members:servicemethod-nodestatemodified }

Allows the user to set the custom name for the service method that’s responsible for the server-side action on changing the checked state of a node in Field List.

#### Default Value: "NodeStateModified"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { nodeStateModified: "NodeStateModifiedMethod" } });
{% endhighlight %}


### serviceMethod.removeButton `string`
{:#members:servicemethod-removebutton}

Allows the user to set the custom name for the service method that’s responsible for remove operation in Field List.

#### Default Value: "RemoveButton"

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { removeButton: "RemoveButtonMethod" } });
{% endhighlight %}


### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({url: "/wcf/PivotService.svc"});
{% endhighlight %}

### width `string`
{:#members:width}

Sets the width for PivotSchemaDesigner.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({width: "415px"});
{% endhighlight %}

### layout `enum`
{:#members:layout}

<ts name = "ej.PivotSchemaDesigner.Layouts"/>

Sets the layout for PivotSchemaDesigner.

#### Default Value: ej.PivotSchemaDesigner.Layouts.Excel

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Excel</td>
            <td class="description">To set the layout as same in the Excel.</td>
        </tr>
        <tr>
            <td class="name">Normal</td>
            <td class="description">To set normal layout for Field List.</td>
        </tr>
        <tr>
            <td class="name">OneByOne</td>
            <td class="description">To set layout with the axes one above the other.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ layout: ej.PivotSchemaDesigner.Layouts.Normal });
{% endhighlight %}

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").ejPivotSchemaDesigner({width: "415px"});
{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Performs an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight javascript %}
 
    var schemaObj = $("#PivotSchemaDesigner1").data("ejPivotSchemaDesigner");
    schemaObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
{% endhighlight %}

### refreshControl()
{:#methods:refreshControl}

Re-renders the control with the data source bound to the pivot control at that instant.

**Example:**

{% highlight javascript %}
 
    var schemaObj = $("#PivotSchemaDesigner1").data("ejPivotSchemaDesigner");
    schemaObj.refreshControl();
{% endhighlight %}


## Events

### afterServiceInvoke
{:#events:afterserviceinvoke}

Triggers when it reaches client-side after any AJAX request.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotSchemaDesigner control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotSchemaDesigner control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotSchemaDesigner control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").$("#PivotSchemaDesigner1")({
        afterServiceInvoke: function (args) {}
    });
{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotSchemaDesigner to service methods.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">returns the current action of PivotSchemaDesigner control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">returns the custom object bound with PivotSchemaDesigner control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">object</td>
<td class="description last">returns the HTML element of PivotSchemaDesigner control.</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").$("#PivotSchemaDesigner1")({
        beforeServiceInvoke: function (args) {}
    });      

{% endhighlight %}


### dragMove
{:#events:dragmove}

Triggers when we start dragging any field from PivotSchemaDesigner.

<table class="params">
<thead>
<tr>
<th colspan="3">Event Parameters</th>
</tr>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">dragTarget</td>
<td class="type">object</td>
<td class="description last">return the HTML of the dragged field from PivotSchemaDesigner.</td>
</tr>
<tr>
<td class="name">draggedElementData</td>
<td class="type">object</td>
<td class="description last">return the JSON details of the dragged field.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotSchemaDesigner.Model"/>object</td>
<td class="description last">returns the PivotSchemaDesigner model</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotSchemaDesigner1").$("#PivotSchemaDesigner1")({
        dragMove: function (args) {}
    });      

{% endhighlight %}