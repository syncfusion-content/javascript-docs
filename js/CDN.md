---
layout: post
title: CDN links for Syncfusion Essential JS widgets
description: Learn how to add  CDN links for syncfusion essential js widgets and dependent scripts.
platform: js
control: Introduction
documentation: ug
---

# CDN

The [CDN](http://en.wikipedia.org/wiki/Content_delivery_network) links are provided individually for all the scripts and style sheets of Syncfusion Essential JS components. 


## CDN scripts links

### External dependency libraries

The basic syntax follows below,


http://cdn.syncfusion.com/js/assets/external/**[fileName]**

_Example: http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js_  

N>  The first three script libraries listed below are mandatory to render any of the Syncfusion Essential JS widgets.

<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
jQuery 1.10.2</td><td>
Common jQuery script to render any of the Syncfusion widgets</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js">https://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js">http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js</a>
</td></tr>
<tr>
<td>
jQuery.easing</td><td>
Supports animation</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js">https://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js</a></td></tr>
<tr>
<td>
JsRender</td><td>
Supports template rendering</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/jsrender.min.js">https://cdn.syncfusion.com/js/assets/external/jsrender.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js">http://cdn.syncfusion.com/js/assets/external/jsrender.min.js</a>  </td></tr>
<tr>
<td>
AngularJS</td><td>
Minified AngularJS file to support custom directives.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/angular.min.js">https://cdn.syncfusion.com/js/assets/external/angular.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/angular.min.js">http://cdn.syncfusion.com/js/assets/external/angular.min.js</a></td></tr>
<tr>
<td>
excanvas</td><td>
To support canvas element rendering in IE8 browser</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/excanvas.min.js">https://cdn.syncfusion.com/js/assets/external/excanvas.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/excanvas.min.js">http://cdn.syncfusion.com/js/assets/external/excanvas.min.js</a></td></tr>
<tr>
<td>
KnockoutJS</td><td>
Minified KnockoutJS file to support the observable binding. </td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/knockout.min.js">https://cdn.syncfusion.com/js/assets/external/knockout.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/knockout.min.js">http://cdn.syncfusion.com/js/assets/external/knockout.min.js</a></td></tr>
<tr>
<td>
RequireJS</td><td>
Supports loading of required dependencies</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/require.min.js">https://cdn.syncfusion.com/js/assets/external/require.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/require.min.js">http://cdn.syncfusion.com/js/assets/external/require.min.js</a> </td></tr>
<tr>
<td>
jQuery.validate</td><td>
Supports client-side validation</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js">https://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js</a></td></tr>
<tr>
<td>
jQuery.validate.unobtrusive</td><td>
To enable unobtrusive validation options in <b>data-*</b> attributes</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js">https://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js">http://cdn.syncfusion.com/js/assets/external/jquery.validate.unobtrusive.min.js</a></td></tr>
</table>

### Syncfusion Dependency Libraries - Based on latest build version

The CDN script files are maintained for each version of the Essential Studio individually. Refer the following syntax:

http://cdn.syncfusion.com/**[version]**/js/web/**[fileName]**

_Example, to access the ej.web.all.min.js file in {{ site.releaseversion }} version – http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js_


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
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js</a> </td></tr>
<tr>
<td>
ej.webform.min</td><td>
supports server-side event functionalities in ASP.NET controls</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.webform.min.js">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.webform.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.webform.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.webform.min.js</a></td></tr>
<tr>
<td>
ej.unobtrusive.min</td><td>
Supports Syncfusion widgets to render in HTML5 format.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js</a>  </td></tr>
<tr>
<td>
ej.widget.angular.min</td><td>
Provides support for AngularJS </td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js</a></td></tr>
<tr>
<td>
ej.widget.ko.min</td><td>
Provides support for KnockoutJS</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js</a></td></tr>
</table>


The **KnockoutJS** and **AngularJS** dependencies can be accessed through the following syntax,

http://cdn.syncfusion.com/**[version]**/js/common/**[fileName]**

_Example, to access the ej.widget.angular.min.js file in {{ site.releaseversion }} version – http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js_


## CDN style sheet links

The CDN links for all the CSS files are provided in the below table. Refer the following syntax:

http://cdn.syncfusion.com/**[version]**/js/web/**[fileName]** – Core 

http://cdn.syncfusion.com/**[version]**/js/web/**[theme-name]**/**[fileName]** – Theme related


<table>
<tr>
<th>
Name</th><th>
Details</th><th>
CDN link</th></tr>
<tr>
<td>
Flat-Azure (default theme)</td><td>
Includes the CSS properties defined for all the widgets in flat-azure theme. (Default-theme)</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Azure Dark</td><td>
Includes the CSS properties defined for all the widgets in flat-azure dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.web.all.min.css</a>  </td></tr>
<tr>
<td>
Flat-lime</td><td>
Includes the CSS properties defined for all the widgets in flat-lime theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-lime Dark</td><td>
Includes the CSS properties defined for all the widgets in flat-lime dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-lime-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Saffron</td><td>
Includes the CSS properties defined for all the widgets in flat-saffron theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Flat-Saffron Dark</td><td>
Includes the CSS properties defined for all the widgets in flat-saffron dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-saffron-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Azure</td><td>
Includes the CSS properties defined for all the widgets in gradient-azure theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure/ej.web.all.min.css</a>  </td></tr>
<tr>
<td>
Gradient-Azure Dark</td><td>
Includes the CSS properties defined for all the widgets in gradient-azure dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-azure-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-lime</td><td>
Includes the CSS properties defined for all the widgets in gradient-lime theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-lime Dark</td><td>
Includes the CSS properties defined for all the widgets in gradient-lime dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-lime-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Saffron</td><td>
Includes the CSS properties defined for all the widgets in gradient-saffron theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Gradient-Saffron Dark</td><td>
Includes the CSS properties defined for all the widgets in gradient-saffron dark theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/gradient-saffron-dark/ej.web.all.min.css</a></td></tr>
<tr>
<td>
Bootstrap-theme</td><td>
Includes the CSS properties defined for all the widgets in bootstrap theme.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/bootstrap-theme/ej.web.all.min.css</a></td></tr>
<tr>
<td>
ej.responsive.css</td><td>
To make the widget responsive, it is necessary to refer this CSS file.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css</a><br>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css</a></td></tr>
</table>

## Refer CDN links for specific theme

Below table provides the links for the `Flat-Azure` and `Flat-Azure Dark` themes . Likewise, you can refer for any of the 13 available themes just by referring the required `ej.theme.min.css` available under each of the theme folders along with the widget core file.

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
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css</a><br/>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.theme.min.css</a><br/></td></tr>
<tr>
<td>
Flat-Azure Dark</td><td>
Here, the widget core file (<b>ej.widget.core.min.css</b>) is common and the theme file <b>ej.theme.min.css</b> is uniquely available under the <b>flat-azure-dark</b> theme folder.</td><td>
Secured Link:
<a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css">https://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css</a><br/>
Unsecured Link:
<a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.widgets.core.min.css</a><br/><br/><a href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css">http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure-dark/ej.theme.min.css</a><br/></td></tr>
</table>

N>    All the provided CDN links can be accessed either through `http` or `https`.


## Refer local Scripts and CSS, when CDN fails

One of the major risk with CDN links is that – sometimes it may go down due to the network or connection problems. On such scenarios, we can refer the local scripts and CSS files dynamically in the application by checking if the scripts and CSS files loaded through CDN returns `undefined` as depicted below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    // CDN LINK references
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jsrender.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script type="text/javascript">

        if (typeof jQuery == "undefined") { // If CDN fails, jQuery returns undefined
            // Referring local scripts - Specify the path where the below files are located in your machine
            document.write(decodeURIComponent('%3Cscript src="Scripts/jquery-1.10.2.min.js" %3E%3C/script%3E'));
            document.write(decodeURIComponent('%3Cscript src="Scripts/jquery.easing.1.3.min.js" %3E%3C/script%3E'));
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

