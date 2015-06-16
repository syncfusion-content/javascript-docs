---
layout: post
title: Orientation
description: orientation
platform: js
control: Rotator
documentation: ug
---

# Orientation

The **Rotator** control supports both vertical and horizontal orientations allowing it to fit into any scenario. The **Rotator** property **orientation** defines the **orientation** where the control is rendered. The value set to this property is **enum or string** type. It accepts the following values.

* ej.Orientation.Horizontal or “Horizontal”

* ej.Orientation.Vertical  or “Vertical”

The following steps explain you how to set **orientation** for the **Rotator**.

## Horizontal

This property sets the **Rotator** in **horizontal** **orientation**. You can refer the following steps to set **horizontal** **orientation** for **Rotator** control.

* In **View**, create ul-li list of **Rotator** items and invoke the **Rotator** helper.

* Add the following script in your **HTML** page.


  {% highlight js %}

  **[JavaScript]**
  
  	<script type="text/javascript">
	    $(function () {
	        // declaration
	        $("#slidercontent").ejRotator({ slideWidth: 500, orientation: ej.Orientation.Horizontal });
	    });
	</script> 


  {% endhighlight %}
  
  
  {% highlight js %}

  **[JavaScript]**
  
  	<script type="text/javascript">
	    $(function () {
	        // declaration
	        $("#slidercontent").ejRotator({ slideWidth: 500, orientation: "Horizontal" });
	    });
	</script>


  {% endhighlight %}


## Vertical

This property sets the **Rotator** in **vertical** **orientation**. You can refer the following steps to set **vertical** **orientation** for **Rotator** control.

* Create ul-li list of **Rotator** items and invoke the **Rotator** helper.

* Add the following script in your **HTML** page.



  {% highlight js %}

  **[JavaScript]**
  	
<script type="text/javascript">
	    $(function () {
	        // declaration
	        $("#slidercontent").ejRotator({ slideWidth: 500, orientation: ej.Orientation.Vertical });
	    });
	</script>

  {% endhighlight %}
  
  
  {% highlight js %}

  **[JavaScript]**
  
<script type="text/javascript">
	    $(function () {
	        // declaration
	        $("#slidercontent").ejRotator({ slideWidth: 500, orientation: "Vertical" });
	    });
	</script>

  {% endhighlight %}

