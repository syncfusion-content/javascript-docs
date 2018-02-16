---
layout: post
title: Functionalities in the DropDownTree widget for Syncfusion Essential JS
description: Functionalities in the DropDownTree widget for Syncfusion Essential JS
platform: js
control: DropDownTree
documentation: ug
keywords: DropDownTree, dropdown, Selection, Grouping, Sorting
api: /api/js/ejDropDownTree
---
# Functionalities

## selectAll/unselectAll

By default, only one item can be selected from the popup list. For multiple selection, enable `allowMultiSelection` in [`treeViewSettings`](https://help.syncfusion.com/api/js/ejdropdowntree#members:treeViewSettings).

{% highlight html %}

     <input type="text" id="itemList" />
     <input type="checkbox" id="toggle" />
     
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
            allowMultiSelection: true,
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

    $("#toggle").ejToggleButton({
        "change": "onCheckUncheckAll",
        "defaultText": "Select All",
        "activeText": "Unselect All"
    });
});

function onCheckUncheckAll(args) {
    var ddTreeObj = $('#itemList').data("ejDropDownTree");
    if (args.isChecked) ddTreeObj.selectAll();
    else ddTreeObj.unselectAll());
}
    
{% endhighlight %}

## selectNode/unselectNode

You can select/unselect the particular node at run time by using [selectNode](https://help.syncfusion.com/api/js/ejdropdowntree#methods:selectnode) and [unselectNode](https://help.syncfusion.com/api/js/ejdropdowntree#methods:unselectnode) method. By default no item will be in checked state. 

{% highlight html %}

     <input type="text" id="itemList" />
     <input type="checkbox" id="toggle" />
     
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
            allowMultiSelection: true,
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

    $("#toggle").ejToggleButton({
        "change": "onSelectUnSelect",
        "defaultText": "Select Node",
        "activeText": "UnSelect Node"
    });
});

function onCheckUncheckAll(args) {
    var ddTreeObj = $('#itemList').data("ejDropDownTree");
    if (args.isChecked) ddTreeObj.selectNode($("#1"));
    else ddTreeObj.unselectNode($("#1"));
}

{% endhighlight %}

N> To select nodes, `allowMultiSelection` must be enabled in [`treeViewSettings`](https://help.syncfusion.com/api/js/ejdropdowntree#members:treeViewSettings).

## moveNode

You can move a node from one index to another index using the [`moveNode`](https://help.syncfusion.com/api/js/ejdropdowntree#methods:moveNode) method.


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
        width: "100%",

    });
    var ddTreeObj = $('#itemList').data("ejDropDownTree");
    ddTreeObj.checkNode($("#1"));
    ddTreeObj.moveNode("#1", "#10");
});

{% endhighlight %}

## RemoveNode/Remove all

You can remove a particular node or all the nodes using [`removeNode`](https://help.syncfusion.com/api/js/ejdropdowntree#methods:removeNode) and [`removeAll`](https://help.syncfusion.com/api/js/ejdropdowntree#methods:removeAll) methods, respectively.

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
        width: "100%",

    });
    var ddTreeObj = $('#itemList').data("ejDropDownTree");
    ddTreeObj.removeAll());
});

{% endhighlight %}

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
            allowMultiSelection: true,
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
    ddTreeObj.selectNode($("#3"));
    ddTreeObj.removeNode($("#3"));

});

{% endhighlight %}

## Validation

You can validate the DropDownList value on form submission by applying `validationRules` and `validationMessage`to the DropDownList. 

N> [jquery.validate.min](http://cdn.syncfusion.com/js/assets/external/jquery.validate.min.js) script file should be referred for validation, for more details, refer [here](http://jqueryvalidation.org/documentation).

### Validation Rules

The validation rules help you to verify the selected text by adding validation attributes to the input element. This can be set by using [validationRules](https://help.syncfusion.com/api/js/ejdropdownlist#members:validationrules) property.

### Validation Messages 

You can set your own custom error message by using [validationMessage](https://help.syncfusion.com/api/js/ejdropdownlist#members:validationmessage) property. To display the error message, specify the corresponding annotation attribute followed by the message to display.

N> jQuery predefined error messages to that annotation attribute will be shown when this property is not defined. The below given example explain this behavior of ‘required’ attribute,

When you initialize the DropDownList widget, it creates an input hidden element which is used to store the selected items value. Hence, the validation is performed based on the value stored in this hidden element.

Required field and min value validation is demonstrated in the below given example.

{% highlight html %}

<form id="form1">
   <input type="text" id="selectCar" />
   <input type="submit" value="Validate" />
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

![](Functionalities_images/validation.png)