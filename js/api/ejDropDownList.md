---
layout: post
title: ejDropDownList
documentation: API
platform: js
metaname: 
metacontent: 
---

The DropDownList control provides a list options to make user to choose an item from the list. It is capable of including other html elements such as images, textboxes, check box, radio buttons and so on.





$(element).ejDropDownList<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList"});    
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>// Another way to render DropDownList control.
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;ComputerIT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();  
&lt;/script&gt; </code>
</pre>



Requires
{:.require}


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.dropdownlist.js

* module:ej.checkbox.js

* module:ej.scroller.js


## Members




### allowGrouping<span class="type-signature type boolean">boolean</span>
{:#allowGrouping}




Groups the search result based on the category value.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;
// Initialize the DropDownList with the grouping value specified.
$("#drpdwn").ejDropDownList({ dataSource: window.countriesField, fields: { text: "name", value: "key" }, allowGrouping: true});
&lt;/script&gt;</code>
</pre>



### allowMultiSelection<span class="type-signature type boolean">boolean</span>
{:#allowMultiSelection}




Indicates that the multiSelectMode values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
&lt;script&gt;
// Initialize the allowMultiSelection with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showCheckbox: true,allowMultiSelection: true });
&lt;/script&gt;</code>
</pre>



### cascadeTo<span class="type-signature type string">string</span>
{:#cascadeTo}




cascadeTois used in cascading Dropdown list scenario, to map the child Dropdown list widget in the parent Dropdown list widget. By selecting an option in the parent dropdown, the child DropDownList has to load the corresponding value regarding the parent Dropdown.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div style="float: left;"&gt;
      &lt;span class="txt"&gt;Select Group&lt;/span&gt;
      &lt;input id="groupsList" type="text" /&gt;
&lt;/div&gt;

&lt;div style="float: right;"&gt;
       &lt;span class="txt"&gt;Select Country&lt;/span&gt;
       &lt;input id="countryList" type="text"/&gt;
&lt;/div&gt;
&lt;script&gt;
 var groups = [
         { parentId: 'a', text: "Group A" },
         { parentId: 'b', text: "Group B" },
         { parentId: 'c', text: "Group C" },
         { parentId: 'd', text: "Group D" },
         { parentId: 'e', text: "Group E" }]
           //first level child
           var countries = [{ value: 11, parentId: 'a', text: "Algeria", sprite: "flag-dz" },
          { value: 12, parentId: 'a', text: "Armenia", sprite: "flag-am" },
          { value: 13, parentId: 'a', text: "Bangladesh", sprite: "flag-bd" },
          { value: 14, parentId: 'a', text: "Cuba", sprite: "flag-cu" },
          { value: 15, parentId: 'b', text: "Denmark", sprite: "flag-dk" },
          { value: 16, parentId: 'b', text: "Egypt", sprite: "flag-eg" },
          { value: 17, parentId: 'c', text: "Finland", sprite: "flag-fi" },
          { value: 18, parentId: 'c', text: "India", sprite: "flag-in" },
          { value: 19, parentId: 'c', text: "Malaysia", sprite: "flag-my" },
          { value: 20, parentId: 'd', text: "New Zealand", sprite: "flag-nz" },
          { value: 21, parentId: 'd', text: "Norway", sprite: "flag-no" },
          { value: 22, parentId: 'd', text: "Poland", sprite: "flag-pl" },
          { value: 23, parentId: 'e', text: "Romania", sprite: "flag-ro" },
          { value: 24, parentId: 'e', text: "Singapore", sprite: "flag-sg" },
          { value: 25, parentId: 'e', text: "Thailand", sprite: "flag-th" },
          { value: 26, parentId: 'e', text: "Ukraine", sprite: "flag-ua" }]
// To set cascadeTo API value during initialization  . 
           $('#groupsList').ejDropDownList({
               dataSource: groups,
               fields: { value: "parentId" },
               cascadeTo: 'countryList'
           });
           $('#countryList').ejDropDownList({
               dataSource: countries,
               enabled:false
           });
&lt;/script&gt;</code>
</pre>



### caseSensitiveSearch<span class="type-signature type boolean">boolean</span>
{:#caseSensitiveSearch}




Sets the case sensitivity of the search operation..


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the caseSensitiveSearch value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",caseSensitiveSearch: true });
&lt;/script&gt;</code>
</pre>



### checkAll<span class="type-signature type boolean">boolean</span>
{:#checkAll}




Specifies to select all the items of DropDownList can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the checkAll value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true, checkAll: true });
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#cssClass}




Sets the root class for DropDownList theme. This cssClass API helps to use custom skinning option for DropDownList control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* "gradient-lime"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
&lt;script&gt;
//Initialize the DropDownList with the cssClass value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",cssClass: 'flat-azure'});
&lt;/script&gt;</code>
</pre>



### dataSource<span class="type-signature type data">data</span>
{:#dataSource}




Specifies the data source of the DropDownList. The data source contains the list of data for generating the DropDownList items.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;          
//To set dataSource API value during initialization  
        $("#drpdwn").ejDropDownList({ dataSource: window.countries });                   
&lt;/script&gt;</code>
</pre>



### delimiterChar<span class="type-signature type string">string</span>
{:#delimiterChar}




Sets the separator to allow multiple word searches.if we enter the delimiter value, the texts after the delimiter are considered as a separate word or query. The delimiter string should have a single character and must be a symbol. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.


Default Value:
{:.param}



* ','




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;          
//To set dataSource API value during initialization  
        $("#drpdwn").ejDropDownList({ delimiterChar:";" });                      
&lt;/script&gt;</code>
</pre>



### disableItemsByIndex<span class="type-signature type string">string</span>
{:#disableItemsByIndex}




Specifies the disableItemsByIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set disableItemsByIndex   API value during initialization  .      
        $("#drpdwn").ejDropDownList({  targetID: "carsList",disableItemsByIndex  : "2,4" });
&lt;/script&gt;</code>
</pre>



### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#enableAnimation}




The enableAnimation property is used to set the milliseconds time between suggestion popup open and close.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
&lt;script&gt;
// Initialize the enableAnimation with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList", enableAnimation: true });
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#enabled}




When this property sets to false, it disables the DropDownList control.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the enabled  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enabled : false });
&lt;/script&gt;</code>
</pre>



### enableIncrementalSearch<span class="type-signature type boolean">boolean</span>
{:#enableIncrementalSearch}




Specifies to perform incremental search for selection of items from DropDownList can be done with the help of this property, this will helpful in selecting the item using the typed character.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the enableIncrementalSearch with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",enableIncrementalSearch: true });
&lt;/script&gt;</code>
</pre>



### enableItemsByIndex<span class="type-signature type string">string</span>
{:#enableItemsByIndex}




Specifies the enableItemsByIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set enableItemsByIndex   API value during initialization  .       
        $("#drpdwn").ejDropDownList({  targetID: "carsList",enableItemsByIndex  : "2,4" });
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#enablePersistence}




Save current model value to browser cookies for state maintains. While refresh the DropDownList control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the enablePersistence  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enablePersistence : false });
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#enableRTL}




Sets the DropDownList textbox direction as right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the enableRTL  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enableRTL : true });
&lt;/script&gt;</code>
</pre>



### fields<span class="type-signature type object">object</span>
{:#fields}




Specifies mapping fields for the data items of the DropDownList textbox.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;          
//To set fields API value during initialization  
        $("#drpdwn").ejDropDownList({ dataSource: window.countriesField,   fields: { text: "name", value: "key" }});
&lt;/script&gt;</code>
</pre>



### fields.category<span class="type-signature type string">String</span>
{:#fields-category}




Used to categorize the items. It is used when the grouping is enabled.






### fields.htmlAttributes<span class="type-signature type object">Object</span>
{:#fields-htmlAttributes}




Defines the html attributes such as id, class, styles for the item.






### fields.id<span class="type-signature type string">String</span>
{:#fields-id}




Defines id for the tag.






### fields.imageAttributes<span class="type-signature type string">String</span>
{:#fields-imageAttributes}




Defines the image attributes such as height, width, styles and so on.






### fields.imageUrl<span class="type-signature type string">String</span>
{:#fields-imageUrl}




Defines the imageURL for the image location.






### fields.selected<span class="type-signature type boolean">Boolean</span>
{:#fields-selected}




Defines the tag value to be selected initially






### fields.spriteCssClass<span class="type-signature type string">String</span>
{:#fields-spriteCssClass}




Defines the sprite css for the image tag.






### fields.tableName<span class="type-signature type string">String</span>
{:#fields-tableName}




Defines the table name for tag value or display text while render with remote data.






### fields.text<span class="type-signature type string">String</span>
{:#fields-text}




Defines the text content for the tag.






### fields.value<span class="type-signature type string">String</span>
{:#fields-value}




Defines the tag value or display text..






### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#height}




Defines the height of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//Initialize the DropDownList height property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",height: 30 });
&lt;/script&gt;</code>
</pre>



### itemsCount<span class="type-signature type number">number</span>
{:#itemsCount}




Specifies the itemsCount for DropDownList.


Default Value:
{:.param}



* 5




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set itemsCount   API value during initialization  .       
        $("#drpdwn").ejDropDownList({  targetID: "carsList",itemsCount  : 2 });
&lt;/script&gt;</code>
</pre>



### popupHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#popupHeight}




Defines the popupHeight of the suggestion box.


Default Value:
{:.param}



* "152px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//Initialize the DropDownList popupHeight property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",popupHeight: '152px' });
&lt;/script&gt;</code>
</pre>



### popupWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#popupWidth}




Defines the popupWidth of the suggestion box.


Default Value:
{:.param}



* "auto"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//Initialize the DropDownList popupWidth property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",popupWidth: '152px' });
&lt;/script&gt;</code>
</pre>



### query<span class="type-signature type object">object</span>
{:#query}




Specifies the query to retrieve the data from online server.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;          
//To set query API value during initialization  
var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});
var queryString = ej.Query().from("Suppliers").select("ContactName");
        $("#drpdwn").ejDropDownList({ dataSource: dataManger, query: queryString, fields: { text: "ContactName" }});
&lt;/script&gt;</code>
</pre>



### readOnly<span class="type-signature type boolean">boolean</span>
{:#readOnly}




Indicates that the DropDownList textbox values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the readOnly value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",readOnly: true });
&lt;/script&gt;</code>
</pre>



### selectedItemIndex<span class="type-signature type number">number</span>
{:#selectedItemIndex}




Specifies the selectedItemIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set selectedItemIndex   API value during initialization  .        
        $("#drpdwn").ejDropDownList({  targetID: "carsList",selectedItemIndex  : 2 });
&lt;/script&gt;</code>
</pre>



### selectedItems<span class="type-signature type integerarray">integerarray</span>
{:#selectedItems}




Specifies the selectedItems for DropDownList.


Default Value:
{:.param}



* []




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set selectedItems   API value during initialization  .    
        $("#drpdwn").ejDropDownList({  targetID: "carsList",showCheckbox: true, selectedItems  : [1,2] });
&lt;/script&gt;</code>
</pre>



### showCheckbox<span class="type-signature type boolean">boolean</span>
{:#showCheckbox}




Specifies the multi selection option in DropDownList with the help of checkbox control. For this we have to enable it by showCheckbox option true.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the showCheckbox value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true });
&lt;/script&gt;</code>
</pre>



### showPopupOnLoad<span class="type-signature type boolean">boolean</span>
{:#showPopupOnLoad}




DropDownList textbox to be displayed with Popup shown.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;                      
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the showPopupOnLoad value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showPopupOnLoad: true });
&lt;/script&gt;</code>
</pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#showRoundedCorner}




DropDownList textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the showRoundedCorner value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showRoundedCorner: true });
&lt;/script&gt;</code>
</pre>



### targetID<span class="type-signature type string">string</span>
{:#targetID}




Specifies the targetID for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// To set targetID API value during initialization  .   
        $("#drpdwn").ejDropDownList({ targetID: "carsList" });
&lt;/script&gt;</code>
</pre>



### template<span class="type-signature type string">string</span>
{:#template}




Specifies the template for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
 
&lt;input type="text" id="drpdwn" /&gt; 
 
&lt;script&gt;          
// To set template API value during initialization  .   
$("#drpdwn").ejDropDownList({ dataSource: window.drpdwnempList, template: '&lt;img class="eimg" src="styles/images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +
  '&lt;div class="ename"&gt; ${text} &lt;/div&gt;&lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;',width: "200px"});
&lt;/script&gt;</code>
</pre>



### text<span class="type-signature type string">string</span>
{:#text}




Defines the default text value to be display in the DropDownList textbox.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
//Initialize the DropDownList text property with the  value specified
  $("#drpdwn").ejDropDownList({ targetID: "carsList",text:"Audi A7" });
&lt;/script&gt;</code>
</pre>



### uncheckAll<span class="type-signature type boolean">boolean</span>
{:#uncheckAll}




Specifies to unselect all the items of DropDownList can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
// Initialize the DropDownList with the uncheckAll value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true, uncheckAll: true });
&lt;/script&gt;</code>
</pre>



### validationMessage<span class="type-signature type object">object</span>
{:#validationMessage}




Set the jquery validation error message in Dropdownlist.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" name="drpdwn" /&gt; 
 
&lt;script&gt;
//To set validationMessage API during initialization            
 $("#drpdwn").ejDropDownList({
  dataSource: window.countriesField, fields: { text: "name", value: "key" }, allowGrouping: true,                       
  validationRules:{                     
          required:true 
        },
  validationMessage:{
          required: "Required Dropdown value"
        }
});
&lt;/script&gt;</code>
</pre>



### validationRules<span class="type-signature type object">object</span>
{:#validationRules}




Set the jquery validation rules in Dropdownlist.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" name="drpdwn" /&gt; 
 
&lt;script&gt;
//To set validationRules API during initialization              
 $("#drpdwn").ejDropDownList({
  dataSource: window.countriesField, fields: { text: "name", value: "key" }, allowGrouping: true,                       
  validationRules:{                     
          required:true
        }
});
&lt;/script&gt;</code>
</pre>



### value<span class="type-signature type string">string</span>
{:#value}




Defines the value eqivalent text to be display in the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
//Initialize the DropDownList value property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",value:"Audi A7" });
&lt;/script&gt;</code>
</pre>



### watermarkText<span class="type-signature type string">string</span>
{:#watermarkText}




Sets the watermark text. When the textbox is empty the watermark text is visible like a shaded text.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//Initialize the DropDownList with the watermarkText value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",watermarkText: 'Enter text' });
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#width}




Defines the width of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//Initialize the DropDownList width property with the width value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",width: 250 });
&lt;/script&gt;</code>
</pre>


## Methods




### addItem<span class="signature">()</span>
{:#addItem}




Add the item into the DropDownList.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("addItem",{value:"value",image:{src:"Pictures/xhtml.png",alt:"images",width:"200px",height:"500px"},htmlAttributes:"style=color:red"});     
&lt;/script&gt;</code>
</pre>



### checkAll<span class="signature">()</span>
{:#checkAll}




This method is used to set all the items to checked.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.checkAll(); // checkAll values the DropDownList
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
$('#drpdwn').ejDropDownList("checkAll");        
&lt;/script&gt;</code>
</pre>



### clearText<span class="signature">()</span>
{:#clearText}




Clears the text in the DropDownList textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.clearText(); // clear the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("clearText");       
&lt;/script&gt;</code>
</pre>



### destroy<span class="signature">()</span>
{:#destroy}




destroys the DropDownList widget.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.destroy(); // hide the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("destroy");         
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#disable}




To disable the DropDownList



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.disable(); // disable the DropDownList
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("disable");         
&lt;/script&gt;</code>
</pre>



### disableItemByIndex<span class="signature">()</span>
{:#disableItemByIndex}




To disable an Item or set of Items in the DropDownList



Example
{:.example}

<pre class="prettyprint">
<code> 
   &lt;ul id="carsList"&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
           &lt;li&gt;BMW 501&lt;/li&gt;
      &lt;li&gt;BMW 502&lt;/li&gt;
      &lt;li&gt;BMW 503&lt;/li&gt;
      &lt;li&gt;BMW 507&lt;/li&gt;
      &lt;li&gt;BMW 3200&lt;/li&gt;
   &lt;/ul&gt;
&lt;script&gt;
// Create DropDownList
$('#carsList').ejDropDownList();        
var DropDownListObj  = $("#carsList").data("ejDropDownList");
DropDownListObj.disableItemByIndex("3,5,7");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;ul id="carsList"&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
           &lt;li&gt;BMW 501&lt;/li&gt;
      &lt;li&gt;BMW 502&lt;/li&gt;
      &lt;li&gt;BMW 503&lt;/li&gt;
      &lt;li&gt;BMW 507&lt;/li&gt;
      &lt;li&gt;BMW 3200&lt;/li&gt;
   &lt;/ul&gt;
&lt;script&gt;
// Create DropDownList
$('#carsList').ejDropDownList();        
$('#carsList').ejDropDownList("disableItemsByIndex" ,"3,5,7");  
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#enable}




To enable the DropDownList



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.enable(); // enable the DropDownList
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("enable");  
&lt;/script&gt;</code>
</pre>



### enableItemByIndex<span class="signature">()</span>
{:#enableItemByIndex}




To enable an Item or set of Items which are in disable in the DropDownList



Example
{:.example}

<pre class="prettyprint">
<code> 
   &lt;ul id="carsList"&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
           &lt;li&gt;BMW 501&lt;/li&gt;
      &lt;li&gt;BMW 502&lt;/li&gt;
      &lt;li&gt;BMW 503&lt;/li&gt;
      &lt;li&gt;BMW 507&lt;/li&gt;
      &lt;li&gt;BMW 3200&lt;/li&gt;
   &lt;/ul&gt;
&lt;script&gt;
// Create DropDownList
$('#carsList').ejDropDownList();        
var DropDownListObj  = $("#carsList").data("ejDropDownList");
DropDownListObj.enableItemByIndex("3,5,7");
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
   &lt;ul id="carsList"&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
           &lt;li&gt;BMW 501&lt;/li&gt;
      &lt;li&gt;BMW 502&lt;/li&gt;
      &lt;li&gt;BMW 503&lt;/li&gt;
      &lt;li&gt;BMW 507&lt;/li&gt;
      &lt;li&gt;BMW 3200&lt;/li&gt;
   &lt;/ul&gt;
&lt;script&gt;
// Create DropDownList
$('#carsList').ejDropDownList();        
$('#carsList').ejDropDownList("enableItemsByIndex" ,"3,5,7");   
&lt;/script&gt;</code>
</pre>



### getSelectedItem<span class="signature">()</span>
{:#getSelectedItem}




This method is used to get the selected items in DropDownList.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getSelectedItem(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
$('#drpdwn').ejDropDownList("getSelectedItem");         
&lt;/script&gt;</code>
</pre>



### getSelectedValue<span class="signature">()</span>
{:#getSelectedValue}




This method is used to get the selected items value in DropDownList.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({value:"Computer IT"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getSelectedValue(); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt; 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({value:"Computer IT"});
$('#drpdwn').ejDropDownList("getSelectedValue");
&lt;/script&gt;</code>
</pre>



### getValue<span class="signature">()</span>
{:#getValue}




Returns the current value selected in the DropDownList textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getValue(); // getValue of the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("getValue");        
&lt;/script&gt;</code>
</pre>



### hidePopup<span class="signature">()</span>
{:#hidePopup}




popup list hide in the DropDownList textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.hidePopup(); // hidePopup of the DropDownList 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("hidePopup");       
&lt;/script&gt;</code>
</pre>



### setSelectedText<span class="signature">()</span>
{:#setSelectedText}




This method is used to select a list item in DropDownList using given text field.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedText("Computer IT"); // setSelectedText for the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedText","Computer IT");   
&lt;/script&gt;</code>
</pre>



### setSelectedValue<span class="signature">()</span>
{:#setSelectedValue}




This method is used to select a list item in DropDownList using given value field.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");   
&lt;/script&gt;</code>
</pre>



### showPopup<span class="signature">()</span>
{:#showPopup}




popup list show in the DropDownList textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.showPopup(); // 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("showPopup");       
&lt;/script&gt;</code>
</pre>



### unCheckAll<span class="signature">()</span>
{:#unCheckAll}




This method is used to set all the items to uncheck.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.unCheckAll(); // UncheckAll values the DropDownList
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
$('#drpdwn').ejDropDownList("unCheckAll");      
&lt;/script&gt;</code>
</pre>



### unselectItemByIndex<span class="signature">()</span>
{:#unselectItemByIndex}




This method is used to unselect a list item in DropDownList using given index field.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("Art"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByIndex(0); // unselectItemByIndex for the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","Art");  // setSelectedValue for the DropDownList text   
$('#drpdwn').ejDropDownList("unselectItemByIndex",0); // unselectItemByIndex for the DropDownList text      
&lt;/script&gt;</code>
</pre>



### unselectItemByText<span class="signature">()</span>
{:#unselectItemByText}




This method is used to unselect a list item in DropDownList using given text field.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByText("Computer IT"); // unselectItemByText for the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");  // setSelectedValue for the DropDownList text    
$('#drpdwn').ejDropDownList("unselectItemByText","Computer IT");        
&lt;/script&gt;</code>
</pre>



### unselectItemByValue<span class="signature">()</span>
{:#unselectItemByValue}




This method is used to unselect a list item in DropDownList using given value field.



Example
{:.example}

<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
 
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByValue("ComputerIT"); // unselectItemByValue for the DropDownList text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
  &lt;select name="selectIndex" id="drpdwn"&gt;
       &lt;option value="Art"&gt;Art&lt;/option&gt;
       &lt;option value="Architecture"&gt;Architecture&lt;/option&gt;
       &lt;option value="Biographies"&gt;Biographies&lt;/option&gt;
       &lt;option value="Business"&gt;Business&lt;/option&gt;
       &lt;option value="ComputerIT"&gt;Computer IT&lt;/option&gt;
       &lt;option value="Comics"&gt;Comics&lt;/option&gt;
       &lt;option value="Cookery"&gt;Cookery&lt;/option&gt;
       &lt;option value="Environment"&gt;Environment&lt;/option&gt;
       &lt;option value="Fiction"&gt;Fiction&lt;/option&gt;
       &lt;option value="Health"&gt;Health&lt;/option&gt;
       &lt;option value="Humanities"&gt;Humanities&lt;/option&gt;
       &lt;option value="Language"&gt;Language&lt;/option&gt;
   &lt;/select&gt;
&lt;script&gt;
 
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");  // setSelectedValue for the DropDownList text    
$('#drpdwn').ejDropDownList("unselectItemByValue","ComputerIT");        
&lt;/script&gt;</code>
</pre>


## Events




### beforePopupHide
{:#beforePopupHide}




Fires beore the popup going to hide.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//beforePopupHide event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        beforePopupHide: function(args) {}
});
&lt;/script&gt;          </code>
</pre>



### beforePopupShown
{:#beforePopupShown}




Fires beore the popup going to display.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//beforePopupShown event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        beforePopupShown: function(args) {}
});
&lt;/script&gt;          </code>
</pre>



### change
{:#change}




Fires when change successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//change event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        change: function(args) {}
}); 
&lt;/script&gt;            </code>
</pre>



### checkChange
{:#checkChange}




Fires when checkChange successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//checkChange event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        checkChange: function(args) {}
}); 
&lt;/script&gt;           </code>
</pre>



### create
{:#create}




Fires when create successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//change event for DropDownList
$("#drpdwn").ejDropDownList({ 
   targetID: "carsList",
        create: function(args) {}
});
&lt;/script&gt;            </code>
</pre>



### destroy
{:#destroy}




Fires when destroy successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//destroy event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        destroy: function(args) {}
});
&lt;/script&gt;           </code>
</pre>



### popupHide
{:#popupHide}




Fires when popupHide successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//popupHide event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        popupHide: function(args) {}
});
&lt;/script&gt;           </code>
</pre>



### popupShown
{:#popupShown}




Fires when popupShown successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//popupShown event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        popupShown: function(args) {}
});
&lt;/script&gt;          </code>
</pre>



### select
{:#select}




Fires when select successfully.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="drpdwn" /&gt; 
 
 &lt;div id="carsList"&gt;
   &lt;ul&gt;
      &lt;li&gt;Audi A4&lt;/li&gt;
      &lt;li&gt;Audi A5&lt;/li&gt;
      &lt;li&gt;Audi A6&lt;/li&gt;
      &lt;li&gt;Audi A7&lt;/li&gt;
      &lt;li&gt;Audi A8&lt;/li&gt;
   &lt;/ul&gt;
 &lt;/div&gt;
 
&lt;script&gt;          
//select event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        select: function(args) {}
});      
&lt;/script&gt;</code>
</pre>


