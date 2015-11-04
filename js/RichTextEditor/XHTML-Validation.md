---
layout: post
title: XHTML Validation
description: XHTML Validation
platform: js
control: RTE
documentation: ug

---
# XHTML Validation

The editor provides option to validate its content through the [enableXHTML](http://help.syncfusion.com/js/api/ejrte#members:enablexhtml) property. When you set or modify the content into the editor, it continuously checks whether the HTML source of the content that you are creating is valid. The editor examines the HTML markup and then removes the elements or attributes that are not valid. 

{% highlight html %}

<script type="text/javascript">
$(function () {

$("#texteditor").ejRTE({
value: "The RichTextEditor (RTE) control enables you to edit the contents with insert table and images," +
" it also provides a toolbar that helps to apply rich text formats to the content entered in the TextArea.",
enableXHTML: true
});

});
</script>
{% endhighlight %}

The editor checks the following settings on validation:

* **Attributes** 
  * Must be specified in lowercase 
  * Proper use of quotation marks around the attributes
  * Must be valid attributes for corresponding HTML element
  * All the required attributes must be incluced in the HTML element
  * Accepts the allowed values alone such as true or false.
* **HTML** **Elements** 
  * Must be in lowercase 
  * IDs are unique throughout the HTML source of the editor
  * All opening tags must be closed
  * Allows only the valid HTML elements

