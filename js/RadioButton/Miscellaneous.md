---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: RadioButton
documentation: ug
api: /api/js/ejradiobutton
---

# Miscellaneous

## RadioButton ID

**RadioButton id** is not shown in the user interface. Here id denotes the id attribute of the root element of **RadioButton** control. This id value is unique. You can give id through **element** and through the **id property**. When you use two id for a single radio button at initialization, the **element id** is considered.

Set **id** for RadioButton control as follows.


{% highlight javascript %}

        $(function () {
            //set new id value as follows
            $("#Radio_Male").ejRadioButton({ name: "Gender", id: "male_type" });
            $("#Radio_Female").ejRadioButton({ name: "Gender", id: "female_type" });
        });


{% endhighlight %}

## RadioButton Prefix id

Id prefix value is appended to id value. It is used to mention the prefix for the wrapper’s id attribute. When you assign a value for **idPrefix** property, the older prefix id gets replaced by the new prefix id. 

Setting a new prefix id for **RadioButton** control is as follows.



{% highlight javascript %}

        $(function () {
            //set new idPrefix value as follows
            $("#Radio_Male").ejRadioButton({ name: "Gender", idPrefix:"sync"  });
            $("#Radio_Female").ejRadioButton({ name: "Gender", idPrefix:"sync"  });
        });


{% endhighlight %}

## RadioButton Name

The **name** setting tells you where a **RadioButton** belongs. When you select one button, all other buttons in the same group are unselected. You can have only one group of **RadioButtons** on each page.

The **name** attribute is also used to identify form data after it has been submitted to the server, or for reference of form data using **JavaScript** on the client’s side. Only form elements with a **name** attribute have their values passed, when submitting a form.

## RadioButton Value

The **value** setting defines what can be submitted when checked.

For **RadioButtons**, the contents of the value property do not appear in the user interface. The **value** property only has meaning when submitting a form. If a radio button is in the checked state when the form is submitted, the name of the Radio button is sent along with the value of the value property, if the radio button is not checked, no information is sent.

To identify, on the server side, which one was checked, give different values for radio buttons in the same group, 

Set name and value for each radio button control as follows.



{% highlight javascript %}

        $(function () {
            //set name and value for each radio button as follows
            $("#Radio_Male").ejRadioButton({ name: "Gender", value: "male"  });
            $("#Radio_Female").ejRadioButton({ name: "Gender", value: "female" });
        });


{% endhighlight %}









