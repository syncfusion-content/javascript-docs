---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: GroupButton
documentation: ug
---

# Miscellaneous

## Show/Hide the items

Particular currently showing button items can be hided. Also it provides the options to show the hided button again. These functionalities can be achieved using **showItem** or **hideItem** method.

**Hide the Button item based on given index**

{% highlight js %}

        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.hideItem(1);

        </script>

{% endhighlight %}

**Show the hided Button item based on given index**

{% highlight js %}

        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.showItem(1);

        </script>

{% endhighlight %}

Also entire group button, can be hide/show using public methods hide(), show().

## Enable/Disable

Particular Items can be enabled/disabled using **enableItem**, **disableItem** methods. This takes the index of the button as the argument. 

Also entire GroupButton can be enabled or disabled using enable (), disable public method.

{% highlight js %}

        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.disableItem(1);

        </script>

{% endhighlight %}

![](Miscellaneous_images/Miscellaneous_img1.jpeg)


## Getting Index of given Element

By passing the jQuery element of the required button to **getIndex** public method, we can get the index of that passed button element.

{% highlight js %}

        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.getIndex(id); // id of the element

        </script>

{% endhighlight %}

## Getting state of given Button

You can get the selection state of required button by passing that button jQuery element to **isSelected** public method.

{% highlight js %}


        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.selectItem(1);

            alert(grpbtnObj.isSelected(1));

        </script>

{% endhighlight %}

Also you can get the active / disabled state required button by passing that button jQuery element to **isDisabled** public method.

{% highlight js %}

        <script>

            grpbtnObj = $("#groupButton").data("ejGroupButton");

            grpbtnObj.disableItem(1);

            alert(grpbtnObj.isDisabled(1));

        </script>

{% endhighlight %}

