---
layout: post
title: ejCaptcha
documentation: API
platform: js
metaname: 
metacontent: 
---

# ejCaptcha


Captcha is a popular technique that is used to prevent computer programs from sending automated requests and is used for meta-searching search engines, performing dictionary attacks in login pages, or sending spam by using mail servers. Captcha is validated at the time of form submission.







$(element).ejCaptcha<span class="signature">(options)</span>







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
options{% endhighlight %}</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">settings for Captcha</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
// Create Captcha
$('#Captcha1').ejCaptcha();     
</script>{% endhighlight %}







Requires
{:.require}




* module:jQuery


* module:ej.core.js


* module:ej.captcha.js


* module:ej.button.js




## Members








### characterSet  `string`
{:#members:characterset}








Specifies the character set of the Captcha that will be used to generate captcha text randomly.




Default Value:
{:.param}






* "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789"








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set character set API value during initialization  
        $("#captcha1").ejCaptcha({  characterSet: "ABCD1234"}); 
</script>                         {% endhighlight %}







### customErrorMessage  `string`
{:#members:customerrormessage}








Specifies the error message to be displayed when the Captcha mismatch.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set error message API value during initialization  
        $("#captcha1").ejCaptcha({  customErrorMessage: "InValid Captcha"});    
</script>                         {% endhighlight %}







### enableAutoValidation  `boolean`
{:#members:enableautovalidation}








Set the Captcha validation automatically.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set auto validation API value during initialization  
        $("#captcha1").ejCaptcha({  enableAutoValidation: true});       
</script>                         {% endhighlight %}







### enableCaseSensitivity  `boolean`
{:#members:enablecasesensitivity}








Specifies the case sensitivity for the characters typed in the Captcha.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set case sensitivity API value during initialization  
        $("#captcha1").ejCaptcha({  enableCaseSensitivity: true});      
</script>                         {% endhighlight %}







### enablePattern  `boolean`
{:#members:enablepattern}








Specifies the background patterns for the Captcha.




Default Value:
{:.param}






* true








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set target input API value during initialization  
        $("#captcha1").ejCaptcha({  enablePattern: true});      
</script>{% endhighlight %}







### enableRTL  `boolean`
{:#members:enablertl}








Sets the Captcha direction as right to left alignment.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set enable RTL API value during initialization  
        $("#captcha1").ejCaptcha({  enableRTL: true});  
</script>                         {% endhighlight %}







### hatchStyle  `enum`
{:#members:hatchstyle}








Specifies the background apperance for the captcha.




Default Value:
{:.param}






* value set as BackwardDiagonal








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set mapper API value during initialization  
        $("#captcha1").ejCaptcha({  hatchStyle: "BackwardDiagonal"});   
</script>                         {% endhighlight %}







### height  `number`
{:#members:height}








Specifies the height of the Captcha.




Default Value:
{:.param}






* 50








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set height API value during initialization  
        $("#captcha1").ejCaptcha({  height: 50});       
</script>                 {% endhighlight %}







### mapper  `string`
{:#members:mapper}








Specifies the method with values to be mapped in the Captcha.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set mapper API value during initialization  
        $("#captcha1").ejCaptcha({  mapper: "GetCurrentItem"}); 
</script>                         {% endhighlight %}







### maximumLength  `number`
{:#members:maximumlength}








Specifies the maximum number of characters used in the Captcha.




Default Value:
{:.param}






* 8








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set maximum length API value during initialization  
        $("#captcha1").ejCaptcha({  maximumLength: 8}); 
</script>                         {% endhighlight %}







### minimumLength  `number`
{:#members:minimumlength}








Specifies the minimum number of characters used in the Captcha.




Default Value:
{:.param}






* 4








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set minimum length API value during initialization  
        $("#captcha1").ejCaptcha({  minimumLength: 6}); 
</script>                         {% endhighlight %}







### requestMapper  `string`
{:#members:requestmapper}








Specifies the method to map values to Captcha.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set request mapper API value during initialization  
        $("#captcha1").ejCaptcha({  requestMapper: "GetCurrentItem"});  
</script>                         {% endhighlight %}







### showAudioButton  `boolean`
{:#members:showaudiobutton}








Sets the Captcha with audio support, that enables to dictate the captcha text.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set enable audio API value during initialization  
        $("#captcha1").ejCaptcha({  showAudioButton: true});    
</script>                         {% endhighlight %}







### showRefreshButton  `boolean`
{:#members:showrefreshbutton}








Sets the Captcha with a refresh button.




Default Value:
{:.param}






* false








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set enable refresh API value during initialization  
        $("#captcha1").ejCaptcha({  showRefreshButton: true});  
</script>                         {% endhighlight %}







### targetButton  `string`
{:#members:targetbutton}








Specifies the target button of the Captcha to validate the entered text and captcha text.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<button id="button1">Submit</button> 
<script>
//To set target button API value during initialization  
        $("#captcha1").ejCaptcha({  targetButton: "button1"});  
</script>{% endhighlight %}







### targetInput  `string`
{:#members:targetinput}








Specifies the target input element that will verify the Captcha.




Default Value:
{:.param}






* null








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set target input API value during initialization  
        $("#captcha1").ejCaptcha({  targetInput: "input1"});    
</script>{% endhighlight %}







### width<span class="type-signature type number">number</span>
{:#members:width}








Specifies the width of the Captcha.




Default Value:
{:.param}






* 150








Example
{:.example}


{% highlight html %}
 
<div id="captcha1"></div> 
 
<script>
//To set width API value during initialization  
        $("#captcha1").ejCaptcha({  width: 150});       
</script>                         {% endhighlight %}





## Events








### refreshBegin
{:#events:refreshbegin}








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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="captcha1"></div> 
 
<script>
//Refresh begin event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshBegin: function(args) {}
                                });     
</script>                         {% endhighlight %}







### refreshComplete
{:#events:refreshcomplete}








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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="captcha1"></div> 
 
<script>
//Refresh complete event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshComplete: function(args) {}
                                });     
</script>                         {% endhighlight %}







### refreshFailure
{:#events:refreshfailure}








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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="captcha1"></div> 
 
<script>
//Refresh failure event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshFailure: function(args) {}
                                });     
</script>                         {% endhighlight %}







### refreshSuccess
{:#events:refreshsuccess}








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
<td class="name">
cancel</td>
<td class="type"><span class="param-type">boolean</span></td>
<td class="description last">if the event should be canceled; otherwise, false.</td>
</tr>
<tr>
<td class="name">
model</td>
<td class="type"><span class="param-type">object</span></td>
<td class="description last">returns the Captcha model</td>
</tr>
<tr>
<td class="name">
type</td>
<td class="type"><span class="param-type">string</span></td>
<td class="description last">returns the name of the event</td>
</tr>
</tbody>
</table>




Example
{:.example}


{% highlight html %}
<div id="captcha1"></div> 
 
<script>
//Refresh success event of Captcha control 
        $("#captcha1").ejCaptcha({  
                                refreshSuccess: function(args) {}
                                });     
</script>                         {% endhighlight %}




