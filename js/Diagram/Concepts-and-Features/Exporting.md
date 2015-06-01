---
layout: post
title: Exporting
description: exporting
platform: js
control: Diagram
documentation: ug
---

# Exporting

You can export the Diagram to the following formats.

* JPG

* PNG

* BMP

* SVG

The following code illustrates how to export the diagram as image

{% highlight js %}

[**JS]**

var diagram = $("#DiagramContent").ejDiagram("instance");

//Exports the diagram as an image of JPEG format

diagram.exportDiagram();


{% endhighlight %}



**Exporting options**

Diagram provides support to export the desired region of the diagram to desired formats. 

The following code example illustrates how to export and download the positive region of diagram to JPEG image format.

{% highlight js %}

[**JS]**

var diagram = $("#DiagramContent").ejDiagram("instance");

var options = {
           //Name of the exported file
           fileName: "diagram", 
           //Specifies whether to export as files/data
           mode: "download", 
           //Specifies the region to be exported
           region: "pageSettings", 
           //Format of the exported file
           format: "jpg",
           //Can be set as a rectangle {x,y width, height}
           bounds: { x: 0, y: 0 }, 
           //margin to the exported file/data
           margin: { left: 30 }
           };

//Exports the positivie region of diagram as an image of JPEG format.
diagram.exportDiagram(options);


{% endhighlight %}



**File Name**

Name of the file to be downloaded. By default, the file name is set as “Diagram”.

**Mode**

Diagram provides support to export and download diagram as files. You can also export Diagram as data of ImageURL/SVG formats.

Mode is to specify whether to export diagram as downloadable files or as data. 

Following table illustrates the possible mode options.

_Exporting modes_

<table>
<tr>
<td>
<b>Modes</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Download</td><td>
Exports and downloads diagram as files. </td></tr>
<tr>
<td>
Data</td><td>
Exports diagram as data of formats ImageURL/SVG.</td></tr>
</table>


**Region**

You can export any particular region of the **Diagram**. The region to be exported is based on the region and bounds properties.

Following table illustrates provided diagram regions.

_Diagram Region_

<table>
<tr>
<td>
<b>Region</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Content</td><td>
Only content of the diagram is exported.</td></tr>
<tr>
<td>
PageSettings</td><td>
Export diagram is based on page setting (page size, multiple page, page margin, etc.)</td></tr>
</table>


**Format**

Format is to specify the type/format of the exported file.

It includes jpg, png, bmp and svg.

{% include image.html url="/js/Diagram/Concepts-and-Features/Exporting_images/Exporting_img1.png" Caption=""%}

_Exported diagram_

