---
layout: post
title: ejNavigationDrawer
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html Navigation Drawer control.










#### $(element).ejNavigationDrawer<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
//create Navigation Drawer in Obtrusive way
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer();     
});
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.core.js


* module:ej.navigationdrawer.js


* module:ej.listview.js




### Members








#### contentid<span class="type-signature type string">string</span>








Specifies the contentId for navigation drawer, where the ajax content need to updated




Default Value:






* null








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer contentId on initialization. 
//To set contentId API value 
&lt;div id="container"&gt; &lt;/div&gt;
&lt;div id="navpane"&gt;
&lt;ul&gt;
                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;
                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;
                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("contentId","container");      
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer contentId, after initialization:
$(function () {
// Gets the contentId API value.                
$("#navpane").ejNavigationDrawer("option", "contenttId");       
// Sets the contentId API       
$("#navpane").ejNavigationDrawer ("option", "contentId", "container");  
});
&lt;/script&gt;  </code>
</pre>






#### cssclass<span class="type-signature type string">string</span>








Sets the root class for NavigationDrawer theme. This cssClass API helps to use custom skinning option for NavigationDrawer control. By defining the root class using this API, we need to include this root class in CSS.




Default Value:






* ""








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer direction on initialization. 
//To set direction API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;            
&lt;input id="target" type="button" text="target"/&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("cssClass","customclass");     
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer cssClass, after initialization:
$(function () {
// Gets the cssClass API value.         
$("#navpane").ejNavigationDrawer("option", "cssClass"); 
// Sets the cssClass API        
$("#navpane").ejNavigationDrawer ("option", "cssClass", "customclass");  
});
&lt;/script&gt;  </code>
</pre>






#### direction<span class="type-signature type enum">enum</span>








Sets the Direction for the control. See <a href="global.html#Direction">Direction</a>




Default Value:






* left








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer direction on initialization. 
//To set direction API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("direction","left");   
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer direction, after initialization:
$(function () {
// Gets the direction API value.                
$("#navpane").ejNavigationDrawer("option", "direction");        
// Sets the direction API       
$("#navpane").ejNavigationDrawer ("option", "direction", "left");  
});
&lt;/script&gt;  </code>
</pre>






#### enablelistview<span class="type-signature type boolean">boolean</span>








Sets the listview to be enabled or not




Default Value:






* false








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer listview on initialization. 
//To set listview API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("enableListView","false");     
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer listview, after initialization:
$(function () {
// Gets the listview API value.         
$("#navpane").ejNavigationDrawer("option", "enableListView");   
// Sets the listview API        
$("#navpane").ejNavigationDrawer ("option", "enableListView", "false");  
});
&lt;/script&gt;  </code>
</pre>






#### items<span class="type-signature type array">array</span>








Specifies the listview items as an array of object.




Default Value:






* []








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer listview items on initialization. 
//To set listview API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer({enableListview:true,items:[{text:"Item1"},{text:"Item2"},{text:"Item3"}]});   
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer listview items, after initialization:
$(function () {
// Gets the listViewSettings API value.         
$("#navpane").ejNavigationDrawer("option", "items");    
// Sets the listViewSettings API        
$("#navpane").ejNavigationDrawer ("option", "items", [{text:"Item1"},{text:"Item2"},{text:"Item3"}]);  
});
&lt;/script&gt;  </code>
</pre>






#### listviewsettings<span class="type-signature type object">object</span>








Sets all the properties of listview to render in navigation drawer





##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer listview on initialization. 
//To set listview API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer({model.listViewSettings{width:200});   
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer listViewSettings, after initialization:
$(function () {
// Gets the listViewSettings API value.         
$("#navpane").ejNavigationDrawer("option", "listViewSettings.width");   
// Sets the listViewSettings API        
$("#navpane").ejNavigationDrawer ("option", "listViewSettings.width", "200");  
});
&lt;/script&gt;  </code>
</pre>






#### position<span class="type-signature type enum">enum</span>








Specifies position whether it is in fixed or relative to the page. See <a href="global.html#Position">Position</a>




Default Value:






* normal








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer position on initialization. 
//To set position API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("position","fixed");   
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer position, after initialization:
$(function () {
// Gets the position API value.         
$("#navpane").ejNavigationDrawer("option", "position"); 
// Sets the position API        
$("#navpane").ejNavigationDrawer ("option", "position", "fixed");  
});
&lt;/script&gt;  </code>
</pre>






#### targetid<span class="type-signature type string">string</span>








Specifies the targetId for navigation drawer




Default Value:






* ""








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer direction on initialization. 
//To set direction API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;            
&lt;input id="target" type="button" text="target"/&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("targetId","target");  
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer targetId, after initialization:
$(function () {
// Gets the targetId API value.         
$("#navpane").ejNavigationDrawer("option", "targetId"); 
// Sets the targetId API        
$("#navpane").ejNavigationDrawer ("option", "targetId", "left");  
});
&lt;/script&gt;  </code>
</pre>






#### type<span class="type-signature type enum">enum</span>








Sets the rendering type of the control. See Type




Default Value:






* overlay








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer type on initialization. 
//To set type API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("type","overlay");     
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer type, after initialization:
$(function () {
// Gets the type API value.             
$("#navpane").ejNavigationDrawer("option", "type");     
// Sets the type API    
$("#navpane").ejNavigationDrawer ("option", "type", "overlay");  
});
&lt;/script&gt;  </code>
</pre>






#### width<span class="type-signature type int">int</span>








Specifies the width of the control




Default Value:






* auto








##### Examples

<pre class="prettyprint">
<code>// Set Navigation Drawer width on initialization. 
//To set width API value 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$(function () {
$("#navpane").ejNavigationDrawer("width","200");        
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;script&gt;
//Get or set the Navigation Drawer width, after initialization:
$(function () {
// Gets the width API value.            
$("#navpane").ejNavigationDrawer("option", "width");    
// Sets the width API   
$("#navpane").ejNavigationDrawer ("option", "width", "overlay");  
});
&lt;/script&gt;  </code>
</pre>




### Methods








#### close<span class="signature">()</span>








To close the navigation drawer control





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script &gt;
$(function(){
  $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("close");
});
&lt;/script &gt;</code>
</pre>






#### open<span class="signature">()</span>








To open the navigation drawer control





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script &gt;
$(function(){
        $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("open");
});
&lt;/script &gt;</code>
</pre>






#### toggle<span class="signature">()</span>








To Toggle the navigation drawer control





##### Example

<pre class="prettyprint">
<code> 
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script &gt;
$(function(){
        $("#navpane").ejNavigationDrawer();
  $("#navpane").ejNavigationDrawer("toggle");
});
&lt;/script &gt;</code>
</pre>




### Events








#### beforeclose








Event triggers before the control gets closed.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Navigation Drawer
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//BeforeClose event for Navigation pane
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#navpane").ejNavigationDrawer({
  beforeClose: function (args) { //handle the event
}
});   
$("#navpane").ejNavigationDrawer("close");
&lt;/script&gt;</code>
</pre>






#### open








Event triggers when the control open.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Navigation Drawer
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//Open event for Navigation pane
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#navpane").ejNavigationDrawer({
  open: function (args) { //handle the event
}
});   
$("#navpane").ejNavigationDrawer("open");   
&lt;/script&gt;</code>
</pre>






#### swipe








Event triggers when the Swipe happens.

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
<td class="name"><code>argument</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from Navigation Drawer
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">returns the Navigation Drawer model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>item</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the item of element</td>
</tr>
<tr>
<td class="name"><code>itemName</code></td>
<td class="type"><span class="param-type">String</span></td>
<td class="description last">returns the name of item</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
//Swipe event for Navigation pane
&lt;div id="home" class="navsubpage"&gt;
&lt;div align="center" class="content"&gt;
&lt;h2 class="title"&gt;
Home&lt;/h2&gt;
&lt;p&gt;
Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.
&lt;/p&gt;
&lt;/div&gt;
&lt;/div&gt;
&lt;style&gt;
.list {
  border-bottom: 1px solid;
  line-height: 50px;
  text-align: center;
  width:200px;
  }
&lt;/style&gt;
&lt;div id="navpane" &gt;
&lt;div class="list"&gt; Home &lt;/div&gt;
&lt;div class="list"&gt; Communities &lt;/div&gt;
&lt;/div&gt;
&lt;script&gt;
$("#navpane").ejNavigationDrawer({
  swipe: function (args) { //handle the event
}
});   
&lt;/script&gt;</code>
</pre>



