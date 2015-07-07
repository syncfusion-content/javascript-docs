---
layout: post
title: ejColorPicker
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html color picker control.










$(element).ejColorPicker<span class="signature">(options)</span>







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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for color picker</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.colorpicker.js


* module:ej.button.js


* module:ej.splitbutton.js


* module:ej.menu.js


* module:ej.slider.js




## Members








### buttonText<span class="type-signature type string">string</span>
{:#buttontext}
{:#buttonText}








The colorpicker control allows to define the customized text to displayed in button elements. Using the property to achieve the customized culture values.




Default Value:
{:.param}






* buttonText.apply= "Apply", buttonText.cancel= "Cancel"








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set buttonText API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {apply: "Set", cancel: "Close" }});
&lt;/script&gt;</code>
</pre>






### columns<span class="type-signature type number">number</span>
{:#columns}
{:#columns}








Specifies the number of columns to be displayed color palette model.




Default Value:
{:.param}






* 10








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set columns API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", columns: 5});
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#cssclass}
{:#cssClass}








This property allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds.




Default Value:
{:.param}






* emptyString








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set cssClass API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  cssClass : "gradient-lime"});
&lt;/script&gt;</code>
</pre>






### custom<span class="type-signature type data">data</span>
{:#custom}
{:#custom}








This property allows to define the custom colors in the palette model.Custom palettes are created by passing a comma delimited string of HEX values or an array of colors.




Default Value:
{:.param}






* empty








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set custom API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "custompalette", custom: ["ffffff", "ffccff", "ff99ff", "ff66ff", "ff33ff", "ff00ff", "ccffff", "ccccff"]});
&lt;/script&gt;</code>
</pre>






### displayInline<span class="type-signature type boolean">boolean</span>
{:#displayinline}
{:#displayInline}








This property allows to embed the popup in the order of DOM element flow . When we set the value as true, the colorpicker popup is always in visible state.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set displayInline API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  displayInline: true});
&lt;/script&gt;</code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>
{:#enabled}
{:#enabled}








This property allows to change the control in enabled or disabled state.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set enabled API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  enabled: false});
&lt;/script&gt;</code>
</pre>






### enableOpacity<span class="type-signature type boolean">boolean</span>
{:#enableopacity}
{:#enableOpacity}








This property allows to enable or disable the opacity slider in the color picker control




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set enableOpacity API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", enableOpacity: false });
&lt;/script&gt;</code>
</pre>






### modelType<span class="type-signature type enum">enum</span>
{:#modeltype}
{:#modelType}








Specifies the model type to be rendered initially in the colorpicker control. There are three different types of model type availabale in colorpicker control. See <a href="global.html#ModelType">ModelType</a>




Default Value:
{:.param}






* ej.ColorPicker.ModelType.Default








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set modelType API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette"});
&lt;/script&gt;</code>
</pre>






### opacityValue<span class="type-signature type number">number</span>
{:#opacityvalue}
{:#opacityValue}








This property allows to change the opacity value .The selected color opacity will be adjusted by using this opacity value.




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set opacityValue API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", opacityValue: 20 });
&lt;/script&gt;</code>
</pre>






### palette<span class="type-signature type enum">enum</span>
{:#palette}
{:#palette}








Specifies the palette type to be displayed at initial time in palette model.There two types of palette model availabale in colorpicker control. See <a href="global.html#Palette">Palette</a>




Default Value:
{:.param}






* ej.ColorPicker.Palette.BasicPalette








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set palette API during initialization 
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "basicpalette"});
&lt;/script&gt;</code>
</pre>






### presetType<span class="type-signature type enum">enum</span>
{:#presettype}
{:#presetType}








This property allows to define the preset model to be rendered initially in palette type.It consists of 12 different types of presets. Each presets have 50 colors. See Presets




Default Value:
{:.param}






* ej.ColorPicker.Presets.Basic








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set presetType API during initialization 
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", presetType: "vintage"});
&lt;/script&gt;</code>
</pre>






### showPreview<span class="type-signature type boolean">boolean</span>
{:#showpreview}
{:#showPreview}








This property allows to provides live preview support for current cursor selection color and selected color.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set showPreview API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", showPreview: false});
&lt;/script&gt;</code>
</pre>






### showRecentColors<span class="type-signature type boolean">boolean</span>
{:#showrecentcolors}
{:#showRecentColors}








This property allows to store the color values in custom list.The colorpicker will keep up to 11 colors in a custom list.By clicking the add button, the selected color from picker or palette will get added in the recent color list.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set showRecentColors API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   showRecentColors: true});
&lt;/script&gt;</code>
</pre>






### showTooltip<span class="type-signature type boolean">boolean</span>
{:#showtooltip}
{:#showTooltip}








This property allows to shows tooltip to notify the slider value in colorpicker control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set showTooltip API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", showTooltip: true});
&lt;/script&gt;</code>
</pre>






### toolIcon<span class="type-signature type string">string</span>
{:#toolicon}
{:#toolIcon}








Specifies the toolIcon to be disaplyed in dropdown control color area.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set toolIcon API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  toolIcon: "e-fontcolor-icon"});
&lt;/script&gt;
&lt;style&gt;
.e-colorwidget .e-tool .e-fontcolor-icon:before
{
content: "\e632";
margin-top: 9px;
font-size: 10px;
margin-left: 5px;
}
&lt;/style&gt;</code>
</pre>






### tooltipText<span class="type-signature type object">object</span>
{:#tooltiptext}
{:#tooltipText}








This property allows to define the customized text or content to displayed when mouse over the following elements. This property also allows to use the culture values.




Default Value:
{:.param}






* tooltipText: { switcher: "Switcher", addbutton: "Add Color", basic: "Basic", monochrome: "Mono Chrome", flatcolors: "Flat Color", seawolf: "Sea Wolf", webcolors: "Web Colors", sandy: "Sandy", pinkshades: "Pink Shades", misty: "Misty", citrus: "Citrus", vintage: "Vintage", moonlight: "Moon Light", candycrush: "Candy Crush", currentcolor: "Current Color", selectedcolor: "Selected Color" }








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set tooltipText API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   tooltipText: { switcher: "Switch",  currentcolor: "New Color", selectedcolor: "Old Color" }});
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type string">string</span>
{:#value}
{:#value}








Specifies the color value for colorpicker control, the value is in hexadecimal form with prefix of "#".




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//To set value API during initialization
$('#colorPick').ejColorPicker({ value: "#278787"});
&lt;/script&gt;</code>
</pre>




## Methods








### disable<span class="signature">()</span>
{:#disable}
{:#disable}








Disables the color picker control





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.disable(); // disables the colorPicker
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// disables the colorPicker
$("#colorPick").ejColorPicker("disable");
&lt;/script&gt;       </code>
</pre>






### enable<span class="signature">()</span>
{:#enable}
{:#enable}








Enable the color picker control





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.enable(); // enables the colorPicker
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// enable the colorPicker
$("#colorPick").ejColorPicker("enable");
&lt;/script&gt;       </code>
</pre>






### getColor<span class="signature">()</span>
{:#getcolor}
{:#getColor}








Gets the selected color in RGB format





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.getColor(); // gets the selected color in RGB format
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// gets the selected color in RGB format
var color=$("#colorPick").ejColorPicker("getColor");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt;       </code>
</pre>






### getValue<span class="signature">()</span>
{:#getvalue}
{:#getValue}








Gets the selected color value as string





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
alert(colorObj.getValue()); // gets the selected color value as string
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// gets the selected color value as string
alert($("#colorPick").ejColorPicker("getValue"));
&lt;/script&gt;       </code>
</pre>






### hexCodeToRGB<span class="signature">()</span>
{:#hexcodetorgb}
{:#hexCodeToRGB}








To Convert color value from hexCode to RGB





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.hexCodeToRGB("#278787"); // Convert color value from hexCode to RGB
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from hexCode to RGB
var color=$("#colorPick").ejColorPicker("hexCodeToRGB","#278787");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt;       </code>
</pre>






### hide<span class="signature">()</span>
{:#hide}
{:#hide}








Hides the colorpicker popup, if in opended state.





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.hide(); // hide the colorpicker popup
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// hide the colorpicker popup
$("#colorPick").ejColorPicker("hide");
&lt;/script&gt;       </code>
</pre>






### HSVToRGB<span class="signature">()</span>
{:#hsvtorgb}
{:#HSVToRGB}








Convert color value from HSV to RGB





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.HSVToRGB({h:230,s:98,v:98}); // Convert color value from HSV to RGB
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from HSV to RGB        
var color=$("#colorPick").ejColorPicker("HSVToRGB","{h:230,s:98,v:98}");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
&lt;/script&gt;       </code>
</pre>






### RGBToHEX<span class="signature">()</span>
{:#rgbtohex}
{:#RGBToHEX}








Convert color value from RGB to HEX





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
alert(colorObj.RGBToHEX(colorObj.getColor())); // Convert color value from RGB to HEX
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
// Convert color value from RGB to HEX
alert($("#colorPick").ejColorPicker("RGBToHEX",colorObj.getColor()));
&lt;/script&gt;       </code>
</pre>






### RGBToHSV<span class="signature">()</span>
{:#rgbtohsv}
{:#RGBToHSV}








Convert color value from RGB to HSV





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.RGBToHSV({r:39,g:135,b:135}); // Convert color value from RGB to HSV
alert("H="+color.r+", S="+color.g+", V="+color.b);
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from RGB to HSV        
var color=$("#colorPick").ejColorPicker("RGBToHSV","{r:39,g:135,b:125}");
alert("H="+color.r+", S="+color.g+", V="+color.b);
&lt;/script&gt;       </code>
</pre>






### show<span class="signature">()</span>
{:#show}
{:#show}








Open the colorpicker popup.





Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.show(); // open the colorpicker popup
&lt;/script&gt; </code>
</pre>
<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// open the colorpicker popup
$("#colorPick").ejColorPicker("show");
&lt;/script&gt;       </code>
</pre>




## Events








### change
{:#change}
{:#change}








Fires after Color value has been changed sucessfully.If the user want to perform any operation after the color value changed then the user can make use of this change event.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the changed color value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//change event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
change: function (args) {
// Write a code block to perform operation after changing the color.
}
});
&lt;/script&gt;</code>
</pre>






### close
{:#close}
{:#close}








Fires after closing the color picker popup.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//close event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
close: function (args) {
// Write a code block to perform operation after closing the color picker popup.
}
});
&lt;/script&gt;</code>
</pre>






### create
{:#create}
{:#create}








Fires after Color picker control is created. If the user want to perform any operation after the color picker control creation then the user can make use of this create event.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//create event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
create: function (args) {
// Write a code block to perform operation after creating the color picker.
}
});
&lt;/script&gt;</code>
</pre>






### destroy
{:#destroy}
{:#destroy}








Fires after Color picker control is destroyed. If the user want to perform any operation after the color picker control destroyed then the user can make use of this destroy event.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//create event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
destroy: function (args) {
// Write a code block to perform operation after creating the color picker.
}
});
&lt;/script&gt;</code>
</pre>






### open
{:#open}
{:#open}








Fires after opening the color picker popup

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//open event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
open: function (args) {
// Write a code block to perform operation after opening the color picker popup.
}
});
&lt;/script&gt;</code>
</pre>






### select
{:#select}
{:#select}








Fires after Color value has been selected sucessfully. If the user want to perform any operation after the color value selected then the user can make use of this select event.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from color picker
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return the selected color value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>   
&lt;input type="text" id="colorPick"/&gt; 
 
&lt;script&gt;
//select event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
select: function (args) {
// Write a code block to perform operation after selecting the color.
}
});
&lt;/script&gt;</code>
</pre>



