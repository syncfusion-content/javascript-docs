---
layout: post
title: Sort Data | ReportDesigner | JS | Syncfusion
description: Sort a Data
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Sorting

Sorting controls the order in which the data appears in a data region. Sort data in a dataset query, or define a sort expression for a data region or group. 

![](Sort-Data-Images/Sort-Dialog.png)

For each sort expression, follow these steps:

1. Click **Add**.

   ![](Sort-Data-Images/Sort-Add.png)

2. Choose field from the first drop-down list or create an expression to decide the data to be sorted.

3. To edit/create an expression, click on the square icon next to the first drop-down list and select `Expression`. 

   The expression can be set like below.

   ![](Filter-Data-Images/Expression-Dialog.png)

   The icon will be indicated in `Black color`, if the expression is applied.

   ![](Filter-Data-Images/Expression-Black.png)

4. From the second drop-down list, choose the sort direction for each expression. 
   
   * **Ascending** sorts an expression in A-Z order. 

   * **Descending** sorts an expression in Z-A order.

   ![](Sort-Data-Images/Sort-Add-Field.png)

5. Click OK.

> Note: For effective sorting experience, apply sorting to the column with string data.
