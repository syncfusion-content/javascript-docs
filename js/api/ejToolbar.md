---
layout: post
title: ejToolbar
description: API reference for ejToolbar
documentation: API
platform: js
keywords: Toolbar, ejToolbar, syncfusion, Toolbar api 
---

# ejToolbar



The Toolbar control supports displaying a list of tools within a web page. This control is capable of customizing toolbar items with any functionality by using enriched client-side methods. This control is composed of collection of unordered lists containing text and images contained into a div.





#### Syntax

{% highlight js %}

$(element).ejToolbar()

{% endhighlight %}







#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// Create Toolbar
 $("#toolbar1").ejToolbar();    
</script>{% endhighlight %}




#### Requires



* module:jQuery

* module:ej.core.js

* module:ej.data.js

* module:ej.toolbar.js


## Members




### cssClass `string`
{:#members:cssclass}




Sets the root class for Toolbar control theme


#### Default Value




* ""




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// Sets the root class for Toolbar control theme on initialization. 
        //To set the cssClass API value.
        $("#toolbar1").ejToolbar({cssClass: "gradient-lime"});
</script>{% endhighlight %}




### dataSource `ObjectArray`
{:#members:datasource}




Specifies dataSource value for the Toolbar during initialization.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// to set dataSource value during initialization. 
        //To set dataSource  API value 
        items = [{ edid: "1", spriteCssClass: "editTools cursor", text: "Cursor" },
{ edid: "2", spriteCssClass: "editTools select", text: "Select" },
{ edid: "3", spriteCssClass: "editTools move", text: "Move" },
{ edid: "4", spriteCssClass: "editTools rectselect", text: "Rectangle Select" }];
$("#toolbar1").ejToolbar({ dataSource:  items}); 
</script>{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Specifies the Toolbar control state.


#### Default Value




* true




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// Enable Toolbar on initialization. 
        //To set enabled API value 
        $("#toolbar1").ejToolbar({ enabled:  true });                   
</script>{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Specifies enableRTL property for the Toolbar during initialization.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// to set enableRTL Toolbar on initialization. 
        //To set enableRTL API value 
        $("#toolbar1").ejToolbar({ enableRTL: false });                  
</script>{% endhighlight %}




### enableSeparator `boolean`
{:#members:enableseparator}




Specifies the to enableSeparator.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//specifies enableSeparator Toolbar on initialization. 
        //To set enableSeparator API value 
        $("#toolbar1").ejToolbar({enableSeparator:true});                        
</script>{% endhighlight %}




### fields `string`
{:#members:fields}




Specifies the mapping fields for the data items of the Toolbar


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
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
</script>{% endhighlight %}




### fields.group `string`
{:#members:fields-group}




Defines the group name for the item.






### fields.htmlAttributes `object`
{:#members:fields-htmlattributes}




Defines the html attributes such as id, class, styles for the item.






### fields.id `string`
{:#members:fields-id}




Defines id for the tag.






### fields.imageAttributes `string`
{:#members:fields-imageattributes}




Defines the image attributes such as height, width, styles and so on.






### fields.imageUrl `string`
{:#members:fields-imageurl}




Defines the imageURL for the image location.






### fields.spriteCssClass `string`
{:#members:fields-spritecssclass}




Defines the sprite css for the image tag.






### fields.text `string`
{:#members:fields-text}




Defines the text content for the tag.






### fields.tooltipText `string`
{:#members:fields-tooltiptext}




Defines the tooltip text for the tag.






### height `number`
{:#members:height}




Specifies the height of the Toolbar.


#### Default Value




* 28




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//To set height API value during initialization  
        $("#toolbar1").ejToolbar({ height: 30 });                                        
</script>{% endhighlight %}




### hide `boolean`
{:#members:hide}




Specifies the to show or hide.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// Hide Toolbar on initialization. 
        //To set hide API value 
        $("#toolbar1").ejToolbar({  hide: true });                      
</script>{% endhighlight %}




### isResponsive `boolean`
{:#members:isresponsive}




Enables/Disables the responsive support for RTE control toolbar items during the window resizing time.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// to set isResponsive Toolbar on initialization. 
        //To set isResponsive API value 
        $("#toolbar1").ejToolbar({ isResponsive: true });                        
</script>{% endhighlight %}




### orientation `enum`  `string`
{:#members:orientation}




Specifies the to toolbar orientation.See orientation


#### Default Value




* Horizontal




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// Specifies orientation of  Toolbar on initialization. 
        //To set orientation API value 
        $("#toolbar1").ejToolbar({ orientation: ej.Orientation.Horizontal }); 
</script>{% endhighlight %}




### query `object`
{:#members:query}




Specifies Specifies the query to retrieve the data from the online server. The query is used only when the online dataSource is used.


#### Default Value




* null




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
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
</script>{% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Specifies showRoundedCorner property for the Toolbar during initialization.


#### Default Value




* false




#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
// to set showRoundedCorner for Toolbar on initialization. 
        //To set showRoundedCorner API value 
        $("#toolbar1").ejToolbar({ showRoundedCorner: true });                   
</script>{% endhighlight %}



## Methods




### deselectItem()
{:#methods:deselectitem}




To Deselect the Toolbar item



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItem",$("li")[3]);//Select the Toolbar item.
$("#toolbar1").ejToolbar("deselectItem",$("li")[3]); //Deselect the Toolbar item.
</script>{% endhighlight %}




### deselectItemByID()
{:#methods:deselectitembyid}




To Deselect the Toolbar item by id



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItemByID","left");//Select the Toolbar item by id.
$("#toolbar1").ejToolbar("deselectItemByID","left"); // To Deselect the Toolbar item by id.
</script>{% endhighlight %}




### destroy()
{:#methods:destroy}




destroy the Toolbar widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
<script>
//Initialize the Toolbar object.
$("#toolbar1").ejToolbar();
var toolbarObj = $("#toolbar1").data("ejToolbar");
 toolbarObj.destroy();       //Calls the destroy method of the Toolbar.
</script>{% endhighlight %}




### disable()
{:#methods:disable}




To Disable all item in the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disable"); //Disable all item in the Toolbar
</script>{% endhighlight %}




### disableItem()
{:#methods:disableitem}




To disable an item the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disableItem",$("li")[3]);// to disable the third item in the toolbar
</script>{% endhighlight %}




### disableItemByID()
{:#methods:disableitembyid}




To Disable the Toolbar item by item id in the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("disableItemByID","left"); //Disable the Toolbar item by item id
</script>{% endhighlight %}




### enable()
{:#methods:enable}




To enable all item in the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enable"); //enable all item in the Toolbar
</script>{% endhighlight %}




### enableItem()
{:#methods:enableitem}




To enable an item the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enableItem",$("li")[3]);// to enable the third item in the toolbar
</script>{% endhighlight %}




### enableItemByID()
{:#methods:enableitembyid}




To Disable the Toolbar item by item id in the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("enableItemByID","left"); //Disable the Toolbar item by item id
</script>{% endhighlight %}




### hide()
{:#methods:hide}




To hide the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar("hide");// to hide the toolbar
</script>{% endhighlight %}




### removeItem()
{:#methods:removeitem}




To Remove the Toolbar item



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("removeItem",$("li")[3]); // Remove the Toolbar item
</script>{% endhighlight %}




### removeItemByID()
{:#methods:removeitembyid}




To Remove the Toolbar item by id



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("removeItemByID","left"); // Remove the Toolbar item by id
</script>{% endhighlight %}




### selectItem()
{:#methods:selectitem}




To Select the Toolbar item



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItem",$("li")[3]);//Select the Toolbar item.
</script>{% endhighlight %}




### selectItemByID()
{:#methods:selectitembyid}




To Select the Toolbar item by id



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
$("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("selectItemByID","left");//Select the Toolbar item by id.
</script>{% endhighlight %}




### show()
{:#methods:show}




To show the Toolbar



#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
        </ul>
        <ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
        $("#toolbar1").ejToolbar();
$("#toolbar1").ejToolbar("show");// to show the toolbar
</script>{% endhighlight %}



## Events




### click
{:#events:click}




Fires after Toolbar control is clicked.

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
<td class="description">Event parameters from Toolbar
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
<td class="description">returns the Toolbar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//create event for Toolbar
 $("#toolbar1").ejToolbar({
 click: function (args) {}
});
</script>{% endhighlight %}




### create
{:#events:create}




Fires after Toolbar control is created.

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
<td class="description">Event parameters from Toolbar
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
<td class="description">returns the Toolbar model</td>
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
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//create event for Toolbar
 $("#toolbar1").ejToolbar({
 create: function (args) {}
});
</script>{% endhighlight %}




### destroy
{:#events:destroy}




Fires when the Toolbar is destroyed successfully.

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
<td class="description">Event parameters from Toolbar
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
<td class="description">returns the Toolbar model</td>
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
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//destroy event for Toolbar
$("#toolbar1").ejToolbar({
   destroy: function (args) {}
});
</script>{% endhighlight %}




### itemHover
{:#events:itemhover}




Fires after Toolbar control is itemHovered.

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
<td class="description">Event parameters from Toolbar
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
<td class="description">returns the Toolbar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//itemHover event for Toolbar
 $("#toolbar1").ejToolbar({
 itemHover: function (args) {}
});
</script>{% endhighlight %}




### itemLeave
{:#events:itemleave}




Fires after Toolbar control is itemLeave.

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
<td class="description">Event parameters from Toolbar
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
<td class="description">returns the Toolbar model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
target{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
currentTarget{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the target of the current object.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
status{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">return the Toolbar state</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<div id="toolbar1">
<ul>
   <li id="Left" title="Left">
       <div class="ToolbarItems LeftAlign_tool"></div>
  </li>
   <li id="Center" title="Center">
       <div class="ToolbarItems CenterAlign_tool"></div>
   </li>
   <li id="Right" title="Right">
       <div class="ToolbarItems RightAlign_tool"></div>
   </li>
   <li id="Justify" title="Justify">
       <div class="ToolbarItems Justify_tool"></div>
   </li>
</ul>
<ul>
   <li id="Bold" title="Bold">
       <div class="ToolbarItems Bold_tool"></div>
   </li>
   <li id="Italic" title="Italic">
       <div class="ToolbarItems Italic_tool"></div>
   </li>
   <li id="StrikeThrough" title="Strike Through">
       <div class="ToolbarItems StrikeThrough_tool"></div>
   </li>
   <li id="UndeLine" title="UnderLine">
       <div class="ToolbarItems Underline_tool"></div>
   </li>
</ul>
</div>
<script>
//itemLeave event for Toolbar
 $("#toolbar1").ejToolbar({
 itemLeave: function (args) {}
});
</script>{% endhighlight %}



