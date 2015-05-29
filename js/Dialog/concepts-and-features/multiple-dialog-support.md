---
layout: post
title: multiple-dialog-support
description: multiple dialog support
platform: js
control: Dialog
documentation: ug
---

# Multiple Dialog Support

The **Dialog** supports multiple controls in the same web page. You can use more number of **Dialog** control with different content and different functionalities in the same web page.

## Configure Multiple Dialog

The following steps explains the implementation of multiple **Dialog** in the same web page. 

* In the **HTML** page set a **&lt;div&gt;** element with dialog content for rendering the **Dialog** control. 



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="mvcDialog" title="MVC"&gt;        &lt;p&gt;            Essential Studio for ASP.NET MVC contains all the controls you need to build line-of-business web applications including grids, charts, gauges, menus, calendars, editors, and much more.        &lt;/p&gt;    &lt;/div&gt;    &lt;div id="orubaseDialog" title="Orubase"&gt;        &lt;p&gt;            Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.         &lt;/p&gt;    &lt;/div&gt;    &lt;div id="winrtDialog" title="WinRT"&gt;        &lt;p&gt;            Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.                                It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.        &lt;/p&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Write multiple <b>Dialog</b> control in a single web page    &lt;script type="text/javascript"&gt;        $("#mvcDialog").ejDialog({ position: { X: 20, Y: 26 } });        $("#orubaseDialog").ejDialog({ position: { X: 521, Y: 20 } });        $("#winrtDialog").ejDialog({ position: { X: 296, Y: 207 } });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// In the CSHTML page add the Dialog widgets using helpers and set the Position values.** 



@{Html.EJ().Dialog("mvcdialog").Title("MVC").ContentTemplate(@&lt;div&gt;

            &lt;p&gt;

                Essential Studio for ASP.NET MVC contains all the controls you need to build line-of-business web applications including grids, charts, gauges, menus, calendars, editors, and much more.

            &lt;/p&gt;

       &lt;/div&gt;).**Position(p => p.XValue("296").YValue("207"))**.Render();}



@{Html.EJ().Dialog("orubasedialog").Title("Orubase").ContentTemplate(@&lt;div&gt;

            &lt;p&gt;

                Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe.

            &lt;/p&gt;

        &lt;/div&gt;).**Position(p => p.XValue("721").YValue("207")).**Render();}



@{Html.EJ().Dialog("winrtdialog").Title("WinRT").ContentTemplate(@&lt;div&gt;

            &lt;p&gt;

                Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more.

                It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.

            &lt;/p&gt;

        &lt;/div&gt;).**Position(p => p.XValue("500").YValue("407"))**.Render();}



**[ASPX]**

**// In the ASPX page add the Dialog widgets with Position.**



    &lt;ej:Dialog ID="mvcdialog" runat="server" Title="MVC"&gt;

        &lt;Position XValue="296" YValue="207" /&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                &lt;p&gt;

                    Essential Studio for ASP.NET MVC contains all the controls you need to build line-of-business web applications including grids, charts, gauges, menus, calendars, editors, and much more.

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;



    &lt;ej:Dialog ID="orubasedialog" runat="server" Title="Orubase"&gt;

        &lt;Position XValue="721" YValue="207" /&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                &lt;p&gt;

                    Orubase is the only mobile application development framework built especially for developing complex line-of-business mobile applications targeting iOS, Android, and Windows Phone platforms in the shortest possible timeframe. 

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;



    &lt;ej:Dialog ID="winrtdialog" runat="server" Title="WinRT"&gt;

        &lt;Position XValue="500" YValue="407" /&gt;

        &lt;DialogContent&gt;

            &lt;div&gt;

                &lt;p&gt;

                    Essential Studio for WinRT contains all the controls you need to build line-of-business tablet applications including grid, chart, map, tree map, SSRS report viewer, rich-text editor, pdf viewer, gauges, barcode, editors, and much more. 

                               It also includes a unique set of controls for reading and writing Excel, Word, and PDF documents in Windows store apps.

                &lt;/p&gt;

            &lt;/div&gt;

        &lt;/DialogContent&gt;

    &lt;/ej:Dialog&gt;





* The output of multiple **Dialog** control is as follows.

![C:\Users\ApoorvahR\Desktop\13.png](multiple-dialog-support_images\multiple-dialog-support_img1.png)

_Figure_ _28__18__: Multiple Dialog___

