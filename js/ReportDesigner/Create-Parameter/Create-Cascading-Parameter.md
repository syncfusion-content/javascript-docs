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

A list of values for a parameter depends on values chosen for a previous parameter. It helps when the parameter has a long list of values and the parameters can be filtered based on the previous parameter.

## Steps to create cascaded parameters in web designer

### Create datasource

* To create new `Datasource`, refer [Create Datasource](/report-platform/reportdesigner/web/create-data/Create-New-Datasource).

* While creating data source, give the data source **Name** as **AdventureWorks** and select **AdventureWorks** database from the drop-down list.
 
   ![](images/Cascade_Datasource.png)

### Create the main dataset with a query and query parameters

* In the configuration panel, click the `Data` icon and select the `Add Dataset`. For more details, refer [Create Dataset](/report-platform/reportdesigner/web/create-data/Create-New-Data).

   ![](images/Dataset-CreateWizard.png)

* Click `Create New`, will launch the below wizard.

  ![](images/Existing-DatsourceWizard.png)

* Choose `AdventureWorks` data source from the drop-down list.

  ![](images/Existing-Datsource-Select.png)

* Click `Connect Datasource`.

* In name field, type **SalesbyCategory**.

* Switch to Query editor by using the switcher icon (highlighted in the below snap).

   ![](images/Switch-Query-Editor.png)

* Paste the following query in the Query editor:

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
    
   The query now includes the query parameters @Category, @Subcategory, and @Product.

     ![](images/Cascade-Query-Editor.png)

* Click run to see the result set. The **Query Parameters** dialog box opens.

   In the parameter value column, type the value for each query parameter like below.

   * Enter `Components` as value for **@Category**.
   * Enter `Brakes` as value for **@Subcategory**.
   * Enter `Front Brakes` as value for **@Product**.

  ![](images/Cascade-Query-Parameter2.png)
   
* Click `Ok`.

  The result set contains a list of sales order numbers that are grouped by date for front brakes.

* Click `Finish`. Now, the dataset will be added with the report under the data pane.

In the configuration panel, click the parameters icon and verify the following report parameters appear: category, subcategory, and product.

To provide values for each report parameter at run time, you should create a dataset for each parameter. 

Go through the [CreateParameter](Create-Parameter-FilterDS) topic to know about how to create parameter, before proceeding with below steps:

#### Create dataset for `Category` parameter:

* Create dataset by following the same procedure described above.

    * In name field, type **CategoryValues**.

    * Paste the following query text in the query editor:

      ```
                SELECT DISTINCT Name AS Category FROM Production.ProductCategory 
      ```          

      ![](images/Cascade-RP1-Dataset.png)

* Click run to see the result. The column category appears with four values: accessories, bikes, clothing, and components.

* Click finish.

Now, you have to set the properties for the report parameter **Category** to use values from the query for both its available values and its default values.

#### Set available values and default values for a `Category` parameter:

* Click `Parameter` icon in the configuration panel to launch a `Parameter` configuration.

* Edit the **Category** parameter.
   
   * In name field, verify that the name is **Category**.

* Click `Assign Value`, will launch the `Parameter Dialog`.

   * Click **Available value**.

   * Click **Query Value**. 

     In **Dataset**, from the drop-down list, select **CategoryValues**.

     In **Value field**, choose **Category**.

     In **Label field**, choose **Category**.

     ![](images/Cascade-CategoryValDef.png)

   * Click **Default value**.

   * Click **Query Value**. 

      In **Dataset**, select **CategoryValues** from the drop-down list.

      In **Value field**, select **Category**.

     ![](images/Cascade-CategoryVal.png)

* Click `Ok`.

* Click `Save` in the `New Parameter` wizard.

Now, you can modify the parameter @Subcategory depends on the value selected for @Category.

#### Create dataset for `Subcategory` parameter

* Create dataset by following the same procedure described above.

    * In name field, type **SubcategoryValues**.

    * Paste the following query text in the query editor:

    ```
              SELECT DISTINCT PSC.Name AS Subcategory 
                    FROM Production.ProductSubcategory AS PSC
                    INNER JOIN Production.ProductCategory AS PC
                    ON PC.ProductCategoryID = PSC.ProductCategoryID
                    WHERE PC.Name = (@Category)
    ```

    Now, the query includes the query parameters @Category.

    ![](images/Cascade-RP2-Dataset.png)

* Click run to see the result set. The **Query Parameters** dialog box opens.

   ![](images/Cascade-Query-Parameter.png)
   
* Click `Ok`, the result set displays 14 rows.

* Click `Finish`, now the dataset will be added with the report under the data pane.

#### Set available values and default values for a `Subcategory` parameter:

* Click `Parameter` icon in the configuration panel to launch a `Parameter` configuration.

* Edit the **Subcategory** parameter.
   
   * In name field, verify that the name is **Subcategory**.

* Click `Assign Value`, will launch the `Parameter Dialog`.

   * Click **Available value**.

   * Click **Query Value**. 

     In **Dataset**, select **SubcategoryValues** from the drop-down list.

     In **Value field**, choose **Subcategory**.

     In **Label field**, choose **Subcategory**.

     ![](images/Cascade-EditRP1.png)

   * Click **Default value**.

   * Click **Query Value**. 

      In **Dataset**, select **SubcategoryValues** from the drop-down list.

      In **Value field**, select **Subcategory**.

      ![](images/Cascade-EditRP1-Default.png)

* Click `Ok`.

* Click `Save` in the `New Parameter` wizard.

Now, create a parameter @Product depends on both the value of @Category and the value of @Subcategory.


#### Create dataset for `Product` parameter:

* Create dataset by following the same procedure described above.

    * In name field, type **ProductValues**.

    * Paste the following query text in the query editor:

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

    ![](images/Cascade-RP3-Dataset.png)

* Click `Finish`, now a dataset named **ProductValues** with one field named **Product** will be added with the report under the data pane.

#### Set available values and default values for a `Product` parameter

* Click `Parameter` icon in the configuration panel to launch the `Parameter` configuration.

* Edit the **Product** parameter
   
   * In name field, verify that the name is **Product**.

* Click `Assign Value`, will launch the `Parameter Dialog`.

   * Click **Available value**.

   * Click **Query Value**. 

     In **Dataset**, select **ProductValues** from the drop-down list.

     In **Value field**, choose **Product**.

     In **Label field**, choose **Product**.

     ![](images/Cascade-EditRP2.png)

   * Click **Default value**.

   * Click **Query Value**. 

      In **Dataset**, select **ProductValues** from the drop-down list.

      In **Value field**, select **Product**.

      ![](images/Cascade-EditRP2-Default.png)

* Click `Ok`.

* Click `Save` in the `New Parameter` wizard.

### Add a grid to display the results

  * In design view, drag and drop the the `Grid` from the left pane into designer panel.

    ![](images/Cascade-Grid-Drag.png)

  * In the configuration panel, click the `Properties` icon to **assign data** to the `Grid`.

    ![](images/Cascade-Grid-Property.png)

    In the properties panel, click the `Data Assign` tab, and drag the following fields SalesOrderNumber, OrderQty, LineTotal from the **SalesbyCategory** dataset.

    ![](images/Cascade-Grid-AssignData.png)

### Preview the cascading parameters

* Click **Preview** at top-right corner of the toolbar.

* From the **Category** drop-down list, select **Components**.

* From the **Subcategory** drop-down list, select **Brakes**.

* From the **Product** drop-down list, select **Front Brakes**.

Notice, when you select each successive parameter, the drop-down list for the next parameter shows only the valid values that are based on your previous choices.

* On the report viewer toolbar, click the view report.

    The report displays sales order numbers with order quantity and line totals for orders that include the "front brakes" product.

  ![](images/Parameter-ViewerICon-Preview.png)


Click the `Parameter` icon in the viewer toolbar to hide the parameter fields.

![](images/Parameter-ViewerICon.png)

Now, the preview will be displayed like below:

  ![](images/Cascade-Preview-Result.png)
