---
layout: post
title: Angular-Support
description: angular support
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# AngularJS Support

**TimePicker** widget is availed with two types of **AngularJS** support namely, 

* One way binding
* Two way binding 



One way binding refers to the process of applying scope values to all the available properties of the **TimePicker** widget where the changes made in the widget is not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **TimePicker** widget.

Two-way binding supports both the processes – it applies the scope values to the **TimePicker** properties as well as the changes made in the widget is also reflected back and triggered within the AngularJS scope change function.

Apply the plugin and property assigning to the **TimePicker** widget element through the directive that starts with a letter **“e-“.**

To know more details about AngularJS binding, refer the following link location,

<https://help.syncfusion.com/js/angularjs>

The following code example depicts you the way to bind data to the **TimePicker** widget through AngularJS support,


{% highlight html %}


<html ng-app="TimeCtrl">
<head>
    <title>Essential Studio for JavaScript : Timepicker AngularJS</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js"> </script>
</head>
<body ng-controller="TimePickerCtrl">
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame" style="width: 30%; height: 17px;">
                    <div id="control" style="float: left;width: 45%;">
                        <input id="time" type="text" ej-timepicker e-value="timePickerValue" />
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 5px;">Note:Two Way AngularJS Support</span></h6>
                    </div>
                    <div id="binding" style=" float: right;width: 45%;">
                        <input id="timectrl" type="text" ej-timepicker e-value="timePickerValue" e-interval="10" />
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script type="text/javascript">
        angular.module('TimeCtrl', ['ejangular'])
               .controller('TimePickerCtrl', function ($scope) {
                   $scope.timePickerValue = "12:50 AM";
               });
    </script>
    <style type="text/css" class="cssStyles">
        .control {
            margin: 0 auto;
            width: 136px;
        }

        #time_timeWidget, #timectrl_timeWidget {
            width: 84%;
        }

        #timeValue {
            text-indent: 10px;
        }
    </style>
</body>
</html>


{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

Execute the above code to render the following output.



![](/js/TimePicker/Angular-Support_images/Angular-Support_img1.png) 

