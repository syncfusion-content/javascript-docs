---
layout: post
title: ejTreeView
metaname: 
metacontent: 
---

The treeview can be easily configured with the DOM element, such as div or ul. you can create a treeview with a highly customizable look and feel.










#### $(element).ejTreeView<span class="signature">(options)</span>







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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for TreeView.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Create TreeView
$('#treeView').ejTreeView();    
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.treeview.js


* module:ej.data.js


* module:ej.checkbox.js


* module:ej.waitingpopup.js


* module:ej.draggable.js




### Members








#### allowDragAndDrop<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable drag &amp; drop a node within the same tree.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To Initialize the TreeView with the allowDragAndDrop value specified.
$("#treeView").ejTreeView({
   allowDragAndDrop: true
});
 &lt;/script&gt;</code>
</pre>






#### allowDragAndDropAcrossControl<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable drag &amp; drop a node into ej.TreeView.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the allowDragAndDropAcrossControl value specified.
$("#treeView").ejTreeView({
   allowDragAndDrop: true,
   allowDragAndDropAcrossControl: true
});
 &lt;/script&gt;</code>
</pre>






#### allowDropSibling<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to drop a node to a sibling of particular node.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the dropSibling value specified.
$("#treeView").ejTreeView({
   allowDragAndDrop: true,
   allowDropSibling: true
});
 &lt;/script&gt;</code>
</pre>






#### allowEditing<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable node editing support for Treeview.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the allowEditing value specified.
$("#treeView").ejTreeView({
   allowEditing: true
});
 &lt;/script&gt;</code>
</pre>






#### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable keyboard support for Treeview actions like nodeSelection, nodeEditing, nodeExpand, nodeCollapse, nodeCut, Copy and Paste.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the allowKeyboardNavigation value specified.
$("#treeView").ejTreeView({
   allowKeyboardNavigation: true
});
 &lt;/script&gt;</code>
</pre>






#### autoCheck<span class="type-signature type boolean">boolean</span>








Allow us to specify the parent and child nodes to get auto check.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;                  
//Its auto checks the corresponding child nodes of the checked parent node. vice versa
$("#treeView").ejTreeView({
   autoCheck: true,
   showCheckbox:true
});
 &lt;/script&gt;</code>
</pre>






#### autoCheckParentNode<span class="type-signature type boolean">boolean</span>








Allow us to specify the parent node to be retain in checked or unchecked state instead of going for indeterminate state.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the autoCheckParentNode value specified.
$("#treeView").ejTreeView({ 
   autoCheckParentNode: false,
   showCheckbox:true
});
 &lt;/script&gt;</code>
</pre>






#### checkedNodes<span class="type-signature type array">array</span>








Gets or sets a value that indicates the checkedNodes index collection as an array. The given array index position denotes the nodes, that are checked while rendering treeview.




Default Value:






* []








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;          
// Initialize the TreeView with the checkedNodes value specified.
$("#treeView").ejTreeView({
   showCheckbox: true,
   checkedNodes: [1, 2] 
});
 &lt;/script&gt;</code>
</pre>






#### cssClass<span class="type-signature type string">string</span>








Sets the root CSS class for treeview which allow us to customize the appearance.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
         &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//Initialize the TreeView with the cssClass value specified
$("#treeView").ejTreeView({
   cssClass: 'gradient-lime'
});
 &lt;/script&gt;</code>
</pre>






#### enableAnimation<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to enable or disable the animation effect while expanding or collapsing a node.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;        
//To set enableAnimation API value during initialization  
$("#treeView").ejTreeView({
   enableAnimation: true
});
&lt;/script&gt;</code>
</pre>






#### enabled<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether a treeview can be enabled or disabled. No actions can be performed while this property is set as false




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;  
// Initialize the TreeView with the enabled value specified.
$("#treeView").ejTreeView({ 
   enabled: true
});
 &lt;/script&gt;</code>
</pre>






#### enablePersistence<span class="type-signature type boolean">boolean</span>








Sets a value that indicates whether to persist the treeview model state in page using applicable medium i.e., HTML5 localStorage or cookies




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the persist value specified.
$("#treeView").ejTreeView({ 
   enablePersistence:false
});
 &lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates to align content in the treeview control from right to left by setting the property as true.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the enableRTL value specified.
$("#treeView").ejTreeView({ 
   enableRTL: true
});
 &lt;/script&gt;</code>
</pre>






#### expandedNodes<span class="type-signature type array">array</span>








Gets or sets a array of value that indicates the expandedNodes index collection as an array. The given array index position denotes the nodes, that are expanded while rendering treeview.




Default Value:






* []








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;          
// Initialize the TreeView with the expandedNodes value specified.
$("#treeView").ejTreeView({
   expandedNodes: [0,7]  
});
 &lt;/script&gt;</code>
</pre>






#### expandOn<span class="type-signature type string">string</span>








Gets or sets a value that indicates the treeview node can be expand or collapse by using the specified action.




Default Value:






* "dblclick"








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;  
//Initialize the TreeView with the expandOn value specified
$("#treeView").ejTreeView({ 
   expandOn: 'dblclick'
});
 &lt;/script&gt;</code>
</pre>






#### fields<span class="type-signature type object">object</span>








Gets or sets a fields object that allow us to map the data members with field properties in order to make the data binding easier.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="treeView"&gt;&lt;/div&gt;
&lt;script&gt;
//To set fields API value during initialization  
$("#treeView").ejTreeView({
   fields: { id: "id", parentId: "pid", text: "name", hasChild: "hasChild", dataSource: window.treeView, expanded: "expanded" }
});
 &lt;/script&gt;</code>
</pre>






#### fields.child<span class="type-signature type string">String</span>








It receives the child level or inner level data source such as Essential DataManager object and JSON object.











#### fields.dataSource<span class="type-signature type object">Object</span>








It receives Essential DataManager object and JSON object.











#### fields.expanded<span class="type-signature type boolean">Boolean</span>








Specifies the node to be in expanded state.











#### fields.hasChild<span class="type-signature type boolean">Boolean</span>








Its allow us to indicate whether the node has child or not in load on demand











#### fields.htmlAttribute<span class="type-signature type object">Object</span>








Specifies the html attributes to &ldquo;li&rdquo; item list.











#### fields.id<span class="type-signature type string">String</span>








Specifies the id to TreeView node items list.











#### fields.imageAttribute<span class="type-signature type string">String</span>








Specifies the image attribute to &ldquo;img&rdquo; tag inside items list











#### fields.imageUrl<span class="type-signature type string">String</span>








Specifies the html attributes to &ldquo;li&rdquo; item list.











#### fields.isChecked<span class="type-signature type boolean">Boolean</span>








If its true Checkbox node will be checked when rendered with checkbox.











#### fields.linkAttribute<span class="type-signature type string">String</span>








Specifies the link attribute to &ldquo;a&rdquo; tag in item list.











#### fields.parentId<span class="type-signature type string">String</span>








Specifies the parent id of the node. The nodes are listed as child nodes of the specified parent node by using its parent id.











#### fields.query<span class="type-signature type object">Object</span>








It receives query to retrieve data from the table (query is same as SQL).











#### fields.selected<span class="type-signature type boolean">Boolean</span>








Allow us to specify the node to be in selected state











#### fields.spriteCssClass<span class="type-signature type string">String</span>








Specifies the sprite CSS class to &ldquo;li&rdquo; item list.











#### fields.tableName<span class="type-signature type string">String</span>








It receives the table name to execute query on the corresponding table.











#### fields.text<span class="type-signature type string">String</span>








Specifies the text of TreeView node items list.











#### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>








Defines the height of the TreeView.




Default Value:






* Null








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;                  
//Initialize the TreeView height property with the  value specified
$("#treeView").ejTreeView({
   height: 50
});
 &lt;/script&gt;</code>
</pre>






#### loadOnDemand<span class="type-signature type boolean">boolean</span>








Specifies the child nodes to be loaded on demand




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
// Initialize the TreeView with the loadOnDemand value specified.
$("#treeView").ejTreeView({
   loadOnDemand: true
});
 &lt;/script&gt;</code>
</pre>






#### selectedNode<span class="type-signature type number">number</span>








Gets or Sets a value that indicates the index position of a tree node. The particular index tree node will be selected while rendering the treeview.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;        
// Initialize the TreeView with the selectedNode value specified.
$("#treeView").ejTreeView({
   selectedNode: 2 
});
 &lt;/script&gt;</code>
</pre>






#### showCheckbox<span class="type-signature type boolean">boolean</span>








Gets or sets a value that indicates whether to display or hide checkbox for all treeview nodes.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;        
//To Initialize the TreeView with the showCheckbox value specified.
$("#treeView").ejTreeView({ 
   showCheckbox: true
});
 &lt;/script&gt;</code>
</pre>






#### template<span class="type-signature type string">string</span>








Allow us to use custom template in order to create treeview




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;&lt;a class="uk-style"&gt;UK&lt;/a&gt;
           &lt;ul&gt;
   &lt;li&gt;
               &lt;div class="cont-list"&gt;
                   &lt;img src="styles/images/treeview/template-image-1.png"/&gt;
                       &lt;div class="cont-del"&gt;&lt;/div&gt;
                       &lt;div class="cont-details"&gt;&lt;/div&gt;
                       &lt;b&gt;Steven John&lt;/b&gt;&lt;br/&gt;
                       &lt;span&gt;London&lt;/span&gt;&lt;br/&gt;
                       &lt;span&gt;555-5665-2323&lt;/span&gt;
                   &lt;/div&gt;
 &lt;div class="treeFooter"&gt;&lt;/div&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;&lt;a class=""usa-style""&gt;USA&lt;/a&gt;
           &lt;ul&gt;
   &lt;li&gt;
               &lt;div class="cont-list"&gt;
                   &lt;img src="styles/images/treeview/template-image-2.png"/&gt;
                       &lt;div class="cont-del"&gt;&lt;/div&gt;
                       &lt;div class="cont-details"&gt;&lt;/div&gt;
                       &lt;b&gt;Andrew&lt;/b&gt;&lt;br/&gt;
                       &lt;span&gt;Capital way&lt;/span&gt;&lt;br/&gt;
                       &lt;span&gt;934-8374-2455&lt;/span&gt;
                   &lt;/div&gt;
 &lt;div class="treeFooter"&gt;&lt;/div&gt;
               &lt;/li&gt;
               &lt;li&gt;
               &lt;div class="cont-list"&gt;
                   &lt;img src="styles/images/treeview/template-image-3.png"/&gt;
                       &lt;div class="cont-del"&gt;&lt;/div&gt;
                       &lt;div class="cont-details"&gt;&lt;/div&gt;
                       &lt;b&gt;Angelica&lt;/b&gt;&lt;br/&gt;
                       &lt;span&gt;Dayton&lt;/span&gt;&lt;br/&gt;
                       &lt;span&gt;988-4243-0806&lt;/span&gt;
                   &lt;/div&gt;
 &lt;div class="treeFooter"&gt;&lt;/div&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//Initialize the TreeView with the template value specified
$("#treeView").ejTreeView({ 
   template: "templatelocaldata"
});
 &lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>








Defines the width of the TreeView.




Default Value:






* Null








##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//Initialize the TreeView height property with the  value specified
$("#treeView").ejTreeView({
   width: 300
});
 &lt;/script&gt;</code>
</pre>




### Methods








#### addNode<span class="signature">(newNodeText, target)</span>








To add Node in the TreeView.

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
<td class="name"><code>newNodeText</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">new Treeview Node Text or JSON Object</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="Music"&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.addNode("NodeNew", "Folk"); // addNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
var obj = { id: "temp", text: "New node" };
treeObj.addNode(obj, $("#Music"));
&lt;/script&gt;</code>
</pre>






#### checkAll<span class="signature">()</span>








To check all the TreeView nodes.





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkAll(); // checkAll the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
$("#treeView").ejTreeView("checkAll");        
&lt;/script&gt;</code>
</pre>






#### checkNode<span class="signature">(element)</span>








To Check particular node checkbox in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkNode($("#book")); // checkNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
$("#treeView").ejTreeView("checkNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### collapseAll<span class="signature">()</span>








To collapse all the TreeView nodes.





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.collapseAll(); // collapseAll the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("collapseAll");        
&lt;/script&gt;</code>
</pre>






#### collapseNode<span class="signature">(element)</span>








To collapseNode particular node in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li id="art"&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.expandAll();
treeObj.collapseNode($("#art")); // collapseNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li id="art"&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("expandAll");
$("#treeView").ejTreeView("collapseNode",$("#art"));        
&lt;/script&gt;</code>
</pre>






#### disableNode<span class="signature">(node)</span>








To disable the node in the TreeView.

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">object of treeview node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.disableNode($("#book")); // disableNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("disableNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### enableNode<span class="signature">(node)</span>








To enable the node in the TreeView.

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">object of treeview node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
         &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="music"&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.disableNode($("#music"));
treeObj.disableNode($("#book"));
treeObj.enableNode($("#book")); // enableNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="music"&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView  
$("#treeView").ejTreeView("disableNode",$("#music")); 
$("#treeView").ejTreeView("disableNode",$("#book")); 
$("#treeView").ejTreeView("enableNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### expandAll<span class="signature">()</span>








To expand all the TreeView nodes.





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.expandAll(); // expandAll the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("expandAll");        
&lt;/script&gt;</code>
</pre>






#### expandNode<span class="signature">(element)</span>








To expandNode particular node in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.collapseAll();
treeObj.expandNode($("#book")); // expandNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("collapseAll");
$("#treeView").ejTreeView("expandNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### getCheckedNodes<span class="signature">()</span>








To getCheckedNodes in the TreeView.





##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkNode($("#book"));
treeObj.getCheckedNodes(); // getAllCheckedNodes in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
$("#treeView").ejTreeView("checkNode",$("#book"));
$("#treeView").ejTreeView("getCheckedNodes");        
&lt;/script&gt;</code>
</pre>






#### getSelectedNode<span class="signature">()</span>








To get the selected nodes in the TreeView.





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.getSelectedNode(); // getSelectedNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("getSelectedNode");        
&lt;/script&gt;</code>
</pre>






#### getText<span class="signature">(node)</span>








To get the text of the nodes in the TreeView.

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">object of treeview node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li id="book"&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.getText($("#book")); // getText in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("getText",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### hasChildNode<span class="signature">(element)</span>








To retrive the status of the collection of childs for the given TreeView node.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of element</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
&lt;li&gt;Artwork
    &lt;ul&gt;
        &lt;li&gt;Abstract
            &lt;ul&gt;
                &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
               &lt;li&gt;Creative Acrylic&lt;/li&gt;
                &lt;li&gt;Modern Painting&lt;/li&gt;
             &lt;li&gt;Canvas Art&lt;/li&gt;
             &lt;li&gt;Black white&lt;/li&gt;
          &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;
&lt;/li&gt;
&lt;li id="book"&gt;Books
   &lt;ul&gt;
        &lt;li&gt;Entertaining&lt;/li&gt;
       &lt;li&gt;Design&lt;/li&gt;
    &lt;/ul&gt;
&lt;/li&gt;
&lt;li&gt;Music
    &lt;ul&gt;
        &lt;li&gt;Mass&lt;/li&gt;
        &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
&lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.hasChildNode($("#book")); // hasChildNode the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("hasChildNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### hide<span class="signature">()</span>








To show nodes in TreeView.





##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                 &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.hide(); // hide the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("hide");        
&lt;/script&gt;</code>
</pre>






#### hideNode<span class="signature">(element)</span>








To hideNode particular node in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                 &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li id="book"&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.hideNode($("#book")); // hideNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("hideNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### isExpanded<span class="signature">(element)</span>








To retrive the expand status of the given TreeView node.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li id="book"&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.isExpanded($("#book")); // isExpanded the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("isExpanded",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### isNodeChecked<span class="signature">(element)</span>








To retrive the checked status of the given TreeView node.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                 &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li id="book"&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.isNodeChecked($("#book")); // isNodeChecked the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
$("#treeView").ejTreeView("isNodeChecked",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### refresh<span class="signature">()</span>








To refresh the TreeView





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
          &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
          &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.refresh(); // refresh the TreeView
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("refresh");        
&lt;/script&gt;</code>
</pre>






#### removeNode<span class="signature">(element)</span>








To remove Node in the TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.removeNode($("#book")); // removeNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("removeNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### selectNode<span class="signature">(node)</span>








To select the node in the TreeView.

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">object of treeview node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.selectNode($("#book")); // selectNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("selectNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### show<span class="signature">()</span>








To show nodes in TreeView.





##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                 &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.show(); // show the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("show");        
&lt;/script&gt;</code>
</pre>






#### showNode<span class="signature">(element)</span>








To showNode particular node in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
     &lt;ul&gt;
         &lt;li&gt;Abstract
             &lt;ul&gt;
                 &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                 &lt;li&gt;Creative Acrylic&lt;/li&gt;
                 &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                 &lt;li&gt;Black white&lt;/li&gt;
             &lt;/ul&gt;
         &lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li id="book"&gt;Books
     &lt;ul&gt;
         &lt;li&gt;Entertaining&lt;/li&gt;
         &lt;li&gt;Design&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
 &lt;li&gt;Music
     &lt;ul&gt;
         &lt;li&gt;Mass&lt;/li&gt;
         &lt;li&gt;Folk&lt;/li&gt;
     &lt;/ul&gt;
 &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.showNode($("#book")); // showNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("showNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### unCheckAll<span class="signature">()</span>








To uncheck all the TreeView nodes.





##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
   &lt;li&gt;Artwork
       &lt;ul&gt;
           &lt;li&gt;Abstract
               &lt;ul&gt;
                   &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                   &lt;li&gt;Creative Acrylic&lt;/li&gt;
                   &lt;li&gt;Modern Painting&lt;/li&gt;
                   &lt;li&gt;Canvas Art&lt;/li&gt;
                   &lt;li&gt;Black white&lt;/li&gt;
               &lt;/ul&gt;
           &lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Books
       &lt;ul&gt;
           &lt;li&gt;Entertaining&lt;/li&gt;
           &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
   &lt;/li&gt;
   &lt;li&gt;Music
       &lt;ul&gt;
           &lt;li&gt;Mass&lt;/li&gt;
           &lt;li&gt;Folk&lt;/li&gt;
       &lt;/ul&gt;
   &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.unCheckAll(); // uncheckAll the TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
$("#treeView").ejTreeView("unCheckAll");        
&lt;/script&gt;</code>
</pre>






#### uncheckNode<span class="signature">(element)</span>








To Uncheck particular node checkbox in TreeView.

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
<td class="name"><code>element</code></td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">object of Tree view node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
  &lt;ul id="treeView"&gt;
 &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                 &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
     &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView({showCheckbox:true});
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkAll();
treeObj.uncheckNode($("#book")); // uncheckNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("checkAll");
$("#treeView").ejTreeView("uncheckNode",$("#book"));        
&lt;/script&gt;</code>
</pre>






#### unselectNode<span class="signature">(node)</span>








To unselect the node in the TreeView.

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
<td class="name"><code>node</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">object of treeview node.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
       &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
var treeObj = $("#treeView").data("ejTreeView");
treeObj.unselectNode($("#book")); // unselectNode in  TreeView nodes
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
 &lt;ul id="treeView"&gt;
  &lt;li&gt;Artwork
      &lt;ul&gt;
          &lt;li&gt;Abstract
              &lt;ul&gt;
                  &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                  &lt;li&gt;Creative Acrylic&lt;/li&gt;
                  &lt;li&gt;Modern Painting&lt;/li&gt;
                  &lt;li&gt;Canvas Art&lt;/li&gt;
                  &lt;li&gt;Black white&lt;/li&gt;
              &lt;/ul&gt;
          &lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li id="book"&gt;Books
      &lt;ul&gt;
          &lt;li&gt;Entertaining&lt;/li&gt;
          &lt;li&gt;Design&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
  &lt;li&gt;Music
      &lt;ul&gt;
          &lt;li&gt;Mass&lt;/li&gt;
          &lt;li&gt;Folk&lt;/li&gt;
      &lt;/ul&gt;
  &lt;/li&gt;
&lt;/ul&gt; 
 
&lt;script&gt;
$("#treeView").ejTreeView();
// Create TreeView
$("#treeView").ejTreeView("unselectNode",$("#book"));        
&lt;/script&gt;</code>
</pre>




### Events








#### beforeCollapse








Fires when beforeCollapse successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create beforeCollapse event for ejTreeView
$("#treeView").ejTreeView({ 
        beforeCollapse: function(args) {}
}); 
 &lt;/script&gt;     </code>
</pre>






#### beforeEdit








Fires when beforeEdit successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create beforeEdit event for ejTreeView
$("#treeView").ejTreeView({ 
        beforeEdit: function(args) {}
}); 
 &lt;/script&gt;     </code>
</pre>






#### beforeExpand








Fires when beforeExpand successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.isChildLoaded</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the child node is ready to expanded state; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create beforeExpand event for ejTreeView
$("#treeView").ejTreeView({ 
        beforeExpand: function(args) {}
});     
 &lt;/script&gt; </code>
</pre>






#### created








Fires when created successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create node for ejTreeView
$("#treeView").ejTreeView({ 
      create: function(args) {}
});
 &lt;/script&gt;      </code>
</pre>






#### destroyed








Fires when destroyed successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create destroy event for ejTreeView
$("#treeView").ejTreeView({ 
      destroy: function(args) {}
}); 
 &lt;/script&gt;     </code>
</pre>






#### inlineEditValidation








Fires when inlineEditValidation successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.newText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the new entered text for the node</td>
</tr>
<tr>
<td class="name"><code>argument.nodeId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current node element id</td>
</tr>
<tr>
<td class="name"><code>argument.oldText</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the old node text</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create inlineEditValidation event for ejTreeView
$("#treeView").ejTreeView({ 
        inlineEditValidation: function(args) {}
});  
 &lt;/script&gt;    </code>
</pre>






#### keyPress








Fires when keyPress successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.path</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns node path from root element</td>
</tr>
<tr>
<td class="name"><code>argument.keyCode</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<td class="name"><code>argument.isExpanded</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns when the current node is in expanded state; otherwise, false.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create keyPress event for ejTreeView
$("#treeView").ejTreeView({ 
        keyPress: function(args) {}
});     
 &lt;/script&gt; </code>
</pre>






#### nodeCheck








Fires when nodeCheck successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.parentId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns true when the node checkbox is checked; otherwise, false.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt; 
//To create select event for ejTreeView
$("#treeView").ejTreeView({ 
                showCheckbox:true,
        nodeCheck: function(args) {}
}); 
 &lt;/script&gt;     </code>
</pre>






#### nodeClick








Fires when nodeClick successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create click event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeClick: function(args) {}
});    
 &lt;/script&gt;  </code>
</pre>






#### nodeCollapse








Fires when nodeCollapse successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.parentId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create nodeCollapse event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeCollapse: function(args) {}
}); 
 &lt;/script&gt;     </code>
</pre>






#### nodeDrag








Fires when nodeDrag successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create nodeDrag event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeDrag: function(args) {}
});      
 &lt;/script&gt;</code>
</pre>






#### nodeDragStart








Fires when nodeDragStart successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//nodeDragStart event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeDragStart: function(args) {}
});  
 &lt;/script&gt;    </code>
</pre>






#### nodeDragStop








Fires when nodeDragStop successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.position</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the element new dragged place from its original place.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create nodeDragStop event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeDragStop: function(args) {}
});  
 &lt;/script&gt;    </code>
</pre>






#### nodeDropped








Fires when nodeDropped successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.dropedElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create nodeDropped event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeDropped: function(args) {}
});  
 &lt;/script&gt;    </code>
</pre>






#### nodeExpand








Fires when nodeExpand successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.parentId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.isChildLoaded</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the child node is ready to expanded state; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create expand event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeExpand: function(args) {}
});      
 &lt;/script&gt;</code>
</pre>






#### nodeSelect








Fires when nodeSelect successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.parentId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create select event for ejTreeView
$("#treeView").ejTreeView({ 
        nodeSelect: function(args) {}
});   
 &lt;/script&gt;   </code>
</pre>






#### nodeUncheck








Fires when nodeUncheck successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>argument.event</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name"><code>argument.id</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.parentId</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.value</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name"><code>argument.currentElement</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name"><code>argument.isChecked</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns true when the node checkbox is checked; otherwise, false.</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;ul id="treeView"&gt;
       &lt;li&gt;Artwork
           &lt;ul&gt;
               &lt;li&gt;Abstract
                   &lt;ul&gt;
                       &lt;li&gt;2 Acrylic Mediums&lt;/li&gt;
                       &lt;li&gt;Creative Acrylic&lt;/li&gt;
                       &lt;li&gt;Modern Painting&lt;/li&gt;
                       &lt;li&gt;Canvas Art&lt;/li&gt;
                       &lt;li&gt;Black white&lt;/li&gt;
                   &lt;/ul&gt;
               &lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Books
           &lt;ul&gt;
               &lt;li&gt;Entertaining&lt;/li&gt;
               &lt;li&gt;Design&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
       &lt;li&gt;Music
           &lt;ul&gt;
               &lt;li&gt;Mass&lt;/li&gt;
               &lt;li&gt;Folk&lt;/li&gt;
           &lt;/ul&gt;
       &lt;/li&gt;
   &lt;/ul&gt;

 
&lt;script&gt;
//To create nodeUncheck event for ejTreeView
$("#treeView").ejTreeView({ 
                showCheckbox:true,
        nodeUncheck: function(args) {}
});   
 &lt;/script&gt;   </code>
</pre>



