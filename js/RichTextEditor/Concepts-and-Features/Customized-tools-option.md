---
layout: post
title: Customized-tools-option
description: customized tools option
platform: js
control: RichTextEditor
documentation: ug
---

# Customized tools option

In RichTextEditor, toolbars are customizable. When you want to include a new tool item with new functionality that is not available in the existing **RTE** toolbar items, it is possible to create a new tool item using the custom tool option. The following example illustrates how to insert an **HTML**, **JavaScript**, or **CSS** code in the editing area as a code block. 

Add the following code in your **HTML** page to render **RTE** with new tool item.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div&gt;        &lt;textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px"&gt;&lt;/textarea&gt;        &lt;div id="cutomSourceCode" title="Paste you code and inset to RTE"&gt;            &lt;table&gt;                &lt;tr&gt;                    &lt;td style="width: 100px"&gt;                        Select type :                    &lt;/td&gt;                    &lt;td&gt;                        &lt;div&gt;                            &lt;select id="languageList"&gt;                                <option value="javascript">Java Script</option>                                <option value="text/html">HTML</option>                                <option value="css">CSS</option>                            &lt;/select&gt;                        &lt;/div&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td colspan="2"&gt;                        &lt;textarea id="srcCode" style="width: 550px; height: 250px"&gt;                            &lt;div id="srcArea"&gt;&lt;/div&gt;                        &lt;/textarea&gt;                    &lt;/td&gt;                &lt;/tr&gt;                &lt;tr&gt;                    &lt;td colspan="2"&gt;                        &lt;div class="e-rte-button e-fieldseparate"&gt;                            <button id="src_insert" class="e-rte-btn" tabindex="">Insert</button>                            <button id="src_cancel" class="e-rte-btn" tabindex="">Cancel</button>                        &lt;/div&gt;                    &lt;/td&gt;                &lt;/tr&gt;            &lt;/table&gt;        &lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\ </b>Add the following code in your script section to render <b>RTE</b> and set the action of the new tool item.$(function () {        $("#rteSample").ejRTE({            toolsList: ["customTool"],            tools: {                <b>customTool</b>: [{                    name: "codeInsert",                    tooltip: "Insert code snippets ",                    css: "codeInsert",                    action: function () {                        $("#srcCode").val("").show();                        $("#cutomSourceCode").ejDialog("open");                    }                }]            }        });        var rteObj;        $("#cutomSourceCode").ejDialog({ enableResize: false, enableModal: true, showOnInit: false, width: "auto" }); //dialog initialization        $("#cutomSourceCode").find(".e-rte-btn").ejButton({ click: "allowText" });    });    function click() {        $("#srcCode").val("").show();        $("#cutomSourceCode").ejDialog("open");    }    function allowText() {        rteObj = $("#rteSample").data("ejRTE");        if (this._id == "src_insert") {            rteObj.executeCommand("inserthtml", $("#srcCode")[0].value);        }        $("#cutomSourceCode").ejDialog("close");    }</td></tr>
</table>


The following screenshot demonstrates the functionality of new tool item.

{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Customized-tools-option_images/Customized-tools-option_img1.png" Caption="HTML Code inserted in RTE"%}

### Remove the tool item

In some cases you may have to remove a particular item from existing toolbar item of RTE. It can easily be done by using the property **removeToolBarItem** in **RTE**. Consider a content blog that does not require "insert table" option. In that case, you can remove the “**createTable**” tool item from the toolbar. The following code illustrates how to remove the “**createTable**” tool item from list of toolbars.

Add the following code in your **HTML** page.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div&gt;        &lt;textarea id="rteSample" rows="10" cols="30" style="width: 740px; height: 440px"&gt;&lt;/textarea&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>\\ </b>Add the following code in your script section to render the <b>RTE</b> and remove the “<b>createTable”</b> tool from the toolbar.$("#rteSample").ejRTE();var rteeObj  = $("#rteSample").data("ejRTE");rteeObj.<b>removeToolbarItem</b>("rteSamplecreateTable"); // remove toolbar item</td></tr>
</table>


{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Customized-tools-option_images/Customized-tools-option_img2.png" Caption=" “Create table” tool item removed from RTE toolbar"%}

