---
layout: post
title: Import Shared Datasource with Syncfusion Web Report Designer
description: How to import a shared data source with Syncfusion Web Report Designer
platform: report-platform
documentation: ug
---

# Shared DataSource

A shared datasource contains the reference of an existing datasources in the ReportServer. It provides an easy way to manage data source properties in ReportServer.

## Import Shared DataSource into Web Designer

This section explains, how to import a Shared Data Source from the server.

Click the `Data` icon in the configuration panel to launch a `Data` configuration.

![](images/DataStartIcon.png)

 To import shared data source, switch over to data source panel using the switcher icon on the top-right corner of the `Data` configuration panel.

![](images/Switcher-Datasource.png)

In the context menu, click `Datasources` to launch the `DataSources` configuration panel.

![](images/Datasource-New-Panel.png)

In the `DataSources` configuration panel, click the `New DataSource` button. In the connection type panel, choose the `Shared` data source type.

 ![](images/Shared-Datasource-Connect.png)

After choosing  the `Shared Datasource`, the new connection wizard will be shown as below:

 ![](images/Shared-Datasource-CreateWizard.png)

 A shared data source panel consists of the following fields:

  * **Name**: Specify the data source name without special characters.
 
 * **Shared DataSource**: You can select an existing shared data sources in the server from the drop-down list.

    ![](images/Datasource-SaveWizard.png)

Finally, click `Save` button in the `New Connection` panel.

Now, a new shared data source will be added in the report like below. You can import multiple shared data sources in the report.

![](images/Select-SharedDS.png)
