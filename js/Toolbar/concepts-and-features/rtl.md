---
layout: post
title: rtl
description: rtl
platform: js
control: Toolbar
documentation: ug
---

# RTL

This feature allows you to change the left-to-right alignment of the **Toolbar** to right-to-left (**RTL**) that sets the **Toolbar** to do its actions from right to left. The **enableRTL** property sets the **Toolbar** from right to left. Set the value to this property as **Boolean** type.



{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px", enableRTL: true });
    });
</script>


{% endhighlight %}



**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**EnableRTL**(true) &lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;ej:Toolbar  ID="editingToolbar" runat="server" EnableRTL="true"&gt;&lt;/ej:Toolbar &gt;



![](rtl_images\rtl_img1.png)

_Figure_ _31__16__: Toolbar from RTL_

