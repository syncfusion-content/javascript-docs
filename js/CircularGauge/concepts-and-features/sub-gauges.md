---
layout: post
title: sub-gauges
description: sub gauges
platform: js
control: Circular Gauge
documentation: ug
---

# Sub Gauges

A **Circular Gauge** containing another circular gauge is said to be **Sub Gauges**. For makingInorder to make  a sample like watch that has second gauge, minute gauge and hour gauge,. For this type of requirement sub gauges are used.

















**Add sub gauges**

Sub gauge collection is directly added to the scale object. Refer the following code example to add custom sub gauge collection in a **Gauge** control



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ showSubGauges: true

                           subGauges:[{

                                       gaugeID: "Gauge1"

                            }]

                }]

            })

        });

&lt;/script&gt;



**[View]**

@(Html.EJ().CircularGauge("circulargauge")

        .Value(50)

        .Scales(sc =>

         {

         sc.Radius(190)

        //For setting sub gauge

        .SubGauges(sg =>

        {

        sg.ControlID("Subgauge1")

        .Height(200)

        .Width(200)

        .Position(p =>p.X(100).Y(120)).Add();

        }).Add();

        })

)

@(Html.EJ().CircularGauge("Subgauge1")

           .BackgroundColor("Blue")

           .Value(50)

           .Scales(sc=>{sc.Radius(150).Add();})

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;%--For setting sub gauge --%&gt;       

     &lt;ej:CircularGauge  runat="server" ID="Subgauge1" value="50" BackgroundColor="blue"  Radius="150"&gt;&lt;/ej:CircularGauge&gt;



        &lt;ej:CircularGauge runat="server" Value="50" ID="CircularGauge1"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales radius="190"&gt;

                &lt;PointerCollection&gt;

                   &lt;ej:Pointers  Value="0"  length="110"&gt;&lt;/ej:Pointers&gt;

                &lt;/PointerCollection&gt;

                &lt;labelCollection&gt;

                    &lt;ej:CircularLabels type="major" /&gt;

                &lt;/labelCollection&gt;

                &lt;SubGaugeCollection&gt;

                   &lt;ej:SubGauge ControlID="Subgauge1" Height="200"  Width="200"&gt;

                        &lt;Position X="100" Y="120"/&gt;        

                   &lt;/ej:SubGauge&gt;

               &lt;/SubGaugeCollection&gt;



             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



**Basic Customization**

Basic attributes such as **height** and **width** property are used to set height and width of the sub gauge. You can easily position the gauge in another gauge using the **position** object and by giving the **X** and **Y** Coordinates value. **controlID** attribute is used to specify the sub gauge ID.



**[JavaScript]**



$(function () {

          $("#SubGauge1").ejCircularGauge({

                backgroundColor: "Blue",value:50,

                scales: [{

                    radius: 150,

                }]

            });



            $("#CircularGauge1").ejCircularGauge({

                height: 500,value:50, width: 500,

                scales: [{radius:190,

                    subGauges:[{

                        //For setting sub gauge control ID

                        **controlID: "SubGauge1",**

                       //For setting sub gauge height

                        **height:200,**

                       //For setting sub gauge width

                        **width: 200,**

                       //For setting sub gauge position

                        **position: { x: 200, y: 150 }**

                    }]

                }]

            });    });





**[View]**

@(Html.EJ().CircularGauge("circulargauge")

        .Height(500)

        .Width(500)

        .Value(50)

        .Scales(sc =>

        {

        sc.Radius(190)

       .SubGauges(sg =>

       {

        //For setting sub gauge control ID

        **sg.ControlID("Subgauge1")**

        //For setting sub gauge Height

       **.Height(200)**

       //For setting sub gauge width

       **.Width(200)**

       //For setting sub gauge position

       **.Position(p =>p.X(200).Y(150)).Add();**

       }).Add();

       })

)

@(Html.EJ().CircularGauge("Subgauge1")

           .BackgroundColor("Blue")

           .Value(50)

           .Scales(sc=>{sc.Radius(150).Add();})

)



**[ASP]**

****&lt;%--For Circular Gauge rendering--%&gt;

**** &lt;ej:CircularGauge  runat="server" ID="Subgauge1" value="50" BackgroundColor="blue" &gt;

        &lt;/ej:CircularGauge&gt;



        &lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" Value="50"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales radius="190"&gt;



                &lt;SubGaugeCollection&gt;

&lt;%--For enabling animation and setting animation speed--%&gt;

                   &lt;ej:SubGauge ControlID="Subgauge1" Height="200"  Width="200"&gt;

                        &lt;Position X="200" Y="150"/&gt;        

                   &lt;/ej:SubGauge&gt;

               &lt;/SubGaugeCollection&gt;



             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;









Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\sub-gauges_images\sub-gauges_img1.png" Caption="Figure 63: Circular Gauge with sub gauge"%}

**Multiple sub gauges**

You can set multiple sub gauges in a single **Circular Gauge** by adding an array of sub gauge objects. Refer the following code example for multiple sub gauges functionality.



**[JavaScript]**



$(function () {

           $("#SubGauge1").ejCircularGauge({

                backgroundColor: "#f5b43f",

                scales: [{

                    radius: 150

                }]

            });

            $("#SubGauge2").ejCircularGauge({

                backgroundColor: "#f5b43f",

                scales: [{

                    radius: 150

                }]

            });



            $("#CircularGauge1").ejCircularGauge({

                height: 500,

                width: 500,

                scales: [{

                    radius:250,

                    subGauges:[

                    //Sub gauge1

                    {

                        controlID: "SubGauge1",

                        height:200,

                        width: 200,

                        position: { x: 200, y: 150 }

                    }, 

                    //Sub gauge2

                    {

                        controlID: "SubGauge2",

                        height: 200,

                        width: 200,

                        position: { x: 50, y: 200 }

                    }]

                }]

            });    });





**[View]**

@(Html.EJ().CircularGauge("circulargauge")

           .Height(500)

           .Width(500)

           .Scales(sc =>

           {

           sc.Radius(250)

          .SubGauges(sg =>

          {

          //Sub gauge1

           sg.ControlID("Subgauge1")

           .Height(200)

           .Width(200)

           .Position(p =>p.X(200).Y(150)).Add();

           //Sub gauge2

           sg.ControlID("Subgauge2")

           .Height(200)

           .Width(200)

           .Position(p =>p.X(50).Y(200)).Add();

            }).Add();

         })

)

@(Html.EJ().CircularGauge("Subgauge1")

           .BackgroundColor("#f5b43f")

           .Scales(sc => { sc.Radius(150).Add(); })

)

@(Html.EJ().CircularGauge("Subgauge2")

            .BackgroundColor("#f5b43f")

            .Scales(sc => { sc.Radius(150).Add(); })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge  runat="server" ID="Subgauge1"  BackgroundColor="#f5b43f" &gt;

        &lt;/ej:CircularGauge&gt;

        &lt;ej:CircularGauge  runat="server" ID="Subgauge2"  BackgroundColor="#f5b43f" &gt;

        &lt;/ej:CircularGauge&gt;

  &lt;ej:CircularGauge runat="server" ID="CircularGauge1" Height="500" Width="500" &gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales ShowRanges="true"  ShowscaleBar="false" radius="250" Size="5" Maximum="100"&gt;

                &lt;SubGaugeCollection&gt;

&lt;%--subgauge1--%&gt;

                   &lt;ej:SubGauge ControlID="Subgauge1" Height="200"  Width="200"&gt;

                        &lt;Position X="200" Y="150"/&gt;        

                   &lt;/ej:SubGauge&gt;

&lt;%--subgauge2--%&gt;

                    &lt;ej:SubGauge ControlID="Subgauge2" Height="200"  Width="200"&gt;

                        &lt;Position X="50" Y="200"/&gt;        

                    &lt;/ej:SubGauge&gt;

               &lt;/SubGaugeCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\sub-gauges_images\sub-gauges_img2.png" Caption="Figure 64: Circular Gauge with multiple sub gauges"%}

## Adding SubGauges

Sub gauge collection is directly added to the scale object. Refer the following code example to add custom sub gauge collection in a **Gauge** control



{% highlight js %}

**[JavaScript]**

<div id="CircularGauge1"></div>

<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{ showSubGauges: true
subGauges:[{
gaugeID: "Gauge1"
}]
}]
})
});
</script>


{% endhighlight %}



**Basic Customization**

Basic attributes such as **height** and **width** property are used to set height and width of the sub gauge. You can easily position the gauge in another gauge using the **position** object and by giving the **X** and **Y** Coordinates value. **controlID** attribute is used to specify the sub gauge ID.



{% highlight js %}

**[JavaScript]**
<div id=" SubGauge1"></div>
<div id="CircularGauge1"> </div>


<script type="text/javascript">

$(function () {
$("#SubGauge1").ejCircularGauge({
backgroundColor: "Blue",value:50, radius: 110,
scales: [{
radius: 110,
}]
});

$("#CircularGauge1").ejCircularGauge({
height: 500,value:50, width: 500,
scales: [{radius:190,
subGauges:[{
//For setting sub gauge control ID
**controlID: "SubGauge1",**
//For setting sub gauge height
**height:250,**
//For setting sub gauge width
**width: 250,**
//For setting sub gauge position
**position: { x: 150, y: 100 }**
}]
}]
});    });


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\sub-gauges_images\sub-gauges_img3.png" Caption="Figure 63: Circular Gauge with sub gauge"%}



## Multiple SubGauges

You can set multiple sub gauges in a single **Circular Gauge** by adding an array of sub gauge objects. Refer the following code example for multiple sub gauges functionality.





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<div id=" SubGauge1"> </div>
<div id=" SubGauge2"> </div

$(function () {
$("#SubGauge1").ejCircularGauge({
backgroundColor: "#f5b43f",
scales: [{
radius: 150
}]
});
$("#SubGauge2").ejCircularGauge({
backgroundColor: "#f5b43f",
scales: [{
radius: 150
}]
});

$("#CircularGauge1").ejCircularGauge({
height: 500,
width: 500,
scales: [{
radius:250,
subGauges:[
//Sub gauge1
{
controlID: "SubGauge1",
height:200,
width: 200,
position: { x: 200, y: 150 }
},
//Sub gauge2
{
controlID: "SubGauge2",
height: 200,
width: 200,
position: { x: 50, y: 200 }
}]
}]
});    });



{% endhighlight %}





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\sub-gauges_images\sub-gauges_img4.png" Caption="Figure 64: Circular Gauge with multiple sub gauges"%}



