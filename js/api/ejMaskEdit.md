---
layout: post
title: ejMaskEdit
description: API reference for ejMaskEdit
documentation: API
platform: js
keywords: MaskEdit, ejMaskEdit, syncfusion, MaskEdit api  
---

# ejMaskEdit

The MaskEdit control provides an easy and reliable way of collecting user input and displaying standard data in a specific format. Some common uses of the MaskEdit control are IP address editors, phone number editors, and Social Security number editors.

#### Syntax

{% highlight js %}

$(element).ejMaskEdit()

{% endhighlight %}


#### Example


{% highlight html %}
     
    <input id="mask" type="text" />

    <script>

        // Create MaskEdit
        $('#mask').ejMaskEdit();

    </script>

{% endhighlight %}


#### Requires


* module:jQuery


* module:ej.core.js


* module:ej.cultures.min.js


* module:ej.maskedit.js


## Members


### cssClass `string`
{:#members:cssclass}

Specify the cssClass to achieve custom theme.

#### Default Value

* null


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set cssClass API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", cssClass: "gradient-lime" });
    </script>

{% endhighlight %}


### customCharacter `string`
{:#members:customcharacter}


Specify the custom character allowed to entered in maskedit textbox control.


#### Default Value


* null


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set customCharacter API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "C-99-9999", customCharacter: "#" });
    </script>

{% endhighlight %}


### enabled `boolean`
{:#members:enabled}


Specify the state of the maskedit textbox control.

#### Default Value


* true


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set enabled API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", enabled: true });
    </script>

{% endhighlight %}


### enablePersistence `boolean`
{:#members:enablepersistence}

Specify the enablePersistence to maskedit textbox to save current model value to browser cookies for state maintains.

#### Example


{% highlight html %}

    <input id="mask" type="text" />

    <script>
        //To set enablePersistence API value during initialization
        $("#mask").ejMaskEdit({ enablePersistence:true });
    </script>
 
{% endhighlight %}

### height `string`
{:#members:height}

Specifies the height for the maskedit textbox control.


#### Default Value

* 28 px


#### Example


{% highlight html %}

    <input id="mask" type="text" />

    <script>
        //To set height API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", height: "28px" });
    </script>
 
{% endhighlight %}


### hidePromptOnLeave `boolean`
{:#members:hidepromptonleave}

Specifies whether hide the prompt characters with spaces on blur. Prompt chars will be shown again on focus the textbox.

#### Default Value


* false


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set hidePromptOnLeave API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", hidePromptOnLeave: true });
    </script>

{% endhighlight %}


### htmlAttributes `JSON`
{:#members:htmlattributes}

Specifies the list of html attributes to be added to maskedit textbox.

#### Default Value

* {}

#### Example

{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set htmlAttributes API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", htmlAttributes: { name:"masktxtbox" } });
    </script>

{% endhighlight %}


### inputMode `enum`
{:#members:inputmode}



Specify the inputMode for maskedit textbox control. See <a href="global.html#InputMode">InputMode</a>


#### Default Value


* ej.InputMode.Text


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set inputMode API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", inputMode: ej.InputMode.Password });
    </script>

{% endhighlight %}


### maskFormat `string`
{:#members:maskformat}


Specifies the input mask.


#### Default Value



* null



#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set maskFormat API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999" });
    </script>

{% endhighlight %}

### name `string`
{:#members:name}

Specifies the name attribute value for the maskedit textbox.

#### Default Value

* null

#### Example

{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set name API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",name:"insurance_number" });
    </script>

{% endhighlight %}


### readOnly `boolean`
{:#members:readonly}

Toggles the readonly state of the maskedit textbox. When the maskedit textbox is readonly, it doesn't allow your input.

#### Default Value


* false


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set readOnly API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", value: "456789", readOnly: true });
    </script>

{% endhighlight %}


### showError `boolean`
{:#members:showerror}


Specifies whether the error will show until correct value entered in the maskedit textbox control.

#### Default Value


* false


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set showError API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", showError: true });
    </script>

 {% endhighlight %}


### showRoundedCorner `boolean`
{:#members:showroundedcorner}

Maskedit input is displayed in rounded corner style when this property is set to true.


#### Default Value


* false


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set showRoundedCorner API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", showRoundedCorner: true });
    </script>

{% endhighlight %}


### textAlign `enum`
{:#members:textalign}


Specify the text alignment for maskedit textbox control.See <a href="global.html#TextAlign">TextAlign</a>


#### Default Value


* "left"


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set textAlign API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", textAlign: "left" });
    </script>

{% endhighlight %}


### validationMessage `object`
{:#members:validationmessage}


Sets the jQuery validation error message in maskedit. This property works when the widget is present inside the form. Include jquery.validate.min.js plugin additionally.


#### Default Value


* null


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set validationMessage value during initialization
        $("#mask").ejMaskEdit({ validationRules: { required: true }, validationMessage: { required: "Required MaskEdit value" } });
    </script>

{% endhighlight %}


### validationRules `object`
{:#members:validationrules}


Sets the jQuery validation rules to the Maskedit. This property works when the widget is present inside the form. Include jquery.validate.min.js plugin additionally.


#### Default Value


* null


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set validationRules value during initialization
        $("#mask").ejMaskEdit({ validationRules: { required: true } });
    </script>

{% endhighlight %}


### value `string`
{:#members:value}


Specifies the value for the maskedit textbox control.

#### Default Value


* null


#### Example



{% highlight html %}

    <input id="mask" type="text" />

    <script>
        //To set value API  during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", value: "459978" });
    </script>

{% endhighlight %}


### watermarkText `string`
{:#members:watermarktext}

Specifies the water mark text to be displayed in input text.

#### Default Value


* null


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set watermarkText API value during initialization
        $("#mask").ejMaskEdit({ watermarkText: "Enter value" });
    </script>

{% endhighlight %}


### width `string`
{:#members:width}


Specifies the width for the maskedit textbox control.


#### Default Value


* 143pixel


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //To set width API value during initialization
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", width: 143 });
    </script>

{% endhighlight %}


## Methods


### clear()
{:#methods:clear}


To clear the text in maskedit textbox control.


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        // Create MaskEdit control
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", value: "345678" });
        
        // Create MaskEdit control object
        var maskObj = $("#mask").data("ejMaskEdit");
        maskObj.clear(); // clear the maskedit control
    </script>
                 
{% endhighlight %}


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        $("#mask").ejMaskEdit({ maskFormat: "99-9999", value: "345678" });
        // clear the maskedit control
        $("#mask").ejMaskEdit("clear");
    </script>

{% endhighlight %}


### disable()
{:#methods:disable}


To disable the maskedit textbox control.


#### Example



{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        // Create MaskEdit control
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "45340078" });

        // Create MaskEdit control object
        var maskObj = $("#mask").data("ejMaskEdit");
        maskObj.disable(); // disable the maskedit control
    </script>
                 
                 
{% endhighlight %}


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "45340078" });
        // disable the maskedit control
        $("#mask").ejMaskEdit("disable");
    </script>

{% endhighlight %}


### enable()
{:#methods:enable}


To enable the maskedit textbox control.


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        // Create MaskEdit control
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });

        // Create MaskEdit control object
        var maskObj = $("#mask").data("ejMaskEdit");
        maskObj.enable(); // enable the maskedit control
    </script>
                
{% endhighlight %}


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });
        // enable the maskedit control 
        $("#mask").ejMaskEdit("enable");
    </script>

{% endhighlight %}


### get_StrippedValue()
{:#methods:get_strippedvalue}


To obtained the pure value of the textvalue, removes all the symbols in maskedit textbox control.


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        // Create MaskEdit control
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });

        // Create MaskEdit control object
        var maskObj = $("#mask").data("ejMaskEdit");
        // Return the pure value of the textvalue, removes all the symbols
        alert(maskObj.get_StrippedValue()); 
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });
        // Return the pure value of the textvalue, removes all the symbols
        alert($("#mask").ejMaskEdit("get_StrippedValue"));
    </script>

{% endhighlight %}


### get_UnstrippedValue()
{:#methods:get_unstrippedvalue}



To obtained the textbox value as such that, Just replace all '_' to ' '(space) in maskedit textbox control.


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        // Create MaskEdit control
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });

        // Create MaskEdit control object
        var maskObj = $("#mask").data("ejMaskEdit");
        // Return the textbox value as such that, Just replace all '_' to ' '(space)
        alert(maskObj.get_UnstrippedValue()); 
    </script>

{% endhighlight %}


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        $("#mask").ejMaskEdit({ maskFormat: "99-99-9999", value: "12345678" });
        // Return the textbox value as such that, Just replace all '_' to ' '(space)
        alert($("#mask").ejMaskEdit("get_UnstrippedValue"));
    </script>

{% endhighlight %}


## Events


### change
{:#events:change}


Fires when value changed in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //change event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "99999 - 9999",
            change: function (args) { }
        });
    </script>                  

{% endhighlight %}

### create
{:#events:create}


Fires after MaskEdit control is created.

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
<td class="description">returns the MaskEdit model</td>
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
 
    <input id="mask" type="text" />

    <script>
        //create event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "(999)999-9999",
            create: function (args) { }
        });
    </script>       

{% endhighlight %}


### destroy
{:#events:destroy}


Fires when the MaskEdit is destroyed successfully.

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
<td class="description">returns the MaskEdit model</td>
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
 
    <input id="mask" type="text" />

    <script>
        //destroy event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "(999)999-9999",
            destroy: function (args) { }
        });
    </script>

{% endhighlight %}


### focusIn
{:#events:focusin}


Fires when focused in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //focusIn event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "aa-99-99-a",
            focusIn: function (args) { }
        });
    </script>                 

{% endhighlight %}


### focusOut
{:#events:focusout}


Fires when focused out in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //focusOut event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "(999)999-9999",
            focusOut: function (args) { }
        });
    </script>                   

{% endhighlight %}


### keydown
{:#events:keydown}



Fires when keydown in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //keydown event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "99-9999",
            keydown: function (args) { }
        });
    </script>                  

{% endhighlight %}



### keyPress
{:#events:keypress}


Fires when keypress in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //keyPress event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "99-99-9999",
            keyPress: function (args) { }
        });
    </script>

{% endhighlight %}


### keyup
{:#events:keyup}


Fires when keyup in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



#### Example


{% highlight html %}

    <input id="mask" type="text" />

    <script>
        //keyup event for mask edit textbox control
        $("#mask").ejMaskEdit({
            maskFormat: "99-99-9999",
            keyup: function (args) { }
        });
    </script>

{% endhighlight %}



### mouseout
{:#events:mouseout}


Fires when mouse out in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //mouseout event for toggle button
        $("#mask").ejMaskEdit({
            maskFormat: "99-99-9999",
            mouseout: function (args) { }
        });
    </script>                 

{% endhighlight %}


### mouseover
{:#events:mouseover}


Fires when mouse over in mask edit textbox control.

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
<td class="description">Event parameters from maskedit textbox control
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
cancel{% endhighlight %}</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name">{% highlight html %}
model{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description">returns the maskedit model</td>
</tr>
<tr>
<td class="name">{% highlight html %}
type{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns the name of the event</td>
</tr>
<tr>
<td class="name">{% highlight html %}
value{% endhighlight %}</td>
<td class="type"><span class="param-type">number</span></td>
<td class="description">returns the maskedit value</td>
</tr>
<tr>
<td class="name">{% highlight html %}
unmaskedValue{% endhighlight %}</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description">returns unstripped value in maskedit textbox control.</td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>


#### Example


{% highlight html %}
 
    <input id="mask" type="text" />

    <script>
        //mouseover event for toggle button
        $("#mask").ejMaskEdit({
            maskFormat: "99-99-9999",
            mouseover: function (args) { }
        });
    </script>                 

{% endhighlight %}




