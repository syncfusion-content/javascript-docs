---
layout: post
title: Localization
description: localization 
platform: js
control: OlapChart
documentation: ug
---

# Localization

## Localization in OlapChart

We can localize the OlapChart controls text with a collection of localized strings using [`ej.olap.OlapChart.locale`](/js/api/ejolapchart#members:locale) for different cultures. By default, the OlapChart control is localized in **“en-US”.**

Following code example illustrates on how to localize OlapChart based on **“French”** culture.

{% highlight js %}

<html> 
  //...

<body>
    <!--Create a tag which acts as a container for OlapChart-->
    <div id="OlapChart1" style="width: 55%; height: 670px;"></div>
    <script type="text/javascript">
        $(function()
        {
            $("#OlapChart1").ejOlapChart(
            {
                url: "../wcf/OlapChartService.svc",
                //....
                locale: "fr-FR",
                //....
            });
        });
        ej.olap.OlapChart.locale["fr-FR"] = {
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

## Localization and Globalization of Cube Info

Content displayed within the OlapChart control are obtained from the OLAP Cube. So following are the steps that needs to be done to get the localized and globalized Cube content.

* To get the localized string based on different cultures, from OLAP Cube, we need to set **"Locale Identifier"** in the connection string to a specific culture. 
* To bind the globalized content in PivotGrid control, we need to set **"Culture"** and **"OverrideDefaultFormatStrings"** properties in OlapDataManager class to a specific culture. 
 
{% highlight c# %}

//1036 refers to “fr-FR” culture.
string connectionString = "Data Source=localhost; Initial Catalog=Adventure Works DW; Locale Identifier=1036;";
DataManager = new OlapDataManager(connectionString);
DataManager.Culture = new System.Globalization.CultureInfo(1036);
DataManager.OverrideDefaultFormatStrings = true;

{% endhighlight %}

![](Localization-and-Translation-support_images/Localization-and-Translation-support_img1.png) 

