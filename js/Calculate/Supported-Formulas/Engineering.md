---
layout: post
title: Supported Formulas of Calculate for Syncfusion Essential JS
description: supported formulas
platform: JS
control: Calculate
documentation: ug
---

# Engineering



## BESSELI



The `BESSELI` function returns the modified Bessel function `In(X)`, which is equivalent to the Bessel function evaluated for purely imaginary arguments.



**Syntax:**



_BESSELI(X, N)_



**where:**



* X is the value at which the function is to be evaluated.



* N is the positive integer, representing the order of the function. If the N value is represented as decimal, it is truncated as integer.



**Remarks:**



* Returns `#NUM!` , if the supplied value of n is lesser than 0.



* If any of the supplied arguments are non-numeric, it returns `#VALUE!` error.



## BESSELJ



The `BESSELJ` function returns the Bessel function `Jn(X)`.
 


**Syntax:**



_BESSELJ( X, N )_



**where:**



* X is the value at which the function is to be evaluated.



* N is the order of the Bessel function and it must be a positive number.



**Remarks:**



* Returns `#NUM!` if the supplied value of n is lesser than 0.



* If any of the supplied arguments are non-numeric, it returns `#VALUE!` error.



## BESSELK



The `BESSELK` function returns the modified Bessel function `Kn(X)`, which is equivalent to the Bessel function evaluated for purely imaginary arguments.



**Syntax:**



_BESSELK( X, N )_



**where:**



* X is the value at which the function is to be evaluated.



* N is the positive integer which denotes the order of the modified Bessel function.



**Remarks:**



* Returns `#NUM!`, if either N is Lesser than 0 or X is lesser than or equal to 0.



* Returns `#VALUE!`, if any of the supplied argument are non-numeric.



## BESSELY



The `BESSELY` function returns the Bessel function `Yn(X)`. 



**Syntax:**



_BESSELY( X, N )_



**where:**



* X is the value at which the function is to be evaluated.



* N is the positive integer which denotes the order of the Bessel function.



**Remarks:**



* Returns `#NUM!`, if either N is Lesser than 0 or X is lesser than or equal to 0.



* Returns `#VALUE!`, if any of the supplied argument are non-numeric.



## BIN2OCT



The `BIN2OCT` function converts a binary number into an octal number.



**Syntax:**



_BIN2OCT(num, places)_ 



**where:**



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



## BIN2HEX



The `BIN2HEX` function converts a binary number into a hexadecimal.



**Syntax:**



_BIN2HEX(num places)_ 



**where:**



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



**Remarks:**



* `#NUM!` occurs when number is not a valid binary number, when places is negative.



* `#VALUE!` occurs when places is non-numeric.



## BIN2DEC



The `BIN2DEC` function converts a binary number into a decimal number.



**Syntax:**



_BIN2DEC(num)_ 



**where:**



* num is the binary number that you want to convert.



**Remarks:**



* `#NUM!` occurs when number is not a valid binary number or when number contains more than 10 characters.



## BITAND


The `BITAND` function returns the bitwise `AND` of two numbers.



**Syntax:**



_BITAND(num1,num2)_



**Where:**



* num1 and num2 should be in decimal format.



**Remarks:**



* `#NUM!` - occurs if num1 or num2 is less than zero, if num1 or num2 is a non-integer or is greater than (2^48)-1.



* `#VALUE!` - occurs if num1 or num2 is a non-numeric value.



## BITLSHIFT



The `BITLSHIFT` function returns a number shifted left by specified number of bits.



**Syntax:**



_BITLSHIFT(num1,num2)_



**Where:**



* num1 must be an integer greater than or equal to 0.



* Num2 must be an integer.



**Remarks:**


	
* `#NUM!` - occurs if num1 or num2 is less than zero, if num1 or num2 is a non-integer or is greater than (2^48)-1.



* `#VALUE!` - occurs if num1 or num2 is a non-numeric value.



## BITOR



The `BITOR` function returns a bitwise ‘OR’ of two numbers.



**Syntax:**



_BITOR(num1, num2)_



**Where:**



* num1 and num2 should be in decimal format.



**Remarks:**



* `#NUM!` - occurs if num1 or num2 is less than zero, if num1 or num2 is a non-integer or is greater than (2^48)-1.



* `#VALUE!` - occurs if num1 or num2 is a non-numeric value.



## BITRSHIFT



The `BITRSHIFT` function returns a number shifted right by the specified number of bits.



**Syntax:**



_BITRSHIFT(num1,num2)_



**Where:**



* num1 must be an integer greater than or equal to 0.



* Num2 must be an integer.



**Remarks:**



* `#NUM!` - occurs if num1 or num2 is less than zero, if num1 or num2 is a non-integer or is greater than (2^48)-1.



* `#VALUE!` - occurs if num1 or num2 is a non-numeric value.



## BITXOR



The `BITXOR` function returns bitwise `XOR` of two numbers.



**Syntax:**



_BITXOR(num1, num2)_



**Where:**



* num1 and num2 should be in decimal format.



**Remarks:**



* `#NUM!` - occurs if num1 or num2 is less than zero, if num1 or num2 is a non-integer or is greater than (2^48)-1.



* `#VALUE!` - occurs if num1 or num2 is a non-numeric value.



## DEC2BIN



The `DEC2BIN` function converts a decimal number into a binary number.



**Syntax:**



_DEC2BIN(num,places)_ 



**where:**



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



**Remarks:**



* `#NUM!` occurs when number < -512 or if number >511 and when places is zero or negative.



* `#VALUE!` occurs when number  or places is non-numeric and when `DEC2BIN` requires more than the number of characters specified in places.



## DEC2OCT



The `DEC2OCT` function converts a decimal number into an octal number.



**Syntax:**



_DEC2OCT(num, places)_ 



**where:**



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



**Remarks:**



* `#NUM!` occurs when number < -512 or if number >511 and when places is zero or negative.



* `#VALUE!` occurs when the number or places is non-numeric and when DEC2OCT requires more than the number of characters specified in places.



## HEX2BIN



The `HEX2BIN` function converts a hexadecimal number into a binary number. 



**Syntax:**



_HEX2BIN(num, places)_ 



**where:**



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



**Remarks:**



* `#NUM!` occurs when number is not a valid binary number and when places is negative.



* `#VALUE!` occurs when places is non-numeric.



## HEX2OCT



The `HEX2OCT` function converts a hexadecimal number into an octal number. 



**Syntax:**



_HEX2OCT(num, places)_



**where:**



* num is the hexadecimal integer you want to convert. 



* places is the number of characters to use.



**Remarks:**



* `#NUM!` occurs when number is not a valid hexadecimal number and when places is negative.



* `#VALUE!` occurs when places is non-numeric.