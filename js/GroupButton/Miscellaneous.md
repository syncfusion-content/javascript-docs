---
layout: post
title: Miscellaneous | GroupButton | JavaScript | Syncfusion
description: miscellaneous
platform: js
control: GroupButton
documentation: ug
api: /api/js/ejgroupbutton
---

# Miscellaneous

## Show/Hide the items

Particular currently showing button items can be hidden. Also it provides the options to show the hidden button again. These functionalities can be achieved using **showItem** or **hideItem** method.

**Hide the Button item based on given index**

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.hideItem(1);

        </script>

{% endhighlight %}

**Show the hidden Button item based on given index**

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.showItem(1);

        </script>

{% endhighlight %}

Also entire group button, can be hide/show using public methods hide(), show().

**Hide the entire GroupButton**

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.hide();

        </script>

{% endhighlight %}

**Show the groupButton**

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.show();

        </script>

{% endhighlight %}

## Enable/Disable

Particular Items can be enabled/disabled using **enableItem**, **disableItem** methods. This takes the index of the button as the argument. 

Also entire GroupButton can be enabled or disabled using enable (), disable public method.

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.disableItem(1);

        </script>

{% endhighlight %}

![Enable/Disable the GroupButton Item](Miscellaneous_images/Miscellaneous_img1.jpeg)


## Getting Index of given Element

By passing the jQuery element of the required button to **getIndex** public method, we can get the index of that passed button element.

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.getIndex(id); // id of the element

        </script>

{% endhighlight %}

## Getting state of given Button

You can get the selection state of required button by passing that button jQuery element to **isSelected** public method.

{% highlight js %}


        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.selectItem(1);

            alert(groupButtonObj.isSelected(1));

        </script>

{% endhighlight %}

Also you can get the active / disabled state required button by passing that button jQuery element to **isDisabled** public method.

{% highlight js %}

        <script>

            groupButtonObj = $("#groupButton").data("ejGroupButton");

            groupButtonObj.disableItem(1);

            alert(groupButtonObj.isDisabled(1));

        </script>

{% endhighlight %}

