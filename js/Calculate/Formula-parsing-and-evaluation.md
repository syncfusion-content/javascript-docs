---
layout: post
title: Formula parsing and evaluation of Calculate for Syncfusion Essential JS
description: formula parsing and evaluation
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# Formula Parsing and Evaluation

Calculate engine have a built-in formula parser and evaluate the parsed formula using `CalcEngine.parseAndComputeFormula` method.

## Parsing 

The built-in formula parser will parse the formula into a well formed version using `CalcEngine.parse` method for computing it. The parsing recognizes and replaces `NamedRanges` with their corresponding value. The parsing also recognizes library functions and tokenizes them as well. 



`CalcEngine.Parse` method accepts a string formula, for example `= A2 + 5` and checks whether it is a valid formula that `CalcEngine` can understand. After that, it returns a string that represents a parsed version of the formula that can be more readily computed.

## Parsing Order

The parsed formula is a Reverse Polish Notation expression using tokens to compactly represent the entered formula. For example, the `4 + 3 * PI()/2` formula will be parsed in the following order,

* All the operands will be indexed into a stack. It can be functions, references, or constants.
* Then, the operators will be parsed using the default of operators. The returned string will be `4 + 3 * PI()/2`.



## Evaluation

The parsed formulas will be evaluated through `computedValue` method. It accepts a parsed formula and uses a stack oriented calculation technique to convert the parsed formula into the value that it represents. The value returned is a string holding the computed quantity



Similarly, parsing and computing will be done through `ParseAndCompute` method. This will be using internal parsing and no parsed string will be returned.

## Computing sheet formulas

To calculate a sheet formula, the sheet should be registered to `CalcEngine` object before that. The sheet / grid should be implemented from `CalcData` which will be having the intermediate methods `SetValueRowCol` and `GetValueRowCol` methods.

### Setting cell formulas

The index based values can be set based on spreadsheet like rowIndex and colIndex when formula is applied in a cell using `SetValueRowCol` method.

{% highlight javascript %}

calcObj.setValueRowCol = function (sheetID, value, row, col) { 
//set the value to grid cell 
}

{% endhighlight %}

### Retrieving cell values

The `GetValueRowCol` method gets the value of a cell based on the spreadsheet like rowIndex and colIndex.

{% highlight javascript %}

calcObj.getValueRowCol = function (sheetID,row, col) { 
//return the data based on row and column index 
}

{% endhighlight %}

## Error messages 

The error messages that are displayed by Essential Calculate can be found in this string array in the `CalcEngine`. After a `CalcEngine` object has been created, the text of these messages can be changed by altering the array values.



When there is no need for throwing these error messages from calculate, the spreadsheet like error strings will be returned from `CalcEngine.errorStrings` collection by disabling the `rethrowLibraryExceptions` property.

