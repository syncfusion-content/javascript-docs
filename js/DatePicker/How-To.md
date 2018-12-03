---
layout: post
title: Syncfusion How-to
description: How-to section
platform: js
control: DatePicker
documentation: ug
api: /api/js/ejdatepicker
---
# How to?

## Customizing template with range selection between two DatePicker. 

You can customize the date field to emphasize the particular dates in DatePicker calendar with help of [specialDates](https://help.syncfusion.com/api/js/ejdatepicker#members:specialdates) and set the date range using [minDate](https://help.syncfusion.com/api/js/ejdatepicker#members:mindate) and [maxDate](https://help.syncfusion.com/api/js/ejdatepicker#members:maxdate) property. Refer the sample from the link [Hotel Booking](http://jsplayground.syncfusion.com/bdr5k4cg#) to know how to customize date with date range.

## Localize DatePicker with browser specific culture

You can get the browser culture name at page load or document ready state. Based on the culture name, DatePicker can be initiated with that specific culture value by assigning to [locale](https://help.syncfusion.com/api/js/ejdatepicker#members:locale) property. Refer the sample from the link [Browser Specific Culture](http://www.syncfusion.com/kb/4904/datepicker-control-culture-have-to-change-based-on-the-browser-language#) to create DatePicker with browser specific culture.

## Disable specific dates to restrict user

DatePicker allows you to restrict date selection in specific range by using date range option. But you can also restrict selective date in DatePicker calendar by utilizing [beforeDateCreate](https://help.syncfusion.com/api/js/ejdatepicker#events:beforedatecreate) event. This event will get triggered at each date creation. So you can disable the selective date in this event to restrict the user.

{% highlight javascript %}

       $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                beforeDateCreate: "restrictDate" // handler to listen each date create.

            });

        });

        //event get triggered for each date create.

        function restrictDate(args) {

            //date to disable in DatePicker calendar to restrict selection.

            var disableDate = new Date("09/22/2015");

            //compares two and adds the disable class.

            if (+args.date === +disableDate)

                args.element.addClass('e-disable');

            // args contains current date and its element.          

        }


{% endhighlight %}

## How to add clear button with DatePicker?

Clear button can be included in the DatePicker control. In the `created` event of DatePicker, clear button element should be appended in the input element and event for clearing the value should bind with the clear button element. Refer the sample from the link [Clear button](http://jsplayground.syncfusion.com/mmdn4d0q) to know how to add the clear button with the DatePicker component.

{% highlight html %}

    <div class="control">
        <label>Select Date</label>
            <input id="datepick" type="text" />
    </div>

<style>
    .e-clear-date {
        text-align: center;
        position: absolute;
        right: 24px;
        top: 0;
        line-height: 2;
        background: #ececec;
        width: 21px !important;
        height: 28px !important;
        margin-top: -14px !important;
    }

    .e-clear-date:hover {
       background: #86cbea;
       cursor: pointer;
    }

    .e-clear-date:before {
       content: "\e605";
       font-size: 16px;
       line-height: 1.8;
   }
</style>

{% endhighlight %}

{% highlight javascript %}

 function onCreate(e) {
        if (this.innerWrapper.find('.e-clear-date').length == 0) {
            this.innerWrapper.append("<span class='e-clear-date e-icon'></span>"); // create and append the 'div' element to the calendar
            this._on($('.e-clear-date', this.innerWrapper), "click", function () { this.option('value', null); if (!this.model.displayInline) this.hide(); }); // bind the 'Click' event to that 'div' element
        }
    }

{% endhighlight %}


## How to integrate with bootstrap grid system? 

DatePicker is responsive control, you have to just set the input element width as 100%. In Bootstrap grid layout use the below code example to get responsive textbox. 

{% highlight javascript %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                width: '100%'// sets width as 100 percentage

            });

        });

{% endhighlight %}

## How to use DatePicker in AngularJS?

You can use DatePicker control in AngularJS Framework. To know more about JS component with AngularJS refer here [JS component in AngularJS](https://help.syncfusion.com/js/angularjs).

