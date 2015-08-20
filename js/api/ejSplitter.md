---
layout: post
title: ejSplitter
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html splitter control.











$(element).ejSplitter<span class="signature">(options)</span>







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
<td class="description last">settings for Slider.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
        <div>
                <div class="cont">Pane 1 </div>
        </div>
        <div>
                <div class="cont">Pane 2 </div>
        </div>
</div> 
<script>
// Create Splitter 
$('#innerSplitter').ejSplitter(); 
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:jquery.easing.1.3.js


* module:ej.core.js


* module:ej.splitter.js




## Members








### animationSpeed<span class="type-signature type number">number</span>
{:#members:animationspeed}








Specify animation speed for the Splitter pane movement while collapsing and expanding.




Default Value:
{:.param}






* 300








Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set animationSpeed API value during initialization
$("#innerSplitter").ejSplitter({animationSpeed: 150 });
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class to splitter control to achieve custom theme.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
        <div>
                <div class="cont">Pane 1 </div>
        </div>
        <div>
                <div class="cont">Pane 2 </div>
        </div>
</div> 
<script>
//To set cssClass API value during initialization
        $("#innerSplitter").ejSplitter({ cssClass: "gradient-lime"});
</script>{% endhighlight %}







### enableAnimation<span class="type-signature type boolean">boolean</span>
{:#members:enableanimation}








Specifies the animation behavior of the splitter.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
        <div>
                <div class="cont">Pane 1 </div>
        </div>
        <div>
                <div class="cont">Pane 2 </div>
        </div>
</div> 
<script>
//To set enableAnimation API value during initialization  
        $("#innerSplitter").ejSplitter({ enableAnimation: false});
</script>{% endhighlight %}







### enableAutoResize<span class="type-signature type boolean">boolean</span>
{:#members:enableautoresize}








Specify window resizing behavior for splitter control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set windowResizing API value during initialization
        $("#innerSplitter").ejSplitter({enableAutoResize: true});
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Specify Right to Left Direction for splitter control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set enableRTL API value during initialization  
        $("#innerSplitter").ejSplitter({enableRTL: true} );
</script>{% endhighlight %}







### height<span class="type-signature type string">string</span>
{:#members:height}








Specify height for splitter control.




Default Value:
{:.param}






* &ldquo;100%&rdquo;








Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set height API value during initialization
        $("#innerSplitter").ejSplitter({height: "100%" });
</script>{% endhighlight %}







### orientation<span class="type-signature type enum">Enum</span>
{:#members:orientation}








Specify the orientation for spliter control.See orientation




Default Value:
{:.param}






* ej.orientation.Horizontal or &ldquo;horizontal&rdquo;








Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set orientation API value during initialization  
$("#innerSplitter").ejSplitter({ orientation: ej.Orientation.Horizontal });
</script>{% endhighlight %}







### properties<span class="type-signature type array">array</span>
{:#members:properties}








Specify properties for each pane.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set properties API value during initialization  
        $("#innerSplitter").ejSplitter({properties: [{ paneSize: "100px" }, { paneSize: "50px"}]});
</script>{% endhighlight %}







### width<span class="type-signature type string">string</span>
{:#members:width}








Specify width for splitter control.




Default Value:
{:.param}






* &ldquo;100%&rdquo;








Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//To set width API value during initialization  
        $("#innerSplitter").ejSplitter({width: 600} );
</script>{% endhighlight %}





## Methods








### addItem<span class="signature">(content, property, index)</span>
{:#methods:additem}








To add the new pane to splitter control.

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
content{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">content of pane.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
property{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">pane properties.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
index{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">index of pane.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.addItem("New pane 0",{ paneSize:20, minSize:20, maxSize:100},0);
</script>{% endhighlight %}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("addItem","New pane 0",{ paneSize:20, minSize:20, maxSize:100},0);
</script>{% endhighlight %}







### collapse<span class="signature">()</span>
{:#methods:collapse}








To collapse the splitter control pane.





Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.collapse(); // collpase the splitter control pane.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// collpase the splitter control
$("#innerSplitter").ejSplitter("collpase");
</script>{% endhighlight %}







### expand<span class="signature">()</span>
{:#methods:expand}








To expand the splitter control pane.





Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.expand(); // expand the splitter control pane.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("expand");
</script>{% endhighlight %}







### refresh<span class="signature">()</span>
{:#methods:refresh}








To refresh the splitter control pane resizing.





Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.refresh(); // refresh the splitter control pane resizing.
</script>{% endhighlight %}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// refresh the splitter control
$("#innerSplitter").ejSplitter("refresh");
</script>{% endhighlight %}







### removeItem<span class="signature">(index)</span>
{:#methods:removeitem}








To remove the new pane from the splitter control.

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
<td class="description last">index of pane.</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// Create splitter control
var splitterObj = $("#innerSplitter").data("ejSplitter");
splitterObj.removeItem(0); 
</script>{% endhighlight %}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div>
<script>
$("#innerSplitter").ejSplitter();
// expand the splitter control
$("#innerSplitter").ejSplitter("removeItem",0);
</script>{% endhighlight %}





## Events








### beforeExpandCollapse
{:#events:beforeexpandcollapse}








Fires when before expand collapse in splitter control.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from splitter control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
collapsed{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
expanded{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
splitbarIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//beforeExpandCollapse event for splitter control
$("#innerSplitter").ejSplitter({
   beforeExpandCollapse: function (args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








Fires when splitter control pane has been created.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from splitter control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//create event for splitter control
$("#innerSplitter").ejSplitter({
   create: function (args) {}
});
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires when splitter control pane has been destroyed.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from splitter control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//destroy event for splitter control
$("#innerSplitter").ejSplitter({
   destroy: function (args) {}
});
</script>{% endhighlight %}







### expandCollapse
{:#events:expandcollapse}








Fires when expandCollapse in splitter control pane.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from splitter control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
collapsed{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
expanded{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
splitbarIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//expandCollapse event for splitter control
$("#innerSplitter").ejSplitter({
   expandCollapse: function (args) {}
});
</script>{% endhighlight %}







### resize
{:#events:resize}








Fires when resize in splitter control pane.

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
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from splitter control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
collapsed{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns collapsed pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
expanded{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns expanded pane details.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the splitter model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
splitbarIndex{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the current split bar index.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="innerSplitter">
<div>
<div class="cont">Pane 1 </div>
</div>
<div>
<div class="cont">Pane 2 </div>
</div>
</div> 
<script>
//resize event for splitter control
$("#innerSplitter").ejSplitter({
   resize: function (args) {}
});
</script>{% endhighlight %}




