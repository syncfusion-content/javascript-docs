---
layout: post
title: Summary types | PivotClient | JavaScript | Syncfusion
description: Summary types
platform: js
control: PivotClient
documentation: ug
---

# Summary Types

I> This feature is applicable only for relational datasource.

Allows you to perform calculations over a group of values using `summaryType` option. This property includes several types of aggregations like sum, average, minimum, maximum etc. You can see the totals of PivotClient control with any one of the below mentioned summary types. 

Also, summary type options are added in the context menu of pivot buttons, in values section, to change the resultant summary value dynamically.

## Client mode

 Client mode supports the following summary types. By default, `sum` is applied.

* Sum
* Average
* Count
* Min
* Max

Refer the following code sample to implement summary type through code behind.

{% highlight js %}

$(function () {
            $("#PivotClient1").ejPivotClient({

                dataSource: {
                    data: pivotData,
                    rows: [
                        {
                            fieldName: "Country",
                            fieldCaption: "Country"
                        }
                    ],
                    columns: [
                        {
                            fieldName: "Product",
                            fieldCaption: "Product"
                        }
                    ],
                    values: [
                        {
                            fieldName: "Amount",
                            fieldCaption: "Amount",
                            summaryType: "count",
                        },
                        {
                            fieldName: "Quantity",
                            fieldCaption: "Quantity",
                            summaryType: "min",
                        },

                    ] ,
                },
            });
        });

{% endhighlight %}

![Summary types in JavaScript pivot client client mode](Getting-Started_images/client_mode_summary.png)


## Server mode

Server mode supports the following summary types. By default, `count` is applied.

* Sum
* Average
* Count
* Min
* Max
* DoubleTotalSum
* DoubleAverage
* DoubleMaximum
* DoubleMinimum
* DoubleStandardDeviation
* DoubleVariance
* DecimalTotalSum
* IntTotalSum
* DisplayIfDiscreteValuesEqual
* Count numbers
* Standard deviation
* Standard deviation of population
* Variance
* Variance of population

### Through code behind

Refer the following code sample to implement summary type through code behind.

{% highlight c# %}

    private PivotReport BindDefaultData()
        {
            PivotReport pivotSetting = new PivotReport();

            //...

            pivotSetting.PivotCalculations.Add(new PivotComputationInfo { CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum });
          
            return pivotSetting;
        }

{% endhighlight %}

### Through UI interaction

You can change summary types at run-time through built-in context menu for respective value field. Once the summary type is selected, the corresponding pivot item will be updated with the respective summary type. 

![Summary types in JavaScript pivot client server mode](Getting-Started_images/server_mode_summary.png)

To achieve this behavior at run-time, add the following `ChangeSummaryType` method in WebAPI/WCF service. 

### WebAPI

{% highlight c# %}

    [System.Web.Http.ActionName("ChangeSummaryType")]
    [System.Web.Http.HttpPost]
    public Dictionary<string, object> ChangeSummaryType(Dictionary<string, object> jsonResult)
        {
            pivotClient.PopulateData(jsonResult["currentReport"].ToString());
            var dictionary = pivotClient.GetJsonData(jsonResult["action"].ToString(), ProductSales.GetSalesData(), jsonResult["summaryType"].ToString());
            return dictionary;
        }

{% endhighlight %}

### WCF

{% highlight c# %}

    public Dictionary<string, object> ChangeSummaryType(string action, string currentReport, string summaryType)
        {
            pivotClient.PopulateData(currentReport);
            return pivotClient.GetJsonData(action, ProductSales.GetSalesData(), summaryType);
        }

{% endhighlight %}
