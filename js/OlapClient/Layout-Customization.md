---
layout: post
title: Layout-Customization
description: layout customization
platform: js
control: OLAP Client
documentation: ug
---

# Layout Customization

**OLAP Client UI** comes with options to customize the **Grid** and **Chart** layout, such as:

   * **Default View** - Sets the start-up control. 

   * **Tab/Tile View** – Tab or Tile view to visualize the controls separately or in the same layout. 

   * **Hide Grid/Chart** - Hides any one of the control by default. 

   * **Toggle Panel** – Turns On/Off the visibility of Cube Browser and Axis Element Builder panels.  

   * **Maximized/Fullscreen** view of the control(s) providing a precise view.

## Display View

###Tile View

In Tile View representation, both **Grid** and **Chart** will be displayed one over the other, in the same layout. 

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { controlPlacement: "tile" }
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img1.png" Caption="Tile View"%}

### Tab View

In **Tab** View representation, both **Grid** and **Chart** will be displayed in a separate tab.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { controlPlacement: "tab" }
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img2.png" Caption="Tab View"%}

## Default View

After you set **defaultView** property either to **Chart** or **Grid**, the corresponding control is selected for initial view/visualization, within the layout when the **OLAP Client** control is loaded for the first time. 

### Chart View

To display/visualize Chart control by default, set defaultView to Chart.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { defaultView: "chart" }
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img3.png" Caption="Default Chart View"%}

### Grid View

To display/visualize **Grid** control by default, set **defaultView** to **Grid**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
     url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
     displaySettings: { defaultView: "grid" }
 });


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img4.png" Caption="Default Grid View"%}

## Hide Grid/Chart

###Grid Only

After you set the**displayMode** option to **GridOnly**, the **Chart** is hidden and the data is displayed only in **Grid**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { mode: ej.olap.OlapClient.DisplayMode.GridOnly}
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img5.png" Caption="Grid Only Mode"%}

###Chart Only

After you set the **displayMode** option to **ChartOnly**, the **Grid** is hidden and data is displayed only in **Chart**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { mode: ej.olap.OlapClient.DisplayMode.ChartOnly }
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img6.png" Caption="Chart Only Mode"%}

###Both Grid and Chart

After you set the **displayMode** option to **ChartAndGrid**, data is displayed in both **Grid** and **Chart**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { mode: ej.olap.OlapClient.DisplayMode.ChartAndGrid }
});


{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img7.png" Caption="Grid and Chart Mode"%}

## Toggle Panel

You are provided with an option to toggle the visibility of Axis Element Builder and Cube Dimension Browser panels in **OLAP Client**.

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { enableTogglePanel: true }});



{% endhighlight %}

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img8.png" Caption="OLAP Client in Toggled View"%}

## Maximized/Full Screen View

You can maximize **OLAP Grid** and **OLAP Chart** to full screen mode inside **OLAP Client** for a precise view. By selecting Full Screen icon in the toolbar, **OLAP Grid** and **OLAP Chart** are maximized depending on the current tab. You can also perform drilldown action in both **OLAP Grid** and **OLAP Chart** in the maximized view.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img9.png" Caption="Full screen view icon"%}

{% highlight js %}

$("#OlapClient1").ejOlapClient({
    url: "../wcf/OlapClientService.svc", title: "OLAP Browser",
    displaySettings: { enableFullScreen: true }
});

{% endhighlight %}

The following screenshot shows the maximized view of **OLAP Grid** and **OLAP Chart.**

{% include image.html url="/js/OlapClient/Concepts-and-Features/Layout-Customization_images/Layout-Customization_img10.png" Caption="Maximized View for OLAP Chart and OLAP Grid"%}

