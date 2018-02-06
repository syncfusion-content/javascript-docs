---
layout: post
title: miscellaneous 
description: miscellaneous 
platform: js
control: DateRangePicker
documentation: ug
api: /api/js/ejdaterangepicker
---

## Miscellaneous 

### Enable / Disable

The control can be enabled / disabled using public methods, **enable** or **disable**. 

{% highlight html %}

      $("#daterange").ejDateRangePicker();
       
      $("#daterange").ejDateRangePicker("disable");

{% endhighlight %}


{% highlight html %}

      $("#daterange").ejDateRangePicker("enable");

{% endhighlight %}


### Allow Editing

Editing in input box can be disabled by setting the false value to **allowEdit** API. By default this will be false and we can edit the value in input box

{% highlight html %}

        $("#daterange").ejDateRangePicker({

            allowEdit: false

        });
        
{% endhighlight %}


### Clear ranges

To clear the all selection and ranges in a popup we can make use of **clearRanges** method.

{% highlight html %}

        $("#daterange").ejDateRangePicker("clearRanges");

{% endhighlight %}

### Add ranges

Add the preset ranges to DateRangePicker popup. we can make use of **addRanges** method.

{% highlight html %}

        $("#daterangepicker").ejDateRangePicker();
        // Create DateRangePicker instance
        var dateObj = $("#daterangepicker").data("ejDateRangePicker");
        dateObj.addRanges("new Range", [new Date("11/12/2019"),new Date("11/12/2021")] ); 

{% endhighlight %}


### set Range

set the preset ranges to DateRangePicker popup.. we can make use of **setRange** method.

{% highlight html %}

        $("#daterangepicker").ejDateRangePicker();
        // Create DateRangePicker instance
        var dateObj = $("#daterangepicker").data("ejDateRangePicker");
        dateObj.setRange([new Date("11/12/2019"),new Date("11/12/2021")]); 

{% endhighlight %}

### popupHide

Close the DateRangePicker popup, if it is in opened state. we can make use of **popupHide** method.

{% highlight html %}

          $("#daterange").ejDateRangePicker();
          // hides the DateRangePicker popup
          $("#daterange").ejDateRangePicker("popupHide");


{% endhighlight %}

### popupShow

Open the DateRangePicker popup. we can make use of **popupShow** method.

{% highlight html %}

          $("#daterange").ejDateRangePicker();
          // hides the DateRangePicker popup
          $("#daterange").ejDateRangePicker("popupShow");


{% endhighlight %}

### WaterMark Text

The **watermarkText** property of the daterangepicker control allows an option to specifies the water mark text to be displayed in input text.

{% highlight javascript %}
     
	   $(function () {
 
            $("#dateRangePicker").ejDateRangePicker({

               watermarkText: "Enter date"  // default value is “Select Range”

            });

        });      

{% endhighlight %}

Execute the above code to render the following output.

![](/js/DateRangePicker/Miscellaneous_images/Miscellaneous_img2.png)


### showPopupButton

The **showPopupButton** property of the daterangepicker control allows an option to shows/hides the date icon button at right side of textbox, which is used to open or close the DateRangePicker calendar popup.

{% highlight javascript %}
     
	   $(function () {
 
            $("#dateRangePicker").ejDateRangePicker({

              showPopupButton:false   
              
            });

        });      

{% endhighlight %}

Execute the above code to render the following output.

![](/js/DateRangePicker/Miscellaneous_images/Miscellaneous_img1.png)
