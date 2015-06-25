---
layout: post
title: ejmNavigationDrawer
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html Navigation Drawer control.





$(element).ejmNavigationDrawer<span class="signature">()</span>






Example
{:.example}
<pre class="prettyprint"><code> //create Navigation Drawer in Unobtrusive way&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-type="overlay" data-ej-position="fixed"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> //create Navigation Drawer in Obtrusive way&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer();    });&lt;/script&gt;</code></pre>



Requires
{:.require}


* module:jQuery

* module:ej.mobile.application

* module:ej.core

* module:ej.unobtrusive

* module:ej.mobile.core

* module:ej.data

* module:ej.touch

* module:ej.mobile.listview

* module:ej.mobile.scrollpanel

* module:ej.mobile.menu

* module:ej.navigationdrawerbase


## Members




### allowScrolling<span class="type-signature type boolean">boolean</span>




While set as true, enables scrollpanel inside the element.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the allowscrolling property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-allowscrolling="true"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Navigation Drawer Scrolling on initialization. //To set scrolling API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("allowScrolling","true");     });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the Navigation Drawer allowscrolling, after initialization:$(function () {// Gets the allowscrolling API value.           $("#navpane").ejmNavigationDrawer("option", "allowScrolling");  // Sets the allowscrolling API  $("#navpane").ejmNavigationDrawer ("option", "allowScrolling", false);  });&lt;/script&gt;  </code></pre>



### considerSubPage<span class="type-signature type boolean">boolean</span>




When set as true, the control will render inside the closest subpage.


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the allowscrolling property in unobtrusive way.//Set the allowscrolling property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-considersubpage="true"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer considersubpage on initialization. //To set scrolling API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("considerSubPage","true");    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the Navigation Drawer allowscrolling, after initialization:$(function () {// Gets the Considersubpage API value.          $("#navpane").ejmNavigationDrawer("option", "considerSubPage"); // Sets the Considersubpage API $("#navpane").ejmNavigationDrawer ("option", "considerSubPage", false);  });&lt;/script&gt;  </code></pre>



### contentId<span class="type-signature type string">string</span>




Specifies the contentId for navigation drawer, where the ajax content need to updated


Default Value:
{:.param}



* null




Example
{:.example}
<pre class="prettyprint"><code> //Set the contentId property in unobtrusive way.&lt;div id="container"&gt; &lt;/div&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-contentid="container" &gt;&lt;ul&gt;                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer contentId on initialization. //To set contentId API value &lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-contentid="container" &gt;&lt;ul&gt;                &lt;li data-ej-text="Artwork"&gt;&lt;/li&gt;                &lt;li data-ej-text="Abstract"&gt;&lt;/li&gt;                &lt;li data-ej-text="2 Acrylic Mediums"&gt;&lt;/li&gt;                &lt;li data-ej-text="Creative Acrylic"&gt;&lt;/li&gt;                &lt;li data-ej-text="Modern Painting"&gt;&lt;/li&gt;&lt;/ul&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("contentId","container");     });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer contentId, after initialization:&lt;script&gt;// Gets the contentId API value.                 $("#navpane").ejmNavigationDrawer ("option", "contentId");             // Sets the contentId API$("#navpane").ejmNavigationDrawer ("option", "contentId", "container");   &lt;/script&gt;</code></pre>



### cssclass<span class="type-signature type string">string</span>




Sets the root class for NavigationDrawer theme. This cssClass API helps to use custom skinning option for NavigationDrawer control. By defining the root class using this API, we need to include this root class in CSS.


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the direction property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt; input id="target" data-role="button" type="button" /&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-cssclass="customclass" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer direction on initialization. //To set direction API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt; input id="target" data-role="button" type="button" /&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("cssClass","customclass");    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer cssClass, after initialization:&lt;script&gt;// Gets the cssClass API value.          $("#navpane").ejmNavigationDrawer ("option", "cssClass");              // Sets the cssClass API$("#navpane").ejmNavigationDrawer ("option", "cssClass", "customclass");   &lt;/script&gt;</code></pre>



### direction<span class="type-signature type enum">enum</span>




Sets the Direction for the control. See Direction


Default Value:
{:.param}



* left




Example
{:.example}
<pre class="prettyprint"><code> //Set the direction property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-direction="left" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer direction on initialization. //To set direction API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("direction","left");  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> &lt;script&gt;//Get or set the Navigation Drawer direction, after initialization:$(function () {// Gets the direction API value.                $("#navpane").ejNavigationDrawer("option", "direction");        // Sets the direction API       $("#navpane").ejNavigationDrawer ("option", "direction", "left");  });&lt;/script&gt;  </code></pre>



### enablelistview<span class="type-signature type boolean">boolean</span>




Sets the listview to be enabled or not


Default Value:
{:.param}



* false




Example
{:.example}
<pre class="prettyprint"><code> //Set the listview property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-enablelistview="false" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer listview on initialization. //To set listview API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("enableListView","false");    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer listview, after initialization:&lt;script&gt;// Gets the listview API value.          $("#navpane").ejmNavigationDrawer ("option", "enableListView");                // Sets the listview API$("#navpane").ejmNavigationDrawer ("option", "enableListView", false);   &lt;/script&gt;</code></pre>



### items<span class="type-signature type array">array</span>




Specifies the listview items as an array of object.


Default Value:
{:.param}



* []




Example
{:.example}
<pre class="prettyprint"><code> //Set the listView items property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-items=window.lvItems &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer listview items on initialization. //To set listview items API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer({enableListview:true,items:[{text:"Item1"},{text:"Item2"},{text:"Item3"}]});  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer listview item, after initialization:&lt;script&gt;// Gets the listview item API value.             $("#navpane").ejmNavigationDrawer ("option", "items"); // Sets the listview item API$("#navpane").ejmNavigationDrawer ("option", "items", [{text:"Item1"},{text:"Item2"},{text:"Item3"}]);   &lt;/script&gt;</code></pre>



### listviewsettings<span class="type-signature type object">object</span>




Sets all the properties of listview to render in navigation drawer



Example
{:.example}
<pre class="prettyprint"><code> //Set the listView Settings property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-listviewsettings-width="200" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer listview settings on initialization. //To set listview settings API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer({model.listViewSettings{width:200});  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer listViewSettings, after initialization:&lt;script&gt;// Gets the listViewSettings API value.          $("#navpane").ejmNavigationDrawer ("option", "listViewSettings.width");        // Sets the listViewSettings API$("#navpane").ejmNavigationDrawer ("option", "listViewSettings.width", "200");   &lt;/script&gt;</code></pre>



### position<span class="type-signature type enum">enum</span>




Specifies position whether it is in fixed or relative to the page. See <a href="global.html#Position">Position</a>


Default Value:
{:.param}



* normal




Example
{:.example}
<pre class="prettyprint"><code> //Set the position property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-position="fixed" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer position on initialization. //To set position API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("position","fixed");  });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer position, after initialization:&lt;script&gt;// Gets the position API value.          $("#navpane").ejmNavigationDrawer ("option", "position");              // Sets the position API$("#navpane").ejmNavigationDrawer ("option", "position", "fixed");   &lt;/script&gt;</code></pre>



### renderMode<span class="type-signature type enum">enum</span>




Changes the rendering mode. See <a href="global.html#RenderMode">RenderMode</a>


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the renderMode property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-rendermode="auto"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Navigation Drawer renderMode on initialization. //To set renderMode API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("renderMode","auto"); });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer renderMode, after initialization:&lt;script&gt;// Gets the renderMode API value.                $("#navpane").ejmNavigationDrawer ("option", "renderMode");                    // Sets the renderMode API$("#navpane").ejmNavigationDrawer ("option", "renderMode", ej.mobile.RenderMode.Auto);   &lt;/script&gt;</code></pre>



### scrollSettings




Used to set scrollpanel related properties to the navigation drawer






### targetid<span class="type-signature type string">string</span>




Specifies the targetId for navigation drawer


Default Value:
{:.param}



* ""




Example
{:.example}
<pre class="prettyprint"><code> //Set the direction property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt; input id="target" data-role="button" type="button" /&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-targetid="target" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer direction on initialization. //To set direction API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt; input id="target" data-role="button" type="button" /&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("targetId","left");   });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer targetId, after initialization:&lt;script&gt;// Gets the TargetId API value.          $("#navpane").ejmNavigationDrawer ("option", "targetId");              // Sets the TargetId API$("#navpane").ejmNavigationDrawer ("option", "targetId", "sample");   &lt;/script&gt;</code></pre>



### theme<span class="type-signature type enum">enum</span>




Changes the Theme of the control


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the Theme property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-theme="auto"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code> // Set Navigation Drawer renderMode on initialization. //To set Theme API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane"&gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("theme","auto");      });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer Theme, after initialization:&lt;script&gt;// Gets the Theme API value.             $("#navpane").ejmNavigationDrawer ("option", "theme");                 // Sets the Theme API$("#navpane").ejmNavigationDrawer ("option", "theme", ej.mobile.Theme.Auto);   &lt;/script&gt;</code></pre>



### type<span class="type-signature type enum">enum</span>




Sets the rendering type of the control. See <a href="global.html#Type">Type</a>


Default Value:
{:.param}



* overlay




Example
{:.example}
<pre class="prettyprint"><code> //Set the type property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-type="overlay" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer type on initialization. //To set type API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("type","overlay");    });&lt;/script&gt;</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer type, after initialization:&lt;script&gt;// Gets the type API value.              $("#navpane").ejmNavigationDrawer ("option", "type");          // Sets the type API$("#navpane").ejmNavigationDrawer ("option", "type", "overlay");   &lt;/script&gt;</code></pre>



### width<span class="type-signature type int">int</span>




Specifies the width of the control


Default Value:
{:.param}



* auto




Example
{:.example}
<pre class="prettyprint"><code> //Set the width property in unobtrusive way.&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-width="200" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;</code></pre><pre class="prettyprint"><code>// Set Navigation Drawer width on initialization. //To set width API value &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$(function () {$("#navpane").ejmNavigationDrawer("width","200");       });</code></pre><pre class="prettyprint"><code> //Get or set the Navigation Drawer width, after initialization:&lt;script&gt;// Gets the type API value.              $("#navpane").ejmNavigationDrawer ("option", "width");         // Sets the type API$("#navpane").ejmNavigationDrawer ("option", "width", "auto");   &lt;/script&gt;</code></pre>


## Methods




### close<span class="signature">()</span>




To close the navigation drawer control



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;$(function(){ var lsm = $("#navpane").data("ejmNavigationDrawer");lsm.close();});&lt;/script &gt;</code></pre>



### open<span class="signature">()</span>




To open the navigation drawer control



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;$(function(){ var lsm = $("#navpane").data("ejmNavigationDrawer");lsm.open();});&lt;/script &gt;</code></pre>



### toggle<span class="signature">()</span>




To Toggle the navigation drawer control



Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;$(function(){ var lsm = $("#navpane").data("ejmNavigationDrawer");lsm.toggle();});&lt;/script &gt;</code></pre>


## Events




### beforeclose




Event triggers before the control gets closed.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Navigation Drawer<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Navigation Drawer model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code>  &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-beforeclose="onBeforeClose" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;function onBeforeClose(args){ //handle the event}&lt;/script &gt;</code></pre><pre class="prettyprint"><code> //BeforeClose event for Navigation pane&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$("#navpane").ejmNavigationDrawer({  beforeClose: function (args) { //handle the event}});   $("#navpane").ejNavigationDrawer();   &lt;/script&gt;</code></pre>



### open




Event triggers when the control open.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Navigation Drawer<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Navigation Drawer model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-open="onOpen" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;function onOpen(args){ //handle the event}&lt;/script &gt;</code></pre><pre class="prettyprint"><code> //Open event for Navigation pane&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$("#navpane").ejNavigationDrawer({  open: function (args) { //handle the event}});   $("#navpane").ejNavigationDrawer("open");&lt;/script&gt;</code></pre>



### swipe




Event triggers when the Swipe happens.
<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>argument</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">Event parameters from Navigation Drawer<table class="params"><thead><tr><th>Name</th><th>Type</th><th class="last">Description</th></tr></thead><tbody><tr><td class="name"><code>cancel</code></td><td class="type"><span class="param-type">boolean</span></td><td class="description last">if the event should be canceled; otherwise, false.</td></tr><tr><td class="name"><code>model</code></td><td class="type"><span class="param-type">Object</span></td><td class="description last">returns the Navigation Drawer model</td></tr><tr><td class="name"><code>type</code></td><td class="type"><span class="param-type">string</span></td><td class="description last">returns the name of the event</td></tr><tr><td class="name"><code>item</code></td><td class="type"><span class="param-type">object</span></td><td class="description last">returns the item of element</td></tr><tr><td class="name"><code>itemName</code></td><td class="type"><span class="param-type">String</span></td><td class="description last">returns the name of item</td></tr></tbody></table></td></tr></tbody></table>


Example
{:.example}
<pre class="prettyprint"><code> &lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div data-role="ejmnavigationdrawer" id="navpane" data-ej-swipe="onSwipe" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script &gt;function onSwipe(args){ //handle the event}&lt;/script &gt;</code></pre><pre class="prettyprint"><code> //Swipe event for Navigation pane&lt;div id="home" class="navsubpage"&gt;&lt;div align="center" class="content"&gt;&lt;h2 class="title"&gt;Home&lt;/h2&gt;&lt;p&gt;Founded by industry experts in 2001,Syncfusion, Inc. provides the broadest range of enterprise-class software components and tools for the Microsoft .NET platform.&lt;/p&gt;&lt;/div&gt;&lt;/div&gt;&lt;style&gt;.list {  border-bottom: 1px solid;  line-height: 50px;  text-align: center;  width:200px;  }&lt;/style&gt;&lt;div id="navpane" &gt;&lt;div class="list"&gt; Home &lt;/div&gt;&lt;div class="list"&gt; Communities &lt;/div&gt;&lt;/div&gt;&lt;script&gt;$("#navpane").ejmNavigationDrawer({  swipe: function (args) { //handle the event}});   &lt;/script&gt;</code></pre>


