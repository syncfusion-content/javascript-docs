---
layout: post
title: Methods and Events
description: methods and events in treemap
platform: js
control: TreeMap
documentation: ug
api: /api/js/ejtreemap
---

# Methods and Events

## Method

## refresh()

[`refresh()`](../api/ejtreemap#methods:refresh) method is used to reload the treemap with updated values.

#### Returns: void

{% highlight js %}

//refresh method for treemap
   $("#container").ejTreeMap("refresh");

{% endhighlight %}

## Events

## treeMapItemSelected

[`treeMapItemSelected`](../api/ejtreemap#events:treeMapItemSelected) event will trigger when treemap item is selected. 

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns selected treeMapItem object.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}

//treemap item selected event for treemap
  $("#container").ejTreeMap({
   treeMapItemSelected: function () {}
  });

{% endhighlight %}

## drillStarted

[`drillStarted`](../api/ejtreemap#events:drillStarted) event will fire, when the drilldown action is started in the treemap control.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns selected drilled treeMap object.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}
 
//drillStarted event for treemap
  $("#container").ejTreeMap({
   drillStarted: function () {}
  });

{% endhighlight %}

## drillDownItemSelected

If the treemap drilldown item is selected, then [`drillDownItemSelected`](../api/ejtreemap#events:drillDownItemSelected) event will fire.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns selected drilldown treeMap object.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}
 
//drillDownItemSelected event for treemap
  $("#container").ejTreeMap({
   drillDownItemSelected: function () {}
  });

{% endhighlight %}

## headerTemplateRendering

[`headerTemplateRendering`](../api/ejtreemap#events:headerTemplateRendering) event will fire before rendering the treemap drilldown header template.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns drilldown header.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}
 
//headerTemplateRendering event for treemap
  $("#container").ejTreeMap({
   headerTemplateRendering: function () {}
  });

{% endhighlight %}

## refreshed

[`refreshed`](../api/ejtreemap#events:refreshed) event will trigger after refreshing the treemap control with updated values.

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
            <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Refresh and load the treemap.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}
 
//refreshed event for treemap
  $("#container").ejTreeMap({
   refreshed: function () {}
  });

{% endhighlight %}

## treeMapGroupSelected

[`treeMapGroupSelected`](../api/ejtreemap#events:treeMapGroupSelected) event will fired when the group selection is performed on treemap items.

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
           <td class="name">{% highlight html %}originalEvent{% endhighlight %}</td>
            <td class="type"><span class="param-type">object</span></td>
            <td class="description last">Returns the  selected group of treeMapItems as  object.</td>
        </tr>
    </tbody>
</table>

{% highlight js %}
 
//treeMapGroupSelected event for treemap
  $("#container").ejTreeMap({
   treeMapGroupSelected: function () {}
  });

{% endhighlight %}