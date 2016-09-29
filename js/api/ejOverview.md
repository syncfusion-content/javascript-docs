---
layout: post
title: ejOverview
description: API reference for ejOverview
documentation: API
platform: js
keywords: overview, ejOverview, overview api, syncfusion
---

# ejOverview
<ts root="datavisualization" />

Overview control allows you to see a preview or an overall view of the entire content of a Diagram. This helps you to look at the overall picture of a large Diagram and also to navigate, pan, or zoom, on a particular position of the page.

#### Syntax
$(element).ejOverview()

#### Example

{% highlight html %}
 
<div id="overview"></div>
<script>
//Create overview
$("#overview").ejOverview();
</script>

{% endhighlight %}

#### Requires

* module:jQuery.js
* module:ej.common.all
* module:ej.widgets.all
* module:jquery.easing.js
* module:jquery.globalize.js
* module:jsrender.js
* module:jquery.validate.js
* module:jquery.validate.unobtrusive.js

## Members
 
### sourceID `String`
{:#members:sourceID}

The sourceId property of overview should be set with the corresponding Diagram ID for you need the overall view.

#### Default Value

* null

#### Example

{% highlight html %}

<div id="overview"></div>
<script>
$("#overview").ejOverview({ sourceID: "diagram" });
</script>

{% endhighlight %}

### height `Number`
{:#members:height}

Defines the height of the overview

#### Default Value

* 400

#### Example

{% highlight html %}

<div id="overview"></div>
<script>
$("#overview").ejOverview( { height:300 } );
</script>

{% endhighlight %}

### width `Number`
{:#members:width}

Defines the width of the overview

#### Default Value

* 250

#### Example

{% highlight html %}

<div id="overview"></div>
<script>
$("#overview").ejOverview({width:300});
</script>

{% endhighlight %}
