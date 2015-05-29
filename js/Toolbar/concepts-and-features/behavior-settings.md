---
layout: post
title: behavior-settings
description: behavior settings
platform: js
control: Toolbar
documentation: ug
---

# Behavior settings

The following are some miscellaneous properties that enables you to change the behavior of **Toolbar** control.

## Enabling Toolbar

The **Toolbar** property **enabled** is used to enable or disable the **Toolbar**. Set the value to this property as **Boolean** type.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="cols-sample-area"&gt;    &lt;div id="toolbarcontent"&gt;        &lt;ul&gt;            &lt;li id="Left" title="Left"&gt;                &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="Center" title="Center"&gt;                &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="Right" title="Right"&gt;                &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="Justify" title="Justify"&gt;                &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;            &lt;/li&gt;        &lt;/ul&gt;        &lt;ul&gt;            &lt;li id="Bold" title="Bold"&gt;                &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="Italic" title="Italic"&gt;                &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="StrikeThrough" title="Strike Through"&gt;                &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;            &lt;/li&gt;            &lt;li id="UndeLine" title="UnderLine"&gt;                &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;            &lt;/li&gt;        &lt;/ul&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ enabled: true });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**Enabled**(true)

&lt;/div&gt;



**[ASPX]**

&lt;div class="cols-sample-area"&gt;

                &lt;ej:Toolbar ID="toolbarcontent" runat="server" Width="290px" Enabled="true"&gt;

                    &lt;Items&gt;

                        &lt;ej:ToolbarItem Id="Left" SpriteCssClass="ToolbarItems LeftAlign_tool" TooltipText="Left"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Center" SpriteCssClass="ToolbarItems CenterAlign_tool" TooltipText="Center"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Right" SpriteCssClass="ToolbarItems RightAlign_tool" TooltipText="Right"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Justify" SpriteCssClass="ToolbarItems Justify_tool" TooltipText="Justify"&gt;&lt;/ej:ToolbarItem&gt;

                    &lt;/Items&gt;

                    &lt;Items&gt;

                        &lt;ej:ToolbarItem Id="Bold" SpriteCssClass="ToolbarItems Bold_tool" TooltipText="Bold"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="Italic" SpriteCssClass="ToolbarItems Italic_tool" TooltipText="Italic"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="StrikeThrough" SpriteCssClass="ToolbarItems StrikeThrough_tool" TooltipText="StrikeThrough"&gt;&lt;/ej:ToolbarItem&gt;

                        &lt;ej:ToolbarItem Id="UnderLine" SpriteCssClass="ToolbarItems Underline_tool" TooltipText="UnderLine"&gt;&lt;/ej:ToolbarItem&gt;

                    &lt;/Items&gt;

                &lt;/ej:Toolbar&gt;

            &lt;/div&gt;



{% highlight css %}

**[CSS]**
<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}

## Hiding Toolbar 

The **Toolbar** property **hide** is used to show or hide the **Toolbar**. Set the value to this property as **Boolean** type.



{% highlight js %}

**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ hide: false true });
    });
</script>


{% endhighlight %}



 **[CSHTML]**

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")).**Hide**(true)

&lt;/div&gt;



**[ASPX]**

&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;

&lt;div class="cols-sample-area"&gt;

    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" Hide="true" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;

&lt;/div&gt;



