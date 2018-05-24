---
layout: post
title: Visualize Data using grid report item with Syncfusion Web Report Designer
description: How to visualize data using grid report item with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Grid Report Item

The grid data region report item displays report data in cells that are organized into rows and columns. Report data can be a data which is retrieved from the data source.

# To add a grid to a report

* Create a report and define a dataset. For more information refer [Create Dataset](/js/ReportDesigner/Create-Data/Create-New-Data).

  ![](images/Dataset-List.png)

> Note: **AdventureWorks** database is used for demonstration.

* To add a **Grid** data region to the report, drag and drop the grid from the item panel.

   ![](images/Grid-Widgets-Pane.png)

    ![](images/Grid-Drag.png)

After adding a grid data region to the design surface, click the properties icon in the configuration panel to display the grid properties panel. In the grid `Properties` pane, click the `Data Assign` tab.

Bind column through drag and drop element from `Measures` section to `Column(s)` section.

![](images/Grid-AssignData.png)

Multiple columns can be binded to the columns section.

![](images/GridItem-Properties.png)

## Designing a grid

In the grid `Properties` pane, the visual effects of the grid can be designed using the **Properties** tab.

![](images/GridItem-Properties2.png)

In the `Properties` pane, to add **Expression** or to open **Advanced** options, click the icon in the right corner of each property.

![](images/Grid-Advanced-Option.png)

> Note: RDL standard windows fonts are not supported in cross platforms. So, you need to load the unsupported [fonts](/js/ReportDesigner/how-to/Load-Unsupported-Fonts) in application level for cross platforms.

**Name**: Title for the grid report item can be set using this property.

**Basic settings**

![](images/Basic-Settings.png)

**Horizontal grid line**: Horizontal grid lines are used to differentiate the rows in the grid. By default the grid appears with horizontal grid lines.

![](images/Horizontal-Grid-Line.png)

   * To hide the grid lines, clear the **Horizontal Grid Line** check box.

      ![](images/Horizontal-Grid-LineNone.png)

**Vertical grid line**: Vertical grid lines are used to differentiate the columns in the grid. By default the grid appears with vertical grid lines.

 ![](images/Vertical-Grid-Line.png)

   * To hide the grid lines, clear the **Vertical Grid Line** check box.

       ![](images/Vertical-Grid-LineNone.png)

**Filters**: Click `Set Filters...` in the filters property. It will launch the `Filter Dialog`.

     ![](images/Filters-Button.png)

To filter data refer [Filters](/js/ReportDesigner/Compose-Report/Filter-Data).

**Sorting**

In the properties panel, click the **Set Sorts** button to launch sort dialog.

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
  
1. Click the highlighted button in the above image to open `Format` dialog.

      ![](images/Format-Dialog.png)

2. To set custom format, enter the format in the text field.

     To demonstrate an example, here **Currency** format is applied to the `Unit Price` column.

     ![](images/Format-UnitPrice.png)

     ![](images/Format-Save.png)
 
 **Enable Link**: To enable **Action** fields, enable the **Enable Link** checkbox.

   ![](images/Enable-Link-Fields.png)

* **Action** - Defines a hyperlink, a bookmark link, or a drill through action.
The action property must contain only one of the following elements: **Hyperlink**, **Drill through**, or **BookmarkLink**. 

### To add a drill through action
  
   1. Select **Report**.

       ![](images/Enable-Link-Reportpath.png)

   2. Click the `Browse` in the report fields and select the report from the list.

      ![](images/Browse-Report-Dialog.png)

      To specify parameters for the drill through report, follow the next step.

   3.  Click the `Set Parameters` in the report fields, it will launch the `Parameters` dialog.

          ![](images/EnableLink-Parameter-Dialog.png)

        * Click **Add**. A new row is added to the parameter grid.

          ![](images/Enable-Link-Add-Row.png)

          * In the **Name** text box, type the name of the report parameter in the drill through report. If the drill through report is in the server, the parameter names are available in the drop-down list.

          * In **Value**, type or select the value to pass to the parameter in the drill through report.
     
          * Values contain an expression that evaluates to a value to pass to the report parameter. The expressions in the value list include the field list for the current report.

            ![](images/Enable-Link-Expression.png)

   4. Click `OK`.

   5. To test the link, run the report and click the report item to which the link is assigned.

      ![](images/Grid-Change-EnableLink.png)

### Add a hyperlink to a URL

Hyperlink can be added to the report item, so that users can able to click the link in the report and open a browser to the URL that you specify.

 1. Select **URL**.

    ![](images/Enable-Link-URL.png)

2. In  **URL** field, type or select a URL or an expression that evaluates to the URL.

    ![](images/Enable-Link-URLGrid.png)

3. To test the link, click **Preview** to preview the report, and then click the report item that you set on this link.

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

**Appearance**

In the appearance category, the border style, border width, border color, and background color of the overall grid (Column and Row) can be set to enhance the grid effects.

![](images/Appearance-Property-Grid.png)

**Position**: The position and size of the grid can be changed using position and size property. The position and size can also be changed using `Resizer`.

![](images/Position-Grid.png)

**Visibility** - Select this option to indicate how the report item is initially displayed in the report.

* Enable the checkbox to show the report item.

   ![](images/Visibility-Grid.png)

* Disable the checkbox to hide the report item.

   ![](images/VisibilityNone-Grid.png)
