---
layout: post
title: Customizing-the-scroll-Step
description: customizing the scroll step
platform: js
control: Scroller
documentation: ug
---

# Customizing the scroll Step

The **Scroller** control allows you to specify the scroll movement step in a pixel value, this step value is added to the scrollbar position when you press the arrow key. Based on position value, the scrollbar moves in its corresponding orientation. You can achieve this by using **scrollOneStepBy.**

The following steps explains you the configuration of **scrollOneStepBy** property in **Scroller**. 

In the HTML page, add a &lt;div&gt; element to configure Scroller widget.

{% highlight html %}

<div id="scrollcontent">
   <div>
      <!--Wrapper div for Scroller.-->
      <div id="innercontent">
         <!--Content div-->
         <h3>MVC </h3>
         <p>
            Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart or a diagram.
         </p>
      </div>
   </div>
</div>

{% endhighlight %}

{% highlight js %}
	
    $(function() {
       $("#scrollcontent").ejScroller({
          height: 170,
          width: 350,
          scrollOneStepBy: 50
       });
    });

{% endhighlight %}

The following screenshot displays the **Scroller** control with scroll step value.

{% include image.html url="/js/Scroller/Customizing-the-scroll-Step_images/Customizing-the-scroll-Step_img1.png"%}

