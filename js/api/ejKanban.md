---
layout: post
title: Properties, Methods and Events of ejKanban Widget
description: Members,Methods,Events available in ejKanban
documentation: API
platform: js
keywords: Kanban, ejKanban, syncfusion, Kanban api
---

# ejKanban

The Kanban can be easily configured to the DOM element, such as div. you can create a Kanban with a highly customizable look and feel.

#### Syntax

{% highlight js %}

    $(element).ejKanban();

{% endhighlight %}

#### Example

{% highlight html %}
   
    <div id="Kanban"></div>
    <script>
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    // Create Kanban
    $("#Kanban").ejKanban({
        dataSource: window.kanbandata,
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "In Progress", key: "InProgress" },
            { headerText: "Testing", key: "Testing" },
            { headerText: "Done", key: "Close" }
        ]
    });
    </script>
    
{% endhighlight %}

#### Requires
{:.require}

* module:jQuery
* module:jquery.easing.1.3.min.js
* module:jsrender.min.js
* module:ej.globalize.min.js
* module:ej.core.min.js
* module:ej.data.min.js
* module:ej.touch.min.js
* module:ej.kanban.min.js
* module:ej.scroller.min.js
* module:ej.waitingpopup.min.js
* module:ej.button.min.js
* module:ej.dialog.min.js
* module:ej.dropdownlist.min.js
* module:ej.datepicker.min.js
* module:ej.datetimepicker.min.js
* module:ej.editor.min.js
* module:ej.checkbox.min.js
* module:ej.tab.min.js
* module:ej.splitbutton.js
* module:ej.rte.min.js
* module:ej.toolbar.min.js
* module:ej.menu.min.js

## Members

### allowDragAndDrop `boolean`
{:#members:allowdraganddrop}

Gets or sets a value that indicates whether to enable allowDragAndDrop behavior on Kanban.

#### Default Value

* true

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban({
            dataSource: data,
            allowDragAndDrop: true,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>

{% endhighlight %}

### allowTitle `boolean`
{:#members:allowtitle}

To enable or disable the title of the card.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban({
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            allowTitle: true,
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>

{% endhighlight %}

### swimlaneSettings `object`
{:#members:swimlanesettings}

Customize the settings for swimlane.

#### Default Value:

* Object

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban({
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            swimlaneSettings: {
                showCount: true
            },
        });
    });
    </script>

{% endhighlight %}

### swimlaneSettings.showCount `boolean`
{:#members:swimlanesettings-showcount}

To enable or disable items count in swimlane

#### Default Value:

* true

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban({
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            swimlaneSettings: {
                showCount: true
            },
        });
    });
    </script>

{% endhighlight %}

### allowToggleColumn `boolean`
{:#members:allowtogglecolumn}

To enable or disable the column expand /collapse.

#### Default Value:

* false

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Text: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Text: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Text: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Text: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                allowToggleColumn: true,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Text",
                },
            });
    });
    </script>

{% endhighlight %}

### allowSearching `boolean`
{:#members:allowsearching}

To enable Searching operation in Kanban.

#### Default Value:

* false

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                allowSearching: true,
            });
    });
    </script>
    
{% endhighlight %}

### allowSelection `boolean`
{:#members:allowselection}

Gets or sets a value that indicates whether to enable allowSelection behavior on Kanban.User can select card and the selected card will be highlighted on Kanban.

#### Default Value:

* true

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            allowSelection: true,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>
    
{% endhighlight %}

### allowHover `boolean`
{:#members:allowhover}

Gets or sets a value that indicates whether to allow card hover actions.

#### Default Value

* true

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            allowHover: true,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>
    
{% endhighlight %}

### allowKeyboardNavigation `boolean`
{:#members:allowkeyboardnavigation}

To allow keyboard navigation actions.

#### Default Value:

* false

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                allowKeyboardNavigation: true,
                columns: [
                        { headerText: "Backlog", key: "Open"},
                        { headerText: "In Progress", key: "InProgress"},
                        { headerText: "Testing", key: "Testing"},
                        { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                },
            });
        $(document).on("keydown", function (e) {
            //if (e.keyCode === 69) { // j- key code.
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#Kanban").focus();
            }
        });
    });
    </script>

{% endhighlight %}

### allowScrolling `boolean`
{:#members:allowscrolling}

Gets or sets a value that indicates whether to enable the scrollbar in the Kanban and view the card by scroll through the Kanban manually.

#### Default Value:

* false

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                keyField: "Status",
                allowScrolling: true,
                scrollSettings: {
                    height: 400,
                    width: 700
                }
            }
        );
    });
    </script>

{% endhighlight %}

### allowPrinting `boolean`
{:#members:allowprinting}

Gets or sets a value that indicates whether to define the number of pages to print.

#### Default Value:

* false

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                keyField: "Status",
                allowPrinting: true,
            }
        );
    });
    </script>

     
{% endhighlight %}

### contextMenuSettings `object`
{:#members:contextmenusettings}

Gets or sets an object that indicates whether to customize the context menu behavior of the Kanban.

#### Default Value:

* Object

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
    { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
    { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
    { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
    { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
    { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
    { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true,

            }
        });
    });
    </script>

{% endhighlight %}

### contextMenuSettings.enable `boolean`
{:#members:contextmenusettings-enable}

To enable Context menu,All default context menu will show.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
     { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
     { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
     { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
     { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
     { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
     { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true
            }
        });
    });
    </script>

{% endhighlight %}

### contextMenuSettings.disableDefaultItems `array`
{:#members:contextmenusettings-disabledefaultitems}

Gets or sets a value that indicates the list of items needs to be disable from default context menu

#### Default Value:

* array

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
        { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
        { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true,
                disableDefaultItems: [ej.Kanban.MenuItem.AddCard]
            },
            editSettings: {
                allowAdding: true
            }
        });
    });
    </script>

{% endhighlight %}

### contextMenuSettings.menuItems `array`
{:#members:contextmenusettings-menuitems}

sets a value that indicates whether to add default Menu items.

#### Default Value:

* array

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
    var data = ej.DataManager(window.kanbandata);
    $("#Kanban").ejKanban(
    {
        dataSource: data,			    
        allowScrolling:true,
        scrollSettings:{  
            height:500,
            width:900,
        },
        columns: [
            { headerText: "Backlog", key: "Open" },
            { headerText: "In Progress", key: "InProgress" },
            { headerText: "Testing", key: "Testing" },
            { headerText: "Done", key: "Close" }
        ],
        keyField: "Status",
        allowTitle: true,
        fields: {
            primaryKey: "Id",
            swimlaneKey: "Assignee",
            content: "Summary",
        },
        contextMenuSettings: {
            enable: true,
             menuItems:[{ menuItem: "Move Right"},{menuItem: "Move Left"  }],
        }
    });
    });
    </script>
   
{% endhighlight %}

### contextMenuSettings.customMenuItems `array`
{:#members:contextmenusettings-custommenuitems}

Gets or sets a value that indicates whether to add custom contextMenu items. 

#### Default Value:

* array

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true,
                customMenuItems: [
                          { text: "Menu1" },
                          { text: "Menu2", target: ej.Kanban.Target.Header },
                          { text: "Menu3", target: "" }
                ],
            }
        });
    });
    </script>

{% endhighlight %}

### contextMenuSettings.customMenuItems.target `enum`
{:#members:contextmenusettings-custommenuitems-target}

<ts name="ej.Kanban.Target"/>

Sets context menu to target element.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Header</td>
<td class="description">Sets context menu to Kanban header</td>
</tr>
<tr>
<td class="name">Content</td>
<td class="description">Sets context menu to Kanban content</td>
</tr>
<tr>
<td class="name">Card</td>
<td class="description">Sets context menu to Kanban card</td>
</tr>
<tr>
<td class="name">All</td>
<td class="description">Sets context menu to Kanban</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.Kanban.Target.All

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true,
                customMenuItems: [
                          { text: "Menu1" },
                          { text: "Menu2", target: ej.Kanban.Target.Header },
                          { text: "Menu3", target: "card" },
                          { text: "Menu4", target: "" }
                ],
            }
        });
    });
    </script>

{% endhighlight %}

### contextMenuSettings.customMenuItems.text `string`
{:#members:contextmenusettings-custommenuitems-text}

Gets the name to custom menu.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            contextMenuSettings: {
                enable: true,
                customMenuItems: [
                          { text: "Menu1" },
                          { text: "Menu2" },
                          { text: "Menu3" }
                ]
            }
        });
    });
    </script>

    
{% endhighlight %}

### contextMenuSettings.customMenuItems.template `String`
{:#members:contextmenusettings-custommenuitems-template}

Gets the template to render custom menu.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <ul id="contexttemplate">
        <li><a>hi</a></li>
        <li><a>hi</a></li>
        <li><a>hi</a></li>
    </ul>
    <ul id="contexttemplate1">
        <li><a>hello</a></li>
        <li><a>hello</a></li>
        <li><a>hello</a></li>
    </ul>
    <ul id="contexttemplate2">
        <li><a>hihello</a></li>
        <li><a>hihello</a></li>
        <li><a>hihello</a></li>
    </ul>
    <script type="text/javascript">
        window.kanbandata = [
             { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
             { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
             { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
             { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
             { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
             { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
        ];
        $(function () {
            var data = ej.DataManager(window.kanbandata);
            $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                contextMenuSettings: {
                    enable: true,
                    customMenuItems: [
                              { text: "Menu1", template: "#contexttemplate" },
                              { text: "Menu2", template: "#contexttemplate1" },
                              { text: "Menu3", template: "#contexttemplate2" }
                    ],
                }
            });
        });
    </script>

{% endhighlight %}

### columns `array`
{:#members:columns}

Gets or sets an object that indicates to render the Kanban with specified columns.

#### Default Value:

* array

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
        { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
        { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            keyField: "Status"
        }
    );
    });
    </script>

{% endhighlight %}

### columns.headerText `string`
{:#members:columns-headertext}

Gets or sets an object that indicates to render the Kanban with specified columns header text.

#### Default Value

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            keyField: "Status"
        }
    );
    });
    </script>

{% endhighlight %}

### columns.key `string/number`
{:#members:columns-key}

Gets or sets an object that indicates to render the Kanban with specified columns key.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            keyField: "Status"
        }
    );
    });
    </script>

 {% endhighlight %}

### columns.isCollapsed `boolean`
{:#members:columns-iscollapsed}

To set column collapse or expand state

#### Default Value

* false

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                allowToggleColumn: true,
                columns: [
                        { headerText: "Backlog", key: "Open", isCollapsed: false },
                        { headerText: "In Progress", key: "InProgress", isCollapsed: false },
                        { headerText: "Testing", key: "Testing", isCollapsed: false },
                        { headerText: "Done", key: "Close", isCollapsed: false }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
            });
    });
    </script>

 {% endhighlight %}

### columns.constraints `object`
{:#members:columns-constraints}

To customize the column constraints whether the constraints contains minimum limit or maximum limit or both.

#### Default Value

* object

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                enableTotalCount: true,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress", constraints: { min: 1, max: 2 }, },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                allowTitle: true,
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSelection: false
            });
        $("#constraint").ejDropDownList({ width: "120px", change: "onConstraintTypeChange", selectedItemIndex: 0 });
    });
    </script>

{% endhighlight %}       
 
### columns.constraints.type `string`
{:#members:columns-constraints-type}

It is used to specify the type whether the constraints based on column or swimlane.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "InProgress", Summary: "Task 6", Assignee: "Nancy" },
         { Id: 7, Status: "Close", Summary: "Task 7", Assignee: "Nancy" },
         { Id: 8, Status: "Testing", Summary: "Task 8", Assignee: "Robert" },
         { Id: 9, Status: "Close", Summary: "Task 9", Assignee: "Nancy" },
         { Id: 10, Status: "Testing", Summary: "Task 10", Assignee: "Robert" },
         { Id: 11, Status: "Testing", Summary: "Task 11", Assignee: "Robert" },
         { Id: 12, Status: "Close", Summary: "Task 12", Assignee: "Andrew" },
         { Id: 13, Status: "Testing", Summary: "Task 13", Assignee: "Nancy" },
         { Id: 14, Status: "Testing", Summary: "Task 14", Assignee: "Robert" },
         { Id: 15, Status: "Close", Summary: "Task 15", Assignee: "Nancy" },

    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,

                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress", constraints: { type: ej.Kanban.Type.Swimlane, min: 1, max: 2 }, },
                     { headerText: "Testing", key: "Testing", constraints: { type: ej.Kanban.Type.Column, max: 5 }, },
                     { headerText: "Done", key: "Close", constraints: { min: 2, max: 7 }, },
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
            }
        );
    });
    </script>

{% endhighlight %}
 
### columns.constraints.min `number`
{:#members:columns-constraints-min}

It is used to specify the minimum amount of card in particular column cell or swimlane cell can hold.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "InProgress", Summary: "Task 6", Assignee: "Nancy" },
         { Id: 7, Status: "Close", Summary: "Task 7", Assignee: "Nancy" },
         { Id: 8, Status: "Testing", Summary: "Task 8", Assignee: "Robert" },
         { Id: 9, Status: "Close", Summary: "Task 9", Assignee: "Nancy" },
         { Id: 10, Status: "Testing", Summary: "Task 10", Assignee: "Robert" },
         { Id: 11, Status: "Testing", Summary: "Task 11", Assignee: "Robert" },
         { Id: 12, Status: "Close", Summary: "Task 12", Assignee: "Andrew" },
         { Id: 13, Status: "Testing", Summary: "Task 13", Assignee: "Nancy" },
         { Id: 14, Status: "Testing", Summary: "Task 14", Assignee: "Robert" },
         { Id: 15, Status: "Close", Summary: "Task 15", Assignee: "Nancy" },

    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,

                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress", constraints: { type: ej.Kanban.Type.Swimlane, min: 1, max: 2 }, },
                     { headerText: "Testing", key: "Testing", constraints: { type: ej.Kanban.Type.Column, max: 5 }, },
                     { headerText: "Done", key: "Close", constraints: { min: 2, max: 7 }, },
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
            }
        );
    });
    </script>

 {% endhighlight %}

### columns.constraints.max `number`
{:#members:columns-constraints-max}

It is used to specify the maximum amount of card in particular column cell or swimlane cell can hold.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "InProgress", Summary: "Task 6", Assignee: "Nancy" },
         { Id: 7, Status: "Close", Summary: "Task 7", Assignee: "Nancy" },
         { Id: 8, Status: "Testing", Summary: "Task 8", Assignee: "Robert" },
         { Id: 9, Status: "Close", Summary: "Task 9", Assignee: "Nancy" },
         { Id: 10, Status: "Testing", Summary: "Task 10", Assignee: "Robert" },
         { Id: 11, Status: "Testing", Summary: "Task 11", Assignee: "Robert" },
         { Id: 12, Status: "Close", Summary: "Task 12", Assignee: "Andrew" },
         { Id: 13, Status: "Testing", Summary: "Task 13", Assignee: "Nancy" },
         { Id: 14, Status: "Testing", Summary: "Task 14", Assignee: "Robert" },
         { Id: 15, Status: "Close", Summary: "Task 15", Assignee: "Nancy" },

    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,

                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress", constraints: { type: ej.Kanban.Type.Swimlane, min: 1, max: 2 }, },
                     { headerText: "Testing", key: "Testing", constraints: { type: ej.Kanban.Type.Column, max: 5 }, },
                     { headerText: "Done", key: "Close", constraints: { min: 2, max: 7 }, },
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
            }
        );
    });
    </script>

 {% endhighlight %}
 
### columns.headerTemplate `string`
{:#members:columns-headertemplate}

Gets or sets a value that indicates to add the template within the header element.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <div id="calender">
    <span class="e-calender e-icon headericon"></span>
    In Progress
    </div>
    <div id="userlogin">
    <span class="e-userlogin e-icon employee"></span>
    Testing
    </div>
    <div id="image">
    <img src="themes/images/kanban/9.png">
    Done
    </div>
    <div id="check">
    <input id="checksync" type="checkbox" />
    Backlog
    </div>
    <style type="text/css" class="cssStyles">
    img {
        height: 14px;
        width: 14px;
    }
    </style>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" },
       { Id: 3, Status: "Close", Summary: "Task 3", Assignee: "Andrew" },
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open", headerTemplate: "#check" },
                    { headerText: "In Progress", key: "InProgress", headerTemplate: "#calender" },
                    { headerText: "Testing", key: "Testing", headerTemplate: "#userlogin" },
                    { headerText: "Done", key: "Close", headerTemplate: "#image" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
            });
    });
    $("#checksync").ejCheckBox();
    </script>

    
 {% endhighlight %}
 
### columns.width `string/number`
{:#members:columns-width}

Gets or sets an object that indicates to render the Kanban with specified columns width.

#### Default Value:

* null

#### Example

{% highlight html %}
      
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
         { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open", width: 80 },
                { headerText: "Validated", key: "Validate", width: 80 },
                { headerText: "Currently Working", key: "InProgress", width: 80 },
                { headerText: "Testing", key: "Testing", width: 80 },
                { headerText: "Done", key: "Close", width: 70 }
            ],
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            keyField: "Status"
        }
    );
    });
    </script>

{% endhighlight %}

### columns.visible `boolean`
{:#members:columns-visible}

Gets or sets an object that indicates to render the Kanban with specified columns visible.

#### Default Value:

* true

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
                    { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
                    { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
                    { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
                    { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
                    { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
                    { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open", visible: false },
                { headerText: "In Progress", key: "InProgress", visible: true },
                { headerText: "Testing", key: "Testing", visible: false },
                { headerText: "Done", key: "Close", visible: true }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        }
    );
    });
    </script>

 {% endhighlight %}

### columns.showAddButton `boolean`
{:#members:columns-showaddbutton}

Gets or sets an object that indicates to render the Kanban with specified columns to show the add button.

#### Default Value:

* false

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
                    { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
                    { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
                    { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
                    { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
                    { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
                    { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open", showAddButton: true },
                    { headerText: "In Progress", key: "InProgress", showAddButton: true },
                    { headerText: "Testing", key: "Testing", showAddButton: true },
                    { headerText: "Done", key: "Close", showAddButton: true }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    imageUrl: "ImgUrl"
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String, validationRules: { required: true, number: true } },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea, validationRules: { required: true } }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },
            });
    });
    </script>

 {% endhighlight %}
 
### cardSettings `object`
{:#members:cardsettings}

Gets or sets an object that indicates whether to Customize the card based on the Mapping Fields.

#### Default Value

* Object

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script id="cardtemplate" type="text/x-jsrender">
    <table>
        <tr>
            <td class="photo">
                <img src="../themes/images/kanban/{{:Priority}}.png">
            </td>

            <td class="details">
                <table>
                    <colgroup>
                        <col width="30%">
                        <col width="70%">
                    </colgroup>
                    <tbody>
                        <tr>
                            <td class="CardHeader">Name: </td>
                            <td>{{:Assignee}}</td>
                        </tr>
                        <tr>
                            <td class="CardHeader">Task: </td>
                            <td>{{:Type}}</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
    </table>
    </script>
    <style type="text/css">
    .details > table {
        margin-left: 10px;
        border-collapse: separate;
        border-spacing: 7px;
        width: 100%;
    }

    .photo {
        padding-left: 6px;
    }

    .CardHeader {
        font-weight: bolder;
    }
    </style>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Type: "UG" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Type: "Improvement" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Type: "Issue", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    color: "Type",
                },
                cardSettings: {
                    template: "#cardtemplate",
                    colorMapping: {
                        "#cb2027": "Issue,Story",
                        "#67ab47": "Improvement",
                        "#fbae19": "Epic",
                        "#6a5da8": "UG"
                    }
                },

            });
    });
    </script>
       
{% endhighlight %}

### cardSettings.template `string`
{:#members:cardsettings-template}

Gets or sets a value that indicates to add the template of card .

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script id="cardtemplate" type="text/x-jsrender">
    <table>
        <tr>
            <td class="photo">
                <img src="../themes/images/kanban/{{:Priority}}.png">
            </td>

            <td class="details">
                <table>
                    <colgroup>
                        <col width="30%">
                        <col width="70%">
                    </colgroup>
                    <tbody>
                        <tr>
                            <td class="CardHeader">Name: </td>
                            <td>{{:Assignee}}</td>
                        </tr>
                        <tr>
                            <td class="CardHeader">Task: </td>
                            <td>{{:Type}}</td>
                        </tr>
                    </tbody>
                </table>
            </td>
        </tr>
    </table>
    </script>
    <style type="text/css">
    .details > table {
        margin-left: 10px;
        border-collapse: separate;
        border-spacing: 7px;
        width: 100%;
    }
    .photo {
        padding-left: 6px;
    }
    .CardHeader {
        font-weight: bolder;
    }
    </style>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Type: "UG" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Type: "Improvement" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Type: "Issue", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    color: "Type",
                },
                cardSettings: {
                    template: "#cardtemplate",
                },
            });
    });
    </script>

{% endhighlight %}
       
### cardSettings.colorMapping `object`
{:#members:cardsettings-colormapping}

To customize the card border color based on assigned task. Colors and corresponding values defined  here will be mapped with colorField mapped data source column.

#### Default Value

* Object

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Type: "UG" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Type: "Improvement" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Type: "Issue", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    color: "Type",
                },
                cardSettings: {
                    colorMapping: {
                        "#cb2027": "Issue,Story",
                        "#67ab47": "Improvement",
                        "#fbae19": "Epic",
                        "#6a5da8": "UG"
                    }
                },

            });
    });
    </script>
  
{% endhighlight %}

### customToolbarItems `Array`
{:#members:customtoolbaritems}

Gets or sets a value that indicates whether to add customToolbarItems within the toolbar to perform any action in the Kanban.

#### Default Value:
{:.param}
* []

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script id="Delete" type="text/x-jsrender">
    <a class="e-customdelete  e-icon" />
    </script>
    <style type="text/css" class="cssStyles">
    .e-customdelete:before {
        content: "\e800";
        line-height: 26px;
        min-height: 26px;
        min-width: 14px;
        display: inline-block;
    }
    </style>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                customToolbarItems: [
                      {
                          template: "#Delete"
                      }
                ],
                allowTitle: true,
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    imageUrl: "ImgUrl"
                },
                toolbarClick: function (args) {
                    if (args.itemName == "Delete" && this.element.find(".e-kanbancard").hasClass("e-cardselection")) {
                        var selectedcard = this.element.find(".e-cardselection");
                        this.KanbanEdit.deleteCard(selectedcard.attr("id"));
                    }
                },
            });
    });
    </script>

{% endhighlight %}

### customToolbarItems.template `string`
{:#members:customtoolbaritems-template}

Gets the template to render customToolbarItems.

#### Default Value:
{:.param}
* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script id="Delete" type="text/x-jsrender">
    <a class="e-customdelete  e-icon" />
    </script>
    <style type="text/css" class="cssStyles">
    .e-customdelete:before {
        content: "\e800";
        line-height: 26px;
        min-height: 26px;
        min-width: 14px;
        display: inline-block;
    }
    </style>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                customToolbarItems: [
                      {
                          template: "#Delete"
                      }
                ],
                allowTitle: true,
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                toolbarClick: function (args) {
                    if (args.itemName == "Delete" && this.element.find(".e-kanbancard").hasClass("e-cardselection")) {
                        var selectedcard = this.element.find(".e-cardselection");
                        this.KanbanEdit.deleteCard(selectedcard.attr("id"));
                    }
                },
            });
    });
    </script>
    
{% endhighlight %}

### cssClass `string`
{:#members:cssclass}

Gets or sets a value that indicates to render the Kanban with custom theme.

#### Default Value:

* ""

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <style type="text/css">
    .gradient-green {
        font-family: cursive;
    }
        .gradient-green .e-swimlanerow {
            background: none repeat scroll 0 0 #71A409;
        }
    </style>
    <script>
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
        {
            dataSource: data,
            cssClass: "gradient-green",
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" }
            ],
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
            keyField: "Status",
        }
    );
    });
    </script>

{% endhighlight %}
 
### dataSource `object`
{:#members:datasource}

Gets or sets the data to render the Kanban with card.

#### Default Value:

* null
 
#### Example

{% highlight html %}
    
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" }
            ],
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
            keyField: "Status",
        }
    );
    });
    </script>

{% endhighlight %}

### enableTouch `Boolean`
{:#members:enabletouch}

To perform kanban functionalities with touch interaction.

#### Default Value:

* true

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                enableTouch:false,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },
            });
    });
    </script>
    
{% endhighlight %}

### enableRTL `boolean`
{:#members:enablertl}

Align content in the Kanban control from right to left by setting the property as true.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                enableRTL: true,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },
            });
    });
    </script>
    
{% endhighlight %}

### enableTotalCount `boolean`
{:#members:enabletotalcount}

To show Total count of cards in each column 
    
#### Default Value:

* false

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                enableTotalCount: true,
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },

            });
    });
    </script>

{% endhighlight %}

### editSettings `object`
{:#members:editsettings}

Get or sets an object that indicates whether to customize the editing behavior of the Kanban.

#### Default Value:

* Object

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                actionComplete: "complete",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },
            }
        );
    });
    </script>
  
{% endhighlight %}

### editSettings.allowEditing `boolean`
{:#members:editsettings-allowediting}

Gets or sets a value that indicates whether to enable the editing action in cards of Kanban.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                actionComplete: "complete",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowEditing: true
                },
            }
        );
    });
    </script>
       
{% endhighlight %}

### editSettings.allowAdding `boolean`
{:#members:editsettings-allowadding}

Gets or sets a value that indicates whether to enable the adding action in cards behavior on Kanban.

#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                actionComplete: "complete",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowAdding: true
                },
            }
        );
    });
    </script>
 
{% endhighlight %}

### editSettings.dialogTemplate `String`
{:#members:editsettings-dialogtemplate}

This specifies the id of the template.which is require to be edited using the Dialog Box

#### Default Value:

* null

#### Example

{% highlight html %}
               
    <div id="Kanban"></div>
    <script id="template" type="text/template">
    <table>
        <tr>
            <td style="text-align: right;">Id
            </td>
            <td style="text-align: left">
                <input id="Id" name="Id" value="{{: Id}}" class="e-field e-ejinputtext valid e-disable" disabled="disabled" />
            </td>
            <td style="text-align: right;">Status
            </td>
            <td style="text-align: left">
                <input id="Status" name="Status" value="{{: Status}}" class="e-field e-ejinputtext valid" />
            </td>
        </tr>
    </table>
    </script>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.DialogTemplate,
                    dialogTemplate: "#template",
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editMode `enum`
{:#members:editsettings-editmode}

<ts name="ej.Kanban.EditMode"/>

Get or sets an object that indicates whether to customize the editMode of the Kanban.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Dialog</td>
<td class="description">Creates Kanban with editMode as Dialog</td>
</tr>
<tr>
<td class="name">DialogTemplate</td>
<td class="description">Creates Kanban with editMode as DialogTemplate</td>
</tr>
<tr>
<td class="name">ExternalForm</td>
<td class="description">Creates Kanban with editMode as ExternalForm</td>
</tr>
<tr>
<td class="name">ExternalFormTemplate</td>
<td class="description">Creates Kanban with editMode as ExternalFormTemplate</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.Kanban.EditMode.Dialog

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editItems `array`
{:#members: editsettings-edititems}

Get or sets an object that indicates whether to customize the editing fields of Kanban card.

#### Default Value:

* Array

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editItems.field `string`
{:#members:editsettings-edititems-field}

It is used to map editing field in the card.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editItems.editType `enum`
{:#members:editsettings-edititems-edittype}

<ts name="ej.Kanban.EditingType"/>

It is used to set the particular editType in the card for editing.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">String</td>
<td class="description">Allows to set edit type as string edit type</td>
</tr>
<tr>
<td class="name">Numeric</td>
<td class="description">Allows to set edit type as numeric edit type </td>
</tr>
<tr>
<td class="name">Dropdown</td>
<td class="description">Allows to set edit type as drop down edit type</td>
</tr>
<tr>
<td class="name">DatePicker</td>
<td class="description">Allows to set edit type as date picker edit type</td>
</tr>
<tr>
<td class="name">DateTimePicker</td>
<td class="description">Allows to set edit type as date time picker edit type</td>
</tr>
<tr>
<td class="name">TextArea</td>
<td class="description">Allows to set edit type as text area edit type</td>
</tr>
<tr>
<td class="name">RTE</td>
<td class="description">Allows to set edit type as RTE edit type</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.Kanban.EditingType.String

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editItems.validationRules `object`
{:#members:editsettings-edititems-validationrules}

Gets or sets a value that indicates to define constraints for saving data to the database.

#### Default Value:

* Object

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                                { field: "Id", editType: ej.Kanban.EditingType.String, validationRules: { required: true, number: true } },
                                { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                                { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                                { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] } },
                                { field: "Summary", editType: ej.Kanban.EditingType.TextArea, validationRules: { required: true } }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.editItems.editParams `object`
{:#members:editsettings-edititems-editparams}

It is used to set the particular editparams in the card for editing.

#### Default Value:

* Object

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                actionComplete: "complete",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    title: "Assignee",
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
        );
    })
    </script>
 
{% endhighlight %}

### editSettings.editItems.defaultValue `string/number`
{:#members:editsettings-edititems-defaultvalue}

It is used to specify defaultValue in the card.

#### Default Value

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                actionComplete: "complete",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.Dialog,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String, validationRules: { required: true, number: true } },
                        { field: "Status", editType: ej.Kanban.EditingType.String, defaultValue: "Open" },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 }, validationRules: { range: [0, 1000] } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea, validationRules: { required: true } }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
        );
    })
    </script>

{% endhighlight %}

### editSettings.externalFormTemplate `String`
{:#members:editsettings-externalformtemplate}

This specifies the id of the template which is require to be edited using the External edit form.

#### Default Value:
{:.param}
* null

#### Example
{:.example}

{% highlight html %}   

    <div id="Kanban"></div>
    <script id="template" type="text/template">
    <table>
        <tr>
            <td style="text-align: right;">Id
            </td>
            <td style="text-align: left">
                <input id="Id" name="Id" value="{{: Id}}" class="e-field e-ejinputtext valid e-disable" disabled="disabled" />
            </td>
            <td style="text-align: right;">Status
            </td>
            <td style="text-align: left">
                <input id="Status" name="Status" value="{{: Status}}" class="e-field e-ejinputtext valid" />
            </td>
        </tr>
    </table>
    </script>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.ExternalFormTemplate,
                    externalFormTemplate: "#template",
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}

### editSettings.formPosition `enum`
{:#members:editsettings-formposition}

<ts name="ej.Kanban.FormPosition"/>

This specifies to set the position of an External edit form either in the top-right or bottom of the Kanban.

#### Default Value:

* ej.Kanban.FormPosition.Bottom

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Bottom</td>
<td class="description">Form position is bottom.</td>
</tr>
<tr>
<td class="name">Right</td>
<td class="description">Form position is right.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
        { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
        { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata)
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                editSettings: {
                    editMode: ej.Kanban.EditMode.ExternalForm,
                    formPosition: ej.Kanban.FormPosition.Bottom,
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.String },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }],
                    allowEditing: true,
                    allowAdding: true
                },
            }
          );
    })
    </script>

{% endhighlight %}
            
### fields `object`
{:#members:fields}

To customize field mappings for card , editing title and control key parameters

#### Default Value:

* Object

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Type: "UG", Tags: "Analyze,Requirements", ImgUrl: "../themes/images/kanban/1.png" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Type: "Issue", Tags: "Improvement,Performance", ImgUrl: "../themes/images/kanban/2.png" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Type: "Improvement", Tags: "Improvement,Performance", ImgUrl: "../themes/images/kanban/2.png" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Type: "UG", Tags: "Analyze,Requirements", ImgUrl: "../themes/images/kanban/1.png" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Janet Leverling", Type: "Epic", Tags: "Meeting,Requirments", ImgUrl: "../themes/images/kanban/3.png" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
                tag: "Tags",
                title: "Id",
                color: "Type",
                imageUrl: "ImgUrl",
            },
            cardSettings: {
                colorMapping: {
                    "#cb2027": "Issue,Story",
                    "#67ab47": "Improvement",
                    "#fbae19": "Epic",
                    "#6a5da8": "UG"
                }
            }
        });
    });
    </script>
    
{% endhighlight %}

### fields.primaryKey `string`
{:#members:fields-primarykey}

The primarykey field is get as property of Kanban. And this will used for Drag and drop and editing mainly.

#### Default Value:

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>
     
{% endhighlight %}

### fields.swimlaneKey `string`
{:#members:fields-swimlanekey}

To enable swimlane grouping based on the given key field.

#### Default Value

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
        });
    });
    </script>

{% endhighlight %}

### fields.priority `string`
{:#members:fields-priority}

Priority field has been mapped data source field to maintain card priority

#### Default Value:

* null

#### Example

{% highlight html %}
     
    
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", RankId: 1 },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", RankId: 2 },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", RankId: 2 },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", RankId: 1 },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", RankId: 3 }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                Priority: "RankId",
                content: "Summary",
            },
        });
    });
    </script>

{% endhighlight %}

### fields.content `string`
{:#members:fields-content}

ContentField has been Mapped into card text.

#### Default Value:

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
            },
        });
    });
    </script>
  
{% endhighlight %}

### fields.tag `string`
{:#members:fields-tag}

TagField has been Mapped into card tag.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Estimate: "2.5" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Estimate: "1.5" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Estimate: "1" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Estimate: "3" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert", Estimate: "1.5" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
                tag: "Tags",
            },
        });
    });
    </script>

{% endhighlight %}

### fields.title `string`
{:#members:fields-title}

Title Field has been Mapped to field in datasource for title content. If title field specified , card expand/collapse will be enabled with header and content section

#### Default Value:

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
                title: "Id",
            },
        });
    });
    </script>
     
{% endhighlight %}

### fields.color `string`
{:#members:fields-color}

To customize the card has been Mapped into card color field.

#### Default Value:

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", Type: "UG" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", Type: "Issue" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", Type: "Improvement" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", Type: "UG" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Janet Leverling", Type: "Epic" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
                color: "Type",
            },
            cardSettings: {
                colorMapping: {
                    "#cb2027": "Issue,Story",
                    "#67ab47": "Improvement",
                    "#fbae19": "Epic",
                    "#6a5da8": "UG"
                }
            }
        });
    });
    </script>

{% endhighlight %}

### fields.imageUrl `string`
{:#members:fields-imageurl}

ImageUrlField has been Mapped into card image.

#### Default Value:

* null

#### Example

{% highlight html %}
     
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy", ImgUrl: "../themes/images/kanban/1.png" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew", ImgUrl: "../themes/images/kanban/2.png" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew", ImgUrl: "../themes/images/kanban/2.png" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy", ImgUrl: "../themes/images/kanban/1.png" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Janet Leverling", ImgUrl: "../themes/images/kanban/3.png" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            columns: [
                { headerText: "Backlog", key: "Open" },
                { headerText: "In Progress", key: "InProgress" },
                { headerText: "Testing", key: "Testing" },
                { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            fields: {
                primaryKey: "Id",
                content: "Summary",
                imageUrl: "ImgUrl",
            },

        });
    });
    </script>
     
{% endhighlight %}

### keyField `string`
{:#members:keyfield}

To map datasource field for column values mapping 

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
        { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
        { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
        { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
        { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    content: "Summary",
                },
            });
    });
    </script>
    
{% endhighlight %}

### isResponsive `boolean`
{:#members:isresponsive}

When set to true, adapts the Kanban layout to fit the screen size of devices on which it renders.

#### Default Value:

* false

#### Example

{% highlight html %}     
  
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                minWidth: 400,
                isResponsive: true,
                columns: [
                    { headerText: "Backlog", key: "Open", width: 150 },
                    { headerText: "In Progress", key: "InProgress", width: 120 },
                    { headerText: "Testing", key: "Testing", width: 120 },
                    { headerText: "Done", key: "Close", width: 150 }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
            });
    });
    </script>

{% endhighlight %}

### minWidth `number`
{:#members:minwidth}

Gets or sets a value that indicates whether to set the minimum width of the responsive Kanban while isResponsive property is true.

#### Default Value:

* 0

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
         { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
         { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
         { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
         { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
         { Id: 5, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                minWidth: 400,
                isResponsive: true,
                columns: [
                    { headerText: "Backlog", key: "Open", width: 150 },
                    { headerText: "In Progress", key: "InProgress", width: 120 },
                    { headerText: "Testing", key: "Testing", width: 120 },
                    { headerText: "Done", key: "Close", width: 150 }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
            });
    });
    </script>

{% endhighlight %}

### filterSettings `array`
{:#members:filtersettings}

To customize the filtering behavior based on queries given.

#### Default Value:

* array

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
           { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Janet Leverling" },
           { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
           { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
           { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Janet Leverling" },
           { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
           { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Janet Leverling" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                filterSettings: [
                         { text: "Janet Issues", query: new ej.Query().where("Assignee", "equal", "Janet Leverling"), description: "Displays issues which matches the assignee as 'Janet Leverling'" },
                         { text: "Testing Issues", query: new ej.Query().where("Status", "equal", "Testing"), description: "Display the issues of 'Testing'" }
                ],
            }
        );
    });
    </script>

{% endhighlight %}

### filterSettings.text `string`
{:#members:filtersettings-text}

Gets or sets an object of display name to filter queries.

#### Default Value:

* null

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
           { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Janet Leverling" },
           { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
           { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
           { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Janet Leverling" },
           { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
           { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Janet Leverling" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                filterSettings: [
                         { text: "Janet Issues", query: new ej.Query().where("Assignee", "equal", "Janet Leverling"), description: "Displays issues which matches the assignee as 'Janet Leverling'" },
                         { text: "Testing Issues", query: new ej.Query().where("Status", "equal", "Testing"), description: "Display the issues of 'Testing'" }
                ],
            }
        );
    });
    </script>

{% endhighlight %}

### filterSettings.query `object`
{:#members:filtersettings-query}

Gets or sets an object that Queries to perform filtering

#### Default Value:

* Object

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
           { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Janet Leverling" },
           { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
           { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
           { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Janet Leverling" },
           { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
           { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Janet Leverling" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                filterSettings: [
                         { text: "Janet Issues", query: new ej.Query().where("Assignee", "equal", "Janet Leverling"), description: "Displays issues which matches the assignee as 'Janet Leverling'" },
                         { text: "Testing Issues", query: new ej.Query().where("Status", "equal", "Testing"), description: "Display the issues of 'Testing'" }
                ],
            }
        );
    });
    </script>

{% endhighlight %}

### filterSettings.description `string`
{:#members:filtersettings-description}

Gets or sets an object of tooltip to filter buttons.

#### Default Value:

* null

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
           { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Janet Leverling" },
           { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
           { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
           { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Janet Leverling" },
           { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
           { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Janet Leverling" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                filterSettings: [
                         { text: "Janet Issues", query: new ej.Query().where("Assignee", "equal", "Janet Leverling"), description: "Displays issues which matches the assignee as 'Janet Leverling'" },
                         { text: "Testing Issues", query: new ej.Query().where("Status", "equal", "Testing"), description: "Display the issues of 'Testing'" }
                ],
            }
        );
    });
    </script>
      
{% endhighlight %}

### query `object`
{:#members:query}

ej Query to query database of Kanban.

#### Default Value:

* null

#### Example

{% highlight html %}       

    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
     { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
     { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
     { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" }
    ];
    $(function () {
        var query = ej.Query().select(["Status", "Assignee", "Text"]);
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                keyField: "Status",
                query: query,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" }
                ],
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
            }
        );
    });
    </script>

{% endhighlight %}

### keySettings `object`
{:#members:keysettings}

To change the key in keyboard interaction to Kanban control.

#### Default Value

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
           { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
           { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
           { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
           { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
           { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
           { Id: 6, Status: "Testing", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                allowKeyboardNavigation: true,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                selectionType: "multiple",
                editSettings: {
                    editItems: [
                        { field: "Id", editType: ej.Kanban.EditingType.String },
                        { field: "Status", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Assignee", editType: ej.Kanban.EditingType.Dropdown },
                        { field: "Estimate", editType: ej.Kanban.EditingType.Numeric, editParams: { decimalPlaces: 2 } },
                        { field: "Summary", editType: ej.Kanban.EditingType.TextArea }
                    ],
                    allowEditing: true,
                    allowAdding: true
                },

                keySettings: {
                    focus: "e",
                    insertCard: "45",
                },
            });

        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) {
                $("#Kanban").focus();
            }
        });
    });
    </script>

{% endhighlight %}

### scrollSettings `object`
{:#members:scrollsettings}

Gets or sets an object that indicates whether to customize the scrolling behavior of the Kanban.

#### Default Value:

* Object

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                keyField: "Status",
                allowScrolling: true,
                scrollSettings: {
                    height: 400,
                    width: 700
                }
            }
        );
    });
    </script>

{% endhighlight %}

### scrollSettings.height `string/number`
{:#members:scrollsettings-height}

Gets or sets an object that indicates to render the Kanban with specified scroll height.

#### Default Value:

* 0

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                keyField: "Status",
                allowScrolling: true,
                scrollSettings: {
                    height: 400
                }
            }
        );
    });
    </script>

{% endhighlight %}

### scrollSettings.width `string/number`
{:#members:scrollsettings-width}

Gets or sets an object that indicates to render the Kanban with specified scroll width.

#### Default Value:

* auto

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Done", key: "Close" }
                ],
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                keyField: "Status",
                allowScrolling: true,
                scrollSettings: {
                    height: 400,
                    width: 700
                }
            }
        );
    });
    </script>

{% endhighlight %}

### scrollSettings.allowFreezeSwimlane `boolean`
{:#members:scrollsettings-allowfreezeswimlane}

To allow the Kanban to freeze particular swimlane at the time of scrolling , until scroll reaches next swimlane and it continues.

#### Default Value:

* false

#### Example

{% highlight html %}
  
    <div id="kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
       { Id: 5, Status: "InProgress", Summary: "Task 5", Assignee: "Andrew" },
       { Id: 6, Status: "Close", Summary: "Task 6", Assignee: "Robert" },
       { Id: 7, Status: "Testing", Summary: "Task 7", Assignee: "Michael" },
       { Id: 8, Status: "InProgress", Summary: "Task 8", Assignee: "Steven" },
       { Id: 9, Status: "Close", Summary: "Task 9", Assignee: "Robert" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                allowScrolling: true,
                scrollSettings: {
                    height: 500,
                    width: 800,
                    allowFreezeSwimlane: true,
                },
                columns: [
                    { headerText: "Backlog", key: "Open", width: 250 },
                    { headerText: "In Progress", key: "InProgress", width: 220 },
                    { headerText: "Testing", key: "Testing", width: 220 },
                    { headerText: "Done", key: "Close", width: 250 }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
            });
    });
    </script>
        
{% endhighlight %}

### searchSettings `object`
{:#members:searchsettings}

To customize the searching behavior of the Kanban.

#### Default Value:

* Object

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSearching: true,
                searchSettings: {
                    fields: ["Text", "Id"],
                    key: "",
                    operator: "contains",
                    ignoreCase: true,
                },
            }
        );
    });
    </script>
      
{% endhighlight %}

### searchSettings.fields `array`
{:#members:searchsettings-fields}

To customize the fields the searching operation can be perform.

#### Default Value:

* Array

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSearching: true,
                searchSettings: {
                    fields: ["Summary", "Id"],
                    key: "",
                    operator: "contains",
                    ignoreCase: true,
                },
            }
        );
    });
    </script>
      
{% endhighlight %}

### searchSettings.key `string`
{:#members:searchsettings-key}

To customize the searching string.

#### Default Value:

* ""

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSearching: true,
                searchSettings: {
                    fields: ["Summary", "Id"],
                    key: "",
                    operator: "contains",
                    ignoreCase: true,
                },
            }
        );
    });
    </script>

{% endhighlight %}

### searchSettings.operator `string`
{:#members:searchsettings-operator}

To customize the operator based on searching.

#### Default Value:

* contains

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSearching: true,
                searchSettings: {
                    fields: ["Summary", "Id"],
                    key: "",
                    operator: "contains",
                    ignoreCase: true,
                },
            }
        );
    });
    </script>

{% endhighlight %}

### searchSettings.ignoreCase `boolean`
{:#members:searchsettings-ignorecase}

To customize the ignore case based on searching.

#### Default Value:

* true

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "In Progress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {
                dataSource: data,
                columns: [
                     { headerText: "Backlog", key: "Open" },
                     { headerText: "In Progress", key: "InProgress" },
                     { headerText: "Testing", key: "Testing" },
                     { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    swimlaneKey: "Assignee",
                    content: "Summary",
                },
                allowSearching: true,
                searchSettings: {
                    fields: ["Summary", "Id"],
                    key: "",
                    operator: "contains",
                    ignoreCase: true,
                },
            }
        );
    });
    </script>

{% endhighlight %}

### selectionType `enum`
{:#members:selectiontype}

<ts name="ej.Kanban.SelectionType"/>

To allow customize selection type. Accepting types are "single" and "multiple".

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">Single</td>
<td class="description">Support for Single selection in Kanban</td>
</tr>
<tr>
<td class="name">Multiple</td>
<td class="description">Support for multiple selections in Kanban</td>
</tr>
</tbody>
</table>

#### Default Value:

* ej.Kanban.SelectionType.Single

#### Example

{% highlight html %} 

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
            {

                dataSource: data,
                selectionType: "multiple",
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
            });
    });
    </script>

{% endhighlight %}

### stackedHeaderRows `array`
{:#members:stackedheaderrows}

Gets or sets an object that indicates to managing the collection of stacked header rows for the Kanban.

#### Default Value:

* Array

#### Example

{% highlight html %}
 
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
            { Id: 5, Status: "Validate", Summary: "Task 5", Assignee: "Andrew" },
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
             {
                 dataSource: data,
                 columns: [
                     { headerText: "Backlog", key: "Open", width: 80 },
                     { headerText: "Validated", key: "Validate", width: 80 },
                     { headerText: "In Progress", key: "InProgress", width: 80 },
                     { headerText: "Testing", key: "Testing", width: 80 },
                     { headerText: "Done", key: "Close", width: 70 }
                 ],
                 keyField: "Status",
                 stackedHeaderRows: [{
                     stackedHeaderColumns: [{ headerText: "Unresolved", column: "Backlog,Validated,In Progress" },
                         { headerText: "Resolved", column: "Testing,Done" }
                     ]
                 }
                 ],
                 fields: {
                     primaryKey: "Id",
                     content: "Summary",
                 },
             });
    });
    </script>

{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns `array`
{:#members:stackedheaderrows-stackedheadercolumns}

Gets or sets a value that indicates whether to add stacked header columns into the stacked header rows.

#### Default Value:

* Array

#### Example

{% highlight html %}
  
    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
            { Id: 5, Status: "Validate", Summary: "Task 5", Assignee: "Andrew" },
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
             {
                 dataSource: data,
                 columns: [
                     { headerText: "Backlog", key: "Open", width: 80 },
                     { headerText: "Validated", key: "Validate", width: 80 },
                     { headerText: "In Progress", key: "InProgress", width: 80 },
                     { headerText: "Testing", key: "Testing", width: 80 },
                     { headerText: "Done", key: "Close", width: 70 }
                 ],
                 keyField: "Status",
                 stackedHeaderRows: [{
                     stackedHeaderColumns: [{ headerText: "Unresolved", column: "Backlog,Validated,In Progress" },
                         { headerText: "Resolved", column: "Testing,Done" }
                     ]
                 }
                 ],
                 fields: {
                     primaryKey: "Id",
                     content: "Summary",
                 },
             });
    });
    </script>
 
{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.headerText `string`
{:#members:stackedheaderrows-stackedheadercolumns-headertext}

Gets or sets a value that indicates the headerText for the particular stacked header column.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
            { Id: 5, Status: "Validate", Summary: "Task 5", Assignee: "Andrew" },
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
             {
                 dataSource: data,
                 columns: [
                     { headerText: "Backlog", key: "Open", width: 80 },
                     { headerText: "Validated", key: "Validate", width: 80 },
                     { headerText: "In Progress", key: "InProgress", width: 80 },
                     { headerText: "Testing", key: "Testing", width: 80 },
                     { headerText: "Done", key: "Close", width: 70 }
                 ],
                 keyField: "Status",
                 stackedHeaderRows: [{
                     stackedHeaderColumns: [{ headerText: "Unresolved", column: "Backlog,Validated,In Progress" },
                         { headerText: "Resolved", column: "Testing,Done" }
                     ]
                 }
                 ],
                 fields: {
                     primaryKey: "Id",
                     content: "Summary",
                 },
             });
    });
    </script>

{% endhighlight %}

### stackedHeaderRows.stackedHeaderColumns.column `string`
{:#members:stackedheaderrows-stackedheadercolumns-column}

Gets or sets a value that indicates the column for the particular stacked header column.

#### Default Value

* null

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
            { Id: 5, Status: "Validate", Summary: "Task 5", Assignee: "Andrew" },
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
             {
                 dataSource: data,
                 columns: [
                     { headerText: "Backlog", key: "Open", width: 80 },
                     { headerText: "Validated", key: "Validate", width: 80 },
                     { headerText: "In Progress", key: "InProgress", width: 80 },
                     { headerText: "Testing", key: "Testing", width: 80 },
                     { headerText: "Done", key: "Close", width: 70 }
                 ],
                 keyField: "Status",
                 stackedHeaderRows: [{
                     stackedHeaderColumns: [{ headerText: "Unresolved", column: "Backlog,Validated,In Progress" },
                         { headerText: "Resolved", column: "Testing,Done" }
                     ]
                 }
                 ],
                 fields: {
                     primaryKey: "Id",
                     content: "Summary",
                 },
             });
    });
    </script>

{% endhighlight %}

### tooltipSettings `object`
{:#members:tooltipsettings}

The tooltip allows to display card details in a tooltip while hovering on it.

### tooltipSettings.enable `boolean`
{:#members:tooltipsettings-enable}

To enable or disable the tooltip display.


#### Default Value:

* false

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                tooltipSettings: {
                    enable: true,
                },
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                },
                fields: {
                    primaryKey: "Id",
                    content: "Text",
                    title: "Id",
                    tag: "Tags",
                    color: "Type",
                    imageUrl: "ImgUrl",
                },
                cardSettings: {
                    colorMapping: {
                        "#cb2027": "Issue,Story",
                        "#67ab47": "Improvement",
                        "#fbae19": "Epic",
                        "#6a5da8": "UG",
                    },
                },
            });
    });
    </script>
   
{% endhighlight %}
  
### tooltipSettings.template `string`
{:#members:tooltipsettings-template}

To customize the tooltip display based on your requirements.

#### Default Value:

* null

#### Example

{% highlight html %}

    <div id="kanban"></div>
    <script id="tooltipTemp" type="text/x-jsrender">
    <div class='e-kanbantooltiptemp ' style="display: none">
        <table>
            <tr>
                <td class="photo">
                    <img src="{{:ImgUrl}}">
                </td>

                <td class="details">
                    <table>
                        <colgroup>
                            <col width="30%">
                            <col width="70%">
                        </colgroup>
                        <tbody>
                            <tr>
                                <td class="CardHeader">Name: </td>
                                <td>{{:Assignee}}</td>
                            </tr>
                            <tr>
                                <td class="CardHeader">Task: </td>
                                <td>{{:Type}}</td>
                            </tr>
                        </tbody>
                    </table>
                </td>
            </tr>
        </table>
    </div>
    </script>
    <script type="text/javascript">
    window.kanbandata = [
       { Id: 1, Status: "Open", Summary: "Task 1", Type: "Epic", Assignee: "Nancy" },
       { Id: 2, Status: "Open", Summary: "Task 2", Type: "Story", Assignee: "Andrew" },
       { Id: 3, Status: "InProgress", Summary: "Task 3", Type: "Improvment", Assignee: "Andrew" },
       { Id: 4, Status: "Testing", Summary: "Task 4", Type: "Issue", Assignee: "Nancy" }
    ];
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#kanban").ejKanban(
            {
                dataSource: data,
                tooltipSettings: {
                    enable: true,
                    template: "#tooltipTemp",
                },
                columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress" },
                    { headerText: "Testing", key: "Testing" },
                    { headerText: "Done", key: "Close" }
                ],
                keyField: "Status",
                fields: {
                    primaryKey: "Id",
                    content: "Summary",
                    title: "Id",
                    tag: "Tags",
                    color: "Type",
                    imageUrl: "ImgUrl",
                },
                cardSettings: {
                    colorMapping: {
                        "#cb2027": "Issue,Story",
                        "#67ab47": "Improvement",
                        "#fbae19": "Epic",
                        "#6a5da8": "UG",
                    },
                },
            });
    });
    </script>
    
{% endhighlight %}
  
### locale `String`
{:#members:locale}

Gets or sets a value that indicates whether to customizing the user interface (UI) as locale-specific in order to display regional data i.e. in a language and culture specific to a particular country or region.

#### Default Value:

* "en-US"

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script>
    window.kanbandata = [
            { Id: 1, Status: "Open", Summary: "Task 1", Assignee: "Nancy" },
            { Id: 2, Status: "Open", Summary: "Task 2", Assignee: "Andrew" },
            { Id: 3, Status: "InProgress", Summary: "Task 3", Assignee: "Andrew" },
            { Id: 4, Status: "Testing", Summary: "Task 4", Assignee: "Nancy" },
            { Id: 5, Status: "Validate", Summary: "Task 5", Assignee: "Andrew" }
    ];
    ej.Kanban.Locale["de-DE"] = {
        EmptyCard: "Keine Karten angezeigt werden",
        SaveButton: "Speichern",
        CancelButton: "stornieren",
        EditFormTitle: "Details von ",
        AddFormTitle: "Neue Karte hinzufügen",
        SwimlaneCaptionFormat: "- {{:count}}{{if count == 1 }} Artikel {{else}} Artikel {{/if}}",
        FilterSettings: "Filter:",
        FilterOfText: "Von",
        Cards: "kaarten"
        Max: "Max.",
        Min: "Min."
    };
    $(function () {
        var data = ej.DataManager(window.kanbandata);
        $("#Kanban").ejKanban(
        {
            dataSource: data,
            locale: "de-DE",
            columns: [
                    { headerText: "Backlog", key: "Open" },
                    { headerText: "In Progress", key: "InProgress", constraints: { max: 2 } },
                    { headerText: "Done", key: "Close" }
            ],
            keyField: "Status",
            allowTitle: true,
            fields: {
                primaryKey: "Id",
                swimlaneKey: "Assignee",
                content: "Summary",
            },
        });
    });
    </script>
  
{% endhighlight %}

## Methods

### clearSearch()
{:#methods:clearsearch}

Method used for send a clear search request to Kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends a clearSearch request to the Kanban
    kanbanObj.clearSearch(); 
    </script>

{% endhighlight %}

### clearSelection()
{:#methods:clearselection}

It is used to clear all the card selection.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#kanban").data("ejKanban");
    kanbanObj.clearSelection();  // clears all of the card selection
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>         
    // clears all of the card selection
    $("#Kanban").ejKanban("clearSelection");        
    </script>
    
{% endhighlight %}


### collapseAll()
{:#methods:collapseall}

Collapse all the swimlane rows in Kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Collapse all the  rows
    kanbanObj.collapseAll(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Collapse all the group caption rows
    $("#Kanban").ejKanban("collapseAll");        
    </script>
    
{% endhighlight %}


### columns(column,key,\[action\])
{:#methods:columns}

Add or remove columns in Kanban columns collections

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">column details</td>
    <td class="type"><span class="param-type">array/string</span></td>
    <td class="description last">Pass array of columns or string of headerText to add/remove the column in Kanban</td>
    </tr>
    <tr>
    <td class="name">key value</td>
    <td class="type"><span class="param-type">array/string</span></td>
    <td class="description last">Pass array of columns or string of key value to add/remove the column in Kanban</td>
    </tr>
    <tr>
    <td class="name">action</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last"><span class="optional">optional</span> Pass add/remove action to be performed. By default "add" action will perform</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#kanban").data("ejKanban");
    // remove Kanban column
    kanbanObj.columns("Testing","Testing", "remove");
    // Add new column into Kanban or modified already existing column in the Kanban.
    kanbanObj.columns("Codereview","codereview","add"); 
    </script>
    
{% endhighlight %}

### clearFilter()
{:#methods:clearfilter}

Send a clear request to filter cards in the kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends clear request to filter the cards
    kanbanObj.clearFilter();
    </script>
    
{% endhighlight %}

### destroy()
{:#methods:destroy}

Destroy the Kanban widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.

#### Example

{% highlight html %}
 
    <script>
    var kanbanObj = $("#Kanban").data("ejKanban");
    kanbanObj.destroy(); // destroy the Kanban
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <script>
    // destroy the Kanban
    $("#Kanban").ejKanban("destroy");        
    </script>
    
{% endhighlight %}

### dataSource(datasource)
{:#methods:datasource}

Refresh the Kanban with new data source.

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">datasource</td><td class="type"><span class="param-type">array</span></td>
    <td class="description last">Pass new data source to the Kanban</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Refreshes the Kanban data source
    kanbanObj.dataSource(data); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Refreshes the Kanban data source
    $("#Kanban").ejKanban("dataSource", data);        
    </script>

{% endhighlight %}

### filterCards()
{:#methods:filtercards}

Send a filtering request to cards in the kanban.

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">query</td><td class="type"><span class="param-type">object</span></td>
    <td class="description last">Pass the query to the cards</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends filtering request to the cards
    kanbanObj.filterCards(new ej.Query().where("Assignee", "equal", "Janet Leverling"));
    </script>
    
{% endhighlight %}

### toggleColumn(headerText or $div)
{:#methods:togglecolumn}

toggleColumn based on the headerText in Kanban.

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    headerText
    </td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Pass the header text of the column to get the corresponding column object</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
      <script>
      // Create Kanban object.
      var kanbanObj = $("#Kanban").data("ejKanban");
      // toggleColumn the row based on the row state
      kanbanObj.toggleColumn("Backlog");  
      </script>
      
{% endhighlight %}

{% highlight html %}
 
      <script>
      // toggleColumn the row based on the row state
      $("#Kanban").ejKanban("toggleColumn",("Backlog"));        
      </script>
      
{% endhighlight %}

### toggleCard($div or id)
{:#methods:togglecard}

Expand or collapse the card based on the state of target "div"

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    key
    </td>
    <td class="type"><span class="param-type">string/number</span></td>
    <td class="description last">Pass the id of card to be toggle </td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
      <script>
      // Create Kanban object.
      var kanbanObj = $("#Kanban").data("ejKanban");
      // toggleCard the row based on the row state
      kanbanObj.toggleCard("2");  
      </script>
      
{% endhighlight %}


{% highlight html %}
 
      <script>
      // toggleCard the row based on the row state
      $("#Kanban").ejKanban("toggleCard",("2"));        
      </script>
      
{% endhighlight %}

### toggleSwimlane($div or key)
{:#methods:toggleswimlane}

Expand or collapse the swimlane row based on the state of target "div"

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    $div 
    </td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Pass the div object to toggleSwimlane row based on its row state</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
      <script>
      // Create Kanban object.
      var kanbanObj = $("#Kanban").data("ejKanban");
      // toggleSwimlane the row based on the row state
      kanbanObj.toggleSwimlane($(".e-slexpandcollapse").eq(1)); 
      </script>
      
{% endhighlight %}


{% highlight html %}
 
      <script>
      // toggleSwimlane the row based on the row state
      $("#Kanban").ejKanban("toggleSwimlane", $(".e-slexpandcollapse").eq(1)); 
      </script>     
      </script>
      
{% endhighlight %}

### expandAll()
{:#methods:expandall}

Expand all the swimlane rows in Kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // expand all the  rows
    kanbanObj.expandAll(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // expand all the group caption rows
    $("#Kanban").ejKanban("expandAll");        
    </script>
    
{% endhighlight %}

### getVisibleColumnNames()
{:#methods:getvisiblecolumnnames}

Used for get the names of all the visible column name collections in Kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Gets the names of all the visible column collections
    kanbanObj.getVisibleColumnNames(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Gets the names of all the visible column collections
    $("#Kanban").ejKanban("getVisibleColumnNames");        
    </script>
    
{% endhighlight %}

### getScrollObject()
{:#methods:getscrollobject}

Get the scroller object of Kanban.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Gets scroll object of Kanban control
    kanbanObj.getScrollObject(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Gets scroll object of Kanban control
    $("#Kanban").ejKanban("getScrollObject");        
    </script>
    
{% endhighlight %}


### getColumnByHeaderText(headerText)
{:#methods:getcolumnbyheadertext}

Get the column details based on the given header text in Kanban.

  <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    headerText
    </td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Pass the header text of the column to get the corresponding column object</td>
    </tr>
    </tbody>
    </table>

#### Returns:

{:#methods:returns:}

String

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Gets the column details based on the given headerText
    kanbanObj.getColumnByHeaderText("Testing"); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Gets the column details based on the given headerText
    $("#Kanban").ejKanban("getColumnByHeaderText", "Testing");        
    </script>
    
{% endhighlight %}

### getHeaderTable()
{:#methods:getheadertable}

Get the table details based on the given header table in Kanban.

#### Returns:

{:#methods:returns:}

String

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Gets the table details based on the given headerTable
    kanbanObj.getHeaderTable(); 
    </script>
    
{% endhighlight %}

### hideColumns(headerText)
{:#methods:hidecolumns}

Hide columns from the Kanban based on the header text

  <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    headerText
    </td>
    <td class="type"><span class="param-type">array/string</span></td>
    <td class="description last">you can pass either array of header text of various columns or a header text of a column to hide</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    kanbanObj.hideColumns("Testing"); // Hides column based on the given header text of the column
    kanbanObj.hideColumns(["Testing", "Done"]); // Hide columns based on the array of header text of the columns given
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <script>
    // Hide column based on the given header text of the column
    $("#Kanban").ejKanban("hideColumns", "Testing"); 
    // Hide columns based on the array of header text of the columns given
    $("#Kanban").ejKanban("hideColumns", ["Testing", "Done"]);                  
    </script>
    
{% endhighlight %}


### print()
{:#methods:print}

Print the Kanban Board

#### Returns:
{:#methods:returns:}

Void

####Example
{:.example}


{% highlight html %}
 
    <div id="Kanban"></div> 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // It prints the kanban board.
    kanbanObj.print(); 
    </script>
{% endhighlight %}


{% highlight html %}
 
    <div id="Kanban"></div>; 
    <script>
    // It prints the kanban board.
    $("#Kanban").ejKanban("print");        
    </script>
{% endhighlight %}


### refreshTemplate()
{:#methods:refreshtemplate}

Refresh the template of the Kanban

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Refreshes the template of the Kanban control
    kanbanObj.refreshTemplate(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Refreshes the template of the Kanban control.
    $("#Kanban").ejKanban("refreshTemplate");        
    </script>
    
{% endhighlight %}

### refresh(\[templateRefresh\])
{:#methods:refresh}

Refresh the Kanban contents.The template refreshment is based on the argument passed along with this method

<table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    templateRefresh
    </td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last"><span class="optional">optional</span> When templateRefresh is set true, template and Kanban contents both are refreshed in Kanban else only Kanban content is refreshed</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <div id="Kanban"></div> 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    kanbanObj.refresh(); // Refresh the Kanban contents only
    kanbanObj.refresh(true); // Refresh the template of the Kanban control.
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <div id="Kanban"></div> 
    <script>
    // Refresh the Kanban.
    $("#Kanban").ejKanban("refresh");        
    // Refresh the template of the Kanban control.
    $("#Kanban").ejKanban("refresh", true);        
    </script>
    
{% endhighlight %}

### searchCards(searchString)
{:#methods:searchcards}

Send a search request to Kanban with specified string passed in it.

  <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">{% highlight html %}
    searchString{% endhighlight %}</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Pass the string to search in Kanban card</td>
    </tr>
    </tbody>
    </table>

#### Example
{:.example}


{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends a search request to the Kanban
    kanbanObj.searchCards("Analyse"); 
    </script>

{% endhighlight %}


{% highlight html %}

    <script>
    // Sends a search request to the Kanban
    $("#Kanban").ejKanban("searchCards", "Analyse");        
    </script>
    
{% endhighlight %}

### showColumns(headerText)
{:#methods:showcolumns}

Show columns in the Kanban based on the header text.

<table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    headerText
    </td>
    <td class="type"><span class="param-type">array/string</span></td>
    <td class="description last">You can pass either array of header text of various columns or a header text of a column to show</td>
    </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#kanban").data("ejKanban");
    kanbanObj.showColumns("Testing"); // Shows column based on the given header text of the column
    kanbanObj.showColumns(["Testing", "Done"]); // Shows columns based on the array of header text of the columns given
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <script>
    // Shows column based on the given header text of the column
    $("#kanban").ejKanban("showColumns", "Testing"); 
    // Shows columns based on the array of header text of the columns given
    $("#Kanban").ejKanban("showColumns", ["Testing", "Done"]);                  
    </script>
    
{% endhighlight %}

### updateCard(key,data)
{:#methods:updatecard}

Update a card in Kanban control based on key and JSON data given.

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    key
    </td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Pass the key field Name of the column</td>
    </tr>
    <tr>
    <td class="name">
    data
    </td>
    <td class="type"><span class="param-type">array</span></td>
    <td class="description last">Pass the edited JSON data of card need to be update.</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends a update card request to the Kanban
    kanbanObj.updateCard(2,{ Id: 2, Status: "Open", Text: "Task 1", Assignee: "Andrew Piller");
    </script>
    
{% endhighlight %}

### KanbanEdit
{:#methods:kanbanedit}

### KanbanEdit.addCard(\[primaryKey\],\[card\])
{:#methods:kanbanedit-addcard}

Add a new card in Kanban control.If parameters are not given default dialog will be open

 <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">primaryKey</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Pass the primary key field Name of the column</td>
    </tr>
    <tr>
    <td class="name">card</td>
    <td class="type"><span class="param-type">array</span></td>
    <td class="description last">Pass the edited JSON data of card need to be add.</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends an add new card request to the Kanban
    kanbanObj.KanbanEdit.addCard(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // add new card to the Kanban
     kanbanObj.KanbanEdit.addCard("2",{Id:2, Status: "Open", Text: "Task 1", Assignee: "Nancy" })     
    </script>
    
{% endhighlight %}

### KanbanEdit.cancelEdit()
{:#methods:kanbanedit-canceledit}

Send a cancel request of add/edit card in Kanban

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends a cancel request to the Kanban
    kanbanObj.KanbanEdit.cancelEdit(); 
    </script>
    
{% endhighlight %}


{% highlight html %}
 
    <script>
    // Sends a cancel request to the Kanban
    $("#Kanban").ejKanban("cancelEdit");        
    </script>
    
{% endhighlight %}

### KanbanEdit.deleteCard(Key)
{:#methods:kanbanedit-deletecard}

Delete a card in Kanban control.

<table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">Key</td>
    <td class="type"><span class="param-type">string/number</span></td>
    <td class="description last">Pass the key of card to be delete</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#kanban").data("ejKanban");
    // Sends a delete card request to the Kanban
    kanbanObj.KanbanEdit.deleteCard(2); 
    </script>
    
{% endhighlight %}

### KanbanEdit.endEdit()
{:#methods:kanbanedit-endedit}

Send a save request in Kanban when any card is in edit/new add card state.

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends a save request to the Kanban
    kanbanObj.KanbanEdit.endEdit(); 
    </script>
    
{% endhighlight %}

{% highlight html %}
 
    <script>
    // Sends a save request to the Kanban
    $("#Kanban").ejKanban("endEdit");        
    </script>
    
{% endhighlight %}

### KanbanEdit.startEdit($div or key)
{:#methods:kanbanedit-startedit}

Send an edit card request in Kanban.Parameter will be HTML element or primary key

  <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">
    $div
    </td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Pass the div selected row element to be edited in Kanban</td>
    </tr>
    <td class="name">
    key
    </td>
    <td class="type"><span class="param-type">string/number</span></td>
    <td class="description last">Pass the key element to be edited in Kanban</td>
    </tr>
    </tbody>
    </table>

#### Example

{% highlight html %}
 
    <script>
    // Create Kanban object.
    var kanbanObj = $("#Kanban").data("ejKanban");
    // Sends an edit card request to the Kanban
    kanbanObj.KanbanEdit.startEdit($(".e-kanbancontent .e-kanbancard").first()); 
    kanbanObj.KanbanEdit.startEdit(2); 
    </script>

{% endhighlight %}

{% highlight html %}
 
    <script>
    // Sends an edit card request to the Kanban
    $("#Kanban").ejKanban("startEdit", ($(".e-kanbancontent .e-kanbancard").first());        
    $("#Kanban").ejKanban("startEdit", 2);        
    </script>
    
{% endhighlight %}

### KanbanEdit.setValidationToField(name, rules)
{:#methods:kanbanedit-setvalidationtofield}

Method used for set validation to a field during editing.

  <table class="params">
     <thead>
     <tr>
     <th>Name</th>
     <th>Type</th>
     <th class="last">Description</th>
     </tr>
     </thead>
     <tbody>
     <tr>
     <td class="name">name</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Specify the name of the column to set validation rules</td>
    </tr>
    <tr>
    <td class="name">rules</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Specify the validation rules for the field</td>
    </tr>
    </tbody>
    </table>

#### Example
{:.example}

{% highlight html %}
 
     <script>
     // Create Kanban object.
     var kanbanObj = $("#Kanban").data("ejKanban");
     // It is used to set validation to a field during editing
     kanbanObj.KanbanEdit.setValidationToField("Id", { required: true }); 
     </script>
     
{% endhighlight %}

{% highlight html %}
 
    <script>
    // It is used to set validation to a field during editing
    $("#Kanban").ejKanban("setValidationToField", "Id", { required: true });
    </script>
    
{% endhighlight %} 

## Events

### actionBegin
{:#events:actionbegin}

Triggered for every Kanban action before its starts.
    
 <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban is initialized:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban card editing action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">originalEventType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the current action event type.</td>
        </tr>
        <tr>
        <td class="name">primaryKeyValue</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns primary key value.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type.</td>
        </tr>
        <tr>
        <td class="name">rowIndex</td>
        <td class="type"><span class="param-type">number</span></td>
        <td class="description last">Returns the edited row index.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban card save action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">data</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the card object (JSON).</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">primaryKeyValue</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns primary key value.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban card cancel action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban card delete action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">data</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the card object (JSON).</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when add new card action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">data</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the card object (JSON).</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type as `beginadd`.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        <tr>
        <td class="name">argument</td>
        <td class="type"><span class="param-type">Object</span></td>
        <td class="description last">Event parameters when Kanban filtering action starts:
        <table class="params">
        <thead>
        <tr>
        <th>Name</th>
        <th>Type</th>
        <th class="last">Description</th>
        </tr>
        </thead>
        <tbody>
        <tr>
        <td class="name">cancel</td>
        <td class="type"><span class="param-type">boolean</span></td>
        <td class="description last">Returns the cancel option value.</td>
        </tr>
        <tr>
        <td class="name">currentFiltering object</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns current filtering object field name.</td>
        </tr>
        <tr>
        <td class="name">filterCollection</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns filter details.</td>
        </tr>
        <tr>
        <td class="name">model</td>
        <td class="type"><span class="param-type">object</span></td>
        <td class="description last">Returns the Kanban model.</td>
        </tr>
        <tr>
        <td class="name">requestType</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns request type.</td>
        </tr>
        <tr>
        <td class="name">type</td>
        <td class="type"><span class="param-type">string</span></td>
        <td class="description last">Returns the name of the event.</td>
        </tr>
        </tbody>
        </table>
        </td>
        </tr>
        </tbody>
        </table>

#### Example

{% highlight html %}
 
      <div id="Kanban"></div> 
      <script>
      $("#Kanban").ejKanban({
      actionBegin: function (args){}
      });
      </script>
    
{% endhighlight %}


### actionComplete
{:#events:actioncomplete}

Triggered for every Kanban action success event.

<table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">Object</span></td>
    <td class="description last">Arguments in actionComplete when Kanban is initialized.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after Kanban card editing action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">primaryKey</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns primary key.</td>
    </tr>
    <tr>
    <td class="name">primaryKeyValue</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns primary key value.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after Kanban card save action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">data</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the card object (JSON).</td>
    </tr>
    <tr>
    <td class="name">selectedRow</td>
    <td class="type"><span class="param-type">number</span></td>
    <td class="description last">Returns the selectedRow index.</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after Kanban card cancel action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after Kanban card delete action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">data</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the card object (JSON).</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after add new card action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">data</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns empty card object (JSON).</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    <tr>
    <td class="name">argument</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Arguments in actionComplete after Kanban filtering action is completed.
    <table class="params">
    <thead>
    <tr>
    <th>Name</th>
    <th>Type</th>
    <th class="last">Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td class="name">cancel</td>
    <td class="type"><span class="param-type">boolean</span></td>
    <td class="description last">Returns the cancel option value.</td>
    </tr>
    <tr>
    <td class="name">currentFilteringColumn</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current filtering column field name.</td>
    </tr>
    <tr>
    <td class="name">filterCollection</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns filter details.</td>
    </tr>
    <tr>
    <td class="name">model</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns the Kanban model.</td>
    </tr>
    <tr>
    <td class="name">originalEventType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns current action event type.</td>
    </tr>
    <tr>
    <td class="name">requestType</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns request type.</td>
    </tr>
    <tr>
    <td class="name">target</td>
    <td class="type"><span class="param-type">object</span></td>
    <td class="description last">Returns Kanban element.</td>
    </tr>
    <tr>
    <td class="name">type</td>
    <td class="type"><span class="param-type">string</span></td>
    <td class="description last">Returns the name of the event.</td>
    </tr>
    </tbody>
    </table>
    </td>
    </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    actionComplete: function (args) {}
    }); 
    </script>

{% endhighlight %}


### actionFailure
{:#events:actionfailure}

Triggered for every Kanban action server failure event.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments in actionFailure when Kanban is initialized.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after Kanban card editing action is completed.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after Kanban card save action is completed.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the card object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after Kanban card delete action is completed.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the card object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after add new card action is completed.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns empty card object (JSON).</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Arguments in actionFailure after Kanban filtering action is completed.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentFilteringColumn</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current filtering column field name.</td>
</tr>
<tr>
<td class="name">filterCollection</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns filter details.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">originalEventType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns current action event type.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">error</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the error return by server.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

     <div id="Kanban"></div> 
     <script>
     $("#Kanban").ejKanban({
     actionFailure: function (args) {}
     }); 
     </script>

{% endhighlight %}


### beginEdit
{:#events:beginedit}

Triggered before the task is going to be edited.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when begin edit event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns begin edit data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    beginEdit: function (args) {}
    });
    </script>
    
{% endhighlight %}


### beginAdd
{:#events:beginadd}

Triggered before the task is going to be added

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when beginAdd event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">primaryKeyValue</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns primary key value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns beginAdd data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    beginAdd: function (args) {}
    });
    </script>
    
{% endhighlight %}

### beforeCardSelect
{:#events:beforecardselect}

Triggered before the card is going to be selecting.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when beforeCardSelect event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select cell index value.</td>
</tr>
<tr>
<td class="name">cardIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select card index value.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the select cell element</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">previousCard</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previously select the card element</td>
</tr>
<tr>
<td class="name">previous Row cell index</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously select card indexes</td>
</tr>
<tr>
<td class="name">Target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Target item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns select card data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    beforeCardSelect: function (args) {}
    });
    </script>
    
{% endhighlight %}

### cardClick
{:#events:cardclick}

Trigger after the card is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardClick event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current record object (JSON).</td>
</tr>
<tr>
<td class="name">currentCard</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the current card to the Kanban.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">columnName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the Header text of the column corresponding to the selected card.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example


{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").Kanban({
    cardClick: function (args) {}
    });
    </script>
    
{% endhighlight %}

### cardDrag
{:#events:carddrag}

Triggered when the card is being dragged.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when columnDrag event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag data.</td>
</tr>
<tr>
<td class="name">drag target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag start element.</td>
</tr>
<tr>
<td class="name">draggedElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dragged element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardDrag: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardDragStart
{:#events:carddragstart}

Triggered when card dragging start.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardDragStart event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns card drag start data.</td>
</tr>
<tr>
<td class="name">draggedElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dragged element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">drag target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag start element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardDragStart: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardDragStop
{:#events:carddragstop}

Triggered when card dragging stops.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardDragStart event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggedElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dragged element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">drop target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag stop element.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drag stop data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardDragStop: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardDrop
{:#events:carddrop}

Triggered when the card is Drop.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardDrop event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">draggedElement</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dragged element.</td>
</tr>
<tr>
<td class="name">draggedParent</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns previous parent of dragged element</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns dragged data.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns drop element.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script>
    $("#Kanban").ejKanban({
    cardDrop: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardSelect
{:#events:cardselect}

Triggered after the card is select.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardSelect event is triggered.
<table class="params">
<thead
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select cell index value.</td>
</tr>
<tr>
<td class="name">cardIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select card index value.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the select cell element</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">previousCard</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previously select the card element</td>
</tr>
<tr>
<td class="name">previous Row cell index</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously select card indexes</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns select card data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardSelect: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardDoubleClick
{:#events:carddoubleclick}

Triggered when card is double clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardDoubleClick event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current card object (JSON).</td>
</tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardDoubleClick: function (args) {}
    });
    </script>
    
{% endhighlight %}


### cardSelecting
{:#events:cardselecting}

Triggered before the card is going to be selecting

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when cardSelecting event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selecting cell index value.</td>
</tr>
<tr>
<td class="name">cardIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the selecting card index value.</td>
</tr>
<tr>
<td class="name">currentCell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the selecting cell element</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">previousCard</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the previously selecting the card element</td>
</tr>
<tr>
<td class="name">previous Row cell index</td>
<td class="type"><span class="param-type">array</span></td>
<td class="description last">Returns the previously rowcell is selecting card indexes</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns added data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cardSelecting: function (args) {}
    });
    </script>
    
{% endhighlight %}

### create
{:#events:create}

TTriggered for every Kanban Create.  

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Kanban.Model"/><span class="param-type">Object</span></td>
<td class="description last">Event parameters from kanban
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}

    <div id="Kanban"></div>
    <script>
    $("#Kanban").ejKanban({
    create: function (args){}
    });
    </script>
    
{% endhighlight %}

### cellClick
{:#events:cellclick}

Triggers after the cell is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select cell index value.</td>
</tr>
<tr>
<td class="name">rowIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the edited row index.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    cellClick: function (args) {}
    });
    </script>

{% endhighlight %}

### dataBound
{:#events:databound}

Triggered the Kanban is bound with data during initial rendering.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when dataBound event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div>
    <script>
    $("#Kanban").ejKanban({
    dataBound: function (args) {}
    });
    </script>
    
{% endhighlight %}

### destroy
{:#events:destroy}

Triggered when Kanban going to destroy.  

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Kanban.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments when destroy event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the kanban model.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    destroy: function (args) {}
    });
    </script>
    
{% endhighlight %}

### endDelete
{:#events:enddelete}

Triggered after the task is deleted.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when endDelete event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns deleted  data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Current action name</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    endDelete: function (args) {}
    });
    </script>
    
{% endhighlight %}


### endEdit
{:#events:endddit}

Triggered after the task is edited.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when endEdit event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">requestType</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns request type.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns modified data.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">action</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Current Action name</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}
 
    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    endEdit: function (args) {}
    });
    </script>
    
{% endhighlight %}

### headerClick
{:#events:headerclick}

Triggers after the header is clicked.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type">boolean</td>
<td class="description">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type">object</td>
<td class="description">Returns the kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type">string</td>
<td class="description">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">cellIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the select cell index value.</td>
</tr>
<tr>
<td class="name">columnData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    headerClick: function (args) {}
    });
    </script>

{% endhighlight %}

### load
{:#events:load}

Triggered initial load.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><ts name="ej.Kanban.Model"/><span class="param-type">Object</span></td>
<td class="description last">Arguments when load event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the kanban model.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

####Example
{:.example}

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    load: function (args) {}
    });
    </script>
    
{% endhighlight %}

### toolbarClick
{:#events:toolbarclick}

Triggered when toolbar item is clicked in Kanban.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when toolBarClick event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">itemId</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the item id of that current element.</td>
</tr>
<tr>
<td class="name">itemIndex</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Returns the item index of that current element.</td>
</tr>
<tr>
<td class="name">itemName</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the item name of that current element.</td>
</tr>
<td class="name">itemText</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the item text of that current element.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">toolbarData</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the toolbar object of the Kanban.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

    <div id="Kanban"></div> 
    <script>
    $("#Kanban").ejKanban({
    toolbarClick: function (args) {
    }
    });
    </script>
    
{% endhighlight %}

### queryCellInfo
{:#events:querycellinfo}

Triggered every time a single card rendered request is made to access particular card information.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Kanban
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">card</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban card.</td>
</tr>
<tr>
<td class="name">cell</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns Kanban card.</td>
</tr>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<tr>
<td class="name">data</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns current row record object (JSON).</td>
</tr>
<tr>
<td class="name">column</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the column object.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

     <div id="Kanban"></div> 
     <script>
     $("#Kanban").ejKanban({
     queryCellInfo: function (args){}
     });
    </script>
    
{% endhighlight %}


### contextClick
{:#events:contextclick}

Triggered when context menu item is clicked in Kanban

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when contextClick event is triggered
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

     <div id="Kanban"></div> 
     <script>
     $("#Kanban").ejKanban({
     contextClick: function (args){}
     });
    </script>
    
{% endhighlight %}

### contextOpen
{:#events:contextopen}

Triggered before the context menu is opened.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Arguments when contextOpen event is triggered.
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the cancel option value.</td>
</tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the Kanban model.</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">Returns the name of the event.</td>
</tr>
<tr>
<td class="name">currentTarget</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the current item.</td>
</tr>
<tr>
<td class="name">status</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">Returns the status of contextmenu item which denotes its enabled state.</td>
</tr>
<tr>
<td class="name">target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns the target item.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>

#### Example

{% highlight html %}

     <div id="Kanban"></div> 
     <script>
     $("#Kanban").ejKanban({
     contextOpen: function (args){}
     });
    </script>
    
{% endhighlight %}