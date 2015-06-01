---
layout: post
title: ejToggleButton
documentation: API
platform: js
metaname: 
metacontent: 
---

The Toggle Button allows you to perform the toggle option by using checked and unchecked state. This Toggle Button can be helpful to user to check their states. The Toggle Button control displays both text and images.





#### $(element).ejToggleButton<span class="signature">()</span>






##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Create ToggleButton 
$('#toggle').ejToggleButton({defaultText:"Play",activeText:"Pause"});   
    &lt;/script&gt; 
</code></pre>



### Requires


* module:jQuery

* module:ej.core.js

* module:ej.togglebutton.js

* module:ej.checkbox.js


### Members




#### activePrefixIcon<span class="type-signature type string">string</span>




Specify the activePrefixIcon to toggle button to achieve custom theme.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the activePrefixIcon during initialization.                              $("#toggle").ejToggleButton({    defaultText:"Play",activeText:"Pause",   contentType: "textandimage",   defaultPrefixIcon: "e-mediaplay e-uiLight",   activePrefixIcon: "e-mediapause e-uiLight", });                    &lt;/script&gt; </code></pre>



#### activeSuffixIcon<span class="type-signature type string">string</span>




Specify the activeSuffixIcon to toggle button to achieve custom theme.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the activeSuffixIcon during initialization.                              $("#toggle").ejToggleButton({    contentType: "imageboth",   defaultSuffixIcon: "e-mediaplay e-uiLight",   activeSuffixIcon: "e-mediapause e-uiLight", });                    &lt;/script&gt; 
</code></pre>



#### activeText<span class="type-signature type string">string</span>




Specifies the activeText of the ToggleButton.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set activeText API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                                   &lt;/script&gt; 
    </code></pre>



#### contentType<span class="type-signature type enum">enum</span>




Specifies the contentType of the ToggleButton. See <a href="global.html#ContentType">ContentType</a>


Default Value:



* ej.ContentType.TextOnly




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the button contentType on initialization.                                $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",contentType : ej.ContentType.TextOnly });                    &lt;/script&gt; 
</code></pre>



#### cssClass<span class="type-signature type string">string</span>




Specify the CSS class to toggle button to achieve custom theme.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the CSS class during initialization.                             $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",cssClass : "gradient-lime" });                        &lt;/script&gt; 
</code></pre>



#### defaultPrefixIcon<span class="type-signature type string">string</span>




Specify the defaultPrefixIcon to toggle button to achieve custom theme.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the defaultPrefixIcon during initialization.                             $("#toggle").ejToggleButton({    defaultText:"Play",activeText:"Pause",   contentType: "textandimage",   defaultPrefixIcon: "e-mediaplay e-uiLight",   activePrefixIcon: "e-mediapause e-uiLight", });                    &lt;/script&gt; 
</code></pre>



#### defaultSuffixIcon<span class="type-signature type string">string</span>




Specify the defaultSuffixIcon to toggle button to achieve custom theme.


Default Value:



* ""




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the defaultSuffixIcon during initialization.                      $("#toggle").ejToggleButton({    defaultText:"Play",activeText:"Pause",   contentType: "textandimage",   defaultSuffixIcon: "e-mediaplay e-uiLight",   activeSuffixIcon: "e-mediapause e-uiLight", });                    &lt;/script&gt; 
</code></pre>



#### defaultText<span class="type-signature type string">string</span>




Specifies the defaultText of the ToggleButton.


Default Value:



* null




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set defaultText API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});                                           &lt;/script&gt; 
            </code></pre>



#### enabled<span class="type-signature type boolean">boolean</span>




Specifies the state of the ToggleButton.


Default Value:



* true




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set enabled API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enabled: true });                                            &lt;/script&gt; 
            </code></pre>



#### enablePersistence<span class="type-signature type boolean">boolean</span>




Specify the enablePersistence to Togglebutton to save current model value to browser cookies for state maintains


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the rounded corner during initialization.                                $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",enablePersistence : true });                         &lt;/script&gt; 
</code></pre>



#### enableRTL<span class="type-signature type boolean">boolean</span>




Specify the Right to Left Direction to Togglebutton


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the enableRTL during initialization.                             $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",enableRTL : true });                  &lt;/script&gt; 
</code></pre>



#### height<span class="type-signature type string">String</span>




Specifies the height of the ToggleButton.


Default Value:



* 28pixel




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set height API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",height: "28px" });                                           &lt;/script&gt;         </code></pre>



#### htmlAttributes<span class="type-signature type object">object</span>




Specifies the HTML Attributes of the ToggleButton


Default Value:



* {}




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// To Set HtmlAttributes on initialization.                             $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",htmlAttributes: {disabled:"disabled"} });                    &lt;/script&gt; 
</code></pre>



#### imagePosition<span class="type-signature type enum">enum</span>




Specifies the image position of the ToggleButton. This image position is applicable only with the textandimage contentType property. The images can be positioned in both imageLeft and imageRight options. See imagePositions


Default Value:



* ej.ImagePosition.ImageLeft




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the image position for toggle button during initialization.                              $("#toggle").ejToggleButton({   contentType: ej.ContentType.TextAndImage,   imagePosition: ej.ImagePosition.ImageRight,   defaultText:"Play",activeText:"Pause",   defaultPrefixIcon: "e-mediaplay e-uiLight",   activePrefixIcon: "e-mediapause e-uiLight"});                     &lt;/script&gt; 
</code></pre>



#### preventToggle<span class="type-signature type boolean">boolean</span>




Specifies the preventToggle of the ToggleButton.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set preventToggle API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",preventToggle: false});                                              &lt;/script&gt; 
            </code></pre>



#### showRoundedCorner<span class="type-signature type boolean">boolean</span>




Specify the rounded corner to Togglebutton


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
// Set the rounded corner during initialization.                                $("#toggle").ejToggleButton({ defaultText:"Play",activeText:"Pause",showRoundedCorner : true });                         &lt;/script&gt; 
</code></pre>



#### size<span class="type-signature type enum">enum</span>




Specifies the size of the ToggleButton. See <a href="global.html#ButtonSize">ButtonSize</a>


Default Value:



* ej.ButtonSize.Normal




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set size API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",size: ej.ButtonSize.Mini});                                                                  &lt;/script&gt; 
</code></pre>



#### toggleState<span class="type-signature type boolean">boolean</span>




Specifies the toggleState of the ToggleButton.


Default Value:



* false




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set toggleState API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",toggleState: false });       &lt;/script&gt; 
    </code></pre>



#### type<span class="type-signature type enum">enum</span>




Specifies the type of the ToggleButton. See <a href="global.html#ButtonType">ButtonType</a>


Default Value:



* ej.ButtonType.Button




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set type API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",type:ej.ButtonType.Submit});                                                                 &lt;/script&gt; 
</code></pre>



#### width<span class="type-signature type string">String</span>




Specifies the width of the ToggleButton.


Default Value:



* 100pixel




##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//To set width API value during initialization          $("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",width: "100px" });                                           &lt;/script&gt; 
                    </code></pre>


### Methods




#### destroy<span class="signature">()</span>




To destroy the toggle button



##### Examples
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// Create toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});var toggleObj = $("#toggle").data("ejToggleButton");toggleObj.destroy(); // destroy the toggle button&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// destroy the toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});$("#toggle").ejToggleButton("destroy"); &lt;/script&gt;</code></pre>



#### disable<span class="signature">()</span>




To disable the toggle button



##### Examples
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// Create toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});var toggleObj = $("#toggle").data("ejToggleButton");toggleObj.disable(); // disable the toggle button&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// disable the toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});$("#toggle").ejToggleButton("disable"); &lt;/script&gt;</code></pre>



#### enable<span class="signature">()</span>




To enable the toggle button



##### Examples
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// Create toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});var toggleObj = $("#toggle").data("ejToggleButton");toggleObj.enable(); // enable the toggle button&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" / &gt; 
 &lt;script&gt;// enable the toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause"});$("#toggle").ejToggleButton("enable");  &lt;/script&gt;</code></pre>


### Events




#### change




Fires when ToggleButton control state is changed successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toggle button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>isChecked</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">return the toggle button checked state</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the toggle button model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//change event for toggle button$("#toggle").ejToggleButton({   defaultText:"Play",activeText:"Pause",   change: function (args) {}});  &lt;/script&gt; 
    </code></pre>



#### click




Fires when ToggleButton control is clicked successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toggle button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>isChecked</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">return the toggle button checked state</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the toggle button model</td></tr><tr><td class="name"><code>status</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">return the toggle button state</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//click event for toggle button$("#toggle").ejToggleButton({defaultText:"Play",activeText:"Pause",   click: function (args) {}}); &lt;/script&gt; 
     </code></pre>



#### create




Fires when ToggleButton control is created successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toggle button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the toggle button model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//create event for toggle button$("#toggle").ejToggleButton({   defaultText:"Play",activeText:"Pause",   create: function (args) {}});   &lt;/script&gt; 
   </code></pre>



#### destroy




Fires when ToggleButton control is destroyed successfully.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from toggle button<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be cancelled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the toggle button model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr></tbody></table></td></tr></tbody></table>


##### Example
<pre class="prettyprint"><code> &lt;input id="toggle" type="checkbox" /&gt; 
        &lt;script&gt; 
//destroy event for toggle button$("#toggle").ejToggleButton({   defaultText:"Play",activeText:"Pause",   destroy: function (args) {}});  &lt;/script&gt; 
    </code></pre>


