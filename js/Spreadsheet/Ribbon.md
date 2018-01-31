---
layout: post
title: Ribbon
description: ribbon
platform: js
control: Spreadsheet
documentation: ug
api: /api/js/ejspreadsheet
---

# Ribbon

A ribbon is a command bar that organizes a spreadsheet's features into a series of tabs at the top of the control.

## Ribbon Customization

You can perform the Ribbon customization in the following two ways.

1) Initial Load

2) Methods


## Initial Load

The Ribbon customization can be done at Initial load by using [`ribbonSettings`](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings "ribbonSettings") API. In ribbonSettings `applicationTab` options is available for ribbon customization.


# Application Tab

To set application tab in Spreadsheet, [`applicationTab`](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings-applicationtab  "applicationTab") property is used. The following options are available in `applicationTab` settings.
   
   * [`type`](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings-applicationtab-type  "type") is used to set application tab type in Spreadsheet.
   * [`menuSettings `](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings-applicationtab-menusettings  "menuSettings ") is used to indicate menu settings for application tab in Spreadsheet. The following options are available in menuSettings.
            
        1) [`isAppend`](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings-applicationtab-menusettings-isappend  "isAppend ") is used to enable or disable isAppend property in ribbon settings.
        
        2) [`dataSource`](https://help.syncfusion.com/api/js/ejspreadsheet#members:ribbonsettings-applicationtab-menusettings-datasource  "dataSource ") is used to specify the data source to append in application tab.



## Methods

You can also customize the ribbon by using the following methods.

<table>
    <colgroup><col width="180px" /></colgroup>
    <tr><th>Feature</br></th><th>Method Name</br></th><th>Description</br></th></tr>
    <tr><td>Add BackStage Item</br></td><td>{{'[`addBackStageItem`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addbackstageitem  "addBackStageItem")'| markdownify }}</br></td><td>To add a new item in the backstage.</br></td></tr>
    <tr><td>Add Contextual Tabs</br></td><td>{{'[`addContextualTabs`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addcontextualtabs  "addContextualTabs")'| markdownify }}</br></td><td>To add the contextual tabs in the ribbon.</br></td></tr>
    <tr><td>Add Menu Item </br></td><td>{{'[`addMenuItem `](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addmenuitem  "addMenuItem ")'| markdownify }}</br></td><td>To dynamically add the menu item in the file menu.</br></td></tr>
    <tr><td>Add Tab  </br></td><td>{{'[`addTab  `](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addtab  "addTab")'| markdownify }}</br></td><td>To dynamically add the tab in the ribbon.</br></td></tr>
    <tr><td>Add Tab Group  </br></td><td>{{'[`addTabGroup`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-addtabgroup  "addTabGroup")'| markdownify }}</br></td><td>To dynamically add the tab group in the ribbon.</br></td></tr>
    <tr><td>Auto Sum  </br></td><td>{{'[`autoSum  `](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-autosum  "autoSum")'| markdownify }}</br></td><td>To insert the few type (SUM, MAX, MIN, AVG, COUNT) of formulas in the selected range of cells in the Spreadsheet.</br></td></tr>
    <tr><td>Change Dimension</br></td><td>{{'[`changeDimension`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-changedimension  "changeDimension")'| markdownify }}</br></td><td>To change the dimensions for chart/picture.</br></td></tr>
    <tr><td>Disable Ribbon Items</br></td><td>{{'[`disableRibbonItems`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-disableribbonitems  "disableRibbonItems  ")'| markdownify }}</br></td><td>To disable ribbon items in the Spreadsheet.</br></td></tr>
    <tr><td>Enable Ribbon Items</br></td><td>{{'[`enableRibbonItems`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-enableribbonitems  "enableRibbonItems  ")'| markdownify }}</br></td><td>To enable ribbon items in the Spreadsheet.</br></td></tr>
    <tr><td>Hide Menu</br></td><td>{{'[`hideMenu  `](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-hidemenu  "hideMenu")'| markdownify }}</br></td><td>To hide the file menu in the ribbon tab.</br></td></tr>
    <tr><td>Remove BackStage Item</br></td><td>{{'[`removeBackStageItem`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-removebackstageitem  "removeBackStageItem  ")'| markdownify }}</br></td><td>To remove the item from the backstage in the Spreadsheet.</br></td></tr>
    <tr><td>Remove Menu Item</br></td><td>{{'[`removeMenuItem`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-removemenuitem  "removeMenuItem")'| markdownify }}</br></td><td>To remove the menu item from file menu in Spreadsheet.</br></td></tr>
    <tr><td>Remove Tab</br></td><td>{{'[`removeTab`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-removetab "removeTab")'| markdownify }}</br></td><td>To remove the tab from ribbon in the spreadsheet.</br></td></tr>
    <tr><td>Remove Tab Group</br></td><td>{{'[`removeTabGroup`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-removetabgroup "removeTabGroup")'| markdownify }}</br></td><td>To remove the tab group from ribbon in the Spreadsheet.</br></td></tr>
    <tr><td>Show Menu</br></td><td>{{'[`showMenu`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-showmenu "showMenu")'| markdownify }}</br></td><td>To show the file menu in the ribbon tab.</br></td></tr>
    <tr><td>Update Menu Item</br></td><td>{{'[`updateMenuItem`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-updatemenuitem "updateMenuItem")'| markdownify }}</br></td><td>To update the menu item in the file menu.</br></td></tr>
    <tr><td>Update Ribbon Icons</br></td><td>{{'[`updateRibbonIcons`](https://help.syncfusion.com/api/js/ejspreadsheet#methods:xlribbon-updateribbonicons "updateRibbonIcons")'| markdownify }}</br></td><td>To update the ribbon icons in the Spreadsheet.</br></td></tr>
</table>


