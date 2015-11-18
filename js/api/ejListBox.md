---
layout: post
title: ejListBox
documentation: API
platform: js
metaname: 
metacontent: 
---


# ejListBox

The ListBox widget provides a list options to make user to choose an item from the list. It includes several other HTML elements such as images, textboxes, check box, and radio buttons and so on. It also supports data binding, template options and multi-select options.

$(element).ejListBox<span class="signature">()</span>

Example
{:.example}

{% highlight html %}

       <ul id="carsList">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
    </ul>

    <script>

        $('#list').ejListBox();

    </script>
	
{% endhighlight  %}

Requires
{:.require}

* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.listbox.js

* module:ej.checkbox.js

* module:ej.scroller.js

## Members

### allowDragAndDrop [Deprecated]  <span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddrop}

Enables/disables the drag and drop behavior of the ListBox widget.

N> Since this is a deprecated property we suggest to use **allowDrag** and **allowDrop** properties.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#list").ejListBox({

                allowDragAndDrop: true

            });
            
{% endhighlight %}

### allowDrag  <span class="type-signature type boolean">boolean</span>
{:#members:allowdrag} 

Enables/disables the dragging behavior of the ListBox widget’s item within a ListBox or between two ListBox widgets.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#list").ejListBox({
                allowDrag: true
            });
            
{% endhighlight %}

### allowDrop  <span class="type-signature type boolean">boolean</span>
{:#members:allowdrop} 

Accepts the items which are dropped in to it, when it is set to true. 

N> Need to enable allowDrag property to drag the list (li) item from the listbox control.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#list").ejListBox({
                allowDrop: true
            });

{% endhighlight %}

### allowMultiSelection <span class="type-signature type boolean">boolean</span>
{:#members:allowmultiselection}  

Enables or disables multiple selection.

Default Value:
{:.param} false

Example 
{:.example}

{% highlight js %}

    $('#list').ejListBox({allowMultiSelection: true}); 

{% endhighlight %}

### allowVirtualScrolling <span class="type-signature type boolean">boolean</span>
{:#members:allowvirtualscrolling}  

Loads the list data on demand via scrolling behavior to improve the application’s performance. There are two ways to load data which can be defined using “virtualScrollMode” property.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#customerlist").ejListBox({

            allowVirtualScrolling: true           

              });

{% endhighlight %}

### caseSensitiveSearch <span class="type-signature type boolean">boolean</span>
{:#members:casesensitivesearch} 
 
Enables or disables the case sensitive search for list item by typing the text (search) value.

N> It works only when the enableIncrementalSearch is set as true.

Default Value: 
{:.param} false

Example
{:.example}

{% highlight js %}

    $('#list).ejListBox({
    
    enableIncrementalSearch : true ,
    
        caseSensitiveSearch : true 
    
    }); 

{% endhighlight %}  


### cascadeTo  <span class="type-signature type string">string</span>
{:#members:cascadeto} 

Dynamically populate data of a list box while selecting an item in another list box i.e. rendering child list box based on the item selection in parent list box. This property accepts the id of the child ListBox widget to populate the data.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox({ 

        cascadeTo: 'countryList' 

        });

{% endhighlight %}


### checkAll [Deprecated] <span class="type-signature type boolean">boolean</span>
{:#members:checkall} 

To check all the items of the ListBox widget. It works only when the showCheckbox property is set to true. 

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({showCheckbox: true, checkAll: true }); 

{% endhighlight %}

### checkedItems [Deprecated] <span class="type-signature type array">array</span>
{:#members:checkeditems} 

List of items to be checked by default using its index. It works only when the showCheckbox property is set to true. 

N> Since this is a deprecated property we suggest to use checkedIndices property.

Default Value:
{:.param} []

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({ showCheckbox:true, checkedItems : [1,2] }); 

{% endhighlight %}

### checkedItemlist [Deprecated] <span class="type-signature type array">array</span>
{:#members:checkeditemlist} 

List of items to be checked by default using its index. It works only when the showCheckbox property is set to true. 

N> Since this is a deprecated property we suggest to use checkedIndices property.

Default Value:
{:.param} []

Example
{:.example}


{% highlight js %}

    $('#list').ejListBox({ showCheckbox:true, checkedItemlist : [1,2] }); 

{% endhighlight %}

### checkItemsByIndex [Deprecated] <span class="type-signature type string">string</span>
{:#members:checkitemsbyindex} 

List of items to be checked by default using index values. It works only when the showCheckbox property is set to true. 

N> Since this is a deprecated property we suggest to use checkedIndices property.

Default Value: 
{:.param} null

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox({ showCheckbox: true, checkItemsByIndex: "2,3" });
        
{% endhighlight %}

### checkedIndices <span class="type-signature type string">string</span>
{:#members:checkedindices} 

Set of list items to be checked by default using its index. It works only when the showCheckbox property is set to true. 

Default Value:
{:param} null

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox({ showCheckbox: true, checkedIndices: "2,3" });
        
{% endhighlight %}

### cssClass <span class="type-signature type string">string</span>
{:#members:cssclass}

The root class for the ListBox widget to customize the existing theme.

Default Value:
{:.param} “”

Example
{:.example}

{% highlight js %}

        $("#list").ejListBox({ cssClass: 'gradient-lime' });
        
 {% endhighlight %}


### dataSource <span class="type-signature type JSONobject">JSONobject</span>
{:#members:datasource}

Contains the list of data for generating the list items.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

            $("#customerlist").ejListBox({

                dataSource: customerData

            });
            
 {% endhighlight %}

### disableItemsByIndex [Deprecated] <span class="type-signature type string">string</span>
{:#members:disableitemsbyindex}

Disables set of list items using its index value.

Default Value:
{:.param} null

Example
{:.example} 

{% highlight js %}

    $('#list').ejListBox({disableItemsByIndex : "2,3"}); 

{% endhighlight %}

### enabled <span class="type-signature type boolean">boolean</span>
{:#members:enabled}

Enables or disables the ListBox widget.

Default Value:
{:.param} true

Example 
{:.example}

{% highlight js %}

    $('#list').ejListBox({enabled : false }); 

{% endhighlight %}

### enableItemsByIndex [Deprecated] <span class="type-signature type string">string</span>
{:#members:enableitemsbyindex}

Enables the set of disabled list items using its index value.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

            $('#list').ejListBox({ enableItemsByIndex: "2,3" });

{% endhighlight  %}

### enableLoadOnDemand [Deprecated] <span class="type-signature type boolean">boolean</span>
{:#members:enableloadondemand}

Loads data on demand for the ListBox widget via scrolling behavior.If this is set to true, this will implicitly make allowVirtualScrolling to true and sets virtualScrollMode to “normal”.

N> Since this is a deprecated property we suggest to use allowVirtualScrolling property.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#customerlist").ejListBox({

                enableLoadOnDemand: true

            });

        });
        
 {% endhighlight %}



### enableIncrementalSearch <span class="type-signature type boolean">boolean</span>
{:#members:enableincrementalsearch}

Enables or disables the search behavior to find the specific list item by typing the text value.

Default Value:
{:.param} false

Example 
{:.example}

{% highlight js %}

    $('#list').ejListBox({enableIncrementalSearch : true}); 

{% endhighlight %}

### enablePersistence <span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true.

N> [Local storage](http://www.w3schools.com/html/html5_webstorage.asp) is supported only in Html5 supported browsers. If the browsers don’t have support for local storage, browser cookies will be used to maintain the state.

Default Value:
{:.param} false

Example 
{:.example}

{% highlight js %}

    $('#list').ejListBox({enablePersistence : false}); 

{% endhighlight %}

### enableRTL <span class="type-signature type boolean">boolean</span>
{:#members:enablertl}

Displays the ListBox widget’s content from right to left when enabled.

Default Value:
{:.param} false

Example 
{:.example}

{% highlight js %}

    $('#list').ejListBox({enableRTL : true }); 

{% endhighlight %}

### enableVirtualScrolling  [Deprecated] <span class="type-signature type boolean">boolean</span>
{:#members:enablevirtualscrolling}

Loads data on demand for the ListBox widget via scrolling behavior. If this is set to true, this will implicitly make allowVirtualScrolling to true and sets virtualScrollMode to “continuous”.

N> Since this is a deprecated property we suggest to use allowVirtualScrolling property.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

            $("#customerlist").ejListBox({
            
            enableVirtualScrolling: true           
            
            });

{% endhighlight %}


### fields <span class="type-signature type JSONobject">JSONobject</span>
{:#members:fields}

Mapping fields for the data items of the ListBox widget.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

        $("#countrylist").ejListBox({ 

        dataSource: countries, 
        
        fields: { text: "name", value: "key" } 
        
        });

{% endhighlight %}

<table>
<tr>
<td>
fields.category [Deprecated]</td><td>
The grouping in the ListBox widget can be defined using this field. 
N> Since this is deprecated we suggest you to use fields.groupBy API.
</td></tr>
<tr>
<td>
fields.checkBy </td><td>
Defines the specific field name which contains Boolean values to specify whether the list items to be checked by default or not. </td></tr>
<tr>
<td>
fields.groupBy </td><td>
The grouping in the ListBox widget can be defined using this field. </td></tr>
<tr>
<td>
fields.htmlAttributes</td><td>
Defines the html attributes such as id, class, styles for the specific ListBox item.</td></tr>
<tr>
<td>
fields.id</td><td>
Defines the specific field name which contains id values for the list items.</td></tr>
<tr>
<td>
fields.imageUrl</td><td>
Defines the imageURL for the image to be displayed in the ListBox item.</td></tr>
<tr>
<td>
fields.imageAttributes</td><td>
Defines the image attributes such as height, width, styles and so on.</td></tr>
<tr>
<td>
fields.selected [Deprecated]</td><td>
Defines the specific field name which contains Boolean values to specify whether the list items to be selected by default or not.Note: Since this is deprecated we suggest you to use fields.selectBy API.</td></tr>
<tr>
<td>
fields.selectBy</td><td>
Defines the specific field name which contains Boolean values to specify whether the list items to be selected by default or not.</td></tr>
<tr>
<td>
fields.spriteCssClass</td><td>
Defines the sprite css class for the image to be displayed.</td></tr>
<tr>
<td>
fields.tableName</td><td>
Defines the table name to get the specific set of list items to be loaded in the ListBox widget while rendering with remote data.</td></tr>
<tr>
<td>
fields.text</td><td>
Defines the specific field name in the data source to load the list with data.</td></tr>
<tr>
<td>
fields.tooltipText [Deprecated]</td><td>
Defines the specific field name to display the tooltip text for all the list items.</td></tr>
</table>


### height  <span class="type-signature type string">string</span>
{:#members:height}

Defines the height of the ListBox widget.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({ height: "300"}); 

{% endhighlight %}

### itemsCount <span class="type-signature type integer">integer</span>
{:#members:itemscount}

The number of list items to be shown in the ListBox widget. The remaining list items will be scrollable.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({itemsCount: 8}); 

{% endhighlight %}

### itemRequestCount  <span class="type-signature type integer">integer</span>
{:#members:itemrequestcount}

The number of list items to be loaded in the list box while enabling virtual scrolling and when virtualScrollMode is set to continuous.

Default Value:
{:.param} 5

Example
{:.example}

{% highlight js %}

            $("#customerlist").ejListBox({

                itemRequestCount: 6 

            });

        });
        
 {% endhighlight %}

### loadDataOnInit <span class="type-signature type boolean">boolean</span>
{:#members:loaddataoninit}

Loads data for the listbox by default (i.e. on initialization) when set to true.

N> It is used along with cascading feature. See also [cascadeTo](http://help.syncfusion.com//js/api/ejlistbox#members:cascadeto).

Default Value: 
{:.param} true

Example
{:.example}

 {% highlight js %}

        $('#countryList').ejListBox({ 

            loadDataOnInit: false 

        });
        
 {% endhighlight %}
 
### query <span class="type-signature type ej.Query">ej.Query</span>
{:#members:query}

The query to retrieve required data from the data source.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

            var query = ej.Query()

                   .from("Customers").take(10);
                   
            $("#customerlist").ejListBox({

                query: query

            });

{% endhighlight %}

### selectedItemIndex [Deprecated] <span class="type-signature type integer">integer</span>
{:#members:selecteditemindex}

The item to be selected by default using its index.

N> Since this is a deprecated property we suggest to use selectedIndex property.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({selectedItemIndex : 2}); 
    
{% endhighlight %}

### selectedItemlist [Deprecated] <span class="type-signature type array">array</span>
{:#members:selecteditemlist}

The list of items to be selected by default using its index values. To use this property allowMultiSelection should be enabled.

N> Since this is a deprecated property we suggest to use selectedIndices property.

Default Value:
{:.param} []

Example
{:.example}

{% highlight js %}

        $('#list).ejListBox({ 
        
        allowMultiSelection:true,
        
            selectedItemlist : [1,2] 
        
        }); 

{% endhighlight %}

### selectedItems [Deprecated] <span class="type-signature type array">array</span>
{:#members:selecteditems}

The list of items to be selected by default using its index. To use this property allowMultiSelection should be enabled.

N> Since this is a deprecated property we suggest to use selectedIndices property.

Default Value:
{:.param} []

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({allowMultiSelection:true, selectedItems : [1,2]}); 

{% endhighlight %}

### selectedIndex  <span class="type-signature type integer">integer</span>
{:#members:selectedindex}

The list item to be selected by default using its index.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({selectedIndex : 2}); 

{% endhighlight %}

### selectedIndices <span class="type-signature type array">array</span>
{:#members:selectedindices}

The list items to be selected by default using its indices. To use this property allowMultiSelection should be enabled.

Default Value:
{:.param} []

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({selectedIndices : [2,4]}); 

{% endhighlight %}

### showCheckbox <span class="type-signature type boolean">boolean</span>
{:#members:showcheckbox}

Enables/Disables the multi selection option with the help of checkbox control.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({showCheckbox: true }); 

{% endhighlight %}

### showRoundedCorner <span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}

To display the ListBox container with rounded corners.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

    $('#list').ejListBox({ showRoundedCorner: true }); 

{% endhighlight %}
### template <span class="type-signature type string">string</span>
{:#members:template}

The template to display the ListBox widget with customized appearance.

Default Value: 
{:.param} null

Example
{:.example}

{% highlight js %}

            $('#selectExperts').ejListBox({

                template: '&lt;div class="ename"&gt; ${text} &lt;/div&gt;&lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;'

            });
        });
        
 {% endhighlight %}

### unCheckAll [Deprecated] <span class="type-signature type boolean">boolean</span>
{:#members:uncheckall}

Unchecks all the checked list items. It is dependent on showCheckbox property.

Default Value:
{:.param} false

Example
{:.example}

{% highlight js %}

    $("#button").ejButton({ text: "uncheck All list Items", click: "uncheckall" });

{% endhighlight %}

### uncheckItemsByIndex [Deprecated] <span class="type-signature type string">string</span>
{:#members:uncheckitemsbyindex}

Unchecks the list of items by using its index values. It is dependent on showCheckbox property.

Default Value:
{:.param} null

Example
{:.example}

{% highlight js %}

            $('#list').ejListBox({ showCheckbox: true, uncheckItemsByIndex: "2,3" });
            
{% endhighlight %}

### value <span class="type-signature type integer">integer</span>
{:#members:value}

Holds the selected items values and used to bind value to the list item using angular and knockout.

Default Value:
{:.param} “”

Example
{:.example}

{% highlight html %}
    <div ng-app="ListCtrl" ng-controller="ListBoxCtrl">

        <ul id="bookSelect" ej-listbox e-datasource="dataList" e-value="value"></ul>
        <input type="text" style="margin-top:20px;" id="dropValue" class="input ejinputtext" ng-model="value" />;

    </div>
        <script type="text/javascript">

            var list = [

            { empid: "cr1", text: "Dodge Avenger" },

            { empid: "cr2", text: "Chrysler 200" },

            { empid: "cr3", text: "Ford Focus" },

            { empid: "cr4", text: "Ford Taurus", },

            { empid: "cr5", text: "Dazzler", },

            { empid: "cr6", text: "Chevy Spark", },

            { empid: "cr7", text: "Chevy Volt", },

            { empid: "cr8", text: "Honda Fit", },

            { empid: "cr9", text: "Honda Crosstour", },

            { empid: "cr10", text: "Acura RL", },

            { empid: "cr11", text: "Hyundai Elantra", },

            { empid: "cr12", text: "Mazda3", }

            ];

            angular.module('ListCtrl', ['ejangular'])

            .controller('ListBoxCtrl', function ($scope) {

                $scope.dataList = list;

                $scope.value = "Ford Taurus";

            });

            $(function () {

                var target = $('#bookSelect').data("ejListBox");

                target.selectItemByIndex(3);

            });
            </script>

            
 {% endhighlight %}

### virtualScrollMode <span class="type-signature type enum">enum</span>
{:#members:virtualscrollmode}

Specifies the virtual scroll mode to load the list data on demand via scrolling behavior. There are two types of mode.

* continuous:

Each time when we scroll to the end of the ListBox widget, the other set of list items will get loaded.

* normal:

This mode allows you to load the list box data while scrolling i.e. each time the scroll bar is scrolled, it will send request to the server to load the data.

Default Value:
{:.param} “normal”. 

Example
{:.example}

 {% highlight js %}
            $("#customerlist").ejListBox({
            
                    allowVirtualScrolling: true, 
            
            virtualScrollMode: "continuous"           
            
            });

 {% endhighlight %}

### width <span class="type-signature type string">string</span>
{:#members:width}

Defines the width of the ListBox widget.

Default Value:
{:.param} null

Example
{:.example}

 {% highlight js %}
 
    $('#list').ejListBox({ width: "220"}); 
    
 {% endhighlight %}
 
 
 
## Methods


### addItem<span class="signature">(listItem, index)</span>
{:#methods:additem}

Adds a given list items in the ListBox widget at a specified index. It accepts two parameters. 

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
listItem</td><td>
object / string</td><td>
This can be a list item object (for JSON binding) or a string (for UL and LI rendering). Also we can the specify this as an array of list item object or an array of strings to add multiple items.</td></tr>
<tr>
<td>
index</td><td>
Integer</td><td>
The index value to add the given items at the specified index. If index is not specified, the given items will be added at the end of the list.</td></tr>
</table>


Example
{:.example}

{% highlight js %}

        $('#list').ejListBox("addItem","Audi R8",1); 

{% endhighlight %}

### checkAll<span class="signature">()</span>
{:#methods:checkAll}

Checks all the list items in the ListBox widget. It is dependent on showCheckbox property.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox("checkAll"); 

{% endhighlight %}


### checkItemByIndex<span class="signature">(index)</span>
{:#methods:checkitembyindex}

Checks a list item by using its index. It is dependent on showCheckbox property.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer</td><td>
Index of the listbox item to be checked. If index is not specified, the given items will be added at the end of the list.</td></tr>
</table>

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox("checkItemByIndex",3); 

{% endhighlight %}


### checkItemsByIndices<span class="signature">(index/indices) </span>
{:#methods:checkitemsbyindices}

Checks multiple list items by using its index values. It is dependent on showCheckbox property.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index/indices</td><td>
Integer array/ string</td><td>
Index/Indices of the listbox items to be checked. If index is not specified, the given items will be added at the end of the list.</td></tr>
</table>


N> This method accepts array of integers or a string containing integer values separated by commas as an argument.

Example
{:.example}

{% highlight js%}
        
        $('#list').ejListBox("checkItemsByIndices","2,3");

{% endhighlight %}


### disable<span class="signature">()</span>
{:#methods:disable}

Disables the ListBox widget.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("disable"); 

{% endhighlight %}


### disableItem<span class="signature">(text)</span>
{:#methods:disableitem}

Disables a list item by passing the item text as parameter.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
String</td><td>
Text of the listbox item to be disabled.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("disableItem","Audi A5"); 

{% endhighlight %}


### disableItemByIndex<span class="signature">(index)</span>
{:#methods:disableitembyindex}

Disables a list Item using its index value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
integer</td><td>
Index of the listbox item to be disabled.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("disableItemByIndex" ,3); 

{% endhighlight %}


### disableItemsByIndices<span class="signature">(indices)</span>
{:#methods:disableitemsbyindices}

Disables set of list Items using its index values.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Indices</td><td>
Integer array/ string</td><td>
Indices of the listbox item to be disabled.</td></tr>
</table>

Example
{:.example}

{% highlight js %}

        $('#list').ejListBox("disableItemsByIndices" ,"3,5,7"); 

{% endhighlight %}


### enable<span class="signature">()</span>
{:#methods:enable}

Enables the ListBox widget when it is disabled.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("enable");
            
{% endhighlight %}


### enableItem<span class="signature">(text)</span>
{:#methods:enableitem}

Enables a list Item using its item text value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
Text of the listbox item to be enabled.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("enableItem", "Audi A5");

{% endhighlight %}


### enableItemByIndex<span class="signature">(index)</span>
{:#methods:enableitembyindex}

Enables a list item using its index value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
Index of the listbox item to be enabled.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("enableItemByIndex", 5);

{% endhighlight %}


### enableItemsByIndices<span class="signature">(indices)</span>
{:#methods:enableitemsbyindices}

Enables a set of list Items using its index values.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
indices</td><td>
Integer array/ string</td><td>
Indices of the listbox items to be enabled.</td></tr>
</table>

Example
{:.example}

{% highlight js%}


        $('#list').ejListBox("enableItemsByIndices", "3,5");

{% endhighlight %}


### getCheckedItems<span class="signature">()</span>
{:#methods:getcheckeditems}

Returns the list of checked items in the ListBox widget. It is dependent on showCheckbox property.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("getCheckedItems");

{% endhighlight %}


### getSelectedItems<span class="signature">()</span>
{:#methods:getselecteditems}

Returns the list of selected items in the ListBox widget. 

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("getSelectedItems");

{% endhighlight %}


### getIndexByText<span class="signature">(text)</span>
{:#methods:getindexbytext}


Returns an item’s index based on the given text.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
The list item text (label)</td></tr>
</table>


Example
{:.example}


{% highlight js%}

        $('#list').ejListBox("getIndexByText", "Audi A5");

{% endhighlight %}


### getIndexByValue<span class="signature">(value)</span>
{:#methods:getindexbyvalue}

Returns an item’s index based on the value given.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
value</td><td>
string</td><td>
The list item’s value</td></tr>
</table>

Example
{:.example}

{% highlight js%}

        $('#list').ejListBox("getIndexByValue", "audia4");

{% endhighlight %}


### getTextByIndex<span class="signature">(index)</span>
{:#methods:gettextbyindex}

Returns an item’s text (label) based on the index given.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
The list item index.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("getTextByIndex", 3);

{% endhighlight %}


### getItemByIndex<span class="signature">(index)</span>
{:#methods:getitembyindex}

Returns a list item’s object using its index.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
The list item index.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("getItemByIndex", 3);

{% endhighlight %}


### getItemByText<span class="signature">(text)</span>
{:#methods:getitembytext}

Returns a list item’s object based on the text given.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
The list item text.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("getItemByText", "Audi A7");

{% endhighlight %}


### moveDown<span class="signature">()</span>
{:#methods:movedown}

Selects the next item based on the current selection.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("moveDown");
            
{% endhighlight %}


### moveUp<span class="signature">()</span>
{:#methods:moveup}

Selects the previous item based on the current selection.

 N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("moveUp");

{% endhighlight %}            


### refresh<span class="signature">(refreshData)</span>
{:#methods:refresh}

Refreshes the ListBox widget.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
refreshData</td><td>
Boolean</td><td>
Refreshes both the datasource and the dimensions of the ListBox widget when the parameter is passed as true, otherwise only the ListBox dimensions will be refreshed.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

                $("#customerlist").ejListBox("refresh", true);

{% endhighlight %}


### removeItem<span class="signature">()</span> [Deprecated]
{:#methods:removeitem}

Removes the selected list items from the listbox. 


N> 1. This method does not accept any arguments.
N> 2.Since this method is deprecated we suggest you to use removeSelectedItems method.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("removeItem"); 
            
 {% endhighlight %}         


### removeSelectedItems<span class="signature">()</span>
{:#methods:removeselecteditems}

Removes the selected list items from the listbox.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("removeSelectedItems");

{% endhighlight %}


### removeItemByText<span class="signature">(text)</span>
{:#methods:removeitembytext}

Removes a list item by using its text.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
Text of the listbox item to be removed. </td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("removeItemByText","Audi A5");

{% endhighlight %}


### removeItemByIndex<span class="signature">(index)</span>
{:#methods:removeitembyindex}

Removes a list item by using its index value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
Index of the listbox item to be removed.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("removeItemByIndex", 2);

{% endhighlight %}


### selectAll<span class="signature">()</span>
{:#methods:selectall}

Selects all the list items dynamically. This method will works when the allowMultiSelection property is set as true.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectAll");

{% endhighlight %}


### selectItemByText<span class="signature">(text)</span>
{:#methods:selectItemByText}

Selects the list tem using its text value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
Text of the listbox item to be selected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectItemByText", "Audi A5");

{% endhighlight %}


### selectItemByValue<span class="signature">(value)</span>
{:#methods:selectitembyvalue}

Selects list tem using its value property.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
value</td><td>
String</td><td>
Value of the listbox item to be selected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectItemByValue", "audia5");

{% endhighlight %}


### selectItemByIndex<span class="signature">(index)</span>
{:#methods:selectitembyindex}

Selects list item using its index value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
Index of the listbox item to be selected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectItemByIndex", 2);

{% endhighlight %}


### selectItemsByIndex<span class="signature">(index/indices)</span> [Deprecated]
{:#methods:selectitemsbyindex}

Selects a set of list items through its index values. This method will works when allowMultiSelection property is set to true.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index/Indices</td><td>
Integer array/ string</td><td>
Index/Indices of the listbox items to be selected.</td></tr>
</table>

N> Since this property is deprecated, we suggest you to use selectItemsByIndices property.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectItemsByIndex", "2,3,5");

{% endhighlight %}


### selectItemsByIndices<span class="signature">(indices)</span> [Deprecated]
{:#methods:selectitemsbyindices}

Selects a set of list items through its index values. 

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index/Indices</td><td>
Integer array/ string</td><td>
Index/Indices of the listbox item to be selected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("selectItemsByIndices", "2,3,5");
            
{% endhighlight %}


### unCheckAll<span class="signature">()</span> [Deprecated]
{:#methods:uncheckall}

Unchecks all the checked list items in the ListBox widget. To use this method showCheckbox property to be set as true.

N> 1. This method does not accept any arguments.
N> 2. Since this method is deprecated, we suggest you to use  uncheckAll method.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unCheckAll");

{% endhighlight %}


### uncheckAll<span class="signature">()</span>
{:#methods:uncheckAll}

Unchecks all the checked list items in the ListBox widget. To use this method showCheckbox property to be set as true.

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("uncheckAll");

{% endhighlight %}


### uncheckItemByIndex<span class="signature">(index)</span>
{:#methods:uncheckitembyindex}

Unchecks a checked list item using its index value. To use this method showCheckbox property to be set as true.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
Index of the listbox item to be unchecked.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("uncheckItemByIndex", 3);
 
{% endhighlight %}


### uncheckItemsByIndices<span class="signature">(indices)</span>
{:#methods:uncheckitemsbyindices}

Unchecks the set of checked list items using its index values. To use this method showCheckbox property must be set to true.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
indices</td><td>
Integer array/ string</td><td>
Indices of the listbox item to be unchecked.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("uncheckItemsByIndices", "2,3,5");

{% endhighlight %}


### unSelectAll<span class="signature">()</span> [Deprecated]
{:#methods:unselectall}

Unselect all the selected list items in the ListBox widget. 

N> 1. This method does not accept any arguments.
N> 2. Since this method is deprecated, we suggest you to use unselectAll method.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unSelectAll");

{% endhighlight %}


### unselectAll<span class="signature">()</span>
{:#methods:unselectall}

Unselect all the selected list items in the ListBox widget. 

N> This method does not accept any arguments.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unselectAll");


{% endhighlight %}


### unselectItemByIndex<span class="signature">(index)</span>
{:#methods:unselectitembyindex}

Unselects a selected list item using its index value

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index</td><td>
Integer </td><td>
Index of the listbox item to be unselected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unselectItemByIndex", 2);

{% endhighlight %}


### unselectItemsByIndex<span class="signature">(index/indices)</span> [Deprecated]
{:#methods:unselectitemsbyindex}

Unselects a set of list items using its index values. 

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
index/Indices</td><td>
Integer array/ string</td><td>
Index/Indices of the listbox item to be unselected.</td></tr>
</table>


N> Since this property is deprecated, we suggest you to use unselectItemsByIndices property.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unselectItemsByIndex", "2,3,5");

{% endhighlight %}


### unselectItemByText<span class="signature">(text)</span>
{:#methods:unselectitembytext}

Unselects a selected list item using its text value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
text</td><td>
string</td><td>
Text of the listbox item to be unselected.</td></tr>
</table>

Example
{:.example}


{% highlight js%}

            $('#list').ejListBox("unselectItemByText", "Audi A5");

{% endhighlight %}


### unselectItemByValue<span class="signature">(value)</span>
{:#methods:unselectitembyvalue}

Unselects a selected list item using its value.

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
value</td><td>
string</td><td>
Value of the listbox item to be unselected.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unselectItemByValue", "audia5");

{% endhighlight %}


### unselectItemsByIndices<span class="signature">(indices)</span>
{:#methods:unselectitemsbyindices}

Unselects a set of list items using its index values. 

<table>
<tr>
<td>
<b>Parameters</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
indices</td><td>
Integer array/ string</td><td>
Indices of the listbox item to be unselected.</td></tr>
</table>


N> This method accepts array of integers or a string containing list of integer values separated by commas as an argument.

Example
{:.example}

{% highlight js%}

            $('#list').ejListBox("unselectItemsByIndices", "2,3,5");

{% endhighlight %}



## Events

### actionSuccess
{:#events:actionsuccess}

Triggers when the data requested from AJAX will get successfully loaded in the ListBox widget. 

N> It internally uses jQuery ajaxSuccess event. For details refer [here](http://api.jquery.com/ajaxsuccess/).

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		actionSuccess: function(args) { 
		
		//do something
		
		}          
		
		});
{% endhighlight %}


### actionComplete
{:#events:actioncomplete}

Triggers when the AJAX requests complete. The request may get failed or succeed.

N> It internally uses jQuery ajaxComplete event. For details refer [here](http://api.jquery.com/ajaxcomplete/).

Example
{:.example}


{% highlight js%}

		$("#list").ejListBox({
		
		actionComplete: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### actionFailure
{:#events:actionfailure}

Triggers when the data requested from AJAX get failed.

N> It internally uses jQuery ajaxError event. For details refer [here](http://api.jquery.com/ajaxerror/).

 Example
 {:.example}

{% highlight js%}
		
		$("#list").ejListBox({
		
		actionFailure: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### change 
{:#events:change}

Triggers when the item selection is changed.

<table>
<tr>
<th>
<b>Event Arguments</b></th><th>
<b>Type</b></th><th>
<b>Description</b></th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		change: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### checkChange
{:#events:checkchange}

Triggers when the list item is checked or unchecked.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

Example
{:.example}


{% highlight js%}

		$("#list").ejListBox({
		
		checkChange: function(args) { 
		
		//do something
		
		}          
		
		});


{% endhighlight %}


### create
{:#events:create}

Triggers when the ListBox widget is created successfully.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
string</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		create: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### destroy
{:#events:destroy}

Triggers when the ListBox widget is destroyed successfully.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		destroy: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemDrag
{:#events:itemdrag}

Triggers when the list item is being dragged.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		itemDrag: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemRequest [Deprecated]
{:#events:itemrequest}

Triggers when the virtual scrolling, requests for new set of list items to be loaded in the ListBox widget.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.originalEvent</td><td>
Object</td><td>
Returns the event arguments like event type,timestamp, etc.,</td></tr>
<tr>
<td>
argument.scrollData</td><td>
Object</td><td>
Returns the dimension and position properties for scrolled element.</td></tr>
</table>

Example
{:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		itemRequest: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemDragStart
{:#events:itemdragstart}

Triggers when the list item is ready to be dragged. 

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		itemDragStart: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemDragStop
{:#events:itemdragstop}

Triggers when the list item stops dragging. 

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		itemDragStop: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemDropped [Deprecated]
{:#events:itemdropped}

Triggers when the list item is dropped. 

N> Since this event is deprecated we suggest to use itemDrop event.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		itemDropped: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### itemDrop 
{:#events:itemdrop}

Triggers when the list item is dropped. 

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
{:.example}


{% highlight js%}

		$("#list").ejListBox({
		
		itemDrop: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### selected [Deprecated]
{:#events:selected}

Triggers when a list item gets selected.

N> Since this event is deprecated, we suggest to use select event.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		selected: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### select
{:#events:select}

Triggers when a list item gets selected. 

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		select: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### unselect
{:#events:unselect}

Triggers when a list item gets unselected. 

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}
		
		$("#list").ejListBox({
		
		unselect: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


### selectIndexChanged [Deprecated]
{:#events:selectindexchanged}

Triggers when the item selection is changed. 

N> Since this event is deprecated. We suggest to use change event.

<table>
<tr>
<th>
Event Arguments</th><th>
Type</th><th>
Description</th></tr>
<tr>
<td>
argument.model</td><td>
Object</td><td>
Instance of the listbox model object.</td></tr>
<tr>
<td>
argument.type</td><td>
String</td><td>
Name of the event.</td></tr>
<tr>
<td>
argument.item</td><td>
Object</td><td>
List item object.</td></tr>
<tr>
<td>
argument.data</td><td>
Object</td><td>
The Datasource of the listbox.</td></tr>
<tr>
<td>
argument.index</td><td>
Number</td><td>
List item’s index.</td></tr>
<tr>
<td>
argument.cancel</td><td>
Boolean</td><td>
Set this option to true to cancel the event.</td></tr>
<tr>
<td>
argument.isChecked</td><td>
Boolean</td><td>
Boolean value based on whether the list item is checked or not.</td></tr>
<tr>
<td>
argument.isSelected</td><td>
Boolean</td><td>
Boolean value based on whether the list item is selected or not.</td></tr>
<tr>
<td>
argument.isEnabled</td><td>
Boolean</td><td>
Boolean value based on the list item is enabled or not.</td></tr>
<tr>
<td>
argument.text</td><td>
String</td><td>
List item’s text (label).</td></tr>
<tr>
<td>
argument.value</td><td>
String</td><td>
List item’s value.</td></tr>
</table>

 Example
 {:.example}

{% highlight js%}

		$("#list").ejListBox({
		
		selectIndexChanged: function(args) { 
		
		//do something
		
		}          
		
		});

{% endhighlight %}


