---
layout: post
title: ejmButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Button control.





$(element).ejmButton<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code> &lt;input  id="button" type="button" /&gt;
&lt;script&gt; // Create Button  $("#button").ejmButton(); $("#button").ejmButton({text:"button"}); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="button"  type="button" data-role="ejmbutton"  data-ej-text="button"/&gt;
</code></pre>



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




### android




Section for android mode specific functionalities.






### android.style<span class="type-signature type enum">enum</span>




Specifies the style of the control in android mode.


Default Value:
{:.param}



* ej.mobile.Button.Android.Style.Normal.




Example
{:.example}
<pre class="prettyprint"><code> // Set the android mode style property in Unobtrusive way.
&lt;input id="button" type="button"  data-role="ejmbutton" data-ej-rendermode="android" data-ej-android-style="normal" data-ej-text="button"  /&gt;
</code></pre><pre class="prettyprint"><code> // To set android mode style property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: "android" });$("#button").ejmButton({ "model.android.style":ej.mobile.Button.Android.Style.Normal });                 &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the android mode style API, after initialization:// Gets the android mode style value  $("#button").ejmButton("option", "model.android.style");                        // Sets the android mode style value $("#button").ejmButton("option", "model.android.style", ej.mobile.Button.Android.Style.Normal); </code></pre>



### contentType<span class="type-signature type enum">enum</span>




Specifies the type of the content. See <a href="global.html#ContentType">ContentType</a>


Default Value:
{:.param}



* ej.mobile.Button.ContentType.Text




Example
{:.example}
<pre class="prettyprint"><code> //Set the contentType property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-contentType="text" /&gt;
</code></pre><pre class="prettyprint"><code> // Set contentType property on initialization. //To set contentType API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ contentType: "text" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the contentType, after initialization:
// Gets the contentType API value.               $("#button").ejmButton("option", "contentType");                       // Sets the contentType API$("#button").ejmButton("option", "contentType", ej.mobile.Button.ContentType.Text);            </code></pre>



### cssClass<span class="type-signature type string">string</span>




Sets the root class for Button theme. This cssClass API helps to use custom skinning option for Button control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the cssClass property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-cssclass="customclass"  /&gt;
</code></pre><pre class="prettyprint"><code> // Set cssClass property on initialization. //To set text API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({ cssClass: "customclass" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the cssClass, after initialization:
// Gets the cssClass API value.          $("#button").ejmButton("option", "cssClass");                  // Sets the cssClass API$("#button").ejmButton("option", "cssClass", "customclass");            </code></pre>



### enabled<span class="type-signature type boolean">boolean</span>




Specifies whether to enable or disable the control.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //Set the enabled property in Unobtrusive way.&lt;input id="button"  type="button" data-role="ejmbutton" data-ej-text="button" data-ej-enabled=false /&gt;
</code></pre><pre class="prettyprint"><code> // Set enabled property on initialization. //To set enabled API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({text:"button"});$("#button").ejmButton({ enabled: false });     &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enabled, after initialization:
// Gets the enabled API value.           $("#button").ejmButton("option", "enabled");   // Sets the enabled API$("#button").ejmButton("option", "enabled", false);            </code></pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>




Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the enablePersistence property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-enablepersistence="true" /&gt;
</code></pre><pre class="prettyprint"><code> // Set enablePersistence property on initialization. //To set enablePersistence API value &lt;input type="button" id="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ enablePersistence: true });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Gets the enablePersistence API value.                 $("#button").ejmButton("option", "enablePersistence");                 // Sets the enablePersistence API$("#button").ejmButton("option", "enablePersistence", true);            </code></pre>



### flat




Section for flat mode specific functionalities.






### flat.style<span class="type-signature type enum">enum</span>




Specifies the style of the control in flat mode.


Default Value:
{:.param}



* ej.mobile.Button.Flat.Style.Normal.




Example
{:.example}
<pre class="prettyprint"><code> // Set the flat mode style property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="flat" data-ej-flat-style="normal" /&gt;
</code></pre><pre class="prettyprint"><code> // To set flat mode style property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({text:"button"});$("#button").ejmButton({renderMode: "flat"});$("#button").ejmButton({ "model.flat.style": ej.mobile.Button.Flat.Style.Normal });              &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the flat mode style API, after initialization:// Gets the flat mode style value  $("#button").ejmButton("option", "model.flat.style");                   // Sets the flat mode style value $("#button").ejmButton({"option", "model.flat.style", ej.mobile.Button.Flat.Style.Normal}); </code></pre>



### imageClass<span class="type-signature type string">string</span>




Specifies the css class of image.


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the imageClass property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-contenttype="image" data-ej-imageClass="imageclass" /&gt;
</code></pre><pre class="prettyprint"><code> // Set imageClass property on initialization. //To set imageClass API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({ contentType:"image" });$("#button").ejmButton({ imageClass: "imageclass" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the imageClass, after initialization:
// Gets the imageClass API value.                $("#button").ejmButton("option", "imageClass");                        // Sets the imageClass API$("#button").ejmButton("option", "imageClass", "imageclass");            </code></pre>



### imagePosition<span class="type-signature type enum">enum</span>




Specifies the position of image. See <a href="global.html#ImagePosition">ImagePosition</a>


Default Value:
{:.param}



* ej.mobile.Button.ImagePosition.Left




Example
{:.example}
<pre class="prettyprint"><code> //Set the imagePosition property in Unobtrusive way.&lt;input id="button" type="button"  data-role="ejmbutton" data-ej-contenttype="both" data-ej-imageclass="imageclass" data-ej-text="button" data-ej-imagePosition="right" /&gt;
</code></pre><pre class="prettyprint"><code> // Set imagePosition property on initialization. //To set imagePosition API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({ text:"submit" });$("#button").ejmButton({ contentType:"both" });$("#button").ejmButton({ imageClass: "imageclass" });   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the imagePosition, after initialization:
// Gets the imagePosition API value.             $("#button").ejmButton("option", "imagePosition");                     // Sets the imagePosition API$("#button").ejmButton("option", "imagePosition", ej.mobile.Button.ImagePosition.Right);            </code></pre>



### inline<span class="type-signature type boolean">boolean</span>




Specifies the button is inline or not


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the inline property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-inline="true" /&gt;
</code></pre><pre class="prettyprint"><code> // Set inline on initialization. //To set inline API value&lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton({text:"button", inline:"true"});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the inline, after initialization:
// Gets the inline API value.            $("#button").ejmButton("option", "inline");                    // Sets the inline API$("#button").ejmButton("option", "inline", "true");            </code></pre>



### ios7




Section for ios7 mode specific functionalities.






### ios7.color<span class="type-signature type enum">enum</span>




Specifies the color of the control in ios7 mode.


Default Value:
{:.param}



* ej.mobile.Button.IOS7.Color.Blue.




Example
{:.example}
<pre class="prettyprint"><code> // Set the ios7 mode buttonColor property in Unobtrusive way.&lt;a id="button"&#65533;type="button" data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="ios7" data-ej-ios7-color="blue" &gt; &lt;/a&gt;
</code></pre><pre class="prettyprint"><code> // To set ios7 mode buttonColor property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: "ios7" });$("#button").ejmButton({ "model.ios7.color": ej.mobile.Button.IOS7.Color.Blue });                &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the ios7 mode buttonColor API, after initialization:// Gets the ios7 mode buttonColor value  $("#button").ejmButton("option", "model.ios7.color");                   // Sets the ios7 mode buttonColor value $("#button").ejmButton("option", "model.ios7.color", ej.mobile.Button.IOS7.Color.Blue); </code></pre>



### ios7.style<span class="type-signature type enum">enum</span>




Specifies the style of the control in ios7 mode.


Default Value:
{:.param}



* ej.mobile.Button.IOS7.Style.Normal.




Example
{:.example}
<pre class="prettyprint"><code> // Set the ios7 mode style property in Unobtrusive way.&lt;input id="button" type="button"  data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="ios7" data-ej-ios7-style="normal"  /&gt;
</code></pre><pre class="prettyprint"><code> // To set ios7 mode style property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: "ios7" });$("#button").ejmButton({ "model.ios7.style": ej.mobile.Button.IOS7.Style.Normal});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the ios7 mode style API, after initialization:// Gets the ios7 mode style value  $("#button").ejmButton("option", "model.ios7.style");                   // Sets the ios7 mode style value $("#button").ejmButton("option", "model.ios7.style", ej.mobile.Button.IOS7.Style.Normal); </code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Specifies the rendering mode of the control.See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the renderMode property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="auto" /&gt;
</code></pre><pre class="prettyprint"><code> // Set rendermode property on initialization. //To set renderMode API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: ej.mobile.RenderMode.Auto });      &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Button rendermode, after initialization:
// Gets the renderMode API value.                $("#button").ejmButton("option", "renderMode");                        // Sets the renderMode API$("#button").ejmButton("option", "renderMode", ej.mobile.RenderMode.Auto);            </code></pre>



### text<span class="type-signature type string">string</span>




Specifies the text.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the text property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button"  /&gt;
</code></pre><pre class="prettyprint"><code> // Set text property on initialization. //To set text API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton(); $("#button").ejmButton({ text: "button" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the text, after initialization:
// Gets the text API value.              $("#button").ejmButton("option", "text");                      // Sets the text API$("#button").ejmButton("option", "text", "button");            </code></pre>



### theme<span class="type-signature type enum">enum</span>




Specifies the theme. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the theme property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-theme="auto" /&gt;
</code></pre><pre class="prettyprint"><code> // Set theme on initialization. //To set theme API value&lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ theme: ej.mobile.Theme.Auto });        &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the theme, after initialization:
// Gets the theme API value.             $("#button").ejmButton("option", "theme");                     // Sets the theme API$("#button").ejmButton("option", "theme", "button");            </code></pre>



### windows




Section for windows mode specific functionalities.






### windows.renderDefault<span class="type-signature type boolean">boolean</span>




Specifies whether to render control based on the windowsphone's current accent color and device theme.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> // Set the windows mode renderDefault property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="windows" data-ej-windows-renderDefault=true /&gt;
</code></pre><pre class="prettyprint"><code> // To set windows mode renderDefault property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: "windows" });$("#button").ejmButton({ "windows.renderDefault": "true" });             &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode renderDefault API, after initialization:// Gets the windows mode renderDefault value  $("#button").ejmButton("option", "windows.renderDefault");                      // Sets the windows mode renderDefault value $("#button").ejmButton("option", "windows.renderDefault", false); </code></pre>



### windows.style<span class="type-signature type enum">enum</span>




Specifies the style of the control in windows mode.


Default Value:
{:.param}



* ej.mobile.Button.Windows.Style.Normal.




Example
{:.example}
<pre class="prettyprint"><code> // Set the windows mode style property in Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-rendermode="windows" data-ej-windows-style="normal" /&gt;
</code></pre><pre class="prettyprint"><code> // To set windows mode style property API value &lt;input  id="button" type="button" /&gt;
&lt;script&gt; $("#button").ejmButton();$("#button").ejmButton({text:"button"});$("#button").ejmButton({ renderMode: "windows" });$("#button").ejmButton({ "model.windows.style": ej.mobile.Button.Windows.Style.Normal });                &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode style API, after initialization:// Gets the windows mode style value  $("#button").ejmButton("option", "model.windows.style");                        // Sets the windows mode style value $("#button").ejmButton("option", "model.windows.style", ej.mobile.Button.Windows.Style.Normal); </code></pre>


## Methods




### destroy<span class="signature">()</span>




destroy the Button widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}
<pre class="prettyprint"><code> &lt;input&#65533;id="button" type="Button" data-role="ejmbutton" data-ej-text="button"/&gt;
&lt;script&gt; var btnObj = $("#button").data("ejmButton");btnObj.destroy();&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input&#65533;id="button" type="button"  /&gt;
&lt;script&gt;// enabled the Button$("#button").ejmButton({text:"button"});$("#button").ejmButton("destroy");      &lt;/script&gt;</code></pre>



### disable<span class="signature">()</span>




To disable the button.



Example
{:.example}
<pre class="prettyprint"><code> &lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button"/&gt;
&lt;script&gt;$(document).ready(function () {var button = $("#button").data("ejmButton");button.disable(); // Disables the toggle button});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input&#65533;id="button" type="button"  /&gt;
&lt;script&gt;// change the button current state$("#button").ejmButton({text:"button"});$("#button").ejmButton(); $("#button").ejmButton("disable");      &lt;/script&gt;</code></pre>



### enable<span class="signature">()</span>




To enable the button.



Example
{:.example}
<pre class="prettyprint"><code> &lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button"/&gt;
&lt;script&gt;$(document).ready(function () {var btnObj = $("#button").data("ejmButton");btnObj.enable(); // changes the button control state});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input&#65533;id="button" type="button"  /&gt;
&lt;script&gt;// change the button current state$("#button").ejmButton({text:"button"});$("#button").ejmButton(); $("#button").ejmButton("enable");       &lt;/script&gt;</code></pre>


## Events




### touchEnd




Event triggers when touch end happens on the control.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Button.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the button model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>status</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">return the button state.</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> //Bind the touchEnd event using Unobtrusive way.&lt;input id="button" type="button" data-role="ejmbutton" data-ej-text="button" data-ej-touchEnd="touchEnd" /&gt;
&lt;script&gt; // touchEnd event for Buttonfunction touchEnd(args){ //handle the event}</code></pre><pre class="prettyprint"><code> &lt;input  id="button" type="button" /&gt;
&lt;script&gt; //touchEnd event for button$("#button").ejmButton({text:"button"});$("#button").ejmButton({touchEnd: function (args) {}});  &lt;/script&gt;</code></pre>



### touchStart




Event triggers when touch start happens on the control.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Button.<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the button model.</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event.</td></tr><tr><td class="name"><code>status</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">return the button state.</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> //Bind the touchStart event using Unobtrusive way.&lt;input id="button"  type="button"  data-role="ejmbutton" data-ej-touchstart="touchstart" data-ej-text="button"/&gt;
&lt;script&gt; // touchStart event for Buttonfunction touchstart(args){ //handle the event}</code></pre><pre class="prettyprint"><code> &lt;input  id="button" type="button" /&gt;
&lt;script&gt;  //touchStart event for button$("#button").ejmButton({text:"button"});$("#button").ejmButton({   touchStart: function (args) {}});       &lt;/script&gt;</code></pre>


