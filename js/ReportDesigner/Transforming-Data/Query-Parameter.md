---
layout: post
title: Configuring Query Parameters in JavaScript ReportDesigner | Syncfusion
description: How to add query parameters with Syncfusion Essential JavaScript ReportDesigner Control, its elements, and more.
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Query Parameters inJavaScript ReportDesigner

A query parameter is created for each query variable or input parameter, and a report parameter is created for each query parameter.

Click on the **Query Parameter** icon in the query designer toolbar.

![JavaScript ReportDesigner param icon](Query-Parameter-images/param-Icon.png)

Now the query parameters dialog will be launched.

![JavaScript ReportDesigner param dialog](Query-Parameter-images/Param-Dialog.png)

## Adding Query Parameter

  1.  Add a query parameter through clicking the `Add` icon in the dialog.

        ![JavaScript ReportDesigner param add](Query-Parameter-images/Param-Add.png)

   2. **Parameter Name** : In the **Parameter Name** text box, type the name of the query parameter.

   3. **Value** : In **Value** field, type or select the value to pass to the parameter.
     
        * Values can contain an expression that evaluates to a value to pass to the query parameter. The expressions in the value list includes the field list for the current report.

            ![JavaScript ReportDesigner param exp icon](Query-Parameter-images/param-Exp-Icon.png)

        * To set expression click on the icon in the right side of the value field.

            ![JavaScript ReportDesigner param exp menu](Query-Parameter-images/Param-Exp-Menu.png)

            ![JavaScript ReportDesigner param exp dialog](Query-Parameter-images/param-Exp-Dialog.png)

        * The icon will be indicated in `Black color`, if the expression is applied.

            ![JavaScript ReportDesigner exp black](Query-Parameter-images/Exp-Black.png)

   3. Click `OK` to save the query parameters.

### Remove Parameters

* Click `Close` icon to remove the query parameter from the list.

    ![JavaScript ReportDesigner delete parameter](Query-Parameter-images/Delete-Parameter.png)

#### Reorder item

 To change the order of an item in the list, click and hold the icon in the left corner of **Parameter Name** field, and then drag the item to higher or lower position in the list.

![JavaScript ReportDesigner param drag](Query-Parameter-images/Param-Drag.png)

The position of dragged item is shown as below:

![JavaScript ReportDesigner param reorder](Query-Parameter-images/Param-Reorder.png)
