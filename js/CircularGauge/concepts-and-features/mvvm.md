---
layout: post
title: mvvm
description: mvvm
platform: js
control: Circular Gauge
documentation: ug
---

# MVVM

**Angular JS**

**Circular Gauge** contains angular support. You can add object, as well as array object in the **Circular Gauge**. The two way binding support is given to the pointer **value**, **minimum** scale value and **maximum** scale value. 

**Rendering the Circular gauge**

**ej-CircularGauge** is the control tag in which **ej** is tag prefix and **CircularGauge** is the control name.

The following code example helps you to render **Circular Gauge**.

 &lt;!--To Render the Circular gauge--&gt;

&lt;!doctype html&gt;

&lt;html ng-app="syncApp"&gt;

&lt;head&gt;

&lt;!—Refer the necessary script here--&gt;

&lt;/head&gt;

&lt;body ng-controller="CircularGauge"&gt;

<ej-CircularGauge id="CircularGauge1" e-backgroundColor="transparent" e-value="50"

                  e-width="500" e-readOnly="false" e-load= "loadGaugeTheme" 

                  e-enableAnimation="false">

&lt;/ej-CircularGauge&gt;



&lt;/body&gt;

&lt;/html&gt;





Execute the above code to render the output as follows.

![](mvvm_images\mvvm_img1.png)

Figure 68: Default Circular gauge in Angular JS

**Adding Scale collection**

**Scale** is an array object and the inner tag is used for it. Object in the array collection (i.e. border) is extended with hyphen in the same tag.

**Example**: e-border-width and e-border-color. 

&lt;!--To Render the Circular gauge--&gt;



&lt;ej-CircularGauge id="CircularGauge1"&gt;



&lt;!--Adding Scale collection to the Circular gauge--&gt;



     &lt;e-scales&gt;

          <e-scale e-showRanges="true" e-startAngle="122" e-sweepAngle="296" 

                   e-radius="130" e-showScaleBar="true" e-size="1" e-maximum="120" 

                   e-majorIntervalValue="20" e-minorIntervalValue="10" 

                   e-border-width="0.5">



          &lt;/e-scale&gt;

     &lt;/e-scales&gt;



&lt;/ej-CircularGauge&gt;





Execute the above code to render the following output.

![](mvvm_images\mvvm_img2.png)

Figure 69: Circular gauge with scale customization in Angular JS

**Adding pointer collection**

**Pointer** is an array object and you can use the inner tag for it. Object in the array collection (i.e. pointer cap) is extended with hyphen in the same tag.

**Example**: e-pointerCap-radius. 

&lt;!--To Render the Circular gauge--&gt;



&lt;ej-CircularGauge id="CircularGauge1"&gt;



&lt;!--Adding Scale collection to the Circular gauge--&gt;



     &lt;e-scales&gt;

          &lt;e-scale&gt;

              &lt;!--Adding pointer collection to the scale collection--&gt;



              &lt;e-pointers&gt;

                   <e-pointer e-showBackNeedle="true" e-backNeedleLength="20" 

                              e-length="95" e-width="7" e-value="80" 

                              e-pointerCap-radius="12">

                   &lt;/e-pointer&gt;

              &lt;/e-pointers&gt;



          &lt;/e-scale&gt;

     &lt;/e-scales&gt;



&lt;/ej-CircularGauge&gt;





Execute the above code to render the output as follows.

![](mvvm_images\mvvm_img3.png)

Figure 70: Circular gauge with pointer customization in Angular JS

**Adding label collection**

**Label** is also an array object. You can use the inner tag for it. 

&lt;!--To Render the Circular gauge--&gt;



&lt;ej-CircularGauge id="CircularGauge1"&gt;



&lt;!--Adding Scale collection to the Circular gauge--&gt;



     &lt;e-scales&gt;

          &lt;e-scale&gt;

              &lt;!--Adding pointer collection to the scale collection--&gt;

              &lt;e-pointers&gt;…&lt;/e-pointers&gt;

              &lt;!--Adding labels collection to the scale collection--&gt;



              &lt;e-labels&gt;

                   &lt;e-label e-color="#8c8c8c"&gt;

                   &lt;/e-label&gt;

              &lt;/e-labels&gt;



          &lt;/e-scale&gt;

     &lt;/e-scales&gt;



&lt;/ej-CircularGauge&gt;





Execute the above code to render the following output.

![](mvvm_images\mvvm_img4.png)

Figure 71: Circular gauge with label customization in Angular JS

**Adding Tick collection**

**Tick** is an array object. You can use the inner tag for it. 

&lt;!--To Render the Circular gauge--&gt;



&lt;ej-CircularGauge id="CircularGauge1"&gt;



&lt;!--Adding Scale collection to the Circular gauge--&gt;



     &lt;e-scales&gt;

          &lt;e-scale&gt;

              &lt;!--Adding pointer collection to the scale collection--&gt;

              &lt;e-pointers&gt;…&lt;/e-pointers&gt;

              &lt;!--Adding labels collection to the scale collection--&gt;

              &lt;e-labels&gt;…&lt;/e-labels&gt;

              &lt;!--Adding ticks collection to the scale collection--&gt;



              &lt;e-ticks&gt;

                   <e-tick e-type="major" e-distanceFromScale="2" e-height="16" 

                           e-width="1" e-color="#8c8c8c">

                   &lt;/e-tick&gt;

                   <e-tick e-type="minor" e-distanceFromScale="2" e-height="8" 

                           e-width="1" e-color="#8c8c8c">

                   &lt;/e-tick&gt;

              &lt;/e-ticks&gt;



          &lt;/e-scale&gt;

     &lt;/e-scales&gt;



&lt;/ej-CircularGauge&gt;





Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img5.png" Caption="Figure 72 : Circular gauge with ticks customization in Angular JS"%}

**Adding Range collection**

**Range** is an array object. You can use the inner tag for it. Object in the array collection (i.e. border) is extended with hyphen in the same tag.

**Example**: e-border-color. 

&lt;!--To Render the Circular gauge--&gt;



&lt;ej-CircularGauge id="CircularGauge1"&gt;



&lt;!--Adding Scale collection to the Circular gauge--&gt;



     &lt;e-scales&gt;

          &lt;e-scale&gt;

              &lt;!--Adding pointer collection to the scale collection--&gt;

              &lt;e-pointers&gt;…&lt;/e-pointers&gt;

              &lt;!--Adding labels collection to the scale collection--&gt;

              &lt;e-labels&gt;…&lt;/e-labels&gt;

              &lt;!--Adding ticks collection to the scale collection--&gt;

              &lt;e-ticks&gt;…&lt;/e-ticks&gt;

              &lt;!--Adding ranges collection to the scale collection--&gt;



              &lt;e-ranges&gt;

                   &lt;e-range e-distanceFromScale="-30" e-startValue="0" e-endValue="70"&gt;

                   &lt;/e-range&gt;

                   <e-range e-distanceFromScale="-30" e-startValue="70" 

                            e-endValue="110" e-backgroundColor="#fc0606" 

                            e-border-color="#fc0606">

                   &lt;/e-range&gt;

                   <e-range e-distanceFromScale="-30" e-startValue="110" 

                            e-endValue="120" e-backgroundColor="#f5b43f" 

                            e-border-color="#f5b43f">

                   &lt;/e-range&gt;

               &lt;/e-ranges&gt;



          &lt;/e-scale&gt;

     &lt;/e-scales&gt;



&lt;/ej-CircularGauge&gt;





Execute the above codes to render the Resultant gauge as follows.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img6.png" Caption="Figure 73: Circular gauge Rendered in Angular JS"%}

**Two Way Binding** 

**Circular Gauge** support the two way binding for the property **value, minimum and maximum** as mentioned earlier. The following code example explains how to achieve the two way binding to the **Circular Gauge**.

&lt;!doctype html&gt;

&lt;html ng-app="syncApp"&gt;

&lt;head&gt;

&lt;!—Refer the necessary script here--&gt;

&lt;/head&gt;

&lt;body ng-controller="CircularGauge"&gt;

&lt;div id="linearframe"&gt;

&lt;ej-CircularGauge id="CircularGauge1" e-backgroundColor="transparent" e-value="nvalue" e-width="500" e-readOnly="false" e-load= "loadGaugeTheme" e-enableAnimation="false"&gt;

      &lt;e-scales&gt;

            <e-scale e-showRanges="true" e-startAngle="122" e-sweepAngle="296"

                     e-radius="130" e-showScaleBar="true" e-size="1"

                     &lt;!—binding maximum value using angular JS --&gt; 

**e-maximum="nmaximum"**

                     &lt;!—binding minimum value using angular JS --&gt; 

**e-minimum="nminimum"**

                     e-majorIntervalValue="20" 

                     e-minorIntervalValue="10" e-border-width="0.5">

             &lt;e-pointers&gt;

                    <e-pointer e-showBackNeedle="true" e-backNeedleLength="20" 

                               e-length="95" e-width="7" 

                               &lt;!—binding pointer value using angular JS --&gt; 

**e-value="nvalue"**

                               e-pointerCap-radius="12">

                    &lt;/e-pointer&gt;

             &lt;/e-pointers&gt;

             &lt;e-labels&gt;

                    &lt;e-label e-color="#8c8c8c"&gt;&lt;/e-label&gt;

             &lt;/e-labels&gt;

             &lt;e-ticks&gt;

                    <e-tick e-type="major" e-distanceFromScale="2" e-height="16" 

                            e-width="1" e-color="#8c8c8c">

                    &lt;/e-tick&gt;

                    <e-tick e-type="minor" e-distanceFromScale="2" e-height="8" 

                            e-width="1" e-color="#8c8c8c">

                    &lt;/e-tick&gt;

             &lt;/e-ticks&gt;

             &lt;e-ranges&gt;

                   &lt;e-range e-distanceFromScale="-30" e-startValue="0" e-endValue="70"&gt;

                   &lt;/e-range&gt;

                   <e-range e-distanceFromScale="-30" e-startValue="70"

                            e-endValue="110" e-backgroundColor="#fc0606" 

                            e-border-color="#fc0606">

                   &lt;/e-range&gt;

                   <e-range e-distanceFromScale="-30" e-startValue="110" 

                            e-endValue="120" e-backgroundColor="#f5b43f" 

                            e-border-color="#f5b43f">

                   &lt;/e-range&gt;

              &lt;/e-ranges&gt;

           &lt;/e-scale&gt;

      &lt;/e-scales&gt;

&lt;/ej-CircularGauge&gt;

&lt;/div&gt;

&lt;input type="text" id="txtMax" e-value="nvalue" ej-numerictextbox ng-model="nvalue"  e-decimalplaces="2" e-showspinbutton="false" Style="width:110px"/&gt;







&lt;script type="text/javascript"&gt;



        &lt;!—binding the value to the scope variables in application controller--&gt; 



        angular.module('syncApp', ['ejangular'])

             .controller('CircularGauge', function ($scope) {

                 $scope.nvalue = 50;

                 $scope.nminimum = 0;

                 $scope.nmaximum = 120;



             });

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img7.png" Caption="Figure 74: Circular gauge with two way binding in Angular JS"%}

**Knockout JS**

Knockout support allows you to bind the **HTML** elements against any of the available data models.

Two types of knockout binding is supported as of angular,

**one-way binding**

two-way binding

One way binding refers to the process of applying observable values to all the available properties of the Circular Gauge control, but the changes made in gauge control does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the circular gauge control.

* **Two-way binding** supports both the processes – it applies the observable values to the **Circular Gauge** properties as well as the changes made in the **Circular Gauge** control also reflects back and triggers within the observable collections. Only few of the schedule properties support two-way binding and they are as follows

* value

* maximum 

* minimum



&lt;!DOCTYPE html&gt;

&lt;html xmlns="http://www.w3.org/1999/xhtml"&gt;

&lt;head&gt;

    <title>Essential JavaScript for Knockout</title>

&lt;/head&gt;

&lt;body&gt;

    <div id="CircularGauge1" 

         data-bind="ejCircularGauge: { 

**value: samplevalue,**

                    **minimum: minimumValue,**

                    **maximum: maximumValue**

                    }">

    &lt;/div&gt;

    &lt;script type="text/javascript"&gt;

        $(function () {

            window.viewModel = {

                **value: ko.observable(50),**

                **minimum: ko.observable(0),**

                **maximum: ko.observable(150)**

            };

            $(function () {

                ko.applyBindings(viewModel);

            });

        });

    &lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



&lt;!DOCTYPEhtml&gt;

&lt;htmlxmlns="http://www.w3.org/1999/xhtml"&gt;

&lt;head&gt;

&lt;title&gt; Knockout Support for Circular Gauge in MVC</title>

&lt;/head&gt;

&lt;body&gt;

<divid="CircularGauge1"

data-bind="ejCircularGauge: { 

**value:samplevalue,**

**minimum:minimumValue,**

**maximum:maximumValue**

                    }">

&lt;/div&gt;

&lt;script type="text/javascript"&gt;

        $(function () {

window.viewModel = {

**samplevalue: ko.observable(50),**

**minimumValue: ko.observable(10),**

**maximumValue: ko.observable(150)**

            };

            $(function () {

ko.applyBindings(viewModel);

            });

        });

&lt;/script&gt;

&lt;/body&gt;

&lt;/html&gt;



Execute the above code to render the following output.

![](mvvm_images\mvvm_img8.png)

_Figure_ _75__: Circular Gauge with Knockout binding_

****



**[ASP]**

&lt;%--content section to refer script files--%&gt;



&lt;%--control section--%&gt;

<div id="circularCore" data-bind="ejCircularGauge:({value:samplevalue,minimum:sampleminimum,maximum:samplemaximum,readOnly:false,enableAnimation:false,backgroundColor: 'transparent', width: 500, height:360,

                scales: [{

                    showRanges: true, 

                    startAngle: 122, sweepAngle: 296, radius: 130, showScaleBar: true, size: 1, border: { width: 0.5 }, majorIntervalValue: 20, minorIntervalValue: 10,

                    pointers: [{

                        showBackNeedle: true,

                        backNeedleLength: 20,

                        length: 95,

                        width: 7,

                        pointerCap: { radius: 12 }

                    }],

                    labels: [{

                        Color: '#8c8c8c'

                    }],

                 ticks: [{

                        type: 'major',

                        distanceFromScale: 2,

                        height: 16,

                        width: 1, Color: '#8c8c8c'

                    }, { type: 'minor', height: 8, width: 1, distanceFromScale: 2, color: '#8c8c8c' }],

                    ranges: [{

                        distanceFromScale: -28,

                        startValue: 0,

                        endValue: 60



                    },{

                        distanceFromScale: -28,

                        backgroundColor: '#fc0606',

                        border:{color: '#fc0606'},

                        startValue: 60,

                        endValue: 120

                    }]

                }]})">

       &lt;/div&gt;

window.viewModel = {

            samplevalue: ko.observable(50),

            sampleminimum: ko.observable(0),

            samplemaximum: ko.observable(120),

        };

        $(function () {

            ko.applyBindings(viewModel);

            $("#sampleProperties").ejPropertiesPanel();

        });





Execute the above code to render the following output. The following screenshot is the output of ASP.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img9.png" Caption="Figure 76: Circular Gauge with Knockout binding"%}



## Rendering the Circular Gauge

**ej-CircularGauge** is the control tag in which **ej** is tag prefix and **CircularGauge** is the control name.The following code example helps you to render **Circular Gauge**.

{% highlight js %}

<!--To Render the Circular gauge-->
<!doctype html>
<html ng-app="syncApp">
<head>
<!—Refer the necessary script here-->
</head>
<body ng-controller="CircularGauge">
<ej-CircularGauge id="CircularGauge1" e-backgroundColor="transparent" e-value="50"
e-width="500" e-readOnly="false" e-load= "loadGaugeTheme"
e-enableAnimation="false">
</ej-CircularGauge>
<script type="text/javascript">

<!—binding the value to the scope variables in application controller-->

angular.module('syncApp', ['ejangular'])
.controller('CircularGauge', function ($scope) {
$scope.nvalue = 50;
$scope.nminimum = 0;
$scope.nmaximum = 120;

});
</script>

</body>
</html>



{% endhighlight %}



Execute the above code to render the output as follows.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img10.png" Caption="Figure 68: Default Circular gauge in Angular JS"%}



## Adding Scale Collection

**Scale** is an array object and you can use the inner tag for it. Object in the array collection (i.e. border) is extended with hyphen in the same tag.

**Example**: e-border-width and e-border-color. 

{% highlight js %}

<!--To Render the Circular gauge-->

<ej-CircularGauge id="CircularGauge1">

<!--Adding Scale collection to the Circular gauge-->

<e-scales>
<e-scale e-showRanges="true" e-startAngle="122" e-sweepAngle="296"
e-radius="130" e-showScaleBar="true" e-size="1" e-maximum="120"
e-majorIntervalValue="20" e-minorIntervalValue="10"
e-border-width="0.5">

</e-scale>
</e-scales>
</ej-CircularGauge>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img11.png" Caption="Figure 69: Circular gauge with scale customization in Angular JS"%}



## Adding Pointer CollectionAdding pointer collection

**Pointer** is an array object and you can use the inner tag for it. Object in the array collection (i.e. pointer cap) is extended with hyphen in the same tag.

**Example**: e-pointerCap-radius. 

{% highlight js %}

<!--To Render the Circular gauge-->

<ej-CircularGauge id="CircularGauge1">

<!--Adding Scale collection to the Circular gauge-->

<e-scales>
<e-scale>
<!--Adding pointer collection to the scale collection-->

<e-pointers>
<e-pointer e-showBackNeedle="true" e-backNeedleLength="20"
e-length="95" e-width="7" e-value="80"
e-pointerCap-radius="12">
</e-pointer>
</e-pointers>

</e-scale>
</e-scales>

</ej-CircularGauge>



{% endhighlight %}



Execute the above code to render the output as follows.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img12.png" Caption="Figure 70: Circular gauge with pointer customization in Angular JS"%}



## Adding Label CollectionAdding label collection

**Label** is also an array object. You can use the inner tag for it. 

{% highlight js %}

<!--To Render the Circular gauge-->

<ej-CircularGauge id="CircularGauge1">

<!--Adding Scale collection to the Circular gauge-->

<e-scales>
<e-scale>
<!--Adding pointer collection to the scale collection-->
<e-pointers>…</e-pointers>
<!--Adding labels collection to the scale collection-->

<e-labels>
<e-label e-color="#8c8c8c">
</e-label>
</e-labels>

</e-scale>
</e-scales>

</ej-CircularGauge>



{% endhighlight %}



Execute the above code to render the following output.

![](mvvm_images\mvvm_img13.png)

Figure 71: Circular gauge with label customization in Angular JS

## Adding Tick CollectionAdding Tick collection

**Tick** is an array object. You can use the inner tag for it. 

{% highlight js %}

<!--To Render the Circular gauge-->

<ej-CircularGauge id="CircularGauge1">

<!--Adding Scale collection to the Circular gauge-->

<e-scales>
<e-scale>
<!--Adding pointer collection to the scale collection-->
<e-pointers>…</e-pointers>
<!--Adding labels collection to the scale collection-->
<e-labels>…</e-labels>
<!--Adding ticks collection to the scale collection-->

<e-ticks>
<e-tick e-type="major" e-distanceFromScale="2" e-height="16"
e-width="1" e-color="#8c8c8c">
</e-tick>
<e-tick e-type="minor" e-distanceFromScale="2" e-height="8"
e-width="1" e-color="#8c8c8c">
</e-tick>
</e-ticks>

</e-scale>
</e-scales>

</ej-CircularGauge>



{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img14.png" Caption="Figure 72 : Circular gauge with ticks customization in Angular JS"%}



## Adding Range Collection

**Range** is an array object. You can use the inner tag for it. Object in the array collection (i.e. border) is extended with hyphen in the same tag.

**Example**: e-border-color. 

{% highlight js %}

<!--To Render the Circular gauge-->

<ej-CircularGauge id="CircularGauge1">

<!--Adding Scale collection to the Circular gauge-->

<e-scales>
<e-scale>
<!--Adding pointer collection to the scale collection-->
<e-pointers>…</e-pointers>
<!--Adding labels collection to the scale collection-->
<e-labels>…</e-labels>
<!--Adding ticks collection to the scale collection-->
<e-ticks>…</e-ticks>
<!--Adding ranges collection to the scale collection-->

<e-ranges>
<e-range e-distanceFromScale="-30" e-startValue="0" e-endValue="70">
</e-range>
<e-range e-distanceFromScale="-30" e-startValue="70"
e-endValue="110" e-backgroundColor="#fc0606"
e-border-color="#fc0606">
</e-range>
<e-range e-distanceFromScale="-30" e-startValue="110"
e-endValue="120" e-backgroundColor="#f5b43f"
e-border-color="#f5b43f">
</e-range>
</e-ranges>

</e-scale>
</e-scales>

</ej-CircularGauge>



{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img15.png" Caption="Figure 73: Circular gauge Rendered in Angular JS"%}



## Two Way Binding 

**Circular Gauge** support the two way binding for the property **value, minimum and maximum** as mentioned earlier. The following code example explains how to achieve the two way binding in **Circular Gauge**.

{% highlight js %}

<!doctype html>
<html ng-app="syncApp">
<head>
<!—Refer the necessary script here-->
</head>
<body ng-controller="CircularGauge">
<div id="linearframe">
<ej-CircularGauge id="CircularGauge1" e-backgroundColor="transparent" e-value="nvalue" e-width="500" e-readOnly="false" e-load= "loadGaugeTheme" e-enableAnimation="false">
<e-scales>
<e-scale e-showRanges="true" e-startAngle="122" e-sweepAngle="296"
e-radius="130" e-showScaleBar="true" e-size="1"
<!—binding maximum value using angular JS -->
**e-maximum="nmaximum"**
<!—binding minimum value using angular JS -->
**e-minimum="nminimum"**
e-majorIntervalValue="20"
e-minorIntervalValue="10" e-border-width="0.5">
<e-pointers>
<e-pointer e-showBackNeedle="true" e-backNeedleLength="20"
e-length="95" e-width="7"
<!—binding pointer value using angular JS -->
**e-value="nvalue"**
e-pointerCap-radius="12">
</e-pointer>
</e-pointers>
<e-labels>
<e-label e-color="#8c8c8c"></e-label>
</e-labels>
<e-ticks>
<e-tick e-type="major" e-distanceFromScale="2" e-height="16"
e-width="1" e-color="#8c8c8c">
</e-tick>
<e-tick e-type="minor" e-distanceFromScale="2" e-height="8"
e-width="1" e-color="#8c8c8c">
</e-tick>
</e-ticks>
<e-ranges>
<e-range e-distanceFromScale="-30" e-startValue="0" e-endValue="70">
</e-range>
<e-range e-distanceFromScale="-30" e-startValue="70"
e-endValue="110" e-backgroundColor="#fc0606"
e-border-color="#fc0606">
</e-range>
<e-range e-distanceFromScale="-30" e-startValue="110"
e-endValue="120" e-backgroundColor="#f5b43f"
e-border-color="#f5b43f">
</e-range>
</e-ranges>
</e-scale>
</e-scales>
</ej-CircularGauge>
</div>
<input type="text" id="txtMax" e-value="nvalue" ej-numerictextbox **ng-model="nvalue"**  e-decimalplaces="2" e-showspinbutton="false" Style="width:110px"/>



<script type="text/javascript">

<!—binding the value to the scope variables in application controller-->

angular.module('syncApp', ['ejangular'])
.controller('CircularGauge', function ($scope) {
$scope.nvalue = 50;
$scope.nminimum = 0;
$scope.nmaximum = 120;

});
</script>
</body>
</html>


{% endhighlight %}



Execute the above code to render the following output.





{% include image.html url="\js\CircularGauge\concepts-and-features\mvvm_images\mvvm_img16.png" Caption="Figure 74: Circular gauge with two way binding in Angular JS"%}











## Knockout JS

* Knockout support allows you to bind the **HTML** elements against any of the available data models.Two types of knockout binding is supported as of angular,

  * one-way binding

  * two-way binding

* **One way binding** refers to the process of applying observable values to all the available properties of the **Circular Gauge** control, but the changes made in gauge control does not reflect and trigger in turn to the observable collection. This kind of binding applies to all the properties of the circular gauge control.

* **Two-way binding** supports both the processes – it applies the observable values to the **Circular Gauge** properties as well as the changes made in the **Circular Gauge** control also reflects back and triggers within the observable collections. Only few of the schedule properties support two-way binding and they are as follows

  * value

  * maximum 

  * minimum



{% highlight js %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>Essential JavaScript for Knockout</title>
</head>
<body>
<div id="CircularGauge1"
data-bind="ejCircularGauge: {
**value: samplevalue,**
**minimum: minimumValue,**
**maximum: maximumValue**
}">
</div>
<script type="text/javascript">
$(function () {
window.viewModel = {
**value: ko.observable(50),**
**minimum: ko.observable(0),**
**maximum: ko.observable(150)**
};
$(function () {
ko.applyBindings(viewModel);
});
});
</script>
</body>
</html>


{% endhighlight %}



Execute the above code to render the following output.

![](mvvm_images\mvvm_img17.png)

_Figure_ _75__: Circular Gauge with Knockout binding_





