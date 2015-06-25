---
layout: post
title: ejmTextBox
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html TextBox control.





$(element).ejmTextBox<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code>//To create the textbox &lt;input id="textbox" /&gt;
&lt;script&gt; //Create the textbox  $("#textbox").ejmTextBox(); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox" data-role="ejmtextbox" /&gt;
</code></pre><pre class="prettyprint"><code> //To create the password&lt;input id="password" /&gt;
&lt;script&gt; //Create the password  $("#password").ejmPassword(); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password" data-role="ejmpassword" /&gt;
</code></pre><pre class="prettyprint"><code> //To create the maskedit&lt;input id="maskedit" /&gt;
&lt;script&gt; //Create the maskedit  $("#maskedit").ejmMaskEdit(); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit" data-role="ejmmaskedit" /&gt;
</code></pre><pre class="prettyprint"><code> //To create the textarea&lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt; //Create the textarea  $("#textarea").ejmTextArea();&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea" data-role="ejmtextarea" &gt;&lt;/textarea&gt;
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




### cssClass<span class="type-signature type string">string</span>




Sets the root class for Textbox theme. This cssClass API helps to use custom skinning option for Textbox control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code>// For TextBox //Set the cssClass property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-cssclass="customclass" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the cssClass on initialization. //To set the cssClass API value &lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ value: "" });               &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the TextBox cssClass, after initialization:
// Get the cssClass API value.          &lt;script&gt; $("#textbox").ejmTextBox ("option", "cssClass");                       // Set the value API$("#textbox").ejmTextBox ("option", "cssClass", "customclass");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the cssClass property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-cssclass="customclass" /&gt;
</code></pre><pre class="prettyprint"><code> // Set Password cssClass on initialization. //To set the value API value &lt;input id="password"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ cssClass: "customclass" });       &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Password cssClass, after initialization:
// Get the cssClass API value.          &lt;script&gt; $("#password").ejmPassword ("option", "cssClass");                     // Set the cssClass API$("#password").ejmPassword ("option", "cssClass", "customclass");&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the cssClass property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-cssclass="customclass" data-ej-mask="+1 (999) 999-9999"/&gt;
</code></pre><pre class="prettyprint"><code> // Set the cssClass on initialization. //To set the cssClass API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ cssClass: "customclass",mask:"+1 (999) 999-9999" });      &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the cssClass, after initialization:
// Get the cssClass API value.          &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "cssClass");                     // Set the cssClass API$("#maskedit").ejmMaskEdit ("option", "cssClass", "customclass");&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For TextArea//Set the cssClass property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-cssclass="customclass" &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the cssClass on initialization. //To set the cssClass API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ cssClass: "customclass" });               &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the cssClass, after initialization:
// Get the cssClass API value.          &lt;script&gt;$("#textarea").ejmTextArea ("option", "cssClass");                      // Set the cssClass API$("#textarea").ejmTextArea ("option", "cssClass", "customclass");    &lt;/script&gt;</code></pre>



### enabled<span class="type-signature type boolean">boolean</span>




Specifies whether to be enable on initialization.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> // For TextBox//Set the enabled property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-enabled=true /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enabled on initialization. //To set the enabled API value&lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ enabled: true });           &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the  enabled, after initialization:
// Get the enabled API value.           &lt;script&gt; $("#textbox").ejmTextBox ("option", "enabled");                        // Set the enabled API$("#textbox").ejmTextBox ("option", "enabled", true);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the enabled property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-enabled=true /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enabled on initialization. //To set enabled API value &lt;input id="password" /&gt;
&lt;script&gt;$("#password").ejmPassword ({ enabled: true });         &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enabled, after initialization:
// Get the enabled API value.           &lt;script&gt; $("#password").ejmPassword ("option", "enabled");                      // Set the enabled API$("#password").ejmPassword ("option", "enabled", true);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the enabled property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-enabled=true data-ej-mask="+1 (999) 999-9999"  /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enabled on initialization. //To set the enabled API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ enabled: true,mask:"+1 (999) 999-9999" });        &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enabled, after initialization:
// Get the enabled API value.           &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "enabled");                      // Set the enabled API$("#maskedit").ejmMaskEdit ("option", "enabled", true); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For textarea//Set the enabled property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-enabled=true &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the enabled on initialization. //To set the enabled API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ enabled: true });                 &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enabled, after initialization:
// Get the enabled API value.           &lt;script&gt; $("#textarea").ejmTextArea ("option", "enabled");                      // Set the enabled API$("#textarea").ejmTextArea ("option", "enabled", true);  &lt;/script&gt;</code></pre>



### enablePersistence<span class="type-signature type boolean">boolean</span>




Specifies to maintain the current model value to browser cookies for state maintenance. While refresh the page, the model value will get apply to the control from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> // For TextBox//Set the enablePersistence property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-enablepersistence=false /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enablePersistence on initialization. //To set the enablePersistence API value &lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ enablePersistence: false });        &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value. &lt;script&gt; $("#textbox").ejmTextBox ("option", "enablePersistence");                      // Set the enablePersistence API$("#textbox").ejmTextBox ("option", "enablePersistence", false);  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the enablePersistence property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-enablepersistence=false /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enablePersistence on initialization. //To set the enablePersistence API value &lt;input id="password"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ enablePersistence: false });      &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         &lt;script&gt; $("#password").ejmPassword ("option", "enablePersistence");                    // Set the enablePersistence API$("#password").ejmPassword ("option", "enablePersistence", false);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the enablePersistence property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-enablepersistence=false data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the enablePersistence on initialization. //To set the enablePersistence API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ enablePersistence: false,mask:"+1 (999) 999-9999" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "enablePersistence");                    // Set the enablePersistence API$("#maskedit").ejmMaskEdit ("option", "enablePersistence", false);  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For TextArea//Set the enablePersistence property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-enablepersistence=false &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the enablePersistence on initialization. //To set the enablePersistence API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ enablePersistence: false });      &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the enablePersistence, after initialization:
// Get the enablePersistence API value.         &lt;script&gt; $("#textarea").ejmTextArea ("option", "enablePersistence");                    // Set the enablePersistence API$("#textarea").ejmTextArea ("option", "enablePersistence", false); &lt;/script&gt;</code></pre>



### readOnly<span class="type-signature type boolean">boolean</span>




Specifies the TextBox, Password, Mask Edit, and Textarea readOnly.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> // For TextBox//Set the readOnly property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-readonly=false /&gt;
</code></pre><pre class="prettyprint"><code> // Set the readOnly on initialization. //To set the readOnly API value&lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ readOnly: false });         &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the readOnly, after initialization:
// Get the readOnly API value.          &lt;script&gt; $("#textbox").ejmTextBox ("option", "readOnly");                       // Set the readOnly API$("#textbox").ejmTextBox ("option", "readOnly", false);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the readOnly property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-readonly=false /&gt;
</code></pre><pre class="prettyprint"><code> // Set the readOnly on initialization. //To set readOnly API value &lt;input id="password"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ readOnly: false });               &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the  readOnly, after initialization:
// Get the readOnly API value.          &lt;script&gt; $("#password").ejmPassword ("option", "readOnly");                     // Set the readOnly API$("#password").ejmPassword ("option", "readOnly", false);  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the readOnly property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-readonly=false data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the readOnly on initialization. //To set the readOnly API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ readOnly: false,mask:"+1 (999) 999-9999" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the readOnly, after initialization:
// Get the readOnly API value.          &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "readOnly");                     // Set the readOnly API$("#maskedit").ejmMaskEdit ("option", "readOnly", false);   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For TextArea//Set the readOnly property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-readonly=false &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the readOnly on initialization. //To set the readOnly API value &lt;textarea id="textarea"&gt; &lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ readOnly: false });                       &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the readOnly, after initialization:
// Get the readOnly API value.          &lt;script&gt; $("#textarea").ejmTextArea ("option", "readOnly");                     // Set the readOnly API$("#textarea").ejmTextArea ("option", "readOnly", false);          &lt;/script&gt;</code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Changes the rendering mode of the TextBox, Password, Mask Edit, and Textarea. See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> // For textbox //Set the renderMode property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-rendermode="auto" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the renderMode on initialization. //To set the renderMode API value &lt;input id="textbox" data-role="ejmtextbox"/&gt;
&lt;script&gt;$(function () {$("#textbox").ejmTextBox ({ renderMode:ej.mobile.RenderMode.Auto });    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the  renderMode, after initialization:
// Get the renderMode API value.        &lt;script&gt; $("#textbox").ejmTextBox ("option", "renderMode");                     // Set the renderMode API$("#textbox").ejmTextBox ("option", "renderMode", ej.mobile.RenderMode.Auto);&lt;/script&gt;
</code></pre><pre class="prettyprint"><code>// For Password //Set the renderMode property in unobtrusive way.&lt;input id="password" data-role="ejmpassword"/&gt;
</code></pre><pre class="prettyprint"><code>// Set the renderMode on initialization. //To set the renderMode API value &lt;input id="password" data-role="ejmpassword"/&gt;
&lt;script&gt;$(function () {$("#password").ejmPassword ({ renderMode: ej.mobile.RenderMode.Auto});});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the renderMode, after initialization:
// Get the renderMode API value.        &lt;script&gt; $("#password").ejmPassword ("option", "renderMode");                   // Set the renderMode API$("#password").ejmPassword ("option", "renderMode", ej.mobile.RenderMode.Auto); &lt;/script&gt;
</code></pre><pre class="prettyprint"><code>             // For MaskEdit//Set the renderMode property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-mask="+1 (999) 999-9999"/&gt;
</code></pre><pre class="prettyprint"><code> // Set the renderMode on initialization. //To set the renderMode API value &lt;input id="maskedit" data-role="ejmmaskedit" /&gt;
&lt;script&gt;$(function () {$("#maskedit").ejmMaskEdit ({ renderMode:ej.mobile.RenderMode.Auto,mask:"+1 (999) 999-9999" });         });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the renderMode, after initialization:
// Get the renderMode API value.        &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "renderMode");                   // Set the renderMode API$("#maskedit").ejmMaskEdit ("option", "renderMode", ej.mobile.RenderMode.Auto);&lt;/script&gt;
</code></pre><pre class="prettyprint"><code>    // For TextArea//Set the renderMode property in unobtrusive way. &lt;textarea id="textarea" data-role="ejmtextarea" &gt; &lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the renderMode on initialization. //To set the renderMode API value &lt;textarea id="textarea" data-role="ejmtextarea" &gt; &lt;/textarea&gt;
&lt;script&gt;$(function () {$("#textarea").ejmTextArea ({ renderMode:ej.mobile.RenderMode.Auto });  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the renderMode, after initialization:
// Get the renderMode API value.                &lt;script&gt; $("#textarea").ejmTextArea ("option", "renderMode");                   // Set the renderMode API$("#textarea").ejmTextArea ("option", "renderMode", ej.mobile.RenderMode.Auto);&lt;/script&gt;</code></pre>



### showBorder<span class="type-signature type boolean">boolean</span>




Specifies whether to show the border on the TextBox, Password, Mask Edit, and Textarea.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code>// For TextBox //Set the showBorder property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-showborder=true /&gt;
</code></pre><pre class="prettyprint"><code> // Set the showBorder on initialization. //To set the showBorder API value &lt;input id="textbox" data-role="ejmtextbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ showBorder: true });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the showBorder, after initialization:
// Get the showBorder API value.&lt;script&gt; $("#textbox").ejmTextBox ("option", "showBorder");                     // Set the showBorder API$("#textbox").ejmTextBox ("option", "showBorder", true); &lt;/script&gt;
</code></pre><pre class="prettyprint"><code> // For Password//Set the showBorder property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-showborder=true /&gt;
</code></pre><pre class="prettyprint"><code> // Set the showBorder on initialization. //To set the showBorder API value &lt;input id="password" data-role="ejmpassword"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ showBorder: true });      &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the showBorder, after initialization:
// Get the showBorder API value.                &lt;script&gt; $("#password").ejmPassword ("option", "showBorder");                   // Set the showBorder API$("#password").ejmPassword ("option", "showBorder", true); &lt;/script&gt;
       </code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the showBorder property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-showborder=true data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the showBorder on initialization. //To set the showBorder API value &lt;input id="maskedit" data-role="ejmmaskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ showBorder: true,mask:"+1 (999) 999-9999" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the showBorder, after initialization:
// Get the showBorder API value.                &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "showBorder");                   // Set the showBorder API$("#maskedit").ejmMaskEdit ("option", "showBorder", true); &lt;/script&gt;
 </code></pre><pre class="prettyprint"><code> // For TextArea//Set the showBorder property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-showborder=true &gt; &lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the showBorder on initialization. //To set the showBorder API value &lt;textarea id="textarea" data-role="ejmtextarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ showBorder: true });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the  showBorder, after initialization:
// Get the showBorder API value.&lt;script&gt; $("#textarea").ejmTextArea ("option", "showBorder");                   // Set the showBorder API$("#textarea").ejmTextArea ("option", "showBorder", true);&lt;/script&gt;</code></pre>



### theme<span class="type-signature type enum">enum</span>




Changes the theme of the TextBox, Password, Mask Edit, and Textarea. See <a href="global.html#Theme">Theme</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code>// For TextBox  //Set the theme property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-theme="auto" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the theme on initialization. //To set the theme API value &lt;input id="textbox" data-role="ejmtextbox" /&gt;
&lt;script&gt;$(function () {$("#textbox").ejmTextBox ({ theme: ej.mobile.Theme.Auto });     });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the theme, after initialization:
// Get the theme API value.             &lt;script&gt; $("#textbox").ejmTextBox ("option", "theme");                  // Set the theme API$("#textbox").ejmTextBox ("option", "theme", ej.mobile.Theme.Auto);&lt;/script&gt; 
 </code></pre><pre class="prettyprint"><code> // For Password//Set the theme property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-theme="auto" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the theme on initialization. //To set the theme API value &lt;input id="password" data-role="ejmpassword"/&gt;
&lt;script&gt;$(function () {$("#password").ejmPassword ({ theme: ej.mobile.Theme.Auto });   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the theme, after initialization:
// Get the theme API value.     &lt;script&gt; $("#password").ejmPassword ("option", "theme");                        // Set the theme API$("#password").ejmPassword ("option", "theme", ej.mobile.Theme.Auto); &lt;/script&gt; 
 </code></pre><pre class="prettyprint"><code>// For MaskEdit //Set the theme property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-theme="auto" data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the theme on initialization. //To set the theme API value &lt;input id="maskedit" data-role="ejmmaskedit"/&gt;
&lt;script&gt;$(function () {$("#maskedit").ejmMaskEdit ({ theme: ej.mobile.Theme.Auto,mask:"+1 (999) 999-9999"  }); });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the theme, after initialization:
// Get the theme API value.     &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "theme");                        // Set the theme API$("#maskedit").ejmMaskEdit ("option", "theme", ej.mobile.Theme.Auto); &lt;/script&gt;
</code></pre><pre class="prettyprint"><code> // For TextArea//Set the theme property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-theme="auto" &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the theme on initialization. //To set the theme API value &lt;textarea id="textarea" data-role="ejmtextarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$(function () {$("#textarea").ejmTextArea ({ theme: ej.mobile.Theme.Auto });});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the textarea theme, after initialization:
// Get the theme API value.     &lt;script&gt; $("#textarea").ejmTextArea ("option", "theme");                        // Set the theme API$("#textarea").ejmTextArea ("option", "theme", ej.mobile.Theme.Auto); &lt;/script&gt;</code></pre>



### value<span class="type-signature type string">string</span>




Specifies the value on initialization.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code>// For TextBox //Set the value property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-value="" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the value on initialization. //To set the value API value &lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ value: "" });               &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the TextBox value, after initialization:
// Get the value API value.             &lt;script&gt; $("#textbox").ejmTextBox ("option", "value");                  // Set the value API$("#textbox").ejmTextBox ("option", "value", "");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the value property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-value="" /&gt;
</code></pre><pre class="prettyprint"><code> // Set Password value on initialization. //To set the value API value &lt;input id="password"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ value: "" });     &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Password value, after initialization:
// Get the value API value.             &lt;script&gt; $("#password").ejmPassword ("option", "value");                        // Set the value API$("#password").ejmPassword ("option", "value", "");&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the value property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-value="" data-ej-mask="+1 (999) 999-9999"/&gt;
</code></pre><pre class="prettyprint"><code> // Set the value on initialization. //To set the value API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ value: "",mask:"+1 (999) 999-9999" });    &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the value, after initialization:
// Get the value API value.             &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "value");                        // Set the value API$("#maskedit").ejmMaskEdit ("option", "value", "");&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For TextArea//Set the value property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-value="" &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the value on initialization. //To set the value API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ value: "" });             &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the value, after initialization:
// Get the value API value.             &lt;script&gt;$("#textarea").ejmTextArea ("option", "value");                 // Set the value API$("#textarea").ejmTextArea ("option", "value", "");    &lt;/script&gt;</code></pre>



### watermarkText<span class="type-signature type string">string</span>




Specifies the watermarkText on initialization.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> // For TextBox//Set the watermarkText property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-watermarktext="" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the watermarkText on initialization. //To set the watermarkText API value &lt;input id="textbox"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox ({ watermarkText: "" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the watermarkText, after initialization:
// Get the watermarkText API value.             &lt;script&gt; $("#textbox").ejmTextBox ("option", "watermarkText");                  // Set the watermarkText API$("#textbox").ejmTextBox ("option", "watermarkText", "");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For Password//Set the watermarkText property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-watermarktext="" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the watermarkText on initialization. //To set the watermarkText API value &lt;input id="password"/&gt;
&lt;script&gt;$("#password").ejmPassword ({ watermarkText: "" });     &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the watermarkText, after initialization:
// Get the watermarkText API value.             &lt;script&gt; $("#password").ejmPassword ("option", "watermarkText");                        // Set the watermarkText API$("#password").ejmPassword ("option", "watermarkText", "");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For MaskEdit//Set the watermarkText property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-watermarktext="" data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // Set the watermarkText on initialization. //To set the watermarkText API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$("#maskedit").ejmMaskEdit ({ watermarkText: "",mask:"+1 (999) 999-9999" });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the watermarkText, after initialization:
// Get the watermarkText API value.     &lt;script&gt; $("#maskedit").ejmMaskEdit ("option", "watermarkText");                        // Set the watermarkText API$("#maskedit").ejmMaskEdit ("option", "watermarkText", ""); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> // For TextArea//Set the watermarkText property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-watermarktext="" &gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // Set the watermarkText on initialization. //To set the watermarkText API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$("#textarea").ejmTextArea ({ watermarkText: "" });             &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the watermarkText, after initialization:
// Get the watermarkText API value.             &lt;script&gt; $("#textarea").ejmTextArea ("option", "watermarkText");                        // Set the watermarkText API$("#textarea").ejmTextArea ("option", "watermarkText", "");        &lt;/script&gt;</code></pre>



### windows




Section for windows rendermode specific functionalities.






### windows.allowReset<span class="type-signature type boolean">boolean</span>




Specifies whether to allow the reset button for the windows mode in TextBox, Password, MaskEdit, TextArea.


Default Value:
{:.param}



* true




Example
{:.example}
<pre class="prettyprint"><code> //For TextBox Control// Set the windows mode allowReset property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-rendermode="windows" data-ej-windows-allowreset=true /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode allowReset property API value &lt;input id="textbox"/&gt;
&lt;script&gt;$(function () {$("#textbox").ejmTextBox({ windows:{allowReset: true},renderMode:ej.mobile.RenderMode.Windows});   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode allowReset API, after initialization:// Get the windows mode allowReset value  &lt;script&gt;$("#textbox").ejmTextBox("option", "windows.allowReset");   // Set the windows mode allowReset value $("#textbox").ejmTextBox("option", "windows.allowReset", true);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password Control// Set the windows mode allowReset property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-rendermode="windows" data-ej-windows-allowreset=true /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode allowReset property API value &lt;input id="password"/&gt;
&lt;script&gt;$(function () {$("#password").ejmPassword({ windows:{allowReset: true},renderMode:ej.mobile.RenderMode.Windows});  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode allowReset API, after initialization:// Get the windows mode allowReset value  &lt;script&gt;$("#password").ejmPassword("option", "windows.allowReset");   // Set the windows mode allowReset value $("#password").ejmPassword("option", "windows.allowReset", true); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit Control// Set the windows mode allowReset property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit"  data-ej-rendermode="windows" data-ej-windows-allowreset=true data-ej-mask="+1 (999) 999-9999" /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode allowReset property API value &lt;input id="maskedit"/&gt;
&lt;script&gt;$(function () {$("#maskedit").ejmMaskEdit({ windows:{allowReset: true},mask:"+1 (999) 999-9999",renderMode:ej.mobile.RenderMode.Windows});   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode allowReset API, after initialization:// Get the windows mode allowReset value  &lt;script&gt;$("#maskedit").ejmMaskEdit("option", "windows.allowReset");   // Set the windows mode allowReset value $("#maskedit").ejmMaskEdit("option", "windows.allowReset", true);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area Control// Set the windows mode allowReset property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-rendermode="windows" data-ej-windows-allowreset=true &gt; &lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode allowReset property API value &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;$(function () {$("#textarea").ejmTextArea({windows:{allowReset: true,renderMode:ej.mobile.RenderMode.Windows}});  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode allowReset API, after initialization:// Get the windows mode allowReset value  &lt;script&gt;$("#textarea").ejmTextArea("option", "windows.allowReset");   // Set the windows mode allowReset value $("#textarea").ejmTextArea("option", "windows.allowReset", true); &lt;/script&gt;</code></pre>



### windows.renderDefault<span class="type-signature type boolean">boolean</span>




Specifies whether to render control based on the windowsphone's current accent color and device theme.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //For TextBox Control// Set the windows mode renderDefault property in unobtrusive way.&lt;input id="textbox" data-role="ejmtextbox" data-ej-rendermode="windows" data-ej-windows-renderDefault=false /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode renderDefault property API value &lt;input id="textbox"/&gt;
&lt;script&gt;$(function () {$("#textbox").ejmTextBox({ windows:{renderDefault: false},renderMode:ej.mobile.RenderMode.Windows});});&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode renderDefault API, after initialization:// Get the windows mode renderDefault value  &lt;script&gt;$("#textbox").ejmTextBox("option", "windows.renderDefault");   // Set the windows mode renderDefault value $("#textbox").ejmTextBox("option", "windows.renderDefault", false);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password Control// Set the windows mode renderDefault property in unobtrusive way.&lt;input id="password" data-role="ejmpassword" data-ej-rendermode="windows" data-ej-windows-renderDefault=false /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode renderDefault property API value &lt;input id="password"/&gt;
&lt;script&gt;$(function () {$("#password").ejmPassword({ windows:{renderDefault: false},renderMode:ej.mobile.RenderMode.Windows});   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode renderDefault API, after initialization:// Get the windows mode renderDefault value  &lt;script&gt;$("#password").ejmPassword("option", "windows.renderDefault");   // Set the windows mode renderDefault value $("#password").ejmPassword("option", "windows.renderDefault", false);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit Control// Set the windows mode renderDefault property in unobtrusive way.&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-rendermode="windows" data-ej-windows-renderDefault=false data-ej-mask="+1 (999) 999-9999"  /&gt;
</code></pre><pre class="prettyprint"><code> // To set the windows mode renderDefault property API value &lt;input id="maskedit" /&gt;
&lt;script&gt;$(function () {$("#maskedit").ejmMaskEdit({ windows:{renderDefault: false},mask:"+1 (999) 999-9999"},renderMode:ej.mobile.RenderMode.Windows); });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode renderDefault API, after initialization:// Get the windows mode renderDefault value  &lt;script&gt;$("#maskedit").ejmMaskEdit("option", "windows.renderDefault"); // Set the windows mode renderDefault value $("#maskedit").ejmMaskEdit("option", "windows.renderDefault", false);&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area Control// Set the windows mode renderDefault property in unobtrusive way.&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-rendermode="windows" data-ej-windows-renderDefault=false&gt;&lt;/textarea&gt;
</code></pre><pre class="prettyprint"><code> // To set windows mode renderDefault property API value &lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt;$(function () {$("#textarea").ejmTextArea({windows:{renderDefault: false},renderMode:ej.mobile.RenderMode.Windows});   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> // Get or set the windows mode renderDefault API, after initialization:// Get the windows mode renderDefault value  &lt;script&gt;$("#textarea").ejmTextArea("option", "windows.renderDefault");   // Set the windows mode renderDefault value $("#textarea").ejmTextArea("option", "windows.renderDefault", false); &lt;/script&gt;</code></pre>


## Methods




### disable<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to disable



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.disable(); // Returns the textbox to disable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;// Get the textbox to disable$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("disable");    &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.disable(); // Returns the password to disable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to disable$("#password").ejmPassword();$("#password").ejmPassword("disable");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the MaskEdit$("#maskedit").ejmMaskEdit({mask:"+1 (999) 999-9999"});var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.disable(); // returns the maskedit to disable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to disable$("#maskedit").ejmMaskEdit({mask:"+1 (999) 999-9999"});$("#maskedit").ejmMaskEdit("disable");  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area&lt;textarea id="textarea" &gt; &lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.disable(); // Returns the textarea to disable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;// Get the textarea to disable$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("disable");  &lt;/script&gt;</code></pre>



### enable<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to enable



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.enable(); // Returns the textbox to enable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;// Get the textbox to enable$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("enable");     &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.enable(); // Returns the password to enable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to enable$("#password").ejmPassword();$("#password").ejmPassword("enable");   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the maskedit$("#maskedit").ejmMaskEdit();var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.enable(); // Returns the maskedit to enable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to enable$("#maskedit").ejmMaskEdit();$("#maskedit").ejmMaskEdit("enable");   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area&lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.enable(); // Returns the textarea to enable mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;// Get the textarea to enable$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("enable");   &lt;/script&gt;</code></pre>



### getStrippedValue<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to getStrippedValue



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.getStrippedValue(); // Returns the textbox value with stripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;// Get the textbox to getStrippedValue$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("getStrippedValue");   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.getStrippedValue(); // Returns the password value with stripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to getStrippedValue$("#password").ejmPassword();$("#password").ejmPassword("getStrippedValue"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the MaskEdit$("#maskedit").ejmMaskEdit();var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.getStrippedValue(); // Returns the maskedit Value with Stripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to getStrippedValue$("#maskedit").ejmMaskEdit();$("#maskedit").ejmMaskEdit("getStrippedValue"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area&lt;textarea id="textarea" &gt; &lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.getStrippedValue(); // Returns the textarea value with stripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;// Get the textarea to getStrippedValue$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("getStrippedValue"); &lt;/script&gt;</code></pre>



### getUnstrippedValue<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to getUnstrippedValue



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.getUnstrippedValue(); // Returns the textbox value with unstripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;// Get the textbox to getUnstrippedValue$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("getUnstrippedValue"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.getUnstrippedValue(); // Returns the password value with unstripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to getUnstrippedValue$("#password").ejmPassword();$("#password").ejmPassword("getUnstrippedValue");       &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the MaskEdit$("#maskedit").ejmMaskEdit();var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.getUnstrippedValue(); // Returns the maskedit value with unstripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to getUnstrippedValue$("#maskedit").ejmMaskEdit();$("#maskedit").ejmMaskEdit("getUnstrippedValue");       &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area&lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.getUnstrippedValue(); // Returns the textarea value with unstripped mode.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt; &lt;/textarea &gt;
&lt;script&gt;// Get the textarea to getUnstrippedValue$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("getUnstrippedValue");       &lt;/script&gt;</code></pre>



### getValue<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to getValue



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.getValue(); // Returns the textbox value.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;// Get the textbox to getValue$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("getValue");   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.getValue(); // Returns the password value.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to getValue$("#password").ejmPassword();$("#password").ejmPassword("getValue"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the maskedit$("#maskedit").ejmMaskEdit();var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.getValue(); // Returns the maskedit value.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to getValue$("#maskedit").ejmMaskEdit();$("#maskedit").ejmMaskEdit("getValue"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Text Area&lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.getValue(); // Returns the textarea value.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt;&lt;/textarea&gt;
&lt;script&gt;// Get the textarea to getValue$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("getValue"); &lt;/script&gt;</code></pre>



### getWatermarkText<span class="signature">()</span>




To handle the TextBox, or Password or MaskEdit or TextArea to getWatermarkText



Example
{:.example}
<pre class="prettyprint"><code> //For TextBox&lt;input id="textbox" /&gt;
&lt;script&gt;// Create the textbox$("#textbox").ejmTextBox();var textbox = $("#textbox").data("ejmTextBox");textbox.getWatermarkText(); // Returns the textbox watermarkText.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="textbox"/&gt;
&lt;script&gt;//Get the textbox to getWatermarkText$("#textbox").ejmTextBox();$("#textbox").ejmTextBox("getWatermarkText");   &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" /&gt;
&lt;script&gt;// Create the password$("#password").ejmPassword();var password = $("#password").data("ejmPassword");password.getWatermarkText(); // Returns the password watermarkText.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="password"/&gt;
&lt;script&gt;// Get the password to getWatermarkText$("#password").ejmPassword();$("#password").ejmPassword("getWatermarkText"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For MaskEdit&lt;input id="maskedit" /&gt;
&lt;script&gt;// Create the maskedit$("#maskedit").ejmMaskEdit();var maskedit = $("#maskedit").data("ejmMaskEdit");maskedit.getWatermarkText(); // Returns the maskedit watermarkText.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;input id="maskedit"/&gt;
&lt;script&gt;// Get the maskedit to getWatermarkText$("#maskedit").ejmMaskEdit();$("#maskedit").ejmMaskEdit("getWatermarkText"); &lt;/script&gt;</code></pre><pre class="prettyprint"><code>//For Text Area &lt;textarea id="textarea" &gt;&lt;/textarea&gt;
&lt;script&gt;// Create the textarea$("#textarea").ejmTextArea();var textarea = $("#textarea").data("ejmTextArea");textarea.getWatermarkText(); // Returns the textarea watermarkText.&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;textarea id="textarea"&gt; &lt;/textarea &gt;
&lt;script&gt;// Get the textarea to getWatermarkText$("#textarea").ejmTextArea();$("#textarea").ejmTextArea("getWatermarkText"); &lt;/script&gt;</code></pre>


## Events




### change




Event triggers when the Textbox or Password or Maskedit or textarea value changed
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Textbox or Password or Maskedit or textarea<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the Textbox or Password or Maskedit or textarea model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>element</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the current element</td></tr><tr><td class="name"><code>value</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the value of the control</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> // For TextBox&lt;input id="textbox" data-role="ejmtextbox" data-ej-change="onChange"/&gt;
&lt;script&gt; // Change event for textboxfunction onChange(args) { //handle the event }&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Change event for textbox&lt;input id="textbox" data-role="ejmtextbox" data-ej-change="onChange"/&gt;
&lt;script&gt;$("#textbox").ejmTextBox({  change: function (args) { //handle the event }});  &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For Password&lt;input id="password" data-role="ejmpassword" data-ej-change="onChange"/&gt;
&lt;script&gt; // Change event for passwordfunction onChange(args) { //handle the event }&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Change event for password&lt;input id="password" data-role="ejmpassword" data-ej-change="onChange"/&gt;
&lt;script&gt;$("#password").ejmPassword({  change: function (args) { //handle the event }});    &lt;/script&gt;</code></pre><pre class="prettyprint"><code> //For maskedit&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-change="onChange" data-ej-mask="+1 (999) 999-9999" /&gt;
&lt;script&gt; // Change event for maskeditfunction onChange(args) { //handle the event }&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Change event for maskedit&lt;input id="maskedit" data-role="ejmmaskedit" data-ej-change="onChange" data-ej-mask="+1 (999) 999-9999" /&gt;
&lt;script&gt; $("#maskedit").ejmMaskEdit({  change: function (args) { //handle the event }});     &lt;/script&gt; </code></pre><pre class="prettyprint"><code> //For textarea&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-change="onChange"&gt;&lt;/textarea&gt;
&lt;script&gt; // Change event for textAreafunction onChange(args) { //handle the event }&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Change event for textarea&lt;textarea id="textarea" data-role="ejmtextarea" data-ej-change="onChange"&gt;&lt;/textarea&gt;
&lt;script&gt; $("#textarea").ejmTextArea({  change: function (args) { //handle the event }});           &lt;/script&gt; </code></pre>


