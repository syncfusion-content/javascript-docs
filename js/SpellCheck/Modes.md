---
title: Syncfusion SpellCheck - Operations
description: SpellCheck Operations
platform: js
control: spellcheck
documentation: ug
keywords: operations, spellcheck modes, dialog mode, context menu mode,  custom menu, handling menu actions, handling dialog actions
api: /api/js/ejspellcheck
---
# SpellCheck Operations

Essential SpellCheck provides two ways to perform the spellcheck operation(error correction). They are,

* Dialog Mode 
* Context Menu Mode  

## Dialog Mode

### Description

SpellCheck provides the dialog mode option to perform the following spellcheck operations.

* Ignore Once
* Ignore All
* Change
* Change All
* Add to Dictionary

### Open Dialog Mode

The following code snippet shows how to open the dialog to spell check the content.

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>
$(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
            });        
            var schObj = $("#SpellCheck").data("ejSpellCheck");
            schObj.showInDialog(); // Open the dialog mode
        });

</script>

{% endhighlight %}

### Handling Dialog Actions

To define the specific actions before the dialog window open, the client-side event [dialogBeforeOpen](/api/js/ejspellcheck#events:dialogbeforeopen) can be used as depicted in the below code example.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                dialogBeforeOpen:"onDialogBeforeOpen"
            });
        });

        function onDialogBeforeOpen(args) {
            if (args.requestType == "dialogBeforeOpen") {
                alert("dialog before open event triggered");
            }
        }

</script>

{% endhighlight %}

The client-side event [dialogOpen](/api/js/ejspellcheck#events:dialogopen) can be used to define the specific actions after the dialog window open as shown in the following code example.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                dialogOpen:"onDialogOpen"
            });
        });

        function onDialogOpen(args) {
            if (args.requestType == "dialogOpen") {
                alert(args.targetText);
            }
        }

</script>

{% endhighlight %}

The following code example used to define some actions after the dialog closing by using the client-side event [dialogClose](/api/js/ejspellcheck#events:dialogclose).

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                dialogClose:"onDialogClose"
            });
        });

        function onDialogClose(args) {
            if (args.requestType == "dialogClose") {
                alert(args.updatedText);
            }
        }

</script>

{% endhighlight %}

It is possible to predict the error word details before starting the spellcheck operations through dialog mode by using the client side event [start](/api/js/ejspellcheck#events:start). The below code example describes the above behavior.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                start:"onSpellCheckStart"
            });
        });

        function onSpellCheckStart(args) {
            if (args.requestType == "spellCheckDialog") {
                alert(args.errorWords);
            }
        }

</script>

{% endhighlight %}

You can get the corrected text content details before updating it into target element with the help of the client side event [complete](/api/js/ejspellcheck#events:complete) as mentioned in the below code example.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                complete:"onCheckComplete"
            });
        });

        function onCheckComplete(args) {
            if (args.requestType == "changeErrorWord") {
                alert(args.targetText);
            }
        }

</script>

{% endhighlight %}

## Context Menu Mode

SpellCheck provides default context menu options to perform the spellcheck operations. It also allows to define additional custom context menu options.

The options that are available under [contextMenuSettings](/api/js/ejspellcheck#members:contextmenusettings) are as follows,

* [**enable**](/api/js/ejspellcheck#members:contextmenusettings-enable) - Enables/disables the context menu option in SpellCheck.
* [**menuItems**](/api/js/ejspellcheck#members:contextmenusettings-menuitems) - Contains the options to perform spellcheck operations.

### Default Menu Options

The menu items contains the following options to perform the spellcheck operation.

* Ignore All
* Add to Dictionary 

The following code snippet shows how to enable the context menu settings in SpellCheck and to make use of it with default available options.

{% highlight html %}
 
<div id="SpellCheck"></div> 
 
<script>

           $("#SpellCheck").ejSpellCheck({
                contextMenuSettings: {
                    enable: true,
                    menuItems: [
                        { id: "IgnoreAll", text: "Ignore All" },
                        { id: "AddToDictionary", text: "Add To Dictionary" }
                    ]
                },
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
</script>

{% endhighlight %}

N> For default menu items, the id must be defined the same as mentioned in the above code example – as we have processed the menus based on this id within our source.

### Custom Menu Options

Apart from the default available options, it is also possible to add custom menu options to the context-menu list.

The following code example depicts how **to add the custom menu items** into the context menu settings.

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
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                }
            });
        });
</script>

{% endhighlight %}

N> The **id** given for the custom menu items **must be unique**.

### Handling Menu Actions

The client-side event [contextClick](/api/js/ejspellcheck#events:contextclick) can be used to define specific actions when a click made on the custom menu items. The following code example describes the above behavior.

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
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                contextClick:"onCustomMenuClick"
            });
        });

        function onCustomMenuClick(args) {
            if (args.selectedOption == "Ignore") {
                alert("Custom menu clicked");
            }
        }

</script>

{% endhighlight %}


It is possible to predict the target (error word) on which the right click is made with the use of the event [contextOpen](/api/js/ejspellcheck#events:contextopen). The below code example shows how to block the display of context menu, when right clicked on the word by setting **args.cancel** as **true**.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({
                contextMenuSettings: {
                    enable: true,
                    menuItems: [
                        { id: "IgnoreAll", text: "Ignore All" },
                        { id: "AddToDictionary", text: "Add To Dictionary" }
                    ]
                },
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                contextOpen:"onBeforeOpen"
            });
        });

        function onBeforeOpen(args) {
            if (args.selectedErrorWord == "Facebook") {
                args.cancel=true;
            }
        }

</script>

{% endhighlight %}

You can get the current spell check operation arguments details with the client-side event [validating](/api/js/ejspellcheck#events:validating). The following code example describes the way to block the ignoreAll operation for the particular word.

{% highlight html %}

<div id="SpellCheck"></div>
    
<script type="text/javascript">
    $(function () {
            $("#SpellCheck").ejSpellCheck({                
                dictionarySettings: {
                    dictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/CheckWords",
                    customDictionaryUrl: "http://js.syncfusion.com/demos/ejservices/api/SpellCheck/AddToDictionary"
                },
                validating:"onSpellChecking"
            });
        });

        function onSpellChecking(args) {
            if (args.requestType == "ignoreAll" && args.ignoreWord=="textarea") {
                args.cancel=true;
            }
        }

</script>

{% endhighlight %}