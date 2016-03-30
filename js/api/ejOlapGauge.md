---
layout: post
title: Properties,methods and events of Essential JS ejOlapGauge widget
documentation: API
platform: js
keywords: ejOlapGauge, API, Essential JS OlapGauge
metaname: 
metacontent: 
---

# OlapGauge

The OlapGauge control is ideal for highlighting business critical Key Performance Indicator (KPI) information in executive dashboards and report cards. The OlapGauge let you present values against goals in a very intuitive manner.

#### Syntax

{% highlight javascript %}

$(element).ejOlapGauge()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
//Create OlapGauge
$("#OlapGauge1").ejOlapGauge(...);       
</script>

{% endhighlight %}

#### Requires

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:jquery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.waitingpopup.js
* module:ej.circulargauge.js
* module:ej.olapgauge.js


## Members

### columnsCount `number`
{:#members:columnscount}

Sets the number of column count to arrange the OlapGauge's.

#### Default Value: 0

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ columnsCount: 1 }); 

{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Specify the CSS class to OlapGauge to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ cssClass : "gradient-lime" });

{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ customObject: {"key":"Hello World"} }); 

{% endhighlight %}

### enableTooltip `boolean`
{:#members:enabletooltip}

Enables/disables tooltip visibility in OlapGauge.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ enableTooltip: true }); 

{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

Allows the user to enable OlapGauge’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ isResponsive: true });

{% endhighlight %}

### labelFormatSettings `enum`
{:#members:labelformatsettings}

<ts name = "ej.olap.OlapGauge.NumberFormat"/>

Allows the user to change the format of the label values in OlapGauge.

#### Default Value: ej.olap.OlapGauge.NumberFormat.Default

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description">To set default format for label values.</td>
        </tr>
        <tr>
            <td class="name">Currency</td>
            <td class="description">To set currency format for label values.</td>
        </tr>
        <tr>
            <td class="name">Percentage</td>
            <td class="description">To set percentage format for label values.</td>
        </tr>
        <tr>
            <td class="name">Fraction</td>
            <td class="description">To set fraction format for label values.</td>
        </tr>
        <tr>
            <td class="name">Scientific</td>
            <td class="description">To set scientific format for label values.</td>
        </tr>
        <tr>
            <td class="name">Text</td>
            <td class="description">To set text format for label values.</td>
        </tr>
        <tr>
            <td class="name">Notation</td>
            <td class="description">To set notation format for label values.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ numberFormat: ej.olap.OlapGauge.NumberFormat.Default });

{% endhighlight %}


### labelFormatSettings.numberFormat `enum`
{:#members:labelformatsettings-numberformat}

<ts name = "ej.olap.OlapGauge.NumberFormat"/>

Allows the user to change the number format of the label values in OlapGauge.

#### Default Value: ej.olap.OlapGauge.NumberFormat.Default

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description">To set default format for label values.</td>
        </tr>
        <tr>
            <td class="name">Currency</td>
            <td class="description">To set currency format for label values.</td>
        </tr>
        <tr>
            <td class="name">Percentage</td>
            <td class="description">To set percentage format for label values.</td>
        </tr>
        <tr>
            <td class="name">Fraction</td>
            <td class="description">To set fraction format for label values.</td>
        </tr>
        <tr>
            <td class="name">Scientific</td>
            <td class="description">To set scientific format for label values.</td>
        </tr>
        <tr>
            <td class="name">Text</td>
            <td class="description">To set text format for label values.</td>
        </tr>
        <tr>
            <td class="name">Notation</td>
            <td class="description">To set notation format for label values.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({labelFormatSettings: {numberFormat: ej.olap.OlapGauge.NumberFormat.Default} });

{% endhighlight %}


### labelFormatSettings.decimalPlaces `number`
{:#members:labelformatsettings-decimalplaces}

Allows you to change the position of a digit on the right-hand side of the decimal point for label value.

#### Default Value: 5

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({labelFormatSettings: {decimalPlaces: 3} });

{% endhighlight %}


### labelFormatSettings.prefixText  `string`
{:#members:labelformatsettings-prefixtext}

Allows you to add a text at the beginning of the label.

#### Default Value: " "

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({labelFormatSettings: {prefixText: “prefixTextValue”} });

{% endhighlight %}


### labelFormatSettings.suffixText `string`
{:#members:labelformatsettings-suffixtext }

Allows you to add text at the end of the label.

#### Default Value: " "

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({labelFormatSettings: {suffixText: “suffixTextValue”} });

{% endhighlight %}


### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ locale: "fr-FR" }); 

{% endhighlight %}

### rowsCount `number`
{:#members:rowscount}

Sets the number of row count to arrange the OlapGauge's.

#### Default Value: 0

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ rowsCount: 1 });

{% endhighlight %}

### scales `object`
{:#members:scales}

Sets the scale values such as pointers, indicators, etc... for OlapGauge.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ scales: {showRanges: true, showIndicators: true} });

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set the custom name for the methods at service-end, communicated during AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ serviceMethodSettings: {initialize: "MyMethod"} });

{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing OlapGauge.

#### Default Value: "InitializeGauge"

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ serviceMethodSettings: {initialize: "InitializeGaugeMyMethod"} });
 
{% endhighlight %}

### showHeaderLabel `boolean`
{:#members:showheaderlabel}

Enables/disables the header labels in OlapGauge.

#### Default Value: true

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ showHeaderLabel: false }); 

{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({ url: "/OlapGaugeService.svc" }); 

{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
$('#OlapGauge1').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge1").data("ejOlapGauge");
gaugeObj.doAjaxPost("POST", "/OlapGaugeService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
</script>

{% endhighlight %}

### refresh()
{:#methods:refresh}

This function is used to refresh the OlapGauge at client-side itself.

**Example:**

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
$('#OlapGauge1').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   pointerType: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge1").data("ejOlapGauge");
gaugeObj.refresh();
</script>

{% endhighlight %}


### removeImg()
{:#methods:removeimg}

This function removes the KPI related images from OlapGauge.

**Example:**

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
$('#OlapGauge1').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge1").data("ejOlapGauge");
gaugeObj.removeImg();
</script>

{% endhighlight %}


### renderControlFromJSON()
{:#methods:rendercontrolfromjson}

This function receives the JSON formatted datasource to render the OlapGauge control.

**Example:**

{% highlight html %}
 
<div id="OlapGauge1"></div> 
 
<script>
$('#OlapGauge1').ejOlapGauge({
      url: "OlapGaugeService.svc",
                enableTooltip: true,
                scales: [{
                pointers: [{
                           showBackNeedle: true,
                           backNeedleLength: 20,
                           length: 120,
                           width: 7
                       },
               {
                   type: "marker",
                   markerType: "diamond",
                   distanceFromScale: 5,
                   placement: "center",
                   backgroundColor: "#29A4D9",
                   length: 25,
                   width: 15
               }]
        }]
  });
var gaugeObj = $("#OlapGauge1").data("ejOlapGauge");
gaugeObj.renderControlFromJSON(this.getJSONRecords());
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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">return the current action of OlapGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapGauge control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   afterServiceInvoke: function (args) {}
});      

{% endhighlight %}


### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from OlapGauge to service methods.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">action</td>
<td class="type">string</td>
<td class="description last">return the current action of OlapGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with OlapGauge control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of OlapGauge control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   beforeServiceInvoke: function (args) {}
});      

{% endhighlight %}


### load
{:#events:load}

Triggers when OlapGauge started loading at client-side.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   load: function (args) {}
});      

{% endhighlight %}

### renderComplete
{:#events:rendercomplete}

Triggers when OlapGauge widget completes all operations at client-side after any AJAX request.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of OlapGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   renderComplete: function (args) {}
});      

{% endhighlight %}


### renderFailure
{:#events:renderfailure}

Triggers when any error occurred during AJAX request.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of OlapGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">message</td>
<td class="type">Object</td>
<td class="description last">returns the error message with error code.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
<tr>
<td class="name">responseJSON</td>
<td class="type">object</td>
<td class="description last">returns the JSON formatted response while error occurs.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   renderFailure: function (args) {}
}); 

{% endhighlight %}


### renderSuccess
{:#events:rendersuccess}

Triggers when OlapGauge successfully reaches client-side after any AJAX request.

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
<td class="name">argument</td>
<td class="type">Object</td>
<td class="description last">Event parameters from OlapGauge.
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
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of OlapGauge control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.OlapGauge.Model"/>object</td>
<td class="description last">returns the OlapGauge model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

**Example:**

{% highlight html %}
 
$("#OlapGauge1").ejOlapGauge({
   renderSuccess: function (args) {}
});      

{% endhighlight %}


## Enumeration

### NumberFormat  `enum`
{:#enum:numberformat}

<ts name = "ej.olap.OlapGauge.NumberFormat"/>

Allows the user to change the format of the label values in OlapGauge.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Default</td>
            <td class="description">To set default format for label values.</td>
        </tr>
        <tr>
            <td class="name">Currency</td>
            <td class="description">To set currency format for label values.</td>
        </tr>
        <tr>
            <td class="name">Percentage</td>
            <td class="description">To set percentage format for label values.</td>
        </tr>
        <tr>
            <td class="name">Fraction</td>
            <td class="description">To set fraction format for label values.</td>
        </tr>
        <tr>
            <td class="name">Scientific</td>
            <td class="description">To set scientific format for label values.</td>
        </tr>
        <tr>
            <td class="name">Text</td>
            <td class="description">To set text format for label values.</td>
        </tr>
        <tr>
            <td class="name">Notation</td>
            <td class="description">To set notation format for label values.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#OlapGauge1").ejOlapGauge({labelFormatSettings: {numberFormat: ej.olap.OlapGauge.NumberFormat.Default} });

{% endhighlight %}

