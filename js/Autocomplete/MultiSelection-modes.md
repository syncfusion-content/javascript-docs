---
layout: post
title: MultiSelection-modes
description: multiselection modes
platform: js
control: AutoComplete
documentation: ug
---

# MultiSelection modes

**AutoComplete** widget allows you to select multiple values from the suggestions list using the **multiSelectMode** property. Multiple values are selected when multiSelectMode value is set to VisualMode or Delimiter. 

**Delimiter mode** separates multiple items using a separator character defined. When the delimiter mode is set, you can define the delimiter character using delimiterChar. It takes a single character and it is a symbol. 

**Visual mode** selects multiple items by enclosing the item in a rounded rectangle with a close icon to remove item from the selection.

## Configuring MultiSelection Mode

The following steps explain the configuration of the **multiSelectMode** for an **AutoComplete** textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget.

{% highlight html %}

<div style="margin-right: 20px;">
    <span class="txt">Using Delimiter</span>
    <input type="text" id="delimit" />
</div>

<div style="margin-right: 20px;">
    <span class="txt">Using VisualMode</span>
    <input type="text" id="visualmode" />
</div>

<div>
    <span class="txt">Single selection</span>
    <input type="text" id="none" />
</div>


{% endhighlight %}


 Configure **multiSelectMode** type for **AutoComplete** control as follows.

{% highlight js %}


    $("#delimit").ejAutocomplete({
        width: 225,
        multiSelectMode: ej.MultiSelectMode.Delimiter,
        delimiterChar: ";",
        dataSource: carList
    });
    $("#none").ejAutocomplete({
        width: 225,
        multiSelectMode: ej.MultiSelectMode.None,
        dataSource: carList
    });
    $("#visualmode").ejAutocomplete({
        width: 225,
        multiSelectMode: ej.MultiSelectMode.VisualMode,
        dataSource: carList
    });


{% endhighlight %}



The following image is the output for **AutoComplete** control with configured multiple selection.

![](/js/Autocomplete/MultiSelection-modes_images/MultiSelection-modes_img1.png)

