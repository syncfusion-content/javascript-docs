---
layout: post
title: Grouping
description: grouping
platform: js
control: ListBox
documentation: ug
api: /api/js/ejlistbox
---

# Grouping

ListBox items can be grouped by providing a heading (header) for each set of items. It can be done in two ways.

1. Using span tag

2. Data binding


## Using span tag

The header for each group can be defined using the “span” element”. 

{% tabs %}
{% highlight html %}


<!--grouped listbox-->
<ul id="listbox">
  <!--header-->
  <span class="e-ghead">A</span>
  <li>Albania</li>
  <li>Argentina</li>
  <li>Algeria</li>
  <li>Angola</li>
  <li>Afghanistan</li>
  <!--header-->
  <span class="e-ghead">B</span>
  <li>Brazil</li>
  <li>Bahrain</li>
  <li>Burma</li>
  <li>Barbados</li>
  <li>Botswana</li>
  <li>Belarus</li>
  <li>Bolivia</li>
</ul>



{% endhighlight %}



{% highlight javascript %}


        jQuery(function ($) {
           $("#listbox").ejListBox();
        });



{% endhighlight %}
{% endtabs %}


![Alt text](Grouping_images\Grouping_img1.png)

## Data binding

The grouped ListBox can be also created via data binding which is explained below. The data items can be categorized by using a specific field in the ListBox widget.

{% seealso %} [Data Binding](https://help.syncfusion.com/js/listbox/databinding). {% endseealso %}

The grouping will be defined based on the [groupBy](https://help.syncfusion.com/api/js/ejlistbox#members:fields-groupBy) API in fields object.

{% highlight html %}

<ul id="listbox"></ul>
    <script type="text/javascript">
        jQuery(function ($) {
            //datasource for listbox
            //Here the category column is used to define the grouping
            var skillSet = [{ skill: "Bahrain", category: "B" },
                { skill: "Brazil", category: "B" },
                { skill: "Argentina", category: "A" },
                { skill: "Bangladesh", category: "B" },
                { skill: "Burma", category: "B" },
                { skill: "Afghanistan", category: "A" },
                { skill: "Antigua and Barbuda", category: "A" },
                { skill: "Barbados", category: "B" },
                { skill: "Botswana", category: "B" },
                { skill: "Albania", category: "A" },
                { skill: "Andorra", category: "A" },
                { skill: "Belarus", category: "B" },
                { skill: "Bolivia", category: "B" },
                { skill: "Algeria", category: "A" },
                { skill: "Angola", category: "A" }];
                
            $("#listbox").ejListBox({
                dataSource: skillSet,
                fields: {
                    text: "skill",
                    //based on this field, grouping will be defined
                    groupBy: "category"
                },
            });
        });
    </script>



{% endhighlight %}



![](Grouping_images\Grouping_img2.png)

I> Virtual scrolling is not supported with Grouping.