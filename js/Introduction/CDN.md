---
layout: post
title: CDN
description: cdn
platform: js
control: Introduction
documentation: ug
---

# CDN

The [CDN](http://en.wikipedia.org/wiki/Content_delivery_network) links are provided individually for all the Scripts and Stylesheets, so that the users can have easier access to the Syncfusion JavaScript components. 


>   **Note**: All the provided cdn links can be accessed either through **http** or **https**.


## CDN Script links

### External dependency libraries

The first four common script libraries listed in the below table are more essential and mandatory to render any of the Syncfusion widgets on the application module.

The basic syntax follows below,

<table>
<tr>
<td>
http://cdn.syncfusion.com/js/assets/external/<b>[fileName]</b>
</td>
</tr>
<tr>
<td>
<b>Example:</b>
http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js
</td>
</tr>
</table>

<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
jquery 1.10.2</td><td>
Common jquery script to render any of the Syncfusion widgets</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js">http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js</a></td></tr>
<tr>
<td>
jquery.easing</td><td>
supports animation</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js</a></td></tr>
<tr>
<td>
jsrender</td><td>
supports template rendering</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js">http://cdn.syncfusion.com/js/assets/external/jsrender.min.js</a>  </td></tr>
<tr>
<td>
Jquery.Globalize</td><td>
Supports Globalization</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js</a>     </td></tr>
<tr>
<td>
Angular JS</td><td>
Minified angular file to support custom directives.</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/angular.min.js">http://cdn.syncfusion.com/js/assets/external/angular.min.js</a></td></tr>
<tr>
<td>
excanvas</td><td>
To support canvas element rendering in IE8 browser</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/excanvas.min.js">http://cdn.syncfusion.com/js/assets/external/excanvas.min.js</a></td></tr>
<tr>
<td>
Knockout JS</td><td>
Minified knockout file to support the observable binding. </td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/knockout.min.js">http://cdn.syncfusion.com/js/assets/external/knockout.min.js</a></td></tr>
<tr>
<td>
requireJS</td><td>
Supports loading of required dependencies</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/require.min.js">http://cdn.syncfusion.com/js/assets/external/require.min.js</a> </td></tr>
<tr>
<td>
jquery.validate</td><td>
Supports client-side validation</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js</a></td></tr>
<tr>
<td>
Jquery.validate.unobtrusive</td><td>
To enable unobtrusive validation options in <b>data-*</b> attributes</td><td>
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js</a></td></tr>
</table>

### Syncfusion Dependency Libraries - Based on latest build version

The **CDN** script files are maintained for each version of the **Essential Studio** individually. Refer the following syntax:

<table>
<tr>
<td>
http://cdn.syncfusion.com/[<b>version</b>]/js/web/[<b>fileName</b>]
</td>
</tr>
<tr>
<td>
</br>
For example, to access the <b>ej.web.all.min.js</b> file in <b>{{ site.releaseversion }}</b> version – 
 http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js
</td>
</tr>
</table>

<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
ej.web.all.min</td><td>
Combined script file which includes the script of all the Syncfusion UI web widgets. </td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js</a> </td></tr>
<tr>
<td>
ej.webform.min</td><td>
supports server-side event functionalities in ASP.NET controls</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.webform.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.webform.min.js</a></td></tr>
<tr>
<td>
ej.unobtrusive.min</td><td>
Supports Syncfusion widgets to render in HTML5 format.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js</a>  </td></tr>
<tr>
<td>
ej.widget.angular.min</td><td>
Provides complete support for Angular JS </td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js</a></td></tr>
<tr>
<td>
ej.widget.ko.min</td><td>
Provides complete support for Knockout JS</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js</a></td></tr>
</table>


The **Knockout** and **angular** dependencies can be accessed through the following syntax,

<table>
<tr>
<td>
http://cdn.syncfusion.com/[<b>version</b>]/js/[<b>fileName</b>]
</td>
</tr>
<tr>
<td>
<br/>
For example, to access the <b>ej.widget.angular.min.js</b> file in <b>{{ site.releaseversion }}</b> version – 
 http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js
</td>
</tr>
</table>


## CDN StyleSheet links

The CDN links for all the css files (both core & theme related) are depicted together in the below table. Refer the following syntax:

<table>
<tr>
<td>
http://cdn.syncfusion.com/[<b>version</b>]/js/web/[<b>fileName</b>] – Core (ej.widgets.core.min.css)
</td>
</tr>
<tr>
<td>
<br/>
http://cdn.syncfusion.com/[<b>version</b>]/js/web/[<b>theme-name</b>]/[<b>fileName</b>] – Theme related
</td>
</tr>
</table>


<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
Flat-Azure (default theme)</td><td>
Includes the css properties defined for all the widgets in flat-azure theme. (Default-theme)</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Azure Dark</td><td>
Includes the css properties defined for all the widgets in flat-azure dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css</a>  </td></tr>
<tr>
<td>
Flat-lime</td><td>
Includes the css properties defined for all the widgets in flat-lime theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-lime Dark</td><td>
Includes the css properties defined for all the widgets in flat-lime dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Saffron</td><td>
Includes the css properties defined for all the widgets in flat-saffron theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Saffron Dark</td><td>
Includes the css properties defined for all the widgets in flat-saffron dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Azure</td><td>
Includes the css properties defined for all the widgets in gradient-azure theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css</a>  </td></tr>
<tr>
<td>
Gradient-Azure Dark</td><td>
Includes the css properties defined for all the widgets in gradient-azure dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-lime</td><td>
Includes the css properties defined for all the widgets in gradient-lime theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-lime Dark</td><td>
Includes the css properties defined for all the widgets in gradient-lime dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Saffron</td><td>
Includes the css properties defined for all the widgets in gradient-saffron theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Saffron Dark</td><td>
Includes the css properties defined for all the widgets in gradient-saffron dark theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Bootstrap-theme</td><td>
Includes the css properties defined for all the widgets in bootstrap theme.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css</a></td></tr>
<tr>
<td>
ej.responsive.css</td><td>
To make the widget responsive, it is necessary to refer this css file.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css</a></td></tr>
</table>


If in case, the user wants to refer the core and theme files of a specific theme separately (instead of the combined version of **ej.web.all.min.css** reference), then they can go with the below specified theme reference method. 

Here – For example, we have depicted another way of theme reference for the **Flat-Azure** and **Flat-Azure Dark** themes in the below table. Likewise, you can refer for any of the 13 available themes (just by referring the required **ej.theme.min.css** available under each of the theme folders along with the widget core file).

<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
Flat-Azure</td><td>
Here, the widget core file (<b>ej.widget.core.min.css</b>) is common and the theme file <b>ej.theme.min.css</b> is uniquely available under the <b>flat-azure</b> theme folder.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css</a><br/></td></tr>
<tr>
<td>
Flat-Azure Dark</td><td>
Here, the widget core file (<b>ej.widget.core.min.css</b>) is common and the theme file <b>ej.theme.min.css</b> is uniquely available under the <b>flat-azure-dark</b> theme folder.</td><td>
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css</a><br/></td></tr>
</table>


## Referring local Scripts and CSS, when CDN fails

One of the major risk with CDN links is that – sometimes it may go down due to the network or connection problems which is so annoying. On such scenarios, we can refer the local scripts and css files dynamically in the application by checking if the scripts and css files loaded through CDN returns **undefined** (if it returns undefined, the local scripts will get referred. Otherwise, the cdn links will work fine) as depicted below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>

    // CDN LINK references
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>

    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>

    <script type="text/javascript">

        if (typeof jQuery == "undefined") { // If CDN fails, jQuery returns undefined
            // Referring local scripts - Specify the path where the below files are located in your machine
            document.write(decodeURIComponent('%3Cscript src="Scripts/jquery-1.10.2.min.js" %3E%3C/script%3E'));
            document.write(decodeURIComponent('%3Cscript src="Scripts/jquery.easing.1.3.min.js" %3E%3C/script%3E'));
            document.write(decodeURIComponent('%3Cscript src="Scripts/jquery.globalize.min.js" %3E%3C/script%3E'));
            document.write(decodeURIComponent('%3Cscript src="Scripts/jsrender.min.js" %3E%3C/script%3E'));
        }

        if (typeof ej == "undefined") { // If CDN fails, ej returns undefined.
            // So that, refer the Syncfusion stylesheets and scripts from the local path here

            // StyleSheet reference from the local system path
            document.write(decodeURIComponent('%3Clink rel="stylesheet" href="Content/ej/web/default-theme/ej.web.all.min.css" %3C/%3E'));

            // Script reference from the local system path
            document.write(decodeURIComponent('%3Cscript src="Scripts/ej/ej.web.all.min.js" %3E%3C/script%3E'));
        }

    </script> 
</head>
<body> 

<!--Container for ejDatePicker widget-->
<input id="startDate" type="text" />

<script type="text/javascript">
        $(function () {
            // initialization
            $("#startDate").ejDatePicker();
        });
</script>
</body>
</html>



{% endhighlight %}



