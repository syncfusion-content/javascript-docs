---
layout: post
title: ejBarcode
metaname: 
metacontent: 
---

Custom Design for Barcode control.










#### $(element).ejBarcode<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;barcode id="barcode1"&gt;Barcode&lt;/barcode&gt; 
 
&lt;script&gt;
// Create Barcode
$('#barcode1').ejBarcode();         
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.common.all




### Members








#### barcodeToTextGapHeight<span class="type-signature type number">number</span>








Specifies the distance between the bar and text in the Barcode. Applicable only for One dimensional barcode.




Default Value:






* 10








##### Examples

<pre class="prettyprint">
<code> 
//To set barcodeToTextGapHeight API value during initialization  
$("#barcode1").ejBarcode({ barcodeToTextGapHeight: 10 });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the barcodeToTextGapHeight API, after initialization:
//Gets the gap distance between the bar and the text
$("#barcode1").ejBarcode("option", "barcodeToTextGapHeight");
//Sets the gap distance between the bar and the text
$("#barcode1").ejBarcode("option", "barcodeToTextGapHeight", 10 ); </code>
</pre>






#### barHeight<span class="type-signature type number">number</span>








Specifies the height of bars in the Barcode. Applicable only for One dimensional barcode.




Default Value:






* 150








##### Examples

<pre class="prettyprint">
<code> 
//To set barHeight API value during initialization  
$("#barcode1").ejBarcode({ barHeight: 150 });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the barHeight API, after initialization:
//Gets the height of the bars  
$("#barcode1").ejBarcode("option", "barHeight");
//Sets the height of the bars 
$("#barcode1").ejBarcode("option", "barHeight", 150 ); </code>
</pre>






#### darkBarColor<span class="type-signature type object">object</span>








Specifies the dark bar color of the Barcode. Applicable only for One dimensional barcode.




Default Value:






* black








##### Examples

<pre class="prettyprint">
<code> 
//To set dark bar color API value during initialization  
$("#barcode1").ejBarcode({ darkBarColor: "black" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the dark bar color API, after initialization:
//Gets the dark bar color value  
$("#barcode1").ejBarcode("option", "darkBarColor");
//Sets the dark bar color value 
$("#barcode1").ejBarcode("option", "darkBarColor", "black" ); </code>
</pre>






#### displayText<span class="type-signature type boolean">boolean</span>








Specifies whether to display original text. Applicable only for One dimensional barcode.




Default Value:






* true








##### Examples

<pre class="prettyprint">
<code> 
//To set displayText API value during initialization  
$("#barcode").ejBarcode({ displayText: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the displayText API, after initialization:
//Gets the displayText value  
$("#barcode1").ejBarcode("option", "displayText");
//Sets the displayText value 
$("#barcode1").ejBarcode("option", "displayText", true ); </code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








Specifies whether the control is enabled.




Default Value:






* true








##### Examples

<pre class="prettyprint">
<code> 
//To set enabled API value during initialization  
$("#barcode").ejBarcode({ enabled: true});</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the enabled API, after initialization:
//Gets the enabled value  
$("#barcode1").ejBarcode("option", "enabled");
//Sets the enabled value 
$("#barcode1").ejBarcode("option", "enabled", true ); </code>
</pre>






#### encodeStartStopSymbol<span class="type-signature type number">number</span>








Specifies whether to encode start and stop symbol in the Barcode. Applicable only for One dimensional barcode.




Default Value:






* 10








##### Examples

<pre class="prettyprint">
<code> 
//To set encodeStartStopSymbol API value during initialization  
$("#barcode1").ejBarcode({ encodeStartStopSymbol: true });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the encodeStartStopSymbol API, after initialization:
//Gets the encodeStartStopSymbol value
$("#barcode1").ejBarcode("option", "encodeStartStopSymbol");
//Sets the whether to encode start and stop symbol value
$("#barcode1").ejBarcode("option", "encodeStartStopSymbol", true ); </code>
</pre>






#### lightBarColor<span class="type-signature type object">object</span>








Specifies the light bar color of the Barcode. Applicable only for One dimensional barcode.




Default Value:






* white








##### Examples

<pre class="prettyprint">
<code> 
//To set light bar color API value during initialization  
$("#barcode1").ejBarcode({ lightBarColor: "white" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the light bar color API, after initialization:
//Gets the light bar color value  
$("#barcode1").ejBarcode("option", "lightBarColor");
//Sets the light bar color value 
$("#barcode1").ejBarcode("option", "lightBarColor", "white" ); </code>
</pre>






#### narrowBarWidth<span class="type-signature type number">number</span>








Specifies the width of narrow bar in the Barcode. Applicable only for One dimensional barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set narrowBarWidth API value during initialization  
$("#barcode1").ejBarcode({ narrowBarWidth: 1 });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the narrowBarWidth API, after initialization:
//Gets the width of the narrow bar value  
$("#barcode1").ejBarcode("option", "narrowBarWidth");
//Sets the width of the narrow bar value 
$("#barcode1").ejBarcode("option", "narrowBarWidth", 1 ); </code>
</pre>






#### quietZone<span class="type-signature type object">object</span>








The blank margin on the side(s) which denotes the reader with the start and stop of the Barcode.











#### quietZone.all<span class="type-signature type number">number</span>








Specifies the quiet zone around the Barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set the quiet zone API value during initialization  
$("#barcode1").ejBarcode({ quietZone: { all: 5} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the quietZone API, after initialization:
//Gets the quiet zone value  
$("#barcode1").ejBarcode("option", "quietZone.all");
                 
//Sets the quiet zone value 
$("#barcode1").ejBarcode("option", "quietZone", {all: 5} ); </code>
</pre>






#### quietZone.bottom<span class="type-signature type number">number</span>








Specifies the bottom quiet zone of the Barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set the quiet zone API value during initialization  
$("#barcode1").ejBarcode({ quietZone: { bottom: 5} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the quietZone API, after initialization:
//Gets the quiet zone value  
$("#barcode1").ejBarcode("option", "quietZone.bottom");
                     
//Sets the quiet zone value 
$("#barcode1").ejBarcode("option", "quietZone", {bottom: 5} ); </code>
</pre>






#### quietZone.left<span class="type-signature type number">number</span>








Specifies the left quiet zone of the Barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set the quiet zone API value during initialization  
$("#barcode1").ejBarcode({ quietZone: { left: 5} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the quietZone API, after initialization:
//Gets the quiet zone value  
$("#barcode1").ejBarcode("option", "quietZone.left");
                        
//Sets the quiet zone value 
$("#barcode1").ejBarcode("option", "quietZone", {left: 5} ); </code>
</pre>






#### quietZone.right<span class="type-signature type number">number</span>








Specifies the right quiet zone of the Barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set the quiet zone API value during initialization  
$("#barcode1").ejBarcode({ quietZone: { right: 5} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the quietZone API, after initialization:
//Gets the quiet zone value  
$("#barcode1").ejBarcode("option", "quietZone.right");
                      
//Sets the quiet zone value 
$("#barcode1").ejBarcode("option", "quietZone", {right: 5} ); </code>
</pre>






#### quietZone.top<span class="type-signature type number">number</span>








Specifies the top quiet zone of the Barcode.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set the quiet zone API value during initialization  
$("#barcode1").ejBarcode({ quietZone: { top: 5} });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the quietZone API, after initialization:
//Gets the quiet zone value  
$("#barcode1").ejBarcode("option", "quietZone.top");
                   
//Sets the quiet zone value 
$("#barcode1").ejBarcode("option", "quietZone", {top: 5} ); </code>
</pre>






#### symbologyType<span class="type-signature type enum">enum</span>








Specifies the symbology type of the Barcode. See <a href="global.html#SymbologyType">SymbologyType</a>




Default Value:






* ej.barcode.SymbologyType.qrbarcode








##### Examples

<pre class="prettyprint">
<code> 
//To set symbology type API value during initialization  
$("#barcode1").ejBarcode({ symbologyType: "code39" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the symbology type API, after initialization:
//Gets the symbology type value  
$("#barcode1").ejBarcode("option", "symbologyType");
          
//Sets the symbology type value 
$("#barcode1").ejBarcode("option", "symbologyType", "code39" ); </code>
</pre>






#### text<span class="type-signature type string">string</span>








Specifies the text to encode.




Default Value:






* empty








##### Examples

<pre class="prettyprint">
<code> 
//To set text value during initialization  
$("#barcode1").ejBarcode({ text:"SYNCFUSION" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the text API, after initialization:
//Gets the text value  
$("#barcode1").ejBarcode("option", "text");
//Sets the text value 
$("#barcode1").ejBarcode("option", "text", "SYNCFUSION" ); </code>
</pre>






#### textColor<span class="type-signature type object">object</span>








Specifies the display text color of the Barcode. Applicable only for One dimensional barcode.




Default Value:






* black








##### Examples

<pre class="prettyprint">
<code> 
//To set text color API value during initialization  
$("#barcode1").ejBarcode({ textColor: "black" });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the text color API, after initialization:
//Gets the text color value  
$("#barcode1").ejBarcode("option", "textColor");
//Sets the text color value 
$("#barcode1").ejBarcode("option", "textColor", "black" ); </code>
</pre>






#### wideBarWidth<span class="type-signature type number">number</span>








Specifies the width of wide bar in the Barcode. Applicable only for One dimensional barcode.




Default Value:






* 3








##### Examples

<pre class="prettyprint">
<code> 
//To set wideBarWidth API value during initialization  
$("#barcode1").ejBarcode({ wideBarWidth: 1 });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the wideBarWidth API, after initialization:
//Gets the width of the wide bar value  
$("#barcode1").ejBarcode("option", "wideBarWidth");
//Sets the width of the wide bar value 
$("#barcode1").ejBarcode("option", "wideBarWidth", 3 ); </code>
</pre>






#### xDimension<span class="type-signature type number">number</span>








Specifies the size of each block in the Barcode. Applicable only for Two dimensional barcode.




Default Value:






* 4








##### Examples

<pre class="prettyprint">
<code> 
//To set xDimension API value during initialization  
$("#barcode1").ejBarcode({ xDimension: 4 });</code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the xDimension API, after initialization:
//Gets the size of each block
$("#barcode1").ejBarcode("option", "xDimension");
//Sets the size of each block
$("#barcode1").ejBarcode("option", "xDimension", 4 ); </code>
</pre>




### Methods








#### disable<span class="signature">()</span>








To disable the barcode





##### Examples

<pre class="prettyprint">
<code> 
&lt;barcode id="barcode1"&gt;Barcode&lt;/barcode&gt; 
 
&lt;script&gt;
// Create Barcode
var btnObj = $("#barcode1").data("ejBarcode");
btnObj.disable(); // disable the barcode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;barcode id="barcode1"&gt;Barcode&lt;/barcode&gt; 
 
&lt;script&gt;
// disable the barcode
$("#barcode1").ejBarcode("disable");    
&lt;/script&gt;</code>
</pre>






#### enable<span class="signature">()</span>








To enable the barcode





##### Examples

<pre class="prettyprint">
<code> 
&lt;barcode id="barcode1"&gt;Barcode&lt;/barcode&gt; 
 
&lt;script&gt;
// Create Barcode
var btnObj = $("#barcode1").data("ejBarcode");
btnObj.enable(); // enable the barcode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;barcode id="barcode1"&gt;Barcode&lt;/barcode&gt; 
 
&lt;script&gt;
// enable the barcode
$("#barcode1").ejBarcode("enable");     
&lt;/script&gt;</code>
</pre>




### Events








#### load








Fires after Barcode control is loaded.

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
<td class="description last">Event parameters from barcode
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
<td class="description last">returns the barcode model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the barcode state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
//create event for barcode
$("#barcode1").ejBarcode({
   load: function (args) {}
});</code>
</pre>
<pre class="prettyprint">
<code> 
//Bind create event using jquery "on"
$("#barcode1").on("ejBarcodeload", function(e) {} );</code>
</pre>



