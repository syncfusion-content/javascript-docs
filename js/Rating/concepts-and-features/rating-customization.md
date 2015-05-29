---
layout: post
title: rating-customization
description: rating customization
platform: js
control: Rating
documentation: ug
---

# Rating Customization

## Setting Value

The **Value** property sets the display value of the **Rating**. For example, when the **Value** property is set to be **four**, the **Rating** control renders **four** ratings. By default, **Value** property’s value is **one**.

The following code example is used to render the **Rating** control with customized value.

* Add the following **HTML** to render **Rating** with customized value.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with customized value.</b>    &lt;script type="text/javascript"&gt;        $("#rating").ejRating({ value: 4 });    &lt;/script&gt;</td></tr>
</table>




**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with customized value.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").Value(4)

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



**[ASPX]**

**// You can add the following code example to the corresponding ASPX page to render Rating with customized value.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                <td valign="top">Rating:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating" Value="4" runat="server"&gt;&lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



**[ASPX]**

**// You can add the following code example to the corresponding ASPX page to render Rating with angular support.**

&lt;!doctype html&gt;

&lt;html lang="en" ng-app="syncApp"&gt;

&lt;head&gt;

    &lt;meta charset="utf-8"&gt;

    <title>Essential Studio for JavaScript : AutoComplete - Angular support</title>

    &lt;meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" /&gt;

    &lt;link href="../themes/bootstrap.min.css" rel="stylesheet" /&gt;   

&lt;link href=" http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;

    &lt;link href="../themes/default.css" rel="stylesheet" /&gt;   

    &lt;script src="../scripts/jquery-1.10.2.min.js"&gt;&lt;/script&gt;

    &lt;script src="../scripts/jquery.easing-1.3.min.js"&gt;&lt;/script&gt;

    &lt;script src="../scripts/angular.min.js"&gt;&lt;/script&gt;

    &lt;script src="../scripts/jquery.globalize.min.js"&gt;&lt;/script&gt;

    &lt;script src=" /ej.web.all.js"&gt;&lt;/script&gt;

    &lt;script src="../scripts/ej.unobtrusive.min.js"&gt;&lt;/script&gt;    

    &lt;script src="../scripts/ej.widget.angular.min.js"&gt;&lt;/script&gt;

&lt;/head&gt;

&lt;body&gt;    

&lt;div class="content-container-fluid"&gt;

    &lt;div class="row"&gt;

        &lt;div class="cols-sample-area"&gt;

            &lt;div class="frame" style="width: 50%"&gt;

                &lt;div style="width: 90%; margin: auto"&gt;

                    &lt;div id="control" style="float: left; width: 45%"&gt;

                        &lt;input id="Text1" type="text" class="rating" ej-rating e-value="ratingValue"&gt;

                        &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 10px;">Note:Two Way Angular Support</span>&lt;/h6&gt;

                    &lt;/div&gt;

                    &lt;div id="binding" style="float: right; width: 45%"&gt;

                        &lt;input type="text" class="input ejinputtext" name="rating" value="" ng-model="ratingValue" /&gt;

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;

&lt;script type="text/javascript"&gt;

    angular.module('syncApp', ['ejangular'])

        .controller('RatingCtrl', function ($scope) {

            $scope.ratingValue = 3;

        });

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



The following screenshot illustrates the **Rating** with custom defined value.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img1.png" Caption="Figure 157: Rating with Value"%}

### Min Value

**EJ Rating** control provides support for setting **minimum****value**. This is achieved by adding **minValue** property. When the **minValue** property is set, the **Rating** value starts with **minValue**+1.

The following code example is used to render the **Rating** control with **minimum****rating**.

* Add the following **HTML** to render **Rating** with **minimum****value**.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with minimum value.</b>&lt;script type="text/javascript"&gt;        $("#rating").ejRating({ minValue: 3});    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with customized minimum value.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").MinValue(3)

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



**[ASPX]**

**// You can add the following code example to the corresponding ASPX page to render Rating with customized minimum value.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                <td valign="top">Rating:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating" MinValue="3" runat="server"&gt;&lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



The following screenshot illustrates **Rating** with **minimum****value**.

****

{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img2.png" Caption="Figure 168: Rating with minimum value"%}

### Max Value

**EJ****Rating** control****provides support for setting **maximum****value**. This is achieved by adding the **maxValue** property**.** By default, **maxValue** is **five**.

The following code example is used to render the **Rating** control with **maximum****rating**.

* Add the following **HTML** to render **Rating** with **maximum****value**.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with maximum value.</b>&lt;script type="text/javascript"&gt;       $("#rating").ejRating({ maxValue: 10 });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with customized maximum value.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").MaxValue(10)

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



**[ASPX]**

**// You can add the following code example to the corresponding ASPX page to render Rating with customized maximum value**



    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                <td valign="top">Rating:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="Rating" MaxValue="10" runat="server"&gt;&lt;/ej:Rating&gt;

                &lt;/td&gt;

            &lt;/tr&gt;

        &lt;/table&gt;

    &lt;/div&gt;



The following screenshot illustrates the **Rating** with **maximum****value**.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img3.png" Caption="Figure 179: Rating with maximum value"%}

## Set Precision

In a real-time movie **Rating** scenario, you can set **Precision** between two whole numbers such as 2.5 or 3.7 and it is done using the property **Precision** by changing the value to **ej.Rating.Precision.Half** or **ej.Rating.Precision.Exact.** By default, **Precision** is **Full.**

The following code example is used to render the **Rating** control with **Precision**.

* Add the following **HTML** to render **Rating** with **Precision**.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Full Precision:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                                   &lt;/td&gt;            &lt;/tr&gt;               &lt;tr&gt;                <td valign="top">Half Precision:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="halfRating" type="text" /&gt;                                   &lt;/td&gt;            &lt;/tr&gt;              &lt;tr&gt;                <td valign="top">Exact Precision:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="exactRating" type="text" /&gt;                                   &lt;/td&gt;            &lt;/tr&gt;                 &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with Precision.</b>&lt;script type="text/javascript"&gt;                $("#rating").ejRating({ value: 4 });        $("#halfRating").ejRating({ precision: ej.Rating.Precision.Half, value: 3.5 });        $("#exactRating").ejRating({ precision: ej.Rating.Precision.Exact, value: 3.7 });    &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with Precison.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("FullRating").Precision(Precision.Full).Value(4)

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("HalfRating").Precision(Precision.Half).Value(3.5)

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("ExactRating").Precision(Precision.Exact).Value(4.7)

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



**[ASPX]**

**// Add the following code example to the corresponding ASPX page to render Rating with precision.**



&lt;div id="Div1" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

        &lt;table&gt;

            &lt;tr&gt;

                <td valign="top">Full Precision:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="FullRating" Precision="Full" Value="4" runat="server"&gt;&lt;/ej:Rating&gt;



                &lt;/td&gt;

            &lt;/tr&gt;   

            &lt;tr&gt;

                <td valign="top">Half Precision:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="HalfRating" Precision="Half" Value="3.5" runat="server"&gt;&lt;/ej:Rating&gt;



                &lt;/td&gt;

            &lt;/tr&gt;  

            &lt;tr&gt;

                <td valign="top">Exact Precision:

                &lt;/td&gt;

                &lt;td&gt;

                    &lt;ej:Rating ID="ExactRating" Precision="Exact" Value="4.7" runat="server"&gt;&lt;/ej:Rating&gt;



                &lt;/td&gt;

            &lt;/tr&gt;         

        &lt;/table&gt;

    &lt;/div&gt;



The following screenshot illustrates the **Rating** with **Precision**.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img4.png" Caption="Figure 1810: Rating with Precision"%}

## Increment Step

**EJ Rating** control supports customized **increment** value for **Rating**. This is achieved by adding the **incrementStep** property.

The following code example is used to render the **Rating** control with customized **increment**.

* Add the following **HTML** to render **Rating** with customized **increment**.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with customized increment.</b>&lt;script type="text/javascript"&gt;       $("#rating").ejRating({ incrementStep: 2, maxValue: 10});   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with customized increment.**



    &lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").IncrementStep(2).MaxValue(10)

            &lt;/td&gt;

        &lt;/tr&gt;      

    &lt;/table&gt;

&lt;/div&gt;



**[ASPX]**

**// Add the following code example to the corresponding ASPX page to render Rating with customized increment**

&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                &lt;ej:Rating ID="Rating" IncrementStep="2" MaxValue="10" runat="server"&gt;&lt;/ej:Rating&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



The following screenshot illustrates the **Rating** with customized increment.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img5.png" Caption="Figure 1911: Rating with customized increment"%}

## Resetting values

**EJ Rating** control provides support for value **reset** at runtime. This is achieved by enabling the **allowReset** property to be **‘True’.** By default, the property value is set to **‘True’.**

The following code example is used to render the **Rating** control with **allowReset**.

* Add the following **HTML** to render **Rating** with **allowReset**.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;        &lt;table&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                    &lt;input id="rating" type="text" /&gt;                                   &lt;/td&gt;            &lt;/tr&gt;            &lt;tr&gt;                <td valign="top">Rating:                &lt;/td&gt;                &lt;td&gt;                     &lt;input id="rest" type="text" /&gt;                                    &lt;/td&gt;            &lt;/tr&gt;        &lt;/table&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b><b>// Add the following script to render Rating with allowReset.</b>&lt;script type="text/javascript"&gt;       $("#rating").ejRating({ allowReset: true });        $("#rest").ejRating({ allowReset: false });   &lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with allowReset.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("ResetRating").AllowReset(true)

            &lt;/td&gt;

        &lt;/tr&gt;  

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").AllowReset(false)

            &lt;/td&gt;

        &lt;/tr&gt;    

    &lt;/table&gt;

&lt;/div&gt; 



**[ASPX]**

**// Add the following code example to the corresponding ASPX page to render Rating with allow reset.**



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                &lt;ej:Rating ID="Ratingreset" AllowReset="true" runat="server"&gt;&lt;/ej:Rating&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                &lt;ej:Rating ID="Rating" AllowReset="false" runat="server"&gt;&lt;/ej:Rating&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



The following screenshot illustrates the **Rating** with **allowReset**.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img6.png" Caption="Figure 2012: Rating with allowReset"%}

## Read only

**Rating** control provides support for changeable or unchangeable values for **Rating** control. This is achieved by the **readOnly** property. When this property is set to **‘True’** the **Rating** value becomes unchangeable. By default, this property value is set to **‘False’.**

The following code example is used to render the **Rating** control with **readOnly**.

* Add the following **HTML** to render **Rating** with **readOnly**.



{% highlight html %}

**[HTML]**
<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

**[JS]**
**// Add the following script to render Rating with readOnly .**

<script type="text/javascript">
     $("#rating").ejRating({ readOnly: true });
   </script>


{% endhighlight %}



[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Rating with readOnly.



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").ReadOnly(true)

            &lt;/td&gt;

        &lt;/tr&gt;  



    &lt;/table&gt;

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Rating with read only.



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                &lt;ej:Rating ID="Rating1" ReadOnly="true" runat="server"&gt;&lt;/ej:Rating&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



The following screenshot illustrates the **Rating** with **readOnly.**



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img7.png" Caption="Figure 2113: Rating with readOnly"%}

## Enable or Disable

**Rating** control provides support to **enable** or **disable** the control. This is achieved by the **enabled** property. By default the property value is **‘True’.**

The following code example is used to render the **Rating** control with **enable** or **disable** support.

* Add the following **HTML** to render **Rating** with **enable** or **disable** support.



{% highlight html %}

**[HTML]**
<div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Rating:
                </td>
                <td>
                    <input id="rating" type="text" />
                </td>
            </tr>
        </table>
    </div>

**[JS]**
**// Add the following script to render Rating in disabled form.**

<script type="text/javascript">
     $("#rating").ejRating({ enabled: false });
   </script>


{% endhighlight %}





[CSHTML]

// Add the following code example to the corresponding CSHTML page to render Rating with Enable/Disable support.

.

&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                @Html.EJ().Rating("Rating").Enabled(false)

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



[ASPX]

// Add the following code example to the corresponding ASPX page to render Rating with Enable/Disable support.



&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:

            &lt;/td&gt;

            &lt;td&gt;

                &lt;ej:Rating ID="Rating1" ReadOnly="true" runat="server"&gt;&lt;/ej:Rating&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;



The following screenshot illustrates the **Rating** in **disabled** form.



{% include image.html url="\js\Rating\concepts-and-features\rating-customization_images\rating-customization_img8.png" Caption="Figure 2214: Rating in disabled form"%}

