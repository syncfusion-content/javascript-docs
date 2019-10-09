---
layout: post
title: behavior settings | Syncfusion
description: Default behavior settings for Essential Studio JavaScript Syncfusion DateRangePicker to perform required operation.
platform: js
control: DateRangePicker
documentation: ug
api: /api/js/ejdaterangepicker
---

## Behavior Settings

DateRangePicker has some default behavior settings which helps you to perform more operation by Built-in.

### Selected Date Range

#### Value

DateRangePicker value can be selected through picking two date values from available two DatePicker calendar or you can set it by using **value** property.

{% highlight html %}


     $(function () {

            // creates DateRangePicker from input with some date range.

            $("#dateRangePicker").ejDateRangePicker({

                value: "11/1/2016 - 11/2/2017", // sets the date range

                onChange: "onChange" // sets handler to listen value change

            });

        });

        function onChange(args) {

            //args contains entire model of DateRangePicker to get the value of all properties.

            //alert DateRangePicker shows the start date and end date.

            alert(" start date is : " + args.startDate + " \n end date is : " + args.endDate);

        }
        
        
{% endhighlight %}

## Date Range

DateRangePicker provides an option to restrict the user to pick the date from specified range of value. You can utilize this option by make use of [minDate](https://help.syncfusion.com/api/js/ejdaterangepicker#members:mindate) and [maxDate](https://help.syncfusion.com/api/js/ejdaterangepicker#members:maxdate) property.

**minDate** - specifies the minimum date to be picked in DateRangePicker calendar by disabling below date of minDate.

**maxDate** -  specifies the maximum date to be picked in DateRangePicker calendar by disabling above date of maxDate. 

{% highlight javascript %}
     
	   $(function () {
 
            $("#dateRangePicker").ejDateRangePicker({

                minDate: new Date("06/03/2017"), // sets min date to be pick able in DateRangePicker calendar

                maxDate: new Date("07/23/2017") // sets max date to be pick able in DateRangePicker calendar

            });

        });      

{% endhighlight %}

![minmax](minmax_images\minmax_img.png)

#### Separator

The value of the DateRangePicker popup will presented with two date strings which is separated by **separator** (e.g. “"11/1/2016 - 11/2/2017"”). Separator will be “- “by default and this can be changed using API called **separator**. Please check with below code example to setting/changing the separator using **separator** API.


{% highlight html %}


     $(function () {

            // creates DateRangePicker from input with some date range.

            $("#dateRangePicker").ejDateRangePicker({

                value: "11/1/2016 - 11/2/2017", // sets the date range

                separator: "&" // sets the separator to & instead of "-"

            });

        });


{% endhighlight %}


![separator](separator_images\separator_img1.png)

#### Start Date

Start Date of the date range can be pick from date range picker calendar. We can select the start date from any one of calendar in a popup.

While selecting the date on calendar in following cases, the clicked date will be considered as StartDate.

1. Click on empty calendar (with no start date, range, end date)

2. Click on date which is lesser than existing start date

3. Click on calendar when already there is start date and end date is updated.



Start Date of range, can be set using API called **startDate** also please refer the below code example:

{% highlight html %}


      $("#dateRangePicker").ejDateRangePicker({
                startDate: new Date("11/2/2016")
        });


{% endhighlight %}


**startDate** can be set to popup, by entering the date value into first input box in popup also.



#### End Date

End Date of the date range can be selected from popup directly. Else this can be also updated by using the API called “**endDate**”.

The Selection next to the **startDate** will be considered as end Date. This selected date should be higher or equal date than the existing start date.  Else this selection will be considered as **startDate** as we discussed in **startDate** section above.

Below code will explain to use the **endDate** API to set the end Date in popup.

{% highlight html %}


         $("#dateRangePicker ").ejDateRangePicker({

                startDate: new Date("11/2/2016"),

                endDate: new Date("11/3/2018")

           });


{% endhighlight %}



End Date can be set to popup by entering the date into the second input box in popup


### Preset Ranges

We can make use of preset range for easy selection on popup. The ranges provided with this API **presetRanges**, will be processed and corresponding label will be added to popup in right side with given label name. By clicking on these labels the associated ranges will be updated in popup. The below code will explain to use **presetRanges** API.

{% highlight html %}


           $(function () {

            // creates DateRangePicker with preset ranges.

            $("#dateRangePicker").ejDateRangePicker({

                ranges: [

                    { label: "Today", range: [new Date(), new Date()] },

                    { label: "Last 1 Week", range: [new Date(new Date().setDate(new Date().getDate() - 7)), new Date()] },

                    { label: "Last 1 Month", range: [new Date(new Date().setMonth(new Date().getMonth() - 1)), new Date()] },

                    { label: "Last 2 Month", range: [new Date(new Date().setMonth(new Date().getMonth() - 2)), new Date()] },

                ],

            });

        });


{% endhighlight %}


![preset](presetranges_images\presetranges_img1.png)

These ranges can be processed and updated to popup by using the **setRange** method also like below code example.

//bind below onClick action to button


{% highlight js %}

        function onClick() {

            //create instance for dateRangePicker.

            // create instance only after control creation, to get dateRangeObj otherwise it throws exception.

            var dateRangeObj = $("#dateRangePicker").ejDateRangePicker('instance');

            //call setRange using label

            dateRangeObj.setRange("Last 1 Week");

            //get value using date range object and displays in alert box

            alert(dateRangeObj.option('value'));
        }


{% endhighlight %}


### TimePicker Option

The ranges can be set with time value also by enable the TimePicker in popup using **enableTimePicker** API. Each start date and end date, have separate Time Pickers. Please check with the below code example to enable the time picker.

{% highlight js %}


        $("#dateRangePicker ").ejDateRangePicker({
            enableTimePicker: true

        });


{% endhighlight %}

![option](timepickeroption_images\timepickeroption_img1.png)

## Backward Date Selection

DateRangePicker value can be selected through picking two date values from right calender to left calender.

{% highlight javascript %}
     
	   $(function () {
 
            $("#dateRangePicker").ejDateRangePicker({

               backwardSelection:true // right to left date selection

            });

        });      

{% endhighlight %}

## Validation

DateRangePicker can be validated using name attribute through jQuery validation. Map the component name attribute with jQuery validation rule, and add required error message to be displayed during validation. Error message can be placed below the control using `setDefaults` of jQuery validator. Refer to the following code.

 {% highlight html %}
     
        <form id="form">
	       <input id="date" name="range" type="text" />  
           <br/>
           <input type="submit" value="post" />
      </form>

{% endhighlight %}

{% highlight javascript %}
     
            $.validator.setDefaults({
                ignore: [],
                errorClass: 'e-validation-error',
                errorPlacement: function (error, element) {
                    $(error).insertAfter(element.closest(".e-widget"));
                }
            });

            $(function()
              {
                $("#form").validate({
                    rules: {
                        //need to map the rule with component name attribute
                        range: "required",
                },
                messages: {
                   "range": {
                      required: "Required Date value"
                 }
                  }
             });
                 $("#date").ejDateRangePicker();
              }) 

{% endhighlight %}

Refer to the sample [here](https://jsplayground.syncfusion.com/dcot5m3b)