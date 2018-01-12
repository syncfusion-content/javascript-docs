---
layout: post
title: Custom-labels
description: custom labels
platform: js
control: Circular Gauge
documentation: ug
api: /api/js/ejcirculargauge
---

# Custom labels

Custom labels are the texts that you can use them in any location of the **Gauge**.

## Adding Custom Label Collection

Custom labels collection is directly added to the scale object. Refer the following code to add [`customLabels`](../api/ejcirculargauge#members:scales-customlabels) collection in a **Gauge** control.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
        //For circular gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                showCustomLabels: true,
                customLabels: [{
                    color: "Red"
                }]
            }]
        })
    });

{% endhighlight %}

**Basic Customization**

You can customize custom labels using the properties such as [`textAngle`](../api/ejcirculargauge#members:scales-customlabels-textangle), [`color`](../api/ejcirculargauge#members:scales-customlabels-color) and [`font`](../api/ejcirculargauge#members:scales-customlabels-font).  **textAngle** attribute is used to display the custom labels in the specified angles and **color** attribute is used to display the custom labels in specified color. 

You can use [`value`](../api/ejcirculargauge#members:scales-customlabels-value) attribute to set the text value in the custom labels. To display the custom labels, set [`showCustomLabels`](../api/ejcirculargauge#members:scales-showcustomlabels) as ‘true’. To set the location of the custom label in **Circular Gauge**, [`position`](../api/ejcirculargauge#members:scales-customlabels-position) property is used. By using [`x`](../api/ejcirculargauge#members:scales-customlabels-position-x) and [`y`](../api/ejcirculargauge#members:scales-customlabels-position-y) axis you can adjust the position of the custom labels.

Font option is also available on  custom labels. The basic three properties of fonts such as size, family and style can be achieved by [`size`](../api/ejcirculargauge#members:scales-customlabels-font-size), [`fontStyle`](../api/ejcirculargauge#members:scales-customlabels-font-fontstyle) and [`fontFamily`](../api/ejcirculargauge#members:scales-customlabels-font-fontfamily) attributes. 

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
        // For Circular Gauge rendering
        $("#CircularGauge1").ejCircularGauge({
            scales: [{
                size: 10,
                shadowOffset: 10,
                showCustomLabels: true,
                showRanges: true,
                showScaleBar: true,
                radius: 150, size: 2,
                customLabels: [{
                    //For setting custom label text angle
                textAngle: 10,
                    //For setting custom label color
                color: "Red",
                    //For setting custom label value
                value: "CustomLabel1",
                    //For setting custom label font option
                font: {
                size: "18px",
                fontFamily: "Arial",
                fontStyle: "bold"
                },
                    position: { x: 180, y: 100 }
                }]
            }]
        });
    });

{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Custom-labels_images/Custom-labels_img1.png)

## Multiple Custom Labels

You can set multiple custom labels in a single **Circular Gauge** by adding an array of custom label objects. Refer the following code example for multiple custom label functionality.

{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
          // For Circular Gauge rendering
          $("#CircularGauge1").ejCircularGauge({
              scales: [{
                  size: 10,
                  shadowOffset: 10,
                  showCustomLabels: true,
                  showRanges: true,
                  showScaleBar: true,
                  radius: 150, size: 2,
                  customLabels: [
                  //custom label1
                  {
                      textAngle: 10,
                      color: "Red",
                      value: "CustomLabel1",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      position: { x: 180, y: 100 }
                  },
                  //custom label2
                  {
                      textAngle: 10,
                      color: "Green",
                      value: "CustomLabel2",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      position: { x: 180, y: 250 }
                  }]
              }]
          });
      });



{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Custom-labels_images/Custom-labels_img2.png)

## Outer Custom Label

**Outer Custom Label** is used to show custom labels outside the **gauge** control. The **Outer Custom Label** can be positioned with API called [`outerCustomLabelPosition`](../api/ejcirculargauge#members:outercustomlabelposition). The value for this API is enumerable type and its possible values are,

* Right

* Left

* Top

* Bottom

When a custom label is to be displayed as an **Outer Custom Label**, set the API [`positionType`](../api/ejcirculargauge#members:scales-customlabels-positiontype) as Outer. Refer to the following code example to get the **Outer Custom Label**.


{% highlight html %}

<div id="CircularGauge1"></div>

{% endhighlight %}


{% highlight javascript %}

 $(function () {
          $("#CircularGauge1").ejCircularGauge({
              // Sets outer custom label position.
              outerCustomLabelPosition: "right",
              //Defines the tooltip object.
              tooltip: {
                  // Enables the custom label tooltip.
                  showCustomLabelTooltip: true,
              },
              // Customizes the scale options.
              scales: [{
                  showLabels: true,
                  radius: 150,
                  // Customizes the custom label options.
                  customLabels: [{
                      value: "Average Speed",
                      position: { x: 360, y: 30 },
                      color: "Red",
                      font: {
                          size: "18px",
                          fontFamily: "Arial",
                          fontStyle: "bold"
                      },
                      positionType: "outer",
                  }],
                  // Customizes the pointers options.
                  pointers: [{
                      value: 60,
                      length: 100,
                  }]
              }]
          });
      });




{% endhighlight %}



Execute the above code to render the following output.

![](/js/CircularGauge/Custom-labels_images/Custom-labels_img3.png)

