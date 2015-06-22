---
layout: post
title: Integration
description: integration
platform: js
control: DatePicker
documentation: ug
---

# Integration

## Angular Binding

**DatePicker** widget is availed with two types of **angular JS** support namely, 

* One way binding

* Two way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **DatePicker** widget. But the changes made in **DatePicker** widget are not reflected or triggered in turn to the scope collection. This kind of binding is applied to all the properties of the **DatePicker** widget.

**Two-way binding** supports both the processes – it applies the scope values to the **DatePicker** properties as well as the changes made in the **DatePicker** widget are also reflected back and triggered within the angular scope change function.

To know more detail about the **Angular binding**, you can refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

> {% include image.html url="/js/DatePicker/Integration_images/Integration_img1.jpeg" Caption=""%}

**Note**: Add the following script files as given in the following example to access angular binding. They have JS library for angular binding.

* angular-min.js

* ej.widget.angular.min.js

The following example depicts the way to bind data to the **DatePicker** widget through **angular support**.

{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateCtrl">
<head>
    <title>Essential Studio for JavaScript : DatePicker - Angular</title>
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="DatePickerCtrl">
    <table>
        <th>
            <div id="control">
                <input id="datepicker" ej-datepicker e-value="dateValue" e-enablestrictmode="true" />
            </div>
        </th>

        <th>
            <div id="binding">
                <input id="datepicker1" ej-datepicker e-value="dateValue" e-enablestrictmode="true" />
            </div>
        </th>
    </table>

    <script type="text/javascript">
        angular.module('DateCtrl', ['ejangular'])
         .controller('DatePickerCtrl', function ($scope) {
             $scope.dateValue = "2/3/2013";
         });
    </script>
    <style type="text/css" class="cssStyles">
        #binding {
            margin-left: 150px;
        }
    </style>
</body>
</html>



{% endhighlight %}



{% include image.html url="/js/DatePicker/Integration_images/Integration_img2.png" Caption="Angular Support in DatePicker"%}

## Knockout Binding

**Knockout** support allows you to bind the **HTML** elements against any of the available data models.

Two types of **Knockout** binding are supported,

* One-way binding

* Two-way binding

**One way binding** refers to the process of applying observable values to all the available properties of the **DatePicker** widget. But the changes made in **DatePicker** widget are not reflected and triggered in turn to the observable collection. This kind of binding is applied to all the properties of the **DatePicker** widget.

**Two-way binding** supports both the processes – it applies the observable values to the **DatePicker** widget properties as well as the changes made in the **DatePicker** widget are also reflected back and triggered within the observable collections. 

For more information about the **Knockout** **binding**, you can refer the following online documentation in the following link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

> {% include image.html url="/js/DatePicker/Integration_images/Integration_img3.jpeg" Caption=""%}**Note**: Add the following script files along with the given code to access knockout binding. They have JS library for knockout binding.

* knockout-min.js

* ej.widget.ko.min.js

The link for those script files are as follows:

[http://cdn.syncfusion.com/js/assets/external/knockout.min.js](http://cdn.syncfusion.com/js/assets/external/knockout.min.js)

[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js)

The following example depicts the way to bind data to the **DatePicker** widget through the **Knockout** support that enables and populate data to a **DatePicker** widget based on the value set to the other **DatePicker** widget.

The following example depicts the way to bind data to the **DatePicker** widget through **Knockout** support.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div class="control" style="float: left">
        <div class="ctrllabel"></div>
        <input id="datepicker1" data-bind="ejDatePicker: { value: value, enableStrictMode: true }" />
    </div>
    <div class="control" style="float: left; margin-left: 20px; height: 30px">
        <div class="ctrllabel"></div>
        <input id="datepicker2" data-bind="ejDatePicker: { value: value, enableStrictMode: true }" />
    </div>

    <script type="text/javascript">

        window.viewModel = {
            value: ko.observable(new Date(2014, 05, 15))
        };
        $(function () {
            // declaration
            ko.applyBindings(viewModel);
        });
    </script>
</body>
</html>

{% endhighlight %}





{% include image.html url="/js/DatePicker/Integration_images/Integration_img4.png" Caption="Knockout Support in DatePicker"%}

