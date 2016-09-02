---
layout: post
title: ejRecurrenceEditor
description: Methods, Members and Events available in ejRecurrenceEditor
documentation: API
platform: js
keywords: ejRecurrenceEditor, API, Essential JS recurrence editor
---

# ejRecurrenceEditor

The **Recurrence Editor** includes the entire recurrence related information in a separate portable manner which can be either utilized as a separate widget or else can be embed within the appointment window of Scheduler to enable recurrence options within it. The recurrence rule can be easily generated based on the frequency selected. The customizations like changing the labels of the Recurrence Editor is also possible to achieve through its properties. The frequencies available are Never, Daily, Weekly, Monthly, Yearly and Every weekday. 
  
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
* module:ej.checkbox.js
* module:ej.datepicker.js

## Members

### frequencies `array`
{:#members:frequencies}

Defines the collection of recurrence frequencies within Recurrence Editor such as Never, Daily, Weekly, Monthly, Yearly and Every Weekday.


#### Default Value

* ["never", "daily", "weekly", "monthly", "yearly", "everyweekday"]

#### Example - To set frequencies for Recurrence Editor.

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

Sets the starting day of the week.

#### Default Value

* null

#### Example - To set Tuesday as starting day of the week.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
              firstDayOfWeek: "tuesday"
            });
        });
</script>

{% endhighlight %}

### enableSpinners `boolean`
{:#members:enablespinners}

When set to true, enables the spin button of numeric textboxes within the Recurrence Editor.  

#### Default Value

* true

#### Example - To disable the spin button of numeric textboxes within Recurrence Editor.

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

Sets the start date of the recurrence. The Recurrence Editor initially displays the current date as its start date.

#### Default Value

* new Date()

#### Example - To set the specific starting date of Recurrence Editor.

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

Sets the specific culture to the Recurrence Editor.

#### Default Value

* "en-US"

#### Example - To set the French culture on Recurrence Editor, set its locale as fr-FR.

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

> To set any culture for Recurrence Editor, refer to the required minified globalize files of the specific culture. For example, to use fr-FR culture in Recurrence Editor, refer to the **globalize.culture.fr-FR.min.js** script file. Also define the locale words of that specific culture properly. For example, define the locale words for fr-FR culture in a variable ej.RecurrenceEditor.Locale[“fr-FR”] = { }; under script section.

### dateFormat `string`
{:#members:dateformat}

Sets the date format for the datepickers available within the Recurrence Editor.

#### Default Value

* ""

#### Example - To set the date format for Recurrence Editor.

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

### enableRTL `boolean`
{:#members:enablertl}

When set to true, renders the Recurrence Editor options from Right-to-Left direction.

#### Default Value

* false

#### Example - To set the enableRTL property for Recurrence Editor.

{% highlight html %}

<div id="RecurrenceEditor"></div>

<script type="text/javascript">
        $(function () {
            $("#RecurrenceEditor").ejRecurrenceEditor({
                enableRTL: true
             });
        });
</script>

{% endhighlight %}

### selectedRecurrenceType `number`
{:#members:selectedrecurrencetype}

Sets the active/current repeat type(frequency) on Recurrence Editor based on the index value provided. For example, setting the value 1 will initially set the repeat type as `Daily` and display its related options.   

#### Default Value

* 0

#### Example - To set the specific recurrence type for Recurrence Editor.

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

### minDate `object`
{:#members:mindate}

Sets the minimum date limit to display on the datepickers defined within the Recurrence Editor. Setting minDate with specific date value disallows the datepickers within  Recurrence Editor to navigate beyond that date.

#### Default Value
{:.param}

* new Date(1900, 01, 01)

#### Example - To set the minimum date on the Recurrence Editor.

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

Sets the maximum date limit to display on the datepickers used within the Recurrence Editor. Setting maxDate with specific date value disallows the datepickers within the Recurrence Editor to navigate beyond that date.

#### Default Value

* new Date(2099, 12, 31)

#### Example - To set the maximum date on the Recurrence Editor.

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

Accepts the custom CSS class name, that defines user-defined styles and themes to be applied on partial or complete elements of the Recurrence Editor. 

#### Default Value

* ""

#### Example - To simply customize the background color of Recurrence Editor by using custom CSS class name.

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

### getRecurrenceRule()
{:#methods:getrecurrencerule}


Generates the recurrence rule with the options selected within the Recurrence Editor.

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
schObj.getRecurrenceRule();
alert(schObj._recRule);
</script>

{% endhighlight %}


### recurrenceDateGenerator(recurrenceString, startDate)
{:#methods:recurrencedategenerator}

Generates the collection of date, that lies within the selected recurrence start and end date for which the recurrence pattern applies.

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
            <td class="description">It refers the recurrence rule.</td>
        </tr>
        <tr>
            <td class="name">startDate</td>
            <td class="type">object</td>
            <td class="description">It refers the start date of the recurrence.</td>
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
var recurrenceString = "FREQ=DAILY;INTERVAL=1;COUNT=10";
var startDate = new Date();
schObj.recurrenceDateGenerator(recurrenceString,startDate);
</script>

{% endhighlight %}

### recurrenceRuleSplit(recurrenceRule,exDate)
{:#methods:recurrencerulesplit}

 It splits and returns the recurrence rule string into object collection.

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
            <td class="description">It refers the recurrence rule string.</td>
        </tr>
        <tr>
            <td class="name">exDate</td>
            <td class="type">object</td>
            <td class="description">It refers the appointment dates (ExDate) to be excluded</td>
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
var recurrenceRule = "FREQ=DAILY;INTERVAL=1;COUNT=10";
var exDate ="11/2/2016"
schObj.recurrenceRuleSplit(recurrenceRule,exDate);
</script>

{% endhighlight %}

## Events

### change
{:#events:change}

Triggers whenever any of the Recurrence Editor’s value is changed.  

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
<td class="description">When set to true, event gets canceled.</td>
</tr>
<tr>
<td class="name">model</td>
<td class="type"><ts ref="ej.RecurrenceEditor.Model"/><span class="param-type">object</span></td>
<td class="description">Returns the Recurrence Editor model</td>
</tr>
<tr>
<td class="name">type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the name of the event</td>
</tr>
<tr>
<td class="name">recurrenceRule</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">Returns the recurrence rule value.</td>
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














