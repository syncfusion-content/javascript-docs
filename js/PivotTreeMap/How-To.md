---
layout: post
title: How To
description: How To
platform: js
control: PivotTreeMap
documentation: ug
api: /api/js/ejpivottreemap
---

# How to

### Generate JSON object from Olap Cube
The [`generateJSON`](/api/js/ejpivottreemap#methods:generateJSON) method is used to render the control with the pivot engine obtained from OLAP cube.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.generateJSON(baseObj, pivotEngineObj);
</script>

{% endhighlight %}

### Explicit asynchronous invoke
The [`doAjaxPost`](/api/js/ejpivottreemap#methods:doajaxpost) method is used to perform an asynchronous HTTP (AJAX) request.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.doAjaxPost("POST", "/PivotTreeMapService.svc/Initialize", { "key", "Hello World" }, successEvent, null);
</script>

{% endhighlight %}

### Destroying object of PivotTreeMap Component
The [`destroy`](/api/js/ejpivottreemap#methods:destroy) method is used to destroy the PivotChart widget associated events that are bound using "this._on" and brings the control to pre-init state.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.destroy();
</script>

{% endhighlight %}

### Getting JSON Records from control object
The [`getJSONRecords`](/api/js/ejpivottreemap#methods:getjsonrecords) method is used to return the JSON records formed to render the control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.getJSONRecords();
</script>

{% endhighlight %}

### Setting JSON Records to control object
The [`setJSONRecords`](/api/js/ejpivottreemap#methods:setjsonrecords) method is used to set the JSON records to render the PivotChart control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.setJSONRecords(pivotTreemap.getJSONRecords());
</script>

{% endhighlight %}

### Invoking event before Pivot Engine population
The [`beforePivotEnginePopulate`](/api/js/ejpivottreemap#events:beforePivotEnginePopulate) event is triggered before populating the pivot engine from datasource.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       beforePivotEnginePopulate: function (args) {

    });
</script>

{% endhighlight %}

### Invoking event in client-side after service invoke
The [`afterServiceInvoke`](/api/js/ejpivottreemap#events:afterserviceinvoke) event is triggered when it is reached the client-side after any AJAX request.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       afterServiceInvoke: function (args) {

    });
</script>

{% endhighlight %}

### Invoking event in client-side before service invoke
The [`beforeServiceInvoke`](/api/js/ejpivottreemap#events:beforeserviceinvoke) event is triggered before any AJAX request is passed from PivotTreeMap to service methods.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       beforeServiceInvoke: function (args) {

    });
</script>

{% endhighlight %}

### Triggering event after performing drill operation
The [`drillSuccess`](/api/js/ejpivottreemap#events:drillsuccess) event is triggered when drill up/down happens in PivotTreeMap control. And it returns the outer HTML of PivotTreeMap control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       drillSuccess: function (args) {

    });
</script>

{% endhighlight %}

### Triggering event before the PivotTreeMap loaded
The [`load`](/api/js/ejpivottreemap#events:load) event is triggered when the pivot treemap is started to render.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       load: function (args) {

    });
</script>

{% endhighlight %}


## Members

### Responsive layout of PivotTreeMap component
You can enable/disable responsiveness in the browser layout for pivot treemap control by setting [`isResponsive`](/api/js/ejpivottreemap#members:isresponsive) property.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       isResponsive: true

    });
</script>

{% endhighlight %}


## Setting Custom Name to Service Methods
The [`serviceMethodSettings`](/api/js/ejpivottreemap#members:servicemethodsettings) allows you to set the custom name for the methods in WebAPI/WCF, communicated during AJAX post. The following table will explain the service methods.

| Service Methods | Description |
|---|---|
|[initialize](/api/js/ejpivottreemap#members:servicemethodsettings-initialize)|It fetches the data required to initialize the control.|
|[drillDown](/api/js/ejpivottreemap#members:servicemethodsettings-drilldown)|It allows drilling up/down action in pivot treemap.|








