---
layout: post
title: Layout-Customization with PivotClient for Syncfusion JavaScript
description: layout customization
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Layout customization

## Size

Allows you to render the pivot client in different sizes. You can set the height and width under the [`size`](/api/js/ejpivotclient#members:size) property.

## Set size in pixels

{% highlight html %}

<div id="PivotClient1"></div>
<script>
    $(function() {
        $("#PivotClient1").ejPivotClient({
            //...
            size: { width: "1000px" , height: "685px" }
        });
    });
</script>

{% endhighlight %}

Th pivot client with decreased size from default size.

![JavaScript pivot client control with reduced size](Layout-Customization_images/small-size.png)

## Set size in percentage

You can also set the pivot client size in percentage.

N> The size of the parent container should be set in pixels.

{% highlight html %}

<div id="control" style="width:1000px; height:800px">
  <div id="PivotClient1">
    <script>
        $(function() {
            $("#PivotClient1").ejPivotClient({
                //...
                size:{ width: "50%" , height: "80%" }
            });
        });
    </script>
  </div>
</div>

{% endhighlight %}

N> The pivot client is set with minimum height and width to show the decent UI.
## Control placement

### Tab view
In tab view representation, both the grid and the chart will be displayed in separate tabs. This can be set by using the [`controlPlacement`](/api/js/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.  By default, the **Tab** value is set.

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    displaySettings: {
        controlPlacement: ej.PivotClient.ControlPlacement.Tab
    }
});

{% endhighlight %}

![JavaScript pivot client control with tab view](Layout-Customization_images/tab.png)

### Tile view
In tile view representation, both the grid and the chart will be displayed one above the other, in the same layout. The tile view can be set by using the [`controlPlacement`](/api/js/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    displaySettings: {
        controlPlacement: ej.PivotClient.ControlPlacement.Tile
    }
});

{% endhighlight %}

![JavaScript pivot client control with tile view](Layout-Customization_images/tile-view.png)

## Default view

### Grid view
To display the grid control by default, set the [`defaultView`](/api/js/ejpivotclient#members:displaysettings-defaultview) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **Grid**, which is the default value of the property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            defaultView: ej.PivotClient.DefaultView.Grid
        }
    });

{% endhighlight %}

![JavaScript pivot client control with grid view as default](Layout-Customization_images/grid-view.png)

### Chart view
To display chart control by default, set the [`defaultView`](/api/js/ejpivotclient#members:displaysettings-defaultview) property to **Chart**.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            defaultView: ej.PivotClient.DefaultView.Chart
        }
    });

{% endhighlight %}

![JavaScript pivot client control with chart view as default](Layout-Customization_images/Chart-view.png)

## Display mode

### Grid only
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **GridOnly**, the pivot grid component alone will get rendered and the pivot chart will not be rendered.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.GridOnly
        }
    });

{% endhighlight %}

![JavaScript pivot client control with grid only view](Layout-Customization_images/Grid-only.png)

### Chart Only
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **ChartOnly**, the pivot chart component alone will get rendered and the pivot grid will not be rendered.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.ChartOnly
        }
    });

{% endhighlight %}

![JavaScript pivot client control with chart only view](Layout-Customization_images/Chart-only.png)

### Both chart and grid
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **ChartAndGrid**, the data is displayed in both the grid and chart.  This is the default value of the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.ChartAndGrid
        }
    });

{% endhighlight %}

![JavaScript pivot client control with grid and chart view](Layout-Customization_images/tile-view.png)

## Toggle panel
The toggle panel option allows you to toggle the visibility of axis element builder and cube dimension browser panels in the pivot client with a use of a button. The button can be added to the control by enabling the [`enableTogglePanel`](/api/js/ejpivotclient#members:displaysettings-enabletogglepanel) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.  This property is disabled by default.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            enableTogglePanel: true
        }
    });

{% endhighlight %}

![JavaScript pivot client control with toggle panel](Layout-Customization_images/toggle-panel.png)

## Collapse toggle panel by default

Allows you to hide the “Cube Browser” and “Axis Element Builder” panels while initiating the widget. You can enable this option in the pivot client by setting the [`collapseCubeBrowserByDefault`](/api/js/ejpivotclient#members:collapsecubebrowserbydefault) property to true.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        collapseCubeBrowserByDefault: true
    });

{% endhighlight %}

![JavaScript pivot client control with toggle panel by default](Layout-Customization_images/collapse-cube-browser-by-default.png)

## Maximized/full screen view
Full screen view helps to visualize the pivot grid and pivot chart controls in the pivot client precisely according to the browser window size.  By selecting full screen icon in the toolbar, the control which is in the view gets maximized. The drill down action can also be performed in both the pivot grid and the pivot chart in the maximized view.  This option is enabled by setting the [`enableFullScreen`](/api/js/ejpivotclient#members:displaysettings-enablefullscreen) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings)  option to true.  The value is false by default.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            enableFullScreen: true
        }
    });

{% endhighlight %}

![Full screen icon in JavaScript pivot client control](Layout-Customization_images/fullscreen-icon.png)

The following screenshot shows the maximized view of the pivot grid:

![Full screen view of JavaScript pivot client control](Layout-Customization_images/fullscreen-view.png)


## Chart types
While loading the pivot client initially, the pivot chart widget can be rendered in any one of the available chart types using the [`chartType`](/api/js/ejpivotclient#members:charttype) property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        chartType: ej.PivotChart.ChartTypes.Area
    });

{% endhighlight %}

The [`chartType`](/api/js/ejpivotclient#members:charttype) property takes column chart by default. The available chart types are column, stacking column, bar, stacking bar, line, spline, step line, area, spline area, step area, stacking area, pie, funnel, and pyramid.

The chart type can also be changed dynamically through the toolbar icon.

![Chart types in JavaScript pivot client control](Layout-Customization_images/chart-type.png)

![JavaScript pivot client control with line chart type](Layout-Customization_images/chart-type-changed.png)

### Pivot tree map

I> This feature is applicable only for the OLAP data source bound from the server-side.

You can include the pivot tree map component as one of the chart type by setting the [`enablePivotTreeMap`](/api/js/ejpivotclient#members:enablepivottreemap) property to true.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        enablePivotTreeMap: true
    });

{% endhighlight %}

![Treemap icon in chart types panel of JavaScript pivot client control](Layout-Customization_images/TreeMap1.png)

![Treemap in JavaScript pivot client control](Layout-Customization_images/TreeMap2.png)

## Report Toolbar

You can customize the display of toolbar by enabling/disabling the visibility of each icon.  This can be achieved by setting the properties under the [`toolbarIconSettings`](/api/js/ejpivotclient#members:toolbariconsettings) option to false. The values are true by default.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        //Disable toolbar icon in PivotClient.
        toolbarIconSettings: {
            enableAddReport: false,
            enableNewReport: false,
            enableRemoveReport: false
        }
    });

{% endhighlight %}

![Report toolbar in JavaScript pivot client control](Layout-Customization_images/toolbarIconSettings1.png)

The following screenshot will be displayed after disabling the toolbar icons.

![Hiding report icons from toolbar of JavaScript pivot client control](Layout-Customization_images/toolbarIconSettings2.png)

The following table will explain you the available properties for the customization of the report toolbar.

| Property | Description
|---|---|
| [`enableNewReport`](/api/js/ejpivotclient#members:toolbariconsettings-enablenewreport) | Allows you to set the visibility of `New Report` icon in the toolbar panel.|
| [`enableAddReport`](/api/js/ejpivotclient#members:toolbariconsettings-enableaddreport) | Allows you to set the visibility of `Add Report` icon in the toolbar panel.|
| [`enableRemoveReport`](/api/js/ejpivotclient#members:toolbariconsettings-enableremovereport) | Allows you to set the visibility of `Remove Report` icon in the toolbar panel.|
| [`enableRenameReport`](/api/js/ejpivotclient#members:toolbariconsettings-enablerenamereport) | Allows you to set the visibility of `Rename Report` icon in the toolbar panel.|
| [`enableDBManipulation`](/api/js/ejpivotclient#members:toolbariconsettings-enabledbmanipulation) | Allows you to set the visibility of `DB Manipulation` icon in the toolbar panel.|
| [`enableMDXQuery`](/api/js/ejpivotclient#members:toolbariconsettings-enablemdxquery) | Allows you to set the visibility of `MDX Query` icon in the toolbar panel.|
| [`enableDeferUpdate`](/api/js/ejpivotclient#members:toolbariconsettings-enabledeferupdate) | Allows you to set the visibility of `Defer Update` icon in the toolbar panel.|
| [`enableExcelExport`](/api/js/ejpivotclient#members:toolbariconsettings-enableexcelexport) | Allows you to set the visibility of `Excel Export` icon in the toolbar panel.|
| [`enableWordExport`](/api/js/ejpivotclient#members:toolbariconsettings-enablewordexport) | Allows you to set the visibility of `Word Export` icon in the toolbar panel.|
| [`enablePdfExport`](/api/js/ejpivotclient#members:toolbariconsettings-enablepdfexport)| Allows you to set the visibility of `PDF Export` icon in the toolbar panel.|
| [`enableFullScreen`](/api/js/ejpivotclient#members:toolbariconsettings-enablefullscreen)| Allows you to set the visibility of `Full Screen` icon in the toolbar panel.|
| [`enableSortOrFilterColumn`](/api/js/ejpivotclient#members:toolbariconsettings-enablesortorfiltercolumn)| Allows you to set the visibility of `Sort/Filter Column` icon in the toolbar panel.|
| [`enableSortOrFilterRow`](/api/js/ejpivotclient#members:toolbariconsettings-enablesortorfilterrow)| Allows you to set the visibility of `Sort/Filter Row` icon in the toolbar panel.|
| [`enableToggleAxis`](/api/js/ejpivotclient#members:toolbariconsettings-enabletoggleaxis)| Allows you to set the visibility of `Toggle Axis` icon in the toolbar panel.|
| [`enableChartTypes`](/api/js/ejpivotclient#members:toolbariconsettings-enablecharttypes)| Allows you to set the visibility of `Chart Types` icon in the toolbar panel.|
| [`enableCalculatedMember`](/api/js/ejpivotclient#members:toolbariconsettings-enablecalculatedmember)| Allows you to set the visibility of `Calculated Member` icon in the toolbar panel.|