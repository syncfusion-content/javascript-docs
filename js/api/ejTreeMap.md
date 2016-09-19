---
layout: post
title: Properties, Methods and Events of ejTreeMap Widget
description: API reference for ejMap
documentation: API
platform: js
keywords: treemap, ejtreemap, treemap api, syncfusion
---

# ejTreeMap
<ts root="datavisualization" />

The treemap can be easily configured to the DOM element, such as div and can be created with a highly customized look and feel.

#### Syntax

{% highlight js %}

$(element).ejTreeMap<span class="signature">()</span>

{% endhighlight %}


#### Example

{% highlight html %}
 
<div id="container"> 
 
<script>
// Create TreeMap
$('#container').ejTreeMap();    
</script> 
  
</div>

{% endhighlight %}


#### Requires

* module:jQuery

* module:ej.datavisualization.TreeMap

* module:JsRender

* module:properties


## Members


### borderBrush `string`
{:#members:borderbrush}

Specifies the border brush color of the treemap


#### Default Value

* "white"

#### Example

{% highlight js %}
 
//To set borderBrush API value during initialization 
  $("#container").ejTreeMap( {borderBrush:'white'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the borderBrush API, after initialization:
   
   //Gets the borderBrush value 
   
   var property =$("#container").data("ejTreeMap").model.borderBrush;
 
   //Sets the borderBrush value 
   
   $("#container").data("ejTreeMap").model.borderBrush = 'white'; 

{% endhighlight %}


### borderThickness `number`
{:#members:borderthickness}

Specifies the border thickness of the treemap

#### Default Value

* 1

#### Example

{% highlight js %}
 
//To set borderThickness API value during initialization 
  $("#container").ejTreeMap({borderThickness:1});

{% endhighlight %}


{% highlight js %}
 
//Get or set the borderThickness API, after initialization:
 
   //Gets the borderThickness value 
 
   var property =$("#container").data("ejTreeMap").model.borderThickness;
 
   //Sets the borderThickness value 
   
   $("#container").data("ejTreeMap").model.borderThickness = 1; 

{% endhighlight %}


### uniColorMapping `object`
{:#members:unicolormapping}

Specifies the uniColorMapping settings of the treemap


### uniColorMapping.color `string`
{:#members:unicolormapping-color}

Specifies the uniform color mapping of the treemap

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set uniColorMapping API value during initialization 
  $("#container").ejTreeMap( {uniColorMapping{ color: null }});

{% endhighlight %}


{% highlight js %}
 
//Get or set the uniColorMapping API, after initialization:
   
   //Gets the uniColorMapping value 
   
   var property =$("#container").data("ejTreeMap").model.uniColorMapping.color;
 
   //Sets the uniColorMapping value 
   
   $("#container").data("ejTreeMap").model.uniColorMapping = { color: null }; 

{% endhighlight %}


### desaturationColorMapping `object`
{:#members:desaturationcolormapping}

Specifies the desaturationColorMapping settings of the treemap


### desaturationColorMapping.to `number`
{:#members:desaturationcolormapping-to}

Specifies the to value for desaturation color mapping

#### Default Value

* 0

#### Example

{% highlight js %}
 
//To set to API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ to:1}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the to API, after initialization:
   
   //Gets the to value 
   
   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.to;
 
   //Sets the to value 
   
   $("#container").data("ejTreeMap").model.desaturationColorMapping = { to:1}; 

{% endhighlight %}


### desaturationColorMapping.color `string`
{:#members:desaturationcolormapping-color}

Specifies the color for desaturationColorMapping


#### Default Value

* null

#### Example

{% highlight js %}
 
//To set color API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ color:"#41B8C4" }});

{% endhighlight %}


{% highlight js %}
 
//Get or set the color API, after initialization:
   
   //Gets the color value 
   
   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.color;
 
   //Sets the color for desaturationColorMapping value 
   
   $("#container").data("ejTreeMap").model.desaturationColorMapping = { color:"#41B8C4" }; 

{% endhighlight %}


### desaturationColorMapping.from `number`
{:#members:desaturationcolormapping-from}

Specifies the from value for desaturation color mapping

#### Default Value

* 0

#### Example

{% highlight js %}
 
//To set from API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ from:1}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the from API, after initialization:
   
   //Gets the from value 
   
   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.from;
 
   //Sets the from value 
   
   $("#container").data("ejTreeMap").model.desaturationColorMapping = { from:1}; 

{% endhighlight %}


### desaturationColorMapping.rangeMaximum `number`
{:#members:desaturationcolormapping-rangemaximum}

Specifies the rangeMaximum value for desaturation color mapping

#### Default Value

* 0

#### Example

{% highlight js %}
 
//To set rangeMaximum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMaximum:1}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the rangeMaximum API, after initialization:
   
   //Gets the rangeMaximum value 
   
   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMaximum;
 
   //Sets the rangeMaximum value 
   
   $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMaximum:1}; 

{% endhighlight %}


### desaturationColorMapping.rangeMinimum `number`
{:#members:desaturationcolormapping-rangeminimum}

Specifies the rangeMinimum value for desaturation color mapping

#### Default Value

* 0

#### Example

{% highlight js %}
 
//To set rangeMinimum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMinimum:1}});

{% endhighlight %}

{% highlight js %}
 
//Get or set the rangeMinimum API, after initialization:
   
   //Gets the rangeMinimum value 
   
   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMinimum;
 
   //Sets the rangeMinimum value 
   
   $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMinimum:1}; 

{% endhighlight %}


### paletteColorMapping `object`
{:#members:palettecolormapping}

Specifies the paletteColorMapping of the treemap


### paletteColorMapping.colors `array`
{:#members:palettecolormapping-colors}

Specifies the colors of the paletteColorMapping

#### Default Value

* []

#### Example

{% highlight js %}
 
//To set the colors of the paletteColorMapping during initialization 
  $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the colors of the paletteColorMapping, after initialization:
   
   //Gets the colors of the paletteColorMapping value 
   
   var property =$("#container").data("ejTreeMap").model.paletteColorMapping;
 
   //Sets the the colors of the paletteColorMapping
   
   $("#container").data("ejTreeMap").model.paletteColorMapping = {colors: ["red","green","blue", "yellow"]}; 

{% endhighlight %}


### colorValuePath `string`
{:#members:colorvaluepath}

Specifies the color value path of the treemap

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set colorValuePath API value during initialization 
  $("#container").ejTreeMap({colorValuePath:'GoldMedals'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the colorValuePath API, after initialization:
   
   //Gets the colorValuePath value 
   
   var property =$("#container").data("ejTreeMap").model.colorValuePath;
 
   //Sets the colorValuePath value 
   
   $("#container").data("ejTreeMap").model.colorValuePath = 'GoldMedals'; 

{% endhighlight %}


### dataSource `object`
{:#members:datasource}

Specifies the datasource of the treemap

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set datasource API value during initialization 
  $("#container").ejTreeMap({datasource:medal_data});

{% endhighlight %}


{% highlight js %}
 
//Get or set the datasource API, after initialization:
   
   //Gets the datasource value 
   
   var property =$("#container").data("ejTreeMap").model.datasource;
 
   //Sets the datasource value 
   
   $("#container").data("ejTreeMap").model.datasource = medal_data; 

{% endhighlight %}


### dockPosition `enum`
{:#members:dockposition}

<ts name = "ej.datavisualization.TreeMap.DockPosition"/>

Specifies the dockPosition for legend

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">top</td>			
			<td class="description">specifies the top position</td>
		</tr>
		<tr>
			<td class="name">bottom</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">right</td>			
			<td class="description">specifies the bottom position</td>
		</tr>
    <tr>
			<td class="name">left</td>			
			<td class="description">specifies the left position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* top

#### Example

{% highlight js %}
 
//To set dockPosition API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ dockPosition: "top"}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the dockPosition API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.dockPosition;
 
   //Sets the dockPosition value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { dockPosition: "top"}; 

{% endhighlight %}


### drillDownHeaderColor `string`
{:#members:drilldownheadercolor}

specifies the drillDown header color

####Default Value

* 'null'

#### Example

{% highlight js %}
  
// Set the drillDownHeaderColor during initialization.                  
   $("#container").ejTreeMap({drillDownHeaderColor:'#0478c3'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the drillDownHeaderColor API, after initialization:
   
   //Gets the drillDownHeaderColor value 
   
   var property =$("#container").data("ejTreeMap").model.drillDownHeaderColor;
 
   //Sets the drillDownHeaderColor value 
   
   $("#container").data("ejTreeMap").model.drillDownHeaderColor = '#0478c3'; 

{% endhighlight %}


### drillDownSelectionColor `string`
{:#members:drilldownselectioncolor}

specifies the drillDown selection color

#### Default Value

* '#000000'

#### Example

{% highlight js %}
  
// Set the drillDownSelectionColor during initialization.                       
   $("#container").ejTreeMap({drillDownSelectionColor:'#e5e5e5'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the drillDownSelectionColor API, after initialization:
   
   //Gets the drillDownSelectionColor value 
   
   var property =$("#container").data("ejTreeMap").model.drillDownSelectionColor;
 
   //Sets the drillDownSelectionColor value 
   
   $("#container").data("ejTreeMap").model.drillDownSelectionColor = '#000000';

{% endhighlight %}


### enableDrillDown `boolean`
{:#members:enabledrilldown}

Enable/Disable the drillDown for treemap

#### Default Value

* false

#### Example
{:.example}


{% highlight js %}
 
//To set enableDrillDown API value during initialization 
  $("#container").ejTreeMap({enableDrillDown:true});

{% endhighlight %}


{% highlight js %}
 
//Get or set the enableDrillDown API, after initialization:
   
   //Gets the enableDrillDown value 
   
   var property =$("#container").data("ejTreeMap").model.enableDrillDown;
 
   //Sets the enableDrillDown value 
   
   $("#container").data("ejTreeMap").model.enableDrillDown = true; 

{% endhighlight %}



### isResponsive `boolean`
{:#members:isresponsive}

Controls whether Treemap has to be responsive while resizing the window.

#### Default Value

* true

#### Example

{% highlight js %}
 
//To set isResponsive API value during initialization 
  $("#container").ejTreeMap({isResponsive:true});
{% endhighlight %}

### enableResize `boolean`
{:#members:enableresize}

Specifies whether treemap need to resize when container is resized

#### Default Value

* true

#### Example

{% highlight js %}
 
//To set enableResize API value during initialization 
  $("#container").ejTreeMap({enableResize:false});

{% endhighlight %}


{% highlight js %}
 
//Get or set the enableResize API, after initialization:
   
   //Gets the enableResize value 
   
   var property =$("#container").data("ejTreeMap").model.enableResize;
 
   //Sets the enableResize value 
   
   $("#container").data("ejTreeMap").model.enableResize = false; 

{% endhighlight %}


### draggingOnSelection`boolean`
{:#members:draggingOnSelection}

This property is used to select treemap items while clicking and dragging

#### Default Value

* false

#### Example

{% highlight js %}
 
//To set draggingOnSelection API value during initialization 
  $("#container").ejTreeMap({draggingOnSelection:false});
{% endhighlight %}


### draggingGroupOnSelection`boolean`
{:#members:draggingGroupOnSelection}

This property is used to select group of treemap items while clicking and dragging 

#### Default Value

* false

#### Example

{% highlight js %}
 
//To set draggingGroupOnSelectionAPI value during initialization 
  $("#container").ejTreeMap({draggingGroupOnSelection:false});
{% endhighlight %}


### groupColorMapping `array`
{:#members:groupcolormapping}

Specifies the group color mapping of the treemap

#### Default Value

* []

#### Example

{% highlight js %}
 
//To set groupColorMapping API value during initialization 
  $("#container").ejTreeMap( {groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}]}] });

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupColorMapping API, after initialization:
   
   //Gets the groupColorMapping value 
   
   var property =$("#container").data("ejTreeMap").model.groupColorMapping;
 
   //Sets the groupColorMapping value 
   
   $("#container").data("ejTreeMap").model.groupColorMapping = [groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}] }]});
   
{% endhighlight %}


### groupColorMapping.groupID `string`
{:#members:groupcolormapping-groupid}

Specifies the groupID for GroupColorMapping.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the groupID for GroupColorMapping during initialization.                         
        $("#container").ejTreeMap({groupColorMapping: [{ groupID:"Asia" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupID for GroupColorMapping after initialization:

  //Gets the groupID for GroupColorMapping from map.

  var property =$("#container").data("ejTreeMap").model.groupColorMapping.groupID;

  //Sets the groupID for GroupColorMapping to map.

  $("#container").data("ejTreeMap").model.groupColorMapping.groupID  = "Asia";
  
{% endhighlight %}


### legendSettings `object`
{:#members:legendsettings}

Specifies the legend settings of the treemap


### legendSettings.height `number`
{:#members:legendsettings-height}

Specifies the height for legend

#### Default Value

* 30

#### Example

{% highlight js %}
 
//To set height API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ height: 15}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the height API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.height;
 
   //Sets the height value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { height: 30};

{% endhighlight %}


### legendSettings.width `number`
{:#members:legendsettings-width}

Specifies the width for legend

#### Default Value

* 100

#### Example

{% highlight js %}
 
//To set width API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ width: 100}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the width API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.width;
 
   //Sets the width value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { width: 100}; 

{% endhighlight %}


### legendSettings.iconHeight `number`
{:#members:legendsettings-iconheight}

Specifies the iconHeight for legend

#### Default Value

* 15

#### Example

{% highlight js %}
 
//To set iconHeight API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ iconHeight: 15}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the iconHeight API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.iconHeight;
 
   //Sets the iconHeight value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { iconHeight: 15};

{% endhighlight %}


### legendSettings.iconWidth `number`
{:#members:legendsettings-iconwidth}

Specifies the iconWidth for legend

#### Default Value

* 15

#### Example

{% highlight js %}
 
//To set iconWidth API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ iconWidth: 15}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the iconWidth API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.iconWidth;
 
   //Sets the iconWidth value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { iconWidth: 15}; 

{% endhighlight %}


### legendSettings.template `string`
{:#members:legendsettings-template}

Specifies the template for legendSettings

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set template API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ template: null}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the template API, after initialization:
   
   //Gets the template value 
   
   var property =$("#container").data("ejTreeMap").model.legendSettings.template;
 
   //Sets the template value 
   
   $("#container").data("ejTreeMap").model.legendSettings = { template: null}; 

{% endhighlight %}

### legendSettings.mode `string`
{:#members:legendsettings-mode}

Specifies the mode for legendSettings whether defaul or interactive mode

#### Default Value

* "default"

#### Example

{% highlight js %}
 
//To set mode API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ mode: "interactive"}});

{% endhighlight %}

### legendSettings.title `string`
{:#members:legendsettings-title}

Specifies the title text for legend

#### Default Value

* ""

#### Example

{% highlight js %}
 
//To set title API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ title: "Population"}});

{% endhighlight %}

### legendSettings.leftLabel `string`
{:#members:legendsettings-leftlabel}

Specifies the leftLabel text for legend

#### Default Value

* ""

#### Example

{% highlight js %}
 
//To set leftLabel API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ leftLabel: "10Million"}});

{% endhighlight %}

### legendSettings.rightLabel `string`
{:#members:legendsettings-leftlabel}

Specifies the rightLabel text for legend

#### Default Value

* ""

#### Example

{% highlight js %}
 
//To set rightLabel API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ rightLabel: "100Million"}});

{% endhighlight %}


### legendSettings.dockPosition `string`
{:#members:legendsettings-dockposition}

Specifies the dockPosition text for legend

#### Default Value

* "top"

#### Example

{% highlight js %}
 
//To set dockPosition API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ dockPosition: "bottom"}});

{% endhighlight %}

### legendSettings.alignment `string`
{:#members:legendsettings-alignment}

Specifies the alignment text for legend

#### Default Value

* "near"

#### Example

{% highlight js %}
 
//To set alignment API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ alignment: "far"}});

{% endhighlight %}

### legendSettings.columnCount `number`
{:#members:legendsettings-columncount}

Specifies the alignment text for legend

#### Default Value

* 0

#### Example

{% highlight js %}
 
//To set columnCount API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ columnCount: 2}});

{% endhighlight %}

### highlightBorderBrush `string`
{:#members:highlightborderbrush}

Specifies the highlight border brush of treemap

#### Default Value

* "gray"

#### Example

{% highlight js %}
 
//To set highlightBorderBrush API value during initialization 
  $("#container").ejTreeMap({highlightBorderBrush:'gray'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightBorderBrush API, after initialization:
   
   //Gets the highlightBorderBrush value 
   
   var property =$("#container").data("ejTreeMap").model.highlightBorderBrush;
 
   //Sets the highlightBorderBrush value 
   
   $("#container").data("ejTreeMap").model.highlightBorderBrush = 'gray';

{% endhighlight %}


### highlightBorderThickness `number`
{:#members:highlightborderthickness}

Specifies the border thickness when treemap items is highlighted in the treemap

#### Default Value

* 5

#### Example

{% highlight js %}
 
//To set highlightBorderThickness API value during initialization 
  $("#container").ejTreeMap({highlightBorderThickness:5});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightBorderThickness API, after initialization:
 
   //Gets the highlightBorderThickness value 
 
   var property =$("#container").data("ejTreeMap").model.highlightBorderThickness;
 
   //Sets the highlightBorderThickness value 
   
   $("#container").data("ejTreeMap").model.highlightBorderThickness = 5; 

{% endhighlight %}


### highlightGroupBorderBrush `string`
{:#members:highlightgroupborderbrush}

Specifies the highlight border brush of treemap

#### Default Value

* "gray"

#### Example

{% highlight js %}
 
//To set highlightGroupBorderBrush API value during initialization 
  $("#container").ejTreeMap({highlightGroupBorderBrush:'gray'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightGroupBorderBrush API, after initialization:
   
   //Gets the highlightGroupBorderBrush value 
   
   var property =$("#container").data("ejTreeMap").model.highlightGroupBorderBrush;
 
   //Sets the highlightGroupBorderBrush value 
   
   $("#container").data("ejTreeMap").model.highlightGroupBorderBrush = 'gray'; 

{% endhighlight %}


### highlightGroupBorderThickness `number`
{:#members:highlightgroupborderthickness}

Specifies the border thickness when treemap items is highlighted in the treemap

#### Default Value

* 5

#### Example

{% highlight js %}
 
//To set highlightGroupBorderThickness API value during initialization 
  $("#container").ejTreeMap({highlightGroupBorderThickness:5});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightGroupBorderThickness API, after initialization:
   
   //Gets the highlightGroupBorderThickness value 
   
   var property =$("#container").data("ejTreeMap").model.highlightGroupBorderThickness;
 
   //Sets the highlightGroupBorderThickness value 
   
   $("#container").data("ejTreeMap").model.highlightGroupBorderThickness = 5;

{% endhighlight %}


### highlightGroupOnSelection `boolean`
{:#members:highlightgrouponselection}

Specifies whether treemap item need to highlighted on selection

#### Default Value

* false

#### Example
{:.example}


{% highlight js %}
 
//To set highlightGroupOnSelection API value during initialization 
  $("#container").ejTreeMap({highlightGroupOnSelection:false});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightGroupOnSelection API, after initialization:
   
   //Gets the highlightGroupOnSelection value 
   
   var property =$("#container").data("ejTreeMap").model.highlightGroupOnSelection;
 
   //Sets the highlightGroupOnSelection value 
   
   $("#container").data("ejTreeMap").model.highlightGroupOnSelection = false; 

{% endhighlight %}


### highlightOnSelection `boolean`
{:#members:highlightonselection}

Specifies whether treemap item need to highlighted on selection

#### Default Value

* false

#### Example

{% highlight js %}
 
//To set highlightOnSelection API value during initialization 
  $("#container").ejTreeMap({highlightOnSelection:false});

{% endhighlight %}


{% highlight js %}
 
//Get or set the highlightOnSelection API, after initialization:
   
   //Gets the highlightOnSelection value 
   
   var property =$("#container").data("ejTreeMap").model.highlightOnSelection;
 
   //Sets the highlightOnSelection value 
   
   $("#container").data("ejTreeMap").model.highlightOnSelection = false; 

{% endhighlight %}


### itemsLayoutMode `enum`
{:#members:itemslayoutmode}

<ts name = "ej.datavisualization.TreeMap.ItemsLayoutMode"/>

Specifies the items layout mode of the treemap. Accepted itemsLayoutMode values are Squarified, SliceAndDiceHorizontal, SliceAndDiceVertical and SliceAndDiceAuto

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">squarified</td>			
			<td class="description">specifies the squarified as layout type position</td>
		</tr>
		<tr>
			<td class="name">sliceanddicehorizontal</td>			
			<td class="description">specifies the sliceanddicehorizontal as layout type position</td>
		</tr>
    <tr>
			<td class="name">sliceanddicevertical</td>			
			<td class="description">specifies the sliceanddicevertical as layout type position</td>
		</tr>
    <tr>
			<td class="name">sliceanddiceauto</td>			
			<td class="description">specifies the sliceanddiceauto as layout type position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* "Squarified"

#### Example

{% highlight js %}
 
//To set itemsLayoutMode API value during initialization 
  $("#container").ejTreeMap({itemsLayoutMode:ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified});

{% endhighlight %}


{% highlight js %}
 
//Get or set the itemsLayoutMode API, after initialization:
   
   //Gets the itemsLayoutMode value 
   
   var property =$("#container").data("ejTreeMap").model.itemsLayoutMode;
 
   //Sets the itemsLayoutMode value 
   
   $("#container").data("ejTreeMap").model.itemsLayoutMode = ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified; 

{% endhighlight %}


### leafItemSettings `Object`
{:#members:leafitemsettings}

Specifies the leaf settings of the treemap


### leafItemSettings.borderBrush `string`
{:#members:leafitemsettings-borderbrush}

Specifies the border brush color of the leaf item.

#### Default Value

* "white"

#### Example

{% highlight js %}
 
//To set borderBrush API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ borderBrush: "white"}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the borderBrush API, after initialization:
   
   //Gets the borderBrush value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderBrush;
 
   //Sets the borderBrush value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings = { borderBrush: "white"}; 

{% endhighlight %}


### leafItemSettings.borderThickness `number`
{:#members:leafitemsettings-borderthickness}

Specifies the border thickness of the leaf item.

#### Default Value

* 1

#### Example

{% highlight js %}
 
//To set borderThickness API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ borderThickness: 1}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the borderThickness API, after initialization:
   
   //Gets the borderThickness value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderThickness;
 
   //Sets the borderThickness value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings = { borderThickness: 1}; 

{% endhighlight %}


### leafItemSettings.itemTemplate `string`
{:#members:leafitemsettings-itemtemplate}

Specifies the label template of the leaf item.

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set itemTemplate API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ itemTemplate: "temp"}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the itemTemplate API, after initialization:
   
   //Gets the itemTemplate value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.itemTemplate;
 
   //Sets the itemTemplate value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings = { itemTemplate: "temp"}; 
 
{% endhighlight %}


### leafItemSettings.labelPath `string`
{:#members:leafitemsettings-labelpath}

Specifies the label path of the leaf item.

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set labelPath API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelPath: "GameName"}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the labelPath API, after initialization:
   
   //Gets the labelPath value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPath;
 
   //Sets the labelPath value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings = { labelPath: "GameName"}; 

{% endhighlight %}


### leafItemSettings.labelPosition `enum`
{:#members:leafitemsettings-labelposition}

<ts name = "ej.datavisualization.TreeMap.Position"/>

Specifies the position of the leaf labels.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">none</td>			
			<td class="description">specifies the none position</td>
		</tr>
		<tr>
			<td class="name">topleft</td>			
			<td class="description">specifies the topleft position</td>
		</tr>
    <tr>
			<td class="name">topcenter</td>			
			<td class="description">specifies the topcenter position</td>
		</tr>
    <tr>
			<td class="name">topright</td>			
			<td class="description">specifies the topright position</td>
		</tr>    
    <tr>
			<td class="name">centerleft</td>			
			<td class="description">specifies the centerleft position</td>
		</tr>
		<tr>
			<td class="name">center</td>			
			<td class="description">specifies the center position</td>
		</tr>
    <tr>
			<td class="name">centerright</td>			
			<td class="description">specifies the centerright position</td>
		</tr>
    <tr>
			<td class="name">bottomleft</td>			
			<td class="description">specifies the bottomleft position</td>
		</tr>
    <tr>
			<td class="name">bottomcenter</td>			
			<td class="description">specifies the bottomcenter position</td>
		</tr>
    <tr>
			<td class="name">bottomright</td>			
			<td class="description">specifies the bottomright position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* center

#### Example

{% highlight js %}
 
//To set labelPosition API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelPosition: "center"}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the labelPosition API, after initialization:
   
   //Gets the labelPosition value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPosition;
 
   //Sets the labelPosition value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings.labelPosition= "topleft"; 

{% endhighlight %}


### leafItemSettings.labelVisibilityMode `enum`
{:#members:leafitemsettings-labelvisibilitymode}

<ts name = "ej.datavisualization.TreeMap.VisibilityMode"/>

Specifies the mode of label visibility

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="visible">top</td>			
			<td class="description">specifies the visible mode</td>
		</tr>
    <tr>
			<td class="name">hide on exceeded length</td>			
			<td class="description">specifies the hide on exceeded length mode</td>
		</tr>
	</tbody>
</table>

#### Default Value

* visible

#### Example

{% highlight js %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelVisibilityMode: "visible"}});
  
{% endhighlight %}


{% highlight js %}
 
//Get or set the labelVisibilityMode API, after initialization:
   
   //Gets the labelVisibilityMode value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode;
 
   //Sets the labelVisibilityMode value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode= "visible"; 

{% endhighlight %}


### leafItemSettings.showLabels `boolean`
{:#members:leafitemsettings-showlabels}

Shows or hides the label of the leaf item.

#### Default Value

* "false"

#### Example

{% highlight js %}
 
//To set showLabels API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ showLabels: "false"}});
  
{% endhighlight %}


{% highlight js %}
 
//Get or set the showLabels API, after initialization:
   
   //Gets the showLabels value 
   
   var property =$("#container").data("ejTreeMap").model.leafItemSettings.showLabels;
 
   //Sets the showLabels value 
   
   $("#container").data("ejTreeMap").model.leafItemSettings = { showLabels: "false"}; 

{% endhighlight %}


### rangeColorMapping `array`
{:#members:rangecolormapping}

Specifies the rangeColorMapping settings of the treemap

#### Default Value

* []

#### Example

{% highlight js %}
 
//To set rangeColorMapping API value during initialization 
  $("#container").ejTreeMap( {rangeColorMapping:[{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]});

{% endhighlight %}


{% highlight js %}
 
//Get or set the rangeColorMapping API, after initialization:
   
   //Gets the rangeColorMapping value 
   
   var property =$("#container").data("ejTreeMap").model.rangeColorMapping;
 
   //Sets the rangeColorMapping value 
   
   $("#container").data("ejTreeMap").model.rangeColorMapping = [{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]; 

{% endhighlight %}


### rangeColorMapping.color `string`
{:#members:rangecolormapping-color}

Specifies the color value for rangeColorMapping.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the color value for rangeColorMapping during initialization.                     
   $("#container").ejTreeMap({rangeColorMapping: [{ color: "#77D8D8" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the color value for rangeColorMapping after initialization:
  
  //Gets the color value for rangeColorMapping from map.
  
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.color;
  
  //Sets the color value for rangeColorMapping to map.
  
  $("#container").data("ejTreeMap").model.rangeColorMapping.color  = "#77D8D8";

{% endhighlight %}


### rangeColorMapping.gradientColors `array`
{:#members:rangecolormapping-gradientcolors}

specifies the gradient colors for th given range value

#### Default Value

* []

#### Example

{% highlight js %}
 
//To set gradientColors API value during initialization 
  $("#container").ejTreeMap( {rangeColorMapping:[{ from: "0", to: "1", gradientColors: ["#fde6cc", "#fab665"] }]});

{% endhighlight %}


{% highlight js %}
 
//Get or set the gradientColors API, after initialization:
   
   //Gets the gradientColors value 
   
   var property =$("#container").data("ejTreeMap").model.rangeColorMapping.gradientColors;
 
   //Sets the gradientColors value 
   
   $("#container").data("ejTreeMap").model.rangeColorMapping.gradientColors = ["#fde6cc", "#fab665"]; 

{% endhighlight %}


### rangeColorMapping.from `number`
{:#members:rangecolormapping-from}

Specifies the from value for rangeColorMapping.

#### Default Value

* -1

#### Example

{% highlight js %}
  
// Set the from value for rangeColorMapping during initialization.                      
   $("#container").ejTreeMap({rangeColorMapping: [{ from:-1 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the from value for rangeColorMapping after initialization:

  //Gets the from value for rangeColorMapping from map.

  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.from;

  //Sets the from value for rangeColorMapping to map.

  $("#container").data("ejTreeMap").model.rangeColorMapping.from  = -1;

{% endhighlight %}


### rangeColorMapping.legendLabel `string`
{:#members:rangecolormapping-legendlabel}

Specifies the legend label value for rangeColorMapping.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the legendlabel value for rangeColorMapping during initialization.                       
   $("#container").ejTreeMap({rangeColorMapping: [{ legendlabel: "1% Growth" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the legendlabel value for rangeColorMapping after initialization:

  //Gets the legendlabel value for rangeColorMapping from map.

  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel;

  //Sets the legendlabel value for rangeColorMapping to map.

  $("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel  = "1% Growth";

{% endhighlight %}


### rangeColorMapping.to `number`
{:#members:rangecolormapping-to}

Specifies the to value for rangeColorMapping.

#### Default Value

* -1

#### Example

{% highlight js %}
  
// Set the to value for rangeColorMapping during initialization.                        
   $("#container").ejTreeMap({rangeColorMapping: [{ to:-1 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the to value for rangeColorMapping after initialization:

  //Gets the to value for rangeColorMapping from map.

  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.to;

  //Sets the to value for rangeColorMapping to map.

  $("#container").data("ejTreeMap").model.rangeColorMapping.to  = -1;

{% endhighlight %}



### selectionMode `enum`
{:#members:selectionmode}

<ts name = "ej.datavisualization.TreeMap.selectionMode"/>

Specifies the selection mode of treemap item. Accepted selection mode values are Default and Multiple.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">default</td>			
			<td class="description">specifies the default mode</td>
		</tr>
		<tr>
			<td class="name">multiple</td>			
			<td class="description">specifies the multiple mode</td>
		</tr>  
	</tbody>
</table>

#### Default Value

* "default"

#### Example

{% highlight js %}
  
// Set the selection mode during initialization.                                        
          $("#container").ejTreeMap({selectionMode:'default'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the selection mode after initialization:
  
  //Gets the selection mode from treemap.
  
  var property =$("#container").data("ejTreeMap").model.selectionMode;
  
  //Sets the selection mode to treemap.
  
  $("#container").data("ejTreeMap").model.selectionMode  = 'default';

{% endhighlight %}

### groupSelectionMode `enum`
{:#members:groupselectionmode}

<ts name = "ej.datavisualization.TreeMap.groupSelectionMode"/>

Specifies the selection mode of the treemap. Accepted selection mode values are Default and Multiple.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">default</td>			
			<td class="description">specifies the default mode</td>
		</tr>
		<tr>
			<td class="name">multiple</td>			
			<td class="description">specifies the multiple mode</td>
		</tr>  
	</tbody>
</table>

#### Default Value

* "default"

#### Example

{% highlight js %}
  
// Set the selection mode during initialization.                                        
          $("#container").ejTreeMap({groupSelectionMode:'default'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupSelection mode after initialization:
  
  //Gets the selection mode from treemap.
  
  var property =$("#container").data("ejTreeMap").model.groupSelectionMode;
  
  //Sets the selection mode to treemap.
  
  $("#container").data("ejTreeMap").model.groupSelectionMode  = 'default';

{% endhighlight %}


### showLegend `boolean`
{:#members:showlegend}

Specifies the legend visibility status of the treemap

#### Default Value

* false

#### Example

{% highlight js %}
 
//To set showLegend API value during initialization 
  $("#container").ejTreeMap({showLegend:false});

{% endhighlight %}


{% highlight js %}
 
//Get or set the showLegend API, after initialization:
   
   //Gets the showLegend value 
   
   var property =$("#container").data("ejTreeMap").model.showLegend;
 
   //Sets the showLegend value 
   
   $("#container").data("ejTreeMap").model.showLegend = false; 

{% endhighlight %}


### enableGradient `boolean`
{:#members:enableGradient}

Specifies whether gradient color has to be applied for treemap items

#### Default Value

* false

#### Example

{% highlight js %}
 
//To set enableGradient API value during initialization 
  $("#container").ejTreeMap({enableGradient:true});

{% endhighlight %}


{% highlight js %}
 
//Get or set the enableGradient API, after initialization:
   
   //Gets the enableGradient value 
   
   var property =$("#container").data("ejTreeMap").model.enableGradient;
 
   //Sets the enableGradient value 
   
   $("#container").data("ejTreeMap").model.enableGradient = false; 

{% endhighlight %}



### showTooltip `boolean`
{:#members:showTooltip}

Specifies whether treemap showTooltip need to be visible

{% highlight js %}
 
//To set showTooltip API value during initialization 
  $("#container").ejTreeMap({showTooltip:false});

{% endhighlight %}


{% highlight js %}
 
//Get or set the showTooltip API, after initialization:
   
   //Gets the showTooltip value 
   
   var property =$("#container").data("ejTreeMap").model.showTooltip;
 
   //Sets the showTooltip value 
   
   $("#container").data("ejTreeMap").model.showTooltip = false; 

{% endhighlight %}


### tooltipTemplate `string`
{:#members:tooltiptemplate}

Specifies the tooltip template of the treemap

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set tooltipTemplate API value during initialization 
  $("#container").ejTreeMap({tooltipTemplate:'template'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the tooltipTemplate API, after initialization:
   
   //Gets the tooltipTemplate value 
   
   var property =$("#container").data("ejTreeMap").model.tooltipTemplate;
 
   //Sets the tooltipTemplate value 
   
   $("#container").data("ejTreeMap").model.tooltipTemplate = 'template'; 

{% endhighlight %}


### treeMapItems `array`
{:#members:treemapitems}

Hold the treeMapItems to be displayed in treemap

#### Default Value

* []

#### Example

{% highlight js %}
  
// Set the treeMapItems during initialization. 
  $("#container").ejTreeMap({treeMapItems:[]});                             

{% endhighlight %}


{% highlight js %}
 
//Get or set the treeMapItems after initialization:

  //Gets the treeMapItems from treemap.

  var property =$("#container").data("ejTreeMap").model.treeMapItems;
             
  //Sets the treeMapItems to treemap.

  $("#container").data("ejTreeMap").model.treeMapItems = []; 

{% endhighlight %}


### levels `array`
{:#members:levels}

Specify levels of treemap for grouped visualization of data

#### Default Value

* []

#### Example

{% highlight js %}
  
// Set the levels during initialization.                
  $("#container").ejTreeMap({   levels: [{ groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the levels after initialization:
  
  //Gets the levels from map.
  
  var levels =$("#container").data("ejTreeMap").model.levels[levelIndex];
  
  //Sets the levels to map.
  
  $("#container").data("ejTreeMap").model.levels[levelIndex]  = { groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' };

{% endhighlight %}


### levels.groupBackground `string`
{:#members:levels-groupbackground}

specifies the group background

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the groupBackground during initialization.                       
   $("#container").ejTreeMap({levels: [{ groupBackground:"white" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupBackground after initialization:

  //Gets the groupBackground from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground;

  //Sets the groupBackground to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground  = "white";

{% endhighlight %}


### levels.groupBorderColor `string`
{:#members:levels-groupbordercolor}

Specifies the group border color for tree map level.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the groupBorderColor during initialization.                      
   $("#container").ejTreeMap({levels: [{ groupBorderColor:"#58585B" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupBorderColor after initialization:

  //Gets the groupBorderColor from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor;

  //Sets the groupBorderColor to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor  = "#58585B";

{% endhighlight %}


### levels.groupBorderThickness `number`
{:#members:levels-groupborderthickness}

Specifies the group border thickness for tree map level.

#### Default Value

* 1

#### Example

{% highlight js %}
  
// Set the groupBorderThickness during initialization.                  
   $("#container").ejTreeMap({levels: [{ groupBorderThickness:1 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupBorderThickness after initialization:

  //Gets the groupBorderThickness from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness;

  //Sets the groupBorderThickness to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness  = 1;

{% endhighlight %}


### levels.groupGap `number`
{:#members:levels-groupgap}

Specifies the group gap for tree map level.

#### Default Value

* 1

#### Example

{% highlight js %}
  
// Set the groupGap during initialization.                      
   $("#container").ejTreeMap({levels: [{ groupGap:1 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupGap after initialization:
  
  //Gets the groupGap from map.
  
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupGap;
  
  //Sets the groupGap to map.
  
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupGap  = 1;

{% endhighlight %}


### levels.groupPadding `number`
{:#members:levels-grouppadding}

Specifies the group padding for tree map level.

#### Default Value

* 4

#### Example

{% highlight js %}
  
// Set the groupPadding during initialization.                  
   $("#container").ejTreeMap({levels: [{ groupPadding:4 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the groupPadding after initialization:

  //Gets the groupPadding from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding;

  //Sets the groupPadding to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding  = 4;

{% endhighlight %}


### levels.groupPath `string`
{:#members:levels-grouppath}

Specifies the group path for tree map level.

#### Example

{% highlight js %}
  
// Set the groupPath during initialization.                     
   $("#container").ejTreeMap({levels: [{ groupPath:"pathName" }]})

{% endhighlight %}

{% highlight js %}
 
//Get or set the groupPath after initialization:

  //Gets the groupPath from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPath;

  //Sets the groupPath to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPath  = "pathName";

{% endhighlight %}


### levels.headerHeight `number`
{:#members:levels-headerheight}

Specifies the header height for tree map level.

#### Default Value

* 0

#### Example

{% highlight js %}
  
// Set the headerHeight during initialization.                  
   $("#container").ejTreeMap({levels: [{ headerHeight:20 }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the headerHeight after initialization:

  //Gets the headerHeight from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight;

  //Sets the headerHeight to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight  = 1;

{% endhighlight %}


### levels.headerTemplate `string`
{:#members:levels-headertemplate}

Specifies the header template for tree map level.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the headerTemplate during initialization.                        
   $("#container").ejTreeMap({levels: [{ headerTemplate:"template" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the headerTemplate after initialization:

  //Gets the headerTemplate from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate;

  //Sets the headerTemplate to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate  = "template";

{% endhighlight %}


### levels.headerVisibilityMode `enum`
{:#members:levels-headervisibilitymode}

<ts name = "ej.datavisualization.TreeMap.VisibilityMode"/>

Specifies the mode of header visibility

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="visible">top</td>			
			<td class="description">specifies the visible mode</td>
		</tr>
    <tr>
			<td class="name">hide on exceeded length</td>			
			<td class="description">specifies the hide on exceeded length mode</td>
		</tr>
	</tbody>
</table>

#### Default Value

* visible

#### Example

{% highlight js %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({levels:[{ headerVisibilityMode: "visible"}]});

{% endhighlight %}


{% highlight js %}
 
//Get or set the headerVisibilityMode API, after initialization:
   
   //Gets the headerVisibilityMode value 
   
   var property =$("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode;
 
   //Sets the headerVisibilityMode value 
   
   $("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode= "visible"; 

{% endhighlight %}


### levels.labelPosition `enum`
{:#members:levels-labelposition}

<ts ref = "ej.datavisualization.TreeMap.Position"/>

Specifies the position of the labels.

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="name">none</td>			
			<td class="description">specifies the none position</td>
		</tr>
		<tr>
			<td class="name">topleft</td>			
			<td class="description">specifies the topleft position</td>
		</tr>
    <tr>
			<td class="name">topcenter</td>			
			<td class="description">specifies the topcenter position</td>
		</tr>
    <tr>
			<td class="name">topright</td>			
			<td class="description">specifies the topright position</td>
		</tr>    
    <tr>
			<td class="name">centerleft</td>			
			<td class="description">specifies the centerleft position</td>
		</tr>
		<tr>
			<td class="name">center</td>			
			<td class="description">specifies the center position</td>
		</tr>
    <tr>
			<td class="name">centerright</td>			
			<td class="description">specifies the centerright position</td>
		</tr>
    <tr>
			<td class="name">bottomleft</td>			
			<td class="description">specifies the bottomleft position</td>
		</tr>
    <tr>
			<td class="name">bottomcenter</td>			
			<td class="description">specifies the bottomcenter position</td>
		</tr>
    <tr>
			<td class="name">bottomright</td>			
			<td class="description">specifies the bottomright position</td>
		</tr>
	</tbody>
</table>

#### Default Value

* center

#### Example

{% highlight js %}
 
//To set labelPosition API value during initialization 
  $("#container").ejTreeMap({levels:[{ labelPosition: "center"]}});

{% endhighlight %}


{% highlight js %}
 
//Get or set the labelPosition API, after initialization:
   
   //Gets the labelPosition value 
   
   var property =$("#container").data("ejTreeMap").model.levels[0].labelPosition;
 
   //Sets the labelPosition value 
   
   $("#container").data("ejTreeMap").model.levels[0].labelPosition= "topleft"; 

{% endhighlight %}


### levels.labelTemplate `string`
{:#members:levels-labeltemplate}

Specifies the label template for tree map level.

#### Default Value

* null

#### Example

{% highlight js %}
  
// Set the labelTemplate during initialization.                         
   $("#container").ejTreeMap({levels: [{ labelTemplate:"template" }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the labelTemplate after initialization:

  //Gets the labelTemplate from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate;

  //Sets the labelTemplate to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate  = "template";

{% endhighlight %}


### levels.labelVisibilityMode `enum`
{:#members:levels-labelvisibilitymode}

<ts ref = "ej.datavisualization.TreeMap.VisibilityMode"/>

Specifies the mode of label visibility

<table class="params">
	<thead>
		<tr>
			<th>Name </th>			
			<th>Description</th>
		</tr>
	</thead>
	<tbody>
		<tr>
			<td class="visible">top</td>			
			<td class="description">specifies the visible mode</td>
		</tr>
    <tr>
			<td class="name">hide on exceeded length</td>			
			<td class="description">specifies the hide on exceeded length mode</td>
		</tr>
	</tbody>
</table>

#### Default Value

* visible

#### Example

{% highlight js %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({levels:[{ labelVisibilityMode: "visible"}]});

{% endhighlight %}


{% highlight js %}
 
//Get or set the labelVisibilityMode API, after initialization:
   
   //Gets the labelVisibilityMode value 
   
   var property =$("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode;
 
   //Sets the labelVisibilityMode value 
   
   $("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode= "visible"; 

{% endhighlight %}


### levels.showHeader `boolean`
{:#members:levels-showheader}

Shows or hides the header for tree map level.

#### Default Value

* false

#### Example

{% highlight js %}
  
// Set the shoeHeader during initialization.                    
   $("#container").ejTreeMap({levels: [{ showHeader:false }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the showHeader after initialization:

  //Gets the showHeader from treemap.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showHeader;

  //Sets the headerHeight to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].showHeader  = true;

{% endhighlight %}


### levels.showLabels `boolean`
{:#members:levels-showlabels}

Shows or hides the labels for tree map level.

#### Default Value

* false

#### Example

{% highlight js %}
  
// Set the showLabels during initialization.                    
   $("#container").ejTreeMap({levels: [{ showLabels:false }]})

{% endhighlight %}


{% highlight js %}
 
//Get or set the showLabels after initialization:

  //Gets the showLabels from map.

  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showLabels;

  //Sets the showLabels to map.

  $("#container").data("ejTreeMap").model.levels[levelIndex].showLabels  = false;

{% endhighlight %}


### weightValuePath `string`
{:#members:weightvaluepath}

Specifies the weight value path of the treemap

#### Default Value

* null

#### Example

{% highlight js %}
 
//To set weightValuePath API value during initialization 
  $("#container").ejTreeMap({weightValuePath:'TotalMedals'});

{% endhighlight %}


{% highlight js %}
 
//Get or set the weightValuePath API, after initialization:
   
   //Gets the weightValuePath value 
   
   var property =$("#container").data("ejTreeMap").model.weightValuePath;
 
   //Sets the weightValuePath value 
   
   $("#container").data("ejTreeMap").model.weightValuePath = 'TotalMedals'; 

{% endhighlight %}


## Methods

### refresh()
{:#methods:refresh}

Method to reload treemap with updated values.

#### Example

{% highlight js %}
 
//refresh method for treemap
   $("#container").ejTreeMap("refresh");
   
{% endhighlight %}



## Events

### treeMapItemSelected
{:#events:treemapitemselected}

Triggers on treemap item selected.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns selected treeMapItem object.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight js %}
 
//treemap item selected event for treemap
  $("#container").ejTreeMap({
   treeMapItemSelected: function () {}
  });

{% endhighlight %}
