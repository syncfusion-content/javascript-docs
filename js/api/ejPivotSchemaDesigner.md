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

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ customObject: {"MyObject": "Hi Syncfusion!!"} });

{% endhighlight %}


### enableWrapper `boolean`
{:#members:enablewrapper}

For ASP.NET and MVC Wrapper, Pivots Shema Designer will be initialized and rendered empty initially. Once PivotGrid widget is rendered completely, Pivots Shema Designer will just be populated with data source by setting this property to “true”.

**Default Value:** false

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ enableWrapper : true });

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


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

**Default Value:** "en-US"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ locale: "en-US" }); 

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

### serviceMethod  `object`
{:#members:servicemethod}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

**Default Value:** {}

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { initialize: "InitializeGrid"} });

{% endhighlight %}


### serviceMethod.fetchMembers  `string`
{:#members:servicemethod-fetchmembers}

Allows the user to set the custom name for the service method that’s responsible for getting the values for the tree-view inside filter dialog.

**Default Value:** "FetchMembers"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod:  { fetchMembers: "FetchMembersMethod" } });

{% endhighlight %}


### serviceMethod.filtering  `string`
{:#members:servicemethod-filtering}

Allows the user to set the custom name for the service method that’s responsible for filtering operation in Field List.

**Default Value:** "Filtering"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod:  { filtering : "FilteringMethod" } });

{% endhighlight %}


### serviceMethod.memberExpand `string`
{:#members:servicemethod-memberexpand}

Allows the user to set the custom name for the service method that’s responsible for the server-side action, on expanding members in Field List.

**Default Value:** "MemberExpanded"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { memberExpand: "MemberExpandedMethod" } });

{% endhighlight %}



### serviceMethod.nodeDropped `string`
{:#members:servicemethod-nodedropped}

Allows the user to set the custom name for the service method that’s responsible for the server-side action, on dropping a node into Field List.

**Default Value:** "NodeDropped"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { nodeDropped: "nodedroppedMethod" } });

{% endhighlight %}

### serviceMethod.nodeStateModified  `string`
{:#members:servicemethod-nodestatemodified }

Allows the user to set the custom name for the service method that’s responsible for the server-side action on changing the checked state of a node in Field List.

**Default Value:** "NodeStateModified"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { nodeStateModified: "NodeStateModifiedMethod" } });

{% endhighlight %}


### serviceMethod.romveButton `string`
{:#members:servicemethod-romvebutton}

Allows the user to set the custom name for the service method that’s responsible for remove operation in Field List.

**Default Value:** "RemoveButton"

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").ejPivotSchemaDesigner({ serviceMethod: { removeButton: "RemoveButtonMethod" } });

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


## Events

### afterServiceInvoke
{:#events:afterserviceinvoke}

Triggers when it reaches client-side after any AJAX request.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotSchemaDesinger
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the current action of PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the PivotSchemaDesinger model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").$("#PivotSchemaDesigner1")({
   afterServiceInvoke: function (args) {}
});     

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotSchemaDesinger to service methods.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type">Object</td>
<td class="description">Event parameters from PivotSchemaDesinger
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
action{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the current action of PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
customObject{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">return the custom object bounds with PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">return the outer HTML of PivotSchemaDesinger control.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type">boolean</td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type">object</td>
<td class="description">returns the PivotSchemaDesinger model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type">string</td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#PivotSchemaDesigner1").$("#PivotSchemaDesigner1")({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}

