---
layout: post
title: Localization-and-Translation-Support
description: localization and translation support
platform: js
control: OLAP Gauge
documentation: ug
---

## Localization and Translation Support

**Localization** is the process of customizing the user interface (UI) as locale-specific in order to display regional data. Using this feature, you can display the data in a specific language and culture, of a particular country or region. The **JavaScript OlapGauge** control provides inherent support to localize its UI.

The following table lists the default English localization User Interface based on French culture.

_Table: List of default English localization User Interface based on French culture_

<table>
<tr>
<td>
<b>Keywords</b></td><td>
<b>Values</b></td></tr>
<tr>
<td>
RevenueGoal</td><td>
"Revenu Objectifs",</td></tr>
<tr>
<td>
RevenueValue</td><td>
"Revenu Valeurs",</td></tr>
<tr>
<td>
RevenueFor</td><td>
"Revenu Pour",</td></tr>
<tr>
<td>
MDXqueryExecutionFailed</td><td>
"L'exécution de la requête MDX pas",</td></tr>
<tr>
<td>
PreparingAndExecutingMDXquery</td><td>
"Préparation et exécution d'une Requête MDX",</td></tr>
<tr>
<td>
MDXqueryExecutedSuccessfully</td><td>
"Requête MDX exécutée avec succès",</td></tr>
<tr>
<td>
RenderingStarted</td><td>
"Rendu en route",</td></tr>
<tr>
<td>
RenderingSucceeded</td><td>
"Rendu Réussi",</td></tr>
<tr>
<td>
RenderingFailed</td><td>
"Rendant pas"</td></tr>
</table>

The following code example illustrates you on how to localize **OlapGuage’s** User Interface (UI) based on “French” culture.

{% highlight js %}

 ej.olap.OlapGauge.locale["fr-FR"] = {
                        RevenueGoal: "Objectif de chiffre d'affaires",
                        RevenueValue: "Valeur du chiffre d'affaires",
                        RevenueFor: "Recettes pour",
                        MDXqueryExecutionFailed: "L'exécution de la requête MDX pas",
                        PreparingAndExecutingMDXquery: "La préparation et l'exécution de la requête MDX",
                        MDXqueryExecutedSuccessfully: "MDX requête exécutée avec succès",
                        RenderingStarted: "Rendu commencé",
                        RenderingSucceeded: "Rendu réussi",
                        RenderingFailed: "Rendant pas"
                    }

$(function () {
$("#OlapGauge1").ejOlapGauge({ url: "../wcf/OlapGaugeService.svc", enableTooltip: true,locale:"fr-FR",
                            backgroundColor: "transparent", 
                            scales: [{
                                showRanges: true, 
                                radius: 150, showScaleBar: true, size: 1,
                                border: {
                                    width: 0.5
                                },
                                showIndicators: true, showLabels: true,
                                pointers: [{
                                    type: "needle",
                                    showBackNeedle: true,
                                    backNeedleLength: 20,
                                    length: 120,
                                    width: 9
                                },
                        {
                            type: "marker",
                            markerType: "diamond",
                            distanceFromScale: 5,
                            placement: "center",
                            backgroundColor: "#29A4D9",
                            length: 25,
                            width: 15
                        }],
                                ticks: [{
                                    type: "major",
                                    distanceFromScale: 15,
                                    height: 16,
                                    width: 1, color: "#8c8c8c"
                                },
                                {
                                    type: "minor",
                                    height: 6,
                                    width: 1,
                                    distanceFromScale: 2,
                                    color: "#8c8c8c"
                                }],
                                labels: [{
                                    color: "#8c8c8c"
                                }],
                                ranges: [{
                                    distanceFromScale: -5,size:7,
                                    backgroundColor: "#fc0606",
                                    border: {color: "#fc0606"}
                                }, {
                                    distanceFromScale: -5, size: 7
                                }],
                                customLabels: [{
                                    position: { x: 180, y: 290 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 320 },
                                    font: { size: "10px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }, {
                                    position: { x: 180, y: 150 },
                                    font: { size: "12px", fontFamily: "Segoe UI", fontStyle: "Normal" }, color: "#666666"
                                }]
                            }]
                        });
                    });

{% endhighlight %}


> _**Note: In order to render the localized OLAP Gauge, You are required to reset the content available in both**_

    1. OLAP Gauge Control

    2. OLAP Cube

###Localizing Control Information

To apply control side localization, refer the following code example:

{% highlight html %}

ej.olap.OlapGauge.locale["zh-CN"] = {
//Corresponding keyword values needs to be set here.
}

{% endhighlight %}

###Localizing Cube Information

To render the localized Cube information, set **"Locale Identifier"** in the connection string.

{% highlight c# %}

//1036 refers to “fr-FR” culture.
string connectionString = "Data Source=localhost; Initial Catalog=Adventure Works DW; Locale Identifier=1036;";
DataManager = new OlapDataManager(connectionString);
DataManager.Culture = new System.Globalization.CultureInfo(1036);
DataManager.OverrideDefaultFormatStrings = true;

{% endhighlight %}

The following screenshot displays the **OlapGauge** with French localization.

{% include image.html url="/js/OlapGauge/Concepts-and-Features/Localization-and-Translation-Support_images/Localization-and-Translation-Support_img1.png" Caption="Localized OlapGuage"%}


