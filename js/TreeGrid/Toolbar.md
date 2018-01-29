---
layout: post
title: Toolbar
description: toolbar
platform: js
control: TreeGrid
documentation: ug
api: /api/js/ejtreegrid
---
# Toolbar

In TreeGrid we can show/hide the Toolbar by using the [`showToolbar`](/api/js/ejtreegrid#members:toolbarsettings-showtoolbar "toolbarSettings.showToolbar") property of [`toolbarSettings`](/api/js/ejtreegrid#members:toolbarsettings). We can add default toolbar items by [`toolbarItems`](/api/js/ejtreegrid#members:toolbarsettings-toolbaritems "toolbarSettings.toolbarItems"). User can also create a custom toolbar items by using the [`customToolbarItems`](/api/js/ejtreegrid#members:toolbarsettings-customtoolbaritems "toolbarSettings.customToolbarItems").

## Default Toolbar Items
Using TreeGrid default toolbar items we can perform below operations.

* **Add**: To add new task.

* **Edit**:To edit a selected task.

* **Delete**: To delete a selected task.
		   
* **Cancel**: To cancel the edited changes in a task.
		   
* **Update**: To save the edited changes in a task.
		   
* **ExpandAll**: To expand all the TreeGrid rows.
		   
* **CollapseAll**: To collapse all the TreeGrid rows.
		   
* **PdfExport**: To export TreeGrid in PDF format.
		   
* **ExcelExport**: To export TreeGrid in Excel format.

* **Search**: To search the TreeGrid content.

We can enable TreeGrid toolbar by using below code example:
{% highlight js %}
    $("#TreeGridContainer").ejTreeGrid(
    //...
    toolbarSettings: {
        showToolbar: true,
        toolbarItems: [
            ej.TreeGrid.ToolbarItems.Add,
            ej.TreeGrid.ToolbarItems.Edit,
            ej.TreeGrid.ToolbarItems.Delete,
            ej.TreeGrid.ToolbarItems.Update,
            ej.TreeGrid.ToolbarItems.Cancel,
            ej.TreeGrid.ToolbarItems.ExpandAll,
            ej.TreeGrid.ToolbarItems.CollapseAll,
	    ej.TreeGrid.ToolbarItems.PdfExport,
            ej.TreeGrid.ToolbarItems.ExcelExport
        ],
    }
    //...
    });

{% endhighlight %}
The following screenshot displays the toolbar option in TreeGrid control.

![](/js/TreeGrid/Toolbar_images/Toolbar_img1.png)

N> To perform add, edit, delete, cancel and update using Toolbar items we need to enable add/edit/delete using the [`editSettings`](https://help.syncfusion.com/api/js/ejtreegrid#members:editsettings "editSettings").
  
## Custom Toolbar Items

CustomToolbarItems allows us to insert custom icons and custom template in TreeGrid toolbar. By using below properties we can customize TreeGrid toolbar as per our requirement.

* [`text`](/api/js/ejtreegrid#members:toolbarsettings-customtoolbaritems-text "toolbarSettings.customToolbarItems.text"): To insert the custom icons in toolbar using CSS class name selector.

* [`templateID`](/api/js/ejtreegrid#members:toolbarsettings-customtoolbaritems-templateid "toolbarSettings.customToolbarItems.templateID"): To insert the custom icons in toolbar using script templates. Using this property we can bind HTML elements and other EJ controls to TreeGrid toolbar.

* [`tooltipText`](/api/js/ejtreegrid#members:toolbarsettings-customtoolbaritems-tooltiptext "toolbarSettings.customToolbarItems.tooltipText"): Displays tooltip text for the custom icons.

To insert EJ Controls in TreeGrid toolbar we need to initiate the control in [`create`](https://help.syncfusion.com/api/js/ejtreegrid#events:create "create") client-side event. In [`toolbarClick`](https://help.syncfusion.com/api/js/ejtreegrid#events:toolbarclick "toolbarclick") client-side event we can bind actions to the custom toolbar items.

{% highlight html %}
    <div id="TreeGridContainer" style="height:400px;width:100%"></div>           
    <script id="ColumnVisibility" type="text/x-jsrender">
        <input id="dropdownContainer" />
    </script>
    <script type="text/javascript">     
        $(function () {
            $("#TreeGridContainer").ejTreeGrid({               
                 toolbarClick: function (args) {
                    if (args.itemName == "Reset") {
                       //we can bind the custom actions here
                    }
                },               
                toolbarSettings: {
                    showToolbar: true,
                     customToolbarItems: [
		    {templateID: "#ColumnVisibility",tooltipText:"Column Visibility" },
		    {text:"Reset",tooltipText:"Reset"}],
                },               
                create: function (args) {
		    //Here we can append custom EJ controls
                    $("#dropdownContainer").ejDropDownList({
					});
                }
            })
        });
    </script>
    <style type="text/css" class="cssStyles">    
        #TreeGridContainer_ColumnVisibility {
            padding-top: 2px;
            padding-bottom: 0px;
        }
        .Reset:before {
            content: "\e677";
        }
    </style>
	{% endhighlight %}
![](/js/TreeGrid/Toolbar_images/Toolbar_img2.png)

[Click](http://js.syncfusion.com/demos/web/#!/bootstrap/treegrid/toolbartemplate) here to view the demo sample for custom toolbar item