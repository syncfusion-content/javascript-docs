---
layout: post
title: Layout-Customization
description: layout customization
platform: js
control: OlapClient
documentation: ug
---

# Layout Customization

**OlapClient UI** comes with options to customize the **Grid** and **Chart** layout, such as:

   * **Default View** - Sets the start-up control. 
   * **Tab/Tile View** – Tab or Tile view to visualize the controls separately or in the same layout. 
   * **Hide Grid/Chart** - Hides any one of the control by default. 
   * **Toggle Panel** – Turns On/Off the visibility of Cube Browser and Axis Element Builder panels.  
   * **Maximized/Fullscreen** view of the control(s) providing a precise view.

## Display View

###Tile View

In [Tile](/js/api/ejOlapClient#members:displaysettings-controlplacement) View representation, both **Grid** and **Chart** will be displayed one over the other, in the same layout. 

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        controlPlacement: "tile"
    }
});

{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img1.png) 

### Tab View

In [Tab](/js/api/ejOlapClient#members:displaysettings-controlplacement) View representation, both **Grid** and **Chart** will be displayed in a separate tab.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        controlPlacement: "tab"
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img2.png) 

## Default View

After you set **defaultView** property either to **Chart** or **Grid**, the corresponding control is selected for initial view/visualization, within the layout when the **OlapClient** control is loaded for the first time. 

### Chart View

To display/visualize Chart control by default, set [defaultView](/js/api/ejOlapClient#members:displaysettings-defaultview) to Chart.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        defaultView: "chart"
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img3.png) 

### Grid View

To display/visualize **Grid** control by default, set [defaultView](/js/api/ejOlapClient#members:displaysettings-defaultview) to **Grid**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        defaultView: "grid"
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img4.png) 

## Hide Grid/Chart

###Grid Only

After you set the [displayMode](/js/api/ejOlapClient#members:displaysettings-mode) option to **GridOnly**, the **Chart** is hidden and the data is displayed only in **Grid**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.GridOnly
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img5.png) 

###Chart Only

After you set the [displayMode](/js/api/ejOlapClient#members:displaysettings-mode) option to **ChartOnly**, the **Grid** is hidden and data is displayed only in **Chart**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.ChartOnly
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img6.png) 

###Both Grid and Chart

After you set the [displayMode](/js/api/ejOlapClient#members:displaysettings-mode) option to **ChartAndGrid**, data is displayed in both **Grid** and **Chart**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        mode: ej.olap.OlapClient.DisplayMode.ChartAndGrid
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img7.png) 

## Toggle Panel

You are provided with an option to [toggle](/js/api/ejOlapClient#members:displaysettings-enabletogglepanel) the visibility of Axis Element Builder and Cube Dimension Browser panels in **OlapClient**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        enableTogglePanel: true
    }
});


{% endhighlight %}

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img8.png) 

## Maximized/Full Screen View

You can maximize **PivotGrid** and **OlapChart** to [full screen mode](/js/api/ejOlapClient#members:displaysettings-enablefullscreen) inside **OlapClient** for a precise view. By selecting Full Screen icon in the toolbar, **PivotGrid** and **OlapChart** are maximized depending on the current tab. You can also perform drilldown action in both **PivotGrid** and **OlapChart** in the maximized view.

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img9.png) 

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc",
    title: "OLAP Browser",
    displaySettings: {
        enableFullScreen: true
    }
});

{% endhighlight %}

The following screenshot shows the maximized view of **PivotGrid** and **OlapChart.**

![](/js/OlapClient/Layout-Customization_images/Layout-Customization_img10.png) 

