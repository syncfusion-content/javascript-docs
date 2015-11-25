---
layout: post
title: DatePicker Customization
description: DatePicker customization such as dimension, highlight dates, other months, etc.
platform: js
control: DatePicker
documentation: ug
---
# Customization

DatePicker provides more flexible way to customize the below listed properties.

## Set Dimension 

By default DatePicker has standard height and width (height: ‘30px’ and width: ’143px’). You can change this height and width by using [height](http://help.syncfusion.com/js/api/ejdatepicker#members:height) and [width](http://help.syncfusion.com/js/api/ejdatepicker#members:width) property respectively.

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                height: '50px', // sets height as 50 pixel

                width: '300px'// sets width as 300 pixel

            });

        });

{% endhighlight %}

Mostly dimension plays a vital role in web application to get responsive layout in all devices. DatePicker is a form control and you can make it as responsive by specifying its width as “**100%**".

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                width: '100%'// sets width as 100 percentage

            });

        });

{% endhighlight %}

## Show Footer

You can show or hide the footer of DatePicker calendar by using [showFooter](http://help.syncfusion.com/js/api/ejdatepicker#members:showfooter) property. 

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                showFooter: false // hides the footer in DatePicker calendar

            });

        });

{% endhighlight %}

N>  Footer contains the today button to quickly navigate to the current date. By turning off it, you have to select current date by manually. 

## Show Popup Button

DatePicker textbox contains a button to open the DatePicker calendar. You can hide this DatePicker calendar button using [showPopupButton](http://help.syncfusion.com/js/api/ejdatepicker#members:showpopupbutton) value as false.

By hiding this button, you can open the DatePicker by focusing the input textbox element itself.

{% highlight js %}

       $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                showPopupButton: false // hides the DatePicker calendar button

            });

        });

{% endhighlight %}

## Show Other Months

You can show or hide the other month days from DatePicker calendar by using [showOtherMonths](http://help.syncfusion.com/js/api/ejdatepicker#members:showothermonths) property.

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                showOtherMonths: false // hides the days of other months in DatePicker calendar

            });

        });

{% endhighlight %}

## Highlight Special Date

DatePicker allows you to highlight the special dates in DatePicker calendar by using [specialDates](http://help.syncfusion.com/js/api/ejdatepicker#members:specialdates) property. It receives the array of JSON data, in which the data should contain the date value, icon CSS class and tooltip as field values with any names.

{% highlight js %}

    var data = [{ specialdate: "28/06/2015", customClass: "birthday", tooltip: "xxx birthday" }]

{% endhighlight %}

And you can map those above field names to DatePicker by using [fields](http://help.syncfusion.com/js/api/ejdatepicker#members:fields) property, which holds following members.

<table>
<tr>
<th>
Members</th><th>
Description</th></tr>
<tr>
<td>
date<br/><br/></td><td>
It specifies the mapping field of special date<br/><br/></td></tr>
<tr>
<td>
iconClass<br/><br/></td><td>
It specifies the mapping field of icon CSS class.<br/><br/></td></tr>
<tr>
<td>
tooltip<br/><br/></td><td>
It specifies the mapping field of tool tip text.<br/><br/></td></tr>
</table>
{% highlight js %}

    // assign special date values in local variable data

    var data = [{ specialdate: "28/06/2015", customClass: "birthday", tooltip: "xxx birthday" }]


    $(function () {

        // creates DatePicker from input

        $("#datePicker").ejDatePicker({

            specialDates: data, // date values in data variable assigned to specialDates

            fields: { date: "specialDate", iconCSS: "customClass", tooltip: "toolTip" }

            // mapping special date fields

        });

    });

{% endhighlight %}

