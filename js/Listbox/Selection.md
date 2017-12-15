---
layout: post
title: Selection
description: selection
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Selection

The ListBox widget allows you to highlight the selected item. It allows multiple selection also. 


## Selection on initialize

By default, the ListBox widget allows single item selection. We can select specific item during initialization of the ListBox widget using the [selectedIndex](https://help.syncfusion.com/api/js/ejlistbox#members:selectedindex) API. 

{% tabs %}
{% highlight html %}

<div>
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
        </ul>
    </div>

{% endhighlight %}

{% highlight javascript %}


        jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    selectedIndex: 2
                });
        });



{% endhighlight %}
{% endtabs %}

![](Selection_images\Selection_img1.png)

## Multiple selection

Multiple selection can be enabled using [allowMultiSelection](https://help.syncfusion.com/api/js/ejlistbox#members:allowmultiselection) property. You can select multiple list items using <kbd>“Ctrl”</kbd> and <kbd>“Shift”</kbd> keys.

{% seealso %} [Keyboard Interaction](https://help.syncfusion.com/js/listbox/keyboard-interaction). {% endseealso %}

{% highlight javascript %}


          jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    allowMultiSelection: true
                });
        });



{% endhighlight %}

![](Selection_images\Selection_img2.png)

## Checkbox

The ListBox widget allows selection through checkbox. It can be enabled using [showCheckbox](https://help.syncfusion.com/api/js/ejlistbox#members:showcheckbox) API.

The specified items can be checked on initialize through [checkedIndices](https://help.syncfusion.com/api/js/ejlistbox#members:checkedindices) property. 

{% seealso %} [checkedIndices](https://help.syncfusion.com/api/js/ejlistbox#members:checkedindices). {% endseealso %}

{% highlight javascript %}


        jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    showCheckbox: true,
                    checkedIndices: [1, 2]
                });
        });



{% endhighlight %}



![](Selection_images\Selection_img3.png)
