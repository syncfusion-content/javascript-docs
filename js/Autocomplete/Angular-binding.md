---
layout: post
title: Angular-binding
description: angular binding
platform: js
control: AutoComplete
documentation: ug
---

# Angular binding

**AutoComplete** widget is availed with two types of **angularJS** support namely, 

* One-way binding
* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the AutoComplete widget. The changes made in AutoComplete widget are not reflected or triggered in turn to the scope collection. This kind of binding is applied to all the properties of the AutoComplete widget.

**Two-way binding** supports both the processes. It applies the scope values to the AutoComplete properties, as well as the changes made in the AutoComplete widget are reflected back and triggered within the angular scope change function.

Apply the plugin and property assigning to the AutoComplete widget element through the directive that starts with **“e-“.**

To know more about the **Angular** binding, you can refer the online documentation in the following link location,

<http://help.syncfusion.com/js/angularjs>

The following code example depicts the way to bind data to the **AutoComplete** widget through **angular** support.

{% highlight html %}

<!doctype html>
<html lang="en" ng-app="syncApp">
   <head>
      <meta charset="utf-8">
      <title>Essential Studio for JavaScript : AutoComplete - Angular support</title>
      <meta name="viewport" content="width=device-width, initial-scale=1.0" 
         charset="utf-8"  />
      <!--scripts-->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js "> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
   </head>
   <body ng-controller="AutocompleteCtrl">
      <div class="content-container-fluid">
         <div class="row">
            <div class="cols-sample-area">
               <div class="" style="width: 40%;height:38px;">
                  <span style="display:block">Select Bike</span>					
                  <div id="control" style="float: left;width:45%">
                     <input type="text" ej-autocomplete e-datasource="dataList" e-value="setValue" />
                     <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 5px;">Note:Two Way Angular Support</span></h6>
                  </div>
                  <div id="binding" style="float: right;width:45%">
                     <input type="text" name="AutoComplete" class="input ejinputtext" ng-model="setValue" />
                  </div>
               </div>
            </div>
         </div>
      </div>
      <script type="text/javascript">	
         var carList = [
              "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
              "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
              "Chevrolet Camaro", "Cadillac ",
              "Duesenberg J ", "Dodge Sprinter",
              "Elantra", "Excavator",
              "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
              "GAZ Siber",
              "Honda S2000", "Hyundai Santro",
              "Isuzu Swift", "Infiniti Skyline",
              "Jaguar XJS",
              "Kia Sedona EX", "Koenigsegg Agera",
              "Lotus Esprit", "Lamborghini Diablo ",
              "Mercedes-Benz ", "Mercury Coupe", "Maruti Alto 800",
              "Nissan Qashqai",
              "Oldsmobile S98", "Opel Superboss",
              "Porsche 356 ", "Pontiac Sunbird",
              "Scion SRS/SC/SD", "Saab Sportcombi", "Subaru Sambar", "Suzuki Swift",
              "Triumph Spitfire ", "Toyota 2000GT",
              "Volvo P1800", "Volkswagen Shirako"
         ];	
         angular.module('syncApp', ['ejangular'])
         .controller('AutocompleteCtrl', function ($scope) {
         $scope.setValue = "Dodge Sprinter";
         $scope.dataList = carList;
         });
      </script>
      <style type="text/css">
         .control {
               margin-top: 10px;
         }
         .input
         {
               height:27px;
               text-indent: 10px;
               width:81%;
         }
      </style>
   </body>
</html>

{% endhighlight %}



The following is the output of **AutoComplete** control with two way **angular binding**.

![](/js/Autocomplete/Angular-binding_images/Angular-binding_img1.png)

