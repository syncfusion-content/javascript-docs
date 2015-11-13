---
layout: post
title: Validation
description: Validate the date using JQuery
platform: js
control: DatePicker
documentation: ug
---
# Validation

DatePicker is a form control and therefore its value to be validated before processing. Client side validation provides a better user experience by responding quickly at browser level. Most common client side validation plugin is “**[](http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js# "")**JQuery Validation”. 

DatePicker supports this validation by built-in, so you can do client validation with simple steps to validate and respond validation message. The jQuery validate plugin rules and custom methods can be used in the DatePicker control with the help of two properties, **[](http://help.syncfusion.com/js/api/ejdatepicker#members:validationrules "")**validationRules and **[](http://help.syncfusion.com/js/api/ejdatepicker#members:validationmessage "")**validationMessage. 

Before using those properties, you need to add the jQuery validate plugin to your html page.

<table>
<tr>
<td>
refer the below JQuery validation plugin script after JQuery script reference <br/><br/><script   src="http://ajax.aspnetcdn.com/ajax/jquery.validate/1.14.0/jquery.validate.min.js"></script><br/><br/><br/><br/></td></tr>
</table>

{% highlight html %}

    <!--form to submit-->

    <form>

        <!--input element to create DatePicker-->

        <input id="datePicker" />

        <!-- submit button -->

        <input type="submit" value="submit" />

    </form>


{% endhighlight %}

{% highlight js %}

        $(function () {

            // creates DatePicker from input

            $("#datePicker").ejDatePicker({

                validationRules: { required: true },// sets the field to be required

                validationMessage: { required: "Required Date value" } // sets validation message

            });

        });

{% endhighlight %}

N>  JQuery validation works only within the form element.

