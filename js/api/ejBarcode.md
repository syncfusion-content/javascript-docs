---
layout: post
title: Properties, options, methods and events of Essential JS ejBarcode widget
documentation: How to use Properties, options, methods and events of Essential JS ejBarcode widget
platform: js
metaname: 
metacontent: 
---

# Custom Design for Barcode control.

$(element).ejBarcode<span class="signature">()</span>


Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 
 
&lt;script&gt;
//Create the barcode by setting the symbologyType and providing input URL to the text property. QR code is rendered by default.
      $("#barcode").ejBarcode({
         text: "http://www.syncfusion.com"
      });         
&lt;/script&gt;</code>
</pre>






Requires
{:.require}

* module:jQuery
* module:ej.common.all


## Members








### barcodeToTextGapHeight<span class="type-signature type number">number</span>








Specifies the distance between the barcode and text below it.

>   **Note:** This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 10 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set barcodeToTextGapHeight during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     barcodeToTextGapHeight: 50
 });
&lt;/script&gt;
</code>
</pre>






### barHeight<span class="type-signature type number">number</span>








Specifies the height of bars in the Barcode. By modifying the barHeight, the entire barcode height can be customized. Please refer to [xDimension](/js/api/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan) for two dimensional barcode height customization.

>   **Note:** This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 150 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set barHeight during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     barHeight: 50
 });
&lt;/script&gt;
</code>
</pre>






### darkBarColor<span class="type-signature type object">object</span>








Specifies the dark bar color of the Barcode. One dimensional barcode contains a series of dark and light bars which are usually colored as black and white respectively. 

>   **Note:** 1. For the barcode should be properly detected by all scanners, choose the best possible contrast color.
>             2. This property is applicable only for one dimensional barcode.

Default Value:
{:.param}






* black








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set darkBarColor during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     darkBarColor: "blue"
 });
&lt;/script&gt;
</code>
</pre>






### displayText<span class="type-signature type boolean">boolean</span>








Specifies whether the text below the barcode is visible or hidden.

>   **Note:** This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to hide displayText during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     displayText: false
 });
&lt;/script&gt;
</code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>








Specifies whether the control is enabled.




Default Value:
{:.param}






* true















### encodeStartStopSymbol<span class="type-signature type boolean">number</span>








Specifies the start and stop encode symbol in the Barcode. In one dimensional barcodes, an additional character is added as start and stop delimiters. These symbols are optional and the unique of the symbol allows the reader to determine the direction of the barcode being scanned.

>   **Note:** This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to remove encodeStartStopSymbol during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    encodeStartStopSymbol: false
 });
&lt;/script&gt;
</code>
</pre>






### lightBarColor<span class="type-signature type object">object</span>








 Specifies the light bar color of the Barcode. One dimensional barcode contains a series of dark and light bars which are usually colored as black and white respectively.

>   **Note:** 1. For the barcode should be properly detected by all scanners, choose the best possible contrast color.
>             2. This property is applicable only for one dimensional barcode.

Default Value:
{:.param}






* white








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set lightBarColor during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     lightBarColor: "blue"
 });
&lt;/script&gt;
</code>
</pre>






### narrowBarWidth<span class="type-signature type number">number</span>








Specifies the width of the narrow bars in the barcode. The dark bars in the one dimensional barcode contains random narrow and wide bars based on the provided input which can be specified during initialization.

>   **Note:** This property is applicable only for one dimensional barcode.



Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set narrowBarWidth during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    narrowBarWidth: 5
 });
&lt;/script&gt;
</code>
</pre>






### quietZone<span class="type-signature type object">object</span>








Specifies the width of the quiet zone. In barcode, a quiet zone is the blank margin on either side of a barcode which informs the reader where a barcode's symbology starts and stops. The purpose of a quiet zone is to prevent the reader from picking up unrelated information.










### quietZone.all<span class="type-signature type number">number</span>








Specifies the quiet zone around the Barcode.




Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        all: 10
    }
});
&lt;/script&gt;
</code>
</pre>






### quietZone.bottom<span class="type-signature type number">number</span>








Specifies the bottom quiet zone of the Barcode.




Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        bottom: 10
    }
});
&lt;/script&gt;
</code>
</pre>






### quietZone.left<span class="type-signature type number">number</span>








Specifies the left quiet zone of the Barcode.




Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        left: 10
    }
});
&lt;/script&gt;
</code>
</pre>






### quietZone.right<span class="type-signature type number">number</span>








Specifies the right quiet zone of the Barcode.




Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        right: 10
    }
});
&lt;/script&gt;
</code>
</pre>






### quietZone.top<span class="type-signature type number">number</span>








Specifies the top quiet zone of the Barcode.




Default Value:
{:.param}






* 1 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        top: 10
    }
});
&lt;/script&gt;
</code>
</pre>






### symbologyType<span class="type-signature type enum">enum</span>

Specifies the type of the Barcode. See <a href="global.html#SymbologyType">SymbologyType</a>

Default Value:
{:.param}

* ej.barcode.SymbologyType.qrbarcode








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set the SymbologyType during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39"
    }
});
&lt;/script&gt;
</pre>






### text<span class="type-signature type string">string</span>








Specifies the text to be encoded in the barcode.




Default Value:
{:.param}






* empty








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 
 
&lt;script&gt;
// All the below script to set the text to be encoded while initialization.
      $("#barcode").ejBarcode({
         text: "http://www.syncfusion.com"
      });         
&lt;/script&gt;
</code>
</pre>






### textColor<span class="type-signature type object">object</span>








Specifies the color of the text/data at the bottom of the barcode.

>   **Note:** This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* black








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 
 
&lt;script&gt;
// All the below script to set the textColor while initialization.
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    textColor: "blue"
});       
&lt;/script&gt;
</code>
</pre>






### wideBarWidth<span class="type-signature type number">number</span>








Specifies the width of the wide bars in the barcode. One dimensional barcode usually contains random narrow and wide bars based on the provided which can be customized during initialization.

>   **Note:** This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 3 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set wideBarWidth during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    wideBarWidth: 5
 });
&lt;/script&gt;
</code>
</pre>






### xDimension<span class="type-signature type number">number</span>








Specifies the width of the narrowest element(bar or space) in a barcode. The greater the x dimension, the more easily a barcode reader will scan.

>   **Note:** This property is applicable only for two dimensional barcode.


Default Value:
{:.param}






* 4 px








Example
{:.example}

<pre class="prettyprint">
<code> 
//Add div container for barcode rendering.
&lt;div id="barcode"&gt;Barcode&lt;/div&gt; 

&lt;script&gt;
// Add the script below to set xDimension during initialization  
$("#barcode").ejBarcode({
    text: "http://www.syncfusion.com",
    xDimension: 10
});
&lt;/script&gt;
</code>
</pre>




## Methods








### disable<span class="signature">()</span>








To disable the barcode





Example
{:.example}

<pre class="prettyprint">
<code>
//Add div container for barcode rendering.
&lt;div id="barcode"&gt; &lt;/div&gt; 
 
&lt;script&gt;
// Create Barcode
var btnObj = $("#barcode").data("ejBarcode");
btnObj.disable(); // disable the barcode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>
//Add div container for barcode rendering.
&lt;div id="barcode"&gt; &lt;/div&gt; 
 
&lt;script&gt;
// disable the barcode
$("#barcode").ejBarcode("disable");    
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>








To enable the barcode





Example
{:.example}

<pre class="prettyprint">
<code>
//Add div container for barcode rendering.
&lt;div id="barcode"&gt; &lt;/div&gt; 
 
&lt;script&gt;
// Create Barcode
var btnObj = $("#barcode").data("ejBarcode");
btnObj.enable(); // enable the barcode
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code>
//Add div container for barcode rendering.
&lt;div id="barcode"&gt; &lt;/div&gt; 
 
&lt;script&gt;
// enable the barcode
$("#barcode").ejBarcode("enable");     
&lt;/script&gt;</code>
</pre>




## Events








### load








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




Example
{:.example}

<pre class="prettyprint">
<code>
//Add div container for barcode rendering.
&lt;div id="barcode"&gt; &lt;/div&gt; 
<code> 
//create event for barcode
$("#barcode").ejBarcode({
   load: function (args) {}
});</code>
</pre>
<pre class="prettyprint">
<code> 
//Bind create event using jquery "on"
$("#barcode").on("ejBarcodeload", function(e) {} );</code>
</pre>
