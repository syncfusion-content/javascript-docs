---
layout: post
title: ejmRadialMenu
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html radialmenu control.





$(element).ejmRadialMenu<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code> //Create radialmenu in unobtrusive way&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Create radialmenu in obtrusive way&lt;script&gt; $(function(){$("#defaultradialmenu").ejmRadialMenu(); });&lt;/script&gt;&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre>



Requires
{:.require}


* module:jQuery

* module:ej.mobile.application

* module:ej.core

* module:ej.unobtrusive

* module:ej.mobile.core

* module:ej.data

* module:ej.touch


## Members




### backImageClass<span class="type-signature type string">string</span>




Renders the back button Image for Radial using class.


Default Value:
{:.param}



* e-m-backimage




Example
{:.example}
<pre class="prettyprint"><code> //Set the backImageClass property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-backimageclass="e-m-backimage" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu backImageClass on initialization. //To set backImageClass API &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "backImageClass":"e-m-backimage" });    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu backImageClass, after initialization:&lt;script&gt;// Gets the backImageClass API.         $("#defaultradialmenu").ejmRadialMenu ("option", "backImageClass");                     // Sets the backImageClass API$("#defaultradialmenu").ejmRadialMenu ("option", "backImageClass", "e-m-backimage");            &lt;/script&gt;</code></pre>



### cssClass<span class="type-signature type string">string</span>




Sets the root class for RadialMenu theme. This cssClass API helps to use custom skinning option for RadialMenu control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the cssClass property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-cssclass="customclass" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu cssClass on initialization. //To set cssClass API  &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "cssClass":"customclass" });    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu cssClass, after initialization:&lt;script&gt;// Gets the cssClass API.                $("#radialmenu").ejmRadialMenu ("option", "cssClass");                 // Sets the cssClass API$("#radialmenu").ejmRadialMenu ("option", "cssClass", "customclass");            &lt;/script&gt;</code></pre>



### enableAnimation<span class="type-signature type boolean">boolean</span>




To enable Animation for Radial Menu.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the enableAnimation property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-enableanimation="true" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu enableAnimation on initialization. //To set enableAnimation API  &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "enableAnimation":true });      });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu enableAnimation, after initialization:&lt;script&gt;// Gets the enableAnimation API.                 $("#radialmenu").ejmRadialMenu ("option", "enableAnimation");                  // Sets the enableAnimation API$("#radialmenu").ejmRadialMenu ("option", "enableAnimation", true);            &lt;/script&gt;</code></pre>



### imageClass<span class="type-signature type string">string</span>




Renders the image for Radial using Class.


Default Value:
{:.param}



* e-m-radialimage




Example
{:.example}
<pre class="prettyprint"><code> //Set the imageClass property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-imagaclass="e-m-radialimage" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu imageClass on initialization. //To set imageClass API  &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "imageClass":"e-m-radialimage" });      });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu imageClass, after initialization:&lt;script&gt;// Gets the imageClass API.              $("#radialmenu").ejmRadialMenu ("option", "imageClass");                       // Sets the imageClass API$("#radialmenu").ejmRadialMenu ("option", "imageClass", "e-m-radialimage");            &lt;/script&gt;</code></pre>



### position<span class="type-signature type enum">enum</span>




Changes the Position of the control.See <a href="global.html#Position">Position</a>


Default Value:
{:.param}



* rightcenter




Example
{:.example}
<pre class="prettyprint"><code> //Set the position property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-position="rightcenter" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu position on initialization. //To set position API value &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "position":"rightcenter" });    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu position, after initialization:&lt;script&gt;// Gets the position API value.          $("#defaultradialmenu").ejmRadialMenu ("option", "position");                  // Sets the position API$("#defaultradialmenu").ejmRadialMenu ("option", "position", "rightcenter");            &lt;/script&gt;</code></pre>



### radius<span class="type-signature type int">int</span>




Specifies the radius of the radialmenu control.


Default Value:
{:.param}



* 150




Example
{:.example}
<pre class="prettyprint"><code> //Set the radius property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-radius="150"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu radius on initialization. //To set radius API value &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "radius":150}); });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu radius, after initialization:&lt;script&gt;// Gets the radius API value.            $("#defaultradialmenu").ejmRadialMenu ("option", "radius");                    // Sets the radius API$("#defaultradialmenu").ejmRadialMenu ("option", "radius", 150);            &lt;/script&gt;</code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Changes the rendering mode. See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the renderMode property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-rendermode="auto" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu renderMode on initialization. //To set renderMode API value &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "renderMode":ej.mobile.RenderMode.Auto });      });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu renderMode, after initialization:&lt;script&gt;// Gets the renderMode API value.                $("#defaultradialmenu").ejmRadialMenu ("option", "renderMode");                        // Sets the renderMode API$("#defaultradialmenu").ejmRadialMenu ("option", "renderMode", ej.mobile.RenderMode.Auto);            &lt;/script&gt;</code></pre>



### theme<span class="type-signature type enum">enum</span>




Specifies the theme. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the theme property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-theme="auto"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu theme on initialization. //To set theme API value &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ "theme":ej.mobile.RenderMode.Auto });   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu renderMode, after initialization:&lt;script&gt;// Gets the theme API value.             $("#defaultradialmenu").ejmRadialMenu ("option", "theme");                     // Sets the theme API$("#defaultradialmenu").ejmRadialMenu ("option", "theme", "ej.mobile.Theme.Auto");            &lt;/script&gt;</code></pre>



### windows




Section for windows rendermode specific functionalities.






### windows.renderDefault<span class="type-signature type boolean">boolean</span>




Specifies whether to render the Radial Menu based on the windowsphone's current accent color and device theme.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the windows renderDefault property in unobtrusive way.&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-windows-renderdefault="true"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Radialmenu windows renderDefault on initialization. //To set windows renderDefault API value &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#defaultradialmenu").ejmRadialMenu({ windows:{ renderDefault: true }});      });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Radialmenu windows renderDefault, after initialization:&lt;script&gt;// Gets the windows renderDefault API value.             $("#defaultradialmenu").ejmRadialMenu ("option", "windows.renderDefault");                     // Sets the windows renderDefault API$("#defaultradialmenu").ejmRadialMenu ("option", "windows.renderDefault", true);            &lt;/script&gt;</code></pre>


## Methods




### hide<span class="signature">()</span>




To hide the redialmenu



Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;$("#defaultradialmenu").ejmRadialMenu ("hide"); &lt;/script&gt;</code></pre>



### menuHide<span class="signature">()</span>




To hide the redialmenu items



Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;$("#defaultradialmenu").ejmRadialMenu ("menuHide");&lt;/script&gt;</code></pre>



### show<span class="signature">()</span>




To Show the redialmenu



Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;$("#defaultradialmenu").ejmRadialMenu ("show");&lt;/script&gt;</code></pre>


## Events




### select




Event triggers when we select an item.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Radialmenu<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Radialmenu model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-select="select" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt; // select event for Radialmenu  function select(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //select event for Radialmenu&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$("#defaultradialmenu").ejmRadialMenu({  select: function (args) { //handle the event}});         &lt;/script&gt;</code></pre>



### touchEnd




Event triggers when the touch end happens.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Radialmenu<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Radialmenu model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-touchend="touchend" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt; // TouchEnd event for Radialmenu  function touchend(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //TouchEnd event for Radialmenu&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$("#defaultradialmenu").ejmRadialMenu({  touchend: function (args) { //handle the event}});         &lt;/script&gt;</code></pre>



### touchStart




Event triggers when the touch start happens.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Radialmenu<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Radialmenu model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu" data-role="ejmradialmenu" data-ej-touchstart="touchstart" &gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt; // touchStart event for Radialmenu  function touchStart(args){ //handle the event}&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //touchStart event for Radialmenu&lt;div &gt;&lt;br /&gt;&lt;p&gt;Syncfusion is the enterprise technology partner of choice for Windows development&lt;/p&gt;&lt;/div&gt;  &lt;div id="defaultradialmenu"&gt;&lt;ul&gt;&lt;li data-ej-imagename="social.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="social"&gt;&lt;/li&gt;&lt;li data-ej-imagename="music.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="music"&gt;&lt;/li&gt;&lt;li data-ej-imagename="direction.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="direction"&gt;&lt;/li&gt;&lt;li data-ej-imagename="message.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="message"&gt;&lt;/li&gt;&lt;li data-ej-imagename="browser.png" data-ej-imagepath="../themes/sample/radialmenu"data-ej-windows-text="browser"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$("#defaultradialmenu").ejmRadialMenu({  touchStart: function (args) { //handle the event}});         &lt;/script&gt;</code></pre>


