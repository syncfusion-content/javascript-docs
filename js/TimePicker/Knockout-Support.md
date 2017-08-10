---
layout: post
title: Knockout-Support
description: knockout support
platform: js
control: TimePicker
documentation: ug
api: /api/js/ejtimepicker
---

# Knockout Support

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of Knockout binding supported,

* One-way binding
* Two-way binding



One way binding refers to the process of applying observable values to all the available properties of the **TimePicker** widget, where the changes made in the widget is not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **TimePicker** widget.

Two-way binding supports both the processes – it applies the observable values to the **TimePicker** widget properties as well as the changes made in the **TimePicker** widget is also reflected back and triggered within the observable collections. 

For more information about the Knockout binding, refer the following link location,

<https://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **TimePicker** widget through the Knockout support that enables and populate data to **TimePicker** widget based on the value set to another **TimePicker** widget.

{% highlight html %}

<html>
<head>
    <title>Essential Studio for JavaScript : Timepicker Knockout</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.ko.min.js"></script>
    <!--Add custom scripts here -->
</head>
<body>
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame">
                    <div class="control" style="width: 136px;">
                        <label style="width: 130px;">Select Show Time </label>
                        <input id="time" type="text" data-bind="ejTimePicker:{value:timePickerValue }" />
                    </div>
                </div>
            </div>
            <div id="sampleProperties">
                <div class="prop-grid">
                    <div class="row">
                        <div class="col-md-3">Time Value</div>
                        <div class="col-md-3">
                            <input type="text" id="timeValue" class="input ejinputtext" value="" data-bind="value: timePickerValue" />
                        </div>
                        <div class="col-md-3">Selected time</div>
                        <div class="col-md-3">
                            <input type="button" class="e-btn inputBtn" id="getTime" value="Get Time" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <script type="text/javascript">
        window.viewModel = {
            //timepicker
            timePickerValue: ko.observable("11:30 AM")
        }
        $(function () {
            // declaration
            ko.applyBindings(viewModel);
            var timeObj = $('#time').data("ejTimePicker");
            $("#getTime").click(function () {
                alert("Selected time is : " + timeObj.getValue());
            });
            $("#sampleProperties").ejPropertiesPanel();
        });
    </script>
    <style>
        .col-md-3 {
            padding-bottom: 5px;
        }

        .cols-sample-area {
            width: 200px;
            height: 80px;
            float: left;
        }
    </style>
</body>
</html>


{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.


Execute the above code to render the following output.

![](/js/TimePicker/Knockout-Support_images/Knockout-Support_img1.png) 

