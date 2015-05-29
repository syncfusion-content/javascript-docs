---
layout: post
title: ticks
description: ticks
platform: js
control: Circular Gauge
documentation: ug
---

# Ticks

Ticks are used to mark some values on the scale. Based on the tick’s value you can set the labels on the required position.

**Add tick collection** 

Tick collection is directly added to the scale object. Refer the following code example to add tick collection in a **Gauge** control.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ 

                           ticks:[{

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

                 sc1.Ticks(tc =>

                   {

                   // For setting tick

                   tc.Type(CircularTickTypes.Major).Color("Red").Add();

                   }).Add();

               })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

       &lt;Scales&gt;

           &lt;ej:CircularScales&gt;

                &lt;TickCollection&gt;

                    &lt;ej:CircularTicks Type="major" Color="red" /&gt;

                &lt;/TickCollection&gt;

          &lt;/ej:CircularScales&gt;           

      &lt;/Scales&gt;

       &lt;/ej:CircularGauge&gt;

**Tick Customization**

Height and width of the ticks can be applied by using the properties **height** and **width**. You can customize ticks with the properties such as angle, color, etc. **angle** attribute is used to display the labels in the specified angles and **color** attribute is used to display the labels in specified color. Ticks are two types such as major and minor.

Major type ticks are for major interval values and minor type ticks are for minor interval values.

* You can position ticks with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and ticks.  **Placement** property is used to locate the ticks with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                      $("#CircularGauge1"). ejCircularGauge ({

                     scales: [{

                    ticks: [

                          // For setting tick1

                            { **type: "major",color:"Red" },**   

                          // For setting tick2

                            **{**

****// For setting tick type

                              **type:"minor",**

                              // For setting tick color****

                              **color:"yellow",**

                              // For setting tick height

                              **height:8,**

                              // For setting tick placement

                              **placement: "near",**

                              // For setting tick distance from scale

                              **distanceFromScale:5**}]



                }]                     

      });

});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

 .Scales(sc1 =>

 {

  sc1.Ticks(tc =>

 {

 // For setting tick1

 **tc.Type(CircularTickTypes.Major).Color("Red").Add();**

 // For setting tick2

 **tc.Type(CircularTickTypes.Minor)**

 // For setting tick color

 **.Color("Yellow")**

 // For setting tick height

 **.Height(8)**

 // For setting tick placement

 **.Placement(TickPlacement.Near)**

 // For setting tick distance from scale

 **.DistanceFromScale(5).Add();**

    }).Add();

      })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="ScaleCircularGauge"&gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales &gt;

                &lt;TickCollection&gt;

&lt;%--For setting tick1--%&gt;

                    &lt;ej:CircularTicks Type="major" Color="red" placement="Near"  DistanceFromScale="5"/&gt;

&lt;%--For setting tick2--%&gt;

                    &lt;ej:CircularTicks Type="minor" Color="yellow" placement="Near" DistanceFromScale="5"/&gt;

                &lt;/TickCollection&gt;

          &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;


Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\ticks_images\ticks_img1.png" Caption="Figure 49: Circular Gauge with tick customization"%}

## Adding Tick Collection 

Tick collection is directly added to the scale object. Refer the following code example to add tick collection in a **Gauge** control.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
ticks:[{
value:30
}]
}]
})  }); </script>


{% endhighlight %}

Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\ticks_images\ticks_img2.png" Caption="Figure 49(a): Circular Gauge with tick collection"%}



## Tick Customization

* Height and width of the ticks can be applied by using the properties **height** and **width**. You can customize ticks with the properties such as angle, color, etc. **angle** attribute is used to display the labels in the specified angles and **color** attribute is used to display the labels in specified color. Ticks are two types such as major and minor.

* Major type ticks are for major interval values and minor type ticks are for minor interval values.You can position ticks with the help of two properties such as **distanceFromScale** and **placement**. **distanceFromScale** property defines the distance between the scale and ticks.  **Placement** property is used to locate the ticks with respect to scale either inside the scale or outside the scale or along the scale. It is an enumerable data type.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1"). ejCircularGauge ({
scales: [{
ticks: [
// For setting tick1
{ **type: "major",color:"Red" },**
// For setting tick2
**{**
// For setting tick type
**type:"minor",**
// For setting tick color
**color:"yellow",**
// For setting tick height
**height:8,**
// For setting tick placement
**placement: "near",**
// For setting tick distance from scale
**distanceFromScale:5**}]

}]
});
});
</script>


{% endhighlight %}




Execute the above code to render the following output.



![](ticks_images\ticks_img3.png)

Figure 49(b): Circular Gauge with tick customization



