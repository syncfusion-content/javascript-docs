---
layout: post
title: Globalizing and Localizing Syncfusion Essential JS Widgets
description: How to localize and globalize the syncfusion essential js widgets during application loading or dynamically.
platform: js
control: Introduction
documentation: ug
---

# Localization

All our Syncfusion Components has been provided with the built-in [Localization](https://msdn.microsoft.com/en-us/library/5839we2z%28v=vs.110%29.aspx) support, so that it will be able to adapt based on the culture-specific **locale** defined for it. The **en-US** locale is currently being used in all the Syncfusion components by default. 

To localize any of our Syncfusion components into a particular culture, it is necessary to refer the below specified scripts in your application,

* **ej.globalize.min.js** (Mandatory for processing specific source-side actions globally)
* Other culture-specific script files, to which specific culture you need to adapt any of our Syncfusion control.

I> **ej.globalize.min.js** library avails as built-in within ej.web.all.min.js file, therefore it is not necessary to externally refer it in your application (applicable for version 13.4.0.53 and higher). For version lower than 13.4.0.53, refer jQuery.globalize.min.js along with ej.web.all.min.js

N> Seven culture-specific script files are available in the below specified location. For all other culture files, please download from the [GitHub](https://github.com/syncfusion/ej-global/tree/master/i18n) location.

<table>
<tr>
<td>
<b>(installed location)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n
</td>
</tr>
<tr>
<td>
<b>For example,</b> If you have installed the Essential Studio package within <b>C:\Program Files (x86)</b>, then navigate to the below location,
<br/>
<b>C:\Program Files (x86)</b>\Syncfusion\Essential Studio\{{ site.releaseversion }}\JavaScript\assets\scripts\i18n
</td>
</tr>
</table>

N>   To translate our control content from default English to any of the culture, say For example - German language, then you need to refer the **ej.culture.de-DE.min.js** file in your application, after the reference of ej.web.all.min.js file. 


## Localizing the Syncfusion components 

Define the **locale** property which is applicable for all the Syncfusion components with the required culture codes declared by **EJ globalize script**. Usually, the culture codes are defined in short forms like **en-US** for English culture, **de-DE** for German culture, **fr-FR** for French culture and so on. The below sample code shows how to define the **locale** property for **DatePicker** control,

{% highlight javascript %}

$("#MyDatePicker").ejDatePicker({
     locale: "de-DE",
     watermarkText: "Datum auswählen",
     buttonText: "heute"
});   

{% endhighlight %}

The Syncfusion components can be localized on two basis,

* Built-in localized words
* Applying the user-defined localized words collection.

### Use of Built-in localized words in the DatePicker control

The date formats, day names and month names are automatically translated into the specific culture based on the culture-code assigned to the **locale** property, as these date related common conversions are processed as built-in within the source. Here, the above code will render the DatePicker control in **German** culture, as shown below,
![](/js/Localization_images/Localization_img1.png) 

#### Example 1: Defining locale property in the DatePicker control using built-in localized texts - Static

Refer the **JavaScript Control Initialization** document for creating a HTML page with Syncfusion components from the link [here](/js/control-initialization). The very first requirement to localize the DatePicker control into **de-DE** culture is to refer the **ej.culture.de-DE.min.js** file in your HTML application, which will be available in the location mentioned in the above note section.

Define the **locale** property for the DatePicker control with the appropriate **culture-code [de-DE]** as shown below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.de-DE.min.js"></script>
</head>
<body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker({
                locale: "de-DE",
                watermarkText: "Datum auswählen",
                buttonText: "heute"
            });
        });
    </script>
</body>
</html>    

{% endhighlight %}

N> jQuery.easing external dependency has been removed from version 14.3.0.49 onwards. Kindly include this jQuery.easing dependency for versions lesser than 14.3.0.49 in order to support animation effects.

Browse your HTML page in any of the web browser and now the screen will display the DatePicker widget with the localized texts as shown below,
![](/js/Localization_images/Localization_img2.png) 

#### To change the locale property dynamically in DatePicker control

Define a dropdownlist control additionally in your HTML page along with the DatePicker control, to hold the required culture codes. When the user selects a particular culture code option from the dropdownlist, the datepicker will get localized appropriately based on the dynamic selection made – which is depicted in the below code.

N>   In the below example, copy the culture files of **vi-VN** and **fr-FR** into the **Scripts** folder of your application and refer it in the head section along with the other CSS and script references, so that the **locale** of the datepicker switches between the selected culture appropriately.


{% highlight html %}

   <!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <!-- CSS and Script reference section -->
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.vi-VN.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.fr-FR.min.js"></script>
</head>
<body> 
    <!--Container for ejDatePicker widget-->
    <input id="startDate" type="text" /> 
    <!--Container for ejDropdown widget-->
    <select id="culture" class="e-ddl">
         <option>en-US</option>
         <option>vi-VN</option>
         <option>fr-FR</option>
     </select>
     <script type="text/javascript">
        $(function () {
            // declaration of ejDatePicker
            $("#startDate").ejDatePicker({
                locale: "fr-FR",
            });

            // declaration of ejDropDownList
            $("#culture").ejDropDownList({ 
                change: "onChange", // Event raised when the dropdown selection changes
                selectedItemIndex: 2 
            });
         });

        // event handler – when the dropdown selection option changes
        function onChange(args) {

            var datebject = $("#startDate").data("ejDatePicker");
            // localizable text
            if (args.value == "vi-VN") {
                datebject.option({ watermarkText: "Chọn ngày", buttonText: "Hôm nay" });
            }
            else if (args.value == "fr-FR") {
                datebject.option({ watermarkText: "Sélectionner une date", buttonText: "aujourd'hui" });
            }
            else {
                datebject.option({ watermarkText: "Select date", buttonText: "Today" });
            }

            // Setting the locale value dynamically for the datePicker
            datebject.setModel({ locale: args.value });
        }
     </script>
</body>
</html>  

{% endhighlight %}

### Applying the user-defined localized words collection in Grid control

There are other Syncfusion components like Grid, Gantt, FileExplorer and Schedule which defines a collection of custom localized-text for each culture. In order to apply those localized label collection appropriately for each custom-texts, we need to define separately a collection of culture based translated words for each culture as shown below,

N>   Based on the components and specific-culture names used in the application, we can define the localized words for it using the below syntax within the script section,   
N>               **ej.ClassName.Locale[Culture-Code] = { … };**

N>   For example, to define the localized words for the grid control in fr-FR culture, it can be done as follows,   
N>               **ej.Grid.Locale["fr-FR"] = { … };**


#### Example 2: Defining locale property in the Grid control using collection of localized text

Refer the same steps mentioned in the previous example – as it is applicable for this grid sample too, where only the control initialization needs to be done for grid control as shown below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.de-DE.min.js"></script>
</head>
<body> 
    <!--Container for ejGrid widget-->
    <div id="Grid"></div>
    <script type="text/javascript">
        $(function () {
            // declaration of ejGrid
            $("#Grid").ejGrid();
        });
    </script>
</body>
</html>   

{% endhighlight %}

Define the collection of custom localized-words for the **de-De** culture within the script section as shown below,

{% highlight javascript %}

       //localized words defined for de-DE culture
        ej.Grid.Locale["de-DE"] = {
            EmptyRecord: "Keine Aufzeichnungen angezeigt",
            GroupDropArea: "Ziehen Sie eine Spaltenüberschrift hier",
            DeleteOperationAlert: "Keine Einträge für Löschvorgang ausgewählt",
            EditOperationAlert: "Keine Einträge für Bearbeiten Betrieb ausgewählt",
            SaveButton: "Speichern",
            CancelButton: "stornieren",
            EditFormTitle: "Korrektur von",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}}Beiträge{{else}}Beiträges{{/if}}",
            UnGroup: "Klicken Sie hier, um die Gruppierung aufheben"
        };

{% endhighlight %}

Now define the **locale** property for the Grid control with the appropriate **culture-code [de-DE]** as shown below,

{% highlight html %}

<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.de-DE.min.js"></script>
</head>
<body> 
    <!--Container for ejGrid widget-->
    <div id="Grid"></div>
    <script type="text/javascript">
       //Collection of localized words defined for **de-DE** culture
        ej.Grid.Locale["de-DE"] = {
            EmptyRecord: "Keine Aufzeichnungen angezeigt",
            GroupDropArea: "Ziehen Sie eine Spaltenüberschrift hier",
            DeleteOperationAlert: "Keine Einträge für Löschvorgang ausgewählt",
            EditOperationAlert: "Keine Einträge für Bearbeiten Betrieb ausgewählt",
            SaveButton: "Speichern",
            CancelButton: "stornieren",
            EditFormTitle: "Korrektur von",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}}Beiträge{{else}}Beiträges{{/if}}",
            UnGroup: "Klicken Sie hier, um die Gruppierung aufheben"
        };
        $(function () {
            var localServ = "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders";
            var dataManger = ej.DataManager({
                url: localServ
            });

            $("#Grid").ejGrid({
                // the datasource is referred from remote service
                dataSource: dataManger,
                allowPaging: true,
                pageSettings: { pageCount: 5 },
                allowGrouping: true,
                editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Dialog },
                groupSettings:{enableDropAreaAnimation: false},
                // de-DE localization defined for Grid control
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
</body>
</html>    

{% endhighlight %}

Browse your HTML page in any of the web browser and now the screen will display the Grid control with the localized texts. Now double click on any of the row – the edit record dialog too pops-up with the localized words as shown below,
![](/js/Localization_images/Localization_img3.png) 

#### To change the locale property dynamically in Grid control

Define a dropdownlist control additionally in your HTML page along with the Grid control, to hold the required culture codes. When the user selects a particular culture code option from the dropdownlist, the grid control will get localized appropriately based on the dynamic selection made. Also, you need to define the collection of custom localized-words for all the required cultures (here, defined for **es-ES** and **de-DE** cultures) within the script section as depicted below,

N>   In the below example, copy the culture files of **de-DE** and **es-ES** into the Scripts folder of your application and refer it in the head section along with the other CSS and script references, so that the **locale** of the Grid control switches between the selected culture appropriately.

{% highlight html %}

   <!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
    <title>My first HTML page</title>
    <!-- CSS and Script reference section -->
    <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
    <script src="Scripts/jquery-1.10.2.min.js"></script>
    <script src="Scripts/jsrender.min.js"></script>
    <script src="Scripts/ej/ej.web.all.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.de-DE.min.js"></script>
    <script src="Scripts/ej/i18n/ej.culture.es-ES.min.js"></script>
</head>
<body> 
    <!--Container for ejGrid widget-->
    <div id="Grid"></div>

    <!--Container for ejDropDownList widget-->
    <select id="language">
         <option value="en-US">English</option>
         <option value="de-DE">Deutsch</option>
         <option value="es-ES">Español</option>
    </select>


    <script type="text/javascript">
       //Collection of localized words defined for de-DE & es-ES culture pre-defined
        ej.Grid.Locale["es-ES"] = {
            EmptyRecord: "No hay registros que mostrar",
            GroupDropArea: "Arrastre un encabezado de columna aquí",
            DeleteOperationAlert: "No hay registros seleccionados para la operación de eliminación",
            EditOperationAlert: "No hay registros seleccionados para la operación de edición",
            SaveButton: "guardar",
            CancelButton: "cancelar",
            EditFormTitle: "Editar detalles de",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}}artículo {{else}}artículos{{/if}}",
            UnGroup: "Haga clic aquí para desagrupar"
        };

        ej.Grid.Locale["de-DE"] = {
            EmptyRecord: "Keine Aufzeichnungen angezeigt",
            GroupDropArea: "Ziehen Sie eine Spaltenüberschrift hier",
            DeleteOperationAlert: "Keine Einträge für Löschvorgang ausgewählt",
            EditOperationAlert: "Keine Einträge für Bearbeiten Betrieb ausgewählt",
            SaveButton: "Speichern",
            CancelButton: "stornieren",
            EditFormTitle: "Korrektur von",
            GroupCaptionFormat: "{{:field}}: {{:key}} - {{:count}} {{if count == 1}}Beiträge{{else}}Beiträges{{/if}}",
            UnGroup: "Klicken Sie hier, um die Gruppierung aufheben"
        };

        $(function () {

            var localServ = "http://mvc.syncfusion.com/Services/Northwnd.svc/Orders";
            var dataManger = ej.DataManager({
                url: localServ
            });

            // declaration of ejGrid
            $("#Grid").ejGrid({
                // the datasource is referred from remote service
                dataSource: dataManger,
                allowPaging: true,
                pageSettings: { pageCount: 5 },
                allowGrouping: true,
                editSettings: { allowEditing: true, editMode: ej.Grid.EditMode.Dialog },
                groupSettings:{enableDropAreaAnimation: false},
                // de-DE localization defined for Grid control
                locale: "de-DE",
                columns: [
                              { field: "OrderID", headerText: "Order ID", isPrimaryKey: true, textAlign: ej.TextAlign.Right, width: 75 },
                              { field: "CustomerID", headerText: "Customer ID", width: 90 },
                              { field: "EmployeeID", headerText: "Employee ID", textAlign: ej.TextAlign.Right, width: 80 },
                              { field: "Freight", headerText: "Freight", textAlign: ej.TextAlign.Right, width: 75, format: "{0:C}" },
                              { field: "ShipCity", headerText: "Ship City", width: 110 }
                ]
            });
           // declaration of ejDropDownList
            $("#language").ejDropDownList({ 
                   change: "onChange", // Event raised when the dropdown selection changes
                   selectedItemIndex: 1 
            });
        });
      // event handler – when the dropdown selection option changes
      function onChange(args) {
           // Setting the locale value dynamically for the Grid control
           $("#Grid").ejGrid("model.locale", args.value);
      }
    </script>
</body>
</html>    

{% endhighlight %}


# Right To Left

All the **Essential JavaScript** **Widget** supports **RTL** option, when set to **true** will align the widget and its contents from **Right to Left**. The property **enableRTL** is used to handle this behavior and is set to false by default for all the widgets. 

**Example**: To display the DatePicker control from Right-To-Left, we need to define its **enableRTL** property to **true** as depicted below,

N> Add and refer the necessary **Scripts** and **Stylesheets** to your sample application, before initializing any of the controls.

{% highlight html %}


<!DOCTYPE html>
<html xmlns="http://www.w3.org/1999/xhtml">
    <head>
        <title>My first HTML page</title>
        <link href="Content/ej/web/default-theme/ej.web.all.min.css" rel="stylesheet" />
        <script src="Scripts/jquery-1.10.2.min.js"></script>
        <script src="Scripts/jsrender.min.js"></script>
        <script src="Scripts/ej/ej.web.all.min.js"></script>
        // Culture file reference to use the ar-DZ culture
        <script src="Scripts/ej/i18n/ej.culture.ar-DZ.min.js"></script>
    </head>
    <body>     
        <!--Container for ejDatePicker widget-->
        <input id="startDate" type="text" /> 

        <script type="text/javascript">
            $(function () {
                // initialization of ejDatePicker control with enableRTL property (Since the arabic script is the most widespread RTL writing system, therefore here we have showcased our datepicker control localized in one of the Arabic language.)
                $("#startDate").ejDatePicker({ locale: "ar-DZ", 
                      enableRTL: true,
                      watermarkText: "حدد تاريخ",
                      buttonText: "اليوم" 
                });
            });
        </script>
    </body>
</html>

{% endhighlight %}



The below screenshot displays the datepicker control from Right to left direction,

![](righttoleft_images\righttoleft_img1.png)






