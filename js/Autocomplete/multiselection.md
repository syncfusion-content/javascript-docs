---
layout: post
title: Multi Selection in AutoComplete widget for Essential JS
description: How to pick multiple values from the AutoComplete suggestion items.
platform: js
control: AutoComplete
documentation: ug
keywords: ejautocomplete, autocomplete widget, autocomplete ui, js autocomplete, jquery autocomplete, web autocomplete, ej autocomplete, essential javascript autocomplete,
api: /api/js/ejautocomplete
---

# MultiSelection

The AutoComplete widget helps you to select multiple values from the suggestion list using the [multiSelectMode](https://help.syncfusion.com/api/js/ejautocomplete#members:multiselectmode) property.

There are two types of multi-selection mode.

1. VisualMode – Selection values are displayed in separate box with close like button.

2. Delimiter – Selection values are separated using the delimiter character which can be specified using [delimiterChar](https://help.syncfusion.com/api/js/ejautocomplete#members:delimiterchar) API. 

{% highlight html %}

        
        <input type="text" id="autocomplete" />
        
        <script type="text/javascript">
        
                /* Local Data */
                var carList = [
                        "Audi S6", "Audi S6", "Austin-Healey", "Alfa Romeo", "Aston Martin",
                        "BMW 7 ", "Bentley Mulsanne", "Bugatti Veyron",
                        "Chevrolet Camaro", "Cadillac ",
                        "Duesenberg J ", "Dodge Sprinter",
                        "Elantra", "Excavator",
                        "Ford Boss 302", "Ferrari 360", "Ford Thunderbird ",
                        "GAZ Siber"];
        
                $('#autocomplete').ejAutocomplete({ dataSource: carList, width: 205, multiSelectMode:ej.MultiSelectMode.VisualMode });
        
        </script>
        


{% endhighlight %}



![AutoComplete-Multiselection](multiselection_images\multiselection_img1.png)

