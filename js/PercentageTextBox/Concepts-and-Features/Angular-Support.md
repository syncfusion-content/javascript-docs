---
layout: post
title: Angular-Support
description: angular support
platform: js
control: PercentageTextBox 
documentation: ug
---

# Angular Support

The **PercentageTextBox** widget supports two types of **Angular JS support** namely, 

* One-way binding

* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **PercentageTextBox** widget, but the changes made in **PercentageTextBox** widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **PercentageTextBox** widget.

**Two-way binding** supports both the processes; it applies the scope values to the **PercentageTextBox** properties as well as the changes made in the **PercentageTextBox** widget also get reflected back and triggered within the angular scope change function.

Apply the plugin and property assigning to the **PercentageTextBox** widget element through the directive that starts with the letter **“e-“.**

To know more details about the **Angular binding**, refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

The following example depicts the way to bind data to the **PercentageTextBox** widget through **angular support**.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="TextCtrl">
<head>
    <title></title>
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"></script>
</head>
<body ng-controller="TextboxCtrl">
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" ej-percentagetextbox e-value="pvalue" />
                    </td>
                    <td>
                        <input type="text" class="e-input" style="border:1px solid #bdbcbd" ng-model="pvalue" />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        angular.module('TextCtrl', ['ejangular'])
           .controller('TextboxCtrl', function ($scope) {
               $scope.pvalue = 400;
           });
    </script>
</body>
</html>


{% endhighlight %}



The output of **PercentageTextBox** controls with **two-way angular binding** is as follows.

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Angular-Support_images/Angular-Support_img1.png" Caption="Figure 28: PercentageTextBox at initial load"%}

{% include image.html url="/js/PercentageTextBox/Concepts-and-Features/Angular-Support_images/Angular-Support_img2.png" Caption="Figure 29: PercentageTextBox with Angular Binding"%}

