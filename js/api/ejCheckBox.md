---
layout: post
title: ejCheckBox
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejCheckBox




The Checkbox control allows you to check an option to perform an action. This control allows you to select true, false or an intermediate option. These checkboxes are supported with themes. The html check box control is rendered as Essential JavaScript Checkbox control.





$(element).ejCheckBox<span class="signature">()</span>



Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
// Create Checkbox  
$("#chkbox").ejCheckBox(); 
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core.js


* module:ej.checkbox.js




## Members








### checked
{:#members:checked}








Specifies whether chechbox has to be in checked or not. We can also specify array of string as value for this property. If any of the value in the specified array matches the value of the textbox, then it will be considered as checked. It will be useful in MVVM binding, specify array type to identify the values of the checked checkboxes.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set check API value during initialization  
$("#chkbox").ejCheckBox({ checked:  true });
</script>{% endhighlight %}







### checkState<span class="type-signature type enum">enum</span>
{:#members:checkstate}








Specifies the State of ChecKBox.See <a href="global.html#CheckState">CheckState</a>




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set CheckState API value during initialization
$("#chkbox").ejCheckBox({ enableTriState: true , checkState:"indeterminate"});
</script>{% endhighlight %}







### cssClass<span class="type-signature type string">string</span>
{:#members:cssclass}








Specify the CSS class to CheckBox to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script>  
// Set the root class for Checkbox control theme. This cssClass API helps to use custom skinning option for Checkbox control. By defining the root class using this API, we need to include this root class in CSS.                     
$("#chkbox").ejCheckBox({cssClass: "gradient-lime"}); 
</script>{% endhighlight %}







### enabled<span class="type-signature type boolean">boolean</span>
{:#members:enabled}








Specifies the checkbox control state.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To Enable checkbox on initialization. 
//To set width API value 
$("#chkbox").ejCheckBox ({ enabled: true });
</script>{% endhighlight %}







### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members:enablepersistence}








Specifies the persist property for Checkbox while initialization. The persist API save current model value to browser cookies for state maintains. While refreshing the Checkbox control page the model value apply from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set persist API value 
$("#chkbox").ejCheckBox({ enablePersistence : false });
</script>{% endhighlight %}







### enableRTL<span class="type-signature type boolean">boolean</span>
{:#members:enablertl}








Specify the Right to Left direction to CheckBox




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
// Set the RTL during initialization.
$("#chkbox").ejCheckBox({  enableRTL : true });
</script>{% endhighlight %}







### enableTriState<span class="type-signature type boolean">boolean</span>
{:#members:enabletristate}








Specifies the enable or disable Tri-State for checkbox control.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
// Specifies to enable or disable Tri-State option checkbox while initialization. 
//To set enableTriState API value 
$("#chkbox").ejCheckBox({  enableTriState: true });
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
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//Set HtmlAttributes to Checkbox element during initialization  
$("#chkbox").ejCheckBox({ htmlAttributes : {required:"required"}});
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
 
<input id="mask" type="text" /> 
 
<script>
//To Set HtmlAttributes API value during initialization  
        $("#mask").ejMaskEdit({ htmlAttributes : {readOnly:"readOnly"}});                                        
</script> {% endhighlight %}







### id<span class="type-signature type string">String</span>
{:#members:id}








Specifies the id atribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set id API value during initialization  
$("#chkbox").ejCheckBox({  id: "sync" });
</script>{% endhighlight %}







### idPrefix<span class="type-signature type string">String</span>
{:#members:idprefix}








Specify the idprefix value to be added before the current id of the checkbox.




Default Value:
{:.param}






* "ej"








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
// To set  idPrefix  API value
$("#chkbox").ejCheckBox ({  idPrefix : "ej" });
</script>{% endhighlight %}







### name<span class="type-signature type string">String</span>
{:#members:name}








Specifies the name attribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set name API value during initialization  
$("#chkbox").ejCheckBox({  name: "sync" });
</script>{% endhighlight %}







### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members:showroundedcorner}








Specify the rounded corner to checkbox




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To Set the rounded corner during initialization.
$("#chkbox").ejCheckBox({ showRoundedCorner: true });
</script>{% endhighlight %}







### size<span class="type-signature type enum">enum</span>
{:#members:size}








Specifies the size of the CheckBox.See <a href="global.html#CheckboxSize">CheckboxSize</a>




Default Value:
{:.param}






* "small"








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set size API value during initialization
$("#chkbox").ejCheckBox({  size: "medium"});
</script>{% endhighlight %}







### text<span class="type-signature type string">string</span>
{:#members:text}








Specifies the text content for CheckBox.




Default Value:
{:.param}






* ""








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<script> 
// To set text API value 
$("#chkbox").ejCheckBox({ text: "Hello World"});
</script>{% endhighlight %}







### validationMessage<span class="type-signature type object">object</span>
{:#members:validationmessage}








Set the jquery validation error message in checkbox.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script>
//To set validationMessage API during initialization  
        $("#chkbox").ejCheckBox({ 
  validationRules:{                     
          required:true
          },
        validationMessage: {
           required: "Required Checkbox value"
        }
});
</script>{% endhighlight %}







### validationRules<span class="type-signature type object">object</span>
{:#members:validationrules}








Set the jquery validation rules in checkbox.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script>
//To set validationRules API during initialization  
        $("#chkbox").ejCheckBox({ 
  validationRules:{                     
          required:true
          }
});
</script>{% endhighlight %}







### value<span class="type-signature type string">String</span>
{:#members:value}








Specifies the value attribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To set value API value during initialization  
$("#chkbox").ejCheckBox({ value: "Hello World"});
</script>{% endhighlight %}





## Methods








### destroy<span class="signature">()</span>
{:#methods:destroy}








destroy the CheckBox widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
// Create Checkbox instance
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.destroy();// Destroy the CheckBox control
</script>{% endhighlight %}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
//To destroy the CheckBox control
$("#chkbox").ejCheckBox("destroy");
</script>{% endhighlight %}







### disable<span class="signature">()</span>
{:#methods:disable}








To disable the checkbox





Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
// Create Checkbox instance 
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.disable(); //disables the CheckBox
</script>{% endhighlight %}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
//To disable the CheckBox
$("#chkbox").ejCheckBox("disable");
</script>{% endhighlight %}







### enable<span class="signature">()</span>
{:#methods:enable}








To enable the checkbox





Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
// Create Checkbox instance 
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.enable(); // enables the CheckBox
</script>{% endhighlight %}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
//To enable the CheckBox
$("#chkbox").ejCheckBox("enable");
</script>{% endhighlight %}







### isChecked<span class="signature">()</span>
{:#methods:ischecked}








To Check the status of checkbox





Example
{:.example}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
// Create Checkbox  instance
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.isChecked(); // check the status of checkbox
</script>{% endhighlight %}


{% highlight html %}
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
$("#chkbox").ejCheckBox();
//To check the status of checkbox
$("#chkbox").ejCheckBox("isChecked");
</script>{% endhighlight %}





## Events








### beforeChange
{:#events:beforechange}








Fires before the Checkbox is going to changed its state successfully

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
<td class="description last">Event parameters from CheckBox
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
<td class="description last">returns the Checkbox model</td>
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
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script>  
//To create beforeChange event for checkbox
$("#chkbox").ejCheckBox({
beforeChange: function (args) {}
});
</script>{% endhighlight %}







### change
{:#events:change}








Fires when the Checkbox state is changed successfully

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
<td class="description last">Event parameters from CheckBox
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
<td class="description last">returns the Checkbox model</td>
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
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
// change event for checkbox
$("#chkbox").ejCheckBox({
change: function (args) {}
});
</script>{% endhighlight %}







### create
{:#events:create}








Fires when the Checkbox state is created successfully

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
<td class="description last">Event parameters from CheckBox
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
<td class="description last">returns the Checkbox model</td>
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
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To create event for checkbox
$("#chkbox").ejCheckBox({
  create: function (args) {}
});    
</script>{% endhighlight %}







### destroy
{:#events:destroy}








Fires when the Checkbox state is destroyed successfully

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
<td class="description last">Event parameters from CheckBox
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
<td class="description last">returns the Checkbox model</td>
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
 
<input type="checkbox" id="chkbox"/>
<label for="chkbox">Experienced</label>
<script> 
//To create destroy event for checkbox
$("#chkbox").ejCheckBox({
destroy: function (args) {}
});
</script>{% endhighlight %}




