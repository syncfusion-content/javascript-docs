---
layout: post
title: CalcQuick
description: calcquick
platform: js
control: Calculate
documentation: ug
---

# CalcQuick

In this section, you can learn how to use the **CalcQuickBase** object to perform arbitrary calculations in the web Application. This shows the minimal steps that are required to use the **ejCalculate** to add calculation support to an application. This quick application lets you type algebraic expressions and display the calculated results in the web page like (([A] * [B] *22) / [C]).

## Web application by using the CalcQuickBase

You have to create a web page that requests a formula from you. The application requires the formula to be an algebraic expression For example, you might register a variable named Rate to be 0.07 and a variable named Amount to be 1500, and then compute a quantity represented by the formula Rate * Amount or by (1 + Rate) * Amount.

### Script for the CalcQuick

Create a new **HTML** Page and add the following script to perform the script-related changes these scripts need for the **calcQuick** calculation. 

{% highlight js %}

    <script src="../scripts/jquery-1.10.2.min.js"></script>
    <script src="../scripts/jquery.easing.1.3.min.js"></script>
    <script src="../scripts/jquery.globalize.min.js"></script>
    <script src="../scripts/jquery.validate.min.js"></script>
    <script src="../scripts/jquery.validate.unobtrusive.min.js"></script>
    <script src="../scripts/jsondata.min.js"></script>
    <script src="../scripts/jsrender.min.js"></script>
    <script src="../scripts/ej.web.all.min.js" type="text/javascript">     
    </script>
    <script src="../scripts/properties.js" type="text/javascript"></script>

{% endhighlight %}



### Adding elements 

Add the Text boxes in the body of the HTML page for calculation. You need to add these elements as CalcQuick keys.

{% highlight html %}

  <div class="col-md-3">
    A
 </div>
 <div class="col-md-3">
     <input type="text" id="txtBoxA" />
 </div>        

{% endhighlight %}

### Register elements as Keys

Now, register these elements as keys in the CalcQuick. The **setKeyValue** method of the CalcQuick is used to register the keys in the CalcQuick object.



{% highlight js %}

  <script type="text/javascript">
      // … other codes
      var calculator = new CalcQuick();
      calculator.setKeyValue("A", document.getElementById("txtBoxA").value);
      calculator.setKeyValue("B", document.getElementById("txtBoxB").value);
      calculator.setKeyValue("C", document.getElementById("txtBoxC").value);
      calculator.setKeyValue("D", document.getElementById("txtBoxD").value);
      // .. other codes.
 </script>

{% endhighlight %}



### Assign Formulas and Values

After registering the keys, you have to assign the formulas and values for the keys.



{% highlight js %}

 <script type="text/javascript">

     // Codes.
     var calculator = new CalcQuick();
     document.getElementById("txtBoxA").value = "12";
     document.getElementById("txtBoxB").value = "3";
     document.getElementById("txtBoxC").value = "= [A] + 2 * [B]";
    // codes
</script>

{% endhighlight %}



Now, the HTML page is displayed like the following image.

![]("/js/Calculate/CalcQuick_images/CalcQuick_img1.png" Caption="")

### Manual Calculation

Click the **calculate** button to perform the calculation of the key elements. On button click, each element is registered as the key in the CalcQuick by using the setKeyValue method. In this application, textbox **C** is used for formula calculation and the formula is passed to compute the A and B text boxes. The following is the formula ("= [A] + 2 * [B]”), and the result is displayed in the following image.



{% highlight js %}

  <script type="text/javascript">

      // Codes.
     calculator.setKeyValue("A", document.getElementById("txtBoxA").value);
     calculator.setKeyValue("B", document.getElementById("txtBoxB").value);
     calculator.setKeyValue("C", document.getElementById("txtBoxC").value);
     calculator.setKeyValue("D", document.getElementById("txtBoxD").value);
     calculator.setDirty();

     document.getElementById("txtBoxA").value = calculator.getKeyValue("A")
     document.getElementById("txtBoxB").value = calculator.getKeyValue("B");
     document.getElementById("txtBoxC").value = calculator.getKeyValue("C");
     document.getElementById("txtBoxD").value = calculator.getKeyValue("D");
     
    </script>



{% endhighlight %}

![]("/js/Calculate/CalcQuick_images/CalcQuick_img2.png" Caption="")

### Auto Calculation

Enable **AutoCalculation** while changing the value of elements that is textboxes in this application. For this, enable the property, **autoCalc**.  When **autoCalc** is enabled in the calcQuick, elements are computed internally while the element value in the HTML page is changed and the computed value is passed through the valueSet event.

In the valueSet event, handle the code to set the value for the elements. Before this, set the function for the event to get the key value of the element on calculation. The **valueSetEventHandler** property is used to set the event method. 



{% highlight js %}

 <script type="text/javascript">
         // Codes.
         calculator.autoCalc = true;

function valueSet(event, data) {
            switch (data.key) {
               case "A":
                    document.getElementById("txtBoxA").value = calculator.getKeyValue("A");
                    break;
                case "B":
                    document.getElementById("txtBoxB").value = calculator.getKeyValue("B")
                    break;
                case "C":
                    document.getElementById("txtBoxC").value = calculator.getKeyValue("C")
                    break;
                case "D":
                    document.getElementById("txtBoxD").value = calculator.getKeyValue("D")
                    break;
                default:
                    break;
            }
        }
     calculator.valueSetEventHandler = valueSet;
        // Codes.
    </script>




{% endhighlight %}



![]("/js/Calculate/CalcQuick_images/CalcQuick_img3.png" Caption="")

### Show Formula

You can view the formula of elements by using the method, showFomula of the calcQuick. Refer to the following codes and image.



{% highlight js %}

 <script type="text/javascript">

      // Codes.
      $("#lt1Button2").click(function () {

      document.getElementById("txtBoxA").value = calculator.getFormula("A")
      document.getElementById("txtBoxB").value = calculator.getFormula("B");
      document.getElementById("txtBoxC").value = calculator.getFormula("C");
      document.getElementById("txtBoxD").value = calculator.getFormula("D");
      });

      // Codes.
    </script>

{% endhighlight %}

![]("/js/Calculate/CalcQuick_images/CalcQuick_img4.png" Caption="")

