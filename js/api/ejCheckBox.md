---
layout: post
title: Properties,Methods and Events of ejCheckBox Widget
description: API reference for ejCheckBox
documentation: API
platform: js
keywords: checkbox, ejCheckBox, syncfusion, checkbox api
---

# ejCheckBox


The CheckBox control allows you to check an option to perform an action. This control allows you to select true, false or an intermediate option. These CheckBoxes are supported with themes. The html CheckBox control is rendered as Essential JavaScript CheckBox control.


#### Syntax

{% highlight javascript %}

        $(element).ejCheckBox()

{% endhighlight %}


#### Example


{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        // Create CheckBox 
        $("#chkbox").ejCheckBox(); 
        </script>

{% endhighlight %}



#### Requires


* module:jQuery


* module:ej.core.js


* module:ej.checkbox.js


## Members



### checked `boolean | string[]`
{:#members:checked}


Specifies whether CheckBox has to be in checked or not. We can also specify array of string as value for this property. If any of the value in the specified array matches the value of the textbox, then it will be considered as checked. It will be useful in MVVM binding, specify array type to identify the values of the checked CheckBoxes.


#### Default Value



* false



#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set check API value during initialization  
        $("#chkbox").ejCheckBox({ checked:  true });
        </script>

{% endhighlight %}



### checkState `enum`
{:#members:checkstate}



<ts name="ej.CheckState" />




Specifies the State of CheckBox.See below to get available CheckState



<table class="props">
<thead>
<tr>
<th>Name</th>
<th>Type</th>
<th>Default</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Uncheck</td>
<td class="type">string</td>
<td class="default">uncheck</td>
<td class="description">Enum for Uncheck state checkbox</td>
</tr>
<tr>
<td class="name">
Check</td>
<td class="type">string</td>
<td class="default">check</td>
<td class="description">Enum for Check state checkbox</td>
</tr>
<tr>
<td class="name">
Indeterminate</td>
<td class="type">string</td>
<td class="default">indeterminate</td>
<td class="description">Enum for Indeterminate state checkbox</td>
</tr>
</tbody>
</table>






#### Default Value







* null








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set CheckState API value during initialization
        $("#chkbox").ejCheckBox({ enableTriState: true , checkState:"indeterminate"});
        </script>

{% endhighlight %}







### cssClass `string`
{:#members:cssclass}






Sets the root CSS class for CheckBox theme, which is used customize. 




#### Default Value







* ""








#### Example



{% highlight html %}
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script>  
        // Set the root class for CheckBox control theme. This cssClass API helps to use custom skinning option for CheckBox control. By defining the root class using this API, we need to include this root class in CSS.                     
        $("#chkbox").ejCheckBox({cssClass: "gradient-lime"}); 
        </script>

{% endhighlight %}







### enabled `boolean`
{:#members:enabled}








Specifies the checkbox control state.




#### Default Value







* true








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To Enable checkbox on initialization. 
        //To set width API value 
        $("#chkbox").ejCheckBox ({ enabled: true });
        </script>

{% endhighlight %}







### enablePersistence `boolean`
{:#members:enablepersistence}








Specifies the persist property for CheckBox while initialization. The persist API save current model value to browser cookies for state maintains. While refreshing the CheckBox control page the model value apply from browser cookies.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set persist API value 
        $("#chkbox").ejCheckBox({ enablePersistence : false });
        </script>

{% endhighlight %}







### enableRTL `boolean`
{:#members:enablertl}








Specify the Right to Left direction to Checkbox




#### Default Value







* false








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        // Set the RTL during initialization.
        $("#chkbox").ejCheckBox({  enableRTL : true });
        </script>

{% endhighlight %}







### enableTriState `boolean`
{:#members:enabletristate}








Specifies the enable or disable Tri-State for checkbox control.




#### Default Value







* false








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        // Specifies to enable or disable Tri-State option checkbox while initialization. 
        //To set enableTriState API value 
        $("#chkbox").ejCheckBox({  enableTriState: true });
        </script>

{% endhighlight %}







### htmlAttributes `object`
{:#members:htmlattributes}








It allows to define the characteristics of the CheckBox control. It will helps to extend the capability of an HTML element.




#### Default Value







* {}








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //Set HtmlAttributes to CheckBox element during initialization  
        $("#chkbox").ejCheckBox({ htmlAttributes : {required:"required"}});
        </script>

{% endhighlight %}






### id `string`
{:#members:id}








Specified value to be added an id attribute of the CheckBox.




#### Default Value







* null








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set id API value during initialization  
        $("#chkbox").ejCheckBox({  id: "sync" });
        </script>

{% endhighlight %}







### idPrefix `string`
{:#members:idprefix}








Specify the prefix value of id to be added before the current id of the CheckBox.




#### Default Value







* "ej"








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        // To set  idPrefix  API value
        $("#chkbox").ejCheckBox ({  idPrefix : "ej" });
        </script>

{% endhighlight %}







### name `string`
{:#members:name}








Specifies the name attribute of the CheckBox.




#### Default Value







* null








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set name API value during initialization  
        $("#chkbox").ejCheckBox({  name: "sync" });
        </script>

{% endhighlight %}







### showRoundedCorner `boolean`
{:#members:showroundedcorner}







Displays rounded corner borders to CheckBox




#### Default Value







* false








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To Set the rounded corner during initialization.
        $("#chkbox").ejCheckBox({ showRoundedCorner: true });
        </script>

{% endhighlight %}







### size `enum`
{:#members:size}


<ts name="ej.CheckboxSize" />



Specifies the size of the CheckBox.See below to know available CheckboxSize</a>
<table class="props">
<thead>
<tr>
<th>Name</th>
<th class="last">Description</th>
</tr>
</thead>
<tbody>
<tr>
<td class="name">
Medium</td>
<td class="description">Displays the CheckBox in medium size</td>
</tr>
<tr>
<td class="name">
Small</td>
<td class="description">Displays the CheckBox in small size</td>
</tr>
</tbody>
</table>



#### Default Value







* "small"








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set size API value during initialization
        $("#chkbox").ejCheckBox({  size: "medium"});
        </script>
        
{% endhighlight %}







### text `string`
{:#members:text}








Specifies the text content to be displayed for CheckBox.




#### Default Value







* ""








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <script> 
        // To set text API value 
        $("#chkbox").ejCheckBox({ text: "Hello World"});
        </script>
        
{% endhighlight %}







### validationMessage `object`
{:#members:validationmessage}








Set the jQuery validation error message in CheckBox.

N> The property will work when the widget present inside the form. Additionally need to include jquery.validate.min.js plugin.



#### Default Value







* null








#### Example



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
                    required: "Required CheckBox value"
                }
        });
        </script>

{% endhighlight %}







### validationRules `object`
{:#members:validationrules}








Set the jQuery validation rules in CheckBox.

N> The property will work when the widget present inside the form. Additionally need to include jquery.validate.min.js plugin.


#### Default Value







* null








#### Example



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
        </script>

{% endhighlight %}







### value `string`
{:#members:value}








Specifies the value attribute of the CheckBox.




#### Default Value







* null








#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To set value API value during initialization  
        $("#chkbox").ejCheckBox({ value: "Hello World"});
        </script>

{% endhighlight %}





## Methods








### destroy()
{:#methods:destroy}








Destroy the CheckBox widget all events bound using this._on will be unbind automatically and bring the control to pre-init state.





#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        // Create CheckBox instance
        var chkObj = $("#chkbox").data("ejCheckBox");
        chkObj.destroy();// Destroy the CheckBox control
        </script>

{% endhighlight %}


{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        //To destroy the CheckBox control
        $("#chkbox").ejCheckBox("destroy");
        </script>
        
{% endhighlight %}







### disable()
{:#methods:disable}








Disable the CheckBox to prevent all user interactions.





#### Example



{% highlight html %}
        
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        // Create CheckBox instance 
        var chkObj = $("#chkbox").data("ejCheckBox");
        chkObj.disable(); //disables the CheckBox
        </script>

{% endhighlight %}


{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        //To disable the CheckBox
        $("#chkbox").ejCheckBox("disable");
        </script>

{% endhighlight %}







### enable()
{:#methods:enable}








To enable the CheckBox





#### Example



{% highlight html %}
        
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        // Create CheckBox instance 
        var chkObj = $("#chkbox").data("ejCheckBox");
        chkObj.enable(); // enables the CheckBox
        </script>

{% endhighlight %}


{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        //To enable the CheckBox
        $("#chkbox").ejCheckBox("enable");
        </script>

{% endhighlight %}







### isChecked()
{:#methods:ischecked}








To Check the status of CheckBox



####Returns

boolean

#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        // Create CheckBox  instance
        var chkObj = $("#chkbox").data("ejCheckBox");
        chkObj.isChecked(); // check the status of checkbox
        </script>

{% endhighlight %}


{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        $("#chkbox").ejCheckBox();
        //To check the status of checkbox
        $("#chkbox").ejCheckBox("isChecked");
        </script>

{% endhighlight %}





## Events








### beforeChange
{:#events:beforechange}








Fires before the CheckBox is going to changed its state successfully


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
<td class="type"><ts ref="ej.CheckBox.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the CheckBox model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event model values</td>
</tr>
<tr>
<td class="name">
isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the status whether the element is checked or not.</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script>  
        //To create beforeChange event for checkbox
        $("#chkbox").ejCheckBox({
        beforeChange: function (args) {}
        });
         </script>
         
{% endhighlight %}







### change
{:#events:change}








Fires when the CheckBox state is changed successfully

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
<td class="type"><ts ref="ej.CheckBox.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the CheckBox model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">
event</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the event arguments</td>
</tr>
<tr>
<td class="name">
isChecked</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">returns the status whether the element is checked or not.</td>
</tr>
<tr>
<td class="name">
checkState</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the state of the checkbox</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}

        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        // change event for checkbox
        $("#chkbox").ejCheckBox({
        change: function (args) {}
        });
        </script>

{% endhighlight %}







### create
{:#events:create}








Fires when the CheckBox state is created successfully


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
<td class="type"><ts ref="ej.CheckBox.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the CheckBox model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To create event for checkbox
        $("#chkbox").ejCheckBox({
        create: function (args) {}
        });    
        </script>

{% endhighlight %}







### destroy
{:#events:destroy}








Fires when the CheckBox state is destroyed successfully


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
<td class="type"><ts ref="ej.CheckBox.Model"/>
<span class="param-type">object</span></td>
<td class="description">returns the CheckBox model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
</tbody>
</table>





#### Example



{% highlight html %}
 
        <input type="checkbox" id="chkbox"/>
        <label for="chkbox">Experienced</label>
        <script> 
        //To create destroy event for checkbox
        $("#chkbox").ejCheckBox({
        destroy: function (args) {}
        });
        </script>

{% endhighlight %}




