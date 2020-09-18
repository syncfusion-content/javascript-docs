---
layout: post
title: Hand written signature | PDF viewer | Javascript | Syncfusion
description: Learn about adding handwritten signatures to the Syncfusion jQuery PDF viewer widget to reduce paper work and more.
platform: js
control: PDF viewer
documentation: ug
keywords: ejPdfViewer, PDF Viewer
api: /api/js/ejpdfviewer
---

# Handwritten Signature

The ejPdfViewer supports  adding handwritten signatures into the PDF document. The handwritten signature reduces the paper work of reviewing the content and verifies it digitally.

The ejPdfViewer control has an option in the [toolbarSettings](https://help.syncfusion.com/api/js/ejpdfviewer#toolbarsettings-object "toolbarSettings property") property to enable or disable the signature button in the default toolbar. 

The following code snippet describes how to disable the signature tool in the widget.

{% highlight javascript %}
$(function () {
    var pdfViewerObject = $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", toolbarSettings: {toolbarItems : ~ej.PdfViewer.ToolbarItems.SignatureTool}});
});
{% endhighlight %}

**Enable or Disable handwritten signature**

The adding of handwritten signature feature in the PDF document can be enabled or disabled using the [enableSignature](https://help.syncfusion.com/api/js/ejpdfviewer#members:enablesignature "enableSignature property") property.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", enableSignature: true });
});
{% endhighlight %}

Providing settings for hand written signature

You can get or set the settings of the handwritten signature using the signatureSettings property. The signatureSettings property is used to set the color and opacity of the hand written signature.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", signatureSettings: { color: “#ff0000”, opacity: “0.5” } });
});
{% endhighlight %}

**Adding signature in the PDF document**

The handwritten signature can be added by drawing the signature content in the signature panel and clicking the button labeled ADD. The following screenshots are the pictorial representation of this.

![Signature panel](Signature_images/Signature_img1.png){:width="624px"}

![Signature draw](Signature_images/Signature_img2.png)

![Signature add](Signature_images/Signature_img3.png)

When the handwritten signature is added in the PDF document, the signatureAdd event will be triggered in the control. The event method can be defined using the [signatureAdd](https://help.syncfusion.com/api/js/ejpdfviewer#signatureadd "signatureAdd Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", signatureAdd: "signatureAdded" });
});
function signatureAdded(args){
    alert("A hand written signature is added in the PDF document”);
}
{% endhighlight %}

**Move, Resize, and Delete the Handwritten Signature**

The handwritten signature content can be moved to the specified location within the page bounds by using touch gestures, arrow keys, and mouse. We can also resize the handwritten signature content by  maintaining the aspect ratio.

When the handwritten signature is resized in the ejPdfViewer control, the signatureResize event will be triggered in the control. The event method can be defined using the [signatureResize](https://help.syncfusion.com/api/js/ejpdfviewer#signatureresize "signatureResize Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", signatureResize: "signatureResize" });
});
function signatureResize(args){
    alert("A hand written signature is resized in the ejPdfViewer control”);
}
{% endhighlight %}

The selected handwritten signature content can be deleted using the “Delete” option in the context menu or delete key. The following screenshots are the pictorial representation of this.

![Signature delete](Signature_images/Signature_img4.png)

When the handwritten signature is deleted from the PDF document, the signatureDelete event will be triggered in the control. The event method can be defined using the [signatureDelete](https://help.syncfusion.com/api/js/ejpdfviewer#signaturedelete "signatureDelete Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", signatureDelete: "signatureDelete" });
});
function signatureDelete(args){
    alert("A hand written signature is removed from the PDF document”);
}
{% endhighlight %}

You can undo and redo the changes made to the handwritten signatures included in the PDF document using the [undo()](https://help.syncfusion.com/api/js/ejpdfviewer#undo "undo method") and the [redo()](https://help.syncfusion.com/api/js/ejpdfviewer#redo "redo method") methods. 

{% highlight javascript %}
function undoChanges() {
    $(“#pdfviewer”).data(“ejPdfViewer”).undo();
}

function redoChanges() {
    $(“#pdfviewer”).data(“ejPdfViewer”).redo();
}
{% endhighlight %}

**Changing properties of handwritten signature**

The properties that is opacity and color of a handwritten signature can be modified by color palate and opacity slider, which is available in the “Properties” option in context menu. The following screenshots are the pictorial representation of this.

![Signature properties](Signature_images/Signature_img5.png)      

Select the desired color from the color palette and then click OK button.

![Signature color palette](Signature_images/Signature_img6.png)  

The selected color will be updated on the signature.

![Signature color](Signature_images/Signature_img7.png)  

You can also change the opacity of the added signature in the "properties" option.

![Signature opacity](Signature_images/Signature_img8.png)

When a property of the handwritten signature is changed in the ejPdfViewer control, the signaturePropertiesChange event will be triggered in the control. The event method can be defined using the [signaturePropertiesChange](https://help.syncfusion.com/api/js/ejpdfviewer#signaturepropertieschange "signaturePropertiesChange Event") property of the control.

{% highlight javascript %}
$(function () {
    $("#container").ejPdfViewer({serviceUrl: "../api/PdfViewerAPI", signaturePropertiesChange: "signaturePropertiesChanged" });
});
function signaturePropertiesChanged(args){
     alert("A property of the hand written signature is changed in the PDF viewer control”);
}
{% endhighlight %}

**Saving the Signature**

The added signature can be saved to the PDF document and can be downloaded by clicking the download button in the toolbar. This action will not affect the original document.

![Signature save](Signature_images/Signature_img9.png) 

**Printing the Signature**

When the print button is clicked in the toolbar, the PDF document will be printed along with the signature added to the pages. This action will not affect the original document.

