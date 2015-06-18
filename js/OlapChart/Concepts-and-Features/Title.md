---
layout: post
title: Title
description: title
platform: js
control: OLAP Chart
documentation: ug
---

#Title

**Title** is the area on top of the Chart control that displays the text explaining the **OlapChart** data. Title text is displayed in a customizable format. 


##Setting Value To Chart Title

Title property allows you to set the default title for a Chart as follows. 


{% highlight js %}

$("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        title: { text: "OLAP Chart in Essential Studio" }
 });


{% endhighlight %}

{% include image.html url="/js/OlapChart/Concepts-and-Features/Title_images/Title_img1.png" Caption="OLAP Chart Title"%}

##Title Text Customization

You can customize the title text font using **title.font** property.

{% highlight js %}

$(function () {
    $("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",title: { text: "OLAP Chart in Essential Studio" 
},load: "load" });
 });
function load(args) {
        this.model.title.font.size = "30px",
        this.model.title.font.fontStyle = "italic",
        this.model.title.font.fontWeight = "bold"
}

{% endhighlight %}

{% include image.html url="/js/OlapChart/Concepts-and-Features/Title_images/Title_img2.png" Caption="Customizing Chart Title"%}

