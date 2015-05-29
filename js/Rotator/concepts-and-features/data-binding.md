---
layout: post
title: data-binding
description: data binding
platform: js
control: Rotator
documentation: ug
---

# Data Binding

**Rotator** provides a flexible approach for binding the data from various data sources. There are various properties in **Toolbar** for **Data Binding**. The value set to this property is **object** type.

## Data fields and Configuration

The following sub-properties provide a way to bind the data either locally/remotely to the **Rotator** control. The value set to this property is **object** type.

## DataSource

This property specifies the list of data that contains a set of data fields. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Fields

It defines mapping fields for the data items of the **Rotator**. The value set to this property is **object** type.

## Text

It specifies the text content of the tag. The value set to this property is **string** type.

## Url

This property specifies the **URL** for an image. The value set to this property is **string** type.

## Query

This property retrieves data from remote data. This property is applicable only when a remote data source is used. Each data value is used to render an item for the **Rotator**. The value set to this property is **object** type.

## Local data binding

**Rotator** provides the data binding support for the **Rotator****item**. So you can bind the data from **JSON****Data**. For this behavior, you need to map the corresponding filed with their column names. The data can be bound as a list and it is assigned to **dDataSource** property. You can refer the following code example to bind local data.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="cols-sample-area"&gt;    &lt;ul id="slidercontent"&gt;&lt;/ul&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script type="text/javascript"&gt;    $(function () {        // declaration        var website = [      { text: "Beautiful Bird", url: "../images/rotator/bird.jpg" },      { text: "Colorful Night", url: "../images/rotator/night.jpg" },      { text: "Technology", url: "../images/rotator/tablet.jpg" },      { text: "Nature", url: "../images/rotator/nature.jpg" },      { text: "Snow Fall", url: "../images/rotator/snowfall.jpg" },      { text: "Credit Card", url: "../images/rotator/card.jpg" },      { text: "Amazing Sculptures", url: "../images/rotator/sculpture.jpg" }        ];        $("#slidercontent").ejRotator({            slideWidth: "600px",            frameSpace: "0px",            displayItemsCount: "1",            slideHeight: "350px",            navigateSteps: "1",            enableResize: true,            pagerPosition: ej.Rotator.PagerPosition.Outside,            dataSource: website,            orientation: ej.Orientation.Horizontal,            showPager: true,            enabled: true,            showCaption: true,            allowKeyboardNavigation: true,            enableRTL: true,            showPlayButton: true,            animationType: "slide",        });    });&lt;/script&gt;</td></tr>
</table>


<table>
<tr>
<td>
<b>[CSHTML]</b>@Html.EJ().Rotator("slidercontent").Datasource((IEnumerable<Localdata>)ViewBag.datasource).RotatorFields(t => t.Text("Text").Url("Url")).SlideWidth("600px").SlideHeight("350px")</td></tr>
<tr>
<td>
<b>[CS]</b>public class Localdata        {            public string Text { get; set; }            public string Url { get; set; }        }        List<Localdata> localvalues = new List<Localdata>();        public ActionResult Index()        {            localvalues.Add(new Localdata { Text = "Beautiful Bird", Url = "../Images/rotator/bird.jpg" });            localvalues.Add(new Localdata { Text = "Colorful Night", Url = "../Images/rotator/night.jpg" });            localvalues.Add(new Localdata { Text = "Technology", Url = "../Images/rotator/tablet.jpg" });            localvalues.Add(new Localdata { Text = "Nature", Url = "../Images/rotator/nature.jpg" });            localvalues.Add(new Localdata { Text = "Snow Fall", Url = "../Images/rotator/snowfall.jpg" });            localvalues.Add(new Localdata { Text = "Credit Card", Url = "../Images/rotator/card.jpg" });            localvalues.Add(new Localdata { Text = "Amazing Sculptures", Url = "../Images/rotator/sculpture.jpg" });            ViewBag.datasource = localvalues;            return View();        }   </td></tr>
</table>


<table>
<tr>
<td>
<b>[ASPX]</b>&lt;ej:Rotator ID="slidercontent" runat="server" SlideWidth="600px" SlideHeight="350px" DataCaptionField="Caption" DataUrlField="Url"&gt;&lt;/ej:Rotator&gt;</td></tr>
<tr>
<td>
<b>[C#]</b>public class RotatorData        {            public string Caption { get; set; }            public string Url { set; get; }        }                protected void Page_Load(object sender, EventArgs e)        {            List<RotatorData> data = new List<RotatorData>();            data.Add(new RotatorData { Caption = "Beautiful Bird", Url = "../images/rotator/bird.jpg" });            data.Add(new RotatorData { Caption = "Colorful Night", Url = "../images/rotator/night.jpg" });            data.Add(new RotatorData { Caption = "Technology", Url = "../images/rotator/tablet.jpg" });            data.Add(new RotatorData { Caption = "Nature", Url = "../images/rotator/nature.jpg" });            data.Add(new RotatorData { Caption = "Snow Fall", Url = "../images/rotator/snowfall.jpg" });            data.Add(new RotatorData { Caption = "Credit Card", Url = "../images/rotator/card.jpg" });            this.slidercontent.DataSource = data;                    }</td></tr>
</table>


![](data-binding_images\data-binding_img1.png)![](data-binding_images\data-binding_img2.png)



_Figure_ _7__3__:_ _Rotator control_ _with local data binding_

## Knockout support

**Knockout** support allows you to bind the **HTML** elements against any of the available data models.

Two types of **Knockout** binding are supported,

* One-way binding

* Two-way binding

**One way binding** refers to the process of applying observable values to all the available properties of the **Rotator**. But the changes made in **Rotator** widget are not reflected and triggered in turn to the observable collection. This kind of binding is applied to all the properties of the **Rotator**.

**Two-way binding** supports both the processes – it applies the observable values to the **Rotator** properties as well as the changes made in the **Rotator** widget are also reflected back and triggered within the observable collections. 

For more information about the **Knockout** binding, you can refer the online documentation in the following link location,

[http://help.syncfusion.com/ug/js/documents/knockoutjs.htm](http://help.syncfusion.com/ug/js/documents/knockoutjs.htm)

> ![](data-binding_images\data-binding_img3.jpeg)_**Note: Add the following script files along with the given code to access Knockout binding. They have JS library for Knockout binding.**_

* knockout-min.js

* ej.widget.ko-latest.min.js

The link for those script files are as follows:

[http://cdnjs.cloudflare.com/ajax/libs/knockout/2.2.0/knockout-min.js](http://cdnjs.cloudflare.com/ajax/libs/knockout/2.2.0/knockout-min.js)

" 

" http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.ko.min.js

The following code example depicts the way to bind data to the **Rotator** through the **Knockout** support.

<table>
<tr>
<td>
<b>[HTML]</b>&lt;body data-autoinit="false"&gt;    &lt;div class="cols-sample-area"&gt;        &lt;ul id="slidercontent" data-bind="ejRotator :{dataSource:dataList,slideWidth:width,slideHeight:height}" /&gt;    &lt;/div&gt;&lt;/body&gt;</td></tr>
<tr>
<td>
<b>[JS]    </b>&lt;script&gt;    $(function () {        var imageList = [          { text: "bird", url: "../images/rotator/bird.jpg" },          { text: "night", url: "../images/rotator/night.jpg" },          { text: "tablet", url: "../images/rotator/tablet.jpg" },          { text: "nature", url: "../images/rotator/nature.jpg" },          { text: "snowfall", url: "../images/rotator/snowfall.jpg" },          { text: "card", url: "../images/rotator/card.jpg" },          { text: "sculpture", url: "../images/rotator/sculpture.jpg" }        ];        window.viewModel = {            dataList: ko.observableArray(imageList),            height: ko.observable("350px"),            width: ko.observable("600px"),        };        ko.applyBindings(viewModel);    });&lt;/script&gt;</td></tr>
</table>


**[CSHTML]**

&lt;ul id="slidercontent" data-bind="ejRotator :{dataSource:dataList,slideWidth:width,slideHeight:height}"/&gt;



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;ul id="slidercontent" data-bind="ejRotator: { dataSource: dataList, slideWidth: width, slideHeight: height }" /&gt;</td></tr>
<tr>
<td>
<b>[JS]    </b>&lt;script&gt;    $(function () {    var imageList = [      { text: "bird", url: "../images/rotator/bird.jpg" },      { text: "night", url: "../images/rotator/night.jpg" },      { text: "tablet", url: "../images/rotator/tablet.jpg" },      { text: "nature", url: "../images/rotator/nature.jpg" },      { text: "snowfall", url: "../images/rotator/snowfall.jpg" },      { text: "card", url: "../images/rotator/card.jpg" },      { text: "sculpture", url: "../images/rotator/sculpture.jpg" }    ];    window.viewModel = {        dataList: ko.observableArray(imageList),        height: ko.observable("350px"),        width: ko.observable("600px"),    };    ko.applyBindings(viewModel);});&lt;/script&gt;</td></tr>
</table>


![](data-binding_images\data-binding_img4.png)![](data-binding_images\data-binding_img5.png)



_Figure_ _8__4__:_ _Rotator control_ _with K__nockout support_

## Angular support

**Rotator** is availed with two types of **angular****JS** support namely, 

* One way binding

* Two way binding 

**One way binding** refers to the process of applying scope values to all the available properties of the Rotator. But the changes made in **Rotator** widget are not reflected or triggered in turn to the scope collection. This kind of binding is applied to all the properties of the **Rotator**.

**Two-way binding** supports both the processes – it applies the scope values to the **Rotator** properties as well as the changes made in the **Rotator** widget are also reflected back and triggered within the angular scope change function.

To know more details about the **Angular****binding**, you can refer the following link location,

[http://help.syncfusion.com/ug/js/documents/angularjs.htm](http://help.syncfusion.com/ug/js/documents/angularjs.htm)

> ![](data-binding_images\data-binding_img6.jpeg)_**Note: Add the following script files as given in the following example to access Knockout binding. They have JS library for angular binding.**_

* angular-min.js

* ej.widget.angular-latest.min.js

The following code example depicts the way to bind data to the **Rotator** widget through **angular** support.

{% highlight html %}

**[HTML]**
<!DOCTYPE html>
<html lang="en" ng-app="rotatApp">
<head>
    <title>Essential Studio for JavaScript :Angular JS Support for Toolbar</title>
    <meta name="viewport" content="width=device-width, initial-scale=1.0" charset="utf-8" />
    <link href="http://cdn.syncfusion.com/13.1.0.21/js/web/flat-azure/ej.web.all.min.css" rel="stylesheet" />
    <!--scripts-->
    <script src="http://cdn.syncfusion.com/js/assets/external/jquery-1.10.2.min.js"></script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.globalize.min.js"> </script>

    <script src="http://cdn.syncfusion.com/js/assets/external/jquery.easing.1.3.min.js"> </script>
    <scriptsrc="[http://cdn.syncfusion.com/js/assets/external/angular.min.js](http://cdn.syncfusion.com/js/assets/external/angular.min.js)"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.web.all.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/web/ej.unobtrusive.min.js"></script>
    <script src="http://cdn.syncfusion.com/13.1.0.21/js/ej.widget.angular.min.js"></script>

</head>
<body ng-controller="RotatCtrl">
    <div class="cols-sample-area">
        <ul id="slidercontent" ej-rotator e-datasource="dataList" e-slidewidth="600px" e-slideheight="350px" />
    </div>
</body>
</html>


{% endhighlight %}





{% highlight js %}

**[JS]**
<script>
    var list = [
      { text: "snowfall", url: "../images/rotator/snowfall.jpg" },
      { text: "tablet", url: "../images/rotator/tablet.jpg" },
      { text: "nature", url: "../images/rotator/nature.jpg" },
      { text: "card", url: "../images/rotator/card.jpg" },
      { text: "bird", url: "../images/rotator/bird.jpg" },
      { text: "wheat", url: "../images/rotator/wheat.jpg" },
      { text: "night", url: "../images/rotator/night.jpg" }];

    angular.module('rotatApp', ['ejangular']).controller('RotatCtrl', function ($scope) {
        $scope.dataList = list;
    });
</script>


{% endhighlight %}



**[CSHTML]**

&lt;div lang="en" ng-app="rotatApp"&gt;

    &lt;div ng-controller="RotatCtrl"&gt;

        &lt;ul id="slidercontent" ej-rotator e-datasource="dataList" e-slidewidth="600px" e-slideheight="350px" /&gt;

    &lt;/div&gt;

&lt;/div&gt;



<table>
<tr>
<td>
<b>[ASPX]</b>&lt;div ng-app="rotatApp"&gt;        &lt;div ng-controller="RotatCtrl"&gt;            &lt;ul id="slidercontent" ej-rotator e-datasource="dataList" e-slidewidth="600px" e-slideheight="350px" /&gt;        &lt;/div&gt;  &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JS]</b>&lt;script&gt;    var list = [      { text: "snowfall", url: "../images/rotator/snowfall.jpg" },      { text: "tablet", url: "../images/rotator/tablet.jpg" },      { text: "nature", url: "../images/rotator/nature.jpg" },      { text: "card", url: "../images/rotator/card.jpg" },      { text: "bird", url: "../images/rotator/bird.jpg" },      { text: "wheat", url: "../images/rotator/wheat.jpg" },      { text: "night", url: "../images/rotator/night.jpg" }];    angular.module('rotatApp', ['ejangular']).controller('RotatCtrl', function ($scope) {        $scope.dataList = list;    });&lt;/script&gt;</td></tr>
</table>


{% include image.html url="\js\Rotator\concepts-and-features\data-binding_images\data-binding_img7.png" Caption="Figure 95: Rotator control with angular support"%}{% include image.html url="\js\Rotator\concepts-and-features\data-binding_images\data-binding_img8.png" Caption="Figure 95: Rotator control with angular support"%}

