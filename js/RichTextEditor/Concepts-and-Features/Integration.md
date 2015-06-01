---
layout: post
title: Integration
description: integration
platform: js
control: RichTextEditor
documentation: ug
---

# Integration

### AngularJS

**Angular Support** is a two-way data binding, connecting **HTML** to **JavaScript** objects seamlessly. It reduces the amount of code from page. **Angular JS** adds more functionality and creates powerful dynamic template. **Angular JS** extends **HTML** with new directives. 

**Angular JS** is an open-source web application framework. **Angular JS** extends **HTML** with new attribute. It can be added to **HTML** page with **&lt;script&gt;** tag. The library reads in **HTML** that contains additional custom tag attributes. **Angular JS** extends **HTML** attribute with **Directives** and binds data to **HTML** with **Expressions**. 

Using this, you can view the equivalent **XHTML** code of the content in the editing area while you type.

To know more details about the **Angular binding**, refer to the following link location,

[http://help.syncfusion.com/ug/js/default.htm#!documents/angularjs.htm](http://help.syncfusion.com/ug/js/default.htm%23!documents/angularjs.htm)

You can bind data to the **RTE** control through **angular support**.

The following example illustrates how to bind the **RTE** data with simple text box as a two-way binding.

Add the following code in your **HTML** page to initialize the **RTE** control.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div ng-app="syncApp" ng-controller="RTECtrl"&gt;    &lt;div id="control" style="float: left; width: 30%;"&gt;        &lt;textarea id="rteSample" ej-rte e-width="100%" e-height="266" e-value="rteValue"&gt;&lt;/textarea&gt;        &lt;h6&gt;<span style="font-style: italic; font-weight: normal; position: absolute; ">Note:Two Way Angular Support</span>&lt;/h6&gt;    &lt;/div&gt;    &lt;div id="binding" style="float: left; margin-left:10px; width:27%;"&gt;        &lt;textarea name="scroll" class="input ejinputarea" ng-model="rteValue" style="height: 262px;"&gt;&lt;/textarea&gt;    &lt;/div&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section.        angular.module('syncApp', ['ejangular'])            .controller('RTECtrl', function ($scope) {                $scope.rteValue = "Description: The Rich Text Editor (RTE) control is an easy to render in client side. Customer easy to edit the contents and get the HTML content for";                $scope.style = "color:ffffff";            });</td></tr>
</table>


{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Integration_images/Integration_img1.png" Caption="Screenshot of RTE with angular support"%}

### Knockout Binding

**KnockoutJS** uses a **Model-View-View Model** (**MVVM**) design pattern, where the model is your stored data and the view is the visual representation of that data (**UI**) and View Model acts as the intermediary between the model and the view. Sometimes you may need to enter some text box value to replicate in **RTE** content area. In such situations, use the knockout binding feature to control the contents from other view field.

If you want to create an **HTML** page for your application and there is a live demo for your **HTML** page, then it is better to customize your **HTML** page. You can achieve this by using **knockout****binding** with **RTE**.

In the following example, one simple text area and one **RTE** control have been created. Added is some **HTML** code (“<h1>Description: The Rich Text Editor (RTE) control is an easy to render in client side. &lt;/h1&gt;”) in the normal text area. When you run the sample, you can get the result of this **RTE** text area. At runtime, add the following **HTML** code in normal text area.

“&lt;div style="border: 2px solid #a1a1a1;padding: 10px 40px;background: #dddddd; width: 300px; border-radius: 25px;"&gt;<h2>Demo of current html content in text area</h2>&lt;/div&gt;”

When you type this **HTML** code and focus out from the text area, you can get the result of **HTML** code in **RTE** editing area. You can apply any styles or changes to this content in **RTE** editing area by using the **RTE Toolbar** or manually. It is reflected in the normal text area as **HTML** code.

Add the following code in your **HTML** page to initialize the **RTE**.



<table>
<tr>
<td>
<b>[HTML]</b>    &lt;div id="control" style="float: left; width: 30%;"&gt;    &lt;textarea id="rteSample" data-bind="ejRTE: {value:rteValue,width:width,height:height}"&gt;&lt;/textarea&gt;&lt;/div&gt;&lt;div id="binding" style="float: left; font-size:25px; width: 27%"&gt;    &lt;textarea name="scroll" style="font-size:25px; height: 262px" class="input ejinputtext" data-bind="value: rteValue"&gt;&lt;/textarea&gt;&lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b>\\ Add the following code in your script section to render RTE.window.viewModel = {    height: ko.observable(266),    width: ko.observable("95%"),    rteValue: ko.observable("<h1>Demo of current html content</h1>"),};$(function () {    ko.applyBindings(viewModel);});</td></tr>
</table>


{% include image.html url="/js/RichTextEditor/Concepts-and-Features/Integration_images/Integration_img2.png" Caption="Show case for RTE control with Knock out"%}

