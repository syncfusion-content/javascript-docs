---
layout: post
title: title
description: title
platform: js
control: OLAP Chart
documentation: ug
---

# Title

**Title** is the area on top of the Chart control that displays the text explaining the **OlapChart** data. Title text is displayed in a customizable format. 

**Setting value to Chart Title**

Title property allows you to set the default title for a Chart as follows. 



{% highlight js %}

**[JS]**
$("#OlapChart1").ejOlapChart({
        url: "../wcf/OlapChartService.svc",
        title: { text: "OLAP Chart in Essential Studio" }
 });


{% endhighlight %}

{% include image.html url="\js\OlapChart\concepts-and-features\title_images\title_img1.png" Caption="Figure: OLAP Chart Title"%}

**Title Text Customization** 

You can customize the title text font using **title.font** property.

{% highlight js %}

**[JS]**
$(function () {
    $("#OlapChart1").ejOlapChart({
    url: "../wcf/OlapChartService.svc",title: { text: "OlapChart in Essential Studio" 
},load: "load" });
 });
function load(args) {
        this.model.title.font.size = "30px",
        this.model.title.font.fontStyle = "italic",
        this.model.title.font.fontWeight = "bold"
}



{% endhighlight %}



{% include image.html url="\js\OlapChart\concepts-and-features\title_images\title_img2.png" Caption="Figure: Customizing Chart Title"%}

