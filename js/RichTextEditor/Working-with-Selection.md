# Working with Selection

The editor control provides option to select all the content and in addition to selection of a particular range of content. 

## Select All 

The [selectAll](http://help.syncfusion.com/js/api/ejrte#methods "") method enables you to select the entire content including images in the editor by programmatically.

@Note: the selection highlight is invisible if the editor does not have focus. So, if you want to call the selectAll method, focus the editor before.

{% highlight html %}

<textarea id="texteditor"></textarea>
<button onclick="selectAll()">Select All</button>

<script type="text/javascript">

$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
});

});

function selectAll() {
var editor = $("#texteditor").ejRTE("instance");
editor.selectAll();
}

</script>
{% endhighlight %}

## Select a Range 

You can programmatically select a range of content in the editor using the selectRange method.  To select a range, create a range object with desired offset position and pass it as arguments to selectRange method. The range object is created from createRange method. 

{% highlight html %}

<textarea id="texteditor"></textarea>
<script type="text/javascript">

$(function () {

$("#texteditor").ejRTE({
value: "<ul>" +
"<li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>" +
"<li>Aliquam tincidunt mauris eu risus.</li>" +
"<li>Vestibulum auctor dapibus neque.</li>" +
"</ul>"
});

var editor = $("#texteditor").ejRTE("instance");
range = editor.createRange();
var liTag = document.getElementsByTagName("li");
range.setStart(liTag[2], 3);
range.setEnd(liTag[3], 3);
editor.selectRange(range);
});

</script>
{% endhighlight %}

## Get Selection

The following public methods helps you to retrieve the selected content from the editor:

* **getSelectedText** method is used to get the currently selected content as raw text.
* getSelectedHtml method is used to get the HTML source of currently selected content.

{% highlight html %}

<textarea id="texteditor"></textarea>
<button onclick="getSelection()">get Selection</button>

<script type="text/javascript">

$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
});

});

function getSelection() {
var editor = $("#texteditor").ejRTE("instance");
var selectedText = editor.getSelectedText();
var selectedHtml = editor.getSelectedHtml();
}

</script>
{% endhighlight %}

