---
layout: post
title: Destroy-Gantt-Contrl
description: Destroy Gantt Control
platform: js
control: Gantt
documentation: ug
---

# Destroy Gantt Control
Gantt control is composed with more sub-controls like TreeGrid, Splitter, Dialog etc. So while destroying the Gantt control we need to
remove all sub-control elements and unbind all events bound by this control. By using [`destroy`](/api/js/ejgantt#methods:destroy "destroy") public method, we can properly remove the Gantt control from DOM.

The following code example explains how to destroy Gantt control.

{% highlight javascript %}

    $("#gantt").ejGantt("destroy");

{% endhighlight %}

N> If you want to re-initialize Gantt control on same `div` element,
we need to perform destroy action before re-initialize the Gantt.




