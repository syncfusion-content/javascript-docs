---
layout: post
title: API reference for ejSpellCheck
description: What are the options, methods and events available in Essential JavaScript ejSpellCheck.
documentation: API
platform: js
keywords: ejSpellCheck, API, Essential JS ejSpellCheck, SpellCheck
---

# ejSpellCheck

The spell check control will be using to check/correct the spelling of words from a given content.

#### Syntax

{% highlight javascript %}

$(element).ejSpellCheck()

{% endhighlight %}

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
    $('#SpellCheck').ejSpellCheck();
</script>

{% endhighlight %}


#### Requires

* module:jQuery
* module:ej.core.js
* module:ej.data.js
* module:ej.globalize.js
* module:ej.scroller.js
* module:ej.draggable.js
* module:ej.dialog.js
* module:ej.button.js
* module:ej.listbox.js
* module:ej.menu.js
* module:ej.spellcheck.js

## Members

### dictionarySettings `object`
{:#members:dictionarysettings}

It includes the service method path to find the error words and its suggestions also adding the custom word into the custom dictionary.

#### Example – DictionarySettings field mapped with string type values

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

### dictionarySettings.dictionaryUrl `string`
{:#members:dictionarysettings-dictionaryurl}

The dictionaryUrl option accepts string, which is the method path to find the error words and get the suggestions to correct the errors.

#### Default Value

* ""

#### Example – To set the dictionaryUrl of SpellCheck control

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords"
                }
            });
        });
</script>

{% endhighlight %}

### dictionarySettings.customDictionaryUrl `string`
{:#members:dictionarysettings-customdictionaryurl}

The customDictionaryUrl option accepts string, which is the method path to add the error word into the custom dictionary.

#### Default Value

* ""

#### Example – To set the customDictionaryUrl of SpellCheck control

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

### misspellWordCss `string`
{:#members:misspellwordcss}

To display the error word in a customized style.

#### Default Value

* "e-errorword"

#### Example - To display the error word in green color.

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                misspellWordCss: "highlight",
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

<style>
    .highlight {
        color: green;
    }
</style>
{% endhighlight %}

### locale `string`
{:#members:locale}

Sets the specific culture to the SpellCheck.

#### Default Value

* "en-US"

#### Example - To set the French culture on SpellCheck, set its locale as fr-FR.

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                locale: "fr-FR",
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

> To set any culture for SpellCheck, refer to the required minified globalize files of the specific culture. For example, to use fr-FR culture in SpellCheck, refer to the **globalize.culture.fr-FR.min.js** script file. Also define the locale words of that specific culture properly. For example, define the locale words for fr-FR culture in a variable ej.SpellCheck.Locale[“fr-FR”] = { }; under script section.

### maxSuggestionCount `number`
{:#members:maxsuggestioncount}

To set the maximum suggestion display count.

#### Default Value

* 6

#### Example - To set the maxSuggestionCount value as 4.

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                maxSuggestionCount: 4,
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

### ignoreWords `array`
{:#members:ignorewords}

To ignore the words from the error word consideration.

#### Default Value

* []

#### Example - To set the ignoreWords.

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                ignoreWords: ["Syncfusion", "JavaScript"],
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

### contextMenuSettings `object`
{:#members:contextmenusettings}

Holds all options related to the context menu settings of SpellCheck.

### contextMenuSettings.enable `boolean`
{:#members:contextmenusettings-enable}

When set to true, enables the context menu options available for the SpellCheck.

#### Default Value

* true

#### Example - To disable the context menu options for SpellCheck control.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                contextMenuSettings: {
                    enable: false
                },
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
        });
</script>

{% endhighlight %}

### contextMenuSettings.menuItems `array`
{:#members:contextmenusettings-menuitems}

Contains all the default context menu options that are applicable for SpellCheck. It also supports adding custom menu items. All the SpellCheck related context menu items are grouped under this menu collection.

#### Default Value

* {% highlight javascript %}

    [
        { id: "IgnoreAll", text: "Ignore All" },
        { id: "AddToDictionary", text: "Add To Dictionary" }
    ]
  
  {% endhighlight %}

#### Example - To add custom context menu option to the SpellCheck.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                contextMenuSettings: {
                    enable: true,
                    menuItems: [
                        { id: "Ignore", text: "IgnoreOnce" },
                        { id: "IgnoreAll", text: "Ignore All" },
                        { id: "AddToDictionary", text: "Add To Dictionary" }
                    ]
                },
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                contextClick:"onCustomMenuClick"
            });
        });


        function onCustomMenuClick(args) {
            if (args.events.ID == "Ignore") {
                var spellObj = $("#TextArea").data("ejSpellCheck");
                var ignoreResult = spellObj.ignore(args.selectedValue, args.targetContent, 0);
            }
        }

</script>

{% endhighlight %}

### ignoreSettings `object`
{:#members:ignoresettings}

It helps to ignore the uppercase, mixed case words, alpha numeric words, file path and email addresses based on the property values.

### ignoreSettings.ignoreAlphaNumericWords `string`
{:#members:ignoresettings-ignorealphanumericwords}

When set to true, ignoring the alphanumeric words from the error word consideration.

#### Default Value

* true

#### Example – To consider the alphanumeric words as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreAlphaNumericWords:false
                }
            });
        });
</script>

{% endhighlight %}

### ignoreSettings.ignoreEmailAddress `boolean`
{:#members:ignoresettings-ignoreemailaddress}

When set to true, ignoring the Email address from the error word consideration.

#### Default Value

* true

#### Example – To consider the Email Address as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreEmailAddress:false
                }
            });
        });
</script>

{% endhighlight %}

### ignoreSettings.ignoreMixedCaseWords `boolean`
{:#members:ignoresettings-ignoremixedcasewords}

When set to true, ignoring the MixedCase words from the error word consideration.

#### Default Value

* true

#### Example – To consider the MixedCase words as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreMixedCaseWords:false
                }
            });
        });
</script>

{% endhighlight %}

### ignoreSettings.ignoreUpperCase `boolean`
{:#members:ignoresettings-ignoreuppercase}

When set to true, ignoring the UpperCase words from the error word consideration.

#### Default Value

* true

#### Example – To consider the UpperCase words as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreUpperCase:false
                }
            });
        });
</script>

{% endhighlight %}

### ignoreSettings.ignoreUrl `boolean`
{:#members:ignoresettings-ignoreurl}

When set to true, ignoring the Url from the error word consideration.

#### Default Value

* true

#### Example – To consider the Url as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreUrl:false
                }
            });
        });
</script>

{% endhighlight %}

### ignoreSettings.ignoreFileNames `boolean`
{:#members:ignoresettings-ignorefilenames}

When set to true, ignoring the file address path from the error word consideration.

#### Default Value

* true

#### Example – To consider the file names as an error word

{% highlight html %}

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                },
                ignoreSettings:{
                    ignoreFileNames:false
                }
            });
        });
</script>

{% endhighlight %}


## Methods

### showInDialog()
{:#methods:showindialog}

Open the dialog to correct the spelling of the target content.

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.showInDialog(); // Open the dialog mode
</script>

{% endhighlight %}

### validate()
{:#methods:validate}

Highlighting the error word in the target area itself and correct the spelling using the context menu.

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                 dictionarySettings: {
                     dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                     customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                 }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.validate(); // highlighting the error word in the target area itself 
</script>

{% endhighlight %}

### spellCheck(targetSentence, misspellWordCss)
{:#methods:spellcheck}

To get the error word highlighted string by passing the given input sentence.

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
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Content to be spell check</td>
        </tr>
        <tr>
            <td class="name">misspellWordCss</td>
            <td class="type">string</td>
            <td class="description">Class name that contains style value to highlight the error word</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = "This exmple sentence cantains errow words".
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.spellCheck(targetSentence,"highlight");
</script>
<style>
    .highlight {
        color: green;
    }
</style>

{% endhighlight %}

### ignoreAll(word, targetSentence)
{:#methods:ignoreall}

To ignore all the error word occurences from the given input sentence.

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
            <td class="name">word</td>
            <td class="type">string</td>
            <td class="description">Error word to ignore from the target content</td>
        </tr>
        <tr>
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Content to perform the ignore all operation</td>
        </tr>        
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = "The first textarea sampeel uses a dialog textarea to display the sampeel spell textarea errrors".

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.ignoreAll("textarea",targetSentence);
</script>

{% endhighlight %}


### ignore(word, targetSentence, index)
{:#methods:ignore}

To ignore the error word once from the given input sentence.

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
            <td class="name">word</td>
            <td class="type">string</td>
            <td class="description">Error word to ignore from the target content</td>
        </tr>
        <tr>
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Content to perform the ignore operation</td>
        </tr>        
        <tr>
            <td class="name">index</td>
            <td class="type">number</td>
            <td class="description">Index of the error word present in the target content</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = "The first textarea sampeel uses a dialog textarea to display the sampeel spell textarea errrors".

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.ignore("textarea",targetSentence, null);
</script>

{% endhighlight %}


### change(word, targetSentence, changeWord, index)
{:#methods:change}

To change the error word once from the given input sentence.

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
            <td class="name">word</td>
            <td class="type">string</td>
            <td class="description">Error word to change from the target content</td>
        </tr>
        <tr>
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Content to perform the change operation</td>
        </tr>
        <tr>
            <td class="name">changeWord</td>
            <td class="type">string</td>
            <td class="description">Word to replace with the error word</td>
        </tr>        
        <tr>
            <td class="name">index</td>
            <td class="type">number</td>
            <td class="description">Index of the error word present in the target content</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = "The first textarea sampeel uses a dialog textarea to display the sampeel spell textarea errrors".

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.change("textarea",targetSentence,"text area", null);

</script>

{% endhighlight %}

> The 'index' is the error word occurence in the given input string. For example, if you pass the index value as 1 means and the error word as textarea it will
ignore the second occurence (which is present after the word dialog) in the given string.  

### changeAll(word, targetSentence, changeWord)
{:#methods:changeall}

To change all the error word occurences from the given input sentence.

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
            <td class="name">word</td>
            <td class="type">string</td>
            <td class="description">Error word to change from the target content</td>
        </tr>
        <tr>
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Content to perform the change all operation</td>
        </tr>
        <tr>
            <td class="name">changeWord</td>
            <td class="type">string</td>
            <td class="description">Word to replace with the error word</td>
        </tr>  
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = "The first textarea sampeel uses a dialog textarea to display the sampeel spell textarea errrors".

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.changeAll("textarea",targetSentence,"text area");
</script>

{% endhighlight %}

### addToDictionary(word)
{:#methods:addtodictionary}

To add the words into the custom dictionary.

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
            <td class="name">Customword</td>
            <td class="type">string</td>
            <td class="description">Word to add into the dictionary file</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.addToDictionary("textarea");
</script>

{% endhighlight %}


## Events

### actionSuccess
{:#events:actionsuccess}

Triggers on the success of ajax call request.

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
            <td class="name">resultHTML</td>
            <td class="type">string</td>
            <td class="description">Returns the error word highlighted string.</td>
        </tr>
        <tr>
            <td class="name">errorWordDetails</td>
            <td class="type">object</td>
            <td class="description">Returns the error word details of the given input.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                actionSuccess: function (args) {}
            });
</script>

{% endhighlight %}

### actionBegin
{:#events:actionbegin}

Triggers on the ajax call request begining.

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
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Returns the input string.</td>
        </tr>
        <tr>
            <td class="name">misspellWordCss</td>
            <td class="type">string</td>
            <td class="description">Returns the misspellWordCss class name.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}

<div id="SpellCheck"></div> 

<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                actionBegin: function (args) {}
            });
</script>

{% endhighlight %}

### actionFailure
{:#events:actionfailure}

Triggers when the ajax call request failure.

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
            <td class="name">errorMessage</td>
            <td class="type">string</td>
            <td class="description">Returns ajax request failure error message.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 

<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                actionFailure: function (args) {}
            });
</script>

{% endhighlight %}


### start
{:#events:start}

Triggers when the dialog mode spell check starting.

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
            <td class="name">targetSentence</td>
            <td class="type">string</td>
            <td class="description">Returns the input string.</td>
        </tr>
        <tr>
            <td class="name">errorWords</td>
            <td class="type">object</td>
            <td class="description">Returns the error words details.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                start: function (args) {}
            });
</script>

{% endhighlight %}


### complete
{:#events:complete}

Triggers when the spell check operations completed through dialog mode.

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
            <td class="name">resultHTML</td>
            <td class="type">string</td>
            <td class="description">Returns the error word highlighted string.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                complete: function (args) {}
            });
</script>

{% endhighlight %}

### contextOpen
{:#events:contextopen}

Triggers before context menu opening.

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
            <td class="name">selectedErrorWord</td>
            <td class="type">string</td>
            <td class="description">Returns the selected error word.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                contextOpen: function (args) {}
            });
</script>

{% endhighlight %}


### contextClick
{:#events:contextclick}

Triggers when the context menu item clicked.

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
            <td class="name">selectedValue</td>
            <td class="type">string</td>
            <td class="description">Returns the selected error word.</td>
        </tr>
        <tr>
            <td class="name">selectedOption</td>
            <td class="type">string</td>
            <td class="description">Returns the selected option in the context menu.</td>
        </tr>
        <tr>
            <td class="name">targetContent</td>
            <td class="type">string</td>
            <td class="description">Returns the input string.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                contextClick: function (args) {}
            });
</script>

{% endhighlight %}

### dialogBeforeOpen
{:#events:dialogbeforeopen}

Triggers before the spell check dialog opens.

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
            <td class="name">spellCheckDialog</td>
            <td class="type">object</td>
            <td class="description">Returns the spell check window details.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                dialogBeforeOpen: function (args) {}
            });
</script>

{% endhighlight %}

### dialogOpen
{:#events:dialogopen}

Triggers after the spell check dialog opens.

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
            <td class="name">targetText</td>
            <td class="type">string</td>
            <td class="description">Returns the target input.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                dialogOpen: function (args) {}
            });
</script>

{% endhighlight %}

### dialogClose
{:#events:dialogclose}

Triggers when the spell check dialog closed.

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
            <td class="name">updatedText</td>
            <td class="type">string</td>
            <td class="description">Returns the error corrected string.</td>
        </tr>
        <tr>
            <td class="name">requestType</td>
            <td class="type">string</td>
            <td class="description">Returns the request type value.</td>
        </tr>
        <tr>
            <td class="name">cancel</td>
            <td class="type">boolean</td>
            <td class="description">Returns the cancel option value.</td>
        </tr>
        <tr>
            <td class="name">model</td>
            <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
            <td class="description">Returns the SpellCheck model.</td>
        </tr>
        <tr>
            <td class="name">type</td>
            <td class="type">string</td>
            <td class="description">Returns the name of the event.</td>
        </tr>
    </tbody>
</table>


#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                dialogClose: function (args) {}
            });
</script>

{% endhighlight %}

### validating
{:#events:validating}

Triggers when the spell check control performing the spell check operations such as ignore, ignoreAll, change, changeAll and addToDictionary.

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
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when ignore the error word once:
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
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">ignoreWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the error word to ignore.</td>
                </tr>
                <tr>
                    <td class="name">targetContent</td>
                    <td class="type">string</td>
                    <td class="description">Returns the target content.</td>
                </tr>
                <tr>
                    <td class="name">index</td>
                    <td class="type">number</td>
                    <td class="description">Returns the index of an error word.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
                    <td class="description">Returns the SpellCheck model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the validating request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when ignore all the occurences of an error word:
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
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">ignoreWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the error word to ignore.</td>
                </tr>
                <tr>
                    <td class="name">targetContent</td>
                    <td class="type">string</td>
                    <td class="description">Returns the target content.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
                    <td class="description">Returns the SpellCheck model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the validating request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when changing the error word occurence once:
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
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">changableWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the error word to change.</td>
                </tr>
                <tr>
                    <td class="name">targetContent</td>
                    <td class="type">string</td>
                    <td class="description">Returns the target content.</td>
                </tr>
                <tr>
                    <td class="name">changeWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the change word to replace the error word.</td>
                </tr>
                <tr>
                    <td class="name">index</td>
                    <td class="type">number</td>
                    <td class="description">Returns the index of an error word.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
                    <td class="description">Returns the SpellCheck model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the validating request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
        </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when changing all the occurences of an error word:
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
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">changableWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the error word to change.</td>
                </tr>
                <tr>
                    <td class="name">targetContent</td>
                    <td class="type">string</td>
                    <td class="description">Returns the target content.</td>
                </tr>
                <tr>
                    <td class="name">changeWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the change word to replace the error word.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
                    <td class="description">Returns the SpellCheck model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the validating request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
            </tbody>
          </table>
        </td>
    </tr>
    <tr>
        <td class="name">argument</td>
        <td class="type">object</td>
        <td class="description">Event parameters when adding the error word into the dictionary file:
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
                    <td class="name">cancel</td>
                    <td class="type">boolean</td>
                    <td class="description">Returns the cancel option value.</td>
                </tr>
                <tr>
                    <td class="name">customWord</td>
                    <td class="type">string</td>
                    <td class="description">Returns the custom word to add into dictionary file.</td>
                </tr>
                <tr>
                    <td class="name">model</td>
                    <td class="type"><ts ref="ej.SpellCheck.Model"/><span class="param-type">object</span></td>
                    <td class="description">Returns the SpellCheck model.</td>
                </tr>
                <tr>
                    <td class="name">requestType</td>
                    <td class="type">string</td>
                    <td class="description">Returns the validating request type.</td>
                </tr>
                <tr>
                    <td class="name">type</td>
                    <td class="type">string</td>
                    <td class="description">Returns the name of the event.</td>
                </tr>
              </tbody>
            </table>
        </td>
    </tr>
    </tbody>
</table>

#### Example

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/GetCustomDictionary"
                }
                validating: function (args) {}
            });
</script>

{% endhighlight %}
