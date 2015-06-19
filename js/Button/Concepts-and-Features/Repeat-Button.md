---
layout: post
title: Repeat-Button
description: repeat button
platform: js
control: Button
documentation: ug
---

# Repeat Button

When you press button continuously, click event is raised at each specific time interval. This type of button is called **Repeat Button**. This functionality repeatedly raises the click event of button in both button click and from button in pressed state to the released state. **timeInterval** property is used to specify the time Interval for triggering click event, when the button is in pressed state. **repeatButton** property is used to set the button in repeat mode.****

The following steps explains you the details about rendering the **Repeat Button.**

* In the **HTML** page, add the following button elements to configure **Button** widget.



<table>
<tr>
<td>
<b>[HTML]</b>&lt;div class="control"&gt;        &lt;div class="align"&gt;            <button id="button_repeat">Click</button>        &lt;/div&gt;        &lt;div class="align"&gt;            &lt;div&gt;<b>Event Trace</b>&lt;/div&gt;            &lt;div class="eventTrace"&gt;&lt;/div&gt;        &lt;/div&gt;    &lt;/div&gt;</td></tr>
<tr>
<td>
<b>[JavaScript]</b><b>//</b> Initialize the control in <b>JavaScript</b>&lt;script type="text/javascript"&gt;    $(function () {        $("#button_repeat").ejButton({            size: "mini",            showRoundedCorner: true,            //used to set the button in repeat mode<b>            repeatButton: true,</b>            //specifies the time interval for click method             //call, when the button is in pressed state<b>            timeInterval: "200",</b>            click: "btnClick"        });    });    //If the button  is in pressed state or clicked, this method will be called     function btnClick(e) {        $(".eventTrace").html("click event has been triggered..&lt;/br&gt;" + $(".eventTrace").html());    }    &lt;/script&gt;</td></tr>
</table>


* Configure the **CSS** styles to apply on button



{% highlight css %}

**[CSS]**
<style>
        .align {
            display: table-cell;
            padding-left: 50px;
        }
    </style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/Button/Concepts-and-Features/Repeat-Button_images/Repeat-Button_img1.png" Caption=""%}

_Figure 10: Output for repeat button_

