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

[`treeMapItemSelected`](../api/ejtreemap#events:treemapitemselected) event will trigger when treemap item is selected. 

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

[`drillStarted`](../api/ejtreemap#events:drillstarted) event will fire, when the drilldown action is started in the treemap control.

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

If the treemap drilldown item is selected, then [`drillDownItemSelected`](../api/ejtreemap#events:drilldownitemselected) event will fire.

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

## itemRendering

[`itemRendering`](../api/ejtreemap#events:itemrendering) event will trigger while rendering each item in treemap.

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
            <td class="description last">Returns each leaf items in treemap</td>
        </tr>
    </tbody>
</table>

{% highlight js %}

//item rendering event for treemap
  $("#container").ejTreeMap({
   itemRendering: function () {}
  });

{% endhighlight %}

## legendItemRendering

[`legendItemRendering`](../api/ejtreemap#events:legenditemrendering) event will trigger while rendering each legend item in treemap.

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
            <td class="description last">Returns each legend item in treemap</td>
        </tr>
    </tbody>
</table>

{% highlight js %}

//legend item rendering event for treemap
  $("#container").ejTreeMap({
   legendItemRendering: function () {}
  });

{% endhighlight %}

## Click

[`click`](../api/ejtreemap#events:click) event will trigger while clicking an item in the treemap.


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
            <td class="description last">Returns the clicked group of treeMapItems as  object.</td>
        </tr>
    </tbody>
</table>



{% highlight js %}
 
//Click event for tree map

 $("#container").ejTreeMap({

    click: function (args) {
              //Do something
    }
   
});

{% endhighlight %}


## doubleClick

[`doubleClick`](../api/ejtreemap#events:doubleclick) event will trigger while double clicking an item in the treemap.


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
            <td class="description last">Returns the  double clicked group of treeMapItems as  object.</td>
        </tr>
    </tbody>
</table>


{% highlight js %}
 
//DoubleClick event for tree map

 $("#container").ejTreeMap({

    doubleClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



## rightClick

[`rightClick`](../api/ejtreemap#events:rightclick) event will trigger while right clicking an item in the treemap.


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
            <td class="description last">Returns the right clicked group of treeMapItems as  object.</td>
        </tr>
    </tbody>
</table>


{% highlight js %}
 
//RightClick event for tree map

 $("#container").ejTreeMap({
    rightClick: function (args) {
              //Do something
    }
   
});

{% endhighlight %}



