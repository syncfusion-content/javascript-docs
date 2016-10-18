---
layout: post
title: Customize the size and appearance of single or multiple Diagram pages
description: How to customize the size and appearance of the Diagram pages?
platform: js
control: Diagram
documentation: ug
---


# Page Settings 

Page settings enable to customize the appearance, width, and height of the Diagram page.

![](/js/Diagram/Page-Settings_images/Page-Settings_img1.png)

## Page size and appearance

The size and appearance of the Diagram pages can be customized with the `pageSettings` property. 

The `pageWidth` and `pageHeight` properties of page settings define the size of the page. In addition to that, you can customize the appearance of the page with `backgroundImage` and set of appearance specific properties.
To explore those properties, refer [Page Settings](/api/js/ejDiagram#members:pagesettings "Page Settings").

You can also customize the appearance of off-page regions with the property `backgroundColor`.

![](/js/Diagram/Page-Settings_images/Page-Settings_img2.png)

![](/js/Diagram/Page-Settings_images/Page-Settings_img3.png)

N> When the pageWidth and pageHeight are not specified, the rectangular region that completely fits all nodes and connectors are considered as page size.

### BackgroundImage

You can stretch and align the background image anywhere over the diagram area. 
The `source` property of `backgroundImage` allows you to set the path of the image. The `scale` and the `align` properties help to stretch/align the background images.
 
To explore the backgroundImage properties, refer [Background Image](/api/js/ejDiagram#members:backgroundimage "Background Image").


The following code illustrates how to stretch and align the background image.

{% highlight javascript %}

$("#diagram").ejDiagram({
	//Sets off-page background
	backgroundColor: "whitesmoke",
    backgroundImage: {alignment:ej.datavisualization.Diagram.ImageAlignment.XMidYMin, scale:ej.datavisualization.Diagram.scaleConstraints.Meet, source:"airplane.png"},
	pageSettings: {
		//Sets page size
		pageHeight: 500,
		pageWidth: 500,
		//Customizes the appearance of page
		pageBorderWidth: 4,
		pageBackgroundColor: "white",
		pageBorderColor: "lightgray",
		pageMargin: 25,
		showPageBreak: true,
		multiplePage: true,
		pageOrientation: ej.datavisualization.Diagram.PageOrientations.Portrait
	}
});
{% endhighlight %}

## MultiplePage and PageBreaks

When MultiplePage is enabled, size of the page dynamically increases or decreases in multiples of page width and height and completely fits diagram within the page boundaries. Page Breaks is used as a visual guide to see how pages are split into multiple pages.

![](/js/Diagram/Page-Settings_images/Page-Settings_img4.png)

`multiplePage` and `showPageBreak` properties of page settings allow you to enable/disable multiple pages and page breaks respectively.
The following code illustrates how to enable multiple page and page break lines.

{% highlight javascript %}

$("#diagram").ejDiagram({
	pageSettings: {
		//Enables the multiple page
		multiplePage: true,
		//Enables the page break lines
		showPageBreak: true,
	}
});

{% endhighlight %}

## Boundary Constraints

 Diagram provides support to restrict/customize the interactive region, out of which the elements cannot be dragged, resized or rotated. 
 `boundaryConstraints` property of page settings allows you to customize the interactive region. To explore the boundary constraints, refer refer [Boundary Constraints](/api/js/ejDiagram#members:boundaryConstraints "Boundary Constraints").

The following code example illustrates how to define boundaryConstraints.

{% highlight js %}

    //set page setting properties
    $("#Diagram").ejDiagram({
        //sets the boundaryConstraints  
        pageSettings: {
		    //Allows to drag within the diagram content
            boundaryConstraints: ej.datavisualization.Diagram.BoundaryConstraints.Diagram; 
        }
    });
    
{% endhighlight %}