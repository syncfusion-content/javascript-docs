---
layout: post
title: Getting-Started
description: getting started
platform: js
control: GroupButton
documentation: ug
api: /api/js/ejgroupbutton
---


# Getting Started

## A new HTML document and required codes

This section explains you briefly on how to create a GroupButton in your application with JavaScript. To get start with GroupButton, create a new HTML file and refer the below specified dependent CSS file as well as scripts files.

**CSS file**

[ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css#) – includes all widgets styles (To know more about theme refer [Theming in Essential JavaScript Component](https://help.syncfusion.com/js/theming-in-essential-javascript-components#))

**External script files**

[jQuery 1.7.1](http://jquery.com/#) and later versions.

<table>
<tr>
<th>
File<br/><br/></th><th>
Description/Usage<br/><br/></th></tr>
<tr>
<td>
ej.core.min.js<br/><br/><br/></td><td>
Must be referred always before using all the JS controls.<br/><br/><br/></td></tr>
<tr>
<td>
ej.data.min.js<br/><br/></td><td>
Must be referred since we have provided the dataSource support to GroupButton<br/><br/></td></tr>
<tr>
<td>
ej.groupbutton.min.js<br/><br/><br/></td><td>
Group Button plugin.<br/><br/><br/></td></tr>
</table>
You can make use of ‘ej.web.all.min.js’ file which encapsulates all ‘ej’ web components and frameworks in single file.

[ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js#) – includes all web widgets.

A simple HTML file with required CSS and script reference added to create GroupButton

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" /> <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /> <!--scripts-->

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>

    </head>

    <body>
        <!--Place input element to create GroupButton-->

        <script>

            // Place your script code here to initialize GroupButton

        </script>

    </body>

    </html>


{% endhighlight %}



## GroupButton initialization

GroupButton can be created using **&lt;DIV&gt;** tag or **&lt;SPAN&gt;** tag and corresponding child button elements can be rendered as **&lt;LI&gt;** tag or **&lt;HREF&gt;** tag. Below is the sample code to showcase the rendering the GroupButton with **&lt;LI&gt;** tags in HTML page,

{% highlight html %}

        <div id="groupButton">

            <ul>

                <li> Save </li>

                <li> Open </li>

                <li> Delete </li>

            </ul>

        </div>

{% endhighlight %}

{% highlight js %}

         <script>

            $("#groupButton").ejGroupButton();// initialize the group button control

         </script>

{% endhighlight %}

Also we can use the dataSource, to create the GroupButton which is explained under the dataSource section in this documentation.

