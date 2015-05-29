---
layout: post
title: splitter-integration
description: splitter integration
platform: js
control: Splitter
documentation: ug
---

# Splitter Integration

The **Splitter** allows you to use other **Essential JavaScript** products inside the pane. The integrated function of those widgets can be used in other panes of the **Splitter**.

## Configuring other widgets in Splitter

The following steps explain the implementation of **Splitter** integration.

* In the **HTML** page set the **&lt;div&gt;** element for rendering **Splitter** with two panes. The first pane has the **TreeView** content and the next one has some content that is related to **TreeView**.



<table>
<tr>
<td>
<b>[HTML]</b>        &lt;div id="splitter"&gt;            &lt;div&gt;                &lt;div style="padding: 20px;"&gt;                    <h3>ASP.NET MVC</h3>                    &lt;ul id="treeview"&gt;                        <li>Tools                            &lt;ul&gt;                                <li id="tools" class="_child">Description</li>                            &lt;/ul&gt;                        &lt;/li&gt;                        <li>Chart                            &lt;ul&gt;                                <li id="chart" class="_child">Description &lt;/li&gt;                            &lt;/ul&gt;                        &lt;/li&gt;                        <li>Grid                            &lt;ul&gt;                                <li id="grid" class="_child">Description</li>                            &lt;/ul&gt;                        &lt;/li&gt;                    &lt;/ul&gt;                &lt;/div&gt;            &lt;/div&gt;            &lt;div&gt;                &lt;div style="padding: 20px"&gt;                    &lt;div class="_content"&gt;                        Select any product from the tree to show the description.                    &lt;/div&gt;                    &lt;div class="tools" style="display: none"&gt;                        <h3>Tools</h3>                        Essential Tools is an collection of user interface components used to create interactive                                        ASP.NET MVC applications.                    &lt;/div&gt;                    &lt;div class="chart" style="display: none"&gt;                        <h3>Chart</h3>                        Essential Chart is a business-oriented charting component.                    &lt;/div&gt;                    &lt;div class="grid" style="display: none"&gt;                        <h3>Grid</h3>                        Essential MVC Grid offers full featured a Grid control with extensive support for                                        Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;            &lt;/div&gt;        &lt;/div&gt;</td></tr>
<tr>
<td>
 <b>[JavaScript]</b>// Handle the <b>nodeSelect</b> event for <b>TreeView</b>.    &lt;script type="text/javascript"&gt;        $("#treeview").ejTreeView({ nodeSelect: "treeClicked" }); /* Render TreeView inside Splitter pane */        $("#splitter").ejSplitter({                height: 280, width: 500,                properties: [{ paneSize: 200 }]            });        });        function treeClicked(sender, args) { //nodeSelect event handle            if (sender.currentElement.hasClass('_child')) {                var content = $('.' + sender.currentElement[0].id).html();                $('._content').html(content);            }        }    &lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>@{Html.EJ().Splitter("outterSplitter").PaneProperties(p =>    {        p.Add().ContentTemplate(            @&lt;div class="cont"&gt;                &lt;h3 class="h3"&gt;                    ASP.NET MVC                &lt;/h3&gt;                &lt;ul id="treeView" class="visibleHide"&gt;                    &lt;li&gt;                        Tools                        &lt;ul&gt;                            <li id="tools" class="_child">Description</li>                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        Chart                        &lt;ul&gt;                            <li id="chart" class="_child">Description &lt;/li&gt;                        &lt;/ul&gt;                    &lt;/li&gt;                    &lt;li&gt;                        Grid                        &lt;ul&gt;                            <li id="grid" class="_child">Description</li>                        &lt;/ul&gt;                    &lt;/li&gt;                &lt;/ul&gt;            &lt;/div&gt;).PaneSize("200");        p.Add().ContentTemplate(            @&lt;div class="cont"&gt;                &lt;div class="_content"&gt;                  Select any product from the tree to show the description.                &lt;/div&gt;                &lt;div class="tools des"&gt;                    &lt;h3&gt;                        Tools                    &lt;/h3&gt;                    &lt;p&gt;                        Essential Tools is an collection of user interface components used to create interactive                        ASP.NET MVC applications.                    &lt;/p&gt;                &lt;/div&gt;                &lt;div class="chart des"&gt;                    &lt;h3&gt;                        Chart                    &lt;/h3&gt;                    &lt;p&gt; Essential Chart is a business-oriented charting component.&lt;/p&gt;                &lt;/div&gt;                &lt;div class="grid des"&gt;                    &lt;h3&gt;                        Grid                    &lt;/h3&gt;                    &lt;p&gt;                        Essential MVC Grid offers full featured a Grid control with extensive support for                        Grouping and the display of hierarchical data.                    &lt;/p&gt;                &lt;/div&gt;            &lt;/div&gt;).PaneSize("200");    }).Height("400").Width("100%").Render();}[CSS]&lt;style type="text/css"&gt;    #outterSplitter {        margin: 0 auto;    }    .cont #treeView_Container {        margin-bottom: 0;        border: none;    }    .h3, ._content, p {        font-size: 14px;        margin-top: 10px;        text-indent: 10px;    }    .des {        display: none;    }&lt;/style&gt;</td></tr>
<tr>
<td>
[JavaScript]&lt;script type="text/javascript"&gt;    $(function () {        $("#treeView").ejTreeView({ nodeSelect: "treeClicked" });    });/* Render TreeView inside Splitter pane */    function treeClicked(sender, args) {        if (sender.currentElement.hasClass('_child')) {//nodeSelect event handle            var content = $('.' + sender.currentElement[0].id).html();            $('._content').html(content);        }    }&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>&lt;ej:Splitter ID="splitter" Height="280" Width="500" runat="server"&gt;            &lt;ej:SplitPane PaneSize="200"&gt;                 &lt;div&gt;                &lt;div style="padding: 20px;"&gt;                    <h3>ASP.NET MVC</h3>                    &lt;ej:TreeView ID="treeview" ClientSideOnNodeSelected="treeClicked"  runat="server"&gt;                    &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="Tools"&gt;                                                               &lt;Nodes&gt;                                 &lt;ej:TreeViewNode Id="tools"  Text="Description"&gt;&lt;/ej:TreeViewNode&gt;                                                                &lt;/Nodes&gt;                                                              &lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="Chart"&gt;                                &lt;Nodes&gt;                                    &lt;ej:TreeViewNode Id="chart" Text="Description"&gt;&lt;/ej:TreeViewNode&gt;                                &lt;/Nodes&gt;                            &lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                        &lt;Nodes&gt;                            &lt;ej:TreeViewNode Text="Grid"&gt;                                &lt;Nodes&gt;                                    &lt;ej:TreeViewNode Id="grid" Text="Description"&gt;&lt;/ej:TreeViewNode&gt;                                &lt;/Nodes&gt;                            &lt;/ej:TreeViewNode&gt;                        &lt;/Nodes&gt;                      &lt;/ej:TreeView&gt;                &lt;/div&gt;                 &lt;/div&gt;                &lt;/ej:SplitPane&gt;            &lt;ej:SplitPane&gt;            &lt;div&gt;                &lt;div style="padding: 20px"&gt;                    &lt;div class="_content"&gt;                        Select any product from the tree to show the description.                    &lt;/div&gt;                    &lt;div class="tools des" style="display: none"&gt;                        <h3>Tools</h3>                       Essential Tools is an collection of user interface components used to create interactive ASP.NET MVC applications.                    &lt;/div&gt;                    &lt;div class="chart des" style="display: none"&gt;                        <h3>Chart</h3>                        Essential Chart is a business-oriented charting component.                    &lt;/div&gt;                    &lt;div class="grid des" style="display: none"&gt;                        <h3>Grid</h3>                        Essential MVC Grid offers full featured a Grid control with extensive support for Grouping and the display of hierarchical data.                    &lt;/div&gt;                &lt;/div&gt;                &lt;/div&gt;                &lt;/ej:SplitPane&gt;        &lt;/ej:Splitter&gt;</td></tr>
<tr>
<td>
[JavaScript]  &lt;script type="text/javascript"&gt;         function treeClicked(sender, args) {             if (sender.value == "Description") {                 var content = $('.' + sender.currentElement[0].id).html();                 $('._content').html(content);             }         }&lt;/script&gt;</td></tr>
</table>


* When the node is selected in **TreeView**, the integrated output is displayed in the second pane.



{% include image.html url="\js\Splitter\concepts-and-features\splitter-integration_images\splitter-integration_img1.png" Caption="Figure 812: Splitter Integration initially"%}



{% include image.html url="\js\Splitter\concepts-and-features\splitter-integration_images\splitter-integration_img2.png" Caption="Figure 913: Integrated output of Splitter"%}

