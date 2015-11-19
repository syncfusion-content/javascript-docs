---
layout: post
title: ejDroppable
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejDroppable


Plugin to make any DOM element Droppable.  










$(element).ejDroppable<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div  id="dropable" ></ div > 
 
<script>
// Create Dragable
$('#dropable').ejDroppable();   
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core




## Members








### accept<span class="type-signature type object">object</span>
{:#members:accept}








Used to accept the droppable items.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ accept: null });                          * {% endhighlight %}


{% highlight html %}
 
//Get or set the accept API, after initialization:
        //Gets the accept value  
        $("#droppable").ejDroppable('option', 'accept');
                    {% endhighlight %}







### scope<span class="type-signature type string">string</span>
{:#members:scope}








Used to group sets of droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.




Default Value:
{:.param}






* 'default'








Example
{:.example}


{% highlight html %}
 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ scope: 'default' });                              * {% endhighlight %}


{% highlight html %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#droppable").ejDroppable('option', 'scope');
                     {% endhighlight %}





## Methods








### _destroy<span class="signature">()</span>
{:#methods:_destroy}








destroy in the Droppable.





Example
{:.example}


{% highlight html %}
 
< div  id="droppable" > </div > 
 
<script>
// Create droppabaleObj
var droppabaleObj  = $("#droppable").data("ejDroppable");
droppabaleObj.destroy(); 
</script>{% endhighlight %}





## Events








### drop
{:#events:drop}








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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        drop: function(args) {}
});      {% endhighlight %}







### out
{:#events:out}








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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        out: function(args) {}
});      {% endhighlight %}







### over
{:#events:over}








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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        over: function(args) {}
});      {% endhighlight %}




