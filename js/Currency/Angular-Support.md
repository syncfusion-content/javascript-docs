---
layout: post
title: Angular-Support
description: angular support
platform: js
control: CurrencyTextBox  
documentation: ug
api: /api/js/
---

# AngularJS Support

The **Textbox** widget supports two types of **Angular JS support** namely, 

* One-way binding
* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the CurrencyTextBox widget, but the changes made in CurrencyTextBox widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the CurrencyTextBox widget.

**Two-way binding** supports both the processes; it applies the scope values to the **CurrencyTextBox** properties as well as the changes made in the CurrencyTextBox widget also get reflected back and triggered within the AngularJS scope change function.

Apply the plugin and property assigning to the CurrencyTextBox widget element through the directive that starts with the letter **“e-“.**

To know more details about the **Angular binding**, refer the following link location,

<https://help.syncfusion.com/js/angularjs>

The following example depicts the way to bind data to the **CurrencyTextBox** widget through **angular support**.

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
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" ej-currencytextbox e-value="currencyValue" />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" ng-model="currencyValue" />
                    </td>
                </tr>

            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        angular.module('TextCtrl', ['ejangular'])
           .controller('TextboxCtrl', function ($scope) {
               $scope.currencyValue = 400;
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



The output of **CurrencyTextBox** controls with **two-way AngularJS binding** is as follows.

![](/js/Currency/Angular-Support_images/Angular-Support_img1.png)

CurrencyTextBox at initial load
{:.caption}

![](/js/Currency/Angular-Support_images/Angular-Support_img2.png)

CurrencyTextBox with AngularJS Binding
{:.caption}

