---
layout: post
title: Properties, Methods and Events of ejTile Widget
description: API reference for ejTile
documentation: API
platform: js
keywords: Tile, ejTile, syncfusion, Tile api 
---

# ejTile



The Web Tiles are simple, opaque rectangles or squares and they are arrayed on the start screen in a grid-like pattern. Tapping or selecting a Tile, launches the app or does some other action that is represented by the Tile. Tiles are arranged in a group separated by columns that looks like a start screen of a device and it can be either static or live.


#### Syntax

{% highlight javascript %}

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


* module:ej.tile




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
 
 <script>
//Get or set the enabled, after initialization:
// Get the enabled API value.
 $("#tile").ejTile("option", "badge.enabled");                  
// Set the enabled API
$("#tile").ejTile("option", "badge.enabled", true);  
</script>        
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
<script>
//Get or set the maxValue, after initialization:
// Get the maxValue API value.
 $("#tile").ejTile("option", "badge.maxValue");                 
// Set the maxValue API
$("#tile").ejTile("option", "badge.maxValue", 3);           
</script>
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
<script>
//Get or set the minValue, after initialization:
// Get the minValue API value.
 $("#tile").ejTile("option", "badge.minValue");                 
// Set the minValue API
$("#tile").ejTile("option", "badge.minValue", 5);           
</script>
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
<script>
//Get or set the badge text, after initialization:
// Get the badge text API value.
 $("#tile").ejTile("option", "badge.text");                     
// Set the badge text API
$("#tile").ejTile("option", "badge.text", "ten"); 
</script>           
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
<script>
//Get or set the value, after initialization:
// Get the value API value.
 $("#tile").ejTile("option", "badge.value");                    
// Set the value API
$("#tile").ejTile("option", "badge.value", 5); 
</script>           {% endhighlight %}


### badge.position `enum`
{:#members:badge-position}


<ts name = "ej.Tile.BadgePosition"/>

Sets position for tile badge.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
topright</td>
<td class="description">To set the topright position of tile badge</td>
</tr>
<tr>
<td class="name">
bottomright</td>
<td class="description">To set the bottomright of tile badge</td>
</tr>
</tbody>
</table>


#### Default Value

 * “bottomright”
 
 
#### Example
 
{% highlight html %}
 
// Set position on initialization. 
// To set position API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, position:"bottomright" }}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the position, after initialization:
// Get the position API value.
 $("#tile").ejTile("option", "badge.position");                    
// Set the position API
$("#tile").ejTile("option", "badge.position","bottomright"); </script>           {% endhighlight %}


### caption `object`
{:#members:caption}


Section for caption specific functionalities and it represents the notification for tile items.

### caption.enabled `boolean`
{:#members:caption-enabled}

Specifies whether the tile text to be shown or hidden.


#### Default Value


* true

#### Example



{% highlight html %}
 
// Set enabled on initialization. 
// To set enabled API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", caption: { enabled: true},tileSize:'medium'}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the enabled, after initialization:
// Get the enabled API value.
 $("#tile").ejTile("option", "caption.enabled");                       
// Set the enabled API
$("#tile").ejTile("option", "caption.enabled", false);</script>            {% endhighlight %}


### caption.text `string`
{:#members:caption-text}

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
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", caption:{text:"Settings"},tileSize:'medium'}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the text, after initialization:
// Get the text API value.
 $("#tile").ejTile("option", "caption.text");                   
// Set the text API
$("#tile").ejTile("option", "caption.text", "Settings");</script>           {% endhighlight %}


### caption.alignment `enum`
{:#members:caption-alignment}


<ts name = "ej.Tile.CaptionAlignment"/>


It is used to align the text of a tile.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Normal</td>
<td class="description">To set the normal alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="description">To set the left alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="description">To set the right alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="description">To set the center alignment of text in tile control</td>
</tr>
</tbody>
</table>



#### Default Value


* "normal"

#### Example



{% highlight html %}
 
// Set alignment on initialization. 
// To set alignment API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", caption:{alignment:"left"},tileSize:'medium' }); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the alignment, after initialization:
// Get the alignment API value.
 $("#tile").ejTile("option", "caption.alignment");                  
// Set the alignment API
$("#tile").ejTile("option", "caption.alignment", "left");</script>           {% endhighlight %}


### caption.position `enum`
{:#members:caption-position}


<ts name = "ej.Tile.CaptionPosition"/>

It is used to specify the caption position like Inner top,  inner bottom and outer.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Innertop</td>
<td class="description">To set the inner top position of the tile text</td>
</tr>
<tr>
<td class="name">
Innerbottom</td>
<td class="description">To set the inner bottom position of the tile text</td>
</tr>
<tr>
<td class="name">
Outer</td>
<td class="description">To set the outer position of the tile text</td>
</tr>
</tbody>
</table>

 
#### Default Value


* "Innerbottom"


#### Example



{% highlight html %}
 
// Set position on initialization. 
// To set position API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", caption:{position:"innerbottom"},tileSize:'medium' }); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the position, after initialization:
// Get the position API value.
 $("#tile").ejTile("option", "caption.position");                  
// Set the position API
$("#tile").ejTile("option", "caption.position", "innerbottom");</script>            {% endhighlight %}

### caption.icon `string`
{:#members:caption-icon}


sets the icon instead of text.

#### Default Value


* null


#### Example



{% highlight html %}
 
// Set icon on initialization. 
// To set icon API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", caption:{icon:'e-icon-images'},tileSize:'medium'}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the icon, after initialization:
// Get the icon API value.
 $("#tile").ejTile("option", "caption.icon");                      
// Set the liveTile imageUrl API
$("#tile").ejTile("option", "caption.icon",);</script>  {% endhighlight %}

### captionTemplateId[Deprecated] `string`
{:#members:captiontemplateid}


Specifies the tile caption in outside of template content.

N>Since it is deprecated.


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
<script>
//Get or set the captionTemplateId, after initialization:
// Get the captionTemplateId API value.
 $("#tile").ejTile("option", "captionTemplateId");                      
// Set the captionTemplateId API
$("#tile").ejTile("option", "captionTemplateId", "sample");</script>            {% endhighlight %}


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
<script>
//Get or set the cssClass, after initialization:
// Get the cssClass API value.
 $("#tile").ejTile("option", "cssClass");                       
// Set the cssClass API
$("#tile").ejTile("option", "cssClass", "customclass");</script>           {% endhighlight %}


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
<script>
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.
 $("#tile").ejTile("option", "enablePersistence");                      
// Set the enablePersistence API
$("#tile").ejTile("option", "enablePersistence", true);</script>            {% endhighlight %}


### height `number`
{:#members:height}

Customize the tile size height.




#### Default Value

* null

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
<script>
//Get or set the height, after initialization:
// Get the height API value.
 $("#tile").ejTile("option", "height");                 
// Set the width API
$("#tile").ejTile("option", "height", 300);</script>            {% endhighlight %}


### imageClass `string`
{:#members:imageclass}


Specifies Tile imageClass, using this property we can give images for each tile through CSS classes.

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
<script>
//Get or set the imageClass, after initialization:
// Get the imageClass API value.
 $("#tile").ejTile("option", "imageClass");                     
// Set the imageClass API
$("#tile").ejTile("option", "imageClass", "sample"); </script>          
 {% endhighlight %}


### imagePosition `enum`
{:#members:imageposition}


<ts name = "ej.Tile.ImagePosition"/>

Specifies the position of tile image.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Center</td>
<td class="description">To set the center position of tile image</td>
</tr>
<tr>
<td class="name">
Top</td>
<td class="description">To set the top position of tile image</td>
</tr>
<tr>
<td class="name">
Bottom</td>
<td class="description">To set the bottom position of tile image</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="description">To set the right position of tile image</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="description">To set the left position of tile image</td>
</tr>
<tr>
<td class="name">
TopLeft</td>
<td class="description">To set the topleft position of tile image</td>
</tr>
<tr>
<td class="name">
TopRight</td>
<td class="description">To set the topright position of tile image</td>
</tr>
<tr>
<td class="name">
BottomRight</td>
<td class="description">To set the bottomright position of tile image</td>
</tr>
<tr>
<td class="name">
BottomLeft</td>
<td class="description">To set the bottomleft position of tile image</td>
</tr>
<tr>
<td class="name">
Fill</td>
<td class="description">To set the fill position of tile image</td>
</tr>
</tbody>
</table>

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
<script>
//Get or set the imagePosition, after initialization:
// Get the imagePosition API value.
 $("#tile").ejTile("option", "imagePosition");                  
// Set the imagePosition API
$("#tile").ejTile("option", "imagePosition", "right");</script>            {% endhighlight %}


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
<script>
//Get or set the imageTemplateId, after initialization:
// Get the imageTemplateId API value.
 $("#tile").ejTile("option", "imageTemplateId");                        
// Set the imageTemplateId API
$("#tile").ejTile("option", "imageTemplateId", "sample");</script>            {% endhighlight %}

### imageUrl `string`
{:#members:imageurl}

Specifies the URL of tile image.

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
<script>
//Get or set the imageUrl, after initialization:
// Get the imageUrl API value.
 $("#tile").ejTile("option", "imageUrl");                       
// Set the imageUrl API
$("#tile").ejTile("option", "imageUrl", "themes/sample/tile/people.png"); </script>           
{% endhighlight %}


### liveTile `object`
{:#members:liveTile}


Section for liveTile specific functionalities.

### liveTile.enabled `boolean`
{:#members:liveTile-enabled}


Specifies whether to enable liveTile or not.




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
<script>
//Get or set the liveTile enabled, after initialization:
// Get the liveTile enabled API value.
 $("#tile").ejTile("option", "liveTile.enabled");                       
// Set the liveTile enabled API
$("#tile").ejTile("option", "liveTile.enabled", true); </script>          
 {% endhighlight %}


### liveTile.imageClass `string`
{:#members:liveTile-imageclass}


Specifies liveTile images in CSS classes.


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
<script> 
//Get or set the liveTile imageClass, after initialization:
// Get the liveTile imageClass API value.
 $("#tile").ejTile("option", "liveTile.imageClass");                    
// Set the liveTile imageClass API
$("#tile").ejTile("option", "liveTile.imageClass", ['img1','img2','img3']);</script>          
 {% endhighlight %}


### liveTile.imageTemplateId `string`
{:#members:liveTile-imagetemplateid}


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
<script>
//Get or set the liveTile imageTemplateId, after initialization:
// Get the liveTile imageTemplateId API value.
 $("#tile").ejTile("option", "liveTile.imageTemplateId");                       
// Set the liveTile imageTemplateId API
$("#tile").ejTile("option", "liveTile.imageTemplateId", ['img1','img2','img3']); </script>       
   {% endhighlight %}


### liveTile.imageUrl `string`
{:#members:liveTile-imageurl}


Specifies liveTile images in CSS classes.

#### Default Value


* null


#### Example



{% highlight html %}
 
// Set liveTile imageUrl on initialization. 
// To set liveTile imageUrl API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'] } }); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the liveTile imageUrl, after initialization:
// Get the liveTile imageUrl API value.
 $("#tile").ejTile("option", "liveTile.imageUrl");                      
// Set the liveTile imageUrl API
$("#tile").ejTile("option", "liveTile.imageUrl", ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png']);</script>           {% endhighlight %}


### liveTile.type `enum`
{:#members:liveTile-type}


<ts name = "ej.Tile.liveTileType"/>

Specifies liveTile type for Tile. See orientation


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Flip</td>
<td class="description">To set flip type of liveTile for tile control</td>
</tr>
<tr>
<td class="name">
Slide</td>
<td class="description">To set slide type of liveTile for tile control</td>
</tr>
<tr>
<td class="name">
Carousel</td>
<td class="description">To set carousel type of liveTile for tile control</td>
</tr>
</tbody>
</table>

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
<script> 
//Get or set the liveTile type, after initialization:
// Get the liveTile type API value.
 $("#tile").ejTile("option", "liveTile.type");                  
// Set the liveTile type API
$("#tile").ejTile("option", "liveTile.type", "carousel");</script>            {% endhighlight %}


### liveTile.updateInterval `number`
{:#members:liveTile-updateinterval}



Specifies time interval between two successive liveTile animation


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
<script>
//Get or set the liveTile updateInterval, after initialization:
// Get the liveTile updateInterval API value.
 $("#tile").ejTile("option", "liveTile.updateInterval");                        
// Set the liveTile updateInterval API
$("#tile").ejTile("option", "liveTile.updateInterval", 1000);</script>            {% endhighlight %}



### liveTile.text `array`
{:#members:liveTile-text}


Sets the text to each living tile


#### Default Value

* Null


#### Example


{% highlight html %}
 
// Set liveTile text on initialization. 
// To set liveTile text API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'], text:["text1","text2","text3"] } }); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the liveTile text, after initialization:
// Get the liveTile text API value.
 $("#tile").ejTile("option", "liveTile.text");                        
// Set the liveTile text API
$("#tile").ejTile("option", "liveTile.text", 1000);</script>           {% endhighlight %}


### showText[Deprecated] `boolean`
{:#members:showtext}

Specifies whether the tile text to be shown or hidden.

N>Since it is deprecated we suggest to use the API “[caption-enabled](#members:caption-enabled)”.


#### Default Value


* true

#### Example



{% highlight html %}
 
// Set showText on initialization. 
// To set showText API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", showText:true}); 
</script>{% endhighlight %}


{% highlight html %}
<script> 
//Get or set the showText, after initialization:
// Get the showText API value.
 $("#tile").ejTile("option", "showText");                       
// Set the showText API
$("#tile").ejTile("option", "showText", false);</script>            {% endhighlight %}


### text[Deprecated] `string`
{:#members:text}


Changes the text of a tile.

N>Since it is deprecated we suggest to use the API “[caption-text](#members:caption-text)”.


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
<script>
//Get or set the text, after initialization:
// Get the text API value.
 $("#tile").ejTile("option", "text");                   
// Set the text API
$("#tile").ejTile("option", "text", "Settings"); </script>          {% endhighlight %}


### textAlignment[Deprecated] `enum`
{:#members:textalignment}


<ts name = "ej.Tile.TextAlignment"/>


It is used to align the text of a tile.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Normal</td>
<td class="description">To set the normal alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Left</td>
<td class="description">To set the left alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="description">To set the right alignment of text in tile control</td>
</tr>
<tr>
<td class="name">
Center</td>
<td class="description">To set the center alignment of text in tile control</td>
</tr>
</tbody>
</table>

 
N>Since it is deprecated we suggest to use the API “[caption-alignment](#members:caption-alignment)”.



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
<script>
//Get or set the textAlignment, after initialization:
// Get the textAlignment API value.
 $("#tile").ejTile("option", "textAlignment");                  
// Set the textAlignment API
$("#tile").ejTile("option", "textAlignment", "left");</script>          {% endhighlight %}

### tileSize `enum`
{:#members:tilesize}


<ts name = "ej.Tile.TileSize"/>

Specifies the size of a tile.  See tileSize


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Medium</td>
<td class="description">To set the medium size for tile control</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="description">To set the small size for tile control</td>
</tr>
<tr>
<td class="name">
Large</td>
<td class="description">To set the large size for tile control</td>
</tr>
<tr>
<td class="name">
Wide</td>
<td class="description">To set the wide size for tile control</td>
</tr>
</tbody>
</table>

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
<script> 
//Get or set the tileSize, after initialization:
// Get the tileSize API value.
 $("#tile").ejTile("option", "tileSize");                       
// Set the tileSize API
$("#tile").ejTile("option", "tileSize", "medium");</script>            {% endhighlight %}

### width `number`
{:#members:width}

Customize the tile size width.


#### Default Value

* null

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
<script> 
//Get or set the width, after initialization:
// Get the width API value.
 $("#tile").ejTile("option", "width");                  
// Set the width API
$("#tile").ejTile("option", "width", 300);</script>            {% endhighlight %}


### showRoundedCorner `boolean`
{:#members:showroundedcorner}

Sets the rounded corner to  tile.

#### Default Value

* false

#### Example


{% highlight html %}
 
// Set showRoundedCorner on initialization. 
// To set showRoundedCorner API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png",showRoundedCorner:true}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the showRoundedCorner, after initialization:
// Get the showRoundedCorner API value.
 $("#tile").ejTile("option", "showRoundedCorner");                       
// Set the showRoundedCorner API
$("#tile").ejTile("option", "showRoundedCorner", false);</script>           {% endhighlight %}



### allowSelection `boolean`
{:#members:allowselection}


Sets allowSelection to  tile.

#### Default Value

* false

#### Example

{% highlight html %}
 
// Set allowSelection on initialization. 
// To set allowSelection API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png",allowSelection:true}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the allowSelection, after initialization:
// Get the allowSelection API value.
 $("#tile").ejTile("option", "allowSelection");                       
// Set the allowSelection API
$("#tile").ejTile("option", "allowSelection", false);</script>           {% endhighlight %}


### backgroundColor `string`
{:#members:backgroundcolor}


Sets the background color to  tile.

#### Default Value


* false

#### Example


{% highlight html %}
 
// Set backgroundColor on initialization. 
// To set backgroundColor API value 
<div id="tile" ></div>
<script> 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png",backgroundColor:"#ffffff"}); 
</script>{% endhighlight %}


{% highlight html %}
<script>
//Get or set the backgroundColor, after initialization:
// Get the backgroundColor API value.
 $("#tile").ejTile("option", "backgroundColor");                       
// Set the backgroundColor API
$("#tile").ejTile("option", "backgroundColor","#ffffff");</script>           {% endhighlight %}


## Methods



### updateTemplate(name)
{:#methods:updatetemplate}



Update the image template of tile item to another one.


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
name</td>
<td class="type">
string</td>
<td class="description">UpdateTemplate by using id</td>
</tr>
</tbody>
</table>


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


Event triggers when the mouseDown happens in the tile

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Tile.Model"/><span class="param-type">boolean</span></td>
<td class="description">returns the tile model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the current tile text</td>
</tr>
<tr>
<td class="name">
index</td>
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



Event triggers when the mouseUp happens in the tile

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Tile.Model"/><span class="param-type">boolean</span></td>
<td class="description">returns the tile model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
text</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the current tile text</td>
</tr>
<tr>
<td class="name">
index</td>
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



