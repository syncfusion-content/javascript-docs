---
layout: post
title: pointers
description: pointers
platform: js
control: Circular Gauge
documentation: ug
---

# Pointers

**Pointer** value points out the actual value set in the **Circular Gauge**. You can customize the pointers to improve the appearance of **Gauge**..

**Add pointer collection**

**Pointer collection** is directly added to the scale object. To add pointer collection in a **Gauge** control refer the following code example.  



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ 

                           pointers:[{

                                       value:30

                            }]

                }]

            })

        });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

          .Scales(sc =>

          {

          sc.Pointers(PO =>

          {

         // For setting pointer value

         PO.Value(30).Add();

          }).Add();

          })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers value="30"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;

**Add pointer value**

**Pointer value** is the important element in the **Circular Gauge** that indicates the **Gauge** value. Real purpose of the **Circular Gauge** is based on the pointer value. You can set the pointer value either directly during rendering the control or it can be achieved by public method too.



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

                        startValue: 20,

                        endValue: 80,

                        backgroundColor: "Green",

                    }],

                    pointers: [{

**value:30**

                      }]



                }]

            }); });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc =>

                {

                    sc.ShowScaleBar(true)

                      .MajorIntervalValue(10)

                      .MinorIntervalValue(2)

                      .Radius(150)

                      .Size(2)

                      .ShowRanges(true)

                      .Ranges(ran =>

                        {

                     ran.StartValue(20)

                       .EndValue(80)

                       .BackgroundColor(ConsoleColor.Green.ToString())

                       .Add();

                        })

                      .Pointers(PO =>

                        {

                    // For setting pointer value

                        **PO.Value(30).Add();**

                        }).Add();

                })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true" ShowScalebar="true" Size="2" radius="150" MajorIntervalValue="10" MinorIntervalValue="2" &gt;

                &lt;RangeCollection&gt;

                    &lt;ej:CircularRanges StartValue="20" EndValue="80" BackgroundColor="green"&gt;&lt;/ej:CircularRanges&gt;

                &lt;/RangeCollection&gt;

&lt;%--For setting ponter value--%&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="30"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

         &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.



![](pointers_images\pointers_img1.png)

_Figure_ _41__: Circular Gauge with customized pointer value_

**Pointer Styles**

**Colors and Border**

* The Pointers border is modified with the object called **border** as in scales. It has two border property called **color** and **width** that are used to customize the border color of the pointer and border width of the pointer. You can set the background color to improve the look of the **Circular Gauge** and you can customize the background color of the scale using **backgroundColor** .



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showScaleBar: true,

                    width: 10, radius: 110,

                    pointers: [{

                        // For setting pointer border

**border: { color: "green", width: 2 },**

                        // For setting pointer background

                        **backgroundColor: "yellow",**

****// For setting pointer value

****value: 45,

****// For setting pointer length

                        length: 80,

                                                 // For setting pointer width

****  width: 16,

                       // For setting pointer opacity

****opacity: 0.6

                    }]

                }]

            });



 });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                {

                sc1.ShowScaleBar(true)

                   .Radius(110)

                   .Pointers(PO =>

                      {

            // For setting pointer Value

           PO.Value(45)

            // For setting pointer length

            .Length(80)

      // For setting pointer width

      .Width(16)

            // For setting pointer background

           **.BackgroundColor(ConsoleColor.Yellow.ToString())**

           // For setting pointer border

           **.Border(bor =>bor.Color(ConsoleColor.Green.ToString()).Width(2))**

           // For setting pointer opacity

           .Opacity(0.6).Add();

                }).Add();

                })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowScalebar="true" radius="110"&gt;

                &lt;PointerCollection&gt;

&lt;%--For setting pointer width,background color,pointer value,length --%&gt;



                   &lt;ej:Pointers Value="45" width="16" Opacity="0.6" BackgroundColor="yellow" Length="80"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img2.png" Caption="Figure 42: Circular Gauge with customized pointer colors and borders"%}

**Appearance**

* Based on the value, the****pointer point outs the label value. You can set the pointer length and width using **length** and **width** property respectively. Add you can also adjust the opacity of the pointer using the property **opacity** that holds the value between 0 and 1. You can add the gradient effects to the pointer using **gradient** object.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showScaleBar: true,

                    backgroundColor: "orange",

                    border: { width: 2, color: "Red" },

                    width: 10, radius: 110,

                    pointers: [{

                        // For setting pointer border

                        border: { color: "red", width: 2 },

                        // For setting pointer background

****backgroundColor: "orange",

****// For setting pointer value

****value: 45,

****// For setting pointer length

**length: 80,**

                                                 // For setting pointer width

                        **width: 16,**

                       // For setting pointer opacity

                        **opacity: 0.6**

                    }]

                }]

            });



 });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

  {

      sc1.ShowScaleBar(true)

         .Radius(110)

         .BackgroundColor(ConsoleColor.Yellow.ToString())

         .Border(bor =>bor.Color(ConsoleColor.Red.ToString()).Width(2))

         .Pointers(PO =>

         {

           PO.Value(45)

           // For setting pointer background

           .BackgroundColor(ConsoleColor.Yellow.ToString())

           // For setting pointer border

           .Border(bor =>bor.Color(ConsoleColor.Red.ToString()).Width(2))

           // For setting pointer length

            **.Length(80)**

            // For setting pointer width

            **.Width(16)**

            // For setting pointer opacity

           **.Opacity(0.6)**.Add();

                 }).Add();

                })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowscaleBar="true" BackgroundColor="orange" radius="110"&gt;

              &lt;Border Width="2" Color="red" /&gt;

&lt;%--For setting pointer value.length,width and background color--%&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="45" width="16" Opacity="0.6" BackgroundColor="orange" ShowBackNeedle="true" Length="80" BackNeedleLength="0"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img3.png" Caption="Figure 43: Circular Gauge with customized pointer styles"%}

**Position the pointer**

* Pointer can be positioned with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and pointer.  **Placement** property is used to locate the pointer with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type. Both the property is applied only if pointer type is marker. For needle type marker, it renders with default position that is unchangeable.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showScaleBar: true, border: {color: "Blue",width:2},

                    backgroundColor: "#DCEBF9",

                    size: 10,

                    radius: 110,

                    pointers: [{

                        // For setting distance between scale and pointer

**distancFromScale: 20,**

                        // For setting pointer placement

                        **placement: "near",**

****// For setting pointer type

                        **type: "marker",**

                        // For setting marker type

                        **markerType:"triangle",**

                        length: 20,

                        width: 20,

                        value: 40,

                        backgroundColor: "#DCEBF9",

                        border: { color: "Blue", width: 2 },

                    }]

                }]

            });

 });

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

               .Scales(sc1 =>

                {

                    sc1.ShowScaleBar(true)

                       .Size(10)

                       .Radius(110)

                       .BackgroundColor("#DCEBF9")

 .Border(bor=>bor.Color(ConsoleColor.Blue.ToString()).Width(2))

                       .Pointers(PO =>

                      {

                        PO.Value(40)

                          .Length(20)

                          .Width(20)

                          .BackgroundColor("#DCEBF9")

              .Border(bor=>bor.Color(ConsoleColor.Blue.ToString()).Width(2))

              // For setting distance between scale and pointer

             **.DistanceFromScale(10)**

              // For setting pointer placement

             **.Placement(PointerPlacement.Near)**

             // For setting pointer type

             **.Type(PointerType.Marker)**

             // For setting marker type

             **.MarkerType(MarkerType.Triangle)**

             .Add();

                }).Add();

                })

)



**[ASP]**

&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowscaleBar="true" BackgroundColor="#DCEBF9" Size="10" radius="110"&gt;

              &lt;Border Width="2" Color="blue" /&gt;

&lt;%--For setting pointer type,placement,marker type,distance from scale--%&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="40" length="20" width="20" BackgroundColor="#DCEBF9" ShowBackNeedle="true" BackNeedleLength="0" DistanceFromScale="20" Placement="Near" Type="Marker" MarkerType="Triangle"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;


Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img4.png" Caption="Figure 44: Circular Gauge with customized pointer type as marker"%}

Types

Circular gauge pointer has two types such as,

Needle

Marker

Needle type pointers are the default pointers that cannot be positioned and that is located at the center of the gauge. There are four different shapes of needle pointers such as 

Rectangle

Triangle

Trapezoid 

Arrow

For marker pointer, the available dimensions are 

Rectangle

Triangle

Ellipse

Diamond

Pentagon

Circle

Slider

Pointer

Wedge

Trapezoid

Rounded Rectangle

**Multiple Pointers**

**Circular Gauge** can have multiple pointers on it. You can use any combination and any number of pointers in a **Gauge**. That is, a Gauge can contain any number of marker pointer and any number of needle pointers. Refer the following code example containing two pointers.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1").ejCircularGauge({

                scales: [{

                    showScaleBar: true,

                    backgroundColor: "#DCEBF9",

                    border: { width: 2, color: "Green" },

                    width: 10, radius: 110,

                    pointers: [

                        // For setting pointer1

                    {

                        border: { color: "Green", width: 2 },

                        backgroundColor: "#DCEBF9",

                        value: 40,

                        length: 80,

                        width: 16,

                        opacity: 0.6

                    }, 

                       // For setting pointer2

                    {

                        distancFromScale: 20, 

                        placement: "near",

                        type: "marker",

                        markerType: "triangle",

                        length: 20,

                        width: 20,

                        value: 60,

                        backgroundColor: "#DCEBF9",

                        border: { color: "Green", width: 2 },

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

                       .Size(10)

                       .Radius(110)

                       .BackgroundColor("#DCEBF9")

.Border(bor =>bor.Color(ConsoleColor.Green.ToString()).Width(2))

                       .Pointers(PO =>

                      {

                       // For setting pointer1

                        PO.Value(40)

                          .Length(80)

                          .Width(16)

                          .Opacity(0.6)

                          .BackgroundColor("#DCEBF9")

                          .Border(bor =>bor.Color(ConsoleColor.Green.ToString()).Width(2)).Add();

                        // For setting pointer2

                          PO.Placement(PointerPlacement.Near)

                            .Type(PointerType.Marker)

                            .MarkerType(MarkerType.Triangle)

                            .Length(20)

                            .Width(20)

                            .Value(60)

                            .BackgroundColor("#DCEBF9")

                            .Border(bor =>bor.Color(ConsoleColor.Green.ToString()).Width(2)).Add();

                   }).Add();

                })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowscaleBar="true" BackgroundColor="#DCEBF9" Size="10" radius="110"&gt;

              &lt;Border Width="2" Color="green" /&gt;

&lt;%--For setting pointer1--%&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers Value="40" length="80" width="16" Opacity="0.6" BackgroundColor="#DCEBF9" &gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

&lt;%--For setting pointer2--%&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers placement="Near" Type="Marker" distanceFromScale="20"  MarkerType="Triangle" Length="20" Width="20" Value="60" backgroundColor="#DCEBF9"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img5.png" Caption="Figure 45: Circular Gauge with multiple pointers"%}

**Pointer Value Text**

**Gauge Pointer value****text** is used to display the current value of the pointer in the **Circular Gauge** control.

**Positioning the text**

You can position the **Circular Gauge** pointer positioning value with the gauge center position by using the **API** called **distance**. You can Disable/ Enable these pointers value by using the API **showValue.**

**[JavaScript]**

    &lt;div style=”float: left” id=”gauge1”&gt;

    &lt;script type=”text/javascript”&gt;

        $(function () {

        $("#CoreCircularGauge").ejCircularGauge({



                // Setting basic properties

                radius: 100, value: 55, backgroundColor: "transparent",



                // Setting scale values

                scales: [{

                    showRanges: true,



                    // Setting tick properties

                    ticks: [{ height: 0, width: 0 }],



                    // Setting range properties

                    ranges: [

                        { size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },

                        { size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }

                    ],



                    // Setting pointer properties

                    pointers: [{



                        // Setting pointer value text properties

                        pointerValueText: {



                            // enable showValue property

**showValue**: true,



                            // setting distance property

**distance**: 0, 



                            color: "#8c8c8c" }

                    }],

                }],



            });         

         });

    &lt;/script&gt; 





<table>
<tr>
<td>
<b>[Razor]</b>@(Html.EJ().CircularGauge("CoreCircularGauge")        // Setting basic properties        .Radius(100).Value(55).BackgroundColor("transparent")        // Setting scale properties        .Scales(SC =>                {                   // enable ranges                    SC.ShowRanges(true)                      // Setting ticks option                      .Ticks(tic => { tic.Height(0).Width(0).Add(); })                       // Setting range properties                      .Ranges(ran =>                    {                        ran.Size(40).StartValue(0).EndValue(50).BackgroundColor("#1B4279").Border(bor => bor.Color("#1B4279")).Add();                        ran.Size(40).StartValue(50).EndValue(100).BackgroundColor("#91B8F3").Border(bor => bor.Color("#91B8F3")).Add();                    })                     // Setting pointer option                    .Pointers(PO =>                    {                        PO.PointerValueText(po=>                            // enable showValue property                            po.ShowValue(true)                            // setting distance property                            .Distance(10)                            .Color("#8c8c8c"))                        .Add();                    }).Add(); }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        //        // GET: /ToolTip/        public ActionResult Semicircular()        {            return View();        }    }</td></tr>
</table>




**[ASPX]**



// Setting basic properties

&lt;ej:CircularGauge runat="server" ID="CoreCircularGauge" Radius= "100" Value= "55" BackgroundColor= "transparent"&gt;



      // Setting scale properties

       &lt;Scales&gt;

           &lt;ej:CircularScalesShowRanges= "true"&gt;



               // Setting ticks properties

               &lt;TickCollection&gt;

                   &lt;ej:CircularTicks Height= "0" Width= "0"/&gt;

               &lt;/TickCollection&gt;



              // Setting pointers properties

               &lt;PointerCollection&gt;

                   &lt;ej:Pointers&gt;

                       <PointerValueText 

                                  Color="red" 



                                  // setting distance property 

                                  Distance="-5" 



                                  // enable showValue property

                                  ShowValue="true">

                       &lt;/PointerValueText&gt;

                   &lt;/ej:Pointers&gt;

               &lt;/PointerCollection&gt;



              // Setting range properties

               &lt;RangeCollection&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "0" EndValue= "50" BackgroundColor= "#1B4279"&gt;

                       &lt;Border Color= "#1B4279"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "50" EndValue= "100" BackgroundColor= "#91B8F3"&gt;

                       &lt;Border Color="#91B8F3"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

               &lt;/RangeCollection&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

&lt;/ej:CircularGauge&gt;



Run the above code to render the output as follows.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img6.png" Caption="Figure 46: Circular Gauge with pointer value text."%}

**Appearance**

Appearance of the **Circular Gauge****pointer value text** is adjusted by using four properties. Such as **color, angle, autoAngle** and **opacity**.

* **Color** property is used to set the color of the pointer value text.

* **Angle** property is used to set the angle in which the text is displayed.

* **Auto Angle** is used to display the text in certain angle based on pointer position angle.

* **Opacity** is used to customize the brightness of the text. 





**[JavaScript]**

    &lt;div style=”float: left” id=”gauge1”&gt;

    &lt;script type=”text/javascript”&gt;

        $(function () {

        $("#CoreCircularGauge").ejCircularGauge({



                // Setting basic properties

                radius: 100, value: 55, backgroundColor: "transparent",



                // Setting scale values

                scales: [{

                    showRanges: true,



                    // Setting tick properties

                    ticks: [{ height: 0, width: 0 }],



                    // Setting range properties

                    ranges: [

                        { size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },

                        { size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }

                    ],



                    // Setting pointer properties

                    pointers: [{



                        // Setting pointer value text properties

                        pointerValueText: {

                            showValue: true,

                            distance: 0, 



                            // Setting color property

                            color: "Red",



                            // Setting opacity property 

                            opacity:0.7,



                            // Setting angle property

                            angle: 20

                      }

                    }],

                }],



            });         

         });

    &lt;/script&gt; 





<table>
<tr>
<td>
<b>[Razor]</b>@(Html.EJ().CircularGauge("CoreCircularGauge")        // Setting basic properties        .Radius(100).Value(55).BackgroundColor("transparent")        // Setting scale properties        .Scales(SC =>                {                   // enable ranges                    SC.ShowRanges(true)                      // Setting ticks option                      .Ticks(tic => { tic.Height(0).Width(0).Add(); })                       // Setting range properties                      .Ranges(ran =>                    {                        ran.Size(40).StartValue(0).EndValue(50).BackgroundColor("#1B4279").Border(bor => bor.Color("#1B4279")).Add();                        ran.Size(40).StartValue(50).EndValue(100).BackgroundColor("#91B8F3").Border(bor => bor.Color("#91B8F3")).Add();                    })                     // Setting pointer option                    .Pointers(PO =>                    {                        PO.PointerValueText(po=>                            po.ShowValue(true)                            .Distance(10)                            // Setting opacity property                            .Opacity(1)                            // Setting color property                            .Color("Red")                            // Setting auto angle property                            .autoAngle(false)                            // Setting angle property                            .Angle(0)                        .Add();                    }).Add(); }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        //        // GET: /ToolTip/        public ActionResult Semicircular()        {            return View();        }    }</td></tr>
</table>




**[ASPX]**

// Setting basic properties

&lt;ej:CircularGauge runat="server" ID="CoreCircularGauge" Radius= "100" Value= "55" BackgroundColor= "transparent"&gt;



      // Setting scale properties

       &lt;Scales&gt;

           &lt;ej:CircularScalesShowRanges= "true"&gt;



               // Setting ticks properties

               &lt;TickCollection&gt;

                   &lt;ej:CircularTicks Height= "0" Width= "0"/&gt;

               &lt;/TickCollection&gt;



              // Setting pointers properties

               &lt;PointerCollection&gt;

                   &lt;ej:Pointers&gt;

                       <PointerValueText 

                                  Distance="-5" 

                                  ShowValue="true"



                                  // Setting color property

                                  Color="red" 



                                  // Setting opacity property

                                  Opacity= "0.7" 



                                  // Setting angle property

                                  Angle="20" 



                                  // Setting auto angle property

                                  AutoAngle="false" >

                       &lt;/PointerValueText&gt;

                   &lt;/ej:Pointers&gt;

               &lt;/PointerCollection&gt;



              // Setting range properties

               &lt;RangeCollection&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "0" EndValue= "50" BackgroundColor= "#1B4279"&gt;

                       &lt;Border Color= "#1B4279"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "50" EndValue= "100" BackgroundColor= "#91B8F3"&gt;

                       &lt;Border Color="#91B8F3"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

               &lt;/RangeCollection&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

&lt;/ej:CircularGauge&gt;



Run the above code to render the output as follows.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img7.png" Caption="Figure 2: Circular Gauge with customized pointer value text."%}

**Font Options**

Similar to other collection, font option is also available in this pointer value text such as size, fontFamily and fontStyle.



**[JavaScript]**

    &lt;div style=”float: left” id=”gauge1”&gt;

    &lt;script type=”text/javascript”&gt;

        $(function () {

        $("#CoreCircularGauge").ejCircularGauge({



                // Setting basic properties

                radius: 100, value: 55, backgroundColor: "transparent",



                // Setting scale values

                scales: [{

                    showRanges: true,



                    // Setting tick properties

                    ticks: [{ height: 0, width: 0 }],



                    // Setting range properties

                    ranges: [

                        { size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },

                        { size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }

                    ],



                    // Setting pointer properties

                    pointers: [{



                        // Setting pointer value text properties

                        pointerValueText: {

                            showValue: true,

                            distance: 0, 

                            color: "Red", 

                            opacity:0.7,

                            angle: 20

                            //setting font option 

                            font:{

                                 size: "25px",

                                 fontStyle: "Bold",

                                 fontFamily: "Consolas",



                            }

                      }

                    }],

                }],



            });         

         });

    &lt;/script&gt; 



<table>
<tr>
<td>
<b>[Razor]</b>@(Html.EJ().CircularGauge("CoreCircularGauge")        // Setting basic properties        .Radius(100).Value(55).BackgroundColor("transparent")        // Setting scale properties        .Scales(SC =>                {                   // enable ranges                    SC.ShowRanges(true)                      // Setting ticks option                      .Ticks(tic => { tic.Height(0).Width(0).Add(); })                       // Setting range properties                      .Ranges(ran =>                    {                        ran.Size(40).StartValue(0).EndValue(50).BackgroundColor("#1B4279").Border(bor => bor.Color("#1B4279")).Add();                        ran.Size(40).StartValue(50).EndValue(100).BackgroundColor("#91B8F3").Border(bor => bor.Color("#91B8F3")).Add();                    })                     // Setting pointer option                    .Pointers(PO =>                    {                        PO.PointerValueText(po=>                            po.ShowValue(true)                            .Distance(10)                            .Opacity(1)                            .Color("Red")                            .autoAngle(false)                            .Angle(0)                            // Setting font option                            .Font(fo=>fo                                .Size("15px")                                .FontFamily("Arial")                                .FontStyle("Normal")))                        .Add();                    }).Add(); }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        //        // GET: /ToolTip/        public ActionResult Semicircular()        {            return View();        }    }</td></tr>
</table>


**[ASPX]**

// Setting basic properties

&lt;ej:CircularGauge runat="server" ID="CoreCircularGauge" Radius= "100" Value= "55" BackgroundColor= "transparent"&gt;



      // Setting scale properties

       &lt;Scales&gt;

           &lt;ej:CircularScalesShowRanges= "true"&gt;



               // Setting ticks properties

               &lt;TickCollection&gt;

                   &lt;ej:CircularTicks Height= "0" Width= "0"/&gt;

               &lt;/TickCollection&gt;



              // Setting pointers properties

               &lt;PointerCollection&gt;

                   &lt;ej:Pointers&gt;

                       <PointerValueText 

                                  Distance="-5" 

                                  ShowValue="true"

                                  Color="red" 

                                  Opacity= "0.7" 

                                  Angle="20" 

                                  AutoAngle="false" >





                                 // Setting font option 

                                 &lt;Font FontFamily="Arial" FontStyle="Normal" Size="15px"&gt;

                       &lt;/PointerValueText&gt;

                   &lt;/ej:Pointers&gt;

               &lt;/PointerCollection&gt;



              // Setting range properties

               &lt;RangeCollection&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "0" EndValue= "50" BackgroundColor= "#1B4279"&gt;

                       &lt;Border Color= "#1B4279"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

                   &lt;ej:CircularRanges Size= "40" StartValue= "50" EndValue= "100" BackgroundColor= "#91B8F3"&gt;

                       &lt;Border Color="#91B8F3"&gt;&lt;/Border&gt;

                   &lt;/ej:CircularRanges&gt;

               &lt;/RangeCollection&gt;

           &lt;/ej:CircularScales&gt;

       &lt;/Scales&gt;

&lt;/ej:CircularGauge&gt;



Run the above code to render the output as follows.





{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img8.png" Caption="Figure 3: Circular Gauge with customized font option in pointer value text."%}

## Adding Pointer Collection

**Pointer collection** is directly added to the scale object. To add pointer collection in a **Gauge** control refer the following code example.  



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
pointers:[{
value:30
}]
}]
})
});
</script>


{% endhighlight %}

Execute the above code to render the following output.

![C:\Users\karthigeyan\Desktop\q.png](pointers_images\pointers_img9.png)

_Figure_ _41__(a): Circular Gauge with  pointer collection_



## Adding Pointer Value

**Pointer value** is the important element in the **Circular Gauge** that indicates the **Gauge** value. Real purpose of the **Circular Gauge** is based on the pointer value. You can set the pointer value either directly during rendering the control or it can be achieved by public method too.



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
startValue: 20,
endValue: 80,
backgroundColor: "Green",
}],
pointers: [{
**value:30**
}]
}] }); }); </script>


{% endhighlight %}



Execute the above code to render the following output.



![](pointers_images\pointers_img10.png)

_Figure_ _41__(b)__: Circular Gauge with customized pointer value_



## Pointer Styles

**Colors and Border**

* The Pointers border is modified with the object called **border** as in scales. It has two border property called **color** and **width** which are used to customize the border color of the pointer and border width of the pointer. 

* You can set the background color to improve the look of the **Circular Gauge** and you can customize the background color of the scale using **backgroundColor**.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true,
width: 10, radius: 110,
pointers: [{
// For setting pointer border
**border: { color: "green", width: 2 },**
// For setting pointer background
**backgroundColor: "yellow",**
// For setting pointer value
value: 45,
// For setting pointer length
length: 80,
// For setting pointer width
width: 16,
// For setting pointer opacity
opacity: 0.6
}]
}]
});

});
</script>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img11.png" Caption="Figure 42: Circular Gauge with customized pointer colors and borders"%}

**Appearance**

* Based on the value, the****pointer point out the label value. You can set the pointer length and width using **length** and **width** property respectively. 

* And you can also adjust the opacity of the pointer using the property **opacity** which holds the value between 0 and 1. You can add the gradient effects to the pointer using **gradient** object.







{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true,
backgroundColor: "orange",
border: { width: 2, color: "Red" },
width: 10, radius: 110,
pointers: [{
// For setting pointer border
border: { color: "red", width: 2 },
// For setting pointer background
backgroundColor: "orange",
// For setting pointer value
value: 45,
// For setting pointer length
**length: 80,**
// For setting pointer width
**width: 16,**
// For setting pointer opacity
**opacity: 0.6**
}]
}]
});

});
</script>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img12.png" Caption="Figure 43: Circular Gauge with customized pointer styles"%}

**Position the pointer**

* Pointer can be positioned with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and pointer.  **Placement** property is used to locate the pointer with respect to scale either inside the scale or outside the scale or along the scale. 

* It is an enumerable data type. Both the property is applied only if pointer type is marker. For needle type marker, it renders with default position that is unchangeable.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true, border: {color: "Blue",width:2},
backgroundColor: "#DCEBF9",
size: 10,
radius: 110,
pointers: [{
// For setting distance between scale and pointer
**distancFromScale: 20,**
// For setting pointer placement
**placement: "near",**
// For setting pointer type
**type: "marker",**
// For setting marker type
**markerType:"triangle",**
length: 20,
width: 20,
value: 40,
backgroundColor: "#DCEBF9",
border: { color: "Blue", width: 2 },
}]
}]
});
});
</script>


{% endhighlight %}


Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img13.png" Caption="Figure 44: Circular Gauge with customized pointer type as marker"%}

**Types**

* Circular gauge pointer has two types such as,

  * Needle

  * Marker

* Needle type pointers are the default pointers that cannot be positioned and that is located at the center of the gauge. There are four different shapes of needle pointers such as 

  * Rectangle

  * Triangle

  * Trapezoid 

  * Arrow

* For marker pointer, the available dimensions are 

  * Rectangle

  * Triangle

  * Ellipse

  * Diamond

  * Pentagon

  * Circle 

  * Slider

  * Pointer

  * Wedge

  * Trapezoid

  * Rounded Rectangle



## Multiple Pointers

**Circular Gauge** can have multiple pointers on it. You can use any combination and any number of pointers in a **Gauge**. That is, a Gauge can contain any number of marker pointer and any number of needle pointers. Refer the following code example containing two pointers.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
showScaleBar: true,
backgroundColor: "#DCEBF9",
border: { width: 2, color: "Green" },
width: 10, radius: 110,
pointers: [
// For setting pointer1
{
border: { color: "Green", width: 2 },
backgroundColor: "#DCEBF9",
value: 40,
length: 80,
width: 16,
opacity: 0.6
},
// For setting pointer2
{
distancFromScale: 20,
placement: "near",
type: "marker",
markerType: "triangle",
length: 20,
width: 20,
value: 60,
backgroundColor: "#DCEBF9",
border: { color: "Green", width: 2 },
}]
}]
});});
</script>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img14.png" Caption="Figure 45: Circular Gauge with multiple pointers"%}



**Pointer Value Text**

**Gauge Pointer value****text** is used to display the current value of the pointer in the **Circular Gauge** control.

**Positioning the text**

You can position the **Circular Gauge** pointer value with the gauge as center by using the **API** called **distance**. You can Disable/ Enable these pointers value by using the API **showValue.**

{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type=”text/javascript”>
$(function () {
$("#CircularGauge1").ejCircularGauge({

// Setting basic properties
radius: 100, value: 55, backgroundColor: "transparent",

// Setting scale values
scales: [{
showRanges: true,

// Setting tick properties
ticks: [{ height: 0, width: 0 }],

// Setting range properties
ranges: [
{ size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },
{ size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }
],

// Setting pointer properties
pointers: [{

// Setting pointer value text properties
pointerValueText: {

// enable showValue property
**showValue**: true,

// setting distance property
**distance**: 0,

color: "#8c8c8c" }
}],
}],

});
});
</script>


{% endhighlight %}



Run the above code to render the output as follows.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img15.png" Caption="Figure 46: Circular Gauge with pointer value text."%}

## Pointer Value Text

**Gauge Pointer value****text** is used to display the current value of the pointer in the **Circular Gauge** control.

**Positioning the text**

You can position the **Circular Gauge** pointer value with the gauge as center by using the **API** called **distance**. You can Disable/ Enable these pointers value by using the API **showValue.**

{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type=”text/javascript”>
$(function () {
$("#CircularGauge1").ejCircularGauge({

// Setting basic properties
radius: 100, value: 55, backgroundColor: "transparent",

// Setting scale values
scales: [{
showRanges: true,

// Setting tick properties
ticks: [{ height: 0, width: 0 }],

// Setting range properties
ranges: [
{ size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },
{ size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }
],

// Setting pointer properties
pointers: [{

// Setting pointer value text properties
pointerValueText: {

// enable showValue property
**showValue**: true,

// setting distance property
**distance**: 0,

color: "#8c8c8c" }
}],
}],

});
});
</script>


{% endhighlight %}



Run the above code to render the output as follows.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img16.png" Caption="Figure 46: Circular Gauge with pointer value text."%}



## Appearance

Appearance of the **Circular Gauge****pointer value text** is adjusted by using four properties. Such as **color, angle, autoAngle** and **opacity**.

* **Color** property is used to set the color of the pointer value text.

* **Angle** property is used to set the angle in which the text is displayed.

* **Auto Angle** is used to display the text in certain angle based on pointer position angle.

* **Opacity** is used to customize the brightness of the text. 





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type=”text/javascript”>
$(function () {
$("#CircularGauge1").ejCircularGauge({

// Setting basic properties
radius: 100, value: 55, backgroundColor: "transparent",

// Setting scale values
scales: [{
showRanges: true,

// Setting tick properties
ticks: [{ height: 0, width: 0 }],

// Setting range properties
ranges: [
{ size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },
{ size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }
],

// Setting pointer properties
pointers: [{

// Setting pointer value text properties
pointerValueText: {
showValue: true,
distance: 0,

// Setting color property
color: "Red",

// Setting opacity property
opacity:0.7,

// Setting angle property
angle: 20
}
}],
}],

});
});
</script>


{% endhighlight %}





Run the above code to render the output as follows.



{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img17.png" Caption="Figure 2: Circular Gauge with customized pointer value text."%}





## Font Options

Similar to other collection, font option is also available in this pointer value text such as size, fontFamily and fontStyle.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type=”text/javascript”>
$(function () {
$("#CircularGauge1").ejCircularGauge({

// Setting basic properties
radius: 100, value: 55, backgroundColor: "transparent",

// Setting scale values
scales: [{
showRanges: true,

// Setting tick properties
ticks: [{ height: 0, width: 0 }],

// Setting range properties
ranges: [
{ size: 40, startValue: 0, endValue: 50, backgroundColor: "#1B4279", border: { color: "#1B4279" } },
{ size: 40, startValue: 50, endValue: 100, backgroundColor: "#91B8F3", border: { color: "#91B8F3" } }
],

// Setting pointer properties
pointers: [{

// Setting pointer value text properties
pointerValueText: {
showValue: true,
distance: 0,
color: "Red",
opacity:0.7,
angle: 20,
//setting font option
font:{
size: "15px",
fontStyle: "Normal",
fontFamily: "Arial",

}
}
}],
}],

});
});
</script>


{% endhighlight %}



Run the above code to render the output as follows.





{% include image.html url="\js\CircularGauge\concepts-and-features\pointers_images\pointers_img18.png" Caption="Figure 3: Circular Gauge with customized font option in pointer value text."%}









