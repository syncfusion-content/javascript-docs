---
layout: post
title: ejRotator
documentation: API
platform: js
metaname: 
metacontent: 
---

The Rotator control displays a set of slides. Each slide may contain images or images with content, or content with user-defined transition between them.










$(element).ejRotator<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code>&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//Initialize the Rotator control in the script as follows.
$(function (){
// document ready
// simple Rotator creation
$("#sliderContent").ejRotator();
});
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.min.js


* module:ej.core.js


* module:ej.data.js


* module:ej.rotator.js




## Members








### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members-allowkeyboardnavigation}








Turns on keyboard interaction with the Rotator items. You must set this property to true to access the following keyboard shortcuts:




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the allowKeyboardNavigation during initialization.                       
        $("#sliderContent").ejRotator({ allowKeyboardNavigation : false});              
&lt;/script&gt;</code>
</pre>






### animationSpeed<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-animationspeed}








Sets the animationSpeed of slide transition.




Default Value:
{:.param}






* 600








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the animationSpeed during initialization.                        
        $("#sliderContent").ejRotator({ animationSpeed : 600});                 
&lt;/script&gt;</code>
</pre>






### animationType<span class="type-signature type string">string</span>
{:#members-animationtype}








Specifies the animationType type for the Rotator Item. animationType options include slide, fastSlide, slowSlide, and other custom easing animationTypes.




Default Value:
{:.param}






* "slide"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the animationType during initialization.                         
        $("#sliderContent").ejRotator({ animationType : "slide" });                     
&lt;/script&gt;</code>
</pre>






### circularMode<span class="type-signature type boolean">boolean</span>
{:#members-circularmode}








Enables the circular mode item rotation.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the circularMode during initialization.                  
        $("#sliderContent").ejRotator({ circularMode : false});         
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}








Specify the CSS class to Rotator to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the CSS class during initialization.                     
        $("#sliderContent").ejRotator({  cssClass : "gradient-lime" });                 
&lt;/script&gt;</code>
</pre>






### dataSource<span class="type-signature type object">object</span>
{:#members-datasource}








Specify the list of data which contains a set of data fields. Each data value is used to render an item for the Rotator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the dataSource during initialization.                    
        $("#sliderContent").ejRotator({ dataSource:window.items });                     
&lt;/script&gt;</code>
</pre>






### delay<span class="type-signature type number">number</span>
{:#members-delay}








Sets the delay between the Rotator Items move after the slide transition.




Default Value:
{:.param}






* 500








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the animationSpeed during initialization.      
  $("#sliderContent").ejRotator({ delay : 600});     
&lt;/script&gt;</code>
</pre>






### displayItemsCount<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-displayitemscount}








Specifies the number of Rotator Items to be displayed.




Default Value:
{:.param}






* "1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the displayItemsCount  during initialization.                    
        $("#sliderContent").ejRotator({ displayItemsCount  : "1"});                     
&lt;/script&gt;</code>
</pre>






### enableAutoPlay<span class="type-signature type boolean">boolean</span>
{:#members-enableautoplay}








Rotates the Rotator Items continuously without user interference.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the enableAutoPlay during initialization.                        
        $("#sliderContent").ejRotator({ enableAutoPlay:true});           
&lt;/script&gt;</code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>
{:#members-enabled}








Enables or disables the Rotator control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the enabled during initialization.                       
        $("#sliderContent").ejRotator({  enabled : true});               
&lt;/script&gt;</code>
</pre>






### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members-enablertl}








Specifies right to left transition of slides.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the enableRTL during initialization.                     
        $("#sliderContent").ejRotator({ enableRTL : false});                    
&lt;/script&gt;</code>
</pre>






### fields<span class="type-signature type object">object</span>
{:#members-fields}








Defines mapping fields for the data items of the Rotator.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the fields during initialization.                        
        $("#sliderContent").ejRotator({ dataSource:window.items, fields: {text:"text",url:"url",linkAttribute:"http://www.google.com",targetAttribute:"blank"}});
&lt;/script&gt;</code>
</pre>






### fields.linkAttribute<span class="type-signature type string">String</span>
{:#members-fields-linkattribute}








Specifies a link for the image.











### fields.targetAttribute<span class="type-signature type string">String</span>
{:#members-fields-targetattribute}








Specifies where to open a given link.











### fields.text<span class="type-signature type string">String</span>
{:#members-fields-text}








Specifies a caption for the image.











### fields.thumbnailText<span class="type-signature type string">String</span>
{:#members-fields-thumbnailtext}








Specifies a caption for the thumbnail image.











### fields.thumbnailUrl<span class="type-signature type string">String</span>
{:#members-fields-thumbnailurl}








Specifies the URL for an thumbnail image.











### fields.url<span class="type-signature type string">String</span>
{:#members-fields-url}








Specifies the URL for an image.











### frameSpace<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-framespace}








Sets the space between the Rotator Items.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the frameSpace during initialization.                    
        $("#sliderContent").ejRotator({ slideWidth:"600px",slideHeight:"400px",displayItemsCount:2, frameSpace:"10px"});                        
&lt;/script&gt;</code>
</pre>






### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members-isresponsive}








Resizes the Rotator when the browser is resized.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the isResponsive during initialization.                  
        $("#sliderContent").ejRotator({ isResponsive : false});                 
&lt;/script&gt;</code>
</pre>






### navigateSteps<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-navigatesteps}








Specifies the number of Rotator Items to navigate on a single click (next/previous/play buttons). The navigateSteps property value must be less than or equal to the displayItemsCount property value.




Default Value:
{:.param}






* "1"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the navigateSteps during initialization.                         
        $("#sliderContent").ejRotator({ navigateSteps : "1"});           
&lt;/script&gt;</code>
</pre>






### orientation<span class="type-signature type enum">enum</span>
{:#members-orientation}








Specifies the orientation for the Rotator control, that is, whether it must be rendered horizontally or vertically. See <a href="global.html#Orientation">Orientation</a>




Default Value:
{:.param}






* ej.Orientation.Horizontal








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the orientation during initialization.                   
        $("#sliderContent").ejRotator({ orientation : ej.Orientation.Horizontal });                     
&lt;/script&gt;</code>
</pre>






### pagerPosition<span class="type-signature type string">string</span> <span class="type-signature type enum">enum</span>
{:#members-pagerposition}








Specifies the position of the showPager in the Rotator Item. See <a href="global.html#PagerPosition">PagerPosition</a>




Default Value:
{:.param}






* "outside"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the pagerPosition during initialization.                         
        $("#sliderContent").ejRotator({ pagerPosition :"outside" });                    
&lt;/script&gt;</code>
</pre>






### query<span class="type-signature type string">string</span>
{:#members-query}








Retrieves data from remote data. This property is applicable only when a remote data source is used.




Default Value:
{:.param}






* null














### showCaption<span class="type-signature type boolean">boolean</span>
{:#members-showcaption}








If the Rotator Item is an image, you can specify a caption for the Rotator Item. The caption text for each Rotator Item must be set by using the title attribute of the respective tag. The caption cannot be displayed if multiple Rotator Items are present.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" title="Nature" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg" title="Bird" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg" title="Sculpture" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" title="Seaview"  /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg" title="Snowfall" /&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the caption during initialization.                       
        $("#sliderContent").ejRotator({showCaption:true});                      
&lt;/script&gt;</code>
</pre>






### showNavigateButton<span class="type-signature type boolean">boolean</span>
{:#members-shownavigatebutton}








Turns on or off the slide buttons (next and previous) in the Rotator Items. Slide buttons are used to navigate the Rotator Items.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the showNavigateButton during initialization.                    
        $("#sliderContent").ejRotator({ showNavigateButton : false});                   
&lt;/script&gt;</code>
</pre>






### showPager<span class="type-signature type boolean">boolean</span>
{:#members-showpager}








Turns on or off the pager support in the Rotator control. The Pager is used to navigate the Rotator Items.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the pager during initialization.                         
        $("#sliderContent").ejRotator({ showPager : false});                    
&lt;/script&gt;</code>
</pre>






### showPlayButton<span class="type-signature type boolean">boolean</span>
{:#members-showplaybutton}








Enable play / pause button on rotator.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the showPlayButton during initialization.                        
        $("#sliderContent").ejRotator({ showPlayButton:true});                  
&lt;/script&gt;</code>
</pre>






### showThumbnail<span class="type-signature type boolean">boolean</span>
{:#members-showthumbnail}








Turns on or off thumbnail support in the Rotator control. Thumbnail is used to navigate between slides. Thumbnail supports only single slide transition You must specify the source for thumbnail elements through the thumbnailSourceID property.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
<!-- Thumbnail Source -->
&lt;ul id="thumbElement"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the showThumbnail during initialization.                         
        $("#sliderContent").ejRotator({ showThumbnail:true, thumbnailSourceID :"thumbElement"});                        
&lt;/script&gt;</code>
</pre>






### slideHeight<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-slideheight}








Sets the height of a Rotator Item.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the slideHeight during initialization.                   
        $("#sliderContent").ejRotator({ slideHeight : "600px"});                        
&lt;/script&gt;</code>
</pre>






### slideWidth<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-slidewidth}








Sets the width of a Rotator Item.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the slideWidth during initialization.                    
        $("#sliderContent").ejRotator({ slideWidth : "600px"});                 
&lt;/script&gt;</code>
</pre>






### startIndex<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members-startindex}








Sets the index of the slide that must be displayed first.




Default Value:
{:.param}






* "0"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the startIndex during initialization.                    
        $("#sliderContent").ejRotator({ startIndex : "1"});                     
&lt;/script&gt;</code>
</pre>






### stopOnHover<span class="type-signature type boolean">boolean</span>
{:#members-stoponhover}








Pause the auto play while hover on the rotator content.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the stopOnHover during initialization.                   
        $("#sliderContent").ejRotator({ enableAutoPlay:true, stopOnHover:true});                        
&lt;/script&gt;</code>
</pre>






### thumbnailSourceID<span class="type-signature type object">object</span>
{:#members-thumbnailsourceid}








Specifies the source for thumbnail elements.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;ul id="thumbElement"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
// Set the thumbnailSourceID during initialization.                     
        $("#sliderContent").ejRotator({ showThumbnail:true, thumbnailSourceID :"thumbElement"});                         
&lt;/script&gt;</code>
</pre>




## Methods








### disable<span class="signature">()</span>
{:#methods-disable}








Disables the Rotator control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //To Disables the Rotator control.
        slideObj.disable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
//To Disables the Rotator control.
 $("#sliderContent").ejRotator("disable");
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>
{:#methods-enable}








Enables the Rotator control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //To Enables the Rotator control.
        slideObj.enable();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
$("#sliderContent").ejRotator("enable");
&lt;/script&gt;</code>
</pre>






### getIndex<span class="signature">()</span>
{:#methods-getindex}








This method is used to get the current slide index.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        // Gets the index value of the current slide.
        slideObj.getIndex();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
        // Gets the index value of the current slide.
 $("#sliderContent").ejRotator("getIndex");
&lt;/script&gt;</code>
</pre>






### gotoIndex<span class="signature">(index)</span>
{:#methods-gotoindex}








This method is used to move a slide to the specified index.

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
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of an slide</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        // Moves the slide to the specified index.
        slideObj.gotoIndex(3);
 &lt;/script&gt;
 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
        // Moves the slide to the specified index.
 $("#sliderContent").ejRotator("gotoIndex",3);
&lt;/script&gt;</code>
</pre>






### pause<span class="signature">()</span>
{:#methods-pause}








This method is used to pause autoplay.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //To Pauses auto play.
        slideObj.pause();       
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
        //To Pause auto play.
 $("#sliderContent").ejRotator("pause");
&lt;/script&gt;</code>
</pre>






### play<span class="signature">()</span>
{:#methods-play}








This method is used to move slides continuously (or start autoplay) in the specified autoplay direction.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //To Starts auto play.
        slideObj.play();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
        //To Starts auto play.
 $("#sliderContent").ejRotator("play");
&lt;/script&gt;</code>
</pre>






### slideNext<span class="signature">()</span>
{:#methods-slidenext}








This method is used to move to the next slide from the current slide. If the current slide is the last slide, then the first slide will be treated as the next slide.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //Moves to the next slide.
        slideObj.slideNext();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
//Moves to the next slide.
 $("#sliderContent").ejRotator("slideNext");
&lt;/script&gt;</code>
</pre>






### slidePrevious<span class="signature">()</span>
{:#methods-slideprevious}








This method is used to move to the previous slide from the current slide. If the current slide is the first slide, then the last slide will be treated as the previous slide.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
//initialize the Rotator object
$("#sliderContent").ejRotator();
        var slideObj = $("#sliderContent").data("ejRotator");
        //Moves to the previous slide.
        slideObj.slidePrevious();
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator();
//Moves to the previous slide.
 $("#sliderContent").ejRotator("slidePrevious");
&lt;/script&gt;</code>
</pre>




## Events








### change
{:#events-change}








This event is fired when the Rotator slides are changed.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>itemId</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">the current rotator id.</td>
</tr>
<tr>
<td class="name"><code>activeItemIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current slide index.</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   change: function (args) {}
}); 
&lt;/script&gt;     </code>
</pre>






### create
{:#events-create}








This event is fired when the Rotator control is initialized.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   create: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






### destroy
{:#events-destroy}








This event is fired when the Rotator control is destroyed.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   destroy: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






### pagerClick
{:#events-pagerclick}








This event is fired when a pager is clicked.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>itemId</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">the current rotator id.</td>
</tr>
<tr>
<td class="name"><code>activeItemIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current slide index.</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   pagerClick: function (args) {}
}); 
&lt;/script&gt;    </code>
</pre>






### start
{:#events-start}








This event is fired when enableAutoPlay is started.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>itemId</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">the current rotator id.</td>
</tr>
<tr>
<td class="name"><code>activeItemIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current slide index.</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   start: function (args) {}
});
&lt;/script&gt;      </code>
</pre>






### stop
{:#events-stop}








This event is fired when autoplay is stopped or paused.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>itemId</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">the current rotator id.</td>
</tr>
<tr>
<td class="name"><code>activeItemIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current slide index.</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   stop: function (args) {}
});    
&lt;/script&gt;  </code>
</pre>






### thumbItemClick
{:#events-thumbitemclick}








This event is fired when a thumbnail pager is clicked.

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
<td class="description last">Event parameters from button
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
<td class="description last">returns the rotator model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>itemId</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">the current rotator id.</td>
</tr>
<tr>
<td class="name"><code>activeItemIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current slide index.</td>
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
&lt;ul id="sliderContent"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;ul id="thumbElement"&gt;
&lt;li&gt;&lt;img src="../images/rotator/nature.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/bird.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/sculpture.jpg"/&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/seaview.jpg" /&gt;&lt;/li&gt;
&lt;li&gt;&lt;img src="../images/rotator/snowfall.jpg"/&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;script&gt;
$("#sliderContent").ejRotator({
   showThumbnail:true,
   thumbnailSourceID:"thumbElement",
   thumbItemClick: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>






<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>



<script type="text/javascript">
prettyPrint();
</script> <script src="scripts/linenumber.js" type="text/javascript">
</script> <script src="scripts/main.js" type="text/javascript">
</script>
