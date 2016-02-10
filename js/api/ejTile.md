---
layout: post
title: ejTile
description: API reference for ejTile
documentation: API
platform: js
keywords: Tile, ejTile, syncfusion, Tile api 
---

# ejTile



The Web Tiles are simple, opaque rectangles or squares and they are arrayed on the start screen in a grid-like pattern. Tapping or selecting a Tile, launches the app or does some other action that is represented by the Tile. Tiles are arranged in a group separated by columns that looks like a start screen of a device and it can be either static or live.


#### Syntax

{% highlight js %}

$(element).ejTile()

{% endhighlight %}





#### Example



{% highlight html %}
 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png" }); 
</script>{% endhighlight %}


#### Requires


* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.data


* module:ej.touch


* module:ej.tilebase




## Members








### badge `object`
{:#members:badge}








Section for badge specific functionalities and it represents the notification for tile items.











### badge.enabled `boolean`
{:#members:badge-enabled}








Specifies whether to enable badge or not.




#### Default Value







* false








#### Example



{% highlight html %}
 
// Set enabled on initialization. 
// To set enabled API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true } }); 
</script>

{% endhighlight %}


{% highlight html %}
 
//Get or set the enabled, after initialization:
// Get the enabled API value.
 $("#tile").ejTile("option", "badge.enabled");                  
// Set the enabled API
$("#tile").ejTile("option", "badge.enabled", true);          
  {% endhighlight %}







### badge.maxValue `number`
{:#members:badge-maxvalue}








Specifies maximum value for tile badge.




#### Default Value







* 100








#### Example



{% highlight html %}
 
// Set maxValue on initialization. 
// To set maxValue API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:5, maxValue:3 } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the maxValue, after initialization:
// Get the maxValue API value.
 $("#tile").ejTile("option", "badge.maxValue");                 
// Set the maxValue API
$("#tile").ejTile("option", "badge.maxValue", 3);           

 {% endhighlight %}







### badge.minValue `number`
{:#members:badge-minvalue}








Specifies minimum value for tile badge.




#### Default Value







* 1








#### Example



{% highlight html %}
 
// Set minValue on initialization. 
// To set minValue API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:3, minValue:5 }}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the minValue, after initialization:
// Get the minValue API value.
 $("#tile").ejTile("option", "badge.minValue");                 
// Set the minValue API
$("#tile").ejTile("option", "badge.minValue", 5);           

 {% endhighlight %}







### badge.text `string`
{:#members:badge-text}








Specifies text instead of number for tile badge.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set text on initialization. 
// To set text API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, text:"ten" } }); 
</script>
{% endhighlight %}


{% highlight html %}
 
//Get or set the badge text, after initialization:
// Get the badge text API value.
 $("#tile").ejTile("option", "badge.text");                     
// Set the badge text API
$("#tile").ejTile("option", "badge.text", "ten");            
{% endhighlight %}







### badge.value `number`
{:#members:badge-value}








Sets value for tile badge.




#### Default Value







* 1








#### Example



{% highlight html %}
 
// Set value on initialization. 
// To set value API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:5 }}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the value, after initialization:
// Get the value API value.
 $("#tile").ejTile("option", "badge.value");                    
// Set the value API
$("#tile").ejTile("option", "badge.value", 5);            {% endhighlight %}







### captionTemplateId `string`
{:#members:captiontemplateid}








Specifies the tile caption in outside of template content.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set captionTemplateId on initialization. 
// To set captionTemplateId API value 
<div id="tile" ></div>
<div id="sample" > Settings
</div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", captionTemplateId: "sample"}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the captionTemplateId, after initialization:
// Get the captionTemplateId API value.
 $("#tile").ejTile("option", "captionTemplateId");                      
// Set the captionTemplateId API
$("#tile").ejTile("option", "captionTemplateId", "sample");            {% endhighlight %}







### cssClass `string`
{:#members:cssclass}








Sets the root class for Tile theme. This cssClass API helps to use custom skinning option for Tile control. By defining the root class using this API, we need to include this root class in CSS.




#### Default Value







* ""








#### Example



{% highlight html %}
 
// Set cssClass on initialization. 
// To set cssClass API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", cssClass:"customclass"}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the cssClass, after initialization:
// Get the cssClass API value.
 $("#tile").ejTile("option", "cssClass");                       
// Set the cssClass API
$("#tile").ejTile("option", "cssClass", "customclass");            {% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Saves current model value to browser cookies for state maintains. While refreshing the page retains the model value applies from browser cookies.




#### Default Value







* false








#### Example



{% highlight html %}
 
// Set enablePersistence on initialization. 
// To set enablePersistence API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", enablePersistence:true}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.
 $("#tile").ejTile("option", "enablePersistence");                      
// Set the enablePersistence API
$("#tile").ejTile("option", "enablePersistence", true);            {% endhighlight %}







### height `number`
{:#members:height}








Customize the tile size height.




#### Default Value







* "null"








#### Example



{% highlight html %}
 
// Set height on initialization. 
// To set height API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", width:300, height:300 }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the height, after initialization:
// Get the height API value.
 $("#tile").ejTile("option", "height");                 
// Set the width API
$("#tile").ejTile("option", "height", 300);            {% endhighlight %}







### imageClass `string`
{:#members:imageclass}








Specifies Tile imageclass, using this property we can give images for each tile through css classes.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set imageClass on initialization. 
// To set imageClass API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageClass: "sample"}); 
</script>
<style>
.sample
{
background-image:url("themes/sample/tile/people.png");
}
</style>{% endhighlight %}


{% highlight html %}
 
//Get or set the imageClass, after initialization:
// Get the imageClass API value.
 $("#tile").ejTile("option", "imageClass");                     
// Set the imageClass API
$("#tile").ejTile("option", "imageClass", "sample");           
 {% endhighlight %}







### imagePosition `enum`
{:#members:imageposition}








Specifies the position of tile image. See  <a href="global#enum:imageposition">imageposition</a>




#### Default Value







* "center"








#### Example



{% highlight html %}
 
// Set imagePosition on initialization. 
// To set imagePosition API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", imagePosition: "right"}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the imagePosition, after initialization:
// Get the imagePosition API value.
 $("#tile").ejTile("option", "imagePosition");                  
// Set the imagePosition API
$("#tile").ejTile("option", "imagePosition", "right");            {% endhighlight %}







### imageTemplateId `string`
{:#members:imagetemplateid}








Specifies the tile image in outside of template content.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set imageTemplateId on initialization. 
// To set imageTemplateId API value 
<div id="tile" ></div>
<div id="sample" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;">
</div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageTemplateId: "sample" }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the imageTemplateId, after initialization:
// Get the imageTemplateId API value.
 $("#tile").ejTile("option", "imageTemplateId");                        
// Set the imageTemplateId API
$("#tile").ejTile("option", "imageTemplateId", "sample");            {% endhighlight %}







### imageUrl `string`
{:#members:imageurl}








Specifies the url of tile image.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set imageUrl on initialization. 
// To set imageUrl API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png"}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the imageUrl, after initialization:
// Get the imageUrl API value.
 $("#tile").ejTile("option", "imageUrl");                       
// Set the imageUrl API
$("#tile").ejTile("option", "imageUrl", "themes/sample/tile/people.png");            
{% endhighlight %}







### livetile `object`
{:#members:livetile}








Section for livetile specific functionalities.











### livetile.enabled `boolean`
{:#members:livetile-enabled}








Specifies whether to enable livetile or not.




#### Default Value







* false








#### Example



{% highlight html %}
 
// Set liveTile enabled on initialization. 
// To set liveTile enabled API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageUrl:['themes/sample/tile/people.png','themes/sample/tile/sports.png'] } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile enabled, after initialization:
// Get the liveTile enabled API value.
 $("#tile").ejTile("option", "liveTile.enabled");                       
// Set the liveTile enabled API
$("#tile").ejTile("option", "liveTile.enabled", true);           
 {% endhighlight %}







### livetile.imageClass `string`
{:#members:livetile-imageclass}








Specifies liveTile images in css classes.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set liveTile imageClass on initialization. 
// To set liveTile imageClass API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageClass: ['img1','img2','img3'] } }); 
</script>
<style>
.img1
{
background-image:url("themes/sample/tile/people.png");
}
.img2
{
background-image:url("themes/sample/tile/sports.png");
}
.img3
{
background-image:url("themes/sample/tile/people_1.png");
}
</style>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile imageClass, after initialization:
// Get the liveTile imageClass API value.
 $("#tile").ejTile("option", "liveTile.imageClass");                    
// Set the liveTile imageClass API
$("#tile").ejTile("option", "liveTile.imageClass", ['img1','img2','img3']);           
 {% endhighlight %}







### livetile.imageTemplateId `string`
{:#members:livetile-imagetemplateid}








Specifies liveTile images in templates.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set liveTile imageTemplateId on initialization. 
// To set liveTile imageTemplateId API value 
<div id="tile" ></div>
<div id="img1" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;">
</div>
<div id="img2" style="background-image: url('themes/sample/tile/sports.png');height:100%;width:100%;">
</div>
<div id="img3" style="background-image: url('themes/sample/tile/settings.png');height:100%;width:100%;">
</div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageTemplateId: ['img1','img2','img3'] } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile imageTemplateId, after initialization:
// Get the liveTile imageTemplateId API value.
 $("#tile").ejTile("option", "liveTile.imageTemplateId");                       
// Set the liveTile imageTemplateId API
$("#tile").ejTile("option", "liveTile.imageTemplateId", ['img1','img2','img3']);         
   {% endhighlight %}







### livetile.imageUrl `string`
{:#members:livetile-imageurl}








Specifies liveTile images in css classes.




#### Default Value







* null








#### Example



{% highlight html %}
 
// Set liveTile imageUrl on initialization. 
// To set liveTile imageUrl API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode: "windows", livetile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'] } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile imageUrl, after initialization:
// Get the liveTile imageUrl API value.
 $("#tile").ejTile("option", "liveTile.imageUrl");                      
// Set the liveTile imageUrl API
$("#tile").ejTile("option", "liveTile.imageUrl", ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png']);            {% endhighlight %}







### livetile.type `enum`
{:#members:livetile-type}








Specifies liveTile type for Tile. See  <a href="global#enum:livetiletype">orientation</a> 




#### Default Value







* "flip"








#### Example



{% highlight html %}
 
// Set liveTile type on initialization. 
// To set liveTile type API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'], type:"carousel" } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile type, after initialization:
// Get the liveTile type API value.
 $("#tile").ejTile("option", "liveTile.type");                  
// Set the liveTile type API
$("#tile").ejTile("option", "liveTile.type", "carousel");            {% endhighlight %}







### livetile.updateInterval `number`
{:#members:livetile-updateinterval}








Specifies time interval between two successive livetile animation




#### Default Value







* 2000








#### Example



{% highlight html %}
 
// Set liveTile updateInterval on initialization. 
// To set liveTile updateInterval API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'], updateInterval:1000 } }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the liveTile updateInterval, after initialization:
// Get the liveTile updateInterval API value.
 $("#tile").ejTile("option", "liveTile.updateInterval");                        
// Set the liveTile updateInterval API
$("#tile").ejTile("option", "liveTile.updateInterval", 1000);            {% endhighlight %}







### showText `boolean`
{:#members:showtext}








Specifies whether the tile text to be shown or hidden.




#### Default Value







* true








#### Example



{% highlight html %}
 
// Set showText on initialization. 
// To set showText API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", showText:false }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the showText, after initialization:
// Get the showText API value.
 $("#tile").ejTile("option", "showText");                       
// Set the showText API
$("#tile").ejTile("option", "showText", false);            {% endhighlight %}







### text `string`
{:#members:text}








Changes the text of a tile.




#### Default Value







* "Text"








#### Example



{% highlight html %}
 
// Set text on initialization. 
// To set text API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", text:"Settings"}); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the text, after initialization:
// Get the text API value.
 $("#tile").ejTile("option", "text");                   
// Set the text API
$("#tile").ejTile("option", "text", "Settings");            {% endhighlight %}







### textAlignment `enum`
{:#members:textalignment}








Aligns the text of a tile. See  <a href="global#enum:textalignment">textalignment</a> 
 




#### Default Value







* "normal"








#### Example



{% highlight html %}
 
// Set textAlignment on initialization. 
// To set textAlignment API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", textAlignment:"left" }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the textAlignment, after initialization:
// Get the textAlignment API value.
 $("#tile").ejTile("option", "textAlignment");                  
// Set the textAlignment API
$("#tile").ejTile("option", "textAlignment", "left");            {% endhighlight %}







### tileSize `enum`
{:#members:tilesize}








Specifies the size of a tile.  See  <a href="global#enum:tilesize">tilesize</a>.




#### Default Value







* "small"








#### Example



{% highlight html %}
 
// Set tileSize on initialization. 
// To set tileSize API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", tileSize:"medium" }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the tileSize, after initialization:
// Get the tileSize API value.
 $("#tile").ejTile("option", "tileSize");                       
// Set the tileSize API
$("#tile").ejTile("option", "tileSize", "medium");            {% endhighlight %}







### width `number`
{:#members:width}








Customize the tile size width.




#### Default Value







* "null"








#### Example



{% highlight html %}
 
// Set width on initialization. 
// To set width API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", width:300,height:300 }); 
</script>{% endhighlight %}


{% highlight html %}
 
//Get or set the width, after initialization:
// Get the width API value.
 $("#tile").ejTile("option", "width");                  
// Set the width API
$("#tile").ejTile("option", "width", 300);            {% endhighlight %}





## Methods








### updateTemplate()
{:#methods:updatetemplate}








Update the image template of tile item to another one.





#### Example



{% highlight html %}
 
<div id="tile" >
</div> 
<div id="sample1" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;">
</div>
<div id="sample2" style="background-image: url('themes/sample/tile/sports.png');height:100%;width:100%;">
</div>
<script> 
$(function () {
$("#tile").ejTile({ imageTemplateId: "sample1" }); 
var value = $("#tile").data("ejTile");
value.updateTemplate("sample2");
});
</script>{% endhighlight %}





## Events








### mouseDown
{:#events:mousedown}








Event triggers when the mousedown happens in the tile

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from tile
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the tile model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current tile text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the index of current tile item </td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
// Define mouseDown event on initialization. 
// To set mouseDown event API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png", 
mouseDown: function (args) { 
//handle the event 
}
}); 
</script>{% endhighlight %}







### mouseUp
{:#events:mouseup}








Event triggers when the mouseup happens in the tile

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from tile
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the tile model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the current tile text</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the index of current tile item </td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
// Define mouseUp event on initialization. 
// To set mouseUp event API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png", 
mouseUp: function (args) { 
//handle the event 
}
}); 
</script>{% endhighlight %}




