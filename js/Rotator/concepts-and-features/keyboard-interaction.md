---
layout: post
title: keyboard-interaction
description: keyboard interaction
platform: js
control: Rotator
documentation: ug
---

# Keyboard interaction

The **Rotator** property **allowKeyboardNavigation** turns on **keyboard****interaction** with the **Rotator** items. You must set this property to ‘**true**’ to access the **keyboard** shortcuts. The default value is ‘**true**’. The value set to this property is **Boolean**.

The entire **Rotator** commands are accessed through the **keyboard** by specifying the **KeyboardShortcut** in the following table.

<table>
<tr>
<td>
<b>KeyboardShortcut	</b></td><td>
<b>Function</b></td></tr>
<tr>
<td>
<b>Alt + j</b></td><td>
Focuses the control</td></tr>
<tr>
<td>
<b>UP</b></td><td>
Navigates up and left.</td></tr>
<tr>
<td>
<b>Down</b></td><td>
Navigates down and right.</td></tr>
<tr>
<td>
<b>Left</b></td><td>
Navigates up and left.</td></tr>
<tr>
<td>
<b>Right</b></td><td>
Navigates down and right.</td></tr>
<tr>
<td>
<b>Home</b></td><td>
Navigates to the starting item.</td></tr>
<tr>
<td>
<b>End</b></td><td>
Navigates to the ending item.</td></tr>
<tr>
<td>
<b>Enter</b></td><td>
Selects the focused item</td></tr>
</table>


You can refer the following code example for **keyboard** navigation.

<table>
<tr>
<td>
<b>[HTML]               </b>&lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent" accesskey="e"&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/nature.jpg" title="Nature" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/bird.jpg" title="Beautiful Bird" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/seaview.jpg" title="Sea-View" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/snowfall.jpg" title="Snow Fall" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/card.jpg" title="Credit Card" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/night.jpg" title="Colorful Night" /&gt;&lt;/li&gt;    &lt;/ul&gt;    &lt;ul id="slide" style="display: none"&gt;        &lt;li&gt;            &lt;img src="../images/rotator/nature.jpg" title="Nature" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/bird.jpg" title="Beautiful Bird" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/seaview.jpg" title="Sea-View" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/snowfall.jpg" title="Snow Fall" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/card.jpg" title="Credit Card" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img src="../images/rotator/night.jpg" title="Colorful Night" /&gt;&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({            slideWidth: "550px",            frameSpace: "0px",            displayItemsCount: "1",            slideHeight: "350px",            navigateSteps: "1",            enableResize: true,            pagerPosition: ej.Rotator.PagerPosition.Outside,            showThumbnail: true,            thumbnailSourceID: "slide",            orientation: ej.Orientation.Horizontal,            enableRTL: true,            showPager: false,            enabled: true,            showCaption: false,            <b>allowKeyboardNavigation: true,</b>            showPlayButton: true,            animationType: "slide",        });        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#slidercontent")[0].focus();            }        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b><b>/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.</b>@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").<b>AllowKeyboardNavigation</b>(true)</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#slidercontent")[0].focus();            }        });    });&lt;/script&gt;</td></tr>
</table>


**[JS]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;script type="text/javascript"&gt;

        $(function () {

            //Control focus key

            $(document).on("keydown", function (e) {

                if (e.altKey && e.keyCode === 74) { // j- key code.

                    $("#slidercontent")[0].focus();

                }

            });

        });

    &lt;/script&gt;



* Add the following code in your **JavaScript** to focus the control.

{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    .e-rotator-wrap .e-thumb .e-thumb-items li img {
        width: 130px;
        height: 82px;
    }
</style>


{% endhighlight %}







{% include image.html url="\js\Rotator\concepts-and-features\keyboard-interaction_images\keyboard-interaction_img1.png" Caption="Figure 2117: Rotator control with keyboard shortcuts"%}{% include image.html url="\js\Rotator\concepts-and-features\keyboard-interaction_images\keyboard-interaction_img2.png" Caption="Figure 2117: Rotator control with keyboard shortcuts"%}









