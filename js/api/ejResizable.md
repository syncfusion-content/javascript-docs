---
layout: post
title: Properties, Methods and Events of ejResizable Widget
description: API reference for ejResizable
documentation: API
platform: js
keywords: Resizable, ejResizable, syncfusion, Resizable api  
---

# ejResizable


Plugin to make any DOM element Resizable.  



#### Syntax

{% highlight javascript %}

$(element).ejResizable()

{% endhighlight %}



#### Example



{% highlight html %}
 
<div  id="resizing" /> 
 
 {% endhighlight %}


{% highlight javascript %}
<script>
// Create resizing
$('#resizing').ejResizable();   
</script>{% endhighlight %}







#### Requires


* module:jQuery


* module:ej.core




## Members








### cursorAt `object`
{:#members:cursorat}








Sets the offset of the resizing helper relative to the mouse cursor.




#### Default Value







* { top: -1, left: -2 }








#### Example



{% highlight javascript %}
 
//To set cursorAt API value during initialization  
        $("#resizing").ejResizable({ cursorAt:  { top: 1, left: -2 } });                                
        
{% endhighlight %}


{% highlight javascript %}
 
//Get or set the cursorAt API, after initialization:
        //Gets the cursorAt value  
        $("#resizing").ejResizable('option', 'cursorAt');
                   
 {% endhighlight %}







### distance `number`
{:#members:distance}








Distance in pixels after mousedown the mouse must move before resizing should start. This option can be used to prevent unwanted drags when clicking on an element.




#### Default Value







* 1








#### Example



{% highlight javascript %}
 
//To set distance API value during initialization  
        $("#resizing").ejResizable({ distance: 1 });                            
      
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the distance API, after initialization:
        //Gets the distance value  
        $("#resizing").ejResizable('option', 'distance');
                   
{% endhighlight %}







### handle `string`
{:#members:handle}








If specified, restricts resize start click to the specified element(s).




#### Default Value







* null








#### Example



{% highlight javascript %}
 
//To set handle API value during initialization  
        $("#resizing").ejResizable({ handle: null });                           
        
{% endhighlight %}


{% highlight javascript %}
 
//Get or set the handle API, after initialization:
        //Gets the handle value  
        $("#resizing").ejResizable('option', 'handle');
                     
 {% endhighlight %}







### maxHeight `number`
{:#members:maxheight}








Sets the max height for resizing




#### Default Value







* null








#### Example



{% highlight javascript %}
 
//To set maxHeight API value during initialization  
        $("#resizing").ejResizable({ maxHeight: null });                                
    
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the maxHeight API, after initialization:
        //Gets the maxHeight value  
        $("#resizing").ejResizable('option', 'maxHeight');
                 
  {% endhighlight %}







### maxWidth `number`
{:#members:maxwidth}








Sets the max width for resizing




#### Default Value







* null








#### Example



{% highlight javascript %}
 
//To set maxWidth API value during initialization  
        $("#resizing").ejResizable({ maxWidth: null });                         
     
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the maxWidth API, after initialization:
        //Gets the maxWidth value  
        $("#resizing").ejResizable('option', 'maxWidth');
                   
 {% endhighlight %}







### minHeight `number`
{:#members:minheight}








Sets the min Height for resizing




#### Default Value







* 10








#### Example



{% highlight javascript %}
 
//To set minHeight API value during initialization  
        $("#resizing").ejResizable({ minHeight: null });                                
   
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the minHeight API, after initialization:
        //Gets the minHeight value  
        $("#resizing").ejResizable('option', 'minHeight');
                  
  {% endhighlight %}







### minWidth `number`
{:#members:minwidth}








Sets the min Width for resizing




#### Default Value







* 10








#### Example



{% highlight javascript %}
 
//To set minWidth API value during initialization  
        $("#resizing").ejResizable({ minWidth: null });                         
     
  {% endhighlight %}


{% highlight javascript %}
 
//Get or set the minWidth API, after initialization:
        //Gets the minWidth value  
        $("#resizing").ejResizable('option', 'minWidth');
                   
                   
{% endhighlight %}







### scope `string`
{:#members:scope}








Used to group sets of resizable items.




#### Default Value







* 'default'








#### Example



{% highlight javascript %}
 
//To set scope API value during initialization  
        $("#resizing").ejResizable({ scope: 'default' });                               
     
 {% endhighlight %}


{% highlight javascript %}
 
//Get or set the scope API, after initialization:
        //Gets the scope value  
        $("#resizing").ejResizable('option', 'scope');
                     
 {% endhighlight %}





## Methods








### _destroy()
{:#methods:_destroy}








destroy in the Resizable.





#### Example



{% highlight html %}
 
< div  id="resizing" > </div > 
 
{% endhighlight %}


{% highlight javascript %}

<script>
// Create resizingObj
var resizingObj  = $("#resizing").data("ejResizable");
resizingObj.destroy(); 
</script>

{% endhighlight %}





## Events








### destroy
{:#events:destroy}








This event is triggered when the widget destroys.

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
<td class="type"><ts ref="ej.Resizable.Model"/><span class="param-type">object</span></td>
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
 
//destroy event for Resizable
$("#resizing").ejResizable({ 
        destroy: function(args) {}
});     

 {% endhighlight %}







### helper
{:#events:helper}








This event is triggered when resized.

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
<td class="type"><ts ref="ej.Resizable.Model"/><span class="param-type">object</span></td>
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
 
//helper event for Resizable
$("#resizing").ejResizable({ 
        helper: function () {
               return $('<pre>').html("resizable").appendTo(document.body);}
});      

{% endhighlight %}






### resize
{:#events:resize}








{% highlight html %}
This event is triggered when the resizing in progress.{% endhighlight %}

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
<td class="type"><ts ref="ej.Resizable.Model"/><span class="param-type">object</span></td>
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
 
//resizeStart event for Resizable
$("#resizing").ejResizable({ 
        resize: function(args) {}
});     
 {% endhighlight %}







### resizeStart
{:#events:resizestart}








This event is triggered when the resizing is start.

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
<td class="type"><ts ref="ej.Resizable.Model"/><span class="param-type">object</span></td>
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
<td class="type"><ts ref="ej.Resizable.Model"/><span class="param-type">object</span></td>
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
 
//resizeStop event for Resizable
$("#resizing").ejResizable({ 
        resizeStop: function(args) {}
});      {% endhighlight %}




