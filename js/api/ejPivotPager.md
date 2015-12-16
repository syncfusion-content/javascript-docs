---
layout: post
title: ejPivotPager
documentation: API
platform: js
keywords: ejPivotPager, API, Essential JS PivotPager
metaname: 
metacontent: 
---

# PivotPager

Custom Design for Html Pivot Pager control.


#### Syntax

{% highlight js %}

$(element).ejPivotPager()

{% endhighlight %}



#### Example

{% highlight html %}
 
<div id="PivotPager"></div> 
 
<script>
// Create Pivot Pager
$("#PivotPager").ejPivotPager(...);     
</script>

{% endhighlight %}


#### Requires

* module:jquery-1.10.2.min.js
* module:jquery.easing.1.3.min.js
* module:ej.core.js
* module:ej.data.js
* module:ej.touch.js
* module:ej.waitingpopup.js
* module:ej.pivotpager.js
* module:ej.pivotgrid


## Members


### categoricalCurrentPage `number`
{:#members:categoricalcurrentpage}

Contains the current page number in categorical axis.


#### Default Value

* 1


#### Example

{% highlight html %}
 
//To set categoricalCurrentPage API value during initialization  
$("#PivotPager").ejPivotPager({  categoricalCurrentPage: 1});

 {% endhighlight %}


{% highlight html %}
 
//Get or set the categoricalCurrentPage API, after initialization:
//Gets the categoricalCurrentPage value  
$("#PivotPager").ejPivotPager("option", "categoricalCurrentPage");
                  
//Sets the categoricalCurrentPage value 
$("#PivotPager").ejPivotPager("option", "categoricalCurrentPage", 2 ); 

{% endhighlight %}



### categoricalPageCount `number`
{:#members:categoricalpagecount}

Contains the total page count in categorical axis.


#### Default Value

* 1


#### Example

{% highlight html %}
 
//To set categPageCount API value during initialization  
$("#PivotPager").ejPivotPager({  categPageCount: 1});

 {% endhighlight %}


{% highlight html %}
 
//Get or set the categPageCount API, after initialization:
//Gets the categPageCount value  
$("#PivotPager").ejPivotPager("option", "categPageCount");
                  
//Sets the categPageCount value 
$("#PivotPager").ejPivotPager("option", "categPageCount", 2 ); 

{% endhighlight %}



### locale `string`
{:#members:locale}

Sets the localized language for the control.


#### Default Value

* 1


#### Example

{% highlight html %}
 
//To set localization API value during initialization  
$("#PivotPager").ejPivotPager({  locale: "en-US"});

{% endhighlight %}


{% highlight html %}
 
//Get or set the localization API, after initialization:
//Gets the localization value  
$("#PivotPager").ejPivotPager("option", "locale");
                  
//Sets the localization value 
$("#PivotPager").ejPivotPager("option", "locale", "fr-FR" ); 

{% endhighlight %}



### mode `enum`
{:#members:mode}

Sets the pager mode for the Pivot pager.


#### Default Value

* ej.PivotPager.Mode.Both



#### Example

{% highlight html %}
 
//To set pagerMode API value during initialization  
$("#PivotPager").ejPivotPager({  mode: ej.PivotPager.Mode.Series});

{% endhighlight %}


{% highlight html %}
 
//Get or set the pagerMode API, after initialization:
//Gets the pagerMode value  
$("#PivotPager").ejPivotPager("option", "mode");
                    
//Sets the pagerMode value 
$("#PivotPager").ejPivotPager("option", "mode", ej.PivotPager.Mode.Categorical ); 

{% endhighlight %}



### seriesCurrentPage `number`
{:#members:seriescurrentpage}

Contains the current page number in series axis.



#### Default Value

* 1


#### Example

{% highlight html %}
 
//To set seriesCurrentPage API value during initialization  
$("#PivotPager").ejPivotPager({  seriesCurrentPage: 1}); 

{% endhighlight %}


{% highlight html %}
 
//Get or set the seriesCurrentPage API, after initialization:
//Gets the seriesCurrentPage value  
$("#PivotPager").ejPivotPager("option", "seriesCurrentPage");
                       
//Sets the seriesCurrentPage value 
$("#PivotPager").ejPivotPager("option", "seriesCurrentPage", 2 ); 

{% endhighlight %}



### seriesPageCount `number`
{:#members:seriespagecount}

Contains the total page count in series axis.


#### Default Value

* 1


#### Example

{% highlight html %}
 
//To set seriesPageCount API value during initialization  
$("#PivotPager").ejPivotPager({  seriesPageCount: 1});

{% endhighlight %}


{% highlight html %}
 
//Get or set the seriesPageCount API, after initialization:
//Gets the seriesPageCount value  
$("#PivotPager").ejPivotPager("option", "seriesPageCount");
                 
//Sets the seriesPageCount value 
$("#PivotPager").ejPivotPager("option", "seriesPageCount", 2 ); 

{% endhighlight %}


### targetControlID `string`
{:#members:targetcontrolid}

Contains the id of the target element for which paging is enabled.


#### Default Value

* ""

#### Example

{% highlight html %}
 
//To set targetControlID API value during initialization  
$("#PivotPager").ejPivotPager({  targetControlID: "PivotGrid"});

{% endhighlight %}


{% highlight html %}
 
//Get or set the targetControlID API, after initialization:
//Gets the targetControlID value  
$("#PivotPager").ejPivotPager("option", "targetControlID");
                 
//Sets the targetControlID value 
$("#PivotPager").ejPivotPager("option", "targetControlID",  "PivotGrid1" ); 

{% endhighlight %}



## Methods

### initPagerProperties()
{:#methods:initpagerproperties}

This function initializes the page counts and page numbers of the PivotPager.


#### Example

{% highlight html %}
 
<div id="PivotPager"></div> 
 
<script>
// Initializing page count and numbers.
$('#PivotPager').ejPivotPager({
      url: "Pager.svc",
});
var pagerObj = $("#PivotPager").data("ejPivotPager");
pagerObj.initPagerProperties(10, {CategorialPageSize: 1, SeriesPageSize: 1, CategorialCurrentPage: 3, SeriesCurrentPage: 4});
// Initializing page count and numbers.
</script>

{% endhighlight %}



### unwireEvents()
{:#methods:unwireevents}

This function is invoked to unwire the events registered for UI interaction.


#### Example

{% highlight html %}
 
<div id="PivotPager"></div> 
 
<script>
// Unwiring events from Pivot Pager control.
$('#PivotPager').ejPivotPager({
      url: "Pager.svc",
});
var pagerObj = $("#PivotPager").data("ejPivotPager");
pagerObj.unwireEvents();
// Unwiring events from Pivot Pager.
</script>

{% endhighlight %}




### wireEvents()
{:#methods:wireevents}

This function is invoked to wire the events for UI interaction.


#### Example

{% highlight html %}
 
<div id="PivotPager"></div> 
 
<script>
// Wiring events to Pivot Pager control.
$('#PivotPager').ejPivotPager({
      url: "Pager.svc",
});
var pagerObj = $("#PivotPager").data("ejPivotPager");
pagerObj.wireEvents();
// Wiring events with Pivot Pager.
</script>

{% endhighlight %}


