---
layout: post
title: Getting-Started
description: getting started
platform: js
control: NumericTextbox
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **NumericTextBox** control in your application with **JavaScript**. From the following steps you can learn how to create and use **NumericTextBox** in your application.You will learn how to use our JavaScript textboxes widgets in the Electric bill calculator Application from the following documentation. This will guide you to use the wide range functionalities of textbox widgets features to complete this application. 

![](/js/NumericTextBox/Getting-Started_images/Getting-Started_img1.png) 

## Create Textboxes Widgets

Create an **HTML** file and add the following template to the HTML file for Textbox widget creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
</head>
<body>
    <!--adds Textboxes elements here -->
</body>
</html>



{% endhighlight %}

Add necessary input elements to render **Textboxes widget**.



{% highlight html %}


<div class="ele-icon"></div>
<div class="ele-txt" style="">Electricity Bill Calculator</div>
<br />
<table class="editors">
    <tbody>
        <tr>
            <td>
                <label>Unit meters</label>
            </td>
            <td>
                <input id="unitmcalc" type="text" />
            </td>
        </tr>
        <tr>
            <td>
                <label>Service Tax</label>
            </td>
            <td>
                <input id="servTax" type="text" />
            </td>
        </tr>
        <tr>
            <td>
                <label>Fare</label>
            </td>
            <td>
                <input id="amountperum" type="text" />
            </td>
        </tr>
        <tr>
            <td>
                <label>Mobile No</label>
            </td>
            <td>
                <input id="mobiNo" type="text" />
            </td>
        </tr>
    </tbody>
</table>
<div class="paybill">
    <button class="e-btn" id="cbill">Calculate</button>
</div>


{% endhighlight %}



Initialize the **Textboxes widget** as shown in the following section.

{% highlight javascript %}


        // Declares Necessary variable creation 
        var kmcalc, servtax, amuntperkm;
        $(function () {
            // document ready
            // simple Numeric creation
            $("#unitmcalc").ejNumericTextbox({
                watermarkText: "Units" // set watermark in numeric
            });
            // simple Percentage creation
            $("#servTax").ejPercentageTextbox({
                watermarkText: "Service Tax" // sets watermark in percentage
            });
            // simple Currency creation
            $("#amountperum").ejCurrencyTextbox({
                watermarkText: "Amount per unit" // sets watermark in currency                       
            });
            // simple MaskEdit creation
            $("#mobiNo").ejMaskEdit({
                watermarkText: "Mobile No" // sets watermark in mask edit
            });

            // simple Button creation
            $("#cbill").ejButton({
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
        });


{% endhighlight %}



You can add the following **URL** path for the background image and to apply styling. [http://js.syncfusion.com/UG/Web/Content/electricity.png](http://js.syncfusion.com/UG/Web/Content/electricity.png)



{% highlight css %}


<style type="text/css" class="cssStyles">

         .ele-icon
        {
            display: inline-block;
            background-image:url(http://js.syncfusion.com/UG/Web/Content/electricity.png);
            background-repeat: no-repeat;
            background-size: contain;
            height: 50px;
            width: 50px;
        }
        .ele-txt
        {
            display: inline-block;
            font-size: 20px;
            font-weight: bolder;
            height: 50px;
            position: relative;
            text-align: center;
            top: -20px;
        }
        .editors
        {
            max-width: 400px;
        }
        .paybill
        {
            margin-left: 208px;
            margin-top: 15px;
        }
        .editors label
        {
            display: block;
            width: 130px;
        }

</style>



{% endhighlight %}



The following screenshot displays the output when the above code is executed. 

![](/js/NumericTextBox/Getting-Started_images/Getting-Started_img2.png) 


## Set the MinValue, MaxValue and value in NumericTextBox

You can set the **“minValue”**,**“maxValue”** and **“value”** in Numeric, Percentage and Currency text boxes for maintaining the range in Textboxes widgets. In this scenario, you have to enter the values between the given ranges. The following code example illustrates how to achieve this.

{% highlight javascript %}


        // Declares the Necessary variable creation 
        var kmcalc, servtax, amuntperkm;
        $(function () {
            // document ready
            // simple Numeric creation
            $("#unitmcalc").ejNumericTextbox({
                watermarkText: "Units", // sets watermark in numeric
                value: 35, // sets value 
                minValue: 1, // sets min value 
                maxValue: 10000 // sets max value
            });
            // simple Percentage creation
            $("#servTax").ejPercentageTextbox({
                watermarkText: " Service Tax", // sets watermark in percentage
                value: 3,// sets value  
                minValue: 5, // sets min value 
                maxValue: 100// sets max value 
            });
            // simple Currency creation
            $("#amountperum").ejCurrencyTextbox({
                watermarkText: " Amount per unit", //sets watermark in currency
                value: 55, // sets value  
                minValue: 5,// sets min value 
                maxValue: 55// sets max value  
            });
            // simple MaskEdit creation
            $("#mobiNo").ejMaskEdit({
                watermarkText: "Mobile No", // sets watermark in mask edit
                maskFormat: "99-999-99999"// sets mask format  
            });
            // simple Button creation
            $("#cbill").ejButton({
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
        });

{% endhighlight %}



The following screenshot illustrates the output of the above code examples.



![](/js/NumericTextBox/Getting-Started_images/Getting-Started_img3.png) 


## Set the Strict Mode Option

You can set the “**strict mode” option** to restrict entering values defined outside the range. The following code example illustrates how to set strict mode option. 

{% highlight javascript %}


        // Declares Necessary variable creation 
        var kmcalc, servtax, amuntperkm;
        $(function () {
            // simple Numeric creation
            $("#unitmcalc").ejNumericTextbox({
                watermarkText: "Units", // sets watermark in numeric
                value: 35, // sets value  
                minValue: 1, // sets min value   
                maxValue: 10000, // sets max value  
                enableStrictMode: true // sets strict mode to True  
            });
            // simple Percentage creation
            $("#servTax").ejPercentageTextbox({
                watermarkText: " Service Tax", // sets watermark in percentage
                value: 3, // sets value   
                minValue: 5, // sets min value  
                maxValue: 100// sets max value  
            });
            // simple Currency creation
            $("#amountperum").ejCurrencyTextbox({
                watermarkText: " Amount per unit", // sets watermark in currency
                value: 55, // sets value  
                minValue: 5, // sets min value  
                maxValue: 55// sets max value  
            });
            // simple MaskEdit creation
            $("#mobiNo").ejMaskEdit({
                watermarkText: "Mobile No", // sets watermark in MaskEdit
                maskFormat: "99-999-99999"// sets the mask format
            });
            // Simple Button creation
            $("#cbill").ejButton({
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
        });


{% endhighlight %}



Run the above code example and you can see that it restricts entering a value exceeding the **minValue** and **maxValue** range mentioned in the numeric textbox. 

## Set Calculation process with NumericTextBox Widget

You can use events to calculate the total and display the value. You can achieve this with the help of “click” event in the button widget. The calculation steps have to be written in the call back function of button’s “click” event.

{% highlight javascript %}

        // Declares Necessary variable to create the Application 
        var kmcalc, servtax, amuntperkm;
        $(function () {
            // Refers to the Textboxes customization section
            // Simple Button creation
            $("#cbill").ejButton({
                click: "calculateBill",
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
            umcalc = $("#unitmcalc").data("ejNumericTextbox");// Object of Numeric 
            servtax = $("#servTax").data("ejPercentageTextbox");// Object of Perentage
            amuntperkm = $("#amountperum").data("ejCurrencyTextbox"); // Object of Currency
            cusmob = $("#mobiNo").data("ejMaskEdit"); // Object of MaskEdit
        });
        // Simple Bill amount calculation.
        function calculateBill() {
            // This is used to calculate the Net amount
            var netamunt = umcalc.model.value * amuntperkm.model.value;
            // This is used to calculate the service tax amount
            var sTax = (netamunt * servtax.model.value) / 100;
            // This shows the calculated amount for the units
            alert("The amount $" + (netamunt + sTax) + " has been sent as message to " + cusmob.model.value + ".");
        }



{% endhighlight %}

Run the above code example, fill the required Textbox fields and click the Calculate button. The values are displayed and an alert message is shown. The following screenshot illustrates the final output of the Electricity bill calculator. 

![](/js/NumericTextBox/Getting-Started_images/Getting-Started_img4.png) 

