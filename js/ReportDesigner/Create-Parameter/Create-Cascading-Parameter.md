---
layout: post
title: Create cascading parameter with Syncfusion Web Report Designer
description: How to create  cascading parameter with Syncfusion Web Report Designer
platform: js
control: ReportDesigner
documentation: ug
api: /api/js/ejreportdesigner
---

# Cascading Parameter

Cascading parameters helps to filter out huge amount of report data. You can define a set of related parameters where the list of values for one parameter depends on values chosen in another parameter.

## Steps to create cascaded parameters in web designer

### Create datasource

To create new `Datasource`, refer [Create Datasource](/js/ReportDesigner/create-data/Create-New-Datasource).

For example, we have selected **AdventureWorks** database and given the data source **Name** as **AdventureWorks**.
 
   ![](Cascade-Parameter-Images/Cascade-Datasource.png)

### Create the main dataset with a query and query parameters

You can follow the below steps to create main dataset:

1. In the configuration panel, click the `Data` icon and select the `Add Dataset`. For more details, refer [Create Dataset](/js/ReportDesigner/create-data/Create-New-Data).

   ![](Cascade-Parameter-Images/Dataset-CreateWizard.png)

2. Click `Create New`, will launch the below wizard.

   ![](Cascade-Parameter-Images/Existing-DatsourceWizard.png)

3. Choose `Create New` option to create new datasource or choose `Existing` to pick existing one. For example, we have picked existing data source `AdventureWorks` from the drop-down list.

   ![](Cascade-Parameter-Images/Existing-Datsource-Select.png)

4. Click `Connect Datasource` to move to the query designer view.

5. In **name** field, type the name of the dataset. For example, we have provided **SalesbyCategory** as dataset name.

6. Switch to Query editor by using the switcher icon (highlighted in the below snap).

   ![](Cascade-Parameter-Images/Switch-Query-Editor.png)

7. The query must have the following parts:

    * A list of column fields in `SELECT` statement to fetch from any specific table.
    
    * One query parameter for each cascading parameter. 
    
    For example, we have chosen tables **SalesPerson**, **SalesOrderHeader**, **SalesOrderDetail**, **Product**, **ProductSubcategory**, **ProductCategory** from `AdventureWorks` database to include query parameters @Category, @Subcategory, and @Product in below query:

    ```
        SELECT 
            PC.Name AS Category,
            PSC.Name AS Subcategory,
            P.Name AS Product,
            SOH.[OrderDate],
            SOH.SalesOrderNumber,
            SD.OrderQty, 
            SD.LineTotal
            FROM [Sales].[SalesPerson] SP 
              INNER JOIN [Sales].[SalesOrderHeader] SOH 
              ON SP.[SalesPersonID] = SOH.[SalesPersonID]
              INNER JOIN Sales.SalesOrderDetail SD
              ON SD.SalesOrderID = SOH.SalesOrderID
              INNER JOIN Production.Product P
              ON SD.ProductID = P.ProductID
              INNER JOIN Production.ProductSubcategory PSC
              ON P.ProductSubcategoryID = PSC.ProductSubcategoryID
              INNER JOIN Production.ProductCategory PC
              ON PC.ProductCategoryID = PSC.ProductCategoryID
              WHERE (PC.Name = (@Category)
              AND PSC.Name = (@Subcategory)
              AND P.Name = (@Product))
    ```
    
    Paste the above query in query editor.

     ![](Cascade-Parameter-Images/Cascade-Query-Editor.png)

8. Click `run` icon in toolbar to see the result and the **Query Parameters** dialog box opens automatically.

   Type the desired value for each query parameter in the parameter value column.

   For example, 

   * In **@Category** parameter, we have typed `Components` as value.
   * In **@Subcategory** parameter, we have typed `Brakes` as value.
   * In **@Product** parameter, we have typed `Front Brakes` as value.

   ![](Cascade-Parameter-Images/Cascade-Query-Parameter2.png)
   
9. Click `Ok`. The result set now contains a list of sales order numbers that are grouped by date for front brakes.

10. Click `Finish`. Now, the dataset will be added with the report under the data pane.

In the configuration panel, click the parameters icon and verify the following report parameters category, subcategory, and product has been listed out.

To provide values for each report parameter at run time, you should create a dataset for each parameter. 

Go through the [CreateParameter](Create-Parameter-FilterDS) topic to know about how to create parameter, before proceeding with below steps:

#### Create dataset for Independent parameter:

1. Repeat steps 1 to 4 given in topic [Create Dataset](Create the main dataset with a query and query parameters) to create dataset for independent parameter. For example, we have chosen `Category` as independent parameter.

2. In **name** field, type the name of the dataset. For example, we have chosen **CategoryValues** as dataset name.

3. Paste the following query text in the query editor:

   ```
      SELECT DISTINCT Name AS Category FROM Production.ProductCategory 
   ```

   Here column name **Name** and table **ProductCategory** has been represented in above query to create dataset for independent parameter `Category`.

    ![](Cascade-Parameter-Images/Cascade-RP1-Dataset.png)

4. Click `run` icon in toolbar to see the result. 

5. Click `Finish`. Now, the dataset will be added with the report under the data pane.

Next, you have to set the properties for the report parameter **Category** to use values from the query for both available and default values.

#### Set available values and default values for independent parameter:

1. Click `Parameter` icon in the configuration panel to launch a `Parameter` configuration.

2. Edit the **Category** parameter. In name field, verify that the name is **Category**.

3. Click `Assign Value` to launch the `Parameter Dialog`.

4. Click **Available value** tab to assign available values.

   * Click **Query Value** radio option. 

     In **Dataset**, from the drop-down list, select the dataset created for independent parameter. Based on our example, we have to choose **CategoryValues**.

     In **Value field**, choose name of the field which will provide parameter value. For example, we have chosen **Category** from the drop-down list.

     In **Label field**, choose name of the field which will provide parameter label. For example, we have chosen **Category** from the drop-down list.

     ![](Cascade-Parameter-Images/Cascade-CategoryValDef.png)

5. Click **Default value** tab to assign default values.

   * Click **Query Value** radio option. 

      In **Dataset**, select dataset **CategoryValues** from the drop-down list based on our example.

      In **Value field**, select field **Category** from the drop-down list.

     ![](Cascade-Parameter-Images/Cascade-CategoryVal.png)

6. Click `Ok`.

7. Click `Save` in the `New Parameter` wizard.

Next, you need to create datasets for dependent parameters and assign values. For example, we have chosen @Subcategory and @Product as dependent parameters.

#### Create dataset for dependent parameters

1. Repeat steps 1 to 4 given in topic [Create Dataset](Create the main dataset with a query and query parameters) to create dataset for dependent parameter. For example, we have chosen `SubCategory` as dependent parameter.

2. In **name** field, type the name of the dataset. For example, we have chosen **SubcategoryValues** as dataset name.

3. Paste the following query text in the query editor:

    ```
        SELECT DISTINCT PSC.Name AS Subcategory 
          FROM Production.ProductSubcategory AS PSC
          INNER JOIN Production.ProductCategory AS PC
          ON PC.ProductCategoryID = PSC.ProductCategoryID
          WHERE PC.Name = (@Category)
    ```

   Here column name **Name** and table **ProductSubCategory** has been represented in above query which joins with table **ProductCategory** and includes condition with independent parameter `Category` to create dataset for dependent parameter `SubCategory`.

    ![](Cascade-Parameter-Images/Cascade-RP2-Dataset.png)

4. Click `run` icon in toolbar to see the result and the **Query Parameters** dialog box opens automatically.

   ![](Cascade-Parameter-Images/Cascade-Query-Parameter.png)

5. Click `Ok`, the result set displays 14 rows.

6. Click `Finish`. Now, the dataset will be added with the report under the data pane.

7. Repeat steps 1 to 6 to create another dependent parameter if needed. For example, we have created another dataset **ProductValues** for parameter **Product** containing below query:

    ```
              SELECT DISTINCT P.Name AS Product
                    FROM Production.Product P
                    INNER JOIN Production.ProductSubcategory AS PSC
                    ON P.ProductSubcategoryID = PSC.ProductSubcategoryID
                    INNER JOIN Production.ProductCategory AS PC
                    ON PC.ProductCategoryID = PSC.ProductCategoryID
                    WHERE (PC.Name = (@Category)
                    AND PSC.Name = (@Subcategory))
    ```
    Here column name **Name** and table **Product** has been represented in above query which joins with tables **ProductSubCategory** and **ProductCategory** to add condition with independent parameter `Category` and dependent parameter `Subcategory` for creating dataset for dependent parameter `Product`.

     ![](Cascade-Parameter-Images/Cascade-RP3-Dataset.png)

Next, you have to set the properties for the dependent parameters **Subcategory** and **Product** to use values from the query for both available and default values.

#### Set available values and default values for dependent parameters

1. Click `Parameter` icon in the configuration panel to launch a `Parameter` configuration.

2. Edit the **Subcategory** parameter. In name field, verify that the name is **Subcategory**.

3. Click `Assign Value` to launch the `Parameter Dialog`.

4. Click **Available value** tab to assign available values.

   * Click **Query Value** radio option. 

     In **Dataset**, from the drop-down list, select the dataset created for dependent parameter. Based on our example, we have to choose **SubcategoryValues**.

     In **Value field**, choose name of the field which will provide parameter value. For example, we have chosen **Subcategory** from the drop-down list.

     In **Label field**, choose name of the field which will provide parameter label. For example, we have chosen **Subcategory** from the drop-down list.

     ![](Cascade-Parameter-Images/Cascade-EditRP1.png)

5. Click **Default value** tab to assign default values.

   * Click **Query Value** radio option. 

      In **Dataset**, select dataset **SubcategoryValues** from the drop-down list based on our example.

      In **Value field**, select field **Subcategory** from the drop-down list.

     ![](Cascade-Parameter-Images/Cascade-EditRP1-Default.png)

6. Click `Ok`.

7. Click `Save` in the `New Parameter` wizard.

8. Repeat steps 1 to 7, to set available and default values for **Product** parameter. Based on our example, we have chosen dataset **ProductValues** to select parameter value and label as **Product** for assigning available and default values to **Product** parameter.

### Test the cascading parameters.

1. To test cascading parameters, choose relevant data visualization report items. For example, we have chosen `Grid` element for testing cascading parameters.

    ![](Cascade-Parameter-Images/Cascade-Grid-Drag.png)

2. In the configuration panel, click the `Properties` icon to assign data to the `Grid`.

    ![](Cascade-Parameter-Images/Cascade-Grid-Property.png)

    In the properties panel, click the `Data` tab, and based on our example we have dragged the following fields `SalesOrderNumber`, `OrderQty`, `LineTotal` from the **SalesbyCategory** dataset.

    ![](Cascade-Parameter-Images/Cascade-Grid-AssignData.png)

### Preview the cascading parameters

1. Click **Preview** at top-right corner of the toolbar.

2. From the independent parameter **Category** drop-down list, select **Components**.

3. From the dependent parameters **Subcategory** and **Product** drop-down list, select **Brakes** and **Front Brakes**.

   > Note: When you select each successive parameter, the drop-down list for the next parameter shows only the valid values that are based on your previous choices.

4. Click `View Report` button in viewer toolbar.

   The report displays sales order numbers with order quantity and line totals for orders that include the "front brakes" product.

   ![](Cascade-Parameter-Images/Parameter-ViewerICon-Preview.png)


5. Click the `Parameter` icon in the viewer toolbar to hide the parameter fields.

   ![](Cascade-Parameter-Images/Parameter-ViewerICon.png)

Now, the preview will be displayed like below:

![](Cascade-Parameter-Images/Cascade-Preview-Result.png)
