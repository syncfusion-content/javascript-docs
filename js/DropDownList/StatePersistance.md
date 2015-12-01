---
layout: post
title: State Persistance with DropDownList
description: State Persistence support to DropDownList
platform: js
control: DropDownList
documentation: ug
---

## State Persistence

DropDownList stores its model is local storage by defining the property “[enablePersistence](http://helpjs.syncfusion.com/js/api/ejdropdownlist#members:enablepersistence)”.
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

{% highlight js %}

        <script type="text/javascript">
			
                 $(function() { 
                        var items = [  {
                            text: "Adams",
                            value: "emp1"
                        },  {
                            text: "James",
                            value: "emp2"
                        },  {
                            text: "Maria",
                            value: "emp3"
                        },  {
                            text: "Jessica",
                            value: "emp4"
                        },  {
                            text: "jenneth",
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
				
            </script>

{% endhighlight %}

### Accessing currently stored state

Persisted state can be accessed through local storage using corresponding key name. Key name formation would be in below order. It is combination of plugin name and control id.

{% highlight js %}

	// DropDownList state as string
	var dropdownlistStateString = window.localStorage.ejDropDownListdropdown;

	//DropDownList state as object
	var dropdownlistStateObject = JSON.parse(window.localStorage.ejDropDownListdropdown);

{% endhighlight %}

N> In the above example, ‘ejDropDownList’ is plugin name and ‘dropdown’ is control id.           
