---
layout: post
title: ejDraggable
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for dragging HTML elements.










$(element).ejDraggable<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div  id="dragable" &gt;&lt;/ div &gt; 
 
&lt;script&gt;
// Create Dragable
$('#dragable').ejDraggable();   
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core




## Members








### clone<span class="type-signature type boolean">boolean</span>
{:#members:clone}








If clone is specified.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set clone API value during initialization  
        $("#dragable").ejDraggable({ clone: true });                            * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the clone API, after initialization:
        //Gets the clone value  
        $("#dragable").ejDraggable('option', 'clone');
                      </code>
</pre>






### cursorAt<span class="type-signature type object">object</span>
{:#members:cursorat}








Sets the offset of the dragging helper relative to the mouse cursor.




Default Value:
{:.param}






* { top: -1, left: -2 }








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set cursorAt API value during initialization  
        $("#dragable").ejDraggable({ cursorAt:  { top: 1, left: -2 } });                                * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#dragable").ejDraggable('option', 'cursorAt');
                   </code>
</pre>






### distance<span class="type-signature type number">number</span>
{:#members:distance}








Distance in pixels after mousedown the mouse must move before dragging should start. This option can be used to prevent unwanted drags when clicking on an element.




Default Value:
{:.param}






* 1








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set distance API value during initialization  
        $("#dragable").ejDraggable({ distance: 1 });                            * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#dragable").ejDraggable('option', 'distance');
                   </code>
</pre>






### dragArea<span class="type-signature type boolean">boolean</span>
{:#members:dragarea}








If Drag area is specified.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set dragArea API value during initialization  
        $("#dragable").ejDraggable({ dragArea: true });                         * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the dragArea API, after initialization:
        //Gets the dragArea value  
        $("#dragable").ejDraggable('option', 'dragArea');
                   </code>
</pre>






### handle<span class="type-signature type string">string</span>
{:#members:handle}








If specified, restricts drag start click to the specified element(s).




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set handle API value during initialization  
        $("#dragable").ejDraggable({ handle: null });                           * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#dragable").ejDraggable('option', 'handle');
                     </code>
</pre>






### scope<span class="type-signature type string">string</span>
{:#members:scope}








Used to group sets of draggable and droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.




Default Value:
{:.param}






* 'default'








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set scope API value during initialization  
        $("#dragable").ejDraggable({ scope: 'default' });                               * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#dragable").ejDraggable('option', 'scope');
                      </code>
</pre>




## Methods








### _destroy<span class="signature">()</span>
{:#methods:_destroy}








destroy in the dragable.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt; div  id="dragable" &gt; &lt;/div &gt; 
 
&lt;script&gt;
// Create dragableObj
var dragableObj  = $("#dragable").data("ejDraggable");
dragableObj.destroy(); 
&lt;/script&gt;</code>
</pre>




## Events








### destroy
{:#events:destroy}








This event is triggered when dragging events are destroyed.

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




Example
{:.example}

<pre class="prettyprint">
<code> 
//destroy event for Draggable
$("#dragable").ejDraggable({ 
        destroy: function(args) {}
});      </code>
</pre>






### drag
{:#events:drag}








This event is triggered when the mouse is moved during the dragging.

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




Example
{:.example}

<pre class="prettyprint">
<code> 
//drag event for Draggable
$("#dragable").ejDraggable({ 
        drag: function(args) {}
});      </code>
</pre>






### dragStart
{:#events:dragstart}








Supply a callback function to handle the drag start event as an init option.

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




Example
{:.example}

<pre class="prettyprint">
<code> 
//dragStart event for Draggable
$("#dragable").ejDraggable({ 
        dragStart: function(args) {}
});      </code>
</pre>






### dragStop
{:#events:dragstop}








This event is triggered when the mouse is moved during the dragging.

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




Example
{:.example}

<pre class="prettyprint">
<code> 
//dragStop event for Draggable
$("#dragable").ejDraggable({ 
        dragStop: function(args) {}
});      </code>
</pre>






### helper
{:#events:helper}








This event is triggered when dragged.

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




Example
{:.example}

<pre class="prettyprint">
<code> 
//helper event for Draggable
$("#dragable").ejDraggable({ 
        helper: function () {
                return $('</code>
</pre>



<pre>
').html("draggable").appendTo(document.body);}
});      
</pre>







<code><a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a></code>




<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
