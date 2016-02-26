---
layout: post
title: ejTextBoxes
description: API reference for ejTextBoxes
documentation: API
platform: js
keywords: TextBoxes, ejTextBoxes, syncfusion, TextBoxes api  
---

# ejTextBoxes



 NumericTextBox is used to display only numeric values. It has Spin buttons to increase or decrease the values in the Text Box.

 CurrencyTextBox is used to display only currency values. it has Spin buttons to increase or decrease the values in the Text Box.

 PercentageTextBox control is used to display only percentage values. It has Spin buttons to increase or decrease the values in the Text Box.





#### Syntax

{% highlight js %}

$(element).ejNumericTextbox()

$(element).ejCurrencyTextbox()

$(element).ejPercentageTextbox()

{% endhighlight %}







#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
// Create Textbox Editors 
$('#numeric').ejNumericTextbox({value:10}); 
        
$('#currency').ejCurrencyTextbox({value:1000}); 
$('#percentage').ejPercentageTextbox({value:100}); 
</script>{% endhighlight %}




#### Requires



* module:jQuery

* module:ej.core.js

* module:ej.globalize.js

* module:ej.editor.js


## Members




### cssClass `string`
{:#members:cssclass}



Sets the root CSS class for Accordion theme, which is used customize. 


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set cssClass API value during initialization  
        $("#numeric").ejNumericTextbox({ cssClass: "gradient-lime" , value:5 });        
        $("#currency").ejCurrencyTextbox({ cssClass: "gradient-lime", value:100  });
        $("#percentage").ejPercentageTextbox({ cssClass: "gradient-lime", value:505  });                         
</script>{% endhighlight %}




### decimalPlaces `number`
{:#members:decimalplaces}




DecimalPlaces declares the number of digits to be displayed right side of the value.


#### Default Value




* 0




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set decimalPlaces API value during initialization  
        $("#numeric").ejNumericTextbox({ decimalPlaces: 2, value:5  }); 
        $("#currency").ejCurrencyTextbox({ decimalPlaces: 2 , value:5 });
        $("#percentage").ejPercentageTextbox({ decimalPlaces: 2, value:5  });                    
</script>{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Specify the editor control state.


#### Default Value




* true




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set enabled API value during initialization  
        $("#numeric").ejNumericTextbox({ enabled: true, value:1200  }); 
        $("#currency").ejCurrencyTextbox({ enabled: true , value:50 });
        $("#percentage").ejPercentageTextbox({ enabled: true, value:100  });                     
</script>{% endhighlight %}




### enablePersistence `boolean`
{:#members:enablepersistence}




Specify the enablePersistence to editor to save current model value to browser cookies for state maintains


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set enablePersistence API value during initialization  
        $("#numeric").ejNumericTextbox({ enablePersistence: true, value:5  });  
        $("#currency").ejCurrencyTextbox({ enablePersistence: true, value:5  });
        $("#percentage").ejPercentageTextbox({ enablePersistence: true, value:5  });                     
</script>{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Specify the Right to Left Direction to editor.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set enableRTL API value during initialization  
        $("#numeric").ejNumericTextbox({ enableRTL: true, value:5  });  
        $("#currency").ejCurrencyTextbox({ enableRTL: true , value:45 });
        $("#percentage").ejPercentageTextbox({ enableRTL: true, value:567  });                   
</script>{% endhighlight %}




### enableStrictMode `boolean`
{:#members:enablestrictmode}




Strict mode option to restrict entering values defined outside the range in the editor.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set enableStrictMode API value during initialization  
        $("#numeric").ejNumericTextbox({ enableStrictMode: true, value:5  });   
        $("#currency").ejCurrencyTextbox({ enableStrictMode: true, value:55  });
        $("#percentage").ejPercentageTextbox({ enableStrictMode: true, value:555  });                   
</script>{% endhighlight %}


### groupSeparator `string`
{:#members:groupseparator}




It provides the options to get the customized character to separate the digits. If not set, the separator defined by the current culture.  


#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set enableStrictMode API value during initialization  
        $("#numeric").ejNumericTextbox({ groupSeparator: "-", value:5  });   
        $("#currency").ejCurrencyTextbox({ groupSeparator: "-", value:55  });
        $("#percentage").ejPercentageTextbox({ groupSeparator: "-", value:555  });                   
</script>{% endhighlight %}


### height `string`
{:#members:height}




Specifies the height of the editor.


#### Default Value




* 30pixel




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set height API value during initialization  
        $("#numeric").ejNumericTextbox({ height: "30px", value:5  });   
        $("#currency").ejCurrencyTextbox({ height: "30px", value:55  });
        $("#percentage").ejPercentageTextbox({ height: "30px", value:555  });                    
</script>{% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}



It allows to define the characteristics of the Editors control. It will helps to extend the capability of an HTML element.


#### Default Value




* {}




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To Set HtmlAttributes API value during initialization  
        $("#numeric").ejNumericTextbox({ htmlAttributes : {required:"required"} });     
        $("#currency").ejCurrencyTextbox({ htmlAttributes : {required:"required"}});
        $("#percentage").ejPercentageTextbox({ htmlAttributes : {required:"required"}});
</script>{% endhighlight %}




### incrementStep `number`
{:#members:incrementstep}




The Editor value increment or decrement based an increment step value.


#### Default Value




* 1




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set incrementStep API value during initialization  
        $("#numeric").ejNumericTextbox({ incrementStep: 2, value:5  }); 
        $("#currency").ejCurrencyTextbox({ incrementStep: 2 , value:55 });
        $("#percentage").ejPercentageTextbox({ incrementStep: 2, value:50  });                   
</script>{% endhighlight %}




### locale `string`
{:#members:locale}




Specifies the Localization info used by the editor.


#### Default Value




* en-US




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set locale API value during initialization  
        $("#numeric").ejNumericTextbox({ locale: "en-US", value:5  });  
        $("#currency").ejCurrencyTextbox({ locale: "en-US", value:5000  });
        $("#percentage").ejPercentageTextbox({ locale: "en-US", value:455  });                   
</script>{% endhighlight %}




### maxValue `number`
{:#members:maxvalue}




Specifies the maximum value of the editor.


#### Default Value




* Number.MAX_VALUE




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set maxValue API value during initialization  
        $("#numeric").ejNumericTextbox({ maxValue: 100, value:500  });  
        $("#currency").ejCurrencyTextbox({ maxValue: 100, value:550  });
        $("#percentage").ejPercentageTextbox({ maxValue: 100, value:50  });                      
</script>{% endhighlight %}




### minValue `number`
{:#members:minvalue}




Specifies the minimum value of the editor.


#### Default Value




* -(Number.MAX_VALUE) and 0 for Currency Textbox.




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set minValue API value during initialization  
        $("#numeric").ejNumericTextbox({ minValue: 50, value:55  });    
        $("#currency").ejCurrencyTextbox({ minValue: 50, value:5  });
        $("#percentage").ejPercentageTextbox({ minValue: 50, value:555  });                      
</script>{% endhighlight %}




### name `string`
{:#members:name}




Specifies the name of the editor.


#### Default Value




* Sets id as name if it is null.




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set name API value during initialization  
        $("#numeric").ejNumericTextbox({ name: "numeric", value:5  });  
        $("#currency").ejCurrencyTextbox({ name: "currency", value:55  });
        $("#percentage").ejPercentageTextbox({ name: "percentage", value:500  });                        
</script>{% endhighlight %}




### readOnly `boolean`
{:#members:readonly}




Toggles the readonly state of the editor. When the Editor is readonly it doesn't allow user interactions.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set readOnly API value during initialization  
        $("#numeric").ejNumericTextbox({ readOnly: true , value:5 });   
        $("#currency").ejCurrencyTextbox({ readOnly: true , value:5 });
        $("#percentage").ejPercentageTextbox({ readOnly: true , value:5 });                      
</script>{% endhighlight %}




### showRoundedCorner `boolean`
{:#members:showroundedcorner}




Specify the rounded corner to editor


#### Default Value




* false




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set showRoundedCorner API value during initialization  
        $("#numeric").ejNumericTextbox({ showRoundedCorner: true, value:5  });  
        $("#currency").ejCurrencyTextbox({ showRoundedCorner: true , value:5 });
        $("#percentage").ejPercentageTextbox({ showRoundedCorner: true, value:5 });                      
</script>{% endhighlight %}




### showSpinButton `boolean`
{:#members:showspinbutton}




Specifies whether the up and down spin buttons should be displayed in editor.


#### Default Value




* true




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set showSpinButton API value during initialization  
        $("#numeric").ejNumericTextbox({ showSpinButton: false, value:5  });    
        $("#currency").ejCurrencyTextbox({ showSpinButton: false, value:55  });
        $("#percentage").ejPercentageTextbox({ showSpinButton: false, value:580  });                     
</script>{% endhighlight %}




### validateOnType `number`
{:#members:validateontype}




Enables decimal separator position validation on type .


#### Default Value




* 0




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set decimalPlaces API value during initialization  
        $("#numeric").ejNumericTextbox({ validateOnType: true, value:5  });     
        $("#currency").ejCurrencyTextbox({ validateOnType: true , value:5 });
        $("#percentage").ejPercentageTextbox({ validateOnType: true, value:5  });                        
</script>{% endhighlight %}




### validationMessage `object`
{:#members:validationmessage}




Set the jQuery validation error message in editor.

N> The property will work when the widget present inside the form. Additionally need to include jquery.validate.min.js plugin.



#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set validationMessage API value during initialization  
        $("#numeric").ejNumericTextbox({ validationRules:{required:true},validationMessage: { required: "Required Numeric value"} });   
        $("#currency").ejCurrencyTextbox({ validationRules:{required:true},validationMessage: { required: "Required Currency value"} });
        $("#percentage").ejPercentageTextbox({ validationRules:{required:true},validationMessage: { required: "Required Percentage value"} });                   
</script>{% endhighlight %}




### validationRules `object`
{:#members:validationrules}




Set the jQuery validation rules to the editor.

N> The property will work when the widget present inside the form. Additionally need to include jquery.validate.min.js plugin.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set validationRules API value during initialization  
        $("#numeric").ejNumericTextbox({ validationRules:{required:true} });    
        $("#currency").ejCurrencyTextbox({ validationRules:{required:true} });
        $("#percentage").ejPercentageTextbox({ validationRules:{required:true} });                       
</script>{% endhighlight %}




### value `number`
{:#members:value}




Specifies the value of the editor.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set value API value during initialization  
        $("#numeric").ejNumericTextbox({ value: 10 });  
        $("#currency").ejCurrencyTextbox({ value: 10 });
        $("#percentage").ejPercentageTextbox({ value: 10 });                     
</script>{% endhighlight %}




### watermarkText `string`
{:#members:watermarktext}




Specify the watermark text to editor.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set watermarkText API value during initialization  
        $("#numeric").ejNumericTextbox({ watermarkText: "Enter the value" });   
        $("#currency").ejCurrencyTextbox({ watermarkText: "Enter the currency value" });
        $("#percentage").ejPercentageTextbox({ watermarkText: "Enter the percentage" });                         
</script>{% endhighlight %}




### width `string`
{:#members:width}




Specifies the width of the editor.


#### Default Value




* 143pixel




#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//To set width API value during initialization  
        $("#numeric").ejNumericTextbox({ width: "143px", value:5 });    
        $("#currency").ejCurrencyTextbox({ width: "143px", value:55 });
        $("#percentage").ejPercentageTextbox({ width: "143px", value:555 });                    
</script>{% endhighlight %}



## Methods




### destroy()
{:#methods:destroy}




Allows you to destroy the Editor widgets.



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:5});
$("#currency").ejCurrencyTextbox({value:55});
$("#percentage").ejPercentageTextbox({value:555});
// Create Editors
var numObj = $("#numeric").data("ejNumericTextbox");
var curObj = $("#currency").data("ejCurrencyTextbox");
var perObj = $("#percentage").data("ejPercentageTextbox");
numObj.destroy(); // destroy the numericTextbox
curObj.destroy(); // destroy the currencyTextbox
perObj.destroy(); // destroy the percentagTextbox
</script>{% endhighlight %}


{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:5});
$("#currency").ejCurrencyTextbox({value:55});
$("#percentage").ejPercentageTextbox({value:555});
// destroy the editors
$("#numeric").ejNumericTextbox("destroy");
$("#currency").ejCurrencyTextbox("destroy");
$("#percentage").ejPercentageTextbox("destroy");                
</script>{% endhighlight %}




### disable()
{:#methods:disable}




To disable the corresponding Editors



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:20});
$("#currency").ejCurrencyTextbox({value:400});
$("#percentage").ejPercentageTextbox({value:2000});
// Create Editors       
var numObj = $("#numeric").data("ejNumericTextbox");
var curObj = $("#currency").data("ejCurrencyTextbox");
var perObj = $("#percentage").data("ejPercentageTextbox");
numObj.disable(); // disable the numericTextbox
curObj.disable(); // disable the currencyTextbox
perObj.disable(); // disable the percentagTextbox
</script>
                 {% endhighlight %}


{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:20});
$("#currency").ejCurrencyTextbox({value:400});
$("#percentage").ejPercentageTextbox({value:2000});
// disable the editors
$("#numeric").ejNumericTextbox("disable");
$("#currency").ejCurrencyTextbox("disable");
$("#percentage").ejPercentageTextbox("disable");                
</script>{% endhighlight %}




### enable()
{:#methods:enable}




To enable the corresponding Editors



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:10});
$("#currency").ejCurrencyTextbox({value:100});
$("#percentage").ejPercentageTextbox({value:1000});
// Create Editors
var numObj = $("#numeric").data("ejNumericTextbox");
var curObj = $("#currency").data("ejCurrencyTextbox");
var perObj = $("#percentage").data("ejPercentageTextbox");
numObj.enable(); // enable the numericTextbox
curObj.enable(); // enable the currencyTextbox
perObj.enable(); // enable the percentagTextbox
</script>
                
 {% endhighlight %}


{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:10});
$("#currency").ejCurrencyTextbox({value:100});
$("#percentage").ejPercentageTextbox({value:1000});
// enable the editors
$("#numeric").ejNumericTextbox("enable");
$("#currency").ejCurrencyTextbox("enable");
$("#percentage").ejPercentageTextbox("enable");         
</script>{% endhighlight %}




### getValue()
{:#methods:getvalue}




To get value from corresponding Editors



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:20});
$("#currency").ejCurrencyTextbox({value:500});
$("#percentage").ejPercentageTextbox({value:1000});
// Create Editors
var numObj = $("#numeric").data("ejNumericTextbox");
var curObj = $("#currency").data("ejCurrencyTextbox");
var perObj = $("#percentage").data("ejPercentageTextbox");
numObj.getValue(); // get value from numericTextbox
curObj.getValue(); // get value from currencyTextbox
perObj.getValue(); // get value from percentagTextbox
</script>
                 
  {% endhighlight %}


{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
$("#numeric").ejNumericTextbox({value:20});
$("#currency").ejCurrencyTextbox({value:500});
$("#percentage").ejPercentageTextbox({value:1000});
// get value from editors
$("#numeric").ejNumericTextbox("getValue");
$("#currency").ejCurrencyTextbox("getValue");
$("#percentage").ejPercentageTextbox("getValue");               
</script>{% endhighlight %}



## Events




### change
{:#events:change}




Fires after Editor control value is changed.


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the corresponding editor control value.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.isInteraction{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true when the value changed by user interaction otherwise returns false</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//change event for editors
$("#numeric").ejNumericTextbox({
          value:10,     
   change: function (args) {}
});
$("#currency").ejCurrencyTextbox({
          value:100,    
   change: function (args) {}
});
$("#percentage").ejPercentageTextbox({
          value:1000,   
   change: function (args) {}
});
</script>{% endhighlight %}




### create
{:#events:create}




Fires after Editor control is created.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the editor model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//create event for editors
$("#numeric").ejNumericTextbox({
          value:50,     
   create: function (args) {}
});
$("#currency").ejCurrencyTextbox({
          value:505,    
   create: function (args) {}
});
$("#percentage").ejPercentageTextbox({
          value:1500,   
   create: function (args) {}
});
</script>                  {% endhighlight %}




### destroy
{:#events:destroy}




Fires when the Editor is destroyed successfully.

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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the editor model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//destroy event for editors
$("#numeric").ejNumericTextbox({
          value:50,     
   destroy: function (args) {}
});
$("#currency").ejCurrencyTextbox({
          value:505,    
   destroy: function (args) {}
});
$("#percentage").ejPercentageTextbox({
          value:1500,   
   destroy: function (args) {}
});
</script>                  {% endhighlight %}




### focusIn
{:#events:focusin}




Fires after Editor control is focused.


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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the corresponding editor control value.</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//focusIn event for editors
$("#numeric").ejNumericTextbox({
          value:20,     
   focusIn: function (args) {}
});
$("#currency").ejCurrencyTextbox({
          value:200,    
   focusIn: function (args) {}
});
$("#percentage").ejPercentageTextbox({
          value:2000,   
   focusIn: function (args) {}
});
</script>{% endhighlight %}




### focusOut
{:#events:focusout}




Fires after Editor control is loss the focus.

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
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from editors.
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
<td class="name">{% highlight html %}
argument.cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the corresponding editor model.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
argument.value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the corresponding editor control value.</td>
</tr>
</tbody>
</table>



#### Example



{% highlight html %}
 
<input id="numeric" type="text" /> 
 
<input id="currency" type="text" /> 
 
<input id="percentage" type="text" /> 
 
<script>
//focusOut event for editors
$("#numeric").ejNumericTextbox({
          value:50,     
   focusOut: function (args) {}
});
$("#currency").ejCurrencyTextbox({
          value:505,    
   focusOut: function (args) {}
});
$("#percentage").ejPercentageTextbox({
          value:1500,   
   focusOut: function (args) {}
});
</script>{% endhighlight %}



