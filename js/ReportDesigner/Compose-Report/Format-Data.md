---
layout: post
title: Line Report Item | ReportDesigner | JS | Syncfusion
description: Draw a Line Item
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Format 

Format numbers and dates in data regions by selecting a format from the corresponding report item `Properties`.

![](Format-Data-Images/FormatDialog.png)

To enable disabled fields, enable the checkbox in the left side of the each field.

## Numbers

Used to display numbers in general format, it does not change the field value, only its appearance.

**Decimal Places**: Used to specify the number of decimal places.

**Negative Values** : To specify how negative numbers are displayed.

**Representation**: Used to separate the values in Thousands, Millions, or Billions to display numbers using financial formats.

**Thousand Separator**: A comma separator, used to separate the values based on the **Representation**.

![](Format-Data-Images/Numbers.png)

**Use Regional Formatting**: Default local culture settings will be applied to the field value.

![](Format-Data-Images/Regional-Option.png)

## Currency

**Decimal Places**: Used to specify the number of decimal places.

**Negative Values** : To specify how negative numbers are displayed.

**Representation**: Used to separate the values in Thousands, Millions, or Billions to display numbers using financial formats.

**Thousand Separator**: Used to separate the values based on the **Representation** format.

For example, if the field value is 1,789,905,394 and you select Billions and specify 2 decimal places, the value displayed in the report is `1.78`.

**Currency Culture**: Displays the financial format value prefixed with the currency symbol based on the selected culture.

For example, if the field value is 1,789,905,394 and you select currency culture as `English(Zimbabwe)`, the value displayed in the report is `US$1,789,905,394`.

**Include Space**: Used to include space between currency culture code and value.

For example, if the field value is 1,789,905,394 and you select currency culture as `English(Zimbabwe)` and if include space checkbox is enabled, the value displayed in the report is `US$ 1,789,905,394`.

 ![](Format-Data-Images/Currency.png)

In the preview pane the field value will be previewed based on the decimal places, currency culture, thousand separator, include space properties.

## Date

Used to handle a number as date and time serial number and displays it as a date value. The list of available date formats will be listed under the date field dropdown list.

![](Format-Data-Images/Date.png)

## Time

Used to handle a number as date and time serial number and displays it as a time value. The list of available time formats will be listed under the time field dropdown list.

![](Format-Data-Images/Time.png)

## Scientific

Used to display numbers in scientific notation. The number is transformed into a real number followed by E+n, where E (which stands for Exponent) multiplies the real number by 10 to the nth power. 

![](Format-Data-Images/Scientific.png)

For example, a 2-decimal scientific format displays 12345678901 as 1.23E+10, which is 1.23 times 10 to the 10th power.

## Percentage

Displays the cell value multiplied by 100 and followed by a percent (%) symbol. The format specifies the number of decimal places used.

![](Format-Data-Images/Percentage.png)

## Custom

Allows modifying any of the predefined formats and creating a new custom number format.

![](Format-Data-Images/Custom.png)

 To set custom format, enter the format in the text field.
