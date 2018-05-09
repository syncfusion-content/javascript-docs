---
layout: post
title: Rectangle Report Item | ReportDesigner | JS | Syncfusion
description: Draw a SubReport Item
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# SubReport

SubReport is a standalone report, that is embedded into another report. You can link the contents of a subreport to main report through parameters.

## To add SubReport


Drag and drop the `SubReport` from the item panel.

![](SubReport-images/SubReport-Drag.png)

> Note: Header and Footer area doesn't allow to drop the pivot grid report item.

You can customize the subreport border, color and type through property panel.
![](SubReport-images/SubReport-Properties.png)

You can configure the sub report path and parameter through following steps,
      1. Click `Browse` in the report fields and select a report from the list; type or select the name of the report.

         ![](SubReport-images/Browse-Report-Dialog.png)

          To specify parameters for the sub report, follow the next step.

      2.  Click `Set Parameters` in the report fields, it will launch the `Parameters` dialog.

            ![](SubReport-images/EnableLink-Parameter-Dialog.png)

            * Click **Add**. A new row is added to the parameter grid.

              ![](SubReport-images/Enable-Link-Add-Row.png)

            * In the **Name** text box, type the name of the report parameter in the sub report. If the sub report is in the server, the parameter names are available in the drop-down list.

            * In **Value**, type or select the value to pass to the parameter in the sub report.
        
            * Values can contain an expression that evaluates a value to pass to the report parameter. The expressions in the value list include the field list for the current report.

      3. Click `OK`.
      4. Selected report the will be loaded while preview.

You can keep the entire report content of subreport in same page without split when enable the keep together property in property panel.
![](SubReport-images/SubReport-Keeptogether.png)

You can configure to display the custom message when there is no data through property panel.
![](SubReport-images/SubReport-NoRowMessage.png)

