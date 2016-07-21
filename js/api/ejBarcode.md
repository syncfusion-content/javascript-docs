---
layout: post
title: Properties, options, methods and events of Essential JS ejBarcode widget
documentation: How to use Properties, options, methods and events of Essential JS ejBarcode widget
platform: js
metaname: 
metacontent: 
---

# Custom Design for Barcode control.
<ts root="datavisualization" />

$(element).ejBarcode<span class="signature">()</span>


Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 
 
<script>
//Create the barcode by setting the symbologyType and providing input URL to the text property. QR code is rendered by default.
      $("#barcode").ejBarcode({
         text: "http://www.syncfusion.com"
      });         
</script>

{% endhighlight %}







Requires
{:.require}

* module:jQuery
* module:ej.common.all


## Members








### barcodeToTextGapHeight `number`
{:#members:barcodetotextgapheight}








Specifies the distance between the barcode and text below it.

N>    This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 10 pixels








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set barcodeToTextGapHeight during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     barcodeToTextGapHeight: 50
 });
</script>
{% endhighlight %}







### barHeight `number`
{:#members:barheight}








Specifies the height of bars in the Barcode. By modifying the barHeight, the entire barcode height can be customized. Please refer to [xDimension](/js/api/ejBarcode#xdimensionspan-classtype-signature-type-numbernumberspan) for two dimensional barcode height customization.

N>    This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 150 pixels








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set barHeight during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     barHeight: 50
 });
</script>
{% endhighlight %}







### darkBarColor `object`
{:#members:darkbarcolor}








Specifies the dark bar color of the Barcode. One dimensional barcode contains a series of dark and light bars which are usually colored as black and white respectively. 

N>    1. For the barcode should be properly detected by all scanners, choose the best possible contrast color.
N>             2. This property is applicable only for one dimensional barcode.

Default Value:
{:.param}






* black








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set darkBarColor during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     darkBarColor: "blue"
 });
</script>
{% endhighlight %}







### displayText `boolean`
{:#members:displaytext}








Specifies whether the text below the barcode is visible or hidden.

N>    This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to hide displayText during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     displayText: false
 });
</script>
{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








Specifies whether the control is enabled.




Default Value:
{:.param}






* true















### encodeStartStopSymbol `number`
{:#members:encodestartstopsymbol}








Specifies the start and stop encode symbol in the Barcode. In one dimensional barcodes, an additional character is added as start and stop delimiters. These symbols are optional and the unique of the symbol allows the reader to determine the direction of the barcode being scanned.

N>    This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to remove encodeStartStopSymbol during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    encodeStartStopSymbol: false
 });
</script>
{% endhighlight %}







### lightBarColor `object`
{:#members:lightbarcolor}








 Specifies the light bar color of the Barcode. One dimensional barcode contains a series of dark and light bars which are usually colored as black and white respectively.

N>    1. For the barcode should be properly detected by all scanners, choose the best possible contrast color.
N>             2. This property is applicable only for one dimensional barcode.

Default Value:
{:.param}






* white








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set lightBarColor during initialization  
 $("#barcode").ejBarcode({
     text: "SYNCFUSION",
     symbologyType: "code39",
     lightBarColor: "blue"
 });
</script>
{% endhighlight %}







### narrowBarWidth `number`
{:#members:narrowbarwidth}








Specifies the width of the narrow bars in the barcode. The dark bars in the one dimensional barcode contains random narrow and wide bars based on the provided input which can be specified during initialization.

N>    This property is applicable only for one dimensional barcode.



Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set narrowBarWidth during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    narrowBarWidth: 5
 });
</script>
{% endhighlight %}







### quietZone `object`
{:#members:quietzone}








Specifies the width of the quiet zone. In barcode, a quiet zone is the blank margin on either side of a barcode which informs the reader where a barcode's symbology starts and stops. The purpose of a quiet zone is to prevent the reader from picking up unrelated information.










### quietZone.all `number`
{:#members:quietzone-all}








Specifies the quiet zone around the Barcode.




Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        all: 10
    }
});
</script>
{% endhighlight %}







### quietZone.bottom `number`
{:#members:quietzone-bottom}








Specifies the bottom quiet zone of the Barcode.




Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        bottom: 10
    }
});
</script>
{% endhighlight %}







### quietZone.left `number`
{:#members:quietzone-left}








Specifies the left quiet zone of the Barcode.




Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        left: 10
    }
});
</script>
{% endhighlight %}







### quietZone.right `number`
{:#members:quietzone-right}








Specifies the right quiet zone of the Barcode.




Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        right: 10
    }
});
</script>
{% endhighlight %}







### quietZone.top `number`
{:#members:quietzone-top}








Specifies the top quiet zone of the Barcode.




Default Value:
{:.param}






* 1 pixel








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set quiet zone during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    quietZone: {
        top: 10
    }
});
</script>
{% endhighlight %}







### symbologyType `enum`
{:#members:symbologytype}

<ts name="ej.datavisualization.Barcode.SymbologyType"/>

Specifies the type of the Barcode. See <a href="global.html#SymbologyType">SymbologyType</a>
<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">QRBarcode</td>
            <td class="description">Represents the QR code</td>
        </tr>
        <tr>
            <td class="name">DataMatrix</td>
            <td class="description">Represents the Data Matrix barcode</td>
        </tr>
        <tr>
            <td class="name">Code39</td>
            <td class="description">Represents the Code 39 barcode</td>
        </tr>
        <tr>
            <td class="name">Code39Extended</td>
            <td class="description">Represents the Code 39 Extended barcode</td>
        </tr>
        <tr>
            <td class="name">Code11</td>
            <td class="description">Represents the Code 11 barcode</td>
        </tr>
        <tr>
            <td class="name">Codabar</td>
            <td class="description">Represents the Codabar barcode</td>
        </tr>
        <tr>
            <td class="name">Code32</td>
            <td class="description">Represents the Code 32 barcode</td>
        </tr>
        <tr>
            <td class="name">Code93</td>
            <td class="description">Represents the Code 93 barcode</td>
        </tr>
        <tr>
            <td class="name">Code93Extended</td>
            <td class="description">Represents the Code 93 Extended barcode</td>
        </tr>
        <tr>
            <td class="name">Code128A</td>
            <td class="description">Represents the Code 128 A barcode</td>
        </tr>
        <tr>
            <td class="name">Code128B</td>
            <td class="description">Represents the Code 128 B barcode</td>
        </tr>
        <tr>
            <td class="name">Code128C</td>
            <td class="description">Represents the Code 128 C barcode</td>
        </tr>
    </tbody>
</table>
Default Value:
{:.param}

* ej.Barcode.SymbologyType.QRBarcode








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set the SymbologyType during initialization  
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39"
    }
});
</script>


{% endhighlight %}




### text `string`
{:#members:text}








Specifies the text to be encoded in the barcode.




Default Value:
{:.param}






* empty








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 
 
<script>
// All the below script to set the text to be encoded while initialization.
      $("#barcode").ejBarcode({
         text: "http://www.syncfusion.com"
      });         
</script>
{% endhighlight %}







### textColor `object`
{:#members:textcolor}








Specifies the color of the text/data at the bottom of the barcode.

N>    This property is applicable only for one dimensional barcode.




Default Value:
{:.param}






* black








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 
 
<script>
// All the below script to set the textColor while initialization.
$("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    textColor: "blue"
});       
</script>
{% endhighlight %}







### wideBarWidth `number`
{:#members:widebarwidth}








Specifies the width of the wide bars in the barcode. One dimensional barcode usually contains random narrow and wide bars based on the provided which can be customized during initialization.

N>    This property is applicable only for one dimensional barcode.


Default Value:
{:.param}






* 3 pixels








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set wideBarWidth during initialization  
 $("#barcode").ejBarcode({
    text: "SYNCFUSION",
    symbologyType: "code39",
    wideBarWidth: 5
 });
</script>
{% endhighlight %}







### xDimension `number`
{:#members:xdimension}








Specifies the width of the narrowest element(bar or space) in a barcode. The greater the x dimension, the more easily a barcode reader will scan.

N>    This property is applicable only for two dimensional barcode.


Default Value:
{:.param}






* 4 pixels








Example
{:.example}


{% highlight html %}
 
//Add div container for barcode rendering.
<div id="barcode">Barcode</div> 

<script>
// Add the script below to set xDimension during initialization  
$("#barcode").ejBarcode({
    text: "http://www.syncfusion.com",
    xDimension: 10
});
</script>
{% endhighlight %}





## Methods








### disable<span class="signature">()</span>
{:#methods:disable}








To disable the barcode





Example
{:.example}


{% highlight html %}

//Add div container for barcode rendering.
<div id="barcode"> </div> 
 
<script>
// Create Barcode
var btnObj = $("#barcode").data("ejBarcode");
btnObj.disable(); // disable the barcode
</script>{% endhighlight %}


{% highlight html %}

//Add div container for barcode rendering.
<div id="barcode"> </div> 
 
<script>
// disable the barcode
$("#barcode").ejBarcode("disable");    
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








To enable the barcode





Example
{:.example}


{% highlight html %}

//Add div container for barcode rendering.
<div id="barcode"> </div> 
 
<script>
// Create Barcode
var btnObj = $("#barcode").data("ejBarcode");
btnObj.enable(); // enable the barcode
</script>{% endhighlight %}


{% highlight html %}

//Add div container for barcode rendering.
<div id="barcode"> </div> 
 
<script>
// enable the barcode
$("#barcode").ejBarcode("enable");     
</script>{% endhighlight %}





## Events








### load
{:#events:load}








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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the barcode model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
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


{% highlight html %}

//Add div container for barcode rendering.
<div id="barcode"> </div> 
 
//create event for barcode
$("#barcode").ejBarcode({
   load: function (args) {}
});
{% endhighlight %}


{% highlight html %}
 
//Bind create event using jquery "on"
$("#barcode").on("ejBarcodeload", function(e) {} );{% endhighlight %}

