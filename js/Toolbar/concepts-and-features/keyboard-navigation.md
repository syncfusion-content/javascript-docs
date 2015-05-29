---
layout: post
title: keyboard-navigation
description: keyboard navigation
platform: js
control: Toolbar
documentation: ug
---

# Keyboard Navigation

The entire **Toolbar** commands can be accessed through the keyboard by specifying the **Keyboard Shortcut** listed in the following table.

_Table_ _4__: List of keyboard shortcuts_

<table>
<tr>
<td>
<b>Keyboard Shortcut</b></td><td>
<b>Function</b></td></tr>
<tr>
<td>
Alt + j</td><td>
Focuses the control</td></tr>
<tr>
<td>
UP</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Left</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Right</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item.</td></tr>
<tr>
<td>
End</td><td>
Navigates to the ending item.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
</table>


The following code example illustrates shortcuts associated with the **Toolbar** items.



{% highlight js %}

**[HTML]**
<!-- Refer Local Data section for style and data bound for toolbar item -->
**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px" });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#toolbarcontent").focus();
            }
        });
    });
</script>


{% endhighlight %}



 **[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

&lt;div class="cols-sample-area"&gt;    @Html.EJ().Toolbar("toolbarcontent").Width("250").Datasource((IEnumerable<ToolbarLocalBinding>)ViewBag.datasource).ToolbarFields(f => f.ID("IconId").SpriteCssClass("SpriteCss").TooltipText("Tooltip")) 

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;%--Refer Local Data section for style and data bound for toolbar items.--%&gt;&lt;div class="cols-sample-area"&gt;    &lt;ej:Toolbar  ID="toolbarcontent" runat="server" Width="300px" DataIdField="Id" DataTooltipTextField="Tooltip" DataSpriteCssClassField="Css"&gt;&lt;/ej:Toolbar &gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#toolbarcontent").ejToolbar({ Width: "290px" });        //Control focus key        $(document).on("keydown", function (e) {            if (e.altKey && e.keyCode === 74) { // j- key code.                $("#toolbarcontent").focus();            }        });    });&lt;/script&gt;</td></tr>
</table>


![](keyboard-navigation_images\keyboard-navigation_img1.png)

_Figure_ _32__17__: ToolBar control with Keyboard shortcuts_

