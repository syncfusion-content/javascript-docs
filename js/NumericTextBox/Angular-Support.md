---
layout: post
title: Angular-Support
description: angular support
platform: js
control: NumericTextbox
documentation: ug
api: /api/js/
---

# AngularJS Support

The **NumericTextBox** widget supports two types of **AngularJS support** namely, 

* One-way binding
* Two-way binding 



**One-way binding** refers to the process of applying scope values to all the available properties of the **NumericTextBox** widget, but the changes made in **NumericTextBox** widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **NumericTextBox** widget.

**Two-way binding** supports both the processes; it applies the scope values to the **NumericTextBox** properties as well as the changes made in the **NumericTextBox** widget also get reflected back and triggered within the AngularJS scope change function.

Apply the plugin and property assigning to the **NumericTextBox** widget element through the directive that starts with the letter **“e-“.**

To know more details about the **AngularJS binding**, refer the following link location,

<https://help.syncfusion.com/js/angularjs>

The following example depicts the way to bind data to the **NumericTextBox** widget through **angularJS support**.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="TextCtrl">
<head>
    <title></title>
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="TextboxCtrl">
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="numeric">Numeric</label>
                    </td>
                    <td>
                        <input id="numeric" type="text" ej-numerictextbox e-value="numericValue" />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" ng-model="numericValue" />
                    </td>
                </tr>

            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        angular.module('TextCtrl', ['ejangular'])
           .controller('TextboxCtrl', function ($scope) {
               $scope.numericValue = 600;
           });
    </script>
    <style>
        .input {
            height: 27px;
            text-indent: 10px;
            width: 81%;
        }
    </style>
</body>
</html>

{% endhighlight %}

The output of **NumericTextBox** controls with **two-way AngularJS binding** is as follows.

![](/js/NumericTextBox/Angular-Support_images/Angular-Support_img1.png)

NumericTextBox at initial load
{:.caption}

![](/js/NumericTextBox/Angular-Support_images/Angular-Support_img2.png)

NumericTextBox with AngularJS Binding
{:.caption}