---
layout: post
title: State Persistance with DropDownList widget for Syncfusion Essential JS
description: State Persistence support to DropDownList widget for Syncfusion Essential JS
platform: js
control: DropDownList
documentation: ug
keywords: Persistence, DropDownList, dropdown, State Persistence
api: /api/js/ejdropdownlist
---

# State Persistence

DropDownList stores its model is local storage by defining the property [enablePersistence](https://help.syncfusion.com/api/js/ejdropdownlist#members:enablepersistence).
You can sustain the below given functionalities in DropDownList by enabling persistence property,

* selected items value in the textbox 
* item’s selection state in the popup list 

Widget model will be stored in local storage / cookies of browser before page refreshes and reinitialized with the restored model after refresh.
The following properties are not included while maintaining DropDownList’s state in local storage to keep localStorage compact.

* Fields
* Data source
* Query 

{% highlight html %}

    <form id="form1">

        <input type="text" id="dropdown1" />

        <input type="submit" value="Post" />

    </form>
     
{% endhighlight %}

{% highlight javascript %}

	$(function() {
	    var items = [{
	        text: "Adams",
	        value: "emp1"
	    }, {
	        text: "James",
	        value: "emp2"
	    }, {
	        text: "Maria",
	        value: "emp3"
	    }, {
	        text: "Jessica",
	        value: "emp4"
	    }, {
	        text: "Jenneth",
	        value: "emp5"
	    }];

	    $('#dropdown1').ejDropDownList({
	        dataSource: items,
	        fields: {
	            text: "text",
	            value: "value"
	        },
	        enablePersistence: true
	    });
	});      		

{% endhighlight %}

## Accessing currently stored state

Persisted state can be accessed through local storage using corresponding key name. Key name formation would be in below order. It is combination of plugin name and control id.

{% highlight javascript %}

	// DropDownList state as string
	var dropdownlistStateString = window.localStorage.ejDropDownListDropDown;

	//DropDownList state as object
	var dropdownlistStateObject = JSON.parse(window.localStorage.ejDropDownListDropDown);

{% endhighlight %}

N> In the above example, ‘ejDropDownList’ is plugin name and ‘DropDown’ is control id.           
