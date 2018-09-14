---
layout: post
title: Pivot Grid Report Item | ReportDesigner | JS | Syncfusion
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

  ![](PivotGrid-Images/Dataset-List.png)

> Note: **AdventureWorks** database is used for demonstration.

* To add a **PivotGrid** data region to the report, drag and drop the pivot grid from the item panel.

   ![](PivotGrid-Images/Grid-Widgets-Pane.png)

    ![](PivotGrid-Images/Grid-Drag.png)

> Note: Header and Footer area doesn't allow to drop the pivot grid report item.

After adding a pivot grid data region to the design surface, click the properties icon in the configuration panel to display the pivot grid properties panel. In the pivot grid `Properties` pane, click the `Data` tab.

Bind column through drag and drop element to `Row(s)`,`Column(s)` and `Values(s)` section from `Measures` and `Dimensions` section.

![](PivotGrid-Images/Grid-AssignData.png)

## Designing a pivot grid

In the pivot grid `Properties` pane, the visual effects of the pivot grid can be designed using the **Properties** tab.

![](PivotGrid-Images/GridItem-Properties2.png)

In the `Properties` pane, to add **Expression** or to open **Advanced** options, click the icon in the right corner of each property.

![](PivotGrid-Images/Grid-Advanced-Option.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

**Name**: Title for the pivot grid report item can be set using this property.

**Basic settings**

![](PivotGrid-Images/Basic-Settings.png)

**Horizontal grid line**: Horizontal grid lines are used to differentiate the rows in the pivot grid. By default the pivot grid appears with horizontal grid lines.

![](PivotGrid-Images/Horizontal-Grid-Line.png)

   * To hide the grid lines, clear the **Horizontal Grid Line** check box.

      ![](PivotGrid-Images/Horizontal-Grid-LineNone.png)

**Vertical grid line**: Vertical grid lines are used to differentiate the columns in the pivot grid. By default the pivot grid appears with vertical grid lines.

 ![](PivotGrid-Images/Vertical-Grid-Line.png)

   * To hide the grid lines, clear the **Vertical Grid Line** check box.

       ![](PivotGrid-Images/Vertical-Grid-LineNone.png)

**Filters**: Click `Set Filters...` in the filters property. It will launch the `Filter Dialog`.

  ![](PivotGrid-Images/Filters-Button.png)

To filter data refer [Filters](/js/ReportDesigner/Compose-Report/Filter-Data).

**Sorting**: In the properties panel, click the **Set Sorts** button to launch sort dialog.

   ![](PivotGrid-Images/Sort-Button.png)

To sort data refer [Sorting](/js/ReportDesigner/Compose-Report/Sort-Data).

**Summary Settings**

* **Summary column style**: Customize the column styles through summary column style property.

  ![](PivotGrid-Images/Summarycolumnstyle.png)

  ![](PivotGrid-Images/Summarycolumn-Preview.png)

  * **Summary Column Border**:

    ![](PivotGrid-Images/Summary-Column-Border.png)

    ![](PivotGrid-Images/Summary-Column-Border-Preview.png)

  * **Choose Summary**: Select the summary type from the **Choose Summary** drop-down list to which you want to set the properties.

    ![](PivotGrid-Images/Choose-Summary.png)

  * **Summary Columns**: Enable the **Enable Summary Column** checkbox, will expand the menu with **Summary Column** option, where the summary of each cell can be edited by clicking the `fx` icon.

       ![](PivotGrid-Images/SummaryColumns.png)

       ![](PivotGrid-Images/SummaryRow-Expression-Dialog.png)

     > Note: Hover the cursor on each row to enable the `Expression` icon.

* **Summary row style**: To enable summary row style properties enable the **Enable summary row** check box.

  ![](PivotGrid-Images/Enable-Summary-Row.png)

  * **Summary row**: To provide the summary details of each cell summary row option can be used.

      ![](PivotGrid-Images/Summary-Row.png)

     * **Summary Row style**: Using the summary style property, the font style, font size,font color, text decoration, text alignment, and padding of the each cell's summary text can be changed.

       ![](PivotGrid-Images/Summary-Row-Style.png)

      > Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

  * **Summary Row Border**:

    ![](PivotGrid-Images/Summary-RowBorder.png)

    ![](PivotGrid-Images/Summary-Row-Border-Preview.png)

   * **Summary Rows**: Enable the **Enable Summary Row** checkbox, will expand the menu with **Summary Rows** option, where the summary of each cell can be edited by clicking the `fx` icon.

       ![](PivotGrid-Images/SummaryRows.png)

**Row Group Settings**: Choose the row group from the **Choose Row Group** drop-down list.

![](PivotGrid-Images/Row-Group-Settings.png)

![](PivotGrid-Images/Row-Group-Properties.png)

* **Format**: The numbers and dates in grid data regions can be formatted by selecting a format from the **Format** dialog.

  ![](PivotGrid-Images/Grid-Format-Field.png)
  
  Click the highlighted button in the above image to open `Format` dialog.

  Refer [Format Data](/js/ReportDesigner/Compose-Report/Format-Data) section for more details on how to format data.

* **Enable Link**: To enable **Action** fields, enable the **Enable Link** checkbox.

  To define a hyperlink, or a drill through action to the pivot grid refer [Link Data](/js/ReportDesigner/Compose-Report/Link-Data).

* **Cell Style**: Using the cell style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column cell can be changed.

  ![](PivotGrid-Images/Cell-Style-Grid.png)

**Row Settings** :  Choose the row number from the drop-down list to customize the specific row appearance.

![](PivotGrid-Images/Row-Settings.png)

![](PivotGrid-Images/Row-Settings-List.png)

* **Height**: Using this property, the `Height` property of the grid `Summary Row` can be adjusted.

    ![](PivotGrid-Images/Row-Settings-Height.png)

**Column Settings**: Choose the column number from the drop-down list to customize the specific column appearance.

![](PivotGrid-Images/Column-Settings.png)

![](PivotGrid-Images/Column-Settings-Properties.png)

 **Width**:  Present more data readable by adjusting the width of the each column using this property.

![](PivotGrid-Images/Width-Pixel-Grid.png)

**Corner Cell Settings**: 

Can be customize the corner cell style, border and caption through this property.

![](PivotGrid-Images/Corner-Cell-Settings.png) 

![](PivotGrid-Images/Corner-Cell-Preview.png)

**Appearance**

In the appearance category, the border style, border width, border color, and background color of the overall grid (Column and Row) can be set to enhance the grid effects.

**Header Style**: Using the header style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column header can be changed.

To apply the above mentioned properties click the icon in the right corner and select `Advanced`.

 ![](PivotGrid-Images/Grid-Header-Style.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

**Cell Style**: Using the cell style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column cell can be changed.

![](PivotGrid-Images/Cell-Style-Grid.png)

**Position**

 The position and size of the pivot grid can be changed using position and size property. The position and size can also be changed using `Resizer`.

![](PivotGrid-Images/Position-Grid.png)

**Miscellaneous** 

![](PivotGrid-Images/Miscellaneous.png)

 * **No Rows Message**: You can configure to display the custom message when data region has no data to display. Type the text that you want to display as a message in NoRowsMessage property field or click icon in the right side to open the expression dialog and create an expression.

    ![](PivotGrid-Images/No-Rows-Message.png)

 * **Keep Together**: You can keep the entire report content of grid in same page without split when enable the keep together property in property panel.

    ![](PivotGrid-Images/Keeptogether.png)

* **Repeat Column Headers**: To display column headers on multiple pages.

    ![](PivotGrid-Images/RepeatColumn.png)

**Visibility** - Select this option to indicate how the report item is initially displayed in the report.

* Enable the checkbox to show the report item.

   ![](PivotGrid-Images/Visibility-Grid.png)

* Disable the checkbox to hide the report item.

   ![](PivotGrid-Images/VisibilityNone-Grid.png)
