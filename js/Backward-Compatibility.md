---
layout: post
title: Backward-Compatibility
description: backward compatibility
platform: js
control: Introduction
documentation: ug
---

# Backward Compatibility

## Version 12.2 Changes

As a part of an effort to improve the user experience and provide consistent API across all our controls, we have made significant changes to the API namings effective from Volume 2, 2014 release. We have documented the changes with mapping between the old and new API names to enable quick up gradation of any control. The users whoever needs to migrate **from Volume 1, 2014 or from earlier versions to this Volume-2, 2014**, needs to refer the below specified API changes,

List of **common changes** made for all the components are as follows,

<table>
<tr>
<th>
Member Type</th><th>
Old Enum Property</th><th>
New Enum Property</th></tr>
<tr>
<td>
<b>Enum</b></td><td>
ej.textAlign = {   <br/>
&nbsp; Center: 'center',<br/>
&nbsp; Justify: 'justify',<br/>
&nbsp; Left: 'left',<br/>
&nbsp; Right: 'right'<br/>
};</td><td>
ej.TextAlign = {    <br/>
&nbsp;Center: 'center',  <br/>
&nbsp;Justify: 'justify', <br/>
&nbsp;Left: 'left',  <br/>
&nbsp;Right: 'right'<br/>
};</td></tr>
<tr>
<td>
 </td><td>
ej.orientation = {   <br/>
   &nbsp;Horizontal: "horizontal",<br/>
   &nbsp;Vertical: "vertical" <br/>
}; </td><td>
ej.Orientation = {    <br/>
  &nbsp;Horizontal: "horizontal",<br/>
  &nbsp;Vertical:"vertical"<br/> 
}; </td></tr>
</table>



The other changes based on each components are as follows,

<table>
<tr>
<td>
<a href="#ejAccordion">ejAccordion</a></td><td>
<a href="#ejDiagram">ejDiagram</a></td><td>
<a href="#ejOlapClient">ejOlapClient</a></td><td>
<a href="#ejScroller">ejScroller</a></td></tr>
<tr>
<td>
<a href="#ejAutoComplete">ejAutoComplete</a></td><td>
<a href="#ejDialog">ejDialog</a></td><td>
<a href="#ejOlapGauge">ejOlapGauge</a></td><td>
<a href="#ejSlider">ejSlider</a></td></tr>
<tr>
<td>
<a href="#ejBarcode">ejBarcode</a></td><td>
<a href="#ejDigitalGauge">ejDigitalGauge</a></td><td>
<a href="#ejOlapGauge">ejOlapGrid</a></td><td>
<a href="#ejSplitButton">ejSplitButton</a></td></tr>
<tr>
<td>
<a href="#ejBulletGraph">ejBulletGraph</a></td><td>
<a href="#ejDropDownList">ejDropDownList</a></td><td>
<a href="#ejTextBoxes">ejPercentageTextbox</a></td><td>
<a href="#ejSplitter">ejSplitter</a></td></tr>
<tr>
<td>
<a href="#ejButton">ejButton</a></td><td>
<a href="#ejGantt">ejGantt</a></td><td>
<a href="#ejPivotPager">ejPivotPager</a></td><td>
<a href="#ejTab">ejTab</a></td></tr>
<tr>
<td>
<a href="#ejChart">ejChart</a></td><td>
<a href="#ejGrid">ejGrid</a></td><td>
<a href="#ejProgressbar">ejProgressbar</a></td><td>
<a href="#ejTagCloud">ejTagCloud</a></td></tr>
<tr>
<td>
<a href="#ejCheckbox">ejCheckbox</a></td><td>
<a href="#ejLinearGauge">ejLinearGauge</a></td><td>
<a href="#ejRadioButton">ejRadioButton</a></td><td>
<a href="#ejTimePicker">ejTimePicker</a></td></tr>
<tr>
<td>
<a href="#ejCircularGauge">ejCircularGauge</a></td><td>
<a href="#ejMaps">ejMaps</a></td><td>
<a href="#ejRangeNavigator">ejRangeNavigator</a></td><td>
<a href="#ejToolbar">ejToolbar</a></td></tr>
<tr>
<td><a href="#ejColorPicker">ejColorPicker</a></td><td>
<a href="#ejMaskEdit">ejMaskEdit</a></td><td>
<a href="#ejRating">ejRating</a></td><td>
<a href="#ejToggleButton">ejToggleButton</a></td></tr>
<tr>
<td>
<a href="#ejTextBoxes">ejCurrencyTextbox</a></td><td>
<a href="#ejMenu">ejMenu</a></td><td>
<a href="#ejRichTextEditor">ejRichTextEditor</a></td><td>
<a href="#ejTreeView">ejTreeView</a></td></tr>
<tr>
<td>
<a href="#ejDatePicker">ejDatePicker</a></td><td>
<a href="#ejTextBoxes">ejNumericTextbox</a></td><td>
<a href="#ejRotator">ejRotator</a></td><td>
<a href="#ejTreeMap">ejTreeMap</a></td></tr>
<tr>
<td>
<a href="#ejDateTimePicker">ejDateTimePicker</a></td><td>
<a href="#ejOlapChart">ejOlapChart</a></td><td>
<a href="#ejSchedule">ejSchedule</a></td><td>
<a href="#ejUploadBox">ejUploadBox</a></td>
</tr>
</table>

<a name="ejaccordion"></a>

### ejAccordion

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API  Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "7">
   <b>Properties</b></td><td>
ajaxOptions</td><td>
ajaxSettings</td><td>
 </td></tr>
<tr>
<td>
iconCSS</td><td>
customIcon</td><td>
 </td></tr>
<tr>
<td>
heightStyle</td><td>
heightAdjustMode</td><td>
 </td></tr>
<tr>
<td>
Rtl</td><td>
enableRTL</td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
multipleOpen</td><td>
enableMultipleOpen</td><td>
 </td></tr>
<tr>
<td>
Persist</td><td>
enablePersistence </td><td>
 </td></tr>
<tr>
<td rowspan = "7">
   Methods</td><td>
disableAll</td><td>
 </td><td>
We have removed this method. Use <b>disable method</b> to achieve this behaviour</td></tr>
<tr>
<td>
disableItemByIndex</td><td>
 </td><td>
We removed this method. Use <b>disableItems method </b> to achieve this behaviour</td></tr>
<tr>
<td>
enableAll</td><td>
 </td><td>
We have removed this method. Use <b>enable method</b> to achieve this behaviour</td></tr>
<tr>
<td>
hideAccordion</td><td>
 </td><td>
We have removed this method. Already we have <b>hide </b>method to achieve this behaviour</td></tr>
<tr>
<td>
panelCount</td><td>
 getItemsCount</td><td>
 </td></tr>
<tr>
<td>
Selected</td><td>
 </td><td>
We have removed this method. We can achieve this scenario through <b>selectedItemIndex </b>property</td></tr>
<tr>
<td>
showAccordion</td><td>
 </td><td>
We have removed this method. Already we have <b>show method</b> to achieve this behaviour</td></tr>
<tr>
<td>
 <b>Enum</b></td> <td>
 ej.Accordion.heightFormat = { <br/>
    &nbsp;Content: "content",<br/>
    &nbsp;Auto: "auto",<br/>
    &nbsp;Fill: "fill"<br/>
    }; </td> <td>
 ej.Accordion.HeightAdjustMode ={<br/>
    &nbsp;Content: "content",<br/>
    &nbsp;Auto: "auto",<br/>
    &nbsp;Fill: "fill"<br/> 
    };</td><td>
 </td></tr>
<tr>
<th>
Event Name</th><th>
Old Event args</th><th>
New Event args</th><th>
comments</th></tr>
<tr>
<td>
ajaxLoad</td><td>
 </td><td>
args.url</td><td>
New event argument</td></tr>
<tr>
<td>
Active</td><td>
args.activePanel</td><td>
 </td><td>
Removed event argument</td></tr>
</table>

<a name="ejautocomplete"></a>

### ejAutoComplete

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
comments</th></tr>
<tr>
<td rowspan = "19">
  <b>Properties</b></td><td>
fields: {uniqueKeyhtmlAttr}</td><td>
key,htmlAttributes</td><td>
 </td></tr>
<tr>
<td>
Grouping</td><td>
allowGrouping</td><td>
 </td></tr>
<tr>
<td>
Distinct</td><td>
enableDistinct</td><td>
 </td></tr>
<tr>
<td>
sortOrder</td><td>
sortingOrder</td><td>
 </td></tr>
<tr>
<td>
allowNew</td><td>
allowAddNew</td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
Watermark</td><td>
watermarkText</td><td>
 </td></tr>
<tr>
<td>
Filter</td><td>
filterType</td><td>
 </td></tr>
<tr>
<td>
caseSensitive</td><td>
caseSensitiveSearch</td><td>
 </td></tr>
<tr>
<td>
loadingImage</td><td>
showLoadingIcon</td><td>
 </td></tr>
<tr>
<td>
listSize </td><td>
itemsCount</td><td>
 </td></tr>
<tr>
<td>
dropdown</td><td>
showPopupButton</td><td>
 </td></tr>
<tr>
<td>
autoFill</td><td>
enableAutoFill</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL </td><td>
 </td></tr>
<tr>
<td>
noResults</td><td>
emptyResultText</td><td>
 </td></tr>
<tr>
<td>
showNoResults</td><td>
showEmptyResultText</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence </td><td>
 </td></tr>
<tr>
<td>
suggestionBoxHeight</td><td>
popupHeight</td><td>
 </td></tr>
<tr>
<td>
suggestionBoxWidth </td><td>
popupWidth</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
 <b>Enum</b></td><td>
 ej.sortingOrder = { <br/> 
       &nbsp;&nbsp;Ascending: "ascending",<br/>
       &nbsp;&nbsp;Descending: "descending"<br/>
       }; </td><td>
 ej.SortOrder = { <br/>
       &nbsp;&nbsp;Ascending: "ascending",<br/>
       &nbsp;&nbsp;Descending: "descending" <br/>
       };</td><td>
</td></tr>
<tr>
<td>
 ej.multiSelectMode = {<br/>
    &nbsp;&nbsp;None: "none",<br/>
    &nbsp;&nbsp;Delimiter: "delimiter",<br/>
    &nbsp;&nbsp;VisualMode: "visualmode"<br/>
    } </td><td>
 ej.MultiSelectMode = { <br/>
    &nbsp;&nbsp;None: "none",<br/>
    &nbsp;&nbsp;Delimiter: "delimiter",<br/> 
   &nbsp;&nbsp;VisualMode: "visualmode"<br/>
    }</td><td>
 </td></tr>
<tr>
<th>
Event Name</th><th>
Old Event args</th><th>
New Event args</th><th>
comments</th></tr>
<tr>
<td>
focusIn</td><td>
 </td><td>
args.value</td><td>
New event argument</td></tr>
<tr>
<td>
focusOut</td><td>
 </td><td>
args.value</td><td>
New event argument</td></tr>
<tr>
<td>
select</td><td>
args.selectedText</td><td>
args.text</td><td>
 </td></tr>
</table>

<a name="ejbarcode"></a>
### ejBarcode

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td>
SymbologyType(Enum)</td><td>
symbologyType</td><td>
SymbologyType</td><td>
 </td></tr>
</table>

<a name="ejbulletgraph"></a>
### ejBulletGraph

<table>
<tr>
<td>
<b>Member Type</b></td><td colspan = "3">
<b>Old API</b></td><td colspan = "2">
<b>New API</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "14">
<b>Property</b></td><td colspan = "3">
 comparativeMeasureSymbolStroke comparativeMeasureSymbolStrokeThickness</td><td colspan = "2">
 comparativeMeasureSettings.stroke,comparativeMeasureSettings.width</td><td>
comparativeMeasureSymbolStroke, comparativeMeasureSymbolStrokeThicknessproperties are renamed as stroke,width and movedunder<b>comparativeMeasureSettings</b></td></tr>
<tr>
<td colspan = "3">
majorTickSizemajorTickStrokemajorTickStrokeThickness</td><td colspan = "2">
majorTickSettings.size, majorTickSettings.stroke,majorTickSettings.width</td><td>
majorTickSize,majorTickStroke,majorTickStrokeThickness properties are renamed as size, stroke, width and moved under <b>majorTickSettings</b></td></tr>
<tr>
<td colspan = "3">
minorTickSizeminorTickStrokeminorTickStrokeThickness</td><td colspan = "2">
minorTickSettings.size, minorTickSettings.stroke,minorTickSettings.width</td><td>
minorTickSize,minorTickStroke,majorTickStrokeThickness properties are renamed as size, stroke, width and moved under <b>minorTickSettings</b></td></tr>
<tr>
<td colspan = "3">
featuredMeasureBarStrokefeaturedMeasureBarStrokeThickness</td><td colspan = "2">
featuredMeasureSettings.stroke,featuredMeasureSettings.width</td><td>
featuredMeasureBarStroke,featuredMeasureBarStrokeThicknessproperties are renamed as stroke, width and moved under <b>featuredMeasureSettings</b></td></tr>
<tr>
<td colspan = "3">
showTooltiptooltipTemplateID</td><td colspan = "2">
tooltip.visible, tooltip.template</td><td>
Tooltip visible property andtemplate property is moved to“<b>tooltip</b>” object</td></tr>
<tr>
<td colspan = "3">
canResize</td><td colspan = "2">
enableResizing</td><td>
canResize property is renamed to<b>enableResizing</b></td></tr>
<tr>
<td colspan = "3">
bindRangeStrokeToLabels</td><td colspan = "2">
applyRangeStrokeToLabels</td><td>
bindRangeStrokeToLabelsproperty is renamed to<b>applyRangeStrokeToLabels</b></td></tr>
<tr>
<td colspan = "3">
bindRangeStrokeToTicks</td><td colspan = "2">
applyRangeStrokeToTicks</td><td>
bindRangeStrokeToTicks propertyis renamed to<b>applyRangeStrokeToTicks</b></td></tr>
<tr>
<td colspan = "3">
featureMeasure</td><td colspan = "2">
featureMeasures</td><td>
featureMeasureproperty isrenamed to<b>featureMeasures</b></td></tr>
<tr>
<td colspan = "3">
caption</td><td colspan = "2">
captionSettings</td><td>
caption property isrenamed to<b>captionSettings</b></td></tr>
<tr>
<td colspan = "3">
caption.subtitle</td><td colspan = "2">
captionSettings.subTitle </td><td>
subtitle in caption is renamed  as<b>subTitle </b>and moved under<b>captionSettings</b></td></tr>
<tr>
<td colspan = "3">
quantitativeScale</td><td colspan = "2">
quantitativeScaleSettings</td><td>
quantitativeScale is renamed to<b>quantitativeScaleSettings</b></td></tr>
<tr>
<td colspan = "3">
quantitativeScale.labels:                           {         labelStroke,        labelSize,        labelOffset        labelPosition   }</td><td colspan = "2">
quantitativeScaleSettings.labelSettings: {      stroke,      size      offset      position }</td><td>
labels in quantitativeScale is renamed to <b>labelSettings</b> and the inner properties are renamed to <b>stroke, size, offset, position</b></td></tr>
<tr>
<td colspan = "3">
tooltip</td><td colspan = "2">
tooltipSettings</td><td>
Renamed tooltip property to <b>tooltipSettings</b></td></tr>
<tr>
<td>
<b>Member Type</b></td><td colspan = "2">
<b>Old Enum Name</b></td><td colspan = "3">
<b>New Enum Name</b></td><td colspan = "2">
<b>Comments</b></td></tr>
<tr>
<td rowspan = "7">
<b>Enum</b></td><td colspan = "2">
ej.BulletGraph.orientation</td><td colspan = "3">
ej.datavisualization.BulletGraph.Orientation</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.tickPosition</td><td colspan = "3">
ej.datavisualization.BulletGraph.TickPosition</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.labelPosition</td><td colspan = "3">
ej.datavisualization.BulletGraph.LabelPosition </td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.flowDirection</td><td colspan = "3">
ej.datavisualization.BulletGraph.FlowDirection</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.fontStyle</td><td colspan = "3">
ej.datavisualization.BulletGraph.FontStyle</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.fontWeight</td><td colspan = "3">
ej.datavisualization.BulletGraph.FontWeight</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
ej.BulletGraph.themes</td><td colspan = "3">
ej.datavisualization.BulletGraph.Themes</td><td colspan = "2">
 </td></tr>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Event Name</b></td><td>
<b>Old Argument Name</b></td><td colspan = "3">
<b>New  Agrument Name</b></td><td colspan = "2">
<b>Comments</b></td></tr>
<tr>
<td rowspan = "7">
<b>Event</b></td><td>
drawTicks</td><td>
<b>args.Object</b></td><td colspan = "3">
<b>args.object</b></td><td colspan = "2">
Modified the args.Object</td></tr>
<tr>
<td>
drawLabels</td><td>
<b>args.Object</b></td><td colspan = "3">
<b>args.object</b></td><td colspan = "2">
Modified the args.Object</td></tr>
<tr>
<td>
drawCaption</td><td>
<b>args.Object</b></td><td colspan = "3">
<b>args.object</b></td><td colspan = "2">
Modified the args.Object</td></tr>
<tr>
<td>
drawQualitativeRanges</td><td>
<b>args.Object</b></td><td colspan = "3">
<b>args.object</b></td><td colspan = "2">
Modified the args.Object</td></tr>
<tr>
<td>
drawFeatureMeasureBar</td><td>
<b>args.Object</b><b>args.Value</b></td><td colspan = "3">
<b>args.object</b><b>args.value</b></td><td colspan = "2">
Modified the args.Object and args.Value</td></tr>
<tr>
<td>
drawCategory</td><td>
<b>args.Object</b><b>args.Value</b></td><td colspan = "3">
<b>args.object</b><b>args.value</b></td><td colspan = "2">
Modified the args.Object and args.Value</td></tr>
<tr>
<td>
drawComparativeMeasureSymbol</td><td>
<b>args.Object</b><b>args.Value</b></td><td colspan = "3">
<b>args.object</b><b>args.value</b></td><td colspan = "2">
Modified the args.Object and args.Value</td></tr>
</table>

<a name="ejbutton"></a>

### ejButton

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th colspan = "2">
Comments</th></tr>
<tr>
<td rowspan = "4">
 <b>Properties</b></td><td>
roundedCorner</td><td colspan = "2">
showRoundedCorner </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td colspan = "2">
enableRTL</td><td>
 </td></tr>
<tr>
<td>
type</td><td colspan = "2">
 </td><td>
Newly added</td></tr>
<tr>
<td></td><td colspan = "2">htmlAttributes
 </td><td>
Newly added</td></tr>
<tr>
<td rowspan = "4">
 <b>Enum</b></td><td>
 ej.contents = {<br/>
       &nbsp; &nbsp;textOnly:"textonly",<br/>
       &nbsp; &nbsp;imageOnly: "imageonly",<br/>
       &nbsp; &nbsp;imageBoth: "imageboth",<br/>
       &nbsp; &nbsp;textAndImage: "textandimage",<br/>
       &nbsp; &nbsp;imageTextImage:"imagetextimage"<br/>
       }; </td>
 <td colspan = "2">
 ej.ContentType = {<br/>
      &nbsp;&nbsp;TextOnly:"textonly",<br/>
      &nbsp;&nbsp;ImageOnly: "imageonly",<br/>
      &nbsp;&nbsp;ImageBoth: "imageboth",<br/>
      &nbsp;&nbsp;TextAndImage:"textandimage",<br/>
      &nbsp;&nbsp;ImageTextImage:"imagetextimage"<br/>
     }; </td>
     <td>
 </td></tr>
<tr>
<td>
 ej.imagePositions = {<br/>
      &nbsp;&nbsp;imageRight:"imageright",<br/>
      &nbsp;&nbsp;imageLeft: "imageleft"<br/>
    }; </td>
<td colspan = "2">
 ej.ImagePosition = { <br/>
      &nbsp;&nbsp;ImageRight:"imageright",<br/>
      &nbsp;&nbsp;ImageLeft: "imageleft"<br/>
    }; </td>
    <td>
 </td></tr>
<tr>
<td> ej.buttonSize ={<br/>
      &nbsp;&nbsp;normal : "normal",<br/>
      &nbsp;&nbsp;mini: "mini",<br/>
      &nbsp;&nbsp;small: "small",<br/>
      &nbsp;&nbsp;medium:"medium",<br/>
      &nbsp;&nbsp;large: "large"<br/>
    }; </td>
  <td colspan = "2">
 ej.ButtonSize = {<br/>
      &nbsp;&nbsp;Normal : "normal",<br/>
      &nbsp;&nbsp;Mini: "mini",<br/>
      &nbsp;&nbsp;Small:"small",<br/>
      &nbsp;&nbsp;Medium:"medium",<br/>
      &nbsp;&nbsp;Large: "large"<br/>
      }; </td><td>
 </td></tr>
 <tr>
<td> </td>
  <td colspan = "2">
 ej.ButtonType = {<br/>
      &nbsp;&nbsp;Button : "button",<br/>
      &nbsp;&nbsp;Reset: "reeset",<br/>
      &nbsp;&nbsp;Submit:"submit",<br/>
      }; </td><td> Newly added
 </td></tr>
</table>

<a name="ejchart"></a>
### ejChart

<table>
<tr>
<td>
<b>Member Type</b></td><td colspan = "5">
<b>Old API</b></td><td colspan = "3">
<b>New API</b></td><td colspan = "4">
<b>Comments</b></td></tr>
<tr>
<td rowspan = "14">
                <b>Property</b></td><td colspan = "5">
Localization</td><td colspan = "3">
locale</td><td colspan = "4">
 </td></tr>
<tr>
<td colspan = "5">
size.width:100</td><td colspan = "3">
size.width:”100”</td><td colspan = "2">
width type changed to<b>string</b> from number</td></tr>
<tr>
<td colspan = "5">
size.height:100</td><td colspan = "3">
size.height:”100”</td><td colspan = "2">
height type changed to<b>string</b> from number</td></tr>
<tr>
<td colspan = "5">
commonSeriesOptions.animation:</td><td colspan = "3">
commonSeriesOptions.enableAnimation:</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
commonSeriesOptions.tooltip.animation:</td><td colspan = "3">
commonSeriesOptions.tooltip.enableAnimation:</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
series.animation:</td><td colspan = "3">
series.enableAnimation:</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
series.tooltip.animation:</td><td colspan = "3">
series.tooltip.enableAnimation:</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
series.dataSource.data:JsonData,series.dataSource.xName:’’,series.dataSource.yName:’’ </td><td colspan = "3">
series.dataSource:JsonData,series.xName:’’,series.yName:’’</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
legend.location.X:10</td><td colspan = "3">
legend.location.x:10</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
legend.location.Y:10</td><td colspan = "3">
legend.location.y:10</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
legend.itemSize:</td><td colspan = "3">
legend.itemStyle:</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
axes.axisName:’’</td><td colspan = "3">
axes.name:’’</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
primaryXAxis.stripline:’’</td><td colspan = "3">
primaryXAxis.stripLine:’’</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
primaryXAxis.stripline.zOrder:’’</td><td colspan = "3">
primaryXAxis.stripLine.zIndex:’’</td><td colspan = "2">
 </td></tr>
<tr>
<td rowspan = "24">
                       <b>Enum</b></td><td colspan = "5">
ej.Chart.crosshairType</td><td colspan = "3">
ej.datavisualization.Chart.CrosshairType</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.valuetype</td><td colspan = "3">
ej.datavisualization.Chart.Valuetype</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.type</td><td colspan = "3">
ej.datavisualization.Chart.Type</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.labelPlacement</td><td colspan = "3">
ej.datavisualization.Chart.LabelPlacement</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.labelIntersectAction</td><td colspan = "3">
ej.datavisualization.Chart.LabelIntersectAction</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.edgeLabelPlacement</td><td colspan = "3">
ej.datavisualization.Chart.EdgeLabelPlacement</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.theme</td><td colspan = "3">
ej.datavisualization.Chart.Theme</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.fontWeight</td><td colspan = "3">
ej.datavisualization.Chart.FontWeight</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.orientation</td><td colspan = "3">
ej.datavisualization.Chart.Orientation</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.fontStyle</td><td colspan = "3">
ej.datavisualization.Chart.FontStyle</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.intervalType</td><td colspan = "3">
ej.datavisualization.Chart.IntervalType</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.rangePadding</td><td colspan = "3">
ej.datavisualization.Chart.RangePadding</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.textAlignment</td><td colspan = "3">
ej.datavisualization.Chart.TextAlignment</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.labelPosition</td><td colspan = "3">
ej.datavisualization.Chart.LabelPosition</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.zOrder</td><td colspan = "3">
ej.datavisualization.Chart.ZOrder</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.unit</td><td colspan = "3">
ej.datavisualization.Chart.Unit</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.pyramidMode</td><td colspan = "3">
ej.datavisualization.Chart.PyramidMode</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.drawType</td><td colspan = "3">
ej.datavisualization.Chart.DrawType</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.shape</td><td colspan = "3">
ej.datavisualization.Chart.Shape</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.drawMode</td><td colspan = "3">
ej.datavisualization.Chart.DrawMode</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.lineCap</td><td colspan = "3">
ej.datavisualization.Chart.LineCap</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.lineJoin</td><td colspan = "3">
ej.datavisualization.Chart.LineJoin</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.position</td><td colspan = "3">
ej.datavisualization.Chart.Position</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "5">
ej.Chart.alignment</td><td colspan = "3">
ej.datavisualization.Chart.Alignment</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "3">
<b>Member Type</b></td><td>
<b>Event Name</b></td><td>
<b>Old Argument Name</b></td><td colspan = "3">
<b>New Argument Name</b></td><td colspan = "3">
<b>Comments</b></td></tr>
<tr>
<td colspan = "3" rowspan = "22">
                     <b>Event</b></td><td>
load</td><td>
args:{cancel,Cancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype}  </td><td colspan = "3">
args.Cancel removed</td></tr>
<tr>
<td>
axesLabelRendering</td><td>
args:{cancel<b>Axis</b><b>Label</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype}</td><td colspan = "3">
args.data is added.args.Cancel removed.args.Axis , args.Label is removed.</td></tr>
<tr>
<td>
axesRangeCalculate</td><td>
args:{cancelCancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype} </td><td colspan = "3">
args.data is added.args.Cancel removed. </td></tr>
<tr>
<td>
axesTitleRendering</td><td>
args:{cancelCancel<b>Data={Axes, Location, Title}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={axes, location, title}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
chartAreaBoundsCalculate</td><td>
args:{cancelCancel<b>Data={AreaBound}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={areaBounds}</b>modeltype} </td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
legendItemRendering</td><td>
args:{cancelCancel<b>Data={Legend, LegendItem, Location, Style, SymbolShape}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={legend, legendItem, location, style, symbolShape}</b>modeltype}  </td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
legendBoundsCalculate</td><td>
args:{cancelCancel<b>Data={LegendBound }</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={legendBounds }</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
preRender</td><td>
args:{cancelCancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype}</td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
seriesRendering</td><td>
args:{cancelCancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype} </td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
symbolRendering</td><td>
args:{cancelCancel<b>Data={Location,</b><b>Style}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={location, style}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
titleRendering</td><td>
args:{cancelCancel<b>Data={Location,</b><b>Size, Title}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={Location, Size, Title}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
axesLabelsInitialize</td><td>
args:{cancelCancel<b>Data={Axes}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={axes}</b>modeltype} </td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
pointRegionClick</td><td>
args:{cancelCancel<b>Data={Region}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={region}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
pointRegionMouseMove</td><td>
args:{cancelCancel<b>Data={Region}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={region}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
legendItemClick</td><td>
args:{cancelCancel<b>Data={LegendItem, Series}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={legendItem, series}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
legendItemMouseMove</td><td>
args:{cancelCancel<b>Data={LegendItem, Series}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={legendItem, series}</b>modeltype}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
displayTextRendering</td><td>
args:{cancelCancel<b>Data={Location, PointIndex,  SeriesIndex, Text}</b>model }</td><td colspan = "3">
args:{cancel<b>data={location,pointIndex, seriesIndex, text}</b>model}</td><td colspan = "3">
Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
toolTipInitialize</td><td>
args:{cancelCancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype}</td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
trackAxisToolTip</td><td>
args:{cancelCancel<b>Data</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data</b>modeltype}</td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
trackToolTip</td><td>
args:{cancelCancel<b>Data</b>modeltype}</td><td colspan = "3">
args:{cancel<b>Data</b>modeltype}</td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
animationComplete</td><td>
args:{cancelCancel<b>Data={Series}</b>modeltype}</td><td colspan = "3">
args:{cancel<b>data={series}</b>modeltype} </td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
<tr>
<td>
loaded</td><td>
args:{cancelCancel<b>Data={Model}</b>modeltype} </td><td colspan = "3">
args:{cancel<b>data={model}</b>modeltype} </td><td colspan = "3">
 Modified the args.Dataargs.Cancel removed</td></tr>
</table>

<a name="ejcheckbox"></a>

### ejCheckbox

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "9">
 <b>Properties</b></td><td>
check</td><td>
checked</td><td>
 </td></tr>
<tr>
<td>
Indeterminate</td><td>
enableTriState</td><td>
 </td></tr>
<tr>
<td>
indeterminateState</td><td>
 </td><td>
We have removed this property.</td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence  </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL</td><td>
 </td></tr>
<tr>
<td></td><td>
htmlAttributes</td><td>Newly added
 </td></tr>
<tr>
<td>
</td><td>
validationMessage</td><td>Newly added
 </td></tr>
<tr>
<td></td><td>
validationRules</td><td>
 Newly added</td></tr>
<tr>
<td rowspan = "2">
 <b>Enum</b></td><td>
 ej.checkboxSize = {<br/>
       &nbsp;&nbsp;small: "small",<br/>
       &nbsp;&nbsp;medium: "medium"<br/>
       }; </td><td>
 ej.CheckboxSize = {<br/>
       &nbsp;&nbsp;Small: "small",<br/>
       &nbsp;&nbsp;Medium: "medium"<br/>
       }; </td><td>
 </td></tr>
<tr>
<td>
 ej.checkboxState = {<br/>
    &nbsp;&nbsp;check: "check",<br/>
    &nbsp;&nbsp;uncheck: "uncheck",<br/>
    &nbsp;&nbsp;indeterminate:"indeterminate"<br/>
    };</td><td>
 ej.CheckState = {<br/>
    &nbsp;&nbsp;Check: "check",<br/>
    &nbsp;&nbsp;UnCheck: "uncheck",<br/>
    &nbsp;&nbsp;Indeterminate:"indeterminate"<br/>
    };</td><td>
 </td></tr>
</table>

<a name="ejcirculargauge"></a>
### ejCircularGauge

<table>
<tr>
<th>
Member Type</th><th>
Old API</th><th>
New API</th><th>
Comments</th></tr>
<tr>
<td rowspan = "50">
<b>Property</b></td><td>
frameType</td><td rowspan = "4">
frame: { <br/>frameType: "fullCircle", <br/>backgroundImageUrl: null, halfCircleFrameStartAngle: 180, halfCircleFrameEndAngle: 360 },</td><td rowspan = "4">
All frame properties moved to Object type</td></tr>
<tr>
<td>
halfCircleFrameStartAngle</td></tr>
<tr>
<td>
halfCircleFrameEndAngle</td></tr>
<tr>
<td>
backgroundImageUrl</td></tr>
<tr>
<td>
canResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
animate</td><td>
enableAnimation</td><td>
 </td></tr>
<tr>
<td>
capBorderColor</td><td rowspan = "5">
pointerCap: { <br/>radius: 7, borderWidth: 3, <br/>interiorGradient: null, <br/>borderColor: null, <br/>backgroundColor: null }</td><td rowspan = "5">
All  pointer cap properties moved to Object type</td></tr>
<tr>
<td>
capBackgroundColor</td></tr>
<tr>
<td>
pointerCapRadius</td></tr>
<tr>
<td>
pointerCapBorderWidth</td></tr>
<tr>
<td>
capInteriorGradient</td></tr>
<tr>
<td>
borderColor</td><td rowspan = "2">
border:{   color: null,   width:3}</td><td rowspan = "2">
All border properties moved to Object type</td></tr>
<tr>
<td>
scaleBorderWidth</td></tr>
<tr>
<td>
scaleBarSize</td><td>
size</td><td>
 </td></tr>
<tr>
<td>
scaleRadius</td><td>
radius</td><td>
 </td></tr>
<tr>
<td>
scaleDirection</td><td>
direction</td><td>
 </td></tr>
<tr>
<td>
labelAutoAngle</td><td>
labels.autoAngle</td><td>
This property moved  under the label collection</td></tr>
<tr>
<td>
pointerLength</td><td>
length</td><td>
 </td></tr>
<tr>
<td>
pointerPosition</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
pointerWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
pointerGradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td>
pointerType</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
borderColor</td><td rowspan = "2">
border:{   color: null,   width:3}</td><td rowspan = "2">
All border properties moved to Object type</td></tr>
<tr>
<td>
borderWidth</td></tr>
<tr>
<td>
rangePosition</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
rangeGradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td>
borderColor</td><td rowspan = "2">
border:{   color: null,   width:3}</td><td rowspan = "2">
All border properties moved to Object type</td></tr>
<tr>
<td>
borderWidth</td></tr>
<tr>
<td>
tickColor</td><td>
color</td><td>
 </td></tr>
<tr>
<td>
tickStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
tickPosition</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
tickHeight</td><td>
height</td><td>
 </td></tr>
<tr>
<td>
tickWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
labelColor</td><td>
color</td><td>
 </td></tr>
<tr>
<td>
labelPosition</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
labelStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
scales.labelAutoAngle</td><td>
autoAngle</td><td>
 </td></tr>
<tr>
<td>
indicatorHeight</td><td>
height</td><td>
 </td></tr>
<tr>
<td>
indicatorWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
indicatorStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
indicatorValue</td><td>
value</td><td>
 </td></tr>
<tr>
<td>
indicatorLocation</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
subGaugeHeight</td><td>
height</td><td>
 </td></tr>
<tr>
<td>
subGaugeWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
location</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
labelColor</td><td>
color</td><td>
 </td></tr>
<tr>
<td>
labelValue</td><td>
value</td><td>
 </td></tr>
<tr>
<td>
location</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
customLabel</td><td>
customLabels</td><td>
 </td></tr>
<tr>
<td>
gradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td rowspan = "12">
<b>Enum</b></td><td>
ej.CircularGauge.<br/>direction = { <br/>Clockwise: "Clockwise", <br/>CounterClockwise: <br/>"CounterClockwise"    };</td><td>
ej.CircularGauge.<br/>Directions = { <br/>Clockwise: "clockwise", <br/>CounterClockwise: <br/>"counterclockwise" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>pointerPlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center" };</td><td>
ej.CircularGauge.<br/>PointerPlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>pointerType = { <br/>Needle: "Needle", <br/>Marker: "Marker" };</td><td>
ej.CircularGauge.<br/>PointerType = { <br/>Needle: "needle", <br/>Marker: "marker" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>needleType = { <br/>Triangle: "Triangle", <br/>Rectangle: "Rectangle", <br/>Trapezoid: "Trapezoid", <br/>Arrow: "Arrow" };</td><td>
ej.CircularGauge.<br/>NeedleType = { <br/>Triangle: "triangle", <br/>Rectangle: "rectangle", <br/>Trapezoid: "trapezoid", <br/>Arrow: "arrow" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>markerType = { <br/>Rectangle: "Rectangle", <br/>Triangle: "Triangle", <br/>Ellipse: "Ellipse", <br/>Diamond: "Diamond", <br/>Pentagon: "Pentagon", <br/>Circle: "Circle", <br/>Slider: "Slider", <br/>Pointer: "Pointer", <br/>Wedge: "Wedge", <br/>Trapezoid: "Trapezoid", <br/>RoundedRectangle: "RoundedRectangle" };</td><td>
ej.CircularGauge.<br/>MarkerType = { <br/>Rectangle: "rectangle", <br/>Triangle: "triangle", <br/>Ellipse: "ellipse", <br/>Diamond: "diamond", <br/>Pentagon: "pentagon", <br/>Circle: "circle", <br/>Slider: "slider", <br/>Pointer: "pointer", <br/>Wedge: "wedge", <br/>Trapezoid: "trapezoid", <br/>RoundedRectangle: <br/>"roundedrectangle" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>rangePlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center" };</td><td>
ej.CircularGauge.<br/>RangePlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>tickType = <br/>{ Major: "Major", <br/>Minor: "Minor" };</td><td>
ej.CircularGauge.<br/>TickType = <br/>{ Major: "major", <br/>Minor: "minor" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>tickPlacement = { <br/>Near: "Near", <br/>Far: "Far", <br/>Center: "Center" };</td><td>
ej.CircularGauge.<br/>TickPlacement = { <br/>Near: "near", <br/>Far: "far", <br/>Center: "center" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>labelPlacement = <br/>{ Near: "Near", <br/>Far: "Far", <br/>Center: "Center" };</td><td>
ej.CircularGauge.<br/>LabelPlacement = <br/>{ Near: "near", <br/>Far: "far", <br/>Center: "center" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>labelType = { <br/>Major: "Major", <br/>Minor: "Minor" };</td><td>
ej.CircularGauge.<br/>LabelType = { <br/>Major: "major", <br/>Minor: "minor" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>unitTextPlacement = { <br/>Back: "Back", <br/>Front: "Front" };</td><td>
ej.CircularGauge.<br/>UnitTextPlacement = { <br/>Back: "back", <br/>Front: "front" };</td><td>
 </td></tr>
<tr>
<td>
ej.CircularGauge.<br/>indicatorType = { <br/>Rectangle: "Rectangle", <br/>Circle: "Circle", RoundedRectangle: "RoundedRectangle", <br/>Text: "Text" };</td><td>
ej.CircularGauge.<br/>IndicatorType = { <br/>Rectangle: "rectangle", <br/>Circle: "circle", <br/>RoundedRectangle: <br/>"roundedrectangle", <br/>Text: "text" };</td><td>
 </td></tr>
<tr>
<td rowspan = "19">
Events arguments</td><td>
args.location</td><td>
args.position</td><td>
For Ticks</td></tr>
<tr>
<td>
args.tickAngle</td><td rowspan = "3">
args.tick{angleelement<br/>Index}</td><td rowspan = "3">
arguments moved to Object type</td></tr>
<tr>
<td>
args.tickElement</td></tr>
<tr>
<td>
args.tickIndex</td></tr>
<tr>
<td>
args.tickValue</td><td>
args.pointervalue</td><td>
 </td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
 </td></tr>
<tr>
<td>
args.labelAngle</td><td rowspan = "3">
args.label{angleelement<br/>Index}</td><td rowspan = "3">
arguments moved to Object type</td></tr>
<tr>
<td>
args.labelElement</td></tr>
<tr>
<td>
args.labelIndex</td></tr>
<tr>
<td>
args.labelValue</td><td>
args.pointerValue</td><td>
 </td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For labels</td></tr>
<tr>
<td>
args.pointerAngle</td><td rowspan = "3">
args.pointer{angleelement<br/>Index}</td><td rowspan = "3">
arguments moved to Object type</td></tr>
<tr>
<td>
args.pointerElement</td></tr>
<tr>
<td>
args.pointerIndex</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For range</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Customlabels</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For indicator</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For pointer cap</td></tr>
<tr>
<td>
args.pointerElement</td><td>
args.pointer{angleelement<br/>valueIndex}</td><td>
arguments moved to Object type</td></tr>
</table>

<a name="ejColorPicker"></a>

#### ejColorPicker

<table>
  <tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "2">
  <b>Properties</b></td><td></td><td>
buttonMode</td><td> Newly added
 </td></tr>
<tr>
<td></td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
  <td> <b> Enum </b> </td>
<td></td><td>
 ej.ColorPicker.ButtonMode = {<br/>
      &nbsp;&nbsp;Default:"dropdown",<br/>
      &nbsp;&nbsp;Split: "split"<br/>
    }; </td>
<td>  Newly added </td></tr>
</table>

<a name="ejdatepicker"></a>

### ejDatePicker

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "11">
  <b>Properties</b></td><td>
showDateIcon</td><td>
showPopupButton</td><td>
 </td></tr>
<tr>
<td>
waterMarkText</td><td>
watermarkText</td><td>
 </td></tr>
<tr>
<td>
localize</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
strictMode</td><td>
enableStrictMode</td><td>
 </td></tr>
<tr>
<td>
Persist</td><td>
enablePersistence  </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td></td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
showToolTip</td><td>
showTooltip</td><td>
 </td></tr>
<tr>
<td>
highlight</td><td>
highlightSection</td><td>
 </td></tr>
<tr>
<td>
highLightWeekend</td><td>
highlightWeekend</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>Enum</b></td> <td>
  ej.DatePicker.Header = {<br/>
        &nbsp;&nbsp;ShowHeaderNone:"ShowHeaderNone",<br/>
        &nbsp;&nbsp;ShowHeaderShort:"ShowHeaderShort",<br/>
        &nbsp;&nbsp;ShowHeaderMin: "ShowHeaderMin",<br/>
        &nbsp;&nbsp;ShowHeaderLong:"ShowHeaderLong"<br/>
        };</td> <td>
  ej.DatePicker.Header = { <br/>
        &nbsp;&nbsp;ShowHeaderNone:"showheadernone",<br/>
        &nbsp;&nbsp;ShowHeaderShort:"showheadershort",<br/>
        &nbsp;&nbsp;ShowHeaderMin: "showheadermin",<br/>
        &nbsp;&nbsp;ShowHeaderLong: "showheaderlong"<br/>
        }; </td> <td>
 </td></tr>
<tr><td>
 ej.DatePicker.highlightSection = {<br/>
    &nbsp;&nbsp;Month: "Month",<br/>
    &nbsp;&nbsp;Week: "Week",<br/>
    &nbsp;&nbsp;WorkDays: "WorkDays",<br/>
    &nbsp;&nbsp;None: "None"<br/>
    }; </td> <td>
 ej.DatePicker.HighlightSection = {<br/>
    &nbsp;&nbsp;Month: "month",<br/>
    &nbsp;&nbsp;Week: "week",<br/>
    &nbsp;&nbsp;WorkDays: "workdays",<br/>
    &nbsp;&nbsp;None: "none"<br/>
    }; </td> <td>
 </td></tr>
<tr><td>
 ej.DatePicker.Level = {<br/>
    &nbsp;&nbsp;Month: "Month",<br/>
    &nbsp;&nbsp;Year: "Year",<br/>
    &nbsp;&nbsp;Decade: "Decade",<br/>
    &nbsp;&nbsp;Century: "Century"<br/>
    }; </td> <td>
 ej.DatePicker.Level = {<br/>
    &nbsp;&nbsp;Month: "month",<br/>
    &nbsp;&nbsp;Year: "year",<br/>
    &nbsp;&nbsp;Decade: "decade",<br/>
    &nbsp;&nbsp;Century: "century"<br/>
    }; </td> <td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>EventName</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
Open</td><td>
args.previousDate</td><td>
args.prevDate</td><td>
 </td></tr>
<tr>
<td>
Close</td><td>
args.previousDate</td><td>
args.prevDate</td><td>
 </td></tr>
<tr>
<td>
Select</td><td>
args.previousDate</td><td>
args.prevDate</td><td>
 </td></tr>
<tr>
<td>
Change</td><td>
args.previousDate</td><td>
args.prevDate</td><td>
 </td></tr>
</table>

<a name="ejdatetimepicker"></a>

### ejDateTimePicker

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th colspan = "2">
New API Name</th><th colspan = "2">
Comments</th></tr>
<tr>
<td rowspan = "8">
  <b>Properties</b></td><td>
localize</td><td>
locale</td><td colspan = "2">
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner </td><td colspan = "2">
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td colspan = "2">
 </td></tr>
<tr>
<td></td><td>
htmlAttributes</td><td colspan = "2"> Newly added
 </td></tr>
<tr>
<td>
min</td><td>
minDateTime</td><td colspan = "2">
 </td></tr>
<tr>
<td>
max</td><td>
maxDateTime</td><td colspan = "2">
 </td></tr>
<tr>
<td>
showButton</td><td>
showPopupButton</td><td colspan = "2">
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence  </td><td colspan = "2">
 </td></tr>
<tr>
<td><b>
Method</b></td><td>
dateTimeNow</td><td>
setCurrentDateTime</td><td colspan = "2">
 </td></tr>
</table>

#### Event Arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th colspan = "2">
Comments</th></tr>
<tr>
<td rowspan = "2">
Open</td><td>
 </td><td>
args.value</td><td colspan = "2">
 </td></tr>
<tr>
<td>
 </td><td>
args.prevDateTime</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
Close</td><td>
 </td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.prevDateTime</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
Change</td><td>
 </td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.prevDateTime</td><td>
 </td></tr>
</table>

<a name="ejdiagram"></a>

### ejDiagram

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API</b></td><td>
<b>New API</b></td></tr>
<tr>
<td rowspan = "9">
<b>Property</b></td><td>
snapToObject</td><td>
enableSnapToObject</td></tr>
<tr>
<td>
autoScroll</td><td>
enableAutoScroll</td></tr>
<tr>
<td>
previewX</td><td rowspan = "2">
previewOffset</td></tr>
<tr>
<td>
previewY</td></tr>
<tr>
<td>
enableTooltip</td><td>
showTooltip</td></tr>
<tr>
<td>
exclude</td><td>
excludeFromLayout</td></tr>
<tr>
<td>
position</td><td>
horizontalAignment,verticalAlignment</td></tr>
<tr>
<td>
selectedPaletteIndex</td><td>
selectedPaletteName</td></tr>
<tr>
<td>
loadDefaults</td><td>
showCustomMenuItemsOnly</td></tr>
<tr>
<td rowspan = "10">
<b>Method</b></td><td>
nudgeUp</td><td rowspan = "4">
nudge(direction) </td></tr>
<tr>
<td>
nudgeDown</td></tr>
<tr>
<td>
nudgeLeft</td></tr>
<tr>
<td>
nudgeRight</td></tr>
<tr>
<td>
alignLeft</td><td rowspan = "6">
align(direction) </td></tr>
<tr>
<td>
alignRight</td></tr>
<tr>
<td>
alignTop</td></tr>
<tr>
<td>
alignBottom</td></tr>
<tr>
<td>
alignCenter</td></tr>
<tr>
<td>
alignMiddle</td></tr>
<tr>
<td rowspan = "14">
<b>Event</b></td><td>
onClick</td><td>
click</td></tr>
<tr>
<td>
onBeforeOpen</td><td>
beforeOpen</td></tr>
<tr>
<td>
nodeCollectionChanging</td><td rowspan = "2">
nodeCollectionChange</td></tr>
<tr>
<td>
nodeCollectionChanged</td></tr>
<tr>
<td>
connectorCollectionChanging</td><td rowspan = "2">
connectorCollectionChange</td></tr>
<tr>
<td>
connectorCollectionChanged</td></tr>
<tr>
<td>
selectionChanging</td><td rowspan = "2">
selectionChange</td></tr>
<tr>
<td>
selectionChanged</td></tr>
<tr>
<td>
textChanged</td><td>
textChange</td></tr>
<tr>
<td>
nodeSizedChanging</td><td rowspan = "2">
sizeChange</td></tr>
<tr>
<td>
nodeSizeChanged</td></tr>
<tr>
<td>
connectionChanging</td><td rowspan = "2">
connectionChange</td></tr>
<tr>
<td>
connectionChanged</td></tr>
<tr>
<td>
nodeRotationChanged </td><td>
rotationChange</td></tr>
</table>

<a name="ejdialog"></a>

### ejDialog

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "16">
 <b>Properties</b></td><td>
autoOpen</td><td>
showOnInit</td><td>
 </td></tr>
<tr>
<td>
closeText</td><td>
closeIconTooltip</td><td>
 </td></tr>
<tr>
<td>
Draggable</td><td>
allowDraggable</td><td>
 </td></tr>
<tr>
<td>
Modal</td><td>
enableModal</td><td>
 </td></tr>
<tr>
<td>
Resizable</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td></td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
Content</td><td>
contentType</td><td>
 </td></tr>
<tr>
<td>
loadUrl</td><td>
contentUrl</td><td>
 </td></tr>
<tr>
<td>
ajaxOptions</td><td>
ajaxSettings</td><td>
 </td></tr>
<tr>
<td>
Rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner </td><td>
 </td></tr>
<tr>
<td>
iconAction</td><td>
actionButtons</td><td>
 </td></tr>
<tr>
<td>
customIconCss</td><td>
faviconCSS</td><td>
 </td></tr>
<tr>
<td>
contentContainer</td><td>
content</td><td>
 </td></tr>
<tr>
<td>
Persist</td><td>
enablePersistence  </td><td>
 </td></tr>
<tr>
<td>
windowResizing</td><td>
enableAutoResize</td><td>
 </td></tr>
<tr>
<td>
<b>Event</b></td><td>
Load</td><td>
contentLoad</td><td>
 </td></tr>
</table>

<a name="ejdigitalgauge"></a>
### ejDigitalGauge

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "9">
<b>Property</b></td><td>
frameBackgroundImageUrl</td><td rowspan = "3">
frame: {     <br/>backgroundImageUrl: null,     <br/>outerWidth: 12,     <br/>innerWidth: 8 }</td><td rowspan = "3">
All properties moved to Object type</td></tr>
<tr>
<td>
frameOuterWidth</td></tr>
<tr>
<td>
frameInnerWidth</td></tr>
<tr>
<td>
segmentLength</td><td rowspan = "5">
segmentSettings: {      <br/>color: null,      <br/>length: 2,      <br/>opacity: 1,      <br/>spacing: 2,      <br/>width: 3    }</td><td rowspan = "5">
 </td></tr>
<tr>
<td>
segmentOpacity</td></tr>
<tr>
<td>
segmentSpacing</td></tr>
<tr>
<td>
segmentWidth</td></tr>
<tr>
<td>
segmentColor</td></tr>
<tr>
<td>
canResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
ej.characterType = { SevenSegment: "SevenSegment", FourteenSegment: "FourteenSegment", SixteenSegment: "SixteenSegment", EightCrossEightDotMatrix: "EightCrossEightDotMatrix", EightCrossEightSquareMatrix: "EightCrossEightSquareMatrix"  <br/>  };</td><td>
ej.CharacterType = { SevenSegment: "sevensegment", FourteenSegment: "fourteensegment", SixteenSegment: "sixteensegment", EightCrossEightDotMatrix: "eightcrosseightdotmatrix", EightCrossEightSquareMatrix: "eightcrosseightsquarematrix"  <br/>  };</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
ej.textAlignment = { <br/>Left: "Left", Right: "Right"    };</td><td>
ej.TextAlignment = { <br/>Left: "left", Right: "right"    };</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
ej.fontStyle = { Normal: "Normal", <br/>Bold: "Bold", Italic: "Italic", Underline: "Underline", Strikeout: "Strikeout"    };</td><td>
ej.FontStyle = { Normal: "normal", <br/>Bold: "bold", Italic: "italic", Underline: "underline", Strikeout: "strikeout"    };</td><td>
 </td></tr>
</table>

<a name="ejdropdownlist"></a>

### ejDropDownList

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "17">
 <b>Properties</b></td><td>
listSize</td><td>
ltemsCount</td><td>
 </td></tr>
<tr>
<td>
fields{spriteCss }</td><td>
spriteCssClass</td><td>
 </td></tr>
<tr>
<td>
Watermark</td><td>
watermarkText</td><td>
 </td></tr>
<tr>
<td>
popupPanelHeight</td><td>
popupHeight</td><td>
 </td></tr>
<tr>
<td>
popupPanelWidth</td><td>
popupWidth</td><td>
 </td></tr>
<tr>
<td>
targetId</td><td>
targetID</td><td>
 </td></tr>
<tr>
<td>
selectedItem</td><td>
selectedItemIndex</td><td>
 </td></tr>
<tr>
<td>
multiSelectedItemsIndex</td><td>
selectedItems</td><td>
 </td></tr>
<tr>
<td>
</td><td>
validationRules</td><td>Newly added
 </td></tr>
<tr>
<td>
</td><td>
validationMessage</td><td>Newly added
 </td></tr>
<tr>
<td>
selectedTo </td><td>
cascadeTo</td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
caseSensitive</td><td>
caseSensitiveSearch</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence   </td><td>
 </td></tr>
<tr>
<td>
incrementalSearch</td><td>
enableIncrementalSearch</td><td>
 </td></tr>
<tr>
<td>
multiSelectMode</td><td>
allowMultiSelection </td><td>
 </td></tr>
<tr>
<td rowspan = "7">
  <b>Methods</b></td><td>
getCheckedItems</td><td>
 </td><td>
We have removed this method .we can get the checked items through value property.</td></tr>
<tr>
<td>
getSelectedIndex</td><td>
 </td><td>
We have removed this method .we can get the checked items through<b>selectedItemIndex</b>property.</td></tr>
<tr>
<td>
popupListHide</td><td>
 hidePopup</td><td>
 </td></tr>
<tr>
<td>
popupListShow</td><td>
 showPopup</td><td>
 </td></tr>
<tr>
<td>
selectItemByIndex</td><td>
 </td><td>
We have removed this method .we can this scenario through<b>selectedItemIndex</b>property.</td></tr>
<tr>
<td>
selectItemByText</td><td>
 setSelectedText</td><td>
 </td></tr>
<tr>
<td>
selectItemByValue</td><td>
 setSelectedValue</td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td rowspan = "2">
popupHide</td><td>
 </td><td>
args.text</td><td>
New Event argument</td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
New Event argument</td></tr>
<tr>
<td rowspan = "2">
popupShown</td><td>
 </td><td>
args.text</td><td>
New Event argument</td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
New Event argument</td></tr>
<tr>
<td rowspan = "2">
beforePopupShown</td><td>
 </td><td>
args.text</td><td>
New Event argument</td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
New Event argument</td></tr>
</table>

<a name="ejgantt"></a>

### ejGantt

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "15">
<b>Property</b></td><td>
mileStoneMapping</td><td>
milestoneMapping</td><td>
 </td></tr>
<tr>
<td>
toolbar</td><td>
toolbarSettings</td><td>
 </td></tr>
<tr>
<td>
toolbar.allowToolbar</td><td>
toolbarSettings.showToolbar</td><td>
 </td></tr>
<tr>
<td>
scheduleHeader</td><td>
scheduleHeaderSettings</td><td>
 </td></tr>
<tr>
<td>
progressbarTooltipTemplateID</td><td>
progressbarTooltipTemplateId</td><td>
 </td></tr>
<tr>
<td>
taskbarEditingTooltipTemplateID</td><td>
taskbarEditingTooltipTemplateId</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
altRow</td><td>
enableAltRow</td><td>
 </td></tr>
<tr>
<td>
canResizeProgressBar</td><td>
enableProgressBarResizing</td><td>
 </td></tr>
<tr>
<td>
showTaskbarDragTooltip</td><td>
enableTaskbarDragTooltip</td><td>
 </td></tr>
<tr>
<td>
showTaskbarTooltip</td><td>
enableTaskbarTooltip</td><td>
 </td></tr>
<tr>
<td>
resourceCollection</td><td>
resources</td><td>
 </td></tr>
<tr>
<td>
edit</td><td>
editSettings</td><td>
 </td></tr>
<tr>
<td>
columns.columnEditType</td><td>
columns.editType</td><td>
 </td></tr>
<tr>
<td>
columns.columnTemplate</td><td>
columns.isTemplateColumn</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>Enum</b></td><td>
ej.Gantt.editingType</td><td>
ej.Gantt.EditingType</td><td>
 </td></tr>
<tr>
<td>
ej.Gantt.toolBarItems</td><td>
ej.Gantt.ToolbarItems</td><td>
 </td></tr>
<tr>
<td>
ej.Gantt.editMode</td><td>
ej.Gantt.EditMode</td><td>
 </td></tr>
</table>

<a name="ejgrid"></a>
### ejGrid

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "29">
<b>Property</b></td><td>
columnTemplate</td><td>
template</td><td>
 </td></tr>
<tr>
<td>
editingType</td><td>
editType</td><td>
 </td></tr>
<tr>
<td>
key</td><td>
isPrimaryKey</td><td>
 </td></tr>
<tr>
<td>
isUnBound</td><td>
isUnbound</td><td>
 </td></tr>
<tr>
<td>
editEvent</td><td>
allowEditOnDblClick</td><td>
API type changed from enum to boolean.</td></tr>
<tr>
<td>
showFilterBarMessage</td><td>
showFilterBarStatus</td><td>
This is applicable only for FilterBar type.</td></tr>
<tr>
<td>
statusBarWidth</td><td>
--</td><td>
Removed(The filter status will be showed in pager)</td></tr>
<tr>
<td>
selectedRow</td><td>
selectedRowIndex</td><td>
 </td></tr>
<tr>
<td>
rowHover</td><td>
enableRowHover</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence</td><td>
 </td></tr>
<tr>
<td>
headerEffect</td><td>
enableHeaderHover</td><td>
 </td></tr>
<tr>
<td>
autoSaveOnRowSelection</td><td>
enableAutoSaveOnSelectionChange</td><td>
 </td></tr>
<tr>
<td>
detailTemplate</td><td>
detailsTemplate</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL</td><td>
 </td></tr>
<tr>
<td>
altRow</td><td>
enableAltRow</td><td>
 </td></tr>
<tr>
<td>
toolbar</td><td>
toolbarSettings</td><td>
 </td></tr>
<tr>
<td>
edit</td><td>
editSettings</td><td>
 </td></tr>
<tr>
<td>
allowSummary</td><td>
showSummary</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
toggleGroup</td><td>
showToggleButton</td><td>
 </td></tr>
<tr>
<td>
showAnimateButton</td><td>
enableDropAreaAnimation</td><td>
 </td></tr>
<tr>
<td>
enableEffects</td><td>
enableDropAreaAutoSizing</td><td>
 </td></tr>
<tr>
<td>
groupedColumn</td><td>
groupedColumns</td><td>
 </td></tr>
<tr>
<td>
allowToolbar</td><td>
showToolbar</td><td>
 </td></tr>
<tr>
<td>
dialogEditorTemplateId</td><td>
dialogEditorTemplateID</td><td>
 </td></tr>
<tr>
<td>
externalFormTemplateId</td><td>
externalFormTemplateID</td><td>
 </td></tr>
<tr>
<td>
inlineFormTemplateId</td><td>
inlineFormTemplateID</td><td>
 </td></tr>
<tr>
<td>
templateId</td><td>
templateID</td><td>
 </td></tr>
<tr>
<td>
headerTemplateId</td><td>
headerTemplateID</td><td>
 </td></tr>
<tr>
<td rowspan = "25">
<b>Events</b></td><td>
drag</td><td>
columnDrag     -  args.column</td><td>
args.column    - Newly added</td></tr>
<tr>
<td>
dragStop</td><td>
columnDrop     -  args.column</td><td>
args.column    - Newly added</td></tr>
<tr>
<td>
dragStart</td><td>
columnDragStart-  args.column</td><td>
args.column    - Newly added</td></tr>
<tr>
<td>
toolBarClick</td><td>
toolbarClick</td><td>
 </td></tr>
<tr>
<td>
gridRightClick <br/>
	&nbsp;&nbsp;- &nbsp;	args.currentRowIndex<br/>
	&nbsp;&nbsp;- &nbsp;	args.currrentRow<br/>
	&nbsp;&nbsp;- &nbsp;	args.currentData<br/>
	&nbsp;&nbsp;- &nbsp;	args.currentCellIndex<br/>
	&nbsp;&nbsp;- &nbsp;	args.currentCellValue<br/>
	&nbsp;&nbsp;- &nbsp;	args.currentCell</td><td>
rightClick<br/>
	&nbsp;&nbsp;- args.rowIndex<br/>
	&nbsp;&nbsp;- args.row<br/>
	&nbsp;&nbsp;- args.data<br/>
	&nbsp;&nbsp;- args.cellIndex<br/>
	&nbsp;&nbsp;- args.cellValue<br/>
	&nbsp;&nbsp;- args.cell</td><td>
While right click on grid content</td></tr>
<tr>
<td>
detailCollapse</td><td>
detailsCollapse</td><td>
 </td></tr>
<tr>
<td>
detailData<br/>
&nbsp;- &nbsp; args.templateDetail</td><td>
detailsDataBound<br/>
&nbsp;-&nbsp; args.detailsElement<br/>
&nbsp;-&nbsp; args.data</td><td>
args.data(newly added)</td></tr>
<tr>
<td>
detailExpand</td><td>
detailsExpand</td><td>
 </td></tr>
<tr>
<td>
--</td><td>
endAdd</td><td>
Newly added</td></tr>
<tr>
<td>
--</td><td>
endDelete</td><td>
Newly added</td></tr>
<tr>
<td>
--</td><td>
endEdit</td><td>
Newly added</td></tr>
<tr>
<td>
beforeBulkAdd</td><td>
beforeBatchAdd</td><td>
 </td></tr>
<tr>
<td>
beforeBulkSave</td><td>
beforeBatchSave</td><td>
 </td></tr>
<tr>
<td>
beforeBulkDelete</td><td>
beforeBatchDelete</td><td>
 </td></tr>
<tr>
<td>
bulkAdd</td><td>
batchAdd</td><td>
 </td></tr>
<tr>
<td>
bulkDelete</td><td>
batchDelete</td><td>
 </td></tr>
<tr>
<td>
rowSelecting<br/>
&nbsp;&nbsp;- &nbsp;   args.currentRowIndex<br/>
&nbsp;&nbsp;- &nbsp;   args.currrentRow <br/>
&nbsp;&nbsp;- &nbsp;   args.currentData </td><td>
rowSelecting<br/>
&nbsp;&nbsp;- &nbsp;  args. rowIndex<br/>
&nbsp;&nbsp;- &nbsp;  args. row <br/>
&nbsp;&nbsp;- &nbsp;  args. data </td><td>
 </td></tr>
<tr>
<td>
rowSelected<br/>
&nbsp;&nbsp;- &nbsp; args.currentRowIndex<br/>
&nbsp;&nbsp;- &nbsp; args.currrentRow<br/>
&nbsp;&nbsp;- &nbsp; args.currentData </td><td>
rowSelected<br/>
&nbsp;&nbsp;- &nbsp; args. rowIndex<br/>
&nbsp;&nbsp;- &nbsp; args. rowIndex<br/>
&nbsp;&nbsp;- &nbsp; args. data </td><td>
 </td></tr>
<tr>
<td>
recordClick<br/>
&nbsp;&nbsp;- &nbsp; args.currentRowIndex<br/>
&nbsp;&nbsp;- &nbsp; args.currrentRow<br/>
&nbsp;&nbsp;- &nbsp; args.currentData </td><td>
recordClick<br/>
&nbsp;&nbsp;- &nbsp; args. rowIndex<br/>
&nbsp;&nbsp;- &nbsp; args. row<br/>
&nbsp;&nbsp;- &nbsp; args. data </td><td>
 </td></tr>
<tr>
<td>
recordDoubleClick<br/>
&nbsp;&nbsp;- &nbsp; args.currentRowIndex <br/>
&nbsp;&nbsp;- &nbsp; args.currrentRow<br/>
&nbsp;&nbsp;- &nbsp; args.currentData </td><td>
recordDoubleClick<br/>
&nbsp;&nbsp;- &nbsp; args. rowIndex<br/>
&nbsp;&nbsp;- &nbsp; args. row<br/>
&nbsp;&nbsp;-&nbsp; args. data </td><td>
 </td></tr>
<tr>
<td>
rowDataBound<br/>
&nbsp;&nbsp;- &nbsp; args. Element</td><td>
rowDataBound<br/>
&nbsp;&nbsp;- &nbsp; args.row</td><td>
 </td></tr>
<tr>
<td>
queryCellInfo<br/>
&nbsp;&nbsp;- &nbsp; args. Element <br/>
&nbsp;&nbsp;- &nbsp; args.Data <br/>
&nbsp;&nbsp;- &nbsp; args.Text</td><td>
queryCellInfo <br/>
&nbsp;&nbsp;- &nbsp; args. cell<br/>
&nbsp;&nbsp;- &nbsp; args.data <br/>
&nbsp;&nbsp;- &nbsp; args.text</td><td>
 </td></tr>
<tr>
<td>
actionBegin<br/>
&nbsp;&nbsp;- &nbsp; args.currentTr</td><td>
actionBegin<br/>
&nbsp;&nbsp;- &nbsp; args.row<br/>
&nbsp;&nbsp;- &nbsp; args.selectedRow</td><td>
args.selectedRow<br/><b>- </b>Newly Added(Passed During Save) </td></tr>
<tr>
<td>
actionComplete<br/>
&nbsp;&nbsp;- &nbsp; args.currentTr</td><td>
actionComplete<br/>
&nbsp;&nbsp;- &nbsp; args.row<br/>
&nbsp;&nbsp;- &nbsp; args.selectedRow</td><td>
args.selectedRow<br/><b>- </b>Newly Added(Passed During Save) </td></tr>
<tr>
<td>
beginEdit<br/>
&nbsp;&nbsp;- &nbsp; args.currentTr</td><td>
beginEdit<br/>
&nbsp;&nbsp;- &nbsp; args.row</td><td>
 </td></tr>
<tr>
<td rowspan = "23">
<b>Method</b></td><td>
cleanUpSelection</td><td>
clearSelection</td><td>
 </td></tr>
<tr>
<td>
refreshGridContent</td><td>
refreshContent</td><td>
 </td></tr>
<tr>
<td>
renderGrid</td><td>
render</td><td>
 </td></tr>
<tr>
<td>
sendAddRequest</td><td>
_startAdd</td><td>
Private Method</td></tr>
<tr>
<td>
sendDeleteRequest</td><td>
_deleteRow</td><td>
Private Method</td></tr>
<tr>
<td>
sendCancelRequest</td><td>
cancelEdit</td><td>
 </td></tr>
<tr>
<td>
sendEditingRequest</td><td>
startEdit</td><td>
 </td></tr>
<tr>
<td>
sendFilteringRequest</td><td>
filterColumn</td><td>
 </td></tr>
<tr>
<td>
sendGroupingRequest</td><td>
groupColumn</td><td>
 </td></tr>
<tr>
<td>
sendPagingRequest</td><td>
gotoPage</td><td>
 </td></tr>
<tr>
<td>
sendReorderingRequest</td><td>
reorderColumns</td><td>
 </td></tr>
<tr>
<td>
sendSaveRequest</td><td>
endEdit</td><td>
 </td></tr>
<tr>
<td>
sendSearchRequest</td><td>
search</td><td>
 </td></tr>
<tr>
<td>
sendSortingRequest</td><td>
sortColumn</td><td>
 </td></tr>
<tr>
<td>
sendUngroupingRequest</td><td>
ungroupColumn</td><td>
 </td></tr>
<tr>
<td>
templateRefresh</td><td>
refreshTemplate</td><td>
 </td></tr>
<tr>
<td>
refreshToolBar</td><td>
refreshToolbar</td><td>
 </td></tr>
<tr>
<td>
refreshGridContent<br/>
renderGrid<br/>
getGridContent<br/>
getGridContentTable<br/>
getGridFilterBar<br/>
getGridFooterContent<br/>
getGridFooterTable<br/>
getGridHeaderContent<br/>
getGridHeaderTable<br/>
getGridPager<br/>
getGridRowHeight<br/>
getGridRows</td><td>
refreshContent<br/>
render<br/>
getContent<br/>
getContentTable<br/>
getFilterBar<br/>
getFooterContent<br/>
getFooterTable<br/>
getHeaderContent<br/>
getHeaderTable<br/>
getPager<br/>
getRowHeight<br/>
getRows</td><td>
 </td></tr>
<tr>
<td>
bulkCancelbulkEditbulkSave</td><td>
batchCanceleditCellbatchSave</td><td>
  </td></tr>
<tr>
<td>
addRow</td><td>
addRecord</td><td>
 </td></tr>
<tr>
<td>
deleteRow</td><td>
deleteRecord</td><td>
 </td></tr>
<tr>
<td>
bulkAddRow</td><td>
_bulkAddRow</td><td>
Private method</td></tr>
<tr>
<td>
bulkDelete</td><td>
_bulkDelete</td><td>
Private method</td></tr>
<tr>
<td rowspan = "11">
<b>Enum</b></td><td>
ej.Grid.localization ["en-US"] = {<br/>
BulkSaveConifrm<br/>
BulkSaveLostChanges<br/>
frozenColumnsViewAlert<br/>
frozenColumnsScrollAlert<br/>
frozenNotSupportedException<br/>
}</td><td>
ej.Grid.locale["en-US"] = {<br/>
BatchSaveConfirm<br/>
BatchSaveLostChanges<br/>
FrozenColumnsViewAlert<br/>
FrozenColumnsScrollAlert<br/>
FrozenNotSupportedException<br/>
}</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.actions= {BulkSave: "bulksave"}</td><td>
ej.Grid.Actions= {BatchSave: "batchsave"}</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.summaryType</td><td>
ej.Grid.SummaryType</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.editMode</td><td>
ej.Grid.EditMode</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.formPosition</td><td>
ej.Grid.FormPosition</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.editingType</td><td>
ej.Grid.EditingType</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.unboundType</td><td>
ej.Grid.UnboundType</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.toolBarItems</td><td>
ej.Grid.ToolBarItems</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.filterType</td><td>
ej.Grid.FilterType</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.filterBarMode</td><td>
ej.Grid.FilterBarMode</td><td>
 </td></tr>
<tr>
<td>
ej.Grid.selectionType</td><td>
ej.Grid.SelectionType</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
ej.Grid.editEvent</td><td>
--</td><td>
Removed</td></tr>
</table>

<a name="ejlineargauge"></a>
### ejLinearGauge

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "44">
<b>Property</b></td><td>
frameBackgroundImageUrl</td><td rowspan = "3">
frame: { <br/>backgroundImageUrl: null, <br/>outerWidth: 12, <br/>innerWidth: 8 }</td><td rowspan = "3">
Properties moved to Object type</td></tr>
<tr>
<td>
frameOuterWidth</td></tr>
<tr>
<td>
frameInnerWidth</td></tr>
<tr>
<td>
canResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
animate</td><td>
enableAnimation</td><td>
 </td></tr>
<tr>
<td>
scaleBarSize</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
scaleDirection</td><td>
direction</td><td>
 </td></tr>
<tr>
<td>
scaleBarLength</td><td>
length</td><td>
 </td></tr>
<tr>
<td>
scaleStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
location</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
borderColor</td><td rowspan = "2">
border:{ color: null, width:3 }</td><td rowspan = "2">
Border properties moved to object type</td></tr>
<tr>
<td>
borderWidth</td></tr>
<tr>
<td>
tickColor</td><td>
color</td><td>
 </td></tr>
<tr>
<td>
tickStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
tickPlacement</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
tickHeight</td><td>
height</td><td>
 </td></tr>
<tr>
<td>
tickWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
xDistanceFromScale</td><td rowspan = "2">
distanceFromScale: { x: 50, y: 50 }</td><td rowspan = "2">
Property moved to Object type</td></tr>
<tr>
<td>
yDistanceFromScale</td></tr>
<tr>
<td>
rangePosition</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
rangeGradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td>
borderColor</td><td rowspan = "2">
border: { color: null, width:3 }</td><td rowspan = "2">
Property moved to object type</td></tr>
<tr>
<td>
borderWidth</td></tr>
<tr>
<td>
labelStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
labelPlacement</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
unitTextPosition</td><td>
unitTextPlacement</td><td>
 </td></tr>
<tr>
<td>
xDistanceFromScale</td><td rowspan = "2">
distanceFromScale: { x: 50, y: 50 }</td><td rowspan = "2">
Property moved to object type</td></tr>
<tr>
<td>
yDistanceFromScale</td></tr>
<tr>
<td>
pointerLength</td><td>
length</td><td>
 </td></tr>
<tr>
<td>
pointerPlacement</td><td>
placement</td><td>
 </td></tr>
<tr>
<td>
pointerGradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td>
pointerWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
markerStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
pointerWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
scaleBarGradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td>
indicatorHeight</td><td>
height</td><td>
 </td></tr>
<tr>
<td>
indicatorStyle</td><td>
type</td><td>
 </td></tr>
<tr>
<td>
indicatorWidth</td><td>
width</td><td>
 </td></tr>
<tr>
<td>
location</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
labelColor</td><td>
color</td><td>
 </td></tr>
<tr>
<td>
labelValue</td><td>
value</td><td>
 </td></tr>
<tr>
<td>
Location</td><td>
position</td><td>
 </td></tr>
<tr>
<td>
customLabel</td><td>
customLabels</td><td>
 </td></tr>
<tr>
<td>
gradient</td><td>
gradients</td><td>
 </td></tr>
<tr>
<td rowspan = "12">
<b>Enum</b></td><td>
ej.tickType = { <br/>MajorInterval: "MajorInterval", <br/>MinorInterval: "MinorInterval"    };</td><td>
ej.TickType = { <br/>MajorInterval: "majorinterval", <br/>MinorInterval: "minorinterval"    };</td><td>
 </td></tr>
<tr>
<td>
ej.labelType = { <br/>Major: "Major", <br/>Minor: "Minor"    };</td><td>
ej.LabelType = { <br/>Major: "major", <br/>Minor: "minor"    };</td><td>
 </td></tr>
<tr>
<td>
ej.fontType = { <br/>Bold: "Bold", Italic: "Italic", <br/>Regular: "Regular", <br/>Strikeout: "Strikeout", <br/>Underline: "Underline"    };</td><td>
ej.FontStyle = { <br/>Bold: "bold", Italic: "italic", <br/>Regular: "regular", <br/>Strikeout: "strikeout", <br/>Underline: "underline"    };</td><td>
 </td></tr>
<tr>
<td>
ej.pointerPlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center"    };</td><td>
ej.PointerPlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center"    };</td><td>
 </td></tr>
<tr>
<td>
ej.tickPlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center"    };</td><td>
ej.TickPlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center"};</td><td>
 </td></tr>
<tr>
<td>
ej.labelPlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center"    };</td><td>
ej.LabelPlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center"    };</td><td>
 </td></tr>
<tr>
<td>
ej.rangePlacement = { <br/>Near: "Near", Far: "Far", <br/>Center: "Center"    };</td><td>
ej.RangePlacement = { <br/>Near: "near", Far: "far", <br/>Center: "center"    };</td><td>
 </td></tr>
<tr>
<td>
ej.unitTextPlacement = { <br/>Front: "Front", Back: "Back"    };</td><td>
ej.UnitTextPlacement = { <br/>Front: "front", Back: "back"    };</td><td>
 </td></tr>
<tr>
<td>
ej.direction = { <br/>Clockwise: "Clockwise", <br/>CounterClockwise: <br/>"CounterClockwise"    };</td><td>
ej.Directions = { <br/>Clockwise: "clockwise", <br/>CounterClockwise: <br/>"counterclockwise"    };</td><td>
 </td></tr>
<tr>
<td>
ej.scaleType = { <br/>Rectangle: "Rectangle", <br/>RoundedRectangle: <br/>"RoundedRectangle", <br/>Thermometer: <br/>"Thermometer"    };</td><td>
ej.ScaleType = { <br/>Rectangle: "rectangle", <br/>RoundedRectangle: <br/>"roundedrectangle", <br/>Thermometer: <br/>"thermometer"    };</td><td>
 </td></tr>
<tr>
<td>
ej.indicatorType = { <br/>Rectangle: "Rectangle", <br/>Circle: "Circle", <br/>RoundedRectangle: <br/>"RoundedRectangle", <br/>Text: "Text"    };</td><td>
ej.IndicatorType = { <br/>Rectangle: "rectangle", <br/>Circle: "circle", <br/>RoundedRectangle: <br/>"roundedrectangle", <br/>Text: "text"    };</td><td>
 </td></tr>
<tr>
<td>
ej.markerType = { <br/>Rectangle: "Rectangle", <br/>Triangle: "Triangle", <br/>Ellipse: "Ellipse", <br/>Diamond: "Diamond", <br/>Pentagon: "Pentagon", <br/>Circle: "Circle", Star: "Star", <br/>Slider: "Slider", <br/>Pointer: "Pointer", <br/>Wedge: "Wedge", <br/>Trapezoid: "Trapezoid", <br/> RoundedRectangle: <br/>"RoundedRectangle"    };</td><td>
ej.MarkerType = { <br/>Rectangle: "rectangle", <br/>Triangle: "triangle", <br/>Ellipse: "ellipse", <br/>Diamond: "diamond", <br/>Pentagon: "pentagon", <br/>Circle: "circle", Star: "star", <br/>Slider: "slider", <br/>Pointer: "pointer", <br/>Wedge: "wedge", <br/>Trapezoid: "trapezoid", <br/>RoundedRectangle: <br/>"roundedrectangle"    };</td><td>
 </td></tr>
<tr>
<td rowspan = "20">
<b>Event Argument</b></td><td>
args.location</td><td>
args.position</td><td>
For ticks</td></tr>
<tr>
<td>
args.tickAngle</td><td rowspan = "4">
args.tick{angle,element,<br/>index,value}</td><td rowspan = "4">
arguments moved to Object type</td></tr>
<tr>
<td>
args.tickElement</td></tr>
<tr>
<td>
args.tickIndex</td></tr>
<tr>
<td>
args.tickValue</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For label</td></tr>
<tr>
<td>
args.labelAngle</td><td rowspan = "4">
args.tick{angle,element,<br/>index,value}</td><td rowspan = "4">
arguments moved to Object type</td></tr>
<tr>
<td>
args.labelElement</td></tr>
<tr>
<td>
args.labelIndex</td></tr>
<tr>
<td>
args.labelValue</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Bar pointer</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Marker pointer</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Custom Label</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Range</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Indicator</td></tr>
<tr>
<td>
args.location</td><td>
args.position</td><td>
For Render Complete</td></tr>
<tr>
<td>
args.pointerElement</td><td rowspan = "4">
args.pointer{angle<br/>elementIndexvalue}</td><td rowspan = "4">
arguments moved to Object type</td></tr>
<tr>
<td>
args.pointerIndex</td></tr>
<tr>
<td>
args.pointerValue</td></tr>
<tr>
<td>
args.pointerAngle</td></tr>
</table>

<a name="ejmaps"></a>
### ejMaps

<table>
<tr>
<td>
<b>Member Type</b></td><td colspan = "2">
<b>Old API Name</b></td><td colspan = "2">
<b>New API Name</b></td><td colspan = "2">
<b>Comments</b></td></tr>
<tr>
<td rowspan = "49">
<b>Property</b></td><td colspan = "2">
zoomOnSelection</td><td colspan = "2">
enableZoomOnSelection</td><td colspan = "2">
This API is moved under new API zoomSettings</td></tr>
<tr>
<td colspan = "2">
mapBackground</td><td colspan = "2">
background</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
Data</td><td colspan = "2">
shapeData</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
annotationTemplate</td><td colspan = "2">
markerTemplate</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
annotations</td><td colspan = "2">
markers</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
annotationDataSource</td><td colspan = "2">
N/A</td><td colspan = "2">
This API is removed since it is achieved in markers API.</td></tr>
<tr>
<td colspan = "2">
shapeFileLayer</td><td colspan = "2">
shapeLayer</td><td colspan = "2">
 </td></tr>

<tr>
<td colspan = "2">
bubbleSetting</td><td colspan = "2">
bubbleSettings</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
labelSetting</td><td colspan = "2">
labelSettings</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
legendSetting</td><td colspan = "2">
legendSettings</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
mapType</td><td colspan = "2">
layerType</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
shapeSetting</td><td colspan = "2">
shapeSettings</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
annotationLabel</td><td colspan = "2">
label</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
shapeSelectionStrokeWidth</td><td colspan = "2">
selectionStrokeWidth</td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeSelectionStroke</td><td colspan = "2">
selectionStroke</td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeSelectionColor</td><td colspan = "2">
selectionColor</td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeFill</td><td colspan = "2">
fill</td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeStroke</td><td colspan = "2">
stroke</td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeColorValuepath </td><td colspan = "2">
colorValuePath </td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeValuepath </td><td colspan = "2">
valuePath </td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeStrokeThickness </td><td colspan = "2">
strokeThickness </td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
shapeColorPalette </td><td colspan = "2">
colorPalette </td><td colspan = "2">
This API comes under shapeSettings</td></tr>
<tr>
<td colspan = "2">
bubbleColor </td><td colspan = "2">
color </td><td colspan = "2">
This API comes under bubbleSettings</td></tr>
<tr>
<td colspan = "2">
bubbleColorValuepath </td><td colspan = "2">
colorValuePath </td><td colspan = "2">
This API comes under bubbleSettings</td></tr>
<tr>
<td colspan = "2">
bubbleValuepath </td><td colspan = "2">
valuePath </td><td colspan = "2">
This API comes under bubbleSettings</td></tr>
<tr>
<td colspan = "2">
legendPositionX </td><td colspan = "2">
positionX </td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendWidth </td><td colspan = "2">
width </td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendHeight</td><td colspan = "2">
height</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendPositionY</td><td colspan = "2">
position</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendType</td><td colspan = "2">
type</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendTitle</td><td colspan = "2">
title</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendLeftLabel</td><td colspan = "2">
leftLabel</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendRightLabel</td><td colspan = "2">
rightLabel</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendMode</td><td colspan = "2">
mode</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
legendPosition</td><td colspan = "2">
position</td><td colspan = "2">
This API comes under legendSettings</td></tr>
<tr>
<td colspan = "2">
minZoom</td><td colspan = "2">
minValue</td><td colspan = "2">
This API is moved under new API zoomSettings</td></tr>
<tr>
<td colspan = "2">
maxZoom</td><td colspan = "2">
maxValue</td><td colspan = "2">
This API is moved under new API zoomSettings</td></tr>
<tr>
<td colspan = "2">
zoomLevel</td><td colspan = "2">
level</td><td colspan = "2">
This API is moved under new API zoomSettings</td></tr>
<tr>
<td colspan = "2">
zoomFactor</td><td colspan = "2">
factor</td><td colspan = "2">
This API is moved under new API zoomSettings</td></tr>
<tr>
<td colspan = "2">
showToolTip</td><td colspan = "2">
showTooltip</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
mouseHoverColor</td><td colspan = "2">
highlightColor</td><td colspan = "2">
This API comes  under API shapeSettings</td></tr>
<tr>
<td colspan = "2">
mouseHoverStroke</td><td colspan = "2">
highlightStroke</td><td colspan = "2">
This API comes under API shapeSettings</td></tr>
<tr>
<td colspan = "2">
mouseHoverWidth</td><td colspan = "2">
highlightBorderWidth</td><td colspan = "2">
This API comes under API shapeSettings</td></tr>
<tr>
<td colspan = "2">
subshapeFileLayers</td><td colspan = "2">
subLayers</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
minSize</td><td colspan = "2">
minValue</td><td colspan = "2">
This API comes under API bubbleSettings</td></tr>
<tr>
<td colspan = "2">
maxSize</td><td colspan = "2">
maxValue</td><td colspan = "2">
This API comes under API bubbleSettings</td></tr>
<tr>
<td colspan = "2">
canResize</td><td colspan = "2">
enableResize</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
shapeIdPath</td><td colspan = "2">
shapeDataPath</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
shapeIdTableField</td><td colspan = "2">
shapePropertyPath</td><td colspan = "2">
 </td></tr>
<td colspan = "2" rowspan = "4">
<b>Event</b></td><td colspan = "2">
shapeHovered</td><td colspan = "2">
mouseover</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
shapeUnHovered</td><td colspan = "2">
mouseleave</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
annotationSelected</td><td colspan = "2">
markerSelected</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
panning</td><td colspan = "2">
N/A</td><td colspan = "2">
This API is removed</td></tr>
<tr>
<tr>
<td colspan = "2">
<b>Enum</b></td><td colspan = "2">
LayerType = {        Geometry: "geometry",        OSM: "osm"    };</td><td colspan = "2">
LayerType = {Geometry: "geometry",        OSM: "osm",        Bing: "bing"    };</td><td colspan = "2">
 </td></tr>
</table>

<a name="ejmaskedit"></a>

### ejMaskEdit

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "6">
 <b>Properties</b></td><td>
customChar</td><td>
customCharacter </td><td>
 </td></tr>
<tr>
<td>
Error</td><td>
showError</td><td>
 </td></tr>
<tr>
<td>
Mask</td><td>
maskFormat</td><td>
 </td></tr>
<tr>
<td>
Persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner </td><td>
 </td></tr>
<tr>
<td>
waterMarkText</td><td>
watermarkText</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
 <b>Events</b></td><td>
mouseOut</td><td>
mouseout</td><td>
 </td></tr>
<tr>
<td>
mouseOver</td><td>
mouseover</td><td>
 </td></tr>
<tr>
<td>
onKeyDown</td><td>
keydown</td><td>
 </td></tr>
<tr>
<td>
KeyUp</td><td>
keyup</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td> <td>
 ej.inputMode = {<br/>
        &nbsp;&nbsp;Password: "password",<br/>
        &nbsp;&nbsp;Text: "text"<br/>
        };  </td> <td>
 ej.InputMode = {<br/>
        &nbsp;&nbsp;Password: "password",<br/>
        &nbsp;&nbsp;Text: "text"<br/>
        };  </td> <td>
 </td> </tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
change</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
focusIn</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
mouseout</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
mouseover</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
keydown</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
focusOut</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
keyPress</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
<tr>
<td>
keyup</td><td>
args.unStrippedValue</td><td>
args.unmaskedValue</td><td>
 </td></tr>
</table>

<a name="ejmenu"></a>

### ejMenu

<table>
<tr>
<th>
Member Type</th><th colspan = "2">
Old API Name</th><th colspan = "2">
New API Name</th><th colspan = "2">
Comments</th></tr>
<tr>
<td colspan = "2" rowspan = "7">
 <b>Properties</b></td><td colspan = "2">
animation</td><td colspan = "2">
animationType</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
centerAlign</td><td colspan = "2">
enableCenterAlign</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
contextTargetId</td><td colspan = "2">
contextMenuTargetID</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
menuTitle</td><td colspan = "2">
titleText</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
rtl</td><td colspan = "2">
enableRTL   </td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
showBottomLevelArrows</td><td colspan = "2">
showSubLevelArrows</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
showTopLevelArrows</td><td colspan = "2">
showRooltLevelArrows</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2" rowspan = "6">
 <b>Events</b></td><td colspan = "2">
beforeContextOpen</td><td colspan = "2">
beforeOpen</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
contextClose</td><td colspan = "2">
close</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
contextOpen</td><td colspan = "2">
open</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
keyDown</td><td colspan = "2">
keydown</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
mouseOut</td><td colspan = "2">
mouseout</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
mouseOver</td><td colspan = "2">
mouseover</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2" rowspan = "6">
 <b>Methods</b></td><td colspan = "2">
disableMenuItem</td><td colspan = "2">
 disableItem</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
disableMenuItembyID</td><td colspan = "2">
 disableItemByID</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
enableMenuItem</td><td colspan = "2">
 enableItem</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
enableMenuItembyID</td><td colspan = "2">
 enableItemByID</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
hideContextMenu</td><td colspan = "2">
 hide</td><td colspan = "2">
 </td></tr>
<tr>
<td colspan = "2">
showContextMenu</td><td colspan = "2">
 show</td><td colspan = "2">
 </td></tr>
<tr>
<td rowspan = "3">
<b>Enum</b></td><td colspan = "2" >
 ej.menuType = {<br/>
       &nbsp;&nbsp;NormalMenu:"NormalMenu",<br/>
       &nbsp;&nbsp;ContextMenu:"ContextMenu"<br/>
       }; </td>
       <td>
 ej.MenuType = {<br/>
           &nbsp;&nbsp;NormalMenu:"normalmenu",<br/>
           &nbsp;&nbsp;ContextMenu:"contextmenu"<br/>
           }; </td>
           <td>
 </td></tr>
 <tr>
<td colspan = "2">
 ej.direction = {<br/>
       &nbsp;&nbsp;Left: "Left",<br/>
       &nbsp;&nbsp;Right: "Right"<br/>
    }; </td> <td>
 ej.Direction = {<br/>
    &nbsp;&nbsp;Left: "left",<br/>
    &nbsp;&nbsp;Right: "right"<br/>
    }; </td> <td>
 </td></tr>
<tr>
<td colspan = "2">
 ej.animationType = {<br/>
    &nbsp;&nbsp;None: "none",<br/>
    &nbsp;&nbsp;Default: "default"<br/>
    }; </td> <td >
 ej.AnimationType = {<br/>
    &nbsp;&nbsp;None: "none",<br/>
    &nbsp;&nbsp;Default: "default"<br/>
    }; </td> <td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<td>
<b>Event Name</b></td><td>
<b>Old Event Args</b></td><td>
<b>New Event Args</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "3">
<b>click</b></td><td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.events.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>keydown</b></td><td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.events.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>mouseout</b></td><td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.events.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>mouseover</b></td><td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.events.menuText</td><td>
args.events.text</td><td>
 </td></tr>
</table>

<a name="ejolapchart"></a>
### ejOlapChart

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td colspan = "2">
<b>New API Name</b></td><td colspan = "2">
<b>Comments</b></td></tr>
<tr>
<td rowspan = "2">
<b>Property</b></td><td>
localization</td><td>
locale</td><td colspan = "2">
 </td></tr>
<tr>
<td>
serviceMethods</td><td>
serviceMethodSettings</td><td colspan = "2">
 </td></tr>
</table>

<a name="ejolapclient"></a>
### ejOlapClient

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "7">
<b>Property</b></td><td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
controlPlacement</td><td>
displaySettings -> controlPlacement</td><td>
 </td></tr>
<tr>
<td>
defaultView</td><td>
displaySettings -> defaultView</td><td>
 </td></tr>
<tr>
<td>
fullScreenView</td><td>
displaySettings -> enableFullScreen</td><td>
 </td></tr>
<tr>
<td>
mode</td><td>
displaySettings -> mode</td><td>
 </td></tr>
<tr>
<td>
serviceMethods</td><td>
serviceMethodSettings</td><td>
 </td></tr>
<tr>
<td>
togglePanel</td><td>
displaySettings -> enableTogglePanel</td><td>
 </td></tr>
<tr>
<td rowspan = "7">
<b>Method</b></td><td>
ChartDrillSuccess</td><td>
chartDrillSuccess</td><td>
 </td></tr>
<tr>
<td>
CubeChanged</td><td>
cubeChanged</td><td>
 </td></tr>
<tr>
<td>
GetAxisPosition</td><td>
getAxisPosition</td><td>
 </td></tr>
<tr>
<td>
GridDrillSuccess</td><td>
gridDrillSuccess</td><td>
 </td></tr>
<tr>
<td>
NodeDropped</td><td>
nodeDropped</td><td>
 </td></tr>
<tr>
<td>
OnTabClick</td><td>
onTabClick</td><td>
 </td></tr>
<tr>
<td>
ReportChanged</td><td>
reportChanged</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
<b>Event</b></td><td>
chartPreRender</td><td>
chartLoad</td><td>
 </td></tr>
<tr>
<td>
clientComplete</td><td>
renderComplete</td><td>
 </td></tr>
<tr>
<td>
clientError</td><td>
renderFailure</td><td>
 </td></tr>
<tr>
<td>
clientSuccess</td><td>
renderSuccess</td><td>
 </td></tr>
</table>

<a name="ejolapgauge"></a>
### ejOlapGauge

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "4">
<b>Property</b></td><td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
serviceMethods</td><td>
serviceMethodSettings</td><td>
 </td></tr>
<tr>
<td>
showHeaderLabels</td><td>
showHeaderLabel</td><td>
 </td></tr>
<tr>
<td>
showTooltip</td><td>
enableTooltip</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>Event</b></td><td>
clientComplete</td><td>
renderComplete</td><td>
 </td></tr>
<tr>
<td>
clientError</td><td>
renderFailure</td><td>
 </td></tr>
<tr>
<td>
clientSuccess</td><td>
renderSuccess</td><td>
 </td></tr>
</table>

<a name="ejpivotgrid"></a>
### ejPivotGrid

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "7">
<b>Property</b></td><td>
enableColumnHeaderHyperlink</td><td>
hyperlinkSettings -> enableColumnHeaderHyperlink</td><td>
 </td></tr>
<tr>
<td>
enableRowHeaderHyperlink</td><td>
hyperlinkSettings -> enableRowHeaderHyperlink</td><td>
 </td></tr>
<tr>
<td>
enableSummaryCellHyperlink</td><td>
hyperlinkSettings  -> enableSummaryCellHyperlink</td><td>
 </td></tr>
<tr>
<td>
enableValueCellHyperlink</td><td>
hyperlinkSettings  -> enableValueCellHyperlink</td><td>
 </td></tr>
<tr>
<td>
gridLayout</td><td>
layout</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
serviceMethods</td><td>
serviceMethodSettings</td><td>
 </td></tr>
<tr>
<td>
<b>Method</b></td><td>
doFullPost</td><td>
doPostBack</td><td>
 </td></tr>
<tr>
<td>
<b>Event</b></td><td>
cellContextEvent</td><td>
cellContext</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
GridLayout</td><td>
Layout</td><td>
 </td></tr>
</table>

<a name="ejpivotpager"></a>
### ejPivotPager

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "3">
<b>Property</b></td><td>
categPageCount</td><td>
categoricalPageCount</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
pagerMode</td><td>
mode</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
PagerMode</td><td>
Mode</td><td>
 </td></tr>
</table>

<a name="ejprogressbar"></a>

### ejProgressbar

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "4">
 <b>Properties</b></td><td>
max</td><td>
maxValue</td><td>
 </td></tr>
<tr>
<td>
min</td><td>
minValue</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence     </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
<b>Method</b></td><td>
getPercent</td><td>
getPercentage</td><td>
 </td></tr>
</table>

<a name="ejradiobutton"></a>

### ejRadioButton

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "3">
 <b>Properties</b></td><td>
check</td><td>
checked</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
 ej.radiobuttonSize = {<br/>
       &nbsp;&nbsp;small: "small",<br/>
       &nbsp;&nbsp;medium:"medium"<br/>
       }; </td> <td>
 ej.RadioButtonSize = {<br/>
       &nbsp;&nbsp;Small: "small",<br/>
       &nbsp;&nbsp;Medium:"medium"<br/>
       }; </td><td>
 </td></tr>
</table>

<a name="ejrangenavigator"></a>
### ejRangeNavigator

<table>
<tr>
<td>
<b>Member Type</b></td><td colspan = "2">
<b>Old API</b></td><td>
<b>New API</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "20">
<b>Property</b></td><td colspan = "2">
canResize</td><td>
enableAutoResizing</td><td>
 </td></tr>
<tr>
<td colspan = "2">
isRTL</td><td>
enableRTL</td><td>
 </td></tr>
<tr>
<td colspan = "2">
navigatorStyle</td><td>
navigatorStyleSettings</td><td>
 </td></tr>
<tr>
<td colspan = "2">
navigatorStyle.border.strokedasharray</td><td>
navigatorStyleSettings.border.dashArray</td><td>
 </td></tr>
<tr>
<td colspan = "2">
labelSettings.higherLevel.gridLineStyle.strokedasharray</td><td>
labelSettings.higherLevel.gridLineStyle.dashArray</td><td>
 </td></tr>
<tr>
<td colspan = "2">
labelSettings.lowerLevel.gridLineStyle.strokedasharray</td><td>
labelSettings.lowerLevel.gridLineStyle.dashArray</td><td>
 </td></tr>
<tr>
<td colspan = "2">
snappingMode </td><td>
allowSnapping</td><td>
 </td></tr>
<tr>
<td colspan = "2">
deferredUpdate</td><td>
enableDeferredUpdate</td><td>
 </td></tr>
<tr>
<td colspan = "2">
tooltipSettings.labelstyles.font</td><td>
tooltipSettings.font</td><td>
<b>labelstyles</b> in tooltipSettings is removed and <b>font </b>property is moved directly undertoolSettings</td></tr>
<tr>
<td colspan = "2">
labelSettings.labelstyles</td><td>
labelSettings.style</td><td>
 </td></tr>
<tr>
<td colspan = "2">
labelSettings.higherLevel.labelstyles</td><td>
labelSettings.higherLevel.style</td><td>
 </td></tr>
<tr>
<td colspan = "2">
labelSettings.lowerLevel .labelstyles</td><td>
labelSettings.lowerLevel.style</td><td>
 </td></tr>
<tr>
<td colspan = "2">
font.fontFamily                    font.fontStyle                   font.fontWeight </td><td>
font.familyfont.stylefont.weight</td><td>
 </td></tr>
<tr>
<td colspan = "2">
Range</td><td>
rangeSettings</td><td>
 </td></tr>
<tr>
<td colspan = "2">
selectedRange</td><td>
selectedRangeSettings</td><td>
 </td></tr>
<tr>
<td colspan = "2">
Size</td><td>
sizeSettings</td><td>
 </td></tr>
<tr>
<td colspan = "2">
tooltip</td><td>
tooltipSettings</td><td>
 </td></tr>
<tr>
<td colspan = "2">
zoomCordinates</td><td>
zoomFactorzoomPositon</td><td>
 </td></tr>
<tr>
<td colspan = "2">
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td colspan = "2">
dataSource.data:”chartdata”,dataSource.xName:”xValue”,dataSource.yName:”yValue”</td><td>
dataSource:”chartdata”, xName:”xValue”,yName:”yValue”</td><td>
Removed dataSourceand movedthe properties under dataSource directly to the rangenavigatormodel, whereas the data property is renamed as <b>dataSource</b></td></tr>
<tr>
<td>
<b>Member Type</b></td><td colspan = "2">
<b>Old Method Name</b></td><td>
<b>New Method Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td>
<b>Method</b></td><td colspan = "2">
rendernavigator</td><td>
renderNavigator</td><td>
 </td></tr>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Event Name</b></td><td>
<b>Old Argument Name</b></td><td>
<b>New Argument Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "2">
Event</td><td>
loaded</td><td>
args:{cancelCancel<b>Data={Model}</b>modeltype} </td><td>
args:{cancelCancel<b>data={model}</b>modeltype} </td><td>
 Modified args.DataRemoved args.Cancel</td></tr>
<tr>
<td>
load</td><td>
args:{cancelCancel<b>Data={Model}</b>modeltype}</td><td>
args:{cancelCancel<b>data={model}</b>modeltype}</td><td>
Modified args.DataRemoved args.Cancel</td></tr>
</table>

<a name="ejrating"></a>

### ejRating

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "3">
<b>Properties</b></td><td>
currentValue</td><td>
value</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td> </td><td>
htmlAttributes</td><td>Newly added
 </td></tr>
<tr>
<td rowspan = "3">
<b>Events</b></td><td>
mouseOut</td><td>
mouseout</td><td>
 </td></tr>
<tr>
<td>
mouseOver</td><td>
mouseover</td><td>
 </td></tr>
<tr>
<td>
valueChanged</td><td>
Change</td><td>
 </td></tr>
<tr>
<td rowspan = "6">
 <b>Methods</b></td><td>
getCurrentValue</td><td>
 getValue</td><td>
 </td></tr>
<tr>
<td>
hideResetButton</td><td>
 </td><td>
We have removed this method. use <b>allowReset  property </b>to achieve this behaviour</td></tr>
<tr>
<td>
setCurrentValue</td><td>
 setValue</td><td>
 </td></tr>
<tr>
<td>
showResetButton</td><td>
 </td><td>
We have removed this method. use <b>allowReset  property </b>to achieve this behaviour</td></tr>
<tr>
<td>
showRating</td><td>
 </td><td>
We have removed this method. use <b>show method </b> to achieve this behaviour</td></tr>
<tr>
<td>
hideRating</td><td>
 </td><td>
We have removed this method. use <b>hide method </b> to achieve this behaviour</td></tr>
<tr>
<td rowspan = "2">
<b>Enum</b></td><td>
 ej.Rating.Orientation = {<br/>
       &nbsp;&nbsp;Horizontal:"Horizontal",<br/>
       &nbsp;&nbsp;Vertical: "vertical"<br/>
       }; </td> <td>
 ej.Rating.Orientation = {<br/>
       &nbsp;&nbsp;Horizontal:"horizontal",<br/>
       &nbsp;&nbsp;Vertical: "vertical"<br/>
       };</td> <td>
 </td></tr>
<tr><td>
ej.Rating.precisions = {<br/>
    &nbsp;&nbsp;Full: "full",<br/>
    &nbsp;&nbsp;Half: "half",<br/>
    &nbsp;&nbsp;Exact: "exact"<br/>
    };</td><td>
ej.Rating.Precision = {<br/>
    &nbsp;&nbsp;Full: "full",<br/>
    &nbsp;&nbsp;Half: "half",<br/>
    &nbsp;&nbsp;Exact: "exact"<br/>
    };</td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
<b>click</b></td><td>
args.Value</td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
<b>mouseover</b></td><td>
args.Value</td><td>
args.value</td><td>
 </td></tr>
</table>

<a name="ejrichtexteditor"></a>

### ejRichTextEditor

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "8">
<b>Properties</b></td><td>
allowEdit</td><td>
allowEditing</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
resizable</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td> </td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
showToolBar</td><td>
showToolbar</td><td>
 </td></tr>
<tr>
<td>
toolsList :{ custom }</td><td>
customTool</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
<b>Methods</b></td><td>
getHtmlString</td><td>
getHtml</td><td>
 </td></tr>
<tr>
<td>
setHtmlString</td><td>
setHtml</td><td>
 </td></tr>
<tr>
<td>
commandStatus</td><td>
getCommandStatus</td><td>
 </td></tr>
<tr>
<td>
selectedHtml</td><td>
getSelectedHtml</td><td>
 </td></tr>
</table>

<a name="ejrotator"></a>

### ejRotator

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "14">
 <b>Properties</b></td><td>
allowResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
animation</td><td>
animationType</td><td>
 </td></tr>
<tr>
<td>
autoPlay</td><td>
enableAutoPlay</td><td>
 </td></tr>
<tr>
<td>
caption</td><td>
showCaption</td><td>
 </td></tr>
<tr>
<td>
enablePlaybtn</td><td>
showPlayButton</td><td>
 </td></tr>
<tr>
<td>
</td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
itemDisplay</td><td>
displayItemsCount </td><td>
 </td></tr>
<tr>
<td>
itemMove</td><td>
navigateSteps</td><td>
 </td></tr>
<tr>
<td>
pager</td><td>
showPager</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
slideButton</td><td>
showNavigateButton</td><td>
 </td></tr>
<tr>
<td>
speed</td><td>
animationSpeed</td><td>
 </td></tr>
<tr>
<td>
thumbSource</td><td>
thumbnailSourceID</td><td>
 </td></tr>
<tr>
<td>
thumbItem</td><td>
showThumbnail</td><td>
 </td></tr>
<tr>
<td>
<b>Event</b></td><td>
thumbClick</td><td>
thumbItemClick</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
<b>Methods</b></td><td>
previousSlide</td><td>
 slidePrevious</td><td>
 </td></tr>
<tr>
<td>
nextSlide</td><td>
 slideNext</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
 ej.Rotator.pagerPosition = {<br/>
       &nbsp;&nbsp;TopLeft: "topleft",<br/>
       &nbsp;&nbsp;TopRight: "topright",<br/>
       &nbsp;&nbsp;BottomLeft: "bottomleft",<br/>
       &nbsp;&nbsp;BottomRight: "bottomright",<br/>
       &nbsp;&nbsp;TopCenter: "topCenter",<br/>
       &nbsp;&nbsp;Outside: "outside"<br/>
       }; </td> <td>
 ej.Rotator.PagerPosition = {<br/>
       &nbsp;&nbsp;TopLeft: "topleft",<br/>
       &nbsp;&nbsp;TopRight: "topright",<br/>
       &nbsp;&nbsp;BottomLeft: "bottomleft",<br/>
       &nbsp;&nbsp;BottomRight: "bottomright",<br/>
       &nbsp;&nbsp;TopCenter: "topCenter",<br/>
       &nbsp;&nbsp;Outside: "outside"<br/>
       }; </td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td rowspan = "2">
change</td><td>
args.id</td><td>
args.itemID</td><td>
 </td></tr>
<tr>
<td>
args.index</td><td>
args.activeItemIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
pagerClick</td><td>
args.id</td><td>
args.itemID</td><td>
 </td></tr>
<tr>
<td>
args.index</td><td>
args.activeItemIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
start</td><td>
args.id</td><td>
args.itemID</td><td>
 </td></tr>
<tr>
<td>
args.index</td><td>
args.activeItemIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
stop</td><td>
args.id</td><td>
args.itemID</td><td>
 </td></tr>
<tr>
<td>
args.index</td><td>
args.activeItemIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
thumbItemClick</td><td>
args.id</td><td>
args.itemID</td><td>
 </td></tr>
<tr>
<td>
args.index</td><td>
args.activeItemIndex</td><td>
 </td></tr>
</table>

<a name="ejschedule"></a>
### ejSchedule

<table>
<tr>
<th>
Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "13">
<b>Property</b></td><td>
canResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL</td><td>
 </td></tr>
<tr>
<td>
localization</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
allowResizing</td><td>
enableAppointmentResize</td><td>
 </td></tr>
<tr>
<td>
fields</td><td>
appointmentSettings</td><td>
 </td></tr>
<tr>
<td>
idField</td><td>
id</td><td>
 </td></tr>
<tr>
<td>
subjectField</td><td>
subject</td><td>
 </td></tr>
<tr>
<td>
descriptionField</td><td>
description</td><td>
 </td></tr>
<tr>
<td>
startTimeField</td><td>
startTime</td><td>
 </td></tr>
<tr>
<td>
endTimeField</td><td>
endTime</td><td>
 </td></tr>
<tr>
<td>
recurrenceField</td><td>
recurrence</td><td>
 </td></tr>
<tr>
<td>
recurrenceRuleField</td><td>
recurrenceRule</td><td>
 </td></tr>
<tr>
<td>
alldayField</td><td>
allDay</td><td>
 </td></tr>
<tr>
<td>
<b>Events</b></td><td>
args.appObj  & args.data </td><td>
args.appointment</td><td>
In <b>appointmentSaved</b> event we have changed the arguments name.</td></tr>
<tr>
<td>
<b>Events</b></td><td>
args.newViewargs.oldViewargs.newDate</td><td>
args.currentViewargs.prevViewargs.currentDate</td><td>
In <b>navigation</b> event we have changed the arguments name.</td></tr>
<tr>
<td>
<b>Enum</b></td><td>
ej.Schedule.actions</td><td>
ej.Schedule.Actions</td><td>
 </td></tr>
</table>

<a name="ejscroller"></a>

### ejScroller

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "3">
<b>Properties</b></td><td>
oneStep</td><td>
scrollOneStepBy</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL</td><td>
 </td></tr>
</table>

<a name="ejslider"></a>

### ejSlider

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "7">
<b>Properties</b></td><td>
animate</td><td>
enableAnimation</td><td>
 </td></tr>
<tr>
<td>
endValue</td><td>
maxValue</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
startValue</td><td>
minValue</td><td>
 </td></tr>
<tr>
<td>
step</td><td>
incrementStep</td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
 ej.sliderType = {<br/>
       &nbsp;&nbsp;Default: "default",<br/>
       &nbsp;&nbsp;MinRange: "minrange",<br/>
       &nbsp;&nbsp;Range: "range"<br/>
       }; </td> <td>
 ej.SliderType = {<br/>
       &nbsp;&nbsp;Default: "default",<br/>
       &nbsp;&nbsp;MinRange: "minrange",<br/>
       &nbsp;&nbsp;Range: "range"<br/>
       }; </td><td></td>
         </tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
change</td><td>
args.handleNo</td><td>
args.sliderIndex</td><td>
 </td></tr>
<tr>
<td>
start</td><td>
args.handleNo</td><td>
args.sliderIndex</td><td>
 </td></tr>
<tr>
<td>
slide</td><td>
args.handleNo</td><td>
args.sliderIndex</td><td>
 </td></tr>
<tr>
<td>
stop</td><td>
args.handleNo</td><td>
args.sliderIndex</td><td>
 </td></tr>
</table>

<a name="ejsplitbutton"></a>

### ejSplitButton

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "3">
<b>Properties</b></td><td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
targetId</td><td>
targetID</td><td>
 </td></tr>
<tr>
<td rowspan = "3">
<b>Enum</b></td><td>
 ej.contents = {<br/>
      &nbsp;&nbsp;textOnly:"textonly",<br/>
      &nbsp;&nbsp;imageOnly:"imageonly",<br/>
      &nbsp;&nbsp;imageBoth: "imageboth",<br/>
      &nbsp;&nbsp;textAndImage: "textandimage",<br/>
      &nbsp;&nbsp;imageTextImage: "imagetextimage"<br/>
      }; </td> <td>
 ej.Contents = {<br/>
      &nbsp;&nbsp;TextOnly:"textonly",<br/>
      &nbsp;&nbsp;ImageOnly: "imageonly",<br/>
      &nbsp;&nbsp;ImageBoth: "imageboth",<br/>
      &nbsp;&nbsp;TextAndImage:"textandimage",<br/>
      &nbsp;&nbsp;ImageTextImage:"imagetextimage"<br/>
      }; </td><td>
 </td></tr>
<tr>
<td>
 ej.imagePositions = {<br/>
    &nbsp;&nbsp;imageRight: "imageright",<br/>
    &nbsp;&nbsp;imageLeft: "imageleft"<br/>
    }; </td><td>
 ej.ImagePositions = {<br/>
    &nbsp;&nbsp;ImageRight:"imageright",<br/>
    &nbsp;&nbsp;ImageLeft: "imageleft"<br/>
    }; </td><td>
 </td></tr>
<tr><td>
 ej.buttonSize = {<br/>
    &nbsp;&nbsp;normal : "normal",<br/>
    &nbsp;&nbsp;mini:"mini",<br/>
    &nbsp;&nbsp;small: "small",<br/>
    &nbsp;&nbsp;medium:"medium",<br/>
    &nbsp;&nbsp;large:"large"<br/>
    }; </td><td>
 ej.ButtonSize = {<br/>
    &nbsp;&nbsp;Normal : "normal",<br/>
    &nbsp;&nbsp;Mini:"mini",<br/>
    &nbsp;&nbsp;Small: "small",<br/>
    &nbsp;&nbsp;Medium:"medium",<br/>
    &nbsp;&nbsp;Large: "large"<br/>
    }; </td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td rowspan = "4">
itemMouseOut</td><td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.evets.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.selectedItem</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td rowspan = "4">
itemMouseOver</td><td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.evets.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.selectedItem</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td rowspan = "4">
itemSelected</td><td>
args.events.menuId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
args.evets.menuText</td><td>
args.events.text</td><td>
 </td></tr>
<tr>
<td>
args.events.itemId</td><td>
args.events.ID</td><td>
 </td></tr>
<tr>
<td>
args.events.selectedItem</td><td>
 </td><td>
Removed event argument</td></tr>
</table>

<a name="ejsplitter"></a>

### ejSplitter

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "2">
<b>Properties</b></td><td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
windowResizing</td><td>
enableAutoResize</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
<b>Methods</b></td><td>
addPane</td><td>
addItem</td><td>
 </td></tr>
<tr>
<td>
removePane</td><td>
removeItem</td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td rowspan = "7">
beforeExpandCollapse</td><td>
args.SplitterId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.collapsed.paneIndex</td><td>
args.collapsed.index</td><td>
 </td></tr>
<tr><td>
args.collapsed.paneObj</td><td>
args.collapsed.item</td><td>
 </td></tr>
<tr><td>
args.collapsed.prevSize</td><td>
args.collapsed.size</td><td>
 </td></tr>
<tr><td>
args.expanded.paneIndex</td><td>
args.expanded.index</td><td>
 </td></tr>
<tr><td>
args.expanded.paneObj</td><td>
args.expanded.item</td><td>
 </td></tr>
<tr><td>
args.expanded.prevSize</td><td>
args.expanded.size</td><td>
 </td></tr>
<tr>
<td rowspan = "7">
expandCollapse</td><td>
args.SplitterId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.collapsed.paneIndex</td><td>
args.collapsed.index</td><td>
 </td></tr>
<tr><td>
args.collapsed.paneObj</td><td>
args.collapsed.item</td><td>
 </td></tr>
<tr><td>
args.collapsed.prevSize</td><td>
args.collapsed.size</td><td>
 </td></tr>
<tr><td>
args.expanded.paneIndex</td><td>
args.expanded.index</td><td>
 </td></tr>
<tr><td>
args.expanded.paneObj</td><td>
args.expanded.item</td><td>
 </td></tr>
<tr><td>
args.expanded.prevSize</td><td>
args.expanded.size</td><td>
 </td></tr>
<tr>
<td rowspan = "7">
resize</td><td>
args.SplitterId</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.prevPane.paneIndex</td><td>
args.prevPane.index</td><td>
 </td></tr>
<tr><td>
args.prevPane.paneObj</td><td>
args.prevPane.item</td><td>
 </td></tr>
<tr><td>
args.prevPane.paneSize</td><td>
args.prevPane.size</td><td>
 </td></tr>
<tr><td>
args.nextPane.paneIndex</td><td>
args.nextPane.index</td><td>
 </td></tr>
<tr><td>
args.nextPane.paneObj</td><td>
args.nextPane.item</td><td>
 </td></tr>
<tr><td>
args.nextPane.paneSize</td><td>
args.nextPane.size</td><td>
 </td></tr>
</table>

<a name="ejtab"></a>

### ejTab

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "8">
<b>Properties</b></td><td>
ajaxOptions</td><td>
ajaxSettings</td><td>
 </td></tr>
<tr>
<td>
disabledItems</td><td>
disabledItemIndex</td><td>
 </td></tr>
<tr>
<td>
heightStyle</td><td>
heightAdjustMode</td><td>
 </td></tr>
<tr>
<td>
</td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
showReloadButton</td><td>
showReloadIcon</td><td>
 </td></tr>
<tr>
<td>
<b>Event</b></td><td>
active</td><td>
itemActive</td><td>
 </td></tr>
<tr>
<td rowspan ="5">
<b>Methods</b></td><td>
add</td><td>
addItem</td><td>
 </td></tr>
<tr><td>
disableItems</td><td>
 </td><td>
We have remove this method. use <b>disabledItemIndex property </b>to achieve this behaviour</td></tr>
<tr><td>
enableItems</td><td>
 </td><td>
We have remove this method. Use <b>enabledItemIndex property </b>to achieve this behaviour</td></tr>
<tr><td>
remove</td><td>
removeItem</td><td>
 </td></tr>
<tr><td>
tabCount</td><td>
getItemsCount</td><td>
    </td></tr>
     <tr>
<td>
<b>Enum</b></td><td>
 ej.Tab.heightFormat = {<br/>
         &nbsp;&nbsp;Content: "content",<br/>
         &nbsp;&nbsp;Auto: "auto",<br/>
         &nbsp;&nbsp;Fill: "fill"<br/>
         }; </td> <td>
 ej.Tab.HeightAdjustMode = {<br/>
         &nbsp;&nbsp;Content: "content",<br/>
         &nbsp;&nbsp;Auto: "auto",<br/>
         &nbsp;&nbsp;Fill: "fill"<br/>
         }; </td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td rowspan = "7">
ajaxBeforeLoad</td><td>
 </td><td>
args.url</td><td>
New event arguments</td></tr>
<tr><td>
args.newContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.newSelectedIndex</td><td>
args.activeIndex</td><td>
 </td></tr>
<tr><td>
args.newTab</td><td>
args.activeHeader</td><td>
 </td></tr>
<tr><td>
args.oldTab</td><td>
args.prevActiveHeader</td><td>
 </td></tr>
<tr><td>
args.oldContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.oldSelectedIndex</td><td>
args.prevActiveIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "7">
ajaxLoad</td><td>
 </td><td>
args.url</td><td>
New event arguments</td></tr>
<tr><td>
args.newContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.newSelectedIndex</td><td>
args.activeIndex</td><td>
 </td></tr>
<tr><td>
args.newTab</td><td>
args.activeHeader</td><td>
 </td></tr>
<tr><td>
args.oldTab</td><td>
args.prevActiveHeader</td><td>
 </td></tr>
<tr><td>
args.oldContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.oldSelectedIndex</td><td>
args.prevActiveIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "6">
beforeActive</td><td>
args.newContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.newSelectedIndex</td><td>
args.activeIndex</td><td>
 </td></tr>
<tr><td>
args.newTab</td><td>
args.activeHeader</td><td>
 </td></tr>
<tr><td>
args.oldTab</td><td>
args.prevActiveHeader</td><td>
 </td></tr>
<tr><td>
args.oldContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>><td>
args.oldSelectedIndex</td><td>
args.prevActiveIndex</td><td>
 </td></tr>
<tr>
<td rowspan = "6">
itemActive</td><td>
args.newContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.newSelectedIndex</td><td>
args.activeIndex</td><td>
 </td></tr>
<tr><td>
args.newTab</td><td>
args.activeHeader</td><td>
 </td></tr>
<tr><td>
args.oldTab</td><td>
args.prevActiveHeader</td><td>
 </td></tr>
<tr><td>
args.oldContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr><td>
args.oldSelectedIndex</td><td>
args.prevActiveIndex</td><td>
 </td></tr>
<tr>
<td>
itemRemove</td><td>
args.removeContentPanel</td><td>
 </td><td>
Removed event argument</td></tr>
<tr>
<td>
beforeItemRemove</td><td>
args.deleteIndex</td><td>
args.index</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
itemAdd</td><td>
args.addTab</td><td>
args.tabHeader</td><td>
 </td></tr>
<tr><td>
args.addContentPanel</td><td>
args.tabContent</td><td>
 </td></tr>
<tr>
<td rowspan = "6">
ajaxSuccess</td><td>
 </td><td>
args.url</td><td>
New Event</td></tr>
<tr><td>
 </td><td>
args.type</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.model</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.cancel</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.data</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.content</td><td>
 </td></tr>
<tr>
<td rowspan = "5">
ajaxError</td><td>
 </td><td>
args.url</td><td>
New Event</td></tr>
<tr>
<td>
 </td><td>
args.type</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.model</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.cancel</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.data</td><td>
 </td></tr>
</table>

<a name="ejtagcloud"></a>

### ejTagCloud

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "3">
<b>Properties</b></td><td>
rtl</td><td>
<b>enableRTL   </b></td><td>
 </td></tr>
<tr>
<td>
</td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
title</td><td>
<b>titleText</b></td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
 ej.format = {<br/>
        &nbsp;&nbsp;Cloud: "cloud",<br/>
        &nbsp;&nbsp;List: "list"<br/>
        }; </td><td>
 ej.Format = {<br/>
        &nbsp;&nbsp;Cloud: "cloud",<br/>
        &nbsp;&nbsp;List: "list"<br/>
        }; </td><td>
 </td></tr>
</table>

<a name="ejtextboxes"></a>

### ejTextBoxes

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "11">
 <b>Properties</b></td><td>
Decimals</td><td>
decimalPlaces</td><td>
 </td></tr>
<tr>
<td>
</td><td>
htmlAttributes</td><td> Newly added
 </td></tr>
<tr>
<td>
Localize</td><td>
locale</td><td>
 </td></tr>
<tr>
<td>
Persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
strictMode</td><td>
enableStrictMode</td><td>
 </td></tr><tr>
<td>
</td><td>
validationMessage</td><td> Newly added
 </td></tr>
<tr>
<td>
</td><td>
validationOnType</td><td> Newly added
 </td></tr>
<tr>
<td>
</td><td>
validationRules</td><td> Newly added
 </td></tr>
<tr>
<td>
waterMarkText</td><td>
watermarkText</td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>
Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><td>
Comments</th></tr>
<tr>
<td>
focusIn</td><td>
 </td><td>
args.value</td><td>
New Event argument</td></tr>
<tr>
<td>
focusOut</td><td>
 </td><td>
args.value</td><td>
New Event argument</td></tr>
</table>

<a name="ejtimepicker"></a>

### ejTimePicker

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "8">
Properties</td><td>
localize</td><td>
locale </td><td>
 </td></tr>
<tr>
<td>
minInterval</td><td>
minutesInterval</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td></td><td>
htmlAttributes </td><td>
Newly added </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
secInterval</td><td>
secondsInterval</td><td>
 </td></tr>
<tr>
<td>
showButton</td><td>
showPopupButton</td><td>
 </td></tr>
<tr>
<td rowspan = "2">
Methods</td><td>
getTime</td><td>
getValue</td><td>
 </td></tr>
<tr>
<td>
updateCurrentTime</td><td>
setCurrentTime</td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>
Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><td>
Comments</th></tr>
<tr>
<td>
change</td><td>
 </td><td>
args.prevTime</td><td>
New Event argument</td></tr>
<tr>
<td>
select</td><td>
 </td><td>
args.prevTime</td><td>
New Event argument</td></tr>
<tr>
<td rowspan = "5">
beforeOpen</td><td>
 </td><td>
args.type</td><td>
New Event</td></tr>
<tr>
<td>
 </td><td>
args.model</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.cancel</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.prevTime</td><td>
 </td></tr>
<tr>
<td rowspan = "6">
open</td><td>
 </td><td>
args.type</td><td>
New Event</td></tr>
<tr>
<td>
 </td><td>
args.model</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.cancel</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.prevTime</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.type</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
close</td><td>
 </td><td>
args.model</td><td>
New Event</td></tr>
<tr>
<td>
 </td><td>
args.cancel</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.value</td><td>
 </td></tr>
<tr>
<td>
 </td><td>
args.prevTime</td><td>
 </td></tr>
</table>

<a name="ejtogglebutton"></a>

### ejToggleButton

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "4">
Properties</td><td>
checkedStatus</td><td>
toggleState</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence     </td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td>
<b>Enum</b></td><td>
 ej.contents = {<br/>
        &nbsp;&nbsp;textOnly:"textonly",<br/>
        &nbsp;&nbsp;imageOnly: "imageonly",<br/>
        &nbsp;&nbsp;imageBoth: "imageboth",<br/>
        &nbsp;&nbsp;textAndImage:"textandimage",<br/>
        &nbsp;&nbsp;imageTextImage:"imagetextimage"<br/>
        }; </td><td>
 ej.Contents = {<br/>
        &nbsp;&nbsp;TextOnly:"textonly",<br/>
        &nbsp;&nbsp;ImageOnly: "imageonly",<br/>
        &nbsp;&nbsp;ImageBoth: "imageboth",<br/>
        &nbsp;&nbsp;TextAndImage: "textandimage",<br/>
        &nbsp;&nbsp;ImageTextImage:"imagetextimage"<br/>
        }; </td><td>
 </td></tr>
</table>

<a name="ejtoolbar"></a>

### ejToolbar

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "4">
Properties</td><td>
itemSeparator</td><td>
enableSeprator</td><td>
 </td></tr>
<tr>
<td>
fields:{spriteCSS}</td><td>
spriteCssClass</td><td>
 </td></tr>
<tr>
<td>
roundedCorner</td><td>
showRoundedCorner</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td rowspan = "8">
Methods</td><td>
disableItembyID</td><td>
disableItemByID</td><td>
 </td></tr>
<tr>
<td>
enableItembyID</td><td>
enableItemByID</td><td>
 </td></tr>
<tr>
<td>
disableAll</td><td>
disable</td><td>
 </td></tr>
<tr>
<td>
enableAll</td><td>
enable</td><td>
 </td></tr>
<tr>
<td>
deSelectItem</td><td>
deselectItem</td><td>
 </td></tr>
<tr>
<td>
selectItembyID</td><td>
selectItemByID</td><td>
 </td></tr>
<tr>
<td>
deSelectItembyID</td><td>
deselectItemByID</td><td>
 </td></tr>
<tr>
<td>
removeItembyID</td><td>
removeItemByID</td><td>
 </td></tr>
</table>

<a name="ejtreemap"></a>
### ejTreeMap

<table>
<tr>
<td>
<b>Member Type</b></td><td>
<b>Old API Name</b></td><td>
<b>New API Name</b></td><td>
<b>Comments</b></td></tr>
<tr>
<td rowspan = "9">
Property</td><td>
treeMapLegend</td><td>
legendSettings</td><td>
 </td></tr>
<tr>
<td>
leafItemSetting</td><td>
leafItemSettings</td><td>
 </td></tr>
<tr>
<td>
legendIconHeight</td><td>
iconHeight</td><td>
This API comes under legendSettings</td></tr>
<tr>
<td>
legendIconWidth</td><td>
iconWidth</td><td>
This API comes under legendSettings</td></tr>
<tr>
<td>
legendTemplate</td><td>
template</td><td>
This API comes under legendSettings</td></tr>
<tr>
<td>
canResize</td><td>
enableResize</td><td>
 </td></tr>
<tr>
<td>
showItems</td><td>
N/A</td><td>
This API is removed from leafItemSettings since it is achieved in showLabels api.</td></tr>
<tr>
<td>
showItems</td><td>
N/A</td><td>
This API is removed from treeMapLevel since it is achieved in showLabels API.</td></tr>
<tr>
<td>
labelTemplate</td><td>
itemTemplate</td><td>
This API comes under leafItemSettings. You can  use this template to customize the item with label.</td></tr>
</table>

<a name="ejtreeview"></a>

### ejTreeView

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "8">
Properties</td><td>
allowEdit</td><td>
allowEditing</td><td>
 </td></tr>
<tr>
<td>
dragAndDrop</td><td>
allowDragAndDrop </td><td>
 </td></tr>
<tr>
<td>
dragAndDropAcrossControl</td><td>
allowDragAndDropAcrossControl</td><td>
 </td></tr>
<tr>
<td>
dropChild</td><td>
allowDropChild </td><td>
 </td></tr>
<tr>
<td>
dropSibling</td><td>
allowDropSibling </td><td>
 </td></tr>
<tr>
<td>
expandEvent</td><td>
 expandOn</td><td>
 </td></tr>
<tr>
<td>
persist</td><td>
enablePersistence    </td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
<tr>
<td rowspan = "10">
Events</td><td>
check</td><td>
nodeCheck</td><td>
 </td></tr>
<tr>
<td>
click</td><td>
nodeClick</td><td>
 </td></tr>
<tr>
<td>
collapse</td><td>
nodeCollapse</td><td>
 </td></tr>
<tr>
<td>
drag</td><td>
nodeDrag</td><td>
 </td></tr>
<tr>
<td>
dragStart</td><td>
nodeDragStart</td><td>
 </td></tr>
<tr>
<td>
dragStop</td><td>
nodeDragStop</td><td>
 </td></tr>
<tr>
<td>
dropped</td><td>
nodeDropped</td><td>
 </td></tr>
<tr>
<td>
expand</td><td>
nodeExpand</td><td>
 </td></tr>
<tr>
<td>
select</td><td>
nodeSelect</td><td>
 </td></tr>
<tr>
<td>
uncheck</td><td>
nodeUncheck</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
Methods</td><td>
addNodeCollection</td><td>
addNodes</td><td>
 </td></tr>
<tr>
<td>
getAllCheckedNodes</td><td>
getCheckedNodes </td><td>
 </td></tr>
<tr>
<td>
unSelectedNode</td><td>
unselectNode</td><td>
 </td></tr>
<tr>
<td>
isNodeExpanded</td><td>
 </td><td>
We have removed this method. Use <b>isExpanded method</b> to achieve  this behavior </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
beforeEdit</td><td>
args.currentNode</td><td>
args.currentElement</td><td>
 </td></tr>
<tr>
<td>
nodeCheck</td><td>
args.checked</td><td>
args.isChecked</td><td>
 </td></tr>
<tr>
<td>
nodeClick</td><td>
 </td><td>
args.currentElement</td><td>
 </td></tr>
<tr>
<td>
nodeUncheck</td><td>
args.checked</td><td>
args.isChecked</td><td>
 </td></tr>
<tr>
<td rowspan = "4">
inlineEditValidation</td><td>
args.NodeId</td><td>
args.nodeId</td><td>
 </td></tr>
<tr>
<td>
args.OriginalText</td><td>
args.oldText</td><td>
 </td></tr>
<tr>
<td>
args.ModifiedText</td><td>
args.newText</td><td>
 </td></tr>
<tr>
<td>
args.UpdateChanges</td><td>
 </td><td>
Removed Event argument</td></tr>
</table>

<a name="ejuploadbox"></a>

### ejUploadBox

<table>
<tr>
<th>Member Type</th><th>
Old API Name</th><th>
New API Name</th><th>
Comments</th></tr>
<tr>
<td rowspan = "4">
Properties</td><td>
fileFormatAllow</td><td>
extensionsAllow</td><td>
 </td></tr>
<tr>
<td>
fileFormatDeny</td><td>
extensionsDeny</td><td>
 </td></tr>
<tr>
<td>
multipleFilesSelect</td><td>
multipleFilesSelection</td><td>
 </td></tr>
<tr>
<td>
rtl</td><td>
enableRTL   </td><td>
 </td></tr>
</table>

#### Event arguments

<table>
<tr>
<th>Event Name</th><th>
Old Event Args</th><th>
New Event Args</th><th>
Comments</th></tr>
<tr>
<td>
remove</td><td>
args.fileStatus</td><td>
args.status</td><td>
 </td></tr>
</table>