---
layout: post
title: Button-types
description: button types
platform: js
control: Toggle Button
documentation: ug
api: /api/js/ejtogglebutton
---

# Button types

**Toggle Button** is used as normal click able button, submitting form data, resetting the form data to its initial value. According to the usage of button, you can render the **Toggle Button** in the following three types by using the **type** property.

Toggle Button Types

<table>
<tr>
<th>Button Type</th><th>Description</th></tr><tr><td>
button</td><td>
The button is a click able button </td></tr>
<tr>
<td>
submit</td><td>
The button is a submit button (submits form-data)</td></tr>
<tr>
<td>
reset</td><td>
The button is a reset button (resets the form-data to its initial values)</td></tr>
</table>


The following steps explains you the details about rendering the **Toggle Button** with above mentioned types. 

In the **HTML** page, add the following button elements to configure **Toggle Button** widget.


{% highlight html %}


<table>
    <tr>
        <td class="btnsht">
            <input type="checkbox" id="type_button" />             
        </td>
    </tr>
    <tr>
        <td class="btnsht">
            <input type="checkbox" id="type_submit" />                
        </td>
    </tr>
    <tr>
        <td class="btnsht">
            <input type="checkbox" id="type_mini" />                
        </td>

    </tr>
</table>
	
{% endhighlight %}

{% highlight javascript %}


      //Initialize the control in JavaScript
      
      $(function () {
          //type property is used to render different type of toggle buttons
          $("#type_button").ejToggleButton({
              size: "large",
              type: "button",
              showRoundedCorner: true,
              defaultText: "Play",
              activeText: "Next",

          });
          $("#type_submit").ejToggleButton({
              size: "large",
              type: "submit",
              showRoundedCorner: true,
              defaultText: "submit",
              activeText: "submitted",
          });
          $("#type_mini").ejToggleButton({
              size: "large",
              type: "reset",
              showRoundedCorner: true,
              defaultText: "reset",
              activeText: "reseted",
          });

      });
    

{% endhighlight %}

Execute the above code to render the following output.

![](/js/ToggleButton/Button-types_images/Button-types_img1.png) 


