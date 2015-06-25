---
layout: post
title: ejListBox
documentation: API
platform: js
metaname: 
metacontent: 
---

The Listbox control provides a list options to make user to choose an item from the list. It is capable of including other html elements such as images, textboxes, check box, radio buttons and so on.





$(element).ejListBox<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     &lt;/script&gt; </code></pre><pre class="prettyprint"><code>// Another way to render ListBox control, using its targetID.        &lt;ul id="listboxsample"&gt;   &lt;/ul&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;   &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#listboxsample').ejListBox({targetID: "carlist"});   &lt;/script&gt; </code></pre>



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




### allowDragAndDrop<span class="type-signature type boolean">boolean</span>




To enable the drag and drop nodes.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the with the allowDragAndDrop value specified.$('#carsList').ejListBox({allowDragAndDrop: true});     &lt;/script&gt; </code></pre>



### allowGrouping<span class="type-signature type boolean">boolean</span>




Specifies the grouping option in ListBox.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="select1"&gt;    &lt;/ul&gt;&lt;script&gt;            var skillset = [          { skill: "Bahrain", category: "B" }, { skill: "Brazil", category: "B" }, { skill: "Argentina", category: "A" },       { skill: "Bangladesh", category: "B" }, { skill: "Burma", category: "B" }, { skill: "Afghanistan", category: "A" }, { skill: "Antigua and Barbuda", category: "A" },       { skill: "Barbados", category: "B" }, { skill: "Botswana", category: "B" }, { skill: "Albania", category: "A" }, { skill: "Andorra", category: "A" },       { skill: "Belarus", category: "B" }, { skill: "Bolivia", category: "B" }, { skill: "Algeria", category: "A" }, { skill: "Angola", category: "A" }       ];// Initialize the ListBox with the allowGrouping value specified.          $("#select1").ejListBox({       dataSource: skillset,         fields: { text: "skill", category: "category" },allowGrouping:true             });&lt;/script&gt; </code></pre>



### allowMultiSelection<span class="type-signature type boolean">boolean</span>




To allow multiple selection of list items


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the allowMultiSelection with the value specified.$('#carsList').ejListBox({allowMultiSelection: true});  &lt;/script&gt; </code></pre>



### cascadeTo<span class="type-signature type string">string</span>




cascadeTo is used in cascading ListBox scenario, to map the child ListBox list widget in the parent ListBox list widget. By selecting an option in the parent ListBox, the child ListBox has to load the corresponding value regarding the parent ListBox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> &lt;div style="float: left;"&gt;      &lt;span class="txt"&gt;Select Group&lt;/span&gt;  &lt;ul id="groupsList" /&gt; &lt;/ul&gt;&lt;/div&gt;&lt;div style="float: right;"&gt;       &lt;span class="txt"&gt;Select Country&lt;/span&gt;       &lt;ul id="countryList" /&gt; &lt;/ul&gt;&lt;/div&gt;&lt;script&gt; var groups = [         { parentId: 'a', text: "Group A" },         { parentId: 'b', text: "Group B" },         { parentId: 'c', text: "Group C" },         { parentId: 'd', text: "Group D" },         { parentId: 'e', text: "Group E" }]           //first level child           var countries = [{ value: 11, parentId: 'a', text: "Algeria", sprite: "flag-dz" },          { value: 12, parentId: 'a', text: "Armenia", sprite: "flag-am" },          { value: 13, parentId: 'a', text: "Bangladesh", sprite: "flag-bd" },          { value: 14, parentId: 'a', text: "Cuba", sprite: "flag-cu" },          { value: 15, parentId: 'b', text: "Denmark", sprite: "flag-dk" },          { value: 16, parentId: 'b', text: "Egypt", sprite: "flag-eg" },          { value: 17, parentId: 'c', text: "Finland", sprite: "flag-fi" },          { value: 18, parentId: 'c', text: "India", sprite: "flag-in" },          { value: 19, parentId: 'c', text: "Malaysia", sprite: "flag-my" },          { value: 20, parentId: 'd', text: "New Zealand", sprite: "flag-nz" },          { value: 21, parentId: 'd', text: "Norway", sprite: "flag-no" },          { value: 22, parentId: 'd', text: "Poland", sprite: "flag-pl" },          { value: 23, parentId: 'e', text: "Romania", sprite: "flag-ro" },          { value: 24, parentId: 'e', text: "Singapore", sprite: "flag-sg" },          { value: 25, parentId: 'e', text: "Thailand", sprite: "flag-th" },          { value: 26, parentId: 'e', text: "Ukraine", sprite: "flag-ua" }]// To set cascadeTo API value during initialization  .            $('#groupsList').ejListBox({               dataSource: groups,               fields: { value: "parentId" },               cascadeTo: 'countryList'           });           $('#countryList').ejListBox({               dataSource: countries,               enabled:false           });&lt;/script&gt;</code></pre>



### checkAll<span class="type-signature type boolean">boolean</span>




Specifies to select all the items of ListBox can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the checkAll value specified.$('#carsList').ejListBox({showCheckbox: true, checkAll: true  });       &lt;/script&gt; </code></pre>



### checkedItemlist<span class="type-signature type integerarray">integerarray</span>




Specifies the checkedItemlist for ListBox.


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To sets the checked item  API value during initialization  .         $('#carsList').ejListBox({ showCheckbox:true,checkedItemlist  : [1,2] });       &lt;/script&gt; </code></pre>



### checkItemsByIndex<span class="type-signature type string">string</span>




Specifies the index value to check the items in the listbox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set checkItemsByIndex API value during initialization  .$('#carsList').ejListBox("disable");    $('#carsList').ejListBox({checkItemsByIndex  : "2,3"});         &lt;/script&gt; </code></pre>



### cssClass<span class="type-signature type string">string</span>




Sets the root class for ListBox theme. This cssClass API helps to use custom skinning option for ListBox control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* "gradient-lime"




Example
{:.example}
<pre class="prettyprint"><code>  &lt;div id="carsList"&gt;   &lt;ul&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;   &lt;/ul&gt; &lt;/div&gt;
&lt;script&gt;//Initialize the ListBox with the cssClass value specified        $("#carsList").ejListBox({ targetID: "carsList",cssClass: 'gradient-lime'});&lt;/script&gt;</code></pre>



### dataSource<span class="type-signature type data">data</span>




Specifies the data source of the ListBox. The data source contains the list of data for generating the List items.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  &lt;ul id="countrylist"&gt;  &lt;/ul&gt;&lt;script&gt;          //To set dataSource API value during initialization          $("#countrylist").ejListBox({ dataSource: window.countries });                   &lt;/script&gt;</code></pre>



### disableItemsByIndex<span class="type-signature type string">string</span>




Specifies the index value to disable the items in the listbox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set disableItemsByIndex API value during initialization  .$('#carsList').ejListBox({disableItemsByIndex  : "2,3"});&lt;/script&gt; </code></pre>



### enabled<span class="type-signature type boolean">boolean</span>




When this property sets to false, it disables the ListBox control.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the enabled  value specified.$('#carsList').ejListBox({enabled : false  });  &lt;/script&gt; </code></pre>



### enableItemsByIndex<span class="type-signature type string">string</span>




Specifies the index value to enable the items in the listbox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set enableItemsByIndex API value during initialization  .$('#carsList').ejListBox("disable");    $('#carsList').ejListBox({enableItemsByIndex  : "2,3"});        &lt;/script&gt; </code></pre>



### enableLoadOnDemand<span class="type-signature type boolean">boolean</span>




Specifies to enable Load data items onDemand for the ListBox.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>  &lt;ul id="countrylist"&gt;  &lt;/ul&gt;&lt;script&gt;          //To set fields API value during initialization          $("#countrylist").ejListBox({ dataSource: window.countriesField, enableLoadOnDemand:true,  fields: { text: "name", value: "key" }});&lt;/script&gt;</code></pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>




Save current model value to browser cookies for state maintains. While refresh the ListBox control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the enablePersistence  value specified.$('#carsList').ejListBox({enablePersistence : false});  &lt;/script&gt;</code></pre>



### enableRTL<span class="type-signature type boolean">boolean</span>




Sets the ListBox textbox direction as right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the enableRTL  value specified.$('#carsList').ejListBox({enableRTL : true  });         &lt;/script&gt; </code></pre>



### enableTooltip<span class="type-signature type boolean">boolean</span>




Sets to enable tooltip text for ListBox.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the enableRTL  value specified.$('#carsList').ejListBox({enableTooltip : true  });     &lt;/script&gt; </code></pre>



### enableVirtualScrolling<span class="type-signature type boolean">boolean</span>




Specifies to enable virtual scrolling behavior along with Load data items onDemand for the ListBox.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>  &lt;ul id="countrylist"&gt;  &lt;/ul&gt;&lt;script&gt;          //To set fields API value during initialization          $("#countrylist").ejListBox({ dataSource: window.countriesField, enableLoadOnDemand:true,enableVirtualScrolling:true,  fields: { text: "name", value: "key" }});&lt;/script&gt;</code></pre>



### fields<span class="type-signature type object">object</span>




Specifies mapping fields for the data items of the ListBox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  &lt;ul id="countrylist"&gt;  &lt;/ul&gt;&lt;script&gt;          //To set fields API value during initialization          $("#countrylist").ejListBox({ dataSource: window.countriesField,   fields: { text: "name", value: "key" }});&lt;/script&gt;</code></pre>



### fields.category<span class="type-signature type string">String</span>




Defines the category for data item.






### fields.htmlAttributes<span class="type-signature type object">Object</span>




Defines the html attributes such as id, class, styles for the item.






### fields.id<span class="type-signature type string">String</span>




Defines id for the tag.






### fields.imageAttributes<span class="type-signature type string">String</span>




Defines the image attributes such as height, width, styles and so on.






### fields.imageUrl<span class="type-signature type string">String</span>




Defines the imageURL for the image location.






### fields.selected<span class="type-signature type string">String</span>




Defines the tag value to be selected initially






### fields.spriteCssClass<span class="type-signature type string">String</span>




Defines the sprite css for the image tag.






### fields.tableName<span class="type-signature type string">String</span>




Defines the table name for tag value or display text while render with remote data.






### fields.text<span class="type-signature type string">String</span>




Defines the text content for the tag.






### fields.toolTipText<span class="type-signature type object">Object</span>




Defines the tooltip text to be displayed for the data list item.






### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>




Defines the height of the ListBox.


Default Value:
{:.param}



* Null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//Initialize the ListBox height property with the  value specified$('#carsList').ejListBox({ height: "300"});     &lt;/script&gt; </code></pre>



### query<span class="type-signature type object">object</span>




Specifies the query to retrieve the data from online server.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  &lt;ul id="customerlist"&gt;  &lt;/ul&gt;&lt;script&gt;          //To set query API value during initialization  var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});var queryString = ej.Query().from("Suppliers").select("Customers");        $("#customerlist").ejListBox({ dataSource: dataManger, query: queryString, fields: { text: "CustomerID" }});&lt;/script&gt;</code></pre>



### selectedItemIndex<span class="type-signature type number">number</span>




Specifies the selectedItemIndex for ListBox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set selectedItemIndex   API value during initialization  .        $('#carsList').ejListBox({selectedItemIndex  : 2});     &lt;/script&gt; </code></pre>



### selectedItemlist<span class="type-signature type integerarray">integerarray</span>




Specifies the selectedItems for ListBox.


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set selectedItemlist   API value during initialization  .         $('#carsList').ejListBox({ allowMultiSelection:true,selectedItemlist  : [1,2] });       &lt;/script&gt; </code></pre>



### selectedItems<span class="type-signature type integerarray">integerarray</span>




Specifies the items to be an selected in listbox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set selectedItems API value during initialization  .$('#carsList').ejListBox({showCheckbox: true, selectedItems : [1,2]});&lt;/script&gt; </code></pre>



### showCheckbox<span class="type-signature type boolean">boolean</span>




Specifies the multi selection option in ListBox with the help of checkbox control. For this we have to set showCheckbox option true.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the showCheckbox value specified.$('#carsList').ejListBox({showCheckbox: true });        &lt;/script&gt; </code></pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>




ListBox textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the showRoundedCorner value specified.$('#carsList').ejListBox({ showRoundedCorner: true });  &lt;/script&gt; </code></pre>



### template<span class="type-signature type string">string</span>




Specifies the template for ListBox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> 
 &lt;ul id="carsList" /&gt; &lt;/ul&gt; 
 &lt;script&gt;          // To set template API value during initialization  .   $("#carsList").ejListBox({ dataSource: window.carsListempList, template: '&lt;img class="eimg" src="styles/images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/&gt;' +  '&lt;div class="ename"&gt; ${text} &lt;/div&gt;&lt;div class="desig"&gt; ${desig} &lt;/div&gt;&lt;div class="cont"&gt; ${country} &lt;/div&gt;'});&lt;/script&gt;</code></pre>



### unCheckAll<span class="type-signature type boolean">boolean</span>




Specifies to uncheck all the items of ListBox can be done with the help of this unCheckAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Initialize the ListBox with the uncheckAll value specified.$('#carsList').ejListBox({showCheckbox: true,  uncheckAll: true  });    &lt;/script&gt; </code></pre>



### uncheckItemsByIndex<span class="type-signature type string">string</span>




Specifies the index value to uncheck the items in the listbox.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// To set uncheckItemsByIndex API value during initialization  .$('#carsList').ejListBox({uncheckItemsByIndex  : "2,3"});&lt;/script&gt; </code></pre>



### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>




Defines the width of the ListBox.


Default Value:
{:.param}



* Null




Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//Initialize the ListBox width property with the  value specified$('#carsList').ejListBox({ width: "220"});      &lt;/script&gt; </code></pre>


## Methods




### addItem<span class="signature">()</span>




To add an list item in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.addItem("Java"); // add an new item in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("addItem","Java");     &lt;/script&gt;</code></pre>



### checkAll<span class="signature">()</span>




To check all the list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.checkAll(); // checks all the list items in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  $('#carsList').ejListBox("checkAll");   &lt;/script&gt;</code></pre>



### checkItemByIndex<span class="signature">()</span>




To check a list items through index in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.checkItemsByIndex(2,3); // checks the specified items the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox       $('#carsList').ejListBox("checkItemByIndex","2,3");     &lt;/script&gt;</code></pre>



### checkitems<span class="signature">()</span>




To check items in the checkitemslist in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.checkitems(); // checks all the list items in the checkedItemlist&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  $('#carsList').ejListBox("checkitems");         &lt;/script&gt;</code></pre>



### disable<span class="signature">()</span>




To disable the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.disable(); // disable the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();$('#carsList').ejListBox("disable");    &lt;/script&gt;</code></pre>



### disableItem<span class="signature">()</span>




To disable an list item in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.disableItem(); // disable selected item in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("disableItem");        &lt;/script&gt;</code></pre>



### disableItemByIndex<span class="signature">()</span>




To disable an Item or set of Items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.disableItemByIndex("3,5,7");&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("disableItemsByIndex" ,"3,5,7");&lt;/script&gt;</code></pre>



### enable<span class="signature">()</span>




To enable the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.enable(); // enable the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();$('#carsList').ejListBox("enable");     &lt;/script&gt;</code></pre>



### enableItemByIndex<span class="signature">()</span>




To enable a single Item or set of Items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.enableItemByIndex("3,5");&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("enableItemsByIndex" ,"3,5");&lt;/script&gt;</code></pre>



### getCheckedItems<span class="signature">()</span>




To get the list of checked list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.getCheckedItems(); // get the list of checked items the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("getCheckedItems");    &lt;/script&gt;</code></pre>



### getSelectedItem<span class="signature">()</span>




To get the selected list item in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.getSelectedItem(); // gets the selected item from the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("getSelectedItem");    &lt;/script&gt;</code></pre>



### getSelectedItems<span class="signature">()</span>




To get the list of selected list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.getSelectedItems(); // gets the list of selected list items from the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("getSelectedItems");   &lt;/script&gt;</code></pre>



### moveDown<span class="signature">()</span>




To move the selected list item one step Down in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.moveDown(); //moves down the selected item in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("moveDown");   &lt;/script&gt;</code></pre>



### moveUp<span class="signature">()</span>




To move the selected list item one step Up in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.moveUp(); // moves up selected item in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("moveUp");     &lt;/script&gt;</code></pre>



### removeItem<span class="signature">()</span>




To remove an list item in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.removeItem(); // removes the selected item from the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("removeItem");         &lt;/script&gt;</code></pre>



### selectAll<span class="signature">()</span>




To select all the list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.selectAll(); // selects all the list items in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("selectAll");  &lt;/script&gt;</code></pre>



### selectItemByIndex<span class="signature">()</span>




To select an Item using its index in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.selectItemByIndex(2); //selects the item in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("selectItemByIndex" ,"2");     &lt;/script&gt;</code></pre>



### selectItemsByIndex<span class="signature">()</span>




To select a list items through index in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.selectItemsByIndex(2,3); // selects the specified items the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("selectItemsByIndex","2,3");   &lt;/script&gt;</code></pre>



### unCheckAll<span class="signature">()</span>




To uncheck all the list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.unCheckAll(); // Unchecks all the list items in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox({showCheckbox:true});  $('#carsList').ejListBox("unCheckAll");         &lt;/script&gt;</code></pre>



### uncheckItemByIndex<span class="signature">()</span>




To uncheck set of list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.uncheckItemsByIndex(2,3); // uncheckItems specified the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox("uncheckItemByIndex","2,3");   &lt;/script&gt;</code></pre>



### unSelectAll<span class="signature">()</span>




To unselect all the list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.unSelectAll(); // unselect all the items in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("unSelectAll");        &lt;/script&gt;</code></pre>



### unselectItemByIndex<span class="signature">()</span>




To unselect a list item in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.unselectItemByIndex(2); // unselects the list item specified in the index  in the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("unselectItemByIndex","2");    &lt;/script&gt;</code></pre>



### unselectItemsByIndex<span class="signature">()</span>




To unselect set of list items in the ListBox



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     var ListBoxObj  = $("#carsList").data("ejListBox");ListBoxObj.unselectItemsByIndex(2,3); // unselectItems specified the ListBox&lt;/script&gt;</code></pre><pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;// Create ListBox$('#carsList').ejListBox();     $('#carsList').ejListBox("unselectItemsByIndex","2,3");         &lt;/script&gt;</code></pre>


## Events




### checkChange




Fires when check state of an list item changed successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//checkChange event for ListBox$('#carsList').ejListBox({      showCheckbox:true,checkChange: function(args) {}});     &lt;/script&gt;            </code></pre>



### create




Fires when create successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//create event for ListBox$('#carsList').ejListBox({      create: function(args) {}});    &lt;/script&gt;            </code></pre>



### destroy




Fires when destroy successfully.



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//destroy event for ListBox$('#carsList').ejListBox({      destroy: function(args) {}});   &lt;/script&gt;           </code></pre>



### destroy




Fires when the listbox data items loaded successfully.



Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//actionComplete event for ListBox$('#carsList').ejListBox({      destroy: function(args) {}});   &lt;/script&gt;           </code></pre>



### itemDrag




Fires when list item is being dragged successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//itemDrag event for ListBox$('#carsList').ejListBox({      itemDrag: function(args) {}});  &lt;/script&gt;            </code></pre>



### itemDragStart




Fires when list item started to drag successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//itemDragStart event for ListBox$('#carsList').ejListBox({      itemDragStart: function(args) {}});     &lt;/script&gt;            </code></pre>



### itemDragStop




Fires when list item stopped dragging successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//itemDragStop event for ListBox$('#carsList').ejListBox({      itemDragStop: function(args) {}});      &lt;/script&gt;            </code></pre>



### itemDropped




Fires when list item stopped dropping successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//itemDropped event for ListBox$('#carsList').ejListBox({      itemDropped: function(args) {}});       &lt;/script&gt;            </code></pre>



### selected




Fires when list item gets selected successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//selected event for ListBox$('#carsList').ejListBox({      selected: function(args) {}});  &lt;/script&gt;            </code></pre>



### selectIndexChanged




Fires when selected list item Index Changed successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument.model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the ListBox model</td></tr><tr><td class="name"><code>argument.type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>    &lt;ul id="carsList"&gt;      &lt;li&gt;Audi A4&lt;/li&gt;      &lt;li&gt;Audi A5&lt;/li&gt;      &lt;li&gt;Audi A6&lt;/li&gt;      &lt;li&gt;Audi A7&lt;/li&gt;      &lt;li&gt;Audi A8&lt;/li&gt;           &lt;li&gt;BMW 501&lt;/li&gt;      &lt;li&gt;BMW 502&lt;/li&gt;      &lt;li&gt;BMW 503&lt;/li&gt;      &lt;li&gt;BMW 507&lt;/li&gt;      &lt;li&gt;BMW 3200&lt;/li&gt;   &lt;/ul&gt;&lt;script&gt;//selectIndexChanged event for ListBox$('#carsList').ejListBox({      selectIndexChanged: function(args) {}});        &lt;/script&gt;            </code></pre>


