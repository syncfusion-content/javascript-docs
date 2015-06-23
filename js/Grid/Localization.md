---
layout: post
title: Localization
description: localization
platform: js
control: Grid
documentation: ug
---

# Localization

The **Localization** concept in **ejGrid** supports switching the control language with various cultures. The `Locale` property in **ejGrid** is a string type used to define the culture code that has been declared by **JQuery globalize script** file. The default value for **Locale** in **ejGrid** is **en-US**.

The following two script files are necessary to perform **Localization** in **ejGrid**.

1. jquery.globalize.min.js

2. globalize.culture.en-US.min.js (Changeable)

The **globalize.culture.en-US.min.js** scripts are changeable based on the culture name. Each culture has its own culture script file that differs by its culture code. For example **en-US** is the culture code for **English - United States**.

The following code example demonstrates how to switch the culture of **ejGrid** as **de-DE** (**German - Germany**).

{% highlight html %}

<script src="../scripts/jquery.globalize.min.js"></script>
<script src="../scripts/globalize.culture.de-DE.min.js"></script>
<div id="Grid"></div>
<script type="text/javascript">
  $(function () {
     $("#Grid").ejGrid({
       // the datasource "window.gridData" is referred from jsondata.min.js
       dataSource: window.gridData,
       allowPaging: true,
       pageSettings: { pageCount: 5 },
       allowGrouping: true,
       groupSettings:{enableDropAreaAnimation: false},
       locale: "de-DE",
       columns: [
                     { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 75 },
                     { field: "CustomerID", headerText: "Customer ID", width: 90 },
                     { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 80 },
                     { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                     { field: "ShipCity", headerText: "Ship City", width: 110 }
       ]
   });
  });
</script>


{% endhighlight %}



The **ejGrid** and **ejPager** has its own locale labels for applying the information about specific fields in its control. You can set them in the sample side for each culture based translation. The following code example is applied in the sample side for all the above platforms.

{% highlight js %}

  <script type="text/javascript">
        // Locale labels for ejGrid
        ej.Grid.locale["de-DE"] = {
            EmptyRecord: "Keine Aufzeichnungen angezeigt",
            GroupDropArea: "Ziehen Sie eine Spaltenüberschrift hier",
            DeleteOperationAlert: "Keine Einträge für Löschvorgang ausgewählt",
            EditOperationAlert: "Keine Einträge für Bearbeiten Betrieb ausgewählt",
            SaveButton: "Speichern",
            CancelButton: "stornieren",
            EditFormTitle: "Korrektur von",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}} Beiträge {{else}} Beiträges {{/if}}",
        };
        // Locale labels for ejGrid pager
        ej.Pager.locale["de-DE"] = {
            pagerInfo: "{0} von {1} Seiten ({2} Beiträge)",
            firstPageTooltip: "Zur ersten Seite",
            lastPageTooltip: "Zur letzten Seite",
            nextPageTooltip: "Zur nächsten Seite",
            previousPageTooltip: "Zurück zur letzten Seite",
            nextPagerTooltip: "Zum nächsten Pager",
            previousPagerTooltip: "Zum vorherigen Pager"
        };
    </script>



{% endhighlight %}



The output for the above code example is displayed as the following screenshot.

{% include image.html url="/js/Grid/Localization_images/Localization_img1.png"%}

The default values of locale labels in **ejGrid** and **ejPager** are listed out in the following code example. You can change the label values based on the cultures with its corresponding meaning of words.

{% highlight js %}
<script type="text/javascript">
        ej.Grid.locale["en-US"] = {
            EmptyRecord: "No records to display",
            //Editing option localization strings
            DeleteOperationAlert: "No records selected for delete operation",
            EditOperationAlert: "No records selected for edit operation",
            SaveButton: "Save",
            OkButton: "OK",
            CancelButton: "Cancel",
            EditFormTitle: "Details of ",
            AddFormTitle: "Add New Record",
            //Key Combination alert message
            Notactionkeyalert: "This Key-Combination is not avaiable",
            Keyconfigalerttext: "This Key-Combination has already been assigned to ",
            //Group drop area and caption format
            GroupDropArea: "Drag a column header here to group its column",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1 }} item {{else}} items {{/if}}",
            //Bulk Editing Alert Messages
            BatchSaveConifrm: "Are you sure you want to save changes?",
            BatchSaveLostChanges: "Unsaved changes will be lost. Are you sure you want to continue?",
            //Pager bar message string
            PagerInfo: "{0} of {1} pages ({2} items)",
            //Frozen Alert Messages
            FrozenColumnsViewAlert: "Frozen columns should be in grid view area",
            FrozenColumnsScrollAlert: "Enable allowScrolling while using frozen Columns",
            FrozenNotSupportedException: "Frozen Columns and Rows are not supported for Grouping, Row Template, Detail Template and Batch Editing",
            //Toolbar tooltip
            Add: "Add",
            Edit: "Edit",
            Delete: "Delete",
            Update: "Update",
            Cancel: "Cancel",
            //Filter menu strings
            StringMenuOptions: [{
                text: "StartsWith",
                value: "StartsWith"
            }, {
                text: "EndsWith",
                value: "EndsWith"
            }, {
                text: "Contains",
                value: "Contains"
            }, {
                text: "Equal",
                value: "Equal"
            }, {
                text: "NotEqual",
                value: "NotEqual"
            }],
            NumberMenuOptions: [{
                text: "LessThan",
                value: "LessThan"
            }, {
                text: "GreaterThan",
                value: "GreaterThan"
            }, {
                text: "LessThanOrEqual",
                value: "LessThanOrEqual"
            }, {
                text: "GreaterThanOrEqual",
                value: "GreaterThanOrEqual"
            }, {
                text: "Equal",
                value: "Equal"
            }, {
                text: "NotEqual",
                value: "NotEqual"
            }],
            PredicateAnd: "AND",
            PredicateOr: "OR",
            Filter: "Filter",
            MatchCase: "Match Case",
            Clear: "Clear",

            PrintGrid: "Print",
            ExcelExport: "Excel Export",
            WordExport: "Word Export",
            PdfExport: "PDF Export",

            ResponsiveFilter: "Filter",
            ResponsiveSorting: "Sort"
        };
        ej.Pager.locale["en-US"] = {

            pagerInfo: "{0} of {1} pages ({2} items)",

            firstPageTooltip: "Go to first page",

            lastPageTooltip: "Go to last page",

            nextPageTooltip: "Go to next page",

            previousPageTooltip: "Go to previous page",

            nextPagerTooltip: "Go to next Pager",

            previousPagerTooltip: "Go to previous Pager"
        };
   </script>
{% endhighlight %}



> _**Note**: You can get the various minified and unminified formatted culture script files from the local folder “C:\Program Files (x86)\Syncfusion\Essential Studio\xx.x.x.xx\JavaScript\assets\external\cultures”. xx.x.x.xx denotes the current version of Essential Studio, for example 12.4.0.34._



