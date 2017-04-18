---
layout: post
title: Custom Functions of Calculate for Syncfusion Essential JS
description: custom functions
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# Custom Functions

Calculate engine have the flexibility to create a new formula function or to modify any built-in formula in function library. 

## Add Function

Adding a custom function to the Formula Library is a two-step process. When the `CalcEngine` object is a member of an application, the additional function methods can be added to the application and then these methods should be registered with the `CalcEngine` object after the object is created.



### Step 1-Writing the Method

To calculate custom formula function, writing a method is required. Any kind of convention with respect to passing arguments can be used within the implementation code. Thus, arguments can be a single entry like `A1` or 153 or it can be more complex like `A1:C15`. The computed value will be returned as a string. The arguments can be enhanced with standard items like cell references, numbers, other formulas, etc., using the parsing tools of `CalcEngine` to minimize the amount of code that is required to be written.



Here, add a method that accepts an argument list and then returns the minimum value in the list. The list can be individual cell references and cell ranges, or numbers. This code example uses `CalcEngine` methods to handle the parsing and retrieving of values from the argument list. For example, custom function code has been used here.

{% highlight javascript %}

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

### Step 2-Registering the Method with the CalcEngine

This is achieved by using the `addCustomFunction` method. This method accepts the string that is used when you refer the function in a spreadsheet formula, and the second argument is a custom method name.

{% highlight javascript %}

//Adds formula name ADD to the Library.
calcObj.addCustomFunction("ADD", "customAdd")

{% endhighlight %}

## Remove Function

To remove a single function from the Function Library, use the `calcObj.removeFunction` method, passing a `function name` as the string that references this function from a formula.

{% highlight javascript %}

// Remove formula name ADD from the Library. 
 calcObj.removeFunction("ADD", "customAdd")

{% endhighlight %}

## Replace Function

To replace a function with another implementation, remove the original name and add the same name again with a different method name.

{% highlight javascript %}

// Remove formula name ADD from the Library.
 calcObj.removeFunction("SUM", "customAdd")

//Adds formula name ADD to the Library.
 calcObj.addCustomFunction("ADD", "customAdd")

{% endhighlight %}

## Usage of custom functions

Removing unused functions from the Function Library, reduces the `memory usage and speeds up parsing` as well. Also, if you are only using a selected few Library functions, you may want to remove the unused ones. 

To remove all functions, you can clear the hash table that holds them by using the `engine.LibraryFunctions.Clear` method.

{% highlight javascript %}

  // Remove all functions from the Library.
  engine.LibraryFunctions.Clear();

{% endhighlight %}

After clearing all functions, you can add few functions that will be used often.

