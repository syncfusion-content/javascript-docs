---
layout: post
title: Supported Formulas | JS | Calculate | WidowsForms | Syncfusion
description: supported formulas
platform: JS
control: Calculate
documentation: ug
---

# Math & Trigonometry



## ABS



Returns the absolute Value of a number. The absolute value of a non-negative number is the number itself. The absolute value of a negative number is 1 times the number.



**Syntax:**



_ABS(number)_



where:



* number is the real number for which you want the absolute value.



## ACOT



The `Acot` function retrieves the principal value of the inverse trigonometric cotangent of a number.



To obtain in degrees, use `Degrees` function before `Acot` function.



**Syntax:**



_ACOT(number) or DEGREES ACOT(number)_



where:



* number that is to be converted into acotangent.



Remarks:



* &#35;VALUE! occurs when the number is a non-numeric value.



* The returned angle when given in radians in the range of 0 (zero) to pi.



## ACOTH



The `Acoth` function retrieves the inverse hyperbolic cotangent of a number.



**Syntax:**



_ACOTH(number)_



where:



* number that is to be converted into cotangent.



**Remarks:**



* &#35;NUM! occurs when number is lesser than one.



* &#35;VALUE! occurs when absolute value of number is lesser than one.



## ARABIC



A Roman numeral is converted into an Arabic numeral.



**Syntax:**



_ARABIC( romannumeral )_



where:



* romannumeral is the text given by you to convert it into Arabic numeral.



Remarks:



* &#35;VALUE! occurs when text is not a valid value.



* &#35;VALUE! occurs when text is not a valid Roman numeral.



* Value zero occurs when an empty string is given as an input.



## ACOS



Returns the inverse cosine of a number. Inverse cosine is also referred to as arccosine. The arccosine is the angle whose cosine is the given number. The returned angle is given in radians in the range of 0 to pi.



**Syntax:**



_ACOS(number)_



where:



* number is the cosine of the angle that you want and must be between -1 and 1.



## ACOSH



Returns the inverse hyperbolic cosine of a number. The number must be greater than or equal to 1. The inverse hyperbolic cosine is the value whose hyperbolic cosine is the given number.



**Syntax:**



_ACOSH(number)_



where:



* number is any real number that is greater than or equal to 1.



## ASIN



Returns the inverse sine of a number. Inverse sine is also referred to as arcsine. The arcsine is the angle whose sine is the given number. The returned angle is given in radians in the range from -pi/2 to +pi/2.



**Syntax**



_ASIN(number)_



where:



* number is the sine of the angle that you want and must be between -1 and 1.



## ATAN



Returns the inverse tangent of a number. Inverse tangent is also known as arctangent. The arctangent is the angle whose tangent is a number. The returned angle is given in radians in the range from -pi/2 to +pi/2.



**Syntax**



_ATAN(number)_



where:



* number is the tangent of the angle that you want.



## ATAN2



Returns the inverse tangent of the specified x- and y-coordinates. The arctangent is the angle from the x-axis to a line containing the origin (0, 0) and the point (x_num, y_num). The angle is given in radians between -pi and pi, excluding -pi.



**Syntax:**



_ATAN2(x_num,y_num)_ 



where:



* x_num is the X coordinate of the point.



* y_num is the Y coordinate of the point.



Remarks:



* A positive result represents counterclockwise angle from the x-axis; and negative result represents clockwise angle.



* `ATAN2(a,b)` equals `ATAN(b/a)` , except that a can equal 0 in ATAN2.



## COMBIN



Returns the number of combinations for a given number of items. Use `COMBIN` to determine the total possible number of groups for a given number of items.



**Syntax:**



_COMBIN(number, number_chosen)_



where:



* number is the number of items.



* number_chosen is the number of items in each combination.



Remarks:



* Numeric arguments are truncated to integers.



* A combination is any set or subset of items, regardless of their internal order. Combinations are distinct from permutations where the internal order is significant.



* The number of combinations is as follows, where number = n and number_chosen = k:



## COT



The `Cot` function returns the cotangent of an angle specified in radians.



**Syntax:**



_COT(number)_



where:



* number-angle radians to get the cotangent value.



Remarks:



* &#35;NUM! occurs when the number is out of the range.



* &#35;VALUE! occurs when the number is a non-numeric value.



## CSC



The `CSC` function returns the cosecant of an angle specified in radians.



**Syntax:**



_CSC(number)_ 



where:



* number-angle radians to get the cosecant value.



Remarks:



* &#35;NUM! occurs when the number is outside its constraints.



* &#35;VALUE! occurs when the number is a non-numeric value.



## CSCH



The `CSCH` function returns the hyperbolic cosecant of an angle specified in radians.



**Syntax:**



_CSCH(number)_



where:



* number-angle radians to get the hyperbolic cosecant value.



Remarks:



* &#35;NUM! occurs when the number is outside its constraints.



* &#35;VALUE! occurs when the number is a non-numeric value.



## COS



Returns the cosine of the given angle.



**Syntax:**



_COS(number)_



where:



* number is the angle in radians for which you want the cosine.



## COSH



Returns the hyperbolic cosine of a number.



**Syntax:**



_COSH(number)_



where:



* number is any real number for which you want to find the hyperbolic cosine.





## COMBINa



For a given number of items, the `Combina` function returns the number of combinations.



**Syntax:**



_COMBINA(number1, number2)_



where:



* number1 is total number of items.



* number2 is total number of items to be chosen.



Remarks:



* &#35;NUM! occurs when either value is out of range.



* &#35;VALUE! occurs when either value is non-numeric.



## CEILING



The `Ceiling` function returns number rounded up, away from zero, to the nearest multiple of significance. For example, if you want to avoid using pennies in your prices and your product is priced at $4.82, use the formula =CEILING(4.82,0.05) to round prices up to the nearest nickel.



**Syntax:**



_CEILING(number, significance)_



where:



* number is the value you want to round off.



* significance is the multiple to which you want to round.



Remarks:



* Both values must be numeric.



* Regardless of the sign of a number, a value is rounded up when adjusted away from zero. If the number is an exact multiple of significance, no rounding occurs.



## CEILING.Math



The `Ceiling.Math` function returns the number rounded up to a multiple of another number.



**Syntax:**



_CEILING(number, [significance],  [mode])_



where:



* number-number that is rounded up to a multiple of significance.



* significance-multiple to which the number is rounded.



* mode is for negative numbers; it controls whether the number is rounded toward or away from zero.



## DECIMAL



A text representation of a number in a given base to be converted into a decimal number.



**Syntax:**



_DECIMAL(text, radix)_ 



where:



* text is a string.



* radix is an integer.



Remarks:



* &#35;NUM! or &#35;VALUE! occurs when text or radix is outside the constraints.



## DEGREES



Converts radians into degrees.



**Syntax:**



_DEGREES(angle)_



where: 



* angle is the angle in radians that you want to convert.



## EVEN



Returns the number rounded up to the nearest even integer.



**Syntax:**



_EVEN(number)_



where:



* number is the value that is to be rounded.



Remarks:



* Regardless of the sign of the number a value is rounded up when adjusted away from zero. If the number is an even integer no rounding occurs.



## EXP



Returns e raised to the power of the given number.



**Syntax:**



_EXP(number)_



where:



* number is the exponent applied to the base e.



## FACT



Returns the factorial of a number. The factorial of a number is the product of all positive integers <= the given number.



**Syntax:**



_FACT(number)_



where:



* number is the non-negative number for which you want the factorial of. If the number is not an integer, it is truncated.



## FACTDouble



`FactDouble` function returns the double factorial of a given value. The given value is an integer value.



**Syntax:**



_FACTDOUBLE (number)_



where:



* number-This value is required.



Remarks:



* &#35;NUM! when the number is lesser than zero (0).



* &#35;VALUE! Occurs when any of the given argument is non-numeric



## INT



Rounds a number down to the nearest integer.



**Syntax:**



_INT(number)_



where: 



* number is the real number that you want to round down to an integer.



## LN



Returns the natural logarithm of a number. Natural logarithms are based on the constant e (2.718281828459...).     



**Syntax:**



_LN(number)_



where:



* number is the positive real number for which, you want the natural logarithm.



Remarks:



* LN is the inverse of the EXP function.



## LOG



Returns the logarithm of a number to the base that you specify.



**Syntax:**



_LOG(number, base)_



where:



* number is the positive real number for which, you want the logarithm.



* base is the base of the logarithm. If base is omitted, it is assumed to be 10.



## LOG10



Returns the base-10 logarithm of a number.



**Syntax:**



_LOG10(number)_



where:



* number is the positive real number for which, you want the base-10 logarithm.



## SIN



Returns the sine of the given angle.



**Syntax:**



_SIN(number)_



where:



* number is the angle in radians for which you want the sine.



## SINH



Returns the hyperbolic sine of a number.



**Syntax:**



_SINH(number)_



where:



* number is any real number.



## SEC



The `Sec` function returns the secant of an angle.



**Syntax:**



_SEC(number)_ 



where:



* number-angle radians to get the secant value.



Remarks:



* &#35;NUM! occurs when the number is outside its constraints.



* &#35;VALUE! occurs when number is a non-numeric value.



## SUBTOTAL



`Subtotal` function returns a subtotal in a list. Once the subtotal list is created, you can modify it by editing the `Subtotal` function.



**Syntax:**



_SUBTOTAL (function_Number, ref1, (ref2)...)_



where:



* A function_Number is required. This specifies which function to use for calculating subtotals within a list. Here is the list of functions supported by Syncfusion:



_Function numbers_



<table>

<tr>

<th>

<b>Function Numbers</b></th><th>

<b>Function Names</b></th></tr>

<tr>

<td>

1</td><td>

AVERAGE</td></tr>

<tr>

<td>

2</td><td>

COUNT</td></tr>

<tr>

<td>

3</td><td>

COUNTA</td></tr>

<tr>

<td>

4</td><td>

MAX</td></tr>

<tr>

<td>

5</td><td>

MIN</td></tr>

<tr>

<td>

6</td><td>

PRODUCT</td></tr>

<tr>

<td>

7</td><td>

STDEV</td></tr>

<tr>

<td>

8</td><td>

STDEVP</td></tr>

<tr>

<td>

9</td><td>

SUM</td></tr>

<tr>

<td>

10</td><td>

VAR</td></tr>

</table>



* ref1-The first named range that is used for the subtotal. This value is required.



* ref2-This value is optional.



## PI



The `PI` function returns the number 3.14159265358979, the mathematical constant pi, accurate to 15 digits.



**Syntax:**



_PI( )_



## PRODUCT



Multiplies all the numbers given as arguments and returns the product.



**Syntax:**



_PRODUCT(number1, number2, ...)_



where: 



* number1, number2, ... are numbers that you want to multiply.



## SQRT



The `SQRT` function returns a positive square root.



**Syntax:**



_SQRT(number)_



where:



* number is the number for which you want the square root.



Remarks:



* Number must be >= 0.



## SUMIF



Adds the cells specified by a given criteria.



**Syntax:**



_SUMIF(range, criteria, sum_range)_ 



where:



* range is the range of cells you want evaluated.



* criteria is the criteria in the form of a number, expression, or text that defines the cells to be added. For example, criteria can be expressed as ">32" or some other logical expression.



* Sum_range is the actual cells to sum.



Remarks:



* The cells in sum_range are summed only if their corresponding cells in range match the criteria.



* If sum_range is omitted, the cells in range are summed.



## TAN



Returns the tangent of a number.



**Syntax:**



_TAN(number)_



where:



* number is the tangent of the angle that you want.



## TRUNC



The `Trunc` function truncates a supplied number to a specified number of decimal places.



**Syntax:**



_TRUNC( number, [num_digits] )_



where:



* number is the initial number that is truncated.



* [num_digits] is an optional argument that specifies the number of decimal places to truncate the supplied number to. The default value is 0.



## ISTEXT



The `IsText` function returns a Boolean value after determining that the provided value is a string.



**Syntax:**



_ISTEXT(text)_



where:



* text is the value you want to test if it is a string or not.