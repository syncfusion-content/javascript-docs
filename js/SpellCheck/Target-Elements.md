---
title: Syncfusion SpellCheck - Working with Target Elements
description: Target element's text spell checking with Syncfusion SpellCheck
platform: js
control: spellcheck
documentation: ug
keywords: multiple target, target element check, iframe element check
api: /api/js/ejspellcheck
---

# Supported Target Elements

The SpellCheck control has support for spell checking for the HTML element’s texts such as div, span, textarea, input, address, article and IFrame elements.

The following code example describes the spell checking of HTML element’s.

{% highlight html %}

<div class="control">
        London, one of the most popular tourist destinations in the world for a reason. A cultural and historical hub, London has an excellent public transportation system that allows visitors to see all the fantastic sights without spending a ton of money on a rental car. London contains four World Heritage Sites.
</div>
<div>
        <input type="button" id="CheckSpell" />
</div>

<script>
           // Rendering the spellcheck control
           $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            // Rendering the button control to call the spell check method to perform spell check
            $("#CheckSpell").ejButton({
                click: "correctErrors",
                text: "Spell check"
            });
            // Perform the spell check through dialog mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.showInDialog();
            }
            // Perform the spell check through context menu mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.validate();
            }

</script>

{% endhighlight %}

## IFrame Element

{% highlight html %}

<iframe id="SpellCheck" src="iframesource.html" height="300" width="800"></iframe>
    
<div>
    <input type="button" id=" CheckSpell " />
</div>

<script type="text/javascript">
           // Rendering the spellcheck control
           $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
            // Rendering the button control to call the spell check method to perform spell check
            $("#CheckSpell").ejButton({
                click: "correctErrors",
                text: "Spell check"
            });
            // Perform the spell check through dialog mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.showInDialog();
            }
            // Perform the spell check through context menu mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.validate();
            }
 </script>


{% endhighlight %}

Adding Styles

You can append the styles of error word from the application side, while performing the spellcheck through context menu mode for the IFrame element. Refer to the following code snippet to append the error word display style

{% highlight js %}

<script>

        var styleText = "<style type='text/css'>" +
                ".e-errorword {" +
                "background-image: url('themes/common-images/spellcheck/highlight.png'); " +
                "background-repeat: repeat-x; " +
                "background-position: bottom; } </style>"; // You can specify your own style with the error word css class name. Here e-errorword is the error word css class name
        $("#Spell").contents().find("head").append(styleText); // Here the Spell is the iFrame element Id

</script>

{% endhighlight %}


## Multiple Target

The SpellCheck control has support for multiple target HTML element’s texts spelling and correct its error words. This can be achieved by passing the target HTML elements “id” values or “CSS Class Name” or combination of both id and class names to the property [`controlsToValidate`](/api/js/ejspellcheck#members:controlstovalidate).

The following code example describes the above behavior.

{% highlight html %}

<div class="control">
        London, one of the most popular tourist destinations in the world for a reason. A cultural and historical hub, London has an excellent public transportation system that allows visitors to see all the fantastic sights without spending a ton of money on a rental car.
        London contains four World Heritage Sites.
</div>
<textarea id="control2">
        Paris, the city of lights and love - this short guide is full of ideas for how to make the most of the romanticism that oozes from every one of its beautiful corners.You couldn't possibly visit Paris without seeing the Eiffel Tower.
        Even if you do not want to visit this world famous structure, you will see its top from all over Paris.
</textarea>
<span class="control">
        Rome, one of the world's most fascinating cities. The old adage that Rome was not built in a day - and that you won't see it in one or even in three - is true. For the intrepid traveler who can keep pace, here is a list of must-sees.
        But remember what the Romans say: Even a lifetime isn't enough to see Rome.
</span>

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                controlsToValidate: ".control,#control2"
            });
        });
</script>

{% endhighlight %}

You need to pass the target HTML element’s id value or CSS class name or combination of the id value and class name with comma separator. Passing the class name followed by (.) character and passing the id value followed by the (#) character.

The following code example describes the spell checking of HTML element’s.

{% highlight html %}

<div class="control">
        London, one of the most popular tourist destinations in the world for a reason. A cultural and historical hub, London has an excellent public transportation system that allows visitors to see all the fantastic sights without spending a ton of money on a rental car. London contains four World Heritage Sites.
</div>
<span id="control1">
        Rome, one of the world's most fascinating cities. The old adage that Rome was not built in a day - and that you won't see it in one or even in three - is true. For the intrepid traveler who can keep pace, here is a list of must-sees.
        But remember what the Romans say: Even a lifetime isn't enough to see Rome.
</span>

<div id="SpellCheck"></div>

<div>
    <input type="button" id="CheckSpell" />
</div>

<script type="text/javascript">
    $(function () {
        $("#SpellCheck").ejSpellCheck({
            dictionarySettings: {
                dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
            },
            controlsToValidate: ".control,#control1"
        });
        $("#CheckSpell").ejButton({
            click: "correctErrors",
            text: "Spell check"
        });
    });
    
    // Perform the spell check through dialog mode
    function correctErrors() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        spellObj.showInDialog();
    }
    // Perform the spell check through context menu mode
    function correctErrors() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        spellObj.validate();
    }
</script>

{% endhighlight %}

The spellcheck component iterates through the target elements which specified in the “controlsToValidate” property, and process the element’s content one by one in the order of CSS elements, and id specified elements.

IFrame Element

{% highlight html %}

<iframe id="Spell" src="iframesource.html" height="300" width="800"></iframe>

<div id="SpellCheck"></div>

<div>
<input type="button" id=" CheckSpell " />
</div>

<script type="text/javascript">

    // Rendering the spellcheck control
           $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                controlsToValidate:"#Spell" // Here passing the IFrame element id value
            });
            // Rendering the button control to call the spell check method to perform spell check
            $("#CheckSpell").ejButton({
                click: "correctErrors",
                text: "Spell check"
            });
            // Perform the spell check through dialog mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.showInDialog();
            }
            // Perform the spell check through context menu mode
            function correctErrors() {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.validate();
            }
 </script>

{% endhighlight %}

N> If you want to spell check the IFrame’s element content, you pass the IFrame element alone in ‘controlsToValidate” property. You could not perform the spell check with the combination of other elements with IFrame element.