---
layout: post
title: Keyboard Support for RichTextEditor widget Syncfusion Essential JS
description: Keyboard Support for RichTextEditor
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
Arrow keys<br/><br/></td><td>
When a toolbar is focused  Move between options in an open drop-down list<br/><br/></td></tr>
<tr>
<td>
Enter<br/><br/></td><td>
Execute the selected button, drop-down item<br/><br/></td></tr>
<tr>
<td>
ESC<br/><br/></td><td>
Cancel an action or close the dialog<br/><br/></td></tr>
<tr>
<td>
HOME <br/><br/>END<br/><br/></td><td>
Go to first/last of the line<br/><br/></td></tr>
<tr>
<td>
CTRL + HOME <br/><br/>CTRL + END<br/><br/></td><td>
Go to the beginning/end of a content<br/><br/></td></tr>
<tr>
<td>
PAGE UP <br/><br/>PAGE DOWN<br/><br/></td><td>
Scroll up/down page in the content<br/><br/></td></tr>
<tr>
<td>
CTRL + A<br/><br/></td><td>
Select all content<br/><br/></td></tr>
<tr>
<td>
CTRL + C<br/><br/></td><td>
Copy the selected text or image<br/><br/></td></tr>
<tr>
<td>
CTRL + X<br/><br/></td><td>
Cut the selected text<br/><br/></td></tr>
<tr>
<td>
CTRL + V<br/><br/></td><td>
Paste text or image<br/><br/></td></tr>
<tr>
<td>
CTRL + Z<br/><br/></td><td>
Undo the last action<br/><br/></td></tr>
<tr>
<td>
CTRL + Y<br/><br/></td><td>
Redo the last action<br/><br/></td></tr>
<tr>
<td>
CTRL + U<br/><br/></td><td>
Make text underline<br/><br/></td></tr>
<tr>
<td>
CTRL  + I<br/><br/></td><td>
Make text italic<br/><br/></td></tr>
<tr>
<td>
CTRL + B<br/><br/></td><td>
Make text bold<br/><br/></td></tr>

To disable the keyboard navigation, set the [allowKeyboardNavigation](http://help.syncfusion.com/js/api/ejrte#members:allowkeyboardnavigation) property of the editor to false (its default value is true). It will disable all the keyboard navigation shortcuts except for the UP/DOWN keys and PAGE UP/PAGE DOWN keys.

{% highlight js %}

$("#texteditor").ejRTE({
        value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
        " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
        allowKeyboardNavigation: false
    });
{% endhighlight %}

