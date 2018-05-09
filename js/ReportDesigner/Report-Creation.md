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

 ![](images/Datasource-Start.png)

Click the `Add DataSet` button in `Data` panel.

![](images/Dataset-CreateWizard.png)

Click `Create New` in the context menu, it will launch connection type panel. In the connection type panel, click on the data source type that you want to connect. Here, `SQL` connection type is used to demonstrate.

 ![](images/SQL-Connect.png)

In the new data source configuration panel, fill the server name and related details. 

![](images/Datasource-CreateWizard.png)

Click the `Connect` button. Now the following view will be displayed.

![](images/Dataset-DesignView.png)

You can enter the query directly in the Query Editor or use the Query Designer to interactively build the query and view the result of the query. Here, the data is created with the help of the Query Designer.

1. Build query using the Query Editor.

   * To switch over to Query Editor, click the switcher icon in the designer toolbar.

      ![Enter the query directly with Query Editor](images/Switcher-Editor.png)

      ![](images/Editor-View.png)

2. Build query using the Query Designer.

   The left pane holds the tables and views associated with the connected database. Drag your preferred table or view from the left pane and drop into the center pane labeled with `Drag and Drop table here` like below:

   ![](images/Drag-Action.png)

   ![](images/Dataset-Drag-DropTable.png)

The dropped tables will be tick marked before the name of table in the left pane like below:

![](images/Table-Tick.png)

The primary key defined in the connected database table will be marked like below:

![](images/PrimaryKey.png)

The data type of the each column is represented with visual icons as shown below:

![](images/Datatype-Icon.png)

Add more than one table by following the same drag and drop procedure as mentioned in above steps, if required.

To rename columns refer [Rename Columns](/report-platform/reportdesigner/web/transforming-data/rename-column).

You can filter specific data out of huge database by using [Data Filters](/report-platform/reportdesigner/web/transforming-data/configure-data-filters).

> Note: At present, you can experience full fledged query design for **SQL** datasource only.

### Execute query

You can visualize the data by using `Execute` option from the tools pane in data design view.

![](images/Execute-Query.png)

Now the data will be retrieved based on the specified query.

![](Images/Execute-Preview.png)

Click the `Finish` button in the tools pane to add the data with the report.

![](Images/Dataset-Designer-Finish.png)

Now, the table fields will be listed in `Data` panel like below.

![](images/Report-Designer-DesignView.png)

## Adding a report item to design view

The item panel at left consists of Basic Items, Data Visualization, Data Regions and SubReport
that you can utilize to design a report.

![](images/Widgets-Pane.png)

You can `drag and drop` report items into the `Header`, `Footer`, and `Design` area.

> Note: You can only drag and drop `Basic Items` category into the `Header` and `Footer` area.

### Enable header and footer

You can enable and disable header/footer by clicking the below icons from the designer toolbar pane.

![](images/Header.png)

![](images/Footer.png)

Click and drag the preferable report item from the toolbox by holding the mouse left button and drop into the design panel like below:

![](images/Chart-Drag.png)

![](images/Widgets-Sample.png)

After you drop the report item, you can resize it by placing the focus over the report item and dragging its corner like below, if required.

![](images/Resize-ChartWidget.png)

## Assigning data to report item

> Note: This step is applicable only for report items other than basic items category.

To bind the data to a report item that is placed in the design area, focus on that report item.

![](images/Focus-Widget.png)

Click the `Properties` icon in the configuration panel.

![](images/Properties-Icon.png)

Now, the report item properties panel displayed like below:

![](images/Properties-Window.png)

Click the `Data Assign` tab in the properties panel. Now, the data assign tab switches like below:

![](images/DataAssign-Window.png)

Data assign panel shows the data configuration view. The numeric columns are listed under the `Measures` section; other type columns are listed under the `Dimensions` section.

![](images/Measures-Dimensions.png)

Select and drag the numeric column (measure element) from the `Measures` section that you want to visualize the data and drop into the `Y Value(s)` section.

![](images/Gripper-AssignData.png)

Now, the report item preview will look like below:

![](images/ColumnChart-DataAssign1.png)

Click the `Settings` icon (highlighted below) to open the aggregation type drop-down list.

![](images/Settings-Icon.png)

You can set the aggregation type by which you can compute the selected column.

![](images/Aggregation-Type.png)

Select and drag the dimension element from the `Dimensions` section to measure against any of the selected numeric column(s) in `Y Value(s)` section, and drop into the `Column(s)` section.  

![](images/DragColumn-Section.png)

Now, the report item preview will look like below:

![](images/Column-Chart2.png)

To group the added column element with another column, add the respective dimension element into Row(s) section.

![](images/Row-DragColumn.png)

Now, the report item design will look like below.

![](images/Column-Chart3.png)

To filter the data from getting bounded to report item, apply filters to the selected measure type or dimension type column(s).

## Configuring report item

> Note: This step is applicable only for report items other than basic items category.

Navigate to the properties pane in the properties tab.

![](images/PropertiesTab-Chart.png)

This pane holds some general settings and some specific settings to the report item. 

You can add more report items by following the above procedure.

## Preview report

Preview the changes made in the report item by clicking the `Preview` in the top-right corner of the Report Server menu.

![](images/Preview-Button.png)

Now, the report preview can be visualized through the built-in report viewer like below:

![](images/Preview-Data.png)

To launch design area, click the `Design` button  in the top-right corner of the Report Server menu.

![](images/Close-Preview.png)

### Save report

To **Save** report refer [Save Report](open-save-report).
