---
layout: post
title: Measure-Groups
description: measure groups 
platform: js
control: OLAP Client
documentation: ug
---

### Measure Groups 

In Cube Dimension Browser tree-view can be viewed in a filtered manner through the **Measure Groups** option. This feature allows you to view the list of measure groups and dimensions associated with the selected measure group from the cube.

{% highlight js %}

[JS]

$("#OlapClient").ejOlapClient({url:"../wcf/OlapClientService.svc", enableMeasureGroups:true});



{% endhighlight %}

On selecting a measure group from the drop-down list, the Cube Dimension Browser tree-view displays the related dimensions as follows.

{% include image.html url="/js/OlapClient/Concepts-and-Features/Measure-Groups_images/Measure-Groups_img1.png" Caption="OLAP Client with Measure Groups in a drop-down list"%}

<br/>

{% include image.html url="/js/OlapClient/Concepts-and-Features/Measure-Groups_images/Measure-Groups_img2.png" Caption="OLAP Client with filtered tree-view in Cube Dimension Browser"%}

