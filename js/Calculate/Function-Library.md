---
layout: post
title: Function-Library
description: function library
platform: js
control: Calculate
documentation: ug
---

## Function Library

The **Function Library** contains many functions from statistics, finance, and mathematics, along with other general purpose functions. There are more than 150 entries in the library, and it is easy to add your own calculations. The functions are discussed in the following topics.

### Add Function

**CalcEngine** supports adding your own formula to get the desired calculation support to your business object. Adding a custom function to the Formula Library is a two-step process. 

The first step is to write a method that actually does the calculation for your custom function. The second step is to register this method with the **CalcEngine**. Thus, when the **CalcEngine** object is a member of an application, you can add your additional function methods to the application and then register these methods with the **CalcEngine** object after the object is created in **HTML**.

The **Add Function** is explained in detail in the following topics.

#### Step 1-Writing the Method

To calculate custom formula function writing a method is required. You can use any kind of convention with respect to passing arguments and within your implementation code. Thus, args can be a single entry like A1 or 153 or it can be more complex like A1:C15. It is up to your implementation code to parse args, use the information parsed in to compute the value and then return this value as a string. When you want your arguments to be standard items like cell references, numbers, other formulas, etc., **CalcEngine** has some parsing tools that can be used to minimize the amount of code that is required to be written, but, you are not limited to what **CalcEngine** contains. You can design and implement any argument convention you want as long as your method has the required signature.

Here, add a method that accepts an argument list and then returns the minimum value in the list. The list can be individual cell references and cell ranges, or numbers. This code example uses **CalcEngine** methods to handle the parsing and retrieving of values from the argument list. For example, custom function code has been used here.

{% highlight js %}

 customAdd = function (argsList) {
                var splitArgs = 
                argsList.split(calcObj.getParseArgumentSeparator())
                var result = 0;
                for (var i in splitArgs) {
                    var s1 = calcObj.getValueFromArg(splitArgs[i]);
                    result = Number(result) + Number(s1);
                }
                return result;
            }


{% endhighlight %}

#### Step 2-Registering the Method with the CalcEngine

The second step to add your own formula is to register your method with the **CalcEngine** object. This is achieved by using the **addCustomFunction** method. This method accepts the string that is used when you refer the function in a spreadsheet formula, and the second argument is a custom method name.

{% highlight js %}

 //Adds formula name ADD to the Library.
 calcObj.addCustomFunction("ADD", "customAdd")


{% endhighlight %}



