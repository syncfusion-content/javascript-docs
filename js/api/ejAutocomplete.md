$(element).ejAutocomplete()

Example

{% highlight html %}
<input type="text" id="autocomplete" /> <script> // Create AutoComplete $('#autocomplete').ejAutocomplete({ dataSource: window.carList,value:"Austin-Healey" }); </script>



{% endhighlight %}

Requires

* module:jQuery
* module:jquery.easing.1.3.js
* module:ej.core.js
* module:ej.data.js
* module:ej.autocomplete.js
* module:ej.scroller.js

Members

addNewText

Customize add new label text to be added in the autocomplete popup for the entered text when there are no suggestions for it. 

**Note****:** This property applicable only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode "")” property is set as “VisualMode” and “[AllowAddNew](http://help.syncfusion.com/js/api/ejautocomplete#members:allowaddnew "")” property is set as “true”.

**Default** **Value****:**  “Add New”****

__Example______

____{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ dataSource: window.carList, allowAddNew: true, addNewText: "Add New Car", multiSelectMode:"visualmode" });



{% endhighlight %}

allowAddNew

Allows new values to be added to the autocomplete input other than the values in the suggestion list. Normally, when there are no suggestions it will display “No suggestions” label in the popup.

**Note****:** This property will work only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode "")” is set as “VisualMode”

**Default** **Value****:** false****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ allowAddNew: true, multiSelectMode: "visualmode" });





{% endhighlight %}

allowSorting

Enables or disables the sorting of suggestion list item. The default sort order is ascending order. You customize sort order. See also SortOder

**Default** **Value****:** true****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ allowSorting: false });



{% endhighlight %}

autoFocus

To focus the items in the suggestion list when the popup is shown. By default first item will be focused. 

**Default** **Value****:** false****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ autoFocus: true });



{% endhighlight %}



caseSensitiveSearch

Enables or disables the case sensitive search.

**Default** **Value****:** false****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ caseSensitiveSearch: true });



{% endhighlight %}

cssClass

The root class for the **Autocomplete** textbox widget which helps in customizing its theme.

**Default** **Value****:** ””****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ cssClass: 'gradient-lime' });



{% endhighlight %}

dataSource

The data source contains the list of data for the suggestions list. It can be a string array or json array. 

**Default** **Value****:** null****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ dataSource: window.carList, value: "Austin-Healey" });



{% endhighlight %}



delaySuggestionTimeout

The time delay (in milliseconds) after which the suggestion popup will be shown.

**Default** **Value****:** 200****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({delaySuggestionTimeout: 500 });



{% endhighlight %}



delimiterChar

The special character which acts as a separator for the given words for multi-mode search i.e. the text after the delimiter are considered as a separate word or query for search operation. 

Note: 

1. This property applicable only when the “[MultiSelectMode](http://help.syncfusion.com/js/api/ejautocomplete#members:multiselectmode "")” set as “Delimiter”.
2. The delimiter string should have a single character and must be a symbol. 
3. Mostly the delimiter symbol is used as (comma ,) or (semi-colon ;) or any other special character.

**Default** **Value****:** ’,’****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({multiSelectMode: ej.MultiSelectMode.Delimiter, delimiterChar: ';' });





{% endhighlight %}



emptyResultText

The text to be displayed in the popup when there are no suggestions available for the entered text.

Note: This property applicable only when the __[showEmptyResultText](http://help.syncfusion.com/js/api/ejautocomplete#members:showemptyresulttext "")__ set as “true”

**Default** **Value****:** “No suggestions”

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({emptyResultText: 'No Results Found' });



{% endhighlight %}



enableAutoFill

Fills the autocomplete textbox with the first matched item from the suggestion list automatically based on the entered text when enabled. 

Note: This property works only when “[filterType](http://help.syncfusion.com/js/api/ejautocomplete#members:filtertype "")” is set as “startswith” 

**Default** **Value****:** false

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({enableAutoFill: true });



{% endhighlight %}



enabled

Enables or disables the **Autocomplete** textbox widget.

**Default** **Value****:** true

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({enabled: false });



{% endhighlight %}



enableDistinct

Enables or disables displaying the duplicate names present in the search result.

**Default** **Value****:** false

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ enableDistinct: true });



{% endhighlight %}



enablePersistence

Allows the current model values to be saved in local storage or browser cookies for state maintenance when it is set to true. While refreshing the page, it retains the model value from browser cookies or local storage.

__**Note**____**:**__ __[Local storage](http://www.w3schools.com/html/html5_webstorage.asp# "")__ __is__ __supported__ __only__ __in__ __Html5__ __supported__ __browsers____.__ __If__ __the__ __browsers__ __don’t__ __have__ __support__ __for__ __local__ __storage____,__ __browser__ __cookies__ __will__ __be__ __used__ __to__ __maintain__ __the__ __state____.__

**Default** **Value****:** false

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ enablePersistence: true });



{% endhighlight %}



enableRTL

Displays the Autocomplete widget’s content from right to left when enabled.

**Default** **Value****:** false

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({enableRTL: true });



{% endhighlight %}





fields

Mapping fields for the suggestion items of the **Autocomplete** textbox widget.

____<table>
<tr>
<td>
fields.category[Deprecated]<br/><br/></td><td>
Used to group the suggestion list items. <br/><br/>Note: Since this is deprecated, we suggest you to use fields.groupBy API.<br/><br/></td></tr>
<tr>
<td>
fields.groupBy<br/><br/></td><td>
Used to group the suggestion list items. <br/><br/></td></tr>
<tr>
<td>
fields.htmlAttributes<br/><br/></td><td>
Defines the html attributes such as id, class, styles for the item.<br/><br/></td></tr>
<tr>
<td>
fields.key<br/><br/></td><td>
Defines the specific field name which contains unique key values for the list items.<br/><br/></td></tr>
<tr>
<td>
fields.text<br/><br/></td><td>
Defines the specific field name in the data source to load the suggestion list with data.<br/><br/></td></tr>
</table>
__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ fields: { text: "name", key: "id" } });



{% endhighlight %}



filterType

Specifies the search filter type. There are several types of search filter available such as ‘startswith’, ‘contains’, ‘endswith’, ‘lessthan’, ‘lessthanorequal’, ‘greaterthan’, ‘greaterthanorequal’, ‘equal’, ‘notequal’. 

**Default** **Value****:******

* ej.filterType.StartsWith

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({filterType: 'contains' });



{% endhighlight %}



height

The height of the Autocomplete textbox.

**Default** **Value****:** Null****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({height: 30 });



{% endhighlight %}



highlightSearch

The search text can be highlighted in the AutoComplete suggestions list when enabled.

**Default** **Value****:** false****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ highlightSearch: true });



{% endhighlight %}



itemsCount

Number of items to be displayed in the suggestion list.

**Default** **Value****:** 0****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ itemsCount: 2 });



{% endhighlight %}



minCharacter

Minimum number of character to be entered in the Autocomplete textbox to show the suggestion list.

**Default** **Value****:** 1****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ minCharacter: 3 });



{% endhighlight %}



multiSelectMode

Enables or disables selecting multiple values from the suggestion list. Multiple values can be selected through either of the following options,

1. Delimiter - Multiple values separated using comma.
2. Visual mode - Each values are displayed in separate box with close button.

See [MultiSelectMode](http://help.syncfusion.com/js/api/global.html#MultiSelectMode "")

**Default** **Value****:******

* ej.MultiSelectMode.None

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ multiSelectMode: ej.MultiSelectMode.Delimiter });



{% endhighlight %}



popupHeight

The height of the suggestion list.

**Default** **Value****:** “152px”****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ popupHeight: '100px' });



{% endhighlight %}



popupWidth

The width of the suggestion list.

**Default** **Value****:** “auto”****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({popupWidth: '152px' });



{% endhighlight %}



query

The query to retrieve the data from the data source.

**Default** **Value****:** null****

__Example______

{% highlight javascript %}
var dataManger = ej.DataManager({ url: "http://mvc.syncfusion.com/Services/Northwnd.svc/" });

var query = ej.Query().from("Suppliers").select("ContactName");

$("#autocomplete").ejAutocomplete({ dataSource: dataManger, query: query, fields: { text: "ContactName" } });





{% endhighlight %}



readOnly

Indicates that the autocomplete textbox values can only be readable.

**Default** **Value****:******

* false

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({readOnly: true });



{% endhighlight %}





selectValueByKey (Deprecated)

Sets the value for the Autocomplete textbox based on the given input key value.

__Example______



{% highlight javascript %}
$('#autocomplete').ejAutocomplete({selectValueByKey: "15", fields: { text: "name", key: "key" } });



{% endhighlight %}

showEmptyResultText

Enables or disables showing the message when there are no suggestions for the entered text.

**Default** **Value****:******

* true

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ showEmptyResultText: false });



{% endhighlight %}



showLoadingIcon

Enables or disables the loading icon to intimate the searching operation. The loading icon is visible when there is a time delay to perform the search.

**Default** **Value****:******

* true

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ showLoadingIcon: false });



{% endhighlight %}



showPopupButton

Enables the showPopup button in autocomplete textbox. When the Showpopup button is clicked, it displays all the available data from the data source.

**Default** **Value****:******

* false

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ showPopupButton: true });



{% endhighlight %}





showRoundedCorner

Enables or disables rounded corner.

**Default** **Value****:******

* false

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ showRoundedCorner: true });



{% endhighlight %}





sortOrder

Sort order specifies whether the suggestion list values has to be displayed in ascending or descending order. See [SortOrder](http://help.syncfusion.com/js/api/global.html#SortOrder "")

**Default** **Value****:** ej.SortOrder.Ascending****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ sortOrder: ej.SortOrder.Decending });



{% endhighlight %}



template

The template to display the suggestion list items with customized appearance.

**Default** **Value****:** null****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ dataSource: window.mobileList, fields: { text: "pName" }, template: "<div><div class='product-text'>${pName}</div> <span class='product-quantity'> Quantity : ${quantity}</span></div>" });



{% endhighlight %}



validationMessage

The jQuery validation error message to be displayed on form validation.

**Default** **Value****:** null****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ validationRules: { required: true }, validationMessage: { required: "Enter some value" } });



{% endhighlight %}



validationRules

The jQuery validation rules for form validation.

**Default** **Value****:** null****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ validationRules: { required: true } });



{% endhighlight %}



value

The value to be displayed in the autocomplete textbox.

**Default** **Value****:** Null****

__Example______

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ value: "USA" });



{% endhighlight %}



visible

Enables or disables the visibility of the autocomplete textbox.

**Default** **Value****:** true****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ visible: false });



{% endhighlight %}



watermarkText

The text to be displayed when the value of the autocomplete textbox is empty.

**Default** **Value****:** Null****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ watermarkText: 'Enter the car name' });



{% endhighlight %}



width

The width of the Autocomplete textbox.

**Default** **Value****:** Null****

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({width: 200 });



{% endhighlight %}



Methods

clearText()

Clears the text in the Autocomplete textbox.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("clearText");



{% endhighlight %}



destroy()

Destroys the Autocomplete widget.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("destroy");



{% endhighlight %}



disable()

Disables the autocomplete widget.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("disable");



{% endhighlight %}



enable()

Enables the autocomplete widget.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("enable");



{% endhighlight %}





getSelectedItems()

Value of the autocomplete textbox.s from the Autocomplete textbox.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("getSelectedItems");



{% endhighlight %}



getValue()

Returns the current selected value from the Autocomplete textbox.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______





{% highlight javascript %}
$("#autocomplete").ejAutocomplete("getValue");



{% endhighlight %}

search()

Search the entered text and show it in the suggestion list if available.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______





{% highlight javascript %}
$("#autocomplete").ejAutocomplete("search");



{% endhighlight %}



open()

Open up the autocomplete suggestion popup with all list items.

__Note____:__ __This__ __method__ __does__ __not__ __accept__ __any__ __arguments____.__

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("open");



{% endhighlight %}



selectValueByKey(key)

Sets the value of the Autocomplete textbox based on the given key value.

<table>
<tr>
<td>
**Parameters**<br/><br/></td><td>
**Type**<br/><br/></td><td>
**Description**<br/><br/></td></tr>
<tr>
<td>
Key<br/><br/></td><td>
string<br/><br/></td><td>
The key value of the specific suggestion item.<br/><br/></td></tr>
</table>
__**Note**____**:**__ __This__ __method__ __accepts__ __string__ __as__ __an__ __argument____.______

__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("selectValueByKey","IND");



{% endhighlight %}



selectValueByText(text)

Sets the value of the Autocomplete textbox based on the given input text value.

<table>
<tr>
<td>
**Parameters**<br/><br/></td><td>
**Type**<br/><br/></td><td>
**Description**<br/><br/></td></tr>
<tr>
<td>
Text<br/><br/></td><td>
string<br/><br/></td><td>
The text (label) value of the specific suggestion item.<br/><br/></td></tr>
</table>
__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete("selectValueByText","India");



{% endhighlight %}

Events

actionSuccess

Triggers when the data requested from AJAX will get successfully loaded in the **Autocomplete** widget. 

__**Note**____**:**__ __It__ __internally__ __uses__ __jQuery__ __ajaxSuccess__ __event____.__ __For__ __details__ __refer__ __[here](http://api.jquery.com/ajaxsuccess/# "")____.______

Example

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({actionSuccess:function(arg){

//Action Success Code

} });





{% endhighlight %}

actionComplete

Triggers when the AJAX requests complete. The request may get failed or succeed.

__**Note**____**:**__ __It__ __internally__ __uses__ __jQuery__ __ajaxComplete__ __event____.__ __For__ __details__ __refer__ __[here](http://api.jquery.com/ajaxcomplete/# "")____.__

Example

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

actionComplete:function(arg){

//Action Complete Code

} 

});



{% endhighlight %}

actionFailure

Triggers when the data requested from AJAX get failed.

__**Note**____**:**__ __It__ __internally__ __uses__ __jQuery__ __ajaxError__ __event____.__ __For__ __details__ __refer__ __[here](http://api.jquery.com/ajaxerror/# "")____.______

Example

{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

actionFailure:function(arg){

//Action Failure Code

} 

});





{% endhighlight %}

change

Triggers when the text box value is changed.

<table>
<tr>
<th>
**Event** **Arguments******<br/><br/></th><th>
**Type******<br/><br/></th><th>
**Description******<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
Boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
Object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
String<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
<tr>
<td>
argument.value<br/><br/></td><td>
String<br/><br/></td><td>
Value of the autocomplete textbox.<br/><br/></td></tr>
</table>
__Example______







{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

change: function (argument) {

//do something

}

});        



{% endhighlight %}



close

Triggers after suggestion popup is closed.

<table>
<tr>
<th>
**Event** **Arguments******<br/><br/></th><th>
**Type******<br/><br/></th><th>
**Description******<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
Object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
String<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
</table>
__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({ 

close: function (argument) {

//do something

}

});





{% endhighlight %}

create

Triggers when Autocomplete widget is created.

<table>
<tr>
<th>
**Event** **Arguments******<br/><br/></th><th>
**Type******<br/><br/></th><th>
**Description******<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
</table>
__Example______







{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

create: function (argument) {

//do something

}

});



{% endhighlight %}



destroy

Triggers after the Autocomplete widget is destroyed.

<table>
<tr>
<th>
**Event** **Arguments******<br/><br/></th><th>
**Type******<br/><br/></th><th>
**Description******<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
</table>
__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

destroy: function (argument) {

//do something

}

});



{% endhighlight %}

focusIn

Triggers after the autocomplete textbox is focused.

<table>
<tr>
<th>
**Event** **Arguments******<br/><br/></th><th>
**Type******<br/><br/></th><th>
**Description******<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
<tr>
<td>
argument.value<br/><br/></td><td>
string<br/><br/></td><td>
Value of the autocomplete textbox.<br/><br/></td></tr>
</table>
__Example______





{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

focusIn: function (argument) {

//do something

}

});





{% endhighlight %}



focusOut

Triggers after the Autocomplete textbox gets out of the focus.

<table>
<tr>
<th>
Event Arguments****<br/><br/></th><th>
Type****<br/><br/></th><th>
Description****<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
<tr>
<td>
argument.value<br/><br/></td><td>
string<br/><br/></td><td>
Value of the autocomplete textbox.<br/><br/></td></tr>
</table>
__Example______





{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

focusOut: function (argument) {

//do something

}

});





{% endhighlight %}



open

Triggers after suggestion list is opened.

<table>
<tr>
<th>
Event Arguments****<br/><br/></th><th>
Type****<br/><br/></th><th>
Description****<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
</table>
__Example______



{% highlight javascript %}
$("#autocomplete").ejAutocomplete({            

open: function (argument) {

//do something

}

});



{% endhighlight %}

select

Triggers when an item has been selected from the suggestion list.

<table>
<tr>
<th>
Event Arguments****<br/><br/></th><th>
Type****<br/><br/></th><th>
Description****<br/><br/></th></tr>
<tr>
<td>
argument.cancel<br/><br/></td><td>
boolean<br/><br/></td><td>
Set this option to true to cancel the event.<br/><br/></td></tr>
<tr>
<td>
argument.model<br/><br/></td><td>
object<br/><br/></td><td>
Instance of the autocomplete model object.<br/><br/></td></tr>
<tr>
<td>
argument.type<br/><br/></td><td>
string<br/><br/></td><td>
Name of the event.<br/><br/></td></tr>
<tr>
<td>
argument.value<br/><br/></td><td>
string<br/><br/></td><td>
Value of the autocomplete textbox.<br/><br/></td></tr>
<tr>
<td>
argument.text<br/><br/></td><td>
string<br/><br/></td><td>
Text of the selected item.<br/><br/></td></tr>
<tr>
<td>
argument.key<br/><br/></td><td>
string<br/><br/></td><td>
Key of the selected item.<br/><br/></td></tr>
<tr>
<td>
arugment.Item<br/><br/></td><td>
object<br/><br/></td><td>
Data object of the selected item.<br/><br/></td></tr>
</table>
__Example______





{% highlight javascript %}
$("#autocomplete").ejAutocomplete({

select: function (argument) {

//do something

}

});





{% endhighlight %}



