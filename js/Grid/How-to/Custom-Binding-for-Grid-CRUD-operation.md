---
layout: post
title: Custom-Binding-for-Grid-CRUD-operation
description: custom binding for grid crud operation
platform: aspnet
control: Grid
documentation: ug
---

### Custom Binding for Grid CRUD operation

In Grid control we have used DataManager for data processing. The adaptors of dataManager are customizable that we can extend it for custom Binding with server-side for Grid CRUD operation.

For instance let me bind data to Grid using `remoteSaveAdaptor` and extend it to modify its update method to bind edited record values of Grid as `FormCollection` in server-side



{% highlight html %}



&lt;div id="Grid"&gt;&lt;/div&gt;




&lt;script type="text/javascript"&gt;

    $(function () {



           // the datasource "window.gridData" is referred from jsondata.min.js

           $("#Grid").ejGrid({

               dataSource: ej.DataManager({ json: window.gridData, updateUrl: "Home/Update", insertUrl: "Home/Insert", removeUrl: "Home/Delete", adaptor: "remoteSaveAdaptor" }),

                allowPaging: true,

                editSettings: { allowEditing: true, allowAdding: true, allowDeleting: true },

                toolbarSettings: { showToolbar: true, toolbarItems: [ej.Grid.ToolBarItems.Add, ej.Grid.ToolBarItems.Edit, ej.Grid.ToolBarItems.Delete, ej.Grid.ToolBarItems.Update, ej.Grid.ToolBarItems.Cancel] },

                columns: [

                        { field: "OrderID", isPrimaryKey: true, headerText: "Order ID", textAlign: ej.TextAlign.Right, validationRules: { required: true, number: true }, width: 90 },

                        { field: "EmployeeID", headerText: 'Employee ID',  textAlign: ej.TextAlign.Right, width: 80, validationRules: { number: true } },

                        { field: "Freight", headerText: 'Freight', textAlign: ej.TextAlign.Right, editType: ej.Grid.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] }, width: 80, format: "{0:C}" },

                        { field: "ShipName", headerText: 'Ship Name', width: 150 }

                ],

            load: function(args){

                    this.model.dataSource.adaptor = new adaptor();

             }          

            });



    var adaptor = new ej.remoteSaveAdaptor().extend({

        insert: function (dm, data, tableName) {

            return {

                url: dm.dataSource.insertUrl,

                dataType: 'json',

                contentType: "application/x-www-form-urlencoded; charset=utf-8",

                data: $("#GridEditForm").serialize()

            };

        },

        update: function (dm, keyField, value, tableName) {

            return {

                type: "POST",

                url: dm.dataSource.updateUrl+"?id="+value.OrderID,

                dataType: 'json',

                contentType: "application/x-www-form-urlencoded; charset=utf-8",

                data: $("#GridEditForm").serialize()

            };

        },

    })





       });



&lt;/script&gt;
{% endhighlight %}



The output is as follows:

![]("/js/Grid/How-to/DCustom-Binding-for-Grid-CRUD-operation_images/Custom-Binding-for-Grid-CRUD-operation_img1.png")
