---
layout: post
title: Orientation
description: orientation
platform: js
control: Toolbar
documentation: ug
---

# Orientation

The **Toolbar** control supports both vertical and horizontal orientations, allowing it to fit into any scenario. The **orientation** property **of Toolbar** defines the orientation in which the control is rendered. Set the value to this property as **enum or string** type. It accepts the following values.

* ej.Orientation.Horizontal or “Horizontal”

* ej.Orientation.Vertical  or “Vertical”

The following section explains you on how to set orientation for the toolbar.

## Horizontal

This property sets the **Toolbar** in **horizontal** orientation. You can refer the following steps to set horizontal orientation for **Toolbar** control.

1. In View, create ul-li list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.


<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ width: "290px", orientation: ej.Orientation.Horizontal });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration                    $("#toolbarcontent").ejToolbar({ width: "290px", orientation: "Horizontal" });    });&lt;/script&gt;</td></tr>
</table>


Build and run the application.

The following screenshot illustrates a **Toolbar** with horizontal orientation.

{% include image.html url="/js/Toolbar/Concepts-and-Features/Orientation_images/Orientation_img1.png" Caption=""%}

_Figure 10: Toolbar with Horizontal Orientation_

## Vertical

This property sets the **Toolbar** in **vertical** orientation. You can refer the following steps to set vertical orientation for **Toolbar** control.

* Create ul-li list of toolbar items and invoke the toolbar helper.

Add the following script in your **HTML** page.


<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ orientation: ej.Orientation.Vertical });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ orientation: "Vertical" });    });&lt;/script&gt;</td></tr>
</table>


Build and run the application.

The following screenshot illustrates a **Toolbar** with vertical orientation.

{% include image.html url="/js/Toolbar/Concepts-and-Features/Orientation_images/Orientation_img2.png" Caption=""%}

_Figure 11: Toolbar with Vertical Orientation_

