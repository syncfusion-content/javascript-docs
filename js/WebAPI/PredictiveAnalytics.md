---
layout: post
title: webAPI reference for ejPredictiveAnalytics
description: webAPI reference for ejPredictiveAnalytics
documentation: ug
platform: js
keywords: ejPredictiveAnalytics,PredictiveAnalytics, syncfusion, PredictiveAnalytics webapi
---

## Load

 [POST] [/Api/PredictiveAnalytics/Load](http://js.syncfusion.com/demos/ejServices/api/PredictiveAnalytics/Load)

This section explains the usage of Predictive Analytics API in JavaScript. This consumes the PMML and input data to retrieve the predicted result.

### URL parameters

|  Parameter |  Data Type |  Description | 
|---|---|---|
| model  | PredictiveModel (Array)  | Send the data, PMML file and model name to retrieve the predicted result. <br><br> List of PMML files shipped within the EJ services are Groceries.pmml, Glass.pmml, Bfeed.pmml, Audit.pmml, Cars.pmml, Wine.pmml, BreastCancer.pmml, Imports.pmml, Iris.pmml, Tips.pmml, Ozone.pmml, Titanic.pmml. <br><br> List of model names supported within the EJ services are AssociationRules, Clustering, CoxRegression, GeneralRegression, GradientBoosting, MultinomialRegression, NaiveBayes, NeuralNetworks, RandomForest, Regression, SupportVectorMachine, TreeModel.  |  


### Response information 

Code: 200

Content-Type: application/json;odata=verbose;charset=utf-8

Response (JSON):   

{% highlight js %}

[{
    "transactionID":1,
    "items":"{citrus fruit,semi-finished bread,margarine,ready soups}",
    "Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",
    "Exclusive_Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",
    "Rule_Association":"[]"
}]

{% endhighlight %}


### Code example 


{% highlight js %}

$.ajax({
        type: "POST",
        url: 'http://js.syncfusion.com/demos/ejServices/api/PredictiveAnalytics/Load',
        data: JSON.stringify({ data: "[{transactionID:1,items:'{citrus fruit,semi-finished bread,margarine,ready soups}'}]", pmmlFile: 'Groceries.pmml', name: 'AssociationRules' }),
        contentType: "application/json; charset=utf-8",
        dataType: "json",
        processdata: true,
 });

{% endhighlight %}