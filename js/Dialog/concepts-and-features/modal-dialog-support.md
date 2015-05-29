---
layout: post
title: modal-dialog-support
description: modal dialog support
platform: js
control: Dialog
documentation: ug
---

# Modal Dialog Support

The modal dialog is used like an alert window that disables the main window and explore its content for the purpose of interacting with others. 

## Configure Modal Dialog

The following steps explains you the implementation of modal dialog. 

* In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="dialogLoginForm" title="Login Form"&gt;        &lt;table&gt;            &lt;tr&gt;                <td>User Name                  &lt;input type="text" id="txtName" class="ejinputtext" style="width: 100%" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                <td>Password                  &lt;input type="text" id="Text1" class="ejinputtext" style="width: 100%" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td align="center"&gt;                    &lt;input type="button" id="downloadBtn" value="Login" class="e-btn" style="width: 100px; height: 30px" /&gt;                &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                &lt;td align="center"&gt;                    <a href="#">Forgot Password</a>                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set <b>enableModal</b> property as true in the <b>Dialog</b> function. The default value of <b>enableModal</b> is <b>false</b> in the <b>Dialog</b> widget    &lt;script type="text/javascript"&gt;        $("#dialogLoginForm").ejDialog({            width: 250,            height: 250,            <b>enableModal: true</b>        });      &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widget using helpers and set EnableModal to ‘true’.** 





@{Html.EJ().Dialog("dialogLoginForm").Title("Login Form").ContentTemplate(@&lt;div&gt;

            &lt;table&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        User Name

                        &lt;input type="text" id="txtName" class="ejinputtext" style="width: 100%" /&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        Password

                        &lt;input type="text" id="Text1" class="ejinputtext" style="width: 100%" /&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td align="center"&gt;

                        &lt;input type="button" id="downloadBtn" value="Login" class="e-btn" style="width: 100px; height: 30px" /&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td align="center"&gt;

                        <a href="#">Forgot Password</a>

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/table&gt;

        &lt;/div&gt;).Width(250).Height("250").**EnableModal(true).**Render();}







**[ASPX]**

**// In the ASPX page add the Dialog widget and set EnableModel as true.**



    &lt;ej:Dialog ID="dialogLoginForm" runat="server" Width="300" Height="300" Title="Login Form" EnableModal="true"&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                &lt;table&gt;

                    &lt;tr&gt;

                        <td>User Name

                  &lt;input type="text" id="txtName" class="ejinputtext" style="width: 100%" /&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        <td>Password

                  &lt;input type="text" id="Text1" class="ejinputtext" style="width: 100%" /&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td align="center"&gt;

                            &lt;input type="button" id="downloadBtn" value="Login" class="e-btn" style="width: 100px; height: 30px" /&gt;

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td align="center"&gt;

                            <a href="#">Forgot Password</a>

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/table&gt;

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output of modal dialog control. 

![C:\Users\ApoorvahR\Desktop\15.png](modal-dialog-support_images\modal-dialog-support_img1.png)

_Figure_ _30__20__: Modal Dialog_

