---
layout: post
title: Properties,Methods and Events of ejColorPicker Widget
description: API reference for ejColorPicker
documentation: API
platform: js
keywords: ColorPicker, ejColorPicker, syncfusion, ColorPicker api 
---

# ejColorPicker

The ColorPicker control provides you a rich visual interface for color selection. You can select the color from the professionally designed palettes or custom color. By clicking a point on the color, you can change the active color to the color that is located under the pointer. 

#### Syntax

{% highlight javascript %}

        $(element).ejColorPicker(options)

{% endhighlight %}



<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
options</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">settings for color picker</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        </script>

{% endhighlight %}



#### Requires



* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.colorpicker.js


* module:ej.button.js


* module:ej.splitbutton.js


* module:ej.menu.js


* module:ej.slider.js




## Members








### buttonText `object`
{:#members:buttontext}


The ColorPicker control allows to define the customized text to displayed in button elements. Using the property to achieve the customized culture values.


#### Default Value

* { apply: "Apply", cancel: "Cancel", swatches: "Swatches" }

#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set buttonText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {apply: "Set", cancel: "Close" }});
        </script>

{% endhighlight %}

### buttonText.apply `string`
{:#members:buttontext-apply}

Sets the text for the apply button.

#### Example


{% highlight html %}
 
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set buttonText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {apply: "select"}});
        </script>
 
 {% endhighlight %}

### buttonText.cancel `string`
{:#members:buttontext-cancel}

Sets the text for the cancel button.

#### Example



{% highlight html %}
 
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set buttonText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {cancel: "Exit" }});
        </script>
 
 {% endhighlight %}

### buttonText.swatches `string`
{:#members:buttontext-swatches}

Sets the header text for the swatches area.

#### Example


{% highlight html %}
 
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set buttonText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   buttonText: {swatches: "colors"}});
        </script>
 
 {% endhighlight %}

### buttonMode `enum|string`
{:#members:buttonmode}

<ts name="ej.ButtonMode"/>

Allows to change the mode of the button. Please refer below to know available button mode

<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Split</td>
<td class="description">Displays the button in split mode </td>
</tr>
<tr>
<td class="name">
Dropdown</td>
<td class="description">Displays the button in Dropdown mode</td>
</tr>
</tbody>
</table>


#### Default Value



* ej.ButtonMode.Split




#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set buttonText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",  buttonMode: ej.ButtonModel.DropDown});
        </script>

{% endhighlight %}







### columns `number|string`
{:#members:columns}








Specifies the number of columns to be displayed color palette model.




#### Default Value







* 10








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set columns API during initialization  
        $('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", columns: 5});
        </script>

{% endhighlight %}







### cssClass `string`
{:#members:cssclass}








This property allows you to customize its appearance using user-defined CSS and custom skin options such as colors and backgrounds.




#### Default Value







* ""








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set cssClass API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",  cssClass : "gradient-lime"});
        </script>

{% endhighlight %}







### custom `array`
{:#members:custom}








This property allows to define the custom colors in the palette model.Custom palettes are created by passing a comma delimited string of HEX values or an array of colors.




#### Default Value







* empty








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set custom API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "custompalette", custom: ["ffffff", "ffccff", "ff99ff", "ff66ff", "ff33ff", "ff00ff", "ccffff", "ccccff"]});
        </script>

{% endhighlight %}







### displayInline `boolean`
{:#members:displayinline}








This property allows to embed the popup in the order of DOM element flow . When we set the value as true, the color picker popup is always in visible state.




#### Default Value







* false








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set displayInline API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",  displayInline: true});
        </script>

{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








This property allows to change the control in enabled or disabled state.




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set enabled API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",  enabled: false});
        </script>

{% endhighlight %}







### enableOpacity `boolean`
{:#members:enableopacity}








This property allows to enable or disable the opacity slider in the color picker control




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set enableOpacity API during initialization  
        $('#colorPick').ejColorPicker({ value: "#278787", enableOpacity: false });
        </script>       

{% endhighlight %}



### htmlAttributes `object`
{:#members:htmlattributes}

It allows to define the characteristics of the ColorPicker control. It will helps to extend the capability of an HTML element.


#### Default Value




* {}




#### Example



{% highlight html %}
 
        <input type="text" id="colorPick"/> 
        
        <script>
        // Set HtmlAttributes to Button on initialization. 
                $('#colorPick').ejColorPicker({ htmlAttributes : {disabled:"disabled"}});       
        </script>

{% endhighlight %}




### modelType `enum|string`
{:#members:modeltype}



<ts name="ej.ColorPicker.ModelType"/>


Specifies the model type to be rendered initially in the color picker control. See below to get available ModelType


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Palette</td>
<td class="description">support palette type mode in color picker.</td>
</tr>
<tr>
<td class="name">
Picker</td>
<td class="description">support palette type mode in color picker.</td>
</tr>
</tbody>
</table>


#### Default Value







* ej.ColorPicker.ModelType.Default








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set modelType API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette"});
        </script>

{% endhighlight %}







### opacityValue `number|string`
{:#members:opacityvalue}








This property allows to change the opacity value .The selected color opacity will be adjusted by using this opacity value.




#### Default Value







* 100








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set opacityValue API during initialization  
        $('#colorPick').ejColorPicker({ value: "#278787", opacityValue: 20 });
        </script>

{% endhighlight %}







### palette `enum|string`
{:#members:palette}



<ts name="ej.ColorPicker.Palette"/>




Specifies the palette type to be displayed at initial time in palette model.There two types of palette model available in ColorPicker control. See below available Palette

<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
BasicPalette</td>
<td class="description">used to show the basic palette</td>
</tr>
<tr>
<td class="name">
CustomPalette</td>
<td class="description">used to show the custompalette</td>
</tr>
</tbody>
</table>



#### Default Value







* ej.ColorPicker.Palette.BasicPalette








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set palette API during initialization 
        $('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", palette: "basicpalette"});
        </script>

{% endhighlight %}







### presetType `enum|string`
{:#members:presettype}


<ts name="ej.ColorPicker.Presets"/>




This property allows to define the preset model to be rendered initially in palette type.It consists of 12 different types of presets. Each presets have 50 colors. See below available Presets


<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Basic</td>
<td class="description">used to show the basic presets</td>
</tr>
<tr>
<td class="name">
CandyCrush</td>
<td class="description">used to show the CandyCrush colors presets</td>
</tr>
<tr>
<td class="name">
Citrus</td>
<td class="description">used to show the Citrus colors presets</td>
</tr>
<tr>
<td class="name">
FlatColors</td>
<td class="description">used to show the FlatColors presets</td>
</tr>
<tr>
<td class="name">
Misty</td>
<td class="description">used to show the Misty presets</td>
</tr>
<tr>
<td class="name">
MoonLight</td>
<td class="description">used to show the MoonLight presets</td>
</tr>
<tr>
<td class="name">
PinkShades</td>
<td class="description">used to show the PinkShades presets</td>
</tr>
<tr>
<td class="name">
Sandy</td>
<td class="description">used to show the Sandy presets</td>
</tr>
<tr>
<td class="name">
SeaWolf</td>
<td class="description">used to show the Seawolf presets</td>
</tr>
<tr>
<td class="name">
Vintage</td>
<td class="description">used to show the Vintage presets</td>
</tr>
<tr>
<td class="name">
WebColors</td>
<td class="description">used to show the WebColors presets</td>
</tr>
</tbody>
</table>

#### Default Value







* ej.ColorPicker.Presets.Basic








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set presetType API during initialization 
        $('#colorPick').ejColorPicker({ value: "#278787", modelType: "palette", presetType: "vintage"});
        </script>

{% endhighlight %}

### showApplyCancel `boolean`
{:#members:showapplycancel}


Allows to show/hides the apply and cancel buttons in ColorPicker control




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showApplyCancel API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", showApplyCancel: false});
        </script>

{% endhighlight %}


### showClearButton `boolean`
{:#members:showclearbutton}


Allows to show/hides the clear button in ColorPicker control




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showClearButton API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", showClearButton: false});
        </script>

{% endhighlight %}






### showPreview `boolean`
{:#members:showpreview}


This property allows to provides live preview support for current cursor selection color and selected color.




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showPreview API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", showPreview: false});
        </script>

{% endhighlight %}







### showRecentColors `boolean`
{:#members:showrecentcolors}








This property allows to store the color values in custom list.The ColorPicker will keep up to 11 colors in a custom list.By clicking the add button, the selected color from picker or palette will get added in the recent color list.




#### Default Value







* false








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showRecentColors API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   showRecentColors: true});
        </script>

{% endhighlight %}



### showSwitcher `boolean`
{:#members:showswitcher}


Allows to show/hides the switcher button in ColorPicker control.It helps to switch palette or picker mode in colorpicker. 




#### Default Value







* true








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showSwitcher API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", showSwitcher: false});
        </script>

{% endhighlight %}



### showTooltip `boolean`
{:#members:showtooltip}








This property allows to shows tooltip to notify the slider value in color picker control.




#### Default Value







* false








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set showTooltip API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787", showTooltip: true});
        </script>

{% endhighlight %}







### toolIcon `string`
{:#members:toolicon}








Specifies the toolIcon to be displayed in dropdown control color area.




#### Default Value







* null








#### Example



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
        </style>

{% endhighlight %}







### tooltipText `object`
{:#members:tooltiptext}








This property allows to define the customized text or content to displayed when mouse over the following elements. This property also allows to use the culture values.




#### Default Value







* { switcher: "Switcher", addbutton: "Add Color", basic: "Basic", monochrome: "Mono Chrome", flatcolors: "Flat Color", seawolf: "Sea Wolf", webcolors: "Web Colors", sandy: "Sandy", pinkshades: "Pink Shades", misty: "Misty", citrus: "Citrus", vintage: "Vintage", moonlight: "Moon Light", candycrush: "Candy Crush", currentcolor: "Current Color", selectedcolor: "Selected Color" }



### tooltipText.switcher `string`
{:#members:tooltiptext-switcher}

Sets the tooltip text for the switcher button.

### tooltipText.addbutton `string`
{:#members:tooltiptext-addbutton}

Sets the tooltip text for the add button.

### tooltipText.basic `string`
{:#members:tooltiptext-basic}

Sets the tooltip text for the basic preset.

### tooltipText.monochrome `string`
{:#members:tooltiptext-monochrome}

Sets the tooltip text for the mono chrome preset.

### tooltipText.flatcolors `string`
{:#members:tooltiptext-flatcolors}

Sets the tooltip text for the flat colors preset.

### tooltipText.seawolf `string`
{:#members:tooltiptext-seawolf}

Sets the tooltip text for the sea wolf preset.

### tooltipText.webcolors `string`
{:#members:tooltiptext-webcolors}

Sets the tooltip text for the web colors preset.

### tooltipText.sandy `string`
{:#members:tooltiptext-sandy}

Sets the tooltip text for the sandy preset.

### tooltipText.pinkshades `string`
{:#members:tooltiptext-pinkshades}

Sets the tooltip text for the pink shades preset.

### tooltipText.misty `string`
{:#members:tooltiptext-misty}

Sets the tooltip text for the misty preset.

### tooltipText.citrus `string`
{:#members:tooltiptext-citrus}

Sets the tooltip text for the citrus preset.

### tooltipText.vintage `string`
{:#members:tooltiptext-vintage}

Sets the tooltip text for the vintage preset.

### tooltipText.moonlight `string`
{:#members:tooltiptext-moonlight}

Sets the tooltip text for the moon light preset.

### tooltipText.candycrush `string`
{:#members:tooltiptext-candycrush}

Sets the tooltip text for the candy crush preset.

### tooltipText.currentcolor `string`
{:#members:tooltiptext-currentcolor}

Sets the tooltip text for the current color area.

### tooltipText.selectedcolor `string`
{:#members:tooltiptext-selectedcolor}

Sets the tooltip text for the selected color area.

#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set tooltipText API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787",   tooltipText: { switcher: "Switch",  currentcolor: "New Color", selectedcolor: "Old Color" }});
        </script>

{% endhighlight %}







### value `string`
{:#members:value}








Specifies the color value for color picker control, the value is in hexadecimal form with prefix of "#".




#### Default Value







* null








#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        //To set value API during initialization
        $('#colorPick').ejColorPicker({ value: "#278787"});
        </script>

{% endhighlight %}





## Methods








### disable()
{:#methods:disable}








Disables the color picker control





#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        colorObj.disable(); // disables the colorPicker
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // disables the colorPicker
        $("#colorPick").ejColorPicker("disable");
        </script>  

 {% endhighlight %}







### enable()
{:#methods:enable}








Enable the color picker control





#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        colorObj.enable(); // enables the colorPicker
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // enable the colorPicker
        $("#colorPick").ejColorPicker("enable");
        </script>      

 {% endhighlight %}







### getColor()
{:#methods:getcolor}








Gets the selected color in RGB format

####Returns
object



#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        var color=colorObj.getColor(); // gets the selected color in RGB format
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // gets the selected color in RGB format
        var color=$("#colorPick").ejColorPicker("getColor");
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script>    

{% endhighlight %}







### getValue()
{:#methods:getvalue}








Gets the selected color value as string



####Returns

string

#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        alert(colorObj.getValue()); // gets the selected color value as string
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // gets the selected color value as string
        alert($("#colorPick").ejColorPicker("getValue"));
        </script>      

{% endhighlight %}







### hexCodeToRGB()
{:#methods:hexcodetorgb}


To Convert color value from hexCode to RGB


####Returns

object



#### Example



{% highlight html %}
        
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        var color=colorObj.hexCodeToRGB("#278787"); // Convert color value from hexCode to RGB
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Convert color value from hexCode to RGB
        var color=$("#colorPick").ejColorPicker("hexCodeToRGB","#278787");
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script>      

 {% endhighlight %}







### hide()
{:#methods:hide}








Hides the ColorPicker popup, if in opened state.





#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        colorObj.hide(); // hide the ColorPicker popup
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // hide the ColorPicker popup
        $("#colorPick").ejColorPicker("hide");
        </script>      

 {% endhighlight %}







### HSVToRGB()
{:#methods:hsvtorgb}








Convert color value from HSV to RGB


####Returns

object





#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        var color=colorObj.HSVToRGB({h:230,s:98,v:98}); // Convert color value from HSV to RGB
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Convert color value from HSV to RGB        
        var color=$("#colorPick").ejColorPicker("HSVToRGB","{h:230,s:98,v:98}");
        alert("Red="+color.r+", Green="+color.g+", Blue="+color.b);
        </script>   

{% endhighlight %}







### RGBToHEX()
{:#methods:rgbtohex}








Convert color value from RGB to HEX


####Returns

string


#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        alert(colorObj.RGBToHEX(colorObj.getColor())); // Convert color value from RGB to HEX
        </script> 

{% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        // Convert color value from RGB to HEX
        alert($("#colorPick").ejColorPicker("RGBToHEX",colorObj.getColor()));
        </script>      


 {% endhighlight %}







### RGBToHSV()
{:#methods:rgbtohsv}








Convert color value from RGB to HSV


####Returns

object


#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        var color=colorObj.RGBToHSV({r:39,g:135,b:135}); // Convert color value from RGB to HSV
        alert("H="+color.r+", S="+color.g+", V="+color.b);
        </script>

 {% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Convert color value from RGB to HSV        
        var color=$("#colorPick").ejColorPicker("RGBToHSV","{r:39,g:135,b:125}");
        alert("H="+color.r+", S="+color.g+", V="+color.b);
        </script>   

{% endhighlight %}







### show()
{:#methods:show}








Open the ColorPicker popup.





#### Example



{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // Create ColorPicker instance
        var colorObj = $("#colorPick").data("ejColorPicker");
        colorObj.show(); // open the ColorPicker popup
        </script>

 {% endhighlight %}


{% highlight html %}
   
        <input type="text" id="colorPick"/> 
        
        <script>
        // Create Color picker
        $('#colorPick').ejColorPicker({ value: "#278787" });
        // open the ColorPicker popup
        $("#colorPick").ejColorPicker("show");
        </script>      

{% endhighlight %}





## Events








### change
{:#events:change}



Fires after Color value has been changed successfully.If the user want to perform any operation after the color value changed then the user can make use of this change event.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<tr>
<td class="name">
changeFrom</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return the previous color value</td>
</tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ColorPicker.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return the changed color value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>





#### Example



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
        </script>

{% endhighlight %}







### close
{:#events:close}








Fires after closing the color picker popup.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ColorPicker.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



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
        </script>

{% endhighlight %}







### create
{:#events:create}








Fires after Color picker control is created. If the user want to perform any operation after the color picker control creation then the user can make use of this create event.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><ts ref="ej.ColorPicker.Model"/>

model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



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
        </script>

{% endhighlight %}







### destroy
{:#events:destroy}








Fires after Color picker control is destroyed. If the user want to perform any operation after the color picker control destroyed then the user can make use of this destroy event.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ColorPicker.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example



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
        </script>

{% endhighlight %}







### open
{:#events:open}








Fires after opening the color picker popup

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ColorPicker.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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
        </script>

{% endhighlight %}







### select
{:#events:select}








Fires after Color value has been selected successfully. If the user want to perform any operation after the color value selected then the user can make use of this select event.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
argument</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">Event parameters from color picker
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.ColorPicker.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the color picker model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
value</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return the selected color value</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



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
        </script>

{% endhighlight %}




