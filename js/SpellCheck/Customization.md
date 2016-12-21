---
title: SpellCheck - Customization
description: SpellCheck Customization
platform: js
control: spellcheck
documentation: ug
keywords: customization, spellcheck customization, misspell word appearance, restrict suggestion count 
---
# SpellCheck customization

The Essential JavaScript SpellCheck provides option to customize for the following scenarios.

* Misspell word appearance
* Restrict suggestion count
    
## Misspell word appearance

The SpellCheck control provide the support([misspellWordCss](/js/api/ejspellcheck#members:misspellwordcss)) to display the error word in user defined style. By default displaying the error words with the red underline. 

The following code example depicts the way to customize the error word highlight (displaying error word with red color font and lightblue background).

{% highlight html %}
    <div id="SpellCheck"></div>
    
    <script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                misspellWordCss: "highlight",
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
        });
    </script>
    <style>
        .highlight {
            background-color: lightblue;
            color: red;
        }
    </style> 

{% endhighlight %}

## Restrict suggestion count

The SpellCheck control provides option ([maxSuggestionCount](/js/api/ejspellcheck#members:maxsuggestioncount)) to restrict the count that the number of items displayed in the suggestion list.

The following code example describes the way to control the suggestion count.

{% highlight html %}
    <div id="SpellCheck"></div>
    
    <script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                maxSuggestionCount: 3,
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
        });
    </script>
{% endhighlight %}