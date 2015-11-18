---
layout: post
title: ejDraggable
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejDraggable


Plugin to make any DOM element draggable.  










$(element).ejDraggable<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div  id="dragable" ></ div > 
 
<script>
// Create Dragable
$('#dragable').ejDraggable();   
</script>{% endhighlight %}







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


{% highlight html %}
 
//To set clone API value during initialization  
        $("#dragable").ejDraggable({ clone: true });                            * {% endhighlight %}


{% highlight html %}
 
//Get or set the clone API, after initialization:
        //Gets the clone value  
        $("#dragable").ejDraggable('option', 'clone');
                      {% endhighlight %}







### cursorAt<span class="type-signature type object">object</span>
{:#members:cursorat}








Sets the offset of the dragging helper relative to the mouse cursor.




Default Value:
{:.param}






* { top: -1, left: -2 }








Example
{:.example}


{% highlight html %}
 
//To set cursorAt API value during initialization  
        $("#dragable").ejDraggable({ cursorAt:  { top: 1, left: -2 } });                                * {% endhighlight %}


{% highlight html %}
 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#dragable").ejDraggable('option', 'cursorAt');
                   {% endhighlight %}







### distance<span class="type-signature type number">number</span>
{:#members:distance}








Distance in pixels after mousedown the mouse must move before dragging should start. This option can be used to prevent unwanted drags when clicking on an element.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set distance API value during initialization  
        $("#dragable").ejDraggable({ distance: 1 });                            * {% endhighlight %}


{% highlight html %}
 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#dragable").ejDraggable('option', 'distance');
                   {% endhighlight %}







### dragArea<span class="type-signature type boolean">boolean</span>
{:#members:dragarea}








If Drag area is specified.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
//To set dragArea API value during initialization  
        $("#dragable").ejDraggable({ dragArea: true });                         * {% endhighlight %}


{% highlight html %}
 
//Get or set the dragArea API, after initialization:
        //Gets the dragArea value  
        $("#dragable").ejDraggable('option', 'dragArea');
                   {% endhighlight %}







### handle<span class="type-signature type string">string</span>
{:#members:handle}








If specified, restricts drag start click to the specified element(s).




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set handle API value during initialization  
        $("#dragable").ejDraggable({ handle: null });                           * {% endhighlight %}


{% highlight html %}
 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#dragable").ejDraggable('option', 'handle');
                     {% endhighlight %}







### scope<span class="type-signature type string">string</span>
{:#members:scope}








Used to group sets of draggable and droppable items, in addition to droppable's accept option. A draggable with the same scope value as a droppable will be accepted by the droppable.




Default Value:
{:.param}






* 'default'








Example
{:.example}


{% highlight html %}
 
//To set scope API value during initialization  
        $("#dragable").ejDraggable({ scope: 'default' });                               * {% endhighlight %}


{% highlight html %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#dragable").ejDraggable('option', 'scope');
                      {% endhighlight %}





## Methods








### _destroy<span class="signature">()</span>
{:#methods:_destroy}








destroy in the dragable.





Example
{:.example}


{% highlight html %}
 
< div  id="dragable" > </div > 
 
<script>
// Create dragableObj
var dragableObj  = $("#dragable").data("ejDraggable");
dragableObj.destroy(); 
</script>{% endhighlight %}





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
 
//destroy event for Draggable
$("#dragable").ejDraggable({ 
        destroy: function(args) {}
});      {% endhighlight %}







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
 
//drag event for Draggable
$("#dragable").ejDraggable({ 
        drag: function(args) {}
});      {% endhighlight %}







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
 
//dragStart event for Draggable
$("#dragable").ejDraggable({ 
        dragStart: function(args) {}
});      {% endhighlight %}







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
 
//dragStop event for Draggable
$("#dragable").ejDraggable({ 
        dragStop: function(args) {}
});      {% endhighlight %}







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
 
//helper event for Draggable
$("#dragable").ejDraggable({ 
        helper: function () {
                return $('{% endhighlight %}




<pre>
').html("draggable").appendTo(document.body);}
});      








{% highlight html %}
<a class="" href="http://www.syncfusion.com/copyright" target="_blank">Copyright &copy; 2001 - 2015 Syncfusion Inc. All Rights Reserved</a>{% endhighlight %}




<script type="text/javascript">
prettyPrint();
</script><script src="scripts/linenumber.js" type="text/javascript">
</script><script src="scripts/main.js" type="text/javascript">
</script>
