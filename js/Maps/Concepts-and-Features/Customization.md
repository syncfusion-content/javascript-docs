---
layout: post
title: Customization
description: customization
platform: js
control: Maps
documentation: ug
---

# Customization

**Maps** control supports color customization to determine the exact combination of colors for shapes displayed in Maps and tooltip support to display additional information of shape data.

**Shapes Color Customization**

The Map control highly supports the customization of the shape’s color. The shape’s color can be customized using the following ways:

1. Using the fill, stroke and stroke thickness properties.

2. Color Mapping support.

3. Color Palette support.

**Shape Settings** 

The **shapeSettings** defines the basic customization settings of shapes in the map. 

The important property that makes an impact on shape colors is **autoFill**. This **autoFill** property is available in the **shapeSettings**. 

* **fill** - It is used to set the fill color of the shapes in the map.

* **stroke** - It is used to set the border color of the shape in the map.

* **strokeThickness** - It is used to set the border thickness of the shape in the map.

* **highlightColor** - It is used to set the mouse hover color for shapes in the map.

* **highlightBorderWidth** - It is used to set the mouse hover border width for shapes in the map.

* **selectionColor** - It is used to set the selection color for shapes in the map.

The above properties of **shapeSettings** are applied only when **autoFill** property value is false. By map, **autoFill** property value is false.

{% highlight html %}

**[HTML]**
jQuery(function ($) {
           $("#mapContainer").ejMap({
               layers: [
                   {
                       shapeData: usMap,
                       enableMouseHover:true,
                       shapeSettings: {
                           fill: "#9CBF4E",
                           strokeThickness: "0.5",
                           stroke: "White",
                           highlightStroke: "White",
                           highlightColor: "#BC5353",
                           highlightBorderWidth: "1"
                       }
                   }                         
               ]
           });
       });  


{% endhighlight %}







{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img1.png" Caption="Map"%}

**Color Mapping**

The **Color Mapping** support enables the customization of shape colors based on the underlying value of shape received from bounded data.

* **colorValuePath** - It renders the field value that is to be fetched from data for each shape used for determining the shape color.

* **valuePath** - It renders the field value that is to be fetched from data for each shape. This support also provides a tree map-like impact on the map UI. The various types of Color Mapping supported in maps are listed as follows.

* **rangeColorMapping** - It is used to differentiate the shape’s fill based on its underlying value and color ranges. The properties of rangeColorMapping are listed in the following table.

_Property Table_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
from</td><td>
Double</td><td>
Gets or sets start value</td></tr>
<tr>
<td>
to</td><td>
Double</td><td>
Gets or sets end value</td></tr>
<tr>
<td>
color</td><td>
Color</td><td>
Gets or sets the colors to be applied for specific range value containing shapes when enableGradient property value is false.</td></tr>
<tr>
<td>
label</td><td>
String</td><td>
Gets or sets the label for legend when mode property value is ‘default’.</td></tr>
<tr>
<td>
gradientColors</td><td>
Array</td><td>
Gets or sets the start point and end point gradient colors to be applied for specific range value containing shapes when enableGradient property value is set to true.</td></tr>
</table>


{% highlight html %}

**[HTML]**
 jQuery(function ($) {
            $("#mapContainer").ejMap({
                layers: [
                    {
                        shapeData: usMap,
                        shapeDataPath: "name",
                        shapeIdTableField: "name",
                        dataSource:populationData,
                        shapeSettings: {
                            fill: "#9CBF4E",
                            strokeThickness: "0.5",
                            stroke: "White",
                            valuePath: 'population',
                            enableGradient: true,
                            colorMappings:
                            {
                                rangeColorMapping: [
                                    {
                                        from: 500000,
                                        to: 1000000,
                                        gradientColors: ["#9CBF4E", "#B8CE7B"]
                                    },
                                    {
                                        from: 1000001,
                                        to: 5000000,
                                        gradientColors: ["#B8CE7B", "#CBD89A"]
                                    },
                                    {
                                        from: 5000001,
                                        to: 10000000,
                                        gradientColors: ["#CBD89A", "#DEE2B9"]
                                    },
                                    {
                                        from: 10000001,
                                        to: 40000000,
                                        gradientColors: ["#DEE2B9", "#F1ECD8"]
                                    }
                                ]
                            }                                  
                        }
                    }                                                               
                ]
            });
        }); 


{% endhighlight %}

When the underlying object value is 700000, then the fill color of the corresponding shape is set between #9CBF4E and #B8CE7B. 

When the underlying value is below any of the given sorted range or above the sorted range, then the fill is set from fill.

{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img2.png" Caption="Map with fill"%}

* **equalColorMapping** - The equalColorMapping is used to differentiate the shape’s fill based on its underlying value and color. The properties of equalColorMapping is listed in the following table.

_Property Table_

<table>
<tr>
<td>
<b>Property</b></td><td>
<b>Type</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
value</td><td>
String</td><td>
Gets or sets the value.</td></tr>
<tr>
<td>
color</td><td>
String</td><td>
Gets or sets the color for mapping.</td></tr>
</table>
In equal color mapping, value property contains the values of the field set in **colorValuePath** property of shape settings.

Here USA election data is considered as input datasource and stored in “electionData.js”.

{% highlight js %}

<table>
<tr>
<td>
<b>[electionData.js]</b>
var electionData = [
    { State: "Alabama", Candidate: "Romney", Electors: 9 }, 
    { State: "Alaska", Candidate: "Romney", Electors: 3 }, 
    { State: "Arizona", Candidate: "Romney", Electors: 11 }, 
    { State: "Arkansas", Candidate: "Romney", Electors: 6 }, 
    { State: "California", Candidate: "Obama", Electors: 55 }, 
    { State: "Colorado", Candidate: "Obama", Electors: 9 }, 
    { State: "Connecticut", Candidate: "Obama", Electors: 7 }, 
    { State: "Delaware", Candidate: "Obama", Electors: 3 }, 
    { State: "District of Columbia", Candidate: "Obama", Electors: 3 }, 
    { State: "Florida", Candidate: "Obama", Electors: 29 }, 
    { State: "Georgia", Candidate: "Romney", Electors: 16 }, 
    { State: "Hawaii", Candidate: "Obama", Electors: 4 }, 
    { State: "Idaho", Candidate: "Romney", Electors: 4 }, 
    { State: "Illinois", Candidate: "Obama", Electors: 20 }, 
    { State: "Indiana", Candidate: "Romney", Electors: 11 }, 
    { State: "Iowa", Candidate: "Obama", Electors: 6 }, 
    { State: "Kansas", Candidate: "Romney", Electors: 6 }, 
    { State: "Kentucky", Candidate: "Romney", Electors: 8 }, 
    { State: "Louisiana", Candidate: "Romney", Electors: 8 },
    { State: "Maine", Candidate: "Obama", Electors: 4 }, 
    { State: "Maryland", Candidate: "Obama", Electors: 10 },     
    { State: "Massachusetts", Candidate: "Obama", Electors: 11 }, 
    { State: "Michigan", Candidate: "Obama", Electors: 16 }, 
    { State: "Minnesota", Candidate: "Obama", Electors: 10 }, 
    { State: "Mississippi", Candidate: "Romney", Electors: 6 }, 
    { State: "Missouri", Candidate: "Romney", Electors: 10 }, 
    { State: "Montana", Candidate: "Romney", Electors: 3 }, 
    { State: "Nebraska", Candidate: "Romney", Electors: 5 }, 
    { State: "Nevada", Candidate: "Obama", Electors: 6 }, 
    { State: "New Hampshire", Candidate: "Obama", Electors: 4 }, 
    { State: "New Jersey", Candidate: "Obama", Electors: 14 }, 
    { State: "New Mexico", Candidate: "Obama", Electors: 5 },     
    { State: "New York", Candidate: "Obama", Electors: 29 }, 
    { State: "North Carolina", Candidate: "Romney", Electors: 15 }, 
    { State: "North Dakota", Candidate: "Romney", Electors: 3 }, 
    { State: "Ohio", Candidate: "Obama", Electors: 18 }, 
    { State: "Oklahoma", Candidate: "Romney", Electors: 7 }, 
    { State: "Oregon", Candidate: "Obama", Electors: 7 }, 
    { State: "Pennsylvania", Candidate: "Obama", Electors: 20 }, 
    { State: "Rhode Island", Candidate: "Obama", Electors: 4 }, 
    { State: "South Carolina", Candidate: "Romney", Electors: 9 }, 
    { State: "South Dakota", Candidate: "Romney", Electors: 3 }, 
    { State: "Tennessee", Candidate: "Romney", Electors: 11 }, 
    { State: "Texas", Candidate: "Romney", Electors: 38 }, 
    { State: "Utah", Candidate: "Romney", Electors: 6 }, 
    { State: "Vermont", Candidate: "Obama", Electors: 3 }, 
    { State: "Virginia", Candidate: "Obama", Electors: 13 }, 
    { State: "Washington", Candidate: "Obama", Electors: 12 }, 
    { State: "West Virginia", Candidate: "Romney", Electors: 5 }, 
    { State: "Wisconsin", Candidate: "Obama", Electors: 10 }, 
    { State: "Wyoming", Candidate: "Romney", Electors: 3 }] 
</td>
</tr>
<tr>
<td>
<b>[HTML]</b>
jQuery(function($) {            
    $("#mapContainer").ejMap({                
        layers: [
        {
            shapeData: usMap,                        
            shapeDataPath: "State",                        
            shapeIdTableField: "name",                        
            dataSource: electionData,                        
            shapeSettings: 
            {                            
                strokeThickness: 0.5,                            
                autoFill: false,                            
                stroke: "white",                            
                valuePath: "Electors",                            
                colorValuePath: "Candidate",                            
                colorMappings:                            
                {                                
                    equalColorMapping:                                
                    [                                    
                        { value: "Romney", color: "#D84444" },                                    
                        { value: "Obama", color: "#316DB5" }                                
                    ]                            
                }                        
            }                    
        }]            
    });        
}); 
</td>
</tr>
</table>

{% endhighlight %}

{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img3.png" Caption="Map with fill color"%}****

**Color Palette**

When **autoFill** property is set to true, shapes are filled with default colors from built-in palettes or custom palette.

**colorPalette**

The **colorPalette** property determines whether the auto fill colors are fetched from built-in color palettes or custom palette.

The **colorPalette** property can be set with palette1, palette2, palette3 and custompalette values where palette1, palette2 and palette3 are built-in color palettes and default value for this property is “palette1”.

{% highlight html %}

[JS]
[HTML]
jQuery(function($) {
            $("#mapContainer").ejMap({
                layers: [
                    {
                        shapeData: usMap,
                        shapeSettings: {
                            strokeThickness: 0.5,
                            stroke: "white",
                            autoFill: true
                        }
                    }
                ]
            });
        }); 


{% endhighlight %}



{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img4.png" Caption="Map with color palette property"%}

**Custom Palette**

The **customPalette** property is used to set an array of colors to be auto filled in shapes.

This property is enabled only when **colorPalette** property value is set to “custompalette”.

{% highlight html %}

[JS]
[HTML]

jQuery(function ($) {
                $("#mapContainer").ejMap({
layers: [
                    {
                                              // ...
                        ShapeSettings: {
                            // ...
                            autoFill: true,
                        colorPalette: "custompalette",
                        customPalette: ["#E51400", "#A4C400", "#730202",
                          "#008B00", "#EF6535",
                          "#1BA0E2", "#C63477", "#0050EF",
                          "#BF004D", "#AA00FF"]
]                                 

                            // ...
                        }
                                            }
                ]
            });
        }); 


{% endhighlight %}



{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img5.png" Caption="Map with custom palette"%}

**Tooltip**

The tooltip is displayed only when you set showTooltip to “True” in the shape layers. By default, it takes the property of the bound object that is referred in the valuePath and displays its content on hovering the corresponding shape. 

{% highlight html %}

**[HTML]**
      jQuery(function ($) {	
             $("#mapContainer").ejMap({
layers: [
                    {
                                              // ...
                        ShapeSettings: {
                            // ...
                            valuePath: "name",
                            // ...
                        }
                        showTooltip: true
                    }
                ]
            });
        });

 </script> 


{% endhighlight %}



{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img6.png" Caption="Map with Tooltip"%}

**Tooltip Template**

The tooltipTemplate property is used for customizing the template for tooltip.

{% highlight html %}

**[HTML]**
<script type="text/javascript">
      jQuery(function ($) {			
                $("#mapContainer").ejMap({
layers: [
                    {
                                              // ...
                        ShapeSettings: {
                            // ...
                            valuePath: "name",
                            // ...
                        }
                        showTooltip: true,
                       toolTipTemplate: 'myTooltip'

                    }
                ]
            });
        });

 </script>
**[HTML]**
     <div  id="myTooltip" style="display: none;">
         <div >
             <div style="height:40px;width:78px;background:#4586a0;border-radius:3px;">
                 <div style="margin-top:-20px;margin-left:9px;padding-top:3px">
                     <label style="margin-top:-20px;font-weight:normal;font-size:12px;color:white;font-family:Segoe UI;">{{:name}}</label>
                 </div>
                 <div style="height:10px;"></div>
                 <div style="margin-top:-10px;margin-left:9px;">
                     <label style="margin-top:-10px;font-weight:normal;font-size:14px;color:white;font-family:segoe ui light;">{{:population}}</label>
                 </div>
             </div>
         </div>
      </div> 


{% endhighlight %}

The following screenshot illustrates a map control displaying a Tooltip with template.

{% include image.html url="/js/Maps/Concepts-and-Features/Customization_images/Customization_img7.png" Caption="Map with tooltip template"%}

