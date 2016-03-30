---
layout: post
title: Backward-Compatibility - Version 13.3
description: backward compatibility - Version 13.3
platform: js
control: Introduction
documentation: ug
---

# Version 13.3 Changes

Significant changes are made to the API namings effective from Volume 3, 2015 release. The changes are documented with mapping between the old and new API names to enable quick upgradation of any control. To migrate from Volume 2, 2015 or from earlier versions to this Volume3, 2015, refer to the following API changes.

List of API changes are as follows,

## ejDatePicker

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
displayDefaultDate<br/><br/></td><td>
<br/><br/></td><td>
This property is removed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
fields: {  <br/>date: "date",    <br/>tooltip: "tooltip",     <br/>icon: "icon"     <br/>}      <br/><br/></td><td>
fields: {<br/>date: "date",<br/>tooltip: "tooltip",<br/>iconClass: "icon"<br/>}<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
Enum<br/><br/></td><td>
ej.DatePicker.Header = {<br/>ShowHeaderNone: "showheadernone",<br/>ShowHeaderShort: "showheadershort",<br/>ShowHeaderMin: "showheadermin",<br/>ShowHeaderLong: "showheaderlong"<br/>};<br/><br/></td><td>
ej.DatePicker.Header = {<br/>None: "none",<br/>Short: "short",<br/>Min: "min",<br/>Long: "long"<br/>};<br/><br/></td><td>
<br/><br/></td></tr>
</table>

## ejColorPicker

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Enum<br/><br/></td><td>
modelType:{<br/>default:”default”,<br/>picker:”picker”,<br/>palette:“palette”<br/>}<br/><br/></td><td>
modelType:{<br/>picker:”picker”,<br/>palette:“palette”<br/>}<br/><br/></td><td>
<br/><br/></td></tr>
</table>

## ejTreeview

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API  Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
fields.linkAttribute<br/><br/></td><td>
fields.linkAttribute<br/><br/></td><td>
Changed the type string to object.<br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
removeNode (node)<br/><br/></td><td>
removeNode(node)<br/><br/></td><td>
Previously, to remove a node from Treeview, you can call removeNode() without any argument that removes the current selected node in the Treeview.<br/>In supposed method, mention the node that has to be deleted and the argument is mandatory.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
addNode(“newnode”, $(“a”))<br/><br/></td><td>
addNode(“newnode”, $(“LI”))<br/>or<br/>addNode(“newnode”, “#node1”)<br/><br/></td><td>
Previously, you can pass “A” element or “LI” element as an argument, but now you can pass only “LI” element, as the ‘li’ element is considered as node always.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeDragStart <br/>- dragElement - dragged node info as json object<br/>- target - target element. “A” element.<br/><br/></td><td>
nodeDragStart<br/>- dragTarget- original element to be dragged. “A” element.<br/>- target – target Tree node<br/>- targetElementData - dragged node info as json object<br/>- parentElement – Current Parent<br/>- parentElementData – parent element details as json<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeDrag <br/>- dragElement - dragged node info as json object<br/>- target - drop target element<br/><br/></td><td>
nodeDrag<br/>- draggedElement - current dragged LI element<br/>- draggedElementData - dragged node info as json object<br/>- dragTarget – Original dragTarget element.<br/>- target– current target LI element<br/>- targetElementData - target node info as json object<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeDragStop <br/>- dragElement - dragged node info as json object<br/>- targetElement - target node info as json object<br/>- target - drop target element<br/><br/></td><td>
nodeDragStop  <br/>- draggedElement - current dragged LI element<br/>- draggedElementData - dragged node info as json object<br/>- target– current target LI element<br/>- targetElementData - target node info as json object<br/>- dropTarget – Original drop target element<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeDropped<br/>- dropedElement - dropped node info as json object<br/>- targetElement - target node info as json object<br/>- target - drop target element<br/>- dropPosition – position like over, before, after<br/><br/></td><td>
nodeDropped <br/>- droppedElement - current dragged LI element<br/>- droppedElementData- - dragged node info as json object<br/>- target– current target LI element<br/>- targetElementData - target node info as json object<br/>- dropTarget – Original drop target element<br/>- position – position like over, before, after<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
beforeExpand<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
beforeExpand<br/>- Id<br/>- text<br/><br/></td><td>
Event argument is changed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeSelect<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
nodeSelect<br/>- Id<br/>- text<br/><br/></td><td>
Event argument is changed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeExpand<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
nodeExpand<br/>- Id<br/>- text<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeCollapse<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
nodeCollapse<br/>- Id<br/>- text<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
inlineEditValidation<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
inlineEditValidation<br/>- Id<br/>- text<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeEdit<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
nodeEdit<br/>-Id<br/>- text<br/><br/></td><td>
<br/><br/></td></tr>
</table>

## ejFileExplorer

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API  Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
showLayout<br/><br/></td><td>
<br/><br/></td><td>
This property is removed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
gridSettings: {<br/>
          allowSearching: true <br/>
}
<br/><br/></td><td>
<br/><br/></td><td>
This property is removed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uploadBoxSettings: {       <br/>multipleFileSelection: true,<br/>fileSize: 31457280 <br/>}<br/><br/></td><td>
uploadSettings: {<br/>allowMultipleFile:true,<br/>maxFileSize: 31457280<br/>}<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
showTreeview<br/><br/></td><td>
showNavigationPane<br/><br/></td><td>
Deprecated showTreeview property.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
ajaxSettings: {<br/>destroy: {},<br/>getDetais: {}<br/>}<br/><br/></td><td>
ajaxSettings: {<br/>remove: {},<br/>getDetails: {}<br/>}<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
path<br/><br/></td><td>
path<br/><br/></td><td>
Previously, “path” API of file explorer returns current folder path. <br/>Now it points the root folder of file explorer.<br/><br/></td></tr>
<tr>
<td>
Method<br/><br/></td><td>
enableToolbarItem(FileExplorerId+toolbarCommand)<br/><br/></td><td>
enableToolbarItem(toolbarCommand)<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableToolbarItem(FileExplorerId+toolbarCommand)<br/><br/></td><td>
disableToolbarItem(toolbarCommand)<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
removeToolbarItem(FileExplorerId+toolbarCommand)<br/><br/></td><td>
removeToolbarItem(toolbarCommand)<br/><br/></td><td>
<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
move<br/><br/></td><td>
cut<br/><br/></td><td>
<br/><br/></td></tr>
</table>

## ejDropDownList

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API  Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
selectedItemIndex<br/><br/></td><td>
selectedIndex<br/><br/></td><td>
Renamed<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unselectItemByIndex<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by unselectedItemsByIndices.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItems<br/><br/></td><td>
selectedIndices<br/><br/></td><td>
Renamed<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowGrouping<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by setting fields.groupBy property.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableItemsByIndex<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by enableItemsByIndices method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItemsByIndex<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by disableItemsByIndices method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkAll<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by checkAll method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can achieve the same functionalities <br/>by uncheckAll method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowMultipleSelection<br/><br/></td><td>
<br/><br/></td><td>
Removed. You can achieve the same functionalities <br/>by multiSelectMode property.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
field.category<br/><br/></td><td>
field.groupBy<br/><br/></td><td>
“category” property deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableIncrementalSearch<br/><br/></td><td>
<br/><br/></td><td>
Default value is changed to True.<br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
setSelectedText<br/><br/></td><td>
selectItemByText<br/><br/></td><td>
Deprecated the old method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
setSelectedValue<br/><br/></td><td>
selectItemByValue<br/><br/></td><td>
Deprecated the old method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getSelectedItemsID<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can get the id of selected<br/>list items with the help of getSelectedItem method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectItemByIndex<br/><br/></td><td>
selectItemsByIndices<br/><br/></td><td>
Deprecated the old method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unselectItemByIndex<br/><br/></td><td>
unselectItemsByIndices<br/><br/></td><td>
Deprecated the old method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getValue<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. You can get the selected value<br/> by using value property.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableItemByIndex<br/><br/></td><td>enableItemsByIndices
<br/><br/></td><td>
Renamed <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItemByIndex<br/><br/></td><td>disableItemsByIndices
<br/><br/></td><td>
Renamed <br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
change<br/>- args.value<br/><br/></td><td>
change<br/>- args.selectedValue<br/><br/></td><td>
Renamed <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkChange<br/>- args.value<br/><br/></td><td>
checkChange<br/>- args.selectedValue<br/><br/></td><td>
Renamed <br/><br/></td></tr>
</table>

## ejRTE

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
customTool<br/><br/></td><td>
customTools<br/><br/></td><td>
customTool renamed as customTools.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
showHtmlSource: true<br/><br/></td><td>
showHtmlSource: false<br/><br/></td><td>
Default value is changed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
tools: {<br/>scripts: ["superscript", "subscript"],<br/>copyPaste: ["cut", "copy","paste"] ,<br/>links: ["createLink"]<br/>}<br/><br/></td><td>
tools: {<br/>effects: ["superscript", "subscript"],<br/>clipbpoard: ["cut", "copy","paste"],<br/>links: ["createLink","removeLink"],<br/>media:[“video”]       <br/>}<br/><br/></td><td>
Renamed the category header for tools.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
iframeAttribute<br/><br/></td><td>
iframeAttributes<br/><br/></td><td>
Now you can apply any kind of attributes to<br/>the iframe's body element by using this attribute.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
showClearAll:true<br/><br/></td><td>
showClearAll:false<br/><br/></td><td>
Default value is changed.<br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
enableToolbarItem(rteId+toolbarCommand)<br/><br/></td><td>
enableToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value is changed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableToolbarItem(rteId+toolbarCommand)<br/><br/></td><td>
disableToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value is changed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
removeToolbarItem(rteId+ toolbarCommand)<br/><br/></td><td>
removeToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value is changed.<br/><br/></td></tr>
</table>

## ejUploadBox

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
multipleFilesSelection: false<br/><br/></td><td>
multipleFilesSelection: true<br/><br/></td><td>
Default value of multipleFilesSelection property <br/>is changed to true.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
dragAreaText<br/><br/></td><td>
dropAreaText<br/><br/></td><td>
As per behavior, the property name is <br/>changed. It is breaking changes in upload.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
fileSelect<br/>- Args[0]<br/><br/></td><td>
fileSelect<br/>- args.files<br/><br/></td><td>
In fileSelect, the selected files are available in<br/>event argument - ‘args.files’.<br/><br/></td></tr>
</table>

## ejListbox

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Properties<br/><br/></td><td>
fields.toolTipText<br/><br/></td><td>
fields.tooltipText<br/><br/></td><td>
The toolTipText property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
fields.selected<br/><br/></td><td>
fields.selectBy<br/><br/></td><td>
The selected property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
fields.category<br/><br/></td><td>
fields.groupBy<br/><br/></td><td>
The category property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItemIndex<br/><br/></td><td>
selectedIndex<br/><br/></td><td>
The selectedItemIndex property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItemlist<br/><br/></td><td>
selectedIndices<br/><br/></td><td>
The selectedItemlist property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItems<br/><br/></td><td>
selectedIndices<br/><br/></td><td>
The selectedItemd property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The checkItemsByIndex property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkedItemlist<br/><br/></td><td>
checkedIndices<br/><br/></td><td>
The checkedItemlist property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkedItems<br/><br/></td><td>
checkedIndices<br/><br/></td><td>
The checkedItems property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkAll<br/><br/></td><td>
-<br/><br/></td><td>
The checkAll property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
-<br/><br/></td><td>
The uncheckAll property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The uncheckItemsByIndex property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableTooltip<br/><br/></td><td>
-<br/><br/></td><td>
The enableTooltip property is removed.<br/>Without this property itself, you can enable tooltip<br/>by specifying the data source field name in<br/>fieldSettings.tooltipText property. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowGrouping<br/><br/></td><td>
-<br/><br/></td><td>
The allowGrouping property is removed. <br/>Without this property itself, you can enable grouping <br/>by specifying the data source field name in <br/>fieldSettings.groupBy property. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowDragAndDrop<br/><br/></td><td>
-<br/><br/></td><td>
The allowDragAndDrop property is deprecated. <br/> This property is divided has two properties <br/>namely allowDrag and allowDrop.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The enableItemsByIndex property is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The disableItemsByIndex property is deprecated.<br/><br/></td></tr>
<tr>
<td>
Events<br/><br/></td><td>
selected<br/><br/></td><td>
select<br/><br/></td><td>
The selected event is deprecated. <br/>The event arguments has the following properties(changes).<br/>index: returns the item index.<br/>isChecked: returns whether the item is checked or not.<br/>isEnabled: returns whether the item is enabled or not.<br/>isSelected: returns whether the item is selected or not.<br/>item: returns the element(item).<br/>model: returns the current model.<br/>text: returns the item text(label).<br/>type: returns the event name.<br/>value: returns the item text.<br/>cancel: returns the cancel option value.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectIndexChanged<br/><br/></td><td>
change<br/><br/></td><td>
The selectIndexChanged event is deprecated. <br/>The event arguments has the following properties(changes).<br/>index: returns the item index.<br/>isChecked: returns whether the item is checked or not.<br/>isEnabled: returns whether the item is enabled or not.<br/>isSelected: returns whether the item is selected or not.<br/>item: returns the element(item).<br/>model: returns the current model.<br/>text: returns the item text(label).<br/>type: returns the event name.<br/>value: returns the item text.<br/>cancel: returns the cancel option value.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
itemDropped<br/><br/></td><td>
itemDrop<br/><br/></td><td>
The itemDropped event is deprecated. <br/>The event arguments has the following <br/>properties(changes).<br/>Items: returns the array of selected item objects.<br/>(to be dropped) that contains the properties like<br/>index, isChecked, isEnabled, isSelected, etc.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
itemRequest<br/><br/></td><td>
-<br/><br/></td><td>
This event is removed. Use actionSuccess or <br/>actionComplete event as an alternative event. <br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
getSelectedItem<br/><br/></td><td>
-<br/><br/></td><td>
This method is removed. Use<br/>getSelectedItems as an alternative method. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getSelectedItems<br/><br/></td><td>
<br/><br/></td><td>
This method’s return value is changed.<br/>It returns all the selected item’s object <br/> that contains properties like index, isChecked, <br/>text, value, item, etc instead of selected elements.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Checkitems<br/><br/></td><td>
-<br/><br/></td><td>
This method is removed.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItem<br/><br/></td><td>
-<br/><br/></td><td>
This method’s behavior is changed. <br/>Previously it disables the selected item.<br/>Now it takes item’s text (label) as an<br/>argument and disables that item.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
refreshContent<br/><br/></td><td>
refresh<br/><br/></td><td>
The refreshContent method is removed. <br/>Use refresh method as an alternative.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
addItem<br/><br/></td><td>
-<br/><br/></td><td>
This method’s behavior is changed.<br/>This method previously accepts only text to <br/>add an item in the ListBox widget. Now it <br/>accepts an object or an array of objects, or <br/>a string or an array of strings to add items.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
removeItem<br/><br/></td><td>
removeSelectedItems<br/><br/></td><td>
The removeItem method is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unCheckAll<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
The unCheckAll method is deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unSelectAll<br/><br/></td><td>
unselectAll<br/><br/></td><td>
The unSelectAll method is deprecated.<br/><br/></td></tr>
</table>

## ejDialog

<table>
<tr>
<td>
Member Type<br/><br/></td><td>
Old API Name<br/><br/></td><td>
New API Name<br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
Property<br/><br/></td><td>
content<br/><br/></td><td>
target<br/><br/></td><td>
The content property is deprecated. Use target property.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
Close<br/><br/></td><td>
close<br/><br/></td><td>
The Close event is deprecated. Use close event.<br/><br/></td></tr>
<tr>
<td>
Method<br/><br/></td><td>
isOpened<br/><br/></td><td>
isOpen<br/><br/></td><td>
The isOpened method is deprecated. Use isOpen method.<br/><br/></td></tr>
</table>

## ejSchedule

<table>
<tr>
<td>
Type<br/><br/></td><td>
Old<br/><br/></td><td>
New <br/><br/></td><td>
Comments<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
highlightBusinessHours : true,<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
The highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime are grouped respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
businessStartHour: 9<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
The highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime are grouped respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
businessEndHour: 18<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
The highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime are grouped respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
timezoneCollection : {<br/>}<br/><br/></td><td>
timeZoneCollection : {<br/><br/>}<br/><br/></td><td>
The API is changed to unique and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.cellIndex,<br/>args.currentDate,<br/>args.resources,<br/>args. events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
While opening the context menu on cell right click, pass the cell index and details.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.appointment,            <br/>args.cancel,<br/>args. events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
While opening the context menu on Appointment right click, pass the appointment details.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
actionBegin:function(args) {<br/>args. currentview,<br/>args.Date,<br/>}<br/><br/></td><td>
actionBegin:function(args) {<br/>args. data. currentView,<br/>args. data. currentDate,<br/>}<br/><br/></td><td>
The arguments are changed to unique and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
navigation:function(args) {<br/>args. currentview,<br/>args.Date,<br/>}<br/><br/></td><td>
navigation:function(args) {<br/>args. currentView,<br/>args. currentDate,<br/>}<br/><br/></td><td>
The arguments are changed to unique <br/>and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
actionComplete:function(args) {<br/>args. preview,<br/>args.Date,<br/>args. prevDate<br/>}<br/><br/></td><td>
actionComplete:function(args) {<br/>args. data.previousView,<br/>args. data.currentDate,<br/>args. data.previousDate<br/>}<br/><br/></td><td>
The arguments are changed to unique and standard format.<br/><br/></td></tr>
</table>