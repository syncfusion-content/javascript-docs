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


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList"});    
</script> {% endhighlight %}


{% highlight html %}
// Another way to render DropDownList control.
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">ComputerIT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();  
</script> {% endhighlight %}




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
{:#members:allowgrouping}




Groups the search result based on the category value.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
<script>
// Initialize the DropDownList with the grouping value specified.
$("#drpdwn").ejDropDownList({ dataSource: window.countriesField, fields: { text: "name", value: "key" }, allowGrouping: true});
</script>{% endhighlight %}




### allowMultiSelection<span class="type-signature type boolean">boolean</span>
{:#members:allowmultiselection}




Indicates that the multiSelectMode values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
<script>
// Initialize the allowMultiSelection with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showCheckbox: true,allowMultiSelection: true });
</script>{% endhighlight %}




### cascadeTo<span class="type-signature type string">string</span>
{:#members:cascadeto}




cascadeTois used in cascading Dropdown list scenario, to map the child Dropdown list widget in the parent Dropdown list widget. By selecting an option in the parent dropdown, the child DropDownList has to load the corresponding value regarding the parent Dropdown.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div style="float: left;">
      <span class="txt">Select Group</span>
      <input id="groupsList" type="text" />
</div>

<div style="float: right;">
       <span class="txt">Select Country</span>
       <input id="countryList" type="text"/>
</div>
<script>
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
</script>{% endhighlight %}




### caseSensitiveSearch<span class="type-signature type boolean">boolean</span>
{:#members:casesensitivesearch}




Sets the case sensitivity of the search operation..


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the caseSensitiveSearch value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",caseSensitiveSearch: true });
</script>{% endhighlight %}




### checkAll<span class="type-signature type boolean">boolean</span>
{:#members:checkall}




Specifies to select all the items of DropDownList can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the checkAll value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true, checkAll: true });
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for DropDownList theme. This cssClass API helps to use custom skinning option for DropDownList control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* "gradient-lime"




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
<script>
//Initialize the DropDownList with the cssClass value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",cssClass: 'flat-azure'});
</script>{% endhighlight %}




### dataSource<span class="type-signature type data">data</span>
{:#members:datasource}




Specifies the data source of the DropDownList. The data source contains the list of data for generating the DropDownList items.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
<script>          
//To set dataSource API value during initialization  
        $("#drpdwn").ejDropDownList({ dataSource: window.countries });                   
</script>{% endhighlight %}




### delimiterChar<span class="type-signature type string">string</span>
{:#members:delimiterchar}




Sets the separator to allow multiple word searches.if we enter the delimiter value, the texts after the delimiter are considered as a separate word or query. The delimiter string should have a single character and must be a symbol. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.


Default Value:
{:.param}



* ','




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
<script>          
//To set dataSource API value during initialization  
        $("#drpdwn").ejDropDownList({ delimiterChar:";" });                      
</script>{% endhighlight %}




### disableItemsByIndex<span class="type-signature type string">string</span>
{:#members:disableitemsbyindex}




Specifies the disableItemsByIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set disableItemsByIndex   API value during initialization  .      
        $("#drpdwn").ejDropDownList({  targetID: "carsList",disableItemsByIndex  : "2,4" });
</script>{% endhighlight %}




### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}




The enableAnimation property is used to set the milliseconds time between suggestion popup open and close.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
<script>
// Initialize the enableAnimation with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList", enableAnimation: true });
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




When this property sets to false, it disables the DropDownList control.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the enabled  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enabled : false });
</script>{% endhighlight %}




### enableIncrementalSearch<span class="type-signature type boolean">boolean</span>
{:#members:enableincrementalsearch}




Specifies to perform incremental search for selection of items from DropDownList can be done with the help of this property, this will helpful in selecting the item using the typed character.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the enableIncrementalSearch with the value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",enableIncrementalSearch: true });
</script>{% endhighlight %}




### enableItemsByIndex<span class="type-signature type string">string</span>
{:#members:enableitemsbyindex}




Specifies the enableItemsByIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set enableItemsByIndex   API value during initialization  .       
        $("#drpdwn").ejDropDownList({  targetID: "carsList",enableItemsByIndex  : "2,4" });
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintains. While refresh the DropDownList control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the enablePersistence  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enablePersistence : false });
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Sets the DropDownList textbox direction as right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the enableRTL  value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",enableRTL : true });
</script>{% endhighlight %}




### fields<span class="type-signature type object">object</span>
{:#members:fields}




Specifies mapping fields for the data items of the DropDownList textbox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
<script>          
//To set fields API value during initialization  
        $("#drpdwn").ejDropDownList({ dataSource: window.countriesField,   fields: { text: "name", value: "key" }});
</script>{% endhighlight %}




### fields.category<span class="type-signature type string">String</span>
{:#members:fields-category}




Used to categorize the items. It is used when the grouping is enabled.






### fields.htmlAttributes<span class="type-signature type object">Object</span>
{:#members:fields-htmlattributes}




Defines the html attributes such as id, class, styles for the item.






### fields.id<span class="type-signature type string">String</span>
{:#members:fields-id}




Defines id for the tag.






### fields.imageAttributes<span class="type-signature type string">String</span>
{:#members:fields-imageattributes}




Defines the image attributes such as height, width, styles and so on.






### fields.imageUrl<span class="type-signature type string">String</span>
{:#members:fields-imageurl}




Defines the imageURL for the image location.






### fields.selected<span class="type-signature type boolean">Boolean</span>
{:#members:fields-selected}




Defines the tag value to be selected initially






### fields.spriteCssClass<span class="type-signature type string">String</span>
{:#members:fields-spritecssclass}




Defines the sprite css for the image tag.






### fields.tableName<span class="type-signature type string">String</span>
{:#members:fields-tablename}




Defines the table name for tag value or display text while render with remote data.






### fields.text<span class="type-signature type string">String</span>
{:#members:fields-text}




Defines the text content for the tag.






### fields.value<span class="type-signature type string">String</span>
{:#members:fields-value}




Defines the tag value or display text..






### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}




Defines the height of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//Initialize the DropDownList height property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",height: 30 });
</script>{% endhighlight %}




### itemsCount<span class="type-signature type number">number</span>
{:#members:itemscount}




Specifies the itemsCount for DropDownList.


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set itemsCount   API value during initialization  .       
        $("#drpdwn").ejDropDownList({  targetID: "carsList",itemsCount  : 2 });
</script>{% endhighlight %}




### popupHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupheight}




Defines the popupHeight of the suggestion box.


Default Value:
{:.param}



* "152px"




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//Initialize the DropDownList popupHeight property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",popupHeight: '152px' });
</script>{% endhighlight %}




### popupWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupwidth}




Defines the popupWidth of the suggestion box.


Default Value:
{:.param}



* "auto"




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//Initialize the DropDownList popupWidth property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",popupWidth: '152px' });
</script>{% endhighlight %}




### query<span class="type-signature type object">object</span>
{:#members:query}




Specifies the query to retrieve the data from online server.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
<script>          
//To set query API value during initialization  
var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});
var queryString = ej.Query().from("Suppliers").select("ContactName");
        $("#drpdwn").ejDropDownList({ dataSource: dataManger, query: queryString, fields: { text: "ContactName" }});
</script>{% endhighlight %}




### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Indicates that the DropDownList textbox values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the readOnly value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",readOnly: true });
</script>{% endhighlight %}




### selectedItemIndex<span class="type-signature type number">number</span>
{:#members:selecteditemindex}




Specifies the selectedItemIndex for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set selectedItemIndex   API value during initialization  .        
        $("#drpdwn").ejDropDownList({  targetID: "carsList",selectedItemIndex  : 2 });
</script>{% endhighlight %}




### selectedItems<span class="type-signature type integerarray">integerarray</span>
{:#members:selecteditems}




Specifies the selectedItems for DropDownList.


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set selectedItems   API value during initialization  .    
        $("#drpdwn").ejDropDownList({  targetID: "carsList",showCheckbox: true, selectedItems  : [1,2] });
</script>{% endhighlight %}




### showCheckbox<span class="type-signature type boolean">boolean</span>
{:#members:showcheckbox}




Specifies the multi selection option in DropDownList with the help of checkbox control. For this we have to enable it by showCheckbox option true.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the showCheckbox value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true });
</script>{% endhighlight %}




### showPopupOnLoad<span class="type-signature type boolean">boolean</span>
{:#members:showpopuponload}




DropDownList textbox to be displayed with Popup shown.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>                      
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the showPopupOnLoad value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showPopupOnLoad: true });
</script>{% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




DropDownList textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the showRoundedCorner value specified.
$("#drpdwn").ejDropDownList({targetID: "carsList",showRoundedCorner: true });
</script>{% endhighlight %}




### targetID<span class="type-signature type string">string</span>
{:#members:targetid}




Specifies the targetID for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// To set targetID API value during initialization  .   
        $("#drpdwn").ejDropDownList({ targetID: "carsList" });
</script>{% endhighlight %}




### template<span class="type-signature type string">string</span>
{:#members:template}




Specifies the template for DropDownList.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
 
<input type="text" id="drpdwn" /> 
 
<script>          
// To set template API value during initialization  .   
$("#drpdwn").ejDropDownList({ dataSource: window.drpdwnempList, template: '<img class="eimg" src="styles/images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/>' +
  '<div class="ename"> ${text} </div><div class="desig"> ${desig} </div><div class="cont"> ${country} </div>',width: "200px"});
</script>{% endhighlight %}




### text<span class="type-signature type string">string</span>
{:#members:text}




Defines the default text value to be display in the DropDownList textbox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
//Initialize the DropDownList text property with the  value specified
  $("#drpdwn").ejDropDownList({ targetID: "carsList",text:"Audi A7" });
</script>{% endhighlight %}




### uncheckAll<span class="type-signature type boolean">boolean</span>
{:#members:uncheckall}




Specifies to unselect all the items of DropDownList can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
// Initialize the DropDownList with the uncheckAll value specified.
$("#drpdwn").ejDropDownList({ targetID: "carsList",showCheckbox: true, uncheckAll: true });
</script>{% endhighlight %}




### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}




Set the jquery validation error message in Dropdownlist.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" name="drpdwn" /> 
 
<script>
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
</script>{% endhighlight %}




### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}




Set the jquery validation rules in Dropdownlist.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" name="drpdwn" /> 
 
<script>
//To set validationRules API during initialization              
 $("#drpdwn").ejDropDownList({
  dataSource: window.countriesField, fields: { text: "name", value: "key" }, allowGrouping: true,                       
  validationRules:{                     
          required:true
        }
});
</script>{% endhighlight %}




### value<span class="type-signature type string">string</span>
{:#members:value}




Defines the value eqivalent text to be display in the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
//Initialize the DropDownList value property with the  value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",value:"Audi A7" });
</script>{% endhighlight %}




### watermarkText<span class="type-signature type string">string</span>
{:#members:watermarktext}




Sets the watermark text. When the textbox is empty the watermark text is visible like a shaded text.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//Initialize the DropDownList with the watermarkText value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",watermarkText: 'Enter text' });
</script>{% endhighlight %}




### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the DropDownList textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//Initialize the DropDownList width property with the width value specified
        $("#drpdwn").ejDropDownList({ targetID: "carsList",width: 250 });
</script>{% endhighlight %}



## Methods




### addItem<span class="signature">()</span>
{:#methods:additem}




Add the item into the DropDownList.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("addItem",{value:"value",image:{src:"Pictures/xhtml.png",alt:"images",width:"200px",height:"500px"},htmlAttributes:"style=color:red"});     
</script>{% endhighlight %}




### checkAll<span class="signature">()</span>
{:#methods:checkall}




This method is used to set all the items to checked.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.checkAll(); // checkAll values the DropDownList
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
$('#drpdwn').ejDropDownList("checkAll");        
</script>{% endhighlight %}




### clearText<span class="signature">()</span>
{:#methods:cleartext}




Clears the text in the DropDownList textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.clearText(); // clear the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("clearText");       
</script>{% endhighlight %}




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroys the DropDownList widget.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.destroy(); // hide the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("destroy");         
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the DropDownList



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.disable(); // disable the DropDownList
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("disable");         
</script>{% endhighlight %}




### disableItemByIndex<span class="signature">()</span>
{:#methods:disableitembyindex}




To disable an Item or set of Items in the DropDownList



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
// Create DropDownList
$('#carsList').ejDropDownList();        
var DropDownListObj  = $("#carsList").data("ejDropDownList");
DropDownListObj.disableItemByIndex("3,5,7");
</script>{% endhighlight %}


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
// Create DropDownList
$('#carsList').ejDropDownList();        
$('#carsList').ejDropDownList("disableItemsByIndex" ,"3,5,7");  
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the DropDownList



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.enable(); // enable the DropDownList
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("enable");  
</script>{% endhighlight %}




### enableItemByIndex<span class="signature">()</span>
{:#methods:enableitembyindex}




To enable an Item or set of Items which are in disable in the DropDownList



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
// Create DropDownList
$('#carsList').ejDropDownList();        
var DropDownListObj  = $("#carsList").data("ejDropDownList");
DropDownListObj.enableItemByIndex("3,5,7");
</script>{% endhighlight %}


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
// Create DropDownList
$('#carsList').ejDropDownList();        
$('#carsList').ejDropDownList("enableItemsByIndex" ,"3,5,7");   
</script>{% endhighlight %}




### getSelectedItem<span class="signature">()</span>
{:#methods:getselecteditem}




This method is used to get the selected items in DropDownList.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getSelectedItem(); 
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A8"});
$('#drpdwn').ejDropDownList("getSelectedItem");         
</script>{% endhighlight %}




### getSelectedValue<span class="signature">()</span>
{:#methods:getselectedvalue}




This method is used to get the selected items value in DropDownList.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({value:"Computer IT"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getSelectedValue(); 
</script>{% endhighlight %}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select> 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({value:"Computer IT"});
$('#drpdwn').ejDropDownList("getSelectedValue");
</script>{% endhighlight %}




### getValue<span class="signature">()</span>
{:#methods:getvalue}




Returns the current value selected in the DropDownList textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.getValue(); // getValue of the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("getValue");        
</script>{% endhighlight %}




### hidePopup<span class="signature">()</span>
{:#methods:hidepopup}




popup list hide in the DropDownList textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.hidePopup(); // hidePopup of the DropDownList 
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("hidePopup");       
</script>{% endhighlight %}




### setSelectedText<span class="signature">()</span>
{:#methods:setselectedtext}




This method is used to select a list item in DropDownList using given text field.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedText("Computer IT"); // setSelectedText for the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedText","Computer IT");   
</script>{% endhighlight %}




### setSelectedValue<span class="signature">()</span>
{:#methods:setselectedvalue}




This method is used to select a list item in DropDownList using given value field.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");   
</script>{% endhighlight %}




### showPopup<span class="signature">()</span>
{:#methods:showpopup}




popup list show in the DropDownList textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.showPopup(); // 
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5"});
$('#drpdwn').ejDropDownList("showPopup");       
</script>{% endhighlight %}




### unCheckAll<span class="signature">()</span>
{:#methods:uncheckall}




This method is used to set all the items to uncheck.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.unCheckAll(); // UncheckAll values the DropDownList
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList({targetID: "carsList",value:"Audi A5",showCheckbox:true});
$('#drpdwn').ejDropDownList("unCheckAll");      
</script>{% endhighlight %}




### unselectItemByIndex<span class="signature">()</span>
{:#methods:unselectitembyindex}




This method is used to unselect a list item in DropDownList using given index field.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("Art"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByIndex(0); // unselectItemByIndex for the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
<select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","Art");  // setSelectedValue for the DropDownList text   
$('#drpdwn').ejDropDownList("unselectItemByIndex",0); // unselectItemByIndex for the DropDownList text      
</script>{% endhighlight %}




### unselectItemByText<span class="signature">()</span>
{:#methods:unselectitembytext}




This method is used to unselect a list item in DropDownList using given text field.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByText("Computer IT"); // unselectItemByText for the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");  // setSelectedValue for the DropDownList text    
$('#drpdwn').ejDropDownList("unselectItemByText","Computer IT");        
</script>{% endhighlight %}




### unselectItemByValue<span class="signature">()</span>
{:#methods:unselectitembyvalue}




This method is used to unselect a list item in DropDownList using given value field.



Example
{:.example}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
 
// Create DropDownList
$('#drpdwn').ejDropDownList();
var DropDownListObj  = $("#drpdwn").data("ejDropDownList");
DropDownListObj.setSelectedValue("ComputerIT"); // setSelectedValue for the DropDownList text
DropDownListObj.unselectItemByValue("ComputerIT"); // unselectItemByValue for the DropDownList text
</script>{% endhighlight %}


{% highlight html %}
 
  <select name="selectIndex" id="drpdwn">
       <option value="Art">Art</option>
       <option value="Architecture">Architecture</option>
       <option value="Biographies">Biographies</option>
       <option value="Business">Business</option>
       <option value="ComputerIT">Computer IT</option>
       <option value="Comics">Comics</option>
       <option value="Cookery">Cookery</option>
       <option value="Environment">Environment</option>
       <option value="Fiction">Fiction</option>
       <option value="Health">Health</option>
       <option value="Humanities">Humanities</option>
       <option value="Language">Language</option>
   </select>
<script>
 
// Create DropDownList
$('#drpdwn').ejDropDownList();
$('#drpdwn').ejDropDownList("setSelectedValue","ComputerIT");  // setSelectedValue for the DropDownList text    
$('#drpdwn').ejDropDownList("unselectItemByValue","ComputerIT");        
</script>{% endhighlight %}



## Events




### beforePopupHide
{:#events:beforepopuphide}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//beforePopupHide event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        beforePopupHide: function(args) {}
});
</script>          {% endhighlight %}




### beforePopupShown
{:#events:beforepopupshown}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//beforePopupShown event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        beforePopupShown: function(args) {}
});
</script>          {% endhighlight %}




### change
{:#events:change}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//change event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        change: function(args) {}
}); 
</script>            {% endhighlight %}




### checkChange
{:#events:checkchange}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//checkChange event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        checkChange: function(args) {}
}); 
</script>           {% endhighlight %}




### create
{:#events:create}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//change event for DropDownList
$("#drpdwn").ejDropDownList({ 
   targetID: "carsList",
        create: function(args) {}
});
</script>            {% endhighlight %}




### destroy
{:#events:destroy}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">its value is set as true,if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//destroy event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        destroy: function(args) {}
});
</script>           {% endhighlight %}




### popupHide
{:#events:popuphide}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
 </div>
 
<script>          
//popupHide event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        popupHide: function(args) {}
});
</script>           {% endhighlight %}




### popupShown
{:#events:popupshown}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//popupShown event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        popupShown: function(args) {}
});
</script>          {% endhighlight %}




### select
{:#events:select}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the DropDownList model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="drpdwn" /> 
 
 <div id="carsList">
   <ul>
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
   </ul>
 </div>
 
<script>          
//select event for DropDownList
$("#drpdwn").ejDropDownList({ 
                targetID: "carsList",
        select: function(args) {}
});      
</script>{% endhighlight %}



