---
layout: post
title: Localization
description: Localization and Globalization
platform: js
control: PivotClient
documentation: ug
---

# Localization and Globalization

## Localization in PivotClient control

We can localize the PivotClient control texts with a collection of localized strings using **"ej.PivotClient.Locale"** for different cultures.

N> By default, the PivotClient control is localized in **"en-US".**

Following code example illustrates on how to localize PivotClient based on **French** culture.

{% highlight javascript %}

    ej.PivotClient.Locale["fr-FR"] = {
        Sort: "Trier",
        SelectField: "sélectionnez Champ",
        LabelFilterLabel: "Afficher les éléments pour lesquels l'étiquette",
        ValueFilterLabel: "Voir les articles pour lesquels",
        LabelFilters: "Filtres d'étiquetage",
        BeginsWith: "Commence par",
        NotBeginsWith: "Non Commence par",
        EndsWith: "Se termine par",
        NotEndsWith: "Non Se termine par",
        Contains: "Contient",
        NotContains: "Ne contient pas",
        ValueFilters: "Filtres de valeur",
        ClearFilter: "Effacer le filtre",
        Equals: "Équivaut à",            
        Top10:"Top Count",		
	    EqualTo: "Égal à",
        NotEquals: "pas equals",
        GreaterThan: "Plus grand que",
        GreaterThanOrEqualTo: "Plus grand ou égal à",
        LessThan: "LessThan",
        LessThanOrEqualTo: "Moins que",
        Between: "Entre",
        NotBetween: "Entre pas",		
        DeferUpdate: "Différer Mise à jour",
        MDXQuery: "de requêtes MDX",
        Column: "Colonne",
        Row: "Rangée",
        Slicer: "Tranche",
        CubeSelector: "Sélecteur de Cube",
        ReportName: "Nom du rapport",
        NewReport: "Nouveau rapport",
        CubeDimensionBrowser: "Cube navigateur dimnesion",
        AddReport: "Ajouter un rapport",
        RemoveReport: "Retirer rapport",
        CannotRemoveSingleReport: "Vous ne pouvez pas supprimer Rapport unique",
        AreYouSureToDeleteTheReport: "Etes-vous sûr de vouloir supprimer le rapport",
        RenameReport: "Renommer rapport",
        SaveReport: "Enregistrer le rapport",
        LoadReport: "Rapport de charge",
        ToggleAxis: "Basculer Axis",
        ExportToExcel: "Exporter vers Excel",
        ExportToWord: "Exporter vers Word",
        ExportToPdf: "Exporter vers Pdf",
        FullScreen: "Plein écran",
        Grid: "Grille",
        Chart: "Graphiq",
        OK: "Bien",
        Cancel: "Annuler",
        MeasureEditor: "Mesurer éditeur",
        MemberEditor: "Sous la direction de membres",
        Measures: "Mesures",
        SortOrFilterColumn: " Tri/filtrage (colonne)",
        SortOrFilterRow: "Tri/filtrage (ligne)",
        SortingAndFiltering: " Trier et filtrer",
        Sorting: " Tri",
        Measure: "Mesurer",
        Order: " Ordre",
        Filtering: " Filtrage",
        Condition: " Condition ",
        Value: " Valeur ",
        PreserveHierarchy: "Préserver hiérarchie ",
        Ascending: " Croissant ",
        Descending: " Descendant ",
        Enable: " Permettre ",
        Disable: " Désactiver ",
        and: "et",	
        ReportList: "Liste des rapports",		
        Line: "ligne",
        Spline: "spline",
        Column: "colonne",
        Area: "zone",
        SplineArea: "spline zone",
        StepLine: "étape ligne",
        StepArea: "étape zone",
        Pie: "tarte",
        Bar: "bar",
        StackingArea: "Stacking zone",
        StackingColumn: "Colonne d'empilage",
        StackingBar: "Stacking bar",
        Pyramid: "pyramide",
        Funnel: "entonnoir",
        ChartTypes: "Types de graphiques",		
        Doughnut: "Donut",
        Scatter: "Scatter",
        Bubble: "bulle",
        TreeMap: "TreeMap",
        Alert: "Alerte",
        MDXAlertMsg: "S'il vous plaît ajouter une mesure, la dimension ou la hiérarchie dans un axe approprié pour afficher la requête MDX.",
        FilterSortRowAlertMsg: "Dimension pas trouvé dans l'axe de la ligne. S'il vous plaît ajouter élément de dimension dans l'axe de ligne de tri / filtrage.",
        FilterSortColumnAlertMsg: "Dimension se trouve pas dans l'axe de la colonne. S'il vous plaît ajouter élément de dimension dans l'axe de la colonne pour trier / filtrage",
        FilterSortcolMeasureAlertMsg: "S'il vous plaît ajouter mesure à l'axe de la colonne",
        FilterSortrowMeasureAlertMsg: "S'il vous plaît ajouter mesure à l'axe de rang.",
        FilterSortElementAlertMsg: "Elément ne se trouve pas dans l'axe de la colonne. S'il vous plaît ajouter un élément dans l'axe de la colonne pour trier / filtrage.",
        LoadReportAlertMsg: "S'il vous plaît sélectionner un rapport valide",
        FilterMeasureSelectionAlertMsg: "S'il vous plaît sélectionnez une mesure valide.",
        FilterConditionAlertMsg: "S'il vous plaît définir une condition valide.",
        FilterStartValueAlertMsg: "S'il vous plaît définir une valeur de départ.",
        FilterEndValueAlertMsg: "S'il vous plaît définir une valeur de fin.",
        FilterInvalidAlertMsg: "Opération invalide!"
    }
    ej.PivotGrid.Locale["fr-FR"] = {
        ToolTipRow: "Rangée",
        ToolTipColumn: "Colonne",
        ToolTipValue: "Valeur"
    }
    ej.PivotChart.Locale["fr-FR"] = {
        Measure: "Mesure",
        Row: "Rangée",
        Column: "Colonne",
        Value: "Valeur",
        Expand: "Développer",
        Collapse: "Effondrement",
        Exit: "Quitter"
    }
    ej.PivotSchemaDesigner.Locale["fr-FR"] = {
        ClearFilter: "Effacer le filtre",
        SelectField: "Select Field",
        Measures: "Les mesures",
        Warning: "Attention",
        AlertMsg: "Le champ que vous déplacez ne peut être placé dans cette zone du rapport",
        Measures: "Les mesures",
        Goal: "Objectif",
        Status: "statut",
        Trend: "Tendance",
        Value: "valeur",
        AddToFilter: "Ajouter au filtre",
        AddToRow: "Ajouter à la rangée",
        AddToColumn: "Ajouter à la colonne",
        AddToValues: "Ajouter à la valeur",
        PivotTableFieldList: "Liste des champs PivotTable",
        ChooseFieldsToAddToReport: "Choisissez les champs à ajouter à signaler :",
        DragFieldBetweenAreasBelow: "champs de glisser entre les zones ci-dessous:",
        ReportFilter: "Rapport Filtre",
        ColumnLabel: "Colonne Étiquette",
        RowLabel: "Label Row",
        Values: "Valeurs",
        DeferLayoutUpdate: "Différer la mise en page de mise à jour",
        Update: "Mettre à jour",
        OK: "D'accord",
        Cancel: "Annuler",
        Close: "Fermer"
    }

    $("#PivotClient1").ejPivotClient({
        url: "/OlapClient",    
        locale: "fr-FR"
    });

{% endhighlight %}

Following table localizes the in-built keywords to **French** culture for PivotClient.
<table>
<tr>
<th>
Keywords</th><th>
Values</th></tr>
<tr>
<td>
DeferUpdate</td><td>
"Différer Mise à jour"</td></tr>
<tr>
<td>
MDXQuery</td><td>
"de requêtes MDX"</td></tr>
<tr>
<td>
Column</td><td>
"Colonne"</td></tr>
<tr>
<td>
Row</td><td>
"Rangée"</td></tr>
<tr>
<td>
Slicer</td><td>
"Tranche"</td></tr>
<tr>
<td>
CubeSelector</td><td>
"Sélecteur de Cube"</td></tr>
<tr>
<td>
ReportName</td><td>
"Nom du rapport"</td></tr>
<tr>
<td>
NewReport</td><td>
"Nouveau rapport"</td></tr>
<tr>
<td>
CubeDimensionBrowser</td><td>
"Cube navigateur dimnesion"</td></tr>
<tr>
<td>
AddReport</td><td>
"Ajouter un rapport"</td></tr>
<tr>
<td>
RemoveReport</td><td>
"Retirer rapport"</td></tr>
<tr>
<td>
CannotRemoveSingleReport</td><td>
"Vous ne pouvez pas supprimer Rapport unique"</td></tr>
<tr>
<td>
AreYouSureToDeleteTheReport</td><td>
"Etes-vous sûr de vouloir supprimer le rapport"</td></tr>
<tr>
<td>
RenameReport</td><td>
"Renommer rapport"</td></tr>
<tr>
<td>
SaveReport</td><td>
"Enregistrer le rapport"</td></tr>
<tr>
<td>
LoadReport</td><td>
"Rapport de charge"</td></tr>
<tr>
<td>
ToggleAxis</td><td>
"Basculer Axis"</td></tr>
<tr>
<td>
ExportToExcel</td><td>
"Exporter vers Excel"</td></tr>
<tr>
<td>
ExportToWord</td><td>
"Exporter vers Word"</td></tr>
<tr>
<td>
ExportToPdf</td><td>
"Exporter vers PDF"</td></tr>
<tr>
<td>
FullScreen</td><td>
"Plein écran"</td></tr>
<tr>
<td>
Grid</td><td>
"Grille"</td></tr>
<tr>
<td>
Chart</td><td>
"Graphiq"</td></tr>
<tr>
<td>
OK</td><td>
"Bien"</td></tr>
<tr>
<td>
Cancel</td><td>
"Annuler"</td></tr>
<tr>
<td>
MeasureEditor</td><td>
"Mesurer éditeur"</td></tr>
<tr>
<td>
MemberEditor</td><td>
"Sous la direction de membres"</td></tr>
<tr>
<td>
Measures</td><td>
"Mesures"</td></tr>
<tr>
<td>
SortOrFilterColumn</td><td>
"Tri/filtrage (colonne)"</td></tr>
<tr>
<td>
SortOrFilterRow</td><td>
"Tri/filtrage (ligne)"</td></tr>
<tr>
<td>
SortingAndFiltering</td><td>
"Trier et filtrer"</td></tr>
<tr>
<td>
Sorting</td><td>
"Tri"</td></tr>
<tr>
<td>
Measure</td><td>
"Mesurer"</td></tr>
<tr>
<td>
Order</td><td>
"Ordre"</td></tr>
<tr>
<td>
Filtering</td><td>
"Filtrage"</td></tr>
<tr>
<td>
Condition</td><td>
"Condition"</td></tr>
<tr>
<td>
Value</td><td>
"Valeur"</td></tr>
<tr>
<td>
PreserveHierarchy</td><td>
"Préserver hiérarchie"</td></tr>
<tr>
<td>
Ascending</td><td>
"Croissant"</td></tr>
<tr>
<td>
Descending</td><td>
"Descendant"</td></tr>
<tr>
<td>
Enable</td><td>
"Permettre"</td></tr>
<tr>
<td>
Disable</td><td>
"Désactiver"</td></tr>
<tr>
<td>
And</td><td>
"et"</td></tr>
<tr>
<td>
Line</td><td>
"ligne"</td></tr>
<tr>
<td>
Spline</td><td>
"spline"</td></tr>
<tr>
<td>
Column</td><td>
"colonne"</td></tr>
<tr>
<td>
Area</td><td>
"zone"</td></tr>
<tr>
<td>
SplineArea</td><td>
"spline zone"</td></tr>
<tr>
<td>
StepLine</td><td>
"étape ligne"</td></tr>
<tr>
<td>
StepArea</td><td>
"étape zone"</td></tr>
<tr>
<td>
Pie</td><td>
"tarte"</td></tr>
<tr>
<td>
Bar</td><td>
"bar"</td></tr>
<tr>
<td>
StackingArea</td><td>
"Stacking zone"</td></tr>
<tr>
<td>
StackingColumn</td><td>
"Colonne d'empilage"</td></tr>
<tr>
<td>
StackingBar</td><td>
"Stacking bar"</td></tr>
<tr>
<td>
Pyramid</td><td>
"pyramide"</td></tr>
<tr>
<td>
Funnel</td><td>
"entonnoir"</td></tr>
<tr>
<td>
ChartTypes</td><td>
"Types de graphiques"</td></tr>
<tr>
<td>Sort</td>
<td>Trier</td>
</tr>  
<tr>
<td>SelectField</td>
<td>sélectionnez Champ</td>
</tr>
<tr>
<td>LabelFilterLabel</td>
<td>Afficher les éléments pour lesquels l'étiquette</td>
</tr>
<tr>
<td>ValueFilterLabel</td>
<td>Voir les articles pour lesquels</td>
</tr>    
<tr>
<td>LabelFilters</td>
<td>Filtres d'étiquetage</td>
</tr>
<tr>
<td>BeginsWith</td>
<td>Commence par</td>
</tr>
<tr>
<td>NotBeginsWith</td>
<td>Non Commence par</td>
</tr>
<tr>
<td>EndsWith</td>
<td>Se termine par</td>
</tr>     
<tr>
<td>NotEndsWith</td>
<td>Non Se termine par</td>
</tr>   
<tr>
<td>Contains</td>
<td>Contient</td>
</tr>    
<tr>
<td>NotContains</td>
<td>Ne contient pas</td>
</tr>
<tr>
<td>ValueFilters</td>
<td>Filtres de valeur</td>
</tr>
<tr>
<td>ClearFilter</td>
<td>Effacer le filtre</td>
</tr>
<tr>
<td>Equals</td>
<td>Équivaut à</td>
</tr>     
<tr>
<td>Top10</td>
<td>"Top Count"</td>
</tr>    
<tr>
<td>EqualTo</td>
<td>Égal à</td>
</tr>     
<tr>
<td>NotEquals</td>
<td>pas equals</td>
</tr>     
<tr>
<td>GreaterThan</td>
<td>Plus grand que</td>
</tr>     
<tr>
<td>GreaterThanOrEqualTo</td>
<td>Plus grand ou égal à</td>
</tr>

<tr>
<td>LessThan</td>
<td>Moins que</td>
</tr>
     
<tr>
<td>LessThanOrEqualTo</td>
<td>Inférieur ou égal à</td>
</tr>

<tr>
<td>Between</td>
<td>Entre</td>
</tr>
     
<tr>
<td>NotBetween</td>
<td>Entre pas</td>
</tr>

</table>

## Localization and Globalization of Cube Info (Client Mode)

Content displayed within the PivotClient control are obtained from the OLAP cube. Following are the steps to get the localized and globalized cube content.

* To get localized data from OLAP cube, we need to set **"Locale Identifier"** in the connection string to a specific culture in the **"data"** property present inside **"dataSource"**. 
* To bind the globalized content in PivotClient control, we need to set **"locale"** property to a specific culture and the specific culture file is referred in the sample. 
 
N> Culture files are present under **"[installed drive]:\Users\ [user name]\AppData\Local\Syncfusion\EssentialStudio\X.X.X.X\JavaScript\samples\web\scripts\cultures".** 
 
{% highlight javascript %}

    //1036 refers to “fr-FR” culture.
    $("#PivotClient1").ejPivotClient({
        dataSource: {
                data: "http://bi.syncfusion.com/olap/msmdpump.dll; Locale Identifier=1036;",
                //...
                },
                locale: "fr-FR",
                //...
    });

{% endhighlight %}

![](Localization_images/localization.png)
 
## Localization and Globalization of Cube (Server Mode)

Content displayed within the PivotClient control are obtained from the OLAP cube. Following are the steps to get the localized and globalized cube content.
 
* To get the localized string based on different cultures, from OLAP cube, you need to set **"Locale Identifier"** in the connection string to a specific culture.
* To bind the globalized content in PivotClient control, you need to set **"Culture"** and `OverrideDefaultFormatStrings` properties in OlapDataManager class to a specific culture. 

{% highlight c# %}

    //1036 refers to "fr-FR" culture.
    string connectionString = "Data Source=localhost; Initial Catalog=Adventure Works DW; Locale Identifier=1036;";
    DataManager = new OlapDataManager(connectionString);
    DataManager.Culture = new System.Globalization.CultureInfo(1036);
    DataManager.OverrideDefaultFormatStrings = true;

{% endhighlight %}

![](Localization_images/localization-servermode.png)

## Localization and Globalization of Relational Info (Client Mode)

Content displayed within the PivotClient control are obtained from the Relational datasource. Following are the steps to get localized as well as globalized content.
 
* To get the localized content, the Relational datasource must have localized headers in them which will be directly applied to PivotClient.  
* To globalize the values appeared in PivotClient, we need to set the **"format"** and **"locale"** property accordingly.  Also the specific culture file is referred in the sample. 

N> Culture files are present under **"[installed drive]:\Users\ [user name]\AppData\Local\Syncfusion\EssentialStudio\X.X.X.X\JavaScript\samples\web\scripts\cultures".** 
 
{% highlight javascript %}

    $("#PivotClient1").ejPivotClient({
        dataSource: {
            //...
            values: [{
                fieldName: "Amount",
                fieldCaption: "Montant",
                format: "currency"
            }]
        },
        locale:"fr-FR"
    });
{% endhighlight %}

![](Localization_images/relational-localization.png)

## Localization and Globalization of Relational Info (Server Mode)
Content displayed within the PivotClient control are obtained from the Relational datasource. Following are the steps to get localized as well as globalized content.
 
* To get the localized content, the Relational datasource must have localized headers in them which will be directly applied to PivotClient.  
* **“Format”** settings in PivotComputationInfo class would globalize the values appeared in PivotClient.

{% highlight c# %}

    PivotReport pivotSetting = new PivotReport();
    //...
    pivotSetting.PivotCalculations.Add(new PivotComputationInfo {
        CalculationName = "Amount", Description = "Amount", FieldHeader = "Amount", FieldName = "Amount", Format = "C", SummaryType = Syncfusion.PivotAnalysis.Base.SummaryType.DoubleTotalSum
    });
    //...

{% endhighlight %}

![](Localization_images/relational-localization.png)

## RTL

You can render our PivotClient control from Right to Left by setting [`enableRTL`](/js/api/ejPivotClient#members:enablertl) property to true.

{% highlight javascript %}

    $(function() {
        $("#PivotClient1").ejPivotClient({
            //...
            enableRTL: true
        });
    });

{% endhighlight %}

![](Localization_images/rtl.png)
