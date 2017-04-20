---
layout: post
title: Layout-Customization
description: layout customization
platform: js
control: PivotClient
documentation: ug
api: /api/js/ejpivotclient
---

# Layout Customization

## Size

Allows you to render PivotClient in different sizes. You can set height and width under ['size'] property. 

## Set size in Pixels

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

PivotClient with decreased size from Default size

![](Layout-Customization_images/small-size.png)

## Set size in percentage

You can set the PivotClient size in percentage also.

N> Size of the parent container should be set in Pixels.

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

N> PivotClient set with minimum height and width to show decent UI.
## Control Placement

### Tab View
In Tab View representation, both Grid and Chart will be displayed in separate tabs. This could be set by using the [`controlPlacement`](/api/js/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.  By default, **Tab** value is set.

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    displaySettings: {
        controlPlacement: ej.PivotClient.ControlPlacement.Tab
    }
});

{% endhighlight %}

![](Layout-Customization_images/tab.png) 

### Tile View
In Tile View representation, both Grid and Chart will be displayed one above the other, in the same layout. Tile view can be set by using the [`controlPlacement`](/api/js/ejpivotclient#members:displaysettings-controlplacement) property under the [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.

{% highlight javascript %}

$("#PivotClient1").ejPivotClient({
    //...
    displaySettings: {
        controlPlacement: ej.PivotClient.ControlPlacement.Tile
    }
});

{% endhighlight %}

![](Layout-Customization_images/tile-view.png)

## Default View

### Grid View
To display Grid control by default, set [`defaultView`](/api/js/ejpivotclient#members:displaysettings-defaultview) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **Grid**, which is the default value of the property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            defaultView: ej.PivotClient.DefaultView.Grid
        }
    });

{% endhighlight %}

![](Layout-Customization_images/grid-view.png)

### Chart View
To display Chart control by default, set the property [`defaultView`](/api/js/ejpivotclient#members:displaysettings-defaultview) property to **Chart**.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            defaultView: ej.PivotClient.DefaultView.Chart
        }
    });

{% endhighlight %}

![](Layout-Customization_images/Chart-view.png)

## Display Mode

### Grid Only
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **GridOnly**, PivotGrid component alone will get rendered and PivotChart will not be rendered.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.GridOnly
        }
    });

{% endhighlight %}

![](Layout-Customization_images/Grid-only.png)

### Chart Only
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **ChartOnly**, PivotChart component alone will get rendered and PivotGrid will not be rendered.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.ChartOnly
        }
    });

{% endhighlight %}

![](Layout-Customization_images/Chart-only.png)

### Both Chart and Grid
By setting the [`mode`](/api/js/ejpivotclient#members:displaysettings-mode) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option to **ChartAndGrid**, data is displayed in both Grid and Chart.  This is the default value of the property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            mode: ej.PivotClient.DisplayMode.ChartAndGrid
        }
    });

{% endhighlight %}

![](Layout-Customization_images/tile-view.png)

## Toggle Panel
Toggle panel option lets the user to toggle the visibility of Axis Element Builder and Cube Dimension Browser panels in PivotClient with a use of a button. The button could be added to the control by enabling the [`enableTogglePanel`](/api/js/ejpivotclient#members:displaysettings-enabletogglepanel) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings) option.  This property is disabled by default.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            enableTogglePanel: true
        }
    });

{% endhighlight %}

![](Layout-Customization_images/toggle-panel.png)

## Maximized/Full Screen View
Full screen view helps to visualize the PivotGrid and PivotChart controls inside PivotClient precisely according to the browser window size.  By selecting full screen icon in the toolbar, the control which is in the view gets maximized.  Drilldown action can also be performed in both PivotGrid and PivotChart in the maximized view.  This option is enabled by setting the [`enableFullScreen`](/api/js/ejpivotclient#members:displaysettings-enablefullscreen) property under [`displaySettings`](/api/js/ejpivotclient#members:displaysettings)  option to true.  The value is false by default.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        displaySettings: {
            enableFullScreen: true
        }
    });

{% endhighlight %}

![](Layout-Customization_images/fullscreen-icon.png)

The following screenshot shows the maximized view of PivotGrid.

![](Layout-Customization_images/fullscreen-view.png)


## Chart Types
While loading the PivotClient initially, the PivotChart widget can be rendered in any one of the available chart types using the [`chartType`](/api/js/ejpivotclient#members:charttype) property.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        //...
        chartType: ej.PivotChart.ChartTypes.Area
    });

{% endhighlight %} 

The [`chartType`](/api/js/ejpivotclient#members:charttype) property takes Column Chart by default. The types available are Column, Stacking Column, Bar, Stacking Bar, Line, Spline, Step Line, Area, Spline Area, Step Area, Stacking Area, Pie, Funnel and Pyramid.

The Chart Type can also be changed dynamically through the toolbar icon. 

![](Layout-Customization_images/chart-type.png)

![](Layout-Customization_images/chart-type-changed.png)

### PivotTreeMap

I> This feature is applicable only for OLAP data source bound from server-side.

You can include the PivotTreeMap component as one of the chart types by setting [`enablePivotTreeMap`](/api/js/ejPivotClient#members:enablepivottreemap) property to true.

{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({ 
        //...
        enablePivotTreeMap: true 
    });

{% endhighlight %} 

![](Layout-Customization_images/TreeMap1.png)

![](Layout-Customization_images/TreeMap2.png)

## Report Toolbar

You can customize the display of toolbar by enabling/disabling the visibility of each of the icons.  This can be achieved by setting the properties under [`toolbarIconSettings`](/api/js/ejpivotclient#members:toolbariconsettings) option to false. The values are true by default.

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

![](Layout-Customization_images/toolbarIconSettings1.png)

The following screenshot shows after disabling the toolbar icons.

![](Layout-Customization_images/toolbarIconSettings2.png)