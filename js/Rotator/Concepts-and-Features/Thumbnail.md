---
layout: post
title: Thumbnail
description: thumbnail 
platform: js
control: Rotator
documentation: ug
---

# Thumbnail 

This feature implements **Thumbnail** in **Rotator** control. You can view or access any of the **Rotator** items instantly. All the images are given as **Thumb Element** to use this feature. 

The property **showThumbnail** turns on or off **thumbnail support** in the **Rotator** control. **Thumbnail** is used to navigate between slides. **Thumbnail** supports only single slide transition. You must specify the source for **thumbnail** elements through the **thumbnailSourceID** property. The default value is ‘**false**’. The value set to this property is **boolean**. 

The property **thumbnailSourceID** specifies the source for **thumbnail** elements. The default value is **null**. The value set to this property is **object**. 

You can refer the following code example of **Thumbnail** in **Rotator**.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent"&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/green.jpg" title="green" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/snow.jpg" title="snow" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/wheat.jpg" title="wheat" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/tablet.jpg" title="tablet" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/sea.jpg" title="sea" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/bread.jpg" title="bread" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/snowfall.jpg" title="snowfall" /&gt;&lt;/li&gt;    &lt;/ul&gt;    &lt;ul id="thumbElement" style="display: none"&gt;        &lt;li&gt;            &lt;img src="../images/rotator/green.jpg" title="green" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/snow.jpg" title="snow" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/wheat.jpg" title="wheat" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/tablet.jpg" title="tablet" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/sea.jpg" title="sea" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/bread.jpg" title="bread" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/snowfall.jpg" title="snowfall" /&gt;&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({            slideWidth: "600px",            frameSpace: "0px",            displayItemsCount: "1",            slideHeight: "350px",            navigateSteps: "1",            enableResize: true,            pagerPosition: ej.Rotator.PagerPosition.Outside,            <b>showThumbnail: true,</b>            <b>thumbnailSourceID: "thumbElement",</b>            orientation: ej.Orientation.Horizontal,            showPager: false,            enabled: true,            showCaption: false,            allowKeyboardNavigation: true,            showPlayButton: true,            enableAutoPlay: false,            animationType: "slide"        });    });&lt;/script&gt;</td></tr>
</table>


{% include image.html url="/js/Rotator/Concepts-and-Features/Thumbnail_images/Thumbnail_img1.png" Caption="Figure 11: Rotator control with thumb nail"%}

