---
layout: post
title: ejCheckBox
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html CheckBox Control.










$(element).ejCheckBox<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
// Create Checkbox  
$("#chkbox").ejCheckBox(); 
&lt;/script&gt;</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core.js


* module:ej.checkbox.js




## Members








### checked








Specifies whether chechbox has to be in checked or not. We can also specify array of string as value for this property. If any of the value in the specified array matches the value of the textbox, then it will be considered as checked. It will be useful in MVVM binding, specify array type to identify the values of the checked checkboxes.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set check API value during initialization  
$("#chkbox").ejCheckBox({ checked:  true });
&lt;/script&gt;</code>
</pre>






### checkState<span class="type-signature type enum">enum</span>








Specifies the State of ChecKBox.See <a href="global.html#CheckState">CheckState</a>




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set CheckState API value during initialization
$("#chkbox").ejCheckBox({ enableTriState: true , checkState:"indeterminate"});
&lt;/script&gt;</code>
</pre>






### cssClass<span class="type-signature type string">string</span>








Specify the CSS class to CheckBox to achieve custom theme.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code>&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt;  
// Set the root class for Checkbox control theme. This cssClass API helps to use custom skinning option for Checkbox control. By defining the root class using this API, we need to include this root class in CSS.                     
$("#chkbox").ejCheckBox({cssClass: "gradient-lime"}); 
&lt;/script&gt;</code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>








Specifies the checkbox control state.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To Enable checkbox on initialization. 
//To set width API value 
$("#chkbox").ejCheckBox ({ enabled: true });
&lt;/script&gt;</code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>








Specifies the persist property for Checkbox while initialization. The persist API save current model value to browser cookies for state maintains. While refreshing the Checkbox control page the model value apply from browser cookies.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set persist API value 
$("#chkbox").ejCheckBox({ enablePersistence : false });
&lt;/script&gt;</code>
</pre>






### enableRTL<span class="type-signature type boolean">boolean</span>








Specify the Right to Left direction to CheckBox




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
// Set the RTL during initialization.
$("#chkbox").ejCheckBox({  enableRTL : true });
&lt;/script&gt;</code>
</pre>






### enableTriState<span class="type-signature type boolean">boolean</span>








Specifies the enable or disable Tri-State for checkbox control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
// Specifies to enable or disable Tri-State option checkbox while initialization. 
//To set enableTriState API value 
$("#chkbox").ejCheckBox({  enableTriState: true });
&lt;/script&gt;</code>
</pre>






### htmlAttributes<span class="type-signature type object">object</span>








Specifies the HTML Attributes of the Checkbox




Default Value:
{:.param}






* {}








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//Set HtmlAttributes to Checkbox element during initialization  
$("#chkbox").ejCheckBox({ htmlAttributes : {required:"required"}});
&lt;/script&gt;</code>
</pre>






### htmlAttributes<span class="type-signature type object">object</span>








Specifies the HTML Attributes of the Checkbox




Default Value:
{:.param}






* {}








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To Set HtmlAttributes API value during initialization  
        $("#mask").ejMaskEdit({ htmlAttributes : {readOnly:"readOnly"}});                                        
&lt;/script&gt; </code>
</pre>






### id<span class="type-signature type string">String</span>








Specifies the id atribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set id API value during initialization  
$("#chkbox").ejCheckBox({  id: "sync" });
&lt;/script&gt;</code>
</pre>






### idPrefix<span class="type-signature type string">String</span>








Specify the idprefix value to be added before the current id of the checkbox.




Default Value:
{:.param}






* "ej"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
// To set  idPrefix  API value
$("#chkbox").ejCheckBox ({  idPrefix : "ej" });
&lt;/script&gt;</code>
</pre>






### name<span class="type-signature type string">String</span>








Specifies the name attribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set name API value during initialization  
$("#chkbox").ejCheckBox({  name: "sync" });
&lt;/script&gt;</code>
</pre>






### showRoundedCorner<span class="type-signature type boolean">boolean</span>








Specify the rounded corner to checkbox




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To Set the rounded corner during initialization.
$("#chkbox").ejCheckBox({ showRoundedCorner: true });
&lt;/script&gt;</code>
</pre>






### size<span class="type-signature type enum">enum</span>








Specifies the size of the CheckBox.See <a href="global.html#CheckboxSize">CheckboxSize</a>




Default Value:
{:.param}






* "small"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set size API value during initialization
$("#chkbox").ejCheckBox({  size: "medium"});
&lt;/script&gt;</code>
</pre>






### text<span class="type-signature type string">string</span>








Specifies the text content for CheckBox.




Default Value:
{:.param}






* ""








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;script&gt; 
// To set text API value 
$("#chkbox").ejCheckBox({ text: "Hello World"});
&lt;/script&gt;</code>
</pre>






### validationMessage<span class="type-signature type object">object</span>








Set the jquery validation error message in checkbox.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt;
//To set validationMessage API during initialization  
        $("#chkbox").ejCheckBox({ 
  validationRules:{                     
          required:true
          },
        validationMessage: {
           required: "Required Checkbox value"
        }
});
&lt;/script&gt;</code>
</pre>






### validationRules<span class="type-signature type object">object</span>








Set the jquery validation rules in checkbox.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt;
//To set validationRules API during initialization  
        $("#chkbox").ejCheckBox({ 
  validationRules:{                     
          required:true
          }
});
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type string">String</span>








Specifies the value attribute of the Checkbox.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To set value API value during initialization  
$("#chkbox").ejCheckBox({ value: "Hello World"});
&lt;/script&gt;</code>
</pre>




## Methods








### destroy<span class="signature">()</span>








destroy the CheckBox widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
// Create Checkbox instance
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.destroy();// Destroy the CheckBox control
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
//To destroy the CheckBox control
$("#chkbox").ejCheckBox("destroy");
&lt;/script&gt;</code>
</pre>






### disable<span class="signature">()</span>








To disable the checkbox





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
// Create Checkbox instance 
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.disable(); //disables the CheckBox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
//To disable the CheckBox
$("#chkbox").ejCheckBox("disable");
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>








To enable the checkbox





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
// Create Checkbox instance 
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.enable(); // enables the CheckBox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
//To enable the CheckBox
$("#chkbox").ejCheckBox("enable");
&lt;/script&gt;</code>
</pre>






### isChecked<span class="signature">()</span>








To Check the status of checkbox





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
// Create Checkbox  instance
var chkObj = $("#chkbox").data("ejCheckBox");
chkObj.isChecked(); // check the status of checkbox
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
$("#chkbox").ejCheckBox();
//To check the status of checkbox
$("#chkbox").ejCheckBox("isChecked");
&lt;/script&gt;</code>
</pre>




## Events








### beforeChange








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the Checkbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>data.element</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>data.isChecked</code></td>
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

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt;  
//To create beforeChange event for checkbox
$("#chkbox").ejCheckBox({
beforeChange: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### change








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the Checkbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>data.element</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the current element</td>
</tr>
<tr>
<td class="name"><code>data.isChecked</code></td>
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

<pre class="prettyprint">
<code>&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
// change event for checkbox
$("#chkbox").ejCheckBox({
change: function (args) {}
});
&lt;/script&gt;</code>
</pre>






### create








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the Checkbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To create event for checkbox
$("#chkbox").ejCheckBox({
  create: function (args) {}
});    
&lt;/script&gt;</code>
</pre>






### destroy








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
<td class="name"><code>argument</code></td>
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
<td class="name"><code>cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">returns the Checkbox model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
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

<pre class="prettyprint">
<code> 
&lt;input type="checkbox" id="chkbox"/&gt;
&lt;label for="chkbox"&gt;Experienced&lt;/label&gt;
&lt;script&gt; 
//To create destroy event for checkbox
$("#chkbox").ejCheckBox({
destroy: function (args) {}
});
&lt;/script&gt;</code>
</pre>



