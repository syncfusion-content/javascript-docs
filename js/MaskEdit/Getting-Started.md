---
layout: post
title: Getting-Started
description: getting started
platform: js
control: MaskEdit
documentation: ug
api: /api/js/ejmaskedit
---

# Getting Started

This section explains you briefly on how to create a **MaskEdit** control in your **JavaScript** application.

## Create your first MaskEdit Widget in JavaScript

Essential JavaScript **MaskEdit** control allows you to set the type and format of the input mask that is used in the textbox and also the number of place holders. Using the following guidelines, you can create **MaskEdit** control for a real-time payment application.

The following screenshot illustrates the functionality of a **MaskEdit**. Using **MaskEdit** control textbox, you can enter only the assigned text format and no other formats. The input mask prevents you from entering invalid characters into the control. In this application, **Mobile Number** textbox has a mask value.

![](/js/MaskEdit/Getting-Started_images/Getting-Started_img1.png)

In the above screenshot, you can type only numbers and it does not allow text format.

### Create a MaskEdit control

**Essential JavaScript MaskEdit** widget provides you built-in features such as character masking, number masking and both together. You can easily create the **MaskEdit** widget by using simple input textbox element as follows:

Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}


<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js">
    </script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add mask edit element here-->
</body>
</html>


{% endhighlight %}



Add input element to create a **Textbox**.



{% highlight html %}


<div class="frame">
    <div class="control">
        <table class="editors">
            <tbody>
                <tr>
                    <td>
                        <label>
                            Kilometers
                        </label>
                    </td>
                    <td>
                        <input id="numeric" type="text" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label>
                            Service Tax
                        </label>
                    </td>
                    <td>
                        <input id="percent" type="text" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label>
                            Fare
                        </label>
                    </td>
                    <td>
                        <input id="currency" type="text" />
                    </td>
                </tr>
                <tr>
                    <td>
                        <label>
                            Mobile No
                        </label>
                    </td>
                    <td>
                        <input id="maskedit" type="text" />
                    </td>
                </tr>
            </tbody>
        </table>
        <div class="pay-bill">
            <button class="e-btn" id="payBill">Pay Bill</button>
        </div>
    </div>
</div>


{% endhighlight %}



Add the following style code to format the textbox.



{% highlight css %}

<style class="cssStyles">
    .frame {
        width: 300px;
    }

    .editors {
        max-width: 400px;
    }

    .control .pay-bill {
        margin-left: 208px;
        margin-top: 15px;
    }

    .editors label {
        display: block;
        width: 130px;
    }

    .control {
        margin-top: 10px;
    }
</style>


{% endhighlight %}



Initialize **textbox** in the **&lt;script&gt;** tag.



{% highlight javascript %}

        $(function() {
            $("#maskedit").ejMaskEdit({
                name: "mask",
                inputMode: ej.InputMode.Text,
                //mask value for mobile no
                maskFormat: "99-999-99999"
            });
            $("#numeric").ejNumericTextbox({
                name: "numeric",
                value: 35
            });
            $("#percent").ejPercentageTextbox({
                name: "percentage",
                value: 3
            });
            $("#currency").ejCurrencyTextbox({
                name: "currency",
                value: 555
            });
            $("#payBill").ejButton({
                width: "80px",
                height: "25px",
            });
        });



{% endhighlight %}


The following screenshot shows the output for the above code example.



![](/js/MaskEdit/Getting-Started_images/Getting-Started_img2.png)

### Create Product Key Validation App using MaskEdit Widget

In real-time, when you install Microsoft applications, you to enter the product key for security. The value of product key format is predefined and that is done using **MaskEdit** control. 

Add the following code example in **&lt;body&gt;** tag.



{% highlight html %}


<div class="frame">
    <div class="control">
        <table class="editors">
            <tbody>
                <tr>
                    <td>
                        <label>
                            Enter your product key
                        </label>
                    </td>
                    <td>
                        <input id="maskedit" type="text" />
                    </td>
                </tr>
            </tbody>
        </table>
        <div class="pay-bill">
            <button class="e-btn" id="payBill">submit</button>
        </div>
    </div>
</div>



{% endhighlight %}



The **&lt;script&gt;** tag defines the mask value for product key.



{% highlight javascript %}


        $(function() {
            $("#maskedit").ejMaskEdit({
                name: "mask",
                inputMode: ej.InputMode.Text,
                //mask value for product key validation
                maskFormat: "aaaa-aaaa-aaaa-aaaa"
            });
            $("#payBill").ejButton({
                width: "80px",
                height: "25px",
            });
        });



{% endhighlight %}



Add the following style code to format the textbox.



{% highlight css %}


<style type="text/css" class="cssStyles">
    .frame {
        width: 300px;
    }
    .editors {
        max-width: 400px;
    }
    .control .pay-bill {
        margin-left: 200px;
        margin-top: 15px;
    }
    .editors label {
        display: block;
        width: 130px;
    }
    .control {
        margin-top: 10px;
    }
</style>


{% endhighlight %}



The following screenshot shows the output for the above code example.



![](/js/MaskEdit/Getting-Started_images/Getting-Started_img3.png)



