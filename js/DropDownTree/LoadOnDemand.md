---
layout: post
title: Load on deamand in DropDownTree widget for Syncfusion Essential JS
description: Describes about loadOnDemand in DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: loadOnDemand, dropdowntree
api: /api/js/ejDropDownTree
---

## Load On Demand

Load on demand feature allows the DropDownTree items to load on request from the service/database, on clicking the expand icon. This functionality helps to improve performance on control’s initial rendering time as data items load only on request. 

The [loadOnDemand](https://help.syncfusion.com/api/js/ejdropdowntree#members:loadOnDemand) property is used to enable or disable the load on demand functionality of the DropDownTree.

{% highlight html %}

     <input type="text" id="itemList" />
     
{% endhighlight %}

{% highlight javascript %}
  
        // DataManager creation
        var dataManager = ej.DataManager({
            url: "http://js.syncfusion.com/demos/ejServices/api/TreeViewData/GetAllData",
            crossDomain: true,
            adaptor: new ej.WebApiAdaptor()

        });
        // Query creation
        var query = ej.Query().from("Categories").select("CategoryID,CategoryName").take(3);

        $(function () {
            $('#itemList').ejDropDownTree({
                watermarkText: "Please select",
                width: "100%",
                treeViewSettings: {
                    loadOnDemand: true,
                    fields: {
                        dataSource: dataManager,
                        id: "id", text: "name", parentId: "pid",
                    }
                }
            });
        });

{% endhighlight %}

![](LoadOnDemand_images/loadondemand.png)