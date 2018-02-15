---
layout: post
title: State Persistance with DropDownTree widget for Syncfusion Essential JS
description: State Persistence support to DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: Persistence, DropDownTree, dropdown, State Persistence
api: /api/js/ejDropDownTree
---

# State Persistence

DropDownTree stores its model in the local storage by defining the property [enablePersistence](https://help.syncfusion.com/api/js/ejdropdowntree#members:enablepersistence).
You can sustain the following functionalities in DropDownTree by enabling the persistence property.

* Selected items value in the textbox 
* Item’s selection state in the popup list 
* Collapsed/expanded item

Widget model will be stored in the local storage/cookies of the browser before page refresh, and reinitialized with the restored model after refresh.

{% highlight html %}

    

        <input type="text" id="itemList" />

     
{% endhighlight %}

{% highlight javascript %}

	 var localData = [
                    { id: 1, name: "Windows Team", hasChild: true, expanded: true },
                    { id: 2, pid: 1, name: "Clark" },
                    { id: 3, pid: 1, name: "Wright" },
                    { id: 4, pid: 1, name: "Lopez" },
                    { id: 6, pid: 1, name: "Anderson" },
                    { id: 7, name: "Web Team", hasChild: true, expanded: true },
                    { id: 8, pid: 7, name: "Joshua" },
                    { id: 9, pid: 7, name: "Matthew" },
                    { id: 10, pid: 7, name: "David" },
                    { id: 11, name: "Build Team", hasChild: true },
                    { id: 12, pid: 11, name: "Ryan" },
                    { id: 13, pid: 11, name: "Justin" },
                    { id: 14, pid: 11, name: "Robert" },
                    { id: 15, pid: 11, name: "Johnson" },
                    { id: 16, name: "WPF Team", hasChild: true },
                    { id: 17, pid: 16, name: "Rock" },
                    { id: 18, pid: 16, name: "Gospel" },
                    { id: 19, pid: 16, name: "Brown" },
                    { id: 20, pid: 16, name: "Miller" }];
        $(function () {
            $('#itemList').ejDropDownTree({               
                treeViewSettings: {
                    fields: { id: "id", parentId: "pid", value: "id", text: "name", hasChild: "hasChild", dataSource: localData, expanded: "expanded" }
                },
                enablePersistence: true,
                watermarkText: "Please select"
            });
        });

{% endhighlight %}

## Accessing currently stored state

Persistent state can be accessed through local storage using corresponding key name. Key name formation would be in the following order. It is a combination of plugin name and control id.

{% highlight javascript %}

	// DropDownTree state as string
	var DropDownTreeStateString = window.localStorage.ejDropDownTreeDropDown;

	//DropDownTree state as object
	var DropDownTreeStateObject = JSON.parse(window.localStorage.ejDropDownTreeDropDown);

{% endhighlight %}

N> In the above example, ‘ejDropDownTree’ is plugin name and ‘DropDown’ is control id.           
