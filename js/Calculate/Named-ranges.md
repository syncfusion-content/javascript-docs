---
layout: post
title: Named ranges of Calculate for Syncfusion Essential JS
description: named ranges
platform: JS
control: Calculate
documentation: ug
api : /api/js/ejcalculate
---

# Named Ranges

A cell, range of cells, formulas, constants, or tables can be represented in a single name called Named range or defined name. This name is used to identify the purpose of cell references easier. For example, the name can be defined for the cell reference `A1` to `FIRSTCELL`.

## Protocols of Names

  The following are the rules to define a name,

  * The name starts with a letter as it is a text string. UnderScore `_` can also be used. And, it must not be a single letter.
  * The name must not equal to Cell references `Eg. A1`
  * No space must be included and the name cannot be empty string.
  * The names will be case-insensitive.
  
## Adding Names

A name can be added for a cell or range of cells using `addNamedRange` method. 

{% highlight javascript %}

calcObj.addNamedRange($("#newName").val(), cell)

{% endhighlight %}



Whereas, the `cell` represents the cell reference like `A1`.

## Managing Names

The added names can be accessed in the formula instead of the particular cell references or range of cells. For example, for the formula `=SUM(GROUPCELLS)`, the `GROUPCELLS` represents the range of cells `A1:A10`.



The names are maintained in a collection `NamedRange`. Thus, the name can be changed or replaced using this collection.



## Removing Names

A name can be removed from a cell or range of cells using `removeNamedRange` method. 

{% highlight javascript %}

calcObj.removeNamedRange($("#newName").val(), cell)

{% endhighlight %}



Whereas, the `cell` represents the cell reference like `A1`.

