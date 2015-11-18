---
layout: post
title: ejAutocomplete
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejAutocomplete

The AutoComplete control is a textbox control that provides a list of suggestions based on the user query.When the users enters the text in the text box, the control performs a search operation and provides a list of results in the suggestion pop up. There are several filter types available to perform the search.


$(element).ejAutocomplete<span class="signature">()</span>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Create AutoComplete
$('#autocomplete').ejAutocomplete({ dataSource: window.carList,value:"Austin-Healey" });        
</script>{% endhighlight %}




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


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the addNewText value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,allowAddNew: true,addNewText: "Add New Car" });
</script>{% endhighlight %}




### allowAddNew<span class="type-signature type boolean">boolean</span>
{:#members:allowaddnew}




Specifies new values can be added to the autocomplete input other than the values in the suggestion list.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the allowAddNew value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,allowAddNew: true });
</script>{% endhighlight %}




### allowGrouping<span class="type-signature type boolean">boolean</span>
{:#members:allowgrouping}




Groups the search result based on the category value and displays the items in set of groups.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the grouping value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.vehicle, allowGrouping: true});
</script>{% endhighlight %}




### allowSorting<span class="type-signature type boolean">boolean</span>
{:#members:allowsorting}




Sorts the lists value in ascending order if set to true and enables sorting.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the allowSorting value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,allowSorting: false });
</script>{% endhighlight %}




### autoFocus<span class="type-signature type boolean">boolean</span>
{:#members:autofocus}




This property enables to active the first element in the popup. It will automatically focus the first element in the popup.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete autoFocus property 
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,autoFocs: true });
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
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the caseSensitiveSearch value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,caseSensitiveSearch: true });
</script>{% endhighlight %}




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for Autocomplete theme. This cssClass API helps to use custom skinning option for Autocomplete control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the cssClass value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,cssClass: 'gradient-lime'});
</script>{% endhighlight %}




### dataSource<span class="type-signature type data">data</span>
{:#members:datasource}




Specifies the Data Source of the AutoComplete.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//To set dataSource API value during initialization  
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,value:"Austin-Healey"});                         
</script>{% endhighlight %}




### delaySuggestionTimeout<span class="type-signature type number">number</span>
{:#members:delaysuggestiontimeout}




The delaySuggestionTimeout used to set the milliseconds time between a keypress and when the widget displays the suggestion popup.


Default Value:
{:.param}



* 200




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with delaySuggestionTimeout in milliseconds value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,delaySuggestionTimeout : 500 });
</script>{% endhighlight %}




### delimiterChar<span class="type-signature type string">string</span>
{:#members:delimiterchar}




Sets the separator to allow multiple word searches. While typing the texts in the text box, if we enter the delimiter value, the texts after the delimiter are considered as a separate word or query. The delimiter string should have a single character and must be a symbol. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.


Default Value:
{:.param}



* ';'




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the delimiterChar value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,multiSelectMode: ej.MultiSelectMode.Delimiter,delimiterChar: ';' });
</script>{% endhighlight %}




### emptyResultText<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:emptyresulttext}




Sets the emptyResultText message text. When there is no suggestions are available at the time this message will be shown.


Default Value:
{:.param}



* "No suggestions"




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete emptyResultText property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,emptyResultText: 'No Results Found' });
</script>{% endhighlight %}




### enableAutoFill<span class="type-signature type boolean">boolean</span>
{:#members:enableautofill}




Automatically fills the first item from the suggestion list in an AutoComplete text box. The autoFill property is only applicable for &ldquo;startswith&rdquo; filterType type.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the enableAutoFill  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enableAutoFill : true });
</script>{% endhighlight %}




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




When this property sets to false, it disables the Autocomplete control.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the enabled  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enabled : false });
</script>{% endhighlight %}




### enableDistinct<span class="type-signature type boolean">boolean</span>
{:#members:enabledistinct}




Prevents the duplicate names presents in the search result.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the enableDistinct value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,enableDistinct: true });
</script>{% endhighlight %}




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Save current model value to browser cookies for state maintains. While refresh the Autocomplete control page retains the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the enablePersistence   value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enablePersistence  : true });
</script>{% endhighlight %}




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Sets the Autocomplete textbox direction as right to left alignment.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the enableRTL    value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,enableRTL   : true });
</script>{% endhighlight %}




### fields<span class="type-signature type object">object</span>
{:#members:fields}




Specifies mapping fields for the data items of the Autocomplete textbox.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>  
//To set fields API value during initialization         
        $("#autocomplete").ejAutocomplete({ dataSource:window.countriesField,fields: { text: "name", key: "key" }});
</script>{% endhighlight %}




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


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the filterType value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,filterType: 'contains'  });                                        
</script>{% endhighlight %}




### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}




Defines the height of the Autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete height property with the  value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList, height: 30 });
</script>{% endhighlight %}




### highlightSearch<span class="type-signature type boolean">boolean</span>
{:#members:highlightsearch}




Enables the highlight search option. When the highlightSearch option set to true, the corresponding string entered in the textbox is highlighted in the suggestion list.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the highlightSearch  value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList, highlightSearch : true });
</script>{% endhighlight %}




### itemsCount<span class="type-signature type number">number</span>
{:#members:itemscount}




Count of the item that gets displayed in the popup


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Count of the item that gets displayed in the popup
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,itemsCount : 2 });
</script>{% endhighlight %}




### minCharacter<span class="type-signature type number">number</span>
{:#members:mincharacter}




Minimum character that the autocomplete popup gets opened.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Minimum character that the autocomplete popup gets opened.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,minCharacter : 3 });
</script>{% endhighlight %}




### multiSelectMode<span class="type-signature type enum">enum</span>
{:#members:multiselectmode}




Allows to select multiple values from the suggestion list. Multiple values can be selected through either of the following options,Delimiter-Multiple values separated using comma.Visual mode- Each values are displayed in separate box with close button. See <a href="global.html#MultiSelectMode">MultiSelectMode</a>


Default Value:
{:.param}



* ej.MultiSelectMode.None




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the multiSelectMode value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,multiSelectMode: ej.MultiSelectMode.Delimiter  });                                         
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
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete popupHeight property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,popupHeight: '152px' });
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
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete popupWidth property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,popupWidth: '152px' });
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
<input type="text" id="autocomplete" /> 
 
<script>                   
//To set query API value during initialization  
var dataManger = ej.DataManager({       url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"});
var queryString = ej.Query().from("Suppliers").select("ContactName");
        $("#autocomplete").ejAutocomplete({ dataSource: dataManger, query: queryString, fields: { text: "ContactName" }});
</script>{% endhighlight %}




### readOnly<span class="type-signature type boolean">boolean</span>
{:#members:readonly}




Indicates that the autocomplete textbox values can only be read.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the readOnly value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,readOnly: true });
</script>{% endhighlight %}




### selectValueByKey
{:#members:selectvaluebykey}




Set the values to the Autocomplete textbox by input key value.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle,selectValueByKey:"a"});   
</script>{% endhighlight %}




### showEmptyResultText<span class="type-signature type boolean">boolean</span>
{:#members:showemptyresulttext}




Sets whether the noResults message will be shown or not.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the showEmptyResultText value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList, showEmptyResultText : false });
</script>{% endhighlight %}




### showLoadingIcon<span class="type-signature type boolean">boolean</span>
{:#members:showloadingicon}




Enables the loading icon to intimate the searching operation. The loading icon is visible when there is a time delay to perform the search.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the showLoadingIcon value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,showLoadingIcon: false });
</script>{% endhighlight %}




### showPopupButton<span class="type-signature type boolean">boolean</span>
{:#members:showpopupbutton}




Enables the showPopup button. When the Showpopup button clicks, it displays the full list from the dataSource.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the showPopupButton  value specified.
$("#autocomplete").ejAutocomplete({ dataSource: window.carList,showPopupButton : true });
</script>{% endhighlight %}




### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Autocomplete textbox to be displayed with rounded corner style.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the showRoundedCorner value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,showRoundedCorner: true });
</script>{% endhighlight %}




### sortOrder<span class="type-signature type enum">enum</span>
{:#members:sortorder}




Sort order specifies whether the suggestion list values has to display in ascending or descending order. See <a href="global.html#SortOrder">SortOrder</a>


Default Value:
{:.param}



* ej.SortOrder.Ascending




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the sortOrder value specified
        $("#autocomplete").ejAutocomplete({dataSource: window.carList,sortOrder:"descending" });                                        
</script>{% endhighlight %}




### template<span class="type-signature type string">string</span>
{:#members:template}




Specifies the template for Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// To set template API value during initialization.     
$("#autocomplete").ejAutocomplete({ dataSource: window.countries,template:"<div class='flag ${sprite}'> </div>"+"<div class='txt'> ${text} </div>"});
</script>{% endhighlight %}




### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}




Set the jquery validation error message in Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" name="autocomplete" /> 
 
<script>
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
</script>{% endhighlight %}




### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}




Set the jquery validation rules in Autocomplete.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" name="autocomplete" /> 
 
<script>
//To set validationRules API during initialization              
  $("#autocomplete").ejAutocomplete({ 
  dataSource: window.carList,                   
  validationRules:{                     
          required:true
        }
});
</script>{% endhighlight %}




### value<span class="type-signature type string">string</span>
{:#members:value}




Defines the default value to be displayed in the autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete value property with the  value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,value:"Elantra" });
</script>{% endhighlight %}




### visible<span class="type-signature type boolean">boolean</span>
{:#members:visible}




Specifies the to show or hide.


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Initialize the Autocomplete with the visible value specified.
$("#autocomplete").ejAutocomplete({dataSource: window.carList,visible: false });
</script>{% endhighlight %}




### watermarkText<span class="type-signature type string">string</span>
{:#members:watermarktext}




Sets the watermarkText text. When the textbox is empty the watermarkText text is visible like a shaded text.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete with the watermarkText value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,watermarkText: 'Enter the car name' });
</script>{% endhighlight %}




### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}




Defines the width of the Autocomplete textbox.


Default Value:
{:.param}



* Null




Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
//Initialize the Autocomplete width property with the width value specified
        $("#autocomplete").ejAutocomplete({ dataSource: window.carList,width: 200 });
</script>{% endhighlight %}



## Methods




### clearText<span class="signature">()</span>
{:#methods:cleartext}




Clears the text in the Autocomplete textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.clearText(); // clear the autocomplete text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Clears the text in the autocomplete
$('#autocomplete').ejAutocomplete("clearText");         
</script>{% endhighlight %}




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy in the Autocomplete textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.destroy(); // destroy the autocomplete 
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// destroys autocomplete
$('#autocomplete').ejAutocomplete("destroy");   
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the autocomplete



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.disable(); // disable the autocomplete
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Disables autocomplete
$('#autocomplete').ejAutocomplete("disable");   
</script>{% endhighlight %}




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the autocomplete



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});   
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.enable(); // enable the autocomplete
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});   
// Enables autocomplete
$('#autocomplete').ejAutocomplete("enable");    
</script>{% endhighlight %}




### getSelectedItems<span class="signature">()</span>
{:#methods:getselecteditems}




Returns the values selected in the Autocomplete textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.getSelectedItems(); // getSelectedItems the autocomplete text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Get the selected items in the autocomplete
$('#autocomplete').ejAutocomplete("getSelectedItems");  
</script>{% endhighlight %}




### getValue<span class="signature">()</span>
{:#methods:getvalue}




Returns the current value selected in the Autocomplete textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.getValue(); // getValue of the autocomplete text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"}); 
// Get the value of the selected item in the autocomplete
$('#autocomplete').ejAutocomplete("getValue");  
</script>{% endhighlight %}




### search<span class="signature">()</span>
{:#methods:search}




search values in the Autocomplete textbox.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.search(); // search the autocomplete text
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.carList,value:"Aston Martin"});
// Searches the item in the autocomplete
$('#autocomplete').ejAutocomplete("search");    
</script>{% endhighlight %}




### selectValueByKey<span class="signature">()</span>
{:#methods:selectvaluebykey}




Set the values to the Autocomplete textbox by input key value.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});   
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
  // set key value corresponding text to the autocomplete textbox
autocompleteObj.selectValueByKey("F"); 
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Create autocomplete
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});
$('#autocomplete').ejAutocomplete("selectValueByKey","F");  
</script>{% endhighlight %}




### selectValueByText<span class="signature">()</span>
{:#methods:selectvaluebytext}




Set the values to the Autocomplete textbox by input text value.



Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle});        
// Create autocomplete
var autocompleteObj  = $("#autocomplete").data("ejAutocomplete");
autocompleteObj.selectValueByText("BMW 7"); // set text value to the autocomplete textbox
</script>{% endhighlight %}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
// Create autocomplete
$('#autocomplete').ejAutocomplete({dataSource: window.vehicle}); 
$('#autocomplete').ejAutocomplete("selectValueByText","BMW 7");         
</script>{% endhighlight %}



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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//change event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        change: function(args) {}
});  
</script>                 {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Autocomplete model</td>
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
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//close event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        close: function(args) {}
}); 
</script>                  {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Autocomplete model</td>
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
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//create event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        create: function(args) {}
}); 
</script>                  {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Autocomplete model</td>
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
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//destroy event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        destroy: function(args) {}
}); 
</script>                  {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//focusIn event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        focusIn: function(args) {}
});      
</script>                 {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//focusOut event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        focusOut: function(args) {}
});  
</script>                                         {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Autocomplete model</td>
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
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//open event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        open: function(args) {}
}); 
</script>                  {% endhighlight %}




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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
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
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the selected text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.key{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the selected value key</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="text" id="autocomplete" /> 
 
<script>
$("#autocomplete").ejAutocomplete({ dataSource: window.carList});
//select event for Autocomplete
$("#autocomplete").ejAutocomplete({ 
        select: function(args) {}
}); 
</script>                 {% endhighlight %}



