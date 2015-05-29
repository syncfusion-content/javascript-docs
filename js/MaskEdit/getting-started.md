---
layout: post
title: getting-started
description: getting started
platform: js
control: MaskEdit
documentation: ug
---

# Getting Started

This section explains you briefly on how to create a **MaskEdit** control in your **JavaScript****ASP.NET MVC** application.



## Create your first MaskEdit Widget in MVCJavaScript

**Essential JavaScript****MaskEdit ASP.NET MVC MaskEdit** control allows you to set the type and format of the input mask that is used in the textbox and also the number of place holders. Using the following guidelines, you can create **MaskEdit** control for a real-time payment application.

The following screenshot illustrates the functionality of a **MaskEdit**. Using **MaskEdit** control textbox, you can enter only the assigned text format and no other formats. The input mask prevents you from entering invalid characters into the control. In this application, **Mobile****Number** textbox has a mask value.



{% include image.html url="\js\MaskEdit\getting-started_images\getting-started_img1.png" Caption="Figure 1: MaskEdit"%}

In the above screenshot, you can type only numbers and it does not allow text format.

### Create a MaskEdit control

**Essential JavaScript MaskEdit** widget provides you built-in features such as character masking, number masking and both together. You can easily create the **MaskEdit** widget by using simple input textbox element as follows:

* Create an **HTML** file and add the following template to the **HTML** file.



{% highlight html %}


<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />

    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js">
    </script>
    <!--Add custom scripts here -->
</head>
<body>
    <!-- add mask edit element here-->
</body>
</html>


{% endhighlight %}



* Add input element to create a **Textbox**.



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
        <div class="paybill">
            <button class="e-btn" id="pbill">Pay Bill</button>
        </div>
    </div>
</div>


{% endhighlight %}



* Add the following style code to format the textbox.



{% highlight css %}


<style type="text/css" class="cssStyles">
    .frame {
        width: 300px;
    }
    .editors {
        max-width: 400px;
    }
    .control .paybill {
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



* Initialize **textbox** in the **&lt;script&gt;** tag.



{% highlight js %}


<script type="text/javascript">
    $(function () {
**$("#maskedit").ejMaskEdit(**
                                **{**
                                    **name: "mask",**
                                    **inputMode: ej.InputMode.Text,**
                                    **//mask value for mobile no**
                                    **maskFormat: "99-999-99999"**
                                **});**
        $("#numeric").ejNumericTextbox(
                                {
                                    name: "numeric",
                                    value: 35
                                });
        $("#percent").ejPercentageTextbox(
                                {
                                    name: "percentage",
                                    value: 3
                                });
        $("#currency").ejCurrencyTextbox(
                                {
                                    name: "currency",
                                    value: 555
                                });
        $("#pbill").ejButton({
            width: "80px",
            height: "25px",
        });
    });
</script>



{% endhighlight %}


The following screenshot shows the output for the above code example.

**ASP.NET MVC MaskEdit** control renders built-in features like text masking, number masking and flexible APIs. You can easily create the **MaskEdit** control using simple **HTML** helper class as follows:

1. Create an **MVC** Project and add necessary assemblies, styles and scripts to it. Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).

2. Add the following code to the corresponding view page to render **MaskEdit**.





&lt;div class="frame"&gt;

        &lt;div class="control"&gt;

            &lt;table class="editors"&gt;

                &lt;tbody&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            &lt;label&gt;

                                Kilometers</label>

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().NumericTextbox("numeric").Value("1000")

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            &lt;label&gt;

                                Service Tax</label>

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().PercentageTextbox("percent").Value("100")

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            &lt;label&gt;

                                Fare</label>

                        &lt;/td&gt;

                        &lt;td&gt;

                            @Html.EJ().CurrencyTextbox("currency").Value("50")

                        &lt;/td&gt;

                    &lt;/tr&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            &lt;label&gt;

                                Mobile No</label>

                        &lt;/td&gt;

                        &lt;td&gt;

 @*creating MaskEdit control*@                           @Html.EJ().MaskEdit("maskedit").MaskFormat("99-999-99999").InputMode(InputMode.Text) 

                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/tbody&gt;

            &lt;/table&gt;

            &lt;div class="paybill"&gt;

                @Html.EJ().Button("btn").Size(ButtonSize.Small).Text("PayBill")

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



3.  Add the following styles to show **MaskEdit** and place it in a particular position.





    &lt;style&gt;

        .frame {

            width: 300px;

        }



        .editors {

            max-width: 400px;

        }



        .control .paybill {

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



        .ctrllabel {

            padding-bottom: 3px;

        }

    &lt;/style&gt;



Execute the above code example to render the following output.



{% include image.html url="\js\MaskEdit\getting-started_images\getting-started_img2.png" Caption="Figure 2: MaskEdit"%}{% include image.html url="\js\MaskEdit\getting-started_images\getting-started_img3.png" Caption="Figure 2: MaskEdit"%}

**Set Mask value to Mobile Number textbox**

In this section, you can learn how to set mask value for **Mobile****Number** textbox. To achieve this, set the mask value in the **MaskEdit** control to the desired values.


@Html.EJ().MaskEdit("maskedit").MaskFormat("99-999-99999").InputMode(InputMode.Text)

**Create a MaskEdit control for Product Key Validation**

**Create a MaskEdit**

You can easily create the **MaskEdit** control using simple **HTML** helper class as follows.

1. Create a **MVC** Project and add necessary assemblies and scripts to it. 

Refer [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm).

2. Add the following code to the corresponding view page to render **MaskEdit.**



  &lt;div class="frame"&gt;

        &lt;div class="control"&gt;

            &lt;table class="editors"&gt;

                &lt;tbody&gt;

                    &lt;tr&gt;

                        &lt;td&gt;

                            &lt;label&gt;

                                Product Key</label>

                        &lt;/td&gt;

                        &lt;td&gt;

                         @Html.EJ().MaskEdit("maskedit").MaskFormat("aaaa-aaaa-aaaa-aaaa").InputMode(InputMode.Text) @*creating MaskEdit control for productkey validation*@                        &lt;/td&gt;

                    &lt;/tr&gt;

                &lt;/tbody&gt;

            &lt;/table&gt;

            &lt;div class="productkey"&gt;

                @Html.EJ().Button("btn").Size(ButtonSize.Small).Text("Submit")

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;



3. Add the following styles to show the **MaskEdit**, and place it in a particular position.





    &lt;style&gt;

        .frame {

            width: 300px;

        }



        .editors {

            max-width: 400px;

        }



        .control .productkey {

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



        .ctrllabel {

            padding-bottom: 3px;

        }

    &lt;/style&gt;

###  Create Product Key Validation App using MaskEdit Widget

In real-time, when you install Microsoft applications, you to enter the product key for security. The value of product key format is predefined and that is done using **MaskEdit** control. 

* Add the following code example in **&lt;body&gt;** tag.



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
        <div class="paybill">
            <button class="e-btn" id="pbill">submit</button>
        </div>
    </div>
</div>



{% endhighlight %}



* The **&lt;script&gt;** tag defines the mask value for product key.



{% highlight js %}


<script type="text/javascript">
    $(function () {
        $("#maskedit").ejMaskEdit(
        {
            name: "mask",
            inputMode: ej.InputMode.Text,
            //mask value for product key validation
            maskFormat: "aaaa-aaaa-aaaa-aaaa"
        });
        $("#pbill").ejButton({
            width: "80px",
            height: "25px",
        });
    });
</script>



{% endhighlight %}



* Add the following style code to format the textbox.



{% highlight css %}


<style type="text/css" class="cssStyles">
    .frame {
        width: 300px;
    }
    .editors {
        max-width: 400px;
    }
    .control .paybill {
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

Run the above code example to render the following output. 

{% include image.html url="\js\MaskEdit\getting-started_images\getting-started_img4.png" Caption="Figure 3: Product Key"%}{% include image.html url="\js\MaskEdit\getting-started_images\getting-started_img5.png" Caption="Figure 3: Product Key"%}

**Set Mask value to Product key textbox**

You can set mask value for **Product****key** textbox by setting the desired values to the **MaskEdit** control.


@Html.EJ().MaskEdit("maskedit").MaskFormat("aaaa-aaaa-aaaa-aaaa").InputMode(InputMode.Text)





