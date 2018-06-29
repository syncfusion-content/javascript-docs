---
layout: post
title: Getting-Started
description: getting started
platform: js
control: TreeView
documentation: ug
api: /api/js/ejtreeview
---

# Getting Started	

## Include Script and CSS

To get start with TreeView, create a new HTML file and add the required dependent CSS file as well as script files.

CSS file

* [ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css) – includes all widgets styles (To know more about theme refer [Theming in Essential JavaScript Component](https://help.syncfusion.com/js/theming-in-essential-javascript-components) )

External script files

* [jQuery 1.7.1](http://jquery.com/#) and later versions.

Internal script files

<table>
<tr>
<th>
File</th><th>
Description/Usage</th></tr>
<tr>
<td>
ej.core.min.js<br/><br/></td><td>
Must be referred always before using all the JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.data.min.js<br/><br/></td><td>
Used to handle data operation and should be used while binding data to JS controls.<br/><br/></td></tr>
<tr>
<td>
ej.treeview.min.js<br/><br/></td><td>
The TreeView main file<br/><br/></td></tr>
<tr>
<td>
ej.checkbox.min.js<br/><br/></td><td>
Should be referred when using check box functionalities in TreeView.  <br/><br/></td></tr>
<tr>
<td>
ej.draggable.min.js<br/><br/></td><td>
Should be referred when using drag option in TreeView.<br/><br/></td></tr>
<tr>
<td>
ej.waitingpopup.min.js<br/><br/></td><td>
Should be referred when using load on demand in TreeView.<br/><br/></td></tr>
</table>
Above internal script files are usable only if TreeView control alone going to be used in application. Otherwise you can make use of ‘ej.web.all.min.js’ file which encapsulates all ‘ej’ components and frameworks in single file.

[ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js) – includes all widgets (link about widgets details).

N>  In production, we highly recommend you to use our [custom script generator](https://help.syncfusion.com/js/include-only-the-needed-widgets) to create custom script file with required controls and its dependencies only. Also to reduce the file size further please use [GZip compression](https://developers.google.com/web/fundamentals/performance/optimizing-content-efficiency/optimize-encoding-and-transfer?hl=en#text-compression-with-gzip) in your server. 

## Initialize TreeView

A simple HTML file with required CSS and script reference added to create TreeView control

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />

        <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"
            rel="stylesheet" />

        <!--scripts-->

        <script src="http://code.jquery.com/jquery-1.10.2.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

    </head>

    <body>

        <!-- add the unordered list element to create TreeView here-->

    </body>

    </html>


{% endhighlight %}

TreeView can be created in two different ways.

## Converting UL into TreeView 

TreeView can be created using unordered hierarchical list as shown below

{% highlight html %}

    <!--unordered list to create TreeView-->

    <ul id="treeView">

        <li>Item 1

            <ul>

                <li>Item 1.1</li>

                <li>Item 1.2</li>

            </ul>

        </li>

        <li>Item 2</li>

        <li>Item 3</li>

    </ul>

{% endhighlight %}

Initialize TreeView from unordered list

{% highlight js %}

        // creates TreeView from unordered list

        $(function () {

            $("#treeView").ejTreeView();

        });

{% endhighlight %}

## TreeView Using Data Binding

Another way of creating TreeView is binding with the data source, you can bind local data source to create a TreeView as shown below code example.
The [beforeLoad](https://help.syncfusion.com/api/js/ejtreeview#events:beforeload) event will be triggered before loading nodes into TreeView.
Create the TreeView wrapper.

{% highlight html %}

    <!--create the TreeView wrapper-->

    <div id="treeView"></div>

{% endhighlight %}

Initialize TreeView with local data source

{% highlight js %}

       $(function () {

            // initialize and bind the TreeView with local data

            $("#treeView").ejTreeView({

                fields: {
                    dataSource: [

                    {

                        text: "Item 1",

                        child: [

                        { text: "Item 1.1" },

                        { text: "Item 1.2" }

                        ]

                    },

                    { text: "Item 2" },

                    { text: "Item 3" }

                    ]

                }

            });

        });

{% endhighlight %}
