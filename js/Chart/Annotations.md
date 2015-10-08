---
layout: post
title: Chart-Annotations
description: chart annotations
platform: js
control: Chart
documentation: ug
---

# Annotations

**Annotations** are used to mark the specific area of interest in chart area with texts, shapes or images. 

You can add annotations to the chart by using the **annotations** option. By using the **content** option of annotation object, you can specify the id of the element that needs to be displayed in the chart area.

{% highlight html %}

<body>
  <div id="chartcontainer"></div> 
              
  <div id= "watermark" style="font-size:100px; display:none">2014</div>
  <script>
   $("#chartcontainer").ejChart({

            //  ...
            annotations: [
                //Add Annotation content here
	 { visible: true, content: "watermark", opacity: 0.2, region: "series" }
                           //  ...
           ],             
        //  ...
   });
  </script>
</body>


{% endhighlight %}


![]("/js/Chart/Annotations_images/Annotations_img1.png" Caption="Chart with Annotations")

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/annotations) here to view the Annotations online demo sample.


## Rotate the annotation template

For rotating the annotation template, you can use the **angle** property of the annotations. 

{% highlight js %}


    $("#chartcontainer").ejChart({
            //  ...
            annotations: [{  visible: true, 
                    content: "watermark", 
                    //Rotate the Annotation template
                    angle: 270,
                  },
                //  ...
              ],             
          //  ...
     });


{% endhighlight %}


![]("/js/Chart/Annotations_images/Annotations_img2.png" Caption="Rotate the annotation template")

## Positioning Annotation

You can position annotations either by using the coordinates (**x** and **y** options) or using alignment options (**horizontalAlignment** and **verticalAlignment**).

By using the **coordinateUnit** option, you can specify whether the value provided in the **x** and **y** options are relative to the chart or axis.

* If the coordinateUnit is set to none, annotations are placed relative to the chart/plot area by using the **horizontalAlignment** and **verticalAlignment** options.

* If the coordinateUnit is set to points, the x and y values of the annotation are the coordinates relative to axis and annotation is positioned relative to the axis. By default, the x and y values are associated with the **primaryXAxis** and **primaryYAxis**. In case, if the chart contains multiple axis and you want to associate the annotation with a particular axis, you can specify the **xAxisName** and **yAxisName** options of the annotation object.

* If the coordinateUnit is set to pixels, the x and y values are coordinates relative to the top-left corner of the chart/plot area.   

N> By using the **region** option, you can specify whether annotation is placed relative to the entire chart or plot area.

{% highlight js %}


    $("#chartcontainer").ejChart({
            //  ...
             annotations: [{  visible: true, 
                  content: "lowtemp", 
                  //Change coordinateUnit type to pixels
                  coordinateUnit: "pixels",  x: 170, y: 350,   
                  //  ...
                  },
                //  ...
             ],  
        //  ...
     });


{% endhighlight %}


![]("/js/Chart/Annotations_images/Annotations_img3.png" Caption="Annotations with chart region")


## Annotation alignments

When the coordinateUnit is set to pixels or points, you can align the annotation relative to the coordinates by using the **horizontalAlignment** and **verticalAlignment** options. 

{% highlight js %}


    $("#chartcontainer").ejChart({
            //  ...
             annotations: [{  visible: true, 
                     content: "hightemp", 
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


![]("/js/Chart/Annotations_images/Annotations_img4.png")

Change annotation alignments
{:.caption}
