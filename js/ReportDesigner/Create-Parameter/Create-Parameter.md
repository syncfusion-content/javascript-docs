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

Report parameters filter report data that is retrieved from a data source. When you cannot filter data at the data source, you can use parameters to filter report data after it is retrieved. You can also sort and group data in a report based on report parameters. For example, by including parameters for a start and end date in a query, you can specify a date range that limits the data retrieved from the data source. An additional parameters can be created to filter the data after it is retrieved from the data source

## Create report parameter

Create a parameter manually using the parameter configuration panel.

The following steps describe the properties that can be set for each parameter:

* **Name**: By default, manually-created parameters name are similar to `ReportParameter1`. Any name can be given as desired to identify it within the report.

* **Prompt**: The text that appears next to the parameter on the report viewer toolbar.

* **Data type**: A report parameter must be one of the following data types:

    * Boolean 

    * DateTime

    * Integer

    * Float

    * Text

* **Allow blank value**: Select this option to specify the value of the parameter as an empty string or a blank value.

  If you specify valid values for a parameter, and you want a blank value to be one of the valid values, you must include it as one of the values that you specify. Selecting this option does not automatically include a blank value for available values.

* **Allow null value**: Select this option, if the value of the parameter can be a null.

  If you specify valid values for a parameter, and you want null to be one of the valid values, you must include null as one of the values that you specify. Selecting this option does not automatically include the null value for available values.

* **Allow multiple values**: Select this option if the value for the parameter can be multiple values. Null values are not allowed.

* **Visible**: Select this option to display the report parameter at the top of the report while running the report. This option allows you to select parameter values at run time.

* **Hidden**: Select this option to hide the report parameter in the published report. The report parameter values can still be set on a report URL, in a subscription definition, or on the Report Server.

* **Internal**: Select this option to hide the report parameter. In the published report, the report parameter can only be viewed in the report definition.

* **Available values**: If you have specified available values for a parameter, the valid values always appear as a drop-down list. 

    **Specify value**: Select this option to enter a static list of parameter values from which the user can choose. If you select this option, a list in which you can type values and labels appears.

    **Query**: Select query option to provide a dynamic list of parameter values from which the user can choose. This list is obtained from a data source. If you select query, three fields appear in which you can define the query information.

    * Label: Appears only when **Specify Value** is selected. Type a label that is displayed to the user. When the user clicks the label in the list, the value specified in **Value** is retained for the parameter.

    * Value: Appears only when **Specify Value** is selected. Type a value that will be retained for the parameter.

    * Dataset: Appears only when **Query Value** is selected. Select this field to retrieve the list of parameters. Datasets can be defined using the data view. For more information, refer [Create Dataset](/js/ReportDesigner/create-data/Create-New-Data).

    * Value field: Appears only when **Query Value** is selected. Select this field to obtain a list of available values, for example, `EmployeeID`. The available fields are retrieved from the list of column or field names in the dataset.

    * Label field: Appears only when **Query** is selected. Select this field to obtain a list of labels to display to the user for the values, for example, `EmployeeName`. The available fields are retrieved from the list of column or field names in the dataset.

* **Default values**: When each parameter has a default value, the report runs automatically on first view.

   **Specify Value**: Select **Specify Value** to enter a static default value or a set of default values for the parameter. If you select **Specify Value**, a text box appears in which you can type a value or set of values.

   **Query**: Select **Query Value** to retrieve the default value or set of default values from the data source. If you select **Query**, two fields appear in which you can define query information.

   * Dataset: Appears only when **Query Value** is selected. Select the dataset to retrieve the default value or the set of default values for the parameter. Datasets can be defined using the data view. For more information, refer [Create Dataset](/js/ReportDesigner/create-data/Create-New-Data).

   * Value field: Appears only when **Query Value** is selected. Select this field to obtain the default value or set of default values. The available fields are retrieved from the list of column or field names in the dataset.

* **None**: Select **None** if you do not want to provide the default or available value for the parameter.

## Add parameter

Click `Parameter` icon in the configuration panel to launch the `Parameter` configuration.

![](Create-Parameter-Images/Parameter-DataPane.png)

In the `Parameter` configuration panel, click the `New Parameter` button.

![](Create-Parameter-Images/New-Parameter.png)

Now, the following wizard will be displayed.

![](Create-Parameter-Images/New-Parameter-Fields.png)

In **Name** field, type `PersonID`.

In **Prompt** field, type `PersonID:` .

Verify that the data type is `integer`.

Click `Assign Value` to set available and default values.

Now, the above action will launch `Parameter dialog`, where you can set the available and default values for the parameter.

![](Create-Parameter-Images/Parameter-Dialog.png)

### Add available values

Click the `Available Value` tab.

* Click **Specify value** to manually provide the list of values, and optionally, name the labels for values.

  ![](Create-Parameter-Images/Parameter-Specify-Avail.png)

* Click **Add** and then enter the value in the **Value** text box, and optionally, the label in the **Label** text box. If you do not provide the label, the value is used.

  ![](Create-Parameter-Images/Parameter-Specify-Add.png)

* You can write an expression for the value by clicking the icon which is right after to **Value** textbox.

Repeat this step for as many values as you want to provide. The order of items you see in this list determines the order. You can see the order in the drop-down list.

* Click  **Query Value** to provide the name of an existing dataset that retrieves the values for this parameter.

  ![](Create-Parameter-Images/Parameter-Query-Avail.png)

  In **Dataset**, choose the name of the dataset.

  In **Value field**, choose the name of the field that provides parameter values.

  In **Label field**, choose the name of the field that provides the friendly names for the parameter. If there is no separate field for friendly names, choose the same field as you chose for the Value field.

When you preview the report, you see a drop-down list of available values for the parameter.

### Add default values

By default, the dialog will be launched with `Available Value` tab. To switch over to `Default Value` tab, click the **Default Value**.

![](Create-Parameter-Images/Default-None.png)

* To manually provide a value or list of values, click **Specify value**.

  ![](Create-Parameter-Images/Default-Specify-Avail.png)

* Click **Add** and then enter the value in the **Value** text box. 

  ![](Create-Parameter-Images/Default-Add-Expr.png)

* You can write an expression for the value by clicking the icon which is right after to **Value** textbox.

For multi value parameters, repeat this step for as many values as you want to provide. The order of items in the list determines the order. You can see the order in the drop-down list.

* To provide the name of the existing dataset that retrieves the values, click **Query Value**. 

   ![](Create-Parameter-Images/Default-Query.png)

     In **Dataset**, choose the name of the dataset.

     In **Value field**, choose the name of the field that provides parameter values.

* Click ok.

> Note: To add multi value parameters, you must check  `Allow multiple values` option.

### Reorder item

 To change the order of an item in the list, click and hold the icon in the left corner of **Label** text box, and then drag the item to higher or lower position in the list.

![](Create-Parameter-Images/Parameter-Specify-Drag.png)

The position of dragged item is shown as below:

![](Create-Parameter-Images/Default-Specify-Add.png)

### Save parameter

* Click `Save` in the parameter wizard.

  ![](Create-Parameter-Images/Parameter-Final-Save.png)

The parameter will be listed under `Parameter` panel in the report like below.

![](Create-Parameter-Images/Parameter-Save-List.png)

Now, the `Parameter` has been create successfully with the Web Report Designer.

## To remove available values for the report parameter

* Click `Assign Value`, the parameters dialog box opens.
 
* Select the **Available Value** tab.

* Choose **None**.

*  Click OK.

When you preview the report, the drop-down list of available values for the parameter no longer appears.

## To remove default values for the report parameter

* Click `Assign Value`, the parameters dialog box opens.
 
* Select the **Default Value** tab.

* Choose **None**.

*  Click ok.

## To display the selected parameter on a page footer

When your report readers have questions about a report, it helps to know which parameter values are chosen by them. You can preserve user-selected values for each parameter in the report, so as to display the parameters in a textbox in the page footer.

* From the parameter configuration panel, drag the parameter @PersonID to the footer.

  ![](Create-Parameter-Images/Parameter-Drag-Footer.png)

* It displays a text box with `<<Expr>>`. Select the `<<Expr>>` text and right-click the `<<Expr>>`

  ![](Create-Parameter-Images/Param-Textbox-Menu.png)

* Click `Expression`.

   The expression dialog box opens, you can edit the expression value in the text area.

   ![](Create-Parameter-Images/Parameter-ExpressionDialog.png)

* Click ok.

You can also display parameter on the page `Header` and `Body`
