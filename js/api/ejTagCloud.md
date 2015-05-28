---
layout: post
title: ejTagCloud
metaname: 
metacontent: 
---

The TagCloud allows the user to display a list of links or tags with a structured cloud format where the importance of the tags can differentiate with varied font sizes, colors, and styles.










#### $(element).ejTagCloud<span class="signature">()</span>











##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt; 
$(function () {
        // document ready
        // initialize the array of data for tagcloud input      
// simple tagcloud creation
        $("#tagcloud").ejTagCloud({ 
            dataSource:  window.websiteCollection,
            titleText: "Tech Sites"
      });
});
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.core.js


* module:ej.data.js


* module:ej.tagcloud.js




### Members








#### cssClass<span class="type-signature type string">string</span>








Specify the CSS class to button to achieve custom theme.




Default Value:






* ""








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the CSS class during initialization.                     
        $("#tagcloud").ejTagCloud({dataSource: window.websiteCollection,cssClass  : "gradient-lime",titleText: "Tech Sites" });                                         
&lt;/script&gt;</code>
</pre>






#### dataSource<span class="type-signature type object">object</span>








The dataSource contains the list of data to display in a cloud format. Each data contains a link url, frequency to categorize the font size and a display text.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Initialize the TagCloud with the dataSource value specified                      
$("#tagcloud").ejTagCloud({ dataSource: window.websiteCollection,titleText: "Tech Sites" });    
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Sets the TagCloud and tag items direction as right to left alignment.




Default Value:






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the enableRTL during initialization.                     
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,enableRTL : false,titleText: "Tech Sites"  });                         
&lt;/script&gt;</code>
</pre>






#### fields<span class="type-signature type object">Object</span>








Defines the mapping fields for the data items of the TagCloud.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$(function () {
// Initialize the TagCloud with the fields value specified    
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
       titleText: "Tech Sites",
fields: { text: "text" , url:"url",frequency: "frequency"}  
});
});
&lt;/script&gt;</code>
</pre>






#### fields.frequency<span class="type-signature type number">Number</span>








Defines the frequency number to categorize the font size.











#### fields.htmlAttributes<span class="type-signature type object">Object</span>








Defines the html attributes for the anchor elements inside the each tag items.











#### fields.text<span class="type-signature type string">String</span>








Defines the tag value or display text.











#### fields.url<span class="type-signature type string">String</span>








Defines the url link to navigate while click the tag.











#### format<span class="type-signature type string">String</span> <span class="type-signature type enum">Enum</span>








Defines the format for the TagCloud to display the tag items.See <a href="global.html#Format">Format</a>




Default Value:






* ej.Format.Cloud








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the format during initialization.                        
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,format: ej.Format.Cloud,titleText: "Tech Sites" });                   
&lt;/script&gt;</code>
</pre>






#### maxFontSize<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Sets the maximum font size value for the tag items. The font size for the tag items will be generated in between the minimum and maximum font size values.




Default Value:






* "40px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the maxFontSize during initialization.                   
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,maxFontSize : "10px" ,titleText: "Tech Sites" });                      
&lt;/script&gt;</code>
</pre>






#### minFontSize<span class="type-signature type string">String</span> <span class="type-signature type number">Number</span>








Sets the minimum font size value for the tag items. The font size for the tag items will be generated in between the minimum and maximum font size values.




Default Value:






* "10px"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the minFontSize during initialization.                   
        $("#tagcloud").ejTagCloud({dataSource:  window.websiteCollection, minFontSize : "10px" ,titleText: "Tech Sites" });                      
&lt;/script&gt;</code>
</pre>






#### query<span class="type-signature type object">object</span>








Define the query to retrieve the data from online server. The query is used only when the online dataSource is used.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Initialize the TagCloud with the query value specified                
var dataManger = ej.DataManager({
      url:"http://mvc.syncfusion.com/Services/Northwnd.svc/"
});
var query = ej.Query().from("Orders").take(10);    
$("#tagcloud").ejTagCloud({
       titleText: "Employee List",
      dataSource: dataManger,
     query: query,
    fields: { text: "CustomerID" , frequency: "EmployeeID" }
});
&lt;/script&gt;</code>
</pre>






#### showTitle<span class="type-signature type boolean">boolean</span>








Shows or hides the TagCloud title. When this set to false, it hides the TagCloud header.




Default Value:






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the showTitle during initialization.                     
        $("#tagcloud").ejTagCloud({     dataSource: window.websiteCollection, showTitle : false  });                     
&lt;/script&gt;</code>
</pre>






#### titleImage<span class="type-signature type string">string</span>








Sets the title image for the TagCloud. To show the title image, the showTitle property should be enabled.




Default Value:






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the titleImage during initialization.                    
        $("#tagcloud").ejTagCloud({  dataSource: window.websiteCollection,titleImage: '../images/bird.png' ,titleText: "Tech Sites"  });                         
&lt;/script&gt;</code>
</pre>






#### titleText<span class="type-signature type string">string</span>








Sets the title text for the TagCloud. To show the title text, the showTitle property should be enabled.




Default Value:






* "Title"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Set the titleText during initialization.                     
        $("#tagcloud").ejTagCloud({  dataSource:  window.websiteCollection,titleText : "Cloud Data"  });                         
&lt;/script&gt;</code>
</pre>




### Methods








#### insert<span class="signature">()</span>








Inserts a new item into the TagCloud





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
  var tagObj="";
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready
// initialize the array of data for tagcloud input
$("#tagcloud").ejTagCloud({ 
            dataSource: window.websiteCollection,
            titleText: "Tech Sites"
});
//initialize the tagCloud object
tagObj = $("#tagcloud").data("ejTagCloud");
//To Inserts a new item into the TagCloud
tagObj.insert(tag);
      });     
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready
// initialize the array of data for tagcloud input  
$("#tagcloud").ejTagCloud({ 
            dataSource: window.websiteCollection,titleText: "Tech Sites"
});  
$("#tagcloud").ejTagCloud("insert", tag);        
});
&lt;/script&gt;</code>
</pre>






#### insertAt<span class="signature">()</span>








Inserts a new item into the TagCloud at a particular position.





##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
var tagObj="";
$(function () {
// document ready 
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
});
 tagObj = $("#tagcloud").data("ejTagCloud");
   tagObj.insertAt(tag,2);
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready 
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
}); 
$("#tagcloud").ejTagCloud("insertAt", tag, 2);
});
&lt;/script&gt;</code>
</pre>






#### remove<span class="signature">(name)</span>








Removes the item from the TagCloud based on the name. It removes all the tags which have the corresponding name

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
<td class="name"><code>name</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">name of the tag.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
  var tagObj="";
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready
// initialize the array of data for tagcloud input
$("#tagcloud").ejTagCloud({ 
            dataSource: window.websiteCollection,
            titleText: "Tech Sites"
});
//initialize the tagCloud object
tagObj = $("#tagcloud").data("ejTagCloud");
//To Inserts a new item into the TagCloud
tagObj.remove(tag);
      });     
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready
// initialize the array of data for tagcloud input
$("#tagcloud").ejTagCloud({ 
            dataSource: window.websiteCollection,
            titleText: "Tech Sites"
});
$("#tagcloud").ejTagCloud("remove", tag);
});
&lt;/script&gt;</code>
</pre>






#### removeAt<span class="signature">(position)</span>








Removes the item from the TagCloud based on the position. It removes the tags from the the corresponding position only.

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
<td class="name"><code>position</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">position of tag item.</td>
</tr>
</tbody>
</table>




##### Examples

<pre class="prettyprint">
<code> 
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
var tagObj = "";
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {       
// document ready   
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
});
//initialize the tagCloud object
var tagObj = $("#tagcloud").data("ejTagCloud");
// Removes the item from the TagCloud based on the position.
tagObj.removeAt(2);
});
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
     &lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
$(function () {
// document ready
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
});
$("#tagcloud").ejTagCloud("removeAt", 4);
});
&lt;/script&gt;</code>
</pre>




### Events








#### click








Event triggers when the TagCloud items are clicked

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
<td class="description last">Event parameters from button
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tagcloud model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current tag name</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current url link</td>
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
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//click event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   click: function (args) {}
});        
&lt;/script&gt;    </code>
</pre>






#### create








Event triggers when the TagCloud are created

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
<td class="description last">Event parameters from button
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tagcloud model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//create event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   create: function (args) {}
});        
&lt;/script&gt;    </code>
</pre>






#### destroy








Event triggers when the TagCloud are destroyed

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
<td class="description last">Event parameters from button
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tagcloud model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
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
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//destroy event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   destroy: function (args) {}
});        
&lt;/script&gt;    </code>
</pre>






#### mouseout








Event triggers when the cursor leaves out from a tag item

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
<td class="description last">Event parameters from button
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tagcloud model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current tag name</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current url link</td>
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
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//mouseout event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   mouseout: function (args) {}
});           
&lt;/script&gt;     </code>
</pre>






#### mouseover








Event triggers when the cursor hovers on a tag item

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
<td class="description last">Event parameters from button
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
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the tagcloud model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>text</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current tag name</td>
</tr>
<tr>
<td class="name"><code>url</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">return current url link</td>
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
&lt;div id="tagcloud"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//mouse over event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
titleText: "Tech Sites",
   mouseover: function (args) {}
});   
&lt;/script&gt;   </code>
</pre>



