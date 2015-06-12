---
layout: post
title: API-Configuration
description: api configuration
platform: js
control: Introduction
documentation: ug
---

## API Configuration

It is possible to get and set the various properties available within the controls after its creation -

### Getting API values

The API values can be accessed/retrieved by using either of the following ways,

{% highlight js %}

```js
1. $(“jquery-selector”).<ej-plugin-name>(“model.propertyName”);
   // Example
   $("#myDate").ejDatePicker("model.buttonText");


2. $(“jquery-selector”).<ej-plugin-name>(“option”, “propertyName”);
   // Example
   $("#myDate").ejDatePicker("option", "buttonText");
```

{% endhighlight %}



### Setting values to the API

It is possible to set new values to the properties of the Syncfusion widgets either **during or after control initialization** which is described below, 

#### During Initialization

{% highlight js %}

```js
1. $(“jquery-selector”).<ej-plugin-name>({ propertyName1 : value1, propertyName2: value2, … });
   // Example
   $("#myDate").ejDatePicker({ value: "01/01/2015", buttonText: "Hôm nay" });

```


{% endhighlight %}



#### After initialization

{% highlight js %}

```js
1. var obj = $(“jquery-selector”).data(“<ej-plugin-name>”);  **[Recommended method]**
   obj.option({ propertyName: value });
   //Example
   var dateObject = $("#myDate").data("ejDatePicker");
   dateObject.option({ buttonText: "Hôm nay" });


2. $(“jquery-selector”).<ej-plugin-name>(“model.propertyName”, “value”);
   //Example
   $("#myDate").ejDatePicker("model.buttonText", "Hôm nay" );


3. $(“jquery-selector”).<ej-plugin-name>(“option”, “propertyName”, “value”);
   //Example
   $("#myDate").ejDatePicker("option", "buttonText", "Hôm nay");

4. $(“jquery-selector”).<ej-plugin-name>({ propertyName : “value” });
   //Example
   $("#myDate").ejDatePicker({ value: "01/01/2015" });
```



{% endhighlight %}



