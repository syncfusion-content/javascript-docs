---
layout: post
title: Grouping in AutoComplete widget for Essential JS
description: How to Group the suggestion list items
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
---

# Grouping

The suggestion list items can be grouped by providing a header for each set of items. The grouping will be defined based on the [groupBy](https://help.syncfusion.com/api/js/ejautocomplete#members:fields-groupBy) API in fields object.

Here the category field is mapped with groupBy field.

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
        /* Local Data */
        var countries = [
                { text: "Australia", category: "A" }, { text: "Antarctica", category: "A" },
                { text: "Bangladesh", category: "B" }, { text: "Belgium", category: "B" },
                { text: "Canada", category: "C" }, { text: "China", category: "C" },
                { text: "Denmark", category: "D" }, { text: "Dominica", category: "D" },
                { text: "Europe", category: "E" }, { text: "Egypt", category: "E" },
                { text: "India", category: "I" }, { text: "Indonesia", category: "I" },
                { text: "France", category: "F" }, { text: "Finland", category: "F" },
                { text: "Germany", category: "G" }, { text: "Greece", category: "G" },
                { text: "Japan", category: "J" }, { text: "Jordan", category: "J" },
                { text: "Madagascar", category: "M" }, { text: "Midway Islands", category: "M" },
                { text: "Nepal", category: "N" }, { text: "Netherlands", category: "N" },
                { text: "Qatar", category: "Q" }, { text: "Romania", category: "R" },
                { text: "Scotland", category: "S" }, { text: "Tibet", category: "T" },
                { text: "Zambia", category: "Z" }, { text: "Zimbabwe", category: "Z" }
        ];
        
        $('#autocomplete').ejAutocomplete({ dataSource: countries, filterType: ej.filterType.Contains, fields: { text: "text", groupBy: "category" } });
        
        </script>



{% endhighlight %}

![AutoComplete-Grouping](grouping_images\grouping_img1.png)

