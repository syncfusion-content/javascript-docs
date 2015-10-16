---
layout: post
title: Search-Customization
description: search customization
platform: js
control: AutoComplete
documentation: ug
---

# Search Customization

## HighlightSearch

**AutoComplete** widget allows you to highlight the search text in the AutoComplete suggestions list using the **highlightSearch** property. When this property is set to ‘**True**’, the suggestions list appear with the search text it contains is highlighted.

### Enabling highlightSearch option

The following steps explain how you can enable the **highlightSearch** property for an AutoComplete textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}



 Enable **highlightSearch** for AutoComplete control as follows.

{% highlight js %}

        // Here define CarList local data as per the previous the code block.
        
           $('#autocomplete').ejAutocomplete({
                width: 205,
                dataSource: carList,
                filterType: "contains",
                highlightSearch:true
            });

{% endhighlight %}



The following image is the output for **AutoComplete** when **highlightSearch** is set to ‘**True**’.

![](/js/Autocomplete/Search-Customization_images/Search-Customization_img1.png)

## Case-sensitive Search

**AutoComplete** allows you to enable case sensitivity to filter the suggest list items based on the entered text casing. This property enables strict filtering of list items based on entered text. To enable it, set **caseSensitiveSearch** value to ‘**True**’. It is **False,** by default.

### Configure case sensitivity for AutoComplete

The following steps explain you how to enable the **caseSensitiveSearch** property for an **AutoComplete** textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure **AutoComplete** widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}

 Enable **caseSensitiveSearch** for AutoComplete control as follows.

{% highlight js %}


        // Here define CarList local data as per the previous the code block.
        $('#autocomplete').ejAutocomplete({
            width: 205,
            dataSource: carList,
            filterType: "startswith",
            caseSensitiveSearch: true
        });

{% endhighlight %}





The following image is the output for **AutoComplete** when **caseSensitiveSearch** is set to ‘**True**’.

![](/js/Autocomplete/Search-Customization_images/Search-Customization_img2.png)

