---
title: Setting dimension
description: Setting dimension for Schedule control
platform: js
control: schedule
documentation: ug
keywords: dimension, cell dimension, cell width, cell height 
---
# Setting Dimension

The dimension normally refers to the height and width of the element. With Scheduler, it is possible to set 2 kinds of dimensions.

* Scheduler dimension (Scheduler control height and width)
* Cell dimension (Scheduler cells height and width)

## Scheduler Dimension


The [height](/js/api/ejschedule#members:height) and [width](/js/api/ejschedule#members:width) properties can be defined to set the outer dimension of the Scheduler control.

{% highlight html %}
<!-- HTML element will initialize as a ejSchedule -->

<div id="schedule"></div>

<script>

$(function () {

$("#schedule").ejSchedule({

//Setting dimension of Scheduler

width: "70%",

height: "500px"

});

});

</script>



{% endhighlight %}

N>	The height and width properties accepts both **pixel** and **percentage** values.

## Scheduler Cell Dimensions

### Cell Height

The [cellHeight](/js/api/ejschedule#members:cellheight) property allows the Scheduler to set the height of the cells in pixels. The appointment height in vertical mode changes accordingly as per the cell size within which it renders.

{% highlight html %}


<div id="Schedule1"></div>



<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

cellHeight: "40px",

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

}

});

});

</script>



{% endhighlight %}

N>	In **desktop** mode, the default height value of the cells is set to **20px**, whereas for **mobile** mode – the Scheduler cells are rendered with **40px** by default.

### Cell Width

The [cellWidth](/js/api/ejschedule#members:cellwidth) property allows the Scheduler to set the width of the cells in pixels. The appointment width adjusts based on the cell width of the Scheduler.

{% highlight html %}


<div id="Schedule1"></div>



<script type="text/javascript">

$(function () {

$("#Schedule1").ejSchedule({

currentDate: new Date(2015, 11, 2),

cellWidth: "97px",

appointmentSettings: {

dataSource: [{

Id: 100,

Subject: "Research on Sky Miracles",

StartTime: new Date(2015, 11, 2, 9, 00),

EndTime: new Date(2015, 11, 2, 10, 30)

}]

}

});

});

</script>



{% endhighlight %}

N>	When the **cellHeight** and **cellWidth** properties are set with some specific pixel values, the cell size does not adapt to the responsive behaviour of the Scheduler when it is resized either in desktop/mobile mode.

