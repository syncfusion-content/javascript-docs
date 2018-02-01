---
layout: post
title: How To
description: How To
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# How To

## Public Methods

### Refresh the PivotGauge at client mode
The [`refresh`](../api/ejpivotgauge#methods:refresh) method is used to refresh the pivot gauge at client-side itself.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.refresh();
</script>

{% endhighlight %}

### Removing KPI images from PivotGauge
The [`removeImg`](../api/ejpivotgauge#methods:removeimg) method is used to remove the KPI related images from PivotGauge on binding OLAP datasource.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.removeImg();
</script>

{% endhighlight %}

### Getting JSON data to render PivotGauge with OLAP datasource
The [`getJSONData`](../api/ejpivotgauge#methods:getJSONData) method is used to return the JSON records required to render the pivot gauge on performing any action with OLAP data source.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var args = { action : "initialize", activeObject : gaugeObj };
    var jsonData = gaugeObj.getJSONData(args, dataSource);
</script>

{% endhighlight %}

### Getting JSON Records from control object
The [`getJSONRecords`](../api/ejpivotgauge#methods:getJSONRecords) method is used to return the JSON records formed to render the control.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var jsonRecords = gaugeObj.getJSONRecords();
</script>

{% endhighlight %}

### Setting JSON Records to control object
The [`setJSONRecords`](../api/ejpivotgauge#methods:setJSONRecords) method is used to set the JSON records to render the control.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.setJSONRecords(gaugeObj.getJSONRecords());
</script>

{% endhighlight %}

### Destroying the object of PivotGauge
The [`destroy`](../api/ejpivotgauge#methods:destroy) method is used to destroy the pivot gauge widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.destroy();
</script>

{% endhighlight %}

### Explicit asynchronous invoke
The [`doAjaxPost`](../api/ejpivotgauge#methods:doajaxpost) method is used to perform an asynchronous HTTP (AJAX) request.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, "renderControlSuccess", null);
</script>

{% endhighlight %}


## Events

### Triggering event before the PivotGauge loaded
The [`load`](../api/ejpivotgauge#events:load) event is triggered when pivot gauge started loading at client-side.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        // load event
        load: function (args) {

        }

    });
</script>

{% endhighlight %}

### Invoking event before Pivot Engine population
The [`beforePivotEnginePopulate`](../api/ejpivotgauge#events:beforepivotenginepopulate) event is triggered before populating the pivot engine on operating in client mode.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        // before pivot engine populate event
        beforePivotEnginePopulate: function (args) {}

    });
</script>

{% endhighlight %}

### Invoking event in client-side after service invoke
The [`afterServiceInvoke`](../api/ejpivotgauge#events:afterserviceinvoke) event is triggered when it is reached client-side after any AJAX request.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        // after service invoke event
        afterServiceInvoke: function (args) {}

    });
</script>

{% endhighlight %}

### Invoking event in client-side before service invoke
The [`beforeServiceInvoke`](../api/ejpivotgauge#events:beforeserviceinvoke) event is triggered before any AJAX request is passed from pivot gauge to service methods.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        // before service invoke event
        beforeServiceInvoke: function (args) {}

    });
</script>

{% endhighlight %}


## Members

### Showing Header label in PivotGauge
You can show/hide header label in pivot gauge by the [`showHeaderLabel`](../api/ejpivotgauge#members:showheaderlabel) property.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        showHeaderLabel: true

    });
</script>

{% endhighlight %}


## Setting Custom Name to Service Methods
The [`serviceMethodSettings`](/api/js/ejpivotgauge#members:servicemethodsettings) allows you to set the custom name for the methods in WebAPI/WCF, communicated during AJAX post. The following table will explain the service methods.

| Service Methods | Description |
|---|---|
|[initialize](/api/js/ejpivotgauge#members:servicemethodsettings-initialize)|It fetches the data required to initialize the control.|


