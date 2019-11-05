---
title: Syncfusion SpellCheck - Responsive
description: How to set the spellcheck, responsive to screen resolutions
platform: js
control: spellcheck
documentation: ug
keywords: Responsive, Responsive spellcheck dialog, Resize spellcheck dialog
api: /api/js/ejspellcheck
---
# Responsive

The SpellCheck control has support for responsive behavior based on client browser’s width and height. To enable responsive, [isResponsive](/api/js/ejspellcheck#members:isresponsive) property should be true.

The following code example describes the above behavior.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({                
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                isResponsive: true
            });
        });      

</script>

{% endhighlight %}

The dialog of spell check control is rendering based on the client browser’s width and height. Refer to the following code to render the spellcheck dialog control with responsive.

{% highlight html %}

<div id="SpellCheck"></div>

<div>
     <input type="button" id="Spell" />
</div>

<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({                
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                isResponsive: true
            });
    
            $("#Spell").ejButton({
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

Mobile Rendering Screenshot:

![SpellCheck responsive image](Responsive_Images/Responsive_Image.png)