---
layout: post
title: appearance-and-styling-
description: appearance and styling 
platform: js
control: Toolbar
documentation: ug
---

# Appearance and Styling 

## Adjusting Toolbar size

### Height

The **height** property is used to set height of the **Toolbar**. Set the value to this property as **number** or **string** type.

<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ height: 300 });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>                                OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ height: "300px" });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").**Height**("300").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip"))

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Height="100px" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;

### Width

The **width** property is used to set width of the **Toolbar**. Set the value to this property as **number** or **string** type.



<table>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ width: 300 });    });&lt;/script&gt;</td></tr>
<tr>
<td>
<b>                             OR</b><b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ width: "300px" });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").**Width**("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip"))

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;

## Enabling Rounded Corner 

The **showRoundedCorner** property is used to enable rounded corner for **Toolbar**. Set the value to this property as **Boolean** type.



{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ showRoundedCorner: true });
    });
</script>


{% endhighlight %}




**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**ShowRoundedCorner**(true)

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" ShowRoundedCorner="true" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;



![](appearance-and-styling-_images\appearance-and-styling-_img1.png)

_Figure_ _27__12__: ToolBar control with rounded corner_

## Enabling Separator 

The **enableSeparator** property is used to set separator between **Toolbar** items. It separates one or more list items. When you want to separate two set of items, then define them in two separate ‘**ul’** tags and set the value to this property as **Boolean** type.



{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ enableSeparator: true });
    });
</script>


{% endhighlight %}



**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**EnableSeparator**(true)

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

                &lt;ej:Toolbar ID="toolbarcontent" EnableSeparator="true" runat="server" Width="290px" Enabled="true"&gt;

                    &lt;Items&gt;

                        &lt;ej:ToolbarItem Id="Left" SpriteCssClass="ToolbarItems LeftAlign_tool" TooltipText="Left"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Center" SpriteCssClass="ToolbarItems CenterAlign_tool" TooltipText="Center"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Right" SpriteCssClass="ToolbarItems RightAlign_tool" TooltipText="Right"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Justify" SpriteCssClass="ToolbarItems Justify_tool" TooltipText="Justify" IsSeparator="true"&gt;&lt;/ej:ToolbarItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:ToolbarItem Id="Bold" SpriteCssClass="ToolbarItems Bold_tool" TooltipText="Bold"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Italic" SpriteCssClass="ToolbarItems Italic_tool" TooltipText="Italic"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="StrikeThrough" SpriteCssClass="ToolbarItems StrikeThrough_tool" TooltipText="StrikeThrough"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="UnderLine" SpriteCssClass="ToolbarItems Underline_tool" TooltipText="UnderLine"&gt;&lt;/ej:ToolbarItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:Toolbar&gt;

            &lt;/div&gt;



![](appearance-and-styling-_images\appearance-and-styling-_img2.png)

_Figure_ _28__13__: ToolBar control with item separator_

## Themes

You can control the****style and appearance of the **Toolbar** based on **CSS** classes. In order to apply styles to the Toolbar control, you can refer two files - **ej.widgets.core.min.css** and **ej.theme.min.css**. When you refer **ej.widgets.all.min.css** file, it is not necessary to include the files **ej.widgets.core.min.css** and **ej.theme.min.css** in your project**,** as **ej.widgets.all.min.css** is the combination of these two. 

By default, there are 12 themes support available for **Toolbar** control namely

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

## CssClass 

The **cssClass** property is used to set root class for **Toolbar** control theme. Set the value to this property as **string** type.



{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px", cssClass: "gradient-lime" });
    });
</script>


{% endhighlight %}



**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**CssClass**("gradient-lime")&lt;/div&gt;



**[ASPX]**

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" CssClass="gradient-lime" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;



{% highlight css %}

**[CSS]**
<style>
    .gradient-lime {
        background-color: yellowgreen;
    }
</style>


{% endhighlight %}



![](appearance-and-styling-_images\appearance-and-styling-_img3.png)

_Figure_ _29__14__: ToolBar control with cssClass_

