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
// Create ListBox
$('#carsList').ejListBox();     
</script> {% endhighlight %}


{% highlight html %}
// Another way to render ListBox control, using its targetID.
        <ul id="listboxsample">
   </ul>
           <li>BMW 501</li>
      <li>BMW 502</li>
   <ul id="carsList">
      <li>Audi A4</li>
      <li>Audi A5</li>
      <li>Audi A6</li>
      <li>Audi A7</li>
      <li>Audi A8</li>
      <li>BMW 503</li>
      <li>BMW 507</li>
      <li>BMW 3200</li>
   </ul>
<script>
// Create ListBox
$('#listboxsample').ejListBox({targetID: "carlist"});   
</script> {% endhighlight %}




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
{:#members:allowdraganddrop}




To enable the drag and drop nodes.


Default Value:
{:.param}



* true




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
// Initialize the with the allowDragAndDrop value specified.
$('#carsList').ejListBox({allowDragAndDrop: true});     
</script> {% endhighlight %}




### allowGrouping<span class="type-signature type boolean">boolean</span>
{:#members:allowgrouping}




Specifies the grouping option in ListBox.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
   <ul id="select1">    </ul>

<script>
            var skillset = [
          { skill: "Bahrain", category: "B" }, { skill: "Brazil", category: "B" }, { skill: "Argentina", category: "A" },
       { skill: "Bangladesh", category: "B" }, { skill: "Burma", category: "B" }, { skill: "Afghanistan", category: "A" }, { skill: "Antigua and Barbuda", category: "A" },
       { skill: "Barbados", category: "B" }, { skill: "Botswana", category: "B" }, { skill: "Albania", category: "A" }, { skill: "Andorra", category: "A" },
       { skill: "Belarus", category: "B" }, { skill: "Bolivia", category: "B" }, { skill: "Algeria", category: "A" }, { skill: "Angola", category: "A" }
       ];
// Initialize the ListBox with the allowGrouping value specified.
          $("#select1").ejListBox({
       dataSource: skillset,
         fields: { text: "skill", category: "category" },allowGrouping:true
             });
</script> {% endhighlight %}




### allowMultiSelection<span class="type-signature type boolean">boolean</span>
{:#members:allowmultiselection}




To allow multiple selection of list items


Default Value:
{:.param}



* true




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
// Initialize the allowMultiSelection with the value specified.
$('#carsList').ejListBox({allowMultiSelection: true});  
</script> {% endhighlight %}




### cascadeTo<span class="type-signature type string">string</span>
{:#members:cascadeto}




cascadeTo is used in cascading ListBox scenario, to map the child ListBox list widget in the parent ListBox list widget. By selecting an option in the parent ListBox, the child ListBox has to load the corresponding value regarding the parent ListBox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<div style="float: left;">
      <span class="txt">Select Group</span>
  <ul id="groupsList" /> </ul>
</div>

<div style="float: right;">
       <span class="txt">Select Country</span>
       <ul id="countryList" /> </ul>
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
           $('#groupsList').ejListBox({
               dataSource: groups,
               fields: { value: "parentId" },
               cascadeTo: 'countryList'
           });
           $('#countryList').ejListBox({
               dataSource: countries,
               enabled:false
           });
</script>{% endhighlight %}




### checkAll<span class="type-signature type boolean">boolean</span>
{:#members:checkall}




Specifies to select all the items of ListBox can be done with the help of this checkAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the checkAll value specified.
$('#carsList').ejListBox({showCheckbox: true, checkAll: true  });       
</script> {% endhighlight %}




### checkedItemlist<span class="type-signature type integerarray">integerarray</span>
{:#members:checkeditemlist}




Specifies the checkedItemlist for ListBox.


Default Value:
{:.param}



* []




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
// To sets the checked item  API value during initialization  .         
$('#carsList').ejListBox({ showCheckbox:true,checkedItemlist  : [1,2] });       
</script> {% endhighlight %}




### checkItemsByIndex<span class="type-signature type string">string</span>
{:#members:checkitemsbyindex}




Specifies the index value to check the items in the listbox.


Default Value:
{:.param}



* null




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
// To set checkItemsByIndex API value during initialization  .
$('#carsList').ejListBox("disable");    
$('#carsList').ejListBox({checkItemsByIndex  : "2,3"});         
</script> {% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for ListBox theme. This cssClass API helps to use custom skinning option for ListBox control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* "gradient-lime"




Example
{:.example}


{% highlight html %}
 

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
//Initialize the ListBox with the cssClass value specified
        $("#carsList").ejListBox({ targetID: "carsList",cssClass: 'gradient-lime'});
</script>{% endhighlight %}




### dataSource<span class="type-signature type data">data</span>
{:#members:datasource}




Specifies the data source of the ListBox. The data source contains the list of data for generating the List items.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
 <ul id="countrylist">  </ul>
<script>          
//To set dataSource API value during initialization  
        $("#countrylist").ejListBox({ dataSource: window.countries });                   
</script>{% endhighlight %}




### disableItemsByIndex<span class="type-signature type string">string</span>
{:#members:disableitemsbyindex}




Specifies the index value to disable the items in the listbox.


Default Value:
{:.param}



* null




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
// To set disableItemsByIndex API value during initialization  .
$('#carsList').ejListBox({disableItemsByIndex  : "2,3"});
</script> {% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




When this property sets to false, it disables the ListBox control.


Default Value:
{:.param}



* true




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
// Initialize the ListBox with the enabled  value specified.
$('#carsList').ejListBox({enabled : false  });  
</script> {% endhighlight %}




### enableItemsByIndex<span class="type-signature type string">string</span>
{:#members:enableitemsbyindex}




Specifies the index value to enable the items in the listbox.


Default Value:
{:.param}



* null




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
// To set enableItemsByIndex API value during initialization  .
$('#carsList').ejListBox("disable");    
$('#carsList').ejListBox({enableItemsByIndex  : "2,3"});        
</script> {% endhighlight %}




### enableLoadOnDemand<span class="type-signature type boolean">boolean</span>
{:#members:enableloadondemand}




Specifies to enable Load data items onDemand for the ListBox.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
 <ul id="countrylist">  </ul>
<script>          
//To set fields API value during initialization  
        $("#countrylist").ejListBox({ dataSource: window.countriesField, enableLoadOnDemand:true,  fields: { text: "name", value: "key" }});
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintains. While refresh the ListBox control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the enablePersistence  value specified.
$('#carsList').ejListBox({enablePersistence : false});  
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Sets the ListBox textbox direction as right to left alignment.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the enableRTL  value specified.
$('#carsList').ejListBox({enableRTL : true  });         
</script> {% endhighlight %}




### enableTooltip<span class="type-signature type boolean">boolean</span>
{:#members:enabletooltip}




Sets to enable tooltip text for ListBox.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the enableRTL  value specified.
$('#carsList').ejListBox({enableTooltip : true  });     
</script> {% endhighlight %}




### enableVirtualScrolling<span class="type-signature type boolean">boolean</span>
{:#members:enablevirtualscrolling}




Specifies to enable virtual scrolling behavior along with Load data items onDemand for the ListBox.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
 <ul id="countrylist">  </ul>
<script>          
//To set fields API value during initialization  
        $("#countrylist").ejListBox({ dataSource: window.countriesField, enableLoadOnDemand:true,enableVirtualScrolling:true,  fields: { text: "name", value: "key" }});
</script>{% endhighlight %}




### fields<span class="type-signature type object">object</span>
{:#members:fields}




Specifies mapping fields for the data items of the ListBox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
 <ul id="countrylist">  </ul>
<script>          
//To set fields API value during initialization  
        $("#countrylist").ejListBox({ dataSource: window.countriesField,   fields: { text: "name", value: "key" }});
</script>{% endhighlight %}




### fields.category<span class="type-signature type string">String</span>
{:#members:fields-category}




Defines the category for data item.






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






### fields.selected<span class="type-signature type string">String</span>
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






### fields.toolTipText<span class="type-signature type object">Object</span>
{:#members:fields-tooltiptext}




Defines the tooltip text to be displayed for the data list item.






### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}




Defines the height of the ListBox.


Default Value:
{:.param}



* Null




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
//Initialize the ListBox height property with the  value specified
$('#carsList').ejListBox({ height: "300"});     
</script> {% endhighlight %}




### query<span class="type-signature type object">object</span>
{:#members:query}




Specifies the query to retrieve the data from online server.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
 <ul id="customerlist">  </ul>
<script>          
//To set query API value during initialization  
var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});
var queryString = ej.Query().from("Suppliers").select("Customers");
        $("#customerlist").ejListBox({ dataSource: dataManger, query: queryString, fields: { text: "CustomerID" }});
</script>{% endhighlight %}




### selectedItemIndex<span class="type-signature type number">number</span>
{:#members:selecteditemindex}




Specifies the selectedItemIndex for ListBox.


Default Value:
{:.param}



* null




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
// To set selectedItemIndex   API value during initialization  .        
$('#carsList').ejListBox({selectedItemIndex  : 2});     
</script> {% endhighlight %}




### selectedItemlist<span class="type-signature type integerarray">integerarray</span>
{:#members:selecteditemlist}




Specifies the selectedItems for ListBox.


Default Value:
{:.param}



* []




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
// To set selectedItemlist   API value during initialization  .         
$('#carsList').ejListBox({ allowMultiSelection:true,selectedItemlist  : [1,2] });       
</script> {% endhighlight %}




### selectedItems<span class="type-signature type integerarray">integerarray</span>
{:#members:selecteditems}




Specifies the items to be an selected in listbox.


Default Value:
{:.param}



* null




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
// To set selectedItems API value during initialization  .
$('#carsList').ejListBox({showCheckbox: true, selectedItems : [1,2]});
</script> {% endhighlight %}




### showCheckbox<span class="type-signature type boolean">boolean</span>
{:#members:showcheckbox}




Specifies the multi selection option in ListBox with the help of checkbox control. For this we have to set showCheckbox option true.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the showCheckbox value specified.
$('#carsList').ejListBox({showCheckbox: true });        
</script> {% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




ListBox textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* true




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
// Initialize the ListBox with the showRoundedCorner value specified.
$('#carsList').ejListBox({ showRoundedCorner: true });  
</script> {% endhighlight %}




### template<span class="type-signature type string">string</span>
{:#members:template}




Specifies the template for ListBox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
 
<ul id="carsList" /> </ul> 
 
<script>          
// To set template API value during initialization  .   
$("#carsList").ejListBox({ dataSource: window.carsListempList, template: '<img class="eimg" src="styles/images/Employee/${eimg}.png" alt="employee" height="50px" width="50px"/>' +
  '<div class="ename"> ${text} </div><div class="desig"> ${desig} </div><div class="cont"> ${country} </div>'});
</script>{% endhighlight %}




### unCheckAll<span class="type-signature type boolean">boolean</span>
{:#members:uncheckall}




Specifies to uncheck all the items of ListBox can be done with the help of this unCheckAll property, it supports only when the showCheckbox property true.


Default Value:
{:.param}



* false




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
// Initialize the ListBox with the uncheckAll value specified.
$('#carsList').ejListBox({showCheckbox: true,  uncheckAll: true  });    
</script> {% endhighlight %}




### uncheckItemsByIndex<span class="type-signature type string">string</span>
{:#members:uncheckitemsbyindex}




Specifies the index value to uncheck the items in the listbox.


Default Value:
{:.param}



* null




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
// To set uncheckItemsByIndex API value during initialization  .
$('#carsList').ejListBox({uncheckItemsByIndex  : "2,3"});
</script> {% endhighlight %}




### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the ListBox.


Default Value:
{:.param}



* Null




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
//Initialize the ListBox width property with the  value specified
$('#carsList').ejListBox({ width: "220"});      
</script> {% endhighlight %}



## Methods




### addItem<span class="signature">()</span>
{:#methods:additem}




To add an list item in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.addItem("Java"); // add an new item in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("addItem","Java");     
</script>{% endhighlight %}




### checkAll<span class="signature">()</span>
{:#methods:checkall}




To check all the list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.checkAll(); // checks all the list items in the ListBox
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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
$('#carsList').ejListBox("checkAll");   
</script>{% endhighlight %}




### checkItemByIndex<span class="signature">()</span>
{:#methods:checkitembyindex}




To check a list items through index in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.checkItemsByIndex(2,3); // checks the specified items the ListBox
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
// Create ListBox       
$('#carsList').ejListBox("checkItemByIndex","2,3");     
</script>{% endhighlight %}




### checkitems<span class="signature">()</span>
{:#methods:checkitems}




To check items in the checkitemslist in the ListBox



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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.checkitems(); // checks all the list items in the checkedItemlist
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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
$('#carsList').ejListBox("checkitems");         
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.disable(); // disable the ListBox
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
// Create ListBox
$('#carsList').ejListBox();
$('#carsList').ejListBox("disable");    
</script>{% endhighlight %}




### disableItem<span class="signature">()</span>
{:#methods:disableitem}




To disable an list item in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.disableItem(); // disable selected item in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("disableItem");        
</script>{% endhighlight %}




### disableItemByIndex<span class="signature">()</span>
{:#methods:disableitembyindex}




To disable an Item or set of Items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.disableItemByIndex("3,5,7");
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("disableItemsByIndex" ,"3,5,7");
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.enable(); // enable the ListBox
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
// Create ListBox
$('#carsList').ejListBox();
$('#carsList').ejListBox("enable");     
</script>{% endhighlight %}




### enableItemByIndex<span class="signature">()</span>
{:#methods:enableitembyindex}




To enable a single Item or set of Items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.enableItemByIndex("3,5");
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("enableItemsByIndex" ,"3,5");
</script>{% endhighlight %}




### getCheckedItems<span class="signature">()</span>
{:#methods:getcheckeditems}




To get the list of checked list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.getCheckedItems(); // get the list of checked items the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("getCheckedItems");    
</script>{% endhighlight %}




### getSelectedItem<span class="signature">()</span>
{:#methods:getselecteditem}




To get the selected list item in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.getSelectedItem(); // gets the selected item from the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("getSelectedItem");    
</script>{% endhighlight %}




### getSelectedItems<span class="signature">()</span>
{:#methods:getselecteditems}




To get the list of selected list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.getSelectedItems(); // gets the list of selected list items from the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("getSelectedItems");   
</script>{% endhighlight %}




### moveDown<span class="signature">()</span>
{:#methods:movedown}




To move the selected list item one step Down in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.moveDown(); //moves down the selected item in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("moveDown");   
</script>{% endhighlight %}




### moveUp<span class="signature">()</span>
{:#methods:moveup}




To move the selected list item one step Up in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.moveUp(); // moves up selected item in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("moveUp");     
</script>{% endhighlight %}




### removeItem<span class="signature">()</span>
{:#methods:removeitem}




To remove an list item in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.removeItem(); // removes the selected item from the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("removeItem");         
</script>{% endhighlight %}




### selectAll<span class="signature">()</span>
{:#methods:selectall}




To select all the list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.selectAll(); // selects all the list items in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("selectAll");  
</script>{% endhighlight %}




### selectItemByIndex<span class="signature">()</span>
{:#methods:selectitembyindex}




To select an Item using its index in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.selectItemByIndex(2); //selects the item in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("selectItemByIndex" ,"2");     
</script>{% endhighlight %}




### selectItemsByIndex<span class="signature">()</span>
{:#methods:selectitemsbyindex}




To select a list items through index in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.selectItemsByIndex(2,3); // selects the specified items the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("selectItemsByIndex","2,3");   
</script>{% endhighlight %}




### unCheckAll<span class="signature">()</span>
{:#methods:uncheckall}




To uncheck all the list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.unCheckAll(); // Unchecks all the list items in the ListBox
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
// Create ListBox
$('#carsList').ejListBox({showCheckbox:true});  
$('#carsList').ejListBox("unCheckAll");         
</script>{% endhighlight %}




### uncheckItemByIndex<span class="signature">()</span>
{:#methods:uncheckitembyindex}




To uncheck set of list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.uncheckItemsByIndex(2,3); // uncheckItems specified the ListBox
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
// Create ListBox
$('#carsList').ejListBox("uncheckItemByIndex","2,3");   
</script>{% endhighlight %}




### unSelectAll<span class="signature">()</span>
{:#methods:unselectall}




To unselect all the list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.unSelectAll(); // unselect all the items in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("unSelectAll");        
</script>{% endhighlight %}




### unselectItemByIndex<span class="signature">()</span>
{:#methods:unselectitembyindex}




To unselect a list item in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.unselectItemByIndex(2); // unselects the list item specified in the index  in the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("unselectItemByIndex","2");    
</script>{% endhighlight %}




### unselectItemsByIndex<span class="signature">()</span>
{:#methods:unselectitemsbyindex}




To unselect set of list items in the ListBox



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
// Create ListBox
$('#carsList').ejListBox();     
var ListBoxObj  = $("#carsList").data("ejListBox");
ListBoxObj.unselectItemsByIndex(2,3); // unselectItems specified the ListBox
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
// Create ListBox
$('#carsList').ejListBox();     
$('#carsList').ejListBox("unselectItemsByIndex","2,3");         
</script>{% endhighlight %}



## Events




### checkChange
{:#events:checkchange}




Fires when check state of an list item changed successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//checkChange event for ListBox
$('#carsList').ejListBox({      showCheckbox:true,checkChange: function(args) {}});     
</script>            {% endhighlight %}




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
<td class="description last">returns the ListBox model</td>
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
//create event for ListBox
$('#carsList').ejListBox({      create: function(args) {}});    
</script>            {% endhighlight %}




### destroy
{:#events:destroy}




Fires when destroy successfully.



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
//destroy event for ListBox
$('#carsList').ejListBox({      destroy: function(args) {}});   
</script>           {% endhighlight %}




### destroy
{:#events:destroy}




Fires when the listbox data items loaded successfully.



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
//actionComplete event for ListBox
$('#carsList').ejListBox({      destroy: function(args) {}});   
</script>           {% endhighlight %}




### itemDrag
{:#events:itemdrag}




Fires when list item is being dragged successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//itemDrag event for ListBox
$('#carsList').ejListBox({      itemDrag: function(args) {}});  
</script>            {% endhighlight %}




### itemDragStart
{:#events:itemdragstart}




Fires when list item started to drag successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//itemDragStart event for ListBox
$('#carsList').ejListBox({      itemDragStart: function(args) {}});     
</script>            {% endhighlight %}




### itemDragStop
{:#events:itemdragstop}




Fires when list item stopped dragging successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//itemDragStop event for ListBox
$('#carsList').ejListBox({      itemDragStop: function(args) {}});      
</script>            {% endhighlight %}




### itemDropped
{:#events:itemdropped}




Fires when list item stopped dropping successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//itemDropped event for ListBox
$('#carsList').ejListBox({      itemDropped: function(args) {}});       
</script>            {% endhighlight %}




### selected
{:#events:selected}




Fires when list item gets selected successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//selected event for ListBox
$('#carsList').ejListBox({      selected: function(args) {}});  
</script>            {% endhighlight %}




### selectIndexChanged
{:#events:selectindexchanged}




Fires when selected list item Index Changed successfully.

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
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the ListBox model</td>
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
//selectIndexChanged event for ListBox
$('#carsList').ejListBox({      selectIndexChanged: function(args) {}});        
</script>            {% endhighlight %}



