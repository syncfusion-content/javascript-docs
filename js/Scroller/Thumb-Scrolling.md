---
layout: post
title: Thumb-Scrolling
description: thumb scrolling
platform: js
control: Scroller
documentation: ug
---

# Thumb Scrolling

Normally the scrollbar position can be changed by dragging the scrollbar handle or clicking the arrows. The **Scroller** control allows you for panning or dragging the scroll content area to drag by dragging inside the scroll content. To achieve this in your **Scroller** control, enable the **enableTouchScroll** to true. By default the value for **enableTouchScroll** is true. When you want to prevent the panning or dragging the scroll content area, set **enableTouchScroll** as false.

The following steps explains you the configuration of **enableTouchScroll** property in **Scroller**. 

In the HTML page, add a &lt;div&gt; element to configure Scroller widget.

{% highlight html %}


	<div id="scrollcontent">
	  <div>                              <!--Wrapper div for Scroller.-->
	     <div id="innercontent">         <!--Content div-->
	        <h3>MVC </h3>
	         <p>
	           Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart           or a diagram.
	         </p>
	    </div>
	  </div>
	</div>


{% endhighlight %}

{% highlight js %}


    $(function () {
        $("#scrollcontent").ejScroller({ 
               height: 170, 
               width: 350,
               enableTouchScroll: false
        });
    }); 
   


{% endhighlight %}


The following screenshot displays **Scroller** control with disabled touch support.

{% include image.html url="/js/Scroller/Thumb-Scrolling_images/Thumb-Scrolling_img1.png" Caption="Scroller control with disabled touch support"%}

