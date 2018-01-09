---
layout: post
title: TreeMap-Elements
description: treemap elements
platform: js
control: TreeMap
documentation: ug
api: /api/js/ejtreemap
---

# TreeMap Elements

TreeMap contains various elements such as,

* [`Legend`](../api/ejtreemap#members:legendsettings)
* [`Headers`](../api/ejtreemap#members:header)
* [`Labels`](../api/ejtreemap#members:rangecolormapping-legendlabel)

## Legend

You can set the color value of **leaf nodes** using `treeMapLegend`. This legend is appropriate only for the **TreeMap** whose leaf nodes are colored using `rangeColorMapping`.

You can set `showLegend` property value to **“True”** to enable or disable legend visibility.

### TreeMap Legend

You can customize the treemap legend using following properties

* For customizing the alignment of legend, you can use [`alignment`](../api/ejtreemap#members:legendsettings-alignment) property.

* You can set the legend column count using [`column count`](../api/ejtreemap#members:legendsettings-columncount) property.

* To set the dock position of the legend text, you can use [`dockPosition`]((../api/ejtreemap#members:legendsettings-dockposition)

* You can specify the size of the legend by setting [`height`](../api/ejtreemap#members:legendsettings-height) and [`width`](../api/ejtreemap#members:legendsettings-width) of the `treeMapLegend`.

* You can decide the size of the legend icons by setting [`iconWidth`](../api/ejtreemap#members:legendsettings-iconwidth) and [`iconHeight`](../api/ejtreemap#members:legendsettings-iconheight) properties of the `treeMapLegend` property avail in **TreeMap**.

* You can customize the left and right label text for the legend using [`leftLabel`](../api/ejtreemap#members:legendsettings-leftlabel) and [`rightLabel`](../api/ejtreemap#members:legendsettings-rightlabel) properties.

* To set the legend mode as default or interactive, you can use [`mode`](../api/ejtreemap#members:legendsettings-mode) property.

* Using the property [`template`](../api/ejtreemap#members:legendsettings-template), you can specify template for legend settings.

* To set the legend title, you can use the[`title`](../api/ejtreemap#members:legendsettings-title) property of the `legendSettings`.

### Label for Legend

You can customize the labels of the **legend item** using `legendLabel` property of `rangeColorMapping`. 

{% highlight js %}

       jQuery(function ($) {

            $("#treemapContainer").ejTreeMap({
                dataSource: population_data,
                colorValuePath: "Growth",
                showLegend: true,
                itemsLayoutMode:"Squarified",
                weightValuePath: "Population",
                rangeColorMapping: [
                { color: "#77D8D8", from: "0", to: "1" ,legendLabel:"Range1"},
                { color: "#AED960", from: "0", to: "2",legendLabel:"Range2" },
                { color: "#FFAF51", from: "0", to: "3", legendLabel: "Range3" },
                { color: "#F3D240", from: "0", to: "4", legendLabel: "Range4" }
                ],                   
                levels: [
                  { groupPath: "Continent", groupGap: 5 }
                ],
                legendSettings:{					
					height:40,
					width:700
				}
            });
        });



{% endhighlight %}

![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img1.png)

Try it: [Legend Label](http://jsplayground.syncfusion.com/yaaqbnna)


### Interactive Legend

The legends can be made interactive with an arrow mark indicating the exact range color in the legend when the mouse hovers over the corresponding treemap items. You can enable this option by setting [`mode`](../api/ejtreemap#members:legendsettings-mode) property in [`legend settings`](../api/ejtreemap#members:legendsettings) value as “interactive” and default value of [`mode`](../api/ejtreemap#members:legendsettings-mode) property is “default” to enable the normal legend.

#### Title for Interactive Legend

You can provide the title for interactive legend by using [`title`](../api/ejtreemap#members:legendsettings-title) property in [`legend settings`](../api/ejtreemap#members:legendsettings).

#### Label for Interactive Legend

You can provide the left and right labels to interactive legend by using [`leftLabel`](../api/ejtreemap#members:legendsettings-leftlabel) and [`rightLabel`](../api/ejtreemap#members:legendsettings-rightlabel) properties in [`legend settings`](../api/ejtreemap#members:legendsettings). 


{% highlight js %}

    jQuery(function ($) {
        $("#treemap").ejTreeMap({            
                // ...
                showLegend: true,
                legendSettings: {                                        
                    height: 15,
                    width: 150,                    
                    mode: "interactive",
                    title: "Population",
                    leftLabel: "0.5M",
                    rightLabel: "40M",
                    dockPosition: "top"
                },
                // ...                                   
        }); 
    });

{% endhighlight %}

![](/js/TreeMap/TreeMap-Elements_images/Interactive_Legend.png)

Try it: [Interactive_Legend](http://jsplayground.syncfusion.com/0mfsg1pp)


## Header

You can set headers for each level by setting the [`showHeader`](../api/ejtreemap#members:levels-showheader) property of the each **TreeMap** levels. The [`headerHeight`](../api/ejtreemap#members:levels-headerheight) property helps to set the height of the header and Group path value determines the header value. You can customize the default header appearance by setting the [`header template`](../api/ejtreemap#members:levels-headertemplate) of the **TreeMap** levels.

{% highlight js %}

    <div  id="treemap" style="width: 950px; height: 500px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...             
                levels: [
                    {groupPath: "Continent", groupGap: 2, headerHeight: 25,  headerTemplate: 'Template' }
                ],
                // ...             
            });
        }); 
    </script>     

    <script  id="Template" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:large;" >{{:header}}</label><br />            
        </div>                        
    </script>                      


{% endhighlight %}



![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img2.png)

Try it: [Treemap Header](http://jsplayground.syncfusion.com/vaas20hr)

## Customizing the header

The text in the header can be customized by triggering the event [`headerTemplateRendering`](../api/ejtreemap#events:headertemplaterendering) of the **TreeMap**. This event is triggered before rendering the header template. 

{% highlight js %}

    <div  id="treemap" style="width: 950px; height: 500px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...             
                levels: [
                    {groupPath: "Continent", headerHeight: 25,  headerTemplate: 'Template' }
                ],
                headerTemplateRendering:'loadTemplate',
                // ...             
            });
        }); 
    </script>     

    <script  id="Template" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:large;" >{{:header}}</label><br />            
        </div>                        
    </script> 

    <script>
    function loadTemplate(sender) {
        //...                   
    }
    </script>



{% endhighlight %}


![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img4.png)

## Label

You can also set labels for the leaf nodes by setting the `showLabels` property as true. Group path value is displayed as a label for leaf nodes. You can customize the default label appearance by setting the [`labelTemplate`](../api/ejtreemap#members:levels-labeltemplate) of the **TreeMap** levels.

{% highlight js %}

    <div  id="treemap" style="width: 1100px; height: 550px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...                 
                levels: [
                  {groupPath: "Continent", showLabels: true, groupGap: 2, headerHeight: 20,  headerTemplate: 'Template', labelPosition:"topleft", }
                ],  
                leafItemSettings: { labelPath: "Region", showLabels: true},
                legendSettings:{					
				    height:40,
					width:700
			    }             
            });
        }); 
    </script>     

    <script  id="Template" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:medium;" >{{:header}}</label><br />            
        </div>                        
    </script>             


{% endhighlight %}



![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img3.png)

Try it: [Treemap Label](http://jsplayground.syncfusion.com/ms0n0uuk)

## Customizing the Overflow labels

You can handle the label overflow, by specifying any one of the following values to the property `textOverflow`as

**None**       - It displays the default label text.
**Hide**       - You can hide the label, when it exceeds the header width.
**Wrap**       - You can wrap the label text by letter.
**WrapByWord** - You can wrap the label text by word.


{% highlight js %}

    <div  id="treemap" style="width: 1100px; height: 550px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...                 
                levels: [
                  {groupPath: "Continent", showLabels: true, headerTemplate: 'Template' }
                ],  
                leafItemSettings: { showLabels: true , textOverFlow: "wrap"},                          
            });
        }); 
    </script>     

    <script  id="headertemplate" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:medium;" >{{:header}}</label><br />            
        </div>                        
    </script>             


{% endhighlight %}

## Palette Color Mapping

Treemap is having support for [`palette color mapping`](../api/ejtreemap#members:levels-palattecolormapping). You can set the color for `palette color mapping` using the property [`color`](../api/ejtreemap#members:levels-palattecolormapping-color) in palette color mapping.

{% highlight js %}

//To set the colors of the paletteColorMapping during initialization 
  $("#container").ejTreeMap( {paletteColorMapping{colors: ["red","green","blue", "yellow"]}});
  
{% endhighlight %}
