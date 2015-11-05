---
layout: post
title: Selection
description: selection
platform: js
control: ListBox
documentation: ug
---

# Selection

The ListBox widget allows you to highlight the selected item. It allows multiple selection also. 


## Selection on initialize

By default, the ListBox widget allows single item selection. We can select specific item during initialization of the ListBox widget using the “selectedIndex” API. 

{% highlight js %}


        jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    selectedIndex: 2
                });
        });




{% endhighlight %}


## Multiple selection

Multiple selection can be enabled using “allowMultiSelection” property. You can select multiple list items using <kbd>“Ctrl”</kbd> and <kbd>“Shift”</kbd> keys.

{% seealso %} [Keyboard Interaction](http://help.syncfusion.com/js/listbox/accessibility#keyboard-interaction) {% endseealso %}

{% highlight js %}


          jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    allowMultiSelection: true
                });
        });



{% endhighlight %}

![MultiSelect Listbox](Selection_Images\multipleselection_img1.png)


## Checkbox

The ListBox widget allows selection through checkbox. It can be enabled using “showCheckbox” API.

The specified items can be checked on initialize through “checkedIndices” property. 

{% seealso %} [Checked Indices](http://helpjs.syncfusion.com/js/api/ejlistbox#members:checkedindices). {% endseealso %}

{% highlight js %}


        jQuery(function ($) {

            $("#listbox").ejListBox(
                {
                    showCheckbox: true,
                    checkedIndices: [1, 2]
                });
        });



{% endhighlight %}



![Checked Listbox](Selection_Images\checkbox_img1.png)
