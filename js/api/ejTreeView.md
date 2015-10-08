---
layout: post
title: ejTreeView
documentation: API
platform: js
metaname: 
metacontent: 
---

The TreeView can be easily configured with the DOM element, such as div or ul. You can create a TreeView with a highly customizable look and feel.










$(element).ejTreeView<span class="signature">(options)</span>







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
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for TreeView.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<ul id="treeView">
       <li>Artwork
           <ul>
               <li>Abstract
                   <ul>
                       <li>2 Acrylic Mediums</li>
                       <li>Creative Acrylic</li>
                       <li>Modern Painting</li>
                       <li>Canvas Art</li>
                       <li>Black white</li>
                   </ul>
               </li>
           </ul>
       </li>
       <li>Books
           <ul>
               <li>Entertaining</li>
               <li>Design</li>
           </ul>
       </li>
       <li>Music
           <ul>
               <li>Mass</li>
               <li>Folk</li>
           </ul>
       </li>
   </ul>

 
<script>
// Create TreeView
$('#treeView').ejTreeView();    
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.treeview.js


* module:ej.data.js


* module:ej.checkbox.js


* module:ej.waitingpopup.js


* module:ej.draggable.js




## Members








### allowDragAndDrop<span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddrop}








Gets or sets a value that indicates whether to enable drag and drop a node within the same tree.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
//To Initialize the TreeView with the allowDragAndDrop value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowDragAndDrop: true
});
 </script>{% endhighlight %}







### allowDragAndDropAcrossControl<span class="type-signature type boolean">boolean</span>
{:#members:allowdraganddropacrosscontrol}








Gets or sets a value that indicates to enable drag and drop a node into ej.TreeView.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the allowDragAndDropAcrossControl value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowDragAndDrop: true,
    allowDragAndDropAcrossControl: true
});
 </script>{% endhighlight %}







### allowDropSibling<span class="type-signature type boolean">boolean</span>
{:#members:allowdropsibling}








Gets or sets a value that indicates to drop a node to a sibling of particular node.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the allowDropSibling value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowDragAndDrop: true,
    allowDropSibling: true
});
 </script>{% endhighlight %}







### allowDropChild<span class="type-signature type boolean">boolean</span>
{:#members:allowdropchild}








Gets or sets a value that indicates to drop a node to a child of particular node.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the allowDropChild value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowDragAndDrop: true,
    allowDropChild: true
});
 </script>{% endhighlight %}







### allowEditing<span class="type-signature type boolean">boolean</span>
{:#members:allowediting}








Gets or sets a value that indicates whether to enable node editing support for TreeView.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the allowEditing value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowEditing: true
});
 </script>{% endhighlight %}







### allowKeyboardNavigation<span class="type-signature type boolean">boolean</span>
{:#members:allowkeyboardnavigation}








Gets or sets a value that indicates whether to enable the keyboard support for TreeView actions like nodeSelection, nodeEditing, nodeExpand, nodeCollapse, nodeCut and Paste.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the allowKeyboardNavigation value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    allowKeyboardNavigation: true
});
 </script>{% endhighlight %}







### autoCheck<span class="type-signature type boolean">boolean</span>
{:#members:autocheck}








Allows to specify the parent and child nodes to get auto check while you check or uncheck a node.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>                  
// Initialize the TreeView with the autoCheck value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    autoCheck: true,
    showCheckbox:true
});
 </script>{% endhighlight %}







### autoCheckParentNode<span class="type-signature type boolean">boolean</span>
{:#members:autocheckparentnode}








Allows to specify the parent node to be retained in checked or unchecked state instead of indeterminate state.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the autoCheckParentNode value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }, 
    autoCheckParentNode: false,
    showCheckbox:true
});
 </script>{% endhighlight %}







### checkedNodes<span class="type-signature type array">array</span>
{:#members:checkednodes}








Gets or sets a value that indicates the checkedNodes index collection as an array. The given array index position denotes the nodes, that are checked while rendering the TreeView.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>          
// Initialize the TreeView with the checkedNodes value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    showCheckbox: true,
    checkedNodes: [1, 2] 
});
 </script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Sets the root CSS class for TreeView that allows to customize the appearance.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the cssClass value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    cssClass: 'gradient-lime'
});
 </script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Gets or sets a value that indicates to enable or disable the animation effect while expanding or collapsing a node.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>        
// Initialize the TreeView with the enableAnimation value specified.  
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    enableAnimation: true
});
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








Gets or sets a value that indicates whether a TreeView can be enabled or disabled. No actions can be performed while this property is set false.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>  
// Initialize the TreeView with the enabled value specified.
$("#treeView").ejTreeView({ 
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    enabled: true
});
 </script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}








Sets a value that indicates whether to persist the TreeView model state in page by using applicable medium like, HTML5 localStorage or cookies




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the enablePersistence value specified.
$("#treeView").ejTreeView({ 
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    enablePersistence:false
});
 </script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Gets or sets a value that indicates to align content in the TreeView control from right to left by setting the property true.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the enableRTL value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }, 
    enableRTL: true
});
 </script>{% endhighlight %}







### expandedNodes<span class="type-signature type array">array</span>
{:#members:expandednodes}








Gets or sets a array of value that indicates the expandedNodes index collection as an array. The given array index position denotes the nodes, that are expanded while rendering TreeView.




Default Value:
{:.param}






* []








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>          
// Initialize the TreeView with the expandedNodes value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    expandedNodes: [0,7]  
});
 </script>{% endhighlight %}







### expandOn<span class="type-signature type string">string</span>
{:#members:expandon}








Gets or sets a value that indicates the TreeView node can be expanded or collapsed by using the specified action.




Default Value:
{:.param}






* "dblclick"








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>  
//Initialize the TreeView with the expandOn value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }, 
    expandOn: 'dblclick'
});
 </script>{% endhighlight %}







### fields<span class="type-signature type object">object</span>
{:#members:fields}








Gets or sets a fields object that allows to map the data members with field properties in order to make the data binding easier.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the fields value specified. 
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});
 </script>{% endhighlight %}







### fields.child<span class="type-signature type string">object</span>
{:#members:fields-child}








It receives the child level or inner level data source such as Essential DataManager object and JSON object.











### fields.dataSource<span class="type-signature type object">object</span>
{:#members:fields-datasource}








It receives Essential DataManager object and JSON object.











### fields.expanded<span class="type-signature type boolean">Boolean</span>
{:#members:fields-expanded}








Specifies the node to be in expanded state.











### fields.hasChild<span class="type-signature type boolean">Boolean</span>
{:#members:fields-haschild}








Its allows to indicate whether the node has child or not in load on demand.











### fields.htmlAttribute<span class="type-signature type object">object</span>
{:#members:fields-htmlattribute}








Specifies the html attributes to &ldquo;li&rdquo; item list.











### fields.id<span class="type-signature type string">string</span>
{:#members:fields-id}








Specifies the id to TreeView node items list.











### fields.imageAttribute<span class="type-signature type string">object</span>
{:#members:fields-imageattribute}








Specifies the image attribute to &ldquo;img&rdquo; tag inside items list.











### fields.imageUrl<span class="type-signature type string">string</span>
{:#members:fields-imageurl}








Specifies the html attributes to &ldquo;li&rdquo; item list.











### fields.isChecked<span class="type-signature type boolean">Boolean</span>
{:#members:fields-ischecked}








When its true, the checkbox node is checked when rendered with checkbox.











### fields.linkAttribute<span class="type-signature type string">object</span>
{:#members:fields-linkattribute}








Specifies the link attribute to &ldquo;a&rdquo; tag in item list.











### fields.parentId<span class="type-signature type string">string</span>
{:#members:fields-parentid}








Specifies the parent id of the node. The nodes are listed as child nodes of the specified parent node by using its parent id.











### fields.query<span class="type-signature type object">object</span>
{:#members:fields-query}








It receives the query to retrieve data from the table (query is same as SQL).











### fields.selected<span class="type-signature type boolean">Boolean</span>
{:#members:fields-selected}








Allows to specify the node to be in selected state.











### fields.spriteCssClass<span class="type-signature type string">string</span>
{:#members:fields-spritecssclass}








Specifies the sprite CSS class to &ldquo;li&rdquo; item list.











### fields.tableName<span class="type-signature type string">string</span>
{:#members:fields-tablename}








It receives the table name to execute query on the corresponding table.











### fields.text<span class="type-signature type string">string</span>
{:#members:fields-text}








Specifies the text of TreeView node items list.











### height<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:height}








Defines the height of the TreeView.




Default Value:
{:.param}






* Null








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>                  
// Initialize the TreeView with the height value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    height: 300
});
 </script>{% endhighlight %}







### loadOnDemand<span class="type-signature type boolean">boolean</span>
{:#members:loadondemand}








Specifies the child nodes to be loaded on demand.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the loadOnDemand value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    loadOnDemand: true
});
 </script>{% endhighlight %}







### enableMultipleExpand<span class="type-signature type boolean">boolean</span>
{:#members:enablemultipleexpand}








Allows to prevent multiple nodes to be in expanded state. When it is set false, previously expanded nodes are collapsed automatically, while you expand a node.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView with the enableMultipleExpand value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    enableMultipleExpand: true
});
 </script>{% endhighlight %}







### selectedNode<span class="type-signature type number">number</span>
{:#members:selectednode}








Gets or sets a value that indicates the index position of a tree node. The particular index tree node is selected while rendering the TreeView.




Default Value:
{:.param}






* -1








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>        
//Initialize the TreeView with the selectedNode value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    selectedNode: 2 
});
 </script>{% endhighlight %}







### showCheckbox<span class="type-signature type boolean">boolean</span>
{:#members:showcheckbox}








Gets or sets a value that indicates to display or hide checkbox for all TreeView nodes.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>        
// Initialize the TreeView with the showCheckbox value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" }, 
    showCheckbox: true
});
 </script>{% endhighlight %}







### template<span class="type-signature type string">string</span>
{:#members:template}








Allows to use custom template in order to create TreeView.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<ul id="treeView">
       <li><a class="uk-style">UK</a>
           <ul>
   <li>
               <div class="cont-list">
                   <img src="styles/images/treeview/template-image-1.png"/>
                       <div class="cont-del"></div>
                       <div class="cont-details"></div>
                       <b>Steven John</b><br/>
                       <span>London</span><br/>
                       <span>555-5665-2323</span>
                   </div>
 <div class="treeFooter"></div>
               </li>
           </ul>
       </li>
       <li><a class=""usa-style"">USA</a>
           <ul>
   <li>
               <div class="cont-list">
                   <img src="styles/images/treeview/template-image-2.png"/>
                       <div class="cont-del"></div>
                       <div class="cont-details"></div>
                       <b>Andrew</b><br/>
                       <span>Capital way</span><br/>
                       <span>934-8374-2455</span>
                   </div>
 <div class="treeFooter"></div>
               </li>
               <li>
               <div class="cont-list">
                   <img src="styles/images/treeview/template-image-3.png"/>
                       <div class="cont-del"></div>
                       <div class="cont-details"></div>
                       <b>Angelica</b><br/>
                       <span>Dayton</span><br/>
                       <span>988-4243-0806</span>
                   </div>
 <div class="treeFooter"></div>
               </li>
           </ul>
       </li>
   </ul>

 
<script>
// Initialize the TreeView with the template value specified.
$("#treeView").ejTreeView({ 
   template: "#templatelocaldata"
});
 </script>{% endhighlight %}







### width<span class="type-signature type string">string</span> <span class="type-signature type number">number</span>
{:#members:width}








Defines the width of the TreeView.




Default Value:
{:.param}






* Null








Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize the TreeView height property with the  value specified.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    width: 300
});
 </script>{% endhighlight %}





## Methods








### addNode<span class="signature">(newNodeText, target)</span>
{:#methods:addnode}








To add a Node or collection of nodes in TreeView. When the target tree node is specified, the given nodes are added as child of target tree node, otherwise nodes are added in TreeView.  

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
newNodeText{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">New node text or JSON object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.addNode("NodeNew", "book"); // The first argument is new node text and it is appended as child of node, the node that is having ID book.
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
var obj = { id: "temp", name: "New node" }; // In this object, we can also use selected, isChecked, imageUrl, spriteCssClass properties.
treeObj.addNode(obj, $("#book"));
</script>{% endhighlight %}







### checkAll<span class="signature">()</span>
{:#methods:checkall}








To check all the nodes in TreeView.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkAll(); // All the TreeView nodes are checked.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("checkAll");        
</script>{% endhighlight %}







### checkNode<span class="signature">(element)</span>
{:#methods:checknode}








To check a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.checkNode($("#book")); // // Given TreeView node is checked.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("checkNode", $("#book"));        
</script>{% endhighlight %}







### collapseAll<span class="signature">()</span>
{:#methods:collapseall}








To collapse all the TreeView nodes.





Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.collapseAll(); // All the TreeView nodes are collapsed.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("collapseAll");        
</script>{% endhighlight %}







### collapseNode<span class="signature">(element)</span>
{:#methods:collapsenode}








To collapse a particular node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.collapseNode($("#book")); // Given TreeView node is collapsed.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("collapseNode", $("#book"));        
</script>{% endhighlight %}







### disableNode<span class="signature">(element)</span>
{:#methods:disablenode}








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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.disableNode($("#book")); // Given TreeView node is disabled and child nodes are also disabled.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("disableNode", $("#book"));        
</script>{% endhighlight %}







### enableNode<span class="signature">(element)</span>
{:#methods:enablenode}








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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.enableNode($("#book")); // Given TreeView node will be enabled and child nodes also enabled.
</script>{% endhighlight %}


{% highlight html %}
 
<script>
$("#treeView").ejTreeView("enableNode", $("#book"));        
</script>{% endhighlight %}








### ensureVisible<span class="signature">(element)</span>
{:#methods:ensurevisible}








To ensure that the TreeView node is visible in the TreeView. This method is useful if we need select a TreeView node dynamically.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
// Given TreeView node is present in TreeView, then the tree is expanded and scrolled automatically to ensure that the current tree node is visible in the TreeView.
treeObj.ensureVisible($("#book")); 
</script>{% endhighlight %}


{% highlight html %}
 
<script>
$("#treeView").ejTreeView("ensureVisible", $("#book"));        
</script>{% endhighlight %}








### expandAll<span class="signature">()</span>
{:#methods:expandall}








To expand all the TreeView nodes.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.expandAll(); // All the TreeView nodes will be expanded.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("expandAll");        
</script>{% endhighlight %}







### expandNode<span class="signature">(element)</span>
{:#methods:expandnode}








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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.expandNode($("#book")); // Given TreeView node will be expanded.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("expandNode", $("#book"));        
</script>{% endhighlight %}







### getCheckedNodes<span class="signature">()</span>
{:#methods:getcheckednodes}








To get currently checked nodes in TreeView.




#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getCheckedNodes(); // All checked TreeView nodes will be returned.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getCheckedNodes");        
</script>{% endhighlight %}







### getCheckedNodesIndex<span class="signature">()</span>
{:#methods:getcheckednodesindex}








To get currently checked nodes indexes in TreeView.




#### Returns:
{:#methods:returns:}

array






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getCheckedNodesIndex(); // All checked TreeView nodes indexes will be returned as array.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getCheckedNodesIndex");        
</script>{% endhighlight %}








### getCount<span class="signature">()</span>
{:#methods:getcount}








To get number of nodes in TreeView.




#### Returns:
{:#methods:returns:}

number






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getCount(); // It will return the TreeView nodes count.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getCount");        
</script>{% endhighlight %}









### getExpandedNodes<span class="signature">()</span>
{:#methods:getexpandenodes}








To get currently expanded nodes in TreeView.





#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getExpandedNodes(); // All expanded TreeView nodes will be returned.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getExpandedNodes");        
</script>{% endhighlight %}







### getExpandedNodesIndex<span class="signature">()</span>
{:#methods:getexpandednodesindex}








To get currently expanded nodes indexes in TreeView.




#### Returns:
{:#methods:returns:}

array






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getExpandedNodesIndex(); // All expanded TreeView nodes indexes will be returned as array.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getExpandedNodesIndex");        
</script>{% endhighlight %}









### getNodeByIndex<span class="signature">(index)</span>
{:#methods:getnodebyindex}








To get TreeView node by using index position in TreeView.

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
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">Index position of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getNodeByIndex(3); // It will return the TreeView node of specified index.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getNodeByIndex", 3);        
</script>{% endhighlight %}








### getNode<span class="signature">(element)</span>
{:#methods:getnode}








To get TreeView node data such as nodeId, nodeText, parentId, selected, checked, expanded, level, childs and index.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getNode($("#book")); // Given TreeView node details will be returned as JSON object.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getNode", $("#book"));        
</script>{% endhighlight %}








### getNodeIndex<span class="signature">(element)</span>
{:#methods:getnodeindex}








To get current index position of TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

number






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getNodeIndex($("#book")); // Given TreeView node index postion will be returned.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getNodeIndex", $("#book"));        
</script>{% endhighlight %}









### getParent<span class="signature">(element)</span>
{:#methods:getparent}








To get immediate parent TreeView node of particular TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>





#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getParent($("#book")); // It will return the immediate parent TreeView node of given TreeView node.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getParent", $("#book"));        
</script>{% endhighlight %}










### getSelectedNode<span class="signature">()</span>
{:#methods:getselectednode}








To get the currently selected node in TreeView.




#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getSelectedNode(); // Currently selected TreeView node will be returned.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("getSelectedNode");        
</script>{% endhighlight %}







### getSelectedNodeIndex<span class="signature">()</span>
{:#methods:getselectednodeindex}








To get the index position of currently selected node in TreeView.






#### Returns:
{:#methods:returns:}

number







Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getSelectedNodeIndex(); // Currently selected TreeView node index poistion will be returned.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("getSelectedNodeIndex");        
</script>{% endhighlight %}








### getText<span class="signature">(element)</span>
{:#methods:gettext}








To get the text of a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>





#### Returns:
{:#methods:returns:}

string







Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getText($("#book")); // Given TreeView node text will be returned.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getText", $("#book"));        
</script>{% endhighlight %}







### getTreeData<span class="signature">()</span>
{:#methods:gettreedata}








To get the updated datasource of TreeView after performing some operation like drag and drop, node editing, adding and removing node.






#### Returns:
{:#methods:returns:}

array






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getTreeData(); // It will return the updated datasource as array of JSON object, after performing some operation.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("getTreeData");        
</script>{% endhighlight %}









### getVisibleNodes<span class="signature">()</span>
{:#methods:getvisiblenodes}








To get currently visible nodes in TreeView.





#### Returns:
{:#methods:returns:}

object






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.getVisibleNodes(); // It will return the currently visible TreeView nodes.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("getVisibleNodes");        
</script>{% endhighlight %}










### hasChildNode<span class="signature">(element)</span>
{:#methods:haschildnode}








To check a node having child or not.


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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean







Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.hasChildNode($("#book")); // It will return true, if the given TreeView node having child node's, else false.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("hasChildNode", $("#book"));        
</script>{% endhighlight %}







### hide<span class="signature">()</span>
{:#methods:hide}








To show nodes in TreeView.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.hide(); // It will hide all the nodes in TreeView.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("hide");        
</script>{% endhighlight %}







### hideNode<span class="signature">(element)</span>
{:#methods:hidenode}








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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.hideNode($("#book")); // It will hide the given TreeView node.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("hideNode", $("#book"));        
</script>{% endhighlight %}








### insertAfter<span class="signature">(newNodeText, target)</span>
{:#methods:insertafter}








To add a Node or collection of nodes after the particular TreeView node.  

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
newNodeText{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">New node text or JSON object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.insertAfter("NodeNew", "book"); // First argument is new node text and it will be appended after the specified TreeView node, which node is having ID book.
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
var obj = { id: "temp", name: "New node" }; // In this object, we can also use selected, isChecked, imageUrl, spriteCssClass properties.
treeObj.insertAfter(obj, $("#book"));
</script>{% endhighlight %}








### insertBefore<span class="signature">(newNodeText, target)</span>
{:#methods:insertbefore}








To add a Node or collection of nodes before the particular TreeView node.  

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
newNodeText{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">New node text or JSON object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.insertBefore("NodeNew", "book"); // First argument is new node text and it will be appended before the specified TreeView node, which node is having ID book.
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
var obj = { id: "temp", name: "New node" }; // In this object, we can also use selected, isChecked, imageUrl, spriteCssClass properties.
treeObj.insertBefore(obj, $("#book"));
</script>{% endhighlight %}









### isNodeChecked<span class="signature">(element)</span>
{:#methods:isnodechecked}








To check the given TreeView node is checked or unchecked.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isNodeChecked($("#book")); // It will return true, if the given TreeView node is checked, else false. 
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isNodeChecked", $("#book"));        
</script>{% endhighlight %}








### isChildLoaded<span class="signature">(element)</span>
{:#methods:ischildloaded}








To check whether the child nodes are loaded of the given TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean






Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isChildLoaded($("#book")); // It will return true, if the given TreeView node is child nodes are loaded, else false. 
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isChildLoaded", $("#book"));        
</script>{% endhighlight %}









### isDisabled<span class="signature">(element)</span>
{:#methods:isdisabled}








To check the given TreeView node is disabled or enabled.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isDisabled($("#book")); // It will return true, if the given TreeView node is disabled, else false. 
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isDisabled", $("#book"));        
</script>{% endhighlight %}









### isExist<span class="signature">(element)</span>
{:#methods:isexist}








To check the given node is exist in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isExist($("#book")); // It will return true, if the given node is exist in TreeView, else false. 
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isExist", $("#book"));        
</script>{% endhighlight %}










### isExpanded<span class="signature">(element)</span>
{:#methods:isexpanded}








To get the expand status of the given TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isExpanded($("#book")); // It will return true, if the given TreeView node is expanded, else false. 
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isExpanded", $("#book"));        
</script>{% endhighlight %}







### isSelected<span class="signature">(element)</span>
{:#methods:isselected}








To get the select status of the given TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isSelected($("#book")); // It will return true, if the given TreeView node is selected, else false.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isSelected", $("#book"));        
</script>{% endhighlight %}







### isVisible<span class="signature">(element)</span>
{:#methods:isvisible}








To get the visibility status of the given TreeView node.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




#### Returns:
{:#methods:returns:}

boolean





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.isVisible($("#book")); // It will return true, if the given TreeView node is visible, else false.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("isVisible", $("#book"));        
</script>{% endhighlight %}








### loadData<span class="signature">(newNodeText, target)</span>
{:#methods:loaddata}








To load the TreeView nodes from the particular URL. If target tree node is specified, then the given nodes are added as child of target tree node, otherwise nodes are added in TreeView.  

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
URL{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">URL location, the data returned from the URL will be loaded in TreeView</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.loadData("myapplication/childdata", "book"); // The array of JSON data returned from the given URL, will be appended as child of node, which node is having ID book.
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
treeObj.loadData("myapplication/childdata", $("#book"));
</script>{% endhighlight %}








### moveNode<span class="signature">(sourceNode, destionationNode, index)</span>
{:#methods:movenode}








To move the TreeView node with in same TreeView. The new poistion of given TreeView node will be based on destionation node and index position.  

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
sourceNode{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
destinationNode{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">New index position of given source node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.moveNode("#art", "#book"); // The source node(#art) will be appended as a child of destination node(book).
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
treeObj.moveNode($("#art"), "", 3); // The source node will be placed directly to the given index position in TreeView.
</script>{% endhighlight %}









### refresh<span class="signature">()</span>
{:#methods:refresh}








To refresh the TreeView





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.refresh(); // It will refresh the TreeView.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("refresh");        
</script>{% endhighlight %}







### removeAll<span class="signature">()</span>
{:#methods:removeall}








To remove all the nodes in TreeView.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.removeAll(); // It will remove all the nodes in TreeView.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("removeAll");        
</script>{% endhighlight %}








### removeNode<span class="signature">(element)</span>
{:#methods:removenode}








To remove a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.removeNode($("#book")); // Given TreeView node will be removed and childnodes also removed.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("removeNode", $("#book"));        
</script>{% endhighlight %}







### selectNode<span class="signature">(element)</span>
{:#methods:selectnode}








To select a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.selectNode($("#book")); // Given TreeView node will be selected.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("selectNode", $("#book"));        
</script>{% endhighlight %}







### show<span class="signature">()</span>
{:#methods:show}








To show nodes in TreeView.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.show(); // It will show all the nodes in TreeView.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("show");        
</script>{% endhighlight %}







### showNode<span class="signature">(element)</span>
{:#methods:shownode}








To show a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.showNode($("#book")); // It will show the given TreeView node.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("showNode", $("#book"));        
</script>{% endhighlight %}







### unCheckAll<span class="signature">()</span>
{:#methods:uncheckall}








To uncheck all the nodes in TreeView.





Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.unCheckAll(); // All the TreeView nodes will be unchecked.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("unCheckAll");        
</script>{% endhighlight %}







### uncheckNode<span class="signature">(element)</span>
{:#methods:unchecknode}








To uncheck a node in TreeView.

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
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    showCheckbox:true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.uncheckNode($("#book")); // Given TreeView node will be unchecked.
</script>{% endhighlight %}


{% highlight html %} 
<script>
$("#treeView").ejTreeView("uncheckNode", $("#book"));        
</script>{% endhighlight %}







### unselectNode<span class="signature">(element)</span>
{:#methods:unselectnode}








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
<td class="name">{% highlight html %}
element{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.unselectNode($("#book")); // Given TreeView node will be unselected.
</script>{% endhighlight %}


{% highlight html %}
<script>
$("#treeView").ejTreeView("unselectNode", $("#book"));        
</script>{% endhighlight %}







### updateText<span class="signature">(target, newText)</span>
{:#methods:updatetext}








To edit or update the text of the TreeView node.  

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
target{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">ID of TreeView node/object of TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
newText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">New text</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="treeView"></div>
<script>
// Initialize TreeView    
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
});

var treeObj = $("#treeView").data("ejTreeView");
treeObj.updateText("book", "NewText"); // It will update the text of the given TreeView node.
</script>{% endhighlight %}


{% highlight html %}
 
 
<script>
var treeObj = $("#treeView").data("ejTreeView");
treeObj.updateText($("#book"), "NewText");
</script>{% endhighlight %}








## Events







### beforeAdd
{:#events:beforeadd}








Fires before adding node to TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">string/object</span></td>
<td class="description last">returns the given new node data</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetParent{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the parent element, the given new nodes to be appended to the given parent element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeAdd event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeAdd: function(args) {}
});
</script>{% endhighlight %}









### beforeCollapse
{:#events:beforecollapse}








Fires before collapse a node.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeCollapse event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeCollapse: function(args) {}
});
</script>{% endhighlight %}







### beforeCut
{:#events:beforecut}








Fires before cut node in TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element, the given node to be cut</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.keyCode{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeCut event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeCut: function(args) {}
});
</script>{% endhighlight %}










### beforeDelete
{:#events:beforedelete}








Fires before deleting node in TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element, the given node to be deleted</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the target node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the parent node values</td> 
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeDelete event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeDelete: function(args) {}
});
</script>{% endhighlight %}











### beforeEdit
{:#events:beforeedit}








Fires before editing the node in TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeEdit event.
$("#treeView").ejTreeView({
    allowEditing: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeEdit: function(args) {}
});
</script>{% endhighlight %}






### beforeExpand
{:#events:beforeexpand}








Fires before expanding the node.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChildLoaded{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the child node is ready to expanded state; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeExpand event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeExpand: function(args) {}
});
</script>{% endhighlight %}







### beforeLoad
{:#events:beforeload}








Fires before loading nodes to TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.ajaxOptions{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the AJAX settings object</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeLoad event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeLoad: function(args) {}
});
</script>{% endhighlight %}












### beforePaste
{:#events:beforepaste}








Fires before paste node in TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element, the given node to be pasted</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.keyCode{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforePaste event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforePaste: function(args) {}
});
</script>{% endhighlight %}












### create
{:#events:create}








Fires when TreeView created successfully.

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
<td class="description last">returns the TreeView model</td>
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

<div id="treeView"></div>
<script>
// Initialize TreeView with create event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    create: function(args) {}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires when TreeView destroyed successfully.

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
<td class="description last">returns the TreeView model</td>
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

<div id="treeView"></div>
<script>
// Initialize TreeView with destroy event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    destroy: function(args) {}
});
</script>{% endhighlight %}







### beforeSelect
{:#events:beforeselect}








Fires before selecting node in TreeView.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element, the given node to be selected</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with beforeSelect event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    beforeSelect: function(args) {}
});
</script>{% endhighlight %}













### inlineEditValidation
{:#events:inlineeditvalidation}








Fires before nodeEdit Successful.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.newText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the new entered text for the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current node element id</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.oldText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the old node text</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with inlineEditValidation event.
$("#treeView").ejTreeView({
    allowEditing: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    inlineEditValidation: function(args) {}
});
</script>{% endhighlight %}






### keyPress
{:#events:keypress}








Fires when key pressed successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.path{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns node path from root element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.keyCode{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isExpanded{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns when the current node is in expanded state; otherwise, false.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with keyPress event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    keyPress: function(args) {}
});
</script>{% endhighlight %}







### loadError
{:#events:loaderror}








Fires when data load fails.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.error{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the AJAX error object</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with loadError event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    loadError: function(args) {}
});
</script>{% endhighlight %}













### loadSuccess
{:#events:loadsuccess}








Fires when data loaded successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the success data from the URL</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetParent{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target parent element, the data returned from the URL to be appended to the given parent element, else in TreeView</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with loadSuccess event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    loadSuccess: function(args) {}
});
</script>{% endhighlight %}












### nodeAdd
{:#events:nodeadd}








Fires when node added successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.data{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the added data, that are given initially</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodes{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the newly added elements</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target parent element of the added element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeAdd event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeAdd: function(args) {}
});
</script>{% endhighlight %}
















### nodeCheck
{:#events:nodecheck}








Fires when node checked successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns true when the node checkbox is checked; otherwise, false.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeCheck event.
$("#treeView").ejTreeView({
    showCheckbox: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeCheck: function(args) {}
});
</script>{% endhighlight %}






### nodeClick
{:#events:nodeclick}








Fires when node clicked successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element target</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeClick event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeClick: function(args) {}
});
</script>{% endhighlight %}






### nodeCollapse
{:#events:nodecollapse}








Fires when node collapsed successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeCollapse event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeCollapse: function(args) {}
});
</script>{% endhighlight %}






### nodeCut
{:#events:nodecut}








Fires when node cut successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the cut node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.keyCode{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeCut event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeCut: function(args) {}
});
</script>{% endhighlight %}










### nodeDelete
{:#events:nodedelete}








Fires when node deleted successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the deleted node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeDelete event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeDelete: function(args) {}
});
</script>{% endhighlight %}












### nodeDrag
{:#events:nodedrag}








Fires when node dragging.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.dragTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original drag target</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current target TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current target details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the target node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeDrag event.
$("#treeView").ejTreeView({
    allowDragAndDrop: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeDrag: function(args) {}
});
</script>{% endhighlight %}







### nodeDragStart
{:#events:nodedragstart}








Fires when node drag start successfully.


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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.dragTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original drag target</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.draggedElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dragging TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.draggedElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dragging TreeView node details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the dragging node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>



Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeDragStart event.
$("#treeView").ejTreeView({
    allowDragAndDrop: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeDragStart: function(args) {}
});
</script>{% endhighlight %}







### nodeDragStop
{:#events:nodedragstop}








Fires before the dragged node to be dropped.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.dropTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original drop target</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.draggedElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dragged TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.draggedElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dragged TreeView node details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the dragged node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.position{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the drop position such as before, after or over</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeDragStop event.
$("#treeView").ejTreeView({
    allowDragAndDrop: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeDragStop: function(args) {}
});
</script>{% endhighlight %}







### nodeDropped
{:#events:nodedropped}








Fires when node dropped successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.dropTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the original drop target</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.droppedElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dropped TreeView node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.droppedElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current dropped TreeView node details</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current parent element of the dropped node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.targetElementData{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given parent node details</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.position{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the drop position such as before, after or over</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeDropped event.
$("#treeView").ejTreeView({
    allowDragAndDrop: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeDropped: function(args) {}
});
</script>{% endhighlight %}







### nodeEdit
{:#events:nodeedit}








Fires when node edited successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the id of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.oldText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the oldText of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.newText{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the newText of the element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target element, the given node to be cut</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeEdit event.
$("#treeView").ejTreeView({
    allowEditing: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeEdit: function(args) {}
});
</script>{% endhighlight %}







### nodeExpand
{:#events:nodeexpand}








Fires when node expanded successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChildLoaded{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the child node is ready to expanded state; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeExpand event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeExpand: function(args) {}
});
</script>{% endhighlight %}







### nodePaste
{:#events:nodepaste}








Fires when node pasted successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the pasted element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.nodeDetails{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the given target node values</td> 
</tr>
<tr>
<td class="name">{% highlight html %}
argument.keyCode{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the keypressed keycode value</td>
</tr>
<tr>
<tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodePaste event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodePaste: function(args) {}
});
</script>{% endhighlight %}












### nodeSelect
{:#events:nodeselect}








Fires when node selected successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeSelect event.
$("#treeView").ejTreeView({
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeSelect: function(args) {}
});
</script>{% endhighlight %}







### nodeUncheck
{:#events:nodeuncheck}








Fires when node unchecked successfully.

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
<td class="description last">returns the TreeView model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.event{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the event object</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.id{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.parentId{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the id of the parent element of current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the value of the node</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.currentElement{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the current element of the node clicked</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">it returns true when the node checkbox is checked; otherwise, false.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}

<div id="treeView"></div>
<script>
// Initialize TreeView with nodeUncheck event.
$("#treeView").ejTreeView({
    showCheckbox: true,
    fields: { dataSource: window.treeData, id: "id", parentId: "pid", text: "name", hasChild: "hasChild", expanded: "expanded" },
    nodeUncheck: function(args) {}
});
</script>{% endhighlight %}




