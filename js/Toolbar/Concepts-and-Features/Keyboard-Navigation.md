---
layout: post
title: Keyboard-Navigation
description: keyboard navigation
platform: js
control: Toolbar
documentation: ug
---

# Keyboard Navigation

The entire **Toolbar** commands can be accessed through the keyboard by specifying the **Keyboard Shortcut** listed in the following table.

_Table_ _4__: List of keyboard shortcuts_

<table>
<tr>
<td>
<b>Keyboard Shortcut</b></td><td>
<b>Function</b></td></tr>
<tr>
<td>
Alt + j</td><td>
Focuses the control</td></tr>
<tr>
<td>
UP</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Down</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Left</td><td>
Navigates up and left.</td></tr>
<tr>
<td>
Right</td><td>
Navigates down and right.</td></tr>
<tr>
<td>
Home</td><td>
Navigates to the starting item.</td></tr>
<tr>
<td>
End</td><td>
Navigates to the ending item.</td></tr>
<tr>
<td>
Enter</td><td>
Selects the focused item</td></tr>
</table>


The following code example illustrates shortcuts associated with the **Toolbar** items.



{% highlight js %}

**[HTML]**
<!-- Refer Local Data section for style and data bound for toolbar item -->
**[JS]**
<script type="text/javascript">
    $(function () {
        // declaration
        $("#toolbarcontent").ejToolbar({ width: "290px" });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) { // j- key code.
                $("#toolbarcontent").focus();
            }
        });
    });
</script>


{% endhighlight %}





{% include image.html url="/js/Toolbar/Concepts-and-Features/Keyboard-Navigation_images/Keyboard-Navigation_img1.png" Caption=""%}

_Figure 17: ToolBar control with Keyboard shortcuts_

