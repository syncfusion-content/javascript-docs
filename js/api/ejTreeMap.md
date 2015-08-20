---
layout: post
title: ejTreeMap
documentation: API
platform: js
metaname: 
metacontent: 
---

The treemap can be easily configured to the DOM element, such as div and can be created with a highly customized look and feel.





$(element).ejTreeMap<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<div id="container"> 
 
<script>
// Create TreeMap
$('#container').ejTreeMap();    
</script> 
  
</div>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.datavisualization.TreeMap

* module:jsrender

* module:properties


## Members




### borderBrush<span class="type-signature type string">string</span>
{:#members:borderbrush}




Specifies the border brush color of the treemap


Default Value:
{:.param}



* "white"




Example
{:.example}


{% highlight html %}
 
//To set borderBrush API value during initialization 
  $("#container").ejTreeMap( {borderBrush:'white'});{% endhighlight %}


{% highlight html %}
 
//Get or set the borderBrush API, after initialization:
        //Gets the borderBrush value 
  var property =$("#container").data("ejTreeMap").model.borderBrush;
 
        //Sets the borderBrush value 
        $("#container").data("ejTreeMap").model.borderBrush = 'white'; {% endhighlight %}




### borderThickness<span class="type-signature type number">number</span>
{:#members:borderthickness}




Specifies the border thickness of the treemap


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
//To set borderThickness API value during initialization 
  $("#container").ejTreeMap({borderThickness:1});{% endhighlight %}


{% highlight html %}
 
//Get or set the borderThickness API, after initialization:
        //Gets the borderThickness value 
  var property =$("#container").data("ejTreeMap").model.borderThickness;
 
        //Sets the borderThickness value 
        $("#container").data("ejTreeMap").model.borderThickness = 1; {% endhighlight %}




### color<span class="type-signature type string">string</span>
{:#members:color}




Specifies the uniform color mapping of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set uniColorMapping API value during initialization 
  $("#container").ejTreeMap( {uniColorMapping{ color: null }});{% endhighlight %}


{% highlight html %}
 
//Get or set the uniColorMapping API, after initialization:
        //Gets the uniColorMapping value 
  var property =$("#container").data("ejTreeMap").model.uniColorMapping.color;
 
        //Sets the uniColorMapping value 
        $("#container").data("ejTreeMap").model.uniColorMapping = { color: null }; {% endhighlight %}




### color<span class="type-signature type string">string</span>
{:#members:color}




Specifies the color for desaturationColorMapping


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set color API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ color:"#41B8C4" }});{% endhighlight %}


{% highlight html %}
 
//Get or set the color API, after initialization:
        //Gets the color value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.color;
 
        //Sets the color for desaturationColorMapping value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { color:"#41B8C4" }; {% endhighlight %}




### color<span class="type-signature type string">string</span>
{:#members:color}




Specifies the color for desaturationColorMapping


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set color API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ color:"#41B8C4" }});{% endhighlight %}


{% highlight html %}
 
//Get or set the color API, after initialization:
        //Gets the color value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.color;
 
        //Sets the color for desaturationColorMapping value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { color:"#41B8C4" }; {% endhighlight %}




### color<span class="type-signature type string">string</span>
{:#members:color}




Specifies the uniform color mapping of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set uniColorMapping API value during initialization 
  $("#container").ejTreeMap( {uniColorMapping{ color: null }});{% endhighlight %}


{% highlight html %}
 
//Get or set the uniColorMapping API, after initialization:
        //Gets the uniColorMapping value 
  var property =$("#container").data("ejTreeMap").model.uniColorMapping.color;
 
        //Sets the uniColorMapping value 
        $("#container").data("ejTreeMap").model.uniColorMapping = { color: null }; {% endhighlight %}




### colors<span class="type-signature type data">data</span>
{:#members:colors}




Specifies the colors of the paletteColorMapping


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
 
//To set the colors of the paletteColorMapping during initialization 
  $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colors of the paletteColorMapping, after initialization:
        //Gets the colors of the paletteColorMapping value 
  var property =$("#container").data("ejTreeMap").model.paletteColorMapping;
 
        //Sets the the colors of the paletteColorMapping
        $("#container").data("ejTreeMap").model.paletteColorMapping = {colors: ["red","green","blue", "yellow"]}; {% endhighlight %}




### colors<span class="type-signature type data">data</span>
{:#members:colors}




Specifies the colors of the paletteColorMapping


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
 
//To set the colors of the paletteColorMapping during initialization 
  $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});{% endhighlight %}


{% highlight html %}
 
//Get or set the colors of the paletteColorMapping, after initialization:
        //Gets the colors of the paletteColorMapping value 
  var property =$("#container").data("ejTreeMap").model.paletteColorMapping;
 
        //Sets the the colors of the paletteColorMapping
        $("#container").data("ejTreeMap").model.paletteColorMapping = {colors: ["red","green","blue", "yellow"]}; {% endhighlight %}




### colorValuePath<span class="type-signature type string">string</span>
{:#members:colorvaluepath}




Specifies the color valuepath of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set colorValuePath API value during initialization 
  $("#container").ejTreeMap({colorValuePath:'GoldMedals'});{% endhighlight %}


{% highlight html %}
 
//Get or set the colorValuePath API, after initialization:
        //Gets the colorValuePath value 
  var property =$("#container").data("ejTreeMap").model.colorValuePath;
 
        //Sets the colorValuePath value 
        $("#container").data("ejTreeMap").model.colorValuePath = 'GoldMedals'; {% endhighlight %}




### dataSource<span class="type-signature type object">object</span>
{:#members:datasource}




Specifies the datasource of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set datasource API value during initialization 
  $("#container").ejTreeMap({datasource:medal_data});{% endhighlight %}


{% highlight html %}
 
//Get or set the datasource API, after initialization:
        //Gets the datasource value 
  var property =$("#container").data("ejTreeMap").model.datasource;
 
        //Sets the datasource value 
        $("#container").data("ejTreeMap").model.datasource = medal_data; {% endhighlight %}




### desaturationColorMapping<span class="type-signature type object">object</span>
{:#members:desaturationcolormapping}




Specifies the desaturationColorMapping settings of the treemap






### dockPosition<span class="type-signature type enum">enum</span>
{:#members:dockposition}




Specifies the dockPosition for legend


Default Value:
{:.param}



* top




Example
{:.example}


{% highlight html %}
 
//To set dockPosition API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ dockPosition: "top"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the dockPosition API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.dockPosition;
 
        //Sets the dockPosition value 
        $("#container").data("ejTreeMap").model.legendSettings = { dockPosition: "top"}; {% endhighlight %}




### drillDownHeaderColor<span class="type-signature type string">string</span>
{:#members:drilldownheadercolor}




specifies the drillDown header color


Default Value:
{:.param}



* 'null'




Example
{:.example}


{% highlight html %}
  
// Set the drillDownHeaderColor during initialization.                  
        $("#container").ejTreeMap({drillDownHeaderColor:'#0478c3'});{% endhighlight %}


{% highlight html %}
 
//Get or set the drillDownHeaderColor API, after initialization:
        //Gets the drillDownHeaderColor value 
  var property =$("#container").data("ejTreeMap").model.drillDownHeaderColor;
 
        //Sets the drillDownHeaderColor value 
        $("#container").data("ejTreeMap").model.drillDownHeaderColor = '#0478c3'; {% endhighlight %}




### drillDownSelectionColor<span class="type-signature type string">string</span>
{:#members:drilldownselectioncolor}




specifies the drillDown selection color


Default Value:
{:.param}



* '#000000'




Example
{:.example}


{% highlight html %}
  
// Set the drillDownSelectionColor during initialization.                       
        $("#container").ejTreeMap({drillDownSelectionColor:'#e5e5e5'});{% endhighlight %}


{% highlight html %}
 
//Get or set the drillDownSelectionColor API, after initialization:
        //Gets the drillDownSelectionColor value 
  var property =$("#container").data("ejTreeMap").model.drillDownSelectionColor;
 
        //Sets the drillDownSelectionColor value 
        $("#container").data("ejTreeMap").model.drillDownSelectionColor = '#000000'; {% endhighlight %}




### enableDrillDown<span class="type-signature type boolean">boolean</span>
{:#members:enabledrilldown}




Enable/Disable the drillDown for treemap


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set enableDrillDown API value during initialization 
  $("#container").ejTreeMap({enableDrillDown:true});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableDrillDown API, after initialization:
        //Gets the enableDrillDown value 
  var property =$("#container").data("ejTreeMap").model.enableDrillDown;
 
        //Sets the enableDrillDown value 
        $("#container").data("ejTreeMap").model.enableDrillDown = true; {% endhighlight %}




### enableResize<span class="type-signature type boolean">boolean</span>
{:#members:enableresize}




Specifies whether treemap need to resize when container is resized


Default Value:
{:.param}



* true




Example
{:.example}


{% highlight html %}
 
//To set enableResize API value during initialization 
  $("#container").ejTreeMap({enableResize:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the enableResize API, after initialization:
        //Gets the enableResize value 
  var property =$("#container").data("ejTreeMap").model.enableResize;
 
        //Sets the enableResize value 
        $("#container").data("ejTreeMap").model.enableResize = false; {% endhighlight %}




### from<span class="type-signature type number">number</span>
{:#members:from}




Specifies the from value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set from API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ from:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the from API, after initialization:
        //Gets the from value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.from;
 
        //Sets the from value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { from:1}; {% endhighlight %}




### from<span class="type-signature type number">number</span>
{:#members:from}




Specifies the from value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set from API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ from:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the from API, after initialization:
        //Gets the from value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.from;
 
        //Sets the from value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { from:1}; {% endhighlight %}




### groupColorMapping<span class="type-signature type treemapgroupcolormapping">TreeMapGroupColorMapping</span>
{:#members:groupcolormapping}




Specifies the group color mapping of the treemap


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
 
//To set groupColorMapping API value during initialization 
  $("#container").ejTreeMap( {groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}]}] });{% endhighlight %}


{% highlight html %}
 
//Get or set the groupColorMapping API, after initialization:
        //Gets the groupColorMapping value 
  var property =$("#container").data("ejTreeMap").model.groupColorMapping;
 
        //Sets the groupColorMapping value 
        $("#container").data("ejTreeMap").model.groupColorMapping = [groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}] }]});{% endhighlight %}




### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height for legend


Default Value:
{:.param}



* 30




Example
{:.example}


{% highlight html %}
 
//To set height API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ height: 15}});{% endhighlight %}


{% highlight html %}
 
//Get or set the height API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.height;
 
        //Sets the height value 
        $("#container").data("ejTreeMap").model.legendSettings = { height: 30}; {% endhighlight %}




### highlightBorderBrush<span class="type-signature type string">string</span>
{:#members:highlightborderbrush}




Specifies the highlight border brush of treemap


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
//To set highlightBorderBrush API value during initialization 
  $("#container").ejTreeMap({highlightBorderBrush:'gray'});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightBorderBrush API, after initialization:
        //Gets the highlightBorderBrush value 
  var property =$("#container").data("ejTreeMap").model.highlightBorderBrush;
 
        //Sets the highlightBorderBrush value 
        $("#container").data("ejTreeMap").model.highlightBorderBrush = 'gray'; {% endhighlight %}




### highlightBorderThickness<span class="type-signature type number">number</span>
{:#members:highlightborderthickness}




Specifies the border thickness when treemap items is highlighted in the treemap


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
//To set highlightBorderThickness API value during initialization 
  $("#container").ejTreeMap({highlightBorderThickness:5});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightBorderThickness API, after initialization:
        //Gets the highlightBorderThickness value 
  var property =$("#container").data("ejTreeMap").model.highlightBorderThickness;
 
        //Sets the highlightBorderThickness value 
        $("#container").data("ejTreeMap").model.highlightBorderThickness = 5; {% endhighlight %}




### highlightGroupBorderBrush<span class="type-signature type string">string</span>
{:#members:highlightgroupborderbrush}




Specifies the highlight border brush of treemap


Default Value:
{:.param}



* "gray"




Example
{:.example}


{% highlight html %}
 
//To set highlightGroupBorderBrush API value during initialization 
  $("#container").ejTreeMap({highlightGroupBorderBrush:'gray'});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightGroupBorderBrush API, after initialization:
        //Gets the highlightGroupBorderBrush value 
  var property =$("#container").data("ejTreeMap").model.highlightGroupBorderBrush;
 
        //Sets the highlightGroupBorderBrush value 
        $("#container").data("ejTreeMap").model.highlightGroupBorderBrush = 'gray'; {% endhighlight %}




### highlightGroupBorderThickness<span class="type-signature type number">number</span>
{:#members:highlightgroupborderthickness}




Specifies the border thickness when treemap items is highlighted in the treemap


Default Value:
{:.param}



* 5




Example
{:.example}


{% highlight html %}
 
//To set highlightGroupBorderThickness API value during initialization 
  $("#container").ejTreeMap({highlightGroupBorderThickness:5});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightGroupBorderThickness API, after initialization:
        //Gets the highlightGroupBorderThickness value 
  var property =$("#container").data("ejTreeMap").model.highlightGroupBorderThickness;
 
        //Sets the highlightGroupBorderThickness value 
        $("#container").data("ejTreeMap").model.highlightGroupBorderThickness = 5; {% endhighlight %}




### highlightGroupOnSelection<span class="type-signature type boolean">boolean</span>
{:#members:highlightgrouponselection}




Specifies whether treemap item need to highlighted on selection


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set highlightGroupOnSelection API value during initialization 
  $("#container").ejTreeMap({highlightGroupOnSelection:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightGroupOnSelection API, after initialization:
        //Gets the highlightGroupOnSelection value 
  var property =$("#container").data("ejTreeMap").model.highlightGroupOnSelection;
 
        //Sets the highlightGroupOnSelection value 
        $("#container").data("ejTreeMap").model.highlightGroupOnSelection = false; {% endhighlight %}




### highlightOnSelection<span class="type-signature type boolean">boolean</span>
{:#members:highlightonselection}




Specifies whether treemap item need to highlighted on selection


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set highlightOnSelection API value during initialization 
  $("#container").ejTreeMap({highlightOnSelection:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the highlightOnSelection API, after initialization:
        //Gets the highlightOnSelection value 
  var property =$("#container").data("ejTreeMap").model.highlightOnSelection;
 
        //Sets the highlightOnSelection value 
        $("#container").data("ejTreeMap").model.highlightOnSelection = false; {% endhighlight %}




### iconHeight<span class="type-signature type number">number</span>
{:#members:iconheight}




Specifies the iconHeight for legend


Default Value:
{:.param}



* 15




Example
{:.example}


{% highlight html %}
 
//To set iconHeight API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ iconHeight: 15}});{% endhighlight %}


{% highlight html %}
 
//Get or set the iconHeight API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.iconHeight;
 
        //Sets the iconHeight value 
        $("#container").data("ejTreeMap").model.legendSettings = { iconHeight: 15}; {% endhighlight %}




### iconWidth<span class="type-signature type number">number</span>
{:#members:iconwidth}




Specifies the iconWidth for legend


Default Value:
{:.param}



* 15




Example
{:.example}


{% highlight html %}
 
//To set iconWidth API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ iconWidth: 15}});{% endhighlight %}


{% highlight html %}
 
//Get or set the iconWidth API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.iconWidth;
 
        //Sets the iconWidth value 
        $("#container").data("ejTreeMap").model.legendSettings = { iconWidth: 15}; {% endhighlight %}




### itemsLayoutMode<span class="type-signature type enum">enum</span>
{:#members:itemslayoutmode}




Specifies the items layout mode of the treemap. Accepted itemsLayoutMode values are Squarified, SliceAndDiceHorizontal, SliceAndDiceVertical and SliceAndDiceAuto


Default Value:
{:.param}



* "Squarified"




Example
{:.example}


{% highlight html %}
 
//To set itemsLayoutMode API value during initialization 
  $("#container").ejTreeMap({itemsLayoutMode:ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified});{% endhighlight %}


{% highlight html %}
 
//Get or set the itemsLayoutMode API, after initialization:
        //Gets the itemsLayoutMode value 
  var property =$("#container").data("ejTreeMap").model.itemsLayoutMode;
 
        //Sets the itemsLayoutMode value 
        $("#container").data("ejTreeMap").model.itemsLayoutMode = ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified; {% endhighlight %}




### leafItemSettings<span class="type-signature type object">object</span>
{:#members:leafitemsettings}




Specifies the leaf settings of the treemap






### leafItemSettings.borderBrush<span class="type-signature type string">string</span>
{:#members:leafitemsettings-borderbrush}




Specifies the border bruch color of the leaf item.


Default Value:
{:.param}



* "white"




Example
{:.example}


{% highlight html %}
 
//To set borderBrush API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ borderBrush: "white"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the borderBrush API, after initialization:
        //Gets the borderBrush value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderBrush;
 
        //Sets the borderBrush value 
        $("#container").data("ejTreeMap").model.leafItemSettings = { borderBrush: "white"}; {% endhighlight %}




### leafItemSettings.borderThickness<span class="type-signature type number">number</span>
{:#members:leafitemsettings-borderthickness}




Specifies the border thickness of the leaf item.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
 
//To set borderThickness API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ borderThickness: 1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the borderThickness API, after initialization:
        //Gets the borderThickness value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderThickness;
 
        //Sets the borderThickness value 
        $("#container").data("ejTreeMap").model.leafItemSettings = { borderThickness: 1}; {% endhighlight %}




### leafItemSettings.itemTemplate<span class="type-signature type string">string</span>
{:#members:leafitemsettings-itemtemplate}




Specifies the label template of the leaf item.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set itemTemplate API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ itemTemplate: "temp"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the itemTemplate API, after initialization:
        //Gets the itemTemplate value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.itemTemplate;
 
        //Sets the itemTemplate value 
        $("#container").data("ejTreeMap").model.leafItemSettings = { itemTemplate: "temp"}; {% endhighlight %}




### leafItemSettings.labelPath<span class="type-signature type string">string</span>
{:#members:leafitemsettings-labelpath}




Specifies the label path of the leaf item.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set labelPath API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelPath: "GameName"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the labelPath API, after initialization:
        //Gets the labelPath value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPath;
 
        //Sets the labelPath value 
        $("#container").data("ejTreeMap").model.leafItemSettings = { labelPath: "GameName"}; {% endhighlight %}




### leafItemSettings.labelPosition<span class="type-signature type enum">enum</span>
{:#members:leafitemsettings-labelposition}




Specifies the position of the leaf labels.


Default Value:
{:.param}



* center




Example
{:.example}


{% highlight html %}
 
//To set labelPosition API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelPosition: "center"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the labelPosition API, after initialization:
        //Gets the labelPosition value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPosition;
 
        //Sets the labelPosition value 
        $("#container").data("ejTreeMap").model.leafItemSettings.labelPosition= "topleft"; {% endhighlight %}




### leafItemSettings.labelVisibilityMode<span class="type-signature type enum">enum</span>
{:#members:leafitemsettings-labelvisibilitymode}




Specifies the mode of label visibility


Default Value:
{:.param}



* visible




Example
{:.example}


{% highlight html %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ labelVisibilityMode: "visible"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the labelVisibilityMode API, after initialization:
        //Gets the labelVisibilityMode value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode;
 
        //Sets the labelVisibilityMode value 
        $("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode= "visible"; {% endhighlight %}




### leafItemSettings.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:leafitemsettings-showlabels}




Shows or hides the label of the leaf item.


Default Value:
{:.param}



* "false"




Example
{:.example}


{% highlight html %}
 
//To set showLabels API value during initialization 
  $("#container").ejTreeMap({leafItemSettings:{ showLabels: "false"}});{% endhighlight %}


{% highlight html %}
 
//Get or set the showLabels API, after initialization:
        //Gets the showLabels value 
  var property =$("#container").data("ejTreeMap").model.leafItemSettings.showLabels;
 
        //Sets the showLabels value 
        $("#container").data("ejTreeMap").model.leafItemSettings = { showLabels: "false"}; {% endhighlight %}




### legendSettings<span class="type-signature type object">object</span>
{:#members:legendsettings}




Specifies the legend settings of the treemap






### levels<span class="type-signature type treemaplevel">treeMapLevel</span>
{:#members:levels}




Specify levels of treemap for grouped visualization of datas


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
  
// Set the levels during initialization.                
  $("#container").ejTreeMap({   levels: [{ groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the levels after initialization:
  //Gets the levels from map.
  var levels =$("#container").data("ejTreeMap").model.levels[levelIndex];
  //Sets the levels to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex]  = { groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' };{% endhighlight %}




### paletteColorMapping<span class="type-signature type object">object</span>
{:#members:palettecolormapping}




Specifies the paletteColorMapping of the treemap






### rangeColorMapping<span class="type-signature type treemaprangecolormapping">TreeMapRangeColorMapping</span>
{:#members:rangecolormapping}




Specifies the rangeColorMapping settings of the treemap



Example
{:.example}


{% highlight html %}
 
//To set rangeColorMapping API value during initialization 
  $("#container").ejTreeMap( {rangeColorMapping:[{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]});{% endhighlight %}


{% highlight html %}
 
//Get or set the rangeColorMapping API, after initialization:
        //Gets the rangeColorMapping value 
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping;
 
        //Sets the rangeColorMapping value 
        $("#container").data("ejTreeMap").model.rangeColorMapping = [{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]; {% endhighlight %}




### rangeMaximum<span class="type-signature type number">number</span>
{:#members:rangemaximum}




Specifies the rangeMaximum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set rangeMaximum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMaximum:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the rangeMaximum API, after initialization:
        //Gets the rangeMaximum value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMaximum;
 
        //Sets the rangeMaximum value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMaximum:1}; {% endhighlight %}




### rangeMaximum<span class="type-signature type number">number</span>
{:#members:rangemaximum}




Specifies the rangeMaximum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set rangeMaximum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMaximum:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the rangeMaximum API, after initialization:
        //Gets the rangeMaximum value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMaximum;
 
        //Sets the rangeMaximum value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMaximum:1}; {% endhighlight %}




### rangeMinimum<span class="type-signature type number">number</span>
{:#members:rangeminimum}




Specifies the rangeMinimum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set rangeMinimum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMinimum:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the rangeMinimum API, after initialization:
        //Gets the rangeMinimum value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMinimum;
 
        //Sets the rangeMinimum value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMinimum:1}; {% endhighlight %}




### rangeMinimum<span class="type-signature type number">number</span>
{:#members:rangeminimum}




Specifies the rangeMinimum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set rangeMinimum API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ rangeMinimum:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the rangeMinimum API, after initialization:
        //Gets the rangeMinimum value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMinimum;
 
        //Sets the rangeMinimum value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMinimum:1}; {% endhighlight %}




### shapeLayer.groupSelectionMode<span class="type-signature type enum">enum</span>
{:#members:shapelayer-groupselectionmode}




Specifies the selection mode of the treemap. Accepted selection mode values are Default and Multiple.


Default Value:
{:.param}



* "default"




Example
{:.example}


{% highlight html %}
  
// Set the selection mode during initialization.                        
        $("#container").ejTreeMap({layers: [{ selectionMode:'default' }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupSelection mode after initialization:
  //Gets the selection mode from treemap.
  var property =$("#container").data("ejTreeMap").model.layers[layerIndex].groupSelectionMode;
  //Sets the selection mode to treemap.
  $("#container").data("ejTreeMap").model.layers[layerIndex].groupSelectionMode  = 'default';{% endhighlight %}




### showLegend<span class="type-signature type boolean">boolean</span>
{:#members:showlegend}




Specifies the legend visibility status of the treemap


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set showLegend API value during initialization 
  $("#container").ejTreeMap({showLegend:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the showLegend API, after initialization:
        //Gets the showLegend value 
  var property =$("#container").data("ejTreeMap").model.showLegend;
 
        //Sets the showLegend value 
        $("#container").data("ejTreeMap").model.showLegend = false; {% endhighlight %}




### showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showtooltip}




Specifies whether treemap tooltip need to be visible


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
 
//To set showTooltip API value during initialization 
  $("#container").ejTreeMap({showTooltip:false});{% endhighlight %}


{% highlight html %}
 
//Get or set the showTooltip API, after initialization:
        //Gets the showTooltip value 
  var property =$("#container").data("ejTreeMap").model.showTooltip;
 
        //Sets the showTooltip value 
        $("#container").data("ejTreeMap").model.showTooltip = false; {% endhighlight %}




### template<span class="type-signature type string">string</span>
{:#members:template}




Specifies the template for legendSettings


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set template API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ template: null}});{% endhighlight %}


{% highlight html %}
 
//Get or set the template API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.template;
 
        //Sets the template value 
        $("#container").data("ejTreeMap").model.legendSettings = { template: null}; {% endhighlight %}




### to<span class="type-signature type number">number</span>
{:#members:to}




Specifies the to value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set to API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ to:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the to API, after initialization:
        //Gets the to value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.to;
 
        //Sets the to value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { to:1}; {% endhighlight %}




### to<span class="type-signature type number">number</span>
{:#members:to}




Specifies the to value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
 
//To set to API value during initialization 
  $("#container").ejTreeMap( {desaturationColorMapping{ to:1}});{% endhighlight %}


{% highlight html %}
 
//Get or set the to API, after initialization:
        //Gets the to value 
  var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.to;
 
        //Sets the to value 
        $("#container").data("ejTreeMap").model.desaturationColorMapping = { to:1}; {% endhighlight %}




### tooltipTemplate<span class="type-signature type string">string</span>
{:#members:tooltiptemplate}




Specifies the tooltip template of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set tooltipTemplate API value during initialization 
  $("#container").ejTreeMap({tooltipTemplate:'template'});{% endhighlight %}


{% highlight html %}
 
//Get or set the tooltipTemplate API, after initialization:
        //Gets the tooltipTemplate value 
  var property =$("#container").data("ejTreeMap").model.tooltipTemplate;
 
        //Sets the tooltipTemplate value 
        $("#container").data("ejTreeMap").model.tooltipTemplate = 'template'; {% endhighlight %}




### TreeMapGroupColorMapping.groupID<span class="type-signature type string">string</span>
{:#members:treemapgroupcolormapping-groupid}




Specifies the groupID for GroupColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the groupID for GroupColorMapping during initialization.                         
        $("#container").ejTreeMap({groupColorMapping: [{ groupID:"Asia" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupID for GroupColorMapping after initialization:
  //Gets the groupID for GroupColorMapping from map.
  var property =$("#container").data("ejTreeMap").model.groupColorMapping.groupID;
  //Sets the groupID for GroupColorMapping to map.
  $("#container").data("ejTreeMap").model.groupColorMapping.groupID  = "Asia";{% endhighlight %}




### treeMapItems<span class="type-signature type treemapitem">TreeMapItem</span>
{:#members:treemapitems}




Hold the treeMapItems to be displayed in treemap


Default Value:
{:.param}



* []




Example
{:.example}


{% highlight html %}
  
// Set the treeMapItems during initialization. 
  $("#container").ejTreeMap({treeMapItems:[]});                             {% endhighlight %}


{% highlight html %}
 
//Get or set the treeMapItems after initialization:
  //Gets the treeMapItems from treemap.
  var property =$("#container").data("ejTreeMap").model.treeMapItems;
             
  //Sets the treeMapItems to treemap.
        $("#container").data("ejTreeMap").model.treeMapItems = []; {% endhighlight %}




### treeMapLevel
{:#members:treemaplevel}




Hold the Level settings of TreeMap






### treeMapLevel.groupBackground<span class="type-signature type string">string</span>
{:#members:treemaplevel-groupbackground}




specifies the group background


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the groupBackground during initialization.                       
        $("#container").ejTreeMap({levels: [{ groupBackground:"white" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupBackground after initialization:
  //Gets the groupBackground from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground;
  //Sets the groupBackground to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground  = "white";{% endhighlight %}




### treeMapLevel.groupBorderColor<span class="type-signature type string">string</span>
{:#members:treemaplevel-groupbordercolor}




Specifies the group border color for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the groupBorderColor during initialization.                      
        $("#container").ejTreeMap({levels: [{ groupBorderColor:"#58585B" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupBorderColor after initialization:
  //Gets the groupBorderColor from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor;
  //Sets the groupBorderColor to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor  = "#58585B";{% endhighlight %}




### treeMapLevel.groupBorderThickness<span class="type-signature type number">number</span>
{:#members:treemaplevel-groupborderthickness}




Specifies the group border thickness for tree map level.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
  
// Set the groupBorderThickness during initialization.                  
        $("#container").ejTreeMap({levels: [{ groupBorderThickness:1 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupBorderThickness after initialization:
  //Gets the groupBorderThickness from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness;
  //Sets the groupBorderThickness to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness  = 1;{% endhighlight %}




### treeMapLevel.groupGap<span class="type-signature type number">number</span>
{:#members:treemaplevel-groupgap}




Specifies the group gap for tree map level.


Default Value:
{:.param}



* 1




Example
{:.example}


{% highlight html %}
  
// Set the groupGap during initialization.                      
        $("#container").ejTreeMap({levels: [{ groupGap:1 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupGap after initialization:
  //Gets the groupGap from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupGap;
  //Sets the groupGap to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupGap  = 1;{% endhighlight %}




### treeMapLevel.groupPadding<span class="type-signature type number">number</span>
{:#members:treemaplevel-grouppadding}




Specifies the group padding for tree map level.


Default Value:
{:.param}



* 4




Example
{:.example}


{% highlight html %}
  
// Set the groupPadding during initialization.                  
        $("#container").ejTreeMap({levels: [{ groupPadding:4 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupPadding after initialization:
  //Gets the groupPadding from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding;
  //Sets the groupPadding to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding  = 4;{% endhighlight %}




### treeMapLevel.groupPath<span class="type-signature type string">string</span>
{:#members:treemaplevel-grouppath}




Specifies the group path for tree map level.



Example
{:.example}


{% highlight html %}
  
// Set the groupPath during initialization.                     
        $("#container").ejTreeMap({levels: [{ groupPath:"pathName" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the groupPath after initialization:
  //Gets the groupPath from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPath;
  //Sets the groupPath to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPath  = "pathName";{% endhighlight %}




### treeMapLevel.headerHeight<span class="type-signature type number">number</span>
{:#members:treemaplevel-headerheight}




Specifies the header height for tree map level.


Default Value:
{:.param}



* 0




Example
{:.example}


{% highlight html %}
  
// Set the headerHeight during initialization.                  
        $("#container").ejTreeMap({levels: [{ headerHeight:20 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the headerHeight after initialization:
  //Gets the headerHeight from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight;
  //Sets the headerHeight to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight  = 1;{% endhighlight %}




### treeMapLevel.headerTemplate<span class="type-signature type string">string</span>
{:#members:treemaplevel-headertemplate}




Specifies the header template for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the headerTemplate during initialization.                        
        $("#container").ejTreeMap({levels: [{ headerTemplate:"template" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the headerTemplate after initialization:
  //Gets the headerTemplate from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate;
  //Sets the headerTemplate to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate  = "template";{% endhighlight %}




### treeMapLevel.headerVisibilityMode<span class="type-signature type enum">enum</span>
{:#members:treemaplevel-headervisibilitymode}




Specifies the mode of header visibility


Default Value:
{:.param}



* visible




Example
{:.example}


{% highlight html %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({levels:[{ headerVisibilityMode: "visible"}]});{% endhighlight %}


{% highlight html %}
 
//Get or set the headerVisibilityMode API, after initialization:
        //Gets the headerVisibilityMode value 
  var property =$("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode;
 
        //Sets the headerVisibilityMode value 
        $("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode= "visible"; {% endhighlight %}




### treeMapLevel.labelPosition<span class="type-signature type enum">enum</span>
{:#members:treemaplevel-labelposition}




Specifies the position of the labels.


Default Value:
{:.param}



* center




Example
{:.example}


{% highlight html %}
 
//To set labelPosition API value during initialization 
  $("#container").ejTreeMap({levels:[{ labelPosition: "center"]}});{% endhighlight %}


{% highlight html %}
 
//Get or set the labelPosition API, after initialization:
        //Gets the labelPosition value 
  var property =$("#container").data("ejTreeMap").model.levels[0].labelPosition;
 
        //Sets the labelPosition value 
        $("#container").data("ejTreeMap").model.levels[0].labelPosition= "topleft"; {% endhighlight %}




### treeMapLevel.labelTemplate<span class="type-signature type string">string</span>
{:#members:treemaplevel-labeltemplate}




Specifies the label template for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the labelTemplate during initialization.                         
        $("#container").ejTreeMap({levels: [{ labelTemplate:"template" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the labelTemplate after initialization:
  //Gets the labelTemplate from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate;
  //Sets the labelTemplate to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate  = "template";{% endhighlight %}




### treeMapLevel.labelVisibilityMode<span class="type-signature type enum">enum</span>
{:#members:treemaplevel-labelvisibilitymode}




Specifies the mode of label visibility


Default Value:
{:.param}



* visible




Example
{:.example}


{% highlight html %}
 
//To set labelVisibilityMode API value during initialization 
  $("#container").ejTreeMap({levels:[{ labelVisibilityMode: "visible"}]});{% endhighlight %}


{% highlight html %}
 
//Get or set the labelVisibilityMode API, after initialization:
        //Gets the labelVisibilityMode value 
  var property =$("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode;
 
        //Sets the labelVisibilityMode value 
        $("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode= "visible"; {% endhighlight %}




### treeMapLevel.showHeader<span class="type-signature type bool">bool</span>
{:#members:treemaplevel-showheader}




Shows or hides the header for tree map level.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
  
// Set the shoeHeader during initialization.                    
        $("#container").ejTreeMap({levels: [{ showHeader:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showHeader after initialization:
  //Gets the showHeader from treemap.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showHeader;
  //Sets the headerHeight to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].showHeader  = true;{% endhighlight %}




### treeMapLevel.showLabels<span class="type-signature type boolean">boolean</span>
{:#members:treemaplevel-showlabels}




Shows or hides the labels for tree map level.


Default Value:
{:.param}



* false




Example
{:.example}


{% highlight html %}
  
// Set the showLabels during initialization.                    
        $("#container").ejTreeMap({levels: [{ showLabels:false }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the showLabels after initialization:
  //Gets the showLabels from map.
  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showLabels;
  //Sets the showLabels to map.
  $("#container").data("ejTreeMap").model.levels[levelIndex].showLabels  = false;{% endhighlight %}




### treeMapRangeColorMapping.color<span class="type-signature type string">string</span>
{:#members:treemaprangecolormapping-color}




Specifies the color value for rangeColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the color value for rangeColorMapping during initialization.                     
        $("#container").ejTreeMap({rangeColorMapping: [{ color: "#77D8D8" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the color value for rangeColorMapping after initialization:
  //Gets the color value for rangeColorMapping from map.
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.color;
  //Sets the color value for rangeColorMapping to map.
  $("#container").data("ejTreeMap").model.rangeColorMapping.color  = "#77D8D8";{% endhighlight %}




### treeMapRangeColorMapping.from<span class="type-signature type number">number</span>
{:#members:treemaprangecolormapping-from}




Specifies the from value for rangeColorMapping.


Default Value:
{:.param}



* -1




Example
{:.example}


{% highlight html %}
  
// Set the from value for rangeColorMapping during initialization.                      
        $("#container").ejTreeMap({rangeColorMapping: [{ from:-1 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the from value for rangeColorMapping after initialization:
  //Gets the from value for rangeColorMapping from map.
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.from;
  //Sets the from value for rangeColorMapping to map.
  $("#container").data("ejTreeMap").model.rangeColorMapping.from  = -1;{% endhighlight %}




### treeMapRangeColorMapping.legendlabel<span class="type-signature type string">string</span>
{:#members:treemaprangecolormapping-legendlabel}




Specifies the legendlabel value for rangeColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
  
// Set the legendlabel value for rangeColorMapping during initialization.                       
        $("#container").ejTreeMap({rangeColorMapping: [{ legendlabel: "1% Growth" }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the legendlabel value for rangeColorMapping after initialization:
  //Gets the legendlabel value for rangeColorMapping from map.
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel;
  //Sets the legendlabel value for rangeColorMapping to map.
  $("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel  = "1% Growth";{% endhighlight %}




### treeMapRangeColorMapping.to<span class="type-signature type number">number</span>
{:#members:treemaprangecolormapping-to}




Specifies the to value for rangeColorMapping.


Default Value:
{:.param}



* -1




Example
{:.example}


{% highlight html %}
  
// Set the to value for rangeColorMapping during initialization.                        
        $("#container").ejTreeMap({rangeColorMapping: [{ to:-1 }]}){% endhighlight %}


{% highlight html %}
 
//Get or set the to value for rangeColorMapping after initialization:
  //Gets the to value for rangeColorMapping from map.
  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.to;
  //Sets the to value for rangeColorMapping to map.
  $("#container").data("ejTreeMap").model.rangeColorMapping.to  = -1;{% endhighlight %}




### uniColorMapping<span class="type-signature type object">object</span>
{:#members:unicolormapping}




Specifies the uniColorMapping settings of the treemap






### weightValuePath<span class="type-signature type string">string</span>
{:#members:weightvaluepath}




Specifies the weight valuepath of the treemap


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set weightValuePath API value during initialization 
  $("#container").ejTreeMap({weightValuePath:'TotalMedals'});{% endhighlight %}


{% highlight html %}
 
//Get or set the weightValuePath API, after initialization:
        //Gets the weightValuePath value 
  var property =$("#container").data("ejTreeMap").model.weightValuePath;
 
        //Sets the weightValuePath value 
        $("#container").data("ejTreeMap").model.weightValuePath = 'TotalMedals'; {% endhighlight %}




### width<span class="type-signature type number">number</span>
{:#members:width}




Specifies the width for legend


Default Value:
{:.param}



* 100




Example
{:.example}


{% highlight html %}
 
//To set width API value during initialization 
  $("#container").ejTreeMap( {legendSettings:{ width: 100}});{% endhighlight %}


{% highlight html %}
 
//Get or set the width API, after initialization:
        //Gets the template value 
  var property =$("#container").data("ejTreeMap").model.legendSettings.width;
 
        //Sets the width value 
        $("#container").data("ejTreeMap").model.legendSettings = { width: 100}; {% endhighlight %}



## Methods




### refresh<span class="signature">()</span>
{:#methods:refresh}




Method to reload treemap with updated values.



Example
{:.example}


{% highlight html %}
 
//refresh method for treemap
$("#container").ejTreeMap("refresh");{% endhighlight %}



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
<td class="name">{% highlight html %}
originalEvent.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">Returns selected treeMapItem object.</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
//treemap item selected event for treemap
$("#container").ejTreeMap({
   treeMapItemSelected: function () {}
});{% endhighlight %}



