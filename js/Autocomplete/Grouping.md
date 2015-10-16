---
layout: post
title: Grouping
description: grouping
platform: js
control: AutoComplete
documentation: ug
---

# Grouping

**AutoComplete** widget provides **Grouping** support for the suggestions list based on the category specified in the dataSource. By default **allowGrouping** is set to ‘**False**’. To enable Grouping for your AutoComplete widget, set the value to ‘**True**’.

## Configuring Grouping for AutoComplete

The following steps explain you how to configure **Grouping** for an AutoComplete textbox.

 In the **HTML** page, add an **&lt;input&gt;** element to configure AutoComplete widget.

{% highlight html %}

<input type="text" id="autocomplete" />


{% endhighlight %}


 Define **dataSource** elements with category field to group them. The category field in dataSource is used for Grouping conditions.

{% highlight js %}

     var countries = [
        { text: "Austria", category: "A" },
        { text: "Australia", category: "A" }, { text: "Lebanon", category: "L" },
        { text: "Leichenstein", category: "L" }, { text: "Malaysia", category: "M" },
        { text: "Mexico", category: "M" }, { text: "Netherlands", category: "N" },
        { text: "New Zealand", category: "N" }, { text: "Nigeria", category: "N" },
        { text: "Oman", category: "O" }, { text: "Philippines", category: "P" },
        { text: "Poland", category: "P" }, { text: "Portugal", category: "P" },
        { text: "Qatar", category: "Q" }, { text: "Romania", category: "R" },
        { text: "Russia", category: "R" }, { text: "Sweden", category: "S" },
        { text: "United States", category: "U" }, { text: "Uruguay", category: "U" },
        {text:"Vatican City",category: "V" },{text: "Western Sahara",category: "W" },
        { text: "Yemen", category: "Y" }, { text: "Zimbabwe", category: "Z" }
     ];


{% endhighlight %}

 Configure Grouping for AutoComplete control as follows.

{% highlight js %}

    $('#autocomplete').ejAutocomplete({
        dataSource: countries,
        filterType: ej.filterType.Contains,
        minCharacter: 2, // starts search only after entering 2 texts
        width: 205,
        allowGrouping: true,
        highlightSearch: true,
        popupHeight: "200px"
    });

{% endhighlight %}


The following image is the output for AutoComplete control that provides Grouping.

![](/js/Autocomplete/Grouping_images/Grouping_img1.png)

