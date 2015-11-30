---
layout: post
title: Demension in DropDownList
description: Setting Dimensions to DropDownList 
platform: js
control: DropDownList
documentation: ug
---

## Setting dimensions 

### Widget Sizing

Fixed Size DropDownList widget
You can customize the widget dimensions using [width](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:width) and [height](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:height) properties. Fixed size values can be specified in pixel or percentage values. By default the DropDownList wrapper will be assigned with “143px” width and “30px” height.

** Fixed size popup list **

You can customize the popup list dimensions using [popupWidth](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:popupwidth) and [popupHeight](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:popupheight) properties. Fixed size values can be specified in pixel or percentage values. By default popup width is auto and popup height is “152px”. 

**Auto Sizing**

DropDownList is adaptive to mobile and web layout such that it is adjustable with screen resolution. The textbox will be rendered based on its parent containers dimensions on assigning 100% values to the width property. Default value for popupWidth is auto, so when you assign 100% to popupWidth then it will be rendered based on specified range.

** Limit the number of items **

You can use “[itemsCount](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:itemscount)” property to fetch only the specific number of items from the data source. To fetch the remaining items you can enable [virtual scrolling](#_Virtual_scrolling_on) support which loads the data on scrolling the data items in popup list. 
Note: By default popup list is shown on DropDownList button click but you can display the list initially by enabling the “[showPopupOnLoad](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:showpopuponload)” property. You can also use [showPopup ()](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:showpopup) or [hidePopup ()](http://helpjs.syncfusion.com/js/api/ejdropdownlist#methods:hidepopup) methods at run time to display or hide the popup list.

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight js %}

    <script type="text/javascript">
	
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
            itemsCount: 3,
            showPopupOnLoad: true
        });
    });
	
	</script>

{% endhighlight %}

![](SettingDimension_images/SettingDimension_img1.jpeg)

### Popup resizing 

To show a resize handle in the popup list, use “[enablePopupResize](http://docs.syncfusion.com/js/api/ejdropdownlist#members:enablepopupresize)” property. You can customize the resize functionality by setting dimensions to the following properties.

<table>
    <tr>
        <td colspan=1 rowspan=1>
            {{'[minPopupWidth](http://docs.syncfusion.com/js/api/ejdropdownlist#members:minpopupwidth)'| markdownify }}
            <br/>
        </td>
        <td colspan=1 rowspan=1>
            Default value is 0, once set you cannot resize below to the specified width
            <br/>
        </td>
    </tr>
    <tr>
        <td colspan=1 rowspan=1>
            {{'[maxPopupWidth](http://docs.syncfusion.com/js/api/ejdropdownlist#members:maxpopupwidth)'| markdownify }}
            <br/>
        </td>
        <td colspan=1 rowspan=1>
            Default value is null, once set you cannot extend beyond to the specified width
            <br/>
        </td>
    </tr>
    <tr>
        <td colspan=1 rowspan=1>
            {{'[minPopupHeight](http://docs.syncfusion.com/js/api/ejdropdownlist#members:minpopupheight)'| markdownify }}
            <br/>
        </td>
        <td colspan=1 rowspan=1>
            Default value is 0, once set you cannot resize below to the specified height
            <br/>
        </td>
    </tr>
    <tr>
        <td colspan=1 rowspan=1>
            {{'[maxPopupHeight](http://docs.syncfusion.com/js/api/ejdropdownlist#members:maxpopupheight)'| markdownify }}
            <br/>
        </td>
        <td colspan=1 rowspan=1>
            Default value is null, once set you cannot extend beyond to the specified height
            <br/>
        </td>
    </tr>
</table>

{% highlight html %}

     <input type="text" id="dropdown1" />
     
{% endhighlight %}

{% highlight js %}

    <script type="text/javascript">
	
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
            enablePopupResize: true,
            minPopupWidth: 150,
            minPopupHeight: 150,
            maxPopupWidth: 550,
            maxPopupHeight: 550,
        });
    });
	
	</script>

{% endhighlight %}

![](SettingDimension_images/SettingDimension_img2.jpeg)

![](SettingDimension_images/SettingDimension_img3.jpeg)

