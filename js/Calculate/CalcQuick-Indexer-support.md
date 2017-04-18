---
layout: post
title: CalcQuick Indexer support of Calculate for Syncfusion Essential JS
description: calcquick (indexer) support
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# CalcQuick (Indexer) Support
The indexer method will be used in calculate through an instance of `CalcQuick` class. This class provides options to directly parse and compute a formula, or register variable names that can later be used in more complex formulas involving these variables. After registering the variables, it provides options to perform manual or automatic calculations.

These keys or virtual references must be enclosed within square brackets `[ ]`. `Eg. [A]`

## Manual Calculation
Manual calculations requires explicit request of Calculate CalcEngine to compute the value and return it. These methods can be invoked from the `CalcQuick` class.

### Working with keys 

CalcQuick object can be created in the `body` tag like below,

{% highlight html %}

<script type="text/javascript">

 // … other codes
 
 var calculator = new CalcQuick();

// .. other codes. 

</script>

{% endhighlight %}

Each element is registered as the key or virtual references in the `CalcQuick` by using the `setKeyValue` method.

{% highlight javascript %}

<script type="text/javascript">

 // … other codes
 var calculator = new CalcQuick();
 calculator.setKeyValue("A", document.getElementById("txtBoxA").value);
 calculator.setKeyValue("B", document.getElementById("txtBoxB").value);
 calculator.setKeyValue("C", document.getElementById("txtBoxC").value);

 // .. other codes.

</script>

{% endhighlight %}

After registering keys, the formulas and values are assigned for the keys.

{% highlight javascript %}

document.getElementById("txtBoxA").value = "12"; 
document.getElementById("txtBoxB").value = "3"; 
document.getElementById("txtBoxC").value = "= [A] + 2 * [B]"; 
// codes -> setDirty

{% endhighlight %}

### Evaluating keys

The evaluation of keys can be triggered using `setDirty` method which will computes the formulas of the keys.

{% highlight javascript %}

//evaluating key formulas
calculator.setDirty(); 
document.getElementById("txtBoxA").value = calculator.getKeyValue("A"); 
document.getElementById("txtBoxB").value = calculator.getKeyValue("B"); 
document.getElementById("txtBoxC").value = calculator.getKeyValue("C");

{% endhighlight %}



Whereas, the result will be returned through `getKeyValue` method.

## Auto Calculation

Instead of using `setDirty`, the automatic calculation can be triggered at the time of assigning the values to keys by enabling `autoCalc` property and the `ValueSet` event handler will be used to retrieve the values.

{% highlight javascript %}

// Codes. 
calculator.autoCalc = true; 
function valueSet(event, data) {
 switch (data.key) {
   case "A":
     document.getElementById("txtBoxA").value = calculator.getKeyValue("A");
     break;
   case "B":
     document.getElementById("txtBoxB").value = calculator.getKeyValue("B");
     break;
   case "C":
     document.getElementById("txtBoxC").value = calculator.getKeyValue("C");
     break;
   case "D":
     document.getElementById("txtBoxD").value = calculator.getKeyValue("D");
     break;
   default:
     break;
 }
}
calculator.valueSetEventHandler = valueSet;

// Codes.

{% endhighlight %}

