---
layout: post
title: Working with content selection in RichTextEditor widget for Syncfusion Essential JS
description: Working with content selection in RichTextEditor widget
platform: js
control: RTE
documentation: ug
keywords: RichTextEditor, Selection, Select a Range
api: /api/js/ejrte
---
# Working with Selection

The editor control provides option to select all the content and in addition to selection of a particular range of content. 

## Select All 

The [selectAll](https://help.syncfusion.com/api/js/ejrte#methods:selectall) method enables you to select the entire content including images in the editor by programmatically.

N> the selection highlight is invisible if the editor does not have focus. So, if you want to call the selectAll method, focus the editor before.

{% highlight html %}

    <textarea id="editor"></textarea>

    <button onclick="selectAll()">Select All</button>

    <script type="text/javascript">

        $(function () {

            $("#editor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });

        });

        function selectAll() {
            var editor = $("#editor").ejRTE("instance");
            editor.selectAll();
        }

    </script>
{% endhighlight %}

## Select a Range 

You can programmatically select a range of content in the editor using the [selectRange](https://help.syncfusion.com/api/js/ejrte#methods:selectRange) method. To select a range, create a
range object with desired offset position and pass it as arguments to the selectRange method.The range object is created from [createRange](https://help.syncfusion.com/api/js/ejrte#methods:createRange) method. The `createRange` returns the new `Range` object. The range can be used to select the content in your editor. 

{% highlight html %}

<textarea id="editor"></textarea>

<script type="text/javascript">

        $(function () {

            $("#editor").ejRTE({
                value: "<ul>" + "<li>Lorem ipsum dolor sit amet, consectetuer adipiscing elit.</li>" + "<li>Aliquam tincidunt mauris eu risus.</li>" + "<li>Vestibulum auctor dapibus neque.</li>" + "</ul>"
            });

            var editor = $("#editor").ejRTE("instance");
            range = editor.createRange();
            var liTag = $(editor.getDocument().body).find("li");        
            if (!editor._isIE8()) {
                range.setStart(liTag[1], 0);
                range.setEnd(liTag[2], 1);
            }
            else {
                range = editor.getDocument().body.createTextRange()
                range.moveToElementText(liTag[2]);
            }
            editor.selectRange(range);
        });

</script>
{% endhighlight %}

## Get Selection

The following public methods helps you to retrieve the selected content from the editor:

* [getText](https://help.syncfusion.com/api/js/ejrte#methods:gettext) method is used to get the currently selected content as raw text.
* [getSelectedHtml](https://help.syncfusion.com/api/js/ejrte#methods:getselectedhtml) method is used to get the HTML source of currently selected content.

{% highlight html %}

    <textarea id="editor"></textarea>

    <button onclick="getSelection()">get Selection</button>

    <script type="text/javascript">

        $(function () {

            $("#editor").ejRTE({
                value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
                " it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
            });

        });

        function getSelection() {
            var editor = $("#editor").ejRTE("instance");
            var selectedText = editor.getText();
            var selectedHtml = editor.getSelectedHtml();
        }

    </script>
{% endhighlight %}

