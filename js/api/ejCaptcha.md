---
layout: post
title: ejCaptcha
documentation: API
platform: js
metaname: 
metacontent: 
---

Custom Design for Html Captcha control.










#### $(element).ejCaptcha<span class="signature">(options)</span>







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
<td class="name"><code>options</code></td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for Captcha</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
// Create Captcha
$('#Captcha1').ejCaptcha();     
&lt;/script&gt;</code>
</pre>






### Requires




* module:jQuery


* module:ej.core.js


* module:ej.captcha.js


* module:ej.button.js




### Members








#### characterSet<span class="type-signature type string">string</span>








Specifies the character set of the Captcha that will be used to generate captcha text randomly.




Default Value:
{:.param}






* "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789"








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set character set API value during initialization  
        $("#captcha1").ejCaptcha({  characterSet: "ABCD1234"}); 
&lt;/script&gt;                         </code>
</pre>






#### customErrorMessage<span class="type-signature type string">string</span>








Specifies the error message to be displayed when the Captcha mismatch.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set error message API value during initialization  
        $("#captcha1").ejCaptcha({  customErrorMessage: "InValid Captcha"});    
&lt;/script&gt;                         </code>
</pre>






#### enableAutoValidation<span class="type-signature type boolean">boolean</span>








Set the Captcha validation automatically.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set auto validation API value during initialization  
        $("#captcha1").ejCaptcha({  enableAutoValidation: true});       
&lt;/script&gt;                         </code>
</pre>






#### enableCaseSensitivity<span class="type-signature type boolean">boolean</span>








Specifies the case sensitivity for the characters typed in the Captcha.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set case sensitivity API value during initialization  
        $("#captcha1").ejCaptcha({  enableCaseSensitivity: true});      
&lt;/script&gt;                         </code>
</pre>






#### enablePattern<span class="type-signature type boolean">boolean</span>








Specifies the background patterns for the Captcha.




Default Value:
{:.param}






* true








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set target input API value during initialization  
        $("#captcha1").ejCaptcha({  enablePattern: true});      
&lt;/script&gt;</code>
</pre>






#### enableRTL<span class="type-signature type boolean">boolean</span>








Sets the Captcha direction as right to left alignment.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set enable RTL API value during initialization  
        $("#captcha1").ejCaptcha({  enableRTL: true});  
&lt;/script&gt;                         </code>
</pre>






#### hatchStyle<span class="type-signature type enum">enum</span>








Specifies the background apperance for the captcha.




Default Value:
{:.param}






* value set as BackwardDiagonal








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set mapper API value during initialization  
        $("#captcha1").ejCaptcha({  hatchStyle: "BackwardDiagonal"});   
&lt;/script&gt;                         </code>
</pre>






#### height<span class="type-signature type number">number</span>








Specifies the height of the Captcha.




Default Value:
{:.param}






* 50








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set height API value during initialization  
        $("#captcha1").ejCaptcha({  height: 50});       
&lt;/script&gt;                 </code>
</pre>






#### mapper<span class="type-signature type string">string</span>








Specifies the method with values to be mapped in the Captcha.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set mapper API value during initialization  
        $("#captcha1").ejCaptcha({  mapper: "GetCurrentItem"}); 
&lt;/script&gt;                         </code>
</pre>






#### maximumLength<span class="type-signature type number">number</span>








Specifies the maximum number of characters used in the Captcha.




Default Value:
{:.param}






* 8








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set maximum length API value during initialization  
        $("#captcha1").ejCaptcha({  maximumLength: 8}); 
&lt;/script&gt;                         </code>
</pre>






#### minimumLength<span class="type-signature type number">number</span>








Specifies the minimum number of characters used in the Captcha.




Default Value:
{:.param}






* 4








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set minimum length API value during initialization  
        $("#captcha1").ejCaptcha({  minimumLength: 6}); 
&lt;/script&gt;                         </code>
</pre>






#### requestMapper<span class="type-signature type string">string</span>








Specifies the method to map values to Captcha.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set request mapper API value during initialization  
        $("#captcha1").ejCaptcha({  requestMapper: "GetCurrentItem"});  
&lt;/script&gt;                         </code>
</pre>






#### showAudioButton<span class="type-signature type boolean">boolean</span>








Sets the Captcha with audio support, that enables to dictate the captcha text.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set enable audio API value during initialization  
        $("#captcha1").ejCaptcha({  showAudioButton: true});    
&lt;/script&gt;                         </code>
</pre>






#### showRefreshButton<span class="type-signature type boolean">boolean</span>








Sets the Captcha with a refresh button.




Default Value:
{:.param}






* false








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set enable refresh API value during initialization  
        $("#captcha1").ejCaptcha({  showRefreshButton: true});  
&lt;/script&gt;                         </code>
</pre>






#### targetButton<span class="type-signature type string">string</span>








Specifies the target button of the Captcha to validate the entered text and captcha text.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;button id="button1"&gt;Submit&lt;/button&gt; 
&lt;script&gt;
//To set target button API value during initialization  
        $("#captcha1").ejCaptcha({  targetButton: "button1"});  
&lt;/script&gt;</code>
</pre>






#### targetInput<span class="type-signature type string">string</span>








Specifies the target input element that will verify the Captcha.




Default Value:
{:.param}






* null








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set target input API value during initialization  
        $("#captcha1").ejCaptcha({  targetInput: "input1"});    
&lt;/script&gt;</code>
</pre>






#### width<span class="type-signature type number">number</span>








Specifies the width of the Captcha.




Default Value:
{:.param}






* 150








##### Example

<pre class="prettyprint">
<code> 
&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//To set width API value during initialization  
        $("#captcha1").ejCaptcha({  width: 150});       
&lt;/script&gt;                         </code>
</pre>




### Events








#### refreshBegin








Fires when captch refresh begins.

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
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Refresh begin event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshBegin: function(args) {}
                                });     
&lt;/script&gt;                         </code>
</pre>






#### refreshComplete








Fires after captch refresh completed.

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
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Refresh complete event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshComplete: function(args) {}
                                });     
&lt;/script&gt;                         </code>
</pre>






#### refreshFailure








Fires when captch refresh fails to load.

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
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Refresh failure event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshFailure: function(args) {}
                                });     
&lt;/script&gt;                         </code>
</pre>






#### refreshSuccess








Fires after captch refresh succeeded.

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
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name"><code>argument.type</code></td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




##### Example

<pre class="prettyprint">
<code>&lt;div id="captcha1"&gt;&lt;/div&gt; 
 
&lt;script&gt;
//Refresh success event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshSuccess: function(args) {}
                                });     
&lt;/script&gt;                         </code>
</pre>



