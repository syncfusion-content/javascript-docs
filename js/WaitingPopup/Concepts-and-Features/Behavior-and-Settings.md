---
layout: post
title: Behavior-and-Settings
description: behavior and settings
platform: js
control: WaitingPopup
documentation: ug
---

# Behavior and Settings

## Automatic Initializing WaitingPopup widget

**WaitingPopup** widget contains **showOnInit** property that allows the popup to display over a target on page load automatically. By default, **showOnInit** property is set as false.

The following steps explains you on how to display the **WaitingPopup** on page load.

1. In an **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}



      <div class="control">               
      <div id="waitingPopUp"></div>            
       </div>  

{% endhighlight %}

{% highlight js %}




// Configure the WaitingPopup to display automatically on page load as follows.
        <script type="text/javascript">
         $(function () {
        // declaration
        $("#waitingPopUp").ejWaitingPopup({
            showOnInit: true,
        });
    });
</script>

{% endhighlight %}

2. Add the following styles to render **WaitingPopup** widget.



{% highlight css %}



<style type="text/css" class="cssStyles">
    #waitingPopUp {
        height: 320px;
        width: 600px;
    }
</style>


{% endhighlight %}



The following screenshot illustrates the **WaitingPopup** when **showOnInit** is set to “**true**”.

{% include image.html url="/js/WaitingPopup/Concepts-and-Features/Behavior-and-Settings_images/Behavior-and-Settings_img1.png" Caption="WaitingPopup with enabled showOnInit property"%}

## Enable / Disable Popup Indicator

You can show or hide the popup indicator of **WaitingPopup** widget using **showImage** property. By default, **showImage** property is set as **true**.

The following steps explains you to enable / disable popup indicator in **WaitingPopup** widget.

1. In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}



      <div class="control">               
    <div id="waitingPopUp"></div>            
    </div>  

{% endhighlight %}

{% highlight js %}



// To configure Enable / Disable popup indicator in WaitingPopup, use the following code.
     <script type="text/javascript">
      Enable popup indicator:
      $(function () {
     // declaration
     $("#waitingPopUp").ejWaitingPopup({
        showOnInit: true,
        showImage: true,
         text: "Loading... Please wait..."
    });
});

      Disable popup indicator:
      $(function () {
      // declaration
      $("#waitingPopUp").ejWaitingPopup({
        showOnInit: true,
        showImage: false,
        text: "Loading... Please wait..."
    });
});
</script>

{% endhighlight %}

2. Add the following styles to render **WaitingPopup** widget.



{% highlight css %}



<style type="text/css" class="cssStyles">
    #waitingPopUp {
        height: 320px;
        width: 600px;
    }
</style>


{% endhighlight %}



Execute the above code to render the following output.

{% include image.html url="/js/WaitingPopup/Concepts-and-Features/Behavior-and-Settings_images/Behavior-and-Settings_img2.png" Caption="Enabled popup indicator WaitingPopup widget"%}

{% include image.html url="/js/WaitingPopup/Concepts-and-Features/Behavior-and-Settings_images/Behavior-and-Settings_img3.png" Caption="Disabled popup indicator WaitingPopup widget"%}

## Show / Hide WaitingPopup

Using **show()** and **hide()** methods, you can display or hide the **WaitingPopup** widget over the target area.

The following steps explains you to show / hide the **WaitingPopup** widget.

1. In the **HTML** page, add a **&lt;div&gt;** element to render **WaitingPopup** widget.

{% highlight html %}



      <div class="control">               
      <div id="waitingPopUp"></div>            
     </div>  

{% endhighlight %}

{% highlight js %}



// Use the following code to Show / Hide WaitingPopup.
    <script type="text/javascript">
Show WaitingPopup:
$(function () {
    $("#waitingPopUp").ejWaitingPopup();
    var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");
    popUpObj.show();
});	

Hide WaitingPopup:
$(function () {
    $("#waitingPopUp").ejWaitingPopup();
    var popUpObj = $("#waitingPopUp").data("ejWaitingPopup");
    popUpObj.hide();
});
</script>
     
{% endhighlight %}

2. Add the following styles to render **WaitingPopup** widget.

{% highlight css %}


<style type="text/css" class="cssStyles">
    #waitingPopUp {
        height: 320px;
        width: 600px;
    }
</style>


{% endhighlight %}



The following screenshot illustrates a **WaitingPopup** when **show()** method is invoked.

{% include image.html url="/js/WaitingPopup/Concepts-and-Features/Behavior-and-Settings_images/Behavior-and-Settings_img4.png" Caption="WaitingPopup with show() method"%}

