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

### Generate JSON object from OLAP cube
The [`generateJSON`](/api/js/ejpivottreemap#methods:generatejson) method is used to render the control with the pivot engine obtained from the OLAP cube.

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

### Destroying object of pivot tree map component
The [`destroy`](/api/js/ejpivottreemap#methods:destroy) method is used to destroy the pivot chart widget associated events that are bound using "this._on" and bring the control to pre-init state.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.destroy();
</script>

{% endhighlight %}

### Getting JSON records from control object
The [`getJSONRecords`](/api/js/ejpivottreemap#methods:getjsonrecords) method is used to return the JSON records that is formed to render the control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.getJSONRecords();
</script>

{% endhighlight %}

### Setting JSON records to control object
The [`setJSONRecords`](/api/js/ejpivottreemap#methods:setjsonrecords) method is used to set the JSON records to render the pivot chart control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var pivotTreemap = $("#PivotTreeMap1").data("ejPivotTreeMap");
    pivotTreemap.setJSONRecords(pivotTreemap.getJSONRecords());
</script>

{% endhighlight %}

### Rendering the widget with predefined JSON records

The [`renderTreeMapFromJSON`](/api/js/ejpivottreemap#methods:rendertreemapfromjson) method is used to render the **PivotTreeMap** component with JSON records available at that instant.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#ejPivotTreeMap1").ejPivotTreeMap();
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.renderTreeMapFromJSON(treeMapObj.getJSONRecords());
</script>

{% endhighlight %}

### Getting the current OLAP report
You can get the current OLAP report along with axis information using the [`getOlapReport`](/api/js/ejpivottreemap#methods:getolapreport) method.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#ejPivotTreeMap1").ejPivotTreeMap();
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    var report = treeMapObj.getOlapReport();

</script>

{% endhighlight %}

### Setting the OLAP report
You can set the OLAP report along with axis information using the [`setOlapReport`](/api/js/ejpivottreemap#methods:setolapreport) method.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#ejPivotTreeMap1").ejPivotTreeMap();
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    var report = treeMapObj.setOlapReport(olapReportObj);
</script>

{% endhighlight %}

### Explicit asynchronous post

The [`doPostBack`](/api/js/ejpivottreemap#methods:dopostback) method is used to perform an asynchronous HTTP (AJAX) post operation.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.doPostBack("/PivotService/Initialize", { "key", "Hello World" });
</script>

{% endhighlight %}

### Rendering the widget using JSON records and report

The [`renderControlSuccess`](/api/js/ejpivottreemap#methods:rendercontrolsuccess) method is used to receive the JSON records and report from the service, which is utilized for rendering the widget.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap();
    var treeMapObj = $("#PivotTreeMap1").data("ejPivotTreeMap");
    treeMapObj.renderControlSuccess({ "OlapReport": this.getOlapReport(), "JsonRecords": this.getJSONRecords() });
</script>

{% endhighlight %}

### Invoking event before pivot engine population
The [`beforePivotEnginePopulate`](/api/js/ejpivottreemap#events:beforepivotenginepopulate) event is triggered before populating the pivot engine from the data source.

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
The [`beforeServiceInvoke`](/api/js/ejpivottreemap#events:beforeserviceinvoke) event is triggered before any AJAX request is passed from the pivot tree map to service methods.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       beforeServiceInvoke: function (args) {

    });
</script>

{% endhighlight %}

### Triggering event after performing drill operation
The [`drillSuccess`](/api/js/ejpivottreemap#events:drillsuccess) event is triggered when drill up/down operation is performed in the pivot tree map control, and it returns the outer HTML of the pivot tree map control.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       drillSuccess: function (args) {

    });
</script>

{% endhighlight %}

### Triggering event before the pivot tree map loaded
The [`load`](/api/js/ejpivottreemap#events:load) event is triggered when the pivot tree map is started to render.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       load: function (args) {

    });
</script>

{% endhighlight %}

### Triggering event on successful completion of AJAX request

The [`renderSuccess`](/api/js/ejpivottreemap#events:rendersuccess) event is triggered when the AJAX request returns successfully at the client-side.

{% highlight javascript %}

$("#PivotTreeMap1").ejPivotTreeMap({

            //render success event
            renderSuccess: function(args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event after the control rendered

The [`renderComplete`](/api/js/ejpivottreemap#events:rendercomplete) event is triggered after the pivot tree map is rendered completely.

{% highlight javascript %}

$("#PivotTreeMap1").ejPivotTreeMap({

            //render complete event
            renderComplete: function(args) {

            },

            //...
        });

{% endhighlight %}

### Triggering event on failure of AJAX request

The [`renderFailure`](/api/js/ejpivottreemap#events:renderfailure) event is triggered when any error occurred during the AJAX request.

{% highlight javascript %}

$("#PivotTreeMap1").ejPivotTreeMap({

            //render complete event
            renderFailure: function(args) {

            },

            //...
        });

{% endhighlight %}


## Members

### Responsive layout of pivot tree map component
You can enable/disable the responsiveness in the browser layout for pivot tree map control by setting the [`isResponsive`](/api/js/ejpivottreemap#members:isresponsive) property.

{% highlight html %}

<div id="PivotTreeMap1"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       isResponsive: true

    });
</script>

{% endhighlight %}

### Enabling XMLHttpRequest object for CORS
Allows you to enable the “withCredentials” property in the XMLHttpRequest object for CORS(Cross-Origin Resource Sharing) request. This feature can be enabled by using the [`enableXHRCredentials`](/api/js/ejpivottreemap#members:enableXHRCredentials) property.

{% highlight html %}

<div id="PivotTreeMap1" type="text/javascript"></div>

<script>
    $("#PivotTreeMap1").ejPivotTreeMap({

       enableXHRCredentials: true

    });
</script>

{% endhighlight %}

### Setting custom theme
You can render the pivot tree map with one of the available built-in themes by using the [`cssClass`](/api/js/ejpivottreemap#members:cssclass) property.

{% highlight html %}

    <script type="text/javascript">
        $(function() {
            $("#PivotTreeMap1").ejPivotTreeMap({
              cssClass: "gradient-lime"
            });

        });

    </script>

{% endhighlight %}


## Setting custom name to service methods
The [`serviceMethodSettings`](/api/js/ejpivottreemap#members:servicemethodsettings) allows you to set the custom name for methods in the WebAPI/WCF, communicated during the AJAX post. The following table will explain the service methods:

| Service methods | Description |
|---|---|
|[initialize](/api/js/ejpivottreemap#members:servicemethodsettings-initialize)|It fetches the required data to initialize the control.|
|[drillDown](/api/js/ejpivottreemap#members:servicemethodsettings-drilldown)|It allows drilling up/down action in the pivot tree map.|








