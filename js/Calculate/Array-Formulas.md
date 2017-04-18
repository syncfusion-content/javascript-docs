---
layout: post
title: Array Formulas of Calculate for Syncfusion Essential JS
description: array formulas
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# Array Formulas

## Array Formulas

Array formula contains two or more range of values. These array arguments can be cell ranges or array constants. `Eg. ={SUM(A1: A10 * B1:B10)}`.



Each argument must have the same number of cell ranges. The formulas will be defined within `{}` braces. A series of data will be returned from the array formula. 

## Array Constants

A bunch of values or constants which are associated within `{}` braces. Array constants can contain numbers, text, logical values or error strings. `Eg. = { 3, 6, 80; 5, TRUE, FALSE }`



Cell references cannot be included in array constants. Also, equal range of row values should be included. These values will be separated using comma `,`. Different rows are separated using semicolon `;`. 

## Table Formulas

A table is a collection of data about a specific topic that is stored in records rows and columns. These tables are defined with a name and calculate engine supports these table format. `Eg. =SUM(Table1[[#All],[Column1]:[Column2]])`



A table needs to be defined with the following protocols,

  * All table, column, and special item specifiers must be enclosed in matching brackets `[ ]`
  * Expression cannot be used with these brackets. Column headers should be a text strings.
  * The special characters such as comma `,`, colon `:`, period `.`, left bracket `[` , right bracket `]`, pound sign `#`, single quotation mark `'`, double quotation mark `"`, left brace `{`, right brace `}`, dollar sign `$`, caret `^`, ampersand `&`, asterisk `*`, plus sign `+`, equal sign `=`, minus sign `-`, greater than symbol `>`, less than symbol `<`, and division sign `/` can be used.

These table are converted into cell ranges and then it will be evaluated. The data from one record row can also be taken with this table structure.

