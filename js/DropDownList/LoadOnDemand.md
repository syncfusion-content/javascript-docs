---
layout: post
title: Load on deamand in JS DropDownList Control | Syncfusion 
description: Learn here about getting started with Syncfusion JavaScript DropDownList control, its elements, and more.
platform: js
control: DropDownList
documentation: ug
keywords: loadOnDemand, dropdown
api: /api/js/ejdropdownlist
---

# Getting started with JS DropDownList

Load on demand feature allows the DropDownList items load on request from the service/database, during only on click the DropDown icon or DropDownList. This functionality helps to improve performance on control initial rendering time. Because data items load on request. 

The [loadOnDemand](https://help.syncfusion.com/api/js/ejdropdownlist#members:loadOnDemand) property is used to enable or disable the load on demand functionality of the DropDownList.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
  
        var target;
        
		$(function() { 
            var items = [{
                text: "ListItem 1",
                value: "item1"
            }, {
                text: "ListItem 2",
                value: "item2"
            }, {
                text: "ListItem 3",
                value: "item3"
            }, {
                text: "ListItem 4",
                value: "item4"
            }, {
                text: "ListItem 5",
                value: "item5"
            }];
        $('#dropdown1').ejDropDownList({
            dataSource: items,
            fields: {
                text: "text",
                value: "value"
            },
            loadOnDemand: true
        });
        
       

{% endhighlight %}

![JS DropDownList LoadOnDemand](LoadOnDemand_images/loadondemand.png)