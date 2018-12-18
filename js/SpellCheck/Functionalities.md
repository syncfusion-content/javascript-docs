---
title: Syncfusion SpellCheck - Functionalities
description: SpellCheck Functionalities
platform: js
control: spellcheck
documentation: ug
keywords: spellcheck functionalities, check spelling, ignore words, change words, change, ignore, ignore settings, SpellCheck on typing,
api: /api/js/ejspellcheck
---
# Functionalities

## Check Spelling

The main functionality of the SpellCheck control is checking the spelling of a word and returns the suggestions for an error word.

For example, if you pass the sentence that contains misspell words as input, you can know the error words in this sentence and its suggestions (apt words to replace).

## Ignore Words

The SpellCheck control provides the support to ignore the words from an error word consideration and also to ignore an error words whenever needed. Please refer the following options to ignore the words.

### Ignore

The [ignore](/api/js/ejspellcheck#methods:ignore) option is used to ignore a specific word once from the given input string. 

The following code example describes the above method implementation.

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = 'The <span class="errorspan e-errorword">textarea</span> sample uses a dialog to display the spell errors.';

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.ignore("textarea",targetSentence, null);
</script>

{% endhighlight %} 

### Ignore All

The [ignore all](/api/js/ejspellcheck#methods:ignoreall) option is used to ignore all the error word occurrences from the given input string.

The following code example describes the way of using ignore all method.

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = 'This <span class="errorspan e-errorword">textarea</span> sample uses a dialog to display all the <span class="errorspan e-errorword">textarea</span> spell errors.';

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.ignoreAll("textarea",targetSentence, null);
</script>

{% endhighlight %}

### Word Collection to Ignore

The [ignore words](/api/js/ejspellcheck#members:ignorewords) option is used to ignore the collection of words from an error word checking. You can pass the technical terms, brand names which is not present in the dictionary file to this property "ignoreWords" as shown in the following code example and then while checking the spelling these passed words are considered as a correct word.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({                
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                ignoreWords:["TypeScript", "JavaScript"]
            });
        });      

</script>

{% endhighlight %}

## Ignore Settings

The [ignore settings](/api/js/ejspellcheck#members:ignoresettings) helps to ignore the uppercase, mixed case words, alphanumeric words, file path and email addresses from the error word checking. Ignore settings contains the following options to ignore the words based on their category.

* [ignoreAlphaNumericWords](/api/js/ejspellcheck#members:ignoresettings-ignorealphanumericwords) - ignoring the alpha numeric words from an error word consideration.
* [ignoreUpperCase](/api/js/ejspellcheck#members:ignoresettings-ignoreuppercase) - ignoring the upper case words from an error word consideration.
* [ignoreMixedCaseWords](/api/js/ejspellcheck#members:ignoresettings-ignoremixedcasewords) - ignoring the mixed case words from an error word consideration.
* [ignoreFileNames](/api/js/ejspellcheck#members:ignoresettings-ignorefilenames) - ignoring the file address path from an error word consideration.
* [ignoreUrl](/api/js/ejspellcheck#members:ignoresettings-ignoreurl) - ignoring the url links from an error word consideration.
* [ignoreEmailAddress](/api/js/ejspellcheck#members:ignoresettings-ignoreemailaddress) - ignoring the email address from an error word consideration.

The following code example uses to enable the checking of all the words formed with alphanumeric, uppercase, mixed case words and file paths and email addresses.  

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({                
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                ignoreSettings:{
                    ignoreAlphaNumericWords:false,
                    ignoreMixedCaseWords:false,
                    ignoreUpperCase:false,
                    ignoreUrl:false,
                    ignoreEmailAddress:false,
                    ignoreFileNames:false
                }
            });
        });      

</script>

{% endhighlight %}

## Change Words

The SpellCheck control provides the support to change an error words from its possible suggestions. Please refer the following options to change an error word.

### Change

The [change](/api/js/ejspellcheck#methods:change) option is used to replace an error word occurrences once from the given input string with the correct word.

The following code example describes the behavior of change method.

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = 'The <span class="errorspan e-errorword">textarea</span> sample uses a dialog to display the spell errors.';

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.change("textarea",targetSentence,"text area", null);

</script>

{% endhighlight %}

### Change All

The [change all](/api/js/ejspellcheck#methods:changeall) option is used to replace all the occurrences of an error word with the correct word(selected from the suggestions list) from the given inputs string.

The following code example uses to change all the error word occurrences.

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            var targetSentence = 'This <span class="errorspan e-errorword">textarea</span> sample uses a dialog to display all the <span class="errorspan e-errorword">textarea</span> spell errors.';

            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.changeAll("textarea",targetSentence,"text area", null);

</script>

{% endhighlight %}

## Custom Words

The SpellCheck control provides the support to add the custom words into the custom dictionary file.

The [addToDictionary](/api/js/ejspellcheck#methods:addToDictionary) option is used to add the custom words into the custom dictionary file by using [`customDictionaryUrl`](/api/js/ejspellcheck#members:dictionarysettings-customdictionaryurl) property.

The following code example uses to add the custom word into the custom dictionary file.

{% highlight html %}

<div id="SpellCheck"></div> 
 
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.addToDictionary("textarea");

</script>

{% endhighlight %}

You can also add the custom words into the custom dictionary file through the dialog mode or context menu mode add to dictionary option.

* Dialog Mode - Add To Dictionary button is available in the dialog window, while highlighting the error word in the given input string and clicking this button then the word will be adding into the custom dictionary file.
* Context Menu Mode - Add To Dictionary option is available while right click on the error word and selecting this option, the word will be adding into the custom dictionary file.


## Checking content on typing

SpellCheck control provides support for checking the content, on pressing the `Enter` and `Space` key. The cursor position will also be properly retained, while processing the SpellCheck operations. If you enable “enableValidateOnType” property, the spellcheck operation will be carried out on typing.

The following code example describes the above behavior.


{% highlight html %}

<div id="SpellCheck" contenteditable="true">

It is a concept vehicle with Liquid Silver body color, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)and 400  (295.02 lbf ft), diesel particulate filter and 
BlueTec emission control system, quattro permanent four-wheel drive system,Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.

</div>
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                contextMenuSettings: {enable: true},
                enableValidateOnType: true
            });
</script>

{% endhighlight %}

The following screenshot displays the output for the above code

![SpellCheck validation type image](ValidateOnType_images/validateontype.png)


You can also validate the content within the IFrame element or IFrame element target text, by passing the IFrame element id or class name value to the `controlsToValidate` property. 
Detailed information is given [here](https://help.syncfusion.com/js/spellcheck/multiple-target)

## Suggestion Words

The [`getSuggestionWords`](/api/js/ejspellcheck#methods:getsuggestionwords) option is used to retrieve the possible suggestion words for an error word which is provided to correct that spelling. By using [`maxSuggestionCount`](/api/js/ejspellcheck#members:maxsuggestioncount), you can set the maximum suggestion display count.

The following code example describes the above behavior.


{% highlight html %}

<div id="SpellCheck" contenteditable="true">

It is a concept vehicle with Liquid Silver body color, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)and 400  (295.02 lbf ft), diesel particulate filter and 
BlueTec emission control system, quattro permanent four-wheel drive system,Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.

</div>
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.getSuggestionWords("textarea");
            setTimeout(function () {
				alert(spellObj._suggestedWords);
			}, 800);
</script>

{% endhighlight %}

N> You can get the suggestion words after some time interval once this method is called. Since, ajax request processing takes place in the background.

## Synchronous request

On setting [`enableAsync`](/api/js/ejspellcheck#members:enableasync) option to false, enables the synchronous request to the server to perform SpellCheck operations.

The following code example describes the above behavior.


{% highlight html %}

<div id="SpellCheck" contenteditable="true">

It is a concept vehicle with Liquid Silver body color, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)and 400  (295.02 lbf ft), diesel particulate filter and 
BlueTec emission control system, quattro permanent four-wheel drive system,Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.

</div>
<script>
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                enableAsync: false,
                ajaxDataType: "json"
            });            
</script>

{% endhighlight %}

N> You need to set the [`ajaxDataType`](/api/js/ejspellcheck#members:ajaxdatatype) value as `json` to retrieve the synchronous request result properly.