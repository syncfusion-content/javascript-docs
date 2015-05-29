---
layout: post
title: gauge-position
description: gauge position
platform: js
control: Circular Gauge
documentation: ug
---

# Gauge Position

**Semi-circular Gauge** can be positioned within the canvas element whichand that provides better appearance ofor the gauge in the canvas.

**Positioning**

* **Semi-circular Gauge** can be positioned with the help of the attribute called **gaugePosition**. It is an enumerable value. You can position the gauge away from the corner with the help of the **distanceFromCorner** attribute. 

* The possible enum values for the **gaugePosition** are as follows:

  * Topleft

  * Topcenter

  * Topright

  * Middleleft

  * Center

  * Middleright

  * Bottomleft

  * Bottomcenter

  * Bottomright

{% highlight js %}

**[JavaScript]**
<div style=”float: left” id=”gauge1”>
<div id=" CoreCircularGaugehalfright "> </div
<script type=”text/javascript”>
$(function () {
$("#CoreCircularGaugehalfright").ejCircularGauge({
backgroundColor: "transparent",

// To set dimension of the canvas.
width: 500, height: 500,

// To set the value and radius of the canvas frame.
radius: 100, value: 60,

// To set the gauge position.
**gaugePosition**: "**topleft**",

// To set the distance from the corner.
**distanceFromCorner**:**25**,

// To set the semicircle frame specifications.
frame: {
frameType: 'halfcircle',
halfCircleFrameStartAngle: 270,
halfCircleFrameEndAngle: 90
},

// To set the scale specification.
scales: [{
startAngle: 270,
sweepAngle: 180, radius: 100,
showScaleBar: true, size: 1,
maximum: 120, majorIntervalValue: 20,
minorIntervalValue: 10,
border: {
width: 0.5,
}
}]
});
});
</script>


{% endhighlight %}





<table>
<tr>
<td>
<b>[Razor]</b>@(Html.EJ().CircularGauge("SemiCircularGauge").BackgroundColor("transparent")                // To set dimension of the canvas.                .Width(500).Height(500).Radius(100).Value(60)                // To set gauge position.                .GaugePosition(GaugePosition.TopLeft)                // To set gauge distance from corner.                .DistanceFromCorner(25)                            // To set frame settings.                .Frame(fr=>fr.FrameType(Frame.HalfCircle)                               // To set frame start angle.                              .HalfCircleFrameStartAngle(270)                                                        // To set frame end angle.                              .HalfCircleFrameEndAngle(90))                // To set basic scale settings.                .Scales(SC =>                {                    SC.Radius(100).Maximum(120).MajorIntervalValue(20)                    .MinorIntervalValue(10).ShowScaleBar(true).Size(1)                    .Border(bor => bor.Width(0.5))                    .StartAngle(270).SweepAngle(180)                    .Add();                })                )</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        //        // GET: /ToolTip/        public ActionResult Semicircular()        {            return View();        }    }</td></tr>
</table>


**[ASPX]**

<ej:CircularGauge runat="server" ID="SemiCircularGauge" Value="60"



&lt;%--&lt;setting basic dimension--%&gt;

BackgroundColor="transparent" Width="500" Height="500" Radius="100" 



          &lt;%--&lt;setting gauge position--%&gt;

         GaugePosition="TopLeft" 



          &lt;%--&lt;setting gauge distance from corner--%&gt;

          DistanceFromCorner="25">



         &lt;%--&lt;setting frame values--%&gt;

         <Frame FrameType="HalfCircle" 

                 HalfCircleFrameEndAngle="90" 

                 HalfCircleFrameStartAngle="270"/>



       &lt;%--&lt;setting gauge distance from corner--%&gt;      

       &lt;Scales&gt;

          <ej:CircularScales SweepAngle="180" StartAngle="270" Radius="100" 

                             ShowScaleBar="true" Size="1" Maximum="120" 

                             MajorIntervalValue="20" MinorIntervalValue="10">



               &lt;%--&lt;setting scale border--%&gt;      

               &lt;Border Width="0.5"&gt;

               &lt;/Border&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

     &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

When the above code is run, the output is displayed as follows:

{% include image.html url="\js\CircularGauge\concepts-and-features\gauge-position_images\gauge-position_img1.png" Caption="Figure 65: Semi-circular Gauge with Default topleft position"%}

