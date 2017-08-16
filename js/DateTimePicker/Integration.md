---
layout: post
title: Integration
description: integration
platform: js
control: DateTimePicker
documentation: ug
api: /api/js/ejdatetimepicker
---

# Integration

## AngularJS Support

**AngularJS** is an open-source web application Framework. **AngularJS** extends HTML with new attributes. **AngularJS** is a JavaScript Framework. It can be added to an **HTML** page with a **&lt;script&gt;** tag. **AngularJS** extends **HTML** attributes with **Directives**, and binds data to **HTML** with **Expressions**. The support is achieved by an integration JS library file. You can know more about the AngularJS support in our documentation. You can find the online documentation in the following link location. 

<https://help.syncfusion.com/js/angularjs>

Sometimes you need to use **DateTimePicker** value for sorting and retrieving the information from database. Consider you are going to sort the number of users registered in your site. Whenever you select the date and time from the **DateTimePicker** popup window the result of sorting should be changed based on date and timings. To achieve this, date and time value has to bind to the model while you change the value of date and time in **DateTimePicker** control. You can achieve data binding with lesser code by integrating the AngularJS concept with your control.  

In the following example the **DateTimePicker** value is bound with simple textbox. The textbox values are updated while updating the values in **DateTimePicker** control. And also changing the date and time information from textbox is reflected in **DateTimePicker** control.

Add the following code in your **HTML** page.



{% highlight html %}
  
<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="DateTimeCtrl">
   <head>
      <title>Essential Studio for JavaScript :  AngularJS</title>
      <!-- style sheet for default theme(flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
   </head>
   <body ng-controller="DateTimePickerCtrl">
      <table>
         <th>
            <div id="control">
               <input type="text" id="dateTime" ej-datetimepicker e-value="value" e-width="width" e-open='isOpen' e-close='isClose' e-change='isChange' />
            </div>
         </th>
         <th>
            <div id="binding">
               <input type="text" id="dateTime1" ej-datetimepicker e-value="value" e-width="width" />
            </div>
         </th>
      </table>
      <script type="text/javascript">
         // Add the code in your script section to render DateTimePicker with AngularJS Binding
         
         angular.module('DateTimeCtrl', ['ejangular'])
         .controller('DateTimePickerCtrl', function ($scope) {
             $scope.value = "9/17/2014 2:47 AM";
             $scope.width = "200px";
         });
         
      </script>
      <style type="text/css" class="cssStyles">
         #binding {
         margin-left: 150px;
         }
      </style>
   </body>
</html>

{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

![](/js/DateTimePicker/Integration_images/Integration_img1.png)

## Knockout Support

**KnockoutJS** is a **MVVM** library that allows the separation of concerns. **Essential** **JavaScript** has full support for **KnockoutJS**. **Knockout support** is achieved by an integrated **JS** library file. Add the following code for **Knockout Binding** menu rendering.

If you use **KO** with your applications, you can get following benefits:

* You can connect UI elements with data model anytime. 
* Easily create complex dynamic data model.  
* Automatically update UI when data model is changed. When UI is changed data model is changed automatically. 


Add the following code in your **HTML** page.


{% highlight html %}
   
<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
   <head>
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
   </head>
   <body>
      <table>
         <th>
            <div id="control">
               <input type="text" id="dateTime" data-bind="ejDateTimePicker: { value: value, width: '160px' }" />
            </div>
         </th>
         <th>
            <div id="control1">
               <input type="text" id="Text1" data-bind="ejDateTimePicker: { value: value, width: '160px' }" />
            </div>
         </th>
      </table>
      <script type="text/javascript">
         // Add the code in your script section to render the DateTimePicker with Knockout binding
         
         window.viewModel = {
             value: ko.observable("3/18/2014 2:47 AM")
         };
         
         $(function () {
             // declaration
             ko.applyBindings(viewModel);
         });
         
      </script>
      <style type="text/css" class="cssStyles">
         #control1 {
               margin-left: 150px;
         }
      </style>
   </body>
</html>


{% endhighlight %}


![](/js/DateTimePicker/Integration_images/Integration_img2.png)

