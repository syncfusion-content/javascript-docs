---
layout: post
title: State Persistence with Grid widget for Syncfusion Essential JS
description: How to persist grid state across page refresh
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
---
# State Persistence 

State Persistence is to maintain the grid state in browser's [local storage](https://www.w3schools.com/html/html5_webstorage.asp) even if browser refresh or move to next page. State persistence stores Grid's model object in local storage while defining [`enablePersistence`](https://help.syncfusion.com/api/js/ejgrid#members:enablepersistence) as true. 

I>  [local storage](https://www.w3schools.com/html/html5_webstorage.asp) is not supported below IE9 then grid state persistence technique is fallback to [cookie](https://www.w3schools.com/js/js_cookies.asp).

## List of properties are not Persisted by default

The following properties are not included while maintaining Grid state in local storage to keep localStorage compact.

* Query
* isEdit
* toolbarClick
* queryCellInfo
* mergeCellInfo
* currentViewData
* enableAltRow
* enableRTL 
* contextClick 
* contextOpen
* rowDataBound
* rowTemplate
* detailsDataBound
* detailsTemplate
* childGrid 
* summaryRows 
* toolbarSettings
* editSettings
* allowMultiSorting 
* enableAutoSaveOnSelectionChange 
* locale 
* allowScrolling 
* allowCellMerging
* allowTextWrap 
* cssClass 
* dataSource 
* groupSettings.enableDropAreaAnimation 
* enableRowHover 
* showSummary 
* allowGrouping
* enableHeaderHover 
* allowKeyboardNavigation 
* scrollSettings.frozenRows 
* scrollSettings.frozenColumns 
* enableTouch 
* editSettings.rowPosition 
* editSettings.showAddNewRow 
* contextMenuSettings.enableContextMenu

I> The given excluded properties can be included in persist state using `_ignoreOnPersist` in grid prototype. 



## Accessing currently stored state

Persisted state can be accessed through local storage using corresponding key name. Key name is the combination of plugin name and control id.

{% highlight javascript %}
var gridStateString = window.localStorage.ejGridGrid; // grid state as string

var gridStateObject = JSON.parse(window.localStorage.ejGridGrid);//grid state as object

{% endhighlight %}


I> In the above example, "ejGrid" is plugin name and "Grid" is control id.        

