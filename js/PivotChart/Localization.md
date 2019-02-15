---
layout: post
title: Localization with PivotChart widget for Syncfusion Essential JS
description: localization
platform: js
control: PivotChart
documentation: ug
api: /api/js/ejpivotchart
---

# Localization

## Localization in pivot chart

You can localize the pivot chart controls text with a collection of localized strings using [`ej.PivotChart.Locale`](/api/js/ejpivotchart#members:locale) for different cultures. By default, the pivot chart control is localized in **“en-US”.**

The following code example illustrates the steps to localize the pivot chart based on the **“French”** culture.

{% highlight javascript %}

<html>
  //...

<body>
    <!--Create a tag which acts as a container for PivotChart-->
    <div id="PivotChart1" style="width: 55%; height: 670px;"></div>
    <script type="text/javascript">
        $(function()
        {
            $("#PivotChart1").ejPivotChart(
            {
                //....
                locale: "fr-FR",
                //....
            });
        });
        ej.PivotChart.Locale["fr-FR"] = {
            Measure: "Mesure",
            Row: "Rangée",
            Column: "Colonne",
            Value: "Valeur",
            Expand: "Développer",
            Collapse: "Effondrement",
            Exit: "Quitter"
        };
    </script>
</body>

</html>

{% endhighlight %}

The following table localizes the in-built keywords to **“French”** culture for the pivot chart.

<table>
<tr>
<th>
Keywords</th><th>
Values</th>
</tr>
<tr><td>
Measure</td><td>
“Mesure”</td>
</tr>
<tr><td>
Row</td><td>
"Rangée "</td>
</tr>
<tr><td>
Column</td><td>
"Colonne”</td>
</tr>
<tr><td>
Value</td><td>
"Valeur "</td>
</tr>
<tr><td>
Expand</td><td>
"Développer "</td>
</tr>
<tr><td>
Collapse</td><td>
"Effondrement "</td>
</tr>
<tr><td>
Exit</td><td>
“Quitter "</td>
</tr>
</table>

## Localization and globalization of cube info (client mode)

The content displayed within the pivot chart control is obtained from the OLAP cube. The following are the steps that should be done to get the localized and globalized cube content.

* To get the localized data from the OLAP cube, set the **"Locale Identifier"** in the connection string to a specific culture in the **"data"** property present in the **"dataSource"**.
* To bind the globalized content in the pivot chart control, set the **"locale"** property to a specific culture and refer the specific culture file in the sample.

N> Culture files are present under **"[installed drive]:\Users\ [user name]\AppData\Local\Syncfusion\EssentialStudio\X.X.X.X\JavaScript\samples\web\scripts\cultures".**

{% highlight js %}

//1036 refers to “fr-FR” culture.
 $("#PivotChart1").ejPivotChart({
      dataSource: {
            data: "https://bi.syncfusion.com/olap/msmdpump.dll; Locale Identifier=1036;",
            ......
            },
            locale: "fr-FR",
            .....
 });

{% endhighlight %}

## Localization and globalization of cube info (server mode)

The content displayed within the pivot chart control is obtained from the OLAP cube. The following are the steps that should be done to get the localized and globalized cube content:

* To get the localized string based on different cultures, set the **"Locale Identifier"** in the connection string to a specific culture in the OLAP cube.
* To bind the globalized content in the pivot chart control, you can set the **"Culture"** and **"OverrideDefaultFormatStrings"** properties in the OlapDataManager class to a specific culture.

{% highlight c# %}

//1036 refers to “fr-FR” culture.
string connectionString = "Data Source=localhost; Initial Catalog=Adventure Works DW; Locale Identifier=1036;";
DataManager = new OlapDataManager(connectionString);
DataManager.Culture = new System.Globalization.CultureInfo(1036);
DataManager.OverrideDefaultFormatStrings = true;

{% endhighlight %}

![Localization support in JavaScript pivot chart control](Localization-and-Translation-support_images/Localization-and-Translation-support_img1.png)

## RTL

You can enable or disable the right to left alignment by using the [`enableRTL`](/api/js/ejpivotchart#members:enablertl) property in the pivot chart.

{% highlight js %}

$("#PivotChart1").ejPivotChart({
      enableRTL: true
 });

{% endhighlight %}

![Right to Left, aka RTL support in JavaScript pivot chart control](Localization-and-Translation-support_images/Rtl.png)

N> RTL is applicable only for the tooltip of the pivot chart.


