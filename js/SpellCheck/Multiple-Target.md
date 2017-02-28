---
title: SpellCheck - Multiple Target
description: Multiple target element's text spell checking with Syncfusion SpellCheck
platform: js
control: spellcheck
documentation: ug
keywords: multiple target, target element check
---
# Multiple Target

The SpellCheck control has support for multiple target HTML element's texts spelling and correct its error words. This can be achieved by passing the target HTML elements “id” values to the property “controlsToValidate”.

You can spell check most of the HTML element’s texts such as div, span, textarea, input, address and article by using this property.

The multiple target HTML element supports in both the modes.

i)	Dialog Mode
ii)	Context Menu Mode

The following code example describes the above behavior.

{% highlight html %}

<div id="control1">
        London, one of the most popular touist destinations in the world for a reason. A cultural and hisorical hub, London has an excellent public transportation system that allows visitors to see all the fantatic sights without spending a ton of money on a rental car.
        London contains four World Heritage Sites.
</div>
<textarea id="control2">
        Paris, the city of lihts and love - this short guide is full of ideas for how to make the most of the romnticism that oozes from every one of its beautiful corners.You couldn't possibly visit Paris without seeing the Eiffel Tower.
        Even if you do not want to visit this world famous structure, you will see its top from all over Paris.
</textarea>
<span id="control3">
        Rome, one of the world's most facinating cities. The old adage that Rome was not built in a day - and that you won't see it in one or even in three - is true. For the intrepid traveler who can keep pace, here is a list of must-sees.
        But reember what the Romans say: Even a lifetime isn't enough to see Rome.
</span>

<div id="SpellCheck"></div>

<script type="text/javascript">
        $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                controlsToValidate: "control1,control2,control3"
            });
        });
</script>

{% endhighlight %}

N> You need to pass the target HTML element's id value with the comma separator. For example, in the above code example passed id values of div(control1), textarea(control2) and span(control3) element.

## Dialog Mode

If the user specifies multiple targets in controlsToValidate property, the control must loop through the multiple HTML target elements one by one in the order which they are specified and process of every individual target’ content.

{% highlight html %}

<div id="control1">
        London, one of the most popular touist destinations in the world for a reason. A cultural and hisorical hub, London has an excellent public transportation system that allows visitors to see all the fantatic sights without spending a ton of money on a rental car.
        London contains four World Heritage Sites.
</div>
<textarea id="control2">
        Paris, the city of lihts and love - this short guide is full of ideas for how to make the most of the romnticism that oozes from every one of its beautiful corners.You couldn't possibly visit Paris without seeing the Eiffel Tower.
        Even if you do not want to visit this world famous structure, you will see its top from all over Paris.
</textarea>
<span id="control3">
        Rome, one of the world's most facinating cities. The old adage that Rome was not built in a day - and that you won't see it in one or even in three - is true. For the intrepid traveler who can keep pace, here is a list of must-sees.
        But reember what the Romans say: Even a lifetime isn't enough to see Rome.
</span>

<div id="SpellCheck"></div>
<div>
    <input type="button" id="SpellDialog" />
</div>

<script type="text/javascript">

    $(function () {
        $("#SpellCheck").ejSpellCheck({
            dictionarySettings: {
                dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
            },
            controlsToValidate: "control1,control2,control3"
        });

        $("#SpellDialog").ejButton({ 
            width: 100, 
            height: 25, 
            click: "showDialog", 
            text: "Spell check" 
        });
    });

    function showDialog() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        spellObj.showInDialog();
    }

</script>

{% endhighlight %}


## Context Menu Mode

By using controlsToValidate property, you can spell check multiple HTML elements at the same time through context menu. You can correct error word by right click on the error word and choose the corresponding context menu option.

{% highlight html %}

<div id="control1">
        London, one of the most popular touist destinations in the world for a reason. A cultural and hisorical hub, London has an excellent public transportation system that allows visitors to see all the fantatic sights without spending a ton of money on a rental car.
        London contains four World Heritage Sites.
</div>
<span id="control2">
        Rome, one of the world's most facinating cities. The old adage that Rome was not built in a day - and that you won't see it in one or even in three - is true. For the intrepid traveler who can keep pace, here is a list of must-sees.
        But reember what the Romans say: Even a lifetime isn't enough to see Rome.
</span>

<div id="SpellCheck"></div>
<div>
    <input type="button" id="SpellMenu" />
</div>

<script type="text/javascript">

    $(function () {
        $("#SpellCheck").ejSpellCheck({
            dictionarySettings: {
                dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
            },
            controlsToValidate: "control1, control2"
        });

        $("#SpellMenu").ejButton({ 
            width: 100, 
            height: 25, 
            click: "showInTarget", 
            text: "Spell check" 
        });
    });

    function showInTarget() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        spellObj.validate();
    }

</script>

{% endhighlight %}