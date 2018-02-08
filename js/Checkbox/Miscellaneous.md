---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: Checkbox
documentation: ug
api : /api/js/ejcheckbox
---

# Miscellaneous

## Checkbox Id

**Checkbox** id is not displayed in user interface. Here, **id** mentions the id attribute of the root element of **Checkbox** control. When you assign a value for **id** property, then this older id is replaced by new id. This id value should be unique. 

Set id for **Checkbox** control as follows.

{% highlight javascript %}


        $(function () {
            $("#check1").ejCheckBox({ id: "sync" });
        });


{% endhighlight %}

## Checkbox Id Prefix

Id prefix value is the one that is appended to id value. It is used to mention the prefix for the wrapper’s id attribute. When you assign a value for **idPrefix** property, the older prefix id is replaced by new prefix id. 

Set prefix id for **Checkbox** control as follows.



{% highlight javascript %}

        
        $(function () {
            $("#check1").ejCheckBox({ idPrefix: "JS" });
        });


{% endhighlight %}

## Checkbox Name

The name attribute is used to identify from data after it is submitted to the server, or to reference from data using **JavaScript** on the client side. **Checkbox** also contains name attribute. This name should be a unique one. It is used to receive the **Checkbox** value. Without using name, you can’t get the particular checkbox values at the time of submitting form.

## Checkbox Value

For **Checkboxes**, the contents of the value property do not appear in the user interface. The value property contains only a meaning when submitting a form. When a Checkbox is in checked state and when the form is submitted, the name of the **Checkbox** is sent along with the value of the value property (When the checkbox is not checked, no information is sent).

You can set name and value for **Checkbox** control as follows.



{% highlight javascript %}


       $(function () {
            $("#check1").ejCheckBox({ name: "Conformation", value :"received" });
       });


{% endhighlight %}

## State Persistence

Specifies the persist property for CheckBox while initialization. The persist API save current model value to browser cookies for state maintains. While refreshing the CheckBox control page the model value apply from browser cookies.

{% highlight javascript %}

        $(function () {

             //To set persist API value

             $("#checkBox").ejCheckBox({ enablePersistence : false });

        });

{% endhighlight %}

## RTL Support

In some cases you need to use right-to-left alignment. You can give RTL support by using **enableRTL** property.  **RTL** mode works when you use the **text** property in **Checkbox**. The **Checkbox** and text are aligned in the right-to-left format. For example, when text is right-aligned and Checkbox is left-aligned, after you apply right-to-left alignment, these positions are interchanged. 

The following steps explain the details about rendering the **Checkbox** with right-to-left alignment support. Here the **text** property is necessary.

In the HTML page, add the following button elements to configure Checkbox widget.

{% highlight html %}

    <input type="checkbox" id="checkBox"/>
    <label for="checkBox">Experienced</label>

{% endhighlight %}

{% highlight javascript %}

    // Initializes the control in JavaScript
    $(function () {
        //set checkbox with right to left format
        $("#checkBox").ejCheckBox({  enableRTL : true });
    });

{% endhighlight %}


In the above mentioned code, the **text** property has been used. In **LTR** format, the **CheckBox** is on the left side. In **RTL** format, the **CheckBox** appears on the right side. Here the **text** property is used and the **enableRTL** property is set as “**true**”**.** It changes the alignment to right-to-left.








