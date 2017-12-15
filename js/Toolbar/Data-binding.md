---
layout: post
title: Data-binding
description: data binding
platform: js
control: Toolbar
documentation: ug
api: /api/js/ejtoolbar
---

# Data binding

**Toolbar** provides you a flexible approach for binding data from various data sources. There are various properties in **Toolbar** for Data Binding.

## Data fields and configuration 

The following sub-properties provides a way to bind either the local/remote data to the **Toolbar** control.

Property Table of JavaScript Toolbar control

<table>
<tr>
<th>
Property</th><th>
Syntax</th><th>
Description</b></th></tr>
<tr>
<td>
[dataSource](https://help.syncfusion.com/api/js/ejtoolbar#members:datasource)</td><td>
dataSource: window.countriesField</td><td>
It specifies the data source of the Toolbar. The data source contains the list of data for generating the Toolbar items. By default, its value is null and its data type is object. </td></tr>
<tr>
<td>
field</td><td>
fields: {text: "name", value: "key" }</td><td>
It specifies the mapping fields for the data items of the Toolbar. By default, its value is null and its data type is object.</td></tr>
<tr>
<td>
[query](https://help.syncfusion.com/api/js/ejtoolbar#members:query)</td><td>
query: ej.Query().from("Suppliers").select("ContactName");       	 </td><td>
It specifies the query to retrieve the data from online server. By default, its value is null and its data type is object. </td></tr>
<tr>
<td>
[id](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-id)</td><td>
id</td><td>
It specifies the id of the tag and its default value is null and data type is string. </td></tr>
<tr>
<td>
[text](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-text)</td><td>
text</td><td>
It specifies the text content of the tag and its default value is null and data type is string. </td></tr>
<tr>
<td>
[imageUrl](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-imageurl)</td><td>
imageUrl</td><td>
This property defines the imageURL for the image location. While setting images, the folder name in which the images are stored should be set to imageUrl property. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
[imageAttributes](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-imageattributes)</td><td>
imageAttributes</td><td>
This property defines style for the image. While setting an image, styles can be applied such as height, width by using this property. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
[spriteCssClass](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-spritecssclass)</td><td>
spriteCssClass</td><td>
This property sets the Sprite CSS for the image tag in Toolbar. The value set to this property should be <b>string</b> type.</td></tr>
<tr>
<td>
[htmlAttributes](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-htmlattributes)</td><td>
htmlAttributes</td><td>
This property sets the <b>HTML</b> attribute for the Toolbar item. The value set to this property should be <b>object</b> type. It can be any <b>HTML</b> attribute such as id, class, style.</td></tr>
<tr>
<td>
[tooltipText](https://help.syncfusion.com/api/js/ejtoolbar#members:fields-tooltiptext)  </td><td>
tooltipText  </td><td>
This property sets the text value for Toolbar item while mouse over in Toolbar. The value set to this property should be <b>string</b> type.</td></tr>
</table>

## Local data

**Toolbar** provides you an extensive data binding support to generate **Toolbar** items, that the values can be mapped to the **ToolBar** [fields](https://help.syncfusion.com/api/js/ejtoolbar#members:fields), namely **key** and **text**.

And also you can add image, image styles, sprite CSS class, query and HTML attributes options with data binding fields. The following code explains the details about the data binding with **Toolbar**. 

{% highlight html %}

    <div class="cols-sample-area">
        <div id="toolbarJson"></div>
    </div>
    
{% endhighlight %}

{% highlight javascript %}

    $(function () {
        BrowserItems = [{
            employeeId: "1",
            spriteCss: "Browsers ie-browser",
            title: "Internet Explorer",

        }, {
            employeeId: "2",
            spriteCss: "Browsers chrome-browser",
            title: "Chrome",
        }, {
            employeeId: "3",
            spriteCss: "Browsers firefox-browser",
            title: "Firefox",

        }, {
            employeeId: "4",
            spriteCss: "Browsers bitty-browser",
            title: "Bitty",

        }, {
            employeeId: "5",
            spriteCss: "Browsers opera-browser",
            title: "Opera",

        }
        ];
        $("#toolbarJson").ejToolbar({
            dataSource: BrowserItems,
            fields: { id: "employeeId", spriteCssClass: "spriteCss", tooltipText:"title" },
            orientation: ej.Orientation.Horizontal,
            width: "100%"
        });
    });

{% endhighlight %}

{% highlight css %}

<style type="text/css" class="cssStyles">
    .darktheme .cols-sample-area .e-tooltxt .Browsers {
        background-image: url('../content/images/toolbar/browserd.png');
    }

    .cols-sample-area .e-tooltxt .Browsers {
        display: block;
        background-image: url('../content/images/toolbar/browserl.png');
        height: 32px;
        width: 32px;
        background-repeat: no-repeat;
    }

    .e-tooltxt:hover .Browsers, .darktheme .cols-sample-area .e-tooltxt:hover .Browsers {
        background-image: url('../content/images/toolbar/browserh.png');
    }

    .Browsers.ie-browser {
        background-position: -84px 0px;
    }

    .Browsers.chrome-browser {
        background-position: -42px 0px;
    }

    .Browsers.firefox-browser {
        background-position: 0px 0px;
    }

    .Browsers.bitty-browser {
        background-position: -126px 0px;
    }

    .Browsers.opera-browser {
        background-position: -168px 0px;
    }
    .material .frame{
        width: 360px;
    }
</style>


{% endhighlight %}

![](/js/Toolbar/Data-binding_images/Data-binding_img1.png) 


## Remote data

You can bind the data for the **Toolbar** items from remote. That is, you can access the data from any other server that is located as remote web service. It uses DataManager to retrieve data and you can create DataManager with its **URL**. To create DataManager, define ej.DataManager() to a variable. Then provide online link to **url** property. Assign this variable to **Toolbar** dataSource. 

To bind Remote data to **Toolbar** and [query](https://help.syncfusion.com/api/js/ejtoolbar#members:query) is used to get the data, use the following code example.

{% highlight html %}

<div id="toolbar"></div>

{% endhighlight %}

{% highlight javascript %}

    $(function () {
        // DataManager creation
        var dataManger = ej.DataManager({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        // Query creation
        var query = ej.Query()
             .from("Orders").take(6);

        $("#toolbar").ejToolbar({
            dataSource: dataManger,
            fields: { text: "CustomerID" },
            query: query,
            orientation: "horizontal",
            width: "340px"
        });
    });

{% endhighlight %}


![](/js/Toolbar/Data-binding_images/Data-binding_img2.png) 

## KnockoutJS binding

KnockoutJS support allows you to bind the **HTML** elements against any of the available data models.

Two types of KnockoutJS binding is supported,

* One-way binding
* Two-way binding

One-way binding refers to the process of applying observable values to all the available properties of the **Toolbar**, where the changes made in **Toolbar** widget is not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **Toolbar**.

Two-way binding supports both the processes – it applies the observable values to the **Toolbar** properties as well as the changes made in the Toolbar widget is reflected back and triggered within the observable collections. 

For more information about the KnockoutJS binding, refer the following link location,

<https://help.syncfusion.com/js/knockoutjs>


N> Add the following script files along with the specified code to access KnockoutJS binding. It contains JS library for KnockoutJS binding.

* Knockout.min.js
* ej.widget.ko.min.js

The link for the script file is as follows:

[http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js](http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js)


The following code example depicts you the way to bind data to the **Toolbar** through the KnockoutJS support. 

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
   <head>
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js"></script>
   </head>
   <body>
      <div class="cols-sample-area">
         <div id="toolbar" data-bind="ejToolbar:{ dataSource:dataList, fields:{ id:'id', spriteCssClass:'spriteCss', text:'text'}, width:width }"></div>
      </div>
   </body>
</html>

    
 {% endhighlight %}
    
 ![](/js/Toolbar/Data-binding_images/Data-binding_img4.png)
    

## AngularJS binding
    
**Toolbar** is availed with two types of **AngularJS** support namely, 

* One way binding
* Two way binding 

One-way binding refers to the process of applying scope values to all the available properties of the Toolbar, where the changes made in **Toolbar** widget is not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **Toolbar**.

Two-way binding supports both the processes – it applies the scope values to the **Toolbar** properties as well as the changes made in the **Toolbar** widget is also reflected back and triggered within the AngularJS scope change function.

To know more detail about the AngularJS binding, refer the following link location,

<https://help.syncfusion.com/js/angularjs>


Add the following script files as given in the below example to access KnockoutJS binding. It contains JS library for AngularJS binding.

* Angular.min.js
* ej.widget.angular.min.js

The following code example depicts you the way to bind data to the **Toolbar** widget through AngularJS support,

{% highlight html %}
    
   
<!DOCTYPE html>
<html lang="en" ng-app="toolApp">
   <head>
      <title>Essential Studio for JavaScript :AngularJS Support for Toolbar</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css"rel="stylesheet"/>
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"> </script>
   </head>
   <body ng-controller="ToolCtrl">
      <div class="cols-sample-area">
         <div id="toolbar" ej-toolbar e-datasource="dataList" e-width="230px"
            e-fields-id="id" e-fields-spritecssclass="spriteCss">
         </div>
      </div>
   </body>
</html>

{% endhighlight %}



{% highlight javascript %}

    var list = [{
        id: "1",
        spriteCss: "ToolbarItems LeftAlign_tool",

    }, {
        id: "2",
        spriteCss: "ToolbarItems CenterAlign_tool",
    }, {
        id: "3",
        spriteCss: "ToolbarItems RightAlign_tool",
    }, {
        id: "4",
        spriteCss: "ToolbarItems Justify_tool",

    }, {
        id: "5",
        spriteCss: "ToolbarItems Bold_tool",
    }, {
        id: "6",
        spriteCss: "ToolbarItems Italic_tool",
    }, {
        id: "7",
        spriteCss: "ToolbarItems StrikeThrough_tool",
    }, {
        id: "8",
        spriteCss: "ToolbarItems Underline_tool",
    }
    ];

    angular.module('toolApp', ['ejangular']).controller('ToolCtrl', function ($scope) {
        $scope.dataList = list;
    });

{% endhighlight %}



{% highlight css %}


<style type="text/css" class="cssStyles">
    /*controls*/
    .darktheme .cols-sample-area .e-tooltxt .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-metro.png');
    }

    .cols-sample-area .e-tooltxt .ToolbarItems {
        display: block;
        background-image: url('../images/toolbar/ui-icons-dark.png');
        height: 22px;
        width: 22px;
    }

    .e-tooltxt:hover .ToolbarItems, .darktheme .cols-sample-area .e-tooltxt:hover .ToolbarItems {
        background-image: url('../images/toolbar/ui-icons-light.png');
    }

    .ToolbarItems.LeftAlign_tool {
        background-position: -26px -39px;
    }

    .ToolbarItems.CenterAlign_tool {
        background-position: -55px -39px;
    }

    .ToolbarItems.RightAlign_tool {
        background-position: -89px -39px;
    }

    .ToolbarItems.Justify_tool {
        background-position: -123px -39px;
    }

    .ToolbarItems.Bold_tool {
        background-position: -159px -39px;
    }

    .ToolbarItems.Italic_tool {
        background-position: -196px -39px;
    }

    .ToolbarItems.StrikeThrough_tool {
        background-position: -55px -70px;
    }

    .ToolbarItems.Underline_tool {
        background-position: -23px -68px;
    }
</style>


{% endhighlight %}

![](/js/Toolbar/Data-binding_images/Data-binding_img6.png)

