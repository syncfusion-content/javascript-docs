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

You can add annotations to chart using **annotations** option. Using **content** option of annotation object, you can specify the id of the element which needs to be displayed in the chart area.

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


{% include image.html url="/js/Chart/Annotations_images/Annotations_img1.png" Caption="Chart with Annotations"%}

[Click](http://js.syncfusion.com/demos/web/#!/azure/chart/chartcustomization/annotations) here to view the Annotations online demo sample.


## Rotate the annotation template

For rotating the annotation template, use **angle** property of annotations. 

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


{% include image.html url="/js/Chart/Annotations_images/Annotations_img2.png" Caption="Rotate the annotation template"%}

## Positioning Annotation

You can position annotations either using coordinates (**x** and **y** options) or using alignment options (**horizontalAlignment** and **verticalAlignment**).

Using **coordinateUnit** option, you can specify whether the value provided in **x** and **y** options are relative to chart or axis.

* If the coordinateUnit is set to none, annotation will be placed relative to chart/plot area using **horizontalAlignment** and **verticalAlignment** options.

* If the coordinateUnit is set to points, x and y values of the annotation are coordinates relative to axis and annotation will be positioned relative to the axis. By default, x and y values will be associated with **primaryXAxis** and **primaryYAxis**. In case, if the chart contains multiple axis and you want to associate the annotation with particular axis, you can specify **xAxisName** and **yAxisName** options of annotation object.

* If the coordinateUnit is set to pixels, x and y values are coordinates relative to the top-left corner of chart/plot area.   

N> Using **region** option, you can specify whether annotation has to be placed relative to entire chart or plot area.

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


{% include image.html url="/js/Chart/Annotations_images/Annotations_img3.png" Caption="Annotations with chart region"%}


## Annotation alignments

When the coordinateUnit is set to pixels or points, you can align the annotation relative to the coordinates using **horizontalAlignment** and **verticalAlignment** options. 

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


{% include image.html url="/js/Chart/Annotations_images/Annotations_img4.png" Caption="Change annotation alignments"%} 
