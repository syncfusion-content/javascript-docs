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

To add the filter, specify one or more conditions; the conditions are filter equations. A filter equation has an expression that identifies the data has to be filtered, and also identifies the value has to be compared.

## Add filters

1. Click **Add**. A new blank filter equation appears.

    ![](Filter-Data-Images/Filters-Add.png)

2. The first field in the filter is an **Expression** field, type or select an expression for the field to filter. The fields of the specific table will be listed in the drop-down list like below.

    ![](Filter-Data-Images/Expression-Field.png)

   * To edit an expression, click on the icon next to the expression field and select `Expression`. 

      ![](Filter-Data-Images/Expression-Icon.png)
   
      The expression can be set like below.

      ![](Filter-Data-Images/Expression-Dialog.png)

   * The icon will be indicated in `Black color`, if the expression is applied.

      ![](Filter-Data-Images/Expression-Black.png)

3. In the **Operator** box, select the operator by which the filter can compare the values in the **Expression** box and the **Value** box.

    ![](Filter-Data-Images/Operators.png)

    To filter specific range of data use **Between** operator.

    ![](Filter-Data-Images/Between-Operator.png)

4. In the **Value** box, type the expression or value against which you want the filter to evaluate the value in **Expression**.

5. You can **Add** multiple filters by clicking the `ADD`.

    ![](Filter-Data-Images/Multiple-Filters.png)

6. Click **OK**.

### Remove Filters

Remove a filter condition by clicking the close icon at left of the respective filter.

![](Filter-Data-Images/Delete-Filter.png)