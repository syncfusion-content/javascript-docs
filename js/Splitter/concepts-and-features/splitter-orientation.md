---
layout: post
title: splitter-orientation
description: splitter orientation
platform: js
control: Splitter
documentation: ug
---

# Splitter Orientation

The **Splitter** supports both vertical and horizontal orientation of the pane. You can declare the orientation by using **enum**, **ej.Orientation.Vertical** or **ej.Orientation.Horizontal**, that have the corresponding value of vertical and horizontal as a string.

## Configure Splitter Orientation

 The following steps explain the implementation of **Splitter** orientation option.

* In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** widget. 



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>            &lt;/div&gt;            &lt;div&gt;                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>// Set the <b>orientation</b> property as <b>ej.Orientation.Vertical</b> for the outer pane in the <b>ejSplitter</b> function. The default orientation value is horizontal in the <b>Splitter</b> widget.    &lt;script type="text/javascript"&gt;        $("#splitter").ejSplitter({            height: 280, width: 400,            <b>orientation: ej.Orientation.Vertical,</b>        });      &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**



        @Html.EJ().Splitter("Splitter").Height("280").Width("400").**Orientation(Orientation.Vertical)**.PaneProperties(

    p =>

    {

        p.Add().ContentTemplate(

            @&lt;div&gt;

                &lt;div&gt;

                    <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

                &lt;/div&gt;

            &lt;/div&gt;);

        p.Add().ContentTemplate(

            @&lt;div&gt;

                &lt;div&gt;

                    <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

                &lt;/div&gt;

            &lt;/div&gt;);

    })



**[ASPX]**



         &lt;ej:Splitter ID="splitter" Height="280" Width="400" Orientation="Vertical" runat="server"&gt;

                &lt;ej:SplitPane&gt;

                                 &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 1</div>

            &lt;/div&gt;

           &lt;/ej:SplitPane&gt;

                &lt;ej:SplitPane&gt;

                                             &lt;div&gt;

                <div style="padding: 10px 0 0 10px; text-align: center;">Pane 2</div>

            &lt;/div&gt;

          &lt;/ej:SplitPane&gt;

         &lt;/ej:Splitter&gt;





The output for **Splitter** with **ej.Orientation.Vertical**.

{% include image.html url="\js\Splitter\concepts-and-features\splitter-orientation_images\splitter-orientation_img1.png" Caption="Figure 95: Splitter with vertical orientation "%}

The output for **Splitter** with **ej.Orientation.Horizontal**.



{% include image.html url="\js\Splitter\concepts-and-features\splitter-orientation_images\splitter-orientation_img2.png" Caption="Figure 610: Splitter with horizontal orientation"%}

