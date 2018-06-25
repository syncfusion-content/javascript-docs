---
layout: post
title: Import Shared Datasets with Syncfusion Web Report Designer
description: How to import a shared datasets with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Shared Dataset

The shared dataset contains the data fields and reference of an existing dataset in ReportServer. It provides an easy way to manage data properties in ReportServer. 

## Import shared datasets into Web Designer

This section explains, how to import a Shared Dataset from the server.

Click the `Data` icon in the configuration panel to launch a `Data` configuration.

![](Linking-Shared-Data-Images/DataStartIcon.png)

Click the `Add DataSet` button in `Data` panel and choose `Shared` from the context menu.

![](Linking-Shared-Data-Images/Shared-Dataset-Button.png)

After choosing  the `Shared Data`, the new data wizard will be shown as below:

![](Linking-Shared-Data-Images/Select-SharedDSet.png)

A shared dataset panel consists of the following fields:

  * **Name**: Specify the dataset name without special characters.
 
  * **Shared DataSet**: You can select existing shared datasets in the server from the drop-down list.
    
Click `Save` in the `New Dataset` configuration panel.

Now, a new shared dataset will be added in the report like below. You can import multiple shared dataset in the report.

   ![](Linking-Shared-Data-Images/Shared-Dataset-List.png)
