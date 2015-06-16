---
layout: post
title: RTL
description: rtl
platform: js
control: Scroller
documentation: ug
---

# RTL

**enableRTL** API provides right-to-left functionality and features for languages that work in a right-to-left for selecting, editing. Arabic and Hebrew are written from right to left. If you have a working style from right to left, you can use this feature in scroller. You can achieve this in your **Scroller** by using **enableRTL** property. Setting this property to true, the Scroller content text is displayed in the right to left format. The vertical scrollbar move to right to left side.

The following steps explains you the configuration of **enableRTL** property in **Scroller**.

1. In the HTML page, add a &lt;div&gt; element to configure Scroller widget.

{% highlight html %}

	
	<div id="scrollcontent">
	  <div>                              <!--Wrapper div for Scroller.-->
	     <div id="innercontent">         <!--Content div-->
	        <h3>MVC </h3>
	         <p>
	           Model–view–controller (MVC) is a software architecture pattern which separates the representation of information from the user's interaction with it. The model consists of application data, business rules, logic, and functions. A view can be any output representation of data, such as a chart or a diagram.
	         </p>
	    </div>
	  </div>
	</div>


{% endhighlight %}

{% highlight js %}


	<script type="text/javascript">
	
	    $(function () {
	        $("#scrollcontent").ejScroller({ 
	               height: 170, 
	               width: 350, 
	               enableRTL: true
	        });
	    }); 
	   
	</script>


{% endhighlight %}


The following screenshot displays the **Scroller** control in **RTL** direction.

{% include image.html url="/js/Scroller/Concepts-and-Features/RTL_images/RTL_img1.png" Caption="Scroller control in RTL direction"%}

