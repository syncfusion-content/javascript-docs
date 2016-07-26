---
layout: post
title: Properties,Methods and Events of Essential JS ejAutocomplete Widget
description: Methods, members, events available in ejAutocomplete
documentation: API
platform: js
keywords: ejAutocomplete, API, Essential JS Autocomplete 
---

# ejAutocomplete

The AutoComplete control is a textbox control that provides a list of suggestions based on the user query.When the users enters the text in the text box, the control performs a search operation and provides a list of results in the suggestion pop up. There are several filter types available to perform the search.

#### Syntax

{% highlight javascript %}
		
	$(element).ejAutocomplete()

{% endhighlight %}

#### Example

{% highlight html %}
		
	<input type="text" id="autocomplete" /> 
	<script> 
	// Create AutoComplete 
	$('#autocomplete').ejAutocomplete({ 
		dataSource: window.carList,value:"Austin-Healey" 
	}); 
	</script>

{% endhighlight %}

#### Requires

* module:jQuery

* module:jquery.easing.1.3.js

* module:ej.core.js

* module:ej.data.js

* module:ej.autocomplete.js

* module:ej.scroller.js

## Members

### addNewText `Boolean`
{:#members:addnewtext}

Customize "Add New" text (label) to be added in the autocomplete popup list for the entered text when there are no suggestions for it. 

N> This property is applicable only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode)” property is set as “VisualMode” and “[AllowAddNew](http://help.syncfusion.com/js/api/ejautocomplete#members:allowaddnew)” property is set as “true”.

#### Default Value:

* "Add New"

#### Example

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		dataSource: window.carList, 
		allowAddNew: true, 
		addNewText: "Add New Car", 
		multiSelectMode:"visualmode" 
	});

{% endhighlight %}

### allowAddNew `Boolean`
{:#members:allowaddnew}

Allows new values to be added to the autocomplete input other than the values in the suggestion list. Normally, when there are no suggestions it will display “No suggestions” label in the popup.

N>  This property will work only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode)” property is set as “VisualMode”

#### Default Value: 
* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		allowAddNew: true, 
		multiSelectMode: "visualmode" 
	});

{% endhighlight %}

### allowSorting `Boolean`
{:#members:allowsorting}

Enables or disables the sorting of suggestion list item. The default sort order is ascending order. You customize sort order. 

{%seealso%} [SortOrder](http://help.syncfusion.com/js/api/global.html#SortOrder) {%endseealso%}

#### Default Value: 

* true

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		allowSorting: false 
	});

{% endhighlight %}

### animateType `Enum`
{:#members:animateType}

<ts name = "ej.Autocomplete.Animation"/>

Enables or disables selecting the animation style for the popup list. Animation types can be selected through either of the following options,

<table>
<tr>
<th>Name<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>none<br/><br/></td>
<td>Supports to animation type with none type only.<br/><br/></td>
</tr>
<tr>
<td>slide<br/><br/></td>
<td>Supports to animation type with slide type only.<br/><br/></td>
</tr>
<tr>
<td>fade<br/><br/></td>
<td>Supports to animation type with fade type only.<br/><br/></td>
</tr>
</table>

#### Default Value: 

* slide

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		animateType: "fade" 
	});

{% endhighlight %}

### autoFocus `Boolean`
{:#members:autofocus}

To focus the items in the suggestion list when the popup is shown. By default first item will be focused. 

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		autoFocus: true 
	});

{% endhighlight %}

### caseSensitiveSearch `Boolean`
{:#members:casesensitivesearch}

Enables or disables the case sensitive search.

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		caseSensitiveSearch: true 
	});

{% endhighlight %}

### cssClass `String`
{:#members:cssclass}

The root class for the **Autocomplete** textbox widget which helps in customizing its theme.

#### Default Value: 

* ””

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		cssClass: 'gradient-lime' 
	});

{% endhighlight %}

### dataSource `object|array`
{:#members:datasource}

The data source contains the list of data for the suggestions list. It can be a string array or JSON array. 

#### Default Value: 

* null

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		dataSource: window.carList, 
		value: "Austin-Healey" 
	});

{% endhighlight %}

### delaySuggestionTimeout `Number`
{:#members:delaysuggestiontimeout}

The time delay (in milliseconds) after which the suggestion popup will be shown.

#### Default Value: 

* 200

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		delaySuggestionTimeout: 500 
	});

{% endhighlight %}

### delimiterChar `String`
{:#members:delimiterchar}

The special character which acts as a separator for the given words for multi-mode search i.e. the text after the delimiter are considered as a separate word or query for search operation. 

N> 1. This property is applicable only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode)” property set as “Delimiter”.
N> 2. The delimiter string should have a single character and must be a symbol. 
N> 3. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.

#### Default Value: 

* ’,’

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		multiSelectMode: ej.MultiSelectMode.Delimiter, 
		delimiterChar: ';' 
	});

{% endhighlight %}

### emptyResultText `String`
{:#members:emptyresulttext}

The text to be displayed in the popup when there are no suggestions available for the entered text.

N> This property is applicable only when the [showEmptyResultText](http://help.syncfusion.com/js/api/ejautocomplete#members:showemptyresulttext) property set as “true”

#### Default Value: 

* “No suggestions”

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		emptyResultText: 'No Results Found' 
	});

{% endhighlight %}

### enableAutoFill `Boolean`
{:#members:enableautofill}

Fills the autocomplete textbox with the first matched item from the suggestion list automatically based on the entered text when enabled. 

N> This property works only when “[filterType](http://help.syncfusion.com/js/api/ejautocomplete#members:filtertype)” property is set as “startswith” 

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		enableAutoFill: true 
	});

{% endhighlight %}

### enabled `Boolean`
{:#members:enabled}

Enables or disables the **Autocomplete** textbox widget.

#### Default Value: 

* true

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		enabled: false
	});

{% endhighlight %}

### enableDistinct `Boolean`
{:#members:enabledistinct}

Enables or disables displaying the duplicate names present in the search result.

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		enableDistinct: true 
	});

{% endhighlight %}

### enablePersistence `Boolean`
{:#members:enablepersistence}

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true. While refreshing the page, it retains the model value from browser cookies or local storage.

N> [Local storage](http://www.w3schools.com/html/html5_webstorage.asp#) is supported only in Html5 supported browsers. If the browsers don’t have support for local storage, browser cookies will be used to maintain the state.

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		enablePersistence: true 
	});

{% endhighlight %}

### enableRTL `Boolean`
{:#members:enablertl}

Displays the Autocomplete widget’s content from right to left when enabled.

#### Default Value: 

* false

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		enableRTL: true 
	});

{% endhighlight %}

### fields `object`
{:#members:fields}

Mapping fields for the suggestion items of the **Autocomplete** textbox widget.

#### Default Value:

* null

<table>
<tr>
<th>Name<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>
fields.groupBy<br/><br/></td><td>
Used to group the suggestion list items. <br/><br/></td>
</tr>
<tr>
<td>fields.htmlAttributes<br/><br/></td>
<td>Defines the HTML attributes such as id, class, styles for the item.<br/><br/></td>
</tr>
<tr>
<td>fields.key<br/><br/></td>
<td>Defines the specific field name which contains unique key values for the list items.<br/><br/></td>
</tr>
<tr>
<td>fields.text<br/><br/></td>
<td>Defines the specific field name in the data source to load the suggestion list with data.<br/><br/></td>
</tr>
</table>

#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		fields: { 
			text: "name", 
			key: "id" 
		} 
	});

{% endhighlight %}


### filterType `String`
{:#members:filtertype}

Specifies the search filter type. There are several types of search filter available such as ‘startswith’, ‘contains’, ‘endswith’, ‘lessthan’, ‘lessthanorequal’, ‘greaterthan’, ‘greaterthanorequal’, ‘equal’, ‘notequal’. 

#### Default Value:  

* ej.filterType.StartsWith

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		filterType: 'contains' 
	});

{% endhighlight %}

### height `String`
{:#members:height}

The height of the Autocomplete textbox.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		height: 30 
	});

{% endhighlight %}

### highlightSearch `Boolean`
{:#members:highlightsearch}

The search text can be highlighted in the AutoComplete suggestion list when enabled.

#### Default Value:  

* false

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		highlightSearch: true 
	});

{% endhighlight %}

### itemsCount `Number`
{:#members:itemscount}

Number of items to be displayed in the suggestion list.

#### Default Value:  

* 0

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		itemsCount: 2 
	});

{% endhighlight %}

### minCharacter `Number`
{:#members:mincharacter}

Minimum number of character to be entered in the Autocomplete textbox to show the suggestion list.

#### Default Value:  

* 1

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		minCharacter: 3 
	});

{% endhighlight %}

### multiColumnSettings `object`
{:#members:multicolumnsettings}

An **Autocomplete** column collection can be defined and customized through the multiColumnSettings property.
Column's header, field, and stringFormat can be define via multiColumnSettings properties.


#### Example 

{% highlight javascript %}

    $("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
	enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.enable `boolean`
{:#members:multicolumnsettings-enable}

Allow list of data to be displayed in several columns.

#### Default Value:

* false


#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.showHeader `boolean`
{:#members:multicolumnsettings-showHeader}

Allow header text to be displayed in corresponding columns.

#### Default Value:

* true


#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.stringFormat `string`
{:#members:multicolumnsettings-stringFormat}

Displayed selected value and autocomplete search based on mentioned column value specified in that format.

N> stringFormat as “{0} ({1}) ({2})” means search based on 0, 1 and 2 columns data.



#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.columns `array`
{:#members:multicolumnsettings-columns}

Field and Header Text collections can be defined and customized through columns field.


#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.columns.field `string`
{:#members:multicolumnsettings-columns-field}

Get or set a value that indicates to display the columns in the autocomplete mapping with column name of the dataSource. 


#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiColumnSettings.columns.headerText `string`
{:#members:multicolumnsettings-columns-headerText}

Get or set a value that indicates to display the title of that particular column.


#### Example 

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
    multiColumnSettings: {
    enable: true,
    showHeader: true,
    stringFormat: "{0} ({1})",
    columns: [{
    field:"name", 
    headerText: "Name"
    },{
    field: "id" ,
    headerText:"ID"
    }]
    }
	});

{% endhighlight %}

### multiSelectMode `Enum`
{:#members:multiselectmode}

<ts name = "ej.Autocomplete.MultiSelectMode"/>

Enables or disables selecting multiple values from the suggestion list. Multiple values can be selected through either of the following options,

<table>
<tr>
<th>Name<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>Delimiter<br/><br/></td>
<td>Multiple values are separated using a given special character.<br/><br/></td>
</tr>
<tr>
<td>VisualMode<br/><br/></td>
<td>Each values are displayed in separate box with close button.<br/><br/></td>
</tr>
</table>


{%seealso%} [MultiSelectMode](http://help.syncfusion.com/js/api/global.html#MultiSelectMode) {%endseealso%}

#### Default Value:  

* ej.MultiSelectMode.None

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		multiSelectMode: ej.MultiSelectMode.Delimiter 
	});

{% endhighlight %}

### popupHeight `String`
{:#members:popupheight}

The height of the suggestion list.

#### Default Value:  

* “152px”

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		popupHeight: '100px' 
	});

{% endhighlight %}

### popupWidth `String`
{:#members:popupwidth}

The width of the suggestion list.

#### Default Value:  

* “auto”

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		popupWidth: '152px' 
	});

{% endhighlight %}

### query `ej.Query`
{:#members:query}

The query to retrieve the data from the data source.

#### Default Value:   

* null

#### Example  

{% highlight javascript %}

	var dataManger = ej.DataManager({ 
		url: "http://mvc.syncfusion.com/Services/Northwnd.svc/" 
	});
	
	var query = ej.Query().from("Suppliers").select("ContactName");
	
	$("#autocomplete").ejAutocomplete({ 
		dataSource: dataManger, 
		query: query, 
		fields: { 
			text: "ContactName" 
		}
	});

{% endhighlight %}

### readOnly `Boolean`
{:#members:readonly}

Indicates that the autocomplete textbox values can only be readable.

#### Default Value:  

* false

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		readOnly: true 
	});

{% endhighlight %}

### selectValueByKey `Number`
{:#members:selectvaluebykey}

Sets the value for the Autocomplete textbox based on the given input key value.

#### Example  

{% highlight javascript %}

	$('#autocomplete').ejAutocomplete({
		selectValueByKey: "15", 
		fields: { 
			text: "name", 
			key: "key" 
		} 
	});

{% endhighlight %}

### showEmptyResultText `Boolean`
{:#members:showemptyresulttext}

Enables or disables showing the message when there are no suggestions for the entered text.

#### Default Value:  

* true

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		showEmptyResultText: false 
	});

{% endhighlight %}

### showLoadingIcon `Boolean`
{:#members:showloadingicon}

Enables or disables the loading icon to intimate the searching operation. The loading icon is visible when there is a time delay to perform the search.

#### Default Value:  

* true

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		showLoadingIcon: false 
	});

{% endhighlight %}

### showPopupButton `Boolean`
{:#members:showpopupbutton}

Enables the showPopup button in autocomplete textbox. When the showPopup button is clicked, it displays all the available data from the data source.

#### Default Value:  

* false

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		showPopupButton: true 
	});

{% endhighlight %}

### showRoundedCorner `Boolean`
{:#members:showroundedcorner}

Enables or disables rounded corner.

#### Default Value:  

* false

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		showRoundedCorner: true 
	});

{% endhighlight %}

### showResetIcon `Boolean`
{:#members:showreseticon}

Enables or disables reset icon to clear the textbox values.

#### Default Value:  

* false

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		showResetIcon: true 
	});

{% endhighlight %}

### sortOrder `Enum`
{:#members:sortorder}

<ts name = "ej.Autocomplete.SortOrder"/>

Sort order specifies whether the suggestion list values has to be displayed in ascending or descending order. 

<table>
<tr>
<th>Name<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>Ascending<br/><br/></td>
<td>Items to be displayed in the suggestion list in ascending order.<br/><br/></td>
</tr>
<tr>
<td>Descending<br/><br/></td>
<td>Items to be displayed in the suggestion list in descending order.<br/><br/></td>
</tr>
</table>

{%seealso%} [SortOrder](http://help.syncfusion.com/js/api/global.html#SortOrder) {%endseealso%}

#### Default Value:  

* ej.SortOrder.Ascending

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		sortOrder: ej.SortOrder.Decending 
	});

{% endhighlight %}

### template `String`
{:#members:template}

The template to display the suggestion list items with customized appearance.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		dataSource: window.mobileList, 
		fields: { 
			text: "pName" 
		}, 
		template: "<div><div class='product-text'>${pName}</div> <span class='product-quantity'> Quantity : ${quantity}</span></div>" 
	});

{% endhighlight %}

### validationMessage `Object`
{:#members:validationmessage}

The jQuery validation error message to be displayed on form validation.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		validationRules: { 
			required: true 
		}, 
		validationMessage: { 
			required: "Enter some value" 
		} 
	});

{% endhighlight %}

### validationRules `Object`
{:#members:validationrules}

The jQuery validation rules for form validation.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		validationRules: { 
			required: true 
		} 
	});

{% endhighlight %}

### value `String`
{:#members:value}

The value to be displayed in the autocomplete textbox.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		value: "USA" 
	});

{% endhighlight %}

### visible `Boolean`
{:#members:visible}

Enables or disables the visibility of the autocomplete textbox.

#### Default Value:  

* true

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		visible: false 
	});

{% endhighlight %}

### watermarkText `String`
{:#members:watermarktext}

The text to be displayed when the value of the autocomplete textbox is empty.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		watermarkText: 'Enter the car name' 
	});

{% endhighlight %}

### width `String`
{:#members:width}

The width of the Autocomplete textbox.

#### Default Value:  

* null

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		width: 200 
	});

{% endhighlight %}

## Methods

### clearText()
{:#methods:cleartext}

Clears the text in the Autocomplete textbox.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("clearText");

{% endhighlight %}

### destroy()
{:#methods:destroy}

Destroys the Autocomplete widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("destroy");

{% endhighlight %}

### disable()
{:#methods:disable}

Disables the autocomplete widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("disable");

{% endhighlight %}

### enable()
{:#methods:enable}

Enables the autocomplete widget.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("enable");

{% endhighlight %}

### getSelectedItems()
{:#methods:getselecteditems}

Returns objects (data object) of all the selected items in the autocomplete textbox.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("getSelectedItems");

{% endhighlight %}

### getValue()
{:#methods:getvalue}

Returns the current selected value from the Autocomplete textbox.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("getValue");

{% endhighlight %}

### getActiveText()
{:#methods:getactivetext}

Returns the current active text value in the Autocomplete suggestion list.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("getActiveText");

{% endhighlight %}


### search()
{:#methods:search}

Search the entered text and show it in the suggestion list if available.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("search");

{% endhighlight %}

### open()
{:#methods:open}

Open up the autocomplete suggestion popup with all list items.

N> This method does not accept any arguments.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("open");

{% endhighlight %}

### selectValueByKey(key)
{:#methods:selectvaluebykey}

Sets the value of the Autocomplete textbox based on the given key value.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>Key<br/><br/></td>
<td>string<br/><br/></td>
<td>The key value of the specific suggestion item.<br/><br/></td>
</tr>
</table>

 N>  This method accepts string as an argument.

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("selectValueByKey","IND");

{% endhighlight %}

### selectValueByText(text)
{:#methods:selectvaluebytext}

Sets the value of the Autocomplete textbox based on the given input text value.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>Text<br/><br/></td>
<td>string<br/><br/></td>
<td>The text (label) value of the specific suggestion item.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete("selectValueByText","India");

{% endhighlight %}

## Events

### actionBegin
{:#events:actionBegin}
Triggers when the AJAX requests Begins.

 N>  It internally uses jQuery ajaxStart event. For details refer [here](http://api.jquery.com/ajaxStart/#).

#### Example

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		actionBegin:function(arg){
			//Action Success Code
		} 
	});

{% endhighlight %}

### actionSuccess
{:#events:actionsuccess}

Triggers when the data requested from AJAX will get successfully loaded in the **Autocomplete** widget. 

 N>  It internally uses jQuery ajaxSuccess event. For details refer [here](http://api.jquery.com/ajaxsuccess/#).

#### Example

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		actionSuccess:function(arg){
			//Action Success Code
		} 
	});

{% endhighlight %}

### actionComplete
{:#events:actioncomplete}

Triggers when the AJAX requests complete. The request may get failed or succeed.

N> It internally uses jQuery ajaxComplete event. For details refer [here](http://api.jquery.com/ajaxcomplete/#).

#### Example

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		actionComplete:function(arg){
			//Action Complete Code
		} 
	});

{% endhighlight %}

### actionFailure
{:#events:actionfailure}

Triggers when the data requested from AJAX get failed.

 N>  It internally uses jQuery ajaxError event. For details refer [here](http://api.jquery.com/ajaxerror/#).

#### Example

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		actionFailure:function(arg){
			//Action Failure Code
		} 
	});

{% endhighlight %}

### change
{:#events:change}

Triggers when the text box value is changed.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>Boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>Object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>String<br/><br/></td>
<td>Value of the autocomplete textbox.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		change: function (argument) {
			//do something
		}
	}); 

{% endhighlight %}

### close
{:#events:close}

Triggers after the suggestion popup is closed.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>Object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>String<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({ 
		close: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### create
{:#events:create}

Triggers when Autocomplete widget is created.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		create: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### destroy
{:#events:destroy}

Triggers after the Autocomplete widget is destroyed.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		destroy: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### focusIn
{:#events:focusin}

Triggers after the autocomplete textbox is focused.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>string<br/><br/></td>
<td>Value of the autocomplete textbox.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		focusIn: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### focusOut
{:#events:focusout}

Triggers after the Autocomplete textbox gets out of the focus.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>string<br/><br/></td>
<td>Value of the autocomplete textbox.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		focusOut: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### open
{:#events:open}

Triggers after the suggestion list is opened.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({  
		open: function (argument) {
			//do something
		}
	});

{% endhighlight %}

### select
{:#events:select}

Triggers when an item has been selected from the suggestion list.

<table>
<tr>
<th>Name<br/><br/></th>
<th>Type<br/><br/></th>
<th>Description<br/><br/></th>
</tr>
<tr>
<td>cancel<br/><br/></td>
<td>boolean<br/><br/></td>
<td>Set this option to true to cancel the event.<br/><br/></td>
</tr>
<tr>
<td>model<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Instance of the autocomplete model object.<br/><br/></td>
</tr>
<tr>
<td>type<br/><br/></td>
<td>string<br/><br/></td>
<td>Name of the event.<br/><br/></td>
</tr>
<tr>
<td>value<br/><br/></td>
<td>string<br/><br/></td>
<td>Value of the autocomplete textbox.<br/><br/></td>
</tr>
<tr>
<td>text<br/><br/></td>
<td>string<br/><br/></td>
<td>Text of the selected item.<br/><br/></td>
</tr>
<tr>
<td>key<br/><br/></td>
<td>string<br/><br/></td>
<td>Key of the selected item.<br/><br/></td
></tr>
<tr>
<td>Item<br/><br/></td>
<td><ts ref="ej.Autocomplete.Model"/>object<br/><br/></td>
<td>Data object of the selected item.<br/><br/></td>
</tr>
</table>

#### Example  

{% highlight javascript %}

	$("#autocomplete").ejAutocomplete({
		select: function (argument) {
			//do something
		}
	});

{% endhighlight %}