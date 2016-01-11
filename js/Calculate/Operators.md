---
layout: post
title: Operators
description: operators
platform: js
control: Calculate
documentation: ug
---

# Operators

The list of the **Operators** supported by **ej.calculate.js** are

_Operators_

<table>
<tr>
<td>
<b>Operators </b></td><td>
<b>Description     </b></td></tr>
<tr>
<td>
Unary Arithmetic Operator</td><td>
Unary Minus Sign</td></tr>
<tr>
<td>
Binary Arithmetic Operators</td><td>
+        Addition-         Subtraction*         Multiplication/         Division^        Exponentiation</td></tr>
<tr>
<td>
Binary Literal Operator</td><td>
&        Concatenation</td></tr>
<tr>
<td>
Binary Logical Operators</td><td>
<        Less Than >        Greater Than=         Equal To<=       Less Than Or Equal>=       Greater Than Or Equal&lt;&gt;       Not Equal</td></tr>
</table>
All operations are subjected to the following hierarchy of operations. The level 1 operations are done first, followed by level 2, and so on. Within the same level, the operations are performed from left to right in the order where they are encountered during the parsing of the formula.

1. \- (Unary Minus)

2. \*    /

3. \+    -

4. &lt;   &gt;    =    &lt;=    &gt;=    &lt;&gt;

5. & (Concatenation)



When you want to change the default operators precedence, then use parentheses to explicitly indicate the operation order.

**Examples**

<table>
<tr>
<td>
<b>Formulas  </b></td><td>
<b>	Computed Value</b></td></tr>
<tr>
<td>
= 6 / 2 + 1                     </td><td>
<i>4</i></td></tr>
<tr>
<td>
<i>= 6 / (2 + 1)                   </i></td><td>
<i>2</i></td></tr>
<tr>
<td>
<i>= 2 + 4 / 2                     </i></td><td>
<i>4</i></td></tr>
<tr>
<td>
<i>= (2 + 4) / 2                   </i></td><td>
<i>3</i></td></tr>
</table>
****

Logical operations return specific values: **True** or **False**. When you require specific numerical values associated with any logical expression, then use the logical expression as the first argument in the Formula Library IF-function, with the second argument being the numerical value as **True** and the third argument being the numerical value as **False**. When you use a well-formed logical expression in a larger calculation, **true** evaluates to numerical 1 and **false** evaluates to numerical 0 for use in the calculations.

## Equal Sign, the Formula Character

To indicate that a particular string is to be treated as a formula, you can start the string with a special character, **CalcEngine.formulaCharacter**. This property is static and so you can change the formula character within your code. Its default value is the equals sign (=).

In general, for **Essential Calculate** to recognize a string as containing a formula, the string is required to start with the **CalcEngine.formulaCharacter**. There is one exception though; when you explicitly use a **CalcEngine** Parse method like **calcObj.parseFormula** or **calcObj.parseAndComputeFormula**, including the formula character as the first character in the passed string, it is optional.

## Function Library Formulas

You can use **Function Library Formulas** as a stand-alone formula, and it can also be incorporated into more complex formulas.

_Function Library formula_

<table>
<tr>
<td>
<b>Formula</b></td><td>
<b>Comment</b></td></tr>
<tr>
<td>
= Sin(3.14159)</td><td>
Returns the sine of 3.14159 radians</td></tr>
<tr>
<td>
= 2 * Sin(3.14159) + Sqrt(2)      </td><td>
Returns 2 * sine of 3.14159 radians plus the square root of 2.</td></tr>
<tr>
<td>
  = 2 * Pi()       </td><td>
 Returns 2 * pi.</td></tr>
</table>
Some library functions cannot have arguments, but you can still include the parentheses to indicate that you are using a library function. For example, = 2 * Pi(), illustrates the proper use of the library function Pi.

## NamedRange support.

**ej.calculate.js** supports namedRange in business object calculations similar to excel worksheet. This provides complete and fast support like excel sheet. You can assign the whole namedRange collection to **CalcEngine** object by using **setNamedRange**() method or you can add the namedRanges by using **calcObj. addNamedRange** method. Refer to the following code example.

{% highlight js %}


                      calcObj.addNamedRange($("#newName").val(), cell


{% endhighlight %}

Refer to the following screenshot to get more details on **addNamedRange** support.

![](/js/Calculate/Operators_images/Operators_img1.png)




