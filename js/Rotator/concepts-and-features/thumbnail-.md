---
layout: post
title: thumbnail-
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


**[CSHTML]**

&lt;ul id="slide" style="display: none"&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/green.jpg")" title="Green" /&gt;&lt;/li&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/snow.jpg")" title="Snow" /&gt;&lt;/li&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/wheat.jpg")" title="Wheat" /&gt;&lt;/li&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/tablet.jpg")" title="Tablet" /&gt;&lt;/li&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/sea.jpg")" title="Sea" /&gt;&lt;/li&gt;

    &lt;li&gt;

        &lt;img src="@Url.Content("~/Images/rotator/bread.jpg")" title="Bread" /&gt;&lt;/li&gt;

&lt;/ul&gt;

@Html.EJ().Rotator("slidercontent").Items(itemElement =>

                       {

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;img class="image" src="@Url.Content("~/Images/rotator/green.jpg")" /&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;img class="image" src="@Url.Content("~/Images/rotator/snow.jpg")"/&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;img class="image" src="@Url.Content("~/Images/rotator/wheat.jpg")" /&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;img class="image" src="@Url.Content("~/Images/rotator/tablet.jpg")" /&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;img class="image" src="@Url.Content("~/Images/rotator/bread.jpg")" /&gt;

                           &lt;/div&gt;);

                       }).SlideWidth("600px").SlideHeight("350px").**ShowThumbnail**(true).**ThumbnailSourceID**("slide")          



**[ASPX]**



    <ej:Rotator ID="slidercontent" runat="server"

        SlideWidth="600px"

        FrameSpace="0px"

        DisplayItemCount="1"

        SlideHeight="350px"

        NavigateSteps="1"

        EnableResize="false"

        ShowPager="true"

        Enabled="true"

        ShowCaption="true"

        AllowKeyboardNavigation="true"

        ShowPlayButton="true"

        EnableRTL="true"

        AnimationType="slide"

        ShowThumbnail="true"

        thumbnailSourceID="thumbContent">

        &lt;Items&gt;

            &lt;ej:RotatorItem Caption="Nature" Url="../images/rotator/nature.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Beautiful Bird" Url="../images/rotator/bird.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Amazing Sculptures" Url="../images/rotator/sculpture.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Sea-View" Url="../images/rotator/seaview.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Snow Fall" Url="../images/rotator/snowfall.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Credit Card" Url="../images/rotator/card.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Colorful Night" Url="../images/rotator/night.jpg"&gt;&lt;/ej:RotatorItem&gt;

        &lt;/Items&gt;

        &lt;ThumbItems&gt;

            &lt;ej:ThumbItem Caption="Nature" Url="../images/rotator/nature.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Beautiful Bird" Url="../images/rotator/bird.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Amazing Sculptures" Url="../images/rotator/sculpture.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Sea-View" Url="../images/rotator/seaview.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Snow Fall" Url="../images/rotator/snowfall.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Credit Card" Url="../images/rotator/card.jpg"&gt;&lt;/ej:ThumbItem&gt;

            &lt;ej:ThumbItem Caption="Colorful Night" Url="../images/rotator/night.jpg"&gt;&lt;/ej:ThumbItem&gt;

        &lt;/ThumbItems&gt;

    &lt;/ej:Rotator&gt;



**[CSS]**

&lt;style type="text/css" class="cssStyles"&gt;

    #slidercontent > li .image {

        width: 600px;

        height: 350px;

    }

&lt;/style&gt;



{% include image.html url="\js\Rotator\concepts-and-features\thumbnail-_images\thumbnail-_img1.png" Caption="Figure 151: Rotator control with thumb nail"%}{% include image.html url="\js\Rotator\concepts-and-features\thumbnail-_images\thumbnail-_img2.png" Caption="Figure 151: Rotator control with thumb nail"%}

