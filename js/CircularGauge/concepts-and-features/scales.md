---
layout: post
title: scales
description: scales
platform: js
control: Circular Gauge
documentation: ug
---

# Scales

**Scales** are the basic functional block of the **Circular Gauge**. By customizing the scales, the appearance of the **Gauge** can be improved. The functional blocks of Circular Gauge are 

* Pointers

* Labels

* CustomLabels

* Indicators

* Ticks

* Ranges

* Subgauges.

**Add scale collection**

**Scale collection** is directly added to the **Gauge** object. Refer the following code example to add scale collection in **Gauge** control.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ 

                           radius:50

                }]

            })

        });

&lt;/script&gt;



**[View]**



//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

             .Scales(SC =>

             {

              SC.Radius(130).Add();

             })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;     

&lt;ej:CircularGauge runat="server" Id="CircularGauge1"&gt;

            &lt;Scales&gt;

            &lt;ej:CircularScales  Radius="130"&gt;

            &lt;/ej:CircularScales&gt;

            &lt;/Scales&gt;

        &lt;/ej:CircularGauge&gt;

**Scale Customization**

**Colors and Border**

* The Scale border is modified with the object called **border**. It has two border property namely **color** and **width** that are used to customize the border color of the scale and border width of the scale. Setting the background color improves the look and feel of the **Circular Gauge**. You can customize the background color of the scale using **backgroundColor**. 


**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ 

                    showScaleBar: true,

                    radius:110,

                    backgroundColor: "Red",

                    border: {

                        //For scale border color  

                        color: "Blue",

                        //For scale border width  

                        width: 3

                    },

                    pointers: [{length:80}]

                }]

            })

        });&lt;/script&gt;



**[View]**



//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

          .Scales(SC =>

                 {

           SC.Radius(130)

           .BackgroundColor("Red")

           .ShowScaleBar(true)

           .Border(b =>{

          //For scale border width

          b.Width(3)

          //For scale border color

          .Color("Blue");

          })

          .Pointers(po =>

          {

          po.Length(80).Add();

          }).Add();

         })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales ShowScaleBar="true" Radius="110" BackgroundColor="Red"&gt;

&lt;%--For setting scale border width and color--%&gt;

           &lt;Border Width="3" Color="blue" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Length="80"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img1.png" Caption="Figure 37: Circular Gauge with customized scale border"%}

**Pointer Cap**

* **Pointer cap** is a circular shape element that is located at the center of the **Circular Gauge**. The pointer cap is one of the cynosures of the **Circular Gauge**. By customizing the pointer cap, Gauge style is improved. The pointer cap is modified with the object **pointerCap**. It contains radius, borderColor, bordrWidth, interiorGradient and backgroundColor properties. The property **radius** is used to set the radius for the pointer cap. **interiorGradient** is used to provide the gradient effects to the pointer cap.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



        // For Circular Gauge rendering

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ **pointerCap: {**

****// For setting pointer cap radius

                           **radius:10,**

****// For setting pointer cap border width

                           **borderWidth: 4,**

****// For setting pointer cap border color

                           **borderColor: "Blue",**

****// Fors etting pointer cap background color

                           **backgroundColor: "Red"** 

                         }}]                            

             })

 });

&lt;/script&gt;



**[View]**



//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

           .Scales(SC =>

            {

            SC.PointerCap(pc =>

                      {

            //For setting pointer cap radius

             pc.Radius(10)

            // For setting pointer cap border width

            .BorderWidth(4)

            // For setting pointer cap border color

            .BorderColor("Blue")

            // For setting pointer cap background

            .BackgroundColor("Red");

             }).Add();

          })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales ShowScaleBar="true" Radius="110" BackgroundColor="Red"&gt;

&lt;%--For setting scale border width and color--%&gt;

           &lt;Border Width="3" Color="blue" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Length="80"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;







Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img2.png" Caption="Figure 38: Circular Gauge with customized pointer cap"%}

**Appearance**

**Circular Gauge** contains two types of scale direction such as clockwise and counter clockwise. You can set them by enumerable property called **direction**. And you can set the minimum and maximum values for the scale with the properties **minimum** and **maximum**. The two properties **minorIntervalValue** and **majorIntervalValue** are the values used to set interval value for the ticks and labels. The **radius** property is used to set the radius value for the circular scale and the **size** property is used to set the scale bar width. You can also adjust the Opacity of the scale with the property **opacity**. The value for opacity lies between 0 and 1. You can also give some shadow effects for the scale by using the property **shadowOffset.** The property **startAngle** is used to set starting position of the scale at certain angle and **sweepAngle** is used to shrink or expand the scale to certain angle. 



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

scales: [{

// For setting scale bar size

**size: 30,**

// For setting scale radius

**scaleRadius: 130,** 

// For setting scale minimum value

**minimum: 20,** 

// For setting scale maximum value

**maximum: 120,** 

// For setting scale major interval value

**majorIntervalValue: 20,** 

// For setting scale minor interval

**minorIntervalValue: 5,** 

// For setting scale direction

      **direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,**

// For setting scale background color****

      **backgroundColor:"red",**

// For setting scale bar opacity

**opcity:0.5,**

// For setting scale bar shadow offset

**shadowOffset: 20**

             }]

});



 });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

.Scales(sc =>

{

// For setting scale bar size

sc.Size(30)

// For setting scale minimum value

.Minimum(20)

// For setting scale maximum value

.Maximum(120)

// For setting scale major interval value

.MajorIntervalValue(20)

// For setting scale minor interval

.MinorIntervalValue(5)

// For setting scale background color

.BackgroundColor("Red")

// For setting scale bar opacity

.Opacity(0.5)

// For setting scale bar shadow offset

.ShadowOffset(20)

// For setting scale direction

.Direction(Directions.CounterClockwise).Add();

})

)





**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

      &lt;%--For setting scale bar size,scale radius,minimum value,maximum value,majorinterval value,minorinterval value and direction--%&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales Size="30" BackgroundColor="red" opacity="0.5" ShadowOffset="20" minimum="20" Maximum="120" MajorIntervalValue="20" MinorIntervalValue="5" Direction="CounterClockwise"&gt;

         &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img3.png" Caption="Figure 39: Circular Gauge with customized scale values"%}

**Enable/Disable properties**

You can enable / disable properties in Circular Gauge using some properties in scale collection. The **showIndicators** property is used to enable/disable the indicators. **ShowLabels**, **showTicks**, **showRanges**, **showPointers** ans **showScaleBar** are used to enable/ disable labels, ticks, ranges, pointers and scale bar respectively. 

**Multiple scales**

You can set **Multiple scales** for a single **Circular Gauge** control by using an array of scale objects. Each scale object is independent of each other. The following code example refers to two scale objects in a **Gauge**.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

scales: [

// For setting scale1

{

size: 30,

scaleRadius: 130, 

minimum: 20, 

maximum: 120, 

majorIntervalValue: 20, 

minorIntervalValue: 5,

      direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,

opcity:0.5,

shadowOffset: 20

       },

// For setting second scale

 {

size: 10,

scaleRadius: 80, 

majorIntervalValue: 10, 

minorIntervalValue: 2,

direction:ej.datavisualization.CircularGauge.Directions.Clockwise, 

opcity:0.5,

shadowOffset: 5

       }]

});



 });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

              .Scales(sc =>

                        {

              // For setting  first scale

              sc.ShowScaleBar(true)

                .Size(10)

                .Radius(150)

                .Minimum(20)

                .Maximum(120)

                .MajorIntervalValue(20)

                .MinorIntervalValue(5)

                .Pointers(p => { p.Length(120).Value(50).Add(); })

                .Direction(Directions.Clockwise)

                .ShadowOffset(20).Add();

                // For setting second scale

                sc.Size(10)

                .ShowScaleBar(false)

                .Radius(80)

                .MajorIntervalValue(10)

                .Labels(lb =>lb.DistanceFromScale(-40).Color("Red").Add())

                .Ticks(t =>t.Color("Red").Add())

        .Pointers(p => { p.Length(50).Value(40).DistanceFromScale(-30).Add();                     })

                 .Direction(Directions.CounterClockwise)

                 .Opacity(0.5)

                 .ShadowOffset(5).Add();

                  })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

&lt;%--For setting scale1 --%&gt;

          &lt;ej:CircularScales ShowScalebar="true" Size="10" radius="150" ShadowOffset="20" minimum="20" Maximum="120" MajorIntervalValue="20" MinorIntervalValue="5" Direction="Clockwise"&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="50" ShowBackNeedle="true" Length="120" Width="7" BackNeedleLength="0"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;

&lt;%--For setting scale2 --%&gt;



          &lt;ej:CircularScales ShowScalebar="false" Size="10" radius="80" opacity="0.5" ShadowOffset="5" MajorIntervalValue="10"  Direction="CounterClockwise"&gt;

                &lt;labelCollection&gt;

                   &lt;ej:CircularLabels DistanceFromScale="-40" Color="red"&gt;&lt;/ej:CircularLabels&gt;

                &lt;/labelCollection&gt;

                &lt;TickCollection&gt;

                   &lt;ej:CircularTicks Color="red"/&gt;

                &lt;/TickCollection&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="40" distanceFromScale="-30" Length="50"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

         &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;







Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img4.png" Caption="Figure 40: Circular Gauge with multiples scales"%}

## Adding Scale Collection

**Scale collection** is directly added to the **Gauge** object. Refer the following code example to add scale collection in **Gauge** control.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
radius:130
}]
})
});
</script>


{% endhighlight %}









Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img5.png" Caption="Figure 37(a): Circular Gauge with scale radius."%}



## Scale Cutomization

**Colors and Border**

* The Scale border is modified with the object called **border**. It has two border property namely **color** and **width** which are used to customize the border color of the scale and border width of the scale. 

* Setting the background color improves the look and feel of the **Circular Gauge**. You can customize the background color of the scale using **backgroundColor**. 


{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true,
radius:110,
backgroundColor: "Red",
border: {
//For scale border color
color: "Blue",
//For scale border width
width: 3
},
pointers: [{length:80}]
}]
})
});</script>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img6.png" Caption="Figure 37(b): Circular Gauge with customized scale border"%}

**Pointer Cap**

* **Pointer cap** is a circular shape element that is located at the center of the **Circular Gauge**. The pointer cap is one of the cynosure of the **Circular Gauge**. By customizing the pointer cap, Gauge style is improved. The pointer cap is modified with the object **pointerCap**. 

* It contains radius, borderColor, bordrWidth, interiorGradient and backgroundColor properties. The property **radius** is used to set the radius for the pointer cap. **interiorGradient** is used to provide the gradient effects to the pointer cap.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{ **pointerCap: {**
// For setting pointer cap radius
**radius:10,**
// For setting pointer cap border width
**borderWidth: 4,**
// For setting pointer cap border color
**borderColor: "Blue",**
// Fors etting pointer cap background color
**backgroundColor: "Red"**
}}]
})
});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img7.png" Caption="Figure 38: Circular Gauge with customized pointer cap"%}



**Appearance**

* **Circular Gauge** contains two types of scale direction such as clockwise and counter clockwise. You can set them by enumerable property called **direction**. And you can set the minimum and maximum values for the scale with the properties **minimum** and **maximum**. The two properties **minorIntervalValue** and **majorIntervalValue** are the values used to set interval value for the ticks and labels. 

* The **radius** property is used to set the radius value for the circular scale and the **size** property is used to set the scale bar width. You can also adjust the Opacity of the scale with the property **opacity**. The value for opacity lies between 0 and 1. You can also give some shadow effects for the scale by using the property **shadowOffset.** The property **startAngle** is used to set starting position of the scale at certain angle and **sweepAngle** is used to shrink or expand the scale to certain angle. 





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
// For setting scale bar size
**size: 30,**
// For setting scale radius
**scaleRadius: 130,**
// For setting scale minimum value
**minimum: 20,**
// For setting scale maximum value
**maximum: 120,**
// For setting scale major interval value
**majorIntervalValue: 20,**
// For setting scale minor interval
**minorIntervalValue: 5,**
// For setting scale direction
**direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,**
// For setting scale background color
**backgroundColor:"red",**
// For setting scale bar opacity
**opcity:0.5,**
// For setting scale bar shadow offset
**shadowOffset: 20**
}]
});

});
</script>


{% endhighlight %}

















Execute the above code to render the following output.





{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img8.png" Caption="Figure 39: Circular Gauge with customized scale values"%}







**Enable/Disable properties**

You can enable / disable properties in Circular Gauge using some properties in scale collection. The **showIndicators** property is used to enable/disable the indicators. **ShowLabels**, **showTicks**, **showRanges**, **showPointers** ans **showScaleBar** are used to enable/ disable labels, ticks, ranges, pointers and scale bar respectively. 





## Multiple Scales

You can set **Multiple scales** for a single **Circular Gauge** control by using an array of scale objects. Each scale object is independent of each other. The following code example refers to two scale objects in a **Gauge**.





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [
// For setting scale1
{
size: 10,
showScaleBar:true,
scaleRadius: 150,
minimum: 20,
maximum: 120,
majorIntervalValue: 20,
minorIntervalValue: 5,
direction:ej.datavisualization.CircularGauge.Directions.Clockwise,
shadowOffset: 20,
pointers:[{value:50,length:120}]
},
// For setting second scale
{
size: 10,
showScaleBar:false,
scaleRadius: 80,
majorIntervalValue: 10,
direction:ej.datavisualization.CircularGauge.Directions.CounterClockwise,
opcity:0.5,
shadowOffset: 5,
pointers:[{value:40,length:50}],
ticks:[{color:”red”,distanceFromScale:80}],
labels:[{ distanceFromScale:40,color:”red”}]

}]
});

});
</script>


{% endhighlight %}



Execute the above code to render the following output.





{% include image.html url="\js\CircularGauge\concepts-and-features\scales_images\scales_img9.png" Caption="Figure 40: Circular Gauge with multiples scales"%}







