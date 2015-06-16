---
layout: post
title: Miscellaneous
description: miscellaneous
platform: js
control: Split Button
documentation: ug
---

# Miscellaneous

## Text

It is necessary to display the user defined text for **Split Button**. Using **text** property, you can easily set text content for **Split Button**. This text property overwrites the text that is provided on input button element.

The following steps explains you the details about rendering the **Split Button** with specified text.

1. In the **HTML** page, add the following button elements to configure **Split Button** widget.


{% highlight html %}



   <div class="spltspan">
        <button id="spltbutton_text">login</button>
        <ul id="Ul11">
            <li><span>User</span></li>
            <li><span>Guest</span></li>
            <li><span>Admin</span></li>
        </ul>
</div>

{% endhighlight %}

{% highlight js %}


// Initialize the control in JavaScript
    <script type="text/javascript">
        $(function () {
            $("#spltbutton_text").ejSplitButton({
                //used to set the text content for split button
                text: "signin",
                size: "small",                                
                targetID: "Ul11"            
            });
        });
    </script>

{% endhighlight %}


2. Configure the styles.

{% highlight css %}

    <style>
        .spltspan {
            margin-left: 120px;
        }
    </style>


{% endhighlight %}


Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img1.png" Caption="Split button with new text"%}

In output “login” text in **Split Button** is replaced by text property value.

## Show Rounded Corner

Specifies the corner of **Split Button** in rounded shape. By default, the edges of **Split Button** is not rounded. To set rounded corner, you can enable **showRoundedCorner** property**.**

The following steps explains you the details about rendering the **Split Button** with rounded corner.

1. In the **HTML** page, add the following button elements to configure **Split Button** widget.

{% highlight html %}


<div class="spltspan">
        <button id="spltbutton_roundedCorner">login</button>
        <ul id="Ul11">
            <li><span>User</span></li>
            <li><span>Guest</span></li>
            <li><span>Admin</span></li>
        </ul>
</div>


{% endhighlight %}

{% highlight js %}



// Initialize the control in JavaScript
    <script type="text/javascript">
        $(function () {
            $("#spltbutton_roundedCorner").ejSplitButton({               
                size: "small",    
                //Enable or disable the rounded corner for split button            
                showRoundedCorner: true,
                targetID: "Ul11"            
            });
        });
    </script>


{% endhighlight %}


2. Configure the styles.

{% highlight css %}


    <style>
        .spltspan {
            margin-left: 120px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/SplitButton/Concepts-and-Features/Miscellaneous_images/Miscellaneous_img2.png" Caption="Split button with rounded corner"%}

