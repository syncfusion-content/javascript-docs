---
layout: post
title: image-with-contents-
description: image with contents 
platform: js
control: Rotator
documentation: ug
---

# Image with Contents 

This feature allows you to add text along with the **image** in **Rotator** control. This is achieved by splitting the content into two panels. In the following code example, image is given in the left panel and text is given in the right panel.

<table>
<tr>
<td>
<b>[HTML]           </b>&lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent"&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/tablet.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel blck"&gt;                <div class="contentPanel">Tablet &lt;/div&gt;                &lt;ul&gt;                    <li>A tablet computer, or simply tablet, is a mobile computer with display, circuitry and battery in a single unit.&lt;/li&gt;                    &lt;li&gt;                    Tablets are equipped with sensors, including cameras, microphone, accelerometer and touchscreen,                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/nature.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel"&gt;                <div class="contentPanel">Nature &lt;/div&gt;                &lt;ul&gt;                    <li>The health of the natural environment is critical to the long-term future of the planet</li>                    <li>Nature, in the broadest sense, is equivalent to the natural, physical, or material world or universe.&lt;/li&gt;                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/card.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel credit"&gt;                <div class="contentPanel">Credit card &lt;/div&gt;                &lt;ul&gt;                    <li>A credit card is a payment card issued to users as a system of payment</li>                    <li>It allows the cardholder to pay for goods and services based on the holder's promise to pay for them</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/rose.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel"&gt;                <div class="contentPanel">Rose &lt;/div&gt;                &lt;ul&gt;                    <li>A rose is a woody perennial of the genus Rosa, within the family Rosaceae</li>                    <li>Flowers vary in size and shape and are usually large and showy,                    There are over 100 species                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;        &lt;li&gt;            &lt;div class="leftPanel"&gt;                &lt;img src="../images/rotator/snowfall.jpg" /&gt;            &lt;/div&gt;            &lt;div class="rightPanel rightSide"&gt;                <div class="contentPanel">Snowfall &lt;/div&gt;                &lt;ul&gt;                    <li>Mt. Baker ski area in Washington State has the world record for snowfall at 1,140 inches of snow in the 1998/1999 winter season</li>                    <li>Mt. Baker ski area is located near but not on the real 10,781� Mount Baker</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration            $("#slidercontent").ejRotator({            slideWidth: "60700px",            displayItemsCount: "1",            slideHeight: "300px",            navigateSteps: "1",            enableResize: true,            pagerPosition: ej.Rotator.PagerPosition.Outside,            orientation: ej.Orientation.Horizontal,            showPager: true,            enabled: true,            showCaption: false,            allowKeyboardNavigation: true,            showPlayButton: true,            animationType: "slide",            enableRTL: true,        });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**           

@{Html.EJ().Rotator("sliderContent").Items(itemElement =>

                       {

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;div class="leftPanel"&gt;

                                   &lt;img src="@Url.Content("~/Images/rotator/tablet.jpg")" /&gt;

                               &lt;/div&gt;

                               &lt;div class="rightPanel blck"&gt;

                                   <div class="contentPanel">Tablet &lt;/div&gt;

                                   &lt;ul&gt;

                                       <li>A tablet computer, or simply tablet, is a mobile computer with display, circuitry and battery in a single unit.&lt;/li&gt;

                                       &lt;li&gt;

                                       Tablets are equipped with sensors, including cameras, microphone, accelerometer and touchscreen,

                                   &lt;/ul&gt;

                               &lt;/div&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;div class="leftPanel"&gt;

                                   &lt;img src="@Url.Content("~/Images/rotator/rose.jpg")" /&gt;

                               &lt;/div&gt;

                               &lt;div class="rightPanel"&gt;

                                   <div class="contentPanel">Rose &lt;/div&gt;

                                   &lt;ul&gt;

                                       <li>A rose is a woody perennial of the genus Rosa, within the family Rosaceae</li>

                                       <li>Flowers vary in size and shape and are usually large and showy,

                    There are over 100 species

                                       &lt;/li&gt;

                                   &lt;/ul&gt;

                               &lt;/div&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;div class="leftPanel"&gt;

                                   &lt;img src="@Url.Content("~/Images/rotator/snowfall.jpg")" /&gt;

                               &lt;/div&gt;

                               &lt;div class="rightPanel rightSide"&gt;

                                   <div class="contentPanel">Snowfall &lt;/div&gt;

                                   &lt;ul&gt;

                                       <li>Mt. Baker ski area in Washington State has the world record for snowfall at 1,140 inches of snow in the 1998/1999 winter season</li>

                                       <li>Mt. Baker ski area is located near but not on the real 10,781’ Mount Baker</li>

                                   &lt;/ul&gt;

                               &lt;/div&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;div class="leftPanel"&gt;

                                   &lt;img src="@Url.Content("~/Images/rotator/nature.jpg")" /&gt;

                               &lt;/div&gt;

                               &lt;div class="rightPanel"&gt;

                                   <div class="contentPanel">Nature &lt;/div&gt;

                                   &lt;ul&gt;

                                       <li>The health of the natural environment is critical to the long-term future of the planet</li>

                                       <li>Nature, in the broadest sense, is equivalent to the natural, physical, or material world or universe.&lt;/li&gt;



                                   &lt;/ul&gt;

                               &lt;/div&gt;

                           &lt;/div&gt;);

                           itemElement.Add().ContentTemplate(@&lt;div&gt;

                               &lt;div class="leftPanel"&gt;

                                   &lt;img src="@Url.Content("~/Images/rotator/card.jpg")" /&gt;

                               &lt;/div&gt;

                               &lt;div class="rightPanel credit"&gt;

                                   <div class="contentPanel">Credit card &lt;/div&gt;

                                   &lt;ul&gt;

                                       <li>A credit card is a payment card issued to users as a system of payment</li>

                                       <li>It allows the cardholder to pay for goods and services based on the holder's promise to pay for them</li>



                                   &lt;/ul&gt;

                               &lt;/div&gt;

                           &lt;/div&gt;);

                       }).SlideWidth("700px").SlideHeight("300px").ShowPlayButton(true).Render();}



**[ASPX]**           

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="700px" SlideHeight="300px" ShowPlayButton="true"&gt;

            &lt;Items&gt;

                &lt;ej:RotatorItem&gt;

                    &lt;ContentSection&gt;

                        &lt;div class="leftPanel"&gt;

                            &lt;img src="../images/rotator/tablet.jpg" /&gt;

                        &lt;/div&gt;

                        &lt;div class="rightPanel blck"&gt;

                            <div class="contentPanel">Tablet &lt;/div&gt;

                            &lt;ul&gt;

                                <li>A tablet computer, or simply tablet, is a mobile computer with display, circuitry and battery in a single unit.&lt;/li&gt;

                                &lt;li&gt;

                                Tablets are equipped with sensors, including cameras, microphone, accelerometer and touchscreen,

                            &lt;/ul&gt;

                        &lt;/div&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:RotatorItem&gt;



                &lt;ej:RotatorItem&gt;

                    &lt;ContentSection&gt;

                        &lt;div class="leftPanel"&gt;

                            &lt;img src="../images/rotator/nature.jpg" /&gt;

                        &lt;/div&gt;

                        &lt;div class="rightPanel"&gt;

                            <div class="contentPanel">Nature &lt;/div&gt;

                            &lt;ul&gt;

                                <li>The health of the natural environment is critical to the long-term future of the planet</li>

                                <li>Nature, in the broadest sense, is equivalent to the natural, physical, or material world or universe.&lt;/li&gt;

                            &lt;/ul&gt;

                        &lt;/div&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:RotatorItem&gt;



                &lt;ej:RotatorItem&gt;

                    &lt;ContentSection&gt;

                        &lt;div class="leftPanel"&gt;

                            &lt;img src="../images/rotator/card.jpg" /&gt;

                        &lt;/div&gt;

                        &lt;div class="rightPanel credit"&gt;

                            <div class="contentPanel">Credit card &lt;/div&gt;

                            &lt;ul&gt;

                                <li>A credit card is a payment card issued to users as a system of payment</li>

                                <li>It allows the cardholder to pay for goods and services based on the holder's promise to pay for them</li>



                            &lt;/ul&gt;

                        &lt;/div&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:RotatorItem&gt;

                &lt;ej:RotatorItem&gt;

                    &lt;ContentSection&gt;

                        &lt;div class="leftPanel"&gt;

                            &lt;img src="../images/rotator/rose.jpg" /&gt;

                        &lt;/div&gt;

                        &lt;div class="rightPanel"&gt;

                            <div class="contentPanel">Rose &lt;/div&gt;

                            &lt;ul&gt;

                                <li>A rose is a woody perennial of the genus Rosa, within the family Rosaceae</li>

                                <li>Flowers vary in size and shape and are usually large and showy,

                    There are over 100 species

                                &lt;/li&gt;

                            &lt;/ul&gt;

                        &lt;/div&gt;

                    &lt;/ContentSection&gt;

                &lt;/ej:RotatorItem&gt;



            &lt;/Items&gt;

        &lt;/ej:Rotator&gt;



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li {
        background-color: #9ee8d8;
    }

        #slidercontent > li .leftPanel {
            float: left;
            width: 700px;
            height: 300px;
            padding-right: 0px;
        }

            #slidercontent > li .leftPanel img {
                width: 700px;
                height: 300px;
            }

    #slidercontent .rightPanel {
        background-color: #FFFFFF;
        height: 259px;
        margin-left: 410px;
        margin-top: 21px;
        opacity: 0.5;
        padding-left: 10px;
        position: absolute;
        width: 260px;
    }

        #slidercontent .rightPanel.credit {
            opacity: 0.6;
        }

        #slidercontent .rightPanel.blck {
            background-color: black;
        }

            #slidercontent .rightPanel.blck li {
                color: white;
                list-style: none;
                line-height: 2;
            }

            #slidercontent .rightPanel.blck .contentPanel {
                padding-top: 30px;
                color: white;
            }

        #slidercontent .rightPanel .contentPanel {
            color: #000000;
            font-size: large;
            font-weight: bold;
            left: 16px;
            padding-top: 30px;
            position: relative;
        }

        #slidercontent .rightPanel li {
            color: black;
            list-style: none;
            line-height: 2;
        }

        #slidercontent .rightPanel.rightSide {
            margin-left: 20px;
            background-color: black;
        }

            #slidercontent .rightPanel.rightSide li {
                color: white;
                list-style: none;
                line-height: 2;
            }

            #slidercontent .rightPanel.rightSide .contentPanel {
                padding-top: 30px;
                color: white;
            }

    .rightPanel > ul {
        padding: 6px 17px 17px;
    }
</style>


{% endhighlight %}





{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img1.png" Caption="Figure 162: Rotator control with image and text"%}{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img2.png" Caption="Figure 162: Rotator control with image and text"%}

## Display items

### Display Items count 

This property specifies the number of **Rotator** Items to be displayed. The default value is ‘**1’**. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {

       // declaration        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "200px", **displayItemsCount: 3**,
slideHeight: "165px"
        });
$("#slidercontent").ejRotator({ slideWidth: 500, **displayItemsCount: 3** });
    });
</script>
**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li .image {
        width:200px;
        height:165px;
    }
</style>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**DisplayItemCount**("3")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" DisplayItemCount="2" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img3.png" Caption="Figure 173: Rotator control with display item count"%}{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img4.png" Caption="Figure 173: Rotator control with display item count"%}

### Navigate steps

This property specifies the number of **Rotator** Items to **navigate** on a single click (next/previous/play buttons). The **navigateSteps** property value must be less than or equal to the **displayItemsCount** property value. The default value is ‘**1**’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 2500, slideHeight: 300165, displayItemsCount: 2, **navigateSteps: 2** });
    });
</script>
**[CSS]**
<style type="text/css" class="cssStyles">
    #slidercontent > li .image {
        width:200px;
        height:165px;
    }
</style>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").DisplayItemCount("2").**NavigateSteps**("2")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" DisplayItemCount="2" NavigateSteps="2" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img5.png" Caption="Figure 1148: Rotator control with navigate steps"%}{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img6.png" Caption="Figure 1148: Rotator control with navigate steps"%}

### Start index

This property sets the **index** of the slide that is displayed first. The default value is ‘1’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 500, **startIndex: 4** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**StartIndex**("4")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" StartIndex="4" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img7.png" Caption="Figure 195: Rotator control with start index	"%}{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img8.png" Caption="Figure 195: Rotator control with start index	"%}

### Frame space

This property sets the space between the **Rotator** Items. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", slideHeight: "300px", displayItemsCount: 2, **frameSpace: "30px"** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").DisplayItemCount("2").**FrameSpace**("30px")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" FrameSpace="30px" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

## Animation 

**animationType** property specifies the **Animation** type for the **Rotator** Item. **animationType** options include slide, fastSlide, slowSlide, and other custom easing animationTypes. The default value is ‘**slide**’. The value set to this property is **string**. 

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **animationType: "slowSlide"** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**AnimationType**("fastSlide")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" AnimationType="fastSlide" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

### Animation speed

This property sets the **speed** of slide transition. The default value is ‘**600**’. The value set to this property is **string** or **number**.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **animationSpeed: 3000** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**AnimationSpeed**(2000)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" AnimationSpeed="2000" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

### Delay

This property sets the **delay** between the **Rotator** Items to move after the slide transition. The default value is **500**. The value set to this property is **string** or **number.**

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: "500px", **delay: 5000** });
    });
</script>


{% endhighlight %}

## Theme

**Rotator** control’s style and appearance are controlled based on **CSS****classes**. In order to apply styles to the **Rotator** control, you can refer 2 files namely, **ej.widgets.core.min.css** and **ej.theme.min.css**. When the file **ej.widgets.all.min.css** is referred, then it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these both. 

By default, there are 12 themes support available for **Rotator** control as follows,

* default-theme

* flat-azure-dark

* fat-lime

* flat-lime-dark

* flat-saffron

* flat-saffron-dark

* gradient-azure

* gradient-azure-dark

* gradient-lime

* gradient-lime-dark

* gradient-saffron

* gradient-saffron-dark

### Css class

This property is used to set **root****class** for **Rotator** control theme. The value set to this property is **string** type.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 500, slideHeight: 300, cssClass: "flat-lime" });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**

@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**CssClass**("mycss")



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" CssClass="blue" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;

Add the following code in your **Css**.

{% highlight css %}

**[CSS]**
<style>
    .flat-lime {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}



**[CSS]**

    &lt;style type="text/css"&gt;

        .blue {

            background-color: lightblue;

        }

    &lt;/style&gt;



{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img9.png" Caption="Figure 2016: Rotator control with cssClass"%}{% include image.html url="\js\Rotator\concepts-and-features\image-with-contents-_images\image-with-contents-_img10.png" Caption="Figure 2016: Rotator control with cssClass"%}

