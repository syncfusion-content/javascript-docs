---
layout: post
title: Grid Report Item in JavaScript Report Designer Control | Syncfusion
description: Learn here all about Grid Report Item support in Syncfusion Essential JavaScript Report Designer, its elements, and more.
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Grid Report Item in JavaScript Report Designer

The grid data region report item displays report data in cells that are organized into rows and columns. Report data can be a data which is retrieved from the data source.

# To add a grid to a report

* Create a report and define a dataset. For more information refer [Create Dataset](/js/ReportDesigner/Create-Data/Create-New-Data).

  ![Dateset List in JavaScript Report Designer](Grid-Images/Dataset-List.png)

> Note: **AdventureWorks** database is used for demonstration.

* To add a **Grid** data region to the report, drag and drop the grid from the item panel.

   ![Grid Widgets Pane in JavaScript Report Designer](Grid-Images/Grid-Widgets-Pane.png)

    ![Grid Drag in JavaScript Report Designer](Grid-Images/Grid-Drag.png)

After adding a grid data region to the design surface, click the properties icon in the configuration panel to display the grid properties panel. In the grid `Properties` pane, click the `Data` tab.

Bind column through drag and drop element from `Measures` section to `Column(s)` section.

![Grid Assign Data in JavaScript Report Designer](Grid-Images/Grid-AssignData.png)

Multiple columns can be binded to the columns section.

![Grid Item Properties in JavaScript Report Designer](Grid-Images/GridItem-Properties.png)

## Designing a grid

In the grid `Properties` pane, the visual effects of the grid can be designed using the **Properties** tab.

![Designing Grid in in JavaScript Report Designer](Grid-Images/GridItem-Properties2.png)

In the `Properties` pane, to add **Expression** or to open **Advanced** options, click the icon in the right corner of each property.

![Grid Advanced Option in JavaScript Report Designer](Grid-Images/Grid-Advanced-Option.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

**Name**: Title for the grid report item can be set using this property.

**Basic settings**

![Basic Settings in JavaScript Report Designer](Grid-Images/Basic-Settings.png)

**Horizontal grid line**: Horizontal grid lines are used to differentiate the rows in the grid. By default the grid appears with horizontal grid lines.

![Horizontal Grid Line in JavaScript Report Designer](Grid-Images/Horizontal-Grid-Line.png)

   * To hide the grid lines, clear the **Horizontal Grid Line** check box.

      ![Horizontal Grid Line None in JavaScript Report Designer](Grid-Images/Horizontal-Grid-LineNone.png)

**Vertical grid line**: Vertical grid lines are used to differentiate the columns in the grid. By default the grid appears with vertical grid lines.

 ![Vertical Grid Line in JavaScript Report Designer](Grid-Images/Vertical-Grid-Line.png)

   * To hide the grid lines, clear the **Vertical Grid Line** check box.

       ![Vertical Grid Line None in JavaScript Report Designer](Grid-Images/Vertical-Grid-LineNone.png)

**Filters**: Click `Set Filters...` in the filters property. It will launch the `Filter Dialog`.

  ![Filters in JavaScript Report Designer](Grid-Images/Filters-Button.png)

To filter data refer [Filters](/js/ReportDesigner/Compose-Report/Filter-Data).

**Sorting**

In the properties panel, click the **Set Sorts** button to launch sort dialog.

   ![Sort Button in JavaScript Report Designer](Grid-Images/Sort-Button.png)

To sort data refer [Sorting](/js/ReportDesigner/Compose-Report/Sort-Data).

**Column** and **Row** settings : 

Row and column group headers are created automatically when data assigned to the grid. 

To differentiate each fields from another the visual effects to the column can be added using **Column** and **Row** settings in the properties pane.

![Column Row Fields in JavaScript Report Designer](Grid-Images/Column-Row-Fields.png)

**To set column properties**: Select the column number from the **Choose Column** drop-down list in which the  properties can be edited . Now, the column properties fields will be displayed under column settings.

   ![Column Properties in JavaScript Report Designer](Grid-Images/Column-Properties.png)

   * **Column name**: By default the field is set with the selected column name. You can set the column name of your choice by editing the default name. You can also set expression for the column name field by clicking the expression icon in the right corner of the field.

      ![Grid Column Name in JavaScript Report Designer](Grid-Images/Grid-Column-Name.png)
    
**Format**: The numbers and dates in grid data regions can be formatted by selecting a format from the **Format** dialog.

  ![Grid Format Field in JavaScript Report Designer](Grid-Images/Grid-Format-Field.png)
  
Click the highlighted button in the above image to open `Format` dialog.

To demonstrate an example, here **Currency** format is applied to the `Unit Price` column.

  ![Format Save in JavaScript Report Designer](Grid-Images/Format-Save.png)

Refer [Format Data](/js/ReportDesigner/Compose-Report/Format-Data) section for more details on how to format data.

 **Enable Link**: To define a hyperlink, or a drill through action to the grid refer [Link Data](/js/ReportDesigner/Compose-Report/Link-Data).

![URL Sample in JavaScript Report Designer](Grid-Images/URL-Sample.png)

**Header Style**: Using the header style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column header can be changed.

To apply the above mentioned properties click the icon in the right corner and select `Advanced`.

 ![Grid Header Style in JavaScript Report Designer](Grid-Images/Grid-Header-Style.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

 ![Cell Style Grid Final in JavaScript Report Designer](Grid-Images/Cell-Style-GridFinal.png)

**Cell Style**: Using the cell style property, the font style, font size,font color, text decoration, text alignment, and padding of the each column cell can be changed.

![Cell Style Grid in JavaScript Report Designer](Grid-Images/Cell-Style-Grid.png)

![Header Style Final Grid in JavaScript Report Designer](Grid-Images/Header-Style-FinalGrid.png)

**Width**:  Present more data readable by adjusting the width of the each column using this property.

![Width Pixel Grid in JavaScript Report Designer](Grid-Images/Width-Pixel-Grid.png)

**To set row properties**: Select the row type from the **Choose Row** drop-down list to which you want to set the properties.

  * **Header row**: Using this property, the `Height` property of the grid `Header Row` can be customized.

    ![Row Properties in JavaScript Report Designer](Grid-Images/Row-Properties.png)

    ![Header Row Height in JavaScript Report Designer](Grid-Images/HeaderRow-Height.png)

  * **Data row**: Using this property, the `Height` property of the grid `Data Row` can be customized.

    ![Data Row in JavaScript Report Designer](Grid-Images/DataRow-Grid.png)

    ![Data Row Grid Final in JavaScript Report Designer](Grid-Images/DataRow-GridFinal.png)

  * **Summary row**: To provide the summary details of each cell summary row option can be used.
      
     * **Summary style**: Using the summary style property, the font style, font size,font color, text decoration, text alignment, and padding of the each cell's summary text can be changed.

       ![Summary Style Grid in JavaScript Report Designer](Grid-Images/Summary-Style-Grid.png)

      > Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

     * **Summary Column**: Enable the **Enable Summary Row** checkbox, will expand the menu with **Summary Column** option, where the summary of each cell can be edited by clicking the `fx` icon.
      
       ![Summary Row Grid in JavaScript Report Designer](Grid-Images/SummaryRow-Grid.png)

       ![Summary Row Expression Dialog in JavaScript Report Designer](Grid-Images/SummaryRow-Expression-Dialog.png)

     > Note: Hover the cursor on each row to enable the `Expression` icon.

     * **Height**: Using this property, the `Height` property of the grid `Summary Row` can be adjusted.

        ![Summary Row Height in JavaScript Report Designer](Grid-Images/Summary-Row-Height.png)

        ![Summmary Row Grid Final in JavaScript Report Designer](Grid-Images/SUmmary-Row-GridFinal.png)

**Appearance**

In the appearance category, the border style, border width, border color, and background color of the overall grid (Column and Row) can be set to enhance the grid effects.

![Appearance Property Grid in JavaScript Report Designer](Grid-Images/Appearance-Property-Grid.png)

**Position**: The position and size of the grid can be changed using position and size property. The position and size can also be changed using `Resizer`.

![Position Grid in JavaScript Report Designer](Grid-Images/Position-Grid.png)

**Miscellaneous** 

![Miscellaneous in JavaScript Report Designer](Grid-Images/Miscellaneous.png)

 * **No Rows Message**: You can configure to display the custom message when data region has no data to display. Type the text that you want to display as a message in NoRowsMessage property field or click icon in the right side to open the expression dialog and create an expression.

    ![No Rows Message in JavaScript Report Designer](Grid-Images/No-Rows-Message.png)

 * **Keep Together**: You can keep the entire report content of grid in same page without split when enable the keep together property in property panel.

    ![Keep Together in JavaScript Report Designer](Grid-Images/Keeptogether.png)

* **Repeat Column Headers**: To display column headers on multiple pages.

    ![Report Column in JavaScript Report Designer](Grid-Images/RepeatColumn.png)

**Visibility** - Select this option to indicate how the report item is initially displayed in the report.

* Enable the checkbox to show the report item.

   ![Visibility Grid in in JavaScript Report Designer](Grid-Images/Visibility-Grid.png)

* Disable the checkbox to hide the report item.

   ![Visibility None Grid in JavaScript Report Designer](Grid-Images/VisibilityNone-Grid.png)
