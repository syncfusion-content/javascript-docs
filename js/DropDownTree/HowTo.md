---
layout: post
title: How to - DropDownTree widget for Syncfusion Essential JS
description: How To Section in DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: DropDownTree, dropdown, Adding Items, Set Focus, custommization
api: /api/js/ejdropdowntree
---

# How To

## Set focus to control initially?

[Access key](https://en.wikipedia.org/wiki/Access_key) property can be added in input element to set focus. Here focus is set by using access key + "j".

{% highlight html %}

<input type="text" id="itemList" />
     
{% endhighlight %}

{% highlight javascript %}
  
var localData = [{
        id: 1,
        name: "Windows Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 2,
        pid: 1,
        name: "Clark"
    },
    {
        id: 3,
        pid: 1,
        name: "Wright"
    },
    {
        id: 4,
        pid: 1,
        name: "Lopez"
    },
    {
        id: 6,
        pid: 1,
        name: "Anderson"
    },
    {
        id: 7,
        name: "Web Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 8,
        pid: 7,
        name: "Joshua"
    },
    {
        id: 9,
        pid: 7,
        name: "Matthew"
    },
    {
        id: 10,
        pid: 7,
        name: "David"
    },
    {
        id: 11,
        name: "Build Team",
        hasChild: true
    },
    {
        id: 12,
        pid: 11,
        name: "Ryan"
    },
    {
        id: 13,
        pid: 11,
        name: "Justin"
    },
    {
        id: 14,
        pid: 11,
        name: "Robert"
    },
    {
        id: 15,
        pid: 11,
        name: "Johnson"
    },
    {
        id: 16,
        name: "WPF Team",
        hasChild: true
    },
    {
        id: 17,
        pid: 16,
        name: "Rock"
    },
    {
        id: 18,
        pid: 16,
        name: "Gospel"
    },
    {
        id: 19,
        pid: 16,
        name: "Brown"
    },
    {
        id: 20,
        pid: 16,
        name: "Miller"
    }
];
$(function() {
    $('#itemList').ejDropDownTree({
        treeViewSettings: {
            fields: {
                id: "id",
                parentId: "pid",
                value: "id",
                text: "name",
                hasChild: "hasChild",
                dataSource: localData,
                expanded: "expanded"
            }
        },
        watermarkText: "Please select",
        width: "100%",

    });
    $(document).on("keydown", function(e) {
        if (e.altKey && e.keyCode === 74) { // j- key code.
            $("#itemList_wrapper").focus();
        }
    });
});{% endhighlight %}

## Clear the text of DropDownTree input?

To clear the text of the DropDownTree input, you can use [clearText](https://help.syncfusion.com/api/js/ejdropdowntree#methods:cleartext) method.

## Add an item dynamically to the DropDownTree?

You can use `addNode` method of `treeView` object with instance of DropDownTree widget to add a single node dynamically to the popup list. You can add multiple nodes using `addNodes` instead of `addNode`. Please refer
to [treeView](https://help.syncfusion.com/api/js/ejtreeview#methods:addnode).

Adding text and value is demonstrated in the following sample.


{% highlight html %}

     <input type="text" id="itemList" />
     
{% endhighlight %}

{% highlight javascript %}

var localData = [{
        id: 1,
        name: "Windows Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 2,
        pid: 1,
        name: "Clark"
    },
    {
        id: 3,
        pid: 1,
        name: "Wright"
    },
    {
        id: 4,
        pid: 1,
        name: "Lopez"
    },
    {
        id: 6,
        pid: 1,
        name: "Anderson"
    },
    {
        id: 7,
        name: "Web Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 8,
        pid: 7,
        name: "Joshua"
    },
    {
        id: 9,
        pid: 7,
        name: "Matthew"
    },
    {
        id: 10,
        pid: 7,
        name: "David"
    },
    {
        id: 11,
        name: "Build Team",
        hasChild: true
    },
    {
        id: 12,
        pid: 11,
        name: "Ryan"
    },
    {
        id: 13,
        pid: 11,
        name: "Justin"
    },
    {
        id: 14,
        pid: 11,
        name: "Robert"
    },
    {
        id: 15,
        pid: 11,
        name: "Johnson"
    },
    {
        id: 16,
        name: "WPF Team",
        hasChild: true
    },
    {
        id: 17,
        pid: 16,
        name: "Rock"
    },
    {
        id: 18,
        pid: 16,
        name: "Gospel"
    },
    {
        id: 19,
        pid: 16,
        name: "Brown"
    },
    {
        id: 20,
        pid: 16,
        name: "Miller"
    }
];
$(function() {
    $('#itemList').ejDropDownTree({
        treeViewSettings: {
            fields: {
                id: "id",
                parentId: "pid",
                value: "id",
                text: "name",
                hasChild: "hasChild",
                dataSource: localData,
                expanded: "expanded"
            }
        },
        watermarkText: "Please select",
        width: "100%",

    });
    var ddTreeObj = $('#itemList').data("ejDropDownTree");
    var newNode = {
        id: 8,
        name: "John"
    };
    ddTreeObj.treeView.addNode(newNode, $('#1'));
});

{% endhighlight %}

## Disable/ Enable the DropDownTree widget?

You can enable or disable the DropDownTree widget using [`enabled`](https://help.syncfusion.com/api/js/ejdropdowntree#members:enabled) property.

## Control the popup visibility via methods in script showPopup ()/hidePopup ()?

By default, popup list is shown on DropDownTree button click, but you can also display the list initially by enabling the [showPopupOnLoad](https://help.syncfusion.com/api/js/ejdropdowntree#members:popupsettings-showpopuponload) property. You can also use [showPopup ()](https://help.syncfusion.com/api/js/ejdropdowntree#methods:showpopup) or [hidePopup ()](https://help.syncfusion.com/api/js/ejdropdowntree#methods:hidepopup) method at run time to display or hide the popup list.

## Retrieve the selected item data from select event via arguments?

Bind the [select](https://help.syncfusion.com/api/js/ejdropdowntree#events:select) event, and you can retrieve the value from args.value.  

{% highlight html %}

     <input type="text" id="itemList" />

{% endhighlight %}

{% highlight javascript %}
  
var localData = [{
        id: 1,
        name: "Windows Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 2,
        pid: 1,
        name: "Clark"
    },
    {
        id: 3,
        pid: 1,
        name: "Wright"
    },
    {
        id: 4,
        pid: 1,
        name: "Lopez"
    },
    {
        id: 6,
        pid: 1,
        name: "Anderson"
    },
    {
        id: 7,
        name: "Web Team",
        hasChild: true,
        expanded: true
    },
    {
        id: 8,
        pid: 7,
        name: "Joshua"
    },
    {
        id: 9,
        pid: 7,
        name: "Matthew"
    },
    {
        id: 10,
        pid: 7,
        name: "David"
    },
    {
        id: 11,
        name: "Build Team",
        hasChild: true
    },
    {
        id: 12,
        pid: 11,
        name: "Ryan"
    },
    {
        id: 13,
        pid: 11,
        name: "Justin"
    },
    {
        id: 14,
        pid: 11,
        name: "Robert"
    },
    {
        id: 15,
        pid: 11,
        name: "Johnson"
    },
    {
        id: 16,
        name: "WPF Team",
        hasChild: true
    },
    {
        id: 17,
        pid: 16,
        name: "Rock"
    },
    {
        id: 18,
        pid: 16,
        name: "Gospel"
    },
    {
        id: 19,
        pid: 16,
        name: "Brown"
    },
    {
        id: 20,
        pid: 16,
        name: "Miller"
    }
];
$(function() {
    $('#itemList').ejDropDownTree({
        treeViewSettings: {
            fields: {
                id: "id",
                parentId: "pid",
                value: "id",
                text: "name",
                hasChild: "hasChild",
                dataSource: localData,
                expanded: "expanded"
            }
        },
        watermarkText: "Please select",
        width: "100%",
        select: function(args) {
            console.log("Value is " + args.value);
        }
    });


});    
{% endhighlight %}

## Add check all option in popup list?

You can use [headerTemplate](https://help.syncfusion.com/api/js/ejdropdowntree#members:headertemplate) property to add any HTML element. Code snippet to add check all option using [change](https://help.syncfusion.com/api/js/ejdropdowntree#events:change) event is given below,

{% highlight html %}

     <input type="text" id="itemList" />
	 
{% endhighlight %}

{% highlight css %}

.temp {
    height: 30px;
    display: block;
    padding-left: 13px;
    padding-top: 5px;
    border-bottom: 1px solid #c8c8c8;
}
.e-chkbox-wrap .e-text {
    font-size: 14px;
    padding-left: 10px;
}

     
{% endhighlight %}

{% highlight javascript %}

$(function() {
    var localData = [{
            id: 1,
            name: "Windows Team",
            hasChild: true,
            expanded: true
        },
        {
            id: 2,
            pid: 1,
            name: "Clark"
        },
        {
            id: 3,
            pid: 1,
            name: "Wright"
        },
        {
            id: 4,
            pid: 1,
            name: "Lopez"
        },
        {
            id: 6,
            pid: 1,
            name: "Anderson"
        },
        {
            id: 7,
            name: "Web Team",
            hasChild: true,
            expanded: true
        },
        {
            id: 8,
            pid: 7,
            name: "Joshua"
        },
        {
            id: 9,
            pid: 7,
            name: "Matthew"
        },
        {
            id: 10,
            pid: 7,
            name: "David"
        },
        {
            id: 11,
            name: "Build Team",
            hasChild: true
        },
        {
            id: 12,
            pid: 11,
            name: "Ryan"
        },
        {
            id: 13,
            pid: 11,
            name: "Justin"
        },
        {
            id: 14,
            pid: 11,
            name: "Robert"
        },
        {
            id: 15,
            pid: 11,
            name: "Johnson"
        },
        {
            id: 16,
            name: "WPF Team",
            hasChild: true
        },
        {
            id: 17,
            pid: 16,
            name: "Rock"
        },
        {
            id: 18,
            pid: 16,
            name: "Gospel"
        },
        {
            id: 19,
            pid: 16,
            name: "Brown"
        },
        {
            id: 20,
            pid: 16,
            name: "Miller"
        }
    ];

    $('#itemList').ejDropDownTree({
        treeViewSettings: {
            showCheckbox: true,
            fields: {
                id: "id",
                parentId: "pid",
                value: "id",
                text: "name",
                hasChild: "hasChild",
                dataSource: localData,
                expanded: "expanded"
            }
        },
        watermarkText: "Please select",
        headerTemplate: "<div class='temp' ><input id ='check' type='checkbox'  />   </div>"
    });
    $("#check").ejCheckBox({
        text: "Check All",
        change: "Change"
    });
    var ddTreeObj = $('#itemList').data("ejDropDownTree");


});

function Change(args) {
    window.flag = true;
    var obj = $('#itemList').ejDropDownTree("instance");
    if (args.isChecked) obj.checkAll();
    else obj.uncheckAll();
    window.flag = false;
}

{% endhighlight %}

The following screenshot exhibits the output of the above code,

![](HowTo_images/howto_checkboxtemplate.png)

## Add tooltip on hovering the DropDownTree’s items?
 
 In order to add  tooltip on hovering the DropDownTree popup items, use the htmlAttributes field in it. Generate a data source with a field for mapping the HtmlAttributes having the “title” attribute value to allow you to show the tooltip on hovering. The htmlAttributes field will set the HTML properties for the list items.

 {% highlight javascript %}
 
<input type="text" id="itemList" />

<script type="text/javascript">
    $(function() {
        var localData = [{
                id: 1,
                name: "Windows Team",
                hasChild: true,
                expanded: true
            },
            {
                id: 2,
                pid: 1,
                name: "Clark",
                tooltip: {
                    title: "Clark"
                }
            },
            {
                id: 3,
                pid: 1,
                name: "Wright",
                tooltip: {
                    title: "Wright"
                }
            },
            {
                id: 4,
                pid: 1,
                name: "Lopez",
                tooltip: {
                    title: "Lopez"
                }
            },
            {
                id: 6,
                pid: 1,
                name: "Anderson",
                tooltip: {
                    title: "Anderson"
                }
            },
            {
                id: 7,
                name: "Web Team",
                hasChild: true,
                expanded: true
            },
            {
                id: 8,
                pid: 7,
                name: "Joshua",
                tooltip: {
                    title: "Joshua"
                }
            },
            {
                id: 9,
                pid: 7,
                name: "Matthew",
                tooltip: {
                    title: "Matthew"
                }
            },
            {
                id: 10,
                pid: 7,
                name: "David",
                tooltip: {
                    title: "David"
                }
            },
            {
                id: 11,
                name: "Build Team",
                hasChild: true
            },
            {
                id: 12,
                pid: 11,
                name: "Ryan",
                tooltip: {
                    title: "Ryan"
                }
            },
            {
                id: 13,
                pid: 11,
                name: "Justin",
                tooltip: {
                    title: "Justin"
                }
            },
            {
                id: 14,
                pid: 11,
                name: "Robert",
                tooltip: {
                    title: "Robert"
                }
            },
            {
                id: 15,
                pid: 11,
                name: "Johnson",
                tooltip: {
                    title: "Johnson"
                }
            },
            {
                id: 16,
                name: "WPF Team",
                hasChild: true
            },
            {
                id: 17,
                pid: 16,
                name: "Rock",
                tooltip: {
                    title: "Rock"
                }
            },
            {
                id: 18,
                pid: 16,
                name: "Gospel",
                tooltip: {
                    title: "Gospel"
                }
            },
            {
                id: 19,
                pid: 16,
                name: "Brown",
                tooltip: {
                    title: "Brown"
                }
            },
            {
                id: 20,
                pid: 16,
                name: "Miller",
                tooltip: {
                    title: "Miller"
                }
            }
        ];

        $('#itemList').ejDropDownTree({
            treeViewSettings: {
                showCheckbox: true,
                fields: {
                    id: "id",
                    parentId: "pid",
                    value: "id",
                    text: "name",
                    hasChild: "hasChild",
                    dataSource: localData,
                    expanded: "expanded",
                    htmlAttribute: "tooltip"
                }
            },
            watermarkText: "Please select",

        });
    });
</script>

{% endhighlight %}

## Stop/Prevent the events (change/select) in the DropDownTree?

The client side events such as “select” or “change” can be prevented in the DropDownTree by using argument, cancel.

{% highlight javascript %}

<input type="text" id="selectCar" />
<script type="text/javascript">
    $(function() {
        var localData = [{
                id: 1,
                name: "Windows Team",
                hasChild: true,
                expanded: true
            },
            {
                id: 2,
                pid: 1,
                name: "Clark",
                tooltip: {
                    title: "Clark"
                }
            },
            {
                id: 3,
                pid: 1,
                name: "Wright",
                tooltip: {
                    title: "Wright"
                }
            },
            {
                id: 4,
                pid: 1,
                name: "Lopez",
                tooltip: {
                    title: "Lopez"
                }
            },
            {
                id: 6,
                pid: 1,
                name: "Anderson",
                tooltip: {
                    title: "Anderson"
                }
            },
            {
                id: 7,
                name: "Web Team",
                hasChild: true,
                expanded: true
            },
            {
                id: 8,
                pid: 7,
                name: "Joshua",
                tooltip: {
                    title: "Joshua"
                }
            },
            {
                id: 9,
                pid: 7,
                name: "Matthew",
                tooltip: {
                    title: "Matthew"
                }
            },
            {
                id: 10,
                pid: 7,
                name: "David",
                tooltip: {
                    title: "David"
                }
            },
            {
                id: 11,
                name: "Build Team",
                hasChild: true
            },
            {
                id: 12,
                pid: 11,
                name: "Ryan",
                tooltip: {
                    title: "Ryan"
                }
            },
            {
                id: 13,
                pid: 11,
                name: "Justin",
                tooltip: {
                    title: "Justin"
                }
            },
            {
                id: 14,
                pid: 11,
                name: "Robert",
                tooltip: {
                    title: "Robert"
                }
            },
            {
                id: 15,
                pid: 11,
                name: "Johnson",
                tooltip: {
                    title: "Johnson"
                }
            },
            {
                id: 16,
                name: "WPF Team",
                hasChild: true
            },
            {
                id: 17,
                pid: 16,
                name: "Rock",
                tooltip: {
                    title: "Rock"
                }
            },
            {
                id: 18,
                pid: 16,
                name: "Gospel",
                tooltip: {
                    title: "Gospel"
                }
            },
            {
                id: 19,
                pid: 16,
                name: "Brown",
                tooltip: {
                    title: "Brown"
                }
            },
            {
                id: 20,
                pid: 16,
                name: "Miller",
                tooltip: {
                    title: "Miller"
                }
            }
        ];

        $('#itemList').ejDropDownTree({
            treeViewSettings: {
                showCheckbox: true,
                fields: {
                    id: "id",
                    parentId: "pid",
                    value: "id",
                    text: "name",
                    hasChild: "hasChild",
                    dataSource: localData,
                    expanded: "expanded"
                }
            },
            select: "onSelect",
            watermarkText: "Please select",

        });
    });
</script>
   
{% endhighlight %}

While selecting the items in the DropDownTree, the select or change event will be triggered. In that, sets “true” to the cancel argument, which will prevent the further selecting of items in the DropDownTree.

{% highlight javascript %}

    function onSelect(args) {
        args.cancel = true;
    }
    
{% endhighlight %}

## Display the Validation message in the same line as the DropDownTree

In the DropDownTree control, the `display` property for the outer wrapper element will be set to `block`, by default. So, modifying it to `inline-block` will move the validation message to the same line as the DropDownTree. Refer to the following code.

{% highlight html %}

<form id="form1">
   <input type="text" id="selectCar" />
   <input id="validate" type="submit" value="Validate" />
</form>
<div id="carsList">
   <ul id="treeView">
      <li class="expanded">
         Artwork
         <ul>
            <li>
               Abstract
               <ul>
                  <li>2 Acrylic Mediums</li>
                  <li>Creative Acrylic</li>
                  <li>Modern Painting</li>
                  <li>Canvas Art</li>
                  <li>Black white</li>
               </ul>
            </li>
            <li>
               Children
               <ul>
                  <li>Preschool Crafts</li>
                  <li>School-age Crafts</li>
                  <li>Fabulous Toddler</li>
               </ul>
            </li>
            <li>
               Comic / Cartoon
               <ul>
                  <li>Batman</li>
                  <li>Adventures of Superman</li>
                  <li>Super boy</li>
               </ul>
            </li>
         </ul>
      </li>
      <li class="expanded">
         Books
         <ul>
            <li>
               Comics
               <ul>
                  <li>The Flash</li>
                  <li>Human Target</li>
                  <li>Birds of Prey</li>
               </ul>
            </li>
            <li>Entertaining</li>
            <li>Design</li>
         </ul>
      </li>
      <li>
         Music
         <ul>
            <li>
               Classical
               <ul>
                  <li>Medieval</li>
                  <li>Orchestral</li>
               </ul>
            </li>
            <li>Mass</li>
            <li>Folk</li>
         </ul>
      </li>
   </ul>
</div>

{% endhighlight %}

{% highlight css %}

<style> 
    .e-ddl { 
        display: inline-block; 
    } 
    #validate{
    display: block; 
    }
</style> 


{% endhighlight %}  

{% highlight javascript %}
 
$.validator.setDefaults({
    ignore: [],
    errorClass: 'e-validation-error', // to get the error message on jQuery validation
    errorPlacement: function(error, element) {
        $(error).insertAfter(element.closest(".e-widget"));
    }
    // any other default options and/or rules
});
//If necessary, we can create custom rules as below. here method defined for min
$.validator.addMethod("min",
    function(value, element, params) {
        if (!/Invalid|NaN/.test(value)) {
            return parseInt(value) > params;
        }
    }, 'Must be greater than 30.');
var target;
$(function() {
    $('#selectCar').ejDropDownTree({
        watermarkText: "Select a car",
        width: "50%",
        targetId: "carsList",
        validationRules: {
            required: true

        },
        validationMessage: {
            required: "* Required"

        }
    });
});

{% endhighlight %}

![](HowTo_images/validation.png)