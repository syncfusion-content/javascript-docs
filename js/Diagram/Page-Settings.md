---
layout: post
title: Page-Settings
description: page settings
platform: js
control: Diagram
documentation: ug
---


# Page Settings 

Page settings enables to customize the appearance, width and height of the diagram page.

{% include image.html url="/js/Diagram/Page-Settings_images/Page-Settings_img1.png" %}

## Page size and appearance

The size and appearance of the diagram pages can be customized with the `pageSettings` property. 

The `pageWidth` and `pageHeight` properties of page settings defines the size of the page. In addition to that, you can customize the appearance of the page with a set of appearance specific properties.
To explore those properties, refer [Page Settings](/js/api/ejDiagram "members:pagesettings").

You can also customize the appearance of off-page regions with the property `backgroundColor`.

The following code illustrates how to customize the page size and the appearance of page and off-page.

{% highlight js %}

    $("#diagram").ejDiagram({
        //Set off-page background
        backgroundColor: "whitesmoke",
        pageSettings: {
            //Set page size
            pageHeight: 500,
            pageWidth: 500,
            
            //Customize the appearance of page
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


{% include image.html url="/js/Diagram/Page-Settings_images/Page-Settings_img2.png" %}

{% include image.html url="/js/Diagram/Page-Settings_images/Page-Settings_img3.png" %}

N> If the pageWidth and pageHeight are not specified, the rectangular region that completely fits all nodes and connectors will be considered as page size.

## MultiplePage and PageBreaks

When MultiplePage is enabled, size of the page dynamically increases or decreases in multiples of page width and height and completely fits diagram within the page boundaries. Page Breaks is used as a visual guide to see how pages are split into multiple pages.

{% include image.html url="/js/Diagram/Page-Settings_images/Page-Settings_img4.png" %}

`multiplePage` and `showPageBreak` properties of page settings allow you to enable/disable multiple pages and page breaks respectively.
The following code illustrates how to enable multiple page and page break lines.

{% highlight js %}

      $("#diagram").ejDiagram({      
            pageSettings: {            
                  //Enable the multiple page            
                  multiplePage: true,            
                  //Enable the page break lines            
                  showPageBreak: true,                  
            }      
      });

{% endhighlight %}

