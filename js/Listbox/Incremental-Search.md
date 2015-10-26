---
layout: post
title: Incremental-Search
description: incremental search
platform: js
control: ListBox
documentation: ug
---

## Incremental Search

The [Incremental search](https://en.wikipedia.org/wiki/Incremental_search) helps in finding the specific item in the ListBox,as the user types the text one or more possible matches for the text are found and the first matched item will be selected.It can be enabled in the ListBox widget using “enableIncrementalSearch” API. The search can be case sensitive or case insensitive.

{% highlight html %}

    <ul id="listbox">
        <li>Audi A4</li>
        <li>Audi A5</li>
        <li>Audi A6</li>
        <li>Audi A7</li>
        <li>Audi A8</li>
        <li>BMW 501</li>
        <li>BMW 502</li>
        <li>BMW 503</li>
        <li>Batch</li>
        <li>BMW 507</li>
        <li>BMW 3200</li>
        <li>Cut</li>
        <li>Copy</li>
        <li>Paste</li>
        <li>Add</li>
        <li>Delete</li>
        <li>D5ishCover</li>
        <li>Di5shCover</li>
        <li>Dis5hCover</li>
        <li>Dish5Cover</li>
        <li>DishC5over</li>
        <li>DishCo5ver</li>
        <li>DishCov5er</li>
        <li>DishCove5r</li>
        <li>Comments</li>
        <li>Links</li>
        <li>Clear Formatting</li>
    </ul>

    <script type="text/javascript">
        jQuery(function ($) {

            $("#listbox").ejListBox({
                enableIncrementalSearch: true,
                caseSensitiveSearch: true
            });
        });

    </script>

{% endhighlight %}



{% include image.html url="Incremental-Search_Images\incremental-search_img1.png" Caption="Before incremental search"%}

Press <kbd> tab </kbd> key to get ListBox focus and press <kbd>“A”</kbd> (enable caps lock or press <kbd>shift</kbd> +<kbd> “A”</kbd> since case sensitive search is enabled) to get the below output.

{% include image.html url="Incremental-Search_Images\incremental-search_img2.png" Caption="After incremental search"%}

__



