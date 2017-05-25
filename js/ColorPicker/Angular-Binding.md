---
layout: post
title: Angular-Binding
description: angular binding
platform: js
control: ColorPicker
documentation: ug
api: /api/js/ejcolorpicker
---

# AngularJS Binding

The **ColorPicker** widget is availed with two types of **angularJS** support namely, 

* One-way binding
* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **ColorPicker** widget. The changes made in **ColorPicker** widget are not reflected or triggered in turn to the scope collection. This kind of binding is applied to all the properties of the **ColorPicker** widget.

**Two-way binding** supports both the processes. It applies the scope values to the **ColorPicker** properties, as well as the changes made in the **ColorPicker** widget are reflected back and triggered within the AngularJS scope change function.

Apply the plugin and property assigning to the **ColorPicker** widget element through the directive that starts with **“e-“.**

To know more about the **Angular** binding, you can refer to the online documentation in the following link location,

<https://help.syncfusion.com/js/angularjs>

The following code example depicts the way to bind data to the **ColorPicker** widget through **angular** support.



{% highlight html %}

<!doctype html>
<html lang="en" ng-app="PickerCtrl">
<head>
    <meta charset="utf-8">
    <title>Essential Studio for JavaScript : ColorPicker - AngularJS support</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"   />
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="ColorPickerCtrl">
    <div class="content-container-fluid">
        <div class="row" style="width: 100%">
            <div class="cols-sample-area" style="width: 100%">
                <div class="frame">
                    <div id="control">
                        <div class="element" style="margin-left: 45px;">
                            <input id="picker" ej-colorpicker e-value="colorValue" e-modeltype="palette" />
                        </div>
                        <div class="element" style="margin-left: 234px">
                            <input id="custom" ej-colorpicker e-value="colorValue" e-modeltype="picker" />
                        </div>
                        <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 5px;margin-left: 45px;">Note:Two Way AngularJS Support</span></h6>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <script>
        angular.module('PickerCtrl', ['ejangular'])
          .controller('ColorPickerCtrl', function ($scope) {
              $scope.colorValue = "#278787";
          });
    </script>
    <style>
        .element {
            display: inline-block;
        }

        .frame {
            width: 457px;
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

![](/js/ColorPicker/Angular-Binding_images/Angular-Binding_img1.png)

