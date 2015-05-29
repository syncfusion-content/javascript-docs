---
layout: post
title: rtl-support
description: rtl support
platform: js
control: Splitter
documentation: ug
---

# RTL Support

The **Splitter** provides you with **RTL** (**Right-To-Left**) support. The alignment of **Splitter** can be changed from **Left-To-Right** to **Right-To-Left**.

## Enable RTL

The following steps explain enabling the right-to-left property for **Splitter** widget.

* In the **HTML** page set the corresponding **&lt;div&gt;** elements for outer and inner **Splitter** control.



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="outersplitter"&gt;            &lt;div&gt;                &lt;div style="padding: 0px 15px;"&gt;                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;                &lt;/div&gt;            &lt;/div&gt;            &lt;div id="innersplitter"&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Tools &lt;/h3&gt;                        Essential Tools is an collection of user interface components used to create interactive                                    ASP.NET MVC applications.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Chart &lt;/h3&gt;                        Essential Chart is a business-oriented charting component.                    &lt;/div&gt;                &lt;/div&gt;                &lt;div&gt;                    &lt;div style="padding: 0px 15px;"&gt;                        <h3 class="h3">Grid &lt;/h3&gt;                        Essential Mvc Grid offers full featured a Grid control with extensive support for                                    Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Set <b>enableRTL</b> as “<b>tTrue</b>” in the <b>ejSplitter</b> function.    &lt;script type="text/javascript"&gt;            $("#outersplitter").ejSplitter({                height: 250, width: 600,                orientation: ej.Orientation.Vertical,                <b>enableRTL: true,</b>                properties: [{ paneSize: 60 }]            });            $("#innersplitter").ejSplitter({                width: 600,                properties: [{ paneSize: 200 }, { paneSize: 170 }]            });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



@{Html.EJ().Splitter("outterSplitter").Height("300").Width("600").Orientation(Orientation.Vertical).EnableRTL(true)

      .PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                &lt;div class="content" style="padding: 0px 15px;"&gt;

                    &lt;h3 class="h3"&gt;

                        ASP.NET MVC

                    &lt;/h3&gt;

                &lt;/div&gt;

            &lt;/div&gt;).PaneSize("60");

        p.Add().ContentTemplate(

            @&lt;div style="height: 100%; width: 100%"&gt;

                @innerSplitter()

            &lt;/div&gt;);

    }).Render();}



@helper innerSplitter()

{

    @Html.EJ().Splitter("innerSplitter").Width("600").PaneProperties(p1 =>

                {

                    p1.Add().ContentTemplate(@&lt;div&gt;

                        &lt;div class="content"&gt;

                            &lt;h3 class="h3"&gt;

                                Tools

                            &lt;/h3&gt;

                            Essential Tools is an collection of user interface components used to create interactive

                            ASP.NET MVC applications.

                        &lt;/div&gt;

                    &lt;/div&gt;).PaneSize("200");

                    p1.Add().ContentTemplate(@&lt;div&gt;

            &lt;div class="content"&gt;

                &lt;h3 class="h3"&gt;

                    Chart

                &lt;/h3&gt;

                Essential Chart is a business-oriented charting component.

            &lt;/div&gt;

        &lt;/div&gt;).PaneSize("200");

                    p1.Add().ContentTemplate(@&lt;div&gt;

            &lt;div class="content"&gt;

                &lt;h3 class="h3"&gt;

                    Grid

                &lt;/h3&gt;

                Essential Mvc Grid offers full featured a Grid control with extensive support for

                Grouping and the display of hierarchical data.

            &lt;/div&gt;

        &lt;/div&gt;).PaneSize("200");

                })

}

**[CSS]**

&lt;style type="text/css"&gt;

    #outterSplitter {

        margin: 0 auto;

    }

    .h3 {

        font-size: 14px;

    }

    #innerSplitter {

        border: 0 none;

    }

    .content {

        padding: 15px;

    }

&lt;/style&gt;





**[ASPX]**



        &lt;ej:Splitter Height="250" Width="600" ID="outersplitter" Orientation="Vertical" EnableRTL="true" runat="server"&gt;

             &lt;ej:SplitPane PaneSize="60"&gt;

                         &lt;div&gt;

                &lt;div style="padding: 0px 15px;"&gt;

                    <h3 class="h3">ASP.NET MVC &lt;/h3&gt;

                &lt;/div&gt;

            &lt;/div&gt;

             &lt;/ej:SplitPane&gt;



       &lt;ej:SplitPane&gt;

            &lt;ej:Splitter ID="innersplitter"   Width="600" runat="server"&gt;

                &lt;ej:SplitPane paneSize="200"&gt;

                                 &lt;div&gt;

                    &lt;div style="padding: 0px 15px;"&gt;

                        <h3 class="h3">Tools &lt;/h3&gt;

                        Essential Tools is an collection of user interface components used to create interactive

                                    ASP.NET MVC applications.

                    &lt;/div&gt;

                &lt;/div&gt;



                &lt;/ej:SplitPane&gt;

                &lt;ej:SplitPane paneSize="170"&gt;

                  &lt;div&gt;

                    &lt;div style="padding: 0px 15px;"&gt;

                        <h3 class="h3">Chart &lt;/h3&gt;

                        Essential Chart is a business-oriented charting component.

                    &lt;/div&gt;

              &lt;/div&gt;



                &lt;/ej:SplitPane&gt;

              &lt;ej:SplitPane PaneSize="60"&gt;

                  &lt;div&gt;

                           &lt;div style="padding: 0px 15px;"&gt;

                        <h3 class="h3">Grid &lt;/h3&gt;

                        Essential Mvc Grid offers full featured a Grid control with extensive support for

                                    Grouping and the display of hierarchical data.

                    &lt;/div&gt;

                    &lt;/div&gt;

              &lt;/ej:SplitPane&gt;

            &lt;/ej:Splitter&gt;

      &lt;/ej:SplitPane&gt;



    &lt;/ej:Splitter&gt;



The output for **Splitter** when **enableRTL** is “**tTrue**”.



{% include image.html url="\js\Splitter\concepts-and-features\rtl-support_images\rtl-support_img1.png" Caption="Figure 1923: Splitter with enableRTL "%}







__

