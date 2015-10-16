---
layout: post
title: Title
description: title
platform: js
control: OlapChart
documentation: ug
---

#Title

**Title** is the area on top of the Chart control that displays the text explaining the **OlapChart** data.[Title](/js/api/ejChart#members:title) property allows you to set the default title for a Chart. 


{% highlight js %}

$("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",
    size: {
        height: "460px",
        width: "950px"
    },
    title: {
        text: "OLAP Chart in Essential Studio"
    }
});


{% endhighlight %}

![](/js/OlapChart/Title_images/Title_img1.png) 

##Title Customization

You can customize the title text font using [font](/js/api/ejChart#members:title-font) property.

{% highlight js %}

$(function() {
    $("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        size: {
            height: "460px",
            width: "950px"
        },
        title: {
            text: "OLAP Chart in Essential Studio"
        },
        load: "load"
    });
});

function load(args) {
    this.model.title.font.size = "30px",
        this.model.title.font.fontStyle = "italic",
        this.model.title.font.fontWeight = "bold"
}

{% endhighlight %}

![](/js/OlapChart/Title_images/Title_img2.png) 

