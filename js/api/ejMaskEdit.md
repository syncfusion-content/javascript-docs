---
layout: post
title: ejMaskEdit
documentation: API
platform: js
metaname: 
metacontent: 
---

# Custom Design for Html ejMaskEdit Textbox control.










$(element).ejMaskEdit<span class="signature">()</span>











Example
{:.example}

<pre class="prettyprint">
<code>     
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
// Create Slider 
$('#mask').ejMaskEdit(); 
   
&lt;/script&gt; 
</code>
</pre>






Requires
{:.require}




* module:jQuery


* module:ej.core.js


* module:jquery.globalize.js


* module:globalize.cultures.min.js


* module:ej.maskedit.js




## Members








### cssClass<span class="type-signature type string">string</span>
{:#members-cssclass}








Specify the cssClass to maskedit textbox control to achieve custom theme.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set cssClass API value during initialization  
        $("#mask").ejMaskEdit({maskFormat: "99-9999",cssClass: "gradient-lime"});                                        
&lt;/script&gt;</code>
</pre>






### customCharacter<span class="type-signature type string">string</span>
{:#members-customcharacter}








Specify the custom character allowed to entered in maskedit textbox control.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//To set customCharacter API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",customCharacter: "gradient-lime"});                                       
&lt;/script&gt; </code>
</pre>






### enabled<span class="type-signature type boolean">boolean</span>
{:#members-enabled}








Specify the state of the maskedit textbox control.




Default Value:
{:.param}






* true








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set enabled API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",enabled: true });                                  
&lt;/script&gt;</code>
</pre>






### enablePersistence<span class="type-signature type boolean">boolean</span>
{:#members-enablepersistence}








Specify the enablePersistence to mask edit textbox control to save current model value to browser cookies for state maintains.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set enablePersistence API value during initialization  
        $("#mask").ejMaskEdit({ enablePersistence: "left" });                                    
&lt;/script&gt;</code>
</pre>






### height<span class="type-signature type string">string</span>
{:#members-height}








Specifies the height for the maskedit textbox control.




Default Value:
{:.param}






* 28pixel








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//To set height API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",height: "28px"});                                  
&lt;/script&gt;</code>
</pre>






### hidePromptOnLeave<span class="type-signature type boolean">boolean</span>
{:#members-hidepromptonleave}








Specify the hidePromptOnLeave for maskedit textbox control to hide the mask on focus out.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set hidePromptOnLeave API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",hidePromptOnLeave: true });                                        
&lt;/script&gt;</code>
</pre>






### inputMode<span class="type-signature type enum">enum</span>
{:#members-inputmode}








Specify the inputMode for maskedit textbox control. See <a href="global.html#InputMode">InputMode</a>




Default Value:
{:.param}






* ej.InputMode.Text








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set inputMode API value during initialization  
        $("#mask").ejMaskEdit({maskFormat: "99-9999",inputMode: ej.InputMode.Password });                                        
&lt;/script&gt; </code>
</pre>






### maskFormat<span class="type-signature type string">string</span>
{:#members-maskformat}








Specifies the maskFormat string for the maskedit textbox control.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//To set maskFormat API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999"});                                         
&lt;/script&gt; </code>
</pre>






### readOnly<span class="type-signature type boolean">boolean</span>
{:#members-readonly}








Specify the readOnly for maskedit textbox control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//To set readOnly API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",value:"456789",readOnly: true });                                  
&lt;/script&gt;</code>
</pre>






### showError<span class="type-signature type boolean">boolean</span>
{:#members-showerror}








Specifies the showError until correct value entered in the maskedit textbox control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set showError API value during initialization  
        $("#mask").ejMaskEdit({maskFormat: "99-9999", showError: true});                                         
&lt;/script&gt; </code>
</pre>






### showRoundedCorner<span class="type-signature type boolean">boolean</span>
{:#members-showroundedcorner}








Specify the rounded corner for maskedit textbox control.




Default Value:
{:.param}






* false








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set showRoundedCorner API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",showRoundedCorner:true});                                  
&lt;/script&gt;</code>
</pre>






### textAlign<span class="type-signature type enum">enum</span>
{:#members-textalign}








Specify the text alignment for maskedit textbox control.




Default Value:
{:.param}






* "left"








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set textAlign API value during initialization  
        $("#mask").ejMaskEdit({maskFormat: "99-9999",textAlign: "left" });                                       
&lt;/script&gt;</code>
</pre>






### validationMessage<span class="type-signature type object">object</span>
{:#members-validationmessage}








Set the jquery validation error message in maskedit.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set validationMessage value during initialization  
        $("#mask").ejMaskEdit({ validationRules:{required:true},validationMessage: { required: "Required MaskEdit value"} });                                    
&lt;/script&gt;</code>
</pre>






### validationRules<span class="type-signature type object">object</span>
{:#members-validationrules}








Set the jquery validation rules in maskedit.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set validationRules value during initialization  
        $("#mask").ejMaskEdit({ validationRules:{required:true} });                                      
&lt;/script&gt;</code>
</pre>






### value<span class="type-signature type string">string</span>
{:#members-value}








Specifies the value string for the maskedit textbox control.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code>&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;                  
//To set value API  during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",value: "459978"});                                         
&lt;/script&gt; </code>
</pre>






### watermarkText<span class="type-signature type string">string</span>
{:#members-watermarktext}








Specifies the watermark text string for the maskedit textbox control.




Default Value:
{:.param}






* null








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//To set watermarkText API value during initialization  
        $("#mask").ejMaskEdit({ watermarkText: "Enter value"});                                 
&lt;/script&gt;</code>
</pre>






### width<span class="type-signature type string">string</span>
{:#members-width}








Specifies the width for the maskedit textbox control.




Default Value:
{:.param}






* 143pixel








Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//To set width API value during initialization  
        $("#mask").ejMaskEdit({ maskFormat: "99-9999",width: 143});                                      
&lt;/script&gt;</code>
</pre>




## Methods








### clear<span class="signature">()</span>
{:#methods-clear}








To clear the text in maskedit textbox control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
              
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-9999",value:"345678"});
// Create MaskEdit control
var maskObj = $("#mask").data("ejMaskEdit");            
maskObj.clear(); // clear the maskedit control          
&lt;/script&gt;
                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
                      
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-9999",value:"345678"});
// clear the maskedit control
$("#mask").ejMaskEdit("clear");         
&lt;/script&gt;</code>
</pre>






### disable<span class="signature">()</span>
{:#methods-disable}








To disable the maskedit textbox control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
              
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"45340078"});
// Create MaskEdit control
var maskObj = $("#mask").data("ejMaskEdit");            
maskObj.disable(); // disable the maskedit control              
&lt;/script&gt;
                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
                      
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"45340078"});
// disable the maskedit control
$("#mask").ejMaskEdit("disable");               
&lt;/script&gt;</code>
</pre>






### enable<span class="signature">()</span>
{:#methods-enable}








To enable the maskedit textbox control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
              
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// Create MaskEdit control
var maskObj = $("#mask").data("ejMaskEdit");            
maskObj.enable(); // enable the maskedit control                
&lt;/script&gt;
                 </code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
                      
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// enable the maskedit control
$("#mask").ejMaskEdit("enable");                
&lt;/script&gt;</code>
</pre>






### get_StrippedValue<span class="signature">()</span>
{:#methods-get_strippedvalue}








To obtained the pure value of the textvalue, removes all the symbols in maskedit textbox control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
              
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// Create MaskEdit control
var maskObj = $("#mask").data("ejMaskEdit");            
alert(maskObj.get_StrippedValue()); // Return the pure value of the textvalue, removes all the symbols          
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
                      
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// Return the pure value of the textvalue, removes all the symbols
alert( $("#mask").ejMaskEdit("get_StrippedValue"));             
&lt;/script&gt;</code>
</pre>






### get_UnstrippedValue<span class="signature">()</span>
{:#methods-get_unstrippedvalue}








To obtained the textbox value as such that, Just replace all '_' to ' '(space) in maskedit textbox control.





Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
              
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// Create MaskEdit control
var maskObj = $("#mask").data("ejMaskEdit");            
alert(maskObj.get_UnstrippedValue()); // Return the textbox value as such that, Just replace all '_' to ' '(space)      
&lt;/script&gt;</code>
</pre>
<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
                      
&lt;script&gt;
$("#mask").ejMaskEdit({maskFormat: "99-99-9999",value:"12345678"});
// Return the textbox value as such that, Just replace all '_' to ' '(space)
alert($("#mask").ejMaskEdit("get_UnstrippedValue"));            
&lt;/script&gt;</code>
</pre>




## Events








### change
{:#events-change}








Fires when value changed in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//change event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "99999 - 9999",
   change: function (args) {}
});    
&lt;/script&gt;                  </code>
</pre>






### create
{:#events-create}








Fires after MaskEdit control is created.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the MaskEdit model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//create event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "(999)999-9999",
   create: function (args) {}
}); 
&lt;/script&gt;          </code>
</pre>






### destroy
{:#events-destroy}








Fires when the MaskEdit is destroyed successfully.

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
<td class="name"><code>argument.cancel</code></td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>argument.model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the MaskEdit model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}

<pre class="prettyprint">
<code> 
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//destroy event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "(999)999-9999",
   destroy: function (args) {}
}); 
&lt;/script&gt;          </code>
</pre>






### focusIn
{:#events-focusin}








Fires when focused in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//focusIn event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "aa-99-99-a",
   focusIn: function (args) {}
});
&lt;/script&gt;                  </code>
</pre>






### focusOut
{:#events-focusout}








Fires when focused out in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//focusOut event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "(999)999-9999",
   focusOut: function (args) {}
}); 
&lt;/script&gt;                  </code>
</pre>






### keydown
{:#events-keydown}








Fires when keydown in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//keydown event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "99-9999",
   keydown: function (args) {}
}); 
&lt;/script&gt;                  </code>
</pre>






### keyPress
{:#events-keypress}








Fires when keypress in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;
//keyPress event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "99-99-9999",
   keyPress: function (args) {}
});      
&lt;/script&gt;</code>
</pre>






### keyup
{:#events-keyup}








Fires when keyup in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
<code>&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt;           
//keyup event for mask edit textbox control
$("#mask").ejMaskEdit({
   maskFormat: "99-99-9999",
   keyup: function (args) {}
});      
&lt;/script&gt;</code>
</pre>






### mouseout
{:#events-mouseout}








Fires when mouse out in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//mouseout event for toggle button
$("#mask").ejMaskEdit({
   maskFormat: "***-**-****",
   mouseout: function (args) {}
});    
&lt;/script&gt;                  </code>
</pre>






### mouseover
{:#events-mouseover}








Fires when mouse over in mask edit textbox control.

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
<td class="description last">Event parameters from maskedit textbox control
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
<td class="description last">if the event should be cancelled; otherwise, false.</td>
</tr>
<tr>
<td class="name"><code>model</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the maskedit model</td>
</tr>
<tr>
<td class="name"><code>type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
<tr>
<td class="name"><code>value</code></td>
<td class="type"><span class="param-type">number</span></td>
<td class="description last">returns the maskedit value</td>
</tr>
<tr>
<td class="name"><code>unmaskedValue</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns unstripped value in maskedit textbox control.</td>
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
&lt;input id="mask" type="text" /&gt; 
 
&lt;script&gt; 
//mouseover event for toggle button
$("#mask").ejMaskEdit({
   maskFormat: "$99999",
   mouseover: function (args) {}
});   
&lt;/script&gt;                  </code>
</pre>



