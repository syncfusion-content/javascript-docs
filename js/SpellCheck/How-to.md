---
title: How-to
description: Customizations in SpellCheck control
platform: js
control: spellcheck
documentation: ug
keywords: target element customizations, target style change
---
# How to

## Target Customization

You can customize the target elements styles (ex: background color, font style) using the “targetUpdating” event. Also, this event will be triggered when spell checking through the dialog mode.

This event is triggered before updating the target text into the SpellCheck dialog content/sentence area. You can apply the target element styles within the targetUpdating event.

The following code example helps you to customize (to highlight the current spell checking target element with the blue background color) the target element style.

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
                controlsToValidate: "control1, control2, control3",
                targetUpdating: function (args) {
                    if (!ej.isNullOrUndefined(args.previousElement))
                        $(args.previousElement)[0].style.background = "white"; // updating the style to the previous target element
                    $(args.currentElement)[0].style.background = "yellow"; // adding the style to the current target element
                },
                complete: function (args) {
                    if (!ej.isNullOrUndefined(args.targetElement))
                        $(args.targetElement)[0].style.background = "white";  // updating the style to the previous target element
                }
            });

        $("#SpellMenu").ejButton({ 
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