---
layout: post
title: How to section in Listview widget for Essential JS? 
description: How to section in Listview widget for Essential JS
documentation: ug
platform: js
keywords: How-to,ListView How-to
api : /api/js/ejListView
---

# How to?

## How to get the selected/checked values?

**Single selection**


Enable the property [PersistSelection](https://help.syncfusion.com/api/js/ejlistview#members:persistselection) in order to use selection in ListView. Then use the [getActiveItemText](https://help.syncfusion.com/api/js/ejlistview#methods:getactiveitemtext) method take the selected active text.

**Multiple selection**

For multi selection i.e. when using the [EnableCheckMark](https://help.syncfusion.com/api/js/ejlistview#members:enablecheckmark) property, we need to use the [getCheckedItemsText](https://help.syncfusion.com/api/js/ejlistview#methods:getcheckeditemstext) method to take all the checked items.
