---
layout: post
title: ejSplitter
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html splitter control.











$(element).ejSplitter<span class="signature">(options)</span>







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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for Slider.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="innerSplitter"&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
        &lt;/div&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
        &lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
// Create Splitter 
$('#innerSplitter').ejSplitter(); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.splitter.js




## Members








### animationSpeed<span class="type-signature type number">number</span>
{:#animationspeed}








Specify animation speed for the Splitter pane movement while collapsing and expanding.




Default Value:
{:.param}






* 300








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set animationSpeed API value during initialization
$("#innerSplitter").ejSplitter({animationSpeed: 150 });
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>
{:#cssclass}








Specify the CSS class to splitter control to achieve custom theme.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="innerSplitter"&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
        &lt;/div&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
        &lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set cssClass API value during initialization
        $("#innerSplitter").ejSplitter({ cssClass: "gradient-lime"});
&lt;/script&gt;</code>
</pre>






### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#enableanimation}








Specifies the animation behavior of the splitter.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
        &lt;/div&gt;
        &lt;div&gt;
                &lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
        &lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set enableAnimation API value during initialization  
        $("#innerSplitter").ejSplitter({ enableAnimation: false});
&lt;/script&gt;</code>
</pre>






### enableAutoResize<span class="type-signature type boolean">boolean</span>
{:#enableautoresize}








Specify window resizing behavior for splitter control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set windowResizing API value during initialization
        $("#innerSplitter").ejSplitter({enableAutoResize: true});
&lt;/script&gt;</code>
</pre>






### enableRTL<span class="type-signature type boolean">boolean</span>
{:#enablertl}








Specify Right to Left Direction for splitter control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set enableRTL API value during initialization  
        $("#innerSplitter").ejSplitter({enableRTL: true} );
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type string">string</span>
{:#height}








Specify height for splitter control.




Default Value:
{:.param}






* &ldquo;100%&rdquo;








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set height API value during initialization
        $("#innerSplitter").ejSplitter({height: "100%" });
&lt;/script&gt;</code>
</pre>






### orientation<span class="type-signature type enum">Enum</span>
{:#orientation}








Specify the orientation for spliter control.See orientation




Default Value:
{:.param}






* ej.orientation.Horizontal or &ldquo;horizontal&rdquo;








Example
{:.example}

<pre class="prettyprint">
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set orientation API value during initialization  
$("#innerSplitter").ejSplitter({ orientation: ej.Orientation.Horizontal });
&lt;/script&gt;</code>
</pre>






### properties<span class="type-signature type array">array</span>
{:#properties}








Specify properties for each pane.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set properties API value during initialization  
        $("#innerSplitter").ejSplitter({properties: [{ paneSize: "100px" }, { paneSize: "50px"}]});
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type string">string</span>
{:#width}








Specify width for splitter control.




Default Value:
{:.param}






* &ldquo;100%&rdquo;








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//To set width API value during initialization  
        $("#innerSplitter").ejSplitter({width: 600} );
&lt;/script&gt;</code>
</pre>




## Methods








### addItem<span class="signature">(content, property, index)</span>
{:#additem}








To add the new pane to splitter control.

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
<td class="name"><code>content</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">content of pane.</td>
</tr>
<tr>
<td class="name"><code>property</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">pane properties.</td>
</tr>
<tr>
<td class="name"><code>index</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of pane.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.addItem("New pane 0",{ paneSize:20, minSize:20, maxSize:100},0);
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("addItem","New pane 0",{ paneSize:20, minSize:20, maxSize:100},0);
&lt;/script&gt;</code>
</pre>






### collapse<span class="signature">()</span>
{:#collapse}








To collapse the splitter control pane.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.collapse(); // collpase the splitter control pane.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// collpase the splitter control
$("#innerSplitter").ejSplitter("collpase");
&lt;/script&gt;</code>
</pre>






### expand<span class="signature">()</span>
{:#expand}








To expand the splitter control pane.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.expand(); // expand the splitter control pane.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("expand");
&lt;/script&gt;</code>
</pre>






### refresh<span class="signature">()</span>
{:#refresh}








To refresh the splitter control pane resizing.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.refresh(); // refresh the splitter control pane resizing.
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// refresh the splitter control
$("#innerSplitter").ejSplitter("refresh");
&lt;/script&gt;</code>
</pre>






### removeItem<span class="signature">(index)</span>
{:#removeitem}








To remove the new pane from the splitter control.

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
<td class="description last">index of pane.</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.removeItem(0); 
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("removeItem",0);
&lt;/script&gt;</code>
</pre>




## Events








### beforeExpandCollapse
{:#beforeexpandcollapse}








Fires when before expand collapse in splitter control.

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
<td class="description last">Event parameters from splitter control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>collapsed</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name"><code>expanded</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name"><code>splitbarIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//beforeExpandCollapse event for splitter control
$("#innerSplitter").ejSplitter({
   beforeExpandCollapse: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### create
{:#create}








Fires when splitter control pane has been created.

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
<td class="description last">Event parameters from splitter control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//create event for splitter control
$("#innerSplitter").ejSplitter({
   create: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### destroy
{:#destroy}








Fires when splitter control pane has been destroyed.

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
<td class="description last">Event parameters from splitter control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//destroy event for splitter control
$("#innerSplitter").ejSplitter({
   destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### expandCollapse
{:#expandcollapse}








Fires when expandCollapse in splitter control pane.

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
<td class="description last">Event parameters from splitter control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>collapsed</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name"><code>expanded</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name"><code>splitbarIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//expandCollapse event for splitter control
$("#innerSplitter").ejSplitter({
   expandCollapse: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### resize
{:#resize}








Fires when resize in splitter control pane.

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
<td class="description last">Event parameters from splitter control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>collapsed</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name"><code>expanded</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name"><code>splitbarIndex</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
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
<code>&lt;div id="innerSplitter"&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 1 &lt;/div&gt;
&lt;/div&gt;
&lt;div&gt;
&lt;div class="cont"&gt;Pane 2 &lt;/div&gt;
&lt;/div&gt;
&lt;/div&gt; 
&lt;script&gt;
//resize event for splitter control
$("#innerSplitter").ejSplitter({
   resize: function (args) {}
});
&lt;/script&gt;</code>
</pre>



