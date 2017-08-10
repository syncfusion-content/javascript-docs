---
title: JQuery validation
description: How to perform jQuery validation for EJ form controls
platform: js
control: Introduction
documentation: UG
keywords: Validation, jQuery validation, Client side validation
---
# Validation 

## jQuery Validation

To perform the jQuery validation for EJ form controls, please refer following steps.

**Step 1:** First you need to include [jquery.validate](http://www.nuget.org/packages/jQuery.Validation/#) (1.15.0) script in your HTML page.

**Step 2:** After adding this script file, you can validate the EJ form controls in same way as you perform the jQuery validation for HTML form elements. But here you have to do some little bit configuration along with that.  Let we discuss about it.

If validation gets fail, you have to place the error message in proper position using “errorPlacement” API which is available in default settings of jQuery validation. Also built-in “error” class will be added to corresponding form element. Here you have to specify a custom class with your own style using “errorClass” API. These are the common settings for all of our EJ form controls.

And some of our EJ form controls contains the form values in hidden element for its functionality purpose and these hidden elements are not validated by default. If you want to include the hidden elements in jQuery validation, you have to set “[]” in “ignore” API of “$.validator.setDefaults”.  Refer following list to find out the EJ form controls, which contains the value in hidden element.

* Checkbox
* MaskEdit
* NumericTextbox
* CurrencyTextbox
* PercentageTextbox
* RTE
* Dropdownlist

Please refer following code block to configure the above mentioned jQuery validation settings.


    {% highlight javascript %}
    
      $.validator.setDefaults({
           //to validate all fields(hidden also)
           ignore: [],
           //if we don’t set custom class, default “error” class will be added
           errorClass: 'e-validation-error',
           //it specifies the error message display position
           errorPlacement: function (error, element) {
               $(error).insertAfter(element.closest(".e-widget"));
           }
       });

    {% endhighlight %}

Up to 13.4.0.58 version, above specified jQuery validation settings were configured in source level of EJ form controls. Since 14.1.0.41 release onwards, above specified settings has been removed from source and it need to be specified in sample level in order to improve the customization of this validation.

**Step 3:** After configuring above jQuery validation settings, you have to specify the validation rules and messages using the APIs (“validationRules”, “validationMessage”), which is available in the validation supportable EJ controls. 


    {% highlight javascript %}
    
        $("#datePicker").ejDatePicker({
            validationRules: {
                required: true
            },
            validationMessage: {
                required: "Required Date value"
            }
        });

    {% endhighlight %}

We have prepared a sample based on this and you can find sample under the following location.

Sample: [http://jsplayground.syncfusion.com/dobcyify](http://jsplayground.syncfusion.com/dobcyify#) 

Also you may create custom rules for validation. Please refer following sample to perform custom validation in “DatePicker” component.

Sample: [http://jsplayground.syncfusion.com/irf1eldu](http://jsplayground.syncfusion.com/irf1eldu#) 
