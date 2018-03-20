---
layout: post
title: Data binding
description: Learn how to bind Sparkline with local data.
platform: js
control: Sparkline
documentation: ug
api: /api/js/ejsparkline
---

# Working with Data

## Local Data

1. You can bind the data to the Sparkline by using [`dataSource`](../api/ejsparkline#members:datasource) property and then you need to map the **X** and **Y** value with [`xName`](../api/ejsparkline#members:xname) and [`yName`](../api/ejsparkline#members:yname) properties respectively.

{% highlight javascript %}

var sparkLineData = [
{ employeeId: 1, sales: 25 },
{ employeeId: 2, sales: 28 },
{ employeeId: 3, sales: 34 },
{ employeeId: 4, sales: 32 },
{ employeeId: 5, sales: 40 },
{ employeeId: 6, sales: 32 },
{ employeeId: 7, sales: 35 },
{ employeeId: 8, sales: 55 },
{ employeeId: 9, sales: 38 },
{ employeeId: 10, sales: 30 }];
    
$("#container").ejSparkline({	
     dataSource: sparkLineData,
     xName: "employeeId",
     yName: "sales",
});

{% endhighlight %}


![](/js/Sparkline/Working-with-Data_images/Working-with-Data_img1.png); 

2. You can also bind an array of data to Sparkline by using [`dataSource`](../api/ejsparkline#members:datasource) property.  

{% highlight javascript %}

$("#container").ejSparkline({  
      // ...
      dataSource:[ 2, 6, -1, 1, 12, 5, -2, 7, -3, 5, 8, 10],
      // ...
   });

{% endhighlight %}

![](/js/Sparkline/Working-with-Data_images/Working-with-Data_img2.png); 

## AngularJS Support

Typically, you will assign data directly to Sparkline using [`dataSource`](../api/ejsparkline#members:datasource) property. In AngularJS, you need to bind the variable, which contains data in the AngularJS scope object, to the dataSource property as illustrated in the following code example.

{% highlight javascript %}

<html ng-app="syncApp">
     <head>
         <script type="text/javascript" src="http://cdn.syncfusion.com/js/assets/external/jquery-2.1.4.min.js"></script>
         <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>
         <script src="https://cdn.syncfusion.com/14.2.0.26/js/web/ej.web.all.min.js"></script>
         <script src="https://cdn.syncfusion.com/14.2.0.26/js/common/ej.widget.angular.min.js"></script>
     </head>
<body ng-controller="sparkline">
<div id="column" ej-sparkline e-datasource="sparkLineData"></div>
<script>
    var data = [2, 6, -1, 1, 12, 5, -2, 7, -3, 5, 8, 10, ];	 
  
   angular.module('syncApp',['ejangular']).controller("sparkline",function($scope){    
    $scope.sparkLineData = data;
});
</script>
</body>
</html>

{% endhighlight %}

