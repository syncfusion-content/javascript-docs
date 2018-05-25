---
layout: post
title: Link Data | ReportDesigner | JS | Syncfusion
description: Link Data
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Enable Link

To enable **Action** fields, enable the **Enable Link** checkbox.

   ![](images/Enable-Link-Fields.png)

* **Action** - Defines a hyperlink, a bookmark link, or a drill through action. The action property must contain only one of the following elements: **Hyperlink**, or **Drill through**. 

## Drill Through:

A drill through report is a report that a user opens by clicking a link within another report. Drill through reports commonly contain details about an item that is contained in an original summary report.You can add drill through links to text boxes, images, charts any other report item that has an **Action** property.

### Drill through action
  
   1. Select **Report**.

       ![](images/Enable-Link-Reportpath.png)

   2. Click the `Browse` in the report fields and select the report from the list.

      ![](images/Browse-Report-Dialog.png)

### Parameters in drill through reports

A drill through report contains parameters that are passed to it by the summary report. To specify parameters for the drill through report, follow the below steps.

   1.  Click the `Set Parameters` in the report fields, it will launch the `Parameters` dialog.

        ![](images/EnableLink-Parameter-Dialog.png)

   2. To add parameter click **Add**.

        ![](images/Enable-Link-Add-Row.png)

   3. **Parameter Name** : In the **Name** text box, type the name of the report parameter in the drill through report. If the drill through report is in the server, the parameter names are available in the drop-down list.

   4. **Value** : In **Value**, type or select the value to pass to the parameter in the drill through report.
     
        * Values contain an expression that evaluates to a value to pass to the report parameter. The expressions in the value list include the field list for the current report. Click on the icon next to the expression field and select `Expression`. 

            ![](Filter-Data-Images/Expression-Icon.png)
   
        * The expression can be set like below.

            ![](Filter-Data-Images/Expression-Dialog.png)

        * The icon will be indicated in `Black color`, if the expression is applied.

            ![](Filter-Data-Images/Expression-Black.png)

   3. Click `OK` to save the parameters.

#### Remove Parameters

* Click `Close` icon to remove the parameters from the list.

    ![](images/Delete-Parameter.png)

#### Reorder item

 To change the order of an item in the list, click and hold the icon in the left corner of **Name** field, and then drag the item to higher or lower position in the list.

![](Create-Parameter-Images/Parameter-Specify-Drag.png)

The position of dragged item is shown as below:

![](Create-Parameter-Images/Default-Specify-Add.png)

## Hyperlink

 The hyperlink will open a browser with a URL that you specify. The static URL or an expression that evaluates URL can be used a hyperlink.

### Add a hyperlink to a URL

Hyperlink can be added to the report item, so that users can able to click the link in the report and open a browser to the URL that you specify.

 1. Select **URL**.

    ![](images/Enable-Link-URL.png)

2. In  **URL** field, type or select a URL or an expression that evaluates to the URL.

    ![](images/Enable-Link-URLGrid.png)

3. To test the link, click **Preview** to preview the report, and then click the report item that you set on this link.

    ![](images/URL-Sample.png)

