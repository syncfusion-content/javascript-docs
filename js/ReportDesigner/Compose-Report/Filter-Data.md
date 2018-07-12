---
layout: post
title: Filter Data | ReportDesigner | JS | Syncfusion
description: Filter a Data
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Filters

Filters are used to limit the data in a report after the data is retrieved from a data source. When a filter is added to the grid data, the report will retrieve data that matches the filter conditions.

![](Filter-Data-Images/Filters-Dialog.png)

To add the filter, specify one or more conditions; the conditions are filter equations. A filter equation has an expression that identifies the data to be filtered and also identifies the value to be compared.

## Add filters

1. Click **Add**. A new blank filter equation appears.

   ![](Filter-Data-Images/Filters-Add.png)

2. The first drop-down list is an **Expression** field which contains the fields of the specific table, choose field from that drop-down list or create an expression to filter.

   ![](Filter-Data-Images/Expression-Field.png)

3. To edit/create an expression, click on the square icon next to the expression field and select `Expression`. 

   ![](Filter-Data-Images/Expression-Icon.png)
   
   The expression can be set like below.

   ![](Filter-Data-Images/Expression-Dialog.png)

   The icon will be filled with `Black color`, if the expression is applied.

   ![](Filter-Data-Images/Expression-Black.png)

4. In the **Operator** box, select the operator to compare the values in the **Expression** box and the **Value** box.

   ![](Filter-Data-Images/Operators.png)

   To filter specific range of data use **Between** operator.

   ![](Filter-Data-Images/Between-Operator.png)

4. In the **Value** box, edit/create an expression using icon next to this field and following step 3 instructions or type value directly.

5. Follow steps 1 - 4, to add multiple filters.

   ![](Filter-Data-Images/Multiple-Filters.png)

6. Click **OK**.

## Remove Filters

Remove a filter condition by clicking the close icon placed at left of the respective filter.

![](Filter-Data-Images/Delete-Filter.png)