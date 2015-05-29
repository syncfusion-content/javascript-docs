---
layout: post
title: angular-support
description: angular support
platform: js
control: CurrencyTextBox Editors 
documentation: ug
---

# Angular Support

The **Textbox** widget supports two types of **Angular JS support** namely, 

* One-way binding

* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **CurrencyTextBox Textbox** widget, but the changes made in **CurrencyTextBox Textbox** widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **CurrencyTextBox Textbox** widget.

**Two-way binding** supports both the processes; it applies the scope values to the **CurrencyTextBox Textbox** properties as well as the changes made in the **CurrencyTextBox Textbox** widget also get reflected back and triggered within the angular scope change function.

Apply the plugin and property assigning to the **CurrencyTextBox Textbox** widget element through the directive that starts with the letter **“e-“.**

To know more details about the **Angular binding**, refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

The following example depicts the way to bind data to the **CurrencyTextBox Textbox** widget through **angular support**.

{% highlight html %}

**[HTML]**


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="TextCtrl">
<head>
    <title></title>
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
<body ng-controller="TextboxCtrl">
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" ej-currencytextbox e-value="cvalue" />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" ng-model="cvalue" />
                    </td>
                </tr>

            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        angular.module('TextCtrl', ['ejangular'])
           .controller('TextboxCtrl', function ($scope) {
               $scope.cvalue = 400;
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



The output of **CurrencyTextBox Textbox** controls with **two-way angular binding** is as follows.

{% include image.html url="\js\Currency\concepts-and-features\angular-support_images\angular-support_img1.png" Caption="Figure 362844: CurrencyTextBox Textboxes at initial load"%}{% include image.html url="\js\Currency\concepts-and-features\angular-support_images\angular-support_img2.png" Caption="Figure 362844: CurrencyTextBox Textboxes at initial load"%}

{% include image.html url="\js\Currency\concepts-and-features\angular-support_images\angular-support_img3.png" Caption="Figure 372945: CurrencyTextBox Textboxes with Angular Binding"%}{% include image.html url="\js\Currency\concepts-and-features\angular-support_images\angular-support_img4.png" Caption="Figure 372945: CurrencyTextBox Textboxes with Angular Binding"%}

