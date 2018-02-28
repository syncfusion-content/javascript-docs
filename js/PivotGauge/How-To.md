---
layout: post
title: How To
description: How To
platform: js
control: PivotGauge
documentation: ug
api: /api/js/ejpivotgauge
---

# How to

## Public methods

### Refresh the pivot gauge at client mode
The [`refresh`](../api/ejpivotgauge#methods:refresh) method is used to refresh the pivot gauge at client-side itself.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.refresh();
</script>

{% endhighlight %}

### Removing KPI images from pivot gauge
The [`removeImg`](../api/ejpivotgauge#methods:removeimg) method is used to remove the KPI related images from the pivot gauge when binding the OLAP data source.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.removeImg();
</script>

{% endhighlight %}

### Getting JSON data to render with OLAP data source
The [`getJSONData`](/api/js/ejpivotgauge#methods:getjsondata) method is used to return the JSON records required to render the pivot gauge when performing any action with the OLAP data source.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var args = { action : "initialize", activeObject : gaugeObj };
    var jsonData = gaugeObj.getJSONData(args, dataSource);
</script>

{% endhighlight %}

### Getting JSON records from control object
The [`getJSONRecords`](/api/js/ejpivotgauge#methods:getjsonrecords) method is used to return the JSON records that is formed to render the control.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var jsonRecords = gaugeObj.getJSONRecords();
</script>

{% endhighlight %}

### Setting JSON records to control object
The [`setJSONRecords`](/api/js/ejpivotgauge#methods:setjsonrecords) method is used to set the JSON records to render the control.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.setJSONRecords(gaugeObj.getJSONRecords());
</script>

{% endhighlight %}

### Destroying the object of pivot gauge
The [`destroy`](../api/ejpivotgauge#methods:destroy) method is used to destroy the pivot gauge widget associated events bound using "this._on" option and bring the control to pre-init state.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.destroy();
</script>

{% endhighlight %}

### Explicit asynchronous invoke
The [`doAjaxPost`](/api/js/ejpivottreemap#methods:doajaxpost) method is used to perform an asynchronous HTTP (AJAX) request.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, "renderControlSuccess", null);
</script>

{% endhighlight %}


## Events

### Triggering event before the pivot gauge loaded
The [`load`](/api/js/ejpivotgauge#events:load) event is triggered when the pivot gauge is started loading at client-side.

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

### Invoking event before pivot engine population
The [`beforePivotEnginePopulate`](/api/js/ejpivotgauge#events:beforepivotenginepopulate) event is triggered before populating the pivot engine when operating in client mode.

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
The [`afterServiceInvoke`](/api/js/ejpivotgauge#events:afterserviceinvoke) event is triggered when it is reached the client-side after any AJAX request.

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
The [`beforeServiceInvoke`](/api/js/ejpivotgauge#events:beforeserviceinvoke) event is triggered before any AJAX request is passed from the pivot gauge to service methods.

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

### Showing header label in pivot gauge
You can show/hide the header label in the pivot gauge by the [`showHeaderLabel`](/api/js/ejpivotgauge#members:showheaderlabel) property.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge({

        showHeaderLabel: true

    });
</script>

{% endhighlight %}


## Setting custom name to service methods
The [`serviceMethodSettings`](/api/js/ejpivotgauge#members:servicemethodsettings) allows you to set the custom name for methods in the WebAPI/WCF, communicated during the AJAX post. The following table will explain the service methods:

| Service methods | Description |
|---|---|
|[initialize](/api/js/ejpivotgauge#members:servicemethodsettings-initialize)|It fetches the required data to initialize the control.|


