---
layout: post
title: How to
description: How to
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# How To

## Public Methods

### Refresh the PivotGrid with modified report
The [`refreshControl`](../api/ejpivotchart#methods:refreshControl) method is used to re-render the pivot chart component with specified datasource and properties initially.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.refreshControl();
</script>

{% endhighlight %}

### Generate JSON object from Olap Cube
The [`generateJSON`](../api/ejpivotchart#methods:generateJSON) method is used to render the pivot chart component with pivot engine from OLAP cube.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.generateJSON(baseObj, pivotEngineObj);
</script>

{% endhighlight %}

### Refresh the PivotChart with paging
The [`refreshPagedPivotChart`](../api/ejpivotchart#methods:refreshPagedPivotChart) method is used to render the pivot chart control with given axis and page number.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.refreshPagedPivotchart("series", 2);
</script>

{% endhighlight %}

### Explicit asynchronous invoke
The [`doAjaxPost`](../api/ejpivotchart#methods:doajaxpost) method is used to post an asynchronous HTTP (AJAX) request.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.doAjaxPost("POST", "/PivotService/Initialize", { "key", "Hello World" }, successEvent, null);
</script>

{% endhighlight %}

### Destroying the object of PivotChart
The [`destroy`](../api/ejpivotchart#methods:destroy) method is used to destroy the pivot chart widget associated events that are bound using "this._on" and brings the control to pre-init state.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.destroy();
</script>

{% endhighlight %}

### Getting JSON Records from control object
The [`getJSONRecords`](../api/ejpivotchart#methods:getjsonrecords) method is used to return the JSON records that are formed to render the pivot chart control.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.getJSONRecords();
</script>

{% endhighlight %}

### Setting JSON Records to control object
The [`setJSONRecords`](../api/ejpivotchart#methods:setjsonrecords) method is used to set the JSON records to render the pivot chart control.

{% highlight html %}

<div id="PivotChart1"></div>

<script>
    $("#PivotChart1").ejPivotChart();
    var pivotChartObj = $("#PivotChart1").data("ejPivotChart");
    pivotChartObj.setJSONRecords(pivotChartObj.getJSONRecords());
</script>

{% endhighlight %}


## Events

### Invoking event in client-side after service invoke
The [`afterServiceInvoke`](../api/ejpivotchart#events:afterserviceinvoke) event is triggered when it is reached the client-side after any AJAX request.

{% highlight javascript %}

$("#PivotChart1").ejPivotChart({

            // after service invoke event
            afterServiceInvoke: function (args) {

            },

            //...
        });

{% endhighlight %}

### Invoking event in client-side before service invoke
The [`beforeServiceInvoke`](../api/ejpivotchart#events:beforeserviceinvoke) event is triggered before any AJAX request is passed from the pivot chart to service methods.

{% highlight javascript %}

$("#PivotChart1").ejPivotChart({

            // before service invoke event
            beforeServiceInvoke: function (args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event after performing drill operation
The [`drillSuccess`](../api/ejpivotchart#events:drillsuccess) event is triggered when performing drill up/down operation in the pivot chart control.

{% highlight javascript %}

$("#PivotChart1").ejPivotChart({

            // drill success event
            drillSuccess: function (args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event before exporting
The [`beforeExport`](../api/ejpivotchart#events:beforeexport) event is triggered before performing export operation in the pivot chart.
{% highlight javascript %}

$("#PivotChart1").ejPivotChart({

            // before export event
            beforeExport: function (args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event before the PivotChart loaded
The [`load`](../api/ejpivotchart#events:load) event is triggered when the pivot chart is started to render.
{% highlight javascript %}

$("#PivotChart1").ejPivotChart({

            // load event
            load: function (args) {

            },

            //...
        });

{% endhighlight %}


## Members

### Enabling Context Menu in PivotChart
To improve user action, the Context Menu option in pivot chart allows you to enable/disable the features with UI operations. This feature can be enabled by the [`enableContextMenu`](/api/js/ejpivotchart#members:enablecontextmenu) property.

{% highlight html %}

    <script type="text/javascript">
        $(function() {
            $("#PivotChart1").ejPivotChart({

              enableContextMenu: true

            });

        });


    </script>

{% endhighlight %}

![](How-To_images/contextMenu.png)

The following are the available features in Context Menu.

* [`Tooltip`](/api/js/ejchart#members:commonseriesoptions-tooltip-visible): It allows you enable/disable the tooltip.
* [`Legend`](/api/js/ejpivotchart#members:legend): You can show/hide legend in pivot chart component.
* [`Zooming`](/api/js/ejchart#members:zooming-enable): You can zoom the chart by using rubber band selection.

![](How-To_images/zooming.png)

* [`Chart Types`](/api/js/ejpivotchart#members:commonseriesoptions-type): You can choose different 2D charts by UI operations.

![](How-To_images/chartTypes.png)

* [`3D Charts`](/api/js/ejpivotchart#members:enable3d): You can choose different 3D chart types. The **"Disable 3D Charts"** option available to disable 3D chart and it is rendered as respective 2D chart.

![](How-To_images/3DCharts.png)

* `Exporting`: You can export the chart in different formats given in the following image. You have to mention the export settings through [`beforeExport`](../api/ejpivotchart#events:beforeexport) event.

![](How-To_images/exporting.png)

* `Interactions`: Different types of interactions available in the context menu to view the datum in the chart.

For more on this topic, [click here](https://help.syncfusion.com/js/pivotchart/user-interactions)

![](How-To_images/interactions.png)

* [`Smart Labels`](/api/js/ejchart#members:primaryxaxis-labelintersectaction): You can customize the labels in a different view by given options mentioned in the following image.

![](How-To_images/smartLabels.png)


## Setting Custom Name to Service Methods
The [`serviceMethodSettings`](/api/js/ejpivotchart#members:servicemethodsettings) allows you to set the custom name for the methods in WebAPI/WCF, communicated during AJAX post. The following table will explain the service methods.

| Service Methods | Description |
|---|---|
|[initialize](/api/js/ejpivotchart#members:servicemethodsettings-initialize)|It fetches the data required to initialize the control.|
|[drillDown](/api/js/ejpivotchart#members:servicemethodsettings-drilldown)|It allows drilling up/down action in pivot chart.|
|[paging](/api/js/ejpivotchart#members:servicemethodsettings-paging)|It fetches the data on navigating between pages in pivot chart data.|







