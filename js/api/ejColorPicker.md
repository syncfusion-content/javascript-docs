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
<td class="name">{% highlight html %}
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for color picker</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
</script>{% endhighlight %}







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
{:#members:buttontext}








The colorpicker control allows to define the customized text to displayed in button elements. Using the property to achieve the customized culture values.




Default Value:
{:.param}






* buttonText.apply= "Apply", buttonText.cancel= "Cancel"








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set buttonText API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {apply: "Set", cancel: "Close" }});
</script>{% endhighlight %}







### columns<span class="type-signature type number">number</span>
{:#members:columns}








Specifies the number of columns to be displayed color palette model.




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set columns API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", columns: 5});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








This property allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds.




Default Value:
{:.param}






* emptyString








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set cssClass API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  cssClass : "gradient-lime"});
</script>{% endhighlight %}







### custom<span class="type-signature type data">data</span>
{:#members:custom}








This property allows to define the custom colors in the palette model.Custom palettes are created by passing a comma delimited string of HEX values or an array of colors.




Default Value:
{:.param}






* empty








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set custom API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "custompalette", custom: ["ffffff", "ffccff", "ff99ff", "ff66ff", "ff33ff", "ff00ff", "ccffff", "ccccff"]});
</script>{% endhighlight %}







### displayInline<span class="type-signature type boolean">boolean</span>
{:#members:displayinline}








This property allows to embed the popup in the order of DOM element flow . When we set the value as true, the colorpicker popup is always in visible state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set displayInline API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  displayInline: true});
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








This property allows to change the control in enabled or disabled state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set enabled API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  enabled: false});
</script>{% endhighlight %}







### enableOpacity<span class="type-signature type boolean">boolean</span>
{:#members:enableopacity}








This property allows to enable or disable the opacity slider in the color picker control




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set enableOpacity API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", enableOpacity: false });
</script>{% endhighlight %}







### modelType<span class="type-signature type enum">enum</span>
{:#members:modeltype}








Specifies the model type to be rendered initially in the colorpicker control. There are three different types of model type availabale in colorpicker control. See <a href="global.html#ModelType">ModelType</a>




Default Value:
{:.param}






* ej.ColorPicker.ModelType.Default








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set modelType API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette"});
</script>{% endhighlight %}







### opacityValue<span class="type-signature type number">number</span>
{:#members:opacityvalue}








This property allows to change the opacity value .The selected color opacity will be adjusted by using this opacity value.




Default Value:
{:.param}






* 100








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set opacityValue API during initialization  
$('#colorPick').ejColorPicker({ value: "#278787", opacityValue: 20 });
</script>{% endhighlight %}







### palette<span class="type-signature type enum">enum</span>
{:#members:palette}








Specifies the palette type to be displayed at initial time in palette model.There two types of palette model availabale in colorpicker control. See <a href="global.html#Palette">Palette</a>




Default Value:
{:.param}






* ej.ColorPicker.Palette.BasicPalette








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set palette API during initialization 
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "basicpalette"});
</script>{% endhighlight %}







### presetType<span class="type-signature type enum">enum</span>
{:#members:presettype}








This property allows to define the preset model to be rendered initially in palette type.It consists of 12 different types of presets. Each presets have 50 colors. See Presets




Default Value:
{:.param}






* ej.ColorPicker.Presets.Basic








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set presetType API during initialization 
$('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", presetType: "vintage"});
</script>{% endhighlight %}







### showPreview<span class="type-signature type boolean">boolean</span>
{:#members:showpreview}








This property allows to provides live preview support for current cursor selection color and selected color.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set showPreview API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", showPreview: false});
</script>{% endhighlight %}







### showRecentColors<span class="type-signature type boolean">boolean</span>
{:#members:showrecentcolors}








This property allows to store the color values in custom list.The colorpicker will keep up to 11 colors in a custom list.By clicking the add button, the selected color from picker or palette will get added in the recent color list.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set showRecentColors API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   showRecentColors: true});
</script>{% endhighlight %}







### showTooltip<span class="type-signature type boolean">boolean</span>
{:#members:showtooltip}








This property allows to shows tooltip to notify the slider value in colorpicker control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set showTooltip API during initialization
$('#colorPick').ejColorPicker({ value: "#278787", showTooltip: true});
</script>{% endhighlight %}







### toolIcon<span class="type-signature type string">string</span>
{:#members:toolicon}








Specifies the toolIcon to be disaplyed in dropdown control color area.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set toolIcon API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",  toolIcon: "e-fontcolor-icon"});
</script>
<style>
.e-colorwidget .e-tool .e-fontcolor-icon:before
{
content: "\e632";
margin-top: 9px;
font-size: 10px;
margin-left: 5px;
}
</style>{% endhighlight %}







### tooltipText<span class="type-signature type object">object</span>
{:#members:tooltiptext}








This property allows to define the customized text or content to displayed when mouse over the following elements. This property also allows to use the culture values.




Default Value:
{:.param}






* tooltipText: { switcher: "Switcher", addbutton: "Add Color", basic: "Basic", monochrome: "Mono Chrome", flatcolors: "Flat Color", seawolf: "Sea Wolf", webcolors: "Web Colors", sandy: "Sandy", pinkshades: "Pink Shades", misty: "Misty", citrus: "Citrus", vintage: "Vintage", moonlight: "Moon Light", candycrush: "Candy Crush", currentcolor: "Current Color", selectedcolor: "Selected Color" }








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set tooltipText API during initialization
$('#colorPick').ejColorPicker({ value: "#278787",   tooltipText: { switcher: "Switch",  currentcolor: "New Color", selectedcolor: "Old Color" }});
</script>{% endhighlight %}







### value<span class="type-signature type string">string</span>
{:#members:value}








Specifies the color value for colorpicker control, the value is in hexadecimal form with prefix of "#".




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//To set value API during initialization
$('#colorPick').ejColorPicker({ value: "#278787"});
</script>{% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








Disables the color picker control





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.disable(); // disables the colorPicker
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// disables the colorPicker
$("#colorPick").ejColorPicker("disable");
</script>       {% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








Enable the color picker control





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.enable(); // enables the colorPicker
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// enable the colorPicker
$("#colorPick").ejColorPicker("enable");
</script>       {% endhighlight %}







### getColor<span class="signature">()</span>
{:#methods:getcolor}








Gets the selected color in RGB format





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.getColor(); // gets the selected color in RGB format
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// gets the selected color in RGB format
var color=$("#colorPick").ejColorPicker("getColor");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script>       {% endhighlight %}







### getValue<span class="signature">()</span>
{:#methods:getvalue}








Gets the selected color value as string





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
alert(colorObj.getValue()); // gets the selected color value as string
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// gets the selected color value as string
alert($("#colorPick").ejColorPicker("getValue"));
</script>       {% endhighlight %}







### hexCodeToRGB<span class="signature">()</span>
{:#methods:hexcodetorgb}








To Convert color value from hexCode to RGB





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.hexCodeToRGB("#278787"); // Convert color value from hexCode to RGB
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from hexCode to RGB
var color=$("#colorPick").ejColorPicker("hexCodeToRGB","#278787");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script>       {% endhighlight %}







### hide<span class="signature">()</span>
{:#methods:hide}








Hides the colorpicker popup, if in opended state.





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.hide(); // hide the colorpicker popup
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// hide the colorpicker popup
$("#colorPick").ejColorPicker("hide");
</script>       {% endhighlight %}







### HSVToRGB<span class="signature">()</span>
{:#methods:hsvtorgb}








Convert color value from HSV to RGB





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.HSVToRGB({h:230,s:98,v:98}); // Convert color value from HSV to RGB
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from HSV to RGB        
var color=$("#colorPick").ejColorPicker("HSVToRGB","{h:230,s:98,v:98}");
alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
</script>       {% endhighlight %}







### RGBToHEX<span class="signature">()</span>
{:#methods:rgbtohex}








Convert color value from RGB to HEX





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
alert(colorObj.RGBToHEX(colorObj.getColor())); // Convert color value from RGB to HEX
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
// Convert color value from RGB to HEX
alert($("#colorPick").ejColorPicker("RGBToHEX",colorObj.getColor()));
</script>       {% endhighlight %}







### RGBToHSV<span class="signature">()</span>
{:#methods:rgbtohsv}








Convert color value from RGB to HSV





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
var color=colorObj.RGBToHSV({r:39,g:135,b:135}); // Convert color value from RGB to HSV
alert("H="+color.r+", S="+color.g+", V="+color.b);
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Convert color value from RGB to HSV        
var color=$("#colorPick").ejColorPicker("RGBToHSV","{r:39,g:135,b:125}");
alert("H="+color.r+", S="+color.g+", V="+color.b);
</script>       {% endhighlight %}







### show<span class="signature">()</span>
{:#methods:show}








Open the colorpicker popup.





Example
{:.example}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// Create ColorPicker instance
var colorObj = $("#colorPick").data("ejColorPicker");
colorObj.show(); // open the colorpicker popup
</script> {% endhighlight %}


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
// Create Color picker
$('#colorPick').ejColorPicker({ value: "#278787" });
// open the colorpicker popup
$("#colorPick").ejColorPicker("show");
</script>       {% endhighlight %}





## Events








### change
{:#events:change}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//change event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
change: function (args) {
// Write a code block to perform operation after changing the color.
}
});
</script>{% endhighlight %}







### close
{:#events:close}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//close event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
close: function (args) {
// Write a code block to perform operation after closing the color picker popup.
}
});
</script>{% endhighlight %}







### create
{:#events:create}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//create event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
create: function (args) {
// Write a code block to perform operation after creating the color picker.
}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//create event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
destroy: function (args) {
// Write a code block to perform operation after creating the color picker.
}
});
</script>{% endhighlight %}







### open
{:#events:open}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//open event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
open: function (args) {
// Write a code block to perform operation after opening the color picker popup.
}
});
</script>{% endhighlight %}







### select
{:#events:select}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the color picker model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
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


{% highlight html %}
   
<input type="text" id="colorPick"/> 
 
<script>
//select event for color picker
$('#colorPick').ejColorPicker({              
value: "#278787", 
select: function (args) {
// Write a code block to perform operation after selecting the color.
}
});
</script>{% endhighlight %}




