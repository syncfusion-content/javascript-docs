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

* Create a report and define a dataset. For more information refer [Create Dataset](/js/ReportDesigner/Create-Data/Create-New-Data).

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

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

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

**Filters**: Click `Set Filters...` in the filters property. It will launch the `Filter Dialog`.

  ![](images/Filters-Button.png)

To filter data refer [Filters](/js/ReportDesigner/Compose-Report/Filter-Data).

**Sorting**: In the properties panel, click the **Set Sorts** button to launch sort dialog.

   ![](images/Sort-Button.png)

To sort data refer [Sorting](/js/ReportDesigner/Compose-Report/Sort-Data).

**Column** and **Row** settings : 

Row and column group headers are created automatically when data assigned to the grid. 

To differentiate each fields from another the visual effects to the column can be added using **Column** and **Row** settings in the properties pane.

![](images/Column-Row-Fields.png)

**To set column properties**: Select the column number from the **Choose Column** drop-down list in which the  properties can be edited . Now, the column properties fields will be displayed under column settings.

   ![](images/Column-Properties.png)

   * **Column name**: By default the field is set with the selected column name. You can set the column name of your choice by editing the default name. You can also set expression for the column name field by clicking the expression icon in the right corner of the field.

      ![](images/Grid-Column-Name.png)
    
**Format**: The numbers and dates in grid data regions can be formatted by selecting a format from the **Format** dialog.

  ![](images/Grid-Format-Field.png)
  
Click the highlighted button in the above image to open `Format` dialog.

To demonstrate an example, here **Currency** format is applied to the `Unit Price` column.

     ![](images/Format-Save.png)

Refer [Format Data](/js/ReportDesigner/Compose-Report/Format-Data) section for more details on how to format data.

 **Enable Link**: To enable **Action** fields, enable the **Enable Link** checkbox.

To define a hyperlink, or a drill through action to the pivot grid refer [Link Data](/js/ReportDesigner/Compose-Report/Link-Data).

![](images/URL-Sample.png)

**Header Style**: Using the header style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column header can be changed.

To apply the above mentioned properties click the icon in the right corner and select `Advanced`.

 ![](images/Grid-Header-Style.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

 ![](images/Cell-Style-GridFinal.png)

**Cell Style**: Using the cell style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column cell can be changed.

![](images/Cell-Style-Grid.png)

![](images/Header-Style-FinalGrid.png)

**Width**:  Present more data readable by adjusting the width of the each column using this property.

![](images/Width-Pixel-Grid.png)

**Summary Settings** : 

**To set row properties**: Select the row type from the **Choose Row** drop-down list to which you want to set the properties.

  * **Header row**: Using this property, the `Height` property of the grid `Header Row` can be customized.

    ![](images/Row-Properties.png)

    ![](images/HeaderRow-Height.png)

  * **Data row**: Using this property, the `Height` property of the grid `Data Row` can be customized.

    ![](images/DataRow-Grid.png)

    ![](images/DataRow-GridFinal.png)

  * **Summary row**: To provide the summary details of each cell summary row option can be used.
      
     * **Summary style**: Using the summary style property, the font style, font size,font color, text decoration, text alignment, and padding of the each cell's summary text can be changed.

       ![](images/Summary-Style-Grid.png)

      > Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

     * **Summary Column**: Enable the **Enable Summary Row** checkbox, will expand the menu with **Summary Column** option, where the summary of each cell can be edited by clicking the `fx` icon.
      
       ![](images/SummaryRow-Grid.png)

       ![](images/SummaryRow-Expression-Dialog.png)

     > Note: Hover the cursor on each row to enable the `Expression` icon.

     * **Height**: Using this property, the `Height` property of the grid `Summary Row` can be adjusted.

        ![](images/Summary-Row-Height.png)

        ![](images/SUmmary-Row-GridFinal.png)

**Row Settings**

 **Width**:  Present more data readable by adjusting the width of the each column using this property.

![](images/Width-Pixel-Grid.png)

**Column Settings**

* **Height**: Using this property, the `Height` property of the grid `Summary Row` can be adjusted.

        ![](images/Summary-Row-Height.png)

        ![](images/SUmmary-Row-GridFinal.png)

**Corner cell Settings**

**Cell Style**: Using the cell style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column cell can be changed.

![](images/Cell-Style-Grid.png)

**No Row Message**

**Appearance**

In the appearance category, the border style, border width, border color, and background color of the overall grid (Column and Row) can be set to enhance the grid effects.

![](images/Appearance-Property-Grid.png)

**Position**: The position and size of the pivot grid can be changed using position and size property. The position and size can also be changed using `Resizer`.

![](images/Position-Pivot-Grid.png)

**Visibility** - Select this option to indicate how the report item is initially displayed in the report.

* Enable the checkbox to show the report item.

   ![](images/Visibility-Pivot-Grid.png)

* Disable the checkbox to hide the report item.

   ![](images/VisibilityNone-Pivot-Grid.png)
