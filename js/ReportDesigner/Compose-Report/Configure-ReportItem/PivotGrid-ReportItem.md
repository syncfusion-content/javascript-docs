---
layout: post
title: Rectangle Report Item | ReportDesigner | JS | Syncfusion
description: Draw a Pivot Grid Item
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# PivotGrid

The pivot grid report item allows to visualize the multi-dimensional data.

# To add a PivotGrid to a report

* Create a report and define a dataset. For more information refer [Create Dataset](/javascript-docs/js/ReportDesigner/Create-Data/Create-New-Data).

  ![](images/Dataset-List.png)

> Note: **AdventureWorks** database is used for demonstration.

* To add a **PivotGrid** data region to the report, drag and drop the grid from the item panel.

   ![](PivotGird-Images/PivotGrid-Widgets-Pane.png)

    ![](PivotGird-Images/PivotGrid-Drag.png)

> Note: Header and Footer area doesn't allow to drop the pivot grid report item.

After adding a pivot grid data region to the design surface, click the properties icon in the configuration panel to display the pivot grid properties panel. In the pivot grid `Properties` pane, click the `Data Assign` tab.

Bind column through drag and drop element to `Row(s)`,`Column(s)` and `Values(s)` section from `Measures` and `Dimensions` section.

![](images/PivotGrid-AssignData.png)

## Designing a pivot grid

In the pivot grid `Properties` pane, the visual effects of the pivot grid can be designed using the **Properties** tab.

![](images/PivotGridItem-Properties2.png)

In the `Properties` pane, to add **Expression** or to open **Advanced** options, click the icon in the right corner of each property.

![](images/PivotGrid-Advanced-Option.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/javascript-docs/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

**Name**: Title for the pivot grid report item can be set using this property.

**Basic settings**

![](images/PivotGrid-Basic-Settings.png)

**Horizontal grid line**: Horizontal grid lines are used to differentiate the rows in the pivot grid. By default the pivot grid appears with horizontal grid lines.

![](images/Horizontal-Grid-Line.png)

   * To hide the grid lines, clear the **Horizontal Grid Line** check box.

      ![](images/Horizontal-Grid-LineNone.png)

**Vertical grid line**: Vertical grid lines are used to differentiate the columns in the pivot grid. By default the pivot grid appears with vertical grid lines.

 ![](images/Vertical-Grid-Line.png)

   * To hide the grid lines, clear the **Vertical Grid Line** check box.

       ![](images/Vertical-Grid-LineNone.png)

**Filters**: Filters are used to limit the data in a report after the data is retrieved from a data source. When a filter is added to the pivot grid data, the report will retrieve data that matches the filter conditions.

To add the filter, specify one or more conditions; the conditions are filter equations. A filter equation has an expression that identifies the data has to be filtered, and also identifies the value has to be compared.

### Add filters

 1. Click `Set Filters...` in the filters property. It will launch the `Filter Dialog`, by default the list is empty.

     ![](images/Filters-Button.png)

2. Click **Add**. A new blank filter equation appears.

    ![](images/Filters-Add.png)

3. The first field in the filter is an **Expression** field, type or select an expression for the field to filter.

   * To edit an expression, click on the icon next to the expression field and select `Expression`. 

      ![](images/Expression-Icon.png)
   
      The expression can be set like below.

      ![](images/Expression-Dialog.png)

   * The icon will be indicated in `Black color`, if the expression is applied.

      ![](images/Expression-Black.png)

4. In the **Operator** box, select the operator by which the filter can compare the values in the **Expression** box and the **Value** box.

5. In the **Value** box, type the expression or value against which you want the filter to evaluate the value in **Expression**.

6. Click **OK**.

### Sort data in a pivot grid data region

**Sorts**: A sort expression controls the order in which data appears in a data region.

1. In the properties panel, click the **Set Sorts**.

   ![](images/Sort-Button.png)

2. For each sort expression, follow these steps:

   * Click **Add**.

     ![](images/Sort-Add.png)

   * Type or select an expression by which the data will be sorted.

   * From the drop-down list, choose the sort direction for each expression. **Ascending** sorts an expression in A-Z order. **Descending** sorts an expression in Z-A order.

     ![](images/Sort-Add-Field.png)

3. Click OK.

> Note: For effective sorting experience, apply sorting to the column with string data.

**Summary Settings**

**Row and Column Group Settings**

**Row Settings**

**Column Settings**

**Corner cell Settings**

**No Row Message**

**Apperance**

**Position**: The position and size of the pivot grid can be changed using position and size property. The position and size can also be changed using `Resizer`.

![](images/Position-Pivot-Grid.png)

**Visibility** - Select this option to indicate how the report item is initially displayed in the report.

* Enable the checkbox to show the report item.

   ![](images/Visibility-Pivot-Grid.png)

* Disable the checkbox to hide the report item.

   ![](images/VisibilityNone-Pivot-Grid.png)
