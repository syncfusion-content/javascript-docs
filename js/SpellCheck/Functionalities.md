---
title: SpellCheck - Functionalities
description: SpellCheck Functionalities
platform: js
control: spellcheck
documentation: ug
keywords: spellcheck functionalities, check spelling, ignore words, change words, change, ignore, ignore settings,
---
# Functionalities

## Check spelling

The main functionality of the SpellCheck control is checking the spelling of a word and returns the suggestions for an error word.

For example, if you pass the sentence that contains misspell words as input, you can know the error words in this sentence and its suggestions (apt words to replace).

## Ignore words

The SpellCheck control provides the support to ignore the words from an error word consideration and also to ignore an error words whenever needed. Please refer the following options to ignore the words.

### Ignore

The [ignore](/api/js/ejspellcheck#methods:ignore) option is used to ignore a specific word once from the given input string. 

The following code example describes the above method implementation.

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

### Ignore all

The [ignore all](/api/js/ejspellcheck#methods:ignoreall) option is used to ignore all the error word occurrences from the given input string.

The following code example describes the way of using ignore all method.

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
            schObj.ignoreAll("textarea",targetSentence, null);
</script>

{% endhighlight %}

### Word collection to ignore

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
                ignoreWords:["Syncfusion", "JavaScript"]
            });
        });      

</script>

{% endhighlight %}

## Ignore settings

The [ignore settings](/api/js/ejspellcheck#members:ignoresettings) helps to ignore the uppercase, mixed case words, alphanumeric words, file path and email addresses from the error word checking. Ignore settings contains the following options to ignore the words based on their category.

* [ignoreAlphaNumericWords](/api/js/ejspellcheck#members:ignoresettings-ignorealphanumericwords) - ignoring the alpha numeric words from an error word consideration.
* [ignoreUpperCase](/api/js/ejspellcheck#members:ignoresettings-ignoreuppercase) - ignoring the upper case words from an error word consideration.
* [ignoreMixedCaseWords](/api/js/ejspellcheck#members:ignoresettings-ignoremixedcasewords) - ignoring the mixed case words from an error word consideration.
* [ignoreFileNames](/api/js/ejspellcheck#members:ignoresettings-ignorefilenames) - ignoring the file address path from an error word consideration.
* [ignoreUrl](/api/js/ejspellcheck#members:ignoresettings-ignoreurl) - ignoring the url links from an error word consideration.
* [ignoreEmailAddress]((/api/js/ejspellcheck#members:ignoresettings-ignoreemailaddress)) - ignoring the email address from an error word consideration.

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

## Change words

The SpellCheck control provides the support to change an error words from its possible suggestions. Please refer the following options to change an error word.

### Change

The [change](/api/js/ejspellcheck#methods:change) option is used to replace an error word occurrences once from the given input string with the correct word.

The following code example describes the behavior of change method.

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

### Change all

The [change all](/api/js/ejspellcheck#methods:changeall) option is used to replace all the occurrences of an error word with the correct word(selected from the suggestions list) from the given inputs string.

The following code example uses to change all the error word occurrences.

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
            schObj.changeAll("textarea",targetSentence,"text area", null);

</script>

{% endhighlight %}