---
layout: post
title: Appearance--Styling
description: appearance & styling
platform: js
control: PivotGrid
documentation: ug
---

# Appearance & Styling

**PivotGrid** control customizes its appearance using user-defined CSS. The custom CSS is applied to the control by referring the **custom theme CSS** next to **ej.widgets.all.min.css** in the view page. You can refer the custom CSS in **default.html** page.


{% highlight html %}

<head>
    <title>PivotGrid Custom theme</title>
    <link href="../themes/default-theme/ej.widgets.all.min.css" rel="stylesheet" type="text/css" />
    <link href="custom-theme**/ej.custom-theme.css**" rel="stylesheet" type="text/css" />
</head>

{% endhighlight %}

{% highlight css %}

/*-----------------------For PivotGrid control definition-----------------*/
.e-pivotgrid table {
    font: 12px Segoe UI !important;
    color: #565656;
    border-collapse: collapse;
    background-color: White;
    cursor: default;
}
.e-pivotgrid th,
.e-pivotgrid td {
    padding: 0 2px 0 3px;
    border: solid 1px;
    border-color: #c4c4c4;
    white-space: nowrap;
    height: 25px;
    font-weight: normal;
}
.e-pivotgrid .value {
    background-color: White;
    text-align: right !important;
    padding: 6px 6px 6px 16px;
}
.e-pivotgrid .summary {
    background-color: aqua;
    color: #565656;
    white-space: nowrap;
    text-align: left;
    font-weight: bold;
}
.e-pivotgrid .colheader,
.e-pivotgrid .rowheader {
    font-weight: bold;
    color: #5c5c5c;
    background: white;
    background-repeat: repeat;
    padding: 6px 16px 6px 2px;
    text-align: left;
    font-style: normal;
}
.e-pivotgrid .colheader:hover,
.e-pivotgrid .rowheader:hover {
    font-weight: bold;
    color: white;
    background: #91aa29;
    background-repeat: repeat;
    padding: 6px 16px 6px 2px;
    text-align: left;
    font-style: normal;
}
.e-pivotgrid .expand,
.e-pivotgrid .collapse {
    content: "";
    background-image: url("../common-images/icons-gray.png");
    background-repeat: no-repeat;
    width: 23px;
    height: 17px;
    display: inline-block;
    cursor: pointer;
}
.e-pivotgrid .expand,
.e-pivotgrid .header-hover-expand {
    background-position: -159px -89px;
}
.e-pivotgrid .collapse,
.e-pivotgrid .header-hover-collapse {
    background-position: -185px -88px;
}
.e-pivotgrid .header-hover-expand,
.e-pivotgrid .header-hover-collapse {
    background-image: url("../common-images/icons-white.png") !important;
    background-repeat: no-repeat;
}
.e-pivotgrid .kpiiconvalue {
    height: 20px;
    background-position: center;
    background-repeat: no-repeat;
}
.e-pivotgrid .kpiuparrow {
    background-image: url("../common-images/olapkpi/up-arrow.png");
}
.e-pivotgrid .kpirightarrow {
    background-image: url("../common-images/olapkpi/right-arrow.png");
}
.e-pivotgrid .kpidownarrow {
    background-image: url("../common-images/olapkpi/down-arrow.png");
    background-position: center center;
}
.e-pivotgrid .kpidiamond {
    background-image: url("../common-images/olapkpi/diamond.png");
    background-position: center center;
}
.e-pivotgrid .kpitriangle {
    background-image: url("../common-images/olapkpi/triangle.png");
    background-position: center center;
}
.e-pivotgrid .kpicircle {
    background-image: url("../common-images/olapkpi/circle.png");
    background-position: center center;
}
.e-pivotgrid .kpiredroad {
    background-image: url("../common-images/olapkpi/red.png");
    background-position: center center;
}
.e-pivotgrid .kpigreenroad {
    background-image: url("../common-images/olapkpi/green.png");
    background-position: center center;
}
.e-pivotgrid .kpiallcolor {
    background-image: url("../common-images/olapkpi/three-color.png");
    background-position: center center;
}
.e-pivotgrid .hyperlinkValueCell {
    color: #0026ff;
    text-decoration: underline;
    cursor: pointer;
}
.e-pivotgrid .hyperlinkHeaderCell {
    text-decoration: underline;
    cursor: pointer;
}
.e-pivotgrid .vScrollPanel {
    background-color: #efefef;
    width: 8px;
    margin-left: 8px;
    display: inline-block;
}
.e-pivotgrid .hScrollPanel {
    background-color: #efefef;
    height: 8px;
    margin-top: 4px;
}
.e-pivotgrid .vScrollThumb {
    width: 6px;
    position: relative;
    top: 1px;
    left: 1px;
    background-color: #cacaca;
}
.e-pivotgrid .hScrollThumb {
    height: 6px;
    position: relative;
    left: 1px;
    top: 1px;
    background-color: #cacaca;
}
.e-pivotgrid .categPageIndicator,
.e-pivotgrid .seriesPageIndicator {
    width: auto;
    background-color: #efefef;
    border: thin solid gray;
    color: #5b5b5b;
    padding: 5px;
    position: absolute;
}
.e-pivotgrid .vScrollThumb:hover,
.e-pivotgrid .hScrollThumb:hover {
    background-color: #909090;
}
.e-pivotgrid .inActive {
    display: none;
}
.e-pivotgrid .dragging {
    background-color: #5e5e5e !important;
}
.progressContainer {
    width: 360px;
    height: 70px;
    border-radius: 10px;
    position: absolute;
    background-color: white;
    box-shadow: 0 0 5px 1px #c4c4c4;
    color: #5c5c5c;
}
.progressBar {
    width: 300px;
    height: 16px;
    top: 25px;
    left: 30px;
    position: absolute;
}
.progressText {
    width: 350px;
    height: 20px;
    top: 0px;
    left: 30px;
    font-size: 16px;
    position: absolute;
}

{% endhighlight %}

{% include image.html url="/js/PivotGrid/Appearance--Styling_images/Appearance--Styling_img1.png" %}

