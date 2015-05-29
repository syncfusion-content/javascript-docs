---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: Rotator
documentation: ug
---

# Behavior settings

## Enabling rotator

The **“eEnabled”** property enables or disables the **Rotator** control. The default value is ‘**true**’. The value set to this property is **Boolean** type. The **Rotator** items are given directly without data base. It is achieved by **Items** tag under **Rotator**. The properties **Caption** and **Url** can be used inside this items. The tag **RotatorItem** is used to set the **Rotator** items under the tag name **Items**. You can refer the following code example to set this property.

<table>
<tr>
<td>
<b>[HTML]               </b> &lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent" accesskey="e"&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/nature.jpg" title="Nature" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/bird.jpg" title="Beautiful Bird" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/sculpture.jpg" title="Amazing Sculptures" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/seaview.jpg" title="Sea-View" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/snowfall.jpg" title="Snow Fall" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/card.jpg" title="Credit Card" /&gt;&lt;/li&gt;        &lt;li&gt;            &lt;img class="image" src="../images/rotator/night.jpg" title="Colorful Night" /&gt;&lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#slidercontent").ejRotator({ <b>enabled: true</b> });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**Enabled**(true)



**[ASPX]**



&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" Enabled="true"&gt;

&lt;Items&gt;

            &lt;ej:RotatorItem Caption="Nature" Url="../images/rotator/nature.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Beautiful Bird" Url="../images/rotator/bird.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Amazing Sculptures" Url="../images/rotator/sculpture.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Sea-View" Url="../images/rotator/seaview.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Snow Fall" Url="../images/rotator/snowfall.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Credit Card" Url="../images/rotator/card.jpg"&gt;&lt;/ej:RotatorItem&gt;

            &lt;ej:RotatorItem Caption="Colorful Night" Url="../images/rotator/night.jpg"&gt;&lt;/ej:RotatorItem&gt;

        &lt;/Items&gt;

&lt;/ej:Rotator&gt;



## Responsive rotator

The “**isResponsive” enableResize** property resizes the **Rotator** when the browser window is resized. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **isResponsive enableResize: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**EnableResize**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" EnableResize="true" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

## Auto Play

The **Rotator** Items continuously rotate without user interference by enable the **enableAutoPlay** property. The default value is ‘**false’**. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **enableAutoPlay: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**EnableAutoPlay**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" EnableAutoPlay="true" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

## Stop on hover

The **stopOnHover** property pauses the **auto play** while hover on the **Rotator** content. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ enableAutoPlay: true, **stopOnHover: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").EnableAutoPlay(true).**StopOnHover**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" EnableAutoPlay="true" StopOnHover="true" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

## Pager settings

### Pager position

This property specifies the position of the **showPager** in the **Rotator** Item. The default value is ‘**outside**’. The value set to this property is **string** or **enum**. 

* Syncfusion.JavaScript.PagerPosition.BottomLeft

* Syncfusion.JavaScript.PagerPosition.BottomRight

* Syncfusion.JavaScript.PagerPosition.Outside

* Syncfusion.JavaScript.PagerPosition.TopCentre

* Syncfusion.JavaScript.PagerPosition.TopLeft

* Syncfusion.JavaScript.PagerPosition.TopRight





{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({
**pagerPosition: ej.Rotator.PagerPosition.BottomLeft**,
            slideWidth: "630px",
            slideHeight: "350px",
        });
    });
</script>


{% endhighlight %}



**[JS]**

&lt;script type="text/javascript"&gt;

    $(function () {

        // declaration

        $("#slidercontent").ejRotator({ **pagerPosition: "Inside"** });

    });

&lt;/script&gt;



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**PagerPosition**(Syncfusion.JavaScript.PagerPosition.TopLeft)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" PagerPosition="TopLeft" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img1.png" Caption="Figure 610: Rotator control with pager position"%}{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img2.png" Caption="Figure 610: Rotator control with pager position"%}

### Show pager

The **“showPager”**is property turns on or off the **pager** support in the **Rotator** control. The **Pager** is used to navigate the **Rotator** Items. The default value is ‘**true**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ **showPager: false** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**ShowPager**(false)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" ShowPager="false" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;





{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img3.png" Caption="Figure 711: Rotator control with no pager"%}{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img4.png" Caption="Figure 711: Rotator control with no pager"%}

## Show options

### Show play button

The “**showPlayButton**”is property enables play / pause button on **Rotator**. The default value is ‘**false**’. The value set to this property is **Boolean**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "60500px", **showPlayButton: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**ShowPlayButton**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" ShowPlayButton="true" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img5.png" Caption="Figure 812: Rotator control with play button"%}{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img6.png" Caption="Figure 812: Rotator control with play button"%}

### Show navigate button

Thise “**showNavigateButton**” property turns on or off the slide buttons (next and previous) in the **Rotator** Items. Slide buttons are used to navigate the **Rotator** Items. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **showNavigateButton: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**ShowNavigateButton**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" ShowNavigateButton="false" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img7.png" Caption="Figure 913: Rotator control with navigate button"%}{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img8.png" Caption="Figure 913: Rotator control with navigate button"%}

### Show caption

When the **Rotator** Item is an image, you can specify a caption for the **Rotator** Item. The caption text for each **Rotator** Item is set by using the title attribute of the respective **&lt;image&gt;** tag. The caption cannot be displayed when multiple **Rotator** Items are present. The default value is ‘**false**’. The value set to this property is **Boolean**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **showCaption: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**ShowCaption**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" ShowCaption="true" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;





{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img9.png" Caption="Figure 140: Rotator control with caption"%}{% include image.html url="\js\Rotator\concepts-and-features\behavior-settings_images\behavior-settings_img10.png" Caption="Figure 140: Rotator control with caption"%}

