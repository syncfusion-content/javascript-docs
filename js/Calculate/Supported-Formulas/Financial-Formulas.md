---
layout: post
title: Supported Formulas of Calculate for Syncfusion Essential JS
description: supported formulas
platform: JS
control: Calculate
documentation: ug
---

# Financial Formulas



## PMT



The `PMT` function calculates the payment for a loan based on constant payments and constant interest rate.



**Syntax:**



_PMT(rate, nper, pv, [fv], [type])_



**Where:**



* rate is the interest rate for the loan.



* nper is the total number of payments for the loan.



* pv is the present value, or the total amount that a series of future payments is worth now.



* fv is the future value, or a cash balance you want to attain after the last payment is made. If Fv is omitted, it is assumed to be zero.



* type is the number 0 or 1 and indicates when payments are due.

  <table>

	<tr>

	<th>

	<b>Set type equal to</b></th><th>

	<b>If payments are due</b></th></tr>

	<tr>

	<td>

	0 or omitted</td><td>

	At the end of the period</td></tr>

	<tr>

	<td>

	1</td><td>

	At the beginning of the period.</td></tr>

  </table>



## PV



Calculates the present value of an investment (i.e. the total amount that a series of future payments is worth now).



**Syntax:**



_PV(rate, nper, pmt, [fv], [type])_



**where:**



* rate is the interest rate per period.



* nper is the total number of payment periods in an annuity.



* pmt is the payment made each period and cannot change over the life of the annuity.



* fv is the future value, or a cash balance you want to attain after the last payment is made.



* type is the number 0 or 1 and indicates when payments are due.