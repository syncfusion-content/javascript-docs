---
layout: post
title: knockout-support
description: knockout support
platform: js
control: CurrencyTextBox Editors 
documentation: ug
---

# Knockout Support

**Knockout support** allows you to bind the **HTML** elements against any of the available data models. It is of two types**.**

* One-way binding

* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **CurrencyTextBox Textbox** widget, but the changes made in **CurrencyTextBox Textbox** widget are not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **CurrencyTextBox Textbox** widget.

**Two-way binding** supports both the processes; it applies the observable values to the **CurrencyTextBox Textbox** widget properties as well as the changes made in the **CurrencyTextBox Textbox** widget are also reflected back and triggered within the observable collections. 

For more information about the **knockout binding**, refer the following online documentation in the given link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

The following example depicts the way to bind data to the **CurrencyTextBox Textbox** widgets through **knockout****support** that enables and populates data to the **CurrencyTextBox Textbox** widget based on the value set to the other **CurrencyTextBox Textbox** widget.

{% highlight html %}

**[HTML]**
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"></script>

</head>
<body>
    <div id="center">
        <table cellpadding="10">
            <tbody>
                <tr>
                    <td>
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" data-bind="ejCurrencyTextbox: { value: cvalue }" />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" data-bind="value: cvalue" />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
     <script type="text/javascript">  
        window.viewModel = {
            cvalue: ko.observable(80),
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
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title></title>
    <link href="Content/bootstrap.min.css" rel="stylesheet" />
    <link href=" http://cdn.syncfusion.com/js/web/flat-azure/ej.web.all-latest.min.css" rel="stylesheet" />
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js](http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/knockout.min.js](http://cdn.syncfusion.com/js/assets/external/knockout.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js](http://cdn.syncfusion.com/js/web/ej.web.all-latest.min.js)"></script>
    <script src=" http://cdn.syncfusion.com/js/web/ej.unobtrusive-latest.min.js "></script>
    <script src="http://cdn.syncfusion.com/js/web/ej.widget.ko-latest.min.js"></script>
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
                        <input id="numeric" type="text" **data-bind="ejNumericTextbox: { value: nvalue }"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **data-bind="value: nvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="percent">Percent</label>
                    </td>
                    <td>
                        <input id="percent" type="text" **data-bind="ejPercentageTextbox: { value: pvalue }"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **data-bind="value: pvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="currency">Currency</label>
                    </td>
                    <td>
                        <input id="currency" type="text" **data-bind="ejCurrencyTextbox: { value: cvalue }"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **data-bind="value: cvalue"** />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label for="maskedit">Mask Edit</label>
                    </td>
                    <td>
                        <input id="maskedit" type="text" **data-bind="ejMaskEdit: { value: mvalue, inputMode: ej.InputMode.Text, maskFormat: '(999)999-9999' }"** />
                    </td>
                    <td>
                        <input type="text" class="input ejinputtext" **data-bind="value: mvalue"** />
                    </td>
                </tr>
            </tbody>
        </table>
    </div>
    <script type="text/javascript">
        var numobject, percentobject, currencyobject, maskobject;
        window.viewModel = {
**nvalue: ko.observable(100),**
            **cvalue: ko.observable(80),**
            **pvalue: ko.observable(50),**
            **mvalue: ko.observable("")**
        }
        jQuery(function ($) {
**ko.applyBindings(viewModel);**
            numobject = $("#numeric").data("ejNumericTextbox");
            percentobject = $("#percent").data("ejPercentageTextbox");
            currencyobject = $("#currency").data("ejCurrencyTextbox");
            maskobject = $("#maskedit").data("ejMaskEdit");

            $(".input").blur(function () {
                var val = parseInt(this.value);
                if (!isNaN(val)) {
                    numobject.option(this.id, val);
                    percentobject.option(this.id, val);
                    currencyobject.option(this.id, val);
                }
            });
        });
    </script>
</body>
</html>



{% endhighlight %}





The output of **Knockout binding** in **CurrencyTextBox Textbox**.



{% include image.html url="\js\Currency\concepts-and-features\knockout-support_images\knockout-support_img1.png" Caption="Figure 342642: CurrencyTextBox Textboxes at initial load"%}{% include image.html url="\js\Currency\concepts-and-features\knockout-support_images\knockout-support_img2.png" Caption="Figure 342642: CurrencyTextBox Textboxes at initial load"%}



{% include image.html url="\js\Currency\concepts-and-features\knockout-support_images\knockout-support_img3.png" Caption="Figure 433527: CurrencyTextBox Textboxes with knockout binding"%}__{% include image.html url="\js\Currency\concepts-and-features\knockout-support_images\knockout-support_img4.png" Caption="Figure 433527: CurrencyTextBox Textboxes with knockout binding"%}

