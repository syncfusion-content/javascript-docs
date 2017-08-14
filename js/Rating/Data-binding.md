---
layout: post
title: Data-binding
description: data-binding
platform: js
control: Rating
documentation: ug
api: /api/js/ejrating
---

# Data-binding

## KnockoutJS Binding

**KnockoutJS** support allows you to bind the **HTML** elements with any of the available data models. For Knockout Binding, you can include the files **knockout-min.js** and **ej.widget.ko.min**.

**KnockoutJS Binding** is of two types:

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the Rating control. But the changes made in Rating control are not reflected and triggered in the observable collection. This kind of binding is applied to all the properties of the Rating control.

**Two-way binding** supports both the processes; it applies the observable values to the Rating properties and the changes made in the Rating control are also reflected back and triggered within the observable collections. The Rating property that supports two-way binding is value.

Apply the plugin and the property assigning the **Rating** element through the directive that starts with the letter “e-“. 

The following example depicts the way to bind data to the **Rating** control through **Knockout** support.

 Add the following HTML to render rating with KnockoutJS support.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
   <head>
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.ko.min.js"></script>
   </head>
   <body>
      <div class="control" style="float: left">
         <div class="ctrl-label"></div>
         <input id="apiRating" type="text" class="rating" data-bind="ejRating: { value: ratingValue, width: '161px', precision: 'exact' }" />
      </div>
      <div class="control" style="float: left; margin-left: 20px; height: 30px">
         <div class="ctrl-label"></div>
         <input type="text" name="rating" class="input ejinputtext" value="" data-bind="value: ratingValue" />
      </div>
      <script type="text/javascript">
         window.viewModel = {
             ratingValue: ko.observable(3),
         };
         
         $(function () {
             ko.applyBindings(viewModel);
         });
         
      </script>
      <style type="text/css">
         .control {
               margin-top: 10px;
         }
         .input {
               height: 27px;
               text-indent: 10px;
               width: 81%;
         }
      </style>
   </body>
</html>


{% endhighlight %}


The following screenshot illustrates **Rating** with **Knockout** support.

![](/js/Rating/Data-binding_images/Data-binding_img1.png) 

## AngularJS Binding

For AngularJS Binding, you can include angular.min.js, ej.unobtrusive.min.js, and ej.widget.angular.min.js files. Rating control is availed with two types of AngularJS support namely, 

* One-way binding
* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the Rating control. But the changes made in Rating control are not reflected or triggered in the scope collection. This kind of binding is applied to all the properties of the Rating control.

**Two-way binding** supports both the processes; it applies the scope values to the Rating properties and also the changes made in the Rating control are reflected back and triggered within the AngularJS scope change function. The Rating property called Value supports **two-way binding**.

Apply the plugin and property assigning the **Rating** element through the directive that starts with the letter **“e-“.** 

The following example depicts the way to bind data to the **Rating** control by **angular** support.

 Add the following HTML to render Rating with AngularJS support.

{% highlight html %}

<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="syncApp">
   <head>
      <title>Essential Studio for JavaScript :  AngularJS</title>
      <!-- style sheet for default theme(flat azure) -->
      <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
      <!--scripts-->
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
      <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js"></script>
      <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/ej.widget.angular.min.js"></script>
   </head>
   <body ng-controller="RatingCtrl">
      <table>
         <th>
            <div id="control">
               <input id="apiRating" type="text" class="rating" ej-rating e-value="ratingValue">
            </div>
         </th>
         <th>
            <div id="binding">
               <input type="text" class="input ejinputtext" name="rating" value="" ng-model="ratingValue" />
            </div>
         </th>
      </table>
      <script type="text/javascript">
         angular.module('syncApp', ['ejangular'])
         .controller('RatingCtrl', function ($scope) {
           $scope.ratingValue = 3;
         });
         
      </script>
      <style type="text/css" class="cssStyles">
         #binding {
            margin-left: 150px;
         }
         .control {
            margin-top: 10px;
         }
         .input {
            height: 27px;
            text-indent: 10px;
            width: 81%;
         }
      </style>
   </body>
</html>

{% endhighlight %}



The following screenshot displays the output of **Rating** with **Angular** support.

![](/js/Rating/Data-binding_images/Data-binding_img2.png) 

