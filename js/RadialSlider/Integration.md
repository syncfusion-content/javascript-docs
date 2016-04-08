---
layout: post
title: Knockout-Support
description: knockout support
platform: js
control:RadialSlider 
documentation: ug
---

#Integration

# Knockout Support

**Knockout support** allows you to bind the **HTML** elements against any of the available data models. It is of two types**.**

* One-way binding
* Two-way binding

**One-way binding** refers to the process of applying observable values to all the available properties of the **RadialSlider** widget, but the changes made in **RadialSlider** widget are not reflected and triggered in turn to the observable collection. This kind of binding applies to all the properties of the **RadialSlider** widget.

**Two-way binding** supports both the processes; it applies the observable values to the **Textbox** widget properties as well as the changes made in the **RadialSlider** widget are also reflected back and triggered within the observable collections. 

For more information about the **knockout binding**, refer the following online documentation in the given link location,

<http://help.syncfusion.com/js/knockoutjs>

The following example depicts the way to bind data to the **RadialSlider** widgets through **knockout** **support** that enables and populates data to the **RadialSlider** widget based on the value set to the other **RadialSlider** widget.

{% highlight html %}

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>RadialSlider - Knockout Support</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css" rel="stylesheet"/>
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js" type="text/javascript"> </script>	
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script>    
        <script src="knockout.min.js" type="text/javascript"></script>
        <script src="ej.widget.ko.min.js" type="text/javascript"></script>
    </head>
    <body>
        <div class="content-container-fluid">
            <div class="row">
                <div class="cols-sample-area">
                    <div id="radialSlider" data-bind="ejRadialSlider: {value:sliderValue, innerCircleImageUrl:'../images/radialslider/chevron-right.png'}"></div>
                </div>
                <div id="sampleProperties">
                    <div class="prop-grid">
                        <div class="row">
                            <div class="col-md-3">
                                Value
                            </div>
                            <div class="col-md-3">
                                <input type="text" name="slider" class="input ejinputtext" value="" data-bind="value: sliderValue" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <script type="text/javascript">
            $(function () {
                window.viewModel = {
                    sliderValue: ko.observable(40),
                };
                ko.applyBindings(viewModel);
            });
        </script>
        <style type="text/css" class="cssStyles">
            .input {
                height: 22px;
                text-indent: 10px;
                width: 100px;
            }
        </style>
    </body>
    </html>

{% endhighlight %}

# Angular Support

The **RadialSlider** widget supports two types of **Angular JS support** namely, 

* One-way binding
* Two-way binding 

**One-way binding** refers to the process of applying scope values to all the available properties of the **RadialSlider** widget, but the changes made in **RadialSlider** widget are not reflected or triggered in turn to the scope collection. This kind of binding applies to all the properties of the **RadialSlider** widget.

**Two-way binding** supports both the processes; it applies the scope values to the **RadialSlider** properties as well as the changes made in the **RadialSlider** widget also get reflected back and triggered within the angular scope change function.

Apply the plugin and property assigning to the **RadialSlider** widget element through the directive that starts with the letter **“e-“.**

To know more details about the **Angular binding**, refer the following link location,

<http://help.syncfusion.com/js/angularjs>

The following example depicts the way to bind data to the **RadialSlider** widget through **angular support**.

{% highlight html %}

    <!DOCTYPE html>
    <html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>RadialSlider - Angular Support</title>
        <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
        <link href="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/responsive-css/ej.responsive.css" rel="stylesheet"/>
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.11.3.min.js" type="text/javascript"> </script>	
        <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/js/assets/external/angular.min.js" type="text/javascript"></script>
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/web/ej.web.all.min.js" type="text/javascript"></script> 	
        <script src="http://cdn.syncfusion.com/{{ site.releaseversion }}/js/common/ej.widget.angular.min.js" type="text/javascript"></script>
        <style type="text/css" class="cssStyles">
            .input {
                height: 22px;
                text-indent: 10px;
                width: 100px;
            }
        </style>
        </head>
        <body ng-controller="radialSliderCtrl">
        <div class="content-container-fluid">
            <div class="row">
                <div class="cols-sample-area">
                    <div id="angularRadialSlider" ej-radialslider e-value="sliderValue" e-innercircleimageurl="../images/radialslider/chevron-right.png"></div>
                </div>
                <div id="sampleProperties">
                    <div class="prop-grid">
                        <div class="row">
                            <div class="col-md-3">
                                Value
                            </div>
                            <div class="col-md-3">
                                <input type="text" name="radialslider" class="input ejinputtext" value="" ng-model="sliderValue" />
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
        <script>
            angular.module('radialSliderApp', ['ejangular']).controller('radialSliderCtrl', function ($scope) {
                $scope.sliderValue = 60;
            });
        
        </script>
    </body>
    </html>

{% endhighlight %}