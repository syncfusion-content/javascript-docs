---
layout: post
title: Behavior-Settings
description: behavior settings 
platform: js
control: Dialog
documentation: ug
---

# Behavior Settings 

## Resize Support

The **Dialog** control can be resized using this feature. You can resize the **Dialog** by dragging the bottom right corner area.

### Enable Resize Option

The following steps explains you the implementation of resize option in the **Dialog** control. 

In an HTML page set a &lt;div&gt; element with dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}
    
        // Enable resize in the Dialog function by setting enableResize property as true. By default, value for enableResize is true
        $(function() {
            // declaration
            $("#Dialog").ejDialog({
                height: 200,
                width: 300,
                enableResize: true
            });
        });

{% endhighlight %}

The output for Dialog control when “enableResize” is “true” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img1.png" %}

## Drag Support

The **Dialog** control supports the drag functionality. You can click the **Dialog** header and drag the control anywhere in the web page.

### Allow Drag Option

The following steps explains you the implementation of drag option in the **Dialog** control. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}


<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>
	
{% endhighlight %}

{% highlight js %}

    // Allow drag in the Dialog function by setting allowDraggable property as true. The default value for allowDraggable is true in the Dialog control
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        allowDraggable: true
    });

{% endhighlight %}

The output for Dialog control when “allowDraggable” is “true” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img2.png" %}

## Close Icon ToolTip Support

You can change the close icon tooltip in the **Dialog** control by using **closeIconTooltip** property. The default value for **closeIconTooltip** is **close** in the **Dialog** control.

### Define Close Icon ToolTip

The following steps explains you the implementation of close icon tooltip option in the **Dialog** control. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}

    // Set the closeIconTooltip value in the Dialog function using the following codes. The default value for closeIconTooltip is close in the Dialog control
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        closeIconTooltip: "close"
    });

{% endhighlight %}

The output for Dialog control when “closeIconTooltip” is “close” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img3.png" %}

## Persistence Support

The **Dialog** control supports the state maintenance where you can maintain the state of the **Dialog** control in the web page. The default value for **enablePersistence** is **false** in the **Dialog** control.

### Enable Persistence Option

The following steps explains the implementation of persistence support in the **Dialog** control. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}

    // Enable the persistence to the Dialog function by setting enablePersistence property as true. The default value for enablePersistence is false in the Dialog control
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        enablePersistence: true
    });


{% endhighlight %}

Make resize and reload the web page. The state is maintained in the **Dialog** control. The output for **Dialog** control when “**enablePersistence**” is “**true**” is as follows. 

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img4.png" %}

## Enabled or Disabled

The **Dialog** control supports the enabled or disabled option that allows you to enable or disable the **Dialog** control in the web page.

### Enable Dialog Control

The following steps explains the implementation of enable option in the **Dialog** control. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}

    // Enable the Dialog in the Dialog function by setting enabled property as true. The default value for enabled is true in the Dialog control
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        enabled: true
    });

{% endhighlight %}

The output for Dialog control when “enabled” is “true” is as follows.          

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img5.png" %}

## Disable Dialog Control

The following steps explains you the implementation of disable option in the **Dialog** control. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}

    // Disable the Dialog in the ejDialog function by setting enabled as false
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        enabled: false
    });

{% endhighlight %}

The output for Dialog control when enabled is “false” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img6.png" %}

## Dialog Position

The **Dialog** provides the option to place the control based upon its X-axis and Y-axis position in the web page. The following steps explains you the implementation of dialog position option.

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.<br />
   Position <br />
   X-Axis : 20 <br />
   Y-Axis : 26
</div>

{% endhighlight %}

{% highlight js %}

    // Set the X and Y position to the Dialog function by setting Position property
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        position: {
            X: 20,
            Y: 26
        }
    });

{% endhighlight %}

The output for Dialog control after setting X-axis and Y-axis value.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img7.png" %}

## Header Option

You can show or hide the **Dialog** header by setting **showHeader** property. The following steps explains you the implementation of **Dialog** header option.

### Show Header

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}


    // Set the showHeader property as true in the Dialog function
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        showHeader: true
    });

{% endhighlight %}

The output for Dialog control when showHeader is “true” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img8.png" %}

### Hide Header

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}
    
    // Set the showHeader property as false in the Dialog function
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        showHeader: false
    });

{% endhighlight %}

The output for Dialog control when showHeader is “false” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img9.png" %}

## Show at Initial

The **Dialog** control contains an option to be visible or hidden at initialization. The default value for **showOnInit** is **true**. Setting false to the **showOnInit** hides the **Dialog** control at initialization.

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>

{% endhighlight %}

{% highlight js %}
    
    // Set the showOnInit property as true in the Dialog function
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        showOnInit: true /* false hides the dialog at initialization */
    });                 

	
{% endhighlight %}

The output for Dialog control when showOnInit is “true” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img10.png" %}

## Rounded Corner Support

The **Dialog** can support with rounded corner appearance, the default value for **showRoundedCorner** is **false**. 

In the HTML page set a &lt;div&gt; element with the dialog content for rendering the Dialog control. 

{% highlight html %}

<div id="Dialog" title="Syncfusion Dialog">
   The Syncfusion Dialog control is rendered.
</div>
	
{% endhighlight %}

{% highlight js %}


    // Set the showRoundedCorner property as true in the Dialog function
    $("#Dialog").ejDialog({
        height: 200,
        width: 300,
        showRoundedCorner: true
    });


{% endhighlight %}

The output for **Dialog** control when **showRoundedCorner** is “**true**” is as follows.

{% include image.html url="/js/Dialog/Behavior-Settings_images/Behavior-Settings_img11.png" %}

