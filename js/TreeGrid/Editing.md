---
layout: post
title: Editing
description: editing
platform: js
control: TreeGrid
documentation: ug
---

# Editing

The TreeGrid control provides built-in support for editing cell items. 

### Cell Editing

Update the task details through cell editing by setting [`editMode`](/api/js/ejtreegrid#editsettingseditmodespan-classtype-signature-type-stringstringspan "editSettings.editMode") as `cellEditing`.

The following code example shows you how to enable `cellEditing` in TreeGrid control.

{% highlight js %}

    $("#TreeGridContainer").ejTreeGrid({
        //...
        editSettings: {
            allowEditing: true,
            editMode: "cellEditing"

        },
    });

{% endhighlight %}

The output of the TreeGrid with `cellEditing` is as follows.

![](/js/TreeGrid/Editing_images/Editing_img1.png)

