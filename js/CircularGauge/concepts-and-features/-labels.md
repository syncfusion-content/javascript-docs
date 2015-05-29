---
layout: post
title: -labels
description:  labels
platform: js
control: Circular Gauge
documentation: ug
---

#  Labels

**Labels** are units that are used to display the values in the scales. You can customize Labels with the properties like angle, color, font, opacity, etc.

**Add label collection** 

**Label collection** is directly added to the scale object. Refer the following code example to add label collection in a **Gauge**.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ 

                           labels:[{

                                       angle:30

                            }]

                }]

            })

        });

&lt;/script&gt;



**[View]**

****

//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                {

                    sc1.Labels(lb =>

                        {

                        // For setting label angle

                        lb.Angle(30).Add();

                        }).Add();                   

                })

)





**[ASP]**

****

&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales&gt;

                &lt;labelCollection&gt;

                    &lt;ej:CircularLabels Angle="30"&gt;&lt;/ej:CircularLabels&gt;

                &lt;/labelCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;



**Label Customization**

**Appearance**

* The****attribute **angle** is used to display the labels in the specified angles and **color** attribute is used to display the labels in specified color. You can adjust the opacity of the label with the property **opacity** and the values of it lies between 0 and 1.

* You can adjust the labels based on the tick’s direction by setting **autoAngle** as true. **includeFirstValue** is an special property especially used in some special scenarios such as in clock, where the value 0 needs to be replaced with that of 12. By enabling this property the first value of the label is not rendered.

Font option is also available on the labels. The basic three properties of fonts such as size, family and style can be achieved by **size**, **fontStyle** and **fontFamily**. Labels are two types such as major and minor.

Major types labels are for major interval values and minor types labels are for minor interval values.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showScaleBar: true,

                    backgroundColor: "#FAF4B5",

                    border: { width: 2, color: "Yellow" },

                    width: 10, radius: 110,

                    pointers: [{

                        border: { color: "Yellow", width: 2 },

                        backgroundColor: "#FAF4B5",

                        value: 40, length: 80,

                        width: 16,: 0.6

                    }],

                    labels: [{

                        // For setting label angle

                        **angle:10,**

                        // For setting label opacity

                        **opacity:0.8,** 

                        // For disable the include first value prperty

                        **includeFistValue: false,**

                        // For setting label color

                        **color: "Yellow",**

                        // For setting label font

                        **font:{size: "15px",**

                            **fontFamily: "Arial",**

                            **fontStyle: "bold"}**

                    }]

                }]

            });});

&lt;/script&gt;



**[View]**

   // For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

                  .Scales(sc1 =>

                     {

                   sc1.ShowScaleBar(true)

                  .BackgroundColor("#FAF4B5")

                  .Border(bo =>bo.Color("Yellow").Width(2))

                  .Radius(110)

                  .Size(10)

                  .Pointers(po =>

                   {

                   po.Border(bo =>bo.Width(2).Color("Yellow"))

                   .BackgroundColor("#FAF4B5")

                   .Value(40).Length(80)

                   .Width(16).Opacity(0.6).Add();

                        })

                   .Labels(lb =>

                      {

                    // For setting label angle

                    **lb.Angle(30)**

                    // For setting label opacity

                   **.Opacity(0.8)**

                   // For disable the include first value property

                   **.IncludeFirstValue(false)**

                   // For setting label color

                   **.Color("Yellow")**

                   // For setting label font

                   .**Font(f =>f.Size("15px").FontFamily("Arial").FontStyle("bold")).Add();**

                    }).Add();

              })

)



**[ASP]**



   &lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowscaleBar="true" BackgroundColor="#FAF4B5" Size="10" radius="110"&gt;

              &lt;Border Width="2" Color="yellow" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="40" length="80" width="16" Opacity="0.6" BackgroundColor="#FAF4B5" &gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

&lt;%--For setting includefirst value,label color--%&gt;

                &lt;labelCollection&gt;

                    &lt;ej:CircularLabels Angle="10" Opacity="0.8" IncludeFirstValue="false" color="yellow"&gt;

                    &lt;Font Size="15px" FontFamily="arial" FontStyle="bold"&gt;&lt;/Font&gt;

                    &lt;/ej:CircularLabels&gt;

                &lt;/labelCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img1.png" Caption="Figure 46: Circular Gauge with customized label"%}

**Unit text and Position**

* **unitText** is used to add some text along with the labels. For example, in speedometer, you need to mention the units in kmph. You can also add the unit text in front of the labels. You can achieve this using an enumerable property **unitTextPosition**. By this you can position the unit text in front or back.

* Labels can be positioned with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and labels.  Placement property is used to locate the labels with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

         $("#CircularGauge1").ejCircularGauge({

                scales: [{showRanges: true,

                    showScaleBar: true,

                    radius: 150,size:2,

                    pointers: [{

                        value: 40,

                        showBackNeedle: true,

                        length: 100

                    }],

                    labels: [{                        

                        // For setting unit text

**unitText: "kmpH",**

                        // For setting unit text position

                        **unitTextPosition: "back"**

                    }],

                    ranges: [{ startValue: 0, endValue: 50, backgroundColor: "Green",placement:"far",distanceFromScale:-30 },

                    { startValue: 50, endValue: 80, backgroundColor: "yellow", placement: "far", distanceFromScale: -30 },

                    { startValue: 80, endValue: 100, backgroundColor: "red", placement: "far", distanceFromScale: -30 }]



                }]

            });});

&lt;/script&gt;



**[view]**



// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

.Scales(sc1 =>

     {

  sc1.ShowRanges(true)

         .ShowScaleBar(true)

         .Radius(150).Size(2)

         .Pointers(po =>

          {

         po.Value(40).Length(100)

        .ShowBackNeedle(true).Add();

           })

          .Labels(lb =>{

          // For setting unit text

          **lb.UnitText("kmph")**

          // For setting unit text position

          **.UnitTextPosition(UnitTextPlacement.Back).Add();**                                              })

         .Ranges(ran =>

            {

          ran.DistanceFromScale(-30).StartValue(0).EndValue(50).BackgroundColor("Green").Placement(RangePlacement.Far).Add();

         ran.DistanceFromScale(-30).StartValue(50).EndValue(80).BackgroundColor("Yellow").Placement(RangePlacement.Far).Add();

         ran.DistanceFromScale(-30).StartValue(80).EndValue(100).BackgroundColor("Red").Placement(RangePlacement.Far).Add();

            }).Add();

        })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true" ShowscaleBar="true"  Size="2" radius="150"&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="40" showbackneedle="true" length="100"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;labelCollection&gt;

&lt;%--For setting unit text and unit text position--%&gt;

                    &lt;ej:CircularLabels unittext="kmpH" UnitTextPosition="back"&gt;

                    &lt;Font Size="15px" FontFamily="arial" FontStyle="bold"&gt;&lt;/Font&gt;

                    &lt;/ej:CircularLabels&gt;

                &lt;/labelCollection&gt;

                &lt;RangeCollection&gt;

                    &lt;ej:CircularRanges StartValue="0" EndValue="50" backgroundColor="green" Placement="far" DistanceFromScale="-30"&gt;&lt;/ej:CircularRanges&gt;

                     &lt;ej:CircularRanges StartValue="50" EndValue="80" backgroundColor="yellow" Placement="far" DistanceFromScale="-30"&gt;&lt;/ej:CircularRanges&gt;

                     &lt;ej:CircularRanges StartValue="80" EndValue="100" backgroundColor="red" Placement="far" DistanceFromScale="-30"&gt;&lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img2.png" Caption="Figure 47: Circular Gauge with unit text"%}

**Multiple labels**

You can achieve multiple labels such as minor and major in a sample scale of a **Gauge**. Refer the following code example for multiple labels variation.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showRanges: true, minorIntervalValue: 5,

                    backgroundColor: "yellow",

                    border: { width: 1.5, color: "Red" },

                    showScaleBar: true, radius: 150, size: 5,

                    pointerCap: {

                        backgroundColor: "yellow",

                        borderColor: "Red", borderWidth: 1.5

                    },

                    labels: [

                        // For setting label1

                             { type: "minor", color: "yellow" }, 

                        // For setting label2

                             { type: "major", color: "Red" }],

                    pointers: [{

                        backgroundColor: "yellow",

                        border: { width: 1.5, color: "Red" },

                        length: 110

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

                        .Radius(150)

                        .Size(5)

                        .MinorIntervalValue(5)

                        .BackgroundColor("Yellow")

                        .Border(bo =>bo.Width(1.5).Color("Red"))

                        .PointerCap(pc => pc.BackgroundColor("Yellow").BorderColor("Red").BorderWidth(0.5).Radius(10))

                        .Labels(lb =>

                              {

                        // For setting label1

                        lb.Type(GaugeTypes.Minor).Color("Yellow").Add();

                        // For setting label2

                        lb.Type(GaugeTypes.Major).Color("Red").Add();

                               })

                       .Pointers(po =>

                               {

                        po.Length(110)

                       .BackgroundColor("Yellow")

                       .Border(bo =>bo.Width(1.5).Color("Red")).Add();

                          })

                       .Add();

                        })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true" MinorIntervalValue="5" majorintervalvalue="10" backgroundColor="yellow" ShowscaleBar="true"  Size="5" radius="150"&gt;

              &lt;PointerCap BackgroundColor="yellow" borderColor="red" BorderWidth="0.5" Radius="10"&gt;&lt;/PointerCap&gt;

              &lt;Border Width="1.5" Color="red" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers BackgroundColor="yellow" length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;labelCollection&gt;

&lt;%--For setting label1--%&gt;                

                    &lt;ej:CircularLabels type="minor" Color="yellow" /&gt;

&lt;%--For setting label2--%&gt;                

                    &lt;ej:CircularLabels type="major" Color="red" /&gt;

                &lt;/labelCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img3.png" Caption="Figure 48: Circular Gauge with multiple labels"%}

## Adding Label Collection 

**Label collection** is directly added to the scale object. Refer the following code example to add label collection in a **Gauge**.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
labels:[{
angle:30
}]
}]
})
});
</script>


{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img4.png" Caption="        Figure 46(a): Circular Gauge with  label collection"%}



## Label Customization

**Appearance**

* The****attribute **angle** is used to display the labels in the specified angles and **color** attribute is used to display the labels in specified color. You can adjust the opacity of the label with the property **opacity** and the values of it lies between 0 and 1.

* You can adjust the labels based on the tick’s direction by setting **autoAngle** as true. **includeFirstValue** is an special property especially used in some special scenarios such as in clock, where the value 0 needs to be replaced with that of 12. By enabling this property the first value of the label is not rendered.

* Font option is also available on the labels. The basic three properties of fonts such as size, family and style can be achieved by **size**, **fontStyle** and **fontFamily**. Labels are two types such as major and minor.Major types labels are for major interval values and minor types labels are for minor interval values.





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true,
backgroundColor: "#FAF4B5",
border: { width: 2, color: "Yellow" },
width: 10, radius: 110,
pointers: [{
border: { color: "Yellow", width: 2 },
backgroundColor: "#FAF4B5",
value: 40, length: 80,
width: 16,
opacity: 0.6
}],
labels: [{
// For setting label angle
**angle:10,**
// For setting label opacity
**opacity:0.8,**
// For disable the include first value prperty
**includeFistValue: false,**
// For setting label color
**color: "Yellow",**
// For setting label font
**font:{size: "15px",**
**fontFamily: "Arial",**
**fontStyle: "bold"}**
}]
}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img5.png" Caption="Figure 46(b): Circular Gauge with customized label"%}



**Unit text and Position**

* **unitText** is used to add some text along with the labels. For example, in speedometer, you need to mention the units in kmph. You can also add the unit text in front of the labels. You can achieve this by using an enumerable property **unitTextPosition**. With this you can position the unit text in front or back.

* Labels can be positioned with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and labels.  Placement property is used to locate the labels with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{showRanges: true,
showScaleBar: true,
radius: 150,size:2,
pointers: [{
value: 40,
showBackNeedle: true,
length: 100
}],
labels: [{
// For setting unit text
**unitText: "kmpH",**
// For setting unit text position
**unitTextPosition: "back"**
}],
ranges: [{ startValue: 0, endValue: 50, backgroundColor: "Green",placement:"far",distanceFromScale:-30 },
{ startValue: 50, endValue: 80, backgroundColor: "yellow", placement: "far", distanceFromScale: -30 },
{ startValue: 80, endValue: 100, backgroundColor: "red", placement: "far", distanceFromScale: -30 }]

}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img6.png" Caption="Figure 47: Circular Gauge with unit text"%}



## Multiple Labels

You can achieve multiple labels such as minor and major in a **Gauge** sample scale. Refer the following code example for multiple labels variation.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showRanges: true, minorIntervalValue: 5,
backgroundColor: "yellow",
border: { width: 1.5, color: "Red" },
showScaleBar: true, radius: 150, size: 5,
pointerCap: {
backgroundColor: "yellow",
borderColor: "Red", borderWidth: 1.5
},
labels: [
// For setting label1
{ type: "minor", color: "yellow" },
// For setting label2
{ type: "major", color: "Red" }],
pointers: [{
backgroundColor: "yellow",
border: { width: 1.5, color: "Red" },
length: 110
}]
}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\-labels_images\-labels_img7.png" Caption="Figure 48: Circular Gauge with multiple labels"%}



