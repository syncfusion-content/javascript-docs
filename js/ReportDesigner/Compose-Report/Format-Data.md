---
layout: post
title: Format Data | ReportDesigner | JS | Syncfusion
description: How to format data to present in better way.
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Format 

Format numbers and dates in data regions by selecting a format from the corresponding report item `Properties`.

![](Format-Data-Images/FormatDialog.png)

> Note: To enable disabled fields, enable the checkbox in the left side of the each field.

## Numbers

This type chosen to display numbers in general format. It does not change the field value, only its representation.

Number type has following options to select:

 * **Decimal Places**: In this field, specify the number of decimal places.

 * **Negative Values** : In this field, specify the representation of negative numbers.

 * **Representation**: In this field, specify the value representation in Thousands, Millions, or Billions to display numbers using financial formats.

 * **Thousand Separator**: In this field, specify the separator for represented value.

   ![](Format-Data-Images/Numbers.png)

 * **Use Regional Formatting**: Enable/Disable this option to apply default local culture settings to the field value and the above formatting options for number will be disable on enabling regional formatting.

   ![](Format-Data-Images/Regional-Option.png)

## Currency

This type chosen to display currency values in general format. It does not change the field value, only its representation.

Currency type has following options to select:

 * **Decimal Places**: In this field, specify the number of decimal places.

 * **Negative Values** : In this field, specify the representation of negative numbers.

 * **Representation**: In this field, specify the value representation in Thousands, Millions, or Billions to display currency values using financial formats.

 * **Thousand Separator**: In this field, specify the separator for represented value.

   For example, if the field value is 1,789,905,394 and you select Billions and specify 2 decimal places, the value displayed in the report is `1.78`.

 * **Currency Culture**: In this field, specify the prefix with currency symbol for financial format value based on the selected culture.

   For example, if the field value is 1,789,905,394 and you select currency culture as `English(Zimbabwe)`, the value displayed in the report is `US$1,789,905,394`.

 * **Include Space**: Enable/Disable this option to include space between currency culture code and value.

   For example, if the field value is 1,789,905,394 and you select currency culture as `English(Zimbabwe)` and if include space checkbox is enabled, the value displayed in the report is `US$ 1,789,905,394`.

 ![](Format-Data-Images/Currency.png)

## Date

This type chosen to providing options for handling a number in date and time format to display as a date value. The list of available date formats will be listed under the date field dropdown list.

![](Format-Data-Images/Date.png)

## Time

This type chosen to providing options for handling a number in date and time format to display as a time value. The list of available time formats will be listed under the time field dropdown list.

![](Format-Data-Images/Time.png)

## Scientific

This type chosen to display numbers in scientific notation. The number is transformed into a real number followed by E+n, where E (which stands for Exponent) multiplies the real number by 10 to the nth power. 

![](Format-Data-Images/Scientific.png)

For example, a 2-decimal scientific format displays 12345678901 as 1.23E+10, which is 1.23 times 10 to the 10th power.

## Percentage

This type chosen to display the percentage value by multiplying the value by 100 and appending percent (%) symbol. 

Percentage type has following options to select:

 * **Decimal Places**: In this field, specify the number of decimal places.

 * **Include Space**: Enable/Disable this option to include space between percentage and value.

![](Format-Data-Images/Percentage.png)

## Custom

This type allows modifying any of the predefined formats and create a new custom number format.

![](Format-Data-Images/Custom.png)
