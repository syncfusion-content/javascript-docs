---
layout: post
title: KnockoutJS
description: knockoutjs
platform: js
control: Introduction
documentation: ug
---

# KnockoutJS

**Essential JavaScript** provides complete support of **[KnockoutJS](http://knockoutjs.com/documentation/introduction.html)** (**MVVM** pattern) for all the Syncfusion widgets, which can be achieved by integrating and referring the Syncfusion JS library (**ej.widget.ko.min.js**) file in the application.

## Required JavaScript libraries

The following two JavaScript libraries are necessary to work with **KnockoutJS**,

* knockout.min.js
* ej.widget.ko.min.js

The **knockout.min.js** file can be availed from the following installed location,

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external
</td>
</tr>
<tr>
<td> 
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\external
</td>
</tr>
</table>

The **ej.widget.ko.min.js** file which needs to be referred along with the knockout.min file can be availed from the following location on your machine,

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common
</td>
</tr>
<tr>
<td> 
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\common
</td>
</tr>
</table>

## KnockoutJS Concepts

The two major concepts of the KnockoutJS on which our Syncfucion widgets mainly relies on are as follows,

* Declarative binding
* Dependency tracking

### Declarative binding

It provides a simpler and more convenient way to synchronize the property values of the UI components to the data model. The declarative binding is usually defined with **data-bind** attribute, so as to bind the component data to the DOM element. Along with this declarative binding, **Essential JavaScript** provides each of the EJ components with a **binding handler**. The control’s binding handler name is nothing but its usual component name. For example, the binding handler name of the Syncfusion Grid component is **ejGrid**.

The below code snippet shows how the data-bind attribute is used with our Syncfusion **DatePicker** widget,

{% highlight html %}


<input id="datepick2" data-bind="ejDatePicker: { value: '01/01/2015', enableStrictMode: true }"/> 


{% endhighlight %}

Here, the **data-bind** attribute is assigned with the control **ejDatePicker**, followed by its properties defined with the required values.

### Dependency tracking

**KnockoutJS** provides a special type of variable **observable**, through which the data-binding can be achieved in a more convenient manner. Everytime, when the model data is being changed, all those changes are automatically synchronized with the associated UI elements. It doesn’t require any additional event handlers or listeners to do this, as all those tasks are performed internally by the Knockout and observable variable. 

Here, the below sample code defines how to define the **observable** variable within the **script** section,

{% highlight js %}

window.viewModel = {
   dateValue: ko.observable(new Date(2014, 05, 15))
};

{% endhighlight %}

The value to be bound to the UI element needs to be passed through the **ko.observable** varaiable as shown above. The **dateValue** defined in the above code is an observable variable holding a date value, which can be assigned to the properties of the UI components.

The **data-bind** attribute which we have defined in the previous section cannot be identified directly by the HTML tags and also the browser on which we run that page.  Therefore, in order to work with Knockout, we need to declare the **ko.applyBindings()** function at the end of the script, so that the **data-bind** attribute will get recognised. Such Knockout code needs to be wrapped in a jQuery function as shown below within the **script** section, in order to work properly.

{% highlight js %}

window.viewModel = {
    value: ko.observable(new Date(2014, 05, 15))
};
            
$(function () {
    // declaration
    ko.applyBindings(viewModel);
});                        

{% endhighlight %}

## Data binding

Data-binding can be defined as an automatic synchronization of data between the model and UI components. Our Syncfusion widgets supports both one-way and two-way binding.

### One way binding

Here, the model values are directly bound to the widget’s properties. The changes made in the property’s value won’t reflect in the model in any way. **All the properties of Syncfusion widgets support one-way binding.** The below code defines the one-way binding used in the DatePicker widget,

{% highlight html %}

<input id="myDatePicker1" data-bind="ejDatePicker: { value: '01/01/2015', enableStrictMode: true }"/>


{% endhighlight %}

Here, in the above code, the **value** property of the DatePicker widget is assigned with the direct value **01/01/2015**. Therefore, whenever we change the value of the DatePicker dynamically, the changes won’t get reflected in the value property.

### Two way binding

It links the data model to an UI, thus making a smooth synchronization between them. Here, the **ko.observable** variable defined in the script section is bound to the widget’s properties instead of direct values, so that both can have a good data synchronization. In general, we could have more than one property bound to the same variable. **The properties of all the Syncfusion widgets that supports two-way data-binding are depicted [here](http://helpjs.syncfusion.com/js/angularjs#two-way-binding-properties)**. 

The two-way data binding has been demonstrated in the below code with two DatePicker controls sharing the same **ko.observable** variable,

{% highlight html %}

<html xmlns="http://www.w3.org/1999/xhtml">
  <head>
    <title>Essential Studio for JavaScript : DatePicker - Knockout</title>
    <!-- SCRIPT & CSS REFERENCE SECTION -->
  </head>
  <body>
    <input id="mydatepicker1" data-bind="ejDatePicker: { value: dateValue, enableStrictMode: true }"/>
    <input id="mydatepicker2" data-bind="ejDatePicker: { value: dateValue, enableStrictMode: true }"/>
    <script type="text/javascript">
            window.viewModel = {
            dateValue: ko.observable(new Date(2014, 05, 15))
            };
            $(function () {
                // declaration
                ko.applyBindings(viewModel);
            });                        
    </script>
  </body>
</html>

{% endhighlight %}

Here, just for the demonstration purpose, we are using two DatePicker controls (with id **mydatepicker1** and **mydatepicker2**), both of its value property is bound to the observable variable **dateValue**. Initially, both the DatePickers will be displayed with the value **15/05/2014** and whenever any of the DatePicker’s value is changed dynamically, it gets simultaneously reflected in another DatePicker too, as both of them shared the same observable variable.

Thus the KnockoutJS simplifies the user interaction and also makes the user interfaces more responsive to any of the dataSource related changes.

