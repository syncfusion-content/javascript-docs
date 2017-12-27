---
layout: post
title: Load on deamand in DropDownList widget for Syncfusion Essential JS
description: Describes about loadOnDemand in DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: loadOnDemand, dropdown
api: /api/js/ejdropdownlist
---

## Load On Demand

The popup and lists will be generated while click on dropdown icon or text box. For this feature, the loadOnDemand property must be enabled.

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

![](LoadOnDemand/loadondemand.png)