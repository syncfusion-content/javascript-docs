---
layout: post
title: data-binding
description: data-binding
platform: js
control: Rating
documentation: ug
---

# Data-binding

## Knockout Binding

**Knockout** support allows you to bind the **HTML** elements with any of the available data models.

For **Knockout****Binding**, you can include the files **knockout-min.js** and **ej.widget.ko.min**.

**Knockout Binding** is of two types:

* One-way binding

* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **Rating** control. But the changes made in **Rating** control are not reflected and triggered in the observable collection. This kind of binding is applied to all the properties of the **Rating** control.

**Two-way binding** supports both the processes; it applies the observable values to the **Rating** properties and the changes made in the **Rating** control are also reflected back and triggered within the observable collections. The **Rating** property that supports two-way binding is **value.**

Apply the plugin and the property assigning the **Rating** element through the directive that starts with the letter “e-“**.** 

The following example depicts the way to bind data to the **Rating** control through K**nockout** support.

* Add the following **HTML** to render rating with **Knockout** support.

{% highlight html %}

**[HTML]**

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"></script>
</head>
<body>
    <div class="control" style="float: left">
        <div class="ctrllabel"></div>
        <input id="apiRating" type="text" class="rating" data-bind="ejRating: { value: ratingValue, width: '161px', precision: 'exact' }" />
    </div>
    <div class="control" style="float: left; margin-left: 20px; height: 30px">
        <div class="ctrllabel"></div>
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

<head>
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
    <!--scripts-->
script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <!--Scripts for Knockout support-->
     <script src="http://cdn.syncfusion.com/js/assets/external/knockout.min.js"></script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js)"></script>
</head>
<body>    
    <div id="container" style="border: 1px solid black; width: 300px; padding: 2px">
        <table>
            <tr>
                <td valign="top">Full Precision:
                </td>
                <td>
                   <input id="apiRating" type="text" class="rating" data-bind="ejRating: { value: ratingValue, width: '161px', precision: 'exact' }" />

                </td>
            </tr>   
            <tr>
                <td valign="top">Half Precision:
                </td>
                <td>
                    <input type="text" name="rating" class="input ejinputtext" value="" data-bind="    value: ratingValue" />

                </td>
            </tr>  

        </table>
    </div>


{% endhighlight %}









**[JS]**

// Add the following script to render Rating with Knockout support.



    &lt;script type="text/javascript"&gt;        

        var raingObj;

        $(function () {

            // declaration            

            raingObj = $("#apiRating").data("ejRating");

            $("#btnGetValue").ejButton({ "click": "onGetValueClck", "width": "87px" });

        });

        window.viewModel = {

            ratingValue: ko.observable(3),

        };



        $(function () {

            ko.applyBindings(viewModel);

            raingObj = $("#apiRating").data("ejRating");

        });       



        function onResetClck() {

            raingObj.reset();

        }

    &lt;/script&gt;





<table>
<tr>
<td>
<b>[CSHTML]</b><b>// Add the following code example to the corresponding CSHTML page to render Rating with Knockout support.</b>&lt;script src="@Url.Content("~/Scripts/knockout-min.js")"&gt;&lt;/script&gt;&lt;script src="@Url.Content("~/Scripts/ej.unobtrusive.min.js")"&gt;&lt;/script&gt;&lt;script src="@Url.Content("~/Scripts/ej.widget.ko.min.js")"&gt;&lt;/script&gt;&lt;div id="container" style="border: 1px solid black; width: 300px; padding: 2px"&gt;    &lt;table&gt;        &lt;tr&gt;            <td valign="top">Rating:            &lt;/td&gt;            &lt;td&gt;              &lt;input id="ApiRating" type="text" class="rating" data-bind="ejRating: { value:ratingValue}" &gt;             &lt;/td&gt;        &lt;/tr&gt;         &lt;tr&gt;            <td valign="top">Rating:            &lt;/td&gt;            &lt;td&gt;              &lt;input type="text" name="rating"  class="ejinputtext input" data-bind="value: ratingValue" /&gt;                &lt;/td&gt;        &lt;/tr&gt;    &lt;/table&gt;&lt;/div&gt; </td></tr>
<tr>
<td>
<b>[JS]</b>    &lt;script&gt;    var ratingObj;    $(function () {        window.viewModel = {            ratingValue: ko.observable(3),        };        ko.applyBindings(viewModel);                ratingObj = $("#apiRating").data("ejRating");    });       &lt;/script&gt;</td></tr>
</table>


**[ASPX]**

**// Add the following code example to the corresponding ASPX page to render Rating with knockout support.**



&lt;head&gt;

&lt;link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" /&gt;

    &lt;!--scripts--&gt;

    &lt;script src="http://code.jquery.com/jquery-1.10.2.min.js"&gt;&lt;/script&gt;

    &lt;script src="http://ajax.aspnetcdn.com/ajax/globalize/0.1.1/globalize.min.js"&gt;&lt;/script&gt;

    &lt;script src="http://cdnjs.cloudflare.com/ajax/libs/jquery-easing/1.3/jquery.easing.min.js"&gt;&lt;/script&gt;   

&lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"&gt;&lt;/script&gt;

    &lt;!--Scripts for Knockout support--&gt;

     &lt;script src="Content/knockout-min.js"&gt;&lt;/script&gt;

&lt;script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js"&gt;&lt;/script&gt;

&lt;/head&gt;

&lt;body&gt;    

&lt;div id="Div2" style="border: 1px solid black; width: 300px; padding: 2px"&gt;

    &lt;table&gt;

        &lt;tr&gt;

            <td valign="top">Rating:&lt;/td&gt;

            &lt;td&gt;

                &lt;input id="Text1" type="text" class="rating" data-bind="ejRating: { value: ratingValue, width: '161px', precision: 'exact' }" /&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

        &lt;tr&gt;

            <td valign="top">Value:&lt;/td&gt;

            &lt;td&gt;

                &lt;input type="text" name="rating" class="input ejinputtext" value="" data-bind="    value: ratingValue" /&gt;

            &lt;/td&gt;

        &lt;/tr&gt;

    &lt;/table&gt;

&lt;/div&gt;





**[JS]**

**// Add the following scripts to render Rating with knockout support.**



&lt;script type="text/javascript"&gt;

    var raingObj;

    $(function () {

        // declaration            

        raingObj = $("#apiRating").data("ejRating");

        $("#btnGetValue").ejButton({ "click": "onGetValueClck", "width": "87px" });

    });

    window.viewModel = {

        ratingValue: ko.observable(3),

    };



    $(function () {

        ko.applyBindings(viewModel);

        raingObj = $("#apiRating").data("ejRating");

    });



    function onResetClck() {

        raingObj.reset();

    }

&lt;/script&gt;



The following screenshot illustrates **Rating** with **Knockout** support.



{% include image.html url="\js\Rating\concepts-and-features\data-binding_images\data-binding_img1.png" Caption="Figure 135: Rating-Knockout Binding"%}{% include image.html url="\js\Rating\concepts-and-features\data-binding_images\data-binding_img2.png" Caption="Figure 135: Rating-Knockout Binding"%}

## Angular Binding

For **Angular Binding**, you can include **angular.min.js, ej.unobtrusive.min.js,** and **ej.widget.angular.min.js** files**.**

**Rating** control is availed with two types of **angular JS** support namely, 

* One-way binding

* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **Rating** control. But the changes made in **Rating** control are not reflected or triggered in the scope collection. This kind of binding is applied to all the properties of the **Rating** control.

**Two-way binding** supports both the processes; it applies the scope values to the **Rating** properties and also the changes made in the **Rating** control are reflected back and triggered within the angular scope change function. The **Rating** property called **Value** supports **two-way binding**.

Apply the plugin and property assigning the **Rating** element through the directive that starts with the letter **“e-“.** 

The following example depicts the way to bind data to the **Rating** control by **angular** support.

* Add the following **HTML** to render **Rating** with **angular** support.

{% highlight html %}

**[HTML]**
<!doctype html>
<html xmlns="http://www.w3.org/1999/xhtml" ng-app="syncApp">
<head>
    <title>Essential Studio for JavaScript :  Angular</title>
    <!-- style sheet for default theme(flat azure) -->
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"></script>
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"> </script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"></script>
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

<!doctype html>
<html lang="en" ng-app="syncApp">
<head>
    <meta charset="utf-8">
    <title>Essential Studio for JavaScript : AutoComplete - Angular support</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <!-- Style sheet for default theme (flat azure) -->
<linkhref="[http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css](http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css)"rel="stylesheet"/>
    <!--Scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js"></script>

<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js)"></script>
    <scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js](http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js)"> </script>
<scriptsrc="[http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js](http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js)"> </script>

</head>
<body ng-controller="RatingCtrl">
    <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div class="frame" style="width: 50%">
                    <div style="width: 90%; margin: auto">
                        <div id="control" style="float: left; width: 45%">
                            <input id="apiRating" type="text" class="rating" ej-rating e-value="ratingValue">
                            <h6><span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 10px;">Note:Two Way Angular Support</span></h6>
                        </div>
                        <div id="binding" style="float: right; width: 45%">
                            <input type="text" class="input ejinputtext" name="rating" value="" ng-model="ratingValue" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    **</div>**


{% endhighlight %}







**[JS]**

**// Add the following script to render Rating with angular support.**



    &lt;script type="text/javascript"&gt;

        angular.module('syncApp', ['ejangular'])

            .controller('RatingCtrl', function ($scope) {

                $scope.ratingValue = 3;

            });

    &lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



**[CSHTML]**

**// Add the following code example to the corresponding CSHTML page to render Rating with angular support.**



&lt;script src="@Url.Content("~/Scripts/angular.min.js")"&gt;&lt;/script&gt;

&lt;script src="@Url.Content("~/Scripts/ej.unobtrusive.min.js")"&gt;&lt;/script&gt;

&lt;script src="@Url.Content("~/Scripts/ej.widget.angular.min.js")"&gt;&lt;/script&gt;

&lt;div style="border: 1px solid black; width: 520px; padding: 30px; height:80px"&gt;

    &lt;div ng-app="syncApp"&gt;

        &lt;div ng-controller="RatingCtrl"&gt;

            &lt;div class="frame" style="width: 50%"&gt;

                &lt;div style="width: 90%; margin: auto"&gt;

                    &lt;div id="control" style="float: left; width: 45%"&gt;

                        &lt;input id="apiRating" type="text" class="rating" ej-rating e-value="ratingValue"&gt;

                        &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; margin-top: 10px;">Note:Two Way Angular Support</span>&lt;/h6&gt;

                    &lt;/div&gt;

                    &lt;div id="binding" style="float: right;width:0"&gt;

                        &lt;input type="text" class="input ejinputtext" name="rating" ng-model="ratingValue" /&gt;

                    &lt;/div&gt;

                &lt;/div&gt;

            &lt;/div&gt;

            &lt;script&gt;

                angular.module('syncApp', ['ejangular'])

                    .controller('RatingCtrl', function ($scope) {

                        $scope.ratingValue = 3;

                    });

            &lt;/script&gt;

        &lt;/div&gt;

    &lt;/div&gt;

&lt;/div&gt;





The following screenshot displays the output of **Rating** with **Angular** support.



{% include image.html url="\js\Rating\concepts-and-features\data-binding_images\data-binding_img3.png" Caption="Figure 146: Rating-Angular Binding "%}{% include image.html url="\js\Rating\concepts-and-features\data-binding_images\data-binding_img4.png" Caption="Figure 146: Rating-Angular Binding "%}

