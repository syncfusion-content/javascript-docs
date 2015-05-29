---
layout: post
title: custom-labels
description: custom labels
platform: js
control: Circular Gauge
documentation: ug
---

# Custom labels

Custom labels are the texts that you can usepaste them in any location of the **Gauge**.

**Add Custom label collection**

Custom labels collection is directly added to the scale object. Refer the following code to add custom labels collection in a **Gauge** control.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



            //For circular gauge rendering  

            $("#CircularGauge1").ejCircularGauge({

                scales: [{ showCustomLabels: true

                           customLabels:[{

                                       color: "Red"

                            }]

                }]

            })

        });

&lt;/script&gt;



**[View]**

//For circular gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

        .Scales(sc =>

         {

         sc.CustomLabels(cl =>

         {

         //custom label

         cl.TextAngle(10)

         .Color("Red")

         .Value("CustomLabel1")

         .Font(f =>f.Size("20px").FontFamily("Arial").FontStyle("bold"))

         .Position(p =>p.X(180).Y(100)).Add();

         }).Add();

         })

)



**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

  &lt;ej:CircularGauge runat="server" ID="CircularGauge1"  &gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales showLabels="true"&gt;

&lt;%--custom label --%&gt;

               &lt;CustomLabelCollection&gt;

                   &lt;ej:CircularCustomLabel TextAngle="10" Color="red" Value="CustomLabel1"&gt;

                       &lt;Font Size="20px" FontStyle="bold" FontFamily="arial" /&gt;

                       &lt;Position X="180" Y="100" /&gt;

                   &lt;/ej:CircularCustomLabel&gt;

               &lt;/CustomLabelCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;

**Basic Customization**

* You can customize Customlabels using the properties such as **textAngle**, **color** and **font**. **textAngle** attribute is used to display the custom labels in the specified angles and **color** attribute is used to display the custom labels in specified color. You can use **Value** attribute to set the text value in the customlabels. To display the custom labels, set **showCustomLabels** as ‘true’. To set the location of the custom label in **Circular Gauge**, **location** property is used. By using **x** and **y** axis you can position the custom labels.

Font option is also available on the Customlabels. The basic three properties of fonts such as size, family and style can be achieved by **size**, **fontStyle** and **fontFamily**. 


**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

$("#CircularGauge1").ejCircularGauge({

                scales: [{

                    size: 10,

                    shadowOffset: 10,

                    showCustomLabels: true,

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    customLabels: [{

                        //For setting custom label text angle

**textAngle: 10,**

                        //For setting custom label color

                        **color: "Red",**

                        //For setting custom label value

                        **value: "CustomLabel1",**

                        //For setting custom label font option

                        **font: {**

                            **size: "18px",**

                            **fontFamily: "Arial",**

                            **fontStyle: "bold"**

**}**,

                        position: { x: 180, y: 100 }

                    }]

                }]

            });

});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

        .Scales(sc =>

         {

          sc.Size(2)

          .ShadowOffset(10)

          .ShowRanges(true)

          .ShowScaleBar(true)

          .Radius(150)

          .ShowLabels(true)

          .CustomLabels(cl =>

           {

           //For setting custom label text angle

           **cl.TextAngle(10)**

          //For setting custom label color

          **.Color("Red")**

           //For setting custom label color

           **.Value("CustomLabel1")**

          //For setting custom label font option

          **.Font(f =>f.Size("20px").FontFamily("Arial").FontStyle("bold"))**

          //For setting custom label position

          **.Position(p =>p.X(180).Y(100)).Add();**

          }).Add();

         })

)



**[ASP]**

&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="CircularGauge1"  &gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales size="2" ShadowOffset="10" showRanges="true" ShowScaleBar="true" radius="150" showLabels="true"&gt;

        &lt;%--For setting custom label text angle,color,font option,position--%&gt;

               &lt;CustomLabelCollection&gt;

                   &lt;ej:CircularCustomLabel TextAngle="10" Color="red" Value="CustomLabel1"&gt;

                       &lt;Font Size="20px" FontStyle="bold" FontFamily="arial" /&gt;

                       &lt;Position X="180" Y="100" /&gt;

                   &lt;/ej:CircularCustomLabel&gt;

               &lt;/CustomLabelCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;





Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img1.png" Caption="Figure 58: Circular Gauge with customized custom label"%}

**Multiple Custom Labels**

You can set multiple custom labels in a single **Circular Gauge** by adding an array of custom label objects. Refer the following code example for multiple custom label functionality.



**[JavaScript]**

&lt;script type="text/javascript"&gt;

        $(function () {



       // For Circular Gauge rendering

                     $("#CircularGauge1").ejCircularGauge({

                scales: [{

                    size: 10,

                    shadowOffset: 10,

                    showCustomLabels: true,

                    showRanges: true,

                    showScaleBar: true,

                    radius: 150, size: 2,

                    customLabels: [

                    //custom label1

                    {

                        textAngle: 10,

                        color: "Red",

                        value: "CustomLabel1",

                        font: {

                            size: "18px",

                            fontFamily: "Arial",

                            fontStyle: "bold"

                        },

                        position: { x: 180, y: 100 }

                    }, 

                    //custom label2

                    {

                        textAngle: 10,

                        color: "Green",

                        value: "CustomLabel2",

                        font: {

                            size: "18px",

                            fontFamily: "Arial",

                            fontStyle: "bold"

                        },

                        position: { x: 180, y: 250 }

                    }]





                }]

            });

});

&lt;/script&gt;



**[View]**

// For Circular Gauge rendering

@(Html.EJ().CircularGauge("circulargauge")

        .Scales(sc =>

         {

         sc.Size(2)

        .ShadowOffset(10)

        .ShowRanges(true)

        .ShowScaleBar(true)

        .Radius(150)

        .ShowLabels(true)

        .CustomLabels(cl =>

        {

        //custom label1

        cl.TextAngle(10)

       .Color("Red")

       .Value("CustomLabel1")

       .Font(f =>f.Size("20px").FontFamily("Arial").FontStyle("bold"))

       .Position(p =>p.X(180).Y(100)).Add();

       //custom label2

       cl.TextAngle(10)

       .Color("Green")

       .Value("CustomLabel2")

       .Font(f =>f.Size("20px").FontFamily("Arial").FontStyle("bold"))

       .Position(p =>p.X(180).Y(250)).Add();

       }).Add();

     })

)





**[ASP]**



&lt;%--For Circular Gauge rendering--%&gt;

&lt;ej:CircularGauge runat="server" ID="CircularGauge1"  &gt;

        &lt;Scales&gt;

          &lt;ej:CircularScales size="2" ShadowOffset="10" showRanges="true" ShowScaleBar="true" radius="150" showLabels="true"&gt;

               &lt;CustomLabelCollection&gt;

                   &lt;ej:CircularCustomLabel TextAngle="10" Color="red" Value="CustomLabel1"&gt;

                       &lt;Font Size="20px" FontStyle="bold" FontFamily="arial" /&gt;

                       &lt;Position X="180" Y="100" /&gt;

                   &lt;/ej:CircularCustomLabel&gt;

                   &lt;ej:CircularCustomLabel TextAngle="10" Color="green" Value="CustomLabel2"&gt;

                       &lt;Font Size="20px" FontStyle="bold" FontFamily="arial" /&gt;

                       &lt;Position X="180" Y="250" /&gt;

                   &lt;/ej:CircularCustomLabel&gt;



               &lt;/CustomLabelCollection&gt;

             &lt;/ej:CircularScales&gt;

      &lt;/Scales&gt;

           &lt;/ej:CircularGauge&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img2.png" Caption="Figure 59: Circular Gauge with multiple custom labels"%}

**Outer Custom Label**

* **Outer Custom Label** is used to show custom labels outside the **gauge** control. The **Outer Custom Label** can be positioned with API called **outerCustomLabelPosition.** The value for this API is enumerable type and its possible values are,

1. Right

2. Left

3. Top

4. Bottom

When a custom label is to be displayed as an **Outer Custom Label**, set the API **customLabelType** as Outer. Refer to the following code example to get the **Outer Custom Label**.



**[JavaScript]**



    &lt;div style="float: left" id="Schedule1"&gt;

    &lt;script type="text/javascript"&gt;

        $(function () {

        $("#CircularGauge1").ejCircularGauge({



// Sets outer custom label position.

                    outerCustomLabelPosition: "right",



//Defines the tooltip object.

                    tooltip: {



// Enables the custom label tooltip.

                        showCustomLabelTooltip: true,

                    },



// Customizes the scale options.

                    scales: [{

                        showCustomLabels: true,

                        radius: 130,



// Customizes the custom label options.

                        customLabels: [{

                            value: "Average Speed", 



                            positionType: "outer",

                        }],



// Customizes the pointers options.

                        pointers: [{

                            value: 60,

                            length: 95,

                        }]

                    }]

                });

            });

    &lt;/script&gt; 



<table>
<tr>
<td colspan = "2">
<b>[Razor]</b>@(Html.EJ().CircularGauge("circularGaugeTooltip")//Defines the outer label position.                .OuterLabelPosition(OuterLabelPosition.Right)//Defines the tooltip object.                .Tooltip(ttp=>ttp// Enables the label tooltip.                .ShowLabelTooltip(true)// Enables the custom label tooltip.                .ShowCustomLabelTooltip(true)// Customizes the scale options.                .Scales(SC =>                {                    SC.Radius(130).ShowCustomLabels(true)// Customizes the custom label options.                    .CustomLabels(cl => {                        cl.Value("AverageSpeed").                           PositionType(PositionType.Outer)Add();                    })// Customizes the pointers options.                    .Pointers(PO =>                    {                        PO.Value(60)                        .Length(90).Add();                    }).Add();                }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public ActionResult Print()        {            var DataSource = new ScheduleDataDataContext().DefaultSchedules.ToList();            ViewBag.dataSource = DataSource;            return View();        }</td></tr>
</table>


**[ASPX]**



<ej:circulargauge runat="server" id="circularGaugeTooltip" backgroundcolor="transparent" enableanimation="false" 



&lt;%--Defines the outer label position.--%&gt; 

OuterLabelPosition="Left">



&lt;%-- Defines the tooltip object.--%&gt; 

      <Tooltip 



&lt;%-- Enables the custom label tooltip.--%&gt;

           ShowCustomLabelTooltip="true" 



&lt;%-- Enables the label tooltip.--%&gt; 

               ShowLabelTooltip="true" />



&lt;%-- Customizes the scale options.--%&gt;

                   &lt;Scales&gt;

                       &lt;ej:CircularScales ShowCustomLabels="true"&gt;



&lt;%-- Customizes the pointers options.--%&gt;

                            &lt;PointerCollection&gt;

                                &lt;ej:Pointers Value="60" Length="95" &gt;

                                &lt;/ej:Pointers&gt;

                            &lt;/PointerCollection&gt;



&lt;%-- Customizes the custom label options.--%&gt;

                            &lt;CustomLabelCollection&gt;

                                <ej:CircularCustomLabel Value="Syncfusion"



&lt;%--Sets the custom label position type--%&gt;

                                 PositionType="Outer">

                                &lt;/ej:CircularCustomLabel&gt;

                            &lt;/CustomLabelCollection&gt;

                        &lt;/ej:CircularScales&gt;

                   &lt;/Scales&gt;

        &lt;/ej:circulargauge&gt;



Running the above code examples yield the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img3.png" Caption="Figure 60: Circular gauge with outer custom label."%}

## Adding Custom Label Collection

Custom labels collection is directly added to the scale object. Refer the following code to add custom labels collection in a **Gauge** control.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

//For circular gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{ showCustomLabels: true,
customLabels:[{
color: "Red"
}]
}]
})
});
</script>


{% endhighlight %}



**Basic Customization**

* You can customize Customlabels using the properties such as **textAngle**, **color** and **font**. **textAngle** attribute is used to display the custom labels in the specified angles and **color** attribute is used to display the custom labels in specified color. 

* You can use **Value** attribute to set the text value in the customlabels. To display the custom labels, set **showCustomLabels** as ‘true’. To set the location of the custom label in **Circular Gauge**, **location** property is used. By using **x** and **y** axis you can adjust the position of the custom labels.

* Font option is also available on  Customlabels. The basic three properties of fonts such as size, family and style can be achieved by **size**, **fontStyle** and **fontFamily** attributes. 




{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
size: 10,
shadowOffset: 10,
showCustomLabels: true,
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
customLabels: [{
//For setting custom label text angle
**textAngle: 10,**
//For setting custom label color
**color: "Red",**
//For setting custom label value
**value: "CustomLabel1",**
//For setting custom label font option
**font: {**
**size: "18px",**
**fontFamily: "Arial",**
**fontStyle: "bold"**
**}**,
position: { x: 180, y: 100 }
}]
}]
});
});
</script>


{% endhighlight %}



Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img4.png" Caption="Figure 58: Circular Gauge with customized custom label"%}



## Multiple Custom Labels

You can set multiple custom labels in a single **Circular Gauge** by adding an array of custom label objects. Refer the following code example for multiple custom label functionality.



{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {

// For Circular Gauge rendering
$("#CircularGauge1").ejCircularGauge({
scales: [{
size: 10,
shadowOffset: 10,
showCustomLabels: true,
showRanges: true,
showScaleBar: true,
radius: 150, size: 2,
customLabels: [
//custom label1
{
textAngle: 10,
color: "Red",
value: "CustomLabel1",
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},
position: { x: 180, y: 100 }
},
//custom label2
{
textAngle: 10,
color: "Green",
value: "CustomLabel2",
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},
position: { x: 180, y: 250 }
}]


}]
});
});
</script>


{% endhighlight %}





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img5.png" Caption="Figure 59: Circular Gauge with multiple custom labels"%}



## Outer Custom Label

* **Outer Custom Label** is used to show custom labels outside the **gauge** control. The **Outer Custom Label** can be positioned with API called **outerCustomLabelPosition.** The value for this API is enumerable type and its possible values are,

  * Right

  * Left

  * Top

  * Bottom

* When a custom label is to be displayed as an **Outer Custom Label**, set the API **customLabelType** as Outer. Refer to the following code example to get the **Outer Custom Label**.





{% highlight js %}

**[JavaScript]**
<div id="CircularGauge1"></div>
<script type="text/javascript">
$(function () {
$("#CircularGauge1").ejCircularGauge({

// Sets outer custom label position.
outerCustomLabelPosition: "right",

//Defines the tooltip object.
tooltip: {

// Enables the custom label tooltip.
showCustomLabelTooltip: true,
},

// Customizes the scale options.
scales: [{
showLabels: true,
radius: 130,

// Customizes the custom label options.
customLabels: [{
value: "Average Speed",
position:{x:360, y:30},
color: "Red",
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},

positionType: "outer",
}],

// Customizes the pointers options.
pointers: [{
value: 60,
length: 95,
}]
}]
});
});
</script>


{% endhighlight %}





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\custom-labels_images\custom-labels_img6.png" Caption="Figure 60: Circular gauge with outer custom label."%}











