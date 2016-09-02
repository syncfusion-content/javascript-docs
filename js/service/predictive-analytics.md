---
layout: post
title: URL, Parameter and Response of Predictive Analytics Service
description: Service reference for Predictive Analytics
documentation: Service
platform: js
keywords: predictive, analytics, syncfusion, analytics service

---

# Predictive Analytics

### URL

{% highlight javascript %}

http://js.syncfusion.com/demos/ejservices/api/PredictiveAnalytics/PostAnalyticsAction

{% endhighlight %}

### Parameter

<table>
<tr>
<th>
Parameter</th><th>
Data type</th><th>
Description</th>
</tr>
<tr>
<td> data<br/></td>
<td> JSON</td>
<td> Input data table in the JSON format.</td>
</tr>
<tr>
<td> pmmlFile<br/></td>
<td> String</td>
<td> PMML file name with extension.<br/>
List of PMML files shipped within the EJ services are as follows:<br/>
* Groceries.pmml
* Glass.pmml
* Bfeed.pmml
* Audit.pmml
* Cars.pmml
* Wine.pmml
* BreastCancer.pmml
* Imports.pmml
* Iris.pmml
* Tips.pmml
* Ozone.pmml
* Titanic.pmml
</td>
</tr>
<tr>
<td> name(Model name)<br/></td>
<td> String</td>
<td> Model name.<br/>
List of model names supported within the EJ services are as follows:<br/>
* AssociationRules
* Clustering
* CoxRegression
* GeneralRegression
* GradientBoosting
* MultinomialRegression
* NaiveBayes
* NeuralNetworks
* RandomForest
* Regression
* SupportVectorMachine
* TreeModel
</td>
</tr>
</table>

N> Here, the PMML files are already available within the hosted 'EJServices'. In order to call the web API with the given URL, we need to give HTTP POST request with parameters - input data, PMML file name already available in the services and name of the model used in the PMML file. 

### HTTP Response   
             
#### Response Code

{% highlight javascript %}

200

{% endhighlight %}

#### Headers

{% highlight javascript %}

contentType: "application/json; charset=utf-8"

{% endhighlight %}

#### Result

Below are the sample results for respective model category.

<table>
<tr>
<th>
Result</th><th>
Model Category</th>
</tr>
<tr>
<td> 
"[{<br/>
"transactionID":1,<br/>
"items":"{citrus fruit,semi-finished bread,margarine,ready soups}",<br/>
"Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",<br/>
"Exclusive_Recommendation":"[whole milk,rolls/buns,other vegetables,yogurt]",<br/>
"Rule_Association":"[]"<br/>
}]"
</td>
<td> Association Rules</td>
</tr>
<tr>
<td> 
"[{<br/>
"RI":-0.16,<br/>
"Na":12.68,<br/>
"Mg":3.67,<br/>
"Al":1.16,<br/>
"Si":73.11,<br/>
"K":0.61,<br/>
"Ca":8.7,<br/>
"Ba":0,<br/>
"Fe":0,<br/>
"type":"WinF",<br/>
"Predicted_Cluster":"5"<br/>
}]"
</td>
<td> Clustering</td>
</tr>
<tr>
<td>
"[{<br/>
"total_bill":16.99,<br/>
"tip":1.01,<br/>
"sex":"Female",<br/>
"smoker":"No",<br/>
"day":"Sun",<br/>
"time":"Dinner",<br/>
"size":2,<br/>
"Predicted_TipAmount":2.6535990649137218<br/>
}]"
</td>
<td> Regression</td>
</tr>
<tr>
<td>
"[{<br/>
"pclass":"1st",<br/>
"survived":"survived",<br/>
"sex":"female",<br/>
"age":29,<br/>
"sibsp":0,<br/>
"parch":0,<br/>
"Predicted_survived":"survived",<br/>
"PassengerDiedProbability":0.184615384615385,<br/>
"PassengerSurvivedProbability":0.815384615384615<br/>
}]"
</td>
<td> Classification</td>
</tr>
</table>