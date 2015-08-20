---
layout: post
title: ejRadioButton
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html RadioButton Control.





$(element).ejRadioButton<span class="signature">()</span>






Example
{:.example}


{% highlight html %}
<input type="radio" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1"> Fresher </label>
<script>
$("#radiobtn").ejRadioButton({checked:true});
$("#radiobtn1").ejRadioButton();
</script>{% endhighlight %}




Requires
{:.require}


* module:jQuery

* module:ej.core.js

* module:ej.radiobutton.js


## Members




### checked<span class="type-signature type boolean">Boolean</span>
{:#members:checked}




Specifies the check atribute of the Radio Button.


Default Value:
{:.param}



* false




Example
{:.example}


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




### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}




Specify the CSS class to RadioButton to achieve custom theme.


Default Value:
{:.param}



* ""




Example
{:.example}


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




### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}




Specifies the RadioButton control state.


Default Value:
{:.param}



* true




Example
{:.example}


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




### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}




Specifies the enablePersistence property for RadioButton while initialization. The enablePersistence API save current model value to browser cookies for state maintains. While refreshing the radiobutton control page the model value apply from browser cookies.


Default Value:
{:.param}



* false




Example
{:.example}


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




### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}




Specify the Right to Left direction to RadioButton


Default Value:
{:.param}



* false




Example
{:.example}


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




### htmlAttributes<span class="type-signature type object">object</span>
{:#members:htmlattributes}




Specifies the HTML Attributes of the Checkbox


Default Value:
{:.param}



* {}




Example
{:.example}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<br/> <input type="radio" name="radiobutn" id="radiobtn1"/>
<label for="radiobtn1">Fresher </label>
<script>
// Set the htmlAttributes during initialization.                        
        $("#radiobtn").ejRadioButton({ htmlAttributes: {disabled:"disabled"} });        
</script>{% endhighlight %}




### id<span class="type-signature type string">String</span>
{:#members:id}




Specifies the id attribute for the Radio Button while initialization.


Default Value:
{:.param}



* null




Example
{:.example}


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




### idPrefix<span class="type-signature type string">String</span>
{:#members:idprefix}




Specify the idprefix value to be added before the current id of the RadioButton.


Default Value:
{:.param}



* "ej"




Example
{:.example}


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




### name<span class="type-signature type string">String</span>
{:#members:name}




Specifies the name attribute for the Radio Button while initialization.


Default Value:
{:.param}



* Sets id as name if it is null







### size<span class="type-signature type enum">enum</span>
{:#members:size}




Specifies the size of the RadioButton. See <a href="global.html#RadioButtonSize">RadioButtonSize</a>


Default Value:
{:.param}



* "small"




Example
{:.example}


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




### text<span class="type-signature type string">string</span>
{:#members:text}




Specifies the text content for RadioButton.


Default Value:
{:.param}



* ""







### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}




Set the jquery validation error message in radio button.


Default Value:
{:.param}



* null




Example
{:.example}


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




### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}




Set the jquery validation rules in radio button.


Default Value:
{:.param}



* null




Example
{:.example}


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




### value<span class="type-signature type string">String</span>
{:#members:value}




Specifies the value atribute of the Radio Button.


Default Value:
{:.param}



* null




Example
{:.example}


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




### destroy<span class="signature">()</span>
{:#methods:destroy}




destroy the RadioButton widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.



Example
{:.example}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script> 
// Create RadioButton
$("#radiobtn").ejRadioButton();
var chkObj = $("#radiobtn").data("ejRadioButton");
chkObj.destroy();
</script>{% endhighlight %}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script>
// enable the RadioButton
$("#radiobtn").ejRadioButton();
$("#radiobtn").ejRadioButton("destroy");        
</script>{% endhighlight %}




### disable<span class="signature">()</span>
{:#methods:disable}




To disable the RadioButton



Example
{:.example}


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




### enable<span class="signature">()</span>
{:#methods:enable}




To enable the RadioButton



Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from RadioButton
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data.element{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from RadioButton
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data.element{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name">{% highlight html %}
data.isChecked{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the status of the element</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from RadioButton
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


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
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
argument{% endhighlight %}</td>
<td class="type"><span class="param-type">Object</span></td>
<td class="description last">Event parameters from RadioButton
<table class="params">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">{% highlight html %}
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the RadioButton model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


Example
{:.example}


{% highlight html %}
 
<input type="radio" name="radiobutn" id="radiobtn"/>
<label for="radiobtn">Experienced</label>
<script>
// //destroy event for RadioButton
$("#radiobtn").ejRadioButton({
  destroy:function(args){}
}); 
</script>          {% endhighlight %}



