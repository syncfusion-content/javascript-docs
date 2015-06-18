---
layout: post
title: Disable-double-click-edit
description: disable double-click edit
platform: js
control: Grid
documentation: ug
---

### Disable double-click edit

The **allowEditOnDblClick** property can be set as **True** to enable editing the record by double-clicking it. When it is set as **False**, it cannot be edited by double-clicking it. In that case, you can edit the record by using the **Toolbar** option only.

{% highlight html %}



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
                    allowEditOnDblClick : false
                },
                allowPaging: true,
                pageSettings: { pageSize: 6 },
                columns: [
                    { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: "right" },
                    { field: "CustomerID", headerText: "Customer ID", editType: ej.Grid.EditingType.String },
                    { field: "EmployeeID", headerText: "Employee ID", textAlign: "right", editType: ej.Grid.EditingType.Numeric },
                    { field: "ShipCity", headerText: "Ship City",editType: ej.Grid.EditingType.Dropdown }
                ]
            });
        });
    </script>



{% endhighlight %}



The following output is displayed as a result of the above code example.

{% include image.html url="/js/Grid/How-to/Disable-double-click-edit_images/Disable-double-click-edit_img1.png" Caption="Disable double-click edit"%}

