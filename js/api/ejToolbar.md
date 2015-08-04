---
layout: post
title: ejToolbar
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Toolbar control.





$(element).ejToolbar<span class="signature">()</span>






Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Create Toolbar
 $("#toolbar1").ejToolbar();    
&lt;/script&gt;</code>
</pre>



Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.data.js

* module:ej.toolbar.js


## Members




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Sets the root class for Toolbar control theme


Default Value:
{:.param}



* ""




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Sets the root class for Toolbar control theme on initialization. 
        //To set the cssClass API value.
        $("#toolbar1").ejToolbar({cssClass: "gradient-lime"});
&lt;/script&gt;</code>
</pre>



### dataSource<span class="type-signature type objectarray">ObjectArray</span>
{:#members:datasource}




Specifies dataSource value for the Toolbar during initialization.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// to set dataSource value during initialization. 
        //To set dataSource  API value 
        items = [{ edid: "1", spriteCssClass: "editTools cursor", text: "Cursor" },
{ edid: "2", spriteCssClass: "editTools select", text: "Select" },
{ edid: "3", spriteCssClass: "editTools move", text: "Move" },
{ edid: "4", spriteCssClass: "editTools rectselect", text: "Rectangle Select" }];
$("#toolbar1").ejToolbar({ dataSource:  items}); 
&lt;/script&gt;</code>
</pre>



### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Specifies the Toolbar control state.


Default Value:
{:.param}



* true




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Enable Toolbar on initialization. 
        //To set enabled API value 
        $("#toolbar1").ejToolbar({ enabled:  true });                   
&lt;/script&gt;</code>
</pre>



### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Specifies enableRTL property for the Toolbar during initialization.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// to set enableRTL Toolbar on initialization. 
        //To set enableRTL API value 
        $("#toolbar1").ejToolbar({ enableRTL: false });                  
&lt;/script&gt;</code>
</pre>



### enableSeparator<span class="type-signature type boolean">boolean</span>
{:#members:enableseparator}




Specifies the to enableSeparator.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//specifies enableSeparator Toolbar on initialization. 
        //To set enableSeparator API value 
        $("#toolbar1").ejToolbar({enableSeparator:true});                        
&lt;/script&gt;</code>
</pre>



### fields<span class="type-signature type string">string</span>
{:#members:fields}




Specifies the mapping fields for the data items of the Toolbar


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// To set fields API value during initialization. 
        //To set the fields API value.
        items = [{ edid: "1", spriteCssClass: "editTools cursor", text: "Cursor" },
 { edid: "2", spriteCssClass: "editTools select", text: "Select" },
 { edid: "3", spriteCssClass: "editTools move", text: "Move" },
 { edid: "4", spriteCssClass: "editTools rectselect", text: "Rectangle Select"
 }];
$("#toolbar1").ejToolbar(
                {
                        dataSource:  items,
          fields:  { id: "empid",spriteCssClass: "spriteCss"}
        });
&lt;/script&gt;</code>
</pre>



### fields.group<span class="type-signature type string">String</span>
{:#members:fields-group}




Defines the group name for the item.






### fields.htmlAttributes<span class="type-signature type object">Object</span>
{:#members:fields-htmlattributes}




Defines the html attributes such as id, class, styles for the item.






### fields.id<span class="type-signature type string">String</span>
{:#members:fields-id}




Defines id for the tag.






### fields.imageAttributes<span class="type-signature type string">String</span>
{:#members:fields-imageattributes}




Defines the image attributes such as height, width, styles and so on.






### fields.imageUrl<span class="type-signature type string">String</span>
{:#members:fields-imageurl}




Defines the imageURL for the image location.






### fields.spriteCssClass<span class="type-signature type string">String</span>
{:#members:fields-spritecssclass}




Defines the sprite css for the image tag.






### fields.text<span class="type-signature type string">String</span>
{:#members:fields-text}




Defines the text content for the tag.






### fields.tooltipText<span class="type-signature type string">String</span>
{:#members:fields-tooltiptext}




Defines the tooltip text for the tag.






### height<span class="type-signature type number">number</span>
{:#members:height}




Specifies the height of the Toolbar.


Default Value:
{:.param}



* 28




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//To set height API value during initialization  
        $("#toolbar1").ejToolbar({ height: 30 });                                        
&lt;/script&gt;</code>
</pre>



### hide<span class="type-signature type boolean">boolean</span>
{:#members:hide}




Specifies the to show or hide.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Hide Toolbar on initialization. 
        //To set hide API value 
        $("#toolbar1").ejToolbar({  hide: true });                      
&lt;/script&gt;</code>
</pre>



### isResponsive<span class="type-signature type boolean">boolean</span>
{:#members:isresponsive}




Enables/Disables the responsive support for RTE control toolbar items during the window resizing time.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// to set isResponsive Toolbar on initialization. 
        //To set isResponsive API value 
        $("#toolbar1").ejToolbar({ isResponsive: true });                        
&lt;/script&gt;</code>
</pre>



### orientation<span class="type-signature type enum">Enum</span> <span class="type-signature type string">String</span>
{:#members:orientation}




Specifies the to toolbar orientation.See orientation


Default Value:
{:.param}



* Horizontal




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// Specifies orientation of  Toolbar on initialization. 
        //To set orientation API value 
        $("#toolbar1").ejToolbar({ orientation: ej.Orientation.Horizontal }); 
&lt;/script&gt;</code>
</pre>



### query<span class="type-signature type object">object</span>
{:#members:query}




Specifies Specifies the query to retrieve the data from the online server. The query is used only when the online dataSource is used.


Default Value:
{:.param}



* null




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// To set query API value on initialization. 
        //To set query API value.
        // DataManager creation.
var dataManger = ej.DataManager({
url: "http://mvc.syncfusion.com/Services/Northwnd.svc/"
});
 // Query creation.
var query = ej.Query()
                .from("Orders").take(6);
                        $("#toolbar1").ejToolbar(
               {
             dataSource: dataManger,
              query: query
        });
&lt;/script&gt;</code>
</pre>



### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}




Specifies showRoundedCorner property for the Toolbar during initialization.


Default Value:
{:.param}



* false




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
// to set showRoundedCorner for Toolbar on initialization. 
        //To set showRoundedCorner API value 
        $("#toolbar1").ejToolbar({ showRoundedCorner: true });                   
&lt;/script&gt;</code>
</pre>


## Methods




### deselectItem<span class="signature">()</span>
{:#methods:deselectitem}




To Deselect the Toolbar item



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItem",$("li")[3]);//Select the Toolbar item.
$("#toolbar1").ejToolbar("deselectItem",$("li")[3]); //Deselect the Toolbar item.
&lt;/script&gt;</code>
</pre>



### deselectItemByID<span class="signature">()</span>
{:#methods:deselectitembyid}




To Deselect the Toolbar item by id



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItemByID","left");//Select the Toolbar item by id.
$("#toolbar1").ejToolbar("deselectItemByID","left"); // To Deselect the Toolbar item by id.
&lt;/script&gt;</code>
</pre>



### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the Toolbar widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
&lt;script&gt;
//Initialize the Toolbar object.
$("#toolbar1").ejToolbar();
var toolbarObj = $("#toolbar1").data("ejToolbar");
 toolbarObj.destroy();       //Calls the destroy method of the Toolbar.
&lt;/script&gt;</code>
</pre>



### disable<span class="signature">()</span>
{:#methods:disable}




To Disable all item in the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disable"); //Disable all item in the Toolbar
&lt;/script&gt;</code>
</pre>



### disableItem<span class="signature">()</span>
{:#methods:disableitem}




To disable an item the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disableItem",$("li")[3]);// to disable the third item in the toolbar
&lt;/script&gt;</code>
</pre>



### disableItemByID<span class="signature">()</span>
{:#methods:disableitembyid}




To Disable the Toolbar item by item id in the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disableItemByID","left"); //Disable the Toolbar item by item id
&lt;/script&gt;</code>
</pre>



### enable<span class="signature">()</span>
{:#methods:enable}




To enable all item in the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enable"); //enable all item in the Toolbar
&lt;/script&gt;</code>
</pre>



### enableItem<span class="signature">()</span>
{:#methods:enableitem}




To enable an item the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enableItem",$("li")[3]);// to enable the third item in the toolbar
&lt;/script&gt;</code>
</pre>



### enableItemByID<span class="signature">()</span>
{:#methods:enableitembyid}




To Disable the Toolbar item by item id in the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enableItemByID","left"); //Disable the Toolbar item by item id
&lt;/script&gt;</code>
</pre>



### hide<span class="signature">()</span>
{:#methods:hide}




To hide the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar("hide");// to hide the toolbar
&lt;/script&gt;</code>
</pre>



### removeItem<span class="signature">()</span>
{:#methods:removeitem}




To Remove the Toolbar item



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("removeItem",$("li")[3]); // Remove the Toolbar item
&lt;/script&gt;</code>
</pre>



### removeItemByID<span class="signature">()</span>
{:#methods:removeitembyid}




To Remove the Toolbar item by id



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("removeItemByID","left"); // Remove the Toolbar item by id
&lt;/script&gt;</code>
</pre>



### selectItem<span class="signature">()</span>
{:#methods:selectitem}




To Select the Toolbar item



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItem",$("li")[3]);//Select the Toolbar item.
&lt;/script&gt;</code>
</pre>



### selectItemByID<span class="signature">()</span>
{:#methods:selectitembyid}




To Select the Toolbar item by id



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItemByID","left");//Select the Toolbar item by id.
&lt;/script&gt;</code>
</pre>



### show<span class="signature">()</span>
{:#methods:show}




To show the Toolbar



Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
        &lt;/ul&gt;
        &lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
        $("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("show");// to show the toolbar
&lt;/script&gt;</code>
</pre>


## Events




### click
{:#events:click}




Fires after Toolbar control is clicked.

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
<td class="description last">Event parameters from Toolbar
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
<td class="description last">returns the Toolbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//create event for Toolbar
 $("#toolbar1").ejToolbar({
 click: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### create
{:#events:create}




Fires after Toolbar control is created.

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
<td class="description last">Event parameters from Toolbar
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
<td class="description last">returns the Toolbar model</td>
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


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//create event for Toolbar
 $("#toolbar1").ejToolbar({
 create: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### destroy
{:#events:destroy}




Fires when the Toolbar is destroyed successfully.

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
<td class="description last">Event parameters from Toolbar
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
<td class="description last">returns the Toolbar model</td>
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


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//destroy event for Toolbar
$("#toolbar1").ejToolbar({
   destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### itemHover
{:#events:itemhover}




Fires after Toolbar control is itemHovered.

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
<td class="description last">Event parameters from Toolbar
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
<td class="description last">returns the Toolbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//itemHover event for Toolbar
 $("#toolbar1").ejToolbar({
 itemHover: function (args) {}
});
&lt;/script&gt;</code>
</pre>



### itemLeave
{:#events:itemleave}




Fires after Toolbar control is itemLeave.

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
<td class="description last">Event parameters from Toolbar
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
<td class="description last">returns the Toolbar model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>target</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>currentTarget</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the target of the current object.</td>
</tr>
<tr>
<td class="name"><code>status</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;div id="toolbar1"&gt;
&lt;ul&gt;
   &lt;li id="Left" title="Left"&gt;
       &lt;div class="ToolbarItems LeftAlign_tool"&gt;&lt;/div&gt;
  &lt;/li&gt;
   &lt;li id="Center" title="Center"&gt;
       &lt;div class="ToolbarItems CenterAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Right" title="Right"&gt;
       &lt;div class="ToolbarItems RightAlign_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Justify" title="Justify"&gt;
       &lt;div class="ToolbarItems Justify_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;ul&gt;
   &lt;li id="Bold" title="Bold"&gt;
       &lt;div class="ToolbarItems Bold_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="Italic" title="Italic"&gt;
       &lt;div class="ToolbarItems Italic_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="StrikeThrough" title="Strike Through"&gt;
       &lt;div class="ToolbarItems StrikeThrough_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
   &lt;li id="UndeLine" title="UnderLine"&gt;
       &lt;div class="ToolbarItems Underline_tool"&gt;&lt;/div&gt;
   &lt;/li&gt;
&lt;/ul&gt;
&lt;/div&gt;
&lt;script&gt;
//itemLeave event for Toolbar
 $("#toolbar1").ejToolbar({
 itemLeave: function (args) {}
});
&lt;/script&gt;</code>
</pre>


