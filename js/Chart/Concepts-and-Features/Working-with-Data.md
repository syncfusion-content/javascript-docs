---
layout: post
title: Working-with-Data
description: working with data
platform: js
control: Chart
documentation: ug
---

# Working with Data

Chart gets data either locally or remotely. To populate the Chart with data, you can use the **dataSource** in **series** properties.

## Local Data

**EjChart** provides you an option to bind the data to the Chart using the **dataSource** property of the series.

{% highlight js %}


        var dataVal = [
            {"FoodName": "CHEESE BURGER", "Calorie": 100, "Protein": 15, "Fat": 15 },
            { "FoodName": "PIZZA", "Calorie": 100, "Protein": 15, "Fat": 9 },
            { "FoodName": "CHICKEN NOODLE", "Calorie": 50, "Protein": 4, "Fat": 2 },
            { "FoodName": "YOGURT", "Calorie": 75, "Protein": 10, "Fat": 2 },
            { "FoodName": "BEEF SANDWICH", "Calorie": 125, "Protein": 22, "Fat": 13}
        ];
        $("#chartcontainer").ejChart({     
            series: [{                        
                dataSource: dataVal,
                xName: 'FoodName', 
                yName: 'Calorie',
                type:'column'

            },
            {
                dataSource: dataVal,
                xName: 'FoodName',
                yName: 'Protein',
                type: 'column'
            }
            ],                      
            // ...                       
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Working-with-Data_images/Working-with-Data_img1.png" Caption="Chart with local data"%}

## Remote Data

You can bind the **ejChart** to remote data using **DataManager** and the **query** in series that is used to retrieve the data by creating queries. Data manager supports the following types of data binding.

1. JSON

2. Web Services

3. oData

The following code example illustrates binding **ejChart** to oData service.   

{% highlight js %}


        $(function () {
            //Remote URL           
            var dataManger = new ej.DataManager({
                url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
            });
            // Query creation
            var query = ej.Query().from("Orders").take(6);
            $("#chartcontainer").ejChart({
                series: [{
                    type: 'column',
                    dataSource: dataManger,
                    xName: "ShipCity",
                    yName: "Freight",
                    query: query,
                }],
            });
        });


{% endhighlight %}



{% include image.html url="/js/Chart/Concepts-and-Features/Working-with-Data_images/Working-with-Data_img2.png" Caption="Chart with Remote data"%}

