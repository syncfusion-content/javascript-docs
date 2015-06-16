---
layout: post
title: Accessibility
description: accessibility
platform: js
control: TreeView
documentation: ug
---

# Accessibility

**TreeView** provides full keyboard support. You can interact with the **TreeView** control using the keyboard. It is compatible with the standard keyboard navigation and you can focus on **TreeView** with a predefined Alt and Key combination. Also, you can navigate through the nodes, expand or collapse, select, check and uncheck nodes with the provided shortcut keys. You can access the **TreeView** with the shortcut keys by using the **allowKeyboardNavigation** property.

This feature is mainly useful for all the keyboard users to access the **TreeView** with the keyboard shortcut keys.

The following table showcases the various keyboard shortcuts available in the **TreeView** control. 

_Keyboard Shortcuts_

<table>
<tr>
<td>
<b>Keys </b></td><td>
<b>Functions</b></td></tr>
<tr>
<td>
Alt+j</td><td>
Focuses the control.</td></tr>
<tr>
<td>
F2</td><td>
Edit the selected node. </td></tr>
<tr>
<td>
Ctrl + X</td><td>
Cut the selected node.</td></tr>
<tr>
<td>
Ctrl + C</td><td>
Copy the selected node.</td></tr>
<tr>
<td>
Ctrl + V</td><td>
Paste the cut or copied nodes to selected node.</td></tr>
<tr>
<td>
Delete key</td><td>
Delete the selected node.</td></tr>
<tr>
<td>
Down</td><td>
Selected next node.</td></tr>
<tr>
<td>
Up</td><td>
Selected previous node.</td></tr>
<tr>
<td>
Right</td><td>
Expand selected node. </td></tr>
<tr>
<td>
Left</td><td>
Collapse selected node.</td></tr>
<tr>
<td>
Enter</td><td>
Select node.</td></tr>
<tr>
<td>
Space</td><td>
Toggle Checks and Unchecks.</td></tr>
<tr>
<td>
Home</td><td>
Selected first child node.</td></tr>
<tr>
<td>
End</td><td>
Selected last child node.</td></tr>
</table>


The following steps explain how to enable the **allowKeyboardNavigation** property for **TreeView**.

1. In the **HTML** page, add &lt;ul&gt; and &lt;li&gt; elements to configure TreeView.

{% highlight html %}

<ul id="treeView">
        <li class="expanded">
            Favorites
            <ul>
                <li>Desktop</li>
                <li>Downloads</li>
                <li>Recent places</li>
            </ul>
        </li>
        <li class="expanded">
            Libraries
            <ul>
                <li>
                    Documents
                    <ul>
                        <li>My Documents</li>
                        <li>Public Documents</li>
                    </ul>
                </li>
                <li>
                    Pictures
                    <ul>
                        <li>My Pictures</li>
                        <li>Public Pictures</li>
                    </ul>
                </li>
                <li>
                    Music
                    <ul>
                        <li>My Music</li>
                        <li>Public Music</li>
                    </ul>
                </li>
                <li>Subversion</li>
            </ul>
        </li>
        <li>
            Computer
            <ul>
                <li>Folder(C)</li>
                <li>Folder(D)</li>
                <li>Folder(F)</li>
            </ul>
        </li>
    </ul>

{% endhighlight %}

{% highlight js %}

<script type="text/javascript">
	$(function () {
        $("#treeView").ejTreeView({
            showCheckbox: true,
            allowEditing: true,
            allowKeyboardNavigation:true
        });
        //Control focus key
        $(document).on("keydown", function (e) {
            if (e.altKey && e.keyCode === 74) {
                // j- key code.
                $("#treeView").focus();
            }
        });
    });
</script>

{% endhighlight %}

The output for **TreeView** when **allowKeyboardNavigation** is set to “**True**”.

{% include image.html url="/js/TreeView/Concepts-and-Features/Accessibility_images/Accessibility_img1.png" Caption=""%}

_TreeView with allowKeyboardNavigation_

