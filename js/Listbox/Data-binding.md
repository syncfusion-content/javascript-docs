---
layout: post
title: Data-binding
description: data-binding 
platform: js
control: ListBox
documentation: ug
---

# Data-binding 

The **ListBox** is populated with the node information taken from a data source. The **ListBox** supports binding data sources containing hierarchical data.

## Data fields and configuration

The following sub-properties provides you a way to bind either the local or remote data to the **ListBox** control.

Property Table for JavaScript ListBox

<table>
<tr>
<th>Name</th><th>Description</th></tr>
<tr>
<td>
dataSource</td><td>
The data source contains the list of data for generating the ListBox items</td></tr>
<tr>
<td>
query</td><td>
It specifies the query to retrieve the data from online server</td></tr>
<tr>
<td>
fields</td><td>
It specifies the mapping fields for the data items of the ListBox</td></tr>
<tr>
<td>
id</td><td>
It specifies the id of the tag</td></tr>
<tr>
<td>
text</td><td>
It specifies the text content of the tag</td></tr>
<tr>
<td>
value</td><td>
It specifies the value of the tag</td></tr>
<tr>
<td>
imageUrl</td><td>
It’s defines the imageURL for the image location</td></tr>
<tr>
<td>
imageAttributes</td><td>
It’s defines the image attributes such as height, width, styles and so on</td></tr>
<tr>
<td>
spriteCssClass</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
htmlAttributes</td><td>
It defines the html attributes such as id, class, styles for the item</td></tr>
<tr>
<td>
selected</td><td>
It defines the tag value to be selected initially</td></tr>
<tr>
<td>
toolTipText  </td><td>
It specifies the Tooltip text  of the tag</td></tr>
<tr>
<td>
category</td><td>
It specifies the category of the tag</td></tr>
<tr>
<td>
tableName</td><td>
It defines the table name for tag value or display text while render with remote data</td></tr>
</table>

## Local data

**ListBox** provides data binding support. Thus, you can bind the data from **JSON** Data source. To achieve this, map the corresponding fields with their column names.

And also, provide support to add and customize the list item by using appropriate data fields. 

The following steps explains you the details of data binding with **ListBox**. 

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}


    jQuery(function ($) {
        // JSON data declaration
        var skillset = [
            { skill: "ASP.NET" }, { skill: "ActionScript" }, { skill: "Basic" },
            { skill: "C++" }, { skill: "C#" }, { skill: "dBase" }, { skill: "Delphi" },
            { skill: "ESPOL" }, { skill: "F#" }, { skill: "FoxPro" }, { skill: "Java" },
            { skill: "J#" }, { skill: "Lisp" }, { skill: "Logo" }, { skill: "PHP" }
        ];
        //Render ListBox by mapping fields with JSON data
        $("#listboxSample").ejListBox({
            width: "350", dataSource: skillset,
            fields: { text: "skill" }
        });
    });


{% endhighlight %}

Output of the above steps

![](/js/ListBox/Data-binding_images/Data-binding_img1.png) 


## Remote data

You can bind the data for the **ListBox** from remote that can fetch the data from remote web service. You can pass the query string to filter the data that helps to avoid the extensive properties look up by using **query** options. 

The following steps explains you the details of data binding from remote. 

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}

<div id="control">
    <h5 class="ctrllabel">Select a skill</h5>
    <ul id="listboxSample"></ul>
</div>

{% endhighlight %}

{% highlight js %}

    $(function () {
        // DataManager creation
        var dataManger = ej.DataManager({
            url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
        });
        // Query creation
        var query = ej.Query()
               .from("Customers").take(16);
    
        $('#listboxSample').ejListBox({
            dataSource: dataManger,
            width: "350",
            fields: { text: "CustomerID" },
            query: query,
        });
    });


{% endhighlight %}


 Output of the above steps.

![](/js/ListBox/Data-binding_images/Data-binding_img2.png) 


## Angular binding

**ListBox** widget contains two types of angular **JS** support namely, 

* One way binding
* Two way binding 

One way binding refers to the process of applying scope values to all the available properties of the **ListBox** widget, but the changes made in **ListBox** widget does not reflect or trigger in turn to the scope collection. This kind of binding applies to all the properties of the **ListBox** widget.

Two-way binding supports both the processes – it applies the scope values to the **ListBox** properties as well as the changes made in the **ListBox** widget is also reflected back and triggered within the angular scope change function.

To know more detail about the Angular binding, you can refer the following link location,

<http://help.syncfusion.com/js/angularjs>

The following example depicts the way to bind data to the **ListBox** widget through angular support.

N> You can include the “ej.widget.angular.min.js” file library to achieve this behaviour and you can pass the control properties as data attribute in ul tag itself as like data role behaviour.

In the HTML page, add a &lt;ul&gt; element to configure ListBox widget.

{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="ListCtrl">
<head>
    <title>Essential Studio for JavaScript :  Angular</title>
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="ListBoxCtrl">
    <div id="control" style="height: 300px;">
        <table>
            <tr>
                <td>
                    <div class="ctrllabel">Select a section</div>
                    <ul id="bookselect" ej-listbox e-datasource="dataList" e-value="value"></ul>
                </td>
                <td id="binding">
                    <div>
                        <input type="text" id="dropvalue" class="input ejinputtext" ng-model="value" />
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span></h6>
                    </div>
                </td>
            </tr>
        </table>
    </div>


    <script type="text/javascript">
        // Initializes the control and binds the data in JavaScript
        var list = [
                    { empid: "cr1", text: "Dodge Avenger" },
                    { empid: "cr2", text: "Chrysler 200" },
                    { empid: "cr3", text: "Ford Focus" },
                    { empid: "cr4", text: "Ford Taurus", },
                    { empid: "cr5", text: "Dazzler", },
                    { empid: "cr6", text: "Chevy Spark", },
                    { empid: "cr7", text: "Chevy Volt", },
                    { empid: "cr8", text: "Honda Fit", },
                    { empid: "cr9", text: "Honda Crosstour", },
                    { empid: "cr10", text: "Acura RL", },
                    { empid: "cr11", text: "Hyundai Elantra", },
                    { empid: "cr12", text: "Mazda3", }
        ];
        angular.module('ListCtrl', ['ejangular'])
           .controller('ListBoxCtrl', function ($scope) {
               $scope.dataList = list;
               $scope.value = "Ford Focus";
           });
    </script>

    <style>
        #binding {
            width: 100px;
            padding-bottom: 216px;
            padding-left: 100px;
        }
    </style>
</body>
</html>



{% endhighlight %}

Output of the above steps.

![](/js/ListBox/Data-binding_images/Data-binding_img3.png) 


## Knockout binding

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One way binding
* Two way binding 

One way binding refers to the process of applying observable values to all the available properties of the **ListBox** widget, but the changes made in the widget does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the ListBox widget.

Two-way binding supports both the processes – it applies the observable values to the **ListBox** widget properties as well as the changes made in the ListBox widget is also reflected back and triggered within the observable collections. 

For more information about the knockout binding, refer the following online documentation in the following link location,

<http://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **ListBox** widget through the knockout support that enables and populates data to a **ListBox** widget based on the value set to the other **ListBox** widget.


N> You can include the “ej.widget. knockout.min.js” file library to achieve this behaviour and you can pass the control properties as data attribute in ul tag itself as like data role behaviour.

In an **HTML** page, add a **&lt;ul&gt;** element to configure **ListBox** widget.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body>

    <div id="control">
        <table>
            <tr>
                <td>
                    <div class="ctrllabel">Select a section</div>
                    <ul id="controlselect" data-bind="ejListBox: { dataSource: dataList, value: value }"></ul>
                </td>
                <td id="binding">
                    <div>
                        <input type="text" id="dropvalue" class="input ejinputtext" data-bind="value: value" />
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Knockout Support</span></h6>
                    </div>
                </td>
            </tr>
        </table>
    </div>

    <script type="text/javascript">
        $(function () {
            var carList = [
                { empid: "cr1", text: "Accordion" },
                { empid: "cr2", text: "Autocomplete" },
                { empid: "cr3", text: "Button" },
                { empid: "cr4", text: "Tab", },
                { empid: "cr5", text: "Menu", },
                { empid: "cr6", text: "Rating", },
                { empid: "cr7", text: "Slider", },
                { empid: "cr8", text: "Splitter", },
                { empid: "cr9", text: "Tagcloud", },
                { empid: "cr10", text: "Scroller", },
                { empid: "cr11", text: "TreeView", },
                { empid: "cr12", text: "WaitingPopup", }
            ];
            window.viewModel = {
                dataList: ko.observable(carList),
                value: ko.observable("Button"),
            }
            ko.applyBindings(viewModel);
        });
    </script>
    <style type="text/css">
        .ejinputtext {
            background-color: #fff;
            border: 1px solid #bbbcbb;
            color: #5c5c5c;
            height: 30px;
            outline: medium none;
            text-indent: 10px;
        }

        #binding {
            width: 100px;
            padding-bottom: 216px;
            padding-left: 100px;
        }
    </style>
</body>
</html>



{% endhighlight %}

Output of the above steps.

![](/js/ListBox/Data-binding_images/Data-binding_img4.png) 


