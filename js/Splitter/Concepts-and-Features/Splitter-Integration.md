---
layout: post
title: Splitter-Integration
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
 <b>[JavaScript]</b>// Handle the <b>nodeSelect</b> event for <b>TreeView</b>.    &lt;script type="text/javascript"&gt;        $("#treeview").ejTreeView({ nodeSelect: "treeClicked" }); /* Render TreeView inside Splitter pane */        $("#splitter").ejSplitter({                height: 280, width: 500,                properties: [{ paneSize: 200 }]        });        function treeClicked(sender, args) { //nodeSelect event handle            if (sender.currentElement.hasClass('_child')) {                var content = $('.' + sender.currentElement[0].id).html();                $('._content').html(content);            }        }    &lt;/script&gt;</td></tr>
</table>


* When the node is selected in **TreeView**, the integrated output is displayed in the second pane.



{% include image.html url="/js/Splitter/Concepts-and-Features/Splitter-Integration_images/Splitter-Integration_img1.png" Caption="Figure 8: Splitter Integration initially"%}



{% include image.html url="/js/Splitter/Concepts-and-Features/Splitter-Integration_images/Splitter-Integration_img2.png" Caption="Figure 9: Integrated output of Splitter"%}

