---
layout: post
title: Properties, Methods and Events of ejPivotPager Widget
documentation: API
platform: js
keywords: ejPivotPager, API, Essential JS PivotPager
metaname: 
metacontent: 
---

# PivotPager

PivotPager is a control used to render large amount of data without any performance constraint in PivotGrid and PivotClient. The PivotPager widget is used to navigate between pages to view the paged information. 


#### Syntax

{% highlight javascript %}

    $(element).ejPivotPager();
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

* module:jQuery-3.0.0.min.js
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

#### Default Value: 1

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ categoricalCurrentPage: 1 });
{% endhighlight %}

### categoricalPageCount `number`
{:#members:categoricalpagecount}

Contains the total page count in categorical axis.

#### Default Value: 1

**Example:**

{% highlight javascript %}
 
$("#PivotPager1").ejPivotPager({ categPageCount: 1 });

{% endhighlight %}

### locale `string`
{:#members:locale}

Allows the user to set the localized language for the widget.

#### Default Value: "en-US"

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ locale: "en-US" });
{% endhighlight %}

### mode `enum`
{:#members:mode}

<ts name = "ej.PivotPager.Mode"/>

Sets the pager mode (Only Categorical Pager/Only Series Pager/Both) for the PivotPager. 

#### Default Value: ej.PivotPager.Mode.Both

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">Both</td>
            <td class="description">To set both categorical and series pager for paging.</td>
        </tr>
        <tr>
            <td class="name">Categorical</td>
            <td class="description">To set only categorical pager for paging.</td>
        </tr>
        <tr>
            <td class="name">Series</td>
            <td class="description">To set only series pager for paging.</td>
        </tr>
    </tbody>
</table>

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ mode: ej.PivotPager.Mode.Series });
{% endhighlight %}

### seriesCurrentPage `number`
{:#members:seriescurrentpage}

Contains the current page number in series axis.

#### Default Value: 1

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ seriesCurrentPage: 1 });
{% endhighlight %}

### seriesPageCount `number`
{:#members:seriespagecount}

Contains the total page count in series axis.

#### Default Value: 1

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ seriesPageCount: 1 });
{% endhighlight %}

### targetControlID `string`
{:#members:targetcontrolid}

Contains the ID of the target element for which paging needs to be done.

#### Default Value: “”

**Example:**

{% highlight javascript %}
 
    $("#PivotPager1").ejPivotPager({ targetControlID: "PivotGrid1" });
{% endhighlight %}


## Methods

### initPagerProperties()
{:#methods:initpagerproperties}

This function initializes the page counts and page numbers for the PivotPager.

**Example:**

{% highlight javascript %}
 
    var pagerObj = $("#PivotPager1").data("ejPivotPager");
    pagerObj.initPagerProperties(150, { CategorialPageSize: 10, SeriesPageSize: 10, CategorialCurrentPage: 1, SeriesCurrentPage: 1});
{% endhighlight %}