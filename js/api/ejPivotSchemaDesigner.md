---
layout: post
title: ejPivotSchemaDesigner
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Pivot Schema Designer control.





$(element).ejPivotSchemaDesigner<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
 
<div id="PivotSchemaDesigner"> </div> 
 
<script>
// Create Pivot Schema Designer
$("#PivotSchemaDesigner").ejPivotSchemaDesigner(...);   
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.common.all

* module:ej.tools.js


## Members




### cssClass<span class="type-signature type string">String</span>
{:#members:cssclass}




Sets the CSS name for custom operation.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
//To set the CSS name during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({cssClass: "gradient-lime"}); {% endhighlight %}


{% highlight html %}
 
//Get or set css class for initialization:
// Gets the css name.           
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "cssClass");                  
// Sets the css class to PivotSchemaDesigner
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "cssClass",  "gradient-lime" );{% endhighlight %}




### filters<span class="type-signature type array">Array</span>
{:#members:filters}




Allows the user to set the filter list.


Default Value:
{:.param}



* new Array()




Example
{:.example}


{% highlight html %}
 
//To set the filter list during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({filterList: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the filter list, after initialization:
//Gets the filter list
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "filterList");
                            
//Sets the filter list
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "filterList","true"); {% endhighlight %}




### height<span class="type-signature type string">String</span>
{:#members:height}




Sets the height for PivotSchemaDesigner.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
//To set the height during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({height: "630px"});     {% endhighlight %}


{% highlight html %}
 
//Get or set height for initialization:
// Gets the height.             
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "height");                    
// Sets the height to PivotSchemaDesigner
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "height",  "630px" ); {% endhighlight %}




### pivotCalculations<span class="type-signature type array">Array</span>
{:#members:pivotcalculations}




Allows the user to set Pivot Calculation List.


Default Value:
{:.param}



* new Array()




Example
{:.example}


{% highlight html %}
 
//To set the pivot calculation cist during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: });{% endhighlight %}


{% highlight html %}
 
//Get or set the pivot calculation list, after initialization:
//Gets the cell context state
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
                   
//Sets the pivot calculation list value
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true");{% endhighlight %}




### pivotColumns<span class="type-signature type array">Array</span>
{:#members:pivotcolumns}




Allows the user to set the pivot column list.


Default Value:
{:.param}



* new Array()




Example
{:.example}


{% highlight html %}
 
//To set the pivot column list during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the pivot column list, after initialization:
//Gets the pivot column list
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
                   
//Sets the pivot column list value
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true");{% endhighlight %}




### pivotControl<span class="type-signature type object">object</span>
{:#members:pivotcontrol}




Sets the pivot control bounds with the Pivot Schema Designer.


Default Value:
{:.param}



* null




Example
{:.example}


{% highlight html %}
 
//To set the pivot control during initialization  
var control = $("#PivotSchemaDesigner").data("ejPivotSchemaDesigner");
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotControl: control});{% endhighlight %}


{% highlight html %}
 
//Get or set the pivot control, after initialization:
//Gets the pivot control value
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotControl");
                  
//Sets the pivot control
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotControl", control);{% endhighlight %}




### pivotRows<span class="type-signature type array">Array</span>
{:#members:pivotrows}




Allows the user to set the pivot row list.


Default Value:
{:.param}



* new Array()




Example
{:.example}


{% highlight html %}
 
//To set the pivot row list during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotRowList: true});{% endhighlight %}


{% highlight html %}
 
//Get or set the pivot row list, after initialization:
//Gets the pivot row list
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotRowList");
          
//Sets the pivot row list
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotRowList","true"); {% endhighlight %}




### pivotTableFields<span class="type-signature type array">Array</span>
{:#members:pivottablefields}




Allows the user to Pivot Table Field List to Pivot Schema Designer.


Default Value:
{:.param}



* new Array()




Example
{:.example}


{% highlight html %}
 
//To set the Pivot Table Field List during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({pivotTableFieldList: });{% endhighlight %}


{% highlight html %}
 
//Get or set the Pivot Table Field List, after initialization:
//Gets the virtual calling state
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList");
           
//Sets the Pivot Table Field List 
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "pivotTableFieldList","true"); {% endhighlight %}




### url<span class="type-signature type string">String</span>
{:#members:url}




Connects the service using the specified URL for any server updates. See url


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
//To set service url during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({url: "/wcf/PivotService.svc"});{% endhighlight %}


{% highlight html %}
 
//Get or set the size API, after initialization:
//Gets the url value  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option","url");
   
//Sets the url value 
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option","url", "/wcf/PivotService.svc" ); {% endhighlight %}




### width<span class="type-signature type string">String</span>
{:#members:width}




Sets the width for PivotSchemaDesigner.


Default Value:
{:.param}



* ""




Example
{:.example}


{% highlight html %}
 
//To set the width during initialization  
$("#PivotSchemaDesigner").ejPivotSchemaDesigner({width: "415px"}); {% endhighlight %}


{% highlight html %}
 
//Get or set width for initialization:
// Gets the width.              
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "width");                     
// Sets the width to PivotSchemaDesigner
$("#PivotSchemaDesigner").ejPivotSchemaDesigner("option", "width",  "415px" ); {% endhighlight %}



## Methods




### doAjaxPost<span class="signature">()</span>
{:#methods:doajaxpost}




Perform an asynchronous HTTP (Ajax) request.



Example
{:.example}


{% highlight html %}
 
<div id="PivotSchemaDesigner"></div> 
 
<script>
// Create PivotSchemaDesigner
$('#PivotSchemaDesigner').ejPivotSchemaDesigner({
      url: "PivotGridService.svc",
  });
var gridObj = $("#PivotSchemaDesigner").data("ejPivotSchemaDesigner");
gridObj.doAjaxPost("POST", "/PivotGridService.svc/Initialize", {"key", "Hello World"}, "_renderControlSuccess", null);
// Initiate an Ajax request.
</script>{% endhighlight %}



