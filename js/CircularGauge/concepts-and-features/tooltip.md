---
layout: post
title: tooltip
description: tooltip
platform: js
control: Circular Gauge
documentation: ug
---

# Tooltip

* **Tooltip** feature has been added to the **Circular Gauge**. **Circular Gauge** has several elements such as pointers, label, customLabel, scales, etc.  

* There is a need for **Tooltip** feature in the **Circular Gauge** control because whenever the text hides or overrides with other gauge elements, it may not be fully visible. For resolving those problems **Tooltip** feature has been implemented in the **Circular Gauge** control.

**Default Tooltip**

* **Tooltip** has three attributes in it. The first two attributes are for enabling the **Tooltip** for label and custom label in default appearance such as **showLabelTooltip** and **showCustomLabelTooltip**. **ShowLabelTooltip** is to enable the **Tooltip** for labels and **showCustomLabelTooltip** is for enabling the **Tooltip** option for customLabels.



**[JavaScript]**



    &lt;div style=”float: left” id=”Schedule1”&gt;

    &lt;script type=”text/javascript”&gt;

        $(function () {

        $(“#tooltipGauge”).ejCircularGauge({



//Defines the tooltip object.

                    Tooltip: {



//Enables the label tooltip.

                        showLabelTooltip: true,



//Enables the custom label tooltip.

                        showCustomLabelTooltip: true,

                    },



//Customizes the scale options.

                    Scales: [{

                        showCustomLabels: true,

                        radius: 130,



//Customizes the custom label options.

                        customLabels: [{

                            value: “0 9 5 3 4 5”, 

                            position: { x: 180, y: 220 }

                        }],



//Customizes the pointers options.

                        Pointers: [{

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
<b>[Razor]</b>@(Html.EJ().CircularGauge(“circularGaugeTooltip”)//Defines the tooltip object.                .Tooltip(ttp=>ttp// Enables the label tooltip.                .ShowLabelTooltip(true)// Enables the custom label tooltip.                .ShowCustomLabelTooltip(true)//Customizes the scale options.                .Scales(SC =>                {                    SC.Radius(130).ShowCustomLabels(true)//Customizes the custom label options.                    .CustomLabels(cl => {                        cl.Value(“0 9 5 3 4 5”).                           Position(pos => pos.X(250).Y(230)).Add();                    })//Customizes the pointers options.                    .Pointers(PO =>                    {                        PO.Value(60)                        .Length(90).Add();                    }).Add();                }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        //        // GET: /ToolTip/        public ActionResult Tooltip()        {            return View();        }    }</td></tr>
</table>


**[ASPX]**

&lt;ej:circulargauge runat=”server” id=”circularGaugeTooltip” backgroundcolor=”transparent” nableAnimation=”false”&gt;



&lt;%-- Defines the tooltip object.--%&gt; 

      <Tooltip 



&lt;%-- Enables the custom label tooltip.--%&gt;

           ShowCustomLabelTooltip=”true” 



&lt;%-- Enables the label tooltip.--%&gt; 

               ShowLabelTooltip=”true” />



&lt;%-- Customizes the scale options.--%&gt;

                   &lt;Scales&gt;

                       &lt;ej:CircularScales ShowCustomLabels=”true”&gt;



 &lt;%-- Customizes the pointers options.--%&gt;

                            &lt;PointerCollection&gt;

                                &lt;ej:Pointers Value=”60” Length=”95” &gt;

                                &lt;/ej:Pointers&gt;

                            &lt;/PointerCollection&gt;



&lt;%-- Customizes the custom label options.--%&gt;

                            &lt;CustomLabelCollection&gt;

                                &lt;ej:CircularCustomLabel Value=”0 9 5 3 4 5”&gt;

                                    &lt;Position X=”180” Y=”250”/&gt;

                                &lt;/ej:CircularCustomLabel&gt;

                            &lt;/CustomLabelCollection&gt;

                        &lt;/ej:CircularScales&gt;

                   &lt;/Scales&gt;

        &lt;/ej:circulargauge&gt;



Running the above code examples yield the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\tooltip_images\tooltip_img1.png" Caption="Figure 61: Gauge with Default ToolTip"%}

**Tooltip Template**

In **Tooltip** option, you can customize the Tooltip widow by adding the tooltip template on that page by using the API **TemplateID**. Refer to the following code example to know more about Tooltip template.



**[JavaScript]**



****&lt;div id=”Tooltip” style=”height: 60px; display: none;”&gt;

        &lt;div id=”icon”&gt;

            &lt;div id=”eficon”&gt;&lt;/div&gt;

        &lt;/div&gt;

        &lt;div id=”value”&gt;

            &lt;div&gt;

                &lt;label id=”efpercentage”&gt;&nbsp;#label#&lt;/label&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

    &lt;div style=”float: left” id=”Schedule1”&gt;

    &lt;script type=”text/javascript”&gt;

        $(function () {

        $(“#tooltipGauge”).ejCircularGauge({



//Defines the tooltip object.

                    Tooltip: {



// Enables the label tooltip.

                        showLabelTooltip: true,



// Enables the custom label tooltip.

                        showCustomLabelTooltip: true,



// Adds tooltip template.

                        templateID: “Tooltip”

                    },



// Customizes the scale options.

                    Scales: [{

                        showCustomLabels: true,

                        radius: 130,



// Customizes the custom label options.

                        customLabels: [{

                            value: “0 9 5 3 4 5”, 

                            position: { x: 180, y: 220 }

                        }],



// Customizes the pointers options.

                        Pointers: [{

                            value: 60,

                            length: 95,

                        }]

                    }]

                });

            });

    &lt;/script&gt;

    &lt;style type=”text/css”&gt;



// Adds the necessary styles here.



    &lt;/style&gt;



<table>
<tr>
<td>
<b>[Razor]</b>@(Html.EJ().CircularGauge(“circularGaugeTooltip”)//Defines the tooltip object.                .Tooltip(ttp=>ttp// Enables the label tooltip.                .ShowLabelTooltip(true)// Enables the custom label tooltip.                .ShowCustomLabelTooltip(true)// Enables the tooltip template ID.                .TemplateID(“Tooltip”))// Customizes the scale options.                .Scales(SC =>                {                    SC.Radius(130).ShowCustomLabels(true)// Customizes the custom label options.                    .CustomLabels(cl => {                        cl.Value(“0 9 5 3 4 5”).                           Position(pos => pos.X(250).Y(230)).Add();                    })// Customizes the pointers options.                    .Pointers(PO =>                    {                        PO.Value(60)                        .Length(90).Add();                    }).Add();                }))</td></tr>
<tr>
<td>
<b>[Controller]</b>public partial class CircularGaugeController : Controller    {        // GET: /ToolTip/        public ActionResult Tooltip()        {            return View();        }    }</td></tr>
</table>


**[ASPX]**



&lt;ej:circulargauge runat=”server” id=”circularGaugeTooltip” backgroundcolor=”transparent” nableAnimation=”false”&gt;



      &lt;%-- Defines the tooltip object.--%&gt; 

      <Tooltip 



&lt;%-- Enables the custom label tooltip.--%&gt;

           ShowCustomLabelTooltip=”true” 



&lt;%-- Enables the label tooltip.--%&gt; 

               ShowLabelTooltip=”true” 



&lt;%-- Enables the Tooltip Template.--%&gt;

              TemplateID=”Tooltip”/>



&lt;%-- Customizes the scale options.--%&gt;

                   &lt;Scales&gt;

                       &lt;ej:CircularScales ShowCustomLabels=”true”&gt;



&lt;%-- Customizes the pointers options.--%&gt;

                            &lt;PointerCollection&gt;

                                &lt;ej:Pointers Value=”60” Length=”95” &gt;

                                &lt;/ej:Pointers&gt;

                            &lt;/PointerCollection&gt;



&lt;%-- Customizes the custom label options.--%&gt;

                            &lt;CustomLabelCollection&gt;

                                &lt;ej:CircularCustomLabel Value=”0 9 5 3 4 5”&gt;

                                    &lt;Position X=”180” Y=”250”/&gt;

                                &lt;/ej:CircularCustomLabel&gt;

                            &lt;/CustomLabelCollection&gt;

                        &lt;/ej:CircularScales&gt;

                   &lt;/Scales&gt;

        &lt;/ej:circulargauge&gt;


Running the above code yields the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\tooltip_images\tooltip_img2.png" Caption="Figure 62: Circular gauge with tooltip template"%}

## Default Tooltip

* **Tooltip** has three attributes in it. The first two attributes such as **showLabelTooltip** and **showCustomLabelTooltip** are for enabling the **Tooltip** for label as well as custom label in default appearance. 

* **ShowLabelTooltip** is to enable the **Tooltip** for labels and **showCustomLabelTooltip** is for enabling the **Tooltip** option for customLabels.



{% highlight js %}

**[JavaScript]**
<div id="tooltipGauge"></div>
<script type=”text/javascript”>
$(function () {
$(“#tooltipGauge”).ejCircularGauge({

//Defines the tooltip object.
tooltip: {

//Enables the label tooltip.
showLabelTooltip: true,

//Enables the custom label tooltip.
showCustomLabelTooltip: true,
},

//Customizes the scale options.
scales: [{
showLabels: true,
radius: 130,

//Customizes the custom label options.
customLabels: [{
value: "095345",
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},

position: { x: 180, y: 220 }
}],

//Customizes the pointers options.
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

{% include image.html url="\js\CircularGauge\concepts-and-features\tooltip_images\tooltip_img3.png" Caption="Figure 61: Gauge with Default ToolTip"%}



## Tooltip Template

In **Tooltip** option, you can customize the Tooltip window by adding the tooltip template on that page with the help of API **TemplateID**. Refer to the following code example to know more about Tooltip template.



{% highlight js %}

**[JavaScript]**

<div id=”Tooltip” style=”height: 60px; display: none;”>
<div id=”icon”>
<div id=”eficon”></div>
</div>
<div id=”value”>
<div>
<label id=”efpercentage”>&nbsp;#label#</label>
</div>
</div>
</div>
<div id="tooltipGauge"></div>

<script type=”text/javascript”>
$(function () {
$(“#tooltipGauge”).ejCircularGauge({

//Defines the tooltip object.
tooltip: {

// Enables the label tooltip.
showLabelTooltip: true,

// Enables the custom label tooltip.
showCustomLabelTooltip: true,

// Adds tooltip template.
templateID: “Tooltip”
},

// Customizes the scale options.
scales: [{
showLabels: true,
radius: 130,

// Customizes the custom label options.
customLabels: [{
value: “0 9 5 3 4 5”,
font: {
size: "18px",
fontFamily: "Arial",
fontStyle: "bold"
},

position: { x: 180, y: 220 }
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
<style type=”text/css”>

// Adds the necessary styles here.

</style>


{% endhighlight %}


Execute the above code to render the following output.



{% include image.html url="\js\CircularGauge\concepts-and-features\tooltip_images\tooltip_img4.png" Caption="Figure 62: Circular gauge with tooltip template"%}







