---
layout: post
title: Subreport Report Item | ReportDesigner | JS | Syncfusion
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

> Note: Header and Footer area doesn't allow to drop the sub report report item.

You can customize the subreport border, color and type through property panel.

![](SubReport-images/SubReport-Properties.png)

In the name field, type a name in the **Name** text box. By default, a general name such as Subreport1 or Subreport2 is assigned. The name must be unique within the report.

To use this report as a subreport refer [Link Report](/js/ReportDesigner/Compose-Report/Link-Data#DrillThrough:Link-Report).

To specify parameters to pass to a subreport refer [Link Parameter](/js/ReportDesigner/Compose-Report/Link-Data#DrillThrough:Link-Parameters).

You can configure to display the custom message when no datasets in the subreport have data at run time.

![](SubReport-images/No-Rows-Message.png)

You can keep the entire report content of subreport in same page without split when enable the keep together property in property panel.

![](SubReport-images/SubReport-Keeptogether.png)
