---
layout: post
title: Properties, Methods and Events of ejRadioButton Widget
description: API reference for ejRadioButton
documentation: API
platform: js
keywords: RadioButton, ejRadioButton, syncfusion, RadioButton api 
---

# ejRadioButton



The RadioButton control allows you to choose an option to perform an action. This control allows you to select true/false.




#### Syntax

{% highlight javascript %}

$(element).ejRadioButton()

{% endhighlight %}







#### Example



{% highlight html %}
<input type="radio" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1"> Fresher </label>
<script>
$("#radiobtn").ejRadioButton({checked:true});
$("#radiobtn1").ejRadioButton();
</script>{% endhighlight %}




#### Requires



* module:jQuery

* module:ej.core.js

* module:ej.radiobutton.js


## Members




### checked `boolean`
{:#members:checked}




Specifies the check attribute of the Radio Button.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set check API value during initialization  
        $("#radiobtn").ejRadioButton({ checked:  true });       
        $("#radiobtn1").ejRadioButton({ checked:  true });
</script>{% endhighlight %}




### cssClass `string`
{:#members:cssclass}




Specify the CSS class to RadioButton to achieve custom theme.


#### Default Value




* ""




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// Set the root class for RadioButton control theme. This cssClass API helps to use custom skinning option for RadioButton control. By defining the root class using this API, we need to include this root class in CSS.                       
        $("#radiobtn").ejRadioButton({cssClass: "gradient-lime"});
        $("#radiobtn1").ejRadioButton({cssClass: "gradient-lime"});
</script>{% endhighlight %}




### enabled `boolean`
{:#members:enabled}




Specifies the RadioButton control state.


#### Default Value




* true




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// Enable RadioButton on initialization. 
        //To set width API value 
         $("#radiobtn").ejRadioButton ({ enabled: true });      
         $("#radiobtn1").ejRadioButton ({ enabled: true });     
</script>{% endhighlight %}




### enablePersistence `boolean`
{:#members:enablepersistence}




Specifies the enablePersistence property for RadioButton while initialization. The enablePersistence API save current model value to browser cookies for state maintains. While refreshing the radio button control page the model value apply from browser cookies.


#### Default Value




* false




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// To set enablePersistence API value 
$("#radiobtn").ejRadioButton({ enablePersistence: false });     
$("#radiobtn1").ejRadioButton({ enablePersistence: false });
</script>{% endhighlight %}




### enableRTL `boolean`
{:#members:enablertl}




Specify the Right to Left direction to RadioButton


#### Default Value




* false




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// Set the enableRTL during initialization.                     
        $("#radiobtn").ejRadioButton({  enableRTL:true });      
        $("#radiobtn1").ejRadioButton({  enableRTL:true });     
</script>{% endhighlight %}




### htmlAttributes `object`
{:#members:htmlattributes}




Specifies the HTML Attributes of the Checkbox


#### Default Value




* {}




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// Set the htmlAttributes during initialization.                        
        $("#radiobtn").ejRadioButton({ htmlAttributes: {disabled:"disabled"} });        
</script>{% endhighlight %}




### id `string`
{:#members:id}




Specifies the id attribute for the Radio Button while initialization.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input type="radio" name="radiobtn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobtn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set id API value during initialization  
        $("#radiobtn").ejRadioButton({  id: "sync" });
        $("#radiobtn1").ejRadioButton({  id: "sync1" });
</script>{% endhighlight %}




### idPrefix `string`
{:#members:idprefix}




Specify the idPrefix value to be added before the current id of the RadioButton.


#### Default Value




* "ej"




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// To set  idPrefix  API value
$("#radiobtn").ejRadioButton ({  idPrefix : "ej" }); 
$("#radiobtn1").ejRadioButton ({  idPrefix : "ej" }); 
</script>{% endhighlight %}




### name `string`
{:#members:name}




Specifies the name attribute for the Radio Button while initialization.


#### Default Value




* Sets id as name if it is null







### size `enum`
{:#members:size}



<ts name="ej.RadioButtonSize"/>

Specifies the size of the RadioButton.


<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Small</td>
<td class="description">Shows small size radio button</td>
</tr>
<tr>
<td class="name">
Medium</td>
<td class="description">Shows medium size radio button</td>
</tr>
</tbody>
</table>




#### Default Value




* "small"




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set size API value during initialization  
        $("#radiobtn").ejRadioButton({  size: "medium"});       
        $("#radiobtn1").ejRadioButton({  size: "medium"});
</script>{% endhighlight %}




### text `string`
{:#members:text}




Specifies the text content for RadioButton.


#### Default Value




* ""







### validationMessage `object`
{:#members:validationmessage}




Set the jquery validation error message in radio button.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set validationMessage API during initialization  
$("#radiobtn").ejRadioButton ({   
  validationRules:{                     
          required:true
        },
  validationMessage: {
          required: "Required Radio value"
        }
});
$("#radiobtn1").ejRadioButton ();
</script>{% endhighlight %}




### validationRules `object`
{:#members:validationrules}




Set the jquery validation rules in radio button.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set validationRules API during initialization  
$("#radiobtn").ejRadioButton ({   
  validationRules:{                     
          required:true
        }
});
$("#radiobtn1").ejRadioButton ();
</script>{% endhighlight %}




### value `string`
{:#members:value}




Specifies the value attribute of the Radio Button.


#### Default Value




* null




#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
//To set value API value during initialization  
        $("#radiobtn").ejRadioButton({ value: "Experienced"});
        $("#radiobtn1").ejRadioButton({ value: "Fresher"});
</script>         {% endhighlight %}



## Methods




### disable()
{:#methods:disable}




To disable the RadioButton



#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>           
<script> 
// Create RadioButton
$("#radiobtn").ejRadioButton();
var chkObj = $("#radiobtn").data("ejRadioButton");
chkObj.disable();
</script>{% endhighlight %}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script> 
// disable the RadioButton
$("#radiobtn").ejRadioButton();
$("#radiobtn").ejRadioButton("disable");        
</script>{% endhighlight %}




### enable()
{:#methods:enable}




To enable the RadioButton



#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script> 
// Create RadioButton
$("#radiobtn").ejRadioButton();
var chkObj = $("#radiobtn").data("ejRadioButton");
chkObj.enable();
</script>{% endhighlight %}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script> 
// enable the RadioButton
$("#radiobtn").ejRadioButton();
$("#radiobtn").ejRadioButton("enable"); 
</script>{% endhighlight %}



## Events




### beforeChange
{:#events:beforechange}




Fires before the RadioButton is going to changed its state successfully

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
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from RadioButton
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.RadioButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true if element is checked, otherwise returns false</td>
</tr>
<tr>
<td class="name">
isInteraction</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true if change event triggered by interaction, otherwise returns false</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>   
<script>
//beforeChange event for RadioButton
$("#radiobtn").ejRadioButton({
  beforeChange:function (args){ }
});  
</script>         {% endhighlight %}




### change
{:#events:change}




Fires when the RadioButton state is changed successfully

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
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from RadioButton
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.RadioButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true if element is checked, otherwise returns false</td>
</tr>
<tr>
<td class="name">
isInteraction</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns true if change event triggered by interaction, otherwise returns false</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script>
//change event for RadioButton
$("#radiobtn").ejRadioButton({
  change: function (args){}
}); 
</script>          {% endhighlight %}




### create
{:#events:create}




Fires when the RadioButton created successfully

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
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from RadioButton
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.RadioButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script>
// //create event for RadioButton
$("#radiobtn").ejRadioButton({
  create:function(args){}
}); 
</script>          {% endhighlight %}




### destroy
{:#events:destroy}




Fires when the RadioButton destroyed successfully

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
<td class="name">
argument</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description">Event parameters from RadioButton
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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><ts ref="ej.RadioButton.Model"/><span class="param-type">object</span></td>
<td class="description">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example



{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script>
// //destroy event for RadioButton
$("#radiobtn").ejRadioButton({
  destroy:function(args){}
}); 
</script>          {% endhighlight %}



