---
layout: post
title: -ranges-and-frames
description:  ranges and frames
platform: js
control: Circular Gauge
documentation: ug
---

#  Ranges and Frames

Ranges are used to specify or group the scale values. By using ranges, you can describe the values in the pointers. 

**Add range collection**

Range collection is directly added to the scale object. Refer the following code example to add range collection in a **Gauge** control. 



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ showRanges: true

                           ranges:[{

                                       startValue:20,

                                       endValue:80

                            }]

                }]

            })

        });

&lt;/script&gt;



**[View]**

//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                  sc1.ShowRanges(true)

                  .Ranges(ran =>

                  {

                  ran.StartValue(20)

                  .EndValue(80)

                  .BackgroundColor("Green")

                  .Placement(RangePlacement.Far).Add();

                   }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales ShowRanges="true"&gt;

               &lt;RangeCollection&gt;

                   &lt;ej:CircularRanges StartValue="20" EndValue="80" BackgroundColor="green" Placement="far"&gt;

                   &lt;/ej:CircularRanges&gt;

               &lt;/RangeCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;

**Range Customization**

**Appearance**

* The API **size** is used to specify the width of the ranges.  The major attributes for ranges are **startValue** and **endValue**. **startValue** defines the start position of the ranges and **endValue** defines the end position of the ranges. **StartWidth** and **endWidth** are used to specify the range width at the starting and ending position of the ranges. You can add the gradient effects to the ranges by using **gradient** object.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                    $("#CircularGauge1").ejCircularGauge({

                    scales: [{

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    ranges: [{

                        //For setting range start value

                        startValue: 20,

                        //For setting range end value

****endValue: 80,

                        //For setting range background color

****backgroundColor: "Green",

                    **}]**



                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowRanges(true)

                         .ShowScaleBar(true)

                         .Radius(150).Size(5)

                         .Ranges(ran =>

                          {

                         //For setting range start value

                          **ran.StartValue(20)**

                         //For setting range end value

                          **.EndValue(80)**

                          //For setting range background color

                         **.BackgroundColor("Green")**

                         //For setting range placement

                         **.Placement(RangePlacement.Far).Add();**

                         }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

   &lt;ej:CircularGauge runat="server" ID="CircularGauge1"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true"  ShowscaleBar="true" radius="150" Size="5"&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers  Value="0"  length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;labelCollection&gt;

                    &lt;ej:CircularLabels type="major" /&gt;

                &lt;/labelCollection&gt;

                &lt;RangeCollection&gt;

                     &lt;ej:CircularRanges StartValue="20" endValue="80" BackgroundColor="green" Placement="far"&gt;

                     &lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img1.png" Caption="Figure 53: Circular Gauge with customized ranges with startValues and endValues"%}

**Colors and Border**

* By customizing the ranges, the appearance of the **Gauge** can be improved. The range border is modified with the object called **border**. It has two border property such as **color** and **width** that are used to customize the border color of the ranges and border width of the ranges. You can set the background color to improve the look and feel of the **Circular Gauge**. For customizing the background color of the ranges, **backgroundColor** is used.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                    $("#CircularGauge1").ejCircularGauge({

                    scales: [{

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    ranges: [{

                        //For setting range start value

                        startValue: 20,

                        //For setting range end value

****endValue: 80,

                        //For setting range background color

****backgroundColor: "yellow",

                        //For setting range border

****border:{color:"green",width:2},

                    **}]**



                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowRanges(true)

                         .ShowScaleBar(true)

                         .Radius(150).Size(5)

                         .Ranges(ran =>

                          {

                          //For setting range start value

                          **ran.StartValue(20)**

                          //For setting range end value

                          **.EndValue(80)**

                          //For setting range background color

                          **.BackgroundColor("Yellow")**

                          //For setting range placement

                          **.Placement(RangePlacement.Far)**

                          //For setting range border

                          **.Border(bo =>bo.Width(2).Color("Green")).Add();**

                          }).Add();

                 })

)



**[ASP]**

&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="CircularGauge1"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true"  ShowscaleBar="true" radius="150" Size="2"&gt;

        &lt;%--For setting range start value,end value,background color and border color--%&gt;

                &lt;RangeCollection&gt;

                     &lt;ej:CircularRanges StartValue="20" endValue="80" BackgroundColor="yellow" Placement="far"&gt;

                         &lt;Border Color="green" Width="2" /&gt;

                     &lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img2.png" Caption="Figure 54: Circular Gauge with customized range colors and borders"%}

**Position the ranges**

You can position ranges using two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and range.  **Placement** property is used to locate the pointer with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type. 



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                    $("#CircularGauge1").ejCircularGauge({

                    scales: [{

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    ranges: [{

                        //For setting range start value

                        startValue: 0,

                        //For setting range end value

****endValue: 100,

                        //For setting range background color

****backgroundColor: "Green",

                        //For setting range placement

                        **placement: "far",**

                        //For setting distance between scale and ranges

                        **distanceFromScale: -30,**

                        //For setting range border

****border:{color:"Black",width:2},

                    **}]**



                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowRanges(true)

                         .ShowScaleBar(true)

                         .Radius(150).Size(2)

                         .Ranges(ran =>

                          {

                         //For setting range start value

                          **ran.StartValue(0)**

                          //For setting range end value

                         **.EndValue(100)**

                           //For setting range background color

                          **.BackgroundColor("Green")**

                           //For setting range placement

                           **.Placement(RangePlacement.Far)**

                          //For setting distance between scale and ranges

                          **.DistanceFromScale(-30)**

                           //For setting range border

                           **.Border(bo =>bo.Width(2).Color("Black")).Add();**

                          }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="CircularGauge1"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true"  ShowscaleBar="true" radius="150" Size="2"&gt;

&lt;%--For setting range start value,end value,distance between scale and ranges--%&gt;

                &lt;RangeCollection&gt;

                     &lt;ej:CircularRanges StartValue="0" endValue="100" BackgroundColor="green" Placement="far" DistanceFromScale="-30"&gt;

                         &lt;Border width="2" Color="black" /&gt;

                     &lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img3.png" Caption="Figure 55: Circular Gauge with customized ranges"%}

**Multiple Ranges**

You can set multiple ranges by adding an array of ranges objects. Refer the following code example for multiple ranges functionality.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    pointers: [{

                        value: 40,

                        showBackNeedle: true,

                        length: 100

                    }],

                    ranges: [

                    //For setting range1

                    {

                        startValue: 0, endValue: 50,

                        backgroundColor: "Green",

                        placement: "far", distanceFromScale: -30

                    },

                    //For setting range2

                    {

                        startValue: 50, endValue: 80,

                        backgroundColor: "yellow",

                        placement: "far", distanceFromScale: -30

                    },

                    //For setting range3

                    {

                        startValue: 80, endValue: 100,

                        backgroundColor: "red",

                        placement: "far", distanceFromScale: -30

                    }]



                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                    sc1.ShowRanges(true)

                       .ShowScaleBar(true)

                       .Radius(150).Size(2)

                       .Pointers(p =>

                        {

                         p.Value(40)

                        .ShowBackNeedle(true)

                        .Length(100).Add();

                        })

                       .Ranges(ran =>

                        {

                        //For setting range1

                        ran.StartValue(0)

                        .EndValue(50)

                        .BackgroundColor("Green")

                        .Placement(RangePlacement.Far)

                        .DistanceFromScale(-30).Add();

                        //For setting range2

                        ran.StartValue(50)

                        .EndValue(80)

                        .BackgroundColor("Yellow")

                        .Placement(RangePlacement.Far)

                        .DistanceFromScale(-30).Add();

                        //For setting range3

                         ran.StartValue(80)

                        .EndValue(100)

                        .BackgroundColor("Red")

                        .Placement(RangePlacement.Far)

                        .DistanceFromScale(-30).Add();

                         }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

    &lt;ej:CircularGauge runat="server" ID="CircularGauge1"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true"  ShowscaleBar="true" radius="150" Size="2" Maximum="100"&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers  Value="40" showbackneedle="true" length="100"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;RangeCollection&gt;

&lt;%--For setting range1--%&gt;

                     &lt;ej:CircularRanges StartValue="0" endValue="50" BackgroundColor="green" Placement="far" DistanceFromScale="-30"&gt;&lt;/ej:CircularRanges&gt;

&lt;%--For setting range2 --%&gt;

                     &lt;ej:CircularRanges StartValue="50" endValue="80" BackgroundColor="yellow" Placement="far" DistanceFromScale="-30"&gt; &lt;/ej:CircularRanges&gt;

&lt;%--For setting range3--%&gt;

                     &lt;ej:CircularRanges StartValue="80" endValue="100" BackgroundColor="red" Placement="far" DistanceFromScale="-30"&gt;&lt;/ej:CircularRanges&gt; 

                &lt;/RangeCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img4.png" Caption="Figure 56: Circular Gauge with multiple ranges"%}

**Frames**

* Frame is the element that decides the appearance of the **Circular Gauge**. You can customize it using the object called **frame**.  It has the properties such as frameType, backGroundUrl, halfCircleFrameStartAngle and halfCircleFrameEndAngle. **frameType** is used to specify whether frame is a half circle frame or full circle frame. **halfCircleFrameStartAngle** and **halfCircleFrameEndAngle** are used to specify the angle for **Gauge** with frame type as half circle. **backgroundUrl** is used to set the background image for the frame.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1").ejCircularGauge({

                frame: {

                    //For setting type

**frameType: "halfcircle",**

                    //For setting half circle frame start angle

                    **halfCircleFrameStartAngle: 205,**

****//For setting half circle frame end angle

                    **halfCircleFrameEndAngle: 335,**

                },pointerCap:{radius:50},

                backgroundColor: "#FFCCCC",

                scales: [{

                    startAngle: 180, sweepAngle: 180,

                    pointers: [{

                        needleType: "rectangle",

                        width: 1, length: 120, value: 40

                    }]

                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

         .Frame(f =>

         {

         //For setting type

         **f.FrameType(Frame.HalfCircle)**

         //For setting half circle frame start angle

         **.HalfCircleFrameStartAngle(205)**

         //For setting half circle frame end angle

         **.HalfCircleFrameEndAngle(335).ToString();**

         })

         .BackgroundColor("#FFCCCC")

         .Scales(sc =>

         {

          sc.StartAngle(180)

         .SweepAngle(180)

         .PointerCap(pc =>pc.Radius(8))

         .Pointers(po =>

         {

          po.NeedleType(NeedleType.Rectangle)

          .Width(1).Length(120)

          .Value(40).Add();

          }).Add();

         })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

    &lt;ej:CircularGauge runat="server" ID="CircularGauge1" backgroundColor="#FFCCCC"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales startAngle="180" SweepAngle="180"&gt;

              &lt;PointerCap Radius="8" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers  type="Needle" needleType="Rectangle" Value="40" width="1" length="120"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

&lt;%--For setting halfcircle frame start angle and end angle--%&gt;

            &lt;Frame FrameType="HalfCircle" HalfCircleFrameStartAngle="205" HalfCircleFrameEndAngle="335" /&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img5.png" Caption="Figure 57: Circular Gauge with multiple ranges"%}

## Adding Range Collection

Range collection is directly added to the scale object. Refer the following code example to add range collection in a **Gauge** control. 



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{ showRanges: true,
ranges:[{
startValue:20,
endValue:80
}]
}]
})
});
</script>


{% endhighlight %}



**Range Customization**

**Appearance**

* The API **size** is used to specify the width of the ranges.  The major attributes for ranges are **startValue** and **endValue**. **startValue** defines the start position of the ranges and **endValue** defines the end position of the ranges.

* **StartWidth** and **endWidth** are used to specify the range width at the starting and ending position of the ranges. You can add the gradient effects to the ranges by using **gradient** object.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
ranges: [{
//For setting range start value
startValue: 20,
//For setting range end value
endValue: 80,
//For setting range background color
backgroundColor: "Green",
**}]**

}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img6.png" Caption="Figure 53: Circular Gauge with customized ranges with startValues and endValues"%}

**Colors and Border**

* By customizing the ranges, the appearance of the **Gauge** can be improved. The range border is modified with the object called **border**. It has two border property such as **color** and **width.** These are used to customize the border color of the ranges and border width of the ranges. 

* You can set the background color to improve the look and feel of the **Circular Gauge**. For customizing the background color of the ranges, **backgroundColor** is used.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
ranges: [{
//For setting range start value
startValue: 20,
//For setting range end value
endValue: 80,
//For setting range background color
backgroundColor: "yellow",
//For setting range border
border:{color:"green",width:2},
**}]**

}]
});});
</script>


{% endhighlight %}









Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img7.png" Caption="Figure 54: Circular Gauge with customized range colors and borders"%}





**Position the ranges**

* You can position ranges using two properties such as **distanceFromScale** and **placement**. 

* **distanceFromScale** property defines the distance between the scale and range. 

* **Placement** property is used to locate the pointer with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
ranges: [{
//For setting range start value
startValue: 0,
//For setting range end value
endValue: 100,
//For setting range background color
backgroundColor: "Green",
//For setting range placement
**placement: "far",**
//For setting distance between scale and ranges
**distanceFromScale: -30,**
//For setting range border
border:{color:"Black",width:2},
**}]**

}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img8.png" Caption="Figure 55: Circular Gauge with customized ranges"%}



## Multiple Ranges

You can set multiple ranges by adding an array of ranges objects. Refer the following code example for multiple ranges functionality.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
pointers: [{
value: 40,
showBackNeedle: true,
length: 100
}],
ranges: [
//For setting range1
{
startValue: 0, endValue: 50,
backgroundColor: "Green",
placement: "far", distanceFromScale: -30
},
//For setting range2
{
startValue: 50, endValue: 80,
backgroundColor: "yellow",
placement: "far", distanceFromScale: -30
},
//For setting range3
{
startValue: 80, endValue: 100,
backgroundColor: "red",
placement: "far", distanceFromScale: -30
}]

}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img9.png" Caption="Figure 56: Circular Gauge with multiple ranges"%}



## Frames

* Frame is the element that decides the appearance of the **Circular Gauge**. You can customize it using the object called **frame**.  It has the properties such as frameType, backGroundUrl, halfCircleFrameStartAngle and halfCircleFrameEndAngle.

* **frameType** is used to specify whether frame is a half circle frame or full circle frame. **halfCircleFrameStartAngle** and **halfCircleFrameEndAngle** are used to specify the angle for **Gauge** with frame type as half circle. **backgroundUrl** is used to set the background image for the frame.









{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
frame: {
//For setting type
**frameType: "halfcircle",**
//For setting half circle frame start angle
**halfCircleFrameStartAngle: 205,**
//For setting half circle frame end angle
**halfCircleFrameEndAngle: 335,**
},pointerCap:{radius:50},
backgroundColor: "#FFCCCC",
scales: [{
startAngle: 180, sweepAngle: 180,
pointers: [{
needleType: "rectangle",
width: 1, length: 120, value: 40
}]
}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-ranges-and-frames_images\-ranges-and-frames_img10.png" Caption="Figure 57: Circular Gauge with multiple ranges"%}



