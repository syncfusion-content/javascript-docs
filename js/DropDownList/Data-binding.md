---
layout: post
title: Data-binding
description: data-binding 
platform: js
control: DropDownList
documentation: ug
---

# Data-binding 

## Data fields and configuration

The following sub-properties provides you a way to bind either the local or remote data to the **Dropdown** control.

Properties of JavaScript

<table>
<tr>
<th>Properties</th><th>Description</th></tr>
<tr>
<td>
dataSource</td><td>
The data source contains the list of data for generating the <b>DropDownList</b> items.</td></tr>
<tr>
<td>
query</td><td>
It specifies the query to retrieve the data from the online server.</td></tr>
<tr>
<td>
fields</td><td>
It specifies the mapping fields for the data items of the <b>DropDownList</b> textbox.</td></tr>
<tr>
<td>
id</td><td>
It specifies the ID of the tag.</td></tr>
<tr>
<td>
text</td><td>
It specifies the text content of the tag.</td></tr>
<tr>
<td>
value</td><td>
It specifies the value of the tag.</td></tr>
<tr>
<td>
category</td><td>
It is used to categorize the items and is used when the grouping is enabled.</td></tr>
<tr>
<td>
imageUrl</td><td>
It defines the <b>imageURL</b> for the image location.</td></tr>
<tr>
<td>
imageAttributes</td><td>
It defines the image attributes such as height, width, styles, etc.</td></tr>
<tr>
<td>
spriteCssClass</td><td>
It defines the sprite CSS for the image tag.</td></tr>
<tr>
<td>
htmlAttributes</td><td>
It defines the HTML attributes such as class and styles for an item.</td></tr>
<tr>
<td>
selected</td><td>
This field defines the tag value to be selected initially. Corresponding field mapped has boolean values to select the list items on control creation. The data with value <b>true</b> in this field is selected automatically when the control is initialized.</td></tr>
<tr>
<td>
tableName</td><td>
It defines the table name for the tag value or displays text while rendering remote data.</td></tr>
</table>

## Local data

**Dropdown** provides data binding support for **DropdownList**. Thus you can bind the data from **JSON** Data. To achieve this, you need to map the corresponding file with their column names

And also you need to provide support to add and customize the images and list item by using appropriate data fields. 

The following steps explains you the details of data binding with **DropdownList**. 

In an HTML page, add a &lt;input&gt; element to configure Dropdownlist widget.

{% highlight html %}

<div class="control">
   <div class="ctrllabel">Select a bike</div>
   <input type="text" id="dropdownlist" />
</div>

{% endhighlight %}

{% highlight js %}

        // Initialize the control in JavaScript       
        $(function() {
            // declaration
            BikeList = [{
                id: "bk1",
                text: "Aache RTR"
            }, {
                id: "bk2",
                text: "CBR 150-R"
            }, {
                id: "bk3",
                text: "CBZ Xtreme"
            }, {
                id: "bk4",
                text: "Discover"
            }, {
                id: "bk5",
                text: "Dazzler"
            }, {
                id: "bk6",
                text: "Flame"
            }, {
                id: "bk7",
                text: "Fazzer"
            }, {
                id: "bk8",
                text: "FZ-S"
            }, {
                id: "bk9",
                text: "Pulsar"
            }, {
                id: "bk10",
                text: "Shine"
            }, {
                id: "bk11",
                text: "R15"
            }, {
                id: "bk12",
                text: "Unicorn"
            }];
            $('#dropdownlist').ejDropDownList({
                dataSource: BikeList,
                fields: {
                    id: "id",
                    text: "text",
                    value: "text"
                }
            });
        });

{% endhighlight %}

Output of the above steps

![]("/js/DropDownList/Data-binding_images/Data-binding_img1.png") 

## Remote data

You can bind the data’s for the **DropdownList** from remote, that can fetch the data from any other server that is located as remote web service. By using **query** options, you can pass the query string to filter the data that helps to avoid the extensive properties look up. 

The following steps explains you the details of data binding from remote. 

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

<div class="ctrllabel">Select a customer</div>
<input type="text" id="dropdownlist" />

{% endhighlight %}

{% highlight js %}

       // Initialize the control in JavaScript       
       $(function() {
           // DataManager creation
           var dataManger = ej.DataManager({
               url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
           });
           // Query creation
           var query = ej.Query()
               .from("Customers").take(6);

           $('#dropdownlist').ejDropDownList({
               dataSource: dataManger,
               fields: {
                   text: "CustomerID"
               },
               query: query,
           });
       }); 

{% endhighlight %}

Output of the above steps

![]("/js/DropDownList/Data-binding_images/Data-binding_img2.png") 

## Angular Binding

**DropdownList** widget contains two types of angular **JS** support namely, 

* One way binding
* Two way binding 

One way binding refers to the process of applying scope values to all the available properties of the **Dropdown list** widget, but the changes made in **DropdownList** widget does not reflect or trigger in turn to the scope collection. This kind of binding applies to all the properties of the **DropdownList** widget.

Two-way binding supports both the processes – it applies the scope values to the **Dropdown list** properties as well as the changes made in the **DropdownList** widget is also reflected back and triggered within the angular scope change function.

To know more detail about the Angular binding, you can refer the following link location,

<http://help.syncfusion.com/js/angularjs>

The following example depicts the way to bind data to the **DropdownList** widget through angular support

N>  You need to include “ej.widget.angular.min.js” file library to achieve this behaviour and you need to pass the control properties as data attribute in input tag itself as like data role behaviour.

In the **HTML** page, add a **&lt;input&gt;** element to configure **DropdownList** widget

{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DropCtrl">
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
   <body ng-controller="DropDownCtrl">
      <div class="content-container-fluid">
         <div class="row">
            <div class="cols-sample-area">
               <div class="frame" style="width: 50%; height: 27px">
                  <span>Select a section</span>
                  <div>
                     <div id="control" style="float: left; width: 45%">
                        <input id="dropdownlist" ej-dropdownlist e-datasource="dataList" e-value="value" />
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 4px;">Note:Two Way Angular Support</span></h6>
                     </div>
                  </div>
                  <div id="binding" style="float: right; margin: auto; width: 45%">
                     <input type="text" id="dropValue" class="input ejinputtext" ng-model="value" />
                  </div>
               </div>
            </div>
         </div>
      </div>
   </body>
</html>

{% endhighlight %}

{% highlight js %}

    // Initialize the control and bind the data in JavaScript 
    var list = [
               { id: "cr1", text: "Dodge Avenger" },
               { id: "cr2", text: "Chrysler 200" },
               { id: "cr3", text: "Ford Focus" },
               { id: "cr4", text: "Ford Taurus", },
               { id: "cr5", text: "Dazzler", },
               { id: "cr6", text: "Chevy Spark", },
               { id: "cr7", text: "Chevy Volt", },
               { id: "cr8", text: "Honda Fit", },
               { id: "cr9", text: "Honda Crosstour", },
               { id: "cr10", text: "Acura RL", },
               { id: "cr11", text: "Hyundai Elantra", },
               { id: "cr12", text: "Mazda3", }
    ];
    angular.module('DropCtrl', ['ejangular'])
      .controller('DropDownCtrl', function ($scope) {
          $scope.dataList = list;
          $scope.value = "Ford Focus";
      });

{% endhighlight %}

{% highlight css %}

<style type="text/css">
    .control {
        margin-top: 10px;
    }

    .input {
        height: 27px;
        text-indent: 10px;
        width: 81%;
    }
</style>

{% endhighlight %}

Output of the above steps

![]("/js/DropDownList/Data-binding_images/Data-binding_img4.png") 

## Knockout Binding

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported,

* One-way binding
* Two-way binding

One way binding refers to the process of applying observable values to all the available properties of the **DropdownList**  widget, but the changes made in the widget does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the dropdown list widget.

Two-way binding supports both the processes – it applies the observable values to the **Dropdown List** widget properties as well as the changes made in the dropdown list widget is also reflected back and triggered within the observable collections. 

For more information about the knockout binding, refer the following online documentation in the following link location,

<http://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **DropdownList** widget through the knockout support that enables and populates data to a **DropdownList** widget based on the value set to the other dropdown widget.


N>  You need to include the “ej.widget.knockout.min.js” file library to achieve this behaviour and you need to pass the control properties as data attribute in input tag itself as like data role behaviour.

In an HTML page, add a &lt;input&gt; element to configure DropdownList widget

{% highlight html %}

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
    <div class="control" style="float: left">
        <div class="ctrllabel">Select a section</div>
        <input id="dropdownlist" data-bind="ejDropDownList: { dataSource: dataList, value: value }">
    </div>
    <div class="control" style="float: left; margin-left: 20px; height: 30px">
        <div class="ctrllabel">Knockout textbox binding</div>
        <input type="text" id="Text4" class="input ejinputtext" data-bind="value: value" />
    </div>
</body>
</html>

{% endhighlight %}

{% highlight js %}

    // Initialize the control and bind the data in JavaScript
    $(function () {
        var carList = [
            { id: "cr1", text: "Accordion" },
            { id: "cr2", text: "Autocomplete" },
            { id: "cr3", text: "Button" },
            { id: "cr4", text: "Tab", },
            { id: "cr5", text: "Menu", },
            { id: "cr6", text: "Rating", },
            { id: "cr7", text: "Slider", },
            { id: "cr8", text: "Splitter", },
            { id: "cr9", text: "Tagcloud", },
            { id: "cr10", text: "Scroller", },
            { id: "cr11", text: "TreeView", },
            { id: "cr12", text: "WaitingPopup", }
        ];
        window.viewModel = {
            dataList: ko.observable(carList),
            value: ko.observable("Button"),
        }
        ko.applyBindings(viewModel);
    });
        
{% endhighlight %}

{% highlight css %}

<style type="text/css">
    .ejinputtext {
        background-color: #fff;
        border: 1px solid #bbbcbb;
        color: #5c5c5c;
        height: 30px;
        outline: medium none;
    }
</style>

{% endhighlight %}

Output of the above steps

![]("/js/DropDownList/Data-binding_images/Data-binding_img6.png") 
