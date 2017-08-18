---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: Split Button
documentation: ug
api: /api/js/ejsplitbutton
---

# Miscellaneous

## Text

It is necessary to display the user defined text for **Split Button**. Using **text** property, you can easily set text content for **Split Button**. This text property overwrites the text that is provided on input button element.

The following steps explains you the details about rendering the **Split Button** with specified text.

In the **HTML** page, add the following button elements to configure **Split Button** widget.


{% highlight html %}



<div class="spltspan">
    <button id="splitButton_text">login</button>
    <ul id="Ul11">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
</div>

{% endhighlight %}

{% highlight javascript %}


    // Initialize the control in JavaScript
    
    $(function () {
        $("#splitButton_text").ejSplitButton({
            //used to set the text content for split button
            text: "signIn",
            size: "small",                                
            targetID: "Ul11"            
        });
    });
    

{% endhighlight %}


Configure the styles.

{% highlight css %}

<style>
    .spltspan {
        margin-left: 120px;
    }
</style>


{% endhighlight %}


Execute the above code to render the following output.

![](/js/SplitButton/Miscellaneous_images/Miscellaneous_img1.png) 

In output “login” text in **Split Button** is replaced by text property value.

## Show Rounded Corner

Specifies the corner of **Split Button** in rounded shape. By default, the edges of **Split Button** is not rounded. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Split Button** with rounded corner.

In the **HTML** page, add the following button elements to configure **Split Button** widget.

{% highlight html %}


<div class="spltspan">
    <button id="splitButton_roundedCorner">login</button>
    <ul id="Ul11">
        <li><span>User</span></li>
        <li><span>Guest</span></li>
        <li><span>Admin</span></li>
    </ul>
</div>


{% endhighlight %}

{% highlight javascript %}


    // Initialize the control in JavaScript
    
    $(function () {
        $("#splitButton_roundedCorner").ejSplitButton({               
            size: "small",    
            //Enable or disable the rounded corner for split button            
            showRoundedCorner: true,
            targetID: "Ul11"            
        });
    });
    

{% endhighlight %}


Configure the styles.

{% highlight css %}


<style>
    .spltspan {
        margin-left: 120px;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.

![](/js/SplitButton/Miscellaneous_images/Miscellaneous_img2.png) 

