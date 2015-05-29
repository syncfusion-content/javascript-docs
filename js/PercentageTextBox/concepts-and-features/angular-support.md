---
layout: post
title: angular-support
description: angular support
platform: js
control: PercentageTextBoxEditors 
documentation: ug
---

# Angular Support

The **PercentageTextBox Textbox** widget supports two types of **Angular JS support** namely, 

* One-way binding

* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **PercentageTextBox Textbox** widget, but the changes made in **PercentageTextBox Textbox** widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **PercentageTextBox Textbox** widget.

**Two-way binding** supports both the processes; it applies the scope values to the **PercentageTextBox Textbox** properties as well as the changes made in the **PercentageTextBox Textbox** widget also get reflected back and triggered within the angular scope change function.

Apply the plugin and property assigning to the **PercentageTextBox Textbox** widget element through the directive that starts with the letter **“e-“.**

To know more details about the **Angular binding**, refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

The following example depicts the way to bind data to the **PercentageTextBox Textbox** widget through **angular support**.

{% highlight html %}

**[HTML]**
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
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" **ng-app="TextCtrl"**>
<head>
    <title></title>
    <link href="Content/bootstrap.min.css" rel="stylesheet" />
    <link href=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" />
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js](http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/angular.min.js](http://cdn.syncfusion.com/js/assets/external/angular.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js](http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js)"></script>
    <script src=" http://cdn.syncfusion.com/js/web/ej.unobtrusive-latest.min.js "></script>
    <script src=" http://cdn.syncfusion.com/js/web/ej.widget.angular-latest.min.js"></script>
</head>
<body **ng-controller="TextboxCtrl"**>
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="numeric">Numeric</label>
                    </td>
                    <td>
                        <input id="numeric" type="text" **ej-numerictextbox e-value="nvalue"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **ng-model="nvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" **ej-percentagetextbox e-value="pvalue"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **ng-model="pvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" **ej-currencytextbox e-value="cvalue"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **ng-model="cvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="maskedit">Mask Edit</label>
                    </td>
                    <td>
                        <input id="maskedit" type="text" **ej-maskedit e-value="mvalue" e-inputmode="ej.InputMode.Text" e-maskformat='99-999'** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **ng-model="mvalue"** />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        **angular.module('TextCtrl', ['ejangular'])**
           **.controller('TextboxCtrl', function ($scope) {**
               **$scope.nvalue = 600;**
               **$scope.pvalue = 400;**
               **$scope.cvalue = 400;**
               **$scope.mvalue = "";**
           **});**
    </script>
</body>
</html> 


{% endhighlight %}



The output of **PercentageTextBox Textbox** controls with **two-way angular binding** is as follows.

{% include image.html url="\js\PercentageTextBox\concepts-and-features\angular-support_images\angular-support_img1.png" Caption="Figure 4428: PercentageTextBox Textboxes at initial load"%}{% include image.html url="\js\PercentageTextBox\concepts-and-features\angular-support_images\angular-support_img2.png" Caption="Figure 4428: PercentageTextBox Textboxes at initial load"%}

{% include image.html url="\js\PercentageTextBox\concepts-and-features\angular-support_images\angular-support_img3.png" Caption="Figure 2945: PercentageTextBox Textboxes with Angular Binding"%}{% include image.html url="\js\PercentageTextBox\concepts-and-features\angular-support_images\angular-support_img4.png" Caption="Figure 2945: PercentageTextBox Textboxes with Angular Binding"%}

