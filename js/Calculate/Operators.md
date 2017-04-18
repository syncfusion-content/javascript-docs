---
layout: post
title: Operators of Calculate for Syncfusion Essential JS
description: operators
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# Operators

The calculation type of an equation will be specified by operators. These operators will be prioritized in a default order for calculating the equation. 

To recognize a particular string is to be treated as a formula, the string is required to start with a special character `formulaCharacter`. Its default character is the equals `=` sign.

## Arithmetic operators

The mathematical operations such as addition, subtraction, multiplication etc can be performed using the arithmetic operators.

<table>
<tr>
<th>
Arithmetic operator</th><th>
denotation</th><th>
Example</th></tr>
<tr>
<td>
+ (plus sign)</td><td>
Addition</td><td>
1 + 2</td></tr>
<tr>
<td>
-  (minus sign - unary) </td><td>
Negation</td><td>
- 5</td></tr>
<tr>
<td>
-  (minus sign - binary)</td><td>
Subtraction </td><td>
4 - 2</td></tr>
<tr>
<td>
* (asterisk)</td><td>
Multiplication </td><td>
2 * 5</td></tr>
<tr>
<td>
/ (forward slash)</td><td>
Division</td><td>
10 / 2</td></tr>
<tr>
<td>
^ (caret)</td><td>
Exponentiation </td><td>
5 ^ 2</td></tr>
</table>




## Logical Operators 

The logical or comparison operators will be used to compare two values of the formula. The return value will be either `True` or `False`.



<table>
<tr>
<th>
Logical operator</th><th>
denotation</th><th>
Example</th></tr>
<tr>
<td>
< (less than sign)</td><td>
Less than</td><td>
5 < A2</td></tr>
<tr>
<td>
> (greater than sign)</td><td>
Greater than</td><td>
A1 > A2</td></tr>
<tr>
<td>
= (Equal sign)</td><td>
Equal to</td><td>
A1 = 4</td></tr>
<tr>
<td>
<= (Less than or equal)</td><td>
Less than or equal</td><td>
A3 <= (A4 + 2)</td></tr>
<tr>
<td>
>= (Greater than or equal)</td><td>
Greater than or equal</td><td>
B1 >= 30</td></tr>
<tr>
<td>
<>(Not equal)</td><td>
Not equal</td><td>
C2 <>10</td></tr>
</table>


## Text concatenation operator (Binary literal operator)

Two or more text strings can be concatenated into one text using this operator. 



<table>
<tr>
<th>
Logical operator</th><th>
denotation</th><th>
Example</th></tr>
<tr>
<td>
& (ampersand)</td><td>
Concatenation</td><td>
“Hello” & “World”</td></tr>
</table>


## Operator precedence

All operations are subjected to the following hierarchy of operations. The level 1 operations are done first, followed by level 2, and so on. Within the same level, the operations are performed from left to right in the order where they are encountered during the parsing of the formula.



1. (Unary Minus)



2. /



3. + -



4. < >= <= >= <>



5. & (Concatenation)



When the default operators’ precedence need to be changed, then the parentheses will be used to explicitly indicate the operation order.



**Examples**

<table>
<tr>
<th>
Formulas</th><th>
Computed Value</th></tr>
<tr>
<td>
= 6 / 2 + 1</td><td>
4</td></tr>
<tr>
<td>
= 6 / (2 + 1)</td><td>
2</td></tr>
<tr>
<td>
= 2 + 4 / 2</td><td>
4</td></tr>
<tr>
<td>
= (2 + 4) / 2</td><td>
3</td></tr>
</table>


