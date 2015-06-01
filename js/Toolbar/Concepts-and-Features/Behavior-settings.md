---
layout: post
title: Behavior-settings
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
        $("#toolbarcontent").ejToolbar({ hide: true });
    });
</script>


{% endhighlight %}



