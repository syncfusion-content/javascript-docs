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
The [`refresh`](/api/js/ejpivotgauge#methods:refresh) method is used to refresh the pivot gauge at client-side itself.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.refresh();
</script>

{% endhighlight %}

### Removing KPI images from pivot gauge
The [`removeImg`](/api/js/ejpivotgauge#methods:removeimg) method is used to remove the KPI related images from the pivot gauge when binding the OLAP data source.

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
The [`doAjaxPost`](/api/js/ejpivotgauge#methods:doajaxpost) method is used to perform an asynchronous HTTP (AJAX) request.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var gaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    gaugeObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, "renderControlSuccess", null);
</script>

{% endhighlight %}

### Rendering the widget with predefined JSON records

The [`renderControlFromJSON`](/api/js/ejpivotgauge#methods:rendercontrolfromjson) method is used to render the **PivotGauge** component with predefined JSON records available at that instant.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var pivotGaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    pivotGaugeObj.renderControlFromJSON({ this.getJSONRecords() });
</script>

{% endhighlight %}

### Getting the current OLAP report
You can get the current OLAP report along with axis information using the [`getOlapReport`](/api/js/ejpivotgauge#methods:getolapreport) method.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var pivotGaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var report = pivotGaugeObj.getOlapReport();
</script>

{% endhighlight %}

### Setting the OLAP report
You can set the OLAP report along with axis information using the [`setOlapReport`](/api/js/ejpivotgauge#methods:setolapreport) method.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGrid();
    var pivotGaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    var report = pivotGaugeObj.setOlapReport(olapReportObj);
</script>

{% endhighlight %}

### Destroying the object of PivotGauge

The [`destroy`](/api/js/ejpivotgauge#methods:destroy) method is used to destroy the **PivotGauge** widget associated events that are bound using “this._on” and brings the control to pre-init state.

{% highlight html %}

<div id="PivotGauge1"></div>

<script>
    $("#PivotGauge1").ejPivotGauge();
    var pivotGaugeObj = $("#PivotGauge1").data("ejPivotGauge");
    pivotGaugeObj.destroy();
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

### Triggering event on successful completion of AJAX request

The [`renderSuccess`](/api/js/ejpivotgauge#events:rendersuccess) event is triggered when AJAX request returns successfully at the client-side.

{% highlight javascript %}

$("#PivotGauge1").ejPivotGauge({

            //render success event
            renderSuccess: function(args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event after the control rendered

The [`renderComplete`](/api/js/ejpivotgauge#events:rendercomplete) event is triggered after the pivot client is rendered completely.

{% highlight javascript %}

    $("#PivotGauge1").ejPivotGauge({

            //render complete event
            renderComplete: function(args) {

            },

            //...
    });

{% endhighlight %}

### Triggering event on failure of AJAX request

The [`renderFailure`](/api/js/ejpivotgauge#events:renderfailure) event is triggered when any error occurred during the AJAX request.

{% highlight javascript %}

   $("#PivotGauge1").ejPivotGauge({

            //render complete event
            renderFailure: function(args) {

            },

            //...
        });

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

### Enabling XMLHttpRequest object for CORS
Allows you to enable the “withCredentials” property in the XMLHttpRequest object for CORS(Cross-Origin Resource Sharing) request. This feature can be enabled by using the [`enableXHRCredentials`](/api/js/ejpivotgauge#members:enableXHRCredentials) property.

{% highlight html %}

<div id="PivotGauge1"></div>

<script type="text/javascript">
    $("#PivotGauge1").ejPivotGauge({

        enableXHRCredentials: true

    });
</script>

{% endhighlight %}

### Setting custom theme
You can render the pivot gauge with one of the available built-in themes by using the [`cssClass`](/api/js/ejpivotgauge#members:cssclass) property.

{% highlight html %}

    <script type="text/javascript">
        $(function() {
            $("#PivotGauge1").ejPivotGauge({
              cssClass: "gradient-lime"
            });

        });

    </script>

{% endhighlight %}


## Setting custom name to service methods
The [`serviceMethodSettings`](/api/js/ejpivotgauge#members:servicemethodsettings) allows you to set the custom name for methods in the WebAPI/WCF, communicated during the AJAX post. The following table will explain the service methods:

| Service methods | Description |
|---|---|
|[initialize](/api/js/ejpivotgauge#members:servicemethodsettings-initialize)|It fetches the required data to initialize the control.|


