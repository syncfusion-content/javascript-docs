---
layout: post
title: Create new parameter with Syncfusion Web Report Designer
description: How to create  new parameter with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Report Parameter

Report parameters filter report data that is retrieved from a data source. When you cannot filter data in data source, you can use parameters to filter report data after it is retrieved. You can also sort and group data in a report based on report parameters. 

For example, by including parameters for a start and end date in a query, you can specify a date range that limits the data retrieved from the data source.

## Add parameter

You can add new parameter using the following steps:

1. Click `Parameter` icon in the configuration panel to launch the `Parameter` configuration.

   ![](Create-Parameter-Images/Parameter-DataPane.png)

2. Next, click the `New Parameter` button.

   ![](Create-Parameter-Images/New-Parameter.png)

   Now, the following wizard will be displayed.

   ![](Create-Parameter-Images/New-Parameter-Fields.png)

3. In **Name**, type the name of the parameter or use default name. By default, manually-created parameters name are similar to `ReportParameter1`.

4. In **Prompt**, type the text that appears next to the parameter when the user previews the report.

5. In **Data type**, select the data type for the parameter value. The supported data types are `Boolean`, `DateTime`, `Integer`, `Float` and `Text`.

6. Select **Allow blank value**, if parameter value needs to be set as an empty string or a blank value.

   > Note: If you specify valid values for a parameter, and you want a blank value to be one of the valid values, you must include it as one of the values that you specify. Selecting this option does not automatically include a blank value for available values.

7. Select **Allow null value**, if the value of the parameter needs to be set as null.

   > Note: If you specify valid values for a parameter, and you want null to be one of the valid values, you must include null as one of the values that you specify. Selecting this option does not automatically include the null value for available values.

8. Select **Allow multiple values**, if the value for the parameter should be multiple values. Null values are not allowed.

9. Set the visibility option.
   
   * Select **Visible** to display the report parameter at the top of the report while running the report. This option allows you to select parameter values at run time.

   * Select **Hidden** to hide the report parameter in the published report. The report parameter values can still be set on a report URL, in a subscription definition, or on the Report Server.

   * Select **Internal** to hide the report parameter. In the published report, the report parameter can only be viewed in the report definition.

10. Click `Assign Value` to set available and default values.

Now, the above action will launch `Parameter dialog`, where you can set the available and default values for the parameter.

![](Create-Parameter-Images/Parameter-Dialog.png)

### Add available values

An available values list limits the user to choose and preview only the data related to valid values for the parameter. You can see this drop-down list of available values for the parameter, while previewing the report.

You can choose the `Available Value` tab in parameter dialog to add available values.

1. Click **Available Value** tab with below options:

   * Click **Specify value** to enter a static list of parameter values from which the user can choose. If you select this option, a list in which you can type values and labels appears.

     ![](Create-Parameter-Images/Parameter-Specify-Avail.png)

     * Click **Add** and then enter the value in the **Value** text box, and optionally, the label in the **Label** text box. If you do not provide the label, the value is used.

       ![](Create-Parameter-Images/Parameter-Specify-Add.png)

       You can write an expression for the value by clicking the icon which is right after to **Value** textbox.

       Repeat this step for as many values as you want to provide. The order of items you see in this list determines the order. 
      
       **Reorder Item**:

       To change the order of an item in the list, click and hold the icon in the left corner of **Label** text box, and then drag the item to higher or lower position in the list.

         ![](Create-Parameter-Images/Parameter-Specify-Drag.png)

       The position of dragged item is shown as below:

         ![](Create-Parameter-Images/Default-Specify-Add.png)

   * Click **Query Value** to provide the name of an existing dataset that retrieves the values for this parameter.

     ![](Create-Parameter-Images/Parameter-Query-Avail.png)
   
     In **Dataset**, choose the name of the dataset. Datasets can be defined using the data view. For more information, refer [Create Dataset](/js/ReportDesigner/create-data/Create-New-Data).

     In **Value field**, choose the name of the field that provides parameter values. 
     
     > Note: These fields are retrieved from the list of column or field names in the dataset.

     In **Label field**, choose the name of the field that provides the parameter names. If there is no separate field for names, choose the same field similar to Value field.

   * Click **None** to remove available values for parameter. When you preview the report, the drop-down list of available values for the parameter no longer appears. 

2. Click `OK`.

> Note: If you have specified available values for a parameter, the valid values always appear as a drop-down list in preview.

### Add default values

Parameters will have default values to automatically run report on first view without choosing any parameters to view it.

1. By default, the parameter dialog will be launched with `Available Value` tab. To switch over to `Default Value` tab, click the **Default Value** which has below options

   ![](Create-Parameter-Images/Default-None.png)

   * Click **Specify value** to provide a value or list of values.

     ![](Create-Parameter-Images/Parameter-Specify-Avail.png)

     * Click **Add** and then enter the value in the **Value** text box.

       ![](Create-Parameter-Images/Default-Add-Expr.png)

       You can write an expression for the value by clicking the icon which is right after to **Value** textbox.

       For multi value parameters, repeat this step for as many values as you want to provide. The order of items in the list determines the order.
      
   * Click **Query Value** to provide the name of an existing dataset that retrieves the values.

     ![](Create-Parameter-Images/Default-Query.png)
   
     In **Dataset**, choose the name of the dataset. Datasets can be defined using the data view. For more information, refer [Create Dataset](/js/ReportDesigner/create-data/Create-New-Data).

     In **Value field**, choose the name of the field that provides parameter values. 
     
     > Note: These fields are retrieved from the list of column or field names in the dataset.

   * Click **None** to remove default values for parameter.

2. Click `OK`.

> Note: To add multi value parameters, you must check  `Allow multiple values` option.

### Save parameter

Click `Save` in the parameter wizard.

  ![](Create-Parameter-Images/Parameter-Final-Save.png)

The parameter will be listed under `Parameter` panel in the report like below.

  ![](Create-Parameter-Images/Parameter-Save-List.png)

Now, the `Parameter` has been created successfully with the Web Report Designer.

## To display the parameter in design area

You can prefer to display the parameters in a textbox placed anywhere in the design area for sharing the information of parameter chosen.

The parameter can be placed easily in design area using below steps:

* From the parameter configuration panel, drag the parameter to the footer.

  ![](Create-Parameter-Images/Parameter-Drag-Footer.png)

* It displays a text box with `<<Expr>>`. Select the `<<Expr>>` text and right-click the `<<Expr>>` to pop up context menu options.

  ![](Create-Parameter-Images/Param-Textbox-Menu.png)

* Click `Expression`.

   The expression dialog box opens, you can edit the expression value in the text area.

   ![](Create-Parameter-Images/Parameter-ExpressionDialog.png)

* Click `OK`.

You can follow the above steps to display parameter on the page `Header` and `Body`.
