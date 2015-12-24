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

Support has been provided in PivotGrid to load and render large amount of data without any performance constraint through pager. The PivotPager widget is used to navigate between pages to view the paged information. 


#### Syntax

{% highlight js %}

$(element).ejPivotPager()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="PivotPager1"></div> 
 
<script>
//Create PivotPager
$("#PivotPager1").ejPivotPager(...);     
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

**Default Value:** 1

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ categoricalCurrentPage: 1 });

{% endhighlight %}

### categoricalPageCount `number`
{:#members:categoricalpagecount}

Contains the total page count in categorical axis.

**Default Value:** 1

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ categPageCount: 1 });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

**Default Value:** "en-US"

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ locale: "en-US" });

{% endhighlight %}

### mode `enum`
{:#members:mode}

Sets the pager mode (Only Categorical Pager/Only Series Pager/Both) for the PivotPager. 

**Default Value:** ej.PivotPager.Mode.Both

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ mode: ej.PivotPager.Mode.Series });

{% endhighlight %}

### seriesCurrentPage `number`
{:#members:seriescurrentpage}

Contains the current page number in series axis.

**Default Value:** 1

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ seriesCurrentPage: 1 }); 

{% endhighlight %}

### seriesPageCount `number`
{:#members:seriespagecount}

Contains the total page count in series axis.

**Default Value:** 1

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ seriesPageCount: 1 });

{% endhighlight %}

### targetControlID `string`
{:#members:targetcontrolid}

Contains the ID of the target element for which paging needs to be done.

**Default Value:** “”

**Example:**

{% highlight html %}
 
$("#PivotPager1").ejPivotPager({ targetControlID: "PivotGrid1" });

{% endhighlight %}


## Methods

### initPagerProperties()
{:#methods:initpagerproperties}

This function initializes the page counts and page numbers for the PivotPager.

**Example:**

{% highlight html %}
 
<div id="PivotPager1"></div> 
 
<script>
var pagerObj = $("#PivotPager1").data("ejPivotPager");
pagerObj.initPagerProperties(150, {CategorialPageSize: 10, SeriesPageSize: 10, CategorialCurrentPage: 1, SeriesCurrentPage: 1});
</script>

{% endhighlight %}