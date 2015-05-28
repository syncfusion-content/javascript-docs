---
layout: post
title: ejResizable
documentation: ug
platform: js
metaname: 
metacontent: 
---

Custom Design for resizing HTML elements.










#### $(element).ejResizable<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div  id="resizing" &gt;&lt;/ div &gt; 
 
&lt;script&gt;
// Create resizing
$('#resizing').ejResizable();   
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.core




### Members








#### cursorAt<span class="type-signature type object">object</span>








Sets the offset of the resizing helper relative to the mouse cursor.




Default Value:






* { top: -1, left: -2 }








##### Examples

<pre class="prettyprint">
<code> 
//To set cursorAt API value during initialization  
        $("#resizing").ejResizable({ cursorAt:  { top: 1, left: -2 } });                                * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#resizing").ejResizable('option', 'cursorAt');
                   </code>
</pre>






#### distance<span class="type-signature type number">number</span>








Distance in pixels after mousedown the mouse must move before resizing should start. This option can be used to prevent unwanted drags when clicking on an element.




Default Value:






* 1








##### Examples

<pre class="prettyprint">
<code> 
//To set distance API value during initialization  
        $("#resizing").ejResizable({ distance: 1 });                            * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#resizing").ejResizable('option', 'distance');
                   </code>
</pre>






#### handle<span class="type-signature type string">string</span>








If specified, restricts resize start click to the specified element(s).




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set handle API value during initialization  
        $("#resizing").ejResizable({ handle: null });                           * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#resizing").ejResizable('option', 'handle');
                     </code>
</pre>






#### maxHeight<span class="type-signature type number">number</span>








Sets the max height for resizing




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set maxHeight API value during initialization  
        $("#resizing").ejResizable({ maxHeight: null });                                * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxHeight API, after initialization:
        //Gets the maxHeight value  
        $("#resizing").ejResizable('option', 'maxHeight');
                  </code>
</pre>






#### maxWidth<span class="type-signature type number">number</span>








Sets the max width for resizing




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code> 
//To set maxWidth API value during initialization  
        $("#resizing").ejResizable({ maxWidth: null });                         * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the maxWidth API, after initialization:
        //Gets the maxWidth value  
        $("#resizing").ejResizable('option', 'maxWidth');
                   </code>
</pre>






#### minHeight<span class="type-signature type number">number</span>








Sets the min Height for resizing




Default Value:






* 10








##### Examples

<pre class="prettyprint">
<code> 
//To set minHeight API value during initialization  
        $("#resizing").ejResizable({ minHeight: null });                                * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minHeight API, after initialization:
        //Gets the minHeight value  
        $("#resizing").ejResizable('option', 'minHeight');
                  </code>
</pre>






#### minWidth<span class="type-signature type number">number</span>








Sets the min Width for resizing




Default Value:






* 10








##### Examples

<pre class="prettyprint">
<code> 
//To set minWidth API value during initialization  
        $("#resizing").ejResizable({ minWidth: null });                         * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the minWidth API, after initialization:
        //Gets the minWidth value  
        $("#resizing").ejResizable('option', 'minWidth');
                   </code>
</pre>






#### scope<span class="type-signature type string">string</span>








Used to group sets of resizeable items.




Default Value:






* 'default'








##### Examples

<pre class="prettyprint">
<code> 
//To set scope API value during initialization  
        $("#resizing").ejResizable({ scope: 'default' });                               * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#resizing").ejResizable('option', 'scope');
                      </code>
</pre>




### Methods








#### _destroy<span class="signature">()</span>








destroy in the Resizable.





##### Example

<pre class="prettyprint">
<code> 
&lt; div  id="resizing" &gt; &lt;/div &gt; 
 
&lt;script&gt;
// Create resizingObj
var resizingObj  = $("#resizing").data("ejResizable");
resizingObj.destroy(); 
&lt;/script&gt;</code>
</pre>




### Events








#### destroy








This event is triggered when the widget destroys.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//destroy event for Resizable
$("#resizing").ejResizable({ 
        destroy: function(args) {}
});      </code>
</pre>






#### helper








This event is triggered when resized.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//helper event for Resizable
$("#resizing").ejResizable({ 
        helper: function () {
               return $('</code>
</pre>



<pre>
').html("resizable").appendTo(document.body);}
});      
</pre>






#### <code>resize</code>








<code>This event is triggered when the resizing in progress.</code>

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//resizeStart event for Resizable
$("#resizing").ejResizable({ 
        resize: function(args) {}
});      </code>
</pre>






#### resizeStart








This event is triggered when the resizing is start.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//resizeStart event for Resizable
$("#resizing").ejResizable({ 
        resizeStart: function(args) {}
});      </code>
</pre>






#### resizeStop








This event is triggered when the resizing is stop.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//resizeStop event for Resizable
$("#resizing").ejResizable({ 
        resizeStop: function(args) {}
});      </code>
</pre>



