---
layout: post
title: Customization in DropDownList widget for Syncfusion Essential JS
description: Customization in DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
---

# Customization

## Adding watermark text

It provides the short description of the expected value in dropdown and will display the text until any item is selected. You can set this text using [watermarkText](http://help.syncfusion.com/js/api/ejdropdownlist#members:watermarktext) property.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
	
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
            watermarkText: "Select an Item"
        });
    });

{% endhighlight %}

![](Customization_images/Customization_img1.jpeg)

![](Customization_images/Customization_img2.jpeg)

## Applying Rounded Corner

You can use [showRoundedCorner](http://help.syncfusion.com/js/api/ejdropdownlist#members:showroundedcorner) property to add rounded borders to the input and popup elements. By default, rounded corner property is disabled in DropDownList.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
  
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
            showRoundedCorner: true
        });
    });

{% endhighlight %}

![](Customization_images/Customization_img3.jpeg)

I> The browser support details for rounded corner is given [here](http://www.w3schools.com/cssref/css3_pr_border-radius.asp).

## Enable/Disable the widget

The [enabled](http://help.syncfusion.com/js/api/ejdropdownlist#members:enabled) property is used to indicate whether the widget can respond to the user interaction or not. You can disable it by assigning false to this property. When the widget is disabled state, you cannot interact with the control.

N> you can also use [enable()](http://help.syncfusion.com/js/api/ejdropdownlist#methods:enable)  or [disable()](http://help.syncfusion.com/js/api/ejdropdownlist#methods:disable)  public methods.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}

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
            enabled: false
        });
    });
	
{% endhighlight %}

![](Customization_images/Customization_img4.jpeg)

N> you can disable/enable the single or multiple list items by using [disableItemsByIndices](http://help.syncfusion.com/js/api/ejdropdownlist#methods:disableitemsbyindices) and [enableItemsByIndices](http://help.syncfusion.com/js/api/ejdropdownlist#methods:enableitemsbyindices) property.

## Applying HTML Attributes

Additional HTML attributes can be applied to the widget by using [htmlAttributes](http://help.syncfusion.com/js/api/ejdropdownlist#members:htmlattributes) property. The valid attributes such as name, required, read-only and disabled are directly applied to the input element of DropDownList, and other attributes such as style, class will be applied to the outer wrapper element of DropDownList. Please refer to the [How-to](http://help.syncfusion.com/js/dropdownlist/howto) section.

N>when you add an item dynamically to the widget, you can specify the HTML attributes in the [addItem()](http://help.syncfusion.com/js/api/ejdropdownlist#methods:additem) method parameters.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight javascript %}
	
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
            htmlAttributes: {
                style: "border:1px solid red;"
            }
        });
    });

{% endhighlight %}

![](Customization_images/Customization_img5.jpeg)

