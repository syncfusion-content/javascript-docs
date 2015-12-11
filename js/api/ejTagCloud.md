---
layout: post
title: ejTagCloud
description: API reference for ejTagCloud
documentation: API
platform: js
keywords: TagCloud, ejTagCloud, syncfusion, TagCloud api 
---

# ejTagCloud





The TagCloud allows the user to display a list of links or tags with a structured cloud format where the importance of the tags can differentiate with varied font sizes, colors, and styles.









#### Syntax

{% highlight js %}

$(element).ejTagCloud()

{% endhighlight %}












#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script> 
$(function () {
        // document ready
        // initialize the array of data for tagcloud input      
// simple tagcloud creation
        $("#tagcloud").ejTagCloud({ 
            dataSource:  window.websiteCollection,
            titleText: "Tech Sites"
      });
});
</script>{% endhighlight %}







#### Requires



* module:jQuery


* module:ej.core.js


* module:ej.data.js


* module:ej.tagcloud.js




## Members








### cssClass `string`
{:#members:cssclass}








Specify the CSS class to button to achieve custom theme.




#### Default Value







* ""








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the CSS class during initialization.                     
        $("#tagcloud").ejTagCloud({dataSource: window.websiteCollection,cssClass  : "gradient-lime",titleText: "Tech Sites" });                                         
</script>{% endhighlight %}







### dataSource `object`
{:#members:datasource}








The dataSource contains the list of data to display in a cloud format. Each data contains a link url, frequency to categorize the font size and a display text.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
//Initialize the TagCloud with the dataSource value specified                      
$("#tagcloud").ejTagCloud({ dataSource: window.websiteCollection,titleText: "Tech Sites" });    
</script>{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Sets the TagCloud and tag items direction as right to left alignment.




#### Default Value







* false








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the enableRTL during initialization.                     
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,enableRTL : false,titleText: "Tech Sites"  });                         
</script>{% endhighlight %}







### fields `object`
{:#members:fields}








Defines the mapping fields for the data items of the TagCloud.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
$(function () {
// Initialize the TagCloud with the fields value specified    
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
       titleText: "Tech Sites",
fields: { text: "text" , url:"url",frequency: "frequency"}  
});
});
</script>{% endhighlight %}







### fields.frequency `number`
{:#members:fields-frequency}








Defines the frequency number to categorize the font size.











### fields.htmlAttributes `object`
{:#members:fields-htmlattributes}








Defines the html attributes for the anchor elements inside the each tag items.











### fields.text `string`
{:#members:fields-text}








Defines the tag value or display text.











### fields.url `string`
{:#members:fields-url}








Defines the url link to navigate while click the tag.











### format `string`  `enum`
{:#members:format}








Defines the format for the TagCloud to display the tag items.See <a href="global.html#Format">Format</a>




#### Default Value







* ej.Format.Cloud








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the format during initialization.                        
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,format: ej.Format.Cloud,titleText: "Tech Sites" });                   
</script>{% endhighlight %}







### maxFontSize `string`  `number`
{:#members:maxfontsize}








Sets the maximum font size value for the tag items. The font size for the tag items will be generated in between the minimum and maximum font size values.




#### Default Value







* "40px"








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the maxFontSize during initialization.                   
        $("#tagcloud").ejTagCloud({ dataSource:  window.websiteCollection,maxFontSize : "10px" ,titleText: "Tech Sites" });                      
</script>{% endhighlight %}







### minFontSize `string`  `number`
{:#members:minfontsize}








Sets the minimum font size value for the tag items. The font size for the tag items will be generated in between the minimum and maximum font size values.




#### Default Value







* "10px"








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the minFontSize during initialization.                   
        $("#tagcloud").ejTagCloud({dataSource:  window.websiteCollection, minFontSize : "10px" ,titleText: "Tech Sites" });                      
</script>{% endhighlight %}







### query `object`
{:#members:query}








Define the query to retrieve the data from online server. The query is used only when the online dataSource is used.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}







### showTitle `boolean`
{:#members:showtitle}








Shows or hides the TagCloud title. When this set to false, it hides the TagCloud header.




#### Default Value







* true








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the showTitle during initialization.                     
        $("#tagcloud").ejTagCloud({     dataSource: window.websiteCollection, showTitle : false  });                     
</script>{% endhighlight %}







### titleImage `string`
{:#members:titleimage}








Sets the title image for the TagCloud. To show the title image, the showTitle property should be enabled.




#### Default Value







* null








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the titleImage during initialization.                    
        $("#tagcloud").ejTagCloud({  dataSource: window.websiteCollection,titleImage: '../images/bird.png' ,titleText: "Tech Sites"  });                         
</script>{% endhighlight %}







### titleText `string`
{:#members:titletext}








Sets the title text for the TagCloud. To show the title text, the showTitle property should be enabled.




#### Default Value







* "Title"








#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
// Set the titleText during initialization.                     
        $("#tagcloud").ejTagCloud({  dataSource:  window.websiteCollection,titleText : "Cloud Data"  });                         
</script>{% endhighlight %}





## Methods








### insert()
{:#methods:insert}








Inserts a new item into the TagCloud





#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}


{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready
// initialize the array of data for tagcloud input  
$("#tagcloud").ejTagCloud({ 
            dataSource: window.websiteCollection,titleText: "Tech Sites"
});  
$("#tagcloud").ejTagCloud("insert", tag);        
});
</script>{% endhighlight %}







### insertAt()
{:#methods:insertat}








Inserts a new item into the TagCloud at a particular position.





#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}


{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
var tag = { text: "google", url: "http://www.google.com", frequency: 12 };
$(function () {
// document ready 
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
}); 
$("#tagcloud").ejTagCloud("insertAt", tag, 2);
});
</script>{% endhighlight %}







### remove(name)</span>
{:#methods:remove}








Removes the item from the TagCloud based on the name. It removes all the tags which have the corresponding name

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
<td class="name">{% highlight html %}
name{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">name of the tag.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}


{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}







### removeAt(position)</span>
{:#methods:removeat}








Removes the item from the TagCloud based on the position. It removes the tags from the the corresponding position only.

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
<td class="name">{% highlight html %}
position{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">position of tag item.</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
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
</script>{% endhighlight %}


{% highlight html %}
 
     <div id="tagcloud"></div> 
 
<script>
$(function () {
// document ready
$("#tagcloud").ejTagCloud({
dataSource:window.websiteCollection,
titleText: "Tech Sites"
});
$("#tagcloud").ejTagCloud("removeAt", 4);
});
</script>{% endhighlight %}





## Events








### click
{:#events:click}








Event triggers when the TagCloud items are clicked

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tagcloud model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current tag name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current url link</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
//click event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   click: function (args) {}
});        
</script>    {% endhighlight %}







### create
{:#events:create}








Event triggers when the TagCloud are created

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tagcloud model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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
 
<div id="tagcloud"></div> 
 
<script>
//create event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   create: function (args) {}
});        
</script>    {% endhighlight %}







### destroy
{:#events:destroy}








Event triggers when the TagCloud are destroyed

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tagcloud model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
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
 
<div id="tagcloud"></div> 
 
<script>
//destroy event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   destroy: function (args) {}
});        
</script>    {% endhighlight %}







### mouseout
{:#events:mouseout}








Event triggers when the cursor leaves out from a tag item

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tagcloud model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current tag name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current url link</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
//mouseout event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
 titleText: "Tech Sites",
   mouseout: function (args) {}
});           
</script>     {% endhighlight %}







### mouseover
{:#events:mouseover}








Event triggers when the cursor hovers on a tag item

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from button
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
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the tagcloud model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
text{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current tag name</td>
</tr>
<tr>
<td class="name">{% highlight html %}
url{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">return current url link</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




#### Example



{% highlight html %}
 
<div id="tagcloud"></div> 
 
<script>
//mouse over event for tagCloud
$("#tagcloud").ejTagCloud({
 dataSource: window.websiteCollection,
titleText: "Tech Sites",
   mouseover: function (args) {}
});   
</script>   {% endhighlight %}




