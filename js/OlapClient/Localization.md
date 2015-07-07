---
layout: post
title: Localization
description: localization 
platform: js
control: OlapClient
documentation: ug
---

# Localization 

The **Essential JavaScript OlapClient** control provides inherent support to localize its **UI**.

The following table lists the default English localization User Interface based on French culture.


<table>
<tr>
<th>
Keywords</th><th>
Values</th></tr>
<tr>
<td>
Column</td><td>
"Colonne “</td></tr>
<tr>
<td>
Row</td><td>
"Rangée"</td></tr>
<tr>
<td>
Slicer</td><td>
"tranche"</td></tr>
<tr>
<td>
CubeSelector</td><td>
"Sélecteur de Cube",</td></tr>
<tr>
<td>
ReportName</td><td>
"Nom du rapport",</td></tr>
<tr>
<td>
NewReport</td><td>
"Nouveau rapport",</td></tr>
<tr>
<td>
CubeDimensionBrowser</td><td>
"Cube navigateur dimnesion",</td></tr>
<tr>
<td>
AddReport</td><td>
"Ajouter un rapport",</td></tr>
<tr>
<td>
RemoveReport</td><td>
"Retirer rapport",</td></tr>
<tr>
<td>
CannotRemoveSingleReport</td><td>
"Vous ne pouvez pas supprimer Rapport unique",</td></tr>
<tr>
<td>
AreYouSureToDeleteTheReport</td><td>
"Etes-vous sûr de vouloir supprimer le rapport",</td></tr>
<tr>
<td>
RenameReport</td><td>
"Renommer rapport",</td></tr>
<tr>
<td>
SaveReport</td><td>
"Enregistrer le rapport",</td></tr>
<tr>
<td>
LoadReport</td><td>
"Rapport de charge",</td></tr>
<tr>
<td>
ExportToExcel:</td><td>
"Exporter vers Excel",</td></tr>
<tr>
<td>
FullScreen</td><td>
"Plein écran",</td></tr>
<tr>
<td>
Grid</td><td>
"Grille",</td></tr>
<tr>
<td>
Chart</td><td>
"Graphiq",</td></tr>
<tr>
<td>
OK</td><td>
"Bien",</td></tr>
<tr>
<td>
Cancel</td><td>
"Annuler",</td></tr>
<tr>
<td>
MeasureEditor</td><td>
"Mesurer éditeur",</td></tr>
<tr>
<td>
MemberEditor:</td><td>
"Sous la direction de membres",</td></tr>
<tr>
<td>
Measures</td><td>
"Mesures",</td></tr>
<tr>
<td>
OpeningDialog</td><td>
"Dialogue d'ouverture",</td></tr>
<tr>
<td>
OpeningDialogSucceeded</td><td>
"Dialogue d'ouverture réussi",</td></tr>
<tr>
<td>
PreparingAndExecutingMDXquery</td><td>
"la préparation et l'exécution de la requête MDX"</td></tr>
<tr>
<td>
MDXqueryExecutionFailed</td><td>
"L'exécution de la requête MDX pas",</td></tr>
<tr>
<td>
MDXqueryExecutedSuccessfully</td><td>
"MDX requête exécutée avec succès"</td></tr>
<tr>
<td>
RenderingLayoutStarted</td><td>
"Disposition rendant commencé",</td></tr>
<tr>
<td>
RenderingLayoutCompleted,</td><td>
" Disposition rendant terminé",</td></tr>
<tr>
<td>
RenderingStarted</td><td>
"Rendu commencé",</td></tr>
<tr>
<td>
RenderingSucceeded</td><td>
"Rendu Réussi",</td></tr>
<tr>
<td>
SortOrFilterColumn</td><td>
" Tri/filtrage (colonne)",</td></tr>
<tr>
<td>
SortOrFilterRow</td><td>
"Tri/filtrage (ligne)",</td></tr>
<tr>
<td>
SortingAndFiltering</td><td>
" Trier et filtrer",</td></tr>
<tr>
<td>
Sorting</td><td>
" Tri",</td></tr>
<tr>
<td>
Measure</td><td>
" Mesurer",</td></tr>
<tr>
<td>
Order</td><td>
" ordre",</td></tr>
<tr>
<td>
Filtering</td><td>
" Filtrage",</td></tr>
<tr>
<td>
Condition</td><td>
" Condition ",</td></tr>
<tr>
<td>
Value</td><td>
" Valeur ",</td></tr>
<tr>
<td>
PreserveHierarchy</td><td>
" Préserver hiérarchie ",</td></tr>
<tr>
<td>
Ascending</td><td>
" Croissant ",</td></tr>
<tr>
<td>
Descending</td><td>
" Descendant ",</td></tr>
<tr>
<td>
Enable</td><td>
" Permettre ",</td></tr>
<tr>
<td>
Disable</td><td>
" Désactiver ",</td></tr>
<tr>
<td>
And</td><td>
" et "</td></tr>
</table>

The following code example shows how to localize OlapClient’s User Interface (UI) based on French culture with the help of [locale](/js/api/ejOlapClient#localespan-classtype-signature-type-stringstringspan) property.

{% highlight js %}

$("#OlapClient1").ejOlapClient({ url: "../wcf/OlapClientService.svc", **locale:"fr-FR"** }); 


{% endhighlight %}

{% highlight js %}

ej.olap.OlapClient.locale["fr-FR"] = {
Column:"Colonne",
Row:"Rangée",
Slicer:"tranche",
CubeSelector:"Sélecteur de Cube",
ReportName:"Nom du rapport",
NewReport:"nouveau rapport",
CubeDimensionBrowser:"Cube navigateur dimnesion",
AddReport:"Ajouter un rapport",
RemoveReport:"Retirer rapport",
CannotRemoveSingleReport:"Vous ne pouvez pas supprimer Rapport unique",
AreYouSureToDeleteTheReport:"Etes-vous sûr de vouloir supprimer le rapport",
RenameReport:"Renommer rapport",
SaveReport:"Enregistrer le rapport",
LoadReport:"Rapport de charge",
ExportToExcel:"Exporter vers Excel",
ExportToWord:"Exporter vers Word",
ExportToPdf:"Exporter vers Pdf",
FullScreen:"Plein écran",
Grid:"Grille",
Chart:"Graphiq",
OK:"bien",
Cancel:"Annuler",
MeasureEditor:"Mesurer éditeur",
MemberEditor:"Sous la direction de membres",
Measures:"Mesures",
OpeningDialog:"Dialogue d'ouverture",
OpeningDialogSucceeded:"Dialogue d'ouverture réussi",
RenderingLayoutStarted:"Disposition rendant commencé",
RenderingLayoutCompleted:"disposition rendant terminé",
MDXqueryExecutionFailed:"L'exécution de la requête MDX pas",
PreparingAndExecutingMDXquery:"la préparation et l'exécution de la requête MDX",
MDXqueryExecutedSuccessfully:"MDX requête exécutée avec succès",
RenderingStarted:"Rendu commencé",
RenderingSucceeded:"Rendu Réussi",
RenderingFailed:"Rendant pas",
SortOrFilterColumn:" tri/filtrage (colonne)",
SortOrFilterRow:"tri/filtrage (ligne)",
SortingAndFiltering:" trier et filtrer",
Sorting:" Tri",
Measure:"mesurer",
Order:"Ordre",
Filtering:"Filtrage",
Condition:" condition ",
Value:" valeur ",
PreserveHierarchy:" préserver hiérarchie ",
Ascending:"Croissant ",
Descending:"Descendant ",
Enable:" Permettre ",
Disable:" Désactiver ",
and:"et "
}
ej.olap.OlapChart.locale["fr-FR"] = {
Row:"Rangée",
Column:"Colonne",
Value:"Valeur",
Expand:"Développer",
Collapse:"Effondrement",
Exit:"Quitter"
}
ej.PivotGrid.locale["fr-FR"] = {
ToolTipRow: "Rangée",
ToolTipColumn: "Colonne",
ToolTipValue: "Valeur"
}


{% endhighlight %}

> **Note:** In order to render the localized OlapClient, we need to reset the content available in both OlapClient Control and OLAP Cube

##Localizing Control Information

To apply control side localization, use the following code example.

{% highlight html %}

ej.olap.OlapClient.locale["zh-CN"]={
//Corresponding keyword values needs to be set here.
}


{% endhighlight %}

##Localizing Cube Information

To get the localized Cube information,set `Locale Identifier` in the connection string.

{% highlight c# %}

//1036 refers to“fr-FR” culture.
string connectionString = "Data Source=localhost; Initial Catalog=Adventure Works DW; Locale Identifier=1036;";
DataManager = new OlapDataManager(connectionString);
DataManager.Culture = new System.Globalization.CultureInfo(1036);
DataManager.OverrideDefaultFormatStrings = true;


{% endhighlight %}

The following screenshot shows the OlapClient with French localization.

{% include image.html url="/js/OlapClient/Localization_images/Localization_img1.png" %}


