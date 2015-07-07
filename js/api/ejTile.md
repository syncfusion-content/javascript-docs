---
layout: post
title: ejTile
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Tile control.










$(element).ejTile<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png" }); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core


* module:ej.unobtrusive


* module:ej.data


* module:ej.touch


* module:ej.tilebase




## Members








### badge<span class="type-signature type object">object</span>
{:#badge}








Section for badge specific functionalities.











### badge.enabled<span class="type-signature type boolean">boolean</span>
{:#badge-enabled}








Specifies whether to enable badge or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set enabled on initialization. 
// To set enabled API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enabled, after initialization:
// Get the enabled API value.
 $("#tile").ejTile("option", "badge.enabled");                  
// Set the enabled API
$("#tile").ejTile("option", "badge.enabled", true);            </code>
</pre>






### badge.maxValue<span class="type-signature type number">number</span>
{:#badge-maxValue}








Specifies maximum value for tile badge.




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set maxValue on initialization. 
// To set maxValue API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:5, maxValue:3 } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxValue, after initialization:
// Get the maxValue API value.
 $("#tile").ejTile("option", "badge.maxValue");                 
// Set the maxValue API
$("#tile").ejTile("option", "badge.maxValue", 3);            </code>
</pre>






### badge.minValue<span class="type-signature type number">number</span>
{:#badge-minValue}








Specifies minimum value for tile badge.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set minValue on initialization. 
// To set minValue API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:3, minValue:5 }}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minValue, after initialization:
// Get the minValue API value.
 $("#tile").ejTile("option", "badge.minValue");                 
// Set the minValue API
$("#tile").ejTile("option", "badge.minValue", 5);            </code>
</pre>






### badge.text<span class="type-signature type string">string</span>
{:#badge-text}








Specifies text instead of number for tile badge.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set text on initialization. 
// To set text API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, text:"ten" } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the badge text, after initialization:
// Get the badge text API value.
 $("#tile").ejTile("option", "badge.text");                     
// Set the badge text API
$("#tile").ejTile("option", "badge.text", "ten");            </code>
</pre>






### badge.value<span class="type-signature type number">number</span>
{:#badge-value}








Sets value for tile badge.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set value on initialization. 
// To set value API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", badge: { enabled: true, value:5 }}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the value, after initialization:
// Get the value API value.
 $("#tile").ejTile("option", "badge.value");                    
// Set the value API
$("#tile").ejTile("option", "badge.value", 5);            </code>
</pre>






### captionTemplateId<span class="type-signature type string">string</span>
{:#captionTemplateId}








Specifies the tile caption in outside template content.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set captionTemplateId on initialization. 
// To set captionTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="sample" &gt; Settings
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", captionTemplateId: "sample"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the captionTemplateId, after initialization:
// Get the captionTemplateId API value.
 $("#tile").ejTile("option", "captionTemplateId");                      
// Set the captionTemplateId API
$("#tile").ejTile("option", "captionTemplateId", "sample");            </code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#cssClass}








Sets the root class for Tile theme. This cssClass API helps to use custom skinning option for Tile control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set cssClass on initialization. 
// To set cssClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", cssClass:"customclass"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cssClass, after initialization:
// Get the cssClass API value.
 $("#tile").ejTile("option", "cssClass");                       
// Set the cssClass API
$("#tile").ejTile("option", "cssClass", "customclass");            </code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#enablePersistence}








Saves current model value to browser cookies for state maintains. While refreshing the page retains the model value applies from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set enablePersistence on initialization. 
// To set enablePersistence API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", enablePersistence:true}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.
 $("#tile").ejTile("option", "enablePersistence");                      
// Set the enablePersistence API
$("#tile").ejTile("option", "enablePersistence", true);            </code>
</pre>






### height<span class="type-signature type number">number</span>
{:#height}








Customize the tile size height.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set height on initialization. 
// To set height API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", width:300, height:300 }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the height, after initialization:
// Get the height API value.
 $("#tile").ejTile("option", "height");                 
// Set the width API
$("#tile").ejTile("option", "height", 300);            </code>
</pre>






### imageClass<span class="type-signature type string">string</span>
{:#imageClass}








Specifies Tile imageclass, using this property we can give images for each tile through css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set imageClass on initialization. 
// To set imageClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageClass: "sample"}); 
&lt;/script&gt;
&lt;style&gt;
.sample
{
background-image:url("themes/sample/tile/people.png");
}
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageClass, after initialization:
// Get the imageClass API value.
 $("#tile").ejTile("option", "imageClass");                     
// Set the imageClass API
$("#tile").ejTile("option", "imageClass", "sample");            </code>
</pre>






### imagePosition<span class="type-signature type enum">enum</span>
{:#imagePosition}








Specifies the position of tile image.




Default Value:
{:.param}






* "center"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set imagePosition on initialization. 
// To set imagePosition API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", imagePosition: "right"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imagePosition, after initialization:
// Get the imagePosition API value.
 $("#tile").ejTile("option", "imagePosition");                  
// Set the imagePosition API
$("#tile").ejTile("option", "imagePosition", "right");            </code>
</pre>






### imageTemplateId<span class="type-signature type string">string</span>
{:#imageTemplateId}








Specifies the tile image in outside template content.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set imageTemplateId on initialization. 
// To set imageTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="sample" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageTemplateId: "sample" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageTemplateId, after initialization:
// Get the imageTemplateId API value.
 $("#tile").ejTile("option", "imageTemplateId");                        
// Set the imageTemplateId API
$("#tile").ejTile("option", "imageTemplateId", "sample");            </code>
</pre>






### imageUrl<span class="type-signature type string">string</span>
{:#imageUrl}








Specifies the file name of tile image.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set imageUrl on initialization. 
// To set imageUrl API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageUrl, after initialization:
// Get the imageUrl API value.
 $("#tile").ejTile("option", "imageUrl");                       
// Set the imageUrl API
$("#tile").ejTile("option", "imageUrl", "themes/sample/tile/people.png");            </code>
</pre>






### livetile<span class="type-signature type object">object</span>
{:#livetile}








Section for livetile specific functionalities.











### livetile.enabled<span class="type-signature type boolean">boolean</span>
{:#livetile-enabled}








Specifies whether to enable livetile or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile enabled on initialization. 
// To set liveTile enabled API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageUrl:['themes/sample/tile/people.png','themes/sample/tile/sports.png'] } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile enabled, after initialization:
// Get the liveTile enabled API value.
 $("#tile").ejTile("option", "liveTile.enabled");                       
// Set the liveTile enabled API
$("#tile").ejTile("option", "liveTile.enabled", true);            </code>
</pre>






### livetile.imageClass<span class="type-signature type string">string</span>
{:#livetile-imageClass}








Specifies liveTile images in css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile imageClass on initialization. 
// To set liveTile imageClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageClass: ['img1','img2','img3'] } }); 
&lt;/script&gt;
&lt;style&gt;
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
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageClass, after initialization:
// Get the liveTile imageClass API value.
 $("#tile").ejTile("option", "liveTile.imageClass");                    
// Set the liveTile imageClass API
$("#tile").ejTile("option", "liveTile.imageClass", ['img1','img2','img3']);            </code>
</pre>






### livetile.imageTemplateId<span class="type-signature type string">string</span>
{:#livetile-imageTemplateId}








Specifies liveTile images in templates.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile imageTemplateId on initialization. 
// To set liveTile imageTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="img1" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img2" style="background-image: url('themes/sample/tile/sports.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img3" style="background-image: url('themes/sample/tile/settings.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ renderMode:"windows", liveTile: { enabled: true, imageTemplateId: ['img1','img2','img3'] } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageTemplateId, after initialization:
// Get the liveTile imageTemplateId API value.
 $("#tile").ejTile("option", "liveTile.imageTemplateId");                       
// Set the liveTile imageTemplateId API
$("#tile").ejTile("option", "liveTile.imageTemplateId", ['img1','img2','img3']);            </code>
</pre>






### livetile.imageUrl<span class="type-signature type string">string</span>
{:#livetile-imageUrl}








Specifies liveTile images in css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile imageUrl on initialization. 
// To set liveTile imageUrl API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ renderMode: "windows", livetile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'] } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageUrl, after initialization:
// Get the liveTile imageUrl API value.
 $("#tile").ejTile("option", "liveTile.imageUrl");                      
// Set the liveTile imageUrl API
$("#tile").ejTile("option", "liveTile.imageUrl", ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png']);            </code>
</pre>






### livetile.type<span class="type-signature type enum">enum</span>
{:#livetile-type}








Specifies liveTile type for Tile. i.e flip, slide or carousel




Default Value:
{:.param}






* "flip"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile type on initialization. 
// To set liveTile type API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'], type:"carousel" } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile type, after initialization:
// Get the liveTile type API value.
 $("#tile").ejTile("option", "liveTile.type");                  
// Set the liveTile type API
$("#tile").ejTile("option", "liveTile.type", "carousel");            </code>
</pre>






### livetile.updateInterval<span class="type-signature type number">number</span>
{:#livetile-updateInterval}








Specifies time interval between two successive livetile animation




Default Value:
{:.param}






* 2000








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set liveTile updateInterval on initialization. 
// To set liveTile updateInterval API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({renderMode: "windows", liveTile: { enabled: true, imageUrl: ['themes/sample/tile/people.png','themes/sample/tile/sports.png','themes/sample/tile/settings.png'], updateInterval:1000 } }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile updateInterval, after initialization:
// Get the liveTile updateInterval API value.
 $("#tile").ejTile("option", "liveTile.updateInterval");                        
// Set the liveTile updateInterval API
$("#tile").ejTile("option", "liveTile.updateInterval", 1000);            </code>
</pre>






### showText<span class="type-signature type boolean">boolean</span>
{:#showText}








Specifies whether the tile text to be shown or hidden.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set showText on initialization. 
// To set showText API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", showText:false }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the showText, after initialization:
// Get the showText API value.
 $("#tile").ejTile("option", "showText");                       
// Set the showText API
$("#tile").ejTile("option", "showText", false);            </code>
</pre>






### text<span class="type-signature type string">string</span>
{:#text}








Changes the text of a tile.




Default Value:
{:.param}






* "Text"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set text on initialization. 
// To set text API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", text:"Settings"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the text, after initialization:
// Get the text API value.
 $("#tile").ejTile("option", "text");                   
// Set the text API
$("#tile").ejTile("option", "text", "Settings");            </code>
</pre>






### textAlignment<span class="type-signature type enum">enum</span>
{:#textAlignment}








Aligns the text of a tile. i.e left, right or center.




Default Value:
{:.param}






* "normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set textAlignment on initialization. 
// To set textAlignment API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", textAlignment:"left" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the textAlignment, after initialization:
// Get the textAlignment API value.
 $("#tile").ejTile("option", "textAlignment");                  
// Set the textAlignment API
$("#tile").ejTile("option", "textAlignment", "left");            </code>
</pre>






### tileSize<span class="type-signature type enum">enum</span>
{:#tileSize}








Specifies the size of a tile. i.e small, medium, large or wide.




Default Value:
{:.param}






* "small"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set tileSize on initialization. 
// To set tileSize API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", tileSize:"medium" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the tileSize, after initialization:
// Get the tileSize API value.
 $("#tile").ejTile("option", "tileSize");                       
// Set the tileSize API
$("#tile").ejTile("option", "tileSize", "medium");            </code>
</pre>






### width<span class="type-signature type number">number</span>
{:#width}








Customize the tile size width.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
// Set width on initialization. 
// To set width API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "themes/sample/tile/people.png", width:300,height:300 }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the width, after initialization:
// Get the width API value.
 $("#tile").ejTile("option", "width");                  
// Set the width API
$("#tile").ejTile("option", "width", 300);            </code>
</pre>




## Methods








### updateTemplate<span class="signature">()</span>
{:#updateTemplate}








Update the image template to another one.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="tile" &gt;
&lt;/div&gt; 
&lt;div id="sample1" style="background-image: url('themes/sample/tile/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="sample2" style="background-image: url('themes/sample/tile/sports.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
$(function () {
$("#tile").ejTile({ imageTemplateId: "sample1" }); 
var value = $("#tile").data("ejTile");
value.updateTemplate("sample2");
});
&lt;/script&gt;</code>
</pre>




## Events








### mouseDown
{:#mouseDown}








Event triggers when the mousedown happens in the tile

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
<td class="description last">Event parameters from tile
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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the tile model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current tile text</td>
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
// Define mouseDown event on initialization. 
// To set mouseDown event API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png", 
mouseDown: function (args) { 
//handle the event 
}
}); 
&lt;/script&gt;</code>
</pre>






### mouseUp
{:#mouseUp}








Event triggers when the mouseup happens in the tile

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
<td class="description last">Event parameters from tile
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
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the tile model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current tile text</td>
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
// Define mouseUp event on initialization. 
// To set mouseUp event API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejTile({ imageUrl: "people.png", 
mouseUp: function (args) { 
//handle the event 
}
}); 
&lt;/script&gt;</code>
</pre>



