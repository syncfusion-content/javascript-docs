---
layout: post
title: How to SpellCheck on typing with time interval? 
description: How to SpellCheck on typing with time interval
platform: js
control: SpellCheck
documentation: ug
api: /api/js/ejspellcheck
---
# How To

How to SpellCheck on typing with time interval?

SpellCheck control provides option to validate the content with periodic interval once we stopped the typing. 
You can achieved sample side time interval by trigger event of keyup. You can add/update the speed of time for validate on typing in the sample.

The following code example describes the above behavior.

{% highlight html %}

<div id="SpellCheck" contenteditable="true" onkeyup="onValidateTimeDelay()"></div>
<script type="text/javascript">
    $(function () {
        $("#SpellCheck").ejSpellCheck({
            dictionarySettings: {
                dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
            },
            contextMenuSettings: { enable: true },
            enableValidateOnType: true,
            validating: function (args) {
                // Space key
                if (args.events.keyCode == 32) {
                    args.events.cancelable = false;
                }
                // Enter key
                if (args.events.keyCode == 13) {
                    args.events.cancelable = false;
                }
            },
            actionSuccess: function (args) {
                var spellObj = $("#SpellCheck").data("ejSpellCheck");
                spellObj.setCursorPosition(pos);
            }
        });
    });
    var pos;
    function onValidateTimeDelay() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        var proxy = spellObj;
        if (proxy.setTimeObj != undefined)
            clearInterval(proxy.setTimeObj);
        // 2000 milliseconds is customizable and it’s to wait before executing the code. If omitted, the value 0 is used
        proxy.setTimeObj = setTimeout(function () {
            pos = proxy.getCursorPosition();
            proxy.validate();
        }, 2000);
    }
</script>

    

{% endhighlight %}



