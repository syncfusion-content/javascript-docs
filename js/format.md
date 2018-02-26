---
layout: post
title: Custom Numeric Format Strings in Syncfusion Essential JS Widgets
description: How to use Custom Numeric Format Strings in syncfusion essential js widgets.
platform: js
control: Introduction
documentation: ug
---

# Custom Numeric Format Strings

Create a custom numeric format string that contains one or more custom numeric specifiers. This numeric specifier helps to defines the format of numeric data. This type of format string is not a [`standard numeric format string`](https://docs.microsoft.com/en-us/dotnet/standard/base-types/standard-numeric-format-strings#) and it can be of any format string.
Some of the custom numeric format specifiers are illustrated in the following sections.

## Custom specifier "0"

The Zero-placeholder symbols fills the missing digits in “0” custom specifier. If there is a digit in the formatting values it will be displayed in the result string, otherwise 0 will replaces the digits according to the format string. 

Please find some of the example formats below,

<table>
<tr>
<td>
{{'**Format**'| markdownify }}
</td>
<td>
{{'**Output**'| markdownify }}
</td>
</tr>
<tr>
<td>
ej.format(123, "00000");
</td>
<td>
00123
</td>
</tr>
<tr>
<td>
ej.format(1.2, "00.00");
</td>
<td>
01.20
</td>
</tr>
<tr>
<td>
ej.format(1.2, "0.00");
</td>
<td>
1.20
</td>
</tr>
<tr>
<td>
ej.format(1.2, "00.00", "de-DE")
</td>
<td>
1,20
</td>
</tr>
<tr>
<td>
ej.format(0.56, "0.0")
</td>
<td>
0.6
</td>
</tr>
<tr>
<td>
ej.format(1234567890, "0,0")
</td>
<td>
1,234,567,890
</td>
</tr>
<tr>
<td>
ej.format(1234567890.123456, "0,0.0")
</td>
<td>
1,234,567,890.1
</td>
</tr>
<tr>
<td>
ej.format(1234.567890, "0,0.00")
</td>
<td>
1, 234.57
</td>
</tr>
</table>


## Custom specifier "#"

Formatting values contains digits in the place of “#” symbol in the format string, it will be displayed in the result string. Otherwise none will be placed in the position of result string. 
It never allowed zero unless it is a significant digit in the formatting values.

Please find some of the example formats below,

<table>
<tr>
<td>
{{'**Format**'| markdownify }}
</td>
<td>
{{'**Output**'| markdownify }}
</td>
</tr>
<tr>
<td>
ej.format(1.2, "#.##")
</td>
<td>
1.2
</td>
</tr>
<tr>
<td>
ej.format(123, "#####")
</td>
<td>
123
</td>
</tr>
<tr>
<td>
ej.format(123456, "[##-##-##]")
</td>
<td>
[12-34-56]
</td>
</tr>
<tr>
<td>
ej.format(1234567890, "#")
</td>
<td>
1234567890
</td>
</tr>
<tr>
<td>
ej.format(1234567890, "(###) ###-####")
</td>
<td>
(123) 456-7890
</td>
</tr>
<tr>
<td>
ej.format(0.324, "#.###")
</td>
<td>
0.324
</td>
</tr>
<tr>
<td>
ej.format(123456789, "#,#")
</td>
<td>
123,456,789
</td>
</tr>
</table>


## Custom specifier "Exponential"

The strings such as "E", "E+", "E-", "e", "e+", or "e-" is presents in the format string, then the number is formatted by scientific notation with “E” or “e” inserted in between the number and the exponent.  The number of zeros following the scientific notation indicator regulates the minimum number of digits to the output of the exponent. 
The plus sign or minus sign is always come with the exponent symbol. The following are the formats used in customer specifier “exponential”:
* "E+" and "e+":  a plus sign preceding the exponent.
* "E", "E-", "e", or "e-":  Precede only negative exponents.

Please find some of the example formats below,

<table>
<tr>
<td>
{{'**Format**'| markdownify }}
</td>
<td>
{{'**Output**'| markdownify }}
</td>
</tr>
<tr>
<td>
ej.format(123456, "#.##E+2")
</td>
<td>
1.23e+2
</td>
</tr>
<tr>
<td>
ej.format(123456, "#.##E+002")
</td>
<td>
1.23e+052
</td>
</tr>
<tr>
<td>
ej.format(123456, "#.##E-2")
</td>
<td>
1.23e2
</td>
</tr>
<tr>
<td>
ej.format(123456, "#.##E-002")
</td>
<td>
1.23e052
</td>
</tr>
<tr>
<td>
ej.format(1634.92, "#.##E+4")
</td>
<td>
1.63e+4
</td>
</tr>
<tr>
<td>
ej.format(1634.92, "#.##E+004")
</td>
<td>
1.63e+034
</td>
</tr>
<tr>
<td>
ej.format(1634.92, "#.##E-2")
</td>
<td>
1.63e2
</td>
</tr>
<tr>
<td>
ej.format(1634.92, "#.##E-002")
</td>
<td>
1.63e032
</td>
</tr>
<tr>
<td>
ej.format(86000, "#.##E+000")
</td>
<td>
8.6e+004
</td>
</tr>
</table>


## Custom specifier "Escape"

The symbols "#", "0", ".", ",", “E” in a format string are consider as format specifiers rather than as literal characters. To prevent these characters from being considered as format specifier, precede it with a back slash ”\” that is the escape character.  The escape character highlights that the following character is a character literal and should be included in the result string without any change. To include a backslash in a result string, escape it with another backslash (\\).

Please find some of the example formats below,

<table>
<tr>
<td>
{{'**Format**'| markdownify }}
</td>
<td>
{{'**Output**'| markdownify }}
</td>
</tr>
<tr>
<td>
ej.format(123, "\\#\\#\\ #00")
</td>
<td>
##123
</td>
</tr>
<tr>
<td>
ej.format(123, "\\#\\#\\ ###")
</td>
<td>
##123
</td>
</tr>
<tr>
<td>
ej.format(123, "\\#\\#\\ 000")
</td>
<td>
##123
</td>
</tr>
<tr>
<td>
ej.format(123, "\\0\\0 000")
</td>
<td>
00123
</td>
</tr>
<tr>
<td>
ej.format(12345, "\\#\\#\\ 0,0")
</td>
<td>
##12,345
</td>
</tr>
<tr>
<td>
ej.format(12345, "\\0\\0 #,#")
</td>
<td>
0012,345
</td>
</tr>
</table>
