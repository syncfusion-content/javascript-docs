---
layout: post
title: How to Syncfusion SpellCheck on typing with time interval? 
description: How to SpellCheck on typing with time interval
platform: js
control: SpellCheck
documentation: ug
api: /api/js/ejspellcheck
---
# How To

## How to SpellCheck on typing with time interval?

SpellCheck control provides option to validate the content with periodic interval once we stopped the typing by using [`enableValidateOnType`](/api/js/ejspellcheck#members:enablevalidateontype) property. 
You can achieved sample side time interval by trigger event of keyup. You can add/update the speed of time for validate on typing in the sample. Here, [`actionSuccess`](/api/js/ejspellcheck#events:actionsuccess) client side event is used to set the cursor position.

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
                spellObj.setCursorPosition(position);
            }
        });
    });
    var position;
    function onValidateTimeDelay() {
        var spellObj = $("#SpellCheck").data("ejSpellCheck");
        var proxy = spellObj;
        if (proxy.setTimeObj != undefined)
            clearInterval(proxy.setTimeObj);
        // 2000 milliseconds is customizable and it’s to wait before executing the code. If omitted, the value 0 is used
        proxy.setTimeObj = setTimeout(function () {
            position = proxy.getCursorPosition();
            proxy.validate();
        }, 2000);
    }
</script>

    
{% endhighlight %}

## How to manually trigger spell check after the spell check dialog has been closed

When a content is validated dynamically through spell check dialog mode, validation classes will not be maintained after the dialog has been closed. To overcome this, validation can be done manually using the dialogClose event of SpellCheck. 

The following code example demonstrates how to trigger spell check manually after the spell check dialog has been closed

{% highlight html %}

     <div class="content-container-fluid">
        <div class="row">
            <div class="cols-sample-area" style="margin-left:50px">
                <div id="TextArea" class="sentence" contenteditable="true" name="sentence">
                    It is a concepts vehicle with Livid Silver body color, 20-inch wheels, fabric folding roof, electrically-controlled hood, 4-cylinder 2.0 TDI engine rated 204 PS (150 kW; 201 hp)
                    and 400  (295.02 lbf ft), diesel particulate filter and Bluetec emission control system, quattro permanent four-wheel drive system,
                    Audi S tronic dual-clutch gearbox, McPherson-strut front axle and a four-link rear axle, Audi drive select system with 3 modes (dynamic, sport, efficiency),
                    MMI control panel with touch pad and dual-view technology, sound system with the prominent extending tweeters.
                </div><br />
                <div>
                    <input type="button" id="SpellCheck"/>
                   <input type="button" id="dialog"/>
                </div>
            </div>
        </div>
      </div>
     <script type="text/javascript">
        $(function () {
            $("#TextArea").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "https://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "https://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                dialogClose: function () {
                    this.validate();
                }
            });
            $("#SpellCheck").ejButton({ width: "200px", height: "25px", click: "showInContextMenu", text: "Spell check" });
            $("#dialog").ejButton({ width: "200px", height: "25px", click: "showDialog", text: "Spell check using Dialog" });
        });
        function showInContextMenu() {
            var spellObj = $("#TextArea").data("ejSpellCheck");
            spellObj.validate();
        }
        function showDialog() {
            var spellChecker = $("#TextArea").data('ejSpellCheck');
            spellChecker.showInDialog();
        }
    </script>

{% endhighlight %}

[Sample](https://jsplayground.syncfusion.com/gq5nodrd)

N> Online services used in dictionarySettings are for demo purpose and own service can be defined in WebApi controller without any connection with outside services. Refer to the [KB](https://www.syncfusion.com/kb/10518/how-to-use-ejspellchecker-in-your-application) for rendering SpellCheck with own WebApi controller 