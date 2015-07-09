---
layout: post
title: ejAutocomplete
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Textbox control.





$(element).ejAutocomplete<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Create AutoComplete
$('#autocomplete').ejAutocomplete({ dataSource: window.carList,value:"Austin-Healey" });        
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.autocomplete.js

* module:ej.scroller.js


## Members




### addNewText<span class="type-signature type string">string</span>
{:#members:addnewtext}




Allows new text to be added to in the popup of the autocomplete when there are no suggestions. This property can only be used in the Visual mode only.


Default Value:
{:.param}



* "Add New"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the addNewText value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,allowAddNew: true,addNewText: "Add New Car" });
&lt;/script&gt;</code>
</pre>



### allowAddNew<span class="type-signature type boolean">boolean</span>
{:#members:allowaddnew}




Specifies new values can be added to the autocomplete input other than the values in the suggestion list.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the allowAddNew value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,allowAddNew: true });
&lt;/script&gt;</code>
</pre>



### allowGrouping<span class="type-signature type boolean">boolean</span>
{:#members:allowgrouping}




Groups the search result based on the category value and displays the items in set of groups.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the grouping value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.vehicle, allowGrouping: true});
&lt;/script&gt;</code>
</pre>



### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowsorting}




Sorts the lists value in ascending order if set to true and enables sorting.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the allowSorting value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,allowSorting: false });
&lt;/script&gt;</code>
</pre>



### autoFocus<span class="type-signature type boolean">boolean</span>
{:#members:autofocus}




This property enables to active the first element in the popup. It will automatically focus the first element in the popup.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete autoFocus property 
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,autoFocs: true });
&lt;/script&gt;</code>
</pre>



### caseSensitiveSearch<span class="type-signature type boolean">boolean</span>
{:#members:casesensitivesearch}




Sets the case sensitivity of the search operation..


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the caseSensitiveSearch value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,caseSensitiveSearch: true });
&lt;/script&gt;</code>
</pre>



### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for Autocomplete theme. This cssClass API helps to use custom skinning option for Autocomplete control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the cssClass value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,cssClass: 'gradient-lime'});
&lt;/script&gt;</code>
</pre>



### dataSource<span class="type-signature type data">data</span>
{:#members:datasource}




Specifies the Data Source of the AutoComplete.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//To set dataSource API value during initialization  
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,value:"Austin-Healey"});                         
&lt;/script&gt;</code>
</pre>



### delaySuggestionTimeout<span class="type-signature type number">number</span>
{:#members:delaysuggestiontimeout}




The delaySuggestionTimeout used to set the milliseconds time between a keypress and when the widget displays the suggestion popup.


Default Value:
{:.param}



* 200




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with delaySuggestionTimeout in milliseconds value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,delaySuggestionTimeout : 500 });
&lt;/script&gt;</code>
</pre>



### delimiterChar<span class="type-signature type string">string</span>
{:#members:delimiterchar}




Sets the separator to allow multiple word searches. While typing the texts in the text box, if we enter the delimiter value, the texts after the delimiter are considered as a separate word or query. The delimiter string should have a single character and must be a symbol. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.


Default Value:
{:.param}



* ';'




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the delimiterChar value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,multiSelectMode: ej.MultiSelectMode.Delimiter,delimiterChar: ';' });
&lt;/script&gt;</code>
</pre>



### emptyResultText<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:emptyresulttext}




Sets the emptyResultText message text. When there is no suggestions are available at the time this message will be shown.


Default Value:
{:.param}



* "No suggestions"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete emptyResultText property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,emptyResultText: 'No Results Found' });
&lt;/script&gt;</code>
</pre>



### enableAutoFill<span class="type-signature type boolean">boolean</span>
{:#members:enableautofill}




Automatically fills the first item from the suggestion list in an AutoComplete text box. The autoFill property is only applicable for &ldquo;startswith&rdquo; filterType type.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the enableAutoFill  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enableAutoFill : true });
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




When this property sets to false, it disables the Autocomplete control.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the enabled  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enabled : false });
&lt;/script&gt;</code>
</pre>



### enableDistinct<span class="type-signature type boolean">boolean</span>
{:#members:enabledistinct}




Prevents the duplicate names presents in the search result.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the enableDistinct value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,enableDistinct: true });
&lt;/script&gt;</code>
</pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintains. While refresh the Autocomplete control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the enablePersistence   value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enablePersistence  : true });
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Sets the Autocomplete textbox direction as right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the enableRTL    value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enableRTL   : true });
&lt;/script&gt;</code>
</pre>



### fields<span class="type-signature type object">object</span>
{:#members:fields}




Specifies mapping fields for the data items of the Autocomplete textbox.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;  
//To set fields API value during initialization         
        $("#autocomplete").ejAutocomplete({ dataSource:window.countriesField,fields: { text: "name", key: "key" }});
&lt;/script&gt;</code>
</pre>



### fields.category<span class="type-signature type string">String</span>
{:#members:fields-category}




Used to categorize the items. It is used when the grouping is enabled..






### fields.htmlAttributes<span class="type-signature type object">Object</span>
{:#members:fields-htmlattributes}




Defines the html attributes such as id, class, styles for the item..






### fields.key<span class="type-signature type string">String</span>
{:#members:fields-key}




Defines the key for the items to differentiate two items with same.






### fields.text<span class="type-signature type string">String</span>
{:#members:fields-text}




Defines the tag value or display text..






### filterType<span class="type-signature type enum">enum</span>
{:#members:filtertype}




Sets the search filter type. There are several filter types are available such as &lsquo;startswith&rsquo;, &lsquo;contains&rsquo;, &lsquo;endswith&rsquo;, &lsquo;lessthan&rsquo;, &lsquo;lessthanorequal&rsquo;, &lsquo;greaterthan&rsquo;, &lsquo;greaterthanorequal&rsquo;, &lsquo;equal&rsquo;, &lsquo;notequal&rsquo;. See <a href="global.html#filterType">filterType</a>


Default Value:
{:.param}



* ej.filterType.StartsWith




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the filterType value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,filterType: 'contains'  });                                        
&lt;/script&gt;</code>
</pre>



### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}




Defines the height of the Autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete height property with the  value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList, height: 30 });
&lt;/script&gt;</code>
</pre>



### highlightSearch<span class="type-signature type boolean">boolean</span>
{:#members:highlightsearch}




Enables the highlight search option. When the highlightSearch option set to true, the corresponding string entered in the textbox is highlighted in the suggestion list.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the highlightSearch  value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList, highlightSearch : true });
&lt;/script&gt;</code>
</pre>



### itemsCount<span class="type-signature type number">number</span>
{:#members:itemscount}




Count of the item that gets displayed in the popup


Default Value:
{:.param}



* 0




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Count of the item that gets displayed in the popup
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,itemsCount : 2 });
&lt;/script&gt;</code>
</pre>



### minCharacter<span class="type-signature type number">number</span>
{:#members:mincharacter}




Minimum character that the autocomplete popup gets opened.


Default Value:
{:.param}



* 1




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Minimum character that the autocomplete popup gets opened.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,minCharacter : 3 });
&lt;/script&gt;</code>
</pre>



### multiSelectMode<span class="type-signature type enum">enum</span>
{:#members:multiselectmode}




Allows to select multiple values from the suggestion list. Multiple values can be selected through either of the following options,Delimiter-Multiple values separated using comma.Visual mode- Each values are displayed in separate box with close button. See <a href="global.html#MultiSelectMode">MultiSelectMode</a>


Default Value:
{:.param}



* ej.MultiSelectMode.None




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the multiSelectMode value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,multiSelectMode: ej.MultiSelectMode.Delimiter  });                                         
&lt;/script&gt;</code>
</pre>



### popupHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupheight}




Defines the popupHeight of the suggestion box.


Default Value:
{:.param}



* "152px"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete popupHeight property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,popupHeight: '152px' });
&lt;/script&gt;</code>
</pre>



### popupWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:popupwidth}




Defines the popupWidth of the suggestion box.


Default Value:
{:.param}



* "auto"




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete popupWidth property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,popupWidth: '152px' });
&lt;/script&gt;</code>
</pre>



### query<span class="type-signature type object">object</span>
{:#members:query}




Specifies the query to retrieve the data from online server.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code>&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;                   
//To set query API value during initialization  
var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});
var queryString = ej.Query().from("Suppliers").select("ContactName");
        $("#autocomplete").ejAutocomplete({ dataSource: dataManger, query: queryString, fields: { text: "ContactName" }});
&lt;/script&gt;</code>
</pre>



### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Indicates that the autocomplete textbox values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the readOnly value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,readOnly: true });
&lt;/script&gt;</code>
</pre>



### selectValueByKey
{:#members:selectvaluebykey}




Set the values to the Autocomplete textbox by input key value.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle,selectValueByKey:"a"});   
&lt;/script&gt;</code>
</pre>



### showEmptyResultText<span class="type-signature type boolean">boolean</span>
{:#members:showemptyresulttext}




Sets whether the noResults message will be shown or not.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the showEmptyResultText value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList, showEmptyResultText : false });
&lt;/script&gt;</code>
</pre>



### showLoadingIcon<span class="type-signature type boolean">boolean</span>
{:#members:showloadingicon}




Enables the loading icon to intimate the searching operation. The loading icon is visible when there is a time delay to perform the search.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the showLoadingIcon value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,showLoadingIcon: false });
&lt;/script&gt;</code>
</pre>



### showPopupButton<span class="type-signature type boolean">boolean</span>
{:#members:showpopupbutton}




Enables the showPopup button. When the Showpopup button clicks, it displays the full list from the dataSource.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the showPopupButton  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,showPopupButton : true });
&lt;/script&gt;</code>
</pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Autocomplete textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the showRoundedCorner value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,showRoundedCorner: true });
&lt;/script&gt;</code>
</pre>



### sortOrder<span class="type-signature type enum">enum</span>
{:#members:sortorder}




Sort order specifies whether the suggestion list values has to display in ascending or descending order. See <a href="global.html#SortOrder">SortOrder</a>


Default Value:
{:.param}



* ej.SortOrder.Ascending




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the sortOrder value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,sortOrder:"descending" });                                        
&lt;/script&gt;</code>
</pre>



### template<span class="type-signature type string">string</span>
{:#members:template}




Specifies the template for Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// To set template API value during initialization.     
$("#autocomplete").ejAutocomplete({ dataSource: window.countries,template:"&lt;div class='flag ${sprite}'&gt; &lt;/div&gt;"+"&lt;div class='txt'&gt; ${text} &lt;/div&gt;"});
&lt;/script&gt;</code>
</pre>



### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}




Set the jquery validation error message in Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" name="autocomplete" /&gt; 
 
&lt;script&gt;
//To set validationMessage API during initialization            
  $("#autocomplete").ejAutocomplete({ 
  dataSource: window.carList,                   
  validationRules:{                     
          required:true
        },
        validationMessage: {
                required: "Required Autocomplete value"
        }
});
&lt;/script&gt;</code>
</pre>



### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}




Set the jquery validation rules in Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" name="autocomplete" /&gt; 
 
&lt;script&gt;
//To set validationRules API during initialization              
  $("#autocomplete").ejAutocomplete({ 
  dataSource: window.carList,                   
  validationRules:{                     
          required:true
        }
});
&lt;/script&gt;</code>
</pre>



### value<span class="type-signature type string">string</span>
{:#members:value}




Defines the default value to be displayed in the autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete value property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,value:"Elantra" });
&lt;/script&gt;</code>
</pre>



### visible<span class="type-signature type boolean">boolean</span>
{:#members:visible}




Specifies the to show or hide.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Initialize the Autocomplete with the visible value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,visible: false });
&lt;/script&gt;</code>
</pre>



### watermarkText<span class="type-signature type string">string</span>
{:#members:watermarktext}




Sets the watermarkText text. When the textbox is empty the watermarkText text is visible like a shaded text.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete with the watermarkText value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,watermarkText: 'Enter the car name' });
&lt;/script&gt;</code>
</pre>



### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the Autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
//Initialize the Autocomplete width property with the width value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,width: 200 });
&lt;/script&gt;</code>
</pre>


## Methods




### clearText<span class="signature">()</span>
{:#methods:cleartext}




Clears the text in the Autocomplete textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.clearText(); // clear the autocomplete text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Clears the text in the autocomplete
$('#autocomplete').ejAutocomplete("clearText");         
&lt;/script&gt;</code>
</pre>



### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy in the Autocomplete textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.destroy(); // destroy the autocomplete 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// destroys autocomplete
$('#autocomplete').ejAutocomplete("destroy");   
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#methods:disable}




To disable the autocomplete



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.disable(); // disable the autocomplete
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Disables autocomplete
$('#autocomplete').ejAutocomplete("disable");   
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#methods:enable}




To enable the autocomplete



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});   
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.enable(); // enable the autocomplete
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});   
// Enables autocomplete
$('#autocomplete').ejAutocomplete("enable");    
&lt;/script&gt;</code>
</pre>



### getSelectedItems<span class="signature">()</span>
{:#methods:getselecteditems}




Returns the values selected in the Autocomplete textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.getSelectedItems(); // getSelectedItems the autocomplete text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Get the selected items in the autocomplete
$('#autocomplete').ejAutocomplete("getSelectedItems");  
&lt;/script&gt;</code>
</pre>



### getValue<span class="signature">()</span>
{:#methods:getvalue}




Returns the current value selected in the Autocomplete textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.getValue(); // getValue of the autocomplete text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Get the value of the selected item in the autocomplete
$('#autocomplete').ejAutocomplete("getValue");  
&lt;/script&gt;</code>
</pre>



### search<span class="signature">()</span>
{:#methods:search}




search values in the Autocomplete textbox.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.search(); // search the autocomplete text
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Searches the item in the autocomplete
$('#autocomplete').ejAutocomplete("search");    
&lt;/script&gt;</code>
</pre>



### selectValueByKey<span class="signature">()</span>
{:#methods:selectvaluebykey}




Set the values to the Autocomplete textbox by input key value.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});   
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
  // set key value corresponding text to the autocomplete textbox
autocompleteObj.selectValueByKey("F"); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Create autocomplete
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});
$('#autocomplete').ejAutocomplete("selectValueByKey","F");  
&lt;/script&gt;</code>
</pre>



### selectValueByText<span class="signature">()</span>
{:#methods:selectvaluebytext}




Set the values to the Autocomplete textbox by input text value.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});        
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.selectValueByText("BMW 7"); // set text value to the autocomplete textbox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
// Create autocomplete
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle}); 
$('#autocomplete').ejAutocomplete("selectValueByText","BMW 7");         
&lt;/script&gt;</code>
</pre>


## Events




### change
{:#events:change}




Fires when changed successfully.

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
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//change event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        change: function(args) {}
});  
&lt;/script&gt;                 </code>
</pre>



### close
{:#events:close}




Fires after Autocomplete control popup is closed.

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
<td class="description last">returns the Autocomplete model</td>
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
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//close event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        close: function(args) {}
}); 
&lt;/script&gt;                  </code>
</pre>



### create
{:#events:create}




Fires after Autocomplete control is created.

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
<td class="description last">returns the Autocomplete model</td>
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
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//create event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        create: function(args) {}
}); 
&lt;/script&gt;                  </code>
</pre>



### destroy
{:#events:destroy}




Fires when the Autocomplete is destroyed successfully

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
<td class="description last">returns the Autocomplete model</td>
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
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//destroy event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        destroy: function(args) {}
}); 
&lt;/script&gt;                  </code>
</pre>



### focusIn
{:#events:focusin}




Fires when focusIn successfully.

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
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//focusIn event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        focusIn: function(args) {}
});      
&lt;/script&gt;                 </code>
</pre>



### focusOut
{:#events:focusout}




Fires when focusOut successfully.

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
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//focusOut event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        focusOut: function(args) {}
});  
&lt;/script&gt;                                         </code>
</pre>



### open
{:#events:open}




Fires after Autocomplete control popup is opned.

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
<td class="description last">returns the Autocomplete model</td>
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
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//open event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        open: function(args) {}
}); 
&lt;/script&gt;                  </code>
</pre>



### select
{:#events:select}




Fires when an item has been selected successfully.

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
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name"><code>argument.key</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected value key</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="text" id="autocomplete" /&gt; 
 
&lt;script&gt;
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//select event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        select: function(args) {}
}); 
&lt;/script&gt;                 </code>
</pre>


