# Keyboard Support

The editor has full keyboard accessibility that includes shortcuts to open and other actions with toolbar items, drop-down lists, and dialogs. 

<table>
<tr>
<td>
**Press******<br/><br/></td><td>
**To** **do** **this******<br/><br/></td></tr>
<tr>
<td>
Arrow keys<br/><br/></td><td>
Move between options in an open drop-down list<br/><br/></td></tr>
<tr>
<td>
Enter<br/><br/></td><td>
Execute the selected button, drop-down item<br/><br/></td></tr>
<tr>
<td>
Tab<br/><br/></td><td>
When a toolbar is active, focuses to the next tool<br/><br/></td></tr>
<tr>
<td>
Shift + Tab<br/><br/></td><td>
When a toolbar is active, focuses to the previous tool<br/><br/></td></tr>
<tr>
<td>
SHIFT + F10<br/><br/></td><td>
Open a selected drop-down list<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Open hyperlink dialog<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Remove hyperlink<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Open custom table dialog<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Edit table properties<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Focus the footer<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Focus to HTML view<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Insert or edit image dialog<br/><br/></td></tr>
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
<tr>
<td>
<br/><br/></td><td>
Decrease font size<br/><br/></td></tr>
<tr>
<td>
<br/><br/></td><td>
Increase font size<br/><br/></td></tr>
</table>
To disable the keyboard navigation, set the [allowKeyboardNavigation](http://help.syncfusion.com/js/api/ejrte#members:allowkeyboardnavigation "") property of the editor to false (its default value is true). It will disable all the keyboard navigation shortcuts except for the UP/DOWN keys and PAGE UP/PAGE DOWN keys.

{% highlight html %}

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
allowKeyboardNavigation: false
});
{% endhighlight %}

