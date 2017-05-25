---
layout: post
title: Knockout-Binding
description: knockout binding
platform: js
control: ColorPicker
documentation: ug
api: /api/js/ejcolorpicker
---

# Knockout Binding

**Knockout** support allows you to bind the **HTML** elements against any of the available data models.

Two types of Knockout binding is supported,

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **ColorPicker** widget. The changes made in **ColorPicker** widget are not reflected and triggered in turn to the observable collection. This kind of binding is applied to all the properties of the **ColorPicker** widget.

**Two-way binding** supports both the processes. It applies the observable values to the **ColorPicker** widget properties and also the changes made in the **ColorPicker** widget are reflected back and triggered within the observable collections. 

For more information about **Knockout** binding, you can refer to the online documentation in the following link location,

<https://help.syncfusion.com/js/knockoutjs>

The following example depicts how you can bind data to the **ColorPicker** widget through **knockout** support that enables and populates data to a **ColorPicker** widget based on the value set to the other **ColorPicker** widget.



{% highlight html %}


<!doctype html>
<html>
<head>
    <title>Essential Studio for JavaScript : ColorPicker - Knockout</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"   />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div class="content-container-fluid">
        <div class="row" style="width: 100%">
            <div class="cols-sample-area" style="width: 100%">
                <div class="frame" style="width: 420px">
                    <div id="control" style="float: left; width: 70%; margin-left: 10px">
                        <input id="colorpick" data-bind="ejColorPicker: { value: value, modelType: palette }" />
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 5px;">Note:Two Way Knockout Support</span></h6>
                    </div>
                    <div id="binding" style="float: left; width: 23%">
                        <input id="colorpick1" data-bind="ejColorPicker: { value: value, modelType: picker }" />
                    </div>
                </div>
            </div>
        </div>
    </div>
    <script>
        window.viewModel = {
            value: ko.observable("#278787"),
            palette: ko.observable("palette"),
            picker: ko.observable("picker")
        };
        $(function () {
            ko.applyBindings(viewModel);
        });
    </script>
    <style>
        .element {
            display: inline-block;
        }

        .frame {
            width: 600px;
            border: 0px;
        }

        #control {
            width: 600px;
        }
    </style>
</body>
</html>


{% endhighlight %}


N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

The following screenshot displays the output of the above code example.



![](/js/ColorPicker/Knockout-Binding_images/Knockout-Binding_img1.png) 

