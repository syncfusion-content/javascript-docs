---
layout: post
title: getting-started
description: getting started
platform: js
control: PercentageTextBoxEditors 
documentation: ug
---

# Getting Started

This section explains briefly about how to create a **Editors** control in your application with **JavaScript,****ASP.NET** and **ASP.NET MVC**.

## Create your first PercentageTextBox Editor in JavaScript

From the following steps you can learn how to create and use **PercentageTextBox** in your application. Here we have showcased, a small Electric bill calculator application using **Editors** widgets. The **Essential JavaScript Editors** control includes numeric, percentage and currency textbox controls. You will learn how to use our JS textboxes widgets in the Electric bill calculator Application from the following documentation. This will guide you to use the wide range functionalities of textbox widgets features to complete this application. 

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img1.png" Caption="Figure 1: Electricity Bill Calculator"%}{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img2.png" Caption="Figure 1: Electricity Bill Calculator"%}

### Create Textboxes Widgets

* Create an **HTML** file and add the following template to the html file for Textbox widget creation.

{% highlight html %}

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8"  />
    <!-- style sheet for default theme(flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>

 <!--scripts-->
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js](http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js](http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js)"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"> </script>
</head>
<body>
    <!--adds Textboxes elements here -->
</body>
</html>


{% endhighlight %}

* Add necessary input elements to render **Textbox widget**.



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



* 3. Initialize the **Textboxes widget** as shown in the following section.

{% highlight js %}


<script type="text/javascript">

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
                  watermarkText: "Mobile No" // sets watermark in maskedit
              });

              // simple Button creation
              $("#cbill").ejButton({
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
          });
    </script>


{% endhighlight %}



*  You can add the following location in the **URL** path for the background image and to apply styling. 

[http://js.syncfusion.com/UG/Web/Content/electricity.png](http://js.syncfusion.com/UG/Web/Content/electricity.png)



{% highlight css %}


<style type="text/css" class="cssStyles">

         .ele-icon
        {
            display: inline-block;
background-image:     url([http://js.syncfusion.com/UG/Web/Content/electricity.png](http://js.syncfusion.com/UG/Web/Content/electricity.png));
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
            margin-left: 21080px;
            margin-top: 15px;
        }
        .editors label
        {
            display: block;
            width: 130px;
        }

</style>



{% endhighlight %}



* The following screenshot displays the output when the above code is executed. 

![](getting-started_images\getting-started_img3.png)![](getting-started_images\getting-started_img4.png)

_Figure_ _2__: Textboxes with watermark text_

### Set the MinValue, MaxValue and value in Textboxes

You can set the **“MinValue”,****“MaxValue”** and **“Value”** in Numeric, percentage and Currency text boxes for maintaining the range in Textboxes widgets. In this scenario, you have to enter the values between the default ranges and enter the phone number in the **Maskedit** widget by using the ”**maskFormat**” property. The following code example illustrates how to achieve this.

{% highlight js %}


<script type="text/javascript">
      // Declares the Necessary variable creation 
          var kmcalc, servtax, amuntperkm;
          $(function () {
              // document ready
       // simple Numeric creation
              $("#unitmcalc").ejNumericTextbox({
                watermarkText: "Units", // sets watermark in numeric
**value: 35,** // sets value in the numeric
**minValue: 1,** // sets min value for range 
                **maxValue: 10000** // sets max value for range
            });
              // simple Percentage creation
              $("#servTax").ejPercentageTextbox({
                watermarkText: " Service Tax", // sets watermark in percentage
**value: 3,** // sets value by default 
**minValue: 5,** // sets min value for calculation
**maxValue: 100**// sets max value for calculation
            });
              // simple Currency creation
              $("#amountperum").ejCurrencyTextbox({
                watermarkText: " Amount per unit", //sets watermark in currency
**value: 55,** // sets value by default
**minValue: 5,** // sets min value for amount
**maxValue: 55**// sets max value for amount
            });
              // simple MaskEdit creation
              $("#mobiNo").ejMaskEdit({
                 watermarkText: "Mobile No", // sets watermark in maskedit
**maskFormat: "99-999-99999"**// sets the mask format in maskedit
            });
              // simple Button creation
              $("#cbill").ejButton({
                width: "100px",
                height: "30px",
                contentType: "textandimage",
                prefixIcon: "e-calender"
            });
          });
    </script>


{% endhighlight %}



The following screenshot illustrates the output of the above code examples.



![](getting-started_images\getting-started_img5.png)![](getting-started_images\getting-started_img6.png)

_Figure_ _3__: Textboxes with_ _value_

### Set the Strict Mode Option

You can set the “**enableStrictModeStrict mode” option** to restrict entering values defined outside the range. The following code example illustrates how to set **enableStrictMode** strict mode option. 

{% highlight js %}

**[JS]**

<script type="text/javascript">
   // Declares Necessary variable creation 
          var kmcalc, servtax, amuntperkm;
          $(function () {
       // simple Numeric creation
              $("#unitmcalc").ejNumericTextbox({
                watermarkText: "Units", // sets watermark in numeric
                value: 35, // sets value in the numeric
                minValue: 1, // sets min value for range 
                maxValue: 10000, // sets max value for range
**enableStrictMode:true** // sets strict mode to True will set the value 
            });
              // simple Percentage creation
              $("#servTax").ejPercentageTextbox({
                watermarkText: " Service Tax", // sets watermark in percentage
                value: 3, // sets value by default 
                minValue: 5, // sets min value for calculation
                maxValue: 100// sets max value for calculation
            });
              // simple Currency creation
              $("#amountperum").ejCurrencyTextbox({
                watermarkText: " Amount per unit", // sets watermark in currency
                value: 55, // sets value by default
                minValue: 5, // sets min value for amount
                maxValue: 55// sets max value for amount
            });
              // simple MaskEdit creation
              $("#mobiNo").ejMaskEdit({
                watermarkText: "Mobile No", // sets watermark in Maskedit
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
</script>


{% endhighlight %}



Run the above code example and you can see that it restricts entering a value exceeding the **mMinValue** and **mMaxValue** range mentioned in the numeric textbox. 

### Set Calculation process with Textboxes Widgets

You can use events to calculate the total and display the value. You can achieve this with the help of “click” event in the button widget. The calculation steps have to be written in the call back function of button’s “click” event.

{% highlight js %}

**[JS]**

<script type="text/javascript">
   // Declares Necessary variable creation 
          var kmcalc, servtax, amuntperkm;
          $(function () {
               // Refers to the Textboxes customization section
              // Simple Button creation
              $("#cbill").ejButton({
**click: "calculateBill",**
****width: "100px",
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
</script>



{% endhighlight %}



Run the above code example, fill the required Textbox fields and click the Calculate button. The values are displayed and an alert message is shown. The following screenshot illustrates the final output of the Electricity bill calculator. 

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img7.png" Caption="Figure 4: Electricity bill calculator with alert"%}

## Create your first Editor in MVC

The **Essential ASP.NET MVC Editors** control includes numeric, percentage, currency and maskedit textbox controls. You can learn how to use **MVC textboxes** widgets in the Electricity bill calculator Application from the following documentation. This will guide you to use the wide range of **textbox** functionalities to complete this application. 

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img8.png" Caption="Figure 5: Electricity Bill Calculator"%}

**Create Textboxes Widgets**

**ASP.NET MVC Textbox** widget renders built-in features like keyboard navigation, min and max range and flexible API’s. You can easily create the **Textbox** widget by using simple input textbox element as follows.

1. Create a MVC Project and add necessary Dll’s and Scripts. Refer  [MVC-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm)

2. Add necessary input elements for **Textbox widget** rendering and initialize the corresponding **Textboxes widget**



&lt;div class="editors"&gt;

&lt;div class="ele-icon"&gt;&lt;/div&gt;

<div class="ele-txt" style="">Electricity Bill Calculator</div>

&lt;br /&gt;

&lt;table class="editors"&gt;

     &lt;tbody&gt;

         &lt;tr&gt;

           &lt;td&gt;

              <label>Unit meters</label>

           &lt;/td&gt;

           &lt;td&gt;    @* Numeric text box creation with watermark text *@

              @Html.EJ().**NumericTextbox**("numeric").WatermarkText("Units")

           &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Service Tax</label>

            &lt;/td&gt;

            &lt;td&gt;     @* Percentage text box creation with watermark text *@

                 @Html.EJ().**PercentageTextbox**("percent").WatermarkText("Tax")

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

             &lt;td&gt;

               <label>Fare</label>

            &lt;/td&gt;

            &lt;td&gt;    @* Currency text box creation with watermark text *@

                @Html.EJ().**CurrencyTextbox**("currency").WatermarkText("Amount per unit")

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Mobile No</label>

            &lt;/td&gt;

            &lt;td&gt;    @* Mask Edit text box creation with watermark text *@

               @Html.EJ().**MaskEdit**("maskedit").WatermarkText("Phone number")

            &lt;/td&gt;

       &lt;/tr&gt;

     &lt;/tbody&gt;&lt;/table&gt;

  &lt;div class="paybill"&gt;      @Html.EJ().Button("btn").Size(ButtonSize.Small).Text("Calculate").ContentType(ContentType.TextAndImage).PrefixIcon("e-calender")

  &lt;/div&gt;

&lt;/div&gt;



3. The following styles are added to arrange the **Textboxes**.  You can add the following location in the **URL** path for the background image and to apply styling [http://js.syncfusion.com/UG/Web/Content/electricity.png](http://js.syncfusion.com/UG/Web/Content/electricity.png)





&lt;style type="text/css" class="cssStyles"&gt;

    .ele-icon

    {

        display: inline-block;

        background-image: url(http://js.syncfusion.com/UG/Web/Content/electricity.png);

        background-repeat: no-repeat;

        background-size: contain;

        height: 50px;

        width: 50px;

        margin-left:50px;

        margin-top:15px;

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

        border: 2px solid #DDDDDD;

    }

        .editors table

        {

            border:0px;

            padding-left:50px;

        }

    .paybill

    {

        margin:15px 0px 10px 208px;

    }

    .editors label

    {

        display: block;

        width: 130px;

    }

&lt;/style&gt;





4. Execute the code to render **Textbox widget** as follows



![](getting-started_images\getting-started_img9.png)

_Figure_ _6__:____Textboxes with watermark text_

**Set MinValue, MaxValue and value in Textboxes**

You can set the **“MinValue”,****“MaxValue”** and **“Value”** in Numeric, percentage and Currency text boxes for maintaining the range in Textboxes widgets. In this scenario, you have to enter the values between the default ranges and enter the phone number in the **Maskedit** widget by using the”**maskFormat**” property. By using **DecimalPlaces** property for **CurrencyTextBox** you can get decimal values. The following code example illustrates how to achieve this.

&lt;div class="editors"&gt;

&lt;div class="ele-icon"&gt;&lt;/div&gt;

<div class="ele-txt" style="">Electricity Bill Calculator</div>

&lt;br /&gt;

&lt;table class="editors"&gt;

     &lt;tbody&gt;

         &lt;tr&gt;

           &lt;td&gt;

              <label>Unit meters</label>

           &lt;/td&gt;

           &lt;td&gt;    @Html.EJ().NumericTextbox("numeric").WatermarkText("Units").**MinValue**(1).**MaxValue**(10000).**Value**("70")

           &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Service Tax</label>

            &lt;/td&gt;

            &lt;td&gt;                 @Html.EJ().PercentageTextbox("percent").WatermarkText("Tax").**MinValue**(5).**MaxValue**(100).**Value**("15")

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

             &lt;td&gt;

               <label>Fare</label>

            &lt;/td&gt;

            &lt;td&gt;                @Html.EJ().CurrencyTextbox("currency").WatermarkText("Amount per unit").**MinValue**(0.00).**MaxValue**(100000.00).**Value**("350.00").**DecimalPlaces**(2)

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Mobile No</label>

            &lt;/td&gt;

            &lt;td&gt;

               @Html.EJ().MaskEdit("maskedit").WatermarkText("Phone number").MaskFormat("99-999-99999").Value("9090909090")

            &lt;/td&gt;

       &lt;/tr&gt;

     &lt;/tbody&gt;

&lt;/table&gt;

  &lt;div class="paybill"&gt;

    @Html.EJ().Button("btn").Size(ButtonSize.Small).Text("Calculate").ContentType(ContentType.TextAndImage).PrefixIcon("e-calender")

  &lt;/div&gt;

&lt;/div&gt;



The following screenshot illustrates the output of the above code examples. 

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img10.png" Caption="Figure 7: Textboxes with Min/Max Value ranges"%}

**Setting the Strict Mode Option**

You can set the “**StrictMode” option** to restrict entering values defined outside the range. The following code example illustrates how to set strict mode option. 

&lt;div class="editors"&gt;

&lt;div class="ele-icon"&gt;&lt;/div&gt;

<div class="ele-txt" style="">ElectricityBill Calculator</div>&lt;br /&gt;

&lt;table class="editors"&gt;

     &lt;tbody&gt;

         &lt;tr&gt;

           &lt;td&gt;

              <label>Unit meters</label>

           &lt;/td&gt;

           &lt;td&gt;                  @Html.EJ().NumericTextbox("numeric").WatermarkText("Units").MinValue(1).MaxValue(10000).Value("70").**EnableStrictMode**(true)

           &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Service Tax</label>

            &lt;/td&gt;

            &lt;td&gt;     

@Html.EJ().PercentageTextbox("percent").WatermarkText("Tax").MinValue(5).MaxValue(100).Value("15")

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

             &lt;td&gt;

               <label>Fare</label>

            &lt;/td&gt;

            &lt;td&gt;   

@Html.EJ().CurrencyTextbox("currency").WatermarkText("Amount per unit").MinValue(0.00).MaxValue(100000.00).Value("350.00").DecimalPlaces(2)

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            &lt;td&gt;

               <label>Mobile No</label>

            &lt;/td&gt;

            &lt;td&gt;    

               @Html.EJ().MaskEdit("maskedit").WatermarkText("Phone number").MaskFormat("99-999-99999").Value("9090909090")

            &lt;/td&gt;

       &lt;/tr&gt;

     &lt;/tbody&gt;

&lt;/table&gt;

  &lt;div class="paybill"&gt;

@Html.EJ().Button("btn").Size(ButtonSize.Small).Text("Calculate").ContentType(ContentType.TextAndImage).PrefixIcon("e-calender")

  &lt;/div&gt;

&lt;/div&gt;

Run the above code example and you can see that it restricts entering a value exceeding the **MinValue** and **MaxValue** range mentioned in the numeric textbox.

**Set Calculation process with Textboxes Widgets**

You can use events to calculate the total and displays the value. You can achieve this with the help of Click **event** in the button widget. The calculation steps are written in the call back function of **Click event** button.

To customize the button, set the **ContentType** as **TextAndImage** to include the icon before the text. Add the **PrefixIcon** value as “**e-calender**” and add the **ClientSideEvents** for click event.

&lt;div class="editors"&gt;



@* Please refer the table format for textboxes customization *@

  &lt;div class="paybill"&gt;

   @Html.EJ().Button("btn").Size(ButtonSize.Small).Text("Calculate").**ContentType**(ContentType.TextAndImage).**PrefixIcon**("e-calender").**ClientSideEvents**(c=>c.**Click**("calculateBill"))

  &lt;/div&gt;

&lt;/div&gt;



&lt;script type="text/javascript"&gt;   

function calculateBill() {

        // Declares Necessary variable creation 

        var kmcalc, servtax, amuntperkm;

        umcalc = $("#numeric").data("ejNumericTextbox");// Object of Numeric 

        servtax = $("#percent").data("ejPercentageTextbox");// Object of Percentage

        amuntperkm = $("#currency").data("ejCurrencyTextbox"); // Object of Currency

        cusmob = $("#maskedit").data("ejMaskEdit"); // Object of MaskEdit        

        // This is used to calculate the Net amount

        var netamunt = umcalc.model.value * amuntperkm.model.value;

        // This is used to calculate the service tax amount

        var sTax = (netamunt * servtax.model.value) / 100;

        // This shows the calculated amount for the units

        alert("The amount $" + (netamunt + sTax) + " has been sent as message to " + cusmob.model.value + ".");

    }

&lt;/script&gt;



Run the above code sample, fill the required Textbox fields and click the Calculate button. The values are displayed and an alert message is shown. The following screen shot illustrates the final output of the Electricity bill calculator. 



{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img11.png" Caption="Figure 8: Electricity bill calculator with alert"%}

## Create your first Editor in ASP.NET

The **Essential ASP.NET WebForms Editors** control includes numeric, percentage, currency and maskedit textbox controls. You can learn how to use **ASP.NET Textboxes** controls in the Electricity bill calculator Application from the following documentation. This guides you to use the wide range of **Textbox** functionalities to complete this application. 

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img12.png" Caption="Figure 9: Electricity Bill Calculator"%}

**Create Textboxes Controls**

**ASP.NET WebForms Textbox** control basically renders with built-in features like keyboard navigation, min and max range and flexible API’s. You can easily create the **Textbox** control by using simple input **Textbox** `element as follows.

1. You can create a WebForms Project and add necessary Dll’s and Scripts with the help of the given [WebForms-Getting Started](http://help.syncfusion.com/ug/js/Documents/gettingstartedwithmv.htm) Documentation.

2. Add necessary **Textbox control** and initialize the corresponding **Textboxes control**



**[ASPX]**





  &lt;div class="editors"&gt;

        &lt;div class="ele-icon"&gt;

        &lt;/div&gt;

        <div class="ele-txt" style="">Electricity Bill Calculator</div>

        &lt;br /&gt;

        &lt;table class="editors"&gt;

            &lt;tbody&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Unit meters</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;%--  Simple numeric text box creation with watermark text--%&gt;

                        &lt;ej:NumericTextBox ID="NumericTextBox" runat="server" WatermarkText="Units"&gt;

                        &lt;/ej:NumericTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Service Tax</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;%--  Percentage text box creation with watermark text --%&gt;

                        &lt;ej:PercentageTextBox ID="PercentageTextBox" runat="server" WatermarkText="Tax"&gt;

                        &lt;/ej:PercentageTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Fare</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;%-- Simple currency text box creation with watermark text --%&gt;

                        &lt;ej:CurrencyTextBox ID="CurrencyTextBox" runat="server" WatermarkText="Amount per unit"&gt;

                        &lt;/ej:CurrencyTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Mobile No</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;%-- Mask Edit text box creation with watermark text --%&gt;

                 &lt;ej:MaskEdit ID="MaskEdit" runat="server" WatermarkText="Phone number"&gt;

                        &lt;/ej:MaskEdit&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/tbody&gt;

        &lt;/table&gt;

        &lt;div class="paybill"&gt;

           &lt;ej:Button ID="Button" runat="server" Text="Calculate" Type="Button" Size="Small" ContentType="TextAndImage" PrefixIcon="e-calender"&gt;

            &lt;/ej:Button&gt;

        &lt;/div&gt;

    &lt;/div&gt;





3. The following styles are added to arrange the **Textboxes**.  You can add the following location in the **URL** path for the background image [http://js.syncfusion.com/UG/Web/Content/electricity.png](http://js.syncfusion.com/UG/Web/Content/electricity.png)



**[CSS]**

  &lt;style type="text/css" class="cssStyles"&gt;

        .ele-icon

        {

            display: inline-block;

            background-image: url(http://js.syncfusion.com/UG/Web/Content/electricity.png);

            background-repeat: no-repeat;

            background-size: contain;

            height: 50px;

            width: 50px;

            margin-left: 50px;

            margin-top: 15px;

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

            border: 2px solid #DDDDDD;

            margin:100px 0 0 100px;

        }

        .editors td

        {

            padding-bottom:5px;

        }



        .editors table

        {

            border: 0px;

            padding-left: 50px;

        }

        .paybill

        {

            margin: 18px 0px 10px 244px;

        }

        table.editors

        {

            margin:0 0 0 61px;

        }

        .editors label

        {

            display: block;

            width: 130px;

        }

    &lt;/style&gt;







4. Execute the code to render a **Textboxes control** as follows

![](getting-started_images\getting-started_img13.png)

_Figure_ _10__: Textboxes with watermark text_

**Set the MinValue, MaxValue and value in Textboxes**

In the above mentioned use case scenario, you can set the **MinValue**, **MaxValue** and **Value** in Numeric, percentage and Currency text boxes for maintaining the range in **Textboxes** controls. You can also enter the values between the ranges that are set as default. You can get the phone number from the user in the **Maskedit control** by using the **MaskFormat** property. You can get the decimal values for **CurrencyTextBox****control** using **DecimalPlaces** property. The following code example illustrates how to achieve this scenario. 

**Code:**

**[ASPX]**

   &lt;div class="editors"&gt;

        &lt;div class="ele-icon"&gt;

        &lt;/div&gt;

        <div class="ele-txt" style="">Electricity Bill Calculator</div>

        &lt;br /&gt;

        &lt;table class="editors"&gt;

            &lt;tbody&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Unit meters</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:NumericTextBox ID="NumericTextBox" runat="server" WatermarkText="Units" MinValue="1" MaxValue="10000" Value="70"&gt;

                        &lt;/ej:NumericTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;&lt;td&gt;<label>Service Tax</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:PercentageTextBox ID="PercentageTextBox" runat="server" WatermarkText="Tax" MinValue="5" MaxValue="100" Value="3"&gt;

                        &lt;/ej:PercentageTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Fare</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:CurrencyTextBox ID="CurrencyTextBox" runat="server" WatermarkText="Amount per unit" DecimalPlaces="2" MinValue="0.00" MaxValue="100000.00" Value="350.00"&gt;

                        &lt;/ej:CurrencyTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Mobile No</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:MaskEdit ID="MaskEdit" runat="server" WatermarkText="Phone number" MaskFormat="99-999-99999" Value="9090909090"&gt;

                        &lt;/ej:MaskEdit&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/tbody&gt;

        &lt;/table&gt;

        &lt;div class="paybill"&gt;

            &lt;ej:Button ID="Button" runat="server" Text="Calculate" Type="Button" Size="Small" ContentType="TextAndImage" PrefixIcon="e-calender"&gt;

            &lt;/ej:Button&gt;

        &lt;/div&gt;

    &lt;/div&gt;

Execute the code to render the resultant output of the above steps

{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img14.png" Caption="Figure 11: Textboxes with Min/Max Value ranges"%}

**Set the Strict Mode Option**

You can set the “**EnableStrictMode”** option****to restrict entering values defined outside the range. The following code example illustrates how to set strict mode option. 

**Code:**

**[ASPX]**

   &lt;div class="editors"&gt;

        &lt;div class="ele-icon"&gt;

        &lt;/div&gt;

        <div class="ele-txt" style="">Electricity Bill Calculator</div>

        &lt;br /&gt;

        &lt;table class="editors"&gt;

            &lt;tbody&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Unit meters</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:NumericTextBox ID="NumericTextBox" runat="server" WatermarkText="Units" MinValue="1" MaxValue="10000" Value="70" EnableStrictMode="true"&gt;

                        &lt;/ej:NumericTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Service Tax</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:PercentageTextBox ID="PercentageTextBox" runat="server" WatermarkText="Tax" MinValue="5" MaxValue="100" Value="3"&gt;

                        &lt;/ej:PercentageTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Fare</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:CurrencyTextBox ID="CurrencyTextBox" runat="server" WatermarkText="Amount per unit" DecimalPlaces="2" MinValue="0.00" MaxValue="100000.00" Value="350.00"&gt;

                        &lt;/ej:CurrencyTextBox&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

                &lt;tr&gt;

                    &lt;td&gt;

                        <label>Mobile No</label>

                    &lt;/td&gt;

                    &lt;td&gt;

                        &lt;ej:MaskEdit ID="MaskEdit" runat="server" WatermarkText="Phone number" MaskFormat="99-999-99999" Value="9090909090"&gt;

                        &lt;/ej:MaskEdit&gt;

                    &lt;/td&gt;

                &lt;/tr&gt;

            &lt;/tbody&gt;

        &lt;/table&gt;

        &lt;div class="paybill"&gt;

            &lt;ej:Button ID="Button" runat="server" Text="Calculate" Type="Button" Size="Small" ContentType="TextAndImage" PrefixIcon="e-calender"&gt;

            &lt;/ej:Button&gt;

        &lt;/div&gt;

    &lt;/div&gt;



Run the above code example and you can see that it restricts entering a value exceeding the **MinValue** and **MaxValue** range mentioned in the numeric textbox.

**Set Calculation process with Textboxes Controls**

You can use events to calculate the total amount and display the value. This is achieved using the **Click event** in the **button** control. The calculation steps are written in the call back function of **Click event** button.

To customize the button, set the **ContentType** as **TextAndImage** to include the icon before the text. Add the **PrefixIcon** value as “**e-calender**” and add the **ClientSideOnClick** event.

**Code:**

**[ASPX]**

  &lt;div class="editors"&gt;

        // Please refer the table format for textboxes customization

  &lt;div class="paybill"&gt;

            &lt;ej:Button ID="Button" runat="server" Text="Calculate" Type="Button" Size="Small" ContentType="TextAndImage" PrefixIcon="e-calender" ClientSideOnClick="calculateBill"&gt;

            &lt;/ej:Button&gt;

        &lt;/div&gt;



    &lt;/div&gt;



**[Script]**

    &lt;script type="text/javascript"&gt;

        function calculateBill() {

             // Declares Necessary variable creation 

        var kmcalc, servtax, amuntperkm;

        umcalc = $("#NumericTextBox").data("ejNumericTextbox");// Object of Numeric 

        servtax = $("#PercentageTextBox").data("ejPercentageTextbox");// Object of Percentage

        amuntperkm = $("#CurrencyTextBox").data("ejCurrencyTextbox"); // Object of Currency

        cusmob = $("#MaskEdit").data("ejMaskEdit"); // Object of MaskEdit        

         // This is used to calculate the Net amount

        var netamunt = umcalc.model.value * amuntperkm.model.value;

        // This is used to calculate the service tax amount

        var sTax = (netamunt * servtax.model.value) / 100;

        // This shows the calculated amount for the units

        alert("The amount $" + (netamunt + sTax) + " has been sent as message to " + cusmob.model.value + ".");

    }  

    &lt;/script&gt;



Execute the above code to render the **Textboxes control.** Fill the required **Textbox** fields and click the **Calculate** button. The values are displayed and an alert message is shown. The following screenshot illustrates the final output of the Electricity bill calculator. 



{% include image.html url="\js\PercentageTextBox\getting-started_images\getting-started_img15.png" Caption="Figure 12: Electricity bill calculator with alert"%}

