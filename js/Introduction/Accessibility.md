---
layout: post
title: Accessibility
description: accessibility
platform: js
control: Introduction
documentation: ug
---

# Accessibility

All our Syncfusion Widgets are developed based on the standards mentioned in the **ARIA specifications**, therefore it supports the full-fledged feature of **Web Accessibility Initiative** ([WAI](http://www.w3.org/WAI/PF/aria-practices/)) – to design a product that is easily accessible to all kinds of people irrespective of their disabilities. 

Since our **Essential JavaScript** has provided the **built-in support for accessibility in all its UI widgets**, therefore it can be easily accessed by the assistive technologies which makes use of the widget’s attribute information (roles, states and properties) and then convey the appropriate information to the persons with disabilities. The two major concepts that has been mainly focussed for providing such accessibility support are as follows,

* Keyboard Navigation
* Defining **ARIA** attributes to the required DOM elements. 

## Keyboard Navigation

Any Syncfusion widgets used within an application are easily accessible to all - especially for the visually disabled peoples and those who cannot use mouse for navigating through the application. To make it more accessible, the built-in **keyboard navigation** support has been provided for almost all the components available within the Essential Studio package which allows all the keyboard enabled widgets to interact with the user. Simply pressing the **TAB** key will move the focus from one element to another within the application.

With this support enabled for the widgets, the various elements present within that particular widget can be easily focussed by pressing the appropriate keyboard shortcuts. The currently focussed element within the widget is clearly indicated with its unique visual style which denotes that it is now ready to accept the user inputs. 

Such visual indications through keyboard navigation are very useful for the accessibility support, as it needs to be properly conveyed to the assistive technologies that the focus has been changed.

Each and every widgets available within the **Syncfusion Essential JavaScript suite** has its unique behavior and responds appropriately to the keyboard actions. As an example, we will look onto the below **3** **editors** placed on the same page and how to navigate between them through keyboard,
{% include image.html url="/js/Introduction/Accessibility_images/Accessibility_img1.png" %}

Initially, the focus is on the first editor (numeric textbox) – which is indicated with the text selection and the border effect provided for the widget’s outline through css.

Having the current focus on the numeric text box, now pressing the **up arrow** will increment the numeric value and **down arrow** will decrement the value. Pressing **tab** key will advance the focus to the next widget present in the page - here the percentage textbox which is placed as second will get focussed on pressing the tab key. 

To enable the default tab key navigation, all the Syncfusion widgets are set with appropriate **tabIndex** property with the provided value as **0** (zero). The element with keyboard focus is essential because it communicates some important information about the widget to the assistive technologies like **screen readers**.

Pressing **Tab** key will traverse the focus in a forward direction and if the **shift + Tab** combination of keys are pressed, the focus will be moved to the previous elements (focus traverse through backward direction).

## Defining ARIA attributes to the required DOM elements

As discussed in the previous topics - To make a component more accessible by all kind of users, it needs to be defined with some essential information along with its initial element creation. Here, the essential information to be defined for the components are its suitable role, state and its properties. Usually the assistive technologies will make use of these information retrieved from the specific attributes and use it to convey the appropriate information to the users.

### Roles, States and Properties

As the widget **role** defines the component type, therefore all the Syncfusion widgets are provided with their corresponding roles. The roles can be anything like button, toolbar, checkbox, radiobutton and so on.

All the Syncfusion widgets are assigned with built-in **States** and **properties** based on its role. Usually the states and properties are defined for a widget using the **ARIA** attributes, which will convey the appropriate current state and action of the control to the assistive technologies. 

For example, our Syncfusion **button** widget, when created through JavaScript code will render in the web browser with HTML DOM elements (along with the assigned built-in ARIA attributes) as shown below,

{% highlight html %}

<!--container to render the Syncfusion button-->
<button id="button11">login</button>

{% endhighlight %}

{% highlight js %} 

//  initialization of ejButton widget 
$("#button11").ejButton({
     size: "normal",
     showRoundedCorner : true
});

{% endhighlight %}

When the above code is executed on the browser, the Syncfusion button widget will render with the following equivalent HTML DOM attributes created for it,

{% highlight html %}


<button id="button11" class="e-button e-js e-btn-normal e-btn e-select e-widget e-corner-all" tabindex="" type="submit" role="button" aria-describedby="login" aria-disabled="false"></button>


{% endhighlight %}

Here, the **aria-describedby** is the **ARIA property** assigned to the Syncfusion button widget as built-in, so that the button description is notified to the user through assistive technologies.

Likewise, the **aria-disabled** is one of the **ARIA state** assigned built-in to the button, which states that if none of that button actions are currently available, then the button is said to be in an aria-disabled state.

