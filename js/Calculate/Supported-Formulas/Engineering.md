---
layout: post
title: Supported Formulas | JS | Calculate | WidowsForms | Syncfusion
description: supported formulas
platform: JS
control: Calculate
documentation: ug
---

# Engineering



## BIN2OCT



The `BIN2OCT` function converts a binary number into an octal number.



**Syntax:**



_BIN2OCT(num, places)_ 



where:



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



## BIN2HEX



The `BIN2HEX` function converts a binary number into a hexadecimal.



**Syntax:**



_BIN2HEX(num places)_ 



where:



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



Remarks:



* &#35;NUM! occurs when number is not a valid binary number, when places is negative.



* &#35;VALUE! occurs when places is non-numeric.



## BIN2DEC



The `BIN2DEC` function converts a binary number into a decimal number.



**Syntax:**



_BIN2DEC(num)_ 



where:



* num is the binary number that you want to convert.



Remarks:



* &#35;NUM! occurs when number is not a valid binary number or when number contains more than 10 characters.



## DEC2BIN



The `DEC2BIN` function converts a decimal number into a binary number.



**Syntax:**



_DEC2BIN(num,places)_ 



where:



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



Remarks:



* &#35;NUM! occurs when number < -512 or if number >511 and when places is zero or negative.



* &#35;VALUE! occurs when number  or places is non-numeric and when `DEC2BIN` requires more than the number of characters specified in places.



## DEC2OCT



The `DEC2OCT` function converts a decimal number into an octal number.



**Syntax:**



_DEC2OCT(num, places)_ 



where:



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



Remarks:



* &#35;NUM! occurs when number < -512 or if number >511 and when places is zero or negative.



* &#35;VALUE! occurs when the number or places is non-numeric and when DEC2OCT requires more than the number of characters specified in places.



## HEX2BIN



The `HEX2BIN` function converts a hexadecimal number into a binary number. 



**Syntax:**



_HEX2BIN(num, places)_ 



where:



* num is the decimal integer you want to convert. 



* places is the number of characters to use.



Remarks:



* &#35;NUM! occurs when number is not a valid binary number and when places is negative.



* &#35;VALUE! occurs when places is non-numeric.



## HEX2OCT



The `HEX2OCT` function converts a hexadecimal number into an octal number. 



**Syntax:**



_HEX2OCT(num, places)_



where:



* num is the hexadecimal integer you want to convert. 



* places is the number of characters to use.



Remarks:



* &#35;NUM! occurs when number is not a valid hexadecimal number and when places is negative.



* &#35;VALUE! occurs when places is non-numeric.