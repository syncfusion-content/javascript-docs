---
layout: post
title: customized-tools-option
description: customized tools option
platform: js
control: RichTextEditor
documentation: ug
---

# Customized tools option

In **Rich Text Editor** RichTextEditor, toolbars are customizable. When you want to include a new tool item with new functionality that is not available in the existing **RTE** toolbar items, it is possible to create a new tool item using the custom tool option. The following example illustrates how to insert an **HTML**, **JavaScript**, or **CSS** code in the editing area as a code block. 

* Add the following code in your **HTML** page to render **RTE** with new tool item.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div&gt;        &lt;textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px"&gt;&lt;/textarea&gt;        &lt;div id="cutomSourceCode" title="Paste you code and inset to RTE"&gt;            &lt;table&gt;                &lt;tr&gt;                    &lt;td style="width: 100px"&gt;                        Select type :                    &lt;/td&gt;                    &lt;td&gt;                        &lt;div&gt;                            &lt;select id="languageList"&gt;                                <option value="javascript">Java Script</option>                                <option value="text/html">HTML</option>                                <option value="css">CSS</option>                            &lt;/select&gt;                        &lt;/div&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td colspan="2"&gt;                        &lt;textarea id="srcCode" style="width: 550px; height: 250px"&gt;                            &lt;div id="srcArea"&gt;&lt;/div&gt;                        &lt;/textarea&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td colspan="2"&gt;                        &lt;div class="e-rte-button e-fieldseparate"&gt;                            <button id="src_insert" class="e-rte-btn" tabindex="">Insert</button>                            <button id="src_cancel" class="e-rte-btn" tabindex="">Cancel</button>                        &lt;/div&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/table&gt;        &lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\ </b>Add the following code in your script section to render <b>RTE</b> and set the action of the new tool item.$(function () {        $("#rteSample").ejRTE({            toolsList: ["customTool"],            tools: {                <b>customTool</b>: [{                    name: "codeInsert",                    tooltip: "Insert code snippets ",                    css: "codeInsert",                    action: function () {                        $("#srcCode").val("").show();                        $("#cutomSourceCode").ejDialog("open");                    }                }]            }        });        var rteObj;        $("#cutomSourceCode").ejDialog({ enableResize: false, enableModal: true, showOnInit: false, width: "auto" }); //dialog initialization        $("#cutomSourceCode").find(".e-rte-btn").ejButton({ click: "allowText" });    });    function click() {        $("#srcCode").val("").show();        $("#cutomSourceCode").ejDialog("open");    }    function allowText() {        rteObj = $("#rteSample").data("ejRTE");        if (this._id == "src_insert") {            rteObj.executeCommand("inserthtml", $("#srcCode")[0].value);        }        $("#cutomSourceCode").ejDialog("close");    }</td></tr>
</table>


<table>
<tr>
<td>
<b>[_cshtml]</b>\\ Add the following code in your view page&lt;div class="rte"&gt;    @*initialization of RTE*@@(Html.EJ().RTE("rteSample").Width("700px").ContentTemplate(@&lt;p&gt;Place the content in this RTE Text area.By Clicking the "AddText" toolbar item in the RTE toolbar,you can add the text at the place of cursor.&lt;/p&gt;).ShowFooter(true)        .Tools(tool => tool.<b>CustomTool</b>(custom =>        {            custom.Name("insert code").Tooltip("Insert Code Snippets").Css("codeInsert").Action("click").Add();        })))    @*Dialog option code for adding the text*@    &lt;div id="cutomSourceCode" title="Paste your content and inset to RTE"&gt;        &lt;table&gt;            &lt;tr&gt;                &lt;td colspan="2"&gt;                    &lt;textarea id="srcCode" style="width: 550px; height: 250px"&gt;                        &lt;div id="srcArea"&gt;&lt;/div&gt;                    &lt;/textarea&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td colspan="2"&gt;                    &lt;div class="e-rte-button e-fieldseparate"&gt;                        <button id="src_insert" class="e-rte-btn" tabindex="">Insert</button>                        <button id="src_cancel" class="e-rte-btn" tabindex="">Cancel</button>                    &lt;/div&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE and set the action of the new tool item.     var rteObj;    $(function () {        $("#cutomSourceCode").ejDialog({ enableResize: false, enableModal: true, showOnInit: false, width: "auto" }); //dialog initialization        $("#cutomSourceCode").find(".e-rte-btn").ejButton({ click: "allowText" });    });    function click() {        $("#srcCode").val("").show();        $("#cutomSourceCode").ejDialog("open"); @*dialog initialization*@        }    function allowText() {        rteObj = $("#rteSample").data("ejRTE");        if (this._id == "src_insert") {            rteObj.executeCommand("inserthtml", $("#srcCode")[0].value); @*add the text in RTE*@            }        $("#cutomSourceCode").ejDialog("close");    }</td></tr>
</table>


<table>
<tr>
<td>
[_aspx]\\ Add the following code in your aspx page.&lt;ej:RTE ID="rteSample" AllowEditing="true" ToolsList="customTool" runat="server"&gt;    &lt;Tools&gt;        &lt;CustomTool&gt;            &lt;ej:CustomTool Action="showDialog" Css="codeInsert" Name="codeInsert" Tooltip="Insert code snippets" /&gt;        &lt;/CustomTool&gt;    &lt;/Tools&gt;&lt;/ej:RTE&gt;&lt;div id="TargetList"&gt;    &lt;ul&gt;        <li>Java Script</li>        <li>HTML</li>        <li>CSS</li>    &lt;/ul&gt;&lt;/div&gt;&lt;ej:Dialog ID="customSourceCode" Title="Paste you code and inset to RTE" ShowOnInit="false" EnableModal="true" Width="596" EnableResize="false" runat="server"&gt;    &lt;DialogContent&gt;        &lt;table&gt;            &lt;tr&gt;                <td style="width: 100px">Select type :&lt;/td&gt;                &lt;td&gt;                    &lt;div&gt;                        &lt;ej:DropDownList ID="languageList" TargetID="TargetList" SelectedItemIndex="0" runat="server" /&gt;                    &lt;/div&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td colspan="2"&gt;                    &lt;textarea id="srcCode" style="width: 550px; height: 250px"&gt;&lt;/textarea&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td colspan="2"&gt;                    &lt;div class="e-rte-button e-fieldseparate"&gt;                        &lt;ej:Button ID="insert" Type="Button" Text="Insert" runat="server" ClientSideOnClick="customBtnClick"&gt;&lt;/ej:Button&gt;                        &lt;ej:Button ID="cancel" Type="Button" Text="Cancel" runat="server" ClientSideOnClick="customBtnClick"&gt;&lt;/ej:Button&gt;                    &lt;/div&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/DialogContent&gt;&lt;/ej:Dialog&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE and set the action of the new tool item.var rteObj;function click() {    $("#srcCode").val("").show();    $("#customSourceCode").ejDialog("open");}function customBtnClick() {    rteObj = $("#rteSample").data("ejRTE");    if (this._id == "src_insert") {        rteObj.executeCommand("inserthtml", $("#srcCode")[0].value);    }    $("#customSourceCode").ejDialog("close");}</td></tr>
</table>


The following screenshot demonstrates the functionality of new tool item.



![](customized-tools-option_images\customized-tools-option_img1.png)

_Figure_ _10__22__: HTML Code inserted in RTE_

### Remove the tool item

In some cases you may have to remove a particular item from existing toolbar item of RTE. It can easily be done by using the property **removeToolBarItem** in **RTE**. Consider a content blog that does not require "insert table" option. In that case, you can remove the “**createTable**” tool item from the toolbar. The following code illustrates how to remove the “**createTable**” tool item from list of toolbars.

* Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div&gt;        &lt;textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px"&gt;&lt;/textarea&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\ </b>Add the following code in your script section to render the <b>RTE</b> and remove the “<b>createTable”</b> tool from the toolbar.            $("#rteSample").ejRTE();		    var rteeObj  = $("#rteSample").data("ejRTE");			rteeObj.<b>removeToolbarItem</b>("rteSamplecreateTable"); // remove toolbar item</td></tr>
</table>


<table>
<tr>
<td>
<b>[_cshtml]</b>\\ Add the following code in your view page.@{Html.EJ().RTE("rteSample").Width("850px").ContentTemplate(@&lt;p&gt;&lt;/p&gt;).Render(); }</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in script section.            $("#rteSample").ejRTE();		    var rteeObj  = $("#rteSample").data("ejRTE");			rteeObj.<b>removeToolbarItem</b>("rteSamplecreateTable"); // remove toolbar item</td></tr>
</table>




<table>
<tr>
<td>
<b>[_aspx]</b>\\ Add the following code in your aspx page. &lt;ej:RTE ID="rteSample" Width="850" runat="server"&gt;&lt;/ej:RTE&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\Add the following code in script section to remove create table tool item.$("#rteSample").ejRTE();var rteeObj = $("#rteSample").data("ejRTE");<b>rteeObj.removeToolbarItem("rteSamplecreateTable"); // remove toolbar item</b></td></tr>
</table>


![](customized-tools-option_images\customized-tools-option_img2.png)

_Figure_ _11__23__: “Create table” tool item removed from RTE toolbar_

