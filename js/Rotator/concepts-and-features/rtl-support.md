---
layout: post
title: rtl-support
description: rtl support
platform: js
control: Rotator
documentation: ug
---

# RTL Support

This feature supports to change the left-to-right alignment of the **Rotator** to right-to-left (RTL). (I.e.) Sets the **Rotator** to do its actions from right to left. The property **enableRTL** sets the **Rotator** from right to left. The value set to this property is **boolean** type.

{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#slidercontent").ejRotator({ slideWidth: 500, **enableRTL: true** });
    });
</script>


{% endhighlight %}



**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for binding Rotator items.**



@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px").**EnableRTL**(true)



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for rotator items.--%&gt;

&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" EnableRTL="false" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;



