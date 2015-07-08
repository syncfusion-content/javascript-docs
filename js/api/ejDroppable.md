---
layout: post
title: ejDroppable
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for droping HTML elements.










$(element).ejDroppable<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div  id="dropable" &gt;&lt;/ div &gt; 
 
&lt;script&gt;
// Create Dragable
$('#dropable').ejDroppable();   
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core




## Members








### accept<span class="type-signature type object">object</span>
{:#members-accept}








Used to accept the droppable items.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ accept: null });                          * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the accept API, after initialization:
        //Gets the accept value  
        $("#droppable").ejDroppable('option', 'accept');
                    </code>
</pre>






### scope<span class="type-signature type string">string</span>
{:#members-scope}








Used to group sets of droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.




Default Value:
{:.param}






* 'default'








Example
{:.example}

<pre class="prettyprint">
<code> 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ scope: 'default' });                              * </code>
</pre>
<pre class="prettyprint">
<code> 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#droppable").ejDroppable('option', 'scope');
                     </code>
</pre>




## Methods








### _destroy<span class="signature">()</span>
{:#methods-_destroy}








destroy in the Droppable.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt; div  id="droppable" &gt; &lt;/div &gt; 
 
&lt;script&gt;
// Create droppabaleObj
var droppabaleObj  = $("#droppable").data("ejDroppable");
droppabaleObj.destroy(); 
&lt;/script&gt;</code>
</pre>




## Events








### drop
{:#events-drop}








This event is triggered when the mouse up is moved during the dragging.

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
//drop event for Droppable
$("#droppable").ejDroppable({ 
        drop: function(args) {}
});      </code>
</pre>






### out
{:#events-out}








This event is triggered when the mouse is moved out.

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
//drop event for Droppable
$("#droppable").ejDroppable({ 
        out: function(args) {}
});      </code>
</pre>






### over
{:#events-over}








This event is triggered when the mouse is moved over.

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
//drop event for Droppable
$("#droppable").ejDroppable({ 
        over: function(args) {}
});      </code>
</pre>



