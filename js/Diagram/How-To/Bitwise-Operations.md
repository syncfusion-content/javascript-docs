---
layout: post
title: Bitwise-Operations
description: bitwise operations
platform: js
control: Diagram
documentation: ug
---

# Bitwise Operations

**Bitwise Operations** are used to manipulate the flagged enumerations \[enum\]. In this section, Bitwise Operations are illustrated using Graph Constraints. The same is applicable while working with Node Constraints, Connector Constraints or Port Constraints.

**Add Operation**

You can **add** or **enable** multiple values at a time by using **Bitwise** ‘\|’ (OR) **operator**.

{% highlight js %}

node.constraints = ej.datavisualization.Diagram.NodeConstraints.Select | ej.datavisualization.Diagram.NodeConstraints.Rotate;

{% endhighlight %}

In the above example, you can do both selection and rotation.

**Remove Operation**

You can **remove** or **disable** values by using **Bitwise** ‘&\~’ (XOR) **operator**.

{% highlight js %}

node.constraints = node.constraints &~ (ej.datavisualization.Diagram.NodeConstraints.Rotate);

{% endhighlight %}

In the above example, **Rotation** is disabled but other constraints are enabled.

**Check Operation** 

You can check any values using **Bitwise** ‘&’ (AND) **operator**.

{% highlight js %}

if ((node.constraints & (ej.datavisualization.Diagram.NodeConstraints.Rotate)) == (ej.datavisualization.Diagram.NodeConstraints.Rotate));

{% endhighlight %}

In the above example, you can check whether the rotate constraints are enabled in a Node. When Node constraints have rotate constraints, the expression returns a rotate constraint.
