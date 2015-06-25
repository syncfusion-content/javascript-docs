---
layout: post
title: ejmTile
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Tile control.










$(element).ejmTile<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png"&gt;&lt;/div&gt;
</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png" }); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.mobile.application


* module:ej.core


* module:ej.unobtrusive


* module:ej.mobile.core


* module:ej.data


* module:ej.touch


* module:ej.tilebase




## Members








### android








Section for android rendermode specific functionalities.











### android.textPosition<span class="type-signature type enum">enum</span>








Specifies the position of the tile text. i.e inner or outer.




Default Value:
{:.param}






* "inner"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the textPosition property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="android" data-ej-android-textposition="outer" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set textPosition on initialization. 
// To set textPosition API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ renderMode:"android", android:{ textPosition:"outer" }, imagePath: "themes/sample/tile", imageUrl:"people.png" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the textPosition, after initialization:
// Get the textPosition API value.
 $("#tile").ejmTile("option", "android.textPosition");                  
// Set the textPosition API
$("#tile").ejmTile("option", "android.textPosition", "outer");            </code>
</pre>






### backgroundColor<span class="type-signature type string">string</span>








Changes the background color of Tile.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the backgroundColor property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-tilesize="medium" data-ej-backgroundcolor="black" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set backgroundColor on initialization. 
// To set backgroundColor API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png", tileSize: "medium", backgroundColor:"black" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the backgroundColor, after initialization:
// Get the backgroundColor API value.
 $("#tile").ejmTile("option", "backgroundColor");                       
// Set the backgroundColor API
$("#tile").ejmTile("option", "backgroundColor", "black");            </code>
</pre>






### badge<span class="type-signature type object">object</span>








Section for badge specific functionalities.











### badge.enabled<span class="type-signature type boolean">boolean</span>








Specifies whether to enable badge or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enabled property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-badge-enabled="true" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set enabled on initialization. 
// To set enabled API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", badge: { enabled: true },imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enabled, after initialization:
// Get the enabled API value.
 $("#tile").ejmTile("option", "badge.enabled");                 
// Set the enabled API
$("#tile").ejmTile("option", "badge.enabled", true);            </code>
</pre>






### badge.maxValue<span class="type-signature type number">number</span>








Specifies maximum value for tile badge.




Default Value:
{:.param}






* 100








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the maxValue property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-badge-enabled="true" data-ej-badge-value="5" data-ej-badge-maxvalue="3" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set maxValue on initialization. 
// To set maxValue API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", badge: { enabled: true, value:5, maxValue:3 },imagePath:"themes/sample/tile"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxValue, after initialization:
// Get the maxValue API value.
 $("#tile").ejmTile("option", "badge.maxValue");                        
// Set the maxValue API
$("#tile").ejmTile("option", "badge.maxValue", 3);            </code>
</pre>






### badge.minValue<span class="type-signature type number">number</span>








Specifies minimum value for tile badge.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the minValue property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-badge-enabled="true" data-ej-badge-value="3" data-ej-badge-minvalue="5"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set minValue on initialization. 
// To set minValue API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", badge: { enabled: true, value:3, minValue:5 } ,imagePath="themes/sample/tile"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minValue, after initialization:
// Get the minValue API value.
 $("#tile").ejmTile("option", "badge.minValue");                        
// Set the minValue API
$("#tile").ejmTile("option", "badge.minValue", 5);            </code>
</pre>






### badge.text<span class="type-signature type string">string</span>








Specifies text instead of number for tile badge.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the text property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-badge-enabled="true" data-ej-badge-text="ten"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set text on initialization. 
// To set text API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", badge: { enabled: true, text:"ten" } ,imagePath:"themes/sample/tile"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the badge text, after initialization:
// Get the badge text API value.
 $("#tile").ejmTile("option", "badge.text");                    
// Set the badge text API
$("#tile").ejmTile("option", "badge.text", "ten");            </code>
</pre>






### badge.value<span class="type-signature type number">number</span>








Sets value for tile badge.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the value property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-badge-enabled="true" data-ej-badge-value="5"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set value on initialization. 
// To set value API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", badge: { enabled: true, value:5 },imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the value, after initialization:
// Get the value API value.
 $("#tile").ejmTile("option", "badge.value");                   
// Set the value API
$("#tile").ejmTile("option", "badge.value", 5);            </code>
</pre>






### captionTemplateId<span class="type-signature type string">string</span>








Specifies the tile text in outside template content.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the captionTemplateId property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-captiontemplateid="sample" &gt;
&lt;/div&gt; 
&lt;div id="sample" &gt; Settings
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set captionTemplateId on initialization. 
// To set captionTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="sample" &gt; Settings
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", captionTemplateId: "sample",imagePath:"themes/sample/tile"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the captionTemplateId, after initialization:
// Get the captionTemplateId API value.
 $("#tile").ejmTile("option", "captionTemplateId");                     
// Set the captionTemplateId API
$("#tile").ejmTile("option", "captionTemplateId", "sample");            </code>
</pre>






### cssClass<span class="type-signature type string">string</span>








Sets the root class for Tile theme. This cssClass API helps to use custom skinning option for Tile control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the text property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-cssclass="customclass"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set cssClass on initialization. 
// To set cssClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", cssClass:"customclass",imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cssClass, after initialization:
// Get the cssClass API value.
 $("#tile").ejmTile("option", "cssClass");                      
// Set the cssClass API
$("#tile").ejmTile("option", "cssClass", "customclass");            </code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Saves current model value to browser cookies for state maintains. While refreshing the page retains the model value applies from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the enablePersistence property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile"  data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-enablepersistence="true"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set enablePersistence on initialization. 
// To set enablePersistence API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", enablePersistence:true,imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.
 $("#tile").ejmTile("option", "enablePersistence");                     
// Set the enablePersistence API
$("#tile").ejmTile("option", "enablePersistence", true);            </code>
</pre>






### height<span class="type-signature type number">number</span>








Customize the tile size height.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the height property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-height=300 data-ej-width=300 data-ej-backgroundcolor="blue"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set height on initialization. 
// To set height API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", width:300,height:300 imagePath:"themes/sample/tile",backgroundColor:"blue" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the height, after initialization:
// Get the height API value.
 $("#tile").ejmTile("option", "height");                        
// Set the height API
$("#tile").ejmTile("option", "height", 300);            </code>
</pre>






### imageClass<span class="type-signature type string">string</span>








Specifies Tile imageclass, using this property we can give images for each tile through css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the imageClass property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageclass="sample"&gt;
&lt;/div&gt;  
&lt;style&gt;
.sample
{
background-image:url("themes/sample/tile/ios7/people.png");
}
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set imageClass on initialization. 
// To set imageClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageClass: "sample" }); 
&lt;/script&gt;
&lt;style&gt;
.sample
{
background-image:url("themes/sample/tile/ios7/people.png");
}
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageClass, after initialization:
// Get the imageClass API value.
 $("#tile").ejmTile("option", "imageClass");                    
// Set the imageClass API
$("#tile").ejmTile("option", "imageClass", "sample");            </code>
</pre>






### imagePath<span class="type-signature type string">string</span>








Specifies the file path of tile image.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the imagePath property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set imagePath on initialization. 
// To set imagePath API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imagePath, after initialization:
// Get the imagePath API value.
 $("#tile").ejmTile("option", "imagePath");                     
// Set the imagePath API
$("#tile").ejmTile("option", "imagePath", "themes/sample/tile");            </code>
</pre>






### imagePosition<span class="type-signature type enum">enum</span>








Specifies the position of tile image.




Default Value:
{:.param}






* "center"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the imagePosition property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-imageposition="right"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set imagePosition on initialization. 
// To set imagePosition API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", imagePosition: "right" ,imagePath:"themes/sample/tile"}); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imagePosition, after initialization:
// Get the imagePosition API value.
 $("#tile").ejmTile("option", "imagePosition");                 
// Set the imagePosition API
$("#tile").ejmTile("option", "imagePosition", "right");            </code>
</pre>






### imageTemplateId<span class="type-signature type string">string</span>








Specifies the tile image in outside template content.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the imageTemplateId property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagetemplateid="sample" &gt;
&lt;/div&gt; 
&lt;div id="sample" style="background-image: url('themes/sample/tile/ios7/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set imageTemplateId on initialization. 
// To set imageTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="sample" style="background-image: url('themes/sample/tile/ios7/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageTemplateId: "sample" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageTemplateId, after initialization:
// Get the imageTemplateId API value.
 $("#tile").ejmTile("option", "imageTemplateId");                       
// Set the imageTemplateId API
$("#tile").ejmTile("option", "imageTemplateId", "sample");            </code>
</pre>






### imageUrl<span class="type-signature type string">string</span>








Specifies the file name of tile image.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the imageUrl property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set imageUrl on initialization. 
// To set imageUrl API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png",imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the imageUrl, after initialization:
// Get the imageUrl API value.
 $("#tile").ejmTile("option", "imageUrl");                      
// Set the imageUrl API
$("#tile").ejmTile("option", "imageUrl", "people.png");            </code>
</pre>






### ios7








Section for ios7 rendermode specific functionalities.











### ios7.textPosition<span class="type-signature type enum">enum</span>








Specifies the position of the tile text. i.e inner or outer.




Default Value:
{:.param}






* "inner"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the textPosition property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="ios7" data-ej-ios7-textposition="outer" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set textPosition on initialization. 
// To set textPosition API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ renderMode:"ios7", ios7:{ textPosition:"outer" }, imagePath: "themes/sample/tile", imageUrl:"people.png" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the textPosition, after initialization:
// Get the textPosition API value.
 $("#tile").ejmTile("option", "ios7.textPosition");                     
// Set the textPosition API
$("#tile").ejmTile("option", "ios7.textPosition", "outer");            </code>
</pre>






### livetile<span class="type-signature type object">object</span>








Section for livetile specific functionalities.











### livetile.enabled<span class="type-signature type boolean">boolean</span>








Specifies whether to enable livetile or not.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile enabled property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="windows" data-ej-imagepath="themes/sample/tile" data-ej-livetile-imageurl="['people.png','sports.png']" data-ej-livetile-enabled="true" data-ej-backgroundcolor="blue" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile enabled on initialization. 
// To set liveTile enabled API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ renderMode:"windows", liveTile: { enabled: true, imageUrl:['people.png','sports.png'] },imagePath:"themes/sample/tile",backgroundColor:"blue" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile enabled, after initialization:
// Get the liveTile enabled API value.
 $("#tile").ejmTile("option", "liveTile.enabled");                      
// Set the liveTile enabled API
$("#tile").ejmTile("option", "liveTile.enabled", true);            </code>
</pre>






### livetile.imageClass<span class="type-signature type string">string</span>








Specifies liveTile images in css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile imageClass property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="windows" data-ej-livetile-imageclass="['img1','img2','img3']" data-ej-livetile-enabled="true" data-ej-backgroundcolor="blue" &gt;
&lt;/div&gt;  
&lt;style&gt;
.img1
{
background-image:url("themes/sample/tile/windows/people.png");
}
.img2
{
background-image:url("themes/sample/tile/windows/sports.png");
}
.img3
{
background-image:url("themes/sample/tile/windows/people_1.png");
}
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile imageClass on initialization. 
// To set liveTile imageClass API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ renderMode:"windows", liveTile: { enabled: true, imageClass: ['img1','img2','img3'] },backgroundColor:"blue" }); 
&lt;/script&gt;
&lt;style&gt;
.img1
{
background-image:url("themes/sample/tile/windows/people.png");
}
.img2
{
background-image:url("themes/sample/tile/windows/sports.png");
}
.img3
{
background-image:url("themes/sample/tile/windows/people_1.png");
}
&lt;/style&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageClass, after initialization:
// Get the liveTile imageClass API value.
 $("#tile").ejmTile("option", "liveTile.imageClass");                   
// Set the liveTile imageClass API
$("#tile").ejmTile("option", "liveTile.imageClass", ['img1','img2','img3']);            </code>
</pre>






### livetile.imageTemplateId<span class="type-signature type string">string</span>








Specifies liveTile images in templates.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile imageTemplateId property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="windows" data-ej-livetile-imagetemplateid="['img1','img2','img3']" data-ej-livetile-enabled="true" data-ej-backgroundcolor="blue" &gt;
&lt;/div&gt;
&lt;div id="img1" style="background-image: url('themes/sample/tile/windows/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img2" style="background-image: url('themes/sample/tile/windows/sports.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img3" style="background-image: url('themes/sample/tile/windows/settings.png');height:100%;width:100%;"&gt;
&lt;/div&gt;                </code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile imageTemplateId on initialization. 
// To set liveTile imageTemplateId API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;div id="img1" style="background-image: url('themes/sample/tile/windows/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img2" style="background-image: url('themes/sample/tile/windows/sports.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="img3" style="background-image: url('themes/sample/tile/windows/settings.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ renderMode:"windows", liveTile: { enabled: true, imageTemplateId: ['img1','img2','img3'] },backgroundColor:"blue" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageTemplateId, after initialization:
// Get the liveTile imageTemplateId API value.
 $("#tile").ejmTile("option", "liveTile.imageTemplateId");                      
// Set the liveTile imageTemplateId API
$("#tile").ejmTile("option", "liveTile.imageTemplateId", ['img1','img2','img3']);            </code>
</pre>






### livetile.imageUrl<span class="type-signature type string">string</span>








Specifies liveTile images in css classes.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile imageUrl property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-backgroundcolor="blue" data-ej-rendermode="windows" data-ej-livetile-enabled="true" data-ej-imagepath="themes/sample/tile" data-ej-livetile-imageurl="['people.png','sports.png','settings.png']"  &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile imageUrl on initialization. 
// To set liveTile imageUrl API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ backgroundColor:"blue",renderMode: "windows", liveTile: { enabled: true, imageUrl: ['people.png','sports.png','settings.png'] },imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile imageUrl, after initialization:
// Get the liveTile imageUrl API value.
 $("#tile").ejmTile("option", "liveTile.imageUrl");                     
// Set the liveTile imageUrl API
$("#tile").ejmTile("option", "liveTile.imageUrl", ['people.png','sports.png','settings.png']);            </code>
</pre>






### livetile.type<span class="type-signature type enum">enum</span>








Specifies liveTile type for Tile. i.e flip, slide or carousel




Default Value:
{:.param}






* "flip"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile type property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="windows" data-ej-backgroundcolor="blue" data-ej-imagepath="themes/sample/tile" data-ej-livetile-enabled="true" data-ej-livetile-imageurl="['people.png','sports.png','settings.png']"  data-ej-livetile-type="carousel"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile type on initialization. 
// To set liveTile type API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({backgroundColor:"blue", renderMode: "windows", liveTile: { enabled: true, imageUrl: ['people.png','sports.png','settings.png'], type:"carousel" },imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile type, after initialization:
// Get the liveTile type API value.
 $("#tile").ejmTile("option", "liveTile.type");                 
// Set the liveTile type API
$("#tile").ejmTile("option", "liveTile.type", "carousel");            </code>
</pre>






### livetile.updateInterval<span class="type-signature type number">number</span>








Specifies time interval between two successive livetile animation




Default Value:
{:.param}






* 2000








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the liveTile updateInterval property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-rendermode="windows" data-ej-backgroundcolor="blue" data-ej-imagepath="themes/sample/tile" data-ej-livetile-enabled="true" data-ej-livetile-imageurl="['people.png','sports.png','settings.png']"  data-ej-livetile-updateinterval=1000&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set liveTile updateInterval on initialization. 
// To set liveTile updateInterval API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ backgroundColor:"blue",renderMode: "windows", liveTile: { enabled: true, imageUrl: ['people.png','sports.png','settings.png'], updateInterval:1000 },imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the liveTile updateInterval, after initialization:
// Get the liveTile updateInterval API value.
 $("#tile").ejmTile("option", "liveTile.updateInterval");                       
// Set the liveTile updateInterval API
$("#tile").ejmTile("option", "liveTile.updateInterval", 1000);            </code>
</pre>






### renderMode<span class="type-signature type enum">enum</span>








Changes the rendering mode of Tile.




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the renderMode property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-rendermode="android" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set renderMode on initialization. 
// To set renderMode API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png", renderMode:"android" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the renderMode, after initialization:
// Get the renderMode API value.
 $("#tile").ejmTile("option", "renderMode");                    
// Set the renderMode API
$("#tile").ejmTile("option", "renderMode", "android");            </code>
</pre>






### showText<span class="type-signature type boolean">boolean</span>








Specifies whether the tile text to be shown or hidden.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the showText property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile"  data-ej-imageurl="people.png" data-ej-showtext=false&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set showText on initialization. 
// To set showText API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", showText:false,imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the showText, after initialization:
// Get the showText API value.
 $("#tile").ejmTile("option", "showText");                      
// Set the showText API
$("#tile").ejmTile("option", "showText", false);            </code>
</pre>






### text<span class="type-signature type string">string</span>








Changes the text of a tile.




Default Value:
{:.param}






* "Text"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the text property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-text="Settings"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set text on initialization. 
// To set text API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", text:"Settings",imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the text, after initialization:
// Get the text API value.
 $("#tile").ejmTile("option", "text");                  
// Set the text API
$("#tile").ejmTile("option", "text", "Settings");            </code>
</pre>






### textAlignment<span class="type-signature type enum">enum</span>








Aligns the text of a tile. i.e left, right or center.




Default Value:
{:.param}






* "normal"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the textAlignment property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-textalignment="left"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set textAlignment on initialization. 
// To set textAlignment API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", textAlignment:"left",imagePath:"themes/sample/tile" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the textAlignment, after initialization:
// Get the textAlignment API value.
 $("#tile").ejmTile("option", "textAlignment");                 
// Set the textAlignment API
$("#tile").ejmTile("option", "textAlignment", "left");            </code>
</pre>






### theme<span class="type-signature type enum">enum</span>








Changes the theme of Tile.




Default Value:
{:.param}






* auto








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the theme property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-theme="dark" &gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set theme on initialization. 
// To set theme API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png", theme:"dark" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the theme, after initialization:
// Get the theme API value.
 $("#tile").ejmTile("option", "theme");                 
// Set the theme API
$("#tile").ejmTile("option", "theme", "dark");            </code>
</pre>






### tileSize<span class="type-signature type enum">enum</span>








Specifies the size of a tile. i.e small, medium, large or wide.




Default Value:
{:.param}






* "small"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the tileSize property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-tilesize="medium" data-ej-backgroundcolor="blue"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set tileSize on initialization. 
// To set tileSize API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", tileSize:"medium",imagePath:"themes/sample/tile",backgroundColor:"blue" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the tileSize, after initialization:
// Get the tileSize API value.
 $("#tile").ejmTile("option", "tileSize");                      
// Set the tileSize API
$("#tile").ejmTile("option", "tileSize", "medium");            </code>
</pre>






### width<span class="type-signature type number">number</span>








Customize the tile size width.




Default Value:
{:.param}






* "null"








Example
{:.example}

<pre class="prettyprint">
<code> 
//Set the width property in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imageurl="people.png" data-ej-imagepath="themes/sample/tile" data-ej-height=300 data-ej-width=300 data-ej-backgroundcolor="blue"&gt;
&lt;/div&gt;  </code>
</pre>
<pre class="prettyprint">
<code> 
// Set width on initialization. 
// To set width API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imageUrl: "people.png", width:300, height:300, imagePath:"themes/sample/tile",backgroundColor:"blue" }); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the width, after initialization:
// Get the width API value.
 $("#tile").ejmTile("option", "width");                 
// Set the width API
$("#tile").ejmTile("option", "width", 300);            </code>
</pre>




## Methods








### updateTemplate<span class="signature">()</span>








Update the image template to another one.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="tile" data-role="ejmtile" data-ej-imagetemplateid="sample1" &gt;
&lt;/div&gt; 
&lt;div id="sample1" style="background-image: url('themes/sample/tile/ios7/people.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;div id="sample2" style="background-image: url('themes/sample/tile/ios7/sports.png');height:100%;width:100%;"&gt;
&lt;/div&gt;
&lt;script&gt; 
$(function () {
var value = $("#tile").data("ejmTile");
value.updateTemplate("sample2");
});
&lt;/script&gt;</code>
</pre>




## Events








### touchEnd








Event triggers when the touchend happens in the tile

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
//Define touchEnd event in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-touchend="touchend" &gt;
&lt;/div&gt;  
&lt;script&gt;
// touchEnd event for tile
function touchend(args){ 
//handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Define touchEnd event on initialization. 
// To set touchEnd event API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png", 
touchEnd: function (args) { 
//handle the event 
}
}); 
&lt;/script&gt;</code>
</pre>






### touchStart








Event triggers when the touchstart happens in the tile

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
//Define touchStart event in unobtrusive way.
&lt;div id="tile" data-role="ejmtile" data-ej-imagepath="themes/sample/tile" data-ej-imageurl="people.png" data-ej-touchstart="touchstart" &gt;
&lt;/div&gt;  
&lt;script&gt;
// touchStart event for tile
function touchstart(args){ 
//handle the event
}
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
// Define touchStart event on initialization. 
// To set touchStart event API value 
&lt;div id="tile" &gt;&lt;/div&gt;
&lt;script&gt; 
// Create Tile control 
$("#tile").ejmTile({ imagePath: "themes/sample/tile", imageUrl: "people.png", 
touchStart: function (args) { 
//handle the event 
}
}); 
&lt;/script&gt;</code>
</pre>



