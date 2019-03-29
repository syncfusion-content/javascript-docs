---
layout: post
title: How to section in Syncfusion Listview widget for Essential JS? 
description: How to section in Listview widget for Essential JS
documentation: ug
platform: js
keywords: How-to,ListView How-to
api : /api/js/ejListView
---

# How to?

## How to get the selected/checked values?

**Single selection**


Enable the property [PersistSelection](https://help.syncfusion.com/api/js/ejlistview#members:persistselection) in order to use selection in ListView. Then use the [getActiveItemText](https://help.syncfusion.com/api/js/ejlistview#methods:getactiveitemtext) method take the selected active text.

**Multiple selection**

For multi selection i.e. when using the [EnableCheckMark](https://help.syncfusion.com/api/js/ejlistview#members:enablecheckmark) property, we need to use the [getCheckedItemsText](https://help.syncfusion.com/api/js/ejlistview#methods:getcheckeditemstext) method to take all the checked items.

## Resolve ListView rendering order issue in IE
 
In Internet Explorer and Microsoft Edge, the sorting order of sub-child elements will be changed when compared to other browsers. To resolve this issue, set `ej.support.stableSort` to false in script section of sample. Refer to the following code.
 
{% highlight html %}

    <div id="defaultListView">
        <ul>
            <li data-ej-text="Discover Music">
                <ul>
                    <li data-ej-text="Hot Singles"></li>
                    <li data-ej-text="Rising Artists"></li>
                    <li data-ej-text="Live Music"></li>
                    <li data-ej-text="Best of 2013 So Far"></li>
                </ul>
            </li>
            <li data-ej-text="Sales and Events">
                <ul>
                    <li data-ej-text="100 Albums - $5 Each"></li>
                    <li data-ej-text="Hip-Hop and R&B Sale"></li>
                    <li data-ej-text="CD Deals"></li>
                </ul>
            </li>
            <li data-ej-text="Categories">
                <ul>
                    <li data-ej-text="Songs"></li>
                    <li data-ej-text="Bestselling Albums"></li>
                    <li data-ej-text="New Releases"></li>
                    <li data-ej-text="Bestselling Songs"></li>
                </ul>
            </li>
            <li data-ej-text="MP3 Albums">
                <ul>
                    <li data-ej-text="Rock"></li>
                    <li data-ej-text="Gospel"></li>
                    <li data-ej-text="Latin Music"></li>
                    <li data-ej-text="Jazz"></li>
                </ul>
            </li>
            <li data-ej-text="More in Music">
                <ul>
                    <li data-ej-text="Music Trade-In"></li>
                    <li data-ej-text="Redeem a Gift Card"></li>
                    <li data-ej-text="Branded T-Shirts"></li>
                    <li data-ej-text="Mobile MVC"></li>

                </ul>
            </li>
        </ul>
    </div>
    
{% endhighlight %}

Add the following script in your code.
    
{% highlight javascript %}

        ej.support.stableSort = false;
        $(function () {
            $("#defaultListView").ejListView({ width: 300 });
        });

{% endhighlight %}

## Disable an item while assigning dataSource

Selection of a particular list item can be prevented using the `preventSelection` field of ejListView. To change the item to disable state, add the `e-disable` class for items (whose selection are prevented) during initial rendering.

Refer to the following code.

{% highlight html %}

     <div id="default" >
      </div>

{% endhighlight %}

{% highlight javascript %}

         window.item = [{ text: "Discover Music" , preventSelection: true},
            { text: "Sales and Events" },
            { text: "Categories" , preventSelection: true},
            { text: "MP3 Albums" },
            {text: "More in Music" }];
        $(function () {
          $("#default").ejListView({showHeader: true, headerTitle: "Favorite", width:400, dataSource: item, enableGroupList: false });
          $("[data-preventselection*=true]").addClass("e-disable"); 
       
        });

{% endhighlight %}

Refer to the sample [here](https://jsplayground.syncfusion.com/qkxmnsdr)