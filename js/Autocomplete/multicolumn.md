---
layout: post
title: Multiple columns in AutoComplete widget for Essential JS
description: How to assign multiple column values into the AutoComplete suggestion items.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
---

# Multiple Columns

The Autocomplete allows list of data to be displayed in several columns and column collection can be defined and customized through the [MultiColumnSettings](http://help.syncfusion.com/js/api/ejautocomplete#members:multiColumnSettings) property.
 
In AutoComplete Multiple Column search is based on [stringFormat](http://help.syncfusion.com/js/api/ejautocomplete#members:multiColumnSettings-stringFormat) property which specifies column indices. 

N> [stringFormat](http://help.syncfusion.com/js/api/ejautocomplete#members:multiColumnSettings-stringFormat) as “{0} ({1}) ({2})” means search based on 0, 1 and 2 columns data.

<table><tr><th>Name</th><th>Description</th></tr>
<tr><td>multiColumnSettings.enable</td><td>Allow list of data to be displayed in several columns.</td></tr>
<tr><td>multiColumnSettings.showHeader</td><td>Allow header text to be displayed in corresponding columns.</td></tr>
<tr><td>multiColumnSettings.stringFormat</td><td>Displayed selected value and autocomplete search is based on mentioned column value specified in that format.</td></tr>
<tr><td>multiColumnSettings.columns</td><td>Field and Header Text collections can be defined and customized through this field.</td></tr>
<tr><td>multiColumnSettings.columns.field</td><td>Get or set a value that indicates to display the columns in the autocomplete mapping with column name of the dataSource. </td></tr>
<tr><td>multiColumnSettings.columns.headerText</td><td>Get or set a value that indicates to display the title of that particular column.</td></tr></table>


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
                        stringFormat:"{0} ({1}) ({2})",
                        columns:[
							{"field": "EmployeeID" , "headerText":"EmployeeID"},
							{"field": "FirstName" , "headerText":"FirstName"},
							{"field": "City" , "headerText":"City"}
						]                        
                    } });
        
        </script>
        


{% endhighlight %}



![AutoComplete-MultiColumn](multicolumn_images\multicolumn_img1.png)
