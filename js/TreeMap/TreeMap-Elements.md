---
layout: post
title: TreeMap-Elements
description: treemap elements
platform: js
control: TreeMap
documentation: ug
---

# TreeMap Elements

TreeMap contains various elements such as,

* Legend
* Headers
* Labels

## Legend

You can set the color value of **leaf nodes** using `treeMapLegend`. This legend is appropriate only for the **TreeMap** whose leaf nodes are colored using `rangeColorMapping`.

You can set `showLegend` propery value to **“True”** to enable or disable legend visibility.

### TreeMap Legend

You can decide the size of the legend icons by setting `iconWidth` and `iconHeight` properties of the `treeMapLegend` property avail in **TreeMap**.

### Label for Legend

You can customize the labels of the **legenditem** using `legendLabel` property of `rangeColorMapping`. 

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


### Interactive Legend

The legends can be made interactive with an arrow mark indicating the exact range color in the legend when the mouse hovers over the corresponding treemap items. You can enable this option by setting `mode` property in `legendSettings` value as “interactive” and default value of `mode` property is “default” to enable the normal legend.

#### Title for Interactive Legend

You can provide the title for interactive legend by using `title` property in `legendSettings`.

#### Label for Interactive Legend

You can provide the left and right labels to interactive legend by using `leftLabel` and `rightLabel` properties in `legendSettings`. 


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


## Header

You can set headers for each level by setting the `showHeader` propery of the each **TreeMap** levels. The `headerHeight` property helps to set the height of the header and Group path value determines the header value. You can customize the default header appearance by setting the `headerTemplate` of the **TreeMap** levels.

{% highlight js %}

    <div  id="treemap" style="width: 950px; height: 500px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...             
                levels: [
                    {groupPath: "Continent", groupGap: 2, headerHeight: 25,  headerTemplate: 'headertemplate' }
                ],
                // ...             
            });
        }); 
    </script>     

    <script  id="headertemplate" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:large;" >{{:header}}</label><br />            
        </div>                        
    </script>                      


{% endhighlight %}



![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img2.png)

## Label

You can also set labels for the leaf nodes by setting the `showLabels` property as true. Group path value is displayed as a label for leaf nodes. You can customize the default label appearance by setting the `labelTemplate` of the **TreeMap** levels.

{% highlight js %}

    <div  id="treemap" style="width: 1100px; height: 550px; "></div>
    
    <script type="text/javascript">
        jQuery(function ($) {
            $("#treemapContainer").ejTreeMap({
                // ...                 
                levels: [
                  {groupPath: "Continent", showLabels: true, groupGap: 2, headerHeight: 20,  headerTemplate: 'headertemplate', labelPosition:"topleft", }
                ],  
                leafItemSettings: { labelPath: "Region", showLabels: true},
                legendSettings:{					
				    height:40,
					width:700
			    }             
            });
        }); 
    </script>     

    <script  id="headertemplate" type="application/jsrender">
        <div style="background-color: white; margin:5px">
            <label style="color:black;font-size:medium;" >{{:header}}</label><br />            
        </div>                        
    </script>             


{% endhighlight %}



![](/js/TreeMap/TreeMap-Elements_images/TreeMap-Elements_img3.png)

