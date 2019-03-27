---
layout: post
title: Multiple columns in Syncfusion AutoComplete widget for Essential JS
description: How to assign multiple column values into the AutoComplete suggestion items.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
---

# Multiple Columns

The Autocomplete adds support for selecting multiple columns in the dropdown list. This multiple column options can be enabled and customized through the [MultiColumnSettings](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings) property.
 
In AutoComplete Multiple Column search is based on [searchColumnIndices](https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-searchColumnIndices) property which allows user to search text for any number of fields in the suggestion list without modifying the selected text format.

In AutoComplete Multiple Column searched value is updated to autocomplete input box based on [stringFormat](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings-stringFormat) property which specifies column indices values to  updated. 


<table><tr><th>Name</th><th>Description</th></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-enable">multiColumnSettings.enable</a></td><td>Allow list of data to be displayed in several columns.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-showheader">multiColumnSettings.showHeader</a></td><td>Allow header text to be displayed in corresponding columns.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-stringformat">multiColumnSettings.stringFormat</a></td><td>Specifies the format for displaying a selected value and columns to be searched.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns">multiColumnSettings.columns</a></td><td>Field and Header Text collections can be defined and customized through this field.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-field">multiColumnSettings.columns.field</a></td><td>Field to be mapped from the dataSource to the columns in Autocomplete suggestion list.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-headertext">multiColumnSettings.columns.headerText</a></td><td>Get or set a value that indicates to display the title of that particular column.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-cssclass">multiColumnSettings.columns.cssClass</a></td><td>Field to be mapped for to add user defined CSS class for the specific column.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-type">multiColumnSettings.columns.type</a></td><td>Get or set the data type for a individual column.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-filtertype">multiColumnSettings.columns.filterType</a></td><td>Get or set the search filter type for the column.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-headertextalign">multiColumnSettings.columns.headerTextAlign</a></td><td>Used to align or position the header value in the column.</td></tr>
<tr><td><a href="https://help.syncfusion.com/api/js/ejautocomplete#members:multicolumnsettings-columns-textalign">multiColumnSettings.columns.textAlign</a></td><td>Used to align or position all the values in a column.</td></tr>
</table>


## Example 
{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Local Data */
                var carList = [
            { "EmployeeID": 1, "FirstName": "Nancy" ,"City": "Seattle" },
            { "EmployeeID": 10, "FirstName": "Laura",  "City": "Seattle" },
            { "EmployeeID": 11,  "FirstName": "Janet",  "City": "Kirkland" },
            { "EmployeeID": 12,  "FirstName": "Michael", "City": "London" },
            { "EmployeeID": 13,  "FirstName": "Steven",  "City": "London"},
            { "EmployeeID": 14,  "FirstName": "Andrew","City": "Tacoma" },
            { "EmployeeID": 15,  "FirstName": "Robert", "City": "London" },
            { "EmployeeID": 16,  "FirstName": "Margaret",  "City": "Redmond" },
            { "EmployeeID": 17,  "FirstName": "Steven",  "City": "London" },
            { "EmployeeID": 18,  "FirstName": "Michael",  "City": "London" },
            { "EmployeeID": 19,  "FirstName": "Robert",  "City": "London"}, ];
        
                $('#autocomplete').ejAutocomplete({ 
                    dataSource: carList, 
                    width: 400, 
                    multiColumnSettings:{
                        enable:true,
                        showHeader:true,
                        stringFormat:"{0}",
                        searchColumnIndices:[0,1,2],
                        columns:[
							{"field": "EmployeeID" , "headerText":"EmployeeID"},
							{"field": "FirstName" , "headerText":"FirstName"},
							{"field": "City" , "headerText":"City"}
						]                        
                    } });
        
        </script>
        


{% endhighlight %}

N> Here [stringFormat](https://help.syncfusion.com/api/js/ejautocomplete#members:multiColumnSettings-stringFormat) is “{0} ({1}) ({2})” so the search will be based on column indices 0, 1 and 2. When using `MultiColumnSettings` in AutoComplete, the value will be returned in string format based on the multiple columns. You can retrieve any specific field like text or key field through `e.item` in the select event.


![AutoComplete-MultiColumn](multicolumn_images\multicolumn_img1.png)

[Live demo](https://js.syncfusion.com/demos/web/#!/bootstrap/autocomplete/multicolumn)
