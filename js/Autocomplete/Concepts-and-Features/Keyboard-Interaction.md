---
layout: post
title: Keyboard-Interaction
description: keyboard interaction
platform: js
control: AutoComplete
documentation: ug
---

# Keyboard Interaction

You can use **keyboard** shortcut keys as an alternative to the mouse while using the **AutoComplete** widget. The **AutoComplete** widget allows you to perform all kinds of actions using **keyboard** shortcuts.

_Keyboard shortcut keys_

<table>
<tr>
<td>
<b>Shortcut Key</b></td><td>
<b>Description</b></td></tr>
<tr>
<td>
<a href=http://en.wikipedia.org/wiki/Access_key>Access key</a> + j	</td><td>
Focuses into the AutoComplete text box</td></tr>
<tr>
<td>
Up</td><td>
Moves to previous item in pop up</td></tr>
<tr>
<td>
Down</td><td>
Moves to next item in pop up</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
<tr>
<td>
Esc</td><td>
Closes the popup</td></tr>
</table>

## Configure Keyboard Interaction

The following steps explain how you can enable **keyboard** interaction for an **AutoComplete** textbox.

1. In the **HTML** page, add an **&lt;input&gt;** element to configure the **AutoComplete** widget and enable keyboard interaction by the **accesskey** property.

{% highlight html %}

           <input type="text" id="autocomplete" accesskey="j" />



{% endhighlight %}



2. Render **AutoComplete** control.

{% highlight js %}

<script type="text/javascript">
    $('#autocomplete').ejAutocomplete({
                width: 200,
                dataSource: carList
            });
</script>


{% endhighlight %}



3. Provide **Keyboard** navigation access to **AutoComplete**.

{% highlight js %}

<script type="text/javascript">
    $(function () {
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#autocomplete").focus();
            }
        });
    });
</script>


{% endhighlight %}



4. Run the sample, press **AccessKey + J** to focus in the **AutoComplete** widget and you can navigate using the arrow keys. Use the **Escape** key to close the popup.

{% include image.html url="/js/Autocomplete/Concepts-and-Features/Keyboard-Interaction_images/Keyboard-Interaction_img1.png" Caption=""%}

_AutoComplete focused with keyboard shortcut_

