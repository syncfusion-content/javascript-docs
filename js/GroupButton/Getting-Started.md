---
layout: post
title: Getting-Started
description: getting started
platform: js
control: GroupButton
documentation: ug
---


# Getting Started

## A new HTML document and required codes

This section explains you briefly on how to create a EJ GroupButton in your application with JavaScript. To get start with Group Button, create a new HTML file and refer the below specified dependent CSS file as well as scripts files.

**CSS file**

[ej.web.all.min.css](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css#) – includes all widgets styles (To know more about theme refer [Theming in Essential JavaScript Component](http://help.syncfusion.com/js/theming-in-essential-javascript-components#))

**External script files**

[jQuery 1.7.1](http://jquery.com/#) and later versions.

<table>
<tr>
<td>
**File**<br/><br/></td><td>
**Description/Usage**<br/><br/></td></tr>
<tr>
<td>
**ej.core.min.js**<br/><br/><br/></td><td>
Must be referred always before using all the JS controls.<br/><br/><br/></td></tr>
<tr>
<td>
**ej.data.min.js**<br/><br/></td><td>
Must be referred since we have provided the dataSource support to Group Button<br/><br/></td></tr>
<tr>
<td>
**ej.groupbutton.min.js**<br/><br/><br/></td><td>
Group Button plugin.<br/><br/><br/></td></tr>
</table>
You can make use of ‘ej.web.all.min.js’ file which encapsulates all ‘ej’ web components and frameworks in single file.

[ej.web.all.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js#) – includes all web widgets.

A simple html file with required CSS and script reference added to create GroupButton

{% highlight html %}

    <!DOCTYPE html>

    <html>

    <head>

        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" /> <!-- style sheet for default theme(flat azure) -->

        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /> <!--scripts-->

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>

    </head>

    <body>
        <!--Place input element to create Group Button-->

        <script>

            // Place your script code here to initialize GroupButton

        </script>

    </body>

    </html>


{% endhighlight %}



## Group Button initialization

GroupButton can be created using “div” tag or “span” tag and corresponding child button elements can be rendered as li tag or href tag. Below is the sample code to showcase the rendering the GroupButton with li tags in html page,

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

Also we can use the dataSoruce, to create the Group Button which is explained under the dataSource section in this documentation.

