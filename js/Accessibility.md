---
layout: post
title: Accessibility of Essential JS UI widgets
description: WAI-ARIA accessibility compliance of Essential JS UI widgets
platform: js
control: Introduction
documentation: ug
---

# Accessibility

All the Essential JS UI widgets provide built-in compliance with the [WAI-ARIA](http://www.w3.org/WAI/PF/aria-practices/) specifications. This ensures that the widgets work properly with  assistive technologies. WAI-ARIA compliance for the widgets have been achieved by providing proper keyboard navigation support as well as by defining the required ARIA attributes to the DOM elements.

For example, the `ejButton` widget, when created through JavaScript code will render in the web browser with HTML DOM elements (along with the assigned built-in ARIA attributes) as shown below,

{% highlight html %}

<!--container to render the Syncfusion button-->
<button id="button11">login</button>

{% endhighlight %}

{% highlight javascript %} 

//  initialization of ejButton widget 
$("#button11").ejButton({
     size: "normal",
     showRoundedCorner : true
});

{% endhighlight %}

When the above code is executed on the browser, the button widget will render with the following equivalent HTML DOM attributes created for it,

{% highlight html %}


<button id="button11" class="e-button e-js e-btn-normal e-btn e-select e-widget e-corner-all" tabindex="" type="submit" role="button" aria-describedby="login" aria-disabled="false"></button>


{% endhighlight %}

Here, `aria-describedby` is the ARIA property assigned to the Syncfusion button widget so that the button description is notified to the user through assistive technologies.

Likewise, `aria-disabled` is one of the ARIA state assigned to the button, which states that if none of the button actions are currently available, then the button is said to be in an `aria-disabled` state.