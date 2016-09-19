---
layout: post
title: Properties, Methods and Events of ejNavigationDrawer Widget
description: API reference for ejNavigationDrawer
documentation: API
platform: js
keywords: NavigationDrawer, ejNavigationDrawer, syncfusion, NavigationDrawer api 
---

# ejNavigationDrawer




The Navigation Drawer is a sliding panel that displays the list of navigation options on demand. That is, by default, it is not visible but you can display it onto the left/right side of the screen by swiping or by clicking with desired target icon.




#### Syntax

{% highlight javascript %}

$(element).ejNavigationDrawer()

{% endhighlight %}













#### Example



{% highlight html %}
 
//create Navigation Drawer in Obtrusive way
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer();     
});
</script>{% endhighlight %}







#### Requires



* module:jQuery


* module:ej.core.js


* module:ej.navigationdrawer.js


* module:ej.listview.js




## Members








### contentId `string`
{:#members:contentid}








Specifies the contentId for navigation drawer, where the AJAX content need to updated




#### Default Value







* null








#### Example



{% highlight html %}
// Set Navigation Drawer contentId on initialization. 
//To set contentId API value 
<div id="container"> </div>
<div id="navpane">
<ul>
                <li data-ej-text="Artwork"></li>
                <li data-ej-text="Abstract"></li>
                <li data-ej-text="2 Acrylic Mediums"></li>
                <li data-ej-text="Creative Acrylic"></li>
                <li data-ej-text="Modern Painting"></li>
</ul>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("contentId","container");      
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer contentId, after initialization:
$(function () {
// Gets the contentId API value.                
$("#navpane").ejNavigationDrawer("option", "contenttId");       
// Sets the contentId API       
$("#navpane").ejNavigationDrawer ("option", "contentId", "container");  
});
</script>  {% endhighlight %}







### cssClass `string`
{:#members:cssclass}








Sets the root class for NavigationDrawer theme. This cssClass API helps to use custom skinning option for NavigationDrawer control. By defining the root class using this API, we need to include this root class in CSS.




#### Default Value







* ""








#### Example



{% highlight html %}
// Set Navigation Drawer direction on initialization. 
//To set direction API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>            
<input id="target" type="button" text="target"/>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("cssClass","customclass");     
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer cssClass, after initialization:
$(function () {
// Gets the cssClass API value.         
$("#navpane").ejNavigationDrawer("option", "cssClass"); 
// Sets the cssClass API        
$("#navpane").ejNavigationDrawer ("option", "cssClass", "customclass");  
});
</script>  {% endhighlight %}







### direction `enum`
{:#members:direction}



<ts name="ej.Direction" />




Sets the Direction for the control. See <a href="global.html#Direction">Direction</a>



<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Left</td>
<td class="type">string</td>
<td class="default">left</td>
<td class="description">Used to set Direction as Left</td>
</tr>
<tr>
<td class="name">
None</td>
<td class="type">string</td>
<td class="default">none</td>
<td class="description">Used to set Direction as None</td>
</tr>
<tr>
<td class="name">
Right</td>
<td class="type">string</td>
<td class="default">right</td>
<td class="description">Used to set Direction as Right</td>
</tr>
</tbody>
</table>



#### Default Value







* left








#### Example



{% highlight html %}
// Set Navigation Drawer direction on initialization. 
//To set direction API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("direction","left");   
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer direction, after initialization:
$(function () {
// Gets the direction API value.                
$("#navpane").ejNavigationDrawer("option", "direction");        
// Sets the direction API       
$("#navpane").ejNavigationDrawer ("option", "direction", "left");  
});
</script>  {% endhighlight %}







### enableListView `boolean`
{:#members:enablelistview}








Sets the listview to be enabled or not




#### Default Value







* false








#### Example



{% highlight html %}
// Set Navigation Drawer listview on initialization. 
//To set listview API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("enableListView","false");     
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer listview, after initialization:
$(function () {
// Gets the listview API value.         
$("#navpane").ejNavigationDrawer("option", "enableListView");   
// Sets the listview API        
$("#navpane").ejNavigationDrawer ("option", "enableListView", "false");  
});
</script>  {% endhighlight %}







### items `array`
{:#members:items}








Specifies the listview items as an array of object.




#### Default Value







* []








#### Example



{% highlight html %}
// Set Navigation Drawer listview items on initialization. 
//To set listview API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer({enableListview:true,items:[{text:"Item1"},{text:"Item2"},{text:"Item3"}]});   
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer listview items, after initialization:
$(function () {
// Gets the listViewSettings API value.         
$("#navpane").ejNavigationDrawer("option", "items");    
// Sets the listViewSettings API        
$("#navpane").ejNavigationDrawer ("option", "items", [{text:"Item1"},{text:"Item2"},{text:"Item3"}]);  
});
</script>  {% endhighlight %}







### listViewSettings `object`
{:#members:listviewsettings}








Sets all the properties of listview to render in navigation drawer





#### Example



{% highlight html %}
// Set Navigation Drawer listview on initialization. 
//To set listview API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer({model.listViewSettings{width:200});   
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer listViewSettings, after initialization:
$(function () {
// Gets the listViewSettings API value.         
$("#navpane").ejNavigationDrawer("option", "listViewSettings.width");   
// Sets the listViewSettings API        
$("#navpane").ejNavigationDrawer ("option", "listViewSettings.width", "200");  
});
</script>  {% endhighlight %}







### position `string`
{:#members:position}








Specifies position whether it is in fixed or relative to the page. See <a href="global.html#Position">Position</a>




#### Default Value







* normal








#### Example



{% highlight html %}
// Set Navigation Drawer position on initialization. 
//To set position API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("position","fixed");   
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer position, after initialization:
$(function () {
// Gets the position API value.         
$("#navpane").ejNavigationDrawer("option", "position"); 
// Sets the position API        
$("#navpane").ejNavigationDrawer ("option", "position", "fixed");  
});
</script>  {% endhighlight %}







### targetId `string`
{:#members:targetid}








Specifies the targetId for navigation drawer




#### Default Value







* ""








#### Example



{% highlight html %}
// Set Navigation Drawer direction on initialization. 
//To set direction API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>            
<input id="target" type="button" text="target"/>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("targetId","target");  
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer targetId, after initialization:
$(function () {
// Gets the targetId API value.         
$("#navpane").ejNavigationDrawer("option", "targetId"); 
// Sets the targetId API        
$("#navpane").ejNavigationDrawer ("option", "targetId", "left");  
});
</script>  {% endhighlight %}







### type `string`
{:#members:type}








Sets the rendering type of the control. See Type




#### Default Value







* overlay








#### Example



{% highlight html %}
// Set Navigation Drawer type on initialization. 
//To set type API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("type","overlay");     
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer type, after initialization:
$(function () {
// Gets the type API value.             
$("#navpane").ejNavigationDrawer("option", "type");     
// Sets the type API    
$("#navpane").ejNavigationDrawer ("option", "type", "overlay");  
});
</script>  {% endhighlight %}







### width `number`
{:#members:width}








Specifies the width of the control




#### Default Value







* auto








#### Example



{% highlight html %}
// Set Navigation Drawer width on initialization. 
//To set width API value 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$(function () {
$("#navpane").ejNavigationDrawer("width","200");        
});
</script>{% endhighlight %}


{% highlight html %}
 
<script>
//Get or set the Navigation Drawer width, after initialization:
$(function () {
// Gets the width API value.            
$("#navpane").ejNavigationDrawer("option", "width");    
// Sets the width API   
$("#navpane").ejNavigationDrawer ("option", "width", "overlay");  
});
</script>  {% endhighlight %}





## Methods








### close()
{:#methods:close}








To close the navigation drawer control





#### Example



{% highlight html %}
 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script >
$(function(){
  $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("close");
});
</script >{% endhighlight %}







### open()
{:#methods:open}








To open the navigation drawer control





#### Example



{% highlight html %}
 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script >
$(function(){
        $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("open");
});
</script >{% endhighlight %}







### toggle()
{:#methods:toggle}








To Toggle the navigation drawer control





#### Example



{% highlight html %}
 
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script >
$(function(){
        $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("toggle");
});
</script >{% endhighlight %}





## Events








### beforeClose
{:#events:beforeclose}








Event triggers before the control gets closed.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from Navigation Drawer
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
<td class="type"><ts ref="ej.NavigationDrawer.Model"/><span class="param-type">object</span></td>
<td class="description">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//BeforeClose event for Navigation pane
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$("#navpane").ejNavigationDrawer({
  beforeClose: function (args) { //handle the event
}
});   
$("#navpane").ejNavigationDrawer("close");
</script>{% endhighlight %}







### open
{:#events:open}








Event triggers when the control open.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from Navigation Drawer
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
<td class="type"><ts ref="ej.NavigationDrawer.Model"/><span class="param-type">object</span></td>
<td class="description">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//Open event for Navigation pane
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$("#navpane").ejNavigationDrawer({
  open: function (args) { //handle the event
}
});   
$("#navpane").ejNavigationDrawer("open");   
</script>{% endhighlight %}







### swipe
{:#events:swipe}








Event triggers when the Swipe happens.

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
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from Navigation Drawer
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
<td class="type"><ts ref="ej.NavigationDrawer.Model"/><span class="param-type">object</span></td>
<td class="description">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
//Swipe event for Navigation pane
<div id="home" class="navsubpage">
<div align="center" class="content">
<h2 class="title">
Home</h2>
<p>
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
</p>
</div>
</div>
<style>
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
</style>
<div id="navpane" >
<div class="list"> Home </div>
<div class="list"> Communities </div>
</div>
<script>
$("#navpane").ejNavigationDrawer({
  swipe: function (args) { //handle the event
}
});   
</script>{% endhighlight %}




