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

This section describes simple steps to create a report with Web Report Designer control. An AdventureWorks and Northwind database is used to demonstrate each of the features in the Web Report Designer.

## Connecting to data

Add a new data source by establishing a data connection with any of the supported data connection types like below:

### Setting up connection

Please find the steps below to set up connection for creating a RDL Dataset which will contains the information needed to retrieve a specific set of data from a data source,

1. Click the `Data` icon in the configuration panel to launch a `Data` configuration.

   ![](Report-Creation-Images/Datasource-Start.png)

2. Next, click the `Add DataSet` button in `Data` panel.

   ![](Report-Creation-Images/Dataset-CreateWizard.png)

3. Then, click `Create New` in the context menu, it will launch connection type panel. In the connection type panel, click on the data source type that you want to connect. Here, `SQL` connection type is used to demonstrate.

   ![](Report-Creation-Images/SQL-Connect.png)

   In the new data source configuration panel, fill the server name and related details. 

   ![](Report-Creation-Images/Datasource-CreateWizard.png)

4. Click the `Connect` button. Now the following view will be displayed.

   ![](Report-Creation-Images/Dataset-DesignView.png)

You can enter the query directly in the Query Editor or use the Query Designer to build the query interactively and view the result of the query. Here, the data is created with the help of the Query Designer.

#### Build query using the Query Designer.

The left pane holds the tables and views associated with the connected database. Drag your preferred table or view from the left pane and drop into the center pane labeled with `Drag and Drop table here` like below:

![](Report-Creation-Images/Drag-Action.png)

![](Report-Creation-Images/Dataset-Drag-DropTable.png)

After dropping the table, you can find below changes in UI:

* The dropped table name will be pre-appended with tick mark in the left pane to indicate the specific table is in use like below:

  ![](Report-Creation-Images/Table-Tick.png)

* The primary key defined in the connected database table will be marked like below:

  ![](Report-Creation-Images/PrimaryKey.png)

* The data type of the each column is represented with visual icons as shown below:

  ![](Report-Creation-Images/Datatype-Icon.png)

Add more than one table by following the same drag and drop procedure as mentioned in above steps, if required.

You can find more configuration options for dropped table such as,

* Renaming column options. For detailed information, refer [Rename Columns](/js/ReportDesigner/transforming-data/rename-column).

* Filtering out specific data from huge database by using [Data Filters](/js/ReportDesigner/transforming-data/configure-data-filters).

> Note: At present, you can experience full fledged query design for **SQL** data connection only.

#### Build query using the Query Editor.

To switch over to Query Editor, click the switcher icon in the designer toolbar.

![Enter the query directly with Query Editor](Report-Creation-Images/Switcher-Editor.png)

![](Report-Creation-Images/Editor-View.png)

### Execute query

You can visualize the data by using `Execute` option from the tools pane in data design view.

![](Report-Creation-Images/Execute-Query.png)

Now the data will be retrieved based on the specified query.

![](Report-Creation-Images/Execute-Preview.png)

### Save Data

Click the `Finish` button in the tools pane to add the data with the report.

![](Report-Creation-Images/Dataset-Designer-Finish.png)

Now, the table fields will be listed in `Data` panel like below.

![](Report-Creation-Images/Report-Designer-DesignView.png)

## Adding a report item to design view

The item panel in left pane consists of Basic Items, Data Visualization, Data Regions and SubReport that you can utilize to design a report.

![](Report-Creation-Images/Widgets-Pane.png)

You can `drag and drop` report items into the `Header`, `Footer`, and `Body` of design area.

> Note: You can only drag and drop `Basic Items` category into the `Header` and `Footer` area.

### Enable header and footer

You can enable and disable header/footer by clicking the below icons from the designer toolbar pane.

![](Report-Creation-Images/Header.png)

![](Report-Creation-Images/Footer.png)

### Drag Drop Items

Click and drag the preferable report item from the item panel by holding the mouse left button and drop into the design panel like below:

![](Report-Creation-Images/Chart-Drag.png)

![](Report-Creation-Images/Widgets-Sample.png)

#### Resize Item

You can resize the dropped report item by placing the focus over the report item and dragging its corner like below, if required.

![](Report-Creation-Images/Resize-ChartWidget.png)

#### Move Item

You can move the dropped report item by clicking and dragging the move icon placed at top corner of selected report item like below, if required.

![](Report-Creation-Images/Move-ChartWidget.png)

## Assigning data to report item

> Note: This step is applicable only for data visualization items like charts and grids.

To bind the data to a report item that is placed in the design area, focus on that report item.

![](Report-Creation-Images/Focus-Widget.png)

1. Click the `Properties` icon in the configuration panel.

   ![](Report-Creation-Images/Properties-Icon.png)

   Now, the report item properties panel displayed like below:

   ![](Report-Creation-Images/Properties-Window.png)

2. Click the `Data` tab in the properties panel. Now, the data assign tab switches like below:

   ![](Report-Creation-Images/DataAssign-Window.png)

Data assign panel shows the data configuration view. The numeric columns are listed under the `Measures` section; other type columns are listed under the `Dimensions` section.

![](Report-Creation-Images/Measures-Dimensions.png)

### Data Assign Options

1. **Drag Drop Measure Element**

   Select and drag the numeric column (measure element) from the `Measures` section that you want to visualize the data and drop into the `Y Value(s)` section.

   ![](Report-creation-Images/ColumnChart-DataAssign1.png)

   Now, the report item preview will look like below:

   ![](Report-Creation-Images/Gripper-AssignData.png)

2. **Aggregate Options**:

   Click the `Settings` icon (highlighted below) to open the aggregation type drop-down list.

   ![](Report-Creation-Images/Settings-Icon.png)

   You can set the aggregation type by which you can compute the selected column.

   ![](Report-Creation-Images/Aggregation-Type.png)

3. **Drag Drop Dimension Element**:

   Select and drag the dimension element from the `Dimensions` section to measure against any of the selected numeric column(s) in `Y Value(s)` section, and drop into the `Column(s)` section.  

   ![](Report-Creation-Images/DragColumn-Section.png)

   Now, the report item preview will look like below:

   ![](Report-Creation-Images/Column-Chart2.png)

4. **Grouping**:

   You can group the added column element with another column, by adding the respective dimension element into Row(s) section.

   ![](Report-Creation-Images/Row-DragColumn.png)

   Now, the report item design will look like below.

   ![](Report-Creation-Images/Column-Chart3.png)

5. **Filtering**:

   You can filter the data from getting bounded to report item, by applying filters to the selected measure type or dimension type columns.

## Configuring report item

Navigate to the properties pane in the properties tab.

![](Report-Creation-Images/PropertiesTab-Chart.png)

This pane holds some general settings and some specific configuration settings to the report item. 

> Note: You can add more report items by following the above procedure.

## Preview report

To **Preview** report refer [Preview Report](/js/ReportDesigner/Working-with-Report/Preview-report).

### Save report

To **Save** report refer [Save Report](/js/ReportDesigner/Working-with-Report/save-report).
