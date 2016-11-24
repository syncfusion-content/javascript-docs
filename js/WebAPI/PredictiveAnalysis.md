---
layout: post
title: webAPI reference for ejPredictiveAnalysis
description: webAPI reference for ejPredictiveAnalysis
documentation: API
platform: js-webapi
keywords: ejPredictiveAnalysis,PredictiveAnalysis, syncfusion, PredictiveAnalysis  webapi
---

## Load

[POST&nbsp;&nbsp;/Api/PredictiveAnalytics/Load](http://js.syncfusion.com/demos/ejServices/api/PredictiveAnalytics/Load)

This section explains the usage of Predictive Analytics API in JavaScript. This consumes the PMML and input data to retrieve the predicted result.

### URL parameters

|  Parameter |  Data Type |  Description | 
|---|---|---|
| model  | PredictiveModel (Array)  | Send the data, PMML file and model name to retrieve the predicted result. <br/><br/> List of PMML files shipped within the EJ services are Groceries.pmml, Glass.pmml, Bfeed.pmml, Audit.pmml, Cars.pmml, Wine.pmml, BreastCancer.pmml, Imports.pmml, Iris.pmml, Tips.pmml, Ozone.pmml, Titanic.pmml. <br/><br/> List of model names supported within the EJ services are AssociationRules, Clustering, CoxRegression, GeneralRegression, GradientBoosting, MultinomialRegression, NaiveBayes, NeuralNetworks, RandomForest, Regression, SupportVectorMachine, TreeModel.  |  


### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

```javascript

[{
    "transactionID":1,
    "items":"{citrus fruit,semi-finished bread,margarine,ready soups}",
    "Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",
    "Exclusive_Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",
    "Rule_Association":"[]"
}]

```


### Code example 


```javascript

$.ajax({
        type: "POST",
        url: 'http://js.syncfusion.com/demos/ejServices/api/PredictiveAnalytics/Load',
        data: JSON.stringify({ data: "[{transactionID:1,items:'{citrus fruit,semi-finished bread,margarine,ready soups}'}]", pmmlFile: 'Groceries.pmml', name: 'AssociationRules' }),
        contentType: "application/json; charset=utf-8",
        dataType: "json",
        processdata: true,
 });

```