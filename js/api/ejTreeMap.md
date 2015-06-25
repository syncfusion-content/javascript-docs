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
<pre class="prettyprint"><code> &lt;div id="container"&gt; 
 &lt;script&gt;// Create TreeMap$('#container').ejTreeMap();    &lt;/script&gt; 
  &lt;/div&gt;</code></pre>



Requires
{:.require}


* module:jQuery

* module:ej.datavisualization.TreeMap

* module:jsrender

* module:properties


## Members




### borderBrush<span class="type-signature type string">string</span>




Specifies the border brush color of the treemap


Default Value:
{:.param}



* "white"




Example
{:.example}
<pre class="prettyprint"><code> //To set borderBrush API value during initialization   $("#container").ejTreeMap( {borderBrush:'white'});</code></pre><pre class="prettyprint"><code> //Get or set the borderBrush API, after initialization:
        //Gets the borderBrush value   var property =$("#container").data("ejTreeMap").model.borderBrush;
         //Sets the borderBrush value         $("#container").data("ejTreeMap").model.borderBrush = 'white'; </code></pre>



### borderThickness<span class="type-signature type number">number</span>




Specifies the border thickness of the treemap


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code> //To set borderThickness API value during initialization   $("#container").ejTreeMap({borderThickness:1});</code></pre><pre class="prettyprint"><code> //Get or set the borderThickness API, after initialization:
        //Gets the borderThickness value   var property =$("#container").data("ejTreeMap").model.borderThickness;
         //Sets the borderThickness value         $("#container").data("ejTreeMap").model.borderThickness = 1; </code></pre>



### color<span class="type-signature type string">string</span>




Specifies the uniform color mapping of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set uniColorMapping API value during initialization   $("#container").ejTreeMap( {uniColorMapping{ color: null }});</code></pre><pre class="prettyprint"><code> //Get or set the uniColorMapping API, after initialization:
        //Gets the uniColorMapping value   var property =$("#container").data("ejTreeMap").model.uniColorMapping.color;
         //Sets the uniColorMapping value         $("#container").data("ejTreeMap").model.uniColorMapping = { color: null }; </code></pre>



### color<span class="type-signature type string">string</span>




Specifies the color for desaturationColorMapping


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set color API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ color:"#41B8C4" }});</code></pre><pre class="prettyprint"><code> //Get or set the color API, after initialization:
        //Gets the color value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.color;
         //Sets the color for desaturationColorMapping value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { color:"#41B8C4" }; </code></pre>



### color<span class="type-signature type string">string</span>




Specifies the color for desaturationColorMapping


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set color API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ color:"#41B8C4" }});</code></pre><pre class="prettyprint"><code> //Get or set the color API, after initialization:
        //Gets the color value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.color;
         //Sets the color for desaturationColorMapping value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { color:"#41B8C4" }; </code></pre>



### color<span class="type-signature type string">string</span>




Specifies the uniform color mapping of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set uniColorMapping API value during initialization   $("#container").ejTreeMap( {uniColorMapping{ color: null }});</code></pre><pre class="prettyprint"><code> //Get or set the uniColorMapping API, after initialization:
        //Gets the uniColorMapping value   var property =$("#container").data("ejTreeMap").model.uniColorMapping.color;
         //Sets the uniColorMapping value         $("#container").data("ejTreeMap").model.uniColorMapping = { color: null }; </code></pre>



### colors<span class="type-signature type data">data</span>




Specifies the colors of the paletteColorMapping


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code> //To set the colors of the paletteColorMapping during initialization   $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});</code></pre><pre class="prettyprint"><code> //Get or set the colors of the paletteColorMapping, after initialization:
        //Gets the colors of the paletteColorMapping value   var property =$("#container").data("ejTreeMap").model.paletteColorMapping;
         //Sets the the colors of the paletteColorMapping        $("#container").data("ejTreeMap").model.paletteColorMapping = {colors: ["red","green","blue", "yellow"]}; </code></pre>



### colors<span class="type-signature type data">data</span>




Specifies the colors of the paletteColorMapping


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code> //To set the colors of the paletteColorMapping during initialization   $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});</code></pre><pre class="prettyprint"><code> //Get or set the colors of the paletteColorMapping, after initialization:
        //Gets the colors of the paletteColorMapping value   var property =$("#container").data("ejTreeMap").model.paletteColorMapping;
         //Sets the the colors of the paletteColorMapping        $("#container").data("ejTreeMap").model.paletteColorMapping = {colors: ["red","green","blue", "yellow"]}; </code></pre>



### colorValuePath<span class="type-signature type string">string</span>




Specifies the color valuepath of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set colorValuePath API value during initialization   $("#container").ejTreeMap({colorValuePath:'GoldMedals'});</code></pre><pre class="prettyprint"><code> //Get or set the colorValuePath API, after initialization:
        //Gets the colorValuePath value   var property =$("#container").data("ejTreeMap").model.colorValuePath;
         //Sets the colorValuePath value         $("#container").data("ejTreeMap").model.colorValuePath = 'GoldMedals'; </code></pre>



### dataSource<span class="type-signature type object">object</span>




Specifies the datasource of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set datasource API value during initialization   $("#container").ejTreeMap({datasource:medal_data});</code></pre><pre class="prettyprint"><code> //Get or set the datasource API, after initialization:
        //Gets the datasource value   var property =$("#container").data("ejTreeMap").model.datasource;
         //Sets the datasource value         $("#container").data("ejTreeMap").model.datasource = medal_data; </code></pre>



### desaturationColorMapping<span class="type-signature type object">object</span>




Specifies the desaturationColorMapping settings of the treemap






### dockPosition<span class="type-signature type enum">enum</span>




Specifies the dockPosition for legend


Default Value:
{:.param}



* top




Example
{:.example}
<pre class="prettyprint"><code> //To set dockPosition API value during initialization   $("#container").ejTreeMap( {legendSettings:{ dockPosition: "top"}});</code></pre><pre class="prettyprint"><code> //Get or set the dockPosition API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.dockPosition;
         //Sets the dockPosition value         $("#container").data("ejTreeMap").model.legendSettings = { dockPosition: "top"}; </code></pre>



### drillDownHeaderColor<span class="type-signature type string">string</span>




specifies the drillDown header color


Default Value:
{:.param}



* 'null'




Example
{:.example}
<pre class="prettyprint"><code>  // Set the drillDownHeaderColor during initialization.                          $("#container").ejTreeMap({drillDownHeaderColor:'#0478c3'});</code></pre><pre class="prettyprint"><code> //Get or set the drillDownHeaderColor API, after initialization:
        //Gets the drillDownHeaderColor value   var property =$("#container").data("ejTreeMap").model.drillDownHeaderColor;
         //Sets the drillDownHeaderColor value         $("#container").data("ejTreeMap").model.drillDownHeaderColor = '#0478c3'; </code></pre>



### drillDownSelectionColor<span class="type-signature type string">string</span>




specifies the drillDown selection color


Default Value:
{:.param}



* '#000000'




Example
{:.example}
<pre class="prettyprint"><code>  // Set the drillDownSelectionColor during initialization.                               $("#container").ejTreeMap({drillDownSelectionColor:'#e5e5e5'});</code></pre><pre class="prettyprint"><code> //Get or set the drillDownSelectionColor API, after initialization:
        //Gets the drillDownSelectionColor value   var property =$("#container").data("ejTreeMap").model.drillDownSelectionColor;
         //Sets the drillDownSelectionColor value         $("#container").data("ejTreeMap").model.drillDownSelectionColor = '#000000'; </code></pre>



### enableDrillDown<span class="type-signature type boolean">boolean</span>




Enable/Disable the drillDown for treemap


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //To set enableDrillDown API value during initialization   $("#container").ejTreeMap({enableDrillDown:true});</code></pre><pre class="prettyprint"><code> //Get or set the enableDrillDown API, after initialization:
        //Gets the enableDrillDown value   var property =$("#container").data("ejTreeMap").model.enableDrillDown;
         //Sets the enableDrillDown value         $("#container").data("ejTreeMap").model.enableDrillDown = true; </code></pre>



### enableResize<span class="type-signature type boolean">boolean</span>




Specifies whether treemap need to resize when container is resized


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //To set enableResize API value during initialization   $("#container").ejTreeMap({enableResize:false});</code></pre><pre class="prettyprint"><code> //Get or set the enableResize API, after initialization:
        //Gets the enableResize value   var property =$("#container").data("ejTreeMap").model.enableResize;
         //Sets the enableResize value         $("#container").data("ejTreeMap").model.enableResize = false; </code></pre>



### from<span class="type-signature type number">number</span>




Specifies the from value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set from API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ from:1}});</code></pre><pre class="prettyprint"><code> //Get or set the from API, after initialization:
        //Gets the from value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.from;
         //Sets the from value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { from:1}; </code></pre>



### from<span class="type-signature type number">number</span>




Specifies the from value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set from API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ from:1}});</code></pre><pre class="prettyprint"><code> //Get or set the from API, after initialization:
        //Gets the from value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.from;
         //Sets the from value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { from:1}; </code></pre>



### groupColorMapping<span class="type-signature type treemapgroupcolormapping">TreeMapGroupColorMapping</span>




Specifies the group color mapping of the treemap


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code> //To set groupColorMapping API value during initialization   $("#container").ejTreeMap( {groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}]}] });</code></pre><pre class="prettyprint"><code> //Get or set the groupColorMapping API, after initialization:
        //Gets the groupColorMapping value   var property =$("#container").data("ejTreeMap").model.groupColorMapping;
         //Sets the groupColorMapping value         $("#container").data("ejTreeMap").model.groupColorMapping = [groupColorMapping:[{ groupID: "Asia", rangeColorMapping:[{ color: "#77D8D8", from: "0", to: "1"}] }]});</code></pre>



### height<span class="type-signature type number">number</span>




Specifies the height for legend


Default Value:
{:.param}



* 30




Example
{:.example}
<pre class="prettyprint"><code> //To set height API value during initialization   $("#container").ejTreeMap( {legendSettings:{ height: 15}});</code></pre><pre class="prettyprint"><code> //Get or set the height API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.height;
         //Sets the height value         $("#container").data("ejTreeMap").model.legendSettings = { height: 30}; </code></pre>



### highlightBorderBrush<span class="type-signature type string">string</span>




Specifies the highlight border brush of treemap


Default Value:
{:.param}



* "gray"




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightBorderBrush API value during initialization   $("#container").ejTreeMap({highlightBorderBrush:'gray'});</code></pre><pre class="prettyprint"><code> //Get or set the highlightBorderBrush API, after initialization:
        //Gets the highlightBorderBrush value   var property =$("#container").data("ejTreeMap").model.highlightBorderBrush;
         //Sets the highlightBorderBrush value         $("#container").data("ejTreeMap").model.highlightBorderBrush = 'gray'; </code></pre>



### highlightBorderThickness<span class="type-signature type number">number</span>




Specifies the border thickness when treemap items is highlighted in the treemap


Default Value:
{:.param}



* 5




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightBorderThickness API value during initialization   $("#container").ejTreeMap({highlightBorderThickness:5});</code></pre><pre class="prettyprint"><code> //Get or set the highlightBorderThickness API, after initialization:
        //Gets the highlightBorderThickness value   var property =$("#container").data("ejTreeMap").model.highlightBorderThickness;
         //Sets the highlightBorderThickness value         $("#container").data("ejTreeMap").model.highlightBorderThickness = 5; </code></pre>



### highlightGroupBorderBrush<span class="type-signature type string">string</span>




Specifies the highlight border brush of treemap


Default Value:
{:.param}



* "gray"




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightGroupBorderBrush API value during initialization   $("#container").ejTreeMap({highlightGroupBorderBrush:'gray'});</code></pre><pre class="prettyprint"><code> //Get or set the highlightGroupBorderBrush API, after initialization:
        //Gets the highlightGroupBorderBrush value   var property =$("#container").data("ejTreeMap").model.highlightGroupBorderBrush;
         //Sets the highlightGroupBorderBrush value         $("#container").data("ejTreeMap").model.highlightGroupBorderBrush = 'gray'; </code></pre>



### highlightGroupBorderThickness<span class="type-signature type number">number</span>




Specifies the border thickness when treemap items is highlighted in the treemap


Default Value:
{:.param}



* 5




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightGroupBorderThickness API value during initialization   $("#container").ejTreeMap({highlightGroupBorderThickness:5});</code></pre><pre class="prettyprint"><code> //Get or set the highlightGroupBorderThickness API, after initialization:
        //Gets the highlightGroupBorderThickness value   var property =$("#container").data("ejTreeMap").model.highlightGroupBorderThickness;
         //Sets the highlightGroupBorderThickness value         $("#container").data("ejTreeMap").model.highlightGroupBorderThickness = 5; </code></pre>



### highlightGroupOnSelection<span class="type-signature type boolean">boolean</span>




Specifies whether treemap item need to highlighted on selection


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightGroupOnSelection API value during initialization   $("#container").ejTreeMap({highlightGroupOnSelection:false});</code></pre><pre class="prettyprint"><code> //Get or set the highlightGroupOnSelection API, after initialization:
        //Gets the highlightGroupOnSelection value   var property =$("#container").data("ejTreeMap").model.highlightGroupOnSelection;
         //Sets the highlightGroupOnSelection value         $("#container").data("ejTreeMap").model.highlightGroupOnSelection = false; </code></pre>



### highlightOnSelection<span class="type-signature type boolean">boolean</span>




Specifies whether treemap item need to highlighted on selection


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //To set highlightOnSelection API value during initialization   $("#container").ejTreeMap({highlightOnSelection:false});</code></pre><pre class="prettyprint"><code> //Get or set the highlightOnSelection API, after initialization:
        //Gets the highlightOnSelection value   var property =$("#container").data("ejTreeMap").model.highlightOnSelection;
         //Sets the highlightOnSelection value         $("#container").data("ejTreeMap").model.highlightOnSelection = false; </code></pre>



### iconHeight<span class="type-signature type number">number</span>




Specifies the iconHeight for legend


Default Value:
{:.param}



* 15




Example
{:.example}
<pre class="prettyprint"><code> //To set iconHeight API value during initialization   $("#container").ejTreeMap( {legendSettings:{ iconHeight: 15}});</code></pre><pre class="prettyprint"><code> //Get or set the iconHeight API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.iconHeight;
         //Sets the iconHeight value         $("#container").data("ejTreeMap").model.legendSettings = { iconHeight: 15}; </code></pre>



### iconWidth<span class="type-signature type number">number</span>




Specifies the iconWidth for legend


Default Value:
{:.param}



* 15




Example
{:.example}
<pre class="prettyprint"><code> //To set iconWidth API value during initialization   $("#container").ejTreeMap( {legendSettings:{ iconWidth: 15}});</code></pre><pre class="prettyprint"><code> //Get or set the iconWidth API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.iconWidth;
         //Sets the iconWidth value         $("#container").data("ejTreeMap").model.legendSettings = { iconWidth: 15}; </code></pre>



### itemsLayoutMode<span class="type-signature type enum">enum</span>




Specifies the items layout mode of the treemap. Accepted itemsLayoutMode values are Squarified, SliceAndDiceHorizontal, SliceAndDiceVertical and SliceAndDiceAuto


Default Value:
{:.param}



* "Squarified"




Example
{:.example}
<pre class="prettyprint"><code> //To set itemsLayoutMode API value during initialization   $("#container").ejTreeMap({itemsLayoutMode:ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified});</code></pre><pre class="prettyprint"><code> //Get or set the itemsLayoutMode API, after initialization:
        //Gets the itemsLayoutMode value   var property =$("#container").data("ejTreeMap").model.itemsLayoutMode;
         //Sets the itemsLayoutMode value         $("#container").data("ejTreeMap").model.itemsLayoutMode = ej.datavisualization.TreeMap.ItemsLayoutMode.Squarified; </code></pre>



### leafItemSettings<span class="type-signature type object">object</span>




Specifies the leaf settings of the treemap






### leafItemSettings.borderBrush<span class="type-signature type string">string</span>




Specifies the border bruch color of the leaf item.


Default Value:
{:.param}



* "white"




Example
{:.example}
<pre class="prettyprint"><code> //To set borderBrush API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ borderBrush: "white"}});</code></pre><pre class="prettyprint"><code> //Get or set the borderBrush API, after initialization:
        //Gets the borderBrush value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderBrush;
         //Sets the borderBrush value         $("#container").data("ejTreeMap").model.leafItemSettings = { borderBrush: "white"}; </code></pre>



### leafItemSettings.borderThickness<span class="type-signature type number">number</span>




Specifies the border thickness of the leaf item.


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code> //To set borderThickness API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ borderThickness: 1}});</code></pre><pre class="prettyprint"><code> //Get or set the borderThickness API, after initialization:
        //Gets the borderThickness value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.borderThickness;
         //Sets the borderThickness value         $("#container").data("ejTreeMap").model.leafItemSettings = { borderThickness: 1}; </code></pre>



### leafItemSettings.itemTemplate<span class="type-signature type string">string</span>




Specifies the label template of the leaf item.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set itemTemplate API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ itemTemplate: "temp"}});</code></pre><pre class="prettyprint"><code> //Get or set the itemTemplate API, after initialization:
        //Gets the itemTemplate value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.itemTemplate;
         //Sets the itemTemplate value         $("#container").data("ejTreeMap").model.leafItemSettings = { itemTemplate: "temp"}; </code></pre>



### leafItemSettings.labelPath<span class="type-signature type string">string</span>




Specifies the label path of the leaf item.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set labelPath API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ labelPath: "GameName"}});</code></pre><pre class="prettyprint"><code> //Get or set the labelPath API, after initialization:
        //Gets the labelPath value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPath;
         //Sets the labelPath value         $("#container").data("ejTreeMap").model.leafItemSettings = { labelPath: "GameName"}; </code></pre>



### leafItemSettings.labelPosition<span class="type-signature type enum">enum</span>




Specifies the position of the leaf labels.


Default Value:
{:.param}



* center




Example
{:.example}
<pre class="prettyprint"><code> //To set labelPosition API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ labelPosition: "center"}});</code></pre><pre class="prettyprint"><code> //Get or set the labelPosition API, after initialization:
        //Gets the labelPosition value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelPosition;
         //Sets the labelPosition value         $("#container").data("ejTreeMap").model.leafItemSettings.labelPosition= "topleft"; </code></pre>



### leafItemSettings.labelVisibilityMode<span class="type-signature type enum">enum</span>




Specifies the mode of label visibility


Default Value:
{:.param}



* visible




Example
{:.example}
<pre class="prettyprint"><code> //To set labelVisibilityMode API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ labelVisibilityMode: "visible"}});</code></pre><pre class="prettyprint"><code> //Get or set the labelVisibilityMode API, after initialization:
        //Gets the labelVisibilityMode value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode;
         //Sets the labelVisibilityMode value         $("#container").data("ejTreeMap").model.leafItemSettings.labelVisibilityMode= "visible"; </code></pre>



### leafItemSettings.showLabels<span class="type-signature type boolean">boolean</span>




Shows or hides the label of the leaf item.


Default Value:
{:.param}



* "false"




Example
{:.example}
<pre class="prettyprint"><code> //To set showLabels API value during initialization   $("#container").ejTreeMap({leafItemSettings:{ showLabels: "false"}});</code></pre><pre class="prettyprint"><code> //Get or set the showLabels API, after initialization:
        //Gets the showLabels value   var property =$("#container").data("ejTreeMap").model.leafItemSettings.showLabels;
         //Sets the showLabels value         $("#container").data("ejTreeMap").model.leafItemSettings = { showLabels: "false"}; </code></pre>



### legendSettings<span class="type-signature type object">object</span>




Specifies the legend settings of the treemap






### levels<span class="type-signature type treemaplevel">treeMapLevel</span>




Specify levels of treemap for grouped visualization of datas


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code>  // Set the levels during initialization.                  $("#container").ejTreeMap({   levels: [{ groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' }]})</code></pre><pre class="prettyprint"><code> //Get or set the levels after initialization:
  //Gets the levels from map.  var levels =$("#container").data("ejTreeMap").model.levels[levelIndex];  //Sets the levels to map.  $("#container").data("ejTreeMap").model.levels[levelIndex]  = { groupPath: "Continent", groupGap: 5, headerHeight: 30, headerTemplate: 'headertemplate' };</code></pre>



### paletteColorMapping<span class="type-signature type object">object</span>




Specifies the paletteColorMapping of the treemap






### rangeColorMapping<span class="type-signature type treemaprangecolormapping">TreeMapRangeColorMapping</span>




Specifies the rangeColorMapping settings of the treemap



Example
{:.example}
<pre class="prettyprint"><code> //To set rangeColorMapping API value during initialization   $("#container").ejTreeMap( {rangeColorMapping:[{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]});</code></pre><pre class="prettyprint"><code> //Get or set the rangeColorMapping API, after initialization:
        //Gets the rangeColorMapping value   var property =$("#container").data("ejTreeMap").model.rangeColorMapping;
         //Sets the rangeColorMapping value         $("#container").data("ejTreeMap").model.rangeColorMapping = [{ color: "#77D8D8",legendLabel:"1% Growth", from: "0", to: "1" }]; </code></pre>



### rangeMaximum<span class="type-signature type number">number</span>




Specifies the rangeMaximum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set rangeMaximum API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ rangeMaximum:1}});</code></pre><pre class="prettyprint"><code> //Get or set the rangeMaximum API, after initialization:
        //Gets the rangeMaximum value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMaximum;
         //Sets the rangeMaximum value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMaximum:1}; </code></pre>



### rangeMaximum<span class="type-signature type number">number</span>




Specifies the rangeMaximum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set rangeMaximum API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ rangeMaximum:1}});</code></pre><pre class="prettyprint"><code> //Get or set the rangeMaximum API, after initialization:
        //Gets the rangeMaximum value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMaximum;
         //Sets the rangeMaximum value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMaximum:1}; </code></pre>



### rangeMinimum<span class="type-signature type number">number</span>




Specifies the rangeMinimum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set rangeMinimum API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ rangeMinimum:1}});</code></pre><pre class="prettyprint"><code> //Get or set the rangeMinimum API, after initialization:
        //Gets the rangeMinimum value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMinimum;
         //Sets the rangeMinimum value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMinimum:1}; </code></pre>



### rangeMinimum<span class="type-signature type number">number</span>




Specifies the rangeMinimum value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set rangeMinimum API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ rangeMinimum:1}});</code></pre><pre class="prettyprint"><code> //Get or set the rangeMinimum API, after initialization:
        //Gets the rangeMinimum value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.rangeMinimum;
         //Sets the rangeMinimum value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { rangeMinimum:1}; </code></pre>



### shapeLayer.groupSelectionMode<span class="type-signature type enum">enum</span>




Specifies the selection mode of the treemap. Accepted selection mode values are Default and Multiple.


Default Value:
{:.param}



* "default"




Example
{:.example}
<pre class="prettyprint"><code>  // Set the selection mode during initialization.                                $("#container").ejTreeMap({layers: [{ selectionMode:'default' }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupSelection mode after initialization:
  //Gets the selection mode from treemap.  var property =$("#container").data("ejTreeMap").model.layers[layerIndex].groupSelectionMode;  //Sets the selection mode to treemap.  $("#container").data("ejTreeMap").model.layers[layerIndex].groupSelectionMode  = 'default';</code></pre>



### showLegend<span class="type-signature type boolean">boolean</span>




Specifies the legend visibility status of the treemap


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //To set showLegend API value during initialization   $("#container").ejTreeMap({showLegend:false});</code></pre><pre class="prettyprint"><code> //Get or set the showLegend API, after initialization:
        //Gets the showLegend value   var property =$("#container").data("ejTreeMap").model.showLegend;
         //Sets the showLegend value         $("#container").data("ejTreeMap").model.showLegend = false; </code></pre>



### showTooltip<span class="type-signature type boolean">boolean</span>




Specifies whether treemap tooltip need to be visible


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //To set showTooltip API value during initialization   $("#container").ejTreeMap({showTooltip:false});</code></pre><pre class="prettyprint"><code> //Get or set the showTooltip API, after initialization:
        //Gets the showTooltip value   var property =$("#container").data("ejTreeMap").model.showTooltip;
         //Sets the showTooltip value         $("#container").data("ejTreeMap").model.showTooltip = false; </code></pre>



### template<span class="type-signature type string">string</span>




Specifies the template for legendSettings


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set template API value during initialization   $("#container").ejTreeMap( {legendSettings:{ template: null}});</code></pre><pre class="prettyprint"><code> //Get or set the template API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.template;
         //Sets the template value         $("#container").data("ejTreeMap").model.legendSettings = { template: null}; </code></pre>



### to<span class="type-signature type number">number</span>




Specifies the to value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set to API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ to:1}});</code></pre><pre class="prettyprint"><code> //Get or set the to API, after initialization:
        //Gets the to value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.to;
         //Sets the to value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { to:1}; </code></pre>



### to<span class="type-signature type number">number</span>




Specifies the to value for desaturation color mapping


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code> //To set to API value during initialization   $("#container").ejTreeMap( {desaturationColorMapping{ to:1}});</code></pre><pre class="prettyprint"><code> //Get or set the to API, after initialization:
        //Gets the to value   var property =$("#container").data("ejTreeMap").model.desaturationColorMapping.to;
         //Sets the to value         $("#container").data("ejTreeMap").model.desaturationColorMapping = { to:1}; </code></pre>



### tooltipTemplate<span class="type-signature type string">string</span>




Specifies the tooltip template of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set tooltipTemplate API value during initialization   $("#container").ejTreeMap({tooltipTemplate:'template'});</code></pre><pre class="prettyprint"><code> //Get or set the tooltipTemplate API, after initialization:
        //Gets the tooltipTemplate value   var property =$("#container").data("ejTreeMap").model.tooltipTemplate;
         //Sets the tooltipTemplate value         $("#container").data("ejTreeMap").model.tooltipTemplate = 'template'; </code></pre>



### TreeMapGroupColorMapping.groupID<span class="type-signature type string">string</span>




Specifies the groupID for GroupColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupID for GroupColorMapping during initialization.                                 $("#container").ejTreeMap({groupColorMapping: [{ groupID:"Asia" }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupID for GroupColorMapping after initialization:
  //Gets the groupID for GroupColorMapping from map.  var property =$("#container").data("ejTreeMap").model.groupColorMapping.groupID;  //Sets the groupID for GroupColorMapping to map.  $("#container").data("ejTreeMap").model.groupColorMapping.groupID  = "Asia";</code></pre>



### treeMapItems<span class="type-signature type treemapitem">TreeMapItem</span>




Hold the treeMapItems to be displayed in treemap


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code>  // Set the treeMapItems during initialization.   $("#container").ejTreeMap({treeMapItems:[]});                             </code></pre><pre class="prettyprint"><code> //Get or set the treeMapItems after initialization:
  //Gets the treeMapItems from treemap.  var property =$("#container").data("ejTreeMap").model.treeMapItems;
               //Sets the treeMapItems to treemap.        $("#container").data("ejTreeMap").model.treeMapItems = []; </code></pre>



### treeMapLevel




Hold the Level settings of TreeMap






### treeMapLevel.groupBackground<span class="type-signature type string">string</span>




specifies the group background


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupBackground during initialization.                               $("#container").ejTreeMap({levels: [{ groupBackground:"white" }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupBackground after initialization:
  //Gets the groupBackground from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground;  //Sets the groupBackground to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBackground  = "white";</code></pre>



### treeMapLevel.groupBorderColor<span class="type-signature type string">string</span>




Specifies the group border color for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupBorderColor during initialization.                              $("#container").ejTreeMap({levels: [{ groupBorderColor:"#58585B" }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupBorderColor after initialization:
  //Gets the groupBorderColor from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor;  //Sets the groupBorderColor to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderColor  = "#58585B";</code></pre>



### treeMapLevel.groupBorderThickness<span class="type-signature type number">number</span>




Specifies the group border thickness for tree map level.


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupBorderThickness during initialization.                          $("#container").ejTreeMap({levels: [{ groupBorderThickness:1 }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupBorderThickness after initialization:
  //Gets the groupBorderThickness from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness;  //Sets the groupBorderThickness to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupBorderThickness  = 1;</code></pre>



### treeMapLevel.groupGap<span class="type-signature type number">number</span>




Specifies the group gap for tree map level.


Default Value:
{:.param}



* 1




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupGap during initialization.                              $("#container").ejTreeMap({levels: [{ groupGap:1 }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupGap after initialization:
  //Gets the groupGap from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupGap;  //Sets the groupGap to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupGap  = 1;</code></pre>



### treeMapLevel.groupPadding<span class="type-signature type number">number</span>




Specifies the group padding for tree map level.


Default Value:
{:.param}



* 4




Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupPadding during initialization.                          $("#container").ejTreeMap({levels: [{ groupPadding:4 }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupPadding after initialization:
  //Gets the groupPadding from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding;  //Sets the groupPadding to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPadding  = 4;</code></pre>



### treeMapLevel.groupPath<span class="type-signature type string">string</span>




Specifies the group path for tree map level.



Example
{:.example}
<pre class="prettyprint"><code>  // Set the groupPath during initialization.                             $("#container").ejTreeMap({levels: [{ groupPath:"pathName" }]})</code></pre><pre class="prettyprint"><code> //Get or set the groupPath after initialization:
  //Gets the groupPath from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].groupPath;  //Sets the groupPath to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].groupPath  = "pathName";</code></pre>



### treeMapLevel.headerHeight<span class="type-signature type number">number</span>




Specifies the header height for tree map level.


Default Value:
{:.param}



* 0




Example
{:.example}
<pre class="prettyprint"><code>  // Set the headerHeight during initialization.                          $("#container").ejTreeMap({levels: [{ headerHeight:20 }]})</code></pre><pre class="prettyprint"><code> //Get or set the headerHeight after initialization:
  //Gets the headerHeight from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight;  //Sets the headerHeight to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].headerHeight  = 1;</code></pre>



### treeMapLevel.headerTemplate<span class="type-signature type string">string</span>




Specifies the header template for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the headerTemplate during initialization.                                $("#container").ejTreeMap({levels: [{ headerTemplate:"template" }]})</code></pre><pre class="prettyprint"><code> //Get or set the headerTemplate after initialization:
  //Gets the headerTemplate from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate;  //Sets the headerTemplate to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].headerTemplate  = "template";</code></pre>



### treeMapLevel.headerVisibilityMode<span class="type-signature type enum">enum</span>




Specifies the mode of header visibility


Default Value:
{:.param}



* visible




Example
{:.example}
<pre class="prettyprint"><code> //To set labelVisibilityMode API value during initialization   $("#container").ejTreeMap({levels:[{ headerVisibilityMode: "visible"}]});</code></pre><pre class="prettyprint"><code> //Get or set the headerVisibilityMode API, after initialization:
        //Gets the headerVisibilityMode value   var property =$("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode;
         //Sets the headerVisibilityMode value         $("#container").data("ejTreeMap").model.levels[0].headerVisibilityMode= "visible"; </code></pre>



### treeMapLevel.labelPosition<span class="type-signature type enum">enum</span>




Specifies the position of the labels.


Default Value:
{:.param}



* center




Example
{:.example}
<pre class="prettyprint"><code> //To set labelPosition API value during initialization   $("#container").ejTreeMap({levels:[{ labelPosition: "center"]}});</code></pre><pre class="prettyprint"><code> //Get or set the labelPosition API, after initialization:
        //Gets the labelPosition value   var property =$("#container").data("ejTreeMap").model.levels[0].labelPosition;
         //Sets the labelPosition value         $("#container").data("ejTreeMap").model.levels[0].labelPosition= "topleft"; </code></pre>



### treeMapLevel.labelTemplate<span class="type-signature type string">string</span>




Specifies the label template for tree map level.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the labelTemplate during initialization.                                 $("#container").ejTreeMap({levels: [{ labelTemplate:"template" }]})</code></pre><pre class="prettyprint"><code> //Get or set the labelTemplate after initialization:
  //Gets the labelTemplate from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate;  //Sets the labelTemplate to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].labelTemplate  = "template";</code></pre>



### treeMapLevel.labelVisibilityMode<span class="type-signature type enum">enum</span>




Specifies the mode of label visibility


Default Value:
{:.param}



* visible




Example
{:.example}
<pre class="prettyprint"><code> //To set labelVisibilityMode API value during initialization   $("#container").ejTreeMap({levels:[{ labelVisibilityMode: "visible"}]});</code></pre><pre class="prettyprint"><code> //Get or set the labelVisibilityMode API, after initialization:
        //Gets the labelVisibilityMode value   var property =$("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode;
         //Sets the labelVisibilityMode value         $("#container").data("ejTreeMap").model.levels[0].labelVisibilityMode= "visible"; </code></pre>



### treeMapLevel.showHeader<span class="type-signature type bool">bool</span>




Shows or hides the header for tree map level.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>  // Set the shoeHeader during initialization.                            $("#container").ejTreeMap({levels: [{ showHeader:false }]})</code></pre><pre class="prettyprint"><code> //Get or set the showHeader after initialization:
  //Gets the showHeader from treemap.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showHeader;  //Sets the headerHeight to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].showHeader  = true;</code></pre>



### treeMapLevel.showLabels<span class="type-signature type boolean">boolean</span>




Shows or hides the labels for tree map level.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code>  // Set the showLabels during initialization.                            $("#container").ejTreeMap({levels: [{ showLabels:false }]})</code></pre><pre class="prettyprint"><code> //Get or set the showLabels after initialization:
  //Gets the showLabels from map.  var property =$("#container").data("ejTreeMap").model.levels[levelIndex].showLabels;  //Sets the showLabels to map.  $("#container").data("ejTreeMap").model.levels[levelIndex].showLabels  = false;</code></pre>



### treeMapRangeColorMapping.color<span class="type-signature type string">string</span>




Specifies the color value for rangeColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the color value for rangeColorMapping during initialization.                             $("#container").ejTreeMap({rangeColorMapping: [{ color: "#77D8D8" }]})</code></pre><pre class="prettyprint"><code> //Get or set the color value for rangeColorMapping after initialization:
  //Gets the color value for rangeColorMapping from map.  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.color;  //Sets the color value for rangeColorMapping to map.  $("#container").data("ejTreeMap").model.rangeColorMapping.color  = "#77D8D8";</code></pre>



### treeMapRangeColorMapping.from<span class="type-signature type number">number</span>




Specifies the from value for rangeColorMapping.


Default Value:
{:.param}



* -1




Example
{:.example}
<pre class="prettyprint"><code>  // Set the from value for rangeColorMapping during initialization.                              $("#container").ejTreeMap({rangeColorMapping: [{ from:-1 }]})</code></pre><pre class="prettyprint"><code> //Get or set the from value for rangeColorMapping after initialization:
  //Gets the from value for rangeColorMapping from map.  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.from;  //Sets the from value for rangeColorMapping to map.  $("#container").data("ejTreeMap").model.rangeColorMapping.from  = -1;</code></pre>



### treeMapRangeColorMapping.legendlabel<span class="type-signature type string">string</span>




Specifies the legendlabel value for rangeColorMapping.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code>  // Set the legendlabel value for rangeColorMapping during initialization.                               $("#container").ejTreeMap({rangeColorMapping: [{ legendlabel: "1% Growth" }]})</code></pre><pre class="prettyprint"><code> //Get or set the legendlabel value for rangeColorMapping after initialization:
  //Gets the legendlabel value for rangeColorMapping from map.  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel;  //Sets the legendlabel value for rangeColorMapping to map.  $("#container").data("ejTreeMap").model.rangeColorMapping.legendlabel  = "1% Growth";</code></pre>



### treeMapRangeColorMapping.to<span class="type-signature type number">number</span>




Specifies the to value for rangeColorMapping.


Default Value:
{:.param}



* -1




Example
{:.example}
<pre class="prettyprint"><code>  // Set the to value for rangeColorMapping during initialization.                                $("#container").ejTreeMap({rangeColorMapping: [{ to:-1 }]})</code></pre><pre class="prettyprint"><code> //Get or set the to value for rangeColorMapping after initialization:
  //Gets the to value for rangeColorMapping from map.  var property =$("#container").data("ejTreeMap").model.rangeColorMapping.to;  //Sets the to value for rangeColorMapping to map.  $("#container").data("ejTreeMap").model.rangeColorMapping.to  = -1;</code></pre>



### uniColorMapping<span class="type-signature type object">object</span>




Specifies the uniColorMapping settings of the treemap






### weightValuePath<span class="type-signature type string">string</span>




Specifies the weight valuepath of the treemap


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //To set weightValuePath API value during initialization   $("#container").ejTreeMap({weightValuePath:'TotalMedals'});</code></pre><pre class="prettyprint"><code> //Get or set the weightValuePath API, after initialization:
        //Gets the weightValuePath value   var property =$("#container").data("ejTreeMap").model.weightValuePath;
         //Sets the weightValuePath value         $("#container").data("ejTreeMap").model.weightValuePath = 'TotalMedals'; </code></pre>



### width<span class="type-signature type number">number</span>




Specifies the width for legend


Default Value:
{:.param}



* 100




Example
{:.example}
<pre class="prettyprint"><code> //To set width API value during initialization   $("#container").ejTreeMap( {legendSettings:{ width: 100}});</code></pre><pre class="prettyprint"><code> //Get or set the width API, after initialization:
        //Gets the template value   var property =$("#container").data("ejTreeMap").model.legendSettings.width;
         //Sets the width value         $("#container").data("ejTreeMap").model.legendSettings = { width: 100}; </code></pre>


## Methods




### refresh<span class="signature">()</span>




Method to reload treemap with updated values.



Example
{:.example}
<pre class="prettyprint"><code> //refresh method for treemap$("#container").ejTreeMap("refresh");</code></pre>


## Events




### treeMapItemSelected




Triggers on treemap item selected.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>originalEvent.data</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">Returns selected treeMapItem object.</td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> //treemap item selected event for treemap$("#container").ejTreeMap({   treeMapItemSelected: function () {}});</code></pre>


