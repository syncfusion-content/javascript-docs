---
layout: post
title: Properties, Methods and Events of ejPivotClient Widget
documentation: API
platform: js
keywords: ejPivotClient, API, Essential JS PivotClient
metaname: 
metacontent: 
---

# PivotClient

PivotClient is an ad hoc analysis tool that can be easily bound to any OLAP datasource to provide a visual presentation of the information retrieved from multidimensional data.

#### Syntax

{% highlight javascript %}

$(element).ejPivotClient()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="PivotClient1"></div> 
 
<script>
//Create PivotClient
$("#PivotClient1").ejPivotClient(...);     
</script>

{% endhighlight %}

#### Requires

* module:jQuery-1.10.2.min.js
* module:jQuery.easing.1.3.min.js
* module:jQuery.globalize.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.button.js
* module:ej.togglebutton.js
* module:ej.checkbox.js
* module:ej.radiobutton.js
* module:ej.dropdownlist.js
* module:ej.dialog.js
* module:ej.draggable.js
* module:ej.toolbar.js
* module:ej.scroller.js
* module:ej.maskedit.js
* module:ej.waitingpopup.js
* module:ej.treeview.js
* module:ej.tab.js
* module:ej.chart.js
* module:ej.pivotchart.js
* module:ej.pivotgrid.js
* module:ej.pivotclient.js

## Members

### chartType `enum`
{:#members:charttype}

<ts name = "ej.PivotChart.ChartTypes"/>

Allows the user to set the specific chart type for PivotChart.

#### Default Value: ej.PivotChart.ChartTypes.Column

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Line</td>
            <td class="description">To render a Line type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Spline</td>
            <td class="description">To render a Spline type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Column</td>
            <td class="description">To render a Column type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Area</td>
            <td class="description">To render a Area type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">SplineArea</td>
            <td class="description">To render a SplineArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepLine</td>
            <td class="description">To render a StepLine type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StepArea</td>
            <td class="description">To render a StepArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pie</td>
            <td class="description">To render a Pie type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bar</td>
            <td class="description">To render a Bar type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingArea</td>
            <td class="description">To render a StackingArea type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingColumn</td>
            <td class="description">To render a StackingColumn type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">StackingBar</td>
            <td class="description">To render a StackingBar type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Pyramid</td>
            <td class="description">To render a Pyramid type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Funnel</td>
            <td class="description">To render a Funnel type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Doughnut</td>
            <td class="description">To render a Doughnut type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Scatter</td>
            <td class="description">To render a Scatter type for PivotChart.</td>
        </tr>
        <tr>
            <td class="name">Bubble</td>
            <td class="description">To render a Bubble type for PivotChart.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ chartType: ej.PivotChart.ChartTypes.Spline });

{% endhighlight %}

### clientExportMode `string`
{:#members:clientexportmode}

Sets the mode to export the OLAP visualization components such as PivotChart and PivotGrid in PivotClient. Based on the option, either Chart or Grid or both gets exported. 

#### Default Value: ej.PivotClient.ClientExportMode.ChartAndGrid 

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid });

{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Specifies the CSS class to PivotClient to achieve custom theme.

#### Default Value: “”

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ cssClass: "Olive" });

{% endhighlight %}

### customObject `object`
{:#members:customobject}

Object utilized to pass additional information between client-end and service-end.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ customObject: {"MyObject": "Hi Syncfusion!!"} });

{% endhighlight %}

### displaySettings `object`
{:#members:displaysettings}

Allows the user to customize the widgets layout and appearance.

#### Default Value: {}

**Example:**

{% highlight html %}
 
 $("#PivotClient1").ejPivotClient({ displaySettings: { mode: ej.PivotClient.DisplayMode.Both } });
 
{% endhighlight %}

### displaySettings.controlPlacement `enum`
{:#members:displaysettings-controlplacement}

<ts name = "ej.PivotClient.ControlPlacement"/>

Let’s the user to customize the display of PivotChart and PivotGrid widgets, either in tab view or in tile view.

#### Default Value: ej.PivotClient.ControlPlacement.Tab

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Tab</td>
            <td class="description">To display PivotChart and PivotGrid widgets in tab view.</td>
        </tr>
        <tr>
            <td class="name">Tile</td>
            <td class="description">To display PivotChart and PivotGrid widgets within the same view, one below the other.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: {controlPlacement: ej.PivotClient.ControlPlacement.Tab} });

{% endhighlight %}

### displaySettings.defaultView `enum`
{:#members:displaysettings-defaultview}

<ts name = "ej.PivotClient.DefaultView"/>

Let’s the user to set either Chart or Grid as the start-up widget.

#### Default Value: ej.PivotClient.DefaultView.Grid

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Chart</td>
            <td class="description">To set PivotChart as a default control in view when the PivotClient widget is loaded for the first time.</td>
        </tr>
        <tr>
            <td class="name">Grid</td>
            <td class="description">To set PivotGrid as a default control in view when the PivotClient widget is loaded for the first time.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: {defaultView: ej.PivotClient.DefaultView.Grid} });

{% endhighlight %}

### displaySettings.enableFullScreen `boolean`
{:#members:displaysettings-enablefullscreen}

Enables/disables the full screen view of PivotChart and PivotGrid in PivotClient.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: { enableFullScreen: true } });

{% endhighlight %}

### displaySettings.enableTogglePanel `boolean`
{:#members:displaysettings-enabletogglepanel}

Enhances the space for PivotGrid and PivotChart, by hiding Cube Browser and Axis Element Builder.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: { enableTogglePanel: true } });

{% endhighlight %}

### displaySettings.isResponsive `boolean`
{:#members:displaysettings-isresponsive}

Allows the user to enable PivotClient’s responsiveness in the browser layout.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: { isResponsive: true } });

{% endhighlight %}

### displaySettings.mode `enum`
{:#members:displaysettings-mode}

<ts name = "ej.PivotClient.DisplayMode"/>

Sets the display mode (Only Chart/Only Grid/Both) in PivotClient.

#### Default Value: ej.PivotClient.DisplayMode.ChartAndGrid

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">To display only PivotChart widget.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">To display only PivotGrid widget.</td>
        </tr>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">To display both PivotChart and PivotGrid widgets.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ displaySettings: { mode: ej.PivotClient.DisplayMode.ChartOnly } });

{% endhighlight %}

### enableDeferUpdate `boolean`
{:#members:enabledeferupdate}

Allows the user to refresh the control on-demand and not during every UI operation. 

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ enableDeferUpdate: true });

{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Allows the user to view the layout of PivotClient from right to left.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ enableRTL: true });

{% endhighlight %}

### enableMeasureGroups `boolean`
{:#members:enablemeasuregroups}

Enables/disables the visibility of measure group selector drop-down in Cube Browser.

#### Default Value: false

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ enableMeasureGroups : true });

{% endhighlight %}

### gridLayout `enum`
{:#members:gridlayout}

<ts ref = "ej.PivotGrid.Layout"/>

Sets the summary layout for PivotGrid. Following are the ways in which summary can be positioned: normal summary (bottom), top summary, no summary and excel-like summary.

#### Default Value: ej.PivotGrid.Layout.Normal

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Normal</td>
            <td class="description">To set normal summary layout in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">NormalTopSummary</td>
            <td class="description">To set layout with summaries at the top in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">NoSummaries</td>
            <td class="description">To set layout without summaries in PivotGrid.</td>
        </tr>
        <tr>
            <td class="name">ExcelLikeLayout</td>
            <td class="description">To set excel-like layout in PivotGrid.</td>
        </tr>
    </tbody>
</table>

**Example:** 

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ gridLayout: ej.PivotGrid.Layout.NoSummaries });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:** 

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ locale: "en-US" });

{% endhighlight %}

### serviceMethodSettings `object`
{:#members:servicemethodsettings}

Allows the user to set custom name for the methods at service-end, communicated during AJAX post.

#### Default Value: {}

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {initialize: "MyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.cubeChanged `string`
{:#members:servicemethodsettings-cubechanged}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating the entire report and widget, while changing the Cube.

#### Default Value: "CubeChanged"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {cubeChanged: "CubeChangedMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.exportPivotClient `string`
{:#members:servicemethodsettings-exportpivotclient}

Allows the user to set the custom name for the service method that’s responsible for exporting.

#### Default Value: "Export"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: { exportPivotClient: "Export"} });
 
{% endhighlight %}

### serviceMethodSettings.fetchMemberTreeNodes `string`
{:#members:servicemethodsettings-fetchmembertreenodes}

Allows the user to set the custom name for the service method that&rsquo;s responsible to get the members, for the tree-view inside member-editor dialog.

#### Default Value: "FetchMemberTreeNodes"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {fetchMemberTreeNodes: "FetchMemberTreeNodesMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.fetchReportList `string`
{:#members:servicemethodsettings-fetchreportlist}

Allows the user to set the custom name for the service method that&rsquo;s responsible for fetching the report names from the database.

#### Default Value: "FetchReportListFromDB"

**Example:**

{% highlight html %}
                     
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {fetchReportList: "FetchReportListFromDBMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.filterElement `string`
{:#members:servicemethodsettings-filterelement}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while filtering members.

#### Default Value: "FilterElement"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {filterElement: "filterElementMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.initialize `string`
{:#members:servicemethodsettings-initialize}

Allows the user to set the custom name for the service method that&rsquo;s responsible for initializing PivotClient.

#### Default Value: "InitializeClient"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {initialize: "InitializeClientMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.loadReport `string`
{:#members:servicemethodsettings-loadreport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for loading the report collection from the database.

#### Default Value: "LoadReportFromDB"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {loadReport: "LoadReportFromDBMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.mdxQuery `string`
{:#members:servicemethodsettings-mdxquery}

Allows the user to set the custom name for the service method that’s responsible for retrieving the MDX query for the current report.

#### Default Value: "GetMDXQuery"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {mdxQuery: "GetMDXQuery"} });

{% endhighlight %}

### serviceMethodSettings.measureGroupChanged `string`
{:#members:servicemethodsettings-measuregroupchanged}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating the tree-view inside Cube Browser, while changing the measure group.

#### Default Value: "MeasureGroupChanged"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {measureGroupChanged: "MeasureGroupChangedMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.memberExpand `string`
{:#members:servicemethodsettings-memberexpand}

Allows the user to set the custom name for the service method that&rsquo;s responsible to get the child members, on tree-view node expansion.

#### Default Value: "MemberExpanded"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {memberExpand: "MemberExpandedMyMethod"} });

{% endhighlight %}

### serviceMethodSettings.nodeDropped `string`
{:#members:servicemethodsettings-nodedropped}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while dropping a node/SplitButton inside Axis Element Builder.

#### Default Value: "NodeDropped"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {nodeDropped: "NodeDroppedMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.removeSplitButton `string`
{:#members:servicemethodsettings-removesplitbutton}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report while removing SplitButton from Axis Element Builder.

#### Default Value: "RemoveSplitButton"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {removeSplitButton: "RemoveSplitButtonMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.saveReport `string`
{:#members:servicemethodsettings-savereport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for saving the report collection to database.

#### Default Value: "SaveReportToDB"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {saveReport: "SaveReportToDBMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.toggleAxis `string`
{:#members:servicemethodsettings-toggleaxis}

Allows the user to set the custom name for the service method that’s responsible for toggling the elements in row and column axes.

#### Default Value: "ToggleAxis"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {toggleAxis: "ToggleAxis"} });

{% endhighlight %}

### serviceMethodSettings.toolbarServices `string`
{:#members:servicemethodsettings-toolbarservices}

Allows the user to set the custom name for the service method that&rsquo;s responsible for any toolbar operation.

#### Default Value: "ToolbarOperations"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ serviceMethodSettings: {toolbarServices: "ToolbarOperationsMyMethod"} });
 
{% endhighlight %}

### serviceMethodSettings.updateReport `string`
{:#members:servicemethodsettings-updatereport}

Allows the user to set the custom name for the service method that&rsquo;s responsible for updating report collection.

#### Default Value: "UpdateReport"

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({  serviceMethodSettings: {updateReport: "UpdateReportFromMyMethod"} });
 
{% endhighlight %}

### title `string`
{:#members:title}

Sets the title for PivotClient widget.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ title: "OLAP Browser" });

{% endhighlight %}

### url `string`
{:#members:url}

Connects the service using the specified URL for any server updates.

#### Default Value: null

**Example:**

{% highlight html %}
 
$("#PivotClient1").ejPivotClient({ url: "/wcf/OlapClientService.svc" });

{% endhighlight %}

## Methods

### doAjaxPost()
{:#methods:doajaxpost}

Perform an asynchronous HTTP (AJAX) request.

**Example:**

{% highlight html %}
 
<div id="PivotClient1"></div> 
 
<script>
$('#PivotClient1').ejPivotClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#PivotClient1").data("ejPivotClient");
clientObj.doAjaxPost("POST", "/OlapClientService.svc/Initialize", {"key", "Hello World"}, "renderControlSuccess", null);
</script>

{% endhighlight %}

### doPostBack()
{:#methods:dopostback}

Perform an asynchronous HTTP (FullPost) submit.

**Example:**

{% highlight html %}

<div id="PivotClient1"></div> 
 
<script>
$('#PivotClient1').ejPivotClient({
      url: "OlapClientService.svc"
  });
var clientObj = $("#PivotClient1").data("ejPivotClient");
clientObj.doPostBack("/OlapClientService.svc/Initialize", {"key", "Hello World"});
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
<td class="description last">Event parameters from PivotClient component.
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
<td class="description last">return the current action of PivotClient control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotClient control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotClient control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
    afterServiceInvoke: function(args) {}
});

{% endhighlight %}



### beforeServiceInvoke
{:#events:beforeserviceinvoke}

Triggers before any AJAX request is passed from PivotClient to service methods.

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
<td class="description last">Event parameters from PivotClient component.
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
<td class="description last">return the current action of PivotClient control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotClient control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotClient control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
    beforeServiceInvoke: function(args) {}
});

{% endhighlight %}


### chartLoad
{:#events:chartload}

Triggers before rendering the PivotChart.

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
<td class="description last">Event parameters from PivotChart component.
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
<td class="description last">return the current action of PivotChart control.</td>
</tr>
<tr>
<td class="name">customObject</td>
<td class="type">object</td>
<td class="description last">return the custom object bounds with PivotChart control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">return the outer HTML of PivotChart control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotChart model.</td>
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
 
$("#PivotClient1").ejPivotClient({
   chartLoad: function (args) {}
});      

{% endhighlight %}

### load
{:#events:load}

Triggers while we initiate loading of the widget.

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
<td class="description last">Event parameters from PivotClient component.
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
<td class="description last">returns the outer HTML of PivotClient component.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
   load: function (args) {}
});     

{% endhighlight %}


### renderComplete
{:#events:rendercomplete}

Triggers when PivotClient widget completes all operations at client-end after any AJAX request. 

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
<td class="description last">Event parameters from PivotClient component
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
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of PivotClient control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
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
<td class="description last">Event parameters from PivotClient component
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
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of PivotClient control.</td>
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
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
   renderFailure: function (args) {}
});     

{% endhighlight %}

### renderSuccess
{:#events:rendersuccess}

Triggers when PivotClient successfully reaches client-side after any AJAX request.

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
<td class="description last">Event parameters from PivotClient component.
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
<td class="name">customObject</td>
<td class="type">Object</td>
<td class="description last">returns the custom object bounded with the control.</td>
</tr>
<tr>
<td class="name">element</td>
<td class="type">string</td>
<td class="description last">returns the outer HTML of PivotClient control.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.PivotClient.Model"/>object</td>
<td class="description last">returns the PivotClient model.</td>
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
 
$("#PivotClient1").ejPivotClient({
   renderSuccess: function (args) {}
});      

{% endhighlight %}


## Enumeration


### clientExportMode `enum`
{:#enum:clientexportmode}

<ts name = "ej.PivotClient.ClientExportMode"/>

Sets the mode to export the OLAP visualization components such as PivotChart and PivotGrid in PivotClient. Based on the option, either Chart or Grid or both gets exported.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">To export both PivotGrid and PivotChart contents.</td>
        </tr>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">To export only PivotChart contents.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">To export only PivotGrid contents.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#PivotClient1").ejPivotClient({ clientExportMode: ej.PivotClient.ClientExportMode.ChartAndGrid});

{% endhighlight %}

### ControlPlacement  `enum`
{:#enum:controlplacement}

<ts name = "ej.PivotClient.ControlPlacement"/>

Allow the user to customize the display of PivotChart and PivotGrid widgets, either in tab view or tile view.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Tab</td>
            <td class="description">To display PivotChart and PivotGrid widgets in tab view.</td>
        </tr>
        <tr>
            <td class="name">Tile</td>
            <td class="description">To display PivotChart and PivotGrid widgets within the same view, one below the other.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotClient1").ejPivotClient({ displaySettings: {controlPlacement: ej.PivotClient.ControlPlacement.Tab} });

{% endhighlight %}


### DisplayMode  `enum`
{:#enum:displaymode}

<ts name = "ej.PivotClient.DisplayMode"/>

Sets the display mode to view only Chart or only Grid or both in PivotClient.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">ChartOnly</td>
            <td class="description">To display only PivotChart widget.</td>
        </tr>
        <tr>
            <td class="name">GridOnly</td>
            <td class="description">To display only PivotGrid widget.</td>
        </tr>
        <tr>
            <td class="name">ChartAndGrid</td>
            <td class="description">To display both PivotChart and PivotGrid widgets.</td>
        </tr>
    </tbody>
</table>


**Example:**

{% highlight html %}

$("#PivotClient1").ejPivotClient({ displaySettings: { mode: ej.PivotClient.DisplayMode.ChartOnly } });

{% endhighlight %}

### DefaultView `enum`
{:#enum:defaultview}

<ts name = "ej.PivotClient.DefaultView"/>

Allows the user to set either Chart or Grid as the start-up widget.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Chart</td>
            <td class="description">To set PivotChart as a default control in view when the PivotClient widget is loaded for the first time.</td>
        </tr>
        <tr>
            <td class="name">Grid</td>
            <td class="description">To set PivotGrid as a default control in view when the PivotClient widget is loaded for the first time.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight html %}

$("#PivotClient1").ejPivotClient({ displaySettings: {defaultView: ej.PivotClient.DefaultView.Grid} });

{% endhighlight %}

