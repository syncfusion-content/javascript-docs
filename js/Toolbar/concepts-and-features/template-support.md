---
layout: post
title: template-support
description: template support
platform: js
control: Toolbar
documentation: ug
---

# Template Support

Template allows you to insert custom or ASP.NET controls inside the toolbar items. Also you can design simple drop down buttons listing the items and radio button inside the **Toolbar**.

Set the list for **DropDown control** inside a list tag and define this tag as a **Toolbar** item. You can use all simple controls as a **ToolbBar** item. To add RadioButton and DropDownList to **Toolbar**, use the following code example.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="toolbarcontent"&gt;    &lt;ul&gt;        &lt;li&gt;            &lt;div&gt;                &lt;input type="radio" name="small" id="Radio1" /&gt;            &lt;/div&gt;            option        &lt;/li&gt;        &lt;li id="Dropdown" title="Dropdown Control"&gt;            &lt;input id="selectcar" type="text" /&gt;            &lt;div id="cars"&gt;                &lt;ul&gt;                    <li>Audi A4</li>                    <li>Audi A5</li>                    <li>Audi A6</li>                    <li>Audi A7</li>                &lt;/ul&gt;            &lt;/div&gt;        &lt;/li&gt;    &lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        $("#Radio1").ejRadioButton({ checked: false });        $('#selectcar').ejDropDownList({ height: "23px", width: "100px", targetID: "cars", selectedItemIndex: 0 });        $("#toolbarcontent").ejToolbar({ width: "250px", height: "28px" });    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]** 

**/ / Add this code in your CSHTML page and refer local data section for data source**

@Html.EJ().Toolbar("toolbarcontent").Items(s =>

{

    s.Add().ContentTemplate(@&lt;div&gt;



        @Html.EJ().RadioButton("radio1").Checked(false)

    &lt;/div&gt;);

    s.Add().ContentTemplate(@&lt;div&gt;

        @Html.EJ().DropDownList("selectcar").Height("23").Width("100").TargetID("cars").SelectedItemIndex(0)

        &lt;div id="cars"&gt;

            &lt;ul&gt;

                <li>Audi A4</li>

                <li>Audi A5</li>

                <li>Audi A6</li>

                <li>Audi A7</li>

            &lt;/ul&gt;

        &lt;/div&gt;

    &lt;/div&gt;);

})



**[ASPX]**

&lt;ej:Toolbar  ID="toolbarTemplate" Width="250px" Height="28px" runat="server"&gt;

                &lt;Items&gt;

                    &lt;ej:Toolbar Item&gt;

                        &lt;Template&gt;

                            &lt;div class="ctrlradio"&gt;

                                <ej:RadioButton ID="RadioButton1" Name="small" runat="server">option</ej:RadioButton>

                            &lt;/div&gt;

                            &lt;ej:DropDownList ID="selectcar" runat="server" SelectedItemIndex="0" Width="100px" Height="23px"&gt;

                                &lt;Items&gt;

                                    &lt;ej:DropDownListItem Text="Audi A4" Value="Audi A4"&gt;&lt;/ej:DropDownListItem&gt;

                                    &lt;ej:DropDownListItem Text="Audi A5" Value="Audi A5"&gt;&lt;/ej:DropDownListItem&gt;

                                    &lt;ej:DropDownListItem Text="Audi A6" Value="Audi A6"&gt;&lt;/ej:DropDownListItem&gt;

                                    &lt;ej:DropDownListItem Text="Audi A7" Value="Audi A7"&gt;&lt;/ej:DropDownListItem&gt;

                                    &lt;ej:DropDownListItem Text="Audi A8" Value="Audi A8"&gt;&lt;/ej:DropDownListItem&gt;

                                &lt;/Items&gt;

                            &lt;/ej:DropDownList&gt;

                        &lt;/Template&gt;

                    &lt;/ej:Toolbar Item&gt;

                &lt;/Items&gt;

            &lt;/ej:Toolbar &gt;



The following screenshot displays a Toolbar with embedded controls.

![](template-support_images\template-support_img1.png)

_Figure_ _30__15__: Toolbar with Template_

