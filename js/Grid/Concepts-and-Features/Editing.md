---
layout: post
title: Editing
description: editing
platform: js
control: Grid
documentation: ug
---

# Editing

**Essential Studio JavaScript Grid** has built-in support for editing **Grid** content. This can be achieved by defining an edit option for the Grid. You must provide toolbar support for editing records and validation support while editing the record. 

## Toolbar with edit option

**Essential Studio JavaScript Grid** provides toolbar support and it can be customized. It contains the following built-in toolbar items: 

* Add

* Edit

* Delete

* Update

* Cancel



{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
              **toolbarSettings: {**
                    **showToolbar: true,**
                    **toolbarItems: [**
                       **ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,**
                       **ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,**
                       **ej.Grid.ToolBarItems.Cancel**
                    **]**
                **},**
                **editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },**
                allowPaging: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID" },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right" },
                    { field: "ShipCity", headerText: "Ship City" },
                    { field: "Verified", headerText: "Verified" }
                ]

            });
        });

    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img1.png" Caption="Toolbar with Edit Option"%}

## Cell edit type

Essential Studio JavaScript Grid supports column edit type by using delegated controls for specific data types. They are:

* **CheckBox** control for boolean data type.

* **NumericTextBox** control for integers, double, and decimal types.

* **InputTextBox** control for string data types.

* **DatePicker** control for date data.

* **DateTimePicker** control for date-time data.

* **DropDownList** control for list of data.

The edit type of every column can be customized using the **editType** property.

{% highlight html %}

**[JS]**

  <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
                allowPaging: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", IsPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", **editType: ej.Grid.EditingType.String** },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right",**editType: ej.Grid.EditingType.Numeric** },
                    { field: "ShipCity", headerText: "Ship City", **editType: ej.Grid.EditingType.Dropdown** },
                    { field: "OrderDate", headerText: "Order Date", **editType: ej.Grid.EditingType.DatePicker**, format: "{0:MM/dd/yyyy}" },
                    { field: "Verified", headerText: "Verified", **editType: ej.Grid.EditingType.Boolean** }
                ]
            });
        });

    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img2.png" Caption="Cell Edit Type"%}

### External DataSource for DropDown EditType Column

By default, the datasource for Dropdown Edit Column is set by Grid Control from its datasource. You can also bind external datasource to the Dropdown control of corresponding column in edit mode by using “**dataSource**” Grid Column property.

> _**Note: The external datasource must be given in a structure that it should contain properties “text” and “value” which holds the data.**_


{% highlight html %}

**[JS]**
 <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
                allowPaging: true,
                columns: [
                   { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 90 },
                    { field: "CustomerID", headerText: 'Customer ID', width: 90 },
                    { field: "EmployeeID", headerText: 'Employee ID',  textAlign: ej.TextAlign.Right, width: 80},
                    { field: "Freight", headerText: 'Freight', width: 80},
                    { field: "ShipCountry", headerText: 'Ship Country', width: 90, editType: ej.Grid.EditingType.Dropdown, **dataSource: countries** }
                ]
            });
        });

    </script>
{% endhighlight %}



{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img3.png" Caption="Dropdown External DataSource"%}

## Edit Template

**Edit Template** feature is used to create a custom editor to edit column values. **Edit Template** has three functions. Using **ediTemplate** property we are able to achieve Edit Template feature.

* **Create** – It is used to create the control at time of initialize

* **Read** –  It is used to read the input value at time of save

* **Write** – It is used to assign the value to control at time of editing

The following code example is for **Edit Template.**

{% highlight html %}

**[JS]**
<div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area">
                <div id="Grid"></div>
            </div>
        </div>
    </div>
    <script type="text/javascript">
        $(function () {
            $("#Grid").ejGrid({
                // the datasource "window.gridData" is referred from jsondata.min.js
                dataSource: window.gridData,
                allowPaging: true,
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true, },
                toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
                columns: [
                        { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, width: 90 },
                        { field: "CustomerID", headerText: 'Customer ID', width: 90 },
                        {
                            field: "EmployeeID", headerText: 'Employee ID',
                            **editTemplate: {**
                                **create: function () {**
                                    **return "<input>";**
                                **},**
                                **read: function (args) {**
                                    **return args.ejMaskEdit("get_StrippedValue");**
                                **},**
                                **write: function (args) {**
                                    **args.element.ejMaskEdit({ width: "100%", maskFormat: "9", value: args.rowdata !== undefined ? args.rowdata["EmployeeID"] : "" });**
                                }
                            }, textAlign: ej.TextAlign.Right, width: 80,
                        },
                        { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, width: 80, format: "{0:C0}" },
                        { field: "ShipName", headerText: 'Ship Name', width: 150 },
                        { field: "ShipCountry", headerText: 'Ship Country', editType: ej.Grid.EditingType.Dropdown, width: 90, }
                ]
            });
        });
    </script>



{% endhighlight %}



The forllowing screen shot showed the out put of the above code snippet.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img4.png" Caption="Edit Template"%}

## Edit Mode

Essential Studio JavaScript Grid supports eight modes of editing feature in grid. They are:

* Normal row editing

* Inline form editing

* Inline template form editing

* Dialog editing

* Dialog template form editing

* External form editing

* External template form editing

* Batch editing

### Normal Editing

This feature allows you to edit various fields of a single record, simultaneously. The row goes to editable state. The following code example shows you how to set **editMode** as **Normal**.

{% highlight html %}

**[JS]**

 <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,
              **editMode: ej.Grid.EditMode.Normal** },
                allowPaging: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimarKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown },
                    { field: "OrderDate", headerText: "Order Date", editType: ej.Grid.EditingType.DatePicker, format: "{0:MM/dd/yyyy}" },
                    { field: "Verified", headerText: "Verified", editType: ej.Grid.EditingType.Boolean }
                ]
            });
        });

    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img5.png" Caption="Normal Editing"%}

### Dialog Editing

The **Dialog Edit** feature allows you to edit data, using a dialog box that has fields associated with the data record being edited. You can only edit the data stored in the fields that you have rendered to be visible. The following code example shows you how to set editMode as **Dialog**.

{% highlight html %}

**[JS]**
    <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,
              **editMode: ej.Grid.EditMode.Dialog**},
                allowPaging: true,
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown },
                    { field: "OrderDate", headerText: "Order Date", editType: ej.Grid.EditingType.DatePicker, format: "{0:MM/dd/yyyy}" },
                    { field: "Verified", headerText: "Verified", editType: ej.Grid.EditingType.Boolean }
                ]
            });
        });

    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img6.png" Caption="Dialog Editing"%}

### Inline Form Editing

This feature allows you to edit various fields of a single record, simultaneously. It is called inline because it is shown in between two rows, called as rows of control. After you have edited a row, the inline form is displayed. 

{% highlight html %}

**[JS]**
    <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,
              **editMode: ej.Grid.EditMode.InlineForm**},
                allowPaging: true,
                pageSettings: { pageSize: 8 },
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown },
                    { field: "OrderDate", headerText: "Order Date",editType: ej.Grid.EditingType.DatePicker, format: "{0:MM/dd/yyyy}" },
                    { field: "Verified", headerText: "Verified", editType: ej.Grid.EditingType.Boolean }
                ]
            });
        });

    </script>



{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img7.png" Caption="Inline Form Editing"%}

### External Form Editing

The **External Form Edit Mode** helps you edit various data entries in the **Grid**, one at a time, using an external edit form.

This is different from the **Dialog Editing** mode in that it allows you to see the other entries in the **Grid** while you are editing one.

You can position the edit form either in the top-right corner or the bottom-left corner (by default) of the **Grid**. The following code example shows you how to set **editMode** as **External Form**.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,
              **editMode: ej.Grid.EditMode.ExternalForm,**
                        **formPosition: ej.Grid.FormPosition.BottomLeft**},
                allowPaging: true,
                pageSettings: { pageSize: 8 },
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City",editType: ej.Grid.EditingType.Dropdown },
                    { field: "OrderDate", headerText: "Order Date", editType: ej.Grid.EditingType.DatePicker, format: "{0:MM/dd/yyyy}" },
                    { field: "Verified", headerText: "Verified", editType: ej.Grid.editingType.Boolean }
                ]
            });
        });

    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img8.png" Caption="External Form Editing"%}

### Template Form Editing

You can edit any of the fields pertaining to a single record of data and apply it to a template so that the same format is applied to all the other records that you may edit later.

You can also edit the fields that are not visible in the **Grid** using this template. You are provided with three template editing support in **Grid**.

* Inline template form editing

* Dialog template form editing

* External template form editing

#### Inline Template Form Editing

In Inline Template, you can specify the template inside the script tag and select the type as text/template. Only then the HTML elements defined in the template will not be displayed in the browser. You can define the template as follows. Using inlineFormTemplateID we are able to set the form template for editing.

{% highlight html %}
**[JS]**
 <script id="template" type="text/template">
        <table cellspacing="10">
            <tr>
                <td style="text-align: right;">Order ID
                </td>
                <td style="text-align: left">
                    <input id="OrderID" name="OrderID" value="{{: OrderID}}" disabled="disabled" />
                </td>
                <td style="text-align: right;">Customer ID
                </td>
                <td style="text-align: left">
                    <input id="CustomerID" name="CustomerID" value="{{: CustomerID}}" />
                </td>
            </tr>
            <tr>
                <td style="text-align: right;">Employee ID
                </td>
                <td style="text-align: left">
                    <input type="text" id="EmployeeID" name="EmployeeID" value="{{:EmployeeID}}" />
                </td>
                <td style="text-align: right;">Ship City
                </td>
                <td style="text-align: left">
                    <input id="ShipCity" name="ShipCity" value="{{: ShipCity}}" class="e-field e-ejinputtext valid" style="width: 116px; height: 28px" />
                </td>
            </tr>
            <tr>
                <td style="text-align: right;">Freight
                </td>
                <td style="text-align: left">
                    <input id="Freight" name="Freight" value="{{: Freight}}" />
                </td>
            </tr>
        </table>
    </script>
    
    
    // Now you can assign the template id to the InlineFormTemplateId property of edit.

    <div id="Grid"></div>

    <script id="template" type="text/template">
        <table cellspacing="10">
            <tr>
                <td style="text-align: right;">Order ID
                </td>
                <td style="text-align: left">
                    <input id="OrderID" name="OrderID" value="{{: OrderID}}" disabled="disabled" />
                </td>
                <td style="text-align: right;">Customer ID
                </td>
                <td style="text-align: left">
                    <input id="CustomerID" name="CustomerID" value="{{: CustomerID}}" />
                </td>
            </tr>
            <tr>
                <td style="text-align: right;">Employee ID
                </td>
                <td style="text-align: left">
                    <input type="text" id="EmployeeID" name="EmployeeID" value="{{:EmployeeID}}" />
                </td>
                <td style="text-align: right;">Ship City
                </td>
                <td style="text-align: left">
                    <input id="ShipCity" name="ShipCity" value="{{: ShipCity}}" class="e-field e-ejinputtext valid" style="width: 116px; height: 28px" />
                </td>
            </tr>
            <tr>
                <td style="text-align: right;">Freight
                </td>
                <td style="text-align: left">
                    <input id="Freight" name="Freight" value="{{: Freight}}" />
                </td>
            </tr>
        </table>
    </script>

    <script type="text/javascript">

        $(function () {// Document is ready.

            $("#Grid").ejGrid({

                dataSource: window.gridData,

                toolbarSettings: {

                    showToolbar: true,

                    toolbarItems: [

                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,

                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,

                       ej.Grid.ToolBarItems.Cancel

                    ]

                },

                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true,

                        editMode: ej.Grid.EditMode.InlineTemplateForm,

                        inlineFormTemplateID: "#template"},

                allowPaging: true,

                pageSettings: { pageSize: 6 },

                columns: [

                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },

                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },

                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },

                    { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown }

              ]

            });

        });

    </script>

{% endhighlight %}

The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img9.png" Caption="Inline Template Form Editing"%}

In the above screenshot you can see that the elements are not rendered based on the type of the column. For example, in Freight column, the textbox is rendered instead of NumericTextBox.

While using template, you can change the elements that are defined in the template, to appropriate control based on the column type. 

Through the **actionComplete** **Grid** event, you can achieve this.

{% highlight html %}

**[JS]**

<script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({

               //. . . .
           **actionComplete: "complete",**
              //. . . .

            });
        });
        **function complete(args) {**
            **$("#EmployeeID").ejNumericTextbox();**
            **$("#Freight").ejNumericTextbox();**
            **$("#ShipCity").ejDropDownList();**
        **}**
</script>


{% endhighlight %}



Now, the elements defined in the templates, are changed to JavaScript controls. You can see the entire code example for Template editing as follows.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script id="template" type="text/template">
        <table cellspacing="10">
            <tr>
                <td style="text-align: right;">Order ID
                </td>
                <td style="text-align: left">
                    <input id="OrderID" name="OrderID" value="**{{:** OrderID**}}**" disabled="disabled" />
                </td>
                <td style="text-align: right;">Customer ID
                </td>
                <td style="text-align: left">
                    <input id="CustomerID" name="CustomerID" value="**{{:** CustomerID**}}**" />
                </td>
            </tr>
            <tr>
                <td style="text-align: right;">Employee ID
                </td>
                <td style="text-align: left">
                    <input type="text" id="EmployeeID" name="EmployeeID" value="**{{:**EmployeeID**}}**" />
                </td>
                <td style="text-align: right;">Ship City
                </td>
                <td style="text-align: left">
                    <input id="ShipCity" name="ShipCity" value="**{{:** ShipCity**}}**" class="e-field e-ejinputtext valid" style="width: 116px; height: 28px" />
                </td>

            </tr>
            <tr>
                <td style="text-align: right;">Freight
                </td>
                <td style="text-align: left">
                    <input id="Freight" name="Freight" value="**{{:** Freight**}}**" />
                </td>

            </tr>
        </table>
    </script>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true,
                   **editMode: ej.Grid.EditMode.InlineTemplateForm,**
                    **inlineFormTemplateID: "#template"**
                },
                allowPaging: true,
                pageSettings: { pageSize: 6 },
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right",editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City",editType: ej.Grid.EditingType.Dropdown }
                ],
                actionComplete: "complete"
            });
        });
        function complete(args) {
            $("#EmployeeID").ejNumericTextbox();
            $("#Freight").ejNumericTextbox();
            $("#ShipCity").ejDropDownList();
        }
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img10.png" Caption="Inline Template Form Editing with actionComplete events"%}

#### External Template Form Editing

The above mentioned procedure applies to **ExternalTemplate** editing feature also. Use the given code example instead of setting inlineTemplateForm as editMode. Using **externalFormTemplateID** we are able to set external template for editing.

{% highlight html %}

 **[JS]**

 $(function () {// Document is ready.
            $("#Grid").ejGrid({
                //. . . .
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true,
                  **editMode: ej.Grid.editMode.ExternalFormTemplate,**
                  **externalFormTemplateID: "#template"**
                },
               //. . . .
            });
        });



{% endhighlight %}



The following screenshot shows External Template Form Editing.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img11.png" Caption="External Template Form Editing"%}

#### Dialog Template Editing

The above mentioned procedure applies to **DialogTemplate** editing feature also. Use the given code example instead of setting for DialogTemplate as editMode. Using **dialogEditorTemplateID** property to set the dialog template for editing.

{% highlight html %}

**[JS]**

 $(function () {// Document is ready.
            $("#Grid").ejGrid({
                //. . . .
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true,
                    **editMode: ej.Grid.EditMode.DialogTemplate,**
                    **dialogEditorTemplateID: "#template"**
                },
               //. . . .
            });
        });


{% endhighlight %}



The following screenshot shows Dialog Template Form Editing.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img12.png" Caption="Dialog Template Form Editing"%}

### Batch Editing

This feature allows you to edit various fields of the **Grid**, simultaneously, with the ease of Excel-like functionality in editing data.

Edited data is marked on the **Grid,** so that you know which fields or cells have been edited.
These markers are not shown after the updated data is rendered. The following code example shows you how to enable Excel-like editing, also called **Batch****editing**, in **Grid**.

{% highlight html %}

**[JS]**
    <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true,
                    **editMode: ej.Grid.EditMode.Batch**
                },
                allowPaging: true,
                pageSettings: { pageSize: 6 },
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown }
                ]
            });
        });
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img13.png" Caption="Batch Editing"%}

When the Save or Cancel button is clicked, or performing an action before you save the edited records, the Confirmation message is displayed. 

The following screenshot shows the Confirmation Dialog box.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img14.png" Caption="Batch Editing with Confimation Dialog box"%}



## Validation

**Essential JavaScript Grid** supports all the standard validation methods of **jquery**. Using this feature you can validate the value of the edited record cell before the edited record cell values are saved.

For validation you can refer the following two **jquery** validation script files.

1. jquery.validate.min.js

2. jquery.validate.unobtrusive.min.js

### jQuery Validation Methods

The following are jquery validation methods.

_List of jquery validation methods_

<table>
<tr>
<td>
<b>Rules</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
Required</td><td>
 Requires an element.</td></tr>
<tr>
<td>
Remote</td><td>
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
rangelength</td><td>
 Requires the element to be in given value range.</td></tr>
<tr>
<td>
Min</td><td>
 The element requires a given minimum.</td></tr>
<tr>
<td>
Max</td><td>
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
 The element requires a valid url</td></tr>
<tr>
<td>
Date</td><td>
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


The following code example shows you how to include the jquery validation support for **Grid** while editing the records. We can set validation rules using **validationRules** property.

{% highlight html %}

  **[JS]**
 <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true
                },
                allowPaging: true,                
                columns: [
                        { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right", **validationRules: { required: true }** },
                        { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String****},
                        { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                        { field: "Freight", textAlign: "right", editType: ej.Grid.EditingType.Numeric, **validationRules: { range: [0, 1000] }** },
                        { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown }
               ]
            });
        });
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img15.png" Caption="JQuery Validation Methods"%}

### Custom Validation

In addition to jquery validation methods, you can also add your own custom validation methods for a specific column. The following code example shows you how to specify the custom validation for a specific column.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
$.validator.addMethod("customCompare", function (value, element, params) {
               return element.value > params[0] && element.value < params[1]
           }, "Freight value must be between 1 and 9");

           $.validator.addMethod("customRegex", function (value, element, params) {
               if (element.value.length == params)
                  return true;
               return false;
            }, "Customer ID must be 5 characters");

            $("#Grid").ejGrid({
                dataSource: window.gridData,
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true
                },
                allowPaging: true,                
                columns: [
                        { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right", validationRules: { required: true } },
                        { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String**, validationRules: { customRegex: 5 }** },
                        { field: "Freight", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                        { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric**, validationRules: { customCompare: [1, 9] }** },
                        { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown }
                    ]
            });
        });
    </script>



{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img16.png" Caption="Custom Validation Methods"%}

## CRUD Operation With Server-Side

The **Server-Side CRUD** operation can be performed by using the following adaptor methods in **ejGrid**.

1. Url Adaptor

2. RemoteSaveAdaptor

The **Server-Side** function is declared with the following parameters for each editing functionality.

_Parameters Table_

<table>
<tr>
<td>
<b>Action</b></td><td>
<b>Parameter Name</b></td><td>
<b>Example</b></td></tr>
<tr>
<td rowspan = "2">
Update, Insert</td><td rowspan = "2">
value</td><td>
public ActionResult Update(EditableOrder value){}</td></tr>
<tr>
<td>
public ActionResult Insert(EditableOrder value){}</td></tr>
<tr>
<td>
Remove</td><td>
key</td><td>
public ActionResult Remove(int key){}</td></tr>
<tr>
<td>
Batch Add</td><td>
added</td><td>
public ActionResult BatchUpdate(List<Orders> changed, List<Orders> added, List<Orders> deleted){}</td></tr>
</table>
### URL Adaptor

You can use the **UrlAdaptor** of ejDataManger when binding datasource from remote data. At initial load of **Grid**, using **URL** property of DataManager, data are fetched from remote data and binded to **Grid**. You can map **CRUD** operation in **Grid** to Server-Side Controller action using the properties “InsertURL”, “UpdateURL” and “RemoveURL”. We can set insert, update and remove url using ejDataManager properties **insertUrl,removeUrl** and **updateUrl.**

Also when you use **UrlAdaptor**, you need to return the data as **JSON** and the **JSON** object must contain field name as “result” with its value as dataSource and one more field name as “count” with its value as dataSource total records count.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
<script type="text/javascript">
    $(function () {
            $("#Grid").ejGrid({
                dataSource: ej.DataManager({ **url: "Home/DataSource", updateUrl: "Home/Update", insertUrl: "Home/Insert", removeUrl: "Home/Delete", adaptor: “UrlAdaptor”** }),
                allowPaging: true,
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
                toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
                columns: [
                        { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, validationRules: { required: true, number: true }, width: 90 },
                        { field: "CustomerID", headerText: 'Customer ID', validationRules: { required: true, minlength: 3 }, width: 90 },
                        { field: "EmployeeID", headerText: 'Employee ID',  textAlign: ej.TextAlign.Right, width: 80, validationRules: { number: true } },
                        { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] }, width: 80, format: "{0:C}" },
                        { field: "ShipName", headerText: 'Ship Name', width: 150 },
                        { field: "ShipCountry", headerText: 'Ship Country', width: 90 }
                ]
        });
        });
</script>


{% endhighlight %}

### remoteSave Adaptor

The **remoteSaveAdaptor** of DataManager can be used when you bind local data to **Grid** datasource. **CRUD** operations in **Grid** local data can be mapped to server-side controller using **CRUD****URL’s** “InsertUrl”, “UpdateUrl” and “RemoveUrl”. We can set insert, update and remove url using ejDataManager properties **insertUrl, removeUrl** and **updateUrl.**

When you use **remoteSaveAdaptor**, server-side post back occurs only for **CRUD** actions in **Grid**. Rest of the **Grid** actions (paging, sorting, filtering, etc.,) can be handled at client-side itself.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
<script type="text/javascript">
    $(function () {
            $("#Grid").ejGrid({
                dataSource: ej.DataManager({ **json: window.gridData, updateUrl: "Home/Update", insertUrl: "Home/Insert", removeUrl: "Home/Delete", adaptor: "remoteSaveAdaptor" }**),
                allowPaging: true,
                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },
                toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
                columns: [
                        { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, validationRules: { required: true, number: true }, width: 90 },
                        { field: "CustomerID", headerText: 'Customer ID', validationRules: { required: true, minlength: 3 }, width: 90 },
                        { field: "EmployeeID", headerText: 'Employee ID',  textAlign: ej.TextAlign.Right, width: 80, validationRules: { number: true } },
                        { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] }, width: 80, format: "{0:C}" },
                        { field: "ShipName", headerText: 'Ship Name', width: 150 },
                        { field: "ShipCountry", headerText: 'Ship Country', width: 90 }
                ]
        });
        });
</script>


{% endhighlight %}



The output for the Server Binding of records is as follows:

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img17.png" Caption=""%}

_Edit_

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img18.png" Caption="Server Bind"%}

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img19.png" Caption="Console Post"%}

## Editing Remote Data

In general, the client-side controls cannot be directly bound to SQL Server database. To access or modify the database, you must create web services that will return the **JSON** data, based on the request made.  **DataManager** can be bound to any web services. For a quick start, you can use **OData****Services** like WebApi, WCF DataServices.

Refer to the following steps to create WCF dataservice.

The **Grid** control for **JavaScript** allows you to bind and edit data from the local server. Refer to the following steps to edit local server data.

1. Open Visual Studio 2012. In the File menu, click New and select Project. The New Project Dialog box is opened.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img20.png" Caption="WCF Dataservice"%}

2. Select ASP.NET Empty Web Application and click OK.

3. Create empty folders named App_Data and Models in the root of the application.

4. Add an HTML page in the root of the application. 

5. Add the NORTHWND.MDF file into the App_Data folder, and the corresponding NORTHWND_log.ldf is created automatically.

6. Right-click the Models folder in the Solution Explorer window and select the menu option Add New Item.

7. In the Add New Item dialog, select the Data category.



{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img21.png" Caption="Creating a New Entity Data Model"%}

8. Select the ADO.NET Entity Data Model template, give the Entity Data Model the name Northwind.edmx, and click the Add button. Click Add to launch the Data Model Wizard. 

9. In the Choose Model Contents step, choose the Generate from database option and click Next.



{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img22.png" Caption="Entity Data Model Wizard"%}

10. In the Choose Your Data Connection step, select the NORTHWND.MDF database connection, enter the entities connection settings name NORTHWNDEntities and click Next.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img23.png" Caption="Entity Data Model Wizard"%}

11. In the **Choose Your Database Objects** step, select all the database tables and click **Finish**.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img24.png" Caption="Figure 70: Entity Data Model Wizard"%}

When you are finished, you can see the following image.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img25.png" Caption="GridDemo"%}

12. Right-click the Models folder in the Solution Explorer window and select the Menu option Add New Item.

13. In the Add New Item dialog, in the Web category, select WCF Data Service, enter Northwnd.svc in the Name textbox and click Add. 

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img26.png" Caption="Add New Item- GridDemo"%}

14. The WCF Data Service file is created. Open the Nothwnd.svs.cs file and set the NORTHWNDEntities as a class for the DataService.

{% highlight c# %}

public class Northwnd : DataService</* TODO: put your data source class name here.*/>
Replace the above line with the following:
public class Northwnd : DataService<NORTHWNDEntities>


{% endhighlight %}



15. Add the highlighted line in the Nothwnd.svs.cs.

{% highlight c# %}

public static void InitializeService(DataServiceConfiguration config)
        {
            // TODO: Set rules to indicate which entity sets and service operations are visible, updatable, etc.
            // Examples:
            // config.SetEntitySetAccessRule("MyEntityset", EntitySetRights.AllRead);
            // config.SetServiceOperationAccessRule("MyServiceOperation", ServiceOperationRights.All);
            config.DataServiceBehavior.MaxProtocolVersion = DataServiceProtocolVersion.V3;
            **config.SetEntitySetAccessRule("*", EntitySetRights.All);**
        }


{% endhighlight %}



16. Refer to the following code sample to get the data from the local server.

{% highlight html %}

**var dataManger = ej.DataManager({
                url: "/model/Northwnd.svc/Orders"
});**


{% endhighlight %}



17. Add the following codes into the HTML page.

{% highlight html %}

**[JS]**

<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {// Document is ready.
**var dataManger = ej.DataManager({**
                **url: "/model/Northwnd.svc/Orders"**
            **});**
            $("#Grid").ejGrid({
              **dataSource: dataManger,**
                toolbarSettings: {
                    showToolbar: true,
                    toolbarItems: [
                       ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit,
                       ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update,
                       ej.Grid.ToolBarItems.Cancel
                    ]
                },
                editSettings: {
                    allowEditing: true, allowAdding: true, allowDeleting: true
                },
                allowPaging: true,                
                columns: [
                        { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right"},
                        { field: "CustomerID", headerText: "Customer ID" },
                        { field: "ShipCity", headerText: "Ship City " },
                        { field: "Freight", textAlign: "right" },
                        { field: "ShipCountry", headerText: "Ship Country" },
                ]
            });
        });
    </script>



{% endhighlight %}



The output for the above Grid creation with editing options code example is as follows.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img27.png" Caption="Editing Remote Data"%}

## Adding New Row Position

Adding new row position allows you to add new row in the top or bottom position that depends upon the requirement. 

ejGrid supports two types of rowposition. Using rowPosition property to assign row position for editing.They are

* Top

* Bottom

The following code example illustrates you how to set rowPosition.

{% highlight html %}

**[JS]**
<div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            // the datasource "window.gridData" is referred from jsondata.min.js
            $("#Grid").ejGrid({
                dataSource:windows.griddata
                allowPaging: true,
                scrollSettings: { width: 500, height: 300 },
                editSettings: { allowAdding: true, **rowPosition: “bottom”,** allowEditing: true, allowDeleting: true },
                allowScrolling: true,
                columns: [
                            { field: "OrderID", headerText: "Order ID", textAlign:ej.TextAlign.Right },
                            { field: "CustomerID", headerText: "Employee ID" },
                            { field: " EmployeeID ", headerText: "Frieght", textAlign:ej.TextAlign.Right },
                            { field: "ShipCity", headerText: "Ship City", editType: ej.Grid.EditingType.Dropdown }
                ]
            });
        });
    </script>


{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img28.png" Caption=""%}

_Adding new row position_

## Render grid with add new row

In **ejGrid,** there is an option to****show the newly add row at the bottom or top of the Grid content during **Grid Initialize** that is achieved by using **showAddNewRow** property of **editSettings** in **Grid**. The default value is **false**.

This property helps you to add a new row dynamically and save the record either top or bottom of the **Grid**.

{% highlight html %}

**[JS]**

<div id="Grid"></div> 
 <script type="text/javascript">
$(function () {// Document is ready.
                $("#Grid").ejGrid({
                    dataSource: ej.DataManager(window.gridData).executeLocal(ej.Query().take(10)),
                    **editSettings**: { allowEditing: true, allowAdding: true, allowDeleting: true, rowPosition: "bottom", **showAddNewRow**: true },
                    toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },
                    columns: [
                           { field: "OrderID", isPrimaryKey: true, headerText: "Order ID" },
                           { field: "CustomerID", headerText: 'Customer ID' },
                           { field: "EmployeeID", headerText: 'Employee ID' },
                           { field: "ShipName", headerText: 'Ship Name', width: 150 },
                           { field: "ShipCountry", headerText: 'Ship Country', editType: ej.Grid.EditingType.Dropdown },

                    ],
                });
            });
</script>


{% endhighlight %}



The following screenshot is the output of the above code example.

{% include image.html url="/js/Grid/Concepts-and-Features/Editing_images/Editing_img29.png" Caption="Grid with new row"%}

