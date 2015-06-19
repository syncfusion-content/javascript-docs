---
layout: post
title: Modal-Dialog-Support
description: modal dialog support
platform: js
control: Dialog
documentation: ug
---

# Modal Dialog Support

The modal dialog is used like an alert window that disables the main window and explore its content for the purpose of interacting with others. 

## Configure Modal Dialog

The following steps explains you the implementation of modal dialog. 

1. In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="dialogLoginForm" title="Login Form"&gt;        &lt;table&gt;            &lt;tr&gt;                <td>User Name                  &lt;input type="text" id="txtName" class="ejinputtext" style="width: 100%" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                <td>Password                  &lt;input type="text" id="Text1" class="ejinputtext" style="width: 100%" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td align="center"&gt;                    &lt;input type="button" id="downloadBtn" value="Login" class="e-btn" style="width: 100px; height: 30px" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td align="center"&gt;                    <a href="#">Forgot Password</a>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set <b>enableModal</b> property as true in the <b>Dialog</b> function. The default value of <b>enableModal</b> is <b>false</b> in the <b>Dialog</b> widget    &lt;script type="text/javascript"&gt;        $("#dialogLoginForm").ejDialog({            width: 250,            height: 250,            <b>enableModal: true</b>        });      &lt;/script&gt;</td></tr>
</table>


2. The output of modal dialog control. 

{% include image.html url="/js/Dialog/Concepts-and-Features/Modal-Dialog-Support_images/Modal-Dialog-Support_img1.png" Caption="Modal Dialog"%}

