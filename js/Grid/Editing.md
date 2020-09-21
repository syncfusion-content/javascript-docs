---
layout: post
title: Editing with Grid widget for Syncfusion Essential JS
description: How to perform editing and configure edit time functionalities like edit type, edit time controls etc
platform: js
control: Grid
documentation: ug
api: /api/js/ejgrid
--- 
# Editing in JavaScript Grid

The grid control has support for the dynamic insertion, updating and deletion of records. You can start the edit action either by double clicking the particular row or by selecting the required row and clicking on Edit icon in toolbar. Similarly, you can add new record to grid either by clicking on insert icon in toolbar or on an external button which is bound to call [`addRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:addrecord "addRecord") method of grid.  `Save` and `Cancel` while on edit mode is possible using respective toolbar icon in grid.

Deletion of the record is possible by selecting the required row and clicking on Delete icon in toolbar. 

By default edit action is enabled while double click on the record.To prevent this behavior, set [`editSettings.allowEditOnDblClick `](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-alloweditondblclick "editSettings.allowEditOnDblClick ") property as `false`.

The primary key for the data source should be defined in [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") definition, for editing to work properly. In [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") definition, particular primary column's [`isPrimaryKey`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isprimarykey "isPrimaryKey") property should be set to `true`. Refer to the Knowledge base [link](http://www.syncfusion.com/kb/2675/cant-edit-any-row-except-the-first-row-in-grid# "link") for more information.

N> 1. In grid, the primary key column will be automatically set to read only while editing the row, but you can specify primary key column value while adding a new record.

N> 2. The column which is specified as [`isIdentity`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isidentity "isIdentity") will be in readonly mode both while editing and adding a record. Also, auto incremented value is assigned to that [`isIdentity`](https://help.syncfusion.com/api/js/ejgrid#members:columns-isidentity "isIdentity") column.

N> 3. To get the primarykey field name, use [`getPrimaryKeyFieldNames`](https://help.syncfusion.com/api/js/ejgrid#methods:getprimarykeyfieldnames "getPrimaryKeyFieldNames") method.


Default behavior of Grid editing (i.e auto save the edit action on row selection changed) which can be modified by setting [`enableAutoSaveOnSelectionChange `](https://help.syncfusion.com/api/js/ejgrid#members:enableautosaveonselectionchange "enableAutoSaveOnSelectionChange ") property as `false`.

## Toolbar with edit option

Using toolbar which is rendered at the top of the grid header, you can show all the CRUD related action. To enable toolbar and toolbar items, set [`showToolbar`](https://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-showtoolbar "showToolbar") property as true and [`toolbarItems`](https://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems "toolbarItems"). The default toolbar items are `Add`, `Edit`, `Delete`, `Update` and `Cancel`.

N> For [`toolbarItems`](https://help.syncfusion.com/api/js/ejgrid#members:toolbarsettings-toolbaritems "toolbarItems") property you can assign either `string` value ("add") or `enum` value (`ej.Grid.ToolBarItems.Add`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {	
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData, 
		toolbarSettings : {	showToolbar : true, toolbarItems : ["add", "edit", "delete", "update", "cancel"] },
		editSettings : { allowEditing: true, allowAdding: true, allowDeleting: true},
		allowPaging : true,
		columns : [
					{ field: "OrderID", isPrimaryKey: true },
					{ field: "CustomerID" },
					{ field: "EmployeeID" },
					{ field: "ShipCity" },
					{ field: "ShipCountry" }
				]
		});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Toolbar with edit option in Javascript grid](Editing_images/Editing_img1.png)


## Cell edit type and its params

The edit type of bound column can be customized using [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). The following Essential JavaScript controls are supported built-in by [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType"). You can set the [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType") based on specific data type of the column. 

* [`CheckBox`](https://help.syncfusion.com/api/js/ejcheckbox# "CheckBox") control for boolean data type.
* [`NumericTextBox`](https://help.syncfusion.com/api/js/ejtextboxes# "NumericTextBox") control for integers, double, and decimal data types.
* `InputTextBox` control for string data type.
* [`DatePicker`](https://help.syncfusion.com/api/js/ejdatepicker# "DatePicker") control for date data type.
* [`DateTimePicker`](https://help.syncfusion.com/api/js/ejdatetimepicker# "DateTimePicker") control for date-time data type.
* [`DropDownList`](https://help.syncfusion.com/api/js/ejdropdownlist# "DropDownList") control for list of data type.



And also you can define the model for all the editTypes controls while editing through [`editParams`](https://help.syncfusion.com/api/js/ejgrid#members:columns-editparams "editParams") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns").

The following table describes [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType") and their corresponding [`editParams`](https://help.syncfusion.com/api/js/ejgrid#members:columns-editparams "editParams") of the specific data type of the column.

<table>
<tr>
<th>
EditControl</th><th>
EditType</th><th>
EditParams</th><th>
Example</th></tr>
<tr>
<td>
CheckBox</td><td>
Boolean</td><td>
{{ '[ejCheckBox](https://help.syncfusion.com/api/js/ejcheckbox)' | markdownify }} </td><td>
editParams: { checked: true }</td></tr>
<tr>
<td>
NumericTextBox </td><td>
Numeric</td><td>
{{ '[ejTextBoxes](https://help.syncfusion.com/api/js/ejtextboxes)' | markdownify }} </td><td>
editParams: { decimalPlaces: 2, value:5  }</td></tr>
<tr>
<td>
InputTextBox </td><td>
String</td><td>
-</td><td>
-</td></tr>
<tr>
<td>
DatePicker </td><td>
DatePicker</td><td>
{{ '[ejDatePicker](https://help.syncfusion.com/api/js/ejdatepicker)' | markdownify }} </td><td>
editParams: {  buttonText : "Now" }</td></tr>
<tr>
<td>
DateTimePicker</td><td>
DateTimePicker</td><td>
{{ '[ejDateTimePicker](https://help.syncfusion.com/api/js/ejdatetimepicker)' | markdownify }} </td><td>
editParams: {  enabled: true }</td></tr>
<tr>
<td>
DropDownList</td><td>
Dropdown</td><td>
{{ '[ejDropDownList](https://help.syncfusion.com/api/js/ejdropdownlist)' | markdownify }} </td><td>
editParams: {  allowGrouping: true }</td></tr>

</table>

N> 1. If [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType") is not set, then by default it will display the input element ("stringedit") while editing a column.

N> 2. For [`editType`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittype "editType") property you can assign either `string` value ("numericedit") or `enum` value (`ej.Grid.EditingType.Numeric`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : { showToolbar : true, toolbarItems : ["add", "edit", "delete", "update", "cancel"] },
		editSettings:{ allowEditing: true, allowAdding: true, allowDeleting: true},
		allowPaging : true,
		columns : [
					{ field: "OrderID", isPrimaryKey: true },
					{ field: "CustomerID", editType: "stringedit" },
					{ field: "Freight", editType: "numericedit", editParams: { decimalPlaces: 2 } },
					{ field: "ShipCity", editType: "dropdownedit", editParams: { enableAnimation: true } },
					{ field: "ShipCountry" },
					{ field: "OrderDate", editType: "datepicker", format: "{0:MM/dd/yyyy}", editParams: { buttonText: "Now" } },
					{ field: "Verified", editType: "booleanedit", editParams: { showRoundedCorner: true } }
			]
		});
	});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Cell edit type and its params in Javascript grid](Editing_images/Editing_img2.png)


## Cell Edit Template

On editing the column values, custom editor can be created by using the [`editTemplate`](https://help.syncfusion.com/api/js/ejgrid#members:columns-edittemplate "editTemplate") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). It has three functions, they are

1. `create` - It is used to create the control at time of initializing.
2. `read` - It is used to read the input value at time of saving.
3. `write` - It is used to assign the value to control at time of editing.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : { showToolbar : true, toolbarItems : ["add", "edit", "delete", "update", "cancel"] },
		editSettings:{ allowEditing: true, allowAdding: true, allowDeleting: true},
		allowPaging : true,
		columns : [
					{ field: "OrderID", isPrimaryKey: true },
					{ field: "CustomerID" },
					{ field: "Freight" },
					{ field: "ShipCountry" },
					{
						field : "ShipPostalCode",
					editTemplate : {
					create : function () {
							return "<input>";
					},
					read : function (args) {
						return args.ejMaskEdit("get_UnstrippedValue");
					},
					write : function (args) {
						args.element.ejMaskEdit({
						maskFormat : "99-99-9999",
						value : args.rowdata["ShipPostalCode"]
						});
					}
				}
			}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Cell edit template in Javascript grid](Editing_images/Editing_img3.png)


## Edit Modes

### Inline 

Set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as `normal`, then the row itself is changed as edited row.

N> For [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") property you can assign either `string` value ("normal") or `enum` value (`ej.Grid.EditMode.Normal`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "normal"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate",editType: "datepicker", format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Editing](Editing_images/Editing_img4.png)


### Inline Form

Set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as `inlineform`, then edit form will be inserted next to the row which is to be edited.

N> For [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") property you can assign either `string` value ("normal") or `enum` value (`ej.Grid.EditMode.Normal`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "inlineform"
		},		
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate",editType: "datepicker", format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Inline Form  of editing in Javascript grid](Editing_images/Editing_img5.png)


### Inline Template Form

You can edit any of the fields pertaining to a single record of data and apply it to a template so that the same format is applied to all the other records that you may edit later.

Using this template support, you can edit the fields that are not bound to grid columns.

To edit the records using Inline template form, set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as `inlineformtemplate` and specify the template ID to [`editSettings.inlineFormTemplateID`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-inlineformtemplateid "editSettings.inlineFormTemplateID") property.

While using template form, you can change the HTML elements to appropriate JS controls based on the column type. This can be achieved by using [`actionComplete`](https://help.syncfusion.com/api/js/ejgrid#events:actioncomplete "actionComplete") event of grid.

N> 1. `value` attribute is used to bind the corresponding field value while editing.

N> 2. `name` attribute is used to get the changed field values while saving the edited record.

N> 3.  It's a standard way to enclose the `template` within the `script` tag with `type` as "text/x-jsrender".

N> 4.  For [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") property you can assign either `string` value ("inlineformtemplate") or `enum` value (`ej.Grid.EditMode.InlineTemplateForm`) 

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="template" type="text/template">
   <table cellspacing="10">
		<tr>
			<td>Order ID</td>
			<td>
				<input id="OrderID" name="OrderID" disabled="disabled" value="{{"{{"}}:OrderID{{}}}}" />
			</td>
			<td>Customer ID</td>
			<td>
				<input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" class="e-field e-ejinputtext" style="width: 116px; height: 28px" />
			</td>
		</tr>
		<tr>
			<td>Employee ID</td>
			<td>
				<input type="text" id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" />
			</td>
			<td>Ship City</td>
			<td>
				<select id="ShipCity" name="ShipCity">
					<option value="Argentina">Argentina</option>
					<option value="Austria">Austria</option>
					<option value="Belgium">Belgium</option>
					<option value="Brazil">Brazil</option>
					<option value="Canada">Canada</option>
					<option value="Denmark">Denmark</option>
				</select>
			</td>
		</tr>
   </table>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "inlineformtemplate",
			inlineFormTemplateID : "#template"
		},		
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity" }
		],
		actionComplete : "complete"
	});
});

function complete(args) {
	$("#EmployeeID").ejNumericTextbox();
	$("#Freight").ejNumericTextbox();
	$("#ShipCity").ejDropDownList();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Inline Template Form  of editing before conversion in Javascript grid](Editing_images/Editing_img6.png)

{:caption}
Before the template elements are converted to JS controls


![Inline Template Form  of editing after conversion in Javascript grid](Editing_images/Editing_img7.png)
{:caption}
After the template elements are converted to JS controls using actionComplete event 


### Dialog

Set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as `dialog` to edit data using a dialog box, which displays the fields associated with the data record being edited.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "dialog"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate",editType: "datepicker", format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Dialog edit mode in Javascript grid](Editing_images/Editing_img8.png)

N> Use [`titleColumn`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-titleColumn "titleColumn") property of editSettings to change the the title for edit form apart from the primarykey column value.

### Dialog Template Form

You can edit any of the fields pertaining to a single record of data and apply it to a template so that the same format is applied to all the other records that you may edit later.

Using this template support, you can edit the fields that are not bound to grid columns.

To edit the records using Inline template form, set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as dialogtemplate and specify the template id to [`dialogEditorTemplateID`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-dialogeditortemplateid "dialogEditorTemplateID") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings").

While using template, you can change the elements that are defined in the `template`, to appropriate JS controls based on the column type. This can be achieved by using [`actionComplete`](https://help.syncfusion.com/api/js/ejgrid#events:actioncomplete "actionComplete") event of grid.

N> 1. `value` attribute is used to bind the corresponding field value while editing.
N> 2. `name` attribute is used to get the changed field values while save the edited record. 
N> 3. For [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") property you can assign either `string` value ("dialogtemplate") or `enum` value (`ej.Grid.EditMode.DialogTemplate`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="template" type="text/template">
   <table cellspacing="10">
		<tr>
			<td>Order ID</td>
			<td>
				<input id="OrderID" name="OrderID" disabled="disabled" value="{{"{{"}}:OrderID{{}}}}" class="e-field e-ejinputtext" style="width:116px;height:28px" />
            </td>
			<td>Customer ID</td>
			<td>
				<input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" class="e-field e-ejinputtext" style="width: 116px; height: 28px" />
			</td>
		</tr>
		<tr>
			<td>Employee ID</td>
			<td>
				<input type="text" id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" />
			</td>
			<td>Ship City</td>
			<td>
				<select id="ShipCity" name="ShipCity">
					<option value="Argentina">Argentina</option>
					<option value="Austria">Austria</option>
					<option value="Belgium">Belgium</option>
					<option value="Brazil">Brazil</option>
					<option value="Canada">Canada</option>
					<option value="Denmark">Denmark</option>
				</select>
			</td>
		</tr>
   </table>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "dialogtemplate",
			dialogEditorTemplateID : "#template"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity" }
		],
		actionComplete : "complete"
	});
});

function complete(args) {
	$("#EmployeeID").ejNumericTextbox();
	$("#Freight").ejNumericTextbox();
	$("#ShipCity").ejDropDownList();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Dialog Template Form of editing before conversion in Javascript grid](Editing_images/Editing_img9.png)
{:caption}
Before the template elements are converted to JS controls

![Dialog Template Form of editing after conversion in Javascript grid](Editing_images/Editing_img10.png)
{:caption}
After the template elements are converted to JS controls using actionComplete event 

### External Form

By setting the [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as externalform, the edit form is opened outside the grid content.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "externalform"
		},
		allowPaging : true,
		pageSettings : {
			pageSize : 7
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate", editType: "datepicker",format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![External Form of editing in Javascript grid](Editing_images/Editing_img11.png)


Form Position:

You can position an external edit form in the following two ways. 

1. Top-right
2. Bottom left

This can be achieved by setting the [`formPosition`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-formposition "formPosition") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings") as "topright" or "bottomleft".

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "externalform",
			formPosition : "topright"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Form Position of editing in Javascript grid](Editing_images/Editing_img12.png)


### External Template Form

You can edit any of the fields pertaining to a single record of data and apply it to a template so that the same format is applied to all the other records that you may edit later.

Using this template support, you can edit the fields that are not bound to grid columns.

To edit the records using External template form, set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as externalformtemplate and specify the template id to [`externalFormTemplateID`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-externalformtemplateid "externalFormTemplateID") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings").

While using template, you can change the elements that are defined in the template, to appropriate JS controls based on the column type. This can be achieved by using [`actionComplete`](https://help.syncfusion.com/api/js/ejgrid#events:actioncomplete "actionComplete") event of grid.

N> 1. `value` attribute is used to bind the corresponding field value while editing. 
N> 2. `name` attribute is used to get the changed field values while save the edited record. 
N> 3. For [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") property you can assign either `string` value ("externalformtemplate") or `enum` value (`ej.Grid.EditMode.ExternalFormTemplate`).

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
<script id="template" type="text/template">
<table cellspacing="10">
   <tr>
      <td>Order ID</td>
      <td>
         <input id="OrderID" name="OrderID" disabled="disabled" value="{{"{{"}}:OrderID{{}}}}" class="e-field e-ejinputtext" style="width:116px;height:28px" />           
      </td>
      <td>Customer ID</td>
      <td>
         <input id="CustomerID" name="CustomerID" value="{{"{{"}}:CustomerID{{}}}}" class="e-field e-ejinputtext" style="width: 116px; height: 28px" />
      </td>
   </tr>
   <tr>
      <td>Employee ID</td>
      <td>
         <input type="text" id="EmployeeID" name="EmployeeID" value="{{"{{"}}:EmployeeID{{}}}}" />
      </td>
      <td>Ship City</td>
      <td>
         <select id="ShipCity" name="ShipCity">
            <option value="Argentina">Argentina</option>
            <option value="Austria">Austria</option>
            <option value="Belgium">Belgium</option>
            <option value="Brazil">Brazil</option>
            <option value="Canada">Canada</option>
            <option value="Denmark">Denmark</option>
         </select>
      </td>
   </tr>
</table>
</script>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "externalformtemplate",
			externalFormTemplateID : "#template"
		},
		allowPaging : true,
		pageSettings : {
			pageSize : 5
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity" }
		],
		actionComplete : "complete"
	});
});

function complete(args) {
	$("#EmployeeID").ejNumericTextbox();
	$("#Freight").ejNumericTextbox();
	$("#ShipCity").ejDropDownList();
}
{% endhighlight %}

The following output is displayed as a result of the above code example.

![External Template Form of editing before conversion in Javascript grid ](Editing_images/Editing_img13.png)
{:caption}
Before the template elements are converted to JS controls

![External Template Form of editing after conversion in Javascript grid](Editing_images/Editing_img14.png)
{:caption}
After the template elements are converted to JS controls using actionComplete event

### Batch / Excel-like

Users can start editing by clicking a cell and typing data into it. Edited cell will be marked while navigating to next cell or any other row, so that you know which fields or cells has been edited. Set [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode") as `batch` to enable batch editing.

N> [`getBatchChanges`](https://help.syncfusion.com/api/js/ejgrid#methods:getbatchchanges "getBatchChanges") method of grid holds the unsaved record changes.
N> Using [`getDataByIndex`](https://help.syncfusion.com/api/js/ejgrid#methods:getdatabyindex "getDataByIndex") method we can get the row data based on index.
N> Refer the KB [link](http://www.syncfusion.com/kb/3016/how-to-suppress-grid-confirmation-messages# "link") for "How to suppress grid confirmation messages" in batch mode.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "batch"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate", editType: "datepicker", format: "{0:dd/MM/yyyy}" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Batch / Excel-like of editing in Javascript grid](Editing_images/Editing_img15.png)

N> During batch editing, you can do any custom actions in-between, using the corresponding events [`batchAdd`](https://help.syncfusion.com/api/js/ejgrid#events:batchadd "batchAdd"), [`batchDelete`](https://help.syncfusion.com/api/js/ejgrid#events:batchdelete "batchDelete"), [`beforeBatchAdd`](https://help.syncfusion.com/api/js/ejgrid#events:beforebatchadd "beforeBatchAdd"), [`beforeBatchDelete`](https://help.syncfusion.com/api/js/ejgrid#events:beforebatchdelete "beforeBatchDelete"), [`beforeBatchSave`](https://help.syncfusion.com/api/js/ejgrid#events:beforebatchsave "beforeBatchSave") .
N> Using [`getCurrentEditCellData`](https://help.syncfusion.com/api/js/ejgrid#methods:getcurrenteditcelldata "getCurrentEditCellData") method, we can get the current edit cell data.

## Batch operations by external action

We can do the batch operations externally by using the following methods,

1. [`batchCancel`](https://help.syncfusion.com/api/js/ejgrid#methods:batchcancel "batchCancel")
2. [`batchSave`](https://help.syncfusion.com/api/js/ejgrid#methods:batchsave "batchSave")
3. [`saveCell`](https://help.syncfusion.com/api/js/ejgrid#methods:savecell "saveCell")
4. [`setCellValue`](https://help.syncfusion.com/api/js/ejgrid#methods:setcellvalue "setCellValue")
5. [`setDefaultData`](https://help.syncfusion.com/api/js/ejgrid#methods:setdefaultdata "setDefaultData")
6. [`editCell`](https://help.syncfusion.com/api/js/ejgrid#methods:editcell "editCell") 

The following code example describes the above behavior.

{% highlight html %}
<button id="batchCancel" class ="buttons" >batchCancel</button>
<button id="batchSave" class ="buttons" >batchSave</button>
<button id="setDefaultData" class ="buttons">setDefaultData</button>
<button id="setCellValue" class ="buttons">setCellValue</button>
<button id="editCell" class ="buttons" >editCell</button>
<button id="saveCell" class ="buttons" >saveCell</button>
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        pageSettings:{pageSize:6},
        editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,editMode: "batch" },
        toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, validationRules: { required: true, number: true }, width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', validationRules: { required: true, minlength: 3 }, width: 90 },
            { field: "EmployeeID", headerText: 'Employee ID', editType: ej.Grid.EditingType.Dropdown, textAlign: ej.TextAlign.Right, width: 80, validationRules: { number: true, range: [0, 1000] } },
            { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] }, width: 80, format: "{0:C}" },
            { field: "ShipName", headerText: 'Ship Name', width: 150 },
        ]
    });
});
$(".buttons").ejButton({
    click: function (args) {
        var option=args.target.id;
        if(option=="batchCancel"||option=="batchSave")
            $("#Grid").ejGrid(option);
        if(option=="editCell")
            $("#Grid").ejGrid("editCell", 0, "EmployeeID"); // cell is ready for editing
        if(option=="saveCell")
            $("#Grid").ejGrid("saveCell",true);    
        if(option=="setDefaultData")
            var defaultData = {OrderID:"10000"};  
            $("#Grid").ejGrid("setDefaultData",defaultData);    
        if(option=="setCellValue")
            $("#Grid").ejGrid("setCellValue",2, "EmployeeID", "10"); // cell value is set to the EmployeeID column
    }
});
{% endhighlight %}


Here we have set the default value to the EmployeeID Column based on index using setCellValue method and also we edit particular cell based on index using editCell method. Refer the below screenshot

![Batch operations of editing in Javascript grid](Editing_images/Editing_img31.png)

N> While editing action the following events are triggered,

1. [`beginEdit`](https://help.syncfusion.com/api/js/ejgrid#events:beginedit "beginEdit")
2. [`cellEdit`](https://help.syncfusion.com/api/js/ejgrid#events:celledit "cellEdit") 
3. [`endAdd`](https://help.syncfusion.com/api/js/ejgrid#events:endadd "endAdd")
4. [`endDelete`](https://help.syncfusion.com/api/js/ejgrid#events:enddelete "endDelete")
5. [`endEdit`](https://help.syncfusion.com/api/js/ejgrid#events:endedit "endEdit") 

## Editing customization by external action

To perform the editing actions like delete, update or insert by external action use the following methods,

1. [`cancelEdit`](https://help.syncfusion.com/api/js/ejgrid#methods:canceledit "cancelEdit")
2. [`cancelEditCell`](https://help.syncfusion.com/api/js/ejgrid#methods:canceleditcell "cancelEditCell")
3. [`endEdit`](https://help.syncfusion.com/api/js/ejgrid#methods:endedit "endEdit")
4. [`startEdit`](https://help.syncfusion.com/api/js/ejgrid#methods:startedit "startEdit")
5. [`deleteRecord`](https://help.syncfusion.com/api/js/ejgrid#methods:deleterecord "deleteRecord")
6. [`deleteRow`](https://help.syncfusion.com/api/js/ejgrid#methods:deleterow "deleteRow")  

The following code example describes the above behavior.

{% highlight html %}
<button id="cancelEdit" class ="buttons" >cancelEdit</button>
<button id="cancelEditCell" class ="buttons" >cancelEditCell</button>  
<button id="startEdit" class ="buttons" >startEdit</button>
<button id="endEdit" class ="buttons" >endEdit</button>
<br/></br>
<button id="deleteRecord" class ="buttons" >deleteRecord</button>
<button id="deleteRow" class ="buttons" >deleteRow</button>
<button id="updateRecord" class ="buttons" >updateRecord</button>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        pageSettings:{pageSize:6},
        editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true},
        toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
        columns: [
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, validationRules: { required: true, number: true }, width: 90 },
            { field: "CustomerID", headerText: 'Customer ID', validationRules: { required: true, minlength: 3 }, width: 90 },
            { field: "EmployeeID", headerText: 'Employee ID', editType: ej.Grid.EditingType.Dropdown, textAlign: ej.TextAlign.Right, width: 80, validationRules: { number: true, range: [0, 1000] } },
            { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] }, width: 80, format: "{0:C}" },
            { field: "ShipName", headerText: 'Ship Name', width: 150 },
        ]
    });
});
$(".buttons").ejButton({
    click:function(args){
        var option=args.target.id,grid = $("#Grid").ejGrid("instance");
        if((option=="cancelEdit")||(option=="cancelEditCell")||(option=="endEdit"))
            $("#Grid").ejGrid(option); 
        if(option=="startEdit")
            grid.startEdit(grid.getSelectedRows());
        if(option=="deleteRow")
            grid.deleteRow(grid.getSelectedRows());
        if(option=="deleteRecord")
            $("#Grid").ejGrid(option, "OrderID", { OrderID: 10249, EmployeeID: 3 });        
        if(option=="updateRecord")
            $("#Grid").ejGrid(option, "OrderID", {  OrderID:102453, EmployeeID: 2 ,CustomerID: "Arum",ShipCountry:"chennai"});        
    }
})
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Editing customization in Javascript grid](Editing_images/Editing_img33.png)

## Confirmation messages

To show the confirm dialog while saving or discarding the batch changes (discarding during the grid action like filtering, sorting and paging), set [`showConfirmDialog`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-showconfirmdialog "showConfirmDialog") as `true`.

N> [`showConfirmDialog`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-showconfirmdialog "showConfirmDialog") property is only for batch editing mode.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "batch"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate", editType: "datepicker", format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Confirmation messages for save option of  editing in Javascript grid](Editing_images/Editing_img16.png)


To show delete confirm dialog while deleting a record, set [`showDeleteConfirmDialog`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-showdeleteconfirmdialog "showDeleteConfirmDialog") as true.

N> [`showDeleteConfirmDialog`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-showdeleteconfirmdialog "showDeleteConfirmDialog") property is for all type of [`editMode`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-editmode "editMode").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
	$("#Grid").ejGrid({
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			showDeleteConfirmDialog : true
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry", editType: "dropdownedit" },
			{ field: "OrderDate", editType: "datepicker", format: "{0:dd/MM/yyyy}"}
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Confirmation messages for delete option of editing in Javascript grid](Editing_images/Editing_img17.png)


## Column Validation

We can validate the value of the added or edited record cell before saving.

The below validation script files are needed when editing is enabled with validation.

1. jquery.validate.min.js
2. jquery.validate.unobtrusive.min.js
 
 
### jQuery Validation


You can set validation rules using [`validationRules`](https://help.syncfusion.com/api/js/ejgrid#members:columns-validationrules "validationRules") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). The following are jQuery validation methods.

__List__ __of__ __Jquery__ __validation__ __methods__

<table>
<tr>
<th>
Rules</th><th>
Description</th></tr>
<tr>
<td>
required</td><td>
Requires an element.</td></tr>
<tr>
<td>
remote</td><td>
Requests a resource to check the element for validity.</td></tr>
<tr>
<td>
minlength</td><td>
Requires the element to be of given minimum length.</td></tr>
<tr>
<td>
maxlength</td><td>
Requires the element to be of given maximum length.</td></tr>
<tr>
<td>
range</td><td>
Requires the element to be in given value range.</td></tr>
<tr>
<td>
min</td><td>
The element requires a given minimum.</td></tr>
<tr>
<td>
max</td><td>
The element requires a given maximum.</td></tr>
<tr>
<td>
range</td><td>
Requires the element to be in a given value range.</td></tr>
<tr>
<td>
email</td><td>
The element requires a valid email.</td></tr>
<tr>
<td>
url</td><td>
The element requires a valid URL</td></tr>
<tr>
<td>
date</td><td>
Requires the element to be a date.</td></tr>
<tr>
<td>
dateISO</td><td>
The element requires an ISO date.</td></tr>
<tr>
<td>
number</td><td>
The element requires a decimal number.</td></tr>
<tr>
<td>
digits</td><td>
The element requires digits only.</td></tr>
<tr>
<td>
creditcard</td><td>
Requires the element to be a credit card number.</td></tr>
<tr>
<td>
equalTo</td><td>
Requires the element to be the same as another.</td></tr>
</table>

Grid supports all the standard validation methods of jQuery, please refer to the jQuery validation documentation [link](http://jqueryvalidation.org/documentation/# "link") for more information.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			showDeleteConfirmDialog : true
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true, validationRules: { required: true, number: true } },
			{ field: "CustomerID", validationRules: { required: true, minlength: 3 } },
			{ field: "ShipCity" },
			{ field: "Freight", editType: "numericedit", validationRules: { range: [0, 1000] } },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![jQuery validation of editing in Javascript grid](Editing_images/Editing_img18.png)

N> 1. Refer this [Knowledge Base link](https://www.syncfusion.com/kb/6817/how-to-perform-server-side-validation-in-grid) to perform server side validation in Grid.

N> 2. Use [`editFormValidate`](https://help.syncfusion.com/api/js/ejgrid#methods:editFormValidate "editFormValidate") to programmatically trigger validation of edit form.

## Column-validation customization by external action

Set validation to edit form in the grid by external action use [`setValidation`](https://help.syncfusion.com/api/js/ejgrid#methods:setvalidation "setValidation") method and Set validation to a particular input field in a edit form dynamically use  [`setValidationToField`](https://help.syncfusion.com/api/js/ejgrid#methods:setvalidation "setValidationToField") method.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
    $("#Grid").ejGrid({
        dataSource: window.gridData,
        allowPaging: true,
        actionComplete:actionComplete,
        editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
        toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
        columns: [
            { field:"Verified", headerText:"status",width:80},
            { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right,  width: 90 },
            { field: "CustomerID", headerText: 'Customer ID',  width: 90 },
            { field: "EmployeeID", headerText: 'Employee ID', editType: ej.Grid.EditingType.Dropdown, textAlign: ej.TextAlign.Right, width: 80,  },
            { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, width: 80, format: "{0:C}" },
            { field: "ShipName", headerText: 'Ship Name', width: 150 },
        ]
    });
});
function actionComplete(args){
    if(args.requestType =="beginedit"){
        if(args.rowData.Verified=="false" && args.rowData.EmployeeID <5){
            $("#Grid").ejGrid("setValidationToField", "CustomerID", { required: true });
        }
    }
}
{% endhighlight %}

 Here we have checked, if the Verified column value is false and EmployeeID value is less than 5 validation is set to CustomerID field.
 
 The following output is displayed as a result of the above code example.

![Column-validation customization of editing in Javascript grid](Editing_images/Editing_img30.png)

### Custom Validation

In addition to jQuery validation methods, you can also add your own custom validation methods for a specific column. Function call to custom validator function to be mentioned within [`validationRules`](https://help.syncfusion.com/api/js/ejgrid#members:columns-validationrules "validationRules") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns"). 

Using `messages` property of [`validationRules`](https://help.syncfusion.com/api/js/ejgrid#members:columns-validationrules "validationRules") you can specify the error message for that column.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$.validator.addMethod("customCompare", function (value, element, params) {
		return element.value > params[0] && element.value < params[1]
	}, "Freight value must be between 0 and 1000");

	$.validator.addMethod("customRegex", function (value, element, params) {
		if (element.value.length == params)
			return true;
		return false;
	}, "Customer ID must be 5 characters");

	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			showDeleteConfirmDialog : true
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true, validationRules: { required: true, number: true } },
			{ field: "CustomerID", validationRules: { customRegex: 5 } },
			{ field: "ShipCity" },
			{ field: "Freight", editType: "numericedit", validationRules: { customCompare: [0, 1000] } },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Custom validation of editing in Javascript grid](Editing_images/Editing_img19.png)


## Persisting data in Server

Edited data can be persisted in database using RESTful web services. 

All the CRUD operations in grid are done through DataManager. DataManager have an option to bind all the CRUD related data in server side. Please refer to the ['link'](https://help.syncfusion.com/js/datamanager/overview# "link") to know about the DataManager.

For you information ODataAdaptor persist data in server as per OData protocol.

In the below section, we have explained how to get the edited data details at the server side using URLAdaptor. 

### URL Adaptor

You can use the `UrlAdaptor` of [`ejDataManger`](https://help.syncfusion.com/api/js/ejdatamanager# "ejDataManger") when binding datasource from remote data. At initial load of Grid, using URL property of DataManager, data are fetched from remote data and bound to Grid. You can map CRUD operation in Grid to Server-Side Controller action using the properties `insertUrl`, `removeUrl`, `updateUrl`, `crudUrl` and `batchUrl`.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager({
			url : "Home/DataSource",
			updateUrl : "Home/Update",
			insertUrl : "Home/Insert",
			removeUrl : "Home/Delete",
			adaptor : "UrlAdaptor"
		}),
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "EmployeeID"},
			{ field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, format: "{0:C}" },
			{ field: "ShipName" },
			{ field: "ShipCountry"}
		]
	});
});
{% endhighlight %}

Also when you use `UrlAdaptor`, you need to return the data as `JSON` and the JSON object must contain a property as `result` with the dataSource as its value and one more property `count` with the dataSource total records count as its value.

The following code example describes the above behavior.

{% highlight cs %}
public ActionResult DataSource(DataManager dataManager)
{
	IEnumerable DataSource = OrderRepository.GetAllRecords();
	DataResult result = new DataResult();
	DataOperations operation = new DataOperations();
	result.result = DataSource;
	result.count = result.result.AsQueryable().Count();
	if (dataManager.Skip > 0)
		result.result = operation.PerformSkip(result.result, dataManager.Skip);
	if (dataManager.Take > 0)
		result.result = operation.PerformTake(result.result, dataManager.Take);
	return Json(result, JsonRequestBehavior.AllowGet);
}
public class DataResult
{
	public IEnumerable result { get; set; }
	public int count { get; set; }
}
{% endhighlight %}

The grid actions (sorting, filtering, paging, searching, and aggregates) details are obtained in the 'DataManager' class. While initializing the grid, paging only enabled hence in the below screen shot paging details are bound to the DataManager class.

Please refer the below screen shot.

![Editing](Editing_images/Editing_img20.png)


Also, using 'DataOperations' helper class you can perform grid action at server side. The built-in methods that we have provided in the DataOperations class are listed below.

1. PerformSorting
2. PerformFiltering
3. PerformSearching
4. PerformSkip
5. PerformTake
6. PerformWhereFilter
7. PerformSelect
8. Execute

### RemoteSave Adaptor

RemoteSaveAdaptor is used for binding local data and performs all data operations in client-side. It interacts with server-side only for CRUD operations to pass the modified records.

The following code example describes the above behavior

{% highlight html %}

<div id="Grid"></div>

{% endhighlight %}

{% highlight javascript %}

$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager({
			json : "window.gridData",
			updateUrl : "Home/Update",
			insertUrl : "Home/Insert",
			removeUrl : "Home/Delete",
			adaptor : "remoteSaveAdaptor"
		}),
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "EmployeeID"},
			{ field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, format: "{0:C}" },
			{ field: "ShipName" },
			{ field: "ShipCountry"}
		]
	});
});

{% endhighlight %}

### Accessing CRUD action request details in server side:

The 'Server-Side' function must be declared with the following parameter name for each editing functionality.

Parameters Table

<table>
        <tr>
            <th>
                Action
            </th>
            <th>
                Parameter Name</th>
            <th>
                Example
            </th>
        </tr>
        <tr>
            <td rowspan="2">
                Update,Insert
            </td>
            <td>
                value
            </td>
            <td rowspan="2">
                public ActionResult Update(EditableOrder value){ }
            </td>
        </tr>
        <tr>
           
            <td>
                public ActionResult Insert(EditableOrder value){ }
            </td>
        </tr>
        <tr>
            <td>
                Remove
            </td>
            <td>
                key
            </td>
            <td>
                public ActionResult Remove(int key){ }
            </td>
        </tr>
        <tr>
            <td>
                Batch Add
            </td>
            <td>
                added
            </td>
            <td rowspan="3">
                public ActionResult BatchUpdate(string action, List &lt;editableorder&gt; added, List &lt;editableorder&gt; changed, List &lt;editableorder&gt; deleted, int? key){ }
            </td>
        </tr>
        <tr>
            <td>
                Batch Update
            </td>
            <td>
                changed
            </td>
            
        </tr>
        <tr>
            <td>
                Batch Delete
            </td>
            <td>
                deleted
            </td>
           
        </tr>
        <tr>
            <td>
                Crud Update,Crud Insert
            </td>
            <td>
                value, action
            </td>
            <td>
                public ActionResult CrudUrl(EditableOrder value, string action){ }
            </td>
        </tr>
        <tr>
            <td>
                Crud Remove
            </td>
            <td>
                action, key, keyColumn
            </td>
            <td>
                public ActionResult CrudUrl(string action, int? key, string keyColumn){ }
            </td>
        </tr>
        <tr>
            <td>
                Crud Remove - Multi Delete
            </td>
            <td>
                action, key, deleted
            </td>
            <td>
                public ActionResult CrudUrl(string action, string key, List &lt;EditableOrder&gt; deleted){ }
            </td>
        </tr>
    </table>

	
### Insert Record:

Using `insertUrl` property, you can specify the controller action mapping URL to perform insert operation at the server side.

The following code example describes the above behavior.

{% highlight cs %}
public ActionResult Insert(EditableOrder value)
{
    OrderRepository.Add(value);
    var data = OrderRepository.GetAllRecords();
    return Json(value, JsonRequestBehavior.AllowGet);
}
{% endhighlight %}

The newly added record details are bound to the 'value' parameter. Please refer to the below image.


![Insert Record of editing in Javascript grid](Editing_images/Editing_img21.png)


### Update Record:

Using `updateUrl` property, you can specify the controller action mapping URL to perform save/update operation at server side.

The following code example describes the above behavior.

{% highlight cs %}
public ActionResult Update(EditableOrder value)
{
    OrderRepository.Update(value);
    var data = OrderRepository.GetAllRecords();
    return Json(value, JsonRequestBehavior.AllowGet);
}
{% endhighlight %}

The updated record details are bound to the 'value' parameter. Please refer to the below image.

![Update Record of editing in Javascript grid](Editing_images/Editing_img22.png)


### Delete Record:

Using `removeUrl` property, you can specify the controller action mapping URL to perform delete operation at the server side.

The following code example describes the above behavior.

{% highlight cs %}
public ActionResult Remove(int key)
{
  OrderRepository.Delete(key);
  var data = OrderRepository.GetAllRecords();
  return Json(key, JsonRequestBehavior.AllowGet);
}
{% endhighlight %}

The deleted record primary key value is bound to the 'key' parameter. Please refer the below image.

![Delete Record of editing in Javascript grid](Editing_images/Editing_img23.png)


### CRUD URL:

Instead of specifying separate controller action method for CRUD (insert, update and delete)operation, using `crudUrl` property you can specify the controller action mapping URL to perform all CRUD operation at the server side using single method.

The action parameter of `crudUrl` is used to get the corresponding CRUD action.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager({
			url : "Home/DataSource",
			crudUrl : "Home/CrudUpdate",
			adaptor : "UrlAdaptor"
		}),
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "EmployeeID"},
			{ field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, format: "{0:C}" },
			{ field: "ShipName" },
			{ field: "ShipCountry"}
		]
	});
});
{% endhighlight %}

{% highlight javascript %}
public ActionResult CrudUpdate(EditableOrder value, string action,int Key)
{
    if (action == "update")
        OrderRepository.Update(value);
    else if (action == "insert")
        OrderRepository.Add(value);
    else if (action == "remove")
        OrderRepository.Delete(key);
    return Json(value, JsonRequestBehavior.AllowGet);
}
{% endhighlight %}

Please refer to the below image to know about the action parameter

![Editing](Editing_images/Editing_img24.png)


N> If you specify `insertUrl` along with `CrudUrl` then while adding `insertUrl` only called.

### Batch URL:

The `batchUrl` property supports only for batch editing mode. You can specify the controller action mapping URL to perform Batch operation at the server side.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>


$(function () {
	$("#Grid").ejGrid({
		dataSource : ej.DataManager({
			url : "Home/DataSource",
			batchUrl : "Home/BatchUpdate",
			adaptor : "UrlAdaptor"
		}),
		allowPaging : true,
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			editMode : "batch"
		},
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel]
		},
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "EmployeeID"},
			{ field: "Freight", editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, format: "{0:C}" },
			{ field: "ShipName" },
			{ field: "ShipCountry"}
		]
	});
});

{% endhighlight %}


{% highlight c# %}

public ActionResult BatchUpdate(string action, List<EditableOrder> added, List<EditableOrder> changed, List<EditableOrder> deleted, int? key)
{
    if (changed != null)
        OrderRepository.Update(changed);
    if (deleted != null)
        OrderRepository.Delete(deleted);
    if (added != null)
        OrderRepository.Add(added);
    var data = OrderRepository.GetComplexRecords();
    return Json(new { changed = changed, added = added, deleted = deleted }, JsonRequestBehavior.AllowGet);
}

{% endhighlight %}


Please refer to the below image for more information about batch parameters

![CRUD URL of editing in Javascript grid](Editing_images/Editing_img25.png)


## Adding New Row Position

To add a new row in the top or bottom position of grid content, set [`rowPosition`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-rowposition "rowPosition") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings") depending on the requirement.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			rowPosition : "bottom"
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry" }
		]
	});
});

{% endhighlight %}

The following output is displayed as a result of the above code example.

![Adding new row position of editing in Javascript grid](Editing_images/Editing_img26.png)


## Render with blank row for easy add new

The blank add new row is displayed in the grid content during grid initialization itself to add a new record easily. To enable show add new row by default, set the [`showAddNewRow`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-showaddnewrow "showAddNewRow") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings") as `true`.

The blank add new row is displayed either in the top or bottom of the corresponding page, its position is based on the [`rowPosition`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-rowposition "rowPosition") property of [`editSettings`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings "editSettings").

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true,
			showAddNewRow : true
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity" },
			{ field: "Freight", editType: "numericedit" },
			{ field: "ShipCountry" }
		]
	});
});
{% endhighlight %}

The following output is displayed as a result of the above code example.

![Render with blank row for add new row option of editing in Javascript grid](Editing_images/Editing_img27.png)


N> 1. If it is remote, then the newly added record is placed based on the index from current view data. 

N> 2. If it is local, then the newly added record is added at the top of the page even if the added new [`rowPosition`](https://help.syncfusion.com/api/js/ejgrid#members:editsettings-rowposition "rowPosition") is mentioned as "bottom".


## Default column values on add new

While adding new record in grid, there is an option to set the default value for the columns. Using the [`defaultValue`](https://help.syncfusion.com/api/js/ejgrid#members:columns-defaultvalue "defaultValue") property of [`columns`](https://help.syncfusion.com/api/js/ejgrid#members:columns "columns") you can set the default values for that particular column while editing or adding a new row.

The following code example describes the above behavior.

{% highlight html %}
<div id="Grid"></div>
{% endhighlight %}

{% highlight javascript %}
$(function () {
	$("#Grid").ejGrid({
		//The datasource "window.gridData" is referred from 'http://js.syncfusion.com/demos/web/scripts/jsondata.min.js'
		dataSource : window.gridData,
		toolbarSettings : {
			showToolbar : true,
			toolbarItems : ["add", "edit", "delete", "update", "cancel"]
		},
		editSettings : {
			allowEditing : true,
			allowAdding : true,
			allowDeleting : true
		},
		allowPaging : true,
		columns : [
			{ field: "OrderID", isPrimaryKey: true },
			{ field: "CustomerID" },
			{ field: "ShipCity", defaultValue: "Bern" },
			{ field: "Freight", editType: "numericedit", defaultValue: 45 },
			{ field: "ShipCountry", defaultValue: "Brazil" }
		]
	});
});
{% endhighlight %}


The following output is displayed as a result of the above code example.

![Default column values on add new of editing in Javascript grid](Editing_images/Editing_img28.png)


