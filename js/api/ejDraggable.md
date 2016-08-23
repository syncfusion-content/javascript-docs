---
layout: post
title: Properties, Methods and Events of ejDraggable Widget
description: API reference for ejDraggable
documentation: API
platform: js
keywords: Draggable, ejDraggable, syncfusion, Draggable api
 
---

# ejDraggable

Plugin to make any DOM element draggable.  



#### Syntax

{% highlight javascript %}

$(element).ejDraggable()

{% endhighlight %}



#### Example



{% highlight html %}
 
<div id="dragable"/>

 {% endhighlight %}
 
{% highlight javascript %}
<script>
// Create Dragable
$('#dragable').ejDraggable();   
</script>{% endhighlight %}



#### Requires


* module:jQuery


* module:ej.core


* module:ej.draggable


## Members



### clone `boolean`
{:#members:clone}




If clone is specified.




#### Default Value







* false








#### Example



{% highlight javascript %}
 
//To set clone API value during initialization  
        $("#dragable").ejDraggable({ clone: true });                           
        
{% endhighlight %}


{% highlight javascript %}
 
//Get or set the clone API, after initialization:
        //Gets the clone value  
        $("#dragable").ejDraggable('option', 'clone');
                      
{% endhighlight %}







### cursorAt `object`
{:#members:cursorat}








Sets the offset of the dragging helper relative to the mouse cursor.




#### Default Value







* { top: -1, left: -2 }








#### Example



{% highlight javascript %}
 
//To set cursorAt API value during initialization  
        $("#dragable").ejDraggable({ cursorAt:  { top: 1, left: -2 } });                                
       
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#dragable").ejDraggable('option', 'cursorAt');
                   
{% endhighlight %}




### distance `number`
{:#members:distance}



Distance in pixels after mousedown the mouse must move before dragging should start. This option can be used to prevent unwanted drags when clicking on an element.



#### Default Value




* 1




#### Example



{% highlight javascript %}
 
//To set distance API value during initialization  
        $("#dragable").ejDraggable({ distance: 1 });                            
        
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#dragable").ejDraggable('option', 'distance');
                   
 {% endhighlight %}







### dragArea `boolean`
{:#members:dragarea}








The drag area is used to restrict the dragging element bounds.




#### Default Value







* false








#### Example



{% highlight javascript %}
 
//To set dragArea API value during initialization  
        $("#dragable").ejDraggable({ dragArea: true });                         
        
{% endhighlight %}


{% highlight javascript %}
 
//Get or set the dragArea API, after initialization:
        //Gets the dragArea value  
        $("#dragable").ejDraggable('option', 'dragArea');
                   
{% endhighlight %}







### handle `string`
{:#members:handle}








If specified, restricts drag start click to the specified element(s).




#### Default Value







* null








#### Example



{% highlight javascript %}
 
//To set handle API value during initialization  
        $("#dragable").ejDraggable({ handle: null });                           
      
  {% endhighlight %}


{% highlight javascript %}
 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#dragable").ejDraggable('option', 'handle');
                     
  {% endhighlight %}







### scope `string`
{:#members:scope}




Used to group sets of draggable and droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.




#### Default Value







* 'default'








#### Example



{% highlight javascript %}
 
//To set scope API value during initialization  
        $("#dragable").ejDraggable({ scope: 'default' });                               
        
{% endhighlight %}


{% highlight javascript %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#dragable").ejDraggable('option', 'scope');
                     
 {% endhighlight %}





## Methods








### _destroy()
{:#methods:_destroy}








destroy in the draggable.





#### Example



{% highlight html %}
 
< div  id="dragable" > </div > 
 
{% endhighlight %}


{% highlight javascript %}
<script>
// Create dragableObj
var dragableObj  = $("#dragable").data("ejDraggable");
dragableObj.destroy(); 
</script>

{% endhighlight %}





## Events








### destroy
{:#events:destroy}








This event is triggered when dragging element is destroyed.

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Draggable.Model"/><span class="param-type">object</span></td>
<td class="description">returns the autocomplete model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>




#### Example



{% highlight javascript %}
 
//destroy event for Draggable
$("#dragable").ejDraggable({ 
        destroy: function(args) {}
});      

{% endhighlight %}







### drag
{:#events:drag}





This event is triggered when the mouse is moved during the dragging.

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Draggable.Model"/><span class="param-type">object</span></td>
<td class="description">returns the draggable model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current draggable element object</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event model values</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the exact mouse down target element</td>
</tr>
</tbody>
</table>




#### Example



{% highlight javascript %}
 
//drag event for Draggable
$("#dragable").ejDraggable({ 
        drag: function(args) {}
});      
{% endhighlight %}







### dragStart
{:#events:dragstart}




Supply a callback function to handle the drag start event as an init option.

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Draggable.Model"/><span class="param-type">object</span></td>
<td class="description">returns the draggable model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current draggable element object</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event model values</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the exact mouse down target element</td>
</tr>
</tbody>
</table>




#### Example



{% highlight javascript %}
 
//dragStart event for Draggable
$("#dragable").ejDraggable({ 
        dragStart: function(args) {}
});      

{% endhighlight %}




### dragStop
{:#events:dragstop}




This event is triggered when the mouse is moved during the dragging.

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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.Draggable.Model"/><span class="param-type">object</span></td>
<td class="description">returns the draggable model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the current draggable element object</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event model values</td>
</tr>
<tr>
<td class="name">
target</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the exact mouse down target element</td>
</tr>
</tbody>
</table>




#### Example



{% highlight javascript %}
 
//dragStop event for Draggable
$("#dragable").ejDraggable({ 
        dragStop: function(args) {}
});     
 {% endhighlight %}







### helper
{:#events:helper}




This event is triggered when dragged.

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
<td class="name">
element</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the draggable element object</td>
</tr>
<tr>
<td class="name">
sender</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event model values</td>
</tr>
<tr>
</tbody>
</table>




#### Example



{% highlight javascript %}
 
//helper event for Draggable
$("#dragable").ejDraggable({ 
        helper: function () {
                return $('<pre>').html("draggable").appendTo(document.body);}
});   
                
                            
{% endhighlight %}

