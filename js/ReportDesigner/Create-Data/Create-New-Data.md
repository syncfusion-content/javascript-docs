---
layout: post
title: Connecting to new data source with Syncfusion Web Report Designer
description: How to connect a new data source with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Data

The report data returns the result of an external datasource query value. The report data contains the datasource name, query, fields and parameter details in the report.

## Add data

This section explains, how to create a new `Data`.

Click the `Data` icon in the configuration panel to launch a `Data` configuration.

 ![](Create-Data-Images/Datasource-Start.png)

Click the `Add DataSet` button in `Data` panel.

![](Create-Data-Images/Dataset-CreateWizard.png)

Click `Create New` in the context menu, In the connection type panel, click the data source type that you want to connect. Here, `SQL` connection type is used to demonstrate.

 ![](Create-Data-Images/SQL-Connect.png)

In the new data source configuration panel, fill the server name and related details. 

![](Create-Data-Images/Datasource-CreateWizard.png)

Click the `Connect` button, then the following view will be displayed.

![](Create-Data-Images/Dataset-DesignView.png)

You can set the dataset name of your choice by editing the `Name` field in the query designer toolbar pane.

![](Create-Data-Images/Dataset-Name-Field.png)

To search the table or view from the data collection, you can use the `Search` field in the left pane of the query designer.

![](Create-Data-Images/Search-Tab.png)

The left pane holds the tables and views associated with the connected database.

Drag the preferred table or view from the left pane and drop into the center pane labeled with `Drag and Drop tables here` like below.

![](Create-Data-Images/Drag-Table.png)

After you drop the item into the center pane, it displays like below:

![](Create-Data-Images/Table-Visual.png)

## Visualize multiple table data

You can visualize multiple tables by drag and drop another table into the design pane.

![](Create-Data-Images/Drag-Table2.png)

Now, the `QueryJoiner` dialog will be launched. You can relate the columns as desired. Refer [Joining Tables](/javascript-docs/js/ReportDesigner/transforming-data/joining-tables).

Click the `Finish` button in the tools pane (highlighted below) to add the data with the report.

![](Create-Data-Images/Finish-Dataset.png)

Now, you have successfully created a `Data` with the Web Designer Report. The table fields will be listed in `Data` panel like below.

![](Create-Data-Images/Final-Panel-Dataset.png)
