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
To explore those properties, refer [Page Settings](/js/api/ejDiagram#members:pagesettings "Page Settings").

You can also customize the appearance of off-page regions with the property `backgroundColor`.

![](/js/Diagram/Page-Settings_images/Page-Settings_img2.png)

![](/js/Diagram/Page-Settings_images/Page-Settings_img3.png)

### BackgroundImage

The `backgroundImage` property sets one or more background images.

`ImageAlignment`, `Scale`, `Source` are the properties of backgroundImage that customize the image.
 
`ImageAlignment` customize the position of the image over the diagram/node area.To explore the properties, refer [Image Alignment](/js/api/ejDiagram#members:backgroundimage-alignment "Image Alignment").

`Scale` describes how the image can be scaled.For more information, refer [Scale](/js/api/ejDiagram#members:backgroundimage-scale "Scale").

`Source` describes the source path of the image.

The following code illustrates how to customize the page size and the appearance of page and off-page.

{% highlight js %}

$("#diagram").ejDiagram({
	//Sets off-page background
	backgroundColor: "whitesmoke",
		backgroundImage: {alignment:ej.datavisualization.Diagram.ImageAlignment.XMidYMid,scale:ej.datavisualization.Diagram.scaleConstraints.Meet,source:"syncfusion.png"},
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

![](/js/Diagram/Page-Settings_images/Page-Settings_img5.png)

N> When the pageWidth and pageHeight are not specified, the rectangular region that completely fits all nodes and connectors are considered as page size.

## MultiplePage and PageBreaks

When MultiplePage is enabled, size of the page dynamically increases or decreases in multiples of page width and height and completely fits diagram within the page boundaries. Page Breaks is used as a visual guide to see how pages are split into multiple pages.

![](/js/Diagram/Page-Settings_images/Page-Settings_img4.png)

`multiplePage` and `showPageBreak` properties of page settings allow you to enable/disable multiple pages and page breaks respectively.
The following code illustrates how to enable multiple page and page break lines.

{% highlight js %}

$("#diagram").ejDiagram({
	pageSettings: {
		//Enables the multiple page
		multiplePage: true,
		//Enables the page break lines
		showPageBreak: true,
	}
});

{% endhighlight %}

