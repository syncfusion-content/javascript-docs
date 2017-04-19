---
layout: post
title: Getting-Started
description: getting started
platform: js
control: File Explorer
documentation: ug
api: /api/js/ejfileexplorer
---


# Getting Started

The following section is briefly explain the things to get started with FileExplorer control.

## Preparing the HTML document

Create a new HTML file and include the below code: 

{% highlight html %}

    <!DOCTYPE html>

    <html xmlns="http://www.w3.org/1999/xhtml">

    <head>

        <meta charset="utf-8">

        <title> </title>

    </head>

    <body>

    </body>

    </html>

{% endhighlight %}

## Adding the references

To include the control in the application the following references need to be added:

* CSS references
* Script references

### CSS references

Add the below CSS reference in the head section, for the default theme

{% highlight javascript %}

       <link rel="stylesheet" href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" /><br /><br />

{% endhighlight %}

N> Essential JS widgets having the support for 13 built-in themes, to know more please check [here](http://docs.syncfusion.com/js/theming-in-essential-javascript-components#)

### Script references

The external script dependencies of the FileExplorer widget are,

* [jQuery 1.7.1](http://jquery.com/#) or later versions.
* [jsrender](https://www.jsviews.com/#jsrender) – for grid view template.

And the internal script dependencies of the FileExplorer widget are:

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
ej. draggable.min.js<br/><br/></td><td>
Used to handle the drag and drop functionality<br/><br/></td></tr>
<tr>
<td>
ej.scroller.min.js<br/><br/></td><td>
Used to show the scroller in the layout area<br/><br/></td></tr>
<tr>
<td>
ej.button.min.js<br/><br/></td><td>
Used to display the buttons in the toolbar<br/><br/></td></tr>
<tr>
<td>
ej.treeview.min.js<br/><br/></td><td>
Used to display the treeview in the navigation pane<br/><br/></td></tr>
<tr>
<td>
ej.uploadbox.min.js<br/><br/></td><td>
Used to perform the upload functionality <br/><br/></td></tr>
<tr>
<td>
ej.waitingpopup.min.js<br/><br/></td><td>
Used to showcase the waiting popup<br/><br/></td></tr>
<tr>
<td>
ej.dialog.min.js<br/><br/></td><td>
Used to create the alert windows <br/><br/></td></tr>
<tr>
<td>
ej.splitter.min.js<br/><br/></td><td>
Used as the body section to separate the navigation and layout area<br/><br/></td></tr>
<tr>
<td>
ej.toolbar.min.js<br/><br/></td><td>
Used to showcase the hearer section<br/><br/></td></tr>
<tr>
<td>
ej.menu.min.js<br/><br/></td><td>
Used to showcase the context menu<br/><br/></td></tr>
<tr>
<td>
ej.grid.min.js<br/><br/></td><td>
Used to showcase the grid layout view<br/><br/></td></tr>
</table>

For getting started you can use the “**ej.web.all.min.js**” file, which encapsulates all the `ej` controls and frameworks in one single file. 

So you can add the below Script references in the head section:

{% highlight javascript %}


    <!--External script references-->

    <script src="https://code.jquery.com/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>

    <!--Internal script references-->

    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>


{% endhighlight %}

N> The above Script and CSS references uses the [CDN links](http://docs.syncfusion.com/js/cdn#). In case if you need to refer the local files then you can copy the corresponding files from the [installed location](http://docs.syncfusion.com/js/installation-and-deployment#) and can include into your application directory

N> In production we recommend you to use our [Custom script generator](http://docs.syncfusion.com/js/include-only-the-needed-widgets#) to create custom script file with required controls and its dependencies only]

## Adding the control element 

The control can be created from a div element. So you can add the div element into your page at where you want to render the FileExplorer.

{% highlight html %}

		<div id="fileExplorer"></div>

{% endhighlight %}

## Initialize and configure the control

Once added the element you can initialize the control from the script section like below:

{% highlight javascript %}

        $(function () {

            var fileSystemPath = "http://js.syncfusion.com/demos/ejServices/Content/FileBrowser/";

            var ajaxActionHandler = "http://js.syncfusion.com/demos/ejServices/api/FileExplorer/FileOperations";

            $("#fileExplorer").ejFileExplorer({

                path: fileSystemPath,

                ajaxAction: ajaxActionHandler

            });

        });

{% endhighlight %}

Here [path](https://help.syncfusion.com/api/js/ejfileexplorer#members:path) and [ajaxAction](https://help.syncfusion.com/api/js/ejfileexplorer#members:ajaxaction) are the mandatory configuration to showcase the FileExplorer control.

    <table>
        <tr>
            <td>
                N> As you know FileExplorer is a client side control but it depends on the server side actions. So in JavaScript to handle the server side actions we are using the Web API service and it was hosted in our server.<br /><br />
            </td>
        </tr>
    </table>
	
To perform the server side actions using local web API service, please refer the [link](https://help.syncfusion.com/js/fileexplorer/how-to#service-for-fileexplorer)

Once you have completed the above steps, you get an output like below

![](Getting-Started_images/Getting-Started_img1.png)


