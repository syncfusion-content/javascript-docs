---
layout: post
title: ejDroppable
description: API reference for ejDroppable
documentation: API
platform: js
keywords: Droppable, ejDroppable, syncfusion, Droppable api
---

# ejDroppable


Plugin to make any DOM element Droppable.  


#### Syntax

{% highlight js %}

$(element).ejDroppable()

{% endhighlight %}



#### Example



{% highlight html %}
 
<div  id="dropable" />
 
<script>
// Create Dragable
$('#dropable').ejDroppable();   
</script>

{% endhighlight %}



#### Requires


* module:jQuery


* module:ej.core



## Members


### accept `object`
{:#members:accept}



Used to accept the droppable items.




#### Default Value



* null



#### Example



{% highlight html %}
 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ accept: null });                          
        
{% endhighlight %}


{% highlight html %}
 
//Get or set the accept API, after initialization:
        //Gets the accept value  
        $("#droppable").ejDroppable('option', 'accept');
                    
{% endhighlight %}




### scope `string`
{:#members:scope}


Used to group sets of droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.


#### Default Value



* 'default'




#### Example



{% highlight html %}
 
//To set scope API value during initialization  
        $("#droppable").ejDroppable({ scope: 'default' });                             
                
{% endhighlight %}


{% highlight html %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#droppable").ejDroppable('option', 'scope');
                     
{% endhighlight %}





## Methods



### _destroy()
{:#methods:_destroy}

destroy in the Droppable.


#### Example


{% highlight html %}
 
< div  id="droppable" > </div > 
 
<script>
// Create droppabaleObj
var droppabaleObj  = $("#droppable").data("ejDroppable");
droppabaleObj.destroy(); 
</script>

{% endhighlight %}



## Events



### drop
{:#events:drop}



This event is triggered when the mouse up is moved during the dragging.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        drop: function(args) {}
});      

{% endhighlight %}





### out
{:#events:out}


This event is triggered when the mouse is moved out.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        out: function(args) {}
});      

{% endhighlight %}







### over
{:#events:over}


This event is triggered when the mouse is moved over.

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//drop event for Droppable
$("#droppable").ejDroppable({ 
        over: function(args) {}
});     

 {% endhighlight %}




