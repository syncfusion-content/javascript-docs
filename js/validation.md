---
title: jQuery validation for EJ widgets
description: How to perform jQuery validation in Essential JS widgets
platform: JS
control: Introduction
documentation: UG
keywords: Syncfusion EJ widgets, UG document, jQuery validation
---
# Client Side validation for EJ widgets

Using jQuery validation, you can perform the client side validation for our EJ widgets. Please refer following steps to achieve this.

**Step 1:** To perform jQuery validation, you need to include the latest version of [jquery.validate](http://www.nuget.org/packages/jQuery.Validation/#) and [jquery.validate.unobtrusive](http://www.nuget.org/packages/Microsoft.jQuery.Unobtrusive.Validation/#) scripts in your HTML page.

**Step 2:** jQuery contains some default settings for the validation and it ignores hidden elements in form validation. But some of our EJ components (“Checkbox”, “MaskEdit”, ”NumericTextbox”, “CurrencyTextbox”, “PercentageTextbox”, “RTE”, “Dropdownlist” ) contains hidden fields with values, these
values need to be validated at here. So to perform the validation properly, you have to set “[]” in “ignore” API of “$.validator.setDefaults”. 

If validation gets fail, built-in “error” class will be added to corresponding element. Here you can specify a custom class with your own style using “errorClass” API and you can place the error message in necessary position using “errorPlacement” API. Refer following code block to customize the default jQuery validation settings.

    
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

Previously, we have specified above settings in source level, but it creates problems in validation behavior. Also user not able to override the inner settings, which is available in source.

In form validation, these settings are common for all controls that is available in the form. So you need to provide this custom settings in sample level and you can customize it as per your requirement.
 
**Step 3:** Specify the validation rules and messages using the APIs (“validationRules”, “validationMessage”), which is available in the validation supportable EJ controls.
 

    {% highlight javascript %}
    
        $("#datepick").ejDatePicker({
            validationRules: {
                required: true
            },
            validationMessage: {
                required: "Required Date value"
            }
        });
        
    {% endhighlight %}
    

We have prepared a sample based on this and you can find sample under the following location 

Sample: [http://jsplayground.syncfusion.com/dobcyify](http://jsplayground.syncfusion.com/dobcyify#)
 
Also you may create custom rules for validation. Please refer following sample to perform custom validation in “DatePicker” component.

Sample: [http://jsplayground.syncfusion.com/irf1eldu](http://jsplayground.syncfusion.com/irf1eldu#) 
