---
layout: post
title: Import Shared Datasource with Syncfusion Web Report Designer
description: How to import a shared data source with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Shared DataSource

A shared datasource contains the reference of an existing datasources in the ReportServer. It provides an easy way to manage data source properties in ReportServer.

## Import Shared DataSource into Web Designer

This section explains, how to import a Shared Data Source from the server.

1. Click the `Data` icon in the configuration panel to launch a `Data` configuration.

   ![](Linking-Shared-DTSource-Images/Datasource-Start.png)

2. To import shared data source, switch over to data source panel using the switcher icon on the top-right corner of the `Data` configuration panel.

   ![](Linking-Shared-DTSource-Images/Switcher-Datasource.png)

3. In the context menu, click `Datasources` to launch the `DataSources` configuration panel.

   ![](Linking-Shared-DTSource-Images/Datasource-New-Panel.png)

4. In the `DataSources` configuration panel, click the `New DataSource` button. In the connection type panel, choose the `Shared` data source type.

   ![](Linking-Shared-DTSource-Images/Shared-Datasource-Connect.png)

5. After choosing  the `Shared Datasource`, the new connection wizard will be shown as below:

   ![](Linking-Shared-DTSource-Images/Shared-Datasource-CreateWizard.png)

6. In **Name** field, specify the data source name without special characters.
 
7. In **Shared DataSource** field, you can select an existing shared data sources in the server from the drop-down list.

8. Finally, click `Save` button in the `New Connection` panel.

   Now, a new shared data source will be added in the report like below. 

   ![](Linking-Shared-DTSource-Images/Select-SharedDS.png)

   > Note: You can import multiple shared data sources in the report.
