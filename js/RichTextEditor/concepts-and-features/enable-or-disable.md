---
layout: post
title: enable-or-disable
description: enable or disable
platform: js
control: RichTextEditor
documentation: ug
---

# Enable or disable

You can enable or disable the tool items that are available in the **RTE** toolbar. Intermittently, it is not possible to allow some tool item actions in the editing area. To avoid mistakes in such a situation, you can disable the unnecessary tool items. Later, you can enable the disabled tool items, and when you are not going to use images in your blog you can disable the image tool item by using the “**disableToolbarItem**” method. The following example illustrates how to disable the “**image**” tool.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div class="rte"&gt;<b>        &lt;textarea id="disable_tool"&gt;&lt;/textarea&gt;</b>    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE    var rteobj;    $("#disable_tool").ejRTE();	    rteobj = $("#disable_tool").data("ejRTE");<b>    rteobj.disableToolbarItem("disable_toolimage");</b></td></tr>
</table>


<table>
<tr>
<td>
<b>[_cshtml]</b>\\ Add the following code in your view page.    @{Html.EJ().RTE("rteSample").Width("850px").ContentTemplate(@&lt;p&gt;&lt;/p&gt;).Render(); }</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE with disabled image icon    var rteobj;    $("#disable_tool").ejRTE();    rteobj = $("#disable_tool").data("ejRTE");<b>    rteobj.disableToolbarItem("disable_toolimage");</b></td></tr>
</table>


<table>
<tr>
<td>
[_aspx]\\ Add the following code in your aspx page to render RTE.&lt;ej:RTE ID="rteSample" Width="850" runat="server"&gt;&lt;/ej:RTE&gt;</td></tr>
<tr>
<td>
[JavaScript]\\ Add the following code in your script section to render RTE with disabled insert image icon.    var rteobj;    $("#rteSample").ejRTE();    rteobj = $("#rteSample").data("ejRTE");<b>    rteobj.disableToolbarItem("disable_toolimage");</b></td></tr>
</table>


![](enable-or-disable_images\enable-or-disable_img1.png)

_Figure_ _3__23__5__: Showcase for disable the insert image in toolbar_

