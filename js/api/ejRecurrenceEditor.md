---
layout: post
title: ejRecurrenceEditor
description: Methods, Members and Events available in ejRecurrenceEditor
documentation: API
platform: js
keywords: ejRecurrenceEditor, API, Essential JS recurrence editor
---

# ejRecurrenceEditor

The recurrence editor used to create the recurrence appointment in event calender and also generate the recurrence rule separtely.
  
#### Syntax

{% highlight js %}

$(element).ejRecurrenceEditor()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="RecurrenceEditor"></div> 
 
<script>
$('#RecurrenceEditor').ejRecurrenceEditor();         
</script>

{% endhighlight %}


#### Requires

* module:jQuery
* module:jquery.easing.min.js
* module:jsrender.min.js
* module:ej.globalize.min.js
* module:ej.core.js
* module:ej.recurrenceeditor.js
* module:ej.scroller.js
* module:ej.radiobutton.js
* module:ej.editor.js
* module:ej.dropdownlist.js
* module:ej.button.js
* module:ej.checkbox.js
* module:ej.datepicker.js
* module:ej.togglebutton.js

## Members

### frequencies `array`
{:#members:frequencies}

Defines the frequencies collection to be displayed on the recurrenceeditor. By default, it displays all the frequencies namely, Never, Daily, Weekly, Monthly, Yearly, Everyweekday.


#### Default Value

* ["never", "daily", "weekly", "monthly", "yearly", "everyweekday"]

#### Example - To display the daily, weekly, monthly, yearly, everyweekday view on the RecurrenceEditor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
              frequencies: ["daily", "weekly", "monthly", "yearly", "everyweekday"]
            });
        });
</script>

{% endhighlight %}

### firstDayOfWeek `string`
{:#members:firstdayofweek}

You can change or set the starting day of the week.

#### Default Value

* null

#### Example - To set Tuesday as starting day of the week.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
              firstDayOfWeek:true
            });
        });
</script>

{% endhighlight %}

### value `string`
{:#members:name}

You can change or set the value to the Recurrence Editor.

#### Default Value

* ""

#### Example - To set RecurrenceEditor value to the recurrence editor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
               value:"RecurrenceEditor"
            });
        });
</script>

{% endhighlight %}

### enableSpinners `boolean`
{:#members:enablespinners}

When set to true, recurrenceeditor allows to enable the spin button in numeric textbox. 

#### Default Value

* true

#### Example - To disable the spin button for numeric textbox.

{% highlight html %}
 
<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
		            enableSpinners: false
            });
        });
</script>

{% endhighlight %}

### startDate `object`
{:#members:startdate}

Sets current date of the RecurrenceEditor. The RecurrenceEditor displays initially with the date that is provided here.

#### Default Value

* new Date()

#### Example - To set current date for RecurrenceEditor.

{% highlight html %}
 
<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
		          startDate:new Date(2014,4,5)
            });
        });
</script>

{% endhighlight %}

### locale `string`
{:#members:locale}

Sets the specific culture to the RecurrenceEditor.

#### Default Value

* "en-US"

#### Example - To set the French culture on RecurrenceEditor, set its locale as fr-FR.

{% highlight html %}
 
<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
		         locale: "fr-FR"
            });
        });
</script>

{% endhighlight %}

> To set any culture for Recurrenceeditor, refer to the required minified globalize files of the specific culture. For example, to use fr-FR culture in RecurrenceEditor, refer to the **globalize.culture.fr-FR.min.js** script file. Also define the locale words of that specific culture properly. For example, define the locale words for fr-FR culture in a variable ej.RecurrenceEditor.Locale[“fr-FR”] = { }; under script section.

### dateFormat `string`
{:#members:dateformat}

Sets the date format for RecurrenceEditor.

#### Default Value

* ""

#### Example - To set the date format for RecurrenceEditor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                dateFormat: "yyyy-MM-dd"
             });
        });
</script>

{% endhighlight %}

### selectedRecurrenceType `number`
{:#members:selectedrecurrencetype}

when a sets the selected recurrence type for RecurrenceEditor, the recurrence type has changed based on the value of selected recurrence type. 

#### Default Value

* 0

#### Example - To set the selected recurrence type for RecurrenceEditor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                selectedRecurrenceType: 0
             });
        });
</script>

{% endhighlight %}

### enableRecurrenceValidation `boolean`
{:#members:enablerecurrencevalidation}

When set to true, Recurrence editor allows the validation of recurrence pattern to take place before it is being assigned to the appointments. For example, when one of the instance of recurrence appointment is dragged beyond the next or previous instance of the same recurrence appointment, a pop-up is displayed with the validation message disallowing the drag functionality. 

#### Default Value

* true

#### Example - To disable the RecurrenceValidation for recurrrence editor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                enableRecurrenceValidation: false
            });
        });
</script>

{% endhighlight %}

### minDate `object`
{:#members:mindate}

Sets the minimum date limit to display on the Recurrence Editor. Setting minDate with specific date value disallows the RecurrenceEditor to navigate beyond that date.

#### Default Value
{:.param}

* new Date(1900, 01, 01)

#### Example - To set the minimum date on the Recurrence Edior.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                startDate: new Date(2014, 04, 05),
                minDate: new Date(2014, 04, 03),
            });
        });
</script>

{% endhighlight %}

### maxDate `object`
{:#members:maxdate}

Sets the maximum date limit to display on the RecurrenceEditor. Setting maxDate with specific date value disallows the RecurrenceEditor to navigate beyond that date.

#### Default Value

* new Date(2099, 12, 31)

#### Example - To set the maximum date on the RecurrenceEditor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                startDate: new Date(2014, 04, 05),
                maxDate: new Date(2014, 04, 06),
            });
        });
</script>

{% endhighlight %}

### cssClass `string`
{:#members:cssclass  }

#### Default Value

* ""

Accepts the custom CSS class name that defines specific user-defined styles and themes to be applied for partial or complete elements of the RecurrenceEditor. 

#### Example - To simply customize the background color of RecurrenceEditor Recurrencetype element by using custom css class name.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<style type="text/css">
    .customStyle .e-textlabel {
        background-color: Teal;
    }
</style>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                    cssClass: "customStyle", 
            });
        });
</script>

{% endhighlight %}

> For more information on applying custom themes to Syncfusion controls, refer [here](/js/theming-in-essential-javascript-components#customizing-themes).

## Methods

### closeRecurPublic()
{:#methods:closerecurpublic}


recurrence rule generates to the RecurreneEditor.

#### Example


{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                startDate: new Date(2014, 04, 05)
            });
        });

var schObj = $("#RecurrenceEditor").data("ejRecurrenceEditor");
schObj.closeRecurPublic();
alert(schObj._recRule);
</script>

{% endhighlight %}


### recurrenceDateGenerator(recurrenceString,startDate)
{:#methods:recurrencedategenerator}

 Generates the collection of the date which render the Recurrence appointment.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">recurrenceString</td>
            <td class="type">string</td>
            <td class="description">It refers recurrence rule for the recurrence editor.</td>
        </tr>
        <tr>
            <td class="name">startDate</td>
            <td class="type">object</td>
            <td class="description">It refers the date object of the appointment</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                startDate: new Date(2014, 04, 05)
            });
        });

var schObj = $("#RecurrenceEditor").data("ejRecurrenceEditor");
schObj.recurrenceDateGenerator();
</script>

{% endhighlight %}

### recurrenceRuleSplit(recurrenceRule,appointment)
{:#methods:recurrencerulesplit}

 return the recurrence rule string into splitted collection of the object.

<table class="params">
    <thead>
        <tr>
            <th>Name</th>
            <th>Type</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td class="name">recurrenceRule</td>
            <td class="type">string</td>
            <td class="description">It refers recurrence rule for the recurrence editor.</td>
        </tr>
        <tr>
            <td class="name">recurrenceRule</td>
            <td class="type">object</td>
            <td class="description">It refers the date object of the appointment</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                startDate: new Date(2014, 04, 05)
            });
        });

var schObj = $("#RecurrenceEditor").data("ejRecurrenceEditor");
schObj.recurrenceRuleSplit(recurrenceRule,appointment);
</script>

{% endhighlight %}

## Events

### change
{:#events:change}

Fires the action when the recurrence Editor control’s value is changed. 

<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the Recurrence Editor model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">recurreneceRule</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the recurreneceRule value.</td>
</tr>
</tbody>
</table>


#### Example

{% highlight html %}
 
 <div id="RecurrenceEditor"></div> 
 
 <script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                selectedRecurrenceType: 0,
                change: function(args)
                {                             
                    /*Do your changes */
                }
            });       
        });
    </script>
  {% endhighlight %}














