---
layout: post
title: Chart Annotations 
description: How to add annotations in Essential JavaScript Chart and the different options available to customize its position. 
platform: js
control: Chart
documentation: ug
api : /api/js/ejchart
---

# Annotations

annotations are used to mark the specific area of interest in the chart area with texts, shapes or images. 

You can add annotations to the chart by using the [`annotations`](../api/ejchart#members:annotations) option. By using the [`content`](../api/ejchart#members:annotations-content) option of annotation object, you can specify the id of the element that needs to be displayed in the chart area.

The visibility of the annotation is controlled by using the [`visible`](../api/ejchart#members:annotations-visible) property.The opacity of the annotation object displayed is customized by using the [`opacity`](../api/ejchart#members:annotations-opacity) property.

{% highlight html %}

<body>
  <div id="container"></div> 
              
  <div id= "water" style="font-size:100px; display:none">2014</div>
  <script>
   $("#container").ejChart({

            //  ...
            annotations: [
                //Add Annotation content here
	              { visible: true, content: "water", opacity: 0.2, region: "series" }
                //  ...
           ],             
        //  ...
   });
  </script>
</body>


{% endhighlight %}


![](/js/Chart/Annotations_images/Annotations_img1.png)


[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/annotations) here to view the Annotations online demo sample.

N> Annotations are not supported in 3D chart types.

## Rotate the annotation template

To rotate the annotation template, you can use the [`angle`](../api/ejchart#members:annotations-angle) property of the annotations. 

{% highlight javascript %}


    $("#container").ejChart({
            //  ...
            annotations: [{  visible: true, 
                    content: "water", 
                    //Rotate the Annotation template
                    angle: 270,
                  },
                //  ...
              ],             
          //  ...
     });


{% endhighlight %}


![](/js/Chart/Annotations_images/Annotations_img2.png)

## Positioning Annotation

You can position annotations either by using the coordinates ([`x`](../api/ejchart#members:annotations-x) and [`y`](../api/ejchart#members:annotations-y) options) or by using the alignment options ([`horizontalAlignment`](../api/ejchart#members:annotations-horizontalalignment) and [`verticalAlignment`](../api/ejchart#members:annotations-verticalalignment)).

By using the [`coordinateUnit`](../api/ejchart#members:annotations-coordinateunit) option, you can specify whether the value provided in the [`x`](../api/ejchart#members:annotations-x) and [`y`](../api/ejchart#members:annotations-y) options are relative to the chart or axis.

* If the coordinateUnit is set to none, the annotations are placed relative to the chart/plot area by using the [`horizontalAlignment`](../api/ejchart#members:annotations-horizontalalignment) and [`verticalAlignment`](../api/ejchart#members:annotations-verticalalignment) options.

* If the coordinateUnit is set to points, the x and y values of the annotation are the coordinates relative to the axis and annotation is positioned relative to the axis. By default, the x and y values are associated with the [`primaryXAxis`](../api/ejchart#members:annotations-primaryxaxis) and [`primaryYAxis`](../api/ejchart#members:annotations-primaryyaxis). In case, when the chart contains multiple axis and you want to associate the annotation with a particular axis, you can specify the [`xAxisName`](../api/ejchart#members:annotations-xaxisname) and [`yAxisName`](../api/ejchart#members:annotations-yaxisname) options of the annotation object.

* If the coordinateUnit is set to pixels, the x and y values are coordinates relative to the top-left corner of the chart/plot area.   

N> By using the [`region`](../api/ejchart#members:annotations-region) option, you can specify whether the annotation is placed relative to the entire chart or plot area.

{% highlight javascript %}


    $("#container").ejChart({
            //  ...
             annotations: [{  visible: true, 
                  content: "lowTemperature", 
                  //Change coordinateUnit type to pixels
                  coordinateUnit: "pixels",  x: 170, y: 350,   
                  //  ...
                  },
                //  ...
             ],  
        //  ...
     });


{% endhighlight %}


![](/js/Chart/Annotations_images/Annotations_img3.png)


## Annotation alignments

When the coordinateUnit is set to pixels or points, you can align the annotation relative to the coordinates by using the [`horizontalAlignment`](../api/ejchart#members:annotations-horizontalalignment) and [`verticalAlignment`](../api/ejchart#members:annotations-verticalalignment) options. 

We can also place the annotation to the specified position by using the [`margin`](../api/ejchart#members:annotations-margin) property. 
The margin property of the annotation can  further be customized in [`right`](../api/ejchart#members:annotations-margin-right),
[`left`](../api/ejchart#members:annotations-margin-left),[`top`](../api/ejchart#members:annotations-margin-top) and [`bottom`](../api/ejchart#members:annotations-margin-bottom) directions.

{% highlight javascript %}


    $("#container").ejChart({
            //  ...
             annotations: [{  visible: true, 
                     content: "highTemperature", 
                     //Change alignment of annotation template
                     verticalAlignment: "middle",
                     horizontalAlignment: "near",
                     margin: { right: 40 }                          
                  },                                
               //  ...
           ],             

          //  ...
      });


{% endhighlight %}


![](/js/Chart/Annotations_images/Annotations_img4.png)
