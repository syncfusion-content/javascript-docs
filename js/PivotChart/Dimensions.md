---
layout: post
title: Dimensions with PivotChart widget for Syncfusion Essential JS
description: dimensions
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Dimensions

## Set size in percentage

You can customize the pivot chart dimension under the [`size`](/api/js/ejpivotchart#members:size) property by setting the width and height of the widget in percentage.

{% highlight javascript %}

<body>
    <div id="PivotChart1" style="width: 100%; height: 450px" ></div>
    <script type="text/javascript">
                //Datasource
                ....
                ....
        $(function () {
            $("#PivotChart1").ejPivotChart({
                ....
                ....
                //Setting size to Chart container
                size: {
                    height: "80%",
                    width: "80%"
               }
            });
        });
    </script>
</body>

{% endhighlight %}

## Set size in pixels

You can customize the pivot chart dimension under the [`size`](/api/js/ejpivotchart#members:size) property by setting the width and height of the widget in pixels.

{% highlight javascript %}

<body>
    <div id="PivotChart1" style="width: 950px; height: 460px" ></div>
    <script type="text/javascript">
                //Datasource
                ....
                ....
        $(function () {
            $("#PivotChart1").ejPivotChart({
                ....
                ....
                //Setting size to Chart container
                size: {
                    height: "460px",
                    width: "950px"
               }
            });
        });
    </script>
</body>

{% endhighlight %}

![JavaScript pivot chart control with specified size](Dimensions_images/Dimensions.png)

## Responsive

The pivot chart widget supports responsive rendering based on the target device (desktop and tablet) resolution. It supports resolution upto 1024x600. You can enable the responsiveness in the pivot chart by setting the [`isResponsive`](/api/js/ejpivotchart#members:isresponsive) property to true.

{% highlight javascript %}

<body>
    <div id="PivotChart1" style="min-width: 950px; min-height: 460px;width: 100%" ></div>
    <script type="text/javascript">
                //Datasource
                ....
                ....
        $(function () {
            $("#PivotChart1").ejPivotChart({
                ....
                ....
                //Enable responsiveness to change the Chart size dynamically.
                isResponsive: true,
                size: {
                    height: "460px",
                    width: "950px"
               }
            });
        });
    </script>
</body>

{% endhighlight %}

![JavaScript pivot chart with normal layout](Dimensions_images/NormalView.png)

_Normal View_

![JavaScript pivot chart with responsive layout](Dimensions_images/ResponsiveView.png)

_ResponsiveView_