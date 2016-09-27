---
layout: post
title: Layout-Customization
description: layout customization
platform: js
control: OlapClient
documentation: ug
---

# Layout Customization

## Display View

### Tab View
In Tab View representation, both Grid and Chart will be displayed in a separate tab.  This could be set using the [`controlPlacement`](/js/api/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option.  By default, **Tab** value is set.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        controlPlacement: ej.olap.OlapClient.ControlPlacement.Tab
    }
});

{% endhighlight %}

![](Layout-Customization_images/tab.png) 

### Tile View
In Tile View representation, both Grid and Chart will be displayed one over the other, in the same layout. Tile view can be set by using the [`controlPlacement`](/js/api/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        controlPlacement: ej.olap.OlapClient.ControlPlacement.Tile
    }
});

{% endhighlight %}

![](Layout-Customization_images/tile view.png)

## Default View

### Grid View
To display Grid control by default, set [`defaultView`](/js/api/ejpivotclient#members:displaysettings-defaultview) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option to **Grid**, which is the default value of the property.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        defaultView: ej.olap.OlapClient.DefaultView.Grid
    }
});

{% endhighlight %}

![](Layout-Customization_images/grid layout.png)

### Chart View
To display Chart control by default, set the property [`defaultView`](/js/api/ejpivotclient#members:displaysettings-defaultview) property to **Chart**.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        defaultView: ej.olap.OlapClient.DefaultView.Chart
    }
});

{% endhighlight %}

![](Layout-Customization_images/Chart view.png)

## Display Mode

### Grid Only
After setting the [`mode`](/js/api/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option to **GridOnly**, the Chart is hidden and the data is displayed only in the Grid.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.GridOnly
    }
});

{% endhighlight %}

![](Layout-Customization_images/Grid only.png)

### Chart Only
After setting the [`mode`](/js/api/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option to **ChartOnly**, the Grid is hidden and data is displayed only in the Chart.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.ChartOnly
    }
});

{% endhighlight %}

![](Layout-Customization_images/Chart only.png)

### Both Chart and Grid
After setting the [`mode`](/js/api/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option to **ChartAndGrid**, data is displayed in both Grid and Chart.  This is the default value of the property.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.ChartAndGrid
    }
});

{% endhighlight %}

![](Layout-Customization_images/grid layout.png)

## Toggle Panel
Toggle panel option lets the user to toggle the visibility of Axis Element Builder and Cube Dimension Browser panels in OlapClient with a use of a button. The button could be added to the control by using the [`enableTogglePanel`](/js/api/ejpivotclient#members:displaysettings-enabletogglepanel) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings) option.  This property is disabled by default.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        enableTogglePanel: true
    }
});

{% endhighlight %}

![](Layout-Customization_images/toggle panel.png)

## Maximized/Full Screen View
Full screen view helps to visualize the PivotGrid and OlapChart controls inside OlapClient precisely according to the browser window size.  By selecting full screen icon in the toolbar, PivotGrid/OlapChart is maximized depending on the selected tab.  Drilldown action can also be performed in both PivotGrid and OlapChart in the maximized view.  This option is enabled by setting the [`enableFullScreen`](/js/api/ejpivotclient#members:displaysettings-enablefullscreen) property under [`displaySettings`](/js/api/ejpivotclient#members:displaysettings)  option to true.  The value is false by default.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    displaySettings: {
        enableFullScreen: true
    }
});

{% endhighlight %}

![](Layout-Customization_images/fullscreen icon.png)

The following screenshot shows the maximized view of PivotGrid.

![](Layout-Customization_images/fullscreen view.png)

## Grid Layout
PivotGrid inside OlapClient control can be rendered in any of the following layouts.

* Normal
* NormalTopSummary
* NoSummaries
* ExcelLikeLayout

The layout is set using the [`gridLayout`](/js/api/ejpivotclient#members:gridlayout) property. By default, normal layout is set.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    gridLayout: ej.PivotGrid.Layout.NoSummaries
});

{% endhighlight %}

![](Layout-Customization_images/grid layout.png)

## Chart Types
While loading the OlapClient initially, the OlapChart widget can be rendered in any one of the available chart types using the [`chartType`](/js/api/ejpivotclient#members:charttype) property.

{% highlight javascript %}

$("#OlapClient").ejOlapClient({
    url: "/OlapClient",
    title: "OLAP Browser",
    chartType: ej.olap.OlapChart.ChartTypes.Area
});

{% endhighlight %} 

The [`chartType`](/js/api/ejpivotclient#members:charttype) property takes Column Chart by default. The types available are Column, Stacking Column, Bar, Stacking Bar, Line, Spline, Step Line, Area, Spline Area, Step Area, Stacking Area, Pie, Funnel and Pyramid.

The Chart Type can also be changed dynamically through the toolbar icon. 

![](Layout-Customization_images/chart type.png)

![](Layout-Customization_images/chart type changed.png)
