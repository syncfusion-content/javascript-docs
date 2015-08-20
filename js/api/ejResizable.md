---
layout: post
title: ejResizable
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for resizing HTML elements.










$(element).ejResizable<span class="signature">()</span>











Example
{:.example}


{% highlight html %}
 
<div  id="resizing" ></ div > 
 
<script>
// Create resizing
$('#resizing').ejResizable();   
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core




## Members








### cursorAt<span class="type-signature type object">object</span>
{:#members:cursorat}








Sets the offset of the resizing helper relative to the mouse cursor.




Default Value:
{:.param}






* { top: -1, left: -2 }








Example
{:.example}


{% highlight html %}
 
//To set cursorAt API value during initialization  
        $("#resizing").ejResizable({ cursorAt:  { top: 1, left: -2 } });                                * {% endhighlight %}


{% highlight html %}
 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#resizing").ejResizable('option', 'cursorAt');
                   {% endhighlight %}







### distance<span class="type-signature type number">number</span>
{:#members:distance}








Distance in pixels after mousedown the mouse must move before resizing should start. This option can be used to prevent unwanted drags when clicking on an element.




Default Value:
{:.param}






* 1








Example
{:.example}


{% highlight html %}
 
//To set distance API value during initialization  
        $("#resizing").ejResizable({ distance: 1 });                            * {% endhighlight %}


{% highlight html %}
 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#resizing").ejResizable('option', 'distance');
                   {% endhighlight %}







### handle<span class="type-signature type string">string</span>
{:#members:handle}








If specified, restricts resize start click to the specified element(s).




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set handle API value during initialization  
        $("#resizing").ejResizable({ handle: null });                           * {% endhighlight %}


{% highlight html %}
 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#resizing").ejResizable('option', 'handle');
                     {% endhighlight %}







### maxHeight<span class="type-signature type number">number</span>
{:#members:maxheight}








Sets the max height for resizing




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set maxHeight API value during initialization  
        $("#resizing").ejResizable({ maxHeight: null });                                * {% endhighlight %}


{% highlight html %}
 
//Get or set the maxHeight API, after initialization:
        //Gets the maxHeight value  
        $("#resizing").ejResizable('option', 'maxHeight');
                  {% endhighlight %}







### maxWidth<span class="type-signature type number">number</span>
{:#members:maxwidth}








Sets the max width for resizing




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
//To set maxWidth API value during initialization  
        $("#resizing").ejResizable({ maxWidth: null });                         * {% endhighlight %}


{% highlight html %}
 
//Get or set the maxWidth API, after initialization:
        //Gets the maxWidth value  
        $("#resizing").ejResizable('option', 'maxWidth');
                   {% endhighlight %}







### minHeight<span class="type-signature type number">number</span>
{:#members:minheight}








Sets the min Height for resizing




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
//To set minHeight API value during initialization  
        $("#resizing").ejResizable({ minHeight: null });                                * {% endhighlight %}


{% highlight html %}
 
//Get or set the minHeight API, after initialization:
        //Gets the minHeight value  
        $("#resizing").ejResizable('option', 'minHeight');
                  {% endhighlight %}







### minWidth<span class="type-signature type number">number</span>
{:#members:minwidth}








Sets the min Width for resizing




Default Value:
{:.param}






* 10








Example
{:.example}


{% highlight html %}
 
//To set minWidth API value during initialization  
        $("#resizing").ejResizable({ minWidth: null });                         * {% endhighlight %}


{% highlight html %}
 
//Get or set the minWidth API, after initialization:
        //Gets the minWidth value  
        $("#resizing").ejResizable('option', 'minWidth');
                   {% endhighlight %}







### scope<span class="type-signature type string">string</span>
{:#members:scope}








Used to group sets of resizeable items.




Default Value:
{:.param}






* 'default'








Example
{:.example}


{% highlight html %}
 
//To set scope API value during initialization  
        $("#resizing").ejResizable({ scope: 'default' });                               * {% endhighlight %}


{% highlight html %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#resizing").ejResizable('option', 'scope');
                      {% endhighlight %}





## Methods








### _destroy<span class="signature">()</span>
{:#methods:_destroy}








destroy in the Resizable.





Example
{:.example}


{% highlight html %}
 
< div  id="resizing" > </div > 
 
<script>
// Create resizingObj
var resizingObj  = $("#resizing").data("ejResizable");
resizingObj.destroy(); 
</script>{% endhighlight %}





## Events








### destroy
{:#events:destroy}








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
 
//destroy event for Resizable
$("#resizing").ejResizable({ 
        destroy: function(args) {}
});      {% endhighlight %}







### helper
{:#events:helper}








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
 
//helper event for Resizable
$("#resizing").ejResizable({ 
        helper: function () {
               return $('{% endhighlight %}




<pre>
').html("resizable").appendTo(document.body);}
});      







### {% highlight html %}
resize{% endhighlight %}
{:#events:}








{% highlight html %}
This event is triggered when the resizing in progress.{% endhighlight %}

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
 
//resizeStart event for Resizable
$("#resizing").ejResizable({ 
        resize: function(args) {}
});      {% endhighlight %}







### resizeStart
{:#events:resizestart}








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
 
//resizeStart event for Resizable
$("#resizing").ejResizable({ 
        resizeStart: function(args) {}
});      {% endhighlight %}







### resizeStop
{:#events:resizestop}








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
 
//resizeStop event for Resizable
$("#resizing").ejResizable({ 
        resizeStop: function(args) {}
});      {% endhighlight %}




