---
layout: post
title: Report Creation with Syncfusion Web Report Designer
description: How to start the report creation with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Report Creation

This is a simple steps to create a report with Web Report Designer application. An AdventureWorks and Northwind database is used to demonstrate each of the features in the Web Report Designer.

## Connecting to data

Add a new data source by establishing a data connection with any of the supported data connection types like below:

### Setting up connection

RDL dataset contains the information that is needed to retrieve a specific set of data from a data source.

Click the `Data` icon in the configuration panel to launch a `Data` configuration.

 ![](Report-Creation-Images/Datasource-Start.png)

Click the `Add DataSet` button in `Data` panel.

![](Report-Creation-Images/Dataset-CreateWizard.png)

Click `Create New` in the context menu, it will launch connection type panel. In the connection type panel, click on the data source type that you want to connect. Here, `SQL` connection type is used to demonstrate.

 ![](Report-Creation-Images/SQL-Connect.png)

In the new data source configuration panel, fill the server name and related details. 

![](Report-Creation-Images/Datasource-CreateWizard.png)

Click the `Connect` button. Now the following view will be displayed.

![](Report-Creation-Images/Dataset-DesignView.png)

You can enter the query directly in the Query Editor or use the Query Designer to interactively build the query and view the result of the query. Here, the data is created with the help of the Query Designer.

1. Build query using the Query Editor.

   * To switch over to Query Editor, click the switcher icon in the designer toolbar.

      ![Enter the query directly with Query Editor](Report-Creation-Images/Switcher-Editor.png)

      ![](Report-Creation-Images/Editor-View.png)

2. Build query using the Query Designer.

   The left pane holds the tables and views associated with the connected database. Drag your preferred table or view from the left pane and drop into the center pane labeled with `Drag and Drop table here` like below:

   ![](Report-Creation-Images/Drag-Action.png)

   ![](Report-Creation-Images/Dataset-Drag-DropTable.png)

The dropped tables will be tick marked before the name of table in the left pane like below:

![](Report-Creation-Images/Table-Tick.png)

The primary key defined in the connected database table will be marked like below:

![](Report-Creation-Images/PrimaryKey.png)

The data type of the each column is represented with visual icons as shown below:

![](Report-Creation-Images/Datatype-Icon.png)

Add more than one table by following the same drag and drop procedure as mentioned in above steps, if required.

To rename columns refer [Rename Columns](/js/ReportDesigner/transforming-data/rename-column).

You can filter specific data out of huge database by using [Data Filters](/js/ReportDesigner/transforming-data/configure-data-filters).

> Note: At present, you can experience full fledged query design for **SQL** datasource only.

### Execute query

You can visualize the data by using `Execute` option from the tools pane in data design view.

![](Report-Creation-Images/Execute-Query.png)

Now the data will be retrieved based on the specified query.

![](Report-Creation-Images/Execute-Preview.png)

Click the `Finish` button in the tools pane to add the data with the report.

![](Report-Creation-Images/Dataset-Designer-Finish.png)

Now, the table fields will be listed in `Data` panel like below.

![](Report-Creation-Images/Report-Designer-DesignView.png)

## Adding a report item to design view

The item panel at left consists of Basic Items, Data Visualization, Data Regions and SubReport
that you can utilize to design a report.

![](Report-Creation-Images/Widgets-Pane.png)

You can `drag and drop` report items into the `Header`, `Footer`, and `Design` area.

> Note: You can only drag and drop `Basic Items` category into the `Header` and `Footer` area.

### Enable header and footer

You can enable and disable header/footer by clicking the below icons from the designer toolbar pane.

![](Report-Creation-Images/Header.png)

![](Report-Creation-Images/Footer.png)

Click and drag the preferable report item from the toolbox by holding the mouse left button and drop into the design panel like below:

![](Report-Creation-Images/Chart-Drag.png)

![](Report-Creation-Images/Widgets-Sample.png)

After you drop the report item, you can resize it by placing the focus over the report item and dragging its corner like below, if required.

![](Report-Creation-Images/Resize-ChartWidget.png)

## Assigning data to report item

> Note: This step is applicable only for report items other than basic items category.

To bind the data to a report item that is placed in the design area, focus on that report item.

![](Report-Creation-Images/Focus-Widget.png)

Click the `Properties` icon in the configuration panel.

![](Report-Creation-Images/Properties-Icon.png)

Now, the report item properties panel displayed like below:

![](Report-Creation-Images/Properties-Window.png)

Click the `Data Assign` tab in the properties panel. Now, the data assign tab switches like below:

![](Report-Creation-Images/DataAssign-Window.png)

Data assign panel shows the data configuration view. The numeric columns are listed under the `Measures` section; other type columns are listed under the `Dimensions` section.

![](Report-Creation-Images/Measures-Dimensions.png)

Select and drag the numeric column (measure element) from the `Measures` section that you want to visualize the data and drop into the `Y Value(s)` section.

![](Report-creation-Images/ColumnChart-DataAssign1.png)

Now, the report item preview will look like below:

![](Report-Creation-Images/Gripper-AssignData.png)

Click the `Settings` icon (highlighted below) to open the aggregation type drop-down list.

![](Report-Creation-Images/Settings-Icon.png)

You can set the aggregation type by which you can compute the selected column.

![](Report-Creation-Images/Aggregation-Type.png)

Select and drag the dimension element from the `Dimensions` section to measure against any of the selected numeric column(s) in `Y Value(s)` section, and drop into the `Column(s)` section.  

![](Report-Creation-Images/DragColumn-Section.png)

Now, the report item preview will look like below:

![](Report-Creation-Images/Column-Chart2.png)

To group the added column element with another column, add the respective dimension element into Row(s) section.

![](Report-Creation-Images/Row-DragColumn.png)

Now, the report item design will look like below.

![](Report-Creation-Images/Column-Chart3.png)

To filter the data from getting bounded to report item, apply filters to the selected measure type or dimension type column(s).

## Configuring report item

> Note: This step is applicable only for report items other than basic items category.

Navigate to the properties pane in the properties tab.

![](Report-Creation-Images/PropertiesTab-Chart.png)

This pane holds some general settings and some specific settings to the report item. 

You can add more report items by following the above procedure.

## Preview report

To **Preview** report refer [Preview Report](/js/ReportDesigner/Working-with-Report/Preview-report).

### Save report

To **Save** report refer [Save Report](/js/ReportDesigner/Working-with-Report/save-report).
