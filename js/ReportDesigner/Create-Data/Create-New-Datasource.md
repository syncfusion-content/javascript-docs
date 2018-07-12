---
layout: post
title: Connecting to new data source with Syncfusion Web Report Designer
description: How to connect a new data source with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# DataSource

The `DataSource` contains the connection properties or reference to an existing datasource in RDL. 

## Add a new DataSource

To bind data to a report item, a minimum of one data source is needed. A data source can be created through the below steps:

1. In the configuration panel, click the `Data` icon to launch a `Data` configuration panel.

   ![](Create-Datasource-Images/Datasource-Start.png)

 2. To create a data source, switch over to the data source panel using the switcher icon on the top-right corner of the `Data` configuration panel.

   ![](Create-Datasource-Images/Switcher-Datasource.png)

3. Click the `DataSources` in context menu, the `DataSource` panel will be loaded.

   ![](Create-Datasource-Images/Datasource-New-Panel.png)

4. In the `DataSources` configuration panel, click the `New DataSource` button. In the connection type panel, choose the data source type that you want to connect. Here, `SQL` connection type is used to demonstrate.

   ![](Create-Datasource-Images/SQL-Connect.png)

   In the new connection configuration panel, 

   * In **Name**, specify the data source name without special characters.

   * In **Server Name**, you need to select existing server in the local network from the drop-down list or specify the specific remote server name like **myserver.domain.com**.

   * In **Authentication Type**, choose `Windows` or `SQL Server` authentication. 
 
   * In **Username** and **Password**, specify the `username` and `password` of the server.

     ![](Create-Datasource-Images/Authentication-sql.png)

   * In **Database name**, choose or enter a existing valid database on the specified server e.g. AdventureWorks.

     ![](Create-Datasource-Images/Datasource-CreateWizard.png)

5. Finally, click `Save` in the `New Connection` panel and the new data source will be added in datasource pane like below.

   ![](Create-Datasource-Images/Datasource-SaveWizard.png)

   Now, the datasource will be added in the report and it is ready to create/use the data. 
