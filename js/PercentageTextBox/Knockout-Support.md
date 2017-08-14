---
layout: post
title: Knockout-Support
description: knockout support
platform: js
control: PercentageTextBox 
documentation: ug
api: /api/js/
---

# Knockout Support

**Knockout support** allows you to bind the **HTML** elements against any of the available data models. It is of two types**.**

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **PercentageTextBox** widget, but the changes made in **PercentageTextBox** widget are not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **PercentageTextBox** widget.

**Two-way binding** supports both the processes; it applies the observable values to the **Textbox** widget properties as well as the changes made in the **PercentageTextBox** widget are also reflected back and triggered within the observable collections. 

For more information about the **knockout binding**, refer the following online documentation in the given link location,

<https://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **PercentageTextBox** widgets through **knockoutJS** **support** that enables and populates data to the **PercentageTextBox** widget based on the value set to the other **PercentageTextBox** widget.

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <!-- Style sheet for default theme (flat azure) -->
    <link href=" http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" data-bind="ejPercentageTextbox: { value: percentValue }" />
                    </td>
                    <td>
                        <input type="text" class="e-input" style="border:1px solid #bdbcbd" data-bind="value: percentValue" />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        window.viewModel = {
            percentValue: ko.observable(50),
        }
        jQuery(function ($) {
            ko.applyBindings(viewModel);
        });
    </script>
</body>
</html>

{% endhighlight %}


The output of **Knockout binding** in **PercentageTextBox** .

![](/js/PercentageTextBox/Knockout-Support_images/Knockout-Support_img1.png)

PercentageTextBox at initial load
{:.caption}

![](/js/PercentageTextBox/Knockout-Support_images/Knockout-Support_img2.png)

PercentageTextBox with KnockoutJS binding
{:.caption}