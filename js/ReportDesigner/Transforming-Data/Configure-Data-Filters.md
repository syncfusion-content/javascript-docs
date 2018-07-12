---
layout: post
title: Configuring Data Filters with Syncfusion Web Report Designer
description: How to configure a data filters with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Data Filters

Data Filters can be used to filter specific data out of huge database based on defined criteria. The data can be filtered by adding and deleting a filter condition. 

Click on the **Data Filter** icon in the query designer toolbar.

![](Data-Filters-Images/QueryFilter-Icon.png)

Now, the data filter dialog will be launched.

![](Data-Filters-Images/Query-Dialog.png)

> Note: The filter icon in the tools pane will be in disabled state, if there is no table found dropped in table design view.

### Adding Data filter

1. Add a filter condition by clicking the `Add` icon in the dialog.

   ![](Data-Filters-Images/Query-Add.png)

   To add a filter, specify one or more filter conditions. A filter equation consists of field name that identifies which field data need to be filtered, an operator, and the value to compare.

2. In **Field** dropdown, select the field to filter.

3. In the **Operator** field, select the operator to compare the values in the **Field** dropdown and the **Value** field. 

4. In the **Value** field, type the value against which the data need to be filtered.

   ![](Data-Filters-Images/Filter-Condition.png)

5. More than one filter condition can be defined by following above steps.

   ![](Data-Filters-Images/Query-FilterMultiple.png)

6. Execute the query. Now, the `OrderID` with data less than or equal to **10295** and `EmployeeID` equal to **8** will be displayed in the preview.

   ![](Data-Filters-Images/Preview-Data.png)

### Removing a filter condition

Remove a filter condition by clicking the `close` icon at left of the respective filter condition.

![](Data-Filters-Images/Close-Icon.png)
