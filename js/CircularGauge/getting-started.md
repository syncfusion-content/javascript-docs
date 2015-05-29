---
layout: post
title: getting-started
description: getting started
platform: js
control: Circular Gauge
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Circular Gauge** in your application with **JavaScript** and **ASP.NET MVC**.

Create your first Circular Gauge in JavaScript

* This section encompasses how to configure **Circular Gauge**. You can provide data to a **Circular Gauge** and make them to display the data in a required way. 

* The following screen shot displays a **Circular Gauge**, which visually represents the functions of an Automobile speedometer with RPM (Rotation per Minute), KmpH (Kilometer per hour) and it denotes the speed level indicators (Safe, Caution and Danger). 



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img1.png" Caption="Figure 2:Speedometer Gauge"%}



* CFirst create an **HTML** file and add references to the required libraries.



{% highlight js %}

**[HTML]**

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<meta charset="utf-8" />
<link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /><link href="http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" />
<!--scripts-->
<script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
<script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.js"></script"></script>
<script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js">                                                               </script><script src=" http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js"></script>
</head>



{% endhighlight %}



* Add a div element that acts as a container for **ejCircularGauge** widget.



{% highlight js %}

**[HTML]**

<body>
<div id="CircularGauge1"></div>

</body>



{% endhighlight %}



* Create the **ejCircularGauge** widget as follows,



{% highlight js %}

**[HTML]**

<script type="text/javascript">
$(function () {
$("#CircularGauge1").ejCircularGauge();
});
</script>

</html>


{% endhighlight %}



On Eexecuting the above code, samples renders a default **Circular Gauge** with default values as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img2.png" Caption="Figure 3: Circular Gauge"%}

**Set Height and Width values**

Pointers have different height and range. You can set the height and width of the gauge.



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
});


{% endhighlight %}



The following screenshot displays a **Gauge** in which height and width areis set.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img3.png" Caption="Figure 4: Circular Gauge"%}

**Set Background Color**

You can draw the speedometer with dark background and to vary the speed of the pointer, set the **readOnly** option as **False** for user interaction. 



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
});


{% endhighlight %}



The above code example renders a **Gauge** as shown in the following screen shot.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img4.png" Caption="Figure 5: Circular Gauge with background color"%}

**Provide scale values**

* You can customize the pointer cap using the following options- Cap radius, Cap border color, cap background color, pointer cap border width. 

* Set the maximum speed limit in the **Gauge** as 200KmpH.

* Major Ticks and Minor Ticks have the interval values 20 and 5 respectively. Show ranges and show indicators are used to display the ranges and indicators in their respective positions.



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
showRanges: true,
showIndicators: true,
pointerCap: {
radius: 15,
borderWidth: 0,
backgroundColor: "#797C79",
borderColor: "#797C79"
},
maximum: 200,
majorIntervalValue: 20,
minorIntervalValue: 5,
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here
}]
});


{% endhighlight %}



On Eexecuting the above code, samples renders a **Circular Gauge** with customized labels as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img5.png" Caption="Figure 6: Circular Gauge with scale values"%}

**Add Label Customization**

To display the values in the **Gauge,** scale labels are used. You can customize the label color.  



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
scales: [{
//Add the labels customization code here

labels: [{
color: "#ffffff"
}],
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});



{% endhighlight %}



On Eexecuting the above code, samples renders a default **Circular Gauge** with customized labels as 

follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img6.png" Caption="Figure 7: Circular Gauge with Labels"%}

**Add pointer data**

You can use three pointers that denote kilometer value, rotation per minute value and torque value.

The torque value pointer should not be similar to other two pointers. Set the torque pointer as marker pointer. You can set other attributes for pointer such as background color, border color, Length, width and distance from scale.



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here

pointers: [{
value: 140,
distanceFromScale: 60,
showBackNeedle: false,
length: 20,
type: "marker",
markerType: "triangle",
width: 10,
radius: 10,
backgroundColor: "#FF940A",
border: {
color: "#FF940A"
},
},
{
value: 110,
showBackNeedle: false,
length: 150,
width: 2,
radius: 10,
needleType: "rectangle",
backgroundColor: "#05AFFF",
border: {
color: "#05AFFF"
},                }, {
value: 67,
showBackNeedle: false,
length: 100,
width: 15,
radius: 10,
backgroundColor: "#FC5D07",
border: {
color: "#FC5D07"
},

}],
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});


{% endhighlight %}



On Eexecuting the above code, samples renders a customized **Circular Gauge** as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img7.png" Caption="Figure 8: Circular Gauge with Pointer"%}

**Add Tick Details**

* You can display the tick value with customization refer as given in the following code example. 

* You can set width and height of the Mmajor ticks greaterhigher than the Minor ticks. 

* You can set dark background for tick Color to have a better visibility.



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,
scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here

ticks: [{
type: "major",
distanceFromScale: 70,
height: 20,
width: 3,
color: "#ffffff"
}, {
type: "minor",
height: 12,
width: 1,
distanceFromScale: 70,
color: "#ffffff"
}],
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});




{% endhighlight %}



On Eexecuting the above code, samples renders a **Circular Gauge** with customized labels as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img8.png" Caption="Figure 9: Circular Gauge with Tick details"%}

**Add Range Values**

Ranges denote the property of scale value in the speedometer. The color values of the ranges specify the speed variation. Set **showRanges** property to **“True”** to show the ranges in the **Circular Gauge**.



* Select safe zone for low speed, caution zone for moderate speed and high zone for high speed.



* Select safe zone for low speed, caution zone for moderate speed and high zone for high speed.You can customize the range with the properties such as start value, end value, start width, end width,  background color , border color, etc.,



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here

ranges: [{
distanceFromScale: 30,
startValue: 0,
endValue: 70,
backgroundColor: "#5DF243",
border: {
color: "#FFFFFF"
},
}, {
distanceFromScale: 30,
startValue: 70,
endValue: 140,
backgroundColor: "#F6FF0A",
border: {
color: "#FFFFFF"
},                },
{
distanceFromScale: 30,
startValue: 140,
endValue: 200,
backgroundColor: "#FF1807",
border: {
color: "#FFFFFF"
},
}],
//Add the indicators customization code here
//Add the Custom labels customization code here

}]
});


{% endhighlight %}



On Eexecuting the above code, samples renders a **Circular Gauge** with customized range as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img9.png" Caption="Figure 10: Circular Gauge with range values"%}

**Add Indicator Details**

* Indicators denote whether the pointer values are placed in their respective zones. You can position the indicator on the respective range value for the required changes.

* You can set the location of the indicator using **position** property. The **stateRanges** property defines how the indicator should behave when the pointer is in certain values. 



{% highlight js %}

$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here

indicators: [
{
height: 10,
width: 10,
type: "circle",
position: { x: 210, y: 300 },
stateRanges: [{
endValue: 70,
startValue: 0,
backgroundColor: "#5DF243",
borderColor: "#5DF243",
text: "",
textColor: "#870505"
}, {
endValue: 200,
startValue: 70,
backgroundColor: "#145608",
borderColor: "#145608",
text: "",
textColor: "#870505"
}]
},
{
height: 10,
width: 10,
type: "circle",
position: { x: 255, y: 200 },
stateRanges: [{
endValue: 140,
startValue: 70,
backgroundColor: "#F6FF0A",
borderColor: "#F6FF0A",
text: "",
}, {
endValue: 70,
startValue: 0,
backgroundColor: "#969B0C",
borderColor: "#969B0C",
text: "",
}, {
endValue: 200,
startValue: 140,
backgroundColor: "#969B0C",
borderColor: "#969B0C",
text: "",
}]
}, {
height: 10,
width: 10,
type: "circle",
position: { x: 300, y: 300 },
stateRanges: [{
endValue: 140,
startValue: 0,
backgroundColor: "#890F06",
borderColor: "#890F06",
text: "",
},
{
endValue: 200,
startValue: 140,
backgroundColor: "#FF1807",
borderColor: "#FF1807",
text: "",
}]
}],
//Add the Custom labels customization code here

}]
});



{% endhighlight %}



On Eexecuting the above code, samples renders a **Circular Gauge** with customized indicators as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img10.png" Caption="Figure 11: Circular Gauge with Customized Indicators"%}

**Add Custom Label Details**

* You can specify the text in the **Gauge** using **Custom labels** and you can customize it through various properties.

* You can use custom texts to display the three range description.



{% highlight js %}


$("#CircularGauge1").ejCircularGauge({
width: 500,
height: 500,
backgroundColor: "#3D3F3D",
readOnly: false,

scales: [{
//Add the labels customization code here
//Add the pointers customization code here
//Add the ticks customization code here
//Add the ranges customization code here
//Add the indicators customization code here
//Add the Custom labels customization code here

customLabels: [{
value: "Safe",
position: { x: 200, y: 280 },
color: "#5DF243",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}, {
value: "Caution",
position: { x: 253, y: 212 },
color: "#F6FF0A",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}, {
value: "Danger",
position: { x: 290, y: 280 },
color: "#FF1807",
font:
{
size: "12px",
fontFamily: "Arial",
fontStyle: "Bold"
}
}]
}]
});




{% endhighlight %}



The following screenshot displays a **Circular Gauge** control with all customization properties.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img11.png" Caption="Figure 12: Circular Gauge with Custom Label details"%}

## Create your first Circular Gauge in MVC

The **ASP.NET MVC Circular Gauge** provides support to display the **Circular Gauge** within your web page and allows you to customize it. This section encompasses the details on how to configure **Circular Gauge.** You can learn how to provide data for a **Circular Gauge** and display that data in a suitable way. In addition, you will learn how to customize the default **Circular Gauge** appearance, according to your requirements. As a result, you will get a **Circular Gauge** that shows you how the Automobile speedometer works with rpm (Rotation per Minute), kmph (Kilometer per hour) and speed level indication (Safe, Caution and Danger). 



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img12.png" Caption="Figure 13: Analog Speedometer"%}

**Create a Circular Gauge**

**ASP.NET MVC Circular Gauge** widget basically renders with animation and flexible APIs. You can easily create the **Circular Gauge** widget by using the following steps.

1. You can create an **MVC** Project and add necessary Dlls and script with the help of the given [MVC-Getting Started](http://help.syncfusion.com/ug/js/default.htm) Documentation.

2. Add the following code example to the corresponding view page to render **Circular****Gauge**.



**[view]**



@(Html.EJ().CircularGauge("circulargauge"))





3. Add the following code example in the controller page.



**[Controller]**



public ActionResult Default()     



    {

        return View();



    }



Run the above code example to get a default **Circular****Gauge** with default values.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img13.png" Caption="Figure 14: Circular Gauge"%}

**Set Height and Width**

Pointers have different height and width so you can set the height and width of the gauge according to your requirements.

Set the basic values of the gauge such as height and width of the canvas element values that are to be rendered and some other basic elements of the gauge.



**[view]**

@(Html.EJ().CircularGauge("circulargauge")        

                             .Height(500)

                             .Width(500)

)



Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img14.png" Caption="Figure 15: Circular Gauge with Height and Width"%}

**Set Background Color**

The speedometer must have some dark color as background so that its value is clearly visible and you can vary the speed of the pointer by setting **ReadOnly** as **False** for user interaction.



**[view]**



 @(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    )





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img15.png" Caption="Figure 16: Circular Gauge with Dark Background"%}

**Provide Scale Values**

* The pointer cap can be customized with the following options. Cap radius, cap border color, cap background color, pointer cap border width are some of the properties that are customizable.

* The speed limit in the gauge has maximum value of 200 kmph. So you can set maximum value for the gauge as 200.

* Major Ticks have the interval value of 20 and minor ticks have the interval value of 5. Show ranges and show indicators are used to display the ranges and indicators in their respective positions.



**[view]**



@(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {

        scl.ShowRanges(true)

        .ShowIndicators(true)

        .PointerCap(cap=>

          cap.Radius(15)

             .BorderWidth(0)

             .BackgroundColor("#797C79")

             .BorderColor("#797C79"))        .Maximum(200)

        .MajorIntervalValue(20)

        .MinorIntervalValue(5).Add();

        //Add the labels customization code here

        //Add the pointers customization code here

        //Add the ticks customization code here

        //Add the ranges customization code here

        //Add the indicators customization code here

        //Add the Custom labels customization code here

    })



)





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img16.png" Caption="Figure 17: Circular Gauge with Scale Values"%}

**Add Label Customization**

To display the value around the scales, labels are used. By customizing the label color it displays as specified.



**[view]**



   @(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {scl

        //Add the labels customization code here

        .Labels(lbl => lbl.Color("#ffffff").Add())

        .Add();

        //Add the pointers customization code here

        //Add the ticks customization code here

        //Add the ranges customization code here

        //Add the indicators customization code here

        //Add the Custom labels customization code here



    }))



Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img17.png" Caption="Figure 18: Circular Gauge with Label"%}

**Add Pointers**

Here, you have three pointers that denote the kilometer value, rotation per minute value and torque value.

The torque value pointer needs not be similar to the other two pointers. You can set torque pointer as marker pointer. And you can set other attributes for pointer such as background color, border color, length, width and distance from scale.



**[view]**



@(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {scl

        //Add the labels customization code here

        //Add the pointers customization code here

        .Pointers(ptr=>{

            ptr.Value(140)

        .DistanceFromScale(60)

        .ShowBackNeedle(false)

        .Length(20)

        .Type(PointerType.Marker)

        .MarkerType(MarkerType.Triangle)

        .Width(10)

        .BackgroundColor("#FF940A")

        .Border(bor => bor.Color("#FF940A")).Add();



            ptr.Value(110)

            .ShowBackNeedle(false)

            .Length(150)

            .NeedleType(NeedleType.Rectangle)

            .Width(2)

            .BackgroundColor("#05AFFF")

            .Border(bor =>bor.Color("#05AFFF")).Add();



            ptr.Value(67)

        .ShowBackNeedle(false)

        .Length(100)

        .Width(15)

        .BackgroundColor("#FC5D07")

        .Border(bor => bor.Color("#FC5D07")).Add();



        })

        .Add();

        //Add the ticks customization code here

        //Add the ranges customization code here

        //Add the indicators customization code here

        //Add the Custom labels customization code here



    }))





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img18.png" Caption="Figure 19: Circular Gauge with Pointers"%}

**Add Tick Details**

* You can set major ticks with their width and height equal to Minor ticks. You can set **Color** according to your preference for better visibility in dark backgrounds.

* To display the tick value and its customization add the following code example. 



**[view]**



@(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {

        scl

        //Add the labels customization code here

        //Add the pointers customization code here

        //Add the ticks customization code here

        .Ticks(tic => { 

        tic.Type(CircularTickTypes.Major)

        .DistanceFromScale(70)

        .Height(20)

        .Width(3)

        .Color("#ffffff").Add();



        tic.Type (CircularTickTypes.Minor)

        .DistanceFromScale(70)

        .Height(12)

        .Width(1)

        .Color("#ffffff").Add();

        })

        .Add();

        //Add the ranges customization code here

        //Add the indicators customization code here

        //Add the Custom labels customization code here



    }))





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img19.png" Caption="Figure 20: Circular Gauge with Ticks"%}

**Add Range Values**

* Ranges denote the property of the scale value in the speedometer. The color values of the ranges denote speed variation. Set **ShowRanges** as **True** for showing the ranges in the **Circular Gauge**.

* For Low speed, you can mention it as safe zone; for moderate speed, you can call it as caution zone and for high speed, you can mark it as high speed.

* You can customize the range with properties such as start value, end value, start width, end width,  background color , border color, etc.,



**[view]**



 @(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {

        scl

        //Add the labels customization code here

        //Add the pointers customization code here

        //Add the ticks customization code here

        //Add the ranges customization code here

        .Ranges(rng => {

            rng.DistanceFromScale(30)

            .StartValue(0)

            .EndValue(70)

            .BackgroundColor("#5DF243")

            .Border(bor => bor.Color("#ffffff")).Add();



            rng.DistanceFromScale(30)

            .StartValue(70)

            .EndValue(140)

            .BackgroundColor("#F6FF0A")

            .Border(bor => bor.Color("#ffffff")).Add();



            rng.DistanceFromScale(30)

            .StartValue(140)

            .EndValue(200)

            .BackgroundColor("#FF1807")

            .Border(bor => bor.Color("#ffffff")).Add();

        })

        .Add();

        //Add the indicators customization code here

        //Add the Custom labels customization code here



    }))





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img20.png" Caption="Figure 21: Circular Gauge with Ranges"%}

**Add Indicator Details**

* Indicators denote whether the pointers values are in their respective zones or not. Positioning the indicator on the respective range value gives you the required changes.

* By using **Position** property, you can set the location of the indicator. **StateRanges** defines how the indicator should behave when the pointer is in certain values. 



**[view]**



   @(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {

            //Add the labels customization code here

            //Add the pointers customization code here 

            //Add the ticks customization code here

            //Add the ranges customization code here

            //Add the indicators customization code here

        .Indicators(ind =>

        {

            ind.Height(10)

                .Width(10)

                . Type(IndicatorType.Circle)                

                .Position(loc => loc.X(210).Y(300))

                .StateRanges(str =>

                {

                    str.EndValue(70)

                    .StartValue(0)

                    .BackgroundColor("#5DF243")

                    .BorderColor("#5DF243").Text("").TextColor("#ffffff")

                    .Add();



                    str.EndValue(200)

                    .StartValue(70)

                    .BackgroundColor("#145608")

                    .BorderColor("#145608").Text("").TextColor("#ffffff")

                    .Add();

                }).Add();



            ind.Height(10)

                .Width(10)

                . Type(IndicatorType.Circle)                

                .Position(loc => loc.X(255).Y(200))

                .StateRanges(str =>

                {

                    str.EndValue(140)

                    .StartValue(70)

                    .BackgroundColor("#F6FF0A")

                    .BorderColor("#F6FF0A").Text("").TextColor("#ffffff")

                    .Add();



                    str.EndValue(70)

                    .StartValue(0)

                    .BackgroundColor("#969B0C")

                    .BorderColor("#969B0C").Text("").TextColor("#ffffff")

                    .Add();



                    str.EndValue(200)

                    .StartValue(140)

                    .BackgroundColor("#969B0C")

                    .BorderColor("#969B0C").Text("").TextColor("#ffffff")

                    .Add();

                }).Add();



            ind.Height(10)

                .Width(10)

                . Type(IndicatorType.Circle)                

                .Position(loc => loc.X(300).Y(300))

                .StateRanges(str =>

                {

                    str.EndValue(140)

                    .StartValue(200)

                    .BackgroundColor("#890F06")

                    .BorderColor("#890F06").Text("").TextColor("#ffffff")

                    .Add();



                    str.EndValue(140)

                   .StartValue(0)

                   .BackgroundColor("#FF1807")

                   .BorderColor("#FF1807").Text("").TextColor("#ffffff")

                   .Add();

                }).Add();

        }).Add();

        //Add the Custom labels customization code here              

    }))





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img21.png" Caption="Figure 22: Circular Gauge with Indicators"%}

**Add Custom Label Details**

Custom labels are used to specify the texts that need to be displayed in the gauge. You can customize it through various properties.

To display the three range description, custom texts are used here.



**[view]**



    @(Html.EJ().CircularGauge("circulargauge")

    .Height(500)

    .Width(500)

    .BackgroundColor("#3D3F3D")

    .ReadOnly(false)

    .Scales(scl => {

            //Add the labels customization code here

            //Add the pointers customization code here

            //Add the ticks customization code here

            //Add the ranges customization code here

            //Add the indicators customization code here

            //Add the Custom labels customization code here

         .CustomLabels(clbl=>{ 

            clbl.Value("Safe")

                .Color("#5DF243")

                .Position(loc=>loc.X(200).Y(280))

                .Font(fnt => { fnt.FontFamily("Arial").Size("12px").FontStyle("Bold"); })

                .Add();



            clbl.Value("Caution")

                .Color("#F6FF0A")

                .Position(loc => loc.X(253).Y(212))

                .Font(fnt => { fnt.FontFamily("Arial").Size("12px").FontStyle("Bold"); })

                .Add();



            clbl.Value("Danger")

                .Color("#FF1807")

                .Position(loc => loc.X(290).Y(280))

                .Font(fnt => { fnt.FontFamily("Arial").Size("12px").FontStyle("Bold"); })

                .Add();

         }).Add();

    }))





Run the above code example and you can see the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img22.png" Caption="Figure 23: Circular Gauge with Custom Label"%}

## Create your first Circular Gauge in ASP.NET

The **ASP.NET Circular Gauge** provides support to display the **Circular****Gauge** within your web page and allows you to customize it. This section encompasses the details on how to configure **Circular Gauge**. You can learn how to provide data for a **Circular Gauge** and display this data in the required way. In addition, you can learn how to customize the default **Circular Gauge** appearance to your requirements. As a result, you can get a **Circular Gauge** that shows how the Automobile speedometer works with rpm (Rotation per Minute), KmpH (Kilometer per hour) and denotes the speed level indication (Safe, Caution and Danger). 

**Speedometer Gauge**



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img23.png" Caption="Figure 24: Analog Speedometer"%}

**Create a Circular Gauge**

**ASP.NET Circular Gauge** widget basically renders with animation and flexible API’s. You can easily create the **Circular Gauge** widget by using simple code example as follows.

1. You can create an ASP Project and adding necessary Dll’s and Scripts with the help of the given ASP-Getting Started Documentation.

2. Add the mentioned code to the corresponding designer page for **Circular Gauge** rendering.



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1"&gt;

&lt;/ej:CircularGauge&gt;





Run this code to get a default **Circular****Gauge** with default values.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img24.png" Caption="Figure 25: Circular Gauge"%}

**Set Height and Width values**

Pointers have different height and width range so you can set the height and width of the gauge according to your requirements.

Set the basic values of the gauge such as height and width of the canvas element values that are rendered and some basic behavior of the gauge.

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500"&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img25.png" Caption="Figure 26: Circular Gauge with height and width"%}

**Set Background Color**

You can draw the speedometer with dark background and to vary the speed of the pointer you can set **ReadOnly** to ‘**false**’ for user Interaction. 

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

&lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img26.png" Caption="Figure 27: Circular Gauge with dark background"%}

**Provide scale values**

* The pointer cap is customized with the following options. Cap radius, cap border color, cap background color, pointer cap border width are some of the properties that are customizable.

* The speed limit in the gauge has maximum value of 200KmpH.So you can set maximum value for the gauge as 200.

* Major Ticks have the interval value of 20 and minor ticks have the interval value of 5. Show ranges and show indicators are used to displaying the ranges and indicators in their respective positions.

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output..



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img27.png" Caption="Figure 28: Circular Gauge with scale values"%}

**Add Label Customization**

To display the value around the scale, labels are used. By customizing the label color it displays as specified 

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

               &lt;LabelCollection&gt;

                   &lt;ej:CircularLabels Color="#FFFFFF"&gt;&lt;/ej:CircularLabels&gt;

               &lt;/LabelCollection&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;%--Add the indicators customization code here--%&gt;

&lt;%--Add the Custom labels customization code here--%&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run the above code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img28.png" Caption="Figure 29: Circular Gauge with label"%}

**Add pointers data**

Here, you have three pointers that denote the kilometer value, rotation per minute value and torque value.

The torque value pointer needs not to be similar to the other two pointers. You can set torque pointer as marker pointer. And you can set other attributes for pointer such as background color, border color, Length, width and distance from scale

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;PointerCollection&gt;

               <ej:Pointers Value="140" DistanceFromScale="60"

                   ShowBackNeedle="false" Length="20" Type="Marker" 

                   MarkerType="Triangle" Width="10" BackgroundColor="#FF940A">

                   &lt;Border Color="#FF940A"/&gt;

               &lt;/ej:Pointers&gt;



               <ej:Pointers Value="110" ShowBackNeedle="false" Length="150" 

                   NeedleType="Rectangle" Width="2" BackgroundColor="#05AFFF">

                   &lt;Border Color="#05AFFF"/&gt;

               &lt;/ej:Pointers&gt;

               <ej:Pointers Value="67" ShowBackNeedle="false" Length="100" 

                   Width="15" BackgroundColor="#FC5D07">

                   &lt;Border Color="#FC5D07"/&gt;

                &lt;/ej:Pointers&gt;

&lt;/PointerCollection&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;%--Add the indicators customization code here--%&gt;

&lt;%--Add the Custom labels customization code here--%&gt;



           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img29.png" Caption="Figure 30: Circular Gauge with pointers"%}

**Add Ticks Details**

You can set major ticks with their width and height bigger than Minor ticks and color must be given for better visibility in dark backgrounds.

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;TickCollection&gt;

                   <ej:CircularTicks Type="Major" DistanceFromScale="70"

                    Height="20" Width="3" Color="#FFFFFF"/>

                   <ej:CircularTicks Type="Minor" DistanceFromScale="70" 

                    Height="12" Width="1" Color="#FFFFFF" />

&lt;/TickCollection&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;%--Add the indicators customization code here--%&gt;

&lt;%--Add the Custom labels customization code here--%&gt;



           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img30.png" Caption="Figure 31: Circular Gauge with Ticks"%}

**Add Range Values**

* Ranges denote the property of the scale value in the speedometer. The color values of the ranges specifie the speed variation. Set **ShowRanges** to ‘**true**’ for showing the ranges in the **Circular Gauge**.

* For Low speed, you can mention it as safe zone; for moderate speed, you can to give as caution zone and for high speed, you can notify it as high speed.

* You can customize the range with the properties such as start value, end value, start width, end width,  background color , border color, etc.,

**Code:**

Ranges denote the property of the scale value in the speedometer. The color values of the ranges denote speed variation. Set **ShowRanges** as **True** for showing the ranges in the **Circular Gauge**.

For Low speed, you can mention it as safe zone; for moderate speed, you can call it as caution zone and for high speed, you can mark it as high speed.

You can customize the range with properties such as start value, end value, start width, end width,  background color , border color, etc.,



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;RangeCollection&gt;

                   <ej:CircularRanges DistanceFromScale="30" StartValue="0" 

                        EndValue="70" 

                        BackgroundColor="#5DF243">

                       &lt;Border Color="#FFFFFF"/&gt;

                   &lt;/ej:CircularRanges&gt;

                   <ej:CircularRanges DistanceFromScale="30" StartValue="70" 

                       EndValue="140" 

                       BackgroundColor="#F6FF0A">

                      &lt;Border Color="#FFFFFF"/&gt;

                   &lt;/ej:CircularRanges&gt;

                   <ej:CircularRanges DistanceFromScale="30" StartValue="140" 

                        EndValue="200" 

                        BackgroundColor="#FF1807">

                       &lt;Border Color="#FFFFFF"/&gt;

                   &lt;/ej:CircularRanges&gt;

&lt;/RangeCollection&gt;



&lt;%--Add the indicators customization code here--%&gt;

&lt;%--Add the Custom labels customization code here--%&gt;



           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img31.png" Caption="Figure 32: Circular Gauge with Ranges"%}

**Add Indicator Details**

* Indicators denote whether the pointers values are in their respective zones or not. Positioning the indicator on the respective range value gives the required changes.

* By using **Position** property, you can set location of the indicator. **StateRanges** defines how the indicator should behave when the pointer is in certain values. 

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;%--Add the indicators customization code here--%&gt;

&lt;IndicatorCollection&gt;

                   <ej:CircularIndicators Type="Circle" 

                        Height="10" Width="10">

                       &lt;Position X="210" Y="300"/&gt;

                       &lt;StateRangeCollection&gt;

                         <ej:CircularStateRanges StartValue="0" EndValue="70"

                           BackgroundColor="#5DF243" BorderColor="#5DF243">

                         &lt;/ej:CircularStateRanges&gt;

                         <ej:CircularStateRanges StartValue="70" EndValue="200" 

                           BackgroundColor="#145608" BorderColor="#145608">

                         &lt;/ej:CircularStateRanges&gt;

                       &lt;/StateRangeCollection&gt;

                   &lt;/ej:CircularIndicators&gt;





                   <ej:CircularIndicators Type="Circle" 

                        Height="10" Width="10">

                       &lt;Position X="255" Y="200"/&gt;

                       &lt;StateRangeCollection&gt;

                         <ej:CircularStateRanges StartValue="0" EndValue="70"

                           BackgroundColor="#969B0C" BorderColor="#969B0C">

                         &lt;/ej:CircularStateRanges&gt;

                         <ej:CircularStateRanges StartValue="70" EndValue="140"

                           BackgroundColor="#F6FF0A" BorderColor="#F6FF0A">

                         &lt;/ej:CircularStateRanges&gt;

                        <ej:CircularStateRanges StartValue="140" EndValue="200" 

                          BackgroundColor="#969B0C" BorderColor="#969B0C">

                        &lt;/ej:CircularStateRanges&gt;

                       &lt;/StateRangeCollection&gt;

                   &lt;/ej:CircularIndicators&gt;





                   <ej:CircularIndicators Type="Circle" 

                       Height="10" Width="10">

                       &lt;Position X="300" Y="300"/&gt;

                       &lt;StateRangeCollection&gt;

                        <ej:CircularStateRanges StartValue="140" EndValue="200" 

                         BackgroundColor="#FF1807" BorderColor="#FF1807">

                        &lt;/ej:CircularStateRanges&gt;

                        <ej:CircularStateRanges StartValue="0" EndValue="140" 

                          BackgroundColor="#890F06" BorderColor="#890F06">

                          &lt;/ej:CircularStateRanges&gt;

                       &lt;/StateRangeCollection&gt;

                   &lt;/ej:CircularIndicators&gt;

               &lt;/IndicatorCollection&gt;

&lt;%--Add the Custom labels customization code here--%&gt;



           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



Run this code to get the following output.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img32.png" Caption="Figure 33: Circular Gauge with Indicators"%}

**Add Custom Label Details**

Custom labels are used to specify the texts that need to be displayed in the gauge .you can customize it using various properties.

To display the three range description, custom texts are used here.

**Code:**



**[ASPX]**



&lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" BackgroundColor="#3D3F3D" ReadOnly="false"&gt;

       &lt;Scales&gt;

           <ej:CircularScales ShowRanges="true" ShowIndicators="true" 

            Maximum="200" MajorIntervalValue="20" MinorIntervalValue="5">

           <PointerCap Radius="15" BackgroundColor="#797C79" 

             BorderColor="#797C79" BorderWidth="0">

           &lt;/PointerCap&gt;

&lt;%--Add the labels customization code here--%&gt;

&lt;%--Add the pointers customization code here--%&gt;

&lt;%--Add the ticks customization code here--%&gt;

&lt;%--Add the ranges customization code here--%&gt;

&lt;%--Add the indicators customization code here--%&gt;

&lt;%--Add the Custom labels customization code here--%&gt;

&lt;CustomLabelCollection&gt;

                   &lt;ej:CircularCustomLabel Color="#5DF243" Value="Safe"&gt;

                       &lt;Position X="200" Y="280"/&gt;

                       <Font FontFamily="Arial" FontStyle="Bold" 

                       Size="12px">&lt;/Font&gt;

                   &lt;/ej:CircularCustomLabel&gt;

                   &lt;ej:CircularCustomLabel Color="#F6FF0A" Value="Caution"&gt;

                       &lt;Position X="253" Y="212"/&gt;

                       <Font FontFamily="Arial" FontStyle="Bold" 

                       Size="12px">&lt;/Font&gt;

                   &lt;/ej:CircularCustomLabel&gt;

                   &lt;ej:CircularCustomLabel Color="#FF1807" Value="Danger"&gt;

                       &lt;Position X="290" Y="280"/&gt;

                       <Font FontFamily="Arial" FontStyle="Bold" 

                       Size="12px">&lt;/Font&gt;

                   &lt;/ej:CircularCustomLabel&gt;

               &lt;/CustomLabelCollection&gt;



           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

   &lt;/ej:CircularGauge&gt;



The final output is as follows.



{% include image.html url="\js\CircularGauge\getting-started_images\getting-started_img33.png" Caption="Figure 34: Circular Gauge with Custom label"%}

