---
layout: post
title: Knockout-Support
description: knockout support
platform: js
control: NumericTextbox
documentation: ug
api: /api/js/
---

# Knockout Support

**Knockout support** allows you to bind the **HTML** elements against any of the available data models. It is of two types**.**

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **NumericTextBox** widget, but the changes made in **NumericTextBox** widget are not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **NumericTextBox** widget.

**Two-way binding** supports both the processes; it applies the observable values to the **NumericTextBox** widget properties as well as the changes made in the **NumericTextBox** widget are also reflected back and triggered within the observable collections. 

For more information about the **knockout binding**, refer the following online documentation in the given link location,

<https://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **NumericTextBox** widgets through **knockout** **support** that enables and populates data to the **NumericTextBox** widget based on the value set to the other **NumericTextBox** widget.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>

</head>
<body>
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="numeric">Numeric</label>
                    </td>
                    <td>
                        <input id="numeric" type="text" data-bind="ejNumericTextbox: { value: numericValue }" />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" data-bind="value: numericValue" />
                    </td>
                </tr>              
            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        window.viewModel = {
            numericValue: ko.observable(100)
        }
        jQuery(function ($) {
            ko.applyBindings(viewModel);          
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

The output of Knockout binding in NumericTextBox .

![](/js/NumericTextBox/Knockout-Support_images/Knockout-Support_img1.png)

NumericTextBox at initial load
{:.caption}

![](/js/NumericTextBox/Knockout-Support_images/Knockout-Support_img2.png)

NumericTextBox with KnockoutJS binding
{:.caption}