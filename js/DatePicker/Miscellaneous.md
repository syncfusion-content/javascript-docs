---
layout: post
title: Miscellaneous
description: Configure start day of week, step month, and enable/disable
platform: js
control: DatePicker
documentation: ug
api: /api/js/ejdatepicker
---
# Miscellaneous 

## Start Day

By default DatePicker calendar starts with “Sunday” and ends with “Monday”. You can redefine this start day by using [startDay](https://help.syncfusion.com/api/js/ejdatepicker#members:startday) property.

Refer below code to start Wednesday as start day. 

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                startDay: 3 // sets start day as Wednesday in DatePicker calendar

            });

        });

{% endhighlight %}

## Step Months

DatePicker calendar allows you to quick navigate back and forth from one month to previous or next month by clicking the arrow button. By default it’s navigate one by one month. You can also navigate by skipping months in odd or even or any count by using [stepMonths](https://help.syncfusion.com/api/js/ejdatepicker#members:stepmonths) property. 

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                stepMonths: 2 // skips the one months from current month(July to Sept to Nov)

            });

        });

{% endhighlight %}

## Read Only

You can make DatePicker as read only by setting [readOnly](https://help.syncfusion.com/api/js/ejdatepicker#members:readonly) property as true. It allows only to read the value and it can’t be changed by interaction.

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                readOnly: true //sets DatePicker as read only

            });

        });

{% endhighlight %}

## Enable or Disable

You can enable or disable the DatePicker textbox by using [enabled](https://help.syncfusion.com/api/js/ejdatepicker#members:enabled) property. In inline mode DatePicker calendar also gets enabled or disabled. 

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                enabled: false //disables the DatePicker textbox

            });

        });

{% endhighlight %}

