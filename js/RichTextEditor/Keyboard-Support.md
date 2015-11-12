---
layout: post
title: Keyboard Support for RichTextEditor widget in Syncfusion Essential JS
description: Keyboard navigation Support for RichTextEditor widget
platform: js
control: RTE
documentation: ug

---
# Keyboard Support

The editor has full keyboard accessibility that includes shortcuts to open and other actions with toolbar items, drop-down lists, and dialogs. 

<table>
<tr>
<th>
Press<br/><br/></th><th>
To do this<br/><br/></th></tr>
<tr>
<td>
<kbd>Arrow keys</kbd><br/><br/></td><td>
When a toolbar is focused  Move between options in an open drop-down list<br/><br/></td></tr>
<tr>
<td>
<kbd>Enter</kbd><br/><br/></td><td>
Execute the selected button, drop-down item<br/><br/></td></tr>
<tr>
<td>
<kbd>ESC</kbd><br/><br/></td><td>
Cancel an action or close the dialog<br/><br/></td></tr>
<tr>
<td>
<kbd>HOME</kbd> <br/><br/><kbd>END</kbd><br/><br/></td><td>
Go to first/last of the line<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL<kbd> + <kbd>HOME</kbd> <br/><br/><kbd>CTRL</kbd> + <kbd>END</kbd><br/><br/></td><td>
Go to the beginning/end of a content<br/><br/></td></tr>
<tr>
<td>
<kbd>PAGE UP </kbd><br/><br/><kbd>PAGE DOWN</kbd><br/><br/></td><td>
Scroll up/down page in the content<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>A</kbd><br/><br/></td><td>
Select all content<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>C</kbd><br/><br/></td><td>
Copy the selected text or image<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>X</kbd><br/><br/></td><td>
Cut the selected text<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>V</kbd><br/><br/></td><td>
Paste text or image<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>Z</kbd><br/><br/></td><td>
Undo the last action<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>Y</kbd><br/><br/></td><td>
Redo the last action<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>U</kbd><br/><br/></td><td>
Make text underline<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd>  + <kbd>I</kbd><br/><br/></td><td>
Make text italic<br/><br/></td></tr>
<tr>
<td>
<kbd>CTRL</kbd> + <kbd>B</kbd><br/><br/></td><td>
Make text bold<br/><br/></td></tr></table>

To disable the keyboard navigation, set the [allowKeyboardNavigation](http://help.syncfusion.com/js/api/ejrte#members:allowkeyboardnavigation) property of the editor to false (its default value is true). It will disable all the keyboard navigation shortcuts except for the UP/DOWN keys and PAGE UP/PAGE DOWN keys.

{% highlight js %}

$("#texteditor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
        " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        allowKeyboardNavigation: false
    });
{% endhighlight %}

