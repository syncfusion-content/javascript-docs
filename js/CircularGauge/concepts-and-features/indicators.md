---
layout: post
title: indicators
description: indicators
platform: js
control: Circular Gauge
documentation: ug
---

# Indicators

Indicators simply indicates the current status of the pointer. Indicators are in several formats such as in shape format, textual format and image format.







**Add indicator collection** 

Indicators collection is directly added to the scale object. Refer the following code to add indicator collection in a **Gauge** control.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ showIndicators: true

                           indicators:[{

                                       value:30

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

                     sc1.ShowIndicators(true)

                        .Indicators(ind =>

                         {

                         ind.Height(10)

                         .Width(10)

                         .Type(IndicatorType.Circle)

                         .Value(0)

                         .Position(pos =>pos.X(185).Y(300)).Add();

                         }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales&gt;

               &lt;IndicatorCollection&gt;

                    &lt;ej:CircularIndicators Height="10" width="10" Type="Circle" Value="0"&gt;

                    &lt;Position X="185" Y="300" /&gt;

                    &lt;/ej:CircularIndicators&gt;

                &lt;/IndicatorCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;

**Basic Customization**

* You can enable indicators by setting **showIndicators** to ‘true’. The **height** and **width** property for the indicators are used to specify the area allocated to the indicator for the width and height respectively. You can use the position collection to position the indicators along **x** and **y** axis. Indicators are of several types such as, dimensions like circle, rectangle, rounded rectangle, text and image. By using the **type** property it can be applied. For image type **imageUrl** property is used. 



**[JavaScript]**

&lt;script type="text/javascript"&gt;

$(function () {



       // For Circular Gauge rendering

                       $("#CircularGauge1").ejCircularGauge({

                scales: [{

**showIndicators: true,** minorIntervalValue: 5,

                    backgroundColor: "#5DF243",

                    border: { width: 1.5, color: "black" },

                    showScaleBar: true, radius: 120, size: 5,

                    pointers: [{

                        backgroundColor: "#5DF243",

                        border: { width: 1.5, color: "black" },

                        length: 110

                    }],

                    indicators: [{

                       // For setting indicator height

**height: 10,**

                       // For setting indicator width

                        **width: 10,**

                       // For setting indicator type

                        **type: "circle",**

                       // For setting indicator value

                        **value: 0,**

                       // For setting indicator position

                        **position: { x: 185, y: 300 },**



                    }],

                }]

            });

});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowIndicators(true)

                         .MinorIntervalValue(5)

                         .BackgroundColor("#5DF243")

                         .Border(bo =>bo.Width(1.5).Color("Black"))

                         .ShowScaleBar(true).Radius(120).Size(5)

                         .Pointers(pc =>

                         {

                          pc.BackgroundColor("#5DF243")

                         .Border(bo =>bo.Width(1.5).Color("Black"))

                         .Length(110).Add();

                         })

                         .Indicators(ind =>

                         {

                        // For setting indicator height

                        **ind.Height(10)**

                        // For setting indicator width

                       **.Width(10)**

                        // For setting indicator type

                       **.Type(IndicatorType.Circle)**

                       // For setting indicator value

                       **.Value(0)**

                       // For setting indicator position

                        **.Position(pos =>pos.X(185).Y(300)).Add();**

                        }).Add();

                 })

)



**[ASP]**

&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales Showindicators="true" backgroundColor="#5DF243" ShowscaleBar="true"  Size="5" radius="120" MinorIntervalValue="5" &gt;

            &lt;Border Width="1.5" Color="black" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers BackgroundColor="#5DF243" length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;labelCollection&gt;

                    &lt;ej:CircularLabels type="major" /&gt;

                &lt;/labelCollection&gt;

                &lt;IndicatorCollection&gt;

                    &lt;ej:CircularIndicators Height="10" width="10" Type="Circle" Value="0"&gt;

                    &lt;Position X="185" Y="300" /&gt;

                    &lt;/ej:CircularIndicators&gt;

                &lt;/IndicatorCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\indicators_images\indicators_img1.png" Caption="Figure 50: Circular Gauge with customized indicator with basic properties"%}

**State Ranges**

* State ranges are used to specify the indicator behavior in the specified region. Use **startValue** and **endValue** to set the range bound for the pointer. Whenever the pointer cross this specified region, the indicator attributes are applied for this ranges. The **backgroundColor** and **borderColor** sets the appearance behavior for the indicators. For text type indicators, **text** can be changed whenever the pointer crossing its state range area, by giving its text values. The basic font options are available for the text in the state range such as size, fontStyle and fontFamily.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

$(function () {



       // For Circular Gauge rendering

                       $("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showIndicators: true, minorIntervalValue: 5,

                    backgroundColor: "#5DF243",

                    border: { width: 1.5, color: "black" },

                    showScaleBar: true, radius: 150, size: 5,

                    pointers: [{

                        backgroundColor: "#5DF243",

                        border: { width: 1.5, color: "black" },

                        length: 110

                    }],

                    indicators: [{

                       // For setting indicator height

                        height: 10,

                       // For setting indicator width

****width: 10,

                       // For setting indicator type

****type: "circle",

                       // For setting indicator value

**** value: 0,

                       // For setting indicator position

****position: { x: 185, y: 300 },

                       // For setting indicator state range collection

                        **stateRanges: [{**

                            // For setting state range end value height

                            **endValue: 100,**

                            // For setting state range start value

                            **startValue: 0,**

                            // For setting indicator background color

                            **backgroundColor: "#5DF243",**

                            // For setting indicator border color

                            **borderColor: "Black",**

                            // For setting indicator text

                            **text: "",**

                            // For setting indicator text color

                            **textColor: "#870505"**

                        }]



                    }],

                }]

            });

});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowIndicators(true)

                         .MinorIntervalValue(5)

                         .BackgroundColor("#5DF243")

                         .Border(bo =>bo.Width(1.5).Color("Black"))

                         .ShowScaleBar(true).Radius(150).Size(5)

                         .Pointers(po =>

                         {

                         po.BackgroundColor("#5DF243")

                        .Border(bo =>bo.Width(1.5).Color("Black"))

                         .Length(110).Add();

                         })

                         .Indicators(ind =>

                         {

                        // For setting indicator height

                        ind.Height(10)

                        // For setting indicator width

                        .Width(10)

                        // For setting indicator type

                        .Type(IndicatorType.Circle)

                        // For setting indicator value

                       .Value(0)

                       // For setting indicator position

                      .Position(pos =>pos.X(185).Y(300))

                       // For setting indicator state range collection

                      **.StateRanges(st =>**

                      {

                       // For setting state range End Value

                       **st.EndValue(100)**

                       // For setting state range start value

                       **.StartValue(0)**

                      // For setting indicator background color

                      **.BackgroundColor("#5DF243")**

                       // For setting indicator border color

                      **.BorderColor("Black")**

                      // For setting indicator text

                      **.Text("")**

                       // For setting indicator text color

                       **.TextColor("#870505").Add();**

                       }).Add();

                       }).Add();

                 })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales Showindicators="true" backgroundColor="#5DF243" ShowscaleBar="true"  Size="5" radius="150" MinorIntervalValue="5" &gt;

            &lt;Border Width="1.5" Color="black" /&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers BackgroundColor="#5DF243" length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;IndicatorCollection&gt;



                    &lt;ej:CircularIndicators Height="10" width="10" Type="Circle" Value="0"&gt;

                    &lt;Position X="185" Y="300" /&gt;

                        &lt;StateRangeCollection&gt; &lt;ej:CircularStateRanges EndValue="100" startValue="0" text="" TextColor="#870505" BackgroundColor="#5DF243" BorderColor="black"&gt;&lt;/ej:CircularStateRanges&gt;&lt;/StateRangeCollection&gt;&lt;%--For setting state range end value,start value,text,text color,background color and bordercolor--%&gt;

                    &lt;/ej:CircularIndicators&gt;

                &lt;/IndicatorCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\indicators_images\indicators_img2.png" Caption="Figure 51: Circular Gauge with customized indicator"%}

**Multiple Indicators**

You can use multiple indicators for a single **Gauge**. Each indicator have a list of state ranges. Refer the following code example for multiple Indicators.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1").ejCircularGauge({

                scales: [{readOnly: false,

                    showIndicators: true,showRanges: true, 

                    minorIntervalValue: 5,

                    showScaleBar: true, radius: 150, size: 5,

                    pointers: [{

                        length: 110,value:70

                    }],

                    ranges: [{

                        startValue: 0, endValue: 50,

                        backgroundColor: "Green",

                        placement: "far", distanceFromScale: -30

                    },

                    {

                        startValue: 50, endValue: 100,

                        backgroundColor: "red",

                        placement: "far", distanceFromScale: -30

                    }],



                    indicators: [

                        //Indicator1

                        {

                        height: 10,

                        width: 10,

                        type: "circle",

                        value: 0,

                        position: { x: 165, y: 300 },

                        stateRanges: [{

                            endValue: 50,

                            startValue: 0,

                            backgroundColor: "#24F92F",

                            borderColor: "Black"

                        }, {

                            endValue: 50,

                            startValue: 100,

                            backgroundColor: "#322C04",

                            borderColor: "Black"

                        }]



                    }, 

                    //Indicator2

                    {

                        height: 10,

                        width: 10,

                        type: "circle",

                        value: 0,

                        position: { x: 215, y: 300 },

                        stateRanges: [{

                            endValue: 50,

                            startValue: 0,

                            backgroundColor: "#600000",

                            borderColor: "Black"

                        }, {

                            endValue: 100,

                            startValue: 50,

                            backgroundColor: "#FF4F2A",

                            borderColor: "Black"

                        }]



                    }],

                }]

            });});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                 {

                     sc1.ShowIndicators(true)

                         .ShowRanges(true)

                         .MinorIntervalValue(5)

                         .ShowScaleBar(true).Radius(150).Size(5)

                         .Pointers(po =>

                         {

                         po.Length(110).Value(70).Add();

                         })

                          .Ranges(ran =>

                          {

                          ran.DistanceFromScale(-30).StartValue(0).EndValue(50).BackgroundColor("Green").Placement(RangePlacement.Far).Add();

                        ran.DistanceFromScale(-30).StartValue(50).EndValue(100).BackgroundColor("Red").Placement(RangePlacement.Far).Add();

                       })

                       .Indicators(ind =>

                       {

                       //Indicator1

                       ind.Height(10).Width(10)

                       .Type(IndicatorType.Circle)  

                       .Value(0)

                       .Position(pos =>pos.X(165).Y(300))

                       .StateRanges(st =>

                       {

                       st.EndValue(50)

                       .StartValue(0)

                       .BackgroundColor("#24F92F")

                       .BorderColor("Black").Add();

                       st.EndValue(50)

                       .StartValue(100)

                       .BackgroundColor("#322C04")

                       .BorderColor("Black").Add();      

                       }).Add();

                       //Indicator2

                       ind.Height(10).Width(10)

                       .Type(IndicatorType.Circle)

                       .Value(0)

                       .Position(pos =>pos.X(215).Y(300))

                       .StateRanges(st =>

                        {

                        st.EndValue(50)

                        .StartValue(0)

                        .BackgroundColor("#600000")

                        .BorderColor("Black").Add();

                        st.EndValue(100)

                       .StartValue(50)

                       .BackgroundColor("#FF4F2A")

                       .BorderColor("Black").Add();

                        }).Add();

                   }).Add();

                 })

)



**[ASP]**

&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales Showindicators="true" ShowRanges="true"  ShowscaleBar="true"  Size="5" radius="150" MinorIntervalValue="5" &gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers  Value="70"  length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;IndicatorCollection&gt;

&lt;%--indicator1 --%&gt;

                    &lt;ej:CircularIndicators Height="10" width="10" Type="Circle" Value="0"&gt;

                    &lt;Position X="165" Y="300" /&gt;

                        &lt;StateRangeCollection&gt; 

                            &lt;ej:CircularStateRanges EndValue="50" startValue="0" BackgroundColor="#24F92F" BorderColor="black"&gt;&lt;/ej:CircularStateRanges&gt;

                            &lt;ej:CircularStateRanges EndValue="50" startValue="100" BackgroundColor="#322C04" BorderColor="black"&gt;&lt;/ej:CircularStateRanges&gt;&lt;/StateRangeCollection&gt;

                    &lt;/ej:CircularIndicators&gt;

&lt;%--indicator2--%&gt;

                    &lt;ej:CircularIndicators Height="10" width="10" Type="Circle" Value="0"&gt;

                    &lt;Position X="215" Y="300" /&gt;

                        &lt;StateRangeCollection&gt; 

                            &lt;ej:CircularStateRanges EndValue="50" startValue="0" BackgroundColor="#600000" BorderColor="black"&gt;&lt;/ej:CircularStateRanges&gt;

                            &lt;ej:CircularStateRanges EndValue="100" startValue="50" BackgroundColor="#FF4F2A" BorderColor="black"&gt;&lt;/ej:CircularStateRanges&gt;&lt;/StateRangeCollection&gt;

                    &lt;/ej:CircularIndicators&gt;

                &lt;/IndicatorCollection&gt;

                &lt;RangeCollection&gt;

                    &lt;ej:CircularRanges DistanceFromScale="-30" startvalue="0" EndValue="50" BackgroundColor="green" Placement="Far"&gt;&lt;/ej:CircularRanges&gt;

                     &lt;ej:CircularRanges DistanceFromScale="-30" StartValue="50" EndValue="100" BackgroundColor="red" Placement="Far"&gt;&lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\indicators_images\indicators_img3.png" Caption="Figure 52: Circular Gauge with multiple indicators"%}

## Adding Indicator Collection 

Indicators collection is directly added to the scale object. Refer the following code to add indicator collection in a **Gauge** control.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{ showIndicators: true
indicators:[{
// For setting indicator height
**height: 10,**
// For setting indicator width
**width: 10,**
// For setting indicator type
**type: "circle",**
// For setting indicator value
**value: 0,**
// For setting indicator position
**position: { x: 185, y: 300 },**
}]
}]
})
});
</script>


{% endhighlight %}







Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\indicators_images\indicators_img4.png" Caption="Figure 50(a): Circular Gauge with indicator collection."%}





## Basic Customization

* You can enable indicators by setting **showIndicators** to ‘true’. The **height** and **width** property for the indicators are used to specify the area allocated to the indicator for the width and height respectively. You can use the position collection to position the indicators along **x** and **y** axis. 

* Indicators are of several types such as, circle, rectangle, rounded rectangle, text and image. By using the **type** property you can avail those shapes. For image type **imageUrl** property is used. 



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
**showIndicators: true,** minorIntervalValue: 5,
backgroundColor: "#5DF243",
border: { width: 1.5, color: "black" },
showScaleBar: true, radius: 120, size: 5,
pointers: [{
backgroundColor: "#5DF243",
border: { width: 1.5, color: "black" },
length: 110
}],
indicators: [{
// For setting indicator height
**height: 10,**
// For setting indicator width
**width: 10,**
// For setting indicator type
**type: "circle",**
// For setting indicator value
**value: 0,**
// For setting indicator position
**position: { x: 185, y: 300 },**

}],
}]
});
});
</script>


{% endhighlight %}



Execute the above code to render the following output.

![](indicators_images\indicators_img5.png)

Figure 50(b): Circular Gauge with customized indicator with basic properties

## State Ranges

* State ranges are used to specify the indicator behavior in the specified region. Use **startValue** and **endValue** to set the range bound for the pointer. Whenever the pointer cross the specified region, the indicator attributes are applied for ranges. 

* The **backgroundColor** and **borderColor** sets the appearance behavior for the indicators. For text type indicators you can give value for text. And **text** can be changed whenever the pointer crosses its state range area. There are many basic font options available for the text in the state range such as size, fontStyle and fontFamily.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showIndicators: true, minorIntervalValue: 5,
backgroundColor: "#5DF243",
border: { width: 1.5, color: "black" },
showScaleBar: true, radius: 150, size: 5,
pointers: [{
backgroundColor: "#5DF243",
border: { width: 1.5, color: "black" },
length: 110
}],
indicators: [{
// For setting indicator height
height: 10,
// For setting indicator width
width: 10,
// For setting indicator type
type: "circle",
// For setting indicator value
value: 0,
// For setting indicator position
position: { x: 185, y: 300 },
// For setting indicator state range collection
**stateRanges: [{**
// For setting state range end value height
**endValue: 100,**
// For setting state range start value
**startValue: 0,**
// For setting indicator background color
**backgroundColor: "#5DF243",**
// For setting indicator border color
**borderColor: "Black",**
// For setting indicator text
**text: "",**
// For setting indicator text color
**textColor: "#870505"**
}]

}],
}]
});
});
</script>


{% endhighlight %}







Execute the above code to render the following output.

![](indicators_images\indicators_img6.png)

Figure 51: Circular Gauge with customized indicator

## Multiple Indicators

You can use multiple indicators for a single **Gauge**. Each indicator have a list of state ranges. Refer the following code example for multiple Indicators.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{readOnly: false,
showIndicators: true,showRanges: true,
minorIntervalValue: 5,
showScaleBar: true, radius: 150, size: 5,
pointers: [{
length: 110,value:70
}],
ranges: [{
startValue: 0, endValue: 50,
backgroundColor: "Green",
placement: "far", distanceFromScale: -30
},
{
startValue: 50, endValue: 100,
backgroundColor: "red",
placement: "far", distanceFromScale: -30
}],

indicators: [
//Indicator1
{
height: 10,
width: 10,
type: "circle",
value: 0,
position: { x: 165, y: 300 },
stateRanges: [{
endValue: 50,
startValue: 0,
backgroundColor: "#24F92F",
borderColor: "Black"
}, {
endValue: 50,
startValue: 100,
backgroundColor: "#322C04",
borderColor: "Black"
}]

},
//Indicator2
{
height: 10,
width: 10,
type: "circle",
value: 0,
position: { x: 215, y: 300 },
stateRanges: [{
endValue: 50,
startValue: 0,
backgroundColor: "#600000",
borderColor: "Black"
}, {
endValue: 100,
startValue: 50,
backgroundColor: "#FF4F2A",
borderColor: "Black"
}]

}],
}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\indicators_images\indicators_img7.png" Caption="Figure 52: Circular Gauge with multiple indicators"%}



