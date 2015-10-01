---
layout: post
title: Backward-Compatibility - Version 13.3
description: backward compatibility - Version 13.3
platform: js
control: Introduction
documentation: ug
---

## Version 13.3 Changes

We have made significant changes to the API namings effective from Volume 3, 2015 release. We have documented the changes with mapping between the old and new API names to enable quick up gradation of any control. The users whoever needs to migrate from Volume 2, 2015 or from earlier versions to this Volume-3, 2015, needs to refer the below specified API changes,

List of API changes made for the components are as follows,

### ejDatePicker

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

### ejColorPicker

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

### ejTreeview

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
In before, if we want to remove a node from Treeview means, we can able to call removeNode() without any argument. It will remove current selected node in the Treeview.<br/>In supposed method, we should give, which node need to be deleted. The argument is mandatory.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
addNode(“newnode”, $(“a”))<br/><br/></td><td>
addNode(“newnode”, $(“LI”))<br/>or<br/>addNode(“newnode”, “#node1”)<br/><br/></td><td>
In before, we can able to pass “A” element or “LI” element as an argument but now we can able to pass only “LI” element because we all ways consider node as ‘li’ element.<br/><br/></td></tr>
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
Event argument is changed<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
nodeSelect<br/>- nodeId<br/>- nodeText<br/><br/></td><td>
nodeSelect<br/>- Id<br/>- text<br/><br/></td><td>
Event argument is changed<br/><br/></td></tr>
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

### ejFileExplorer

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
We have removed this property.<br/><br/></td></tr>
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
Deprecated showTreeview property<br/><br/></td></tr>
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
Previously, “path” API of file explorer returns current folder path. <br/>Now it points the root folder of file explorer<br/><br/></td></tr>
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

### ejDropDownList

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
Deprecated. The same functionalities can achieved <br/>by unselectedItemsByIndices<br/><br/></td></tr>
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
Deprecated. The same functionalities can be achieved <br/>by setting fields.groupBy property<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableItemsByIndex<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. The same functionality can achieved <br/>by enableItemsByIndices method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItemsByIndex<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. The same functionality can achieved <br/>by disableItemsByIndices method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkAll<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. The same functionality can achieved <br/>by checkAll method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. The same functionality can achieved <br/>by uncheckAll method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowMultipleSelection<br/><br/></td><td>
<br/><br/></td><td>
Removed. Same can be achieved <br/>by multiSelectMode property<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
field.category<br/><br/></td><td>
field.groupBy<br/><br/></td><td>
Property “category” deprecated.<br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
setSelectedText<br/><br/></td><td>
selectItemByText<br/><br/></td><td>
Deprecated the old method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
setSelectedValue<br/><br/></td><td>
selectItemByValue<br/><br/></td><td>
Deprecated the old method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getSelectedItemsID<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. We can get the id of selected<br/>list items with the help of getSelectedItem method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectItemByIndex<br/><br/></td><td>
selectItemsByIndices<br/><br/></td><td>
Deprecated the old method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unselectItemByIndex<br/><br/></td><td>
unselectItemsByIndices<br/><br/></td><td>
Deprecated the old method<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getValue<br/><br/></td><td>
<br/><br/></td><td>
Deprecated. We can get the selected value<br/>using value property.<br/><br/></td></tr>
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

### ejRTE

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
customTool renamed as customTools<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
showHtmlSource: true<br/><br/></td><td>
showHtmlSource: false<br/><br/></td><td>
Default value changed<br/><br/></td></tr>
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
Now we can apply any kind of attributes to<br/>the iframe's body element using this<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
showClearAll:true<br/><br/></td><td>
showClearAll:false<br/><br/></td><td>
Default value changed<br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
enableToolbarItem(rteId+toolbarCommand)<br/><br/></td><td>
enableToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value changed<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableToolbarItem(rteId+toolbarCommand)<br/><br/></td><td>
disableToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value changed<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
removeToolbarItem(rteId+ toolbarCommand)<br/><br/></td><td>
removeToolbarItem (toolbarCommand)<br/><br/></td><td>
Parameter attribute value changed<br/><br/></td></tr>
</table>

### ejUploadBox

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
As per behavior, the property name has been <br/>changed. It is breaking changes in upload.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
fileSelect<br/>- Args[0]<br/><br/></td><td>
fileSelect<br/>- args.files<br/><br/></td><td>
In fileSelect, the selected files will be available in<br/>event argument - ‘args.files’<br/><br/></td></tr>
</table>

### ejListbox

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
The property toolTipText has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
fields.selected<br/><br/></td><td>
fields.selectBy<br/><br/></td><td>
The property selected has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
fields.category<br/><br/></td><td>
fields.groupBy<br/><br/></td><td>
The property category has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItemIndex<br/><br/></td><td>
selectedIndex<br/><br/></td><td>
The property selectedItemIndex has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItemlist<br/><br/></td><td>
selectedIndices<br/><br/></td><td>
The property selectedItemlist has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectedItems<br/><br/></td><td>
selectedIndices<br/><br/></td><td>
The property selectedItemd has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The property checkItemsByIndex has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkedItemlist<br/><br/></td><td>
checkedIndices<br/><br/></td><td>
The property checkedItemlist has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkedItems<br/><br/></td><td>
checkedIndices<br/><br/></td><td>
The property checkedItems has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
checkAll<br/><br/></td><td>
-<br/><br/></td><td>
The property checkAll has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
-<br/><br/></td><td>
The property uncheckAll has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
uncheckItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The property uncheckItemsByIndex has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableTooltip<br/><br/></td><td>
-<br/><br/></td><td>
The property enableTooltip has been removed.<br/>Without this property itself, we can enable tooltip<br/>by specifying the data source field name in<br/>fieldSettings.tooltipText property. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowGrouping<br/><br/></td><td>
-<br/><br/></td><td>
The property allowGrouping has been removed. <br/>Without this property itself, we can enable grouping <br/>by specifying the data source field name in <br/>fieldSettings.groupBy property. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
allowDragAndDrop<br/><br/></td><td>
-<br/><br/></td><td>
The property allowDragAndDrop has been deprecated. <br/>We have separated this property as two properties <br/>namely allowDrag and allowDrop.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
enableItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The property enableItemsByIndex has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItemsByIndex<br/><br/></td><td>
-<br/><br/></td><td>
The property disableItemsByIndex has been deprecated.<br/><br/></td></tr>
<tr>
<td>
Events<br/><br/></td><td>
selected<br/><br/></td><td>
select<br/><br/></td><td>
The event selected has been deprecated. <br/>The event arguments contains the following properties (changes).<br/>index: returns the item index<br/>isChecked: returns whether the item is checked or not.<br/>isEnabled: returns whether the item is checked or not.<br/>isSelected: returns whether the item is selected or not.<br/>item: returns the element (item)<br/>model: returns the current model<br/>text: returns the item text (label)<br/>type: returns the event name<br/>value: returns the item text<br/>cancel: returns the cancel option value.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
selectIndexChanged<br/><br/></td><td>
change<br/><br/></td><td>
The event selectIndexChanged has been deprecated. <br/>The event arguments contains the following properties (changes).<br/>index: returns the item index<br/>isChecked: returns whether the item is checked or not.<br/>isEnabled: returns whether the item is checked or not.<br/>isSelected: returns whether the item is selected or not.<br/>item: returns the element (item)<br/>model: returns the current model<br/>text: returns the item text (label)<br/>type: returns the event name<br/>value: returns the item text<br/>cancel: returns the cancel option value.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
itemDropped<br/><br/></td><td>
itemDrop<br/><br/></td><td>
The event itemDropped has been deprecated. <br/>The event arguments contains the following <br/>properties (changes).<br/>Items: returns the array of selected item objects<br/>(to be dropped) which contains the properties like<br/>index, isChecked, isEnabled, isSelected, etc.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
itemRequest<br/><br/></td><td>
-<br/><br/></td><td>
We have removed this event. Use actionSuccess or <br/>actionComplete event as an alternative event. <br/><br/></td></tr>
<tr>
<td>
Methods<br/><br/></td><td>
getSelectedItem<br/><br/></td><td>
-<br/><br/></td><td>
This method has been removed. Since we can use<br/>getSelectedItems as an alternative method. <br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
getSelectedItems<br/><br/></td><td>
<br/><br/></td><td>
This method’s return value has been changed.<br/>It will return all the selected item’s object <br/>(contains properties like index, isChecked, <br/>text, value, item, etc.) instead of selected elements.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Checkitems<br/><br/></td><td>
-<br/><br/></td><td>
We have removed this method.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
disableItem<br/><br/></td><td>
-<br/><br/></td><td>
This method’s behavior has been changed. <br/>Previously it disables the selected item.<br/>But now it takes item’s text (label) as an<br/>argument and disables that item.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
refreshContent<br/><br/></td><td>
refresh<br/><br/></td><td>
The method refreshContent has been removed. <br/>Use refresh method as an alternative.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
addItem<br/><br/></td><td>
-<br/><br/></td><td>
This method’s behavior has been changed.<br/>This method previously accepts only text to <br/>add an item in the ListBox widget. Now it <br/>accepts an object or an array of objects or <br/>a string or an array of strings to add items.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
removeItem<br/><br/></td><td>
removeSelectedItems<br/><br/></td><td>
The method removeItem has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unCheckAll<br/><br/></td><td>
uncheckAll<br/><br/></td><td>
The method unCheckAll has been deprecated.<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
unSelectAll<br/><br/></td><td>
unselectAll<br/><br/></td><td>
The method unSelectAll has been deprecated.<br/><br/></td></tr>
</table>

### ejDialog

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
The property content has been deprecated. Use target property.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
Close<br/><br/></td><td>
close<br/><br/></td><td>
The event Close has been deprecated. Use close event. <br/><br/></td></tr>
<tr>
<td>
Method<br/><br/></td><td>
isOpened<br/><br/></td><td>
isOpen<br/><br/></td><td>
The method isOpened has been deprecated. Use isOpen method.<br/><br/></td></tr>
</table>

### ejSchedule

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
views: ["Day", "Week", "WorkWeek", "Month"]<br/><br/></td><td>
views: ["Day", "Week", "WorkWeek", "Month", "Agenda"]<br/><br/></td><td>
We have added new view type for Agenda view.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
<br/><br/></td><td>
agendaViewSettings: {<br/>daysInAgenda: 7,<br/>dateColumnTemplateId: null,<br/>timeColumnTemplateId: null,<br/>},<br/><br/></td><td>
daysInAgenda -  In Agenda View by default <br/>display one week appointment summary, suppose <br/>customer want to display the more than one <br/>week(10,days, 2 week, etc.) so we can<br/>give the days count.<br/><br/>dateColumnTemplateId – To assign template <br/>design to the date column in the agenda view.<br/><br/>timeColumnTemplateId – To assign template<br/>design to the time column in the agenda view.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
<br/><br/></td><td>
firstDayOfWeek:null<br/><br/></td><td>
To changing starting day of the week, <br/>workweek and month view given day.<br/>firstDayOfWeek : “Monday”<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
<br/><br/></td><td>
workweek:[]<br/><br/></td><td>
We are customize the workweek view days  <br/>workweek: [“Monday”,”Tuesday”,”Wednesday”,”Thursday”<br/>,”Friday”,”Saturday”]<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
<br/><br/></td><td>
tooltipSettings:{<br/>enable: false,<br/>template: null <br/>},<br/><br/></td><td>
For Tool tip feature. The tooltip allows to show<br/>appointment details. To enable and disable <br/>tooltip and customize the tooltip with help of template<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
highlightBusinessHours : true,<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
We have grouped the highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
businessStartHour: 9<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
We have grouped the highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
businessEndHour: 18<br/><br/></td><td>
workHours:{<br/>highlight:true,<br/>start:9,<br/>end:18<br/>}<br/><br/></td><td>
We have grouped the highlighrBusinessHours, <br/>businessHourStartTime and <br/>businessHourEndTime respectively.<br/><br/></td></tr>
<tr>
<td>
API<br/><br/></td><td>
timezoneCollection : {<br/>}<br/><br/></td><td>
timeZoneCollection : {<br/><br/>}<br/><br/></td><td>
We have changed the API in unique and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.cellIndex,<br/>args.currentDate,<br/>args.resources,<br/>args. events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
While open the context menu on cell right click. Pass the cell index and details.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.cancel,<br/>args.events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
beforeContextMenuOpen:function(args){<br/>args.appointment,            <br/>args.cancel,<br/>args. events,<br/>args.model,<br/>args.type<br/>}<br/><br/></td><td>
While open the context menu on Appointment right click. Pass the appointment details.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
actionBegin:function(args) {<br/>args. currentview,<br/>args.Date,<br/>}<br/><br/></td><td>
actionBegin:function(args) {<br/>args. data. currentView,<br/>args. data. currentDate,<br/>}<br/><br/></td><td>
We have changed the arguments in unique and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
navigation:function(args) {<br/>args. currentview,<br/>args.Date,<br/>}<br/><br/></td><td>
navigation:function(args) {<br/>args. currentView,<br/>args. currentDate,<br/>}<br/><br/></td><td>
We have changed the arguments in unique <br/>and standard format.<br/><br/></td></tr>
<tr>
<td>
Event<br/><br/></td><td>
actionComplete:function(args) {<br/>args. preview,<br/>args.Date,<br/>args. prevDate<br/>}<br/><br/></td><td>
actionComplete:function(args) {<br/>args. data.previousView,<br/>args. data.currentDate,<br/>args. data.previousDate<br/>}<br/><br/></td><td>
We have changed the arguments in unique and standard format.<br/><br/></td></tr>
</table>